---
title: Configurer Microsoft Edge pour Windows
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 10/09/2019
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer les paramètres de stratégie MicrosoftEdge sur les appareils Windows
ms.openlocfilehash: 99aaf002f868ce29e81aa40024fa1de2e83d76e1
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979663"
---
# Configurer les paramètres de stratégie MicrosoftEdge sur Windows

Utilisez les informations suivantes pour configurer les paramètres de stratégie MicrosoftEdge sur vos appareils Windows.

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

## Configurer les paramètres de stratégie sur Windows

Vous pouvez utiliser des _objets de stratégie de groupe_ pour configurer les paramètres de stratégie pour MicrosoftEdge et les mises à jour MicrosoftEdge gérées sur toutes les versions de Windows. Vous pouvez également configurer une stratégie par le biais du registre pour les appareils Windows qui sont joints à un domaine MicrosoftActiveDirectory ou des instances Windows10 Professionnel ou Entreprise inscrites pour la gestion des périphériques dans MicrosoftIntune. Pour configurer MicrosoftEdge avec des objets de stratégie de groupe, vous devez installer des _modèles d’administration_ qui ajoutent des règles et des paramètres pour MicrosoftEdge au magasin Central de stratégie de groupe dans votre domaine ActiveDirectory ou au dossier de modèles de définition de stratégie sur des ordinateurs individuels, puis configurer les stratégies spécifiques que vous souhaitez définir.

Vous pouvez utiliser la stratégie de groupe ActiveDirectory pour configurer les paramètres de stratégie MicrosoftEdge si vous préférez gérer la stratégie au niveau du domaine. Cela vous permet de gérer globalement les paramètres de stratégie, de cibler différents paramètres de stratégie sur des unités d’organisation spécifiques ou d’utiliser des filtres WMI pour appliquer les paramètres uniquement aux utilisateurs ou aux ordinateurs retournés par une requête particulière. Si vous souhaitez configurer la stratégie sur des ordinateurs individuels, vous pouvez appliquer des paramètres de stratégie qui affectent uniquement le périphérique local à l’aide de l’Éditeur d’objets de stratégie de groupe sur l’ordinateur cible.

MicrosoftEdge prend en charge les stratégies _obligatoires_ et _recommandées_. Les stratégies obligatoires remplacent les préférences utilisateur et empêchent l’utilisateur de les modifier. Les stratégies recommandées fournissent un paramètre par défaut qui peut être remplacé par l’utilisateur. La plupart des stratégies sont obligatoires uniquement; un sous-ensemble est obligatoire et recommandée. Si les deux versions d’une stratégie sont définies, le paramètre obligatoire est prioritaire.

>[!TIP]
> Vous pouvez utiliser Microsoft Intune pour configurer les paramètres de stratégie MicrosoftEdge. Pour plus d’informations, consultez [Configurer MicrosoftEdge à l’aide de Microsoft Intune](configure-edge-with-intune.md).

Il existe deux modèles d’administration pour MicrosoftEdge, qui peuvent être appliqués au niveau de l’ordinateur ou du domaine ActiveDirectory:

- *msedge. admx* pour [configurer les paramètres de MicrosoftEdge](microsoft-edge-policies.md)
- *msedgeupdate. admx* pour [gérer les mises à jour de MicrosoftEdge](microsoft-edge-update-policies.md).

Pour commencer, téléchargez et installez le modèle d’administration de MicrosoftEdge.

### 1. Télécharger et installer le modèle d’administration de MicrosoftEdge

Si vous souhaitez configurer des paramètres de stratégie MicrosoftEdge dans ActiveDirectory, téléchargez les fichiers vers un emplacement réseau auquel vous pouvez accéder à partir d’un contrôleur de domaine ou d’une station de travail sur laquelle les Outils d’administration de serveur distant sont installés. Pour effectuer la configuration sur un ordinateur individuel, téléchargez simplement les fichiers sur cet ordinateur.

Lorsque vous ajoutez les fichiers de modèles d’administration à l’emplacement approprié, les paramètres de stratégie MicrosoftEdge sont immédiatement disponibles dans l’Éditeur de stratégie de groupe.

Accédez à la [page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise) pour télécharge le fichier de modèle de stratégie Microsoft Edge (*MicrosoftEdgePolicyTemplates.cab*) et extrayez le contenu.

#### Ajouter le modèle d’administration à ActiveDirectory

