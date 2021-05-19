---
title: Déploiements progressifs pour les mises à jour du canal stable Microsoft Edge
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 05/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Déploiements progressifs pour les mises à jour du canal stable Microsoft Edge
ms.openlocfilehash: 5b0d2f58318b10538d0470b644d346b5b9b9489b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979780"
---
# <span data-ttu-id="6e989-103">Déploiements progressifs pour les mises à jour du canal stable Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6e989-103">Progressive rollouts for Microsoft Edge Stable channel updates</span></span>

<span data-ttu-id="6e989-104">À compter de la version 83 de Microsoft Edge, nous allons effectuer un déploiement progressif des mises à jour majeures du canal stable Microsoft Edge sur une période de quelques jours.</span><span class="sxs-lookup"><span data-stu-id="6e989-104">Starting with Microsoft Edge 83 release, we will perform gradual rollouts of major updates to Microsoft Edge Stable channel over the span of a few days.</span></span> <span data-ttu-id="6e989-105">Ce déploiement progressif nous permet de contrôler les mises à niveau et de mettre à jour le navigateur en toute sécurité au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="6e989-105">This progressive rollout allows us to monitor upgrades and safely update the browser across the organization.</span></span>

> [!NOTE]
> <span data-ttu-id="6e989-106">Cela concerne la version 83 ou ultérieure du canal stable Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6e989-106">This applies to Microsoft Edge Stable channel version 83 or later.</span></span>

## <span data-ttu-id="6e989-107">Pourquoi un déploiement progressif ?</span><span class="sxs-lookup"><span data-stu-id="6e989-107">Why do we need progressive rollout?</span></span>

<span data-ttu-id="6e989-108">En surveillant étroitement l’intégrité de nos mises à jour et en les déployant sur plusieurs jours, nous pouvons limiter l’impact des problèmes liés aux nouvelles mises à jour.</span><span class="sxs-lookup"><span data-stu-id="6e989-108">By monitoring the health of our updates closely and rolling out the updates over the course of several days, we can limit the impact of issues that might occur with the new update.</span></span> <span data-ttu-id="6e989-109">Avec Microsoft Edge version 83, le déploiement progressif est activé pour toutes les versions Windows 7, Windows 8 et 8.1, et Windows 10 de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6e989-109">With Microsoft Edge release 83, Progressive Rollouts will be enabled for all Windows 7, Windows 8 & 8.1, and Windows 10 versions of Microsoft Edge.</span></span> <span data-ttu-id="6e989-110">Nous prendrons en charge Microsoft Edge sur Mac dès qu’il sera prêt.</span><span class="sxs-lookup"><span data-stu-id="6e989-110">We will support Microsoft Edge on Mac as soon as it is ready.</span></span>

## <span data-ttu-id="6e989-111">Comment se dérouleront les mises à jour ?</span><span class="sxs-lookup"><span data-stu-id="6e989-111">How will the updates work?</span></span>

<span data-ttu-id="6e989-112">Une valeur de mise à niveau est attribuée à chaque installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6e989-112">Each installation of Microsoft Edge is assigned an upgrade value.</span></span> <span data-ttu-id="6e989-113">Lorsque nous lançons le déploiement par incréments, la mise à jour s’affiche lorsque la valeur de votre appareil est comprise dans la plage de valeurs de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="6e989-113">When we start rolling out incrementally, you'll see the update when the value on your device falls within the upgrade value range.</span></span> <span data-ttu-id="6e989-114">Au fur et à mesure du déploiement (dans un délai de quelques jours), tous les utilisateurs finissent par obtenir la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="6e989-114">As the rollout progresses (within a few days), all users will eventually get the update.</span></span> <span data-ttu-id="6e989-115">Les mises à jour de navigateur incluant des correctifs de sécurité critiques auront une cadence de déploiement plus rapide que les mises à jour qui en sont dépourvu.</span><span class="sxs-lookup"><span data-stu-id="6e989-115">Browser updates with critical security fixes will have a faster rollout cadence than updates that don't have critical security fixes.</span></span> <span data-ttu-id="6e989-116">Cela permet de garantir une protection rapide contre les vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="6e989-116">This is done to ensure prompt protection from vulnerabilities.</span></span>

## <span data-ttu-id="6e989-117">En quoi les grandes entreprises sont-elles affectées ?</span><span class="sxs-lookup"><span data-stu-id="6e989-117">How does this affect enterprises?</span></span>

<span data-ttu-id="6e989-118">Les artefacts Microsoft Edge sont distribués aux grandes entreprises à l’aide de plusieurs mécanismes tels que Microsoft Intune, Windows Server Update Service (WSUS) et le gestionnaire de configuration.</span><span class="sxs-lookup"><span data-stu-id="6e989-118">Microsoft Edge artifacts are distributed to enterprises using multiple mechanisms such as Microsoft Intune, Windows Server Update Service (WSUS), and Configuration Manager.</span></span> <span data-ttu-id="6e989-119">Ces outils de déploiement se comportent différemment en ce qui concerne le déploiement progressif :</span><span class="sxs-lookup"><span data-stu-id="6e989-119">These deployment tools behave differently with respect to Progressive Rollout:</span></span>

- <span data-ttu-id="6e989-120">Les grandes entreprises qui gèrent la distribution via Microsoft Intune sont inscrites aux mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="6e989-120">Enterprises that manage distribution via Microsoft Intune are registered for auto-updates.</span></span> <span data-ttu-id="6e989-121">Le déploiement progressif est utilisé et tous les utilisateurs verront une mise à jour dans quelques jours.</span><span class="sxs-lookup"><span data-stu-id="6e989-121">Progressive Rollout is used, and all the users will see an update in a few days.</span></span>
- <span data-ttu-id="6e989-122">Les entreprises qui gèrent la distribution via WSUS (Windows Server Update Services) ou le gestionnaire de configuration ne sont pas inscrites aux mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="6e989-122">Enterprises that manage distribution through WSUS (Windows Server Update Services) or Configuration Manager are not registered for auto-updates.</span></span> <span data-ttu-id="6e989-123">Les administrateurs gèrent et appliquent les mises à jour disponibles dès le début.</span><span class="sxs-lookup"><span data-stu-id="6e989-123">Administrators manage and apply the updates that will be available from the start.</span></span> <span data-ttu-id="6e989-124">Le déploiement progressif n’affecte pas ce processus.</span><span class="sxs-lookup"><span data-stu-id="6e989-124">Progressive Rollout does not affect this process.</span></span>

<span data-ttu-id="6e989-125">Partagez vos précieux commentaires par le biais de UserVoice, du bouton Commentaires dans les applications ou ci-dessous dans la section Commentaires si vous avez des questions ou des remarques.</span><span class="sxs-lookup"><span data-stu-id="6e989-125">Please share your valuable feedback through user voice, the in-application feedback button, or below in the comments if you have any concerns or questions.</span></span>

## <span data-ttu-id="6e989-126">Voir également</span><span class="sxs-lookup"><span data-stu-id="6e989-126">See also</span></span>

- [<span data-ttu-id="6e989-127">Page d’accueil Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="6e989-127">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
