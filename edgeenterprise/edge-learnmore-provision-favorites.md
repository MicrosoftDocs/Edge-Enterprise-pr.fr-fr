---
title: Configurer les favoris pour Microsoft Edge
ms.author: capoon
author: dan-wesley
manager: abutcher
ms.date: 09/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer les favoris pour Microsoft Edge
ms.openlocfilehash: 94bd42573bdbc0fd1b971ded1c82e5fe152acc54
ms.sourcegitcommit: 854dd73eb168960c0eb4b483f81a8efe88806a64
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088694"
---
# Configurer les favoris pour Microsoft Edge

Sur la base des commentaires des clients, nous avons apporté des améliorations aux favoris de mise en service. À partir de la version 85 de Microsoft Edge, les administrateurs n’ont plus besoin de créer manuellement un fichier pour configurer les favoris. Les administrateurs peuvent ajouter des favoris et dossiers à l’aide de l’interface utilisateur Microsoft Edge pour générer un fichier qui peut être exporté vers une stratégie de groupe.

Cet article décrit la mise en service d’un ensemble de favoris et de dossiers pour votre organisation. Vous pouvez utiliser la stratégie [configurer les favoris](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#configure-favorites) pour configurer les favoris et les dossiers.

> [!NOTE]
> Cet article concerne Microsoft Edge version 85 ou ultérieure.

## Conditions préalables et recommandations

- Microsoft Edge version 85 avec le modèle d’administration approprié installé pour les stratégies de groupe.
- Nous vous recommandons d’utiliser un nouveau profil dans Microsoft Edge pour configurer ces favoris. Tous les favoris enregistrés avec le profil sont inclus dans l’exportation.  

## Configurer les favoris et les dossiers

Procédez comme suit pour mettre en service vos favoris et dossiers pour vos utilisateurs.

1. Accédez à la barre d’adresse Microsoft Edge et tapez l’URL suivante : *edge://flags/#edge-favorites-admin-export*.
2. Sous **Exporter la configuration des favoris pour les administrateurs**, sélectionnez **Activé** dans la liste déroulante, puis cliquez sur **Redémarrer**.

3. Accédez à la page **Favoris** sur *edge://favorites* pour ajouter les favoris et dossiers que vous voulez configurer.

<!--
4. On the **Favorites bar**, click **Add folder**. The folder structure of favorites that are set in the profile you're using will be reflected in the folder you provision for your users. The next screenshot shows "Managed favorites", the folder we'll use to provision favorites.

   ![Add a folder](media/edge-learnmore-provision-favorites/provision-favorites-add-folder.png)

   > [!TIP]
   > Add existing folders that contain favorites you want to provision for your users.

5. Select "Managed favorites" and then click **Add favorite**. The next screenshot shows the favorite we've added.

   ![Add a favorite](media/edge-learnmore-provision-favorites/provision-favorites-add-favorite.png)-->

4. Lorsque vous avez terminé d’ajouter des favoris et des dossiers, vous pouvez les exporter de sorte qu’ils puissent être utilisés par la stratégie **Configurer les favoris**. Accédez à la barre d’adresses et accédez à *edge://favorites*, cliquez sur les points de suspension « **...** », puis sélectionnez **Exporter la configuration des favoris**. La capture d’écran suivante présente les options qui s’offrent à vous lors de la mise en service des favoris.

   ![Options de menu pour l’utilisation des favoris.](media/edge-learnmore-provision-favorites/provision-favorites-menu-options.png)

5. Sous **Exporter votre configuration de favoris** vous indiquez un nom pour le dossier que vos utilisateurs verront. Tapez le nom du dossier, puis sélectionnez le format de plateforme que vous voulez utiliser. Cliquez sur **Copier dans le Presse-papiers**. La capture d’écran suivante indique « Favoris gérés » pour le nom du dossier et la plateforme est Windows.

   ![Boîte de dialogue pour exporter des favoris vers un dossier Windows.](media/edge-learnmore-provision-favorites/provision-favorites-export.png)

6. Ouvrez l’éditeur de stratégies de groupe, accédez à *Configuration de l’ordinateur/Modèles d’administration/* , puis sélectionnez **Configurer les Favoris**. Activer la stratégie « Configurer les favoris ». Sous **options :**, collez le contenu exporté dans la zone de texte Configurer les favoris, puis cliquez sur **Appliquer**. La capture d’écran suivante montre un exemple de dossier « Favoris gérés » de l’étape 5.

   ![Utilisez gpedit pour activer et configurer la stratégie « Configurer les favoris ».](media/edge-learnmore-provision-favorites/provision-favorites-gpedit.png)

7. Cliquez sur **OK** ou sur **Appliquer** pour sécuriser les paramètres de stratégie.

## Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)