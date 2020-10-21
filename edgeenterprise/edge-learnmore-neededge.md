---
title: Redirection d’InternetExplorer vers MicrosoftEdge pour assurer une compatibilité avec les sites web modernes
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 10/19/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Redirection d’InternetExplorer vers MicrosoftEdge pour assurer une compatibilité avec les sites web modernes
ms.openlocfilehash: ce9e8dabdff25cc3ba375746ec82ddd78b6d7694
ms.sourcegitcommit: cf991cc4bd2e70169902cbda9ddc870d70e31ca2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120519"
---
# <span data-ttu-id="a4823-103">Redirection d’InternetExplorer vers MicrosoftEdge pour assurer une compatibilité avec les sites web modernes</span><span class="sxs-lookup"><span data-stu-id="a4823-103">Redirection from Internet Explorer to Microsoft Edge for compatibility with modern web sites</span></span>

> [!NOTE]
> <span data-ttu-id="a4823-104">Cet article concerne le canal stable MicrosoftEdge version87 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a4823-104">This article applies to Microsoft Edge Stable version 87 or later.</span></span>

## <span data-ttu-id="a4823-105">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="a4823-105">Overview</span></span>

<span data-ttu-id="a4823-106">De nombreux sites web modernes comportent des conceptions incompatibles avec InternetExplorer.</span><span class="sxs-lookup"><span data-stu-id="a4823-106">Many modern websites have designs that are incompatible with Internet Explorer.</span></span> <span data-ttu-id="a4823-107">Chaque fois qu’un utilisateur d’InternetExplorer visite un site public incompatible, il reçoit un message l’informant que le site est incompatible avec son navigateur et qu’il doit basculer manuellement vers un autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="a4823-107">Whenever an Internet Explorer user visits an incompatible public site, they get a message that tells them the site is incompatible with their browser, and they need to manually switch to a different browser.</span></span>

<span data-ttu-id="a4823-108">Vous devez basculer manuellement vers d’autres navigateurs à partir de la version87 du canal stable de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="a4823-108">The need to  manually switch to a different browser changes starting with Microsoft Edge Stable version 87.</span></span>

<span data-ttu-id="a4823-109">Lorsqu’un utilisateur accède à un site incompatible avec InternetExplorer, il est automatiquement redirigé vers MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="a4823-109">When a user goes to a site that is incompatible with Internet Explorer, they will be automatically redirected to Microsoft Edge.</span></span> <span data-ttu-id="a4823-110">Cet article décrit l’expérience utilisateur pour la redirection et les stratégies de groupe utilisées pour configurer ou désactiver la redirection automatique.</span><span class="sxs-lookup"><span data-stu-id="a4823-110">This article describes the user experience for redirection and the group policies that are used to configure or disable automatic redirection.</span></span>

> [!NOTE]
> <span data-ttu-id="a4823-111">Microsoft gère une liste de tous les sites connus comme incompatibles avec InternetExplorer.</span><span class="sxs-lookup"><span data-stu-id="a4823-111">Microsoft maintains a list of all sites that are known to be incompatible with Internet Explorer.</span></span>

## <span data-ttu-id="a4823-112">Expérience de redirection</span><span class="sxs-lookup"><span data-stu-id="a4823-112">Redirection experience</span></span>

<span data-ttu-id="a4823-113">Lors de la redirection vers MicrosoftEdge, une boîte de dialogue ponctuelle s’affiche aux utilisateurs dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="a4823-113">On redirection to Microsoft Edge, users are shown the one-time dialog in the next screenshot.</span></span> <span data-ttu-id="a4823-114">Cette boîte de dialogue explique les raisons de leur redirection et les invite à consentir à la copie de leurs données de navigation et préférences d’InternetExplorer vers MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="a4823-114">This dialog explains why they're getting redirected and prompts for consent to copy their browsing data and preferences from Internet Explorer to Microsoft Edge.</span></span> <span data-ttu-id="a4823-115">Les données de navigation suivantes sont importées: les favoris, mots de passe, moteurs de recherche, onglets ouverts, l’historique, les paramètres, cookies et la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="a4823-115">The following browsing data will be imported: Favorites, Passwords, Search engines, open tabs, History, settings, cookies, and the Home Page.</span></span>

![Notification de navigation et invite à importer les données et les préférences.](media/edge-learnmore-neededge/neededge-dialog1.png)

<span data-ttu-id="a4823-117">Même s’ils n’accordent pas leur consentement en cochant «Toujours récupérer les données et préférences de navigation à partir d’InternetExplorer», les utilisateurs peuvent cliquer sur **Poursuivre la navigation** pour continuer leur session.</span><span class="sxs-lookup"><span data-stu-id="a4823-117">Even if they don't give their consent by checking "Always bring over my browsing data and preferences from Internet Explorer", they can click **Continue browsing** to continue their session.</span></span>

