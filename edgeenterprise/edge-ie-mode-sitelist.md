---
title: Stratégie de configuration de site d’entreprise
ms.author: shisub
author: shisub
manager: srugh
ms.date: 03/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Guide pas à pas de la configuration de la liste des sites en mode Entreprise pour le mode Internet Explorer.
ms.openlocfilehash: 1d0b80950439fce77513413c3f5d1143538487d1
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470152"
---
# <a name="enterprise-site-configuration-strategy"></a>Stratégie de configuration de site d’entreprise

Cet article décrit les modifications apportées à la liste des sites en mode Entreprise pour prendre en charge le mode Internet Explorer pour Microsoft Edge version77 et ultérieures.

Pour plus d’informations sur le schéma du fichier XML de liste des sites en mode Entreprise, voir [Guide de schéma Mode Enterprise v.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.
<!--
## Updated schema elements

The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:

| **Element** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | A child element that controls what browser is used for sites. This element is required for sites that need to **open in IE11**.|

**Example:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

The following table shows the possible values of the \<open-in\> element:

| **Value** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Opens the site in IE mode or a full IE11 window. To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Opens the site in a full IE11 window |
| **\<open-in\>MSEdge\</open-in\>** | Opens the site in Microsoft Edge |
| **\<open-in\>None or not specified\</open-in\>** | Opens the site in the default browser or in the browser where the user navigated to the site. |
|**\<open-in\>Configurable\</open-in\>** | Allows the site to participate in IE mode engine determination. To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_. Adding it to the other 'open-in' elements won't change browser behavior.   -->

## <a name="configuration-strategy"></a>Stratégie de configuration

Les étapes suivantes font partie d’une stratégie de configuration de site pour le mode IE :
1. Préparer votre liste des sites
2. Configurer des sites neutres
3. (Facultatif) Utiliser le partage de cookies si nécessaire

<!--
Step 1.  – if you don’t have one use Site Discovery Step-by-Step
Step 2 – Neutral sites + sticky mode
        Use more examples and explain sticky mode better
Step 3 – If that doesn’t cover your needs, then use Cookie sharing -->

## <a name="prepare-your-site-list"></a>Préparer votre liste des sites

Si vous avez déjà une liste des sites en mode Entreprise pour IE11 ou Microsoft Edge Hérité, vous pouvez la réutiliser pour configurer le mode IE.

Toutefois, si vous n’avez pas de liste des sites, vous pouvez utiliser [l’outil de découverte de site d’entreprise](https://docs.microsoft.com/deployedge/edge-ie-mode-site-discovery) pour remplir votre liste des sites.

## <a name="configure-neutral-sites"></a>Configurer des sites neutres

Pour que le mode IE fonctionne correctement, les serveurs d’authentification/authentification unique (SSO) doivent être explicitement configurés en tant que sites neutres. Dans le cas contraire, les pages du mode IE tenteront d’effectuer une redirection vers Microsoft Edge, et l’authentification échouera.

Un site neutre utilise le navigateur dans lequel la navigation a commencé, soit Microsoft Edge, soit le mode IE. La configuration de sites neutres garantit que toutes les applications utilisant ces serveurs d’authentification, modernes et héritées, continuent de fonctionner.

Vous pouvez configurer des sites neutres en paramétrant le menu déroulant *Ouvrir dans* sur «Note»dans l’outil Gestionnaire de liste de sites en mode entreprise ou en mettant directement à jour le fichier XML de liste de sites:

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

Pour identifier les serveurs d’authentification, examinez le trafic réseau d’une application à l’aide des outils de développement IE11. Si vous avez besoin de plus de temps pour identifier vos serveurs d’authentification, vous pouvez configurer une stratégie pour conserver toutes les navigations dans la page en mode IE afin de permettre à vos utilisateurs de poursuivre leurs flux de travail sans interruption. Pour réduire l’utilisation du mode IE lorsque cela est inutile, désactivez ce paramètre une fois que vous avez identifié et ajouté vos serveurs d’authentification à la liste des sites. Pour plus d’informations, voir [Conserver la navigation dans la page en mode IE.](https://docs.microsoft.com/deployedge/edge-learnmore-inpage-nav)

>[!NOTE]
   >Le schéma du mode entreprisev.1 n’est pas pris en charge pour l’intégration du mode IE. Si vous utilisez actuellement le schémav.1 avec Internet Explorer11, vous devez effectuer la mise à niveau vers le schémav.2. Pour plus d’informations, consultez [Recommandations sur le schéma du mode Entreprisev.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

## <a name="optional-use-cookie-sharing-if-necessary"></a>(Facultatif) Utiliser le partage de cookies si nécessaire

Par défaut, les processus Microsoft Edge et Internet Explorer ne partagent pas les cookies de session, et ce manque de partage peut être peu pratique dans certains cas lors de l’utilisation du mode IE. Par exemple, lorsqu’un utilisateur doit s’authentifier à nouveau en mode IE alors qu’auparavant il était habitué à le faire ou lors de la connexion d’une session Microsoft Edge, il ne se déconnecte pas de la session en mode Internet Explorer pour les transactions critiques. Dans ces scénarios, vous pouvez configurer des cookies spécifiques définis par l’authentification unique pour qu’ils soient envoyés de Microsoft Edge à Internet Explorer afin que l’expérience d’authentification devienne plus transparente en éliminant la nécessité de s’authentifier à nouveau. Pour plus d’informations, voir [Partage de cookies de Microsoft Edge vers Internet Explorer](https://docs.microsoft.com/deployedge/edge-ie-mode-add-guidance-cookieshare).

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [À propos du mode Internet Explorer](./edge-ie-mode.md)
- [Informations supplémentaires sur le mode entreprise](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
