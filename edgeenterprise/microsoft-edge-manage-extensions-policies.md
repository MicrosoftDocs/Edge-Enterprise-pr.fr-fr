---
title: Utiliser des stratégies de groupe pour gérer les extensions MicrosoftEdge
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Utiliser des stratégies de groupe pour gérer les extensions MicrosoftEdge dans l’entreprise
ms.openlocfilehash: a633b036c1733716dfb257b4711bca57bd6721f0
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618102"
---
# <a name="use-group-policies-to-manage-microsoft-edge-extensions"></a>Utiliser des stratégies de groupe pour gérer les extensions MicrosoftEdge

Cet article décrit les options et les étapes de gestion des extensions à l’aide de stratégies de groupe. Ces options supposent que vous avez déjà MicrosoftEdge géré pour vos utilisateurs. Si vous n’avez pas encore configuré la gestion de MicrosoftEdge par vos utilisateurs, suivez le lien ci-dessous pour le faire maintenant.

- [Gérer les extensions MicrosoftEdge dans l’entreprise](/deployedge/microsoft-edge-manage-extensions)

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

## <a name="block-extensions-based-on-their-permissions"></a>Bloquer les extensions en fonction de leurs autorisations

Vous pouvez contrôler les extensions que vos utilisateurs peuvent installer en fonction des autorisations à l’aide de la [stratégie ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings). Si une extension installée a besoin d’une autorisation bloquée, elle ne s’exécute pas. L’extension n’est pas supprimée, mais simplement désactivée.

> [!NOTE]
> Le paramètre d’autorisations bloquées peut uniquement être définie dans la stratégie de paramètres d’extension.  

Utilisez les étapes suivantes comme guide pour bloquer une extension.

1. Ouvrez l’éditeur de gestion des stratégies de groupe et sélectionnez **Modèles d’administration > Microsoft Edge > Extensions**, puis sélectionnez **Configurer les paramètres de gestion des extensions**.
2. Activez la stratégie, puis entrez les autorisations que vous souhaitez autoriser ou bloquer, à l’aide d’une chaîne JSON qui est compressée. La capture d’écran suivante montre comment bloquer une extension qui utilise l’autorisation «usb».

    :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-1.png" alt-text="Configurez la stratégie de groupe pour bloquer une extension.":::

L’exemple suivant montre le JSON pour bloquer toute extension qui nécessite l’utilisation de l’autorisation «usb» et de sa chaîne compressée.

### <a name="json-example"></a>Exemple JSON

   ```json
   { 
        "*": { 
             "blocked_permissions": ["usb"] 
        } 
   } 
   ```

   ```json
   {"*":{"blocked_permissions":["usb"]}} 
   ```

   > [!NOTE]
   > Pour bloquer toutes les extensions qui utilisent l’autorisation, utilisez un astérisque pour l’ID d’extension, comme illustré dans l’exemple précédent. Si vous spécifiez un ID d’extension, la stratégie s’applique uniquement à cette extension. Vous pouvez en bloquer plusieurs, mais il doit s’y trouver des entrées distinctes.

## <a name="prevent-extensions-from-altering-web-pages"></a>Empêcher les extensions de modifier les pages web

Ce paramètre empêche les extensions de lire et de modifier des données provenant de sites web et de domaines sensibles. Le blocage des actions indésirables s’effectuera en bloquant des actions telles que l’injection de scripts dans vos sites web, la lecture des cookies ou les modifications de demande web. Ce paramètre n’empêche pas vos utilisateurs d’installer ou de supprimer des extensions, il empêche uniquement les extensions de modifier les sites web spécifiés. 
  
> [!NOTE]
> Le paramètre Hôtes autorisés/bloqués runtime peut uniquement être défini dans la stratégie de paramètres d’extension.  

Vous pouvez configurer les paramètres suivants dans la stratégie ExtensionSettings pour empêcher (ou autoriser) les modifications de sites web ou de domaines:

