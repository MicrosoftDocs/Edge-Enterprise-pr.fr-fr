---
title: Synchronisation locale pour les utilisateurs de Active Directory (AD)
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 08/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Synchronisation locale pour les utilisateurs de Active Directory (AD)
ms.openlocfilehash: 89f061072fdaa748d317ca8dc0c290893cfdfd6c
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979832"
---
# <span data-ttu-id="f422a-103">Synchronisation locale pour les utilisateurs de Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="f422a-103">On-premises sync for Active Directory (AD) users</span></span>

<span data-ttu-id="f422a-104">Cet article explique comment les utilisateurs d’Active Directory (AD) peuvent parcourir les favoris et paramètres entre les ordinateurs sans se connecter aux services Cloud de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f422a-104">This article explains how Active Directory (AD) users can roam Microsoft Edge favorites and settings between computers without connecting to Microsoft cloud services.</span></span>

> [!NOTE]
> <span data-ttu-id="f422a-105">Cet article concerne MicrosoftEdge version85 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f422a-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <span data-ttu-id="f422a-106">Introduction</span><span class="sxs-lookup"><span data-stu-id="f422a-106">Introduction</span></span>

<span data-ttu-id="f422a-107">La synchronisation des données d’utilisateur dans Microsoft Edge nécessite normalement un compte Microsoft ou un compte Azure Active Directory (Azure AD), ainsi qu’une connexion aux services Cloud de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f422a-107">Syncing user data in Microsoft Edge normally requires either a Microsoft Account or an Azure Active Directory (Azure AD) account, and a connection to Microsoft cloud services.</span></span> <span data-ttu-id="f422a-108">Avec la synchronisation locale, Microsoft Edge enregistre les favoris et paramètres d’un utilisateur d’Active Directory dans un fichier qui peut être transféré entre différents ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="f422a-108">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can be moved between different computers.</span></span> <span data-ttu-id="f422a-109">La synchronisation locale n’interfère pas avec la synchronisation Cloud pour les profils qui l’autorisent.</span><span class="sxs-lookup"><span data-stu-id="f422a-109">On-premises sync doesn't interfere with cloud syncing for those profiles that allow it.</span></span>

## <span data-ttu-id="f422a-110">Fonctionnement</span><span class="sxs-lookup"><span data-stu-id="f422a-110">How it works</span></span>

<span data-ttu-id="f422a-111">Microsoft Edge permet aux profils d’être associés à des comptes Active Directory (AD), qui ne peuvent pas être utilisés avec la synchronisation cloud. Lorsque la synchronisation locale est activée, les données du profil AD sont enregistrées dans un fichier nommé profil.pb.</span><span class="sxs-lookup"><span data-stu-id="f422a-111">Microsoft Edge allows profiles to be associated with Active Directory (AD) accounts, which can't be used with cloud sync. When on-premises sync is enabled, the data from the AD profile is saved to a file named profile.pb.</span></span> <span data-ttu-id="f422a-112">Par défaut, ce fichier est stocké dans \* %APP_DATA%/Microsoft/Edge\*.</span><span class="sxs-lookup"><span data-stu-id="f422a-112">By default, this file is stored in *%APP_DATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="f422a-113">Une fois ce fichier écrit, il peut être transféré entre différents ordinateurs, et les données d’utilisateur sont lues et écrites sur chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f422a-113">After this file is written, it can be moved between different computers, and user data will be read and written on each computer.</span></span>

## <span data-ttu-id="f422a-114">Utiliser la synchronisation locale</span><span class="sxs-lookup"><span data-stu-id="f422a-114">Use on-premises sync</span></span>

<span data-ttu-id="f422a-115">Pour utiliser la synchronisation locale, vous devez l’activer, associer un profil à un compte AD, et éventuellement, changer l’emplacement des données d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f422a-115">To use on-premises sync, you have to enable it, associate a profile with an AD account, and optionally, change the location of the user data.</span></span>