1. Sur un contrôleur de domaine ou une station de travail sur laquelle sont installés les Outils d’administration de serveur distant, accédez au dossier **PolicyDefinition** (également appelé _magasin central_) sur n’importe quel contrôleur de domaine de votre domaine. Pour les versions antérieures de Windows Server, vous devrez peut-être créer le dossier PolicyDefinition. Pour plus d’informations, consultez le [Guide pratique pour créer et gérer le magasin central pour les modèles d’administration de stratégie de groupe dans Windows](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).
1. Ouvrez *MicrosoftEdgePolicyTemplates* et accédez à **Windows** > **ADMX**.
1. Copiez le fichier *msedge.admx* dans le dossier PolicyDefinition. (Exemple: %systemroot%\sysvol\domain\policies\PolicyDefinitions)
1. Dans le dossier *admx*, ouvrez le dossier de langue approprié. Par exemple, si vous êtes aux États-unis, ouvrez le dossier **en-US**.
1. Copiez le fichier *msedge.adml* dans le dossier de langue correspondant dans le dossier de définition de stratégie. Créez le dossier s’il n’existe pas déjà. (Exemple: %systemroot%\sysvol\domain\policies\PolicyDefinitions\EN-US)
1. Si votre domaine comporte plusieurs contrôleurs de domaine, les nouveaux fichiers ADMX y seront répliqués à l’intervalle de réplication du domaine suivant.
1. Pour vérifier le chargement correct des fichiers, ouvrez l’**Éditeur de gestion des stratégies de groupe** dans les Outils d’administration de Windows et développez **Configuration de l’ordinateur** > **Stratégies** > **Modèles d’administration** > **Microsoft Edge**. Vous devez voir un ou plusieurs nœuds MicrosoftEdge, comme illustré ci-dessous.

    ![Stratégies Microsoft Edge](./media/configure-microsoft-edge/edge-gpo-policies.png)

#### Ajouter le modèle d’administration à un ordinateur individuel

1. Sur l’ordinateur cible, ouvrez *MicrosoftEdgePolicyTemplates* et accédez à **Windows** > **ADMX**.
2. Copiez le fichier *msedge.admx* dans le dossier de modèles de définition de stratégie. (Exemple: C:\Windows\PolicyDefinitions)
3. Dans le dossier *admx*, ouvrez le dossier de langue approprié. Par exemple, si vous êtes aux États-unis, ouvrez le dossier **en-US**.
4. Copiez le fichier *msedge.adml* dans le dossier de langue correspondant dans le dossier de définition de stratégie. (Exemple: C:\Windows\PolicyDefinitions\en-US)
5. Pour vérifier que les fichiers sont chargés correctement, ouvrez l’Éditeur d’objets de stratégie de groupe directement (touche Windows + R et entrez gpedit.msc) ou ouvrez MMC et chargez le composant logiciel enfichable Éditeur d’objets de stratégie de groupe. Si une erreur se produit, cela est généralement dû au fait que les fichiers se trouvent dans un emplacement incorrect.

<!--
To add the administrative template to manage Microsoft Edge updates:

1. Open the *MicrosoftEdgePolicyTemplates* file and go to **windows** > **admx**.
2. Copy the *msedgeupdate.admx* file to your Policy Definition template folder. (Example: C:\Windows\PolicyDefinitions)
3. In the *updatepolicies* folder, open the appropriate language folder. For example, if you’re in Germany, open the **de-DE** folder.
4. Copy the *msedgeupdate.adml* file to the matching language folder in your Policy Definition folder. (Example: C:\Windows\PolicyDefinitions\de-DE)
5. Open MMC and load the Local Group Policy Editor snap-in to confirm the files loaded correctly. If an error occurs, it’s usually because the files are in an incorrect location.

> [!NOTE]
> Currently the Microsoft Edge update policies are only localized in en-US. Additional language support will be added in a future release.
-->

### 2. Définir les stratégies obligatoires ou recommandées

Vous pouvez définir des stratégies obligatoires ou recommandées pour configurer MicrosoftEdge avec l’éditeur de stratégie de groupe pour les ordinateurs ActiveDirectory et individuels. Vous pouvez définir le périmètre des paramètres de stratégie sur la **Configuration de l’ordinateur** ou la **Configuration de l’utilisateur** en sélectionnant le nœud approprié comme décrit ci-dessous.

