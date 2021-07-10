---
title: Configurer les favoris pour Microsoft Edge
ms.author: capoon
author: dan-wesley
manager: abutcher
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Configurer les favoris pour Microsoft Edge
ms.openlocfilehash: 2d75e9c22a8aa9cc70d8b96c280934137396620a
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642180"
---
# <a name="provision-favorites-for-microsoft-edge"></a><span data-ttu-id="ffde0-103">Configurer les favoris pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ffde0-103">Provision favorites for Microsoft Edge</span></span>

<span data-ttu-id="ffde0-104">Sur la base des commentaires des clients, nous avons apporté des améliorations aux favoris de mise en service.</span><span class="sxs-lookup"><span data-stu-id="ffde0-104">Based on customer feedback, we've made improvements to provisioning favorites.</span></span> <span data-ttu-id="ffde0-105">À partir de la version 85 de Microsoft Edge, les administrateurs n’ont plus besoin de créer manuellement un fichier pour configurer les favoris.</span><span class="sxs-lookup"><span data-stu-id="ffde0-105">Starting with Microsoft Edge version 85, Admins no longer have to manually craft a file to provision favorites.</span></span> <span data-ttu-id="ffde0-106">Les administrateurs peuvent ajouter des favoris et dossiers à l’aide de l’interface utilisateur Microsoft Edge pour générer un fichier qui peut être exporté vers une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ffde0-106">Admins can add favorites and folders using the Microsoft Edge UI to generate a file that can be exported to a group policy.</span></span>

<span data-ttu-id="ffde0-107">Cet article décrit la mise en service d’un ensemble de favoris et de dossiers pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ffde0-107">This article describes how to provision a set of favorites and folders for your organization.</span></span> <span data-ttu-id="ffde0-108">Vous pouvez utiliser la stratégie [configurer les favoris](//DeployEdge/microsoft-edge-policies#configure-favorites) pour configurer les favoris et les dossiers.</span><span class="sxs-lookup"><span data-stu-id="ffde0-108">You can use the [Configure favorites](//DeployEdge/microsoft-edge-policies#configure-favorites) policy to provision favorites and folders.</span></span>

> [!NOTE]
> <span data-ttu-id="ffde0-109">Cet article concerne Microsoft Edge version 85 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ffde0-109">This article applies to Microsoft Edge version 85 or later.</span></span>

## <a name="prerequisites-and-recommendations"></a><span data-ttu-id="ffde0-110">Conditions préalables et recommandations</span><span class="sxs-lookup"><span data-stu-id="ffde0-110">Prerequisites and recommendations</span></span>

- <span data-ttu-id="ffde0-111">Microsoft Edge version 85 avec le modèle d’administration approprié installé pour les stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="ffde0-111">Microsoft Edge version 85 with the appropriate administrative template installed for group policies.</span></span>
- <span data-ttu-id="ffde0-112">Nous vous recommandons d’utiliser un nouveau profil dans Microsoft Edge pour configurer ces favoris.</span><span class="sxs-lookup"><span data-stu-id="ffde0-112">We recommend that you use a new profile in Microsoft Edge to provision these favorites.</span></span> <span data-ttu-id="ffde0-113">Tous les favoris enregistrés avec le profil sont inclus dans l’exportation.</span><span class="sxs-lookup"><span data-stu-id="ffde0-113">All favorites that are saved with the profile will be included in the export.</span></span>  

## <a name="provision-favorites-and-folders"></a><span data-ttu-id="ffde0-114">Configurer les favoris et les dossiers</span><span class="sxs-lookup"><span data-stu-id="ffde0-114">Provision favorites and folders</span></span>

<span data-ttu-id="ffde0-115">Procédez comme suit pour mettre en service vos favoris et dossiers pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ffde0-115">Use the following steps to provision favorites and folders for your users.</span></span>

1. <span data-ttu-id="ffde0-116">Accédez à la barre d’adresse Microsoft Edge et tapez l’URL suivante : *edge://flags/#edge-favorites-admin-export*.</span><span class="sxs-lookup"><span data-stu-id="ffde0-116">Go to the Microsoft Edge address bar and type this URL: *edge://flags/#edge-favorites-admin-export*.</span></span>
2. <span data-ttu-id="ffde0-117">Sous **Exporter la configuration des favoris pour les administrateurs**, sélectionnez **Activé** dans la liste déroulante, puis cliquez sur **Redémarrer**.</span><span class="sxs-lookup"><span data-stu-id="ffde0-117">Under **Favorites configuration export for administrators**, pick **Enabled** from the dropdown list and then click **Restart**.</span></span>

3. <span data-ttu-id="ffde0-118">Accédez à la page **Favoris** sur *edge://favorites* pour ajouter les favoris et dossiers que vous voulez configurer.</span><span class="sxs-lookup"><span data-stu-id="ffde0-118">Go to the **Favorites** page at *edge://favorites* so you can add the favorites and folders that you want to provision.</span></span>