### <span data-ttu-id="f422a-116">Activer la synchronisation locale</span><span class="sxs-lookup"><span data-stu-id="f422a-116">Enable on-premises sync</span></span>

<span data-ttu-id="f422a-117">Pour activer la synchronisation locale dans Microsoft Edge, configurez la stratégie de [ParcourirSupportduProfilActivé](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled).</span><span class="sxs-lookup"><span data-stu-id="f422a-117">To enable on-premises sync in Microsoft Edge, configure the [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled) policy.</span></span>

### <span data-ttu-id="f422a-118">Vérifier qu’un profil est associé à un compte Active Directory</span><span class="sxs-lookup"><span data-stu-id="f422a-118">Ensure that a profile is associated with an Active Directory account</span></span>

<span data-ttu-id="f422a-119">La synchronisation locale fonctionne uniquement avec le profil associé à un compte Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="f422a-119">On-premises sync only works with the profile associated with an Active Directory (AD) account.</span></span> <span data-ttu-id="f422a-120">Si aucun profil de ce type n’existe, la synchronisation locale ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="f422a-120">If no such profile exists, on-premises sync will not function.</span></span> <span data-ttu-id="f422a-121">Pour vous assurer que les utilisateurs se connectent à l’aide d’un compte AD, configurez la stratégie de [ConfigurerlaConnexionAutomatiqueauCompteLocale](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin).</span><span class="sxs-lookup"><span data-stu-id="f422a-121">To ensure that users sign on with an AD account, configure the [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin) policy.</span></span>

### <span data-ttu-id="f422a-122">Changer l’emplacement des données d’utilisateur (facultatif)</span><span class="sxs-lookup"><span data-stu-id="f422a-122">Change the location of the user data (optional)</span></span>

<span data-ttu-id="f422a-123">Par défaut, les données d’utilisateur sont stockées dans un fichier nommé**profil.pb** dans \* %APP_DATA%/Microsoft/Edge\*.</span><span class="sxs-lookup"><span data-stu-id="f422a-123">By default, the user data is stored in a filed named **profile.pb** in *%APP_DATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="f422a-124">Pour changer l’emplacement de ce fichier, configurez la stratégie [Parcourirl’EmplacementduProfil](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation).</span><span class="sxs-lookup"><span data-stu-id="f422a-124">To change the location of this file, configure the [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation) policy.</span></span>

## <span data-ttu-id="f422a-125">Modifications apportées à l’expérience d’utilisateur lorsque la synchronisation locale est activée</span><span class="sxs-lookup"><span data-stu-id="f422a-125">Changes in the user experience when on-premises sync is enabled</span></span>

<span data-ttu-id="f422a-126">Lorsque la synchronisation locale est activée, les utilisateurs ne sont pas invités à activer la synchronisation. De plus, les utilisateurs ne peuvent pas désactiver la synchronisation dans les paramètres de synchronisation et ils ne peuvent pas activer les types de synchronisation qui ne sont pas pris en charge par la synchronisation locale.</span><span class="sxs-lookup"><span data-stu-id="f422a-126">When on-premises sync is enabled, users won't be asked to enable sync. In addition, users can't turn off sync in Sync settings, and they can't turn on sync types that aren't supported by on-premises sync.</span></span>

## <span data-ttu-id="f422a-127">Notes d’utilisation de la synchronisation locale</span><span class="sxs-lookup"><span data-stu-id="f422a-127">On-premises sync usage notes</span></span>

### <span data-ttu-id="f422a-128">Exécution de la synchronisation cloud et de la synchronisation locale sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="f422a-128">Running cloud sync and on-premises sync on the same computer</span></span>

