---
title: Déployer Microsoft Edge à l’aide de SystemCenter ConfigurationManager
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez comment déployer Microsoft Edge avec SystemCenter ConfigurationManager (SCCM).
ms.openlocfilehash: b403c8924a0f970aaadff2e1b20ebd05c0641a96
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617544"
---
# <a name="deploy-microsoft-edge-using-system-center-configuration-manager"></a><span data-ttu-id="ccdfa-103">Déployer Microsoft Edge à l’aide de SystemCenter ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="ccdfa-103">Deploy Microsoft Edge using System Center Configuration Manager</span></span>

<span data-ttu-id="ccdfa-104">Cet article explique comment automatiser un déploiement de MicrosoftEdge à l’aide de SystemCenter ConfigurationManager (SCCM).</span><span class="sxs-lookup"><span data-stu-id="ccdfa-104">This article shows you how to automate a Microsoft Edge deployment by using System Center Configuration Manager (SCCM).</span></span>

>[!NOTE]
><span data-ttu-id="ccdfa-105">Cet article concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="ccdfa-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="ccdfa-106">Before you begin</span></span>

<span data-ttu-id="ccdfa-107">Consultez les informations dans [Présentation de la gestion d’applications dans Configuration Manager](/sccm/apps/understand/introduction-to-application-management).</span><span class="sxs-lookup"><span data-stu-id="ccdfa-107">Review the information in [Introduction to application management in Configuration Manager](/sccm/apps/understand/introduction-to-application-management).</span></span> <span data-ttu-id="ccdfa-108">Cet article relatif à la gestion des applications vous aidera à mieux appréhender la terminologie utilisée dans cet article. Il vous aidera également à préparer votre site à l’installation d’applications.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-108">This application management article will help you understand the terminology used in this article and is a guide to preparing your site to install applications.</span></span>

