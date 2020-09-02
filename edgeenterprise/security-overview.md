---
title: Vue d’ensemble de la sécurité de MicrosoftEdge
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 04/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Vue d’ensemble du déploiement de la sécurité de MicrosoftEdge
ms.openlocfilehash: f22f2dcbace00cd535d201950c2af488c708525b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979846"
---
# <span data-ttu-id="6bab5-103">Vue d’ensemble de la sécurité de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="6bab5-103">Overview of Microsoft Edge security</span></span>
  
<span data-ttu-id="6bab5-104">Les administrateurs informatiques de l’entreprise sont constamment confrontés à une myriade de défis de sécurité existants et émergents lorsqu’ils tentent de protéger le réseau et les périphériques de leur entreprise des attaques malveillantes et d’empêcher les accès non autorisés et les fuites de données d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="6bab5-104">IT admins in the enterprise are constantly facing a myriad of existing and emerging security challenges while protecting the corporate network and devices from malicious attacks and preventing unauthorized access and leaks of corporate data.</span></span> <span data-ttu-id="6bab5-105">MicrosoftEdge offre plusieurs fonctionnalités natives uniques qui permettent de relever ces défis.</span><span class="sxs-lookup"><span data-stu-id="6bab5-105">Microsoft Edge provides several natively built, unique capabilities that help address these challenges.</span></span>

> [!NOTE]
> <span data-ttu-id="6bab5-106">Cet article concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6bab5-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="6bab5-107">Accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="6bab5-107">Conditional Access</span></span>

<span data-ttu-id="6bab5-108">L’un des aspects clés de la sécurité du cloud est l’identité et l’accès pour la gestion de vos ressources cloud.</span><span class="sxs-lookup"><span data-stu-id="6bab5-108">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="6bab5-109">Dans un monde où la priorité est donnée aux appareils mobiles et au cloud, les utilisateurs peuvent accéder aux ressources de votre organisation via divers appareils et applications, où qu’ils se trouvent.</span><span class="sxs-lookup"><span data-stu-id="6bab5-109">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="6bab5-110">En conséquence, se focaliser sur qui peut accéder à une ressource ne suffit pas.</span><span class="sxs-lookup"><span data-stu-id="6bab5-110">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="6bab5-111">Vous devez également prendre en compte le mode d’accès à la ressource.</span><span class="sxs-lookup"><span data-stu-id="6bab5-111">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="6bab5-112">L’accès conditionnel Azure ActiveDirectory (Azure AD) vous aide à maîtriser l’équilibre entre sécurité et productivité.</span><span class="sxs-lookup"><span data-stu-id="6bab5-112">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

### <span data-ttu-id="6bab5-113">Accès aux ressources protégées par un accès conditionnel dans MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="6bab5-113">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="6bab5-114">MicrosoftEdge prend en charge en mode natif l’accès conditionnel AzureAD.</span><span class="sxs-lookup"><span data-stu-id="6bab5-114">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="6bab5-115">Il n’est pas nécessaire d’installer une extension distincte.</span><span class="sxs-lookup"><span data-stu-id="6bab5-115">There's no need to install a separate extension.</span></span> <span data-ttu-id="6bab5-116">Lorsque vous êtes connecté(e) à un profil MicrosoftEdge avec des informations d’identification Azure AD d’entreprise, MicrosoftEdge permet un accès transparent aux ressources cloud d’entreprise protégées par l’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="6bab5-116">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="6bab5-117">Sur un appareil conforme, l’identité qui accède à la ressource doit correspondre à l’identité du profil.</span><span class="sxs-lookup"><span data-stu-id="6bab5-117">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="6bab5-118">Si ce n’est pas le cas, vous verrez un message semblable à celui de la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="6bab5-118">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="6bab5-119">Dans l’exemple de capture d’écran, «testadmin@evostsoneboxtest.com» est le compte de connexion nécessaire pour accéder à la ressource.</span><span class="sxs-lookup"><span data-stu-id="6bab5-119">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![Message d’accès conditionnel dans le navigateur](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="6bab5-121">Pour continuer, vous devez basculer vers le profil requis (si vous en possédez un) ou créer un profil avec une identité correspondante.</span><span class="sxs-lookup"><span data-stu-id="6bab5-121">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="6bab5-122">Pour vous connecter et utiliser votre profil, cliquez sur l’avatar du compte dans l’angle supérieur droit du navigateur.</span><span class="sxs-lookup"><span data-stu-id="6bab5-122">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="6bab5-123">Le menu Gérer l’alerte vous permet d’effectuer les actions suivantes:</span><span class="sxs-lookup"><span data-stu-id="6bab5-123">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="6bab5-124">Sélectionner un autre profil.</span><span class="sxs-lookup"><span data-stu-id="6bab5-124">Select another profile.</span></span> <span data-ttu-id="6bab5-125">Cliquer sur le nom du profil.</span><span class="sxs-lookup"><span data-stu-id="6bab5-125">Click the profile name.</span></span>
- <span data-ttu-id="6bab5-126">Créer un profil.</span><span class="sxs-lookup"><span data-stu-id="6bab5-126">Create a profile.</span></span> <span data-ttu-id="6bab5-127">Cliquez sur **Ajouter un profil**.</span><span class="sxs-lookup"><span data-stu-id="6bab5-127">Click **Add a profile**.</span></span>
- <span data-ttu-id="6bab5-128">Gérer vos profils.</span><span class="sxs-lookup"><span data-stu-id="6bab5-128">Manage your profiles.</span></span> <span data-ttu-id="6bab5-129">Cliquez sur **Gérer les paramètres de profil**.</span><span class="sxs-lookup"><span data-stu-id="6bab5-129">Click **Manage profile settings**.</span></span>

<span data-ttu-id="6bab5-130">Cette prise en charge est disponible sur toutes les plateformes, y compris toutes les versions prises en charge de Windows et de macOS.</span><span class="sxs-lookup"><span data-stu-id="6bab5-130">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <span data-ttu-id="6bab5-131">Procédure de déploiement de l’accès conditionnel dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6bab5-131">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="6bab5-132">[Déployer l’accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) fournit un guide détaillé pour vous aider à déployer l’accès conditionnel dans Azure ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="6bab5-132">[Deploy Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <span data-ttu-id="6bab5-133">Voir également</span><span class="sxs-lookup"><span data-stu-id="6bab5-133">See also</span></span>

- [<span data-ttu-id="6bab5-134">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="6bab5-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="6bab5-135">Vidéo: sécurité, compatibilité et facilité de gestion</span><span class="sxs-lookup"><span data-stu-id="6bab5-135">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)