<span data-ttu-id="f422a-129">La synchronisation locale n’interfère pas avec la synchronisation cloud. Si Microsoft Edge possède plusieurs comptes Microsoft ou des profils Azure Active Directory synchronisés avec le cloud, ceux-ci continuent d’être synchronisés pendant que la synchronisation locale est activée.</span><span class="sxs-lookup"><span data-stu-id="f422a-129">On-premises sync doesn't interfere with cloud sync. If Microsoft Edge has multiple Microsoft Account or Azure Active Directory profiles that sync to the cloud, these profiles will continue to sync while on-premises sync is enabled.</span></span>

### <span data-ttu-id="f422a-130">Il n’est pas recommandé d’utiliser Microsoft Edge sur plusieurs ordinateurs à la fois</span><span class="sxs-lookup"><span data-stu-id="f422a-130">Running Microsoft Edge on more than one computer at a time isn't recommended</span></span>

<span data-ttu-id="f422a-131">Étant donné que la synchronisation locale fonctionne en transférant un fichier de données d’utilisateur entre les ordinateurs, la synchronisation locale ne synchronise pas les modifications entre les sessions simultanées.</span><span class="sxs-lookup"><span data-stu-id="f422a-131">Because on-premises sync works by moving a user data file between computers, on-premises sync doesn't sync changes between simultaneous sessions.</span></span> <span data-ttu-id="f422a-132">Pour cette raison, la synchronisation locale fonctionne de manière optimale lorsqu’elle est utilisée sur un ordinateur à la fois.</span><span class="sxs-lookup"><span data-stu-id="f422a-132">For this reason, on-premises sync works best when used on one computer at a time.</span></span> <span data-ttu-id="f422a-133">Lorsque des sessions simultanées locales sont exécutées, les données sur les ordinateurs peuvent être écrasées de manière inattendue par les données d’un autre ordinateur lors du prochain démarrage d’une session de navigateur.</span><span class="sxs-lookup"><span data-stu-id="f422a-133">If there are simultaneous on-premises sessions running, data on any of the computers may be unexpectedly overwritten by data from another computer the next time you start a browser session.</span></span>

> [!NOTE]
> <span data-ttu-id="f422a-134">Microsoft Edge verrouille le fichier **profil.pb** lorsque la synchronisation locale est activée.</span><span class="sxs-lookup"><span data-stu-id="f422a-134">Microsoft Edge locks the **profile.pb** file when on-premises sync is enabled.</span></span> <span data-ttu-id="f422a-135">Si la redirection de dossiers est utilisée pour partager un fichier unique **profil.pb** entre différents ordinateurs, une seule instance de Microsoft Edge utilisant ce fichier peut être alors démarrée.</span><span class="sxs-lookup"><span data-stu-id="f422a-135">If folder redirection is used to share a single **profile.pb** file between different computers, then only one instance of Microsoft Edge using that file can be started.</span></span>

### <span data-ttu-id="f422a-136">Utiliser d’autres stratégies de synchronisation avec la synchronisation locale</span><span class="sxs-lookup"><span data-stu-id="f422a-136">Using other sync policies with on-premises sync</span></span>

<span data-ttu-id="f422a-137">La stratégie [ListedeTypedeSynchronisationDésactivée](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) peut être utilisée pour désactiver de façon sélective la synchronisation des favoris ou des paramètres, si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="f422a-137">The [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policy can be used to selectively disable either favorites or settings sync if desired.</span></span> <span data-ttu-id="f422a-138">Si la stratégie [SynchronisationDésactivée](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) est active, la synchronisation locale est alors désactivée également.</span><span class="sxs-lookup"><span data-stu-id="f422a-138">If the [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) policy is active, then on-premises sync is disabled as well.</span></span>  

## <span data-ttu-id="f422a-139">Voir également</span><span class="sxs-lookup"><span data-stu-id="f422a-139">See also</span></span>

- [<span data-ttu-id="f422a-140">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="f422a-140">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f422a-141">MicrosoftEdge et Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="f422a-141">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="f422a-142">Synchronisation de Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="f422a-142">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
