---
title: Automatiser MicrosoftEdge pour le déploiement sur macOS avec Jamf
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 11/30/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Procédure d’automatisation de MicrosoftEdge pour le déploiement sur macOS avec Jamf.
ms.openlocfilehash: f02b9efde872082cf2301a4cf66b0a3f3782e39b
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447488"
---
# <a name="deploy-to-macos-with-jamf"></a><span data-ttu-id="f324b-103">Déployer sur macOS avec Jamf</span><span class="sxs-lookup"><span data-stu-id="f324b-103">Deploy to macOS with Jamf</span></span>

<span data-ttu-id="f324b-104">Cet article décrit comment déployer MicrosoftEdge pour macOS à l’aide de Jamf.</span><span class="sxs-lookup"><span data-stu-id="f324b-104">This article describes how to deploy Microsoft Edge for macOS using Jamf.</span></span>

> [!NOTE]
> <span data-ttu-id="f324b-105">Cet article concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f324b-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f324b-106">Prérequis</span><span class="sxs-lookup"><span data-stu-id="f324b-106">Prerequisites</span></span>

<span data-ttu-id="f324b-107">Avant de déployer Microsot Edge, assurez-vous que les conditions préalables suivantes sont réunies:</span><span class="sxs-lookup"><span data-stu-id="f324b-107">Before you deploy Microsoft Edge, make sure you meet the following prerequisites:</span></span>