- **Runtime_blocked_hosts**. Ce paramètre empêche les extensions d’apporter des modifications ou de lire des données à partir des sites web que vous spécifiez.
- **Runtime_allowed_hosts**. Ce paramètre permet aux extensions d’apporter des modifications ou de lire des données à partir des sites web que vous spécifiez. Le format suivant est utilisé pour spécifier vos sites dans la chaîne JSON de la stratégie:

  ```json
  [http|https|ftp|*]://[subdomain|*].[hostname|*].[eTLD|*] [http|https|ftp|*],
  ```

  > [!NOTE]
  > `[hostname|*], and [eTLD|*]` les sections sont obligatoires, mais la section `[subdomain|*]` est facultative.

Le tableau suivant présente des exemples de modèles d’hôte valides et de modèles correspondants.

|Modèles d’hôte valides|Correspond|Ne correspond pas|
|--|--|--|
|  `*://*.example.*` | `http://example.com`<br>`https://test.example.co.uk`   | `https://example.microsoft.com`<br>`http://example.microsoft.co.uk`  |
| `http://example.*` | `http://example.com`<br>`http://example.ly` | `https://example.com`<br>`http://test.example.com`   |
| `http://example.com`   | `http://example.com` | `https://example.com`<br>`http://test.example.co.uk` |
| `*://*`   | Toutes les URL  |   |

Utilisez les étapes suivantes comme guide pour bloquer ou autoriser les extensions à accéder à un site web ou un domaine.

1. Ouvrez l’éditeur de gestion des stratégies de groupe et sélectionnez **Modèles d’administration > Microsoft Edge > Extensions**, puis sélectionnez **Configurer les paramètres de gestion des extensions**.  
2. Activez la stratégie, puis entrez les autorisations que vous souhaitez autoriser ou bloquer, en compressant les autorisations sur une seule chaîne JSON.

Les exemples suivants montrent comment bloquer des extensions sur un nom d’hôte et comment bloquer des extensions sur le même domaine.

### <a name="json-example-to-block-hostname"></a>Exemple JSON pour bloquer le nom d’hôte

Cet exemple illustre le JSON et la chaîne JSON compressée pour empêcher toute extension d’accéder au nom d’hôte `www.microsoft.com`.

```json
{ 
    "*":{ 
            "runtime_blocked_hosts":["www.microsoft.com"] 
    } 
} 
```

```json
{"*":{"runtime_blocked_hosts":["www.microsoft.com"]}} 
```

> [!NOTE]
> Pour empêcher toutes les extensions d’accéder à une page web, utilisez un astérisque pour l’ID d’extension, comme illustré dans l’exemple précédent.  Si vous spécifiez un ID d’extension au lieu d’un astérisque, la stratégie s’applique uniquement à cette extension. Vous pouvez bloquer plusieurs extensions, mais elles doivent être des entrées distinctes.

### <a name="json-example-to-block-extensions-on-same-domain"></a>Exemple JSON pour bloquer les extensions sur le même domaine

Cet exemple montre la chaîne JSON et JSON compressée pour empêcher l’exécution d’extensions spécifiques sur le même domaine, «importantwebsite».

```json
{ 
    "aapbdbdomjkkjkaonfhkkikfgjllcleb": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    }, 
    "bfbmjmiodbnnpllbbbfblcplfjjepjdn": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    } 
} 
```

```json
{"aapbdbdomjkkjkaonfhkkikfgjllcleb": {"runtime_blocked_hosts": ["*://,*.importantwebsite"]},"bfbmjmiodbnnpllbbbfblcplfjjepjdn": {"runtime_blocked_hosts": ["*://*.importantwebsite"]}} 
```

## <a name="allow-or-block-extensions-in-group-policy"></a>Autoriser ou bloquer les extensions dans la stratégie de groupe

Vous pouvez utiliser les stratégies [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist) et [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist) pour contrôler les extensions bloquées ou autorisées. Utilisez les étapes suivantes comme guide pour autoriser toutes les extensions à l’exception de celles que vous souhaitez bloquer.

