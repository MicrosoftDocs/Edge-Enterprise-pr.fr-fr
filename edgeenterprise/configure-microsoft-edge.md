---
title: Configurer Microsoft Edge pour Windows
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer les paramètres de stratégie Microsoft Edge sur les appareils Windows
ms.openlocfilehash: a5db4352e723539843a5ad80a7b067e670bced5c
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642000"
---
# <a name="configure-microsoft-edge-policy-settings-on-windows"></a>Configurer les paramètres de stratégie Microsoft Edge sur Windows

Utilisez les informations suivantes pour configurer les paramètres de stratégie Microsoft Edge sur vos appareils Windows.

> [!NOTE]
> Cet article concerne Microsoft Edge version 77 ou ultérieure.

## <a name="configure-policy-settings-on-windows"></a>Configurer les paramètres de stratégie sur Windows

Vous pouvez utiliser des _objets de stratégie de groupe_ pour configurer les paramètres de stratégie pour Microsoft Edge et les mises à jour Microsoft Edge gérées sur toutes les versions de Windows. Vous pouvez également configurer une stratégie par le biais du registre pour les appareils Windows qui sont joints à un domaine Microsoft Active Directory ou des instances Windows 10 Professionnel ou Entreprise inscrites pour la gestion des périphériques dans Microsoft Intune. Pour configurer Microsoft Edge avec des objets de stratégie de groupe, vous devez installer des _modèles d’administration_ qui ajoutent des règles et des paramètres pour Microsoft Edge au magasin Central de stratégie de groupe dans votre domaine Active Directory ou au dossier de modèles de définition de stratégie sur des ordinateurs individuels, puis configurer les stratégies spécifiques que vous souhaitez définir.

Vous pouvez utiliser la stratégie de groupe Active Directory pour configurer les paramètres de stratégie Microsoft Edge si vous préférez gérer la stratégie au niveau du domaine. Cela vous permet de gérer globalement les paramètres de stratégie, de cibler différents paramètres de stratégie sur des unités d’organisation spécifiques ou d’utiliser des filtres WMI pour appliquer les paramètres uniquement aux utilisateurs ou aux ordinateurs retournés par une requête particulière. Si vous souhaitez configurer la stratégie sur des ordinateurs individuels, vous pouvez appliquer des paramètres de stratégie qui affectent uniquement le périphérique local à l’aide de l’Éditeur d’objets de stratégie de groupe sur l’ordinateur cible.

Microsoft Edge prend en charge les stratégies _obligatoires_ et _recommandées_. Les stratégies obligatoires remplacent les préférences utilisateur et empêchent l’utilisateur de les modifier. Les stratégies recommandées fournissent un paramètre par défaut qui peut être remplacé par l’utilisateur. La plupart des stratégies sont obligatoires uniquement ; un sous-ensemble est obligatoire et recommandée. Si les deux versions d’une stratégie sont définies, le paramètre obligatoire est prioritaire. Une stratégie recommandée prend effet uniquement lorsque l’utilisateur n’a pas modifié le paramètre.

>[!TIP]
> Vous pouvez utiliser Microsoft Intune pour configurer les paramètres de stratégie Microsoft Edge. Pour plus d’informations, consultez [Configurer Microsoft Edge à l’aide de Microsoft Intune](configure-edge-with-intune.md).

Il existe deux modèles d’administration pour Microsoft Edge, qui peuvent être appliqués au niveau de l’ordinateur ou du domaine Active Directory :

- *msedge. admx* pour [configurer les paramètres de Microsoft Edge](microsoft-edge-policies.md)
- *msedgeupdate. admx* pour [gérer les mises à jour de Microsoft Edge](microsoft-edge-update-policies.md).

Pour commencer, téléchargez et installez le modèle d’administration de Microsoft Edge.

### <a name="1-download-and-install-the-microsoft-edge-administrative-template"></a>1. Télécharger et installer le modèle d’administration de Microsoft Edge

Si vous souhaitez configurer des paramètres de stratégie Microsoft Edge dans Active Directory, téléchargez les fichiers vers un emplacement réseau auquel vous pouvez accéder à partir d’un contrôleur de domaine ou d’une station de travail sur laquelle les Outils d’administration de serveur distant sont installés. Pour effectuer la configuration sur un ordinateur individuel, téléchargez simplement les fichiers sur cet ordinateur.

Lorsque vous ajoutez les fichiers de modèles d’administration à l’emplacement approprié, les paramètres de stratégie Microsoft Edge sont immédiatement disponibles dans l’Éditeur de stratégie de groupe.

Accédez à la [page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise) pour télécharge le fichier de modèle de stratégie Microsoft Edge (*MicrosoftEdgePolicyTemplates.cab*) et extrayez le contenu.

#### <a name="add-the-administrative-template-to-active-directory"></a>Ajouter le modèle d’administration à Active Directory