- <span data-ttu-id="f324b-108">Le fichier d’installation de MicrosoftEdge, **MicrosoftEdgeDev-\\<version\>.pkg**, se trouve dans un emplacement accessible sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="f324b-108">The Microsoft Edge installation file,  **MicrosoftEdgeDev-\<version\>.pkg** is in an accessible location on your network.</span></span> <span data-ttu-id="f324b-109">Vous pouvez téléchargez les fichiers d’installation de Microsoft Edge Entreprise sur la [page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="f324b-109">You can download the Microsoft Edge Enterprise installation files from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="f324b-110">Vous disposez d’un compte Cloud Jamf avec le niveau d’accès et de privilèges nécessaires pour créer et déployer des fichiers d’installation sur des ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="f324b-110">You have a Jamf Cloud account with the level of access and privileges needed to create and deploy installation files to computers.</span></span>

## <a name="to-deploy-microsoft-edge-using-jamf"></a><span data-ttu-id="f324b-111">Pour déployer MicrosoftEdge à l’aide de Jamf:</span><span class="sxs-lookup"><span data-stu-id="f324b-111">To deploy Microsoft Edge using Jamf:</span></span>

1. <span data-ttu-id="f324b-112">Connectez-vous à Jamf et accédez à **Tous les paramètres**.</span><span class="sxs-lookup"><span data-stu-id="f324b-112">Sign on to Jamf and go to **All Settings**.</span></span>

    ![Ouvrez Tous les paramètres](./media/mac-deploy/jamf-dash-main-open-settings.png)

2. <span data-ttu-id="f324b-114">Sous **Tous les paramètres**, cliquez sur **Gestion de l’ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="f324b-114">Under **All Settings**, click **Computer Management**.</span></span>

    ![Sélectionnez Gestion de l’ordinateur](./media/mac-deploy/jamf-all-settings-computer-mgmt.png)

3. <span data-ttu-id="f324b-116">Sous **Gestion de l’ordinateur**, cliquez sur **Packages**.</span><span class="sxs-lookup"><span data-stu-id="f324b-116">Under **Computer Management**, click **Packages**.</span></span>

    ![Sélectionnez Packages](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkgs.png)

4. <span data-ttu-id="f324b-118">Sur la page **Packages**, cliquez sur **+ Nouveau** pour ajouter un nouveau package.</span><span class="sxs-lookup"><span data-stu-id="f324b-118">On the **Packages** page, click **+ New** to add a new package.</span></span>

    ![Sélectionnez Nouveau pour ajouter un nouveau package](./media/mac-deploy/jamf-all-settings-computer-mgmt-new-pkg.png)

5. <span data-ttu-id="f324b-120">Sur la page **Nouveau package**, entrez les détails du package, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f324b-120">On the **New Package** page, enter the details about the package and then click **Save**.</span></span> <span data-ttu-id="f324b-121">(Par exemple, NOM D’AFFICHAGE, INFO ou NOTES.)</span><span class="sxs-lookup"><span data-stu-id="f324b-121">(For example, DISPLAY NAME, INFO, or NOTES.)</span></span>

    ![Sélectionnez Enregistrer pour enregistrer les informations relatives au package](./media/mac-deploy/jamf-all-settings-computer-mgmt-save-pkg-info.png)

6. <span data-ttu-id="f324b-123">Sélectionnez **Ordinateurs** dans la barre de menus, puis **Stratégies** dans la barre de navigation.</span><span class="sxs-lookup"><span data-stu-id="f324b-123">Select **Computers** on the menu bar, and then select **Policies** in the navigation bar.</span></span>

7. <span data-ttu-id="f324b-124">Sélectionnez **+ Nouveau** pour afficher le volet **Nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="f324b-124">Select **+ New** to display the **New Policy** pane.</span></span>

    ![Sélectionnez Nouveau pour créer une nouvelle stratégie](./media/mac-deploy/jamf-all-settings-computer-new-policy.png)

8. <span data-ttu-id="f324b-126">Sous l’onglet **Options**, sélectionnez **Général**.</span><span class="sxs-lookup"><span data-stu-id="f324b-126">On the **Options** tab, select **General**.</span></span>

    - <span data-ttu-id="f324b-127">Sous **NOM D’AFFICHAGE**, entrez le nom d’affichage de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="f324b-127">Under **DISPLAY NAME**, enter the display name for the policy.</span></span>
    - <span data-ttu-id="f324b-128">Sous **Déclencheur**, sélectionnez l’événement qui déclenchera la stratégie.</span><span class="sxs-lookup"><span data-stu-id="f324b-128">Under **Trigger**, select the event that will trigger the policy.</span></span> <span data-ttu-id="f324b-129">Dans l’exemple suivant, l’événement est Démarrage.</span><span class="sxs-lookup"><span data-stu-id="f324b-129">(In the following example, the event is Startup.)</span></span>

    ![Entrez les informations relatives au déploiement](./media/mac-deploy/jamf-all-settings-computer-cfg-policy.png)

9. <span data-ttu-id="f324b-131">Sous l’onglet **Options**, cliquez sur **Packages**.</span><span class="sxs-lookup"><span data-stu-id="f324b-131">On the **Options** tab, click **Packages**.</span></span>

10. <span data-ttu-id="f324b-132">Dans la fenêtre contextuelle **Configurer des packages**, cliquez sur **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="f324b-132">On the **Configure Packages** popup, click **Configure**.</span></span>

    ![Configurer un package d’application](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-configure.png)

11. <span data-ttu-id="f324b-134">Le package que vous avez ajouté apparaît dans le volet **Packages**.</span><span class="sxs-lookup"><span data-stu-id="f324b-134">The package that you added shows on the **Packages** pane.</span></span> <span data-ttu-id="f324b-135">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f324b-135">Click **Add**.</span></span> <span data-ttu-id="f324b-136">Pour cet exemple, le package est «MicrosoftEdgeBeta» dans la capture d’écran suivant.</span><span class="sxs-lookup"><span data-stu-id="f324b-136">For this example, the package is "MicrosoftEdgeBeta" in the following screenshot.</span></span>

    ![Ajouter un package](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-add-beta.png)

12. <span data-ttu-id="f324b-138">Sur la page **Nouvelle stratégie**, utilisez les listes déroulantes pour sélectionner le **POINT DE DISTRIBUTION** et l’**ACTION** à effectuer pout la stratégie.</span><span class="sxs-lookup"><span data-stu-id="f324b-138">On the **New Policy** page, uUse the drop-down lists to select the **DISTRIBUTION POINT** and **ACTION** to take for the policy.</span></span> <span data-ttu-id="f324b-139">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f324b-139">Click **Save**.</span></span> <span data-ttu-id="f324b-140">La capture d’écran suivante utilise par exemple «Le point de distribution par défaut de chaque ordinateur» et «Installer».</span><span class="sxs-lookup"><span data-stu-id="f324b-140">The following screenshot uses "Each computer's default distribution point" and "Install" as an example.</span></span>

    ![Sélectionner un point de distribution de une action](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkg-cfg-distro.png)

13. <span data-ttu-id="f324b-142">Sur la page **Nouvelle stratégie**, sélectionnez l’onglet **Étendue**. Vous pouvez gérer l’étendue du déploiement en fonction des ordinateurs ou des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f324b-142">On the **New Policy** page, select the **Scope** tab. You can manage the scope of the deployment based on computers or users.</span></span> <span data-ttu-id="f324b-143">Pour cet exemple, sélectionnez \*\*Tous les ordinateurs \*\*dans la liste déroulante **ORDINATEURS CIBLES**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f324b-143">For this example, select **All Computers** from the **TARGET COMPUTERS** drop-down list and then click **Save**.</span></span>

    ![Sélectionnez l’étendue du déploiement](./media/mac-deploy/jamf-all-settings-computer-mgmt-add-target.png)

14. <span data-ttu-id="f324b-145">À ce stade, vous pouvez passer en revue la stratégie de déploiement de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="f324b-145">At this point you can review the Microsoft Edge deployment policy.</span></span> <span data-ttu-id="f324b-146">Si les options de déploiement répondent à vos besoins cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="f324b-146">If the deployment options meet your requirements, click **Done**.</span></span>

    ![Cliquez sur Terminé.](./media/mac-deploy/jamf-all-settings-computer-mgmt-finish-add-deployment.png)

    > [!NOTE]
    > <span data-ttu-id="f324b-148">Vous pouvez revenir à une stratégie de déploiement à tout moment pour modifier les paramètres.</span><span class="sxs-lookup"><span data-stu-id="f324b-148">You can return to a deployment policy at any time to change settings.</span></span>

<span data-ttu-id="f324b-149">Félicitations!</span><span class="sxs-lookup"><span data-stu-id="f324b-149">Congratulations!</span></span> <span data-ttu-id="f324b-150">Vous venez de terminer la configuration de Jamf pour déployer MicrosoftEdge pour macOS.</span><span class="sxs-lookup"><span data-stu-id="f324b-150">You’ve just finished configuring Jamf to deploy Microsoft Edge for macOS.</span></span> <span data-ttu-id="f324b-151">Lorsque la condition de déclencheur que vous avez définie sera true, le package sera déployé sur les ordinateurs que vous avez désignés.</span><span class="sxs-lookup"><span data-stu-id="f324b-151">When the trigger condition you defined is true, the package will get deployed to the computers you specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="f324b-152">Articles associés</span><span class="sxs-lookup"><span data-stu-id="f324b-152">See also</span></span>

- [<span data-ttu-id="f324b-153">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="f324b-153">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f324b-154">Jamf.com</span><span class="sxs-lookup"><span data-stu-id="f324b-154">Jamf.com</span></span>](https://www.jamf.com/)
- [<span data-ttu-id="f324b-155">Intégrer Jamf à Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="f324b-155">Integrate Jamf with Microsoft Intune</span></span>](/intune/conditional-access-integrate-jamf)