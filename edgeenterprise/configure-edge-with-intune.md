---
title: Configurer les paramètres de stratégie Microsoft Edge pour Windows avec Microsoft Intune
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Configurer les paramètres de stratégie Microsoft Edge pour Windows avec Microsoft Intune.
ms.openlocfilehash: adcd80f68250a9694b9bbaa21fb7941ebcbaf15a
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641670"
---
# <a name="configure-microsoft-edge-policy-settings-with-microsoft-intune"></a><span data-ttu-id="ff1aa-103">Configurer les paramètres de stratégie Microsoft Edge avec Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="ff1aa-103">Configure Microsoft Edge policy settings with Microsoft Intune</span></span>

<span data-ttu-id="ff1aa-104">Cet article explique comment configurer les paramètres de stratégie Microsoft Edge pour Windows 10 à l’aide de Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-104">This article explains how to configure Microsoft Edge policy settings for Windows 10 using Microsoft Intune.</span></span>

> [!NOTE]
> <span data-ttu-id="ff1aa-105">Cet article concerne Microsoft Edge version 77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="ff1aa-106">Vous pouvez configurer les stratégies et paramètres Microsoft Edge en ajoutant un profil de configuration de périphérique à Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-106">You can configure Microsoft Edge policies and settings by adding a device configuration profile to Microsoft Intune.</span></span> <span data-ttu-id="ff1aa-107">L’utilisation de Intune pour gérer et appliquer des méthodes revient à utiliser la méthode de groupe Active Directory ou à configurer les paramètres du Group Policy Object (GPO) local sur les périphériques des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-107">Using Intune to manage and enforce policies is equivalent to using Active Directory Group Policy or configuring local Group Policy Object (GPO) settings on user devices.</span></span>

<span data-ttu-id="ff1aa-108">Pour plus d’informations sur la gestion des stratégies de Microsoft Edge avec Microsoft Intune, vous pouvez consulter [Gérer l’accès au web à l’aide de Microsoft Edge avec Microsoft Intune](/intune/manage-microsoft-edge). Gardez néanmoins à l’esprit que l’article associé est spécifique à Microsoft Edge version 45 et versions antérieures et que, par conséquent, il peut contenir des informations et des références qui ne concernent pas Microsoft Edge Enterprise version 77 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-108">For more information about managing Microsoft Edge policies with Microsoft Intune, you can read [Manage web access by using Microsoft Edge with Microsoft Intune](/intune/manage-microsoft-edge), but keep in mind that the linked article is specific to Microsoft Edge version 45 and earlier and therefore may contain information and references that don't apply to Microsoft Edge Enterprise version 77 and later.</span></span>

> [!TIP]
> <span data-ttu-id="ff1aa-109">Pour plus d’informations sur la configuration de Microsoft Edge sur macOS à l’aide de Microsoft Intune, consultez [Configurer pour macOS](configure-microsoft-edge-on-mac.md).</span><span class="sxs-lookup"><span data-stu-id="ff1aa-109">For information on how to configure Microsoft Edge on macOS using Microsoft Intune, see [Configure for macOS](configure-microsoft-edge-on-mac.md).</span></span>

## <a name="create-a-profile-to-manage-settings-in-microsoft-edge-for-windows-10"></a><span data-ttu-id="ff1aa-110">Créer un profil pour gérer les paramètres dans Microsoft Edge pour Windows 10</span><span class="sxs-lookup"><span data-stu-id="ff1aa-110">Create a profile to manage settings in Microsoft Edge for Windows 10</span></span>

<span data-ttu-id="ff1aa-111">Grâce aux modèles d’administration dans Microsoft Intune, vous pouvez gérer les stratégies de groupe Microsoft Edge sur vos appareils Windows 10 en utilisant le cloud.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-111">Using Administrative Templates in Microsoft Intune, you can manage Microsoft Edge group policies on your Windows 10 devices using the cloud.</span></span> <span data-ttu-id="ff1aa-112">Cette section vous aidera à créer un modèle pour configurer les paramètres d’application spécifiques de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-112">This section will help you create a template to configure Microsoft Edge-specific application settings.</span></span> <span data-ttu-id="ff1aa-113">Lorsque vous créez le modèle, il crée un profil de configuration de périphérique.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-113">When you create the template, it creates a device configuration profile.</span></span> <span data-ttu-id="ff1aa-114">Vous pouvez ensuite attribuer ou déployer ce profil sur les appareils Windows 10 de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-114">You can then assign or deploy this profile to Windows 10 devices in your organization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ff1aa-115">Prérequis</span><span class="sxs-lookup"><span data-stu-id="ff1aa-115">Prerequisites</span></span>

