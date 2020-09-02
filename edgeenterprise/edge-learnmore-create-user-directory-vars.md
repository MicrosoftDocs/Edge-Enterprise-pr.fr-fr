---
title: Créer des variables de répertoire de données utilisateur MicrosoftEdge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez comment créer des variables de répertoire de données utilisateur MicrosoftEdge
ms.openlocfilehash: 284bef9156dc3dff1413f349eebe4e7dac854a98
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979807"
---
# Créer des variables de répertoire de données utilisateur MicrosoftEdge

Cet article explique comment vous pouvez utiliser des variables de répertoire de données plutôt que des chemins d’accès codés en dur lors de la modification de MicrosoftEdge.

>[!NOTE]
>Cet article concerne MicrosoftEdge version77 ou ultérieure.

## Variables de chemin d’accès

Stratégies de modification des chemins d’accès aux répertoires de données (par exemple, configuration des variables de prise en charge [UserDataDir](microsoft-edge-policies.md#userdatadir) ou [DownloadDirectory](microsoft-edge-policies.md#downloaddirectory). Lors de la configuration de ces stratégies, vous pouvez utiliser des variables au lieu de chemins d’accès codés en dur. Par exemple, pour stocker vos données de profil sous les données d’application locales de l’utilisateur sur Windows, au lieu de l’emplacement par défaut. Définissez la stratégie [UserDataDir](microsoft-edge-policies.md#userdatadir) sur **${local_app_data}\Edge\Profile**. Sur la plupart des installations de Windows10, la résolution de ce chemin d’accès est *C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\Profile*.

>[!NOTE]
>Si la valeur n’est pas définie, MicrosoftEdge utilise les chemins d’accès aux répertoires par défaut. Un utilisateur peut utiliser l’indicateur de ligne de commande `--user-data-dir` pour remplacer la valeur par défaut.

Pour afficher le **Chemin du profil** actuel, ouvrez la page **À propos de la version** (tapez «edge://version»). Le **Chemin du profil** respect ce format: *C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\User Data\Default*.

### Conseils pour l’utilisation des variables de chemin d’accès

Avant d’utiliser des variables pour les chemins d’accès, consultez les instructions suivantes.

- Toutes les stratégies qui impliquent des chemins dans lesquels MicrosoftEdge stocke des différentes données dépendent de la plateforme. Certaines de ces stratégies sont disponibles uniquement sur des plateformes spécifiques, d’autres peuvent être utilisées sur toutes les plateformes.
- Pour éviter les erreurs causées par des applications démarrant à partir d’emplacements différents à des occasions différentes, assurez-vous que les chemins d’accès sont absolus.
- Chaque variable ne peut être exécutée qu’une seule fois dans un chemin d’accès. La plupart du temps, cette utilisation des variables est la seule qui ait du sens, car elles sont résolues en chemins d’accès absolus.
- Presque toutes les stratégies créent le chemin d’accès s’il n’existe pas (si possible dans les circonstances existantes).
- L’utilisation d’emplacements réseau pour certaines stratégies peut donner des résultats inattendus en raison des différences dans la façon dont les différentes versions/canaux de MicrosoftEdge gèrent la structure de dossiers.

### Variables de chemin d’accès prises en charge

MicrosoftEdge prend en charge les variables de chemin d’accès suivantes.

#### Toutes les plateformes

| Variable | Description |
| --- | --- |
| **${user_name}** | L’utilisateur qui utilise MicrosoftEdge. MicrosoftEdge respecte les SUID (identifiants utilisateur définis du propriétaire au moment de l’exécution ) Exemple: *audreysmall* |
| **${machine_name}** | Nom de l’ordinateur, comprenant éventuellement le nom du domaine. Exemple: *audreysmall* ou *audrey.ex.contoso.com* |

#### Windows uniquement.

| Variable | Description |
| --- | --- |
| **${documents}** | Dossier Documents pour l’utilisateur actuel. Exemple: *C:\Users\Administrator\Documents* |
|**${local_app_data}** | Dossier de données d’application pour l’utilisateur actuel. Exemple: *C:\Users\Administrator\AppData\Local* |
|**${roaming_app_data}** | Dossier de données d’application itinérantes pour l’utilisateur actuel. Exemple: *C:\Users\Administrator\AppData\Roaming* |
| **${profile}** | Dossier de base pour l’utilisateur actuel. Exemple: *C:\Users\Administrator* |
| **${global_app_data}** | Dossier de données d’application à l’échelle du système. Exemple: *C:\AppData* |
| **${program_files}** | Dossier de fichiers de programme pour le processus actuel. Ce dossier varie selon qu’il s’agit d’un processus 32bits ou 64bits. Exemple de résolution: *C:\Program Files (x86)* |
| **${windows}** | Dossier Windows. Exemple: *C:\Windows* |
| **${client_name)** | Nom du PC client connecté à une session RDP ou Citrix. Cette variable est vide si elle est utilisée à partir d’une session locale. Si elle est utilisée dans un chemin d’accès, faites-la précéder d’un élément qui est assuré de ne pas être vide. Exemple: *C:\edge_profiles\session_${client_name}* est résolu en *C:\edge_profiles\session_&lt;ForlocalSessions&gt;* et *C:\edge_profiles\session_&lt;SomePCname&gt;* pour les sessions à distance. |
| **${session_name}** | Nom de la session active. Utilisez ce nom pour distinguer plusieurs sessions à distance connectées simultanément qui utilisent un seul profil utilisateur. Exemple: *WinSta0 pour les sessions de bureau local* |

#### macOS uniquement

| Variable | Description |
| --- | --- |
| **${users}** | Dossier dans lequel sont stockés les profils des utilisateurs. Exemple: */Users* |
| **${documents}** | Dossier Documents pour l’utilisateur actuel. Exemple: */Users/audreysmall/Documents* |

## Licence de contenu

>[!NOTE]
>Certaines parties de cette page sont des modifications basées sur le travail créé et partagé par Chromium.org et utilisé conformément aux conditions décrites dans la [Licence internationale Creative Commons Attribution4.0](http://creativecommons.org/licenses/by/4.0/). La page d’origine est disponible [ici](https://www.chromium.org/administrators/policy-list-3/user-data-directory-variables).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br/>Ce travail est concédé sous une <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licence internationale Creative Commons Attribution4.0</a>.

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)