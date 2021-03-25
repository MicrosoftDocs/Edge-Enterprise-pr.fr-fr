---
title: Déployer Microsoft Edge avec les mises à jour Windows10
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Déployer Microsoft Edge avec les mises à jour Windows10
ms.openlocfilehash: c8ea65f6c452b52b01c00d8fca418fe59db801b1
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447378"
---
# <a name="deploy-microsoft-edge-with-windows-10-updates"></a><span data-ttu-id="b4735-103">Déployer Microsoft Edge avec les mises à jour Windows10</span><span class="sxs-lookup"><span data-stu-id="b4735-103">Deploy Microsoft Edge with Windows 10 updates</span></span>

<span data-ttu-id="b4735-104">Cet article fournit des informations pour les utilisateurs qui déploient Microsoft Edge à l’aide des mises à jour Windows10.</span><span class="sxs-lookup"><span data-stu-id="b4735-104">The article provides information for users who are deploying Microsoft Edge by using Windows 10 updates.</span></span>

## <a name="for-windows-10-release-20h2"></a><span data-ttu-id="b4735-105">Pour Windows10 version 20H2</span><span class="sxs-lookup"><span data-stu-id="b4735-105">For Windows 10 release 20H2</span></span>

<span data-ttu-id="b4735-106">Windows10 version20H2 dispose déjà de Microsoft Edge installé comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="b4735-106">Windows 10 version 20H2 already has Microsoft Edge installed as its default browser.</span></span>

## <a name="for-windows-10-releases-rs4-through-20h1"></a><span data-ttu-id="b4735-107">Pour Windows10 versions RS4 à 20H1</span><span class="sxs-lookup"><span data-stu-id="b4735-107">For Windows 10 releases RS4 through 20H1</span></span>

<span data-ttu-id="b4735-108">Windows Server Update Services (WSUS) propose des mises à jour pour chaque version de Windows10, de RS4 à 20H1, qui suppriment l’application de bureau ancienne version Microsoft Edge et la remplacent par Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b4735-108">Windows Server Update Services (WSUS) has updates for each version of Windows 10 from RS4 through 20H1 that will remove the Microsoft Edge Legacy desktop app and replace it with Microsoft Edge.</span></span> <span data-ttu-id="b4735-109">Pour plus d’informations, consultez [cet article de support](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c) pour savoir quelle mise à jour WSUS est la bonne pour votre version de Windows.</span><span class="sxs-lookup"><span data-stu-id="b4735-109">For more information, see [this support article](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c) to find out which WSUS update is right for your Windows version.</span></span>

## <a name="for-windows-10-releases-prior-to-rs4-and-windows-7-81-and-earlier"></a><span data-ttu-id="b4735-110">Pour les version de Windows10 antérieures à RS4 (et Windows7, 8.1 et antérieures)</span><span class="sxs-lookup"><span data-stu-id="b4735-110">For Windows 10 releases prior to RS4 (and Windows 7, 8.1, and earlier)</span></span>

<span data-ttu-id="b4735-111">Les mises à jour Windows pour installer Microsoft Edge ne sont pas disponibles pour ces versions.</span><span class="sxs-lookup"><span data-stu-id="b4735-111">Windows updates to install Microsoft Edge aren't available for these versions.</span></span> <span data-ttu-id="b4735-112">Envisagez d’autres options de déploiement de Microsoft Edge sur ces appareils, telles que [Gestionnaire de configuration](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) ou [Intune.](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="b4735-112">Consider other options for deploying Microsoft Edge to these devices such as [Configuration Manager](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) or [Intune](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json).</span></span>

## <a name="see-also"></a><span data-ttu-id="b4735-113">Voir également</span><span class="sxs-lookup"><span data-stu-id="b4735-113">See also</span></span>

- [<span data-ttu-id="b4735-114">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="b4735-114">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="b4735-115">Planifier votre déploiement de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="b4735-115">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)