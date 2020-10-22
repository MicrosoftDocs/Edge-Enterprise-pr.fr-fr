---
title: Liste verte pour les points de terminaison de MicrosoftEdge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 10/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Liste verte pour les points de terminaison de MicrosoftEdge
ms.openlocfilehash: 48a3a72e5af3744516e3b72d02b5254ad2e0504a
ms.sourcegitcommit: b32d8d64ae65dc5a46e47b7c34b0211097a0cc65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "11133119"
---
# <span data-ttu-id="eebe8-103">Liste verte pour les points de terminaison de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="eebe8-103">Allow list for Microsoft Edge endpoints</span></span>

<span data-ttu-id="eebe8-104">MicrosoftEdge nécessite une connectivité à Internet pour prendre en charge ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="eebe8-104">Microsoft Edge requires connectivity to the Internet to support its features.</span></span> <span data-ttu-id="eebe8-105">Cet article identifie les URL de domaine que vous devez ajouter à la liste verte pour garantir les communications via des pare-feu et d’autres mécanismes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="eebe8-105">This article identifies the domain URLs that you need to add to the Allow list to ensure communications through firewalls and other security mechanisms.</span></span>

> [!NOTE]
> <span data-ttu-id="eebe8-106">Ceci concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="eebe8-106">This applies  to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="eebe8-107">URL de domaine à autoriser</span><span class="sxs-lookup"><span data-stu-id="eebe8-107">Domain URLs to allow</span></span>

<span data-ttu-id="eebe8-108">Autorisez les URL de domaine suivantes pour MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="eebe8-108">Allow the following domain URLs for Microsoft Edge.</span></span>

### <span data-ttu-id="eebe8-109">Service de mise à jour</span><span class="sxs-lookup"><span data-stu-id="eebe8-109">Update Service</span></span>

<span data-ttu-id="eebe8-110">Service que MicrosoftEdge utilise pour rechercher les nouvelles mises à jour.</span><span class="sxs-lookup"><span data-stu-id="eebe8-110">The service that Microsoft Edge uses to check for new updates.</span></span>

- `https://msedge.api.cdp.microsoft.com`

### <span data-ttu-id="eebe8-111">Service d’expérimentation et de configuration</span><span class="sxs-lookup"><span data-stu-id="eebe8-111">Experimentation and Configuration service</span></span>

- `https://config.edge.skype.com`

### <span data-ttu-id="eebe8-112">Télécharger les emplacements pour MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="eebe8-112">Download locations for Microsoft Edge</span></span>

<span data-ttu-id="eebe8-113">Les emplacements MicrosoftEdge peuvent être téléchargés à partir d’une installation initiale ou lorsqu’une mise à jour est disponible.</span><span class="sxs-lookup"><span data-stu-id="eebe8-113">Locations Microsoft Edge can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="eebe8-114">L’emplacement de téléchargement est déterminé par le service de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="eebe8-114">The download location is determined by the Update Service.</span></span>

#### <span data-ttu-id="eebe8-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="eebe8-115">HTTP</span></span>

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### <span data-ttu-id="eebe8-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="eebe8-116">HTTPS</span></span>

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="eebe8-117">Pour simplifier la liste verte des emplacements de téléchargement, vous pouvez utiliser un caractère générique:</span><span class="sxs-lookup"><span data-stu-id="eebe8-117">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <span data-ttu-id="eebe8-118">Télécharger les emplacements pour les extensions MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="eebe8-118">Download locations for Microsoft Edge Extensions</span></span>

<span data-ttu-id="eebe8-119">Les emplacements des extensions MicrosoftEdge peuvent être téléchargés à partir d’une installation initiale ou lorsqu’une mise à jour est disponible.</span><span class="sxs-lookup"><span data-stu-id="eebe8-119">Locations Microsoft Edge Extensions can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="eebe8-120">L’emplacement de téléchargement est déterminé par le service de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="eebe8-120">The download location is determined by the Update Service.</span></span>

#### <span data-ttu-id="eebe8-121">HTTP</span><span class="sxs-lookup"><span data-stu-id="eebe8-121">HTTP</span></span>

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### <span data-ttu-id="eebe8-122">HTTPS</span><span class="sxs-lookup"><span data-stu-id="eebe8-122">HTTPS</span></span>

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="eebe8-123">Pour simplifier la liste verte des emplacements de téléchargement, vous pouvez utiliser un caractère générique:</span><span class="sxs-lookup"><span data-stu-id="eebe8-123">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <span data-ttu-id="eebe8-124">Éventuellement pour l’optimisation de la distribution des téléchargements</span><span class="sxs-lookup"><span data-stu-id="eebe8-124">Optionally for Download Delivery Optimization</span></span>

