---
title: Désactiver Internet Explorer 11
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/04/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez comment désactiver Internet Explorer 11 et utiliser le mode Internet Explorer dans Microsoft Edge.
ms.openlocfilehash: be52f33b091977aff0ca29a4e10d4fc6ea4be957
ms.sourcegitcommit: f63a30c3e64e9e57fd76b6675ddff1fc2bbbeac8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "11393614"
---
# <a name="disable-internet-explorer-11"></a><span data-ttu-id="8522b-103">Désactiver Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="8522b-103">Disable Internet Explorer 11</span></span>

<span data-ttu-id="8522b-104">Cet article explique comment désactiver Internet Explorer 11 en tant que navigateur autonome dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="8522b-104">This article describes how to disable Internet Explorer 11 as a standalone browser in your environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8522b-105">Prérequis</span><span class="sxs-lookup"><span data-stu-id="8522b-105">Prerequisites</span></span>

<span data-ttu-id="8522b-106">Les mises à jour Windows et les logiciels Microsoft Edge suivants sont requis :</span><span class="sxs-lookup"><span data-stu-id="8522b-106">The following Windows updates and Microsoft Edge software are required:</span></span>

- <span data-ttu-id="8522b-107">Mises à jour Windows</span><span class="sxs-lookup"><span data-stu-id="8522b-107">Windows updates</span></span>

  - <span data-ttu-id="8522b-108">Windows 10, version 2004, Windows Server version 2004, Windows 10, version 20H2 : [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8522b-108">Windows 10, version 2004, Windows Server version 2004, Windows 10, version 20H2: [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) or later</span></span>
  - <span data-ttu-id="8522b-109">Windows 10 version 1909, Windows Server version 1909 : [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8522b-109">Windows 10 version 1909, Windows Server version 1909: [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) or later</span></span>
  - <span data-ttu-id="8522b-110">Windows 10 version 1809, Windows Server version 1809 et Windows Server 2019 : [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8522b-110">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019: [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) or later</span></span>
  - <span data-ttu-id="8522b-111">Windows 10, version 1607, Windows Server 2016 : [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8522b-111">Windows 10, version 1607, Windows Server 2016: [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) or later</span></span>
   - <span data-ttu-id="8522b-112">Version initiale de Windows 10 (juillet 2015) : [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8522b-112">Windows 10 initial version (July 2015): [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) or later</span></span>
  - <span data-ttu-id="8522b-113">Windows 8.1 : [KB4601384 ou](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) ultérieur</span><span class="sxs-lookup"><span data-stu-id="8522b-113">Windows 8.1: [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) or later</span></span>
  - <span data-ttu-id="8522b-114">Windows Server 2012 : [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) ou ultérieur</span><span class="sxs-lookup"><span data-stu-id="8522b-114">Windows Server 2012: [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) or later</span></span>
  
- <span data-ttu-id="8522b-115">Canal Stable Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8522b-115">Microsoft Edge Stable Channel</span></span>


## <a name="overview"></a><span data-ttu-id="8522b-116">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="8522b-116">Overview</span></span>

<span data-ttu-id="8522b-117">Pour les organisations qui ont besoin d’Internet Explorer 11 (IE11) pour la compatibilité héritée, le mode Internet Explorer (mode IE) sur Microsoft Edge offre une expérience de navigateur unique et transparente.</span><span class="sxs-lookup"><span data-stu-id="8522b-117">For organizations that require Internet Explorer 11 (IE11) for legacy compatibility, Internet Explorer mode (IE mode) on Microsoft Edge provides a seamless, single browser experience.</span></span> <span data-ttu-id="8522b-118">Les utilisateurs peuvent accéder aux applications héritées à partir de Microsoft Edge sans avoir à revenir à IE11.</span><span class="sxs-lookup"><span data-stu-id="8522b-118">Users can access legacy applications from within Microsoft Edge without having to switch back to IE11.</span></span>

<span data-ttu-id="8522b-119">Après avoir configuré le mode Internet Explorer, vous pouvez désactiver Internet Explorer 11 en tant que navigateur autonome**sans affecter les fonctionnalités du mode IE**au sein de votre organisation à l’aide de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8522b-119">After you configure IE mode, you can disable IE11 as a standalone browser **without affecting IE mode functionality** across your organization using group policy.</span></span>

> [!NOTE]
> <span data-ttu-id="8522b-120">Si vous avez besoin de l’application IE11 autonome pour des sites spécifiques et que vous souhaitez rediriger tout le trafic du navigateur vers Microsoft Edge, vous pouvez configurer la stratégie[Envoyer tous les sites non inclus dans la liste des sites vers Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge) pour rediriger les sites d’Internet Explorer vers Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8522b-120">If you need the standalone IE11 app for specific sites, and want to redirect all other browser traffic to Microsoft Edge, you can configure the [Send all sites not included in the site list to Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge) policy to redirect sites from IE to Microsoft Edge.</span></span>

## <a name="user-experience-after-redirecting-traffic-to-microsoft-edge"></a><span data-ttu-id="8522b-121">Expérience utilisateur après la redirection du trafic vers Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8522b-121">User experience after redirecting traffic to Microsoft Edge</span></span>

<span data-ttu-id="8522b-122">Lorsque vous activez la stratégie **Désactiver Internet Explorer 11 en tant que navigateur autonome**, toute l’activité Internet Explorer 11 est redirigée vers Microsoft Edge et les utilisateurs ont l’expérience suivante :</span><span class="sxs-lookup"><span data-stu-id="8522b-122">When you enable the **Disable Internet Explorer 11 as a standalone browser** policy, all IE11 activity is redirected to Microsoft Edge and users have the following experience:</span></span>

- <span data-ttu-id="8522b-123">L’icône IE11 du menu Démarrer sera supprimée, mais celle de la barre des tâches restera.</span><span class="sxs-lookup"><span data-stu-id="8522b-123">The IE11 icon on the Start Menu will be removed, but the one on the taskbar will remain.</span></span>
- <span data-ttu-id="8522b-124">Lorsque les utilisateurs tentent de lancer des raccourcis ou des associations de fichiers qui utilisent IE11, ils sont redirigés pour ouvrir le même fichier/URL dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8522b-124">When users try to launch shortcuts or file associations that use IE11, they will be redirected to open the same file/URL in Microsoft Edge.</span></span>
- <span data-ttu-id="8522b-125">Lorsque les utilisateurs tentent de lancer IE11 en invoquant directement iexplore.exe binaire, Microsoft Edge se lance à la place.</span><span class="sxs-lookup"><span data-stu-id="8522b-125">When users try to launch IE11 by directly invoking the iexplore.exe binary, Microsoft Edge will launch instead.</span></span>

<span data-ttu-id="8522b-126">Dans le cadre de la définition de la stratégie pour cette expérience, vous pouvez éventuellement afficher un message de redirection pour chaque utilisateur qui tente de lancer IE11.</span><span class="sxs-lookup"><span data-stu-id="8522b-126">As part of setting the policy for this experience, you can optionally show a redirect message for each user who tries to launch IE11.</span></span> <span data-ttu-id="8522b-127">Ce message peut être affiché « Toujours » ou « Une fois par utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="8522b-127">This message can be set to display "Always" or "Once per user".</span></span> <span data-ttu-id="8522b-128">Par défaut, le message de redirection affiché dans la capture d’écran suivante n’est jamais affiché.</span><span class="sxs-lookup"><span data-stu-id="8522b-128">By default, the redirect message shown in the next screenshot is never shown.</span></span>

:::image type="content" source="media/edge-ie-disable-ie11/disable-ie-redirect-msg.png" alt-text="Alerte lors de la tentative d’ouverture d’IE après qu’une redirection vers Microsoft Edge est active.":::

<span data-ttu-id="8522b-130">Si votre liste des sites en mode Entreprise contient des applications configurées pour s’ouvrir dans l’application IE11 et que vous désactivez IE11 avec cette stratégie, elles s’ouvrent en mode IE sur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8522b-130">If your Enterprise Mode Site List contains applications that are configured to open in the IE11 app and you disable IE11 with this policy, they will open in IE mode on Microsoft Edge.</span></span>
> [!NOTE]
> <span data-ttu-id="8522b-131">Il existe un problème connu avec le flux d’utilisateurs lorsqu’un site est configuré pour s’ouvrir dans IE11 et que la stratégie désactiver InternetE11 est définie.</span><span class="sxs-lookup"><span data-stu-id="8522b-131">There is a known issue with the user flow when a site is configured to open in IE11 and the disable IE11 policy is set.</span></span> <span data-ttu-id="8522b-132">Ce problème est activement examiné.</span><span class="sxs-lookup"><span data-stu-id="8522b-132">The issue being actively investigated.</span></span>

## <a name="disable-internet-explorer-11-as-a-standalone-browser"></a><span data-ttu-id="8522b-133">Désactiver Internet Explorer 11 en tant que navigateur autonome</span><span class="sxs-lookup"><span data-stu-id="8522b-133">Disable Internet Explorer 11 as a standalone browser</span></span>

<span data-ttu-id="8522b-134">Pour désactiver Internet Explorer 11 à l’aide de la stratégie de groupe, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8522b-134">To disable Internet Explorer 11 using group policy, follow these steps:</span></span>

1. <span data-ttu-id="8522b-135">Téléchargez et installez le dernier [modèle de stratégie Microsoft Edge.](https://www.microsoft.com/edge/business/download)</span><span class="sxs-lookup"><span data-stu-id="8522b-135">Download and install the latest [Microsoft Edge Policy Template](https://www.microsoft.com/edge/business/download).</span></span>
2. <span data-ttu-id="8522b-136">Ouvrez l’Éditeur de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8522b-136">Open the Group Policy Editor.</span></span>
3. <span data-ttu-id="8522b-137">Allez à ***Computer Configuration/Administrative Templates/Windows Components/Internet Explorer***.</span><span class="sxs-lookup"><span data-stu-id="8522b-137">Go to ***Computer Configuration/Administrative Templates/Windows Components/Internet Explorer***.</span></span> 
4. <span data-ttu-id="8522b-138">Double-cliquez **Désactiver Internet Explorer 11 en tant que navigateur autonome**.</span><span class="sxs-lookup"><span data-stu-id="8522b-138">Double-click **Disable Internet Explorer 11 as a standalone browser**.</span></span>
5. <span data-ttu-id="8522b-139">Sélectionnez **Activé.**</span><span class="sxs-lookup"><span data-stu-id="8522b-139">Select **Enabled**.</span></span>
6. <span data-ttu-id="8522b-140">Sous **Options,** sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8522b-140">Under **Options**, pick one of the following values:</span></span>

   - <span data-ttu-id="8522b-141">**Jamais**   si vous ne souhaitez pas informer les utilisateurs qu’IE11 est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8522b-141">**Never** if you don’t want to notify users that IE11 is disabled.</span></span>
   - <span data-ttu-id="8522b-142">**Toujours**   si vous souhaitez avertir les utilisateurs chaque fois qu’ils sont redirigés à partir d’Internet IE11.</span><span class="sxs-lookup"><span data-stu-id="8522b-142">**Always** if you want to notify users every time they're redirected from IE11.</span></span>
   - <span data-ttu-id="8522b-143">**Une fois par utilisateur**   si vous souhaitez avertir les utilisateurs uniquement la première fois qu’ils sont redirigés.</span><span class="sxs-lookup"><span data-stu-id="8522b-143">**Once per user** if you want to notify users only the first time they are redirected.</span></span>

7. <span data-ttu-id="8522b-144">Cliquez \*\* OK** ou  **Appliquez\*\*   pour enregistrer ce paramètre de stratégie.</span><span class="sxs-lookup"><span data-stu-id="8522b-144">Click **OK** or **Apply** to save this policy setting.</span></span>

## <a name="see-also"></a><span data-ttu-id="8522b-145">Voir également</span><span class="sxs-lookup"><span data-stu-id="8522b-145">See also</span></span>

- [<span data-ttu-id="8522b-146">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="8522b-146">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="8522b-147">À propos du mode Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="8522b-147">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="8522b-148">Informations supplémentaires sur le mode entreprise</span><span class="sxs-lookup"><span data-stu-id="8522b-148">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
