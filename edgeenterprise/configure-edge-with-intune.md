---
title: Configurer les paramètres de stratégie MicrosoftEdge pour Windows avec MicrosoftIntune
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/18/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer les paramètres de stratégie MicrosoftEdge pour Windows avec MicrosoftIntune.
ms.openlocfilehash: 6200b52e9061f37f85fe0bfe7cf59a2172db97df
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979698"
---
# <span data-ttu-id="3e10b-103">Configurer les paramètres de stratégie MicrosoftEdge avec MicrosoftIntune</span><span class="sxs-lookup"><span data-stu-id="3e10b-103">Configure Microsoft Edge policy settings with Microsoft Intune</span></span>

<span data-ttu-id="3e10b-104">Cet article explique comment configurer les paramètres de stratégie MicrosoftEdge pour Windows10 à l’aide de MicrosoftIntune.</span><span class="sxs-lookup"><span data-stu-id="3e10b-104">This article explains how to configure Microsoft Edge policy settings for Windows 10 using Microsoft Intune.</span></span>

> [!NOTE]
> <span data-ttu-id="3e10b-105">Cet article concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3e10b-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="3e10b-106">Vous pouvez configurer les stratégies et paramètres MicrosoftEdge en ajoutant un profil de configuration de périphérique à MicrosoftIntune.</span><span class="sxs-lookup"><span data-stu-id="3e10b-106">You can configure Microsoft Edge policies and settings by adding a device configuration profile to Microsoft Intune.</span></span> <span data-ttu-id="3e10b-107">L’utilisation de Intune pour gérer et appliquer des méthodes revient à utiliser la méthode de groupe ActiveDirectory ou à configurer les paramètres du Group Policy Object (GPO) local sur les périphériques des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="3e10b-107">Using Intune to manage and enforce policies is equivalent to using Active Directory Group Policy or configuring local Group Policy Object (GPO) settings on user devices.</span></span>