<span data-ttu-id="eebe8-125">Pour plus d’informations sur l’optimisation de la distribution, consultez [Optimisation de la distribution pour les mises à jour de Windows10](https://aka.ms/waas-do).</span><span class="sxs-lookup"><span data-stu-id="eebe8-125">For information about delivery optimization, see [Delivery Optimization for Windows 10 updates](https://aka.ms/waas-do).</span></span>

- <span data-ttu-id="eebe8-126">Communication client à service: `*.do.dsp.mp.microsoft.com` (HTTP Port80, HTTPS Port443)</span><span class="sxs-lookup"><span data-stu-id="eebe8-126">Client to Service communication: `*.do.dsp.mp.microsoft.com` (HTTP Port 80, HTTPS Port 443)</span></span>
- <span data-ttu-id="eebe8-127">Communication client à client: le port TCP7680 doit être ouvert pour le trafic entrant</span><span class="sxs-lookup"><span data-stu-id="eebe8-127">Client to Client communication: TCP port 7680 should be open for inbound traffic</span></span>

### <span data-ttu-id="eebe8-128">Sync</span><span class="sxs-lookup"><span data-stu-id="eebe8-128">Sync</span></span>

<span data-ttu-id="eebe8-129">Ces points de terminaison gèrent la lecture et l’écriture de données synchronisées, la gestion des droits pour sécuriser les données et l’envoi d’une notification au navigateur lorsque de nouvelles données de synchronisation sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="eebe8-129">These endpoints manage the reading and writing of synced data, rights management for secure data, and notifying the browser when new sync data is available.</span></span>

- <span data-ttu-id="eebe8-130">Points de terminaison du service de synchronisation Edge:</span><span class="sxs-lookup"><span data-stu-id="eebe8-130">Edge sync service endpoints:</span></span>

  - `https://enterprise.edge.activity.windows.com`
  - `https://edge.activity.windows.com`

- <span data-ttu-id="eebe8-131">Points de terminaison Azure Information Protection:</span><span class="sxs-lookup"><span data-stu-id="eebe8-131">Azure Information Protection endpoints:</span></span>

  - `https://api.aadrm.com` <span data-ttu-id="eebe8-132">(pour la plupart des locataires)</span><span class="sxs-lookup"><span data-stu-id="eebe8-132">(for most tenants)</span></span>
  - `https://api.aadrm.de` <span data-ttu-id="eebe8-133">(pour les locataires résidant en Allemagne)</span><span class="sxs-lookup"><span data-stu-id="eebe8-133">(for tenants in Germany)</span></span>
  - `https://api.aadrm.cn` <span data-ttu-id="eebe8-134">(pour les locataires résidant en Chine)</span><span class="sxs-lookup"><span data-stu-id="eebe8-134">(for tenants in China)</span></span>

- [<span data-ttu-id="eebe8-135">Points de terminaison des services de notifications Windows.</span><span class="sxs-lookup"><span data-stu-id="eebe8-135">Windows Notification Service endpoints</span></span>](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## <span data-ttu-id="eebe8-136">Autres services de prise en charge de navigateur</span><span class="sxs-lookup"><span data-stu-id="eebe8-136">Other browser support services</span></span>

<span data-ttu-id="eebe8-137">Fournir des métadonnées pour les fonctionnalités de navigateur telles que la protection contre le suivi, les listes de révocation de certificats et d’autres mises à jour de composants de navigateur.</span><span class="sxs-lookup"><span data-stu-id="eebe8-137">Provide metadata for browser features such as tracking protection, certificate revocation lists, and other browser component updates.</span></span> <span data-ttu-id="eebe8-138">Fournir des dictionnaires de vérification orthographique téléchargeables et des listes rouges de blocage de publicités.</span><span class="sxs-lookup"><span data-stu-id="eebe8-138">Provide downloadable spellcheck dictionaries and ad-blocking block lists.</span></span> <span data-ttu-id="eebe8-139">Fournir des services pour prendre en charge des fonctionnalités de navigateur telles que les collections, le remplissage automatique et le magasin d’extensions.</span><span class="sxs-lookup"><span data-stu-id="eebe8-139">Provide services to support browser features such as collections, autofill, and extension store.</span></span>

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## <span data-ttu-id="eebe8-140">Articles associés</span><span class="sxs-lookup"><span data-stu-id="eebe8-140">See also</span></span>

- [<span data-ttu-id="eebe8-141">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="eebe8-141">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="eebe8-142">Page d’accueil de la documentation MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="eebe8-142">Microsoft Edge documentation landing page</span></span>](https://docs.microsoft.com/DeployEdge/)
- [<span data-ttu-id="eebe8-143">Gérer les points de terminaison de connexion pour Windows10 Entreprise, version1903</span><span class="sxs-lookup"><span data-stu-id="eebe8-143">Manage connection endpoints for Windows 10 Enterprise, version 1903</span></span>](https://docs.microsoft.com/windows/privacy/manage-windows-1903-endpoints)