- Pour configurer une stratégie obligatoire, ouvrez l’Éditeur de stratégie de groupe et accédez à (**Configuration de l’ordinateur** ou **Configuration de l’utilisateur**) > **Stratégies** > **Modèles d’administration** > **Microsoft Edge**.
- Pour configurer une stratégie recommandée, ouvrez l’Éditeur de stratégie de groupe et accédez à (**Configuration de l’ordinateur** ou **Configuration de l’utilisateur**) > **Stratégies** > **Modèles d’administration** > **Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent remplacer)**.

  ![Ouvrir l’Éditeur de stratégie de groupe](./media/configure-microsoft-edge/edge-ad-policy.png)

### 3. Tester votre déploiement

Sur un périphérique client cible, ouvrez MicrosoftEdge et accédez à **edge://policy** pour afficher toutes les stratégies qui sont appliquées. Si vous avez appliqué des paramètres de stratégie sur l’ordinateur local, les stratégies doivent apparaître immédiatement. Vous devrez peut-être fermer et rouvrir MicrosoftEdge s’il était ouvert pendant la configuration des paramètres de stratégie.

![Afficher les stratégies configurées dans le navigateur](./media/configure-microsoft-edge/edge-gpEdit.png)

Pour les paramètres de stratégie de groupe ActiveDirectory, les paramètres de stratégie sont propagés vers les ordinateurs du domaine à un intervalle régulier défini par votre administrateur de domaine et les ordinateurs cibles peuvent ne pas recevoir immédiatement les mises à jour des stratégies. Pour actualiser manuellement les paramètres de stratégie de groupe ActiveDirectory sur un ordinateur cible, exécutez la commande suivante à partir d’une invite de commandes ou d’une session PowerShell sur l’ordinateur cible:

``` powershell
gpupdate /force
```

Vous devrez peut-être fermer et rouvrir MicrosoftEdge pour que les nouvelles stratégies s’affichent.

Vous pouvez également utiliser REGEDIT.exe sur un ordinateur cible pour afficher les paramètres du registre qui stockent les paramètres de stratégie de groupe. Ces paramètres se trouvent dans le chemin d’accès **HKLM\SOFTWARE\Policies\Microsoft\Edge**.

## Forum aux questions

### MicrosoftEdge peut-il être configuré pour utiliser les préférences principales?

Oui, vous pouvez configurer MicrosoftEdge pour qu’il utilise un fichier de préférences principales.

 Un fichier de préférences principales vous permet de configurer les paramètres par défaut lors du déploiement de MicrosoftEdge. Vous pouvez également utiliser un fichier de préférences principales pour appliquer des paramètres sur des ordinateurs qui ne sont pas gérés par un système de gestion des périphériques. Ces paramètres sont appliqués au profil de l’utilisateur la première fois que l’utilisateur exécute le navigateur. Une fois que l’utilisateur a exécuté le navigateur, les modifications apportées au fichier de préférences principales ne sont pas appliquées. Un utilisateur peut modifier les paramètres à partir des préférences principales dans le navigateur. Si vous souhaitez rendre un paramètre obligatoire ou modifier un paramètre après la première exécution du navigateur, vous devez utiliser une stratégie.

Un fichier de préférences principales vous permet de personnaliser de nombreux paramètres et préférences pour le navigateur, y compris ceux partagés avec d’autres navigateurs basés Chromium et spécifiques à MicrosoftEdge.  Les préférences liées à la stratégie peuvent être configurées à l’aide du fichier de préférences principales. Dans les cas où une stratégie est définie et qu’un jeu de préférences principales correspondant est défini, le paramètre de stratégie est prioritaire.

> [!IMPORTANT]
> Toutes les préférences disponibles peuvent ne pas être cohérentes avec la terminologie et les conventions d’affectation de noms de MicrosoftEdge.  Il n’est pas garanti que ces préférences continuent de fonctionner comme prévu dans les prochaines versions. Les préférences peuvent être modifiées ou ignorées dans les versions ultérieures.

Un fichier de préférences principales est un fichier texte mis en forme à l’aide du balisage JSON. Ce fichier doit être ajouté au même répertoire que le msedge.exe exécutable. Pour les déploiements à l’échelle du système sur Windows, il s’agit généralement de: *Windows: C:\Program Files\Microsoft\Edge\Application\master_preferences*.

## Articles associés

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Configurer pour Windows avec Intune](configure-edge-with-intune.md)
- [Configurer pour macOS](configure-microsoft-edge-on-mac.md)
- [Parcourir les stratégies d’entreprise MicrosoftEdge](microsoft-edge-policies.md)


