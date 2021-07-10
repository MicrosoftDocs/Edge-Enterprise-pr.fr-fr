---
title: Compatibilité descendante pour la page Nouvel onglet de l’Entreprise
ms.author: ruchir
author: dan-wesley
manager: vwehren
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Compatibilité descendante pour la page Nouvel onglet de l’Entreprise
ms.openlocfilehash: e2534f9df82aa81843d7cd292ada99a4c7574a3c
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642080"
---
# <a name="backwards-compatibility-for-the-enterprise-new-tab-page"></a><span data-ttu-id="59e1b-103">Compatibilité descendante pour la page Nouvel onglet de l’Entreprise</span><span class="sxs-lookup"><span data-stu-id="59e1b-103">Backwards compatibility for the Enterprise New tab page</span></span>

<span data-ttu-id="59e1b-104">Cet article décrit la modification apportée à la page Nouvel onglet et la manière dont les utilisateurs peuvent être rétrocompatibles avec les versions Microsoft Edge version 87 et antérieures.</span><span class="sxs-lookup"><span data-stu-id="59e1b-104">This article describes the change to the New tab page and how users can be backwards compatible with Microsoft Edge version 87 and earlier.</span></span>

> [!NOTE]
> <span data-ttu-id="59e1b-105">Cet article concerne Microsoft Edge version 87 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="59e1b-105">This article applies to Microsoft Edge version 87 or later.</span></span>

## <a name="information-feeds-from-single-endpoint"></a><span data-ttu-id="59e1b-106">Flux d’informations à partir d’un point de terminaison unique</span><span class="sxs-lookup"><span data-stu-id="59e1b-106">Information feeds from single endpoint</span></span>

<span data-ttu-id="59e1b-107">La nouvelle version de la page Nouvel onglet de l’Entreprise associe le contenu conforme à Microsoft 365 à des flux d’informations pertinents et conformes au secteur qui sont traités via le point de terminaison MSN.com.</span><span class="sxs-lookup"><span data-stu-id="59e1b-107">The new version of the Enterprise New tab page combines compliant Microsoft 365 content with industry relevant and compliant information feeds that are served via the MSN.com endpoint.</span></span>