<!--
4. On the **Favorites bar**, click **Add folder**. The folder structure of favorites that are set in the profile you're using will be reflected in the folder you provision for your users. The next screenshot shows "Managed favorites", the folder we'll use to provision favorites.

   ![Add a folder](media/edge-learnmore-provision-favorites/provision-favorites-add-folder.png)

   > [!TIP]
   > Add existing folders that contain favorites you want to provision for your users.

5. Select "Managed favorites" and then click **Add favorite**. The next screenshot shows the favorite we've added.

   ![Add a favorite](media/edge-learnmore-provision-favorites/provision-favorites-add-favorite.png)-->

4. <span data-ttu-id="ffde0-119">Lorsque vous avez terminé d’ajouter des favoris et des dossiers, vous pouvez les exporter de sorte qu’ils puissent être utilisés par la stratégie **Configurer les favoris**.</span><span class="sxs-lookup"><span data-stu-id="ffde0-119">When you finish adding favorites and folders you'll export them so they can be used by the **Configure favorites** policy.</span></span> <span data-ttu-id="ffde0-120">Accédez à la barre d’adresses et accédez à *edge://favorites*, cliquez sur les points de suspension « **...** », puis sélectionnez **Exporter la configuration des favoris**.</span><span class="sxs-lookup"><span data-stu-id="ffde0-120">Go to the address bar and navigate to *edge://favorites*, click the ellipsis "**…**" and choose **Export favorites configuration**.</span></span> <span data-ttu-id="ffde0-121">La capture d’écran suivante présente les options qui s’offrent à vous lors de la mise en service des favoris.</span><span class="sxs-lookup"><span data-stu-id="ffde0-121">The next screenshot shows the options you have when provisioning favorites.</span></span>

   ![Options de menu pour l’utilisation des favoris.](media/edge-learnmore-provision-favorites/provision-favorites-menu-options.png)

5. <span data-ttu-id="ffde0-123">Sous **Exporter votre configuration de favoris** vous indiquez un nom pour le dossier que vos utilisateurs verront.</span><span class="sxs-lookup"><span data-stu-id="ffde0-123">Under **Export your favorites configuration** you provide a name for the folder that your users will see.</span></span> <span data-ttu-id="ffde0-124">Tapez le nom du dossier, puis sélectionnez le format de plateforme que vous voulez utiliser.</span><span class="sxs-lookup"><span data-stu-id="ffde0-124">Type the Folder name and pick the Platform format you want to use.</span></span> <span data-ttu-id="ffde0-125">Cliquez sur **Copier dans le Presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="ffde0-125">Click **Copy to clipboard**.</span></span> <span data-ttu-id="ffde0-126">La capture d’écran suivante indique « Favoris gérés » pour le nom du dossier et la plateforme est Windows.</span><span class="sxs-lookup"><span data-stu-id="ffde0-126">The next screenshot shows "Managed favorites" for the folder name and the platform is Windows.</span></span>

   ![Boîte de dialogue pour exporter des favoris vers un dossier Windows.](media/edge-learnmore-provision-favorites/provision-favorites-export.png)

6. <span data-ttu-id="ffde0-128">Ouvrez l’éditeur de stratégies de groupe, accédez à *Configuration de l’ordinateur/Modèles d’administration/* , puis sélectionnez **Configurer les Favoris**.</span><span class="sxs-lookup"><span data-stu-id="ffde0-128">Open the Group Policy Editor, navigate to *Computer Configuration/Administrative Templates/* and pick **Configure Favorites**.</span></span> <span data-ttu-id="ffde0-129">Activer la stratégie « Configurer les favoris ».</span><span class="sxs-lookup"><span data-stu-id="ffde0-129">Enable the "Configure Favorites" policy.</span></span> <span data-ttu-id="ffde0-130">Sous **options :**, collez le contenu exporté dans la zone de texte Configurer les favoris, puis cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="ffde0-130">Under **Options:**, paste the exported contents in the Configure favorites text area then click **Apply**.</span></span> <span data-ttu-id="ffde0-131">La capture d’écran suivante montre un exemple de dossier « Favoris gérés » de l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="ffde0-131">The next screenshot shows an example of the "Managed favorites" folder from step 5.</span></span>

   ![Utilisez gpedit pour activer et configurer la stratégie « Configurer les favoris ».](media/edge-learnmore-provision-favorites/provision-favorites-gpedit.png)

7. <span data-ttu-id="ffde0-133">Cliquez sur **OK** ou sur **Appliquer** pour sécuriser les paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="ffde0-133">Click **OK** or **Apply** to safe the policy settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="ffde0-134">Voir également</span><span class="sxs-lookup"><span data-stu-id="ffde0-134">See also</span></span>

- [<span data-ttu-id="ffde0-135">Page d’accueil Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="ffde0-135">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)