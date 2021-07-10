---
title: Edge pour l’infrastructure de bureau de virtualisation
ms.author: anlake
author: AndreaLBarr
manager: collw
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge pour l’infrastructure bureau virtualisée.
ms.openlocfilehash: 5dc234b0e6fbba4778f8236399a0ff438f704578
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641850"
---
# <a name="microsoft-edge-for-virtualized-desktop-infrastructure"></a><span data-ttu-id="e0fe8-103">Microsoft Edge pour l’infrastructure bureau virtualisée</span><span class="sxs-lookup"><span data-stu-id="e0fe8-103">Microsoft Edge for Virtualized Desktop Infrastructure</span></span>

<span data-ttu-id="e0fe8-104">Cet article décrit les exigences et les limitations relatives à l’utilisation de Microsoft Edge dans un environnement virtualisé.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-104">This article describes the requirements and limitations for using Microsoft Edge in a virtualized environment.</span></span>

## <a name="what-is-vdi"></a><span data-ttu-id="e0fe8-105">Qu’est-ce que VDI ?</span><span class="sxs-lookup"><span data-stu-id="e0fe8-105">What is VDI?</span></span>

<span data-ttu-id="e0fe8-106">L’infrastructure VDI (Virtual Desktop Infrastructure) est une technologie de virtualisation qui héberge un système d’exploitation de bureau et des applications sur un serveur centralisé dans un centre de données.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-106">Virtual Desktop Infrastructure (VDI) is virtualization technology that hosts a desktop operating system and applications on a centralized server in a data center.</span></span> <span data-ttu-id="e0fe8-107">Cela permet aux utilisateurs d’avoir une expérience de bureau entièrement personnalisée avec une source centralisée entièrement sécurisée et conforme.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-107">This enables a fully personalized desktop experience for users with a fully secured and compliant centralized source.</span></span>

<span data-ttu-id="e0fe8-108">Microsoft Edge peut être utilisé dans un environnement virtualisé de la même manière que sur l’appareil local, tout en s’exécutant à partir d’un environnement serveur sécurisé et contrôlé.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-108">Microsoft Edge can be used in such a virtualized environment in much the same ways as it can be used on the local device, all the while running from secure and controlled server environment.</span></span> <span data-ttu-id="e0fe8-109">En fonction de votre solution VDI choisie, il peut également être possible de donner à vos utilisateurs un accès transparent aux sites et applications intranet.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-109">Depending on your chosen VDI solution it may also be possible to give your users seamless access to intranet Applications and Sites.</span></span>

<span data-ttu-id="e0fe8-110">La plupart des fonctionnalités de Edge sont prises en charge dans les environnements VDI sans configuration spéciale.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-110">Most features of Edge are supported on VDI environments without any special configuration.</span></span> <span data-ttu-id="e0fe8-111">Toutefois, pour garantir une expérience optimale, il est recommandé de suivre les instructions ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-111">However, to ensure an optimal experience it’s recommended to follow the guidance below.</span></span>

## <a name="platforms-certified-for-edge"></a><span data-ttu-id="e0fe8-112">Plateformes certifiées pour Edge</span><span class="sxs-lookup"><span data-stu-id="e0fe8-112">Platforms certified for Edge</span></span>

- <span data-ttu-id="e0fe8-113">Azure Virtual Desktop</span><span class="sxs-lookup"><span data-stu-id="e0fe8-113">Azure Virtual Desktop</span></span>
- <span data-ttu-id="e0fe8-114">Citrix Virtual Apps and Desktops (anciennement XenApp et XenDesktop)</span><span class="sxs-lookup"><span data-stu-id="e0fe8-114">Citrix Virtual Apps and Desktops (formerly known as XenApp and XenDesktop)</span></span>

<span data-ttu-id="e0fe8-115">Bien que d’autres solutions VDI n’ont pas encore été vérifiées par l’équipe Edge, il est prévu que les flux de travail les plus courants dans Edge soient pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-115">While other VDI solutions have not yet been verified by the Edge team, it is expected that the most common workflows in Edge should be supported.</span></span> <span data-ttu-id="e0fe8-116">Les conseils fournis ci-dessous peuvent s’appliquer ou non à la solution que vous avez choisie.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-116">Guidance provided below may or may not be applicable to your chosen solution.</span></span>

