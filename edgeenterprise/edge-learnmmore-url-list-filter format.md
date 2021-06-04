---
title: Format de filtre pour les stratégies d’URL de MicrosoftEdge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez le format de filtre utilisé pour les stratégies URLBlocklist et URLAllowlist de MicrosoftEdge.
ms.openlocfilehash: 5a0eff1ca7be17fccd1087716d426b13ea302847
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979755"
---
# Format de filtre pour les stratégies basées sur une liste d’URL

Cet article décrit le format de filtre utilisé pour les stratégies basées sur les listes d’URL de MicrosoftEdge (par exemple, [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist) et [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls).

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

##  <a name="the-filter-format"></a>Format de filtre

Le format de filtre est:

```
    [scheme://][.]host[:port][/path][@query]
```

Les champs de format de filtre sont les suivants:

| Champ | Description |
| --- | --- |
| **schéma** (*facultatif*) | Il peut s’agir de http://, https://, ftp://, edge://, etc. |
| **hôte** (*obligatoire*) | Il doit s’agir d’un nom d’hôte ou d’une adresse IP valides, et vous pouvez utiliser un caractère générique («\*»). Pour désactiver la correspondance de sous-domaines, vous pouvez insérer un point facultatif («.») devant l’**hôte**. |
| **port** (*facultatif*) | Les valeurs valides sont comprises entre 1 et 65535. |
| **chemin d’accès** (*facultatif*) | Vous pouvez utiliser n’importe quelle chaîne dans le chemin d’accès. |
| **requête** (*facultatif*) | La **requête** est constituée de jetons de paire clé-valeur ou de clé uniquement séparés par une esperluette («&»). Séparez les jetons de paire clé-valeur par un signe égal («=»). Pour indiquer une correspondance de préfixe, vous pouvez utiliser un astérisque («\*») à la fin de la **requête**. |

##  <a name="comparing-the-filter-format-to-the-url-format"></a>Comparaison du format de filtre au format URL

Le format de filtre ressemble au format d’URL, à l’exception des différences suivantes:

- Si vous incluez «user:pass», il est ignoré. Exemple : http://user:pass@ftp.contoso.com/pub/example.iso.
- Si vous ajoutez un identifiant de fragment («#»), tout ce qui suit l’identifiant est ignoré.
- Vous pouvez utiliser un caractère générique («*») comme **hôte** et le faire précéder d’un point («.»).
- Vous pouvez utiliser une barre oblique («/») ou un point («.») comme suffixe pour l’**hôte**. Dans ce cas, le suffixe est ignoré.

##  <a name="filter-selection-criteria"></a>Critères de sélection du filtre

Le filtre sélectionné pour une URL est la correspondance la plus précise trouvée après le traitement des règles de sélection de filtre suivantes:

1. Les filtres avec l’**hôte** correspondant le plus long sont sélectionnés en premier.
2. À partir des filtres sélectionnés, tout filtre doté d’un schéma ou d’un port ne correspondant pas est ignoré.
3. Dans les filtres restants, le filtre avec le **chemin** correspondant le plus long est sélectionné.
4. Dans les filtres restants, le filtre avec le jeu de jetons de requête le plus long est sélectionné. À cette étape, le filtre de liste verte est prioritaire sur le filtre de liste rouge si les deux filtres ont la même longueur de **chemin d’accès** et le même nombre de jetons de **requête**.
5. S’il ne reste aucun filtre valide, le sous-domaine le plus à gauche est supprimé de l’**hôte** et le processus de sélection reprend à l’étape1. L’ordinateur **hôte** assorti d’un astérisque spécial («*» ) est le dernier recherché, et correspond à tous les ordinateurs hôtes.
6. Si un filtre est disponible, il bloque ou autorise la demande d’URL.

   >[!NOTE]
   >Le comportement par défaut consiste à autoriser la demande d’URL si aucun filtre n’a de correspondance.

##  <a name="example-filter-selection-criteria"></a>Exemple de critère de sélection du filtre

Dans cet exemple, lors de la recherche d’une correspondance à «https://sub.contoso.com/docs», la sélection de filtre effectue les actions suivantes:

1. Rechercher un filtre pour «sub.contoso.com». Si elle trouve un filtre, la recherche passe à l’étape2. Si aucun filtre n’est trouvé, elle effectue une nouvelle tentative avec «contoso.com», «com» et enfin «».
2. Parmi les filtres sélectionnés, tout filtre dont le **schéma** ne contient pas «http» est supprimé.
3. Dans les filtres restants, tous ceux dont le numéro de port exact n’est pas «80» sont supprimés.
4. Dans les filtres restants, tous les éléments qui n’ont pas «/docs" comme préfixe du **chemin d’accès** sont supprimés.
5. Dans les filtres restants, le filtre avec le préfixe de chemin correspondant le plus long est sélectionné et appliqué. Si aucun filtre n’est trouvé, le processus de sélection reprend à l’étape1. Le processus est répété avec le sous-domaine suivant.

###  <a name="additional-filter-information"></a>Informations de filtre complémentaires

Si un filtre a un point («.») comme préfixe de l’**hôte**, seules les correspondances exactes d’**hôte** sont filtrées. Par exemple:

- «contoso.com» (aucun point) correspond à «contoso.com», «www.contoso.com» et «sub.www.contoso.com».
- «.www.contoso.com» (avec un préfixe point) ne correspond qu’à «www.contoso.com».

Vous pouvez utiliser un **schéma** standard ou client. Les schémas standard pris en charge sont les suivants:

- _about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_ et _wss_.

Tout autre **schéma** est traité comme un **schéma**personnalisé, mais seuls les modèles _schema:*_ et _schema://*_ * sont autorisés. Par exemple:

- «custom:*» ou «custom://*» correspondent à «custom:app».
- «custom:app» ou «custom://app» ne sont pas valides.

Le **schéma** et l’**hôte** ne respectent pas la casse. Par exemple:

- Le filtre «http://contoso.com» correspond à «HTTP://contoso.com», «http://contoso.COM» et «http://contoso.com».

Le **chemin** et la **requête** respectent la casse. Par exemple:

- Le filtre «http://contoso.com/path?query=A» ne correspond pas à «http://contoso.com/Path?query=A» ou «http://contoso.com/path?Query=A». Mais il correspond à «http://contoso.COM/path?query=A».

##  <a name="content-license"></a>Licence de contenu

> [!NOTE]
> Certaines parties de cette page sont des modifications basées sur le travail créé et partagé par Chromium.org et utilisé conformément aux conditions décrites dans la [Licence internationale Creative Commons Attribution4.0](http://creativecommons.org/licenses/by/4.0/). La [page Chromium d’origine est disponible ici](https://www.chromium.org/administrators/url-blacklist-filter-format).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Ce travail est concédé sous une <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licence internationale Creative Commons Attribution4.0</a>.

##  <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