> [!NOTE]
> <span data-ttu-id="59e1b-108">Le contenu Office 365 était à l’origine traité en utilisant le domaine [Office.com](https://www.office.com).</span><span class="sxs-lookup"><span data-stu-id="59e1b-108">Office 365 content was originally served using the [Office.com](https://www.office.com) domain.</span></span>

<span data-ttu-id="59e1b-109">Si l’accès au domaine MSN.com est limité pour votre organisation, nous vous recommandons vivement d’autoriser les utilisateurs à accéder à cette [URL](https://ntp.msn.com).</span><span class="sxs-lookup"><span data-stu-id="59e1b-109">If access to the MSN.com domain is restricted for your organization, we strongly recommend giving users access to this [url](https://ntp.msn.com).</span></span>

<span data-ttu-id="59e1b-110">Si vous avez besoin de davantage de temps pour autoriser l’accès au domaine MSN, nous vous recommandons d’utiliser [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) qui vous permet de choisir entre l’expérience de flux Microsoft News ou Office 365 pour la nouvelle page d’onglets.</span><span class="sxs-lookup"><span data-stu-id="59e1b-110">If you need more time to enable access to the MSN domain, we recommend using the [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype), that lets you choose either the Microsoft News or Office 365 feed experience for the new tab page.</span></span>

### <a name="keep-using-officecom"></a><span data-ttu-id="59e1b-111">Continuer à utiliser Office.com</span><span class="sxs-lookup"><span data-stu-id="59e1b-111">Keep using Office.com</span></span>

 <span data-ttu-id="59e1b-112">Vous pouvez configurer la stratégie **NewTabPageSetFeedType** pour continuer à utiliser le domaine Office.com déconseillé.</span><span class="sxs-lookup"><span data-stu-id="59e1b-112">You can configure the **NewTabPageSetFeedType** policy to keep using the deprecated Office.com domain.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59e1b-113">La stratégie **NewTabPageSetFeedType** et le domaine Office.com qui traitent le contenu Office 365 cesseront de fonctionner lorsque la version 90 de Microsoft Edge est publiée.</span><span class="sxs-lookup"><span data-stu-id="59e1b-113">The **NewTabPageSetFeedType** policy and the Office.com domain that serves Office 365 content will quit working when Microsoft Edge version 90 is released.</span></span>

<span data-ttu-id="59e1b-114">Les paramètres de stratégie suivants forcent la page Nouvel onglet de l’Entreprise à afficher le contenu d’un document Office à partir du domaine Office.com.</span><span class="sxs-lookup"><span data-stu-id="59e1b-114">The following policy settings will force the Enterprise New tab page to render Office document content from the Office.com domain.</span></span>

- <span data-ttu-id="59e1b-115">Configurez la stratégie comme **Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="59e1b-115">Set the policy as **Mandatory**.</span></span>
- <span data-ttu-id="59e1b-116">Définissez la valeur du mappage de stratégie sur **Office (1) = expérience de flux Office 365**.</span><span class="sxs-lookup"><span data-stu-id="59e1b-116">Set the value of the policy mapping to **Office (1) = Office 365 feed experience**.</span></span>

<span data-ttu-id="59e1b-117">Si le passage à Office.com n’est pas possible, n’hésitez pas à nous envoyer vos commentaires.</span><span class="sxs-lookup"><span data-stu-id="59e1b-117">If the switch to the Office.com isn't possible, reach out and send us feedback.</span></span> <span data-ttu-id="59e1b-118">Une autre option consiste à configurer [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) pour qu’elle pointe vers une URL de point de terminaison autorisée par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="59e1b-118">Another option is to configure the [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) so it points to an endpoint URL that's allowed by your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="59e1b-119">La stratégie **NewTabPageLocation** a priorité si la stratégie **NewTabPageSetFeedType** est également configurée.</span><span class="sxs-lookup"><span data-stu-id="59e1b-119">The **NewTabPageLocation** policy has precedence if the **NewTabPageSetFeedType** policy is also configured.</span></span>

## <a name="enterprise-users-will-now-get-microsoft-news-content-via-my-feed"></a><span data-ttu-id="59e1b-120">Les utilisateurs Entreprise reçoivent désormais du contenu Microsoft News via Mon flux</span><span class="sxs-lookup"><span data-stu-id="59e1b-120">Enterprise users will now get Microsoft news content via My Feed</span></span>

<span data-ttu-id="59e1b-121">La page Nouvel onglet de l’Entreprise propose des informations pertinentes de **Mon flux** et le contenu Office 365 dans un affichage unique pour les utilisateurs connectés avec leur compte Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="59e1b-121">The Enterprise New tab page will offer industry relevant information in **My Feed** and Office 365 content in a single view for users signed in with their Azure Active Directory (Azure AD) account.</span></span> <span data-ttu-id="59e1b-122">Pour les utilisateurs connectés avec leur compte Azure Active Directory (Azure AD) ayant sélectionné l’option Microsoft News dans le paramètres du menu volant, leur nouvel affichage de page d’onglet est remplacé par le contenu **Mon flux**.</span><span class="sxs-lookup"><span data-stu-id="59e1b-122">For users signed in with their Azure Active Directory (Azure AD) who selected the Microsoft News option in the settings flyout, their new tab page view will be replaced with **My Feed** content.</span></span> <span data-ttu-id="59e1b-123">Lorsqu’ils ouvrent une page nouvel onglet dans le navigateur, celle-ci se présente comme dans l’exemple de la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="59e1b-123">When they open a new tab page in the browser it will look like the example in the next screenshot.</span></span>

![Page nouvel onglet affichant le contenu de Mon flux.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-myfeed-view.png)

> [!NOTE]
> <span data-ttu-id="59e1b-125">Les utilisateurs qui ne se sont pas connectés avec Azure AD continueront à voir le flux Actualités MSN lorsqu’ils ouvrent un nouvel onglet.</span><span class="sxs-lookup"><span data-stu-id="59e1b-125">Users who aren't signed in with Azure AD will continue to see the MSN News feed when they open a new tab.</span></span>

## <a name="page-layout"></a><span data-ttu-id="59e1b-126">Mise en page</span><span class="sxs-lookup"><span data-stu-id="59e1b-126">Page layout</span></span>

<span data-ttu-id="59e1b-127">Avec les modifications apportées à la page nouvel onglet, la mise en page ne doit plus contrôler deux types de contenu spécifiques (Office 365 et Microsoft News), de sorte que le bouton bascule de contenu n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="59e1b-127">With the changes to the New tab page, the Page layout no longer has to control two specific content types (Office 365 and Microsoft News), so the content toggle isn't available.</span></span> <span data-ttu-id="59e1b-128">La capture d’écran suivante montre le menu volant pour la mise en page.</span><span class="sxs-lookup"><span data-stu-id="59e1b-128">The next screenshot shows the flyout for the Page layout.</span></span>

![Affichage de la mise en page pour la page Nouvel onglet.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-page-layout.png)

<span data-ttu-id="59e1b-130">Si vous voulez continuer à accéder au contenu de Microsoft News qui n’est pas lié à votre organisation, vous devez utiliser un autre profil de navigateur.</span><span class="sxs-lookup"><span data-stu-id="59e1b-130">If you want to keep accessing Microsoft News content that isn't tied to your organization, you must use a different browser profile.</span></span> <span data-ttu-id="59e1b-131">Accédez à *edge://settings/profiles* et déconnectez-vous de votre profil Azure AD.</span><span class="sxs-lookup"><span data-stu-id="59e1b-131">Go to  *edge://settings/profiles* and sign out of your Azure AD profile.</span></span> <span data-ttu-id="59e1b-132">Cette action ouvre l’affichage standard pour la page Nouvel onglet de l’Entreprise.</span><span class="sxs-lookup"><span data-stu-id="59e1b-132">This action will bring up the  standard view for the Enterprise new tab page.</span></span> 

## <a name="see-also"></a><span data-ttu-id="59e1b-133">Voir également</span><span class="sxs-lookup"><span data-stu-id="59e1b-133">See also</span></span>

- [<span data-ttu-id="59e1b-134">Page d’accueil Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="59e1b-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="59e1b-135">Mode Entreprise d’Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="59e1b-135">Enterprise Mode for Internet Explorer 11</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)