## <a name="edge-on-vdi-performance-considerations"></a><span data-ttu-id="e0fe8-117">Considérations des performances Edge sur VDI</span><span class="sxs-lookup"><span data-stu-id="e0fe8-117">Edge on VDI performance considerations</span></span>

<span data-ttu-id="e0fe8-118">Lors de la conception de votre environnement VDI, vous devez considérer attentivement les flux de travail et les besoins de vos utilisateurs pour obtenir des performances optimales, ainsi que les limites de votre configuration de serveur.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-118">When designing your VDI environment you should carefully consider the workflows and needs of your users to achieve optimal performance, as well as the limits of your server configuration.</span></span>

<span data-ttu-id="e0fe8-119">Edge recommande les exigences minimales suivantes pour le déploiement d’Edge dans des environnements VDI :</span><span class="sxs-lookup"><span data-stu-id="e0fe8-119">Edge recommends the following minimal requirements for deploying Edge to VDI environments:</span></span>

- <span data-ttu-id="e0fe8-120">vCPU – 2 à 4 cœurs par utilisateur</span><span class="sxs-lookup"><span data-stu-id="e0fe8-120">vCPU – 2-4 Cores per User</span></span>
- <span data-ttu-id="e0fe8-121">RAM – 1 Go par utilisateur</span><span class="sxs-lookup"><span data-stu-id="e0fe8-121">RAM – 1 GB per User</span></span>

<span data-ttu-id="e0fe8-122">Notez que les extensions et les applications web complexes de grande taille nécessitent davantage de mémoire et doivent être prises en compte lors de la configuration de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-122">Please note that large complex web applications and extensions will require more memory and will have to be accounted for when configuring your environment.</span></span>

## <a name="edge-on-non-persisted-vdi-environments"></a><span data-ttu-id="e0fe8-123">Edge sur les environnements VDI non persistants</span><span class="sxs-lookup"><span data-stu-id="e0fe8-123">Edge on non-persisted VDI environments</span></span>

<span data-ttu-id="e0fe8-124">De nombreuses solutions VDI permettent d’accéder à des environnements persistants, où les utilisateurs se voit attribuer un environnement virtuel qui persiste entre les sessions et des environnements non persistants, où les utilisateurs sont affectés à l’un des ordinateurs disponibles, éventuellement à un autre ordinateur chaque session, les données utilisateur peuvent ou non se synchroniser entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-124">Many VDI solutions allow access to persisted environments, where users are assigned a virtual environment that persists between sessions, and non-persisted environments, where users are assigned to one of several available machines, possibly a different machine each session, user data may or may not sync between sessions.</span></span>

<span data-ttu-id="e0fe8-125">Lorsque vous utilisez un environnement non persistant, on crée généralement une « image de base » qui est utilisée pour chaque appareil qui inclut les applications et configurations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-125">When using a non-persisted environment, one usually creates a “golden image” which is used for each device that includes the needed apps and configurations.</span></span> <span data-ttu-id="e0fe8-126">Voici nos recommandations pour préparer Edge pour une telle image.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-126">Below are our recommendations for preparing Edge for such an image.</span></span>

### <a name="deploy-edge"></a><span data-ttu-id="e0fe8-127">Déployer Edge</span><span class="sxs-lookup"><span data-stu-id="e0fe8-127">Deploy Edge</span></span>

<span data-ttu-id="e0fe8-128">Si vous êtes sur Windows 10 version 1803 et supérieure, vous devez avoir installé Microsoft Edge sur votre système.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-128">If you are on Windows 10, version 1803 and above, you should have Microsoft Edge installed on your system.</span></span> <span data-ttu-id="e0fe8-129">Toutefois, si vous êtes sur une version antérieure de Windows ou que vous souhaitez déployer un autre canal d’Edge, les étapes suivantes sont recommandées.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-129">However, if you are on an older version of Windows or wish to deploy a different channel of Edge, the following steps are recommended.</span></span>