1. Ouvrez l’éditeur de gestion des stratégies de groupe et sélectionnez Modèles d’administration **> Microsoft Edge > Extensions >**, puis sélectionnez **Contrôler les extensions qui ne peuvent pas être installées**.
2. Sélectionnez **Activé**.
3. Cliquez sur **Afficher**.
4. Entrez l’ID d’application des extensions que vous souhaitez bloquer. Lorsque vous ajoutez plusieurs ID d’application, utilisez une ligne distincte pour chaque ID.
5. Pour bloquer toutes les extensions, tapez **\*** dans la stratégie pour empêcher l’installation des extensions. Vous pouvez l’utiliser conjointement avec la stratégie «Autoriser l’installation d’extensions spécifiques» pour autoriser uniquement l’installation de certaines extensions. La capture d’écran suivante montre une extension qui sera bloquée en fonction de l’ID d’application fourni.

   :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-2.png" alt-text="Utilisez l’ID d’application pour bloquer une extension.":::

   > [!TIP]
   > Si vous ne trouvez pas l’ID d’application d’une extension, reportez-vous à l’extension sur le site web des modules complémentaires MicrosoftEdge. Recherchez l’extension spécifique et l’ID de l’application s’affichera à la fin de l’URL dans l’omnibox.

> [!NOTE]
> Vous pouvez ajouter une extension à la liste de blocage déjà installée sur l’ordinateur d’un utilisateur. Cela désactive l’extension et empêche l’utilisateur de la réactiver. Elle ne sera pas désinstallée, mais simplement désactivée.

## <a name="force-install-an-extension"></a>Forcer l’installation d’une extension

Utilisez la [stratégie ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) pour contrôler les extensions bloquées ou autorisées. Utilisez les étapes suivantes comme guide pour forcer l’installation d’une extension.

1. Dans l’Éditeur de stratégie de groupe, sélectionnez **Modèles d’administration> Microsoft Edge > Extensions >**, puis sélectionnez **Contrôler les extensions installées en mode silencieux**.
2. Sélectionnez **Activé**.  
3. Cliquez sur **Afficher**.
4. Entrez l’ID d’application ou les ID de l’extension ou des extensions pour lesquelles vous souhaitez forcer l’installation.  

L’extension sera installée sans intervention de l’utilisateur. L’utilisateur ne peut pas non plus désinstaller ou désactiver l’extension. Ce paramètre remplace toute stratégie de liste de blocage activée.

> [!NOTE]
> Pour les extensions hébergées dans le Chrome Web Store, utilisez une chaîne telle que: `pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`.

## <a name="block-extensions-from-a-specific-store-or-update-url"></a>Bloquer les extensions à partir d’une URL de mise à jour ou de magasin spécifique

Pour bloquer les extensions d’un magasin ou d’une URL spécifique, vous devez uniquement bloquer la stratégie *update_url* pour ce magasin à l’aide de la stratégie [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings).

Utilisez les étapes suivantes comme guide pour bloquer les extensions à partir d’un magasin ou d’une URL spécifique.

1. Ouvrez l’éditeur de gestion des stratégies de groupe et sélectionnez **Modèles d’administration > Microsoft Edge > Extensions >**, puis sélectionnez **Configurer les paramètres de gestion des extensions**.  
2. Activez la stratégie, puis entrez les autorisations que vous souhaitez autoriser ou bloquer, en la compressant en une seule chaîne JSON.

L’exemple suivant montre JSON et la chaîne JSON compressée à bloquer à partir du Chrome Web Store à l’aide de son URL de mise à jour (`https://clients2.google.com/service/update2/crx`).

### <a name="json-example-for-blocking-on-update-url"></a>Exemple JSON pour le blocage sur l’URL de mise à jour

```json
{ 
"update_url:https://clients2.google.com/service/update2/crx":{ 
                                                             " installation_mode":"blocked" 
                                                             } 
} 
```

```json
{"update_url:https://clients2.google.com/service/update2/crx":{"installation_mode":"blocked"}} 
```

> [!NOTE]
> Vous pouvez toujours utiliser **ExtensionInstallForceList** et **ExtensionInstallAllowList** pour autoriser/forcer l’installation d’extensions spécifiques, même si le magasin est bloqué à l’aide du JSON dans l’exemple précédent.

## <a name="see-also"></a>Voir également

- [Gérer les extensions MicrosoftEdge dans l’entreprise](microsoft-edge-manage-extensions.md)
- [Créer un magasin web pour héberger les extensions MicrosoftEdge](microsoft-edge-manage-extensions-webstore.md)
- [Guide de référence pour la stratégie ExtensionSettings](microsoft-edge-manage-extensions-ref-guide.md)
- [FAQ sur les extensions Microsoft Edge](microsoft-edge-manage-extensions-faq.md)
- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
