---
title: Microsoft Edge et l’accès conditionnel
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge et l’accès conditionnel
ms.openlocfilehash: 27d93627f8a86ad821a00d6d78b7db352e9e557a
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642850"
---
# <a name="microsoft-edge-and-conditional-access"></a><span data-ttu-id="f6f83-103">Microsoft Edge et l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="f6f83-103">Microsoft Edge and Conditional Access</span></span>
  
<span data-ttu-id="f6f83-104">Cet article décrit la prise en charge de l’accès conditionnel par Microsoft Edge et l’accès aux ressources protégées par ce biais.</span><span class="sxs-lookup"><span data-stu-id="f6f83-104">This article describes how Microsoft Edge supports Conditional Access, and how to access resources protected by Conditional Access.</span></span>

> [!NOTE]
> <span data-ttu-id="f6f83-105">Cet article concerne Microsoft Edge version 77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f6f83-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="f6f83-106">L’un des aspects clés de la sécurité du cloud est l’identité et l’accès pour la gestion de vos ressources cloud.</span><span class="sxs-lookup"><span data-stu-id="f6f83-106">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="f6f83-107">Dans un monde où la priorité est donnée aux appareils mobiles et au cloud, les utilisateurs peuvent accéder aux ressources de votre organisation via divers appareils et applications, où qu’ils se trouvent.</span><span class="sxs-lookup"><span data-stu-id="f6f83-107">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="f6f83-108">En conséquence, se focaliser sur qui peut accéder à une ressource ne suffit pas.</span><span class="sxs-lookup"><span data-stu-id="f6f83-108">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="f6f83-109">Vous devez également prendre en compte le mode d’accès à la ressource.</span><span class="sxs-lookup"><span data-stu-id="f6f83-109">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="f6f83-110">L’accès conditionnel Azure Active Directory (Azure AD) vous aide à maîtriser l’équilibre entre sécurité et productivité.</span><span class="sxs-lookup"><span data-stu-id="f6f83-110">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

## <a name="accessing-conditional-access-protected-resources-in-microsoft-edge"></a><span data-ttu-id="f6f83-111">Accès aux ressources protégées par un accès conditionnel dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f6f83-111">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="f6f83-112">Microsoft Edge prend en charge en mode natif l’accès conditionnel Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f6f83-112">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="f6f83-113">Il n’est pas nécessaire d’installer une extension distincte.</span><span class="sxs-lookup"><span data-stu-id="f6f83-113">There's no need to install a separate extension.</span></span> <span data-ttu-id="f6f83-114">Lorsque vous êtes connecté(e) à un profil Microsoft Edge avec des informations d’identification Azure AD d’entreprise, Microsoft Edge permet un accès transparent aux ressources cloud d’entreprise protégées par l’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="f6f83-114">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="f6f83-115">Sur un appareil conforme, l’identité qui accède à la ressource doit correspondre à l’identité du profil.</span><span class="sxs-lookup"><span data-stu-id="f6f83-115">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="f6f83-116">Si ce n’est pas le cas, vous verrez un message semblable à celui de la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="f6f83-116">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="f6f83-117">Dans l’exemple de capture d’écran, « testadmin@evostsoneboxtest.com » est le compte de connexion nécessaire pour accéder à la ressource.</span><span class="sxs-lookup"><span data-stu-id="f6f83-117">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![Message d’accès conditionnel dans le navigateur](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="f6f83-119">Pour continuer, vous devez basculer vers le profil requis (si vous en possédez un) ou créer un profil avec une identité correspondante.</span><span class="sxs-lookup"><span data-stu-id="f6f83-119">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="f6f83-120">Pour vous connecter et utiliser votre profil, cliquez sur l’avatar du compte dans l’angle supérieur droit du navigateur.</span><span class="sxs-lookup"><span data-stu-id="f6f83-120">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="f6f83-121">Le menu Gérer l’alerte vous permet d’effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="f6f83-121">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="f6f83-122">Sélectionner un autre profil.</span><span class="sxs-lookup"><span data-stu-id="f6f83-122">Select another profile.</span></span> <span data-ttu-id="f6f83-123">Cliquer sur le nom du profil.</span><span class="sxs-lookup"><span data-stu-id="f6f83-123">Click the profile name.</span></span>
- <span data-ttu-id="f6f83-124">Créer un profil.</span><span class="sxs-lookup"><span data-stu-id="f6f83-124">Create a profile.</span></span> <span data-ttu-id="f6f83-125">Cliquez sur **Ajouter un profil**.</span><span class="sxs-lookup"><span data-stu-id="f6f83-125">Click **Add a profile**.</span></span>
- <span data-ttu-id="f6f83-126">Gérer vos profils.</span><span class="sxs-lookup"><span data-stu-id="f6f83-126">Manage your profiles.</span></span> <span data-ttu-id="f6f83-127">Cliquez sur **Gérer les paramètres de profil**.</span><span class="sxs-lookup"><span data-stu-id="f6f83-127">Click **Manage profile settings**.</span></span>

<span data-ttu-id="f6f83-128">Cette prise en charge est disponible sur toutes les plateformes, y compris toutes les versions prises en charge de Windows et de macOS.</span><span class="sxs-lookup"><span data-stu-id="f6f83-128">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <a name="how-to-deploy-conditional-access-in-azure-active-directory"></a><span data-ttu-id="f6f83-129">Procédure de déploiement de l’accès conditionnel dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f6f83-129">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="f6f83-130">[Déployer l’accès conditionnel](/azure/active-directory/conditional-access/plan-conditional-access) fournit un guide détaillé pour vous aider à déployer l’accès conditionnel dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f6f83-130">[Deploy Conditional Access](/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6f83-131">Voir également</span><span class="sxs-lookup"><span data-stu-id="f6f83-131">See also</span></span>

- [<span data-ttu-id="f6f83-132">Page d’accueil Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="f6f83-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f6f83-133">Vidéo : sécurité, compatibilité et facilité de gestion</span><span class="sxs-lookup"><span data-stu-id="f6f83-133">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)