1. <span data-ttu-id="e0fe8-130">Téléchargez le package Edge MSI correspondant au système d’exploitation de votre machine virtuelle VDI à partir de :</span><span class="sxs-lookup"><span data-stu-id="e0fe8-130">Download the Edge MSI package matching your VDI VM operating system from:</span></span>

    - [<span data-ttu-id="e0fe8-131">Télécharger Microsoft Edge pour les entreprises – Microsoft</span><span class="sxs-lookup"><span data-stu-id="e0fe8-131">Download Microsoft Edge for Business - Microsoft</span></span>](https://www.microsoft.com/edge/business/download)

2. <span data-ttu-id="e0fe8-132">Installez MSI sur la machine virtuelle VDI en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e0fe8-132">Install the MSI to the VDI VM by running the following command:</span></span>

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### <a name="disable-automatic-updates"></a><span data-ttu-id="e0fe8-133">Désactiver les mises à jour automatiques</span><span class="sxs-lookup"><span data-stu-id="e0fe8-133">Disable automatic updates</span></span>

<span data-ttu-id="e0fe8-134">Pour les ordinateurs non persistants, il est préférable de désactiver les mises à jour automatiques et de mettre à jour Edge en mettant à jour l'« image de base » pour s’assurer qu’il n’y a pas de version non correspondante parmi le groupe d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-134">For non-persisted machines it is best practice to disable automatic updates and instead update Edge by updating the “golden image” to ensure that there are no version mismatches among the pool of machines.</span></span>

<span data-ttu-id="e0fe8-135">Consultez les stratégies suivantes pour désactiver les mises à jour automatiques :</span><span class="sxs-lookup"><span data-stu-id="e0fe8-135">See the following policies for disabling automatic updates:</span></span>

- [<span data-ttu-id="e0fe8-136">Remplacer la stratégie de mise à jour par défaut</span><span class="sxs-lookup"><span data-stu-id="e0fe8-136">Update policy override default</span></span>](/deployedge/microsoft-edge-update-policies#updatedefault)

- [<span data-ttu-id="e0fe8-137">Remplacer la stratégie de mise à jour</span><span class="sxs-lookup"><span data-stu-id="e0fe8-137">Update policy override</span></span>](/deployedge/microsoft-edge-update-policies#update)

### <a name="profile-management"></a><span data-ttu-id="e0fe8-138">Gestion des profils</span><span class="sxs-lookup"><span data-stu-id="e0fe8-138">Profile management</span></span>

<span data-ttu-id="e0fe8-139">Sur les configurations non persistantes, il est important de prendre en compte le fait que les ordinateurs virtuels peuvent ne pas maintenir l’état utilisateur entre les sessions ou qu’un ordinateur personnel qu’ils n’ont jamais utilisé auparavant peut ne pas avoir de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-139">On non-persisted setups it is important to consider that VMs may not maintain user state between sessions or users may be assigned a VM they have never used before and as such has none of their user data.</span></span>

<span data-ttu-id="e0fe8-140">Edge prend en charge plusieurs méthodes de synchronisation des données utilisateur de telle manière qu’elles soient disponibles, quelle que soit la façon dont ils accèdent à Edge.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-140">Edge supports several methods for syncing user data such that it is available regardless of how they are accessing Edge.</span></span>

### <a name="azure-ad-sync"></a><span data-ttu-id="e0fe8-141">Azure AD Sync</span><span class="sxs-lookup"><span data-stu-id="e0fe8-141">Azure AD Sync</span></span>

<span data-ttu-id="e0fe8-142">Si votre plan Azure AD le prend en charge, la synchronisation Entreprise est la méthode la plus rapide et la plus simple pour vous assurer que les données utilisateur Edge sont synchronisées avec tous les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-142">If your Azure AD plan supports it, Enterprise sync is the fastest and easiest method to ensure that Edge user data is synced to all user devices.</span></span>  

<span data-ttu-id="e0fe8-143">Pour plus d’informations sur les conditions requises et la configuration, voir les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-143">See the following for more information on requirements and configuration.</span></span>  

- [<span data-ttu-id="e0fe8-144">Configurer la synchronisation Microsoft Edge Entreprise | Microsoft Docs</span><span class="sxs-lookup"><span data-stu-id="e0fe8-144">Configure Microsoft Edge enterprise sync | Microsoft Docs</span></span>](/deployedge/microsoft-edge-enterprise-sync)

### <a name="on-premise-sync-for-active-directory-users"></a><span data-ttu-id="e0fe8-145">Synchronisation sur site pour les utilisateurs Active Directory</span><span class="sxs-lookup"><span data-stu-id="e0fe8-145">On-premise Sync for Active Directory Users</span></span>

<span data-ttu-id="e0fe8-146">Avec la synchronisation sur site, Microsoft Edge enregistre les favoris et les paramètres d’un utilisateur Active Directory dans un fichier qui peut facilement être déplacé entre différents ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-146">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can easily be moved between different computers.</span></span>  

<span data-ttu-id="e0fe8-147">Pour plus d’informations sur les conditions requises et la configuration, voir les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-147">See the following for more information on requirements and configuration.</span></span>  

- [<span data-ttu-id="e0fe8-148">Synchronisation locale pour les utilisateurs Active Directory (AD) | Microsoft Docs</span><span class="sxs-lookup"><span data-stu-id="e0fe8-148">On-premises sync for Active Directory (AD) users | Microsoft Docs</span></span>](/deployedge/microsoft-edge-on-premises-sync)

### <a name="user-profile-redirection"></a><span data-ttu-id="e0fe8-149">Redirection de profil utilisateur</span><span class="sxs-lookup"><span data-stu-id="e0fe8-149">User Profile Redirection</span></span>  

<span data-ttu-id="e0fe8-150">Il existe plusieurs solutions pour migrer et rediriger l’intégralité du dossier utilisateur afin de garantir que le contexte utilisateur est conservé dans ces environnements non persistants.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-150">There are several solutions for migrating and redirecting the entire user folder to ensure that user context is maintained in such non-persisted environments.</span></span> <span data-ttu-id="e0fe8-151">Consultez votre fournisseur VDI pour déterminer la solution recommandée.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-151">Check with your VDI provider to determine the recommended solution.</span></span>

<span data-ttu-id="e0fe8-152">Voici quelques solutions populaires :</span><span class="sxs-lookup"><span data-stu-id="e0fe8-152">Some popular solutions include:</span></span>

- [<span data-ttu-id="e0fe8-153">Vue d’ensemble de FSLogix – FSLogix | Microsoft Docs</span><span class="sxs-lookup"><span data-stu-id="e0fe8-153">FSLogix Overview - FSLogix | Microsoft Docs</span></span>](/fslogix/overview)
- [<span data-ttu-id="e0fe8-154">Comment configurer la gestion des profils Citrix</span><span class="sxs-lookup"><span data-stu-id="e0fe8-154">How to Configure Citrix Profile Management</span></span>](https://support.citrix.com/article/CTX222893)

<span data-ttu-id="e0fe8-155">Il est également recommandé d’exclure, lors de l’utilisation de cette méthode, les dossiers inutiles du dossier utilisateur sauvegardé afin de réduire les temps de chargement initiaux lorsque les utilisateurs se connectent à un ordinateur et que le profil est en cours de migration.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-155">It is also may be recommended that when using this method unnecessary folders be excluded from the backed-up user folder to reduce initial loading times when users are logging on to a machine and the profile is being migrated.</span></span> <span data-ttu-id="e0fe8-156">Si c’est le cas, nous vous recommandons d’exclure les dossiers suivants de votre sauvegarde pour réduire la taille.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-156">If so, we recommend the following folders be excluded from your backup to reduce size.</span></span>

- <span data-ttu-id="e0fe8-157">%LocalAppData%\Microsoft\Edge\User Data\Default\Cache</span><span class="sxs-lookup"><span data-stu-id="e0fe8-157">%LocalAppData%\Microsoft\Edge\User Data\Default\Cache</span></span>
- <span data-ttu-id="e0fe8-158">%LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache</span><span class="sxs-lookup"><span data-stu-id="e0fe8-158">%LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache</span></span>
- <span data-ttu-id="e0fe8-159">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites</span><span class="sxs-lookup"><span data-stu-id="e0fe8-159">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites</span></span>
- <span data-ttu-id="e0fe8-160">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed</span><span class="sxs-lookup"><span data-stu-id="e0fe8-160">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed</span></span>

## <a name="known-issues"></a><span data-ttu-id="e0fe8-161">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="e0fe8-161">Known issues</span></span>

### <a name="microsoft-edge-crashes-in-older-versions-of-xenapp-and-xendesktop"></a><span data-ttu-id="e0fe8-162">Microsoft Edge se bloque dans les versions antérieures de XenApp et XenDesktop</span><span class="sxs-lookup"><span data-stu-id="e0fe8-162">Microsoft Edge crashes in older versions of XenApp and XenDesktop</span></span>

<span data-ttu-id="e0fe8-163">Ce problème doit être corrigé dans les versions plus récentes. Cependant, si vous rencontrez ce problème dans votre environnement, vous pouvez le contourner en désactivant les Hooks d’API Citrix pour Edge. Consultez [Comment désactiver les hooks d’API Citrix par application.](https://support.citrix.com/article/CTX107825)</span><span class="sxs-lookup"><span data-stu-id="e0fe8-163">This issue should be mitigated in newer versions however if you are encountering this issue in your environment, you can work around the issue by disabling Citrix API Hooks for Edge, see [How to Disable Citrix API Hooks on a Per-application Basis.](https://support.citrix.com/article/CTX107825)</span></span>

### <a name="degraded-performance-when-rendering-pages-with-exceptionally-large-html-tables"></a><span data-ttu-id="e0fe8-164">Performances dégradées lors du rendu de pages avec des tableaux HTML exceptionnellement grands</span><span class="sxs-lookup"><span data-stu-id="e0fe8-164">Degraded performance when rendering pages with exceptionally large HTML tables</span></span>

<span data-ttu-id="e0fe8-165">Les stratégies Citrix suivantes sont connues pour ralentir le rendu des pages html avec des tableaux très grands (plus de 30 000 lignes).</span><span class="sxs-lookup"><span data-stu-id="e0fe8-165">The following Citrix policies are known to slow rendering of html pages with very large (30,000+ row) tables.</span></span>

- <span data-ttu-id="e0fe8-166">Affichage automatique du clavier</span><span class="sxs-lookup"><span data-stu-id="e0fe8-166">Automatic keyboard display</span></span>
- <span data-ttu-id="e0fe8-167">Distant du contrôle zone de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="e0fe8-167">Remote the combo box</span></span>

<span data-ttu-id="e0fe8-168">Voir [paramètres de stratégie d’expérience mobile (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-168">See [Mobile experience policy settings (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) for more information.</span></span> <span data-ttu-id="e0fe8-169">La désactivation de ces stratégies doit atténuer le problème.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-169">Disabling these policies should mitigate the issue.</span></span>

### <a name="windows-account-manager-authorization-scenarios-ie--azure-sync-fail-in-edge-when-run-as-a-citrix-seamless-application"></a><span data-ttu-id="e0fe8-170">Les scénarios d’autorisation Windows Account Manger (c’est-à-dire,  la synchronisation) sont en échec dans Edge lorsqu’ils sont exécutés en tant qu’application transparente Citrix</span><span class="sxs-lookup"><span data-stu-id="e0fe8-170">Windows Account Manager authorization scenarios (i.e.  Azure sync) fail in Edge when run as a Citrix seamless application</span></span>

<span data-ttu-id="e0fe8-171">Il s’agit d’un problème connu dans Edge et dans d’autres applications qui utilisent WAM (c’est-à-dire, Office) en raison des composants Windows nécessaires pour ces scénarios qui ne sont pas initialisés lors de l’exécution en mode « transparent ».</span><span class="sxs-lookup"><span data-stu-id="e0fe8-171">This is a known issue in Edge and other applications that use WAM (i.e. Office) due to Windows components necessary for such scenarios not being initialized when running in the “seamless” mode.</span></span> <span data-ttu-id="e0fe8-172">Pour contourner ce problème :</span><span class="sxs-lookup"><span data-stu-id="e0fe8-172">To work around this issue:</span></span>

- <span data-ttu-id="e0fe8-173">Utilisez Edge via un Bureau à distance vers l’hôte Citrix au lieu d’une application distante transparente.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-173">Use Edge via a Remote Desktop to the Citrix Host instead of as a seamless remote application.</span></span>
- <span data-ttu-id="e0fe8-174">Utilisez plutôt les applications distantes Azure Virtual Desktop, qui ont des atténuations pour ce problème.</span><span class="sxs-lookup"><span data-stu-id="e0fe8-174">Use Azure Virtual Desktop remote apps instead, which has mitigation's for this issue.</span></span>