1. Sur un contrôleur de domaine ou une station de travail sur laquelle sont installés les Outils d’administration de serveur distant, accédez au dossier **PolicyDefinition** (également appelé _magasin central_) sur n’importe quel contrôleur de domaine de votre domaine. Pour les versions antérieures de Windows Server, vous devrez peut-être créer le dossier PolicyDefinition. Pour plus d’informations, consultez le [Guide pratique pour créer et gérer le magasin central pour les modèles d’administration de stratégie de groupe dans Windows](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).
2. Ouvrez *MicrosoftEdgePolicyTemplates* et accédez à **Windows** > **ADMX**.
3. Copiez le fichier *msedge.admx* dans le dossier PolicyDefinition. (Exemple : %systemroot%\sysvol\domain\policies\PolicyDefinitions)
4. Dans le dossier *admx*, ouvrez le dossier de langue approprié. Par exemple, si vous êtes aux États-unis, ouvrez le dossier **en-US**.
5. Copiez le fichier *msedge.adml* dans le dossier de langue correspondant dans le dossier de définition de stratégie. Créez le dossier s’il n’existe pas déjà. (Exemple : %systemroot%\sysvol\domain\policies\PolicyDefinitions\EN-US)
6. Si votre domaine comporte plusieurs contrôleurs de domaine, les nouveaux fichiers ADMX y seront répliqués à l’intervalle de réplication du domaine suivant.
7. Pour vérifier le chargement correct des fichiers, ouvrez l’**Éditeur de gestion des stratégies de groupe** dans les Outils d’administration de Windows et développez **Configuration de l’ordinateur** > **Stratégies** > **Modèles d’administration** > **Microsoft Edge**. Vous devez voir un ou plusieurs nœuds Microsoft Edge, comme illustré ci-dessous.

    ![Stratégies Microsoft Edge](./media/configure-microsoft-edge/edge-gpo-policies.png)

#### <a name="add-the-administrative-template-to-an-individual-computer"></a>Ajouter le modèle d’administration à un ordinateur individuel

1. Sur l’ordinateur cible, ouvrez *MicrosoftEdgePolicyTemplates* et accédez à **Windows** > **ADMX**.
2. Copiez le fichier *msedge.admx* dans le dossier de modèles de définition de stratégie. (Exemple : C:\Windows\PolicyDefinitions)
3. Dans le dossier *admx*, ouvrez le dossier de langue approprié. Par exemple, si vous êtes aux États-unis, ouvrez le dossier **en-US**.
4. Copiez le fichier *msedge.adml* dans le dossier de langue correspondant dans le dossier de définition de stratégie. (Exemple : C:\Windows\PolicyDefinitions\en-US)
5. Pour vérifier que les fichiers sont chargés correctement, ouvrez l’Éditeur d’objets de stratégie de groupe directement (touche Windows + R et entrez gpedit.msc) ou ouvrez MMC et chargez le composant logiciel enfichable Éditeur d’objets de stratégie de groupe. Si une erreur se produit, cela est généralement dû au fait que les fichiers se trouvent dans un emplacement incorrect.

### <a name="2-set-mandatory-or-recommended-policies"></a>2. Définir les stratégies obligatoires ou recommandées

Vous pouvez définir des stratégies obligatoires ou recommandées pour configurer Microsoft Edge avec l’éditeur de stratégie de groupe pour les ordinateurs Active Directory et individuels. Vous pouvez définir le périmètre des paramètres de stratégie sur la **Configuration de l’ordinateur** ou la **Configuration de l’utilisateur** en sélectionnant le nœud approprié comme décrit ci-dessous.

- Pour configurer une stratégie obligatoire, ouvrez l’Éditeur de stratégie de groupe et accédez à (**Configuration de l’ordinateur** ou **Configuration de l’utilisateur**) > **Stratégies** > **Modèles d’administration** > **Microsoft Edge**.
- Pour configurer une stratégie recommandée, ouvrez l’Éditeur de stratégie de groupe et accédez à (**Configuration de l’ordinateur** ou **Configuration de l’utilisateur**) > **Stratégies** > **Modèles d’administration** > **Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent remplacer)**.

  ![Ouvrir l’Éditeur de stratégie de groupe](./media/configure-microsoft-edge/edge-ad-policy.png)

### <a name="3-test-your-policies"></a>3. Tester votre déploiement

Sur un périphérique client cible, ouvrez Microsoft Edge et accédez à **edge://policy** pour afficher toutes les stratégies qui sont appliquées. Si vous avez appliqué des paramètres de stratégie sur l’ordinateur local, les stratégies doivent apparaître immédiatement. Vous devrez peut-être fermer et rouvrir Microsoft Edge s’il était ouvert pendant la configuration des paramètres de stratégie.

![Afficher les stratégies configurées dans le navigateur](./media/configure-microsoft-edge/edge-gpEdit.png)

Pour les paramètres de stratégie de groupe Active Directory, les paramètres de stratégie sont propagés vers les ordinateurs du domaine à un intervalle régulier défini par votre administrateur de domaine et les ordinateurs cibles peuvent ne pas recevoir immédiatement les mises à jour des stratégies. Pour actualiser manuellement les paramètres de stratégie de groupe Active Directory sur un ordinateur cible, exécutez la commande suivante à partir d’une invite de commandes ou d’une session PowerShell sur l’ordinateur cible :

``` powershell
gpupdate /force
```

Vous devrez peut-être fermer et rouvrir Microsoft Edge pour que les nouvelles stratégies s’affichent.

Vous pouvez également utiliser REGEDIT.exe sur un ordinateur cible pour afficher les paramètres du registre qui stockent les paramètres de stratégie de groupe. Ces paramètres se trouvent dans le chemin d’accès **HKLM\SOFTWARE\Policies\Microsoft\Edge**.

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Configurer pour Windows avec Intune](configure-edge-with-intune.md)
- [Configurer pour macOS](configure-microsoft-edge-on-mac.md)
- [Parcourir les stratégies d’entreprise Microsoft Edge](microsoft-edge-policies.md)