<span data-ttu-id="ccdfa-109">Téléchargez les fichiers d’installation de MicrosoftEdge (**MicrosoftEdgeDevEnterpriseX64.msi** et/ou **MicrosoftEdgeDevEnterpriseX86.msi**) sur la [page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="ccdfa-109">Download the Microsoft Edge Enterprise installation files (**MicrosoftEdgeDevEnterpriseX64.msi** and/or **MicrosoftEdgeDevEnterpriseX86.msi**) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="ccdfa-110">Enregistrez les fichiers d’installation de MicrosoftEdge dans un emplacement réseau accessible.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-110">Make sure you store the Microsoft Edge installation files in an accessible network location.</span></span>

## <a name="create-the-application"></a><span data-ttu-id="ccdfa-111">Créez la liste des langues de l’application.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-111">Create the application</span></span>

<span data-ttu-id="ccdfa-112">Vous allez créer l’application à l’aide d’un Assistant Gestionnaire de configuration.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-112">You'll create the application using a Configuration Manager wizard.</span></span>

### <a name="start-the-create-application-wizard-and-create-the-application"></a><span data-ttu-id="ccdfa-113">Démarrer l’Assistant Création d’une application et créer l’application</span><span class="sxs-lookup"><span data-stu-id="ccdfa-113">Start the Create Application Wizard and create the application</span></span>  

1. <span data-ttu-id="ccdfa-114">Dans la console Configuration Manager, cliquez sur **Bibliothèque de logiciels** > **Gestion des applications** > **Applications**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-114">In the Configuration Manager console, click **Software Library** > **Application Management** > **Applications**.</span></span>  

2. <span data-ttu-id="ccdfa-115">Dans l’onglet **Accueil**, dans le groupe **Créer**, cliquez sur **Créer une application**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-115">On the **Home** tab, in the **Create** group, click **Create Application**.</span></span> <span data-ttu-id="ccdfa-116">Vous pouvez également cliquer avec le bouton droit sur **Applications** dans la barre de navigation, puis cliquer sur **Créer une application**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-116">Or, right-click on **Applications** in the navigation bar and then click **Create Application**.</span></span>

    ![Créer votre première application](./media/edge-ent-deployment-sccm/edge-ent-create-app-1.png)

3. <span data-ttu-id="ccdfa-118">Dans la page **Général** de l’**Assistant Création d’une application**, cochez la case **Détecter automatiquement les informations de cette application à partir des fichiers d’installation**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-118">On the **General** page of the **Create Application Wizard**, choose **Automatically detect information about this application from installation files**.</span></span> <span data-ttu-id="ccdfa-119">Ces informations sont pré-renseignées dans l’Assistant avec les données extraites du fichier d’installation. msi.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-119">This pre-populates some of the information in the wizard with information that's extracted from the installation .msi file.</span></span> <span data-ttu-id="ccdfa-120">Indiquez les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="ccdfa-120">Provide the following information:</span></span>  

   - <span data-ttu-id="ccdfa-121">**Type**: choisissez **Windows Installer (fichier \*.msi)**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-121">**Type**: Choose **Windows Installer (\*.msi file)**.</span></span>  

   - <span data-ttu-id="ccdfa-122">**Emplacement**: tapez l’emplacement (ou cliquez sur **Parcourir** pour sélectionner l’emplacement) du fichier d’installation **MicrosoftEdgeDevEnterpriseX64.msi** ou **MicrosoftEdgeDevEnterpriseX86.msi**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-122">**Location**: Type the location (or click **Browse** to select the location) of the installation file **MicrosoftEdgeDevEnterpriseX64.msi** or **MicrosoftEdgeDevEnterpriseX86.msi**.</span></span> <span data-ttu-id="ccdfa-123">Notez que l’emplacement doit être spécifié sous la forme *\\\Serveur\Partage\Fichier* pour que Configuration Manager localise les fichiers d’installation.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-123">Note that the location must be specified in the form *\\\Server\Share\File* for Configuration Manager to locate the installation files.</span></span>  

   <span data-ttu-id="ccdfa-124">La page **Spécifier les paramètres de cette application** ressemblera à l’exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="ccdfa-124">Your **Specify settings for this application** page will look like the following example:</span></span>  

    ![Spécifier les paramètres de cette application](./media/edge-ent-deployment-sccm/edge-ent-create-app-2.png)

4. <span data-ttu-id="ccdfa-126">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-126">Click **Next**.</span></span> <span data-ttu-id="ccdfa-127">Sous **Détails** sur la page **Informations importées**, vous verrez des informations concernant l’application et tous les fichiers associés qui ont été importés.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-127">Under **Details** on the **Imported Information** page, you'll see information about the application and any associated files that were imported.</span></span> <span data-ttu-id="ccdfa-128">Cliquez sur **Suivant** pour poursuivre l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-128">Click **Next** to continue with the wizard.</span></span>  

    ![Afficher les informations importées](./media/edge-ent-deployment-sccm/edge-ent-create-app-3.png)

5. <span data-ttu-id="ccdfa-130">Sur la page **Informations générales**, vous pouvez ajouter des informations supplémentaires sur l’application.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-130">On the **General Information** page, you can add more information about the application.</span></span> <span data-ttu-id="ccdfa-131">Par exemple, version du logiciel, commentaires de l’administrateur et éditeur.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-131">For example, Software version, Administrator comments, and Publisher.</span></span> <span data-ttu-id="ccdfa-132">Vous pouvez utiliser ces informations pour vous aider à trier et à rechercher l’application dans la console Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-132">You can use this information to to help you sort and find the application in the Configuration Manager console.</span></span>

   <span data-ttu-id="ccdfa-133">Vous pouvez également utiliser le champ **Programme d’installation** pour spécifier la ligne de commande complète qui sera utilisée pour installer l’application sur les PC.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-133">You can also use the **Installation program** field to specify the full command line that will be used to install the application on PCs.</span></span> <span data-ttu-id="ccdfa-134">Vous pouvez la modifier pour ajouter vos propres propriétés (par exemple, **/q** pour une installation sans assistance).</span><span class="sxs-lookup"><span data-stu-id="ccdfa-134">You can edit this to add your own properties (for example, **/q** for an unattended installation).</span></span>

   <span data-ttu-id="ccdfa-135">La capture d’écran suivante présente un exemple d’utilisation des champs **Spécifier des informations sur cette application**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-135">The following screenshot shows an example where the **Specify information about this application** fields are used.</span></span>

   ![Spécifier les métadonnées de l’application](./media/edge-ent-deployment-sccm/edge-ent-create-app-5.png)

6. <span data-ttu-id="ccdfa-137">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-137">Click **Next**.</span></span>
7. <span data-ttu-id="ccdfa-138">Sur la page **Résumé**, vous pouvez confirmer vos paramètres d’application sous **Détails**, puis terminer à l’aide de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-138">On the **Summary** page, you can confirm your application settings under **Details** and then finish using the wizard.</span></span> <span data-ttu-id="ccdfa-139">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-139">Click **Next**.</span></span>  

    ![Détails des paramètres d’application](./media/edge-ent-deployment-sccm/edge-ent-create-app-6.png)

8. <span data-ttu-id="ccdfa-141">Sur la page **Fin**, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-141">On the **Completion** page, click **Close**.</span></span>

    ![Boîte de dialogue Réussite](./media/edge-ent-deployment-sccm/edge-ent-create-app-7.png)

<span data-ttu-id="ccdfa-143">Vous avez terminé de créer l’application.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-143">You've finished creating the application.</span></span> <span data-ttu-id="ccdfa-144">Utilisez la procédure suivante pour la voir dans Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="ccdfa-144">Use the following steps to see it in Configuration Manager:</span></span>

- <span data-ttu-id="ccdfa-145">sélectionnez l’espace de travail **Bibliothèque de logiciels**</span><span class="sxs-lookup"><span data-stu-id="ccdfa-145">select the **Software Library** workspace</span></span>
- <span data-ttu-id="ccdfa-146">développez **Gestion des applications**</span><span class="sxs-lookup"><span data-stu-id="ccdfa-146">expand **Application Management**</span></span>
- <span data-ttu-id="ccdfa-147">cliquez sur **Applications**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-147">click **Applications**.</span></span>

<span data-ttu-id="ccdfa-148">La capture d’écran suivante illustre l’exemple utilisé pour cet article.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-148">The following screenshot shows the example used for this article.</span></span>  

![Applications](./media/edge-ent-deployment-sccm/edge-ent-create-app-8.png)

## <a name="change-application-properties-and-deployment-settings"></a><span data-ttu-id="ccdfa-150">Modifier les propriétés de l’application et les paramètres de déploiement</span><span class="sxs-lookup"><span data-stu-id="ccdfa-150">Change application properties and deployment settings</span></span>

<span data-ttu-id="ccdfa-151">Après avoir créé une application, vous pouvez affiner les paramètres d’application, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-151">After you create an application, you can refine the application settings if you need to.</span></span> <span data-ttu-id="ccdfa-152">Pour consulter les propriétés de l’application:</span><span class="sxs-lookup"><span data-stu-id="ccdfa-152">To look at the application properties:</span></span>

- <span data-ttu-id="ccdfa-153">sélectionnez l’application</span><span class="sxs-lookup"><span data-stu-id="ccdfa-153">select the application</span></span>
- <span data-ttu-id="ccdfa-154">dans **Accueil**>**Propriétés**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-154">in **Home**>**Properties**, click **Properties**.</span></span>  

   ![Configurer les propriétés de l’application](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-1.png)

 <span data-ttu-id="ccdfa-156">Dans la boîte de dialogue **Propriétés de l’application <nom de l’application\>**, vous verrez une vue avec onglets des éléments que vous pouvez configurer pour modifier le comportement de l’application.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-156">In the **<application name\> Application Properties** dialog page, you'll see a tabbed view of the items that you can configure to change the behavior of the application.</span></span> <span data-ttu-id="ccdfa-157">Pour plus d’informations sur les paramètres que vous pouvez configurer, consultez [Créer des applications](/sccm/apps/deploy-use/create-applications).</span><span class="sxs-lookup"><span data-stu-id="ccdfa-157">For more information about the settings you can configure, see [Create applications](/sccm/apps/deploy-use/create-applications).</span></span>

<span data-ttu-id="ccdfa-158">Pour cet exemple, vous allez modifier certaines propriétés du type de déploiement de l’application.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-158">For this example, you'll change some properties of the application's deployment type.</span></span> <span data-ttu-id="ccdfa-159">Pour modifier les propriétés de déploiement:</span><span class="sxs-lookup"><span data-stu-id="ccdfa-159">To change the deployment properties:</span></span>

1. <span data-ttu-id="ccdfa-160">Cliquez sur l’onglet **Types de déploiement**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-160">Click the **Deployment Types** tab.</span></span>
2. <span data-ttu-id="ccdfa-161">Sous **Types de déploiement**:, sélectionnez le **Nom** de l’application</span><span class="sxs-lookup"><span data-stu-id="ccdfa-161">Under **Deployment types:**, select the application **Name**</span></span>
3. <span data-ttu-id="ccdfa-162">Cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-162">Click **Edit**.</span></span>

   ![Modifier le type de déploiement](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-2.png)

### <a name="add-a-requirement-to-the-deployment-type"></a><span data-ttu-id="ccdfa-164">Ajouter une condition requise au type de déploiement</span><span class="sxs-lookup"><span data-stu-id="ccdfa-164">Add a requirement to the deployment type</span></span>

 <span data-ttu-id="ccdfa-165">Les conditions requises spécifient les critères à remplir pour qu’une application soit installée sur un périphérique.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-165">Requirements specify conditions that must be met before an application is installed on a device.</span></span> <span data-ttu-id="ccdfa-166">Vous pouvez choisir parmi les conditions requises intégrées ou vous pouvez créer votre propre configuration.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-166">You can choose from built-in requirements or you can create your own.</span></span> <span data-ttu-id="ccdfa-167">Par exemple, vous pouvez ajouter une condition stipulant que l’application sera installée uniquement sur les PC exécutant Windows10 **x86** ou **x64**, en fonction de l’architecture du processeur cible du fichier d’installation.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-167">For example, you can add a requirement that the application will only be installed on PCs that are running Windows 10 **x86** or **x64**, depending on the installation file's target processor architecture.</span></span> <span data-ttu-id="ccdfa-168">Dans cet exemple, vous allez spécifier Windows10 **x86**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-168">In this example, you'll specify Windows 10 **x86**.</span></span>

1. <span data-ttu-id="ccdfa-169">Dans la page Propriétés du type de déploiement que vous venez d’ouvrir, cliquez sur l’onglet **Conditions requises**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-169">From the deployment type properties page you just opened, click the **Requirements** tab.</span></span>

2. <span data-ttu-id="ccdfa-170">Cliquez sur **Ajouter** pour ouvrir la boîte de dialogue **Créer une spécification**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-170">Click **Add** to open the **Create Requirement** dialog.</span></span>

    ![Créer une spécification](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-3.png)

3. <span data-ttu-id="ccdfa-172">Dans la boîte de dialogue **Créer une spécification**, spécifiez les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="ccdfa-172">In the **Create Requirement** dialog box, specify the following information:</span></span>

    - <span data-ttu-id="ccdfa-173">**Catégorie**: **Périphérique**</span><span class="sxs-lookup"><span data-stu-id="ccdfa-173">**Category**: **Device**</span></span>  

    - <span data-ttu-id="ccdfa-174">**Condition**: **Système d’exploitation**</span><span class="sxs-lookup"><span data-stu-id="ccdfa-174">**Condition**: **Operating system**</span></span>  

    - <span data-ttu-id="ccdfa-175">**Type de règle**: **Valeur**</span><span class="sxs-lookup"><span data-stu-id="ccdfa-175">**Rule type**: **Value**</span></span>  

    - <span data-ttu-id="ccdfa-176">**Opérateur**: **Un de**</span><span class="sxs-lookup"><span data-stu-id="ccdfa-176">**Operator**: **One of**</span></span>  

    - <span data-ttu-id="ccdfa-177">Dans la liste systèmes d’exploitation, sélectionnez **Windows10** > **Tous les Windows10 (32bits)**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-177">From the operating systems list, select **Windows 10** > **All Windows 10 (32-bit)**.</span></span>  

    <span data-ttu-id="ccdfa-178">Lorsque vous avez terminé, la boîte de dialogue ressemble à la capture d’écran suivante:</span><span class="sxs-lookup"><span data-stu-id="ccdfa-178">When you're finished, the dialog will look like the following screenshot example:</span></span>

    ![Ajouter une condition requise](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-4.png)

4. <span data-ttu-id="ccdfa-180">Cliquez sur **OK** pour fermer chaque page de propriétés ouverte et revenir à la liste **Applications** dans la console Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-180">Click **OK** to close each open property page and return to the **Applications** list in the Configuration Manager console.</span></span>  

## <a name="add-the-application-content-to-a-distribution-point"></a><span data-ttu-id="ccdfa-181">Ajouter le contenu de l’application à un point de distribution</span><span class="sxs-lookup"><span data-stu-id="ccdfa-181">Add the application content to a distribution point</span></span>  

<span data-ttu-id="ccdfa-182">Pour déployer l’application mise à jour sur des PC, assurez-vous que le contenu de l’application est copié sur un point de distribution.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-182">To deploy the updated application to PCs, make sure that the application content is copied to a distribution point.</span></span> <span data-ttu-id="ccdfa-183">Les PC accèdent au point de distribution pour installer l’application.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-183">PCs access the distribution point to install the application.</span></span>  

>[!TIP]
><span data-ttu-id="ccdfa-184">Pour en savoir plus sur les points de distribution et la gestion de contenu dans Configuration Manager, consultez [Déployer et gérer le contenu pour SystemCenter ConfigurationManager](/sccm/core/servers/deploy/configure/deploy-and-manage-content).</span><span class="sxs-lookup"><span data-stu-id="ccdfa-184">To find out more about distribution points and content management in Configuration Manager, see [Deploy and manage content for System Center Configuration Manager](/sccm/core/servers/deploy/configure/deploy-and-manage-content).</span></span>  

1. <span data-ttu-id="ccdfa-185">Dans la console Configuration Manager, cliquez sur **Bibliothèque de logiciels**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-185">In the Configuration Manager console, click **Software Library**.</span></span>  

2. <span data-ttu-id="ccdfa-186">Dans l’espace de travail **Bibliothèque de logiciels**, développez **Applications**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-186">In the **Software Library** workspace, expand **Applications**.</span></span> <span data-ttu-id="ccdfa-187">Sélectionnez l’application que vous avez créée dans la liste des applications.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-187">Select the application you created in the list of applications.</span></span>

3. <span data-ttu-id="ccdfa-188">Sous l’onglet **Accueil** du groupe **Déploiement**, cliquez sur **Distribuer du contenu**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-188">On the **Home** tab in the **Deployment** group, click **Distribute Content**.</span></span>  

4. <span data-ttu-id="ccdfa-189">Sur la page **Général** de l’**Assistant de distribution de contenu**, vérifiez que le nom de l’application est correct, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-189">On the **General** page of the **Distribute Content Wizard**, check that the application name is correct, and then click **Next**.</span></span>  

5. <span data-ttu-id="ccdfa-190">Sur la page **Contenu**, vérifiez les informations qui seront copiées dans le point de distribution, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-190">On the **Content** page, review the information that will be copied to the distribution point, and then click **Next**.</span></span>  

6. <span data-ttu-id="ccdfa-191">Sur la page **Destination du contenu**, cliquez sur **Ajouter** pour sélectionner un ou plusieurs regroupements, points de distribution ou groupes de points de destination où vous souhaitez installer le contenu de l’application.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-191">On the **Content Destination** page, click **Add** to select one or more collections, distribution points, or distribution point groups on which to install the application content.</span></span>

7. <span data-ttu-id="ccdfa-192">Terminez l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-192">Complete the wizard.</span></span>

<span data-ttu-id="ccdfa-193">Vous pouvez vérifier que le contenu de l’application a été copié correctement dans le point de distribution à partir de l’espace de travail **Surveillance**, sous **État de la distribution** > **État du contenu**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-193">You can check that the application content was copied successfully to the distribution point from the **Monitoring** workspace, under **Distribution Status** > **Content Status**.</span></span>  

## <a name="deploy-the-application"></a><span data-ttu-id="ccdfa-194">Déployer l’application</span><span class="sxs-lookup"><span data-stu-id="ccdfa-194">Deploy the application</span></span>  

<span data-ttu-id="ccdfa-195">Ensuite, déployez l’application sur un regroupement de périphériques dans votre hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-195">Next, deploy the application to a device collection in your hierarchy.</span></span> <span data-ttu-id="ccdfa-196">Dans cet exemple, vous déployez l’application sur le regroupement de périphériques **Tous les systèmes**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-196">In this example, you deploy the application to the **All Systems** device collection.</span></span>  

>[!TIP]
><span data-ttu-id="ccdfa-197">N’oubliez pas que seuls les ordinateurs Windows10 de l’architecture de processeur spécifiée installent l’application, en raison des conditions requises que vous avez sélectionnées précédemment.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-197">Remember that only Windows 10 computers of the specified processor architecture will install the application because of the requirements that you selected earlier.</span></span>  

1. <span data-ttu-id="ccdfa-198">Dans la console Configuration Manager, cliquez sur **Bibliothèque de logiciels** > **Gestion des applications** > **Applications**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-198">In the Configuration Manager console, click **Software Library** > **Application Management** > **Applications**.</span></span>

2. <span data-ttu-id="ccdfa-199">Dans la liste des applications, sélectionnez l’application que vous avez créée.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-199">From the list of applications, select the application that you created earlier.</span></span> <span data-ttu-id="ccdfa-200">Puis, sous l’onglet **Accueil** du groupe **Déploiement**, cliquez sur **Déployer** ou cliquez avec le bouton droit sur l’application et sélectionnez **Déployer**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-200">Then, on the **Home** tab in the **Deployment** group, click **Deploy**, or right-click the application and select **Deploy**.</span></span>

    ![Déployer l’application](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-1.png)

3. <span data-ttu-id="ccdfa-202">Sur la page **Général** de l’**Assistant de déploiement de logiciel**, cliquez sur **Parcourir** pour sélectionner le regroupement de périphériques sur lequel vous souhaitez déployer l’application.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-202">On the **General** page of the **Deploy Software Wizard**, click **Browse** to select the device collection to which you want to deploy the application.</span></span>

    ![Accéder au fichier d’installation](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-2.png)

4. <span data-ttu-id="ccdfa-204">Sur la page **Contenu**, vérifiez que le point de distribution à partir duquel vous souhaitez que les PC installent l’application est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-204">On the **Content** page, check that the distribution point from which you want PCs to install the application is selected.</span></span>

    ![Spécifier un point de distribution](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-6.png)

5. <span data-ttu-id="ccdfa-206">Sur la page **Paramètres de déploiement**, vérifiez que l’action de déploiement est définie sur **Installer** et que l’objet du déploiement est défini sur **Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-206">On the **Deployment Settings** page, make sure that the deployment action is set to **Install**, and the deployment purpose is set to **Required**.</span></span>

    ![Configurer les paramètres de déploiement](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-8.png)

    >[!TIP]
    ><span data-ttu-id="ccdfa-208">En définissant l’objet du déploiement sur **Obligatoire**, vous vous assurez que l’application est installée sur les PC qui répondent aux conditions que vous avez définies.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-208">By setting the deployment purpose to **Required**, you make sure that the application is installed on PCs that meet the requirements that you set.</span></span> <span data-ttu-id="ccdfa-209">Si vous définissez cette valeur sur **Disponible**, les utilisateurs peuvent installer l’application à la demande à partir du Centre logiciel.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-209">If you set this value to **Available**, then users can install the application on demand from Software Center.</span></span>  

6. <span data-ttu-id="ccdfa-210">Sur la page **Planification**, vous pouvez configurer le moment où l’application sera installée.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-210">On the **Scheduling** page, you can configure when the application will be installed.</span></span> <span data-ttu-id="ccdfa-211">Pour cet exemple, sélectionnez **Dès que possible après le temps disponible**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-211">For this example, select **As soon as possible after the available time**.</span></span>

    ![Planifier le déploiement](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-9.png)

7. <span data-ttu-id="ccdfa-213">Sur la page **Expérience utilisateur**, sélectionnez les valeurs de votre choix et cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-213">On the **User Experience** page, select your desired values and click **Next**.</span></span>

    ![Spécifier l’expérience utilisateur](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-10.png)

8. <span data-ttu-id="ccdfa-215">Définissez les options d’alerte de votre choix, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-215">Specify your desired alert options and click **Next**.</span></span>

    ![Spécifier des paramètres d’alerte](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-11.png)

9. <span data-ttu-id="ccdfa-217">Terminez l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-217">Complete the wizard.</span></span>

<span data-ttu-id="ccdfa-218">Utilisez les informations de la section **Surveiller l’application** suivante pour afficher l’état du déploiement de votre application.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-218">Use the information in the following **Monitor the application** section to see the status of your application deployment.</span></span>  

## <a name="monitor-the-application"></a><span data-ttu-id="ccdfa-219">Surveiller l’application</span><span class="sxs-lookup"><span data-stu-id="ccdfa-219">Monitor the application</span></span>

 <span data-ttu-id="ccdfa-220">Dans cette section, vous allez consulter rapidement l’état du déploiement de l’application que vous venez de déployer.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-220">In this section, you'll take a quick look at the deployment status of the application that you just deployed.</span></span>  

### <a name="to-review-the-deployment-status"></a><span data-ttu-id="ccdfa-221">Pour consulter l’état du déploiement</span><span class="sxs-lookup"><span data-stu-id="ccdfa-221">To review the deployment status</span></span>  

1. <span data-ttu-id="ccdfa-222">Dans la console Configuration Manager, cliquez sur **Surveillance** > **Déploiements**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-222">In the Configuration Manager console, click **Monitoring** > **Deployments**.</span></span>  

2. <span data-ttu-id="ccdfa-223">Dans la liste des déploiements, sélectionnez l’application.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-223">From the list of deployments, select the application.</span></span>

    ![Surveiller le déploiement](./media/edge-ent-deployment-sccm/edge-ent-monitor-deployment.png)

3. <span data-ttu-id="ccdfa-225">Dans l’onglet **Accueil** du groupe **Déploiement**, cliquez sur **Afficher l’état**.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-225">On the **Home** tab in the **Deployment** group, click **View Status**.</span></span>  

4. <span data-ttu-id="ccdfa-226">Sélectionnez l’un des onglets suivants pour afficher plus de mises à jour d’état concernant le déploiement d’applications:</span><span class="sxs-lookup"><span data-stu-id="ccdfa-226">Select one of the following tabs to see more status updates about the application deployment:</span></span>  

    - <span data-ttu-id="ccdfa-227">**Réussite**: l’application a été installée correctement sur les PC indiqués.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-227">**Success**: The application installed successfully on the indicated PCs.</span></span>  

    - <span data-ttu-id="ccdfa-228">**En cours**: l’installation de l’application n’est pas encore terminée.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-228">**In Progress**: The application has not yet finished installing.</span></span>  

    - <span data-ttu-id="ccdfa-229">**Erreur**: une erreur s’est produite lors de l’installation de l’application sur les PC indiqués.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-229">**Error**: An error occurred installing the application on the indicated PCs.</span></span> <span data-ttu-id="ccdfa-230">Des informations supplémentaires sur l’erreur s’affichent également.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-230">Further information about the error is also displayed.</span></span>  

    - <span data-ttu-id="ccdfa-231">**Conditions non remplies**: aucune tentative d’installation n’a été effectuée sur les appareils indiqués, car ils ne répondent pas aux critères que vous avez configurés (dans cet exemple, parce qu’ils ne fonctionnent pas sur Windows10.)</span><span class="sxs-lookup"><span data-stu-id="ccdfa-231">**Requirements Not Met**: No installation attempt was made on the indicated devices because they did not meet the requirements you configured (in this example, because they do not run on Windows 10.)</span></span>

    - <span data-ttu-id="ccdfa-232">**Inconnu**: ConfigurationManager n’a pas pu signaler l’état du déploiement.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-232">**Unknown**: Configuration Manager was unable to report the status of the deployment.</span></span> <span data-ttu-id="ccdfa-233">Vérifiez à nouveau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-233">Check back again later.</span></span>  

    >[!TIP]
    ><span data-ttu-id="ccdfa-234">Il existe plusieurs façons de surveiller le déploiements des applications.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-234">There are several ways you can monitor application deployments.</span></span> <span data-ttu-id="ccdfa-235">Pour plus d’informations, consultez [Surveiller les applications avec la console SystemCenterConfigurationManager](/sccm/apps/deploy-use/monitor-applications-from-the-console).</span><span class="sxs-lookup"><span data-stu-id="ccdfa-235">For more information, see [Monitor applications from the System Center Configuration Manager console](/sccm/apps/deploy-use/monitor-applications-from-the-console).</span></span>  

## <a name="end-user-experience"></a><span data-ttu-id="ccdfa-236">Expérience pour l’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="ccdfa-236">End-user experience</span></span>  

<span data-ttu-id="ccdfa-237">Les utilisateurs qui disposent de PC gérés par ConfigurationManager et qui exécutent Windows10 de l’architecture de processeur spécifiée verront un message leur indiquant qu’ils doivent installer l’application MicrosoftEdge Dev.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-237">Users who have PCs that are managed by Configuration Manager and are running Windows 10 of the specified processor architecture, will see a message telling them that they must install the Microsoft Edge Dev application.</span></span> <span data-ttu-id="ccdfa-238">Lorsqu’ils acceptent cette option d’installation, l’application est installée.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-238">When they accept this installation option, the application is installed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ccdfa-239">Articles associés</span><span class="sxs-lookup"><span data-stu-id="ccdfa-239">See also</span></span>

- [<span data-ttu-id="ccdfa-240">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="ccdfa-240">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="ccdfa-241">Pour plus d’informations sur le déploiement de packages MSI, voir Créer et déployer une application avec System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ccdfa-241">Create and deploy an application with System Center Configuration Manager</span></span>](/sccm/apps/get-started/create-and-deploy-an-application)