<span data-ttu-id="3e10b-108">Pour plus d’informations sur la gestion des stratégies de MicrosoftEdge avec MicrosoftIntune, vous pouvez consulter [Gérer l’accès au web à l’aide de MicrosoftEdge avec MicrosoftIntune](https://docs.microsoft.com/intune/manage-microsoft-edge). Gardez néanmoins à l’esprit que l’article associé est spécifique à MicrosoftEdge version45 et versions antérieures et que, par conséquent, il peut contenir des informations et des références qui ne concernent pas MicrosoftEdge Enterprise version77 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3e10b-108">For more information about managing Microsoft Edge policies with Microsoft Intune, you can read [Manage web access by using Microsoft Edge with Microsoft Intune](https://docs.microsoft.com/intune/manage-microsoft-edge), but keep in mind that the linked article is specific to Microsoft Edge version 45 and earlier and therefore may contain information and references that don't apply to Microsoft Edge Enterprise version 77 and later.</span></span>

> [!TIP]
> <span data-ttu-id="3e10b-109">Pour plus d’informations sur la configuration de MicrosoftEdge sur macOS à l’aide de MicrosoftIntune, consultez [Configurer pour macOS](configure-microsoft-edge-on-mac.md).</span><span class="sxs-lookup"><span data-stu-id="3e10b-109">For information on how to configure Microsoft Edge on macOS using Microsoft Intune, see [Configure for macOS](configure-microsoft-edge-on-mac.md).</span></span>

## <span data-ttu-id="3e10b-110">Créer un profil pour gérer les paramètres dans MicrosoftEdge pour Windows10</span><span class="sxs-lookup"><span data-stu-id="3e10b-110">Create a profile to manage settings in Microsoft Edge for Windows 10</span></span>

<span data-ttu-id="3e10b-111">Grâce aux modèles d’administration dans MicrosoftIntune, vous pouvez gérer les stratégies de groupe MicrosoftEdge sur vos appareils Windows10 en utilisant le cloud.</span><span class="sxs-lookup"><span data-stu-id="3e10b-111">Using Administrative Templates in Microsoft Intune, you can manage Microsoft Edge group policies on your Windows 10 devices using the cloud.</span></span> <span data-ttu-id="3e10b-112">Cette section vous aidera à créer un modèle pour configurer les paramètres d’application spécifiques de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="3e10b-112">This section will help you create a template to configure Microsoft Edge-specific application settings.</span></span> <span data-ttu-id="3e10b-113">Lorsque vous créez le modèle, il crée un profil de configuration de périphérique.</span><span class="sxs-lookup"><span data-stu-id="3e10b-113">When you create the template, it creates a device configuration profile.</span></span> <span data-ttu-id="3e10b-114">Vous pouvez ensuite attribuer ou déployer ce profil sur les appareils Windows10 de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3e10b-114">You can then assign or deploy this profile to Windows 10 devices in your organization.</span></span>

### <span data-ttu-id="3e10b-115">Prérequis</span><span class="sxs-lookup"><span data-stu-id="3e10b-115">Prerequisites</span></span>

- <span data-ttu-id="3e10b-116">Windows10, avec la configuration minimale requise suivante:</span><span class="sxs-lookup"><span data-stu-id="3e10b-116">Windows 10 with the following minimum system requirements:</span></span>
  - <span data-ttu-id="3e10b-117">Windows10 version1909</span><span class="sxs-lookup"><span data-stu-id="3e10b-117">Windows 10, version 1909</span></span>
  - <span data-ttu-id="3e10b-118">Windows10, version1903 avec la mise à jour [KB4512941](https://support.microsoft.com/kb/4512941) installée</span><span class="sxs-lookup"><span data-stu-id="3e10b-118">Windows 10, version 1903 with [KB4512941](https://support.microsoft.com/kb/4512941) installed</span></span>
  - <span data-ttu-id="3e10b-119">Windows10, version1809 avec la mise à jour [KB4512534](https://support.microsoft.com/kb/4512534) installée</span><span class="sxs-lookup"><span data-stu-id="3e10b-119">Windows 10, version 1809 with [KB4512534](https://support.microsoft.com/kb/4512534) installed</span></span>
  - <span data-ttu-id="3e10b-120">Windows10, version1803 avec la mise à jour [KB4512509](https://support.microsoft.com/kb/4512509) installée</span><span class="sxs-lookup"><span data-stu-id="3e10b-120">Windows 10, version 1803 with [KB4512509](https://support.microsoft.com/kb/4512509) installed</span></span>
  - <span data-ttu-id="3e10b-121">Windows10, version1709 avec la mise à jour [KB4516071](https://support.microsoft.com/kb/4516071) installée</span><span class="sxs-lookup"><span data-stu-id="3e10b-121">Windows 10, version 1709 with [KB4516071](https://support.microsoft.com/kb/4516071) installed</span></span>

### <span data-ttu-id="3e10b-122">Utiliser les modèles d’administration pour créer méthode pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3e10b-122">Use Administrative Templates to create a policy for Microsoft Edge</span></span>

<span data-ttu-id="3e10b-123">Cette procédure s’inspire des modèles d’administration (que vous avez peut-être utilisés dans la méthode de groupe) intégrés à Intune.</span><span class="sxs-lookup"><span data-stu-id="3e10b-123">This procedure leverages Administrative templates (which you might be familiar with from Group Policy) that are built into Intune.</span></span> <span data-ttu-id="3e10b-124">Vous pouvez utiliser ces modèles pour créer une méthode pour Microsoft Edge en sélectionnant les paramètres dans une liste préconfigurée.</span><span class="sxs-lookup"><span data-stu-id="3e10b-124">You can use these templates to create a policy for Microsoft Edge by selecting settings from a pre-configured list.</span></span>

1. <span data-ttu-id="3e10b-125">Connectez-vous au portail [Microsoft Endpoint Manager](https://endpoint.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="3e10b-125">Sign in to the [Microsoft Endpoint Manager](https://endpoint.microsoft.com/) portal.</span></span>
2. <span data-ttu-id="3e10b-126">Sélectionnez **Appareils** dans le volet gauche de navigation.</span><span class="sxs-lookup"><span data-stu-id="3e10b-126">Select **Devices** in the left-hand navigation pane.</span></span>
3. <span data-ttu-id="3e10b-127">De \*\* Appareils \*\* | **Vue d’ensemble**, sélectionner \*\* Profil de Configuration\*\* (sous l’en-tête Méthode).</span><span class="sxs-lookup"><span data-stu-id="3e10b-127">From **Devices** | **Overview**, select **Configuration Profiles** (under Policy heading).</span></span>
4. <span data-ttu-id="3e10b-128">Dans la barre de commandes supérieure, sélectionnez **Créer profil**.</span><span class="sxs-lookup"><span data-stu-id="3e10b-128">On the top command bar, select **Create profile**.</span></span>
5. <span data-ttu-id="3e10b-129">Dans la liste déroulante ci-dessous **Plateforme**,sélectionner **Windows 10 et ultérieure**.</span><span class="sxs-lookup"><span data-stu-id="3e10b-129">In the drop-down list below **Platform**, select **Windows 10 and later**.</span></span>
6. <span data-ttu-id="3e10b-130">Dans la liste déroulante ci-dessous**Profil**,sélectionner **Modèles d’Administration** puis cliquer sur le \*\* bouton \*\*.Créer.</span><span class="sxs-lookup"><span data-stu-id="3e10b-130">In the drop-down list below **Profile**, select **Administrative Templates** and then click the **Create** button.</span></span> <span data-ttu-id="3e10b-131">La capture d’écran suivante montre les listes déroulantes permettant de sélectionner la plateforme et le type de profil.</span><span class="sxs-lookup"><span data-stu-id="3e10b-131">The next screenshot shows the drop-down lists to select the platform and type of profile.</span></span>

    ![Sélectionner une plateforme et un type de profil](./media/configure-edge-with-intune/create-profile-platform.png)

7. <span data-ttu-id="3e10b-133">Sous l’onglet Notions de Base, entrer un\*\*Nom descriptif \*\*, tel que Méthode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3e10b-133">On the **Basics** tab, enter a descriptive **Name**, such as Microsoft Edge Policy.</span></span> <span data-ttu-id="3e10b-134">Si vous le souhaitez, saisissez une **Description**pour la méthode.</span><span class="sxs-lookup"><span data-stu-id="3e10b-134">Optionally, enter a  **Description** for the policy.</span></span>
<span data-ttu-id="3e10b-135">La capture d’écran suivante montre le formulaire de l’onglet **Notions de Base** et la barre de menus affiche les étapes suivantes (sous la forme d’onglets grisés) pour créer le profil.</span><span class="sxs-lookup"><span data-stu-id="3e10b-135">The next screenshot shows the form for the **Basics** tab and the menu bar shows the next steps (as grayed out tabs) to create the profile.</span></span>

   ![Entrer Nom et Description](./media/configure-edge-with-intune/create-profile-basics-tab.png)

8. <span data-ttu-id="3e10b-137">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="3e10b-137">Select **Next**.</span></span>
9. <span data-ttu-id="3e10b-138">Sous l’onglet **Paramètres de configuration**, sélectionnez le dossier Microsoft Edge dans l’un des emplacements suivants:</span><span class="sxs-lookup"><span data-stu-id="3e10b-138">On the **Configuration settings** tab, select the Microsoft Edge folder in one of the following locations:</span></span>

   - <span data-ttu-id="3e10b-139">ci-dessous le dossier Configuration Ordinateur</span><span class="sxs-lookup"><span data-stu-id="3e10b-139">below the Computer Configuration folder</span></span>
   - <span data-ttu-id="3e10b-140">ci-dessous le dossier Configuration Utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3e10b-140">below the User Configuration folder.</span></span>

   <span data-ttu-id="3e10b-141">Les paramètres disponibles pour Microsoft Edge s’affichent dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="3e10b-141">The available settings for Microsoft Edge will be shown on the right pane.</span></span> <span data-ttu-id="3e10b-142">Par exemple, *Configuration Ordinateur/Microsoft Edge/Autoriser les restrictions de téléchargement* présenté dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="3e10b-142">For example, *Computer Configuration/Microsoft Edge/Allow download restrictions* shown in the following screenshot.</span></span>

   ![Onglet Paramètres de configuration](./media/configure-edge-with-intune/create-profile-configuration-settings-tab.png)

   > [!NOTE]
   > <span data-ttu-id="3e10b-144">Consulter [MICROSOFT– Méthodes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies) et [Microsoft Edge– Méthodes de Mises à jour](https://docs.microsoft.com/DeployEdge/microsoft-edge-update-policies) pour la liste la plus complète et récente de tous les paramètres disponibles pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3e10b-144">See [Microsoft Edge – Policies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies) and [Microsoft Edge – Update policies](https://docs.microsoft.com/DeployEdge/microsoft-edge-update-policies) for the most complete and up to date list of all the available settings for Microsoft Edge.</span></span>

10. <span data-ttu-id="3e10b-145">Utiliser le champ de recherche («Rechercher pour filtrer les éléments...») pour trouver un paramètre spécifique que vous voulez configurer.</span><span class="sxs-lookup"><span data-stu-id="3e10b-145">Use the search field ("Search to filter items ...") to find a specific setting you want to configure.</span></span> <span data-ttu-id="3e10b-146">Dans cet exemple, la chaîne de recherche est «page d’accueil».</span><span class="sxs-lookup"><span data-stu-id="3e10b-146">In this example, the search string is "home page".</span></span> <span data-ttu-id="3e10b-147">La capture d’écran suivante montre les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="3e10b-147">The next screenshot shows the search results.</span></span>

    ![Résultats de la recherche](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-search.png)

11. <span data-ttu-id="3e10b-149">Une fois que vous avez trouvé le paramètre que vous voulez configurer, sélectionnez le pour afficher les valeurs que vous pouvez définir.</span><span class="sxs-lookup"><span data-stu-id="3e10b-149">After you find the setting you intend to configure, select it to expose the values you can set.</span></span> <span data-ttu-id="3e10b-150">Dans la capture d’écran suivante, nous avons sélectionné «Configurer l’URL de la page d’accueil» à titre d’exemple.</span><span class="sxs-lookup"><span data-stu-id="3e10b-150">In the next screenshot, we selected "Configure the home page URL" as an example.</span></span>

    ![Configurer la méthode URL de la page d’accueil](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-edit-pol.png)

12. <span data-ttu-id="3e10b-152">Activer la méthode et entrez une valeur pour l’URL de la Page d’accueil URL, comme présenté dans la capture d’écran précédente.</span><span class="sxs-lookup"><span data-stu-id="3e10b-152">Enable the policy and enter a value for the Home page URL, as shown in the previous screenshot.</span></span>

13. <span data-ttu-id="3e10b-153">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e10b-153">Click **OK**.</span></span> <span data-ttu-id="3e10b-154">La colonne des paramètres «État» doit apparaître comme «activé», comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="3e10b-154">The settings "State" column should appear as "Enabled", as shown in the following screenshot example.</span></span>

    ![L’état du paramètre est activé](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-set-enabled.png)

14. <span data-ttu-id="3e10b-156">Cliquez sur le bouton **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="3e10b-156">Click the **Next** button.</span></span>

15. <span data-ttu-id="3e10b-157">Sur l’onglet Indicateurs d’étendue, ajoutez une balise d’étendue si vous le souhaitez, sinon cliquez sur le\*\*bouton \*\* suivant.</span><span class="sxs-lookup"><span data-stu-id="3e10b-157">On the **Scope tags** tab, add a Scope tag if wanted, otherwise click the **Next** button.</span></span>

16. <span data-ttu-id="3e10b-158">Sous l’onglet **Assignations**, cliquez sur + sélectionner des groupes à inclure  pour assigner cette méthode au groupe Azure Active Directory (Azure AD) qui contient les appareils ou les utilisateurs auxquels vous voulez assigner ce paramètre de méthode.</span><span class="sxs-lookup"><span data-stu-id="3e10b-158">On the **Assignments** tab, click **+ Select groups to include** to assign this policy to the Azure Active Directory (Azure AD) group that contains the devices or the users that you want to receive this policy setting.</span></span> <span data-ttu-id="3e10b-159">Consultez [Assigner les profils d’utilisateur et de périphérique dans MicrosoftIntune](https://docs.microsoft.com/intune/device-profile-assign) pour les informations sur comment assigner le profil à vos groupes d’utilisateurs ou à périphériques Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3e10b-159">See [Assign user and device profiles in Microsoft Intune](https://docs.microsoft.com/intune/device-profile-assign) for information about how to assign the profile to your Azure AD user or device groups.</span></span>

    ![Sélectionner les groupes à inclure](./media/configure-edge-with-intune/create-profile-assignments-tab.png)

17. <span data-ttu-id="3e10b-161">Cliquez sur le bouton **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="3e10b-161">Click the **Next** button.</span></span>

18. <span data-ttu-id="3e10b-162">Sous l’onglet **Révision + créer**, réviser le résumé de vos modifications pour vous assurer qu’il est correct, puis cliquez sur le**bouton**Créer.</span><span class="sxs-lookup"><span data-stu-id="3e10b-162">On the **Review + create** tab, review the summary of your changes to ensure it's correct and then click the **Create** button.</span></span>

19. <span data-ttu-id="3e10b-163">La méthode récemment créée (Méthode Microsoft Edge) est présentée dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="3e10b-163">The newly created policy (Microsoft Edge Policy) is shown in the following screenshot.</span></span>

    ![Sélectionner les groupes à inclure](./media/configure-edge-with-intune/create-profile-new-policy-finished.png)

<span data-ttu-id="3e10b-165">Pour plus d’informations sur les profils Windows10, consultez [Utiliser des modèles Windows10 pour configurer les paramètres de stratégie de groupe dans MicrosoftIntune](https://docs.microsoft.com/intune/administrative-templates-windows).</span><span class="sxs-lookup"><span data-stu-id="3e10b-165">For more information about Windows 10 profiles, see [Use Windows 10 templates to configure group policy settings in Microsoft Intune](https://docs.microsoft.com/intune/administrative-templates-windows).</span></span>

## <span data-ttu-id="3e10b-166">Articles associés</span><span class="sxs-lookup"><span data-stu-id="3e10b-166">See also</span></span>

- [<span data-ttu-id="3e10b-167">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="3e10b-167">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="3e10b-168">Gérer l’accès web à l’aide de MicrosoftEdge avec MicrosoftIntune</span><span class="sxs-lookup"><span data-stu-id="3e10b-168">Manage web access by using Microsoft Edge with Microsoft Intune</span></span>](https://docs.microsoft.com/intune/manage-microsoft-edge)
- [<span data-ttu-id="3e10b-169">Utilisez les modèles Windows10 pour configurer les paramètres de stratégie de groupe dans MicrosoftIntune</span><span class="sxs-lookup"><span data-stu-id="3e10b-169">Use Windows 10 templates to configure group policy settings in Microsoft Intune</span></span>](https://docs.microsoft.com/intune/administrative-templates-windows)
- [<span data-ttu-id="3e10b-170">Déployer MicrosoftEdge à l’aide de MicrosoftIntune</span><span class="sxs-lookup"><span data-stu-id="3e10b-170">Deploy Microsoft Edge using Microsoft Intune</span></span>](https://docs.microsoft.com/intune/apps/apps-windows-edge/?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)