- <span data-ttu-id="ff1aa-116">Windows 10, avec la configuration minimale requise suivante :</span><span class="sxs-lookup"><span data-stu-id="ff1aa-116">Windows 10 with the following minimum system requirements:</span></span>
  - <span data-ttu-id="ff1aa-117">Windows 10 version 1909</span><span class="sxs-lookup"><span data-stu-id="ff1aa-117">Windows 10, version 1909</span></span>
  - <span data-ttu-id="ff1aa-118">Windows 10, version 1903 avec la mise à jour [KB4512941](https://support.microsoft.com/kb/4512941) installée</span><span class="sxs-lookup"><span data-stu-id="ff1aa-118">Windows 10, version 1903 with [KB4512941](https://support.microsoft.com/kb/4512941) installed</span></span>
  - <span data-ttu-id="ff1aa-119">Windows 10, version 1809 avec la mise à jour [KB4512534](https://support.microsoft.com/kb/4512534) installée</span><span class="sxs-lookup"><span data-stu-id="ff1aa-119">Windows 10, version 1809 with [KB4512534](https://support.microsoft.com/kb/4512534) installed</span></span>
  - <span data-ttu-id="ff1aa-120">Windows 10, version 1803 avec la mise à jour [KB4512509](https://support.microsoft.com/kb/4512509) installée</span><span class="sxs-lookup"><span data-stu-id="ff1aa-120">Windows 10, version 1803 with [KB4512509](https://support.microsoft.com/kb/4512509) installed</span></span>
  - <span data-ttu-id="ff1aa-121">Windows 10, version 1709 avec la mise à jour [KB4516071](https://support.microsoft.com/kb/4516071) installée</span><span class="sxs-lookup"><span data-stu-id="ff1aa-121">Windows 10, version 1709 with [KB4516071](https://support.microsoft.com/kb/4516071) installed</span></span>

### <a name="use-administrative-templates-to-create-a-policy-for-microsoft-edge"></a><span data-ttu-id="ff1aa-122">Utiliser les modèles d’administration pour créer méthode pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff1aa-122">Use Administrative Templates to create a policy for Microsoft Edge</span></span>

<span data-ttu-id="ff1aa-123">Cette procédure s’inspire des modèles d’administration (que vous avez peut-être utilisés dans la méthode de groupe) intégrés à Intune.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-123">This procedure leverages Administrative templates (which you might be familiar with from Group Policy) that are built into Intune.</span></span> <span data-ttu-id="ff1aa-124">Vous pouvez utiliser ces modèles pour créer une méthode pour Microsoft Edge en sélectionnant les paramètres dans une liste préconfigurée.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-124">You can use these templates to create a policy for Microsoft Edge by selecting settings from a pre-configured list.</span></span>

1. <span data-ttu-id="ff1aa-125">Connectez-vous au portail [Microsoft Endpoint Manager](https://endpoint.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="ff1aa-125">Sign in to the [Microsoft Endpoint Manager](https://endpoint.microsoft.com/) portal.</span></span>
2. <span data-ttu-id="ff1aa-126">Sélectionnez **Appareils** dans le volet gauche de navigation.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-126">Select **Devices** in the left-hand navigation pane.</span></span>
3. <span data-ttu-id="ff1aa-127">De \*\* Appareils \*\* | **Vue d’ensemble**, sélectionner \*\* Profil de Configuration\*\* (sous l’en-tête Méthode).</span><span class="sxs-lookup"><span data-stu-id="ff1aa-127">From **Devices** | **Overview**, select **Configuration Profiles** (under Policy heading).</span></span>
4. <span data-ttu-id="ff1aa-128">Dans la barre de commandes supérieure, sélectionnez **Créer profil**.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-128">On the top command bar, select **Create profile**.</span></span>
5. <span data-ttu-id="ff1aa-129">Dans la liste déroulante ci-dessous **Plateforme**,sélectionner **Windows 10 et ultérieure**.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-129">In the drop-down list below **Platform**, select **Windows 10 and later**.</span></span>
6. <span data-ttu-id="ff1aa-130">Dans la liste déroulante ci-dessous**Profil**,sélectionner **Modèles d’Administration** puis cliquer sur le \*\* bouton \*\*.Créer.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-130">In the drop-down list below **Profile**, select **Administrative Templates** and then click the **Create** button.</span></span> <span data-ttu-id="ff1aa-131">La capture d’écran suivante montre les listes déroulantes permettant de sélectionner la plateforme et le type de profil.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-131">The next screenshot shows the drop-down lists to select the platform and type of profile.</span></span>

    ![Sélectionner une plateforme et un type de profil](./media/configure-edge-with-intune/create-profile-platform.png)

7. <span data-ttu-id="ff1aa-133">Sous l’onglet Notions de Base, entrer un\*\*Nom descriptif \*\*, tel que Méthode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-133">On the **Basics** tab, enter a descriptive **Name**, such as Microsoft Edge Policy.</span></span> <span data-ttu-id="ff1aa-134">Si vous le souhaitez, saisissez une **Description**pour la méthode.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-134">Optionally, enter a  **Description** for the policy.</span></span>
<span data-ttu-id="ff1aa-135">La capture d’écran suivante montre le formulaire de l’onglet **Notions de Base** et la barre de menus affiche les étapes suivantes (sous la forme d’onglets grisés) pour créer le profil.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-135">The next screenshot shows the form for the **Basics** tab and the menu bar shows the next steps (as grayed out tabs) to create the profile.</span></span>

   ![Entrer Nom et Description](./media/configure-edge-with-intune/create-profile-basics-tab.png)

8. <span data-ttu-id="ff1aa-137">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-137">Select **Next**.</span></span>
9. <span data-ttu-id="ff1aa-138">Sous l’onglet **Paramètres de configuration**, sélectionnez le dossier Microsoft Edge dans l’un des emplacements suivants:</span><span class="sxs-lookup"><span data-stu-id="ff1aa-138">On the **Configuration settings** tab, select the Microsoft Edge folder in one of the following locations:</span></span>

   - <span data-ttu-id="ff1aa-139">ci-dessous le dossier Configuration Ordinateur</span><span class="sxs-lookup"><span data-stu-id="ff1aa-139">below the Computer Configuration folder</span></span>
   - <span data-ttu-id="ff1aa-140">ci-dessous le dossier Configuration Utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-140">below the User Configuration folder.</span></span>

   <span data-ttu-id="ff1aa-141">Les paramètres disponibles pour Microsoft Edge s’affichent dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-141">The available settings for Microsoft Edge will be shown on the right pane.</span></span> <span data-ttu-id="ff1aa-142">Par exemple, *Configuration Ordinateur/Microsoft Edge/Autoriser les restrictions de téléchargement* présenté dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-142">For example, *Computer Configuration/Microsoft Edge/Allow download restrictions* shown in the following screenshot.</span></span>

   ![Onglet Paramètres de configuration](./media/configure-edge-with-intune/create-profile-configuration-settings-tab.png)

   > [!NOTE]
   > <span data-ttu-id="ff1aa-144">Consulter [MICROSOFT– Méthodes](./microsoft-edge-policies.md) et [Microsoft Edge– Méthodes de Mises à jour](./microsoft-edge-update-policies.md) pour la liste la plus complète et récente de tous les paramètres disponibles pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-144">See [Microsoft Edge – Policies](./microsoft-edge-policies.md) and [Microsoft Edge – Update policies](./microsoft-edge-update-policies.md) for the most complete and up to date list of all the available settings for Microsoft Edge.</span></span>

10. <span data-ttu-id="ff1aa-145">Utiliser le champ de recherche (« Rechercher pour filtrer les éléments... ») pour trouver un paramètre spécifique que vous voulez configurer.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-145">Use the search field ("Search to filter items ...") to find a specific setting you want to configure.</span></span> <span data-ttu-id="ff1aa-146">Dans cet exemple, la chaîne de recherche est « page d’accueil ».</span><span class="sxs-lookup"><span data-stu-id="ff1aa-146">In this example, the search string is "home page".</span></span> <span data-ttu-id="ff1aa-147">La capture d’écran suivante montre les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-147">The next screenshot shows the search results.</span></span>

    ![Résultats de la recherche](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-search.png)

11. <span data-ttu-id="ff1aa-149">Une fois que vous avez trouvé le paramètre que vous voulez configurer, sélectionnez le pour afficher les valeurs que vous pouvez définir.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-149">After you find the setting you intend to configure, select it to expose the values you can set.</span></span> <span data-ttu-id="ff1aa-150">Dans la capture d’écran suivante, nous avons sélectionné « Configurer l’URL de la page d’accueil » à titre d’exemple.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-150">In the next screenshot, we selected "Configure the home page URL" as an example.</span></span>

    ![Configurer la méthode URL de la page d’accueil](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-edit-pol.png)

12. <span data-ttu-id="ff1aa-152">Activer la méthode et entrez une valeur pour l’URL de la Page d’accueil URL, comme présenté dans la capture d’écran précédente.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-152">Enable the policy and enter a value for the Home page URL, as shown in the previous screenshot.</span></span>

13. <span data-ttu-id="ff1aa-153">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-153">Click **OK**.</span></span> <span data-ttu-id="ff1aa-154">La colonne des paramètres « État » doit apparaître comme « activé », comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-154">The settings "State" column should appear as "Enabled", as shown in the following screenshot example.</span></span>

    ![L’état du paramètre est activé](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-set-enabled.png)

14. <span data-ttu-id="ff1aa-156">Cliquez sur le bouton **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-156">Click the **Next** button.</span></span>

15. <span data-ttu-id="ff1aa-157">Sur l’onglet Indicateurs d’étendue, ajoutez une balise d’étendue si vous le souhaitez, sinon cliquez sur le\*\*bouton \*\* suivant.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-157">On the **Scope tags** tab, add a Scope tag if wanted, otherwise click the **Next** button.</span></span>

16. <span data-ttu-id="ff1aa-158">Sous l’onglet **Assignations**, cliquez sur + sélectionner des groupes à inclure  pour assigner cette méthode au groupe Azure Active Directory (Azure AD) qui contient les appareils ou les utilisateurs auxquels vous voulez assigner ce paramètre de méthode.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-158">On the **Assignments** tab, click **+ Select groups to include** to assign this policy to the Azure Active Directory (Azure AD) group that contains the devices or the users that you want to receive this policy setting.</span></span> <span data-ttu-id="ff1aa-159">Consultez [Assigner les profils d’utilisateur et de périphérique dans Microsoft Intune](/intune/device-profile-assign) pour les informations sur comment assigner le profil à vos groupes d’utilisateurs ou à périphériques Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-159">See [Assign user and device profiles in Microsoft Intune](/intune/device-profile-assign) for information about how to assign the profile to your Azure AD user or device groups.</span></span>

    ![Sélectionner les groupes à inclure](./media/configure-edge-with-intune/create-profile-assignments-tab.png)

17. <span data-ttu-id="ff1aa-161">Cliquez sur le bouton **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-161">Click the **Next** button.</span></span>

18. <span data-ttu-id="ff1aa-162">Sous l’onglet **Révision + créer**, réviser le résumé de vos modifications pour vous assurer qu’il est correct, puis cliquez sur le**bouton**Créer.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-162">On the **Review + create** tab, review the summary of your changes to ensure it's correct and then click the **Create** button.</span></span>

19. <span data-ttu-id="ff1aa-163">La méthode récemment créée (Méthode Microsoft Edge) est présentée dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-163">The newly created policy (Microsoft Edge Policy) is shown in the following screenshot.</span></span>

    ![Sélectionner les groupes à inclure](./media/configure-edge-with-intune/create-profile-new-policy-finished.png)

<span data-ttu-id="ff1aa-165">Pour plus d’informations sur les profils Windows 10, consultez [Utiliser des modèles Windows 10 pour configurer les paramètres de stratégie de groupe dans Microsoft Intune](/intune/administrative-templates-windows).</span><span class="sxs-lookup"><span data-stu-id="ff1aa-165">For more information about Windows 10 profiles, see [Use Windows 10 templates to configure group policy settings in Microsoft Intune](/intune/administrative-templates-windows).</span></span>

## <a name="see-also"></a><span data-ttu-id="ff1aa-166">Articles associés</span><span class="sxs-lookup"><span data-stu-id="ff1aa-166">See also</span></span>

- [<span data-ttu-id="ff1aa-167">Page d’accueil Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="ff1aa-167">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="ff1aa-168">Gérer l’accès web à l’aide de Microsoft Edge avec Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="ff1aa-168">Manage web access by using Microsoft Edge with Microsoft Intune</span></span>](/intune/manage-microsoft-edge)
- [<span data-ttu-id="ff1aa-169">Utilisez les modèles Windows 10 pour configurer les paramètres de stratégie de groupe dans Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="ff1aa-169">Use Windows 10 templates to configure group policy settings in Microsoft Intune</span></span>](/intune/administrative-templates-windows)
- [<span data-ttu-id="ff1aa-170">Déployer Microsoft Edge à l’aide de Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="ff1aa-170">Deploy Microsoft Edge using Microsoft Intune</span></span>](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)