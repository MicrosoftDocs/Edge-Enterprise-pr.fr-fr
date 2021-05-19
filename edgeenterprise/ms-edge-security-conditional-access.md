---
title: Microsoft Edge et l’accès conditionnel
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 10/02/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge et l’accès conditionnel
ms.openlocfilehash: a81d39c15f418dab6565ee7acc45de17f66e3828
ms.sourcegitcommit: 3478cfcf2b03944213a7c7c61f05490bc37aa7c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/03/2020
ms.locfileid: "11094771"
---
# <span data-ttu-id="66438-103">Microsoft Edge et l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="66438-103">Microsoft Edge and Conditional Access</span></span>
  
<span data-ttu-id="66438-104">Cet article décrit la prise en charge de l’accès conditionnel par Microsoft Edge et l’accès aux ressources protégées par ce biais.</span><span class="sxs-lookup"><span data-stu-id="66438-104">This article describes how Microsoft Edge supports Conditional Access, and how to access resources protected by Conditional Access.</span></span>

> [!NOTE]
> <span data-ttu-id="66438-105">Cet article concerne Microsoft Edge version 77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="66438-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="66438-106">L’un des aspects clés de la sécurité du cloud est l’identité et l’accès pour la gestion de vos ressources cloud.</span><span class="sxs-lookup"><span data-stu-id="66438-106">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="66438-107">Dans un monde où la priorité est donnée aux appareils mobiles et au cloud, les utilisateurs peuvent accéder aux ressources de votre organisation via divers appareils et applications, où qu’ils se trouvent.</span><span class="sxs-lookup"><span data-stu-id="66438-107">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="66438-108">En conséquence, se focaliser sur qui peut accéder à une ressource ne suffit pas.</span><span class="sxs-lookup"><span data-stu-id="66438-108">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="66438-109">Vous devez également prendre en compte le mode d’accès à la ressource.</span><span class="sxs-lookup"><span data-stu-id="66438-109">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="66438-110">L’accès conditionnel Azure Active Directory (Azure AD) vous aide à maîtriser l’équilibre entre sécurité et productivité.</span><span class="sxs-lookup"><span data-stu-id="66438-110">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

## <span data-ttu-id="66438-111">Accès aux ressources protégées par un accès conditionnel dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="66438-111">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="66438-112">Microsoft Edge prend en charge en mode natif l’accès conditionnel Azure AD.</span><span class="sxs-lookup"><span data-stu-id="66438-112">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="66438-113">Il n’est pas nécessaire d’installer une extension distincte.</span><span class="sxs-lookup"><span data-stu-id="66438-113">There's no need to install a separate extension.</span></span> <span data-ttu-id="66438-114">Lorsque vous êtes connecté(e) à un profil Microsoft Edge avec des informations d’identification Azure AD d’entreprise, Microsoft Edge permet un accès transparent aux ressources cloud d’entreprise protégées par l’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="66438-114">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="66438-115">Sur un appareil conforme, l’identité qui accède à la ressource doit correspondre à l’identité du profil.</span><span class="sxs-lookup"><span data-stu-id="66438-115">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="66438-116">Si ce n’est pas le cas, vous verrez un message semblable à celui de la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="66438-116">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="66438-117">Dans l’exemple de capture d’écran, « testadmin@evostsoneboxtest.com » est le compte de connexion nécessaire pour accéder à la ressource.</span><span class="sxs-lookup"><span data-stu-id="66438-117">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![Message d’accès conditionnel dans le navigateur](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="66438-119">Pour continuer, vous devez basculer vers le profil requis (si vous en possédez un) ou créer un profil avec une identité correspondante.</span><span class="sxs-lookup"><span data-stu-id="66438-119">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="66438-120">Pour vous connecter et utiliser votre profil, cliquez sur l’avatar du compte dans l’angle supérieur droit du navigateur.</span><span class="sxs-lookup"><span data-stu-id="66438-120">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="66438-121">Le menu Gérer l’alerte vous permet d’effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="66438-121">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="66438-122">Sélectionner un autre profil.</span><span class="sxs-lookup"><span data-stu-id="66438-122">Select another profile.</span></span> <span data-ttu-id="66438-123">Cliquer sur le nom du profil.</span><span class="sxs-lookup"><span data-stu-id="66438-123">Click the profile name.</span></span>
- <span data-ttu-id="66438-124">Créer un profil.</span><span class="sxs-lookup"><span data-stu-id="66438-124">Create a profile.</span></span> <span data-ttu-id="66438-125">Cliquez sur **Ajouter un profil**.</span><span class="sxs-lookup"><span data-stu-id="66438-125">Click **Add a profile**.</span></span>
- <span data-ttu-id="66438-126">Gérer vos profils.</span><span class="sxs-lookup"><span data-stu-id="66438-126">Manage your profiles.</span></span> <span data-ttu-id="66438-127">Cliquez sur **Gérer les paramètres de profil**.</span><span class="sxs-lookup"><span data-stu-id="66438-127">Click **Manage profile settings**.</span></span>

<span data-ttu-id="66438-128">Cette prise en charge est disponible sur toutes les plateformes, y compris toutes les versions prises en charge de Windows et de macOS.</span><span class="sxs-lookup"><span data-stu-id="66438-128">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <span data-ttu-id="66438-129">Procédure de déploiement de l’accès conditionnel dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="66438-129">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="66438-130">[Déployer l’accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) fournit un guide détaillé pour vous aider à déployer l’accès conditionnel dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="66438-130">[Deploy Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <span data-ttu-id="66438-131">Voir également</span><span class="sxs-lookup"><span data-stu-id="66438-131">See also</span></span>

- [<span data-ttu-id="66438-132">Page d’accueil Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="66438-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="66438-133">Vidéo : sécurité, compatibilité et facilité de gestion</span><span class="sxs-lookup"><span data-stu-id="66438-133">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)
