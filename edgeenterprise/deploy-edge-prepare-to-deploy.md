---
title: Microsoft Edge dans votre environnement
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge dans votre environnement
ms.openlocfilehash: e1418d21ff9e541d83d5b86baf5ff25c50d2299d
ms.sourcegitcommit: 16a92a51560fdba6f6480e4533453348f026c7ef
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313930"
---
# <span data-ttu-id="1ef97-103">Microsoft Edge dans votre environnement</span><span class="sxs-lookup"><span data-stu-id="1ef97-103">Microsoft Edge in your environment</span></span>

<span data-ttu-id="1ef97-104">Cet article explique comment préparer le déploiement de Microsoft Edge lorsque l’ancienne version de Microsoft Edge atteint sa fin de service.</span><span class="sxs-lookup"><span data-stu-id="1ef97-104">This article describes how to prepare to deploy Microsoft Edge when Microsoft Edge Legacy reaches its end of service.</span></span>

<span data-ttu-id="1ef97-105">Comme le permet [le billet de blog](https://aka.ms/EdgeLegacyEOS) de l’équipe produit Microsoft Edge, la prise en charge de l’application de bureau de l’ancienne version de Microsoft Edge prendra fin le 9 mars 2021.</span><span class="sxs-lookup"><span data-stu-id="1ef97-105">As per the Microsoft Edge Product Team’s [blog post](https://aka.ms/EdgeLegacyEOS), support for the Microsoft Edge Legacy desktop application will end on March 9, 2021.</span></span> <span data-ttu-id="1ef97-106">Lorsque vous appliquez la version Update Tuesday (ou « B ») en avril, elle supprimera l’ancienne version de Microsoft Edge des appareils exécutant Windows 10 RS4 à 20H1 et la remplacera par Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1ef97-106">When you apply the Update Tuesday (or "B") release in April, it will remove Microsoft Edge Legacy from devices running Windows 10 RS4 through 20H1 and replace it with Microsoft Edge.</span></span>

## <span data-ttu-id="1ef97-107">Comment se préparer</span><span class="sxs-lookup"><span data-stu-id="1ef97-107">How to Prepare</span></span>

<span data-ttu-id="1ef97-108">Pour préparer l’installation de Microsoft Edge sur les appareils Windows 10 RS4 à 20H1 avec la version Update Tuesday en avril, nous vous recommandons de lire [Planifier votre déploiement de Microsoft Edge](deploy-edge-plan-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="1ef97-108">To prepare for Microsoft Edge being installed on Windows 10 RS4 through 20H1 devices with the Update Tuesday release in April, we recommend reading [Plan your deployment of Microsoft Edge](deploy-edge-plan-deployment.md).</span></span>

<span data-ttu-id="1ef97-109">Après avoir planifié votre déploiement, utilisez l’une des approches suivantes pour préparer le déploiement de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1ef97-109">After you plan your deployment, use one of the following approaches to prepare to deploy Microsoft Edge.</span></span>

- <span data-ttu-id="1ef97-110">**Installez des stratégies de groupe pour personnaliser votre approche de mise à jour Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="1ef97-110">**Install group policies to customize your Microsoft Edge update approach**.</span></span> <span data-ttu-id="1ef97-111">Pour plus d’informations, voir [Configurer les paramètres de stratégie Microsoft Edge sur Windows](configure-microsoft-edge.md) et prêter une attention particulière au document [de référence de la stratégie de mise à jour](microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="1ef97-111">For more information, see [Configure Microsoft Edge policy settings on Windows](configure-microsoft-edge.md), and pay special attention to the [Update Policy reference](microsoft-edge-update-policies.md) material.</span></span> <span data-ttu-id="1ef97-112">Si vous installez des stratégies de groupe pour gérer vos mises à jour avant d’installer la version Update Tuesday d’avril, Microsoft Edge commencera immédiatement à respecter votre stratégie.</span><span class="sxs-lookup"><span data-stu-id="1ef97-112">If you install group policies to manage your updates before installing April’s Update Tuesday release, Microsoft Edge will immediately start respecting your policy.</span></span> <span data-ttu-id="1ef97-113">S’il n’existe aucune stratégie de groupe installée, Microsoft Edge se mettra automatiquement à jour.</span><span class="sxs-lookup"><span data-stu-id="1ef97-113">If there isn't any installed group policy, Microsoft Edge will automatically update itself.</span></span>

- <span data-ttu-id="1ef97-114">**Supprimez l’application de bureau de l’ancienne version de Microsoft Edge avant sa date de fin de service du 9 mars 2021 et déployez Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="1ef97-114">**Remove the Microsoft Edge Legacy desktop application before its end of service date of March 9, 2021 and deploy Microsoft Edge**.</span></span> <span data-ttu-id="1ef97-115">Pour Windows 10 RS4 à 20H1, vous pouvez le faire à l’aide des mises à jour Windows.</span><span class="sxs-lookup"><span data-stu-id="1ef97-115">For Windows 10 RS4 through 20H1, you can do this by using Windows Updates.</span></span> <span data-ttu-id="1ef97-116">Pour plus d’informations, voir [Déployer Microsoft Edge avec les mises à jour Windows 10](deploy-edge-with-windows-10-updates.md).</span><span class="sxs-lookup"><span data-stu-id="1ef97-116">For more information, see [Deploy Microsoft Edge with Windows 10 updates](deploy-edge-with-windows-10-updates.md).</span></span>

## <span data-ttu-id="1ef97-117">Voir également</span><span class="sxs-lookup"><span data-stu-id="1ef97-117">See also</span></span>

- [<span data-ttu-id="1ef97-118">Page d’accueil Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="1ef97-118">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="1ef97-119">Planifier votre déploiement de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1ef97-119">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)