<span data-ttu-id="a4823-118">Enfin, une bannière d’incompatibilité de site web, illustrée dans la capture d’écran suivante, apparaît sous la barre d’adresses lors de chaque redirection.</span><span class="sxs-lookup"><span data-stu-id="a4823-118">Finally, a website incompatibility banner, shown in the next screenshot, appears below the address bar for every redirection.</span></span>

![Notification sur les sites modernes et invite de configuration de MicrosoftEdge en tant que navigateur par défaut ou exploration de MicrosoftEdge.](media/edge-learnmore-neededge/neededge-banner.png)

<span data-ttu-id="a4823-120">Bannière d’incompatibilité du site web:</span><span class="sxs-lookup"><span data-stu-id="a4823-120">The website incompatibility banner:</span></span>

- <span data-ttu-id="a4823-121">encourage l’utilisateur à basculer vers MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="a4823-121">encourages the user to switch to Microsoft Edge</span></span>
- <span data-ttu-id="a4823-122">propose la définition de MicrosoftEdge en tant que navigateur par défaut</span><span class="sxs-lookup"><span data-stu-id="a4823-122">offers to make Microsoft Edge as the default browser</span></span>
- <span data-ttu-id="a4823-123">donne à l’utilisateur la possibilité d’explorer MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="a4823-123">gives the user the option to explore Microsoft Edge</span></span>

<span data-ttu-id="a4823-124">Lors de la redirection d’un site depuis InternetExplorer vers MicrosoftEdge, l’onglet InternetExplorer qui a commencé le chargement du site est fermé s’il ne dispose pas de contenu antérieur.</span><span class="sxs-lookup"><span data-stu-id="a4823-124">When a site is redirected from Internet Explorer to Microsoft Edge, the Internet Explorer tab that started loading the site is closed if it had no prior content.</span></span> <span data-ttu-id="a4823-125">Dans le cas contraire, l’onglet actif permet d’accéder à la page de un support [support](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) de Microsoft qui explique la raison de la redirection du site vers MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="a4823-125">Otherwise, the active tab view goes to a  Microsoft [support](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) page that explains why the site was redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="a4823-126">Après la redirection, les utilisateurs peuvent revenir à l’utilisation d’Internet Explorer pour les sites qui ne figurent pas dans la liste d’incompatibilités d’InternetExplorer.</span><span class="sxs-lookup"><span data-stu-id="a4823-126">After a redirection users can go back to using Internet Explorer for sites that are not on the Internet Explorer incompatibility list.</span></span>  

## <span data-ttu-id="a4823-127">Stratégies de configuration de la redirection vers MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="a4823-127">Policies to configure redirection to Microsoft Edge</span></span>

> [!NOTE]
> <span data-ttu-id="a4823-128">Ces stratégies sont disponibles sous forme de mises à jour de fichiers ADMX à partir du 26octobre2020 et seront disponibles dans Intune d’ici au 9novembre2020.</span><span class="sxs-lookup"><span data-stu-id="a4823-128">These policies will be available as ADMX file updates by October 26, 2020 and will be available in Intune by November 9, 2020.</span></span>

<span data-ttu-id="a4823-129">Trois stratégies de groupe doivent être configurées pour activer la redirection automatique vers MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="a4823-129">Three group policies must be configured to enable automatic redirection to Microsoft Edge.</span></span> <span data-ttu-id="a4823-130">Ces stratégies sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="a4823-130">These policies are:</span></span>

- <span data-ttu-id="a4823-131">RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="a4823-131">RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>
- <span data-ttu-id="a4823-132">RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="a4823-132">RedirectSitesFromInternetExplorerRedirectMode</span></span>
- <span data-ttu-id="a4823-133">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="a4823-133">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

### <span data-ttu-id="a4823-134">Stratégie: RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="a4823-134">Policy: RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>

<span data-ttu-id="a4823-135">La redirection d’InternetExplorer vers MicrosoftEdge nécessite un Objet Application d’assistance du navigateur (BHO) d’InternetExplorer nommé «BHO IEtoEdge».</span><span class="sxs-lookup"><span data-stu-id="a4823-135">Redirection from Internet Explorer to Microsoft Edge requires an Internet Explorer Browser Helper Object (BHO) named "IEtoEdge BHO".</span></span> <span data-ttu-id="a4823-136">La stratégie **RedirectSitesFromInternetExplorerPreventBHOInstall** détermine si cet Objet Application d’assistance du navigateur (BHO) est installé ou non.</span><span class="sxs-lookup"><span data-stu-id="a4823-136">The **RedirectSitesFromInternetExplorerPreventBHOInstall** policy controls whether or not this BHO is installed.</span></span>  

- <span data-ttu-id="a4823-137">Si vous activez cette stratégie, l’Objet Application d’assistance du navigateur (BHO) nécessaire à la redirection ne sera pas installé et vos utilisateurs continueront à voir les messages d’incompatibilité relatifs à certains sites web sur InternetExplorer.</span><span class="sxs-lookup"><span data-stu-id="a4823-137">If you enable this policy, the BHO required for redirection will not be installed and your users will continue to see incompatibility messages for certain websites on Internet Explorer.</span></span> <span data-ttu-id="a4823-138">Si l’Objet Application d’assistance du navigateur (BHO) est déjà installé, il sera désinstallé lors de la prochaine mise à jour du canal stable de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="a4823-138">If the BHO is already installed, it will be uninstalled the next time the Microsoft Edge Stable channel is updated.</span></span>
- <span data-ttu-id="a4823-139">Si vous désactivez ou ne configurez pas cette stratégie, l’Objet Application d’assistance du navigateur (BHO) est installé.</span><span class="sxs-lookup"><span data-stu-id="a4823-139">If you disable or don't configure this policy, the BHO will be installed.</span></span> <span data-ttu-id="a4823-140">Il s’agit du comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="a4823-140">This is the default behavior.</span></span>

<span data-ttu-id="a4823-141">Outre la nécessité de l’Objet Application d’assistance du navigateur (BHO), il existe une dépendance sur **RedirectSitesFromInternetExplorerRedirectMode**, qui doit être défini sur «Liste de sites» ou «Non configuré».</span><span class="sxs-lookup"><span data-stu-id="a4823-141">In addition to needing the BHO, there is a dependency on the **RedirectSitesFromInternetExplorerRedirectMode**, which needs to be set to "Sitelist" or "Not Configured".</span></span>

### <span data-ttu-id="a4823-142">Stratégie: RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="a4823-142">Policy: RedirectSitesFromInternetExplorerRedirectMode</span></span>

 <span data-ttu-id="a4823-143">Cette stratégie correspond au paramètre **Navigateur par défaut** «Laisser InternetExplorer ouvrir les sites dans MicrosoftEdge» de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="a4823-143">This policy corresponds to the Microsoft Edge **Default browser** setting "Let Internet Explorer open sites in Microsoft Edge".</span></span> <span data-ttu-id="a4823-144">Vous pouvez accéder à ce paramètre en accédant à l’URL *edge://settings/defaultbrowser*.</span><span class="sxs-lookup"><span data-stu-id="a4823-144">You can access this setting by going to the *edge://settings/defaultbrowser* URL.</span></span>  

- <span data-ttu-id="a4823-145">Si vous ne configurez pas cette stratégie ou si vous la définissez-la sur «Liste de sites», InternetExplorer redirige les sites incompatibles vers MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="a4823-145">If you don't configure this policy or set it to "Sitelist", Internet Explorer will redirect incompatible sites to Microsoft Edge.</span></span> <span data-ttu-id="a4823-146">Il s’agit du comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="a4823-146">This is the default behavior.</span></span>
- <span data-ttu-id="a4823-147">Si vous désactivez cette stratégie, les sites incompatibles ne sont pas redirigés vers MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="a4823-147">If you disable this policy, incompatible sites aren't redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="a4823-148">Si vous utilisez un appareil personnel non géré par votre organisation, un autre paramètre s’affiche intitulé «Autoriser le chargement de sites en mode InternetExplorer» sous **Compatibilité d’InternetExplorer**.</span><span class="sxs-lookup"><span data-stu-id="a4823-148">If you're on a personal device that isn't  managed by your organization, you'll see another setting named "Allow sites to be loaded in Internet Explorer mode" under **Internet Explorer compatibility**.</span></span>
>
><span data-ttu-id="a4823-149">Si vous utilisez un ordinateur joint à un domaine ou inscrit à la Gestion des appareils mobiles (MDM), cette option ne sera pas visible.</span><span class="sxs-lookup"><span data-stu-id="a4823-149">If you're on a domain joined or Mobile Device Management (MDM) enrolled device, you won't see this option.</span></span>
>
> <span data-ttu-id="a4823-150">Au lieu de cela, si vous voulez laisser vos utilisateurs charger des sites en mode InternetExplorer, vous pouvez le faire en configurant la stratégie [Autoriser le test du mode InternetExplorer](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing).</span><span class="sxs-lookup"><span data-stu-id="a4823-150">Instead, if you want to let your users load sites in Internet Explorer mode, you can do so by configuring the policy [Allow Internet Explorer mode testing](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing).</span></span>

### <span data-ttu-id="a4823-151">Stratégie: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="a4823-151">Policy: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

<span data-ttu-id="a4823-152">Cette stratégie configure l’expérience utilisateur pour la redirection de sites incompatibles vers MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="a4823-152">This policy configures the user experience for incompatible site redirection to Microsoft Edge.</span></span>  

- <span data-ttu-id="a4823-153">Si vous activez cette stratégie, les utilisateurs ne verront jamais la boîte de dialogue de redirection ponctuelle et la bannière de redirection.</span><span class="sxs-lookup"><span data-stu-id="a4823-153">If you enable this policy, users never see the one-time redirection dialog and the redirection banner.</span></span> <span data-ttu-id="a4823-154">Les données du navigateur ou les préférences utilisateur ne sont pas importées.</span><span class="sxs-lookup"><span data-stu-id="a4823-154">No browser data or user preferences are imported.</span></span>
- <span data-ttu-id="a4823-155">Si vous désactivez ou ne configurez pas cette stratégie, la boîte de dialogue de redirection s’affiche lors de la première redirection et la bannière de redirection permanente apparaît pour les sessions commençant par une redirection.</span><span class="sxs-lookup"><span data-stu-id="a4823-155">If you disable or don't configure this policy, the redirection dialog will be shown on the first redirection and the persistent redirection banner will be shown for sessions that start with a redirection.</span></span>

  > [!NOTE]
  > <span data-ttu-id="a4823-156">Les données de navigation utilisateur sont importées chaque fois qu’un utilisateur rencontre une nouvelle redirection.</span><span class="sxs-lookup"><span data-stu-id="a4823-156">User browsing data will be imported every time a user encounters a new redirection.</span></span> <span data-ttu-id="a4823-157">Cela ne se produit toutefois que si l’utilisateur a consenti à l’importation dans la boîte de dialogue de redirection ponctuelle.</span><span class="sxs-lookup"><span data-stu-id="a4823-157">However, this only happens if the user consented to the import on the one-time redirection dialog.</span></span>

## <span data-ttu-id="a4823-158">Désactiver la redirection vers MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="a4823-158">Disable redirection to Microsoft Edge</span></span>

<span data-ttu-id="a4823-159">Si vous voulez désactiver la redirection AVANT de procéder à la mise à jour vers la version87 du canal stable de MicrosoftEdge, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="a4823-159">If you want to disable redirection BEFORE updating to Microsoft Edge Stable version 87, use the following step:</span></span>

1. <span data-ttu-id="a4823-160">Définissez la stratégie **RedirectSitesFromInternetExplorerRedirectMode** sur **Activé**.</span><span class="sxs-lookup"><span data-stu-id="a4823-160">Set the **RedirectSitesFromInternetExplorerRedirectMode** policy to **Enabled**.</span></span> <span data-ttu-id="a4823-161">Ce paramètre arrête la redirection dès que la stratégie prend effet.</span><span class="sxs-lookup"><span data-stu-id="a4823-161">This setting will stop redirecting as soon as the policy takes effect.</span></span>

<span data-ttu-id="a4823-162">Si vous voulez désactiver la redirection APRÈS la mise à jour vers la version87 du canal stable de MicrosoftEdge, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="a4823-162">If you want to disable redirection AFTER updating to Microsoft Edge Stable version 87, use the following steps:</span></span>

1. <span data-ttu-id="a4823-163">Définissez la stratégie **RedirectSitesFromInternetExplorerRedirectMode** sur **Désactivé**.</span><span class="sxs-lookup"><span data-stu-id="a4823-163">Set the **RedirectSitesFromInternetExplorerRedirectMode** policy to **Disabled**.</span></span> <span data-ttu-id="a4823-164">Ce paramètre arrête la redirection dès que la stratégie prend effet.</span><span class="sxs-lookup"><span data-stu-id="a4823-164">This setting will stop redirecting as soon as the policy takes effect.</span></span>
2. <span data-ttu-id="a4823-165">Définissez la stratégie **RedirectSitesFromInternetExplorerPreventBHOInstall** sur **Activé**.</span><span class="sxs-lookup"><span data-stu-id="a4823-165">Set the **RedirectSitesFromInternetExplorerPreventBHOInstall** policy to **Enabled**.</span></span> <span data-ttu-id="a4823-166">Cette opération désinstalle l’Objet Application d’assistance du navigateur (BHO) après la prochaine mise à jour de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="a4823-166">This will uninstall the BHO after the next Microsoft Edge update.</span></span>

## <span data-ttu-id="a4823-167">Voir également</span><span class="sxs-lookup"><span data-stu-id="a4823-167">See also</span></span>

- [<span data-ttu-id="a4823-168">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="a4823-168">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="a4823-169">Stratégies MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="a4823-169">Microsoft Edge Policies</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies)