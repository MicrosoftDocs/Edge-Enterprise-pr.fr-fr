---
title: Microsoft Edge et sites configurables en mode InternetExplorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/28/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge et sites configurables en mode InternetExplorer
ms.openlocfilehash: a846d71d63a4f837041acc9b601f704999bb826a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979808"
---
# <span data-ttu-id="22aa9-103">Découvrez les sites configurables en mode InternetExplorer</span><span class="sxs-lookup"><span data-stu-id="22aa9-103">Learn about Configurable sites in IE mode</span></span>

<span data-ttu-id="22aa9-104">Cet article décrit la fonctionnalité de sites configurables de la liste des sites en mode Entreprise lorsque vous utilisez le mode InternetExplorer dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="22aa9-104">This article explains the Configurable sites feature of the Enterprise Mode Site List when using IE mode in Microsoft Edge.</span></span>

## <span data-ttu-id="22aa9-105">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="22aa9-105">Prerequisites</span></span>

- <span data-ttu-id="22aa9-106">Mises à jour Windows</span><span class="sxs-lookup"><span data-stu-id="22aa9-106">Windows updates</span></span>

  - <span data-ttu-id="22aa9-107">Windows10 version1909, Windows Server version1909 – KB4550945 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="22aa9-107">Windows 10 version 1909, Windows server version 1909 – KB4550945  or higher</span></span>
  - <span data-ttu-id="22aa9-108">Windows10 version1903, Windows Server version1903 – KB4550945 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="22aa9-108">Windows 10 version 1903, Windows server version 1903 – KB4550945  or higher</span></span>
  - <span data-ttu-id="22aa9-109">Windows10 version1809, Windows Server version1809 et Windows Server2019 – KB4550969 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="22aa9-109">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4550969 or higher</span></span>
  - <span data-ttu-id="22aa9-110">Windows10 version1803 – KB4550944 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="22aa9-110">Windows 10 version 1803 – KB4550944 or higher</span></span>
  - <span data-ttu-id="22aa9-111">Windows10 version1607, Windows Server2016 – KB4556826 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="22aa9-111">Windows 10 version 1607, Windows Server 2016 - KB4556826 or higher</span></span>
  - <span data-ttu-id="22aa9-112">Version initiale de Windows10, juillet2015 – KB4550947 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="22aa9-112">Windows 10 initial version, July 2015 - KB4550947 or higher</span></span>
  - <span data-ttu-id="22aa9-113">Windows8.1 – KB4556798 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="22aa9-113">Windows 8.1 – KB4556798 or higher</span></span>

- <span data-ttu-id="22aa9-114">Microsoft Edge version83 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="22aa9-114">Microsoft Edge version 83 or later</span></span>
- <span data-ttu-id="22aa9-115">[Mode Internet Explorer](https://aka.ms/iemodeonedge) configuré avec la liste des sites en mode Entreprise</span><span class="sxs-lookup"><span data-stu-id="22aa9-115">[IE mode](https://aka.ms/iemodeonedge) configured with Enterprise Mode Site List</span></span>

## <span data-ttu-id="22aa9-116">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="22aa9-116">Overview</span></span>

<span data-ttu-id="22aa9-117">La configuration des sites nécessitant le mode InternetExplorer dans la liste des sites en mode Entreprise fonctionne parfaitement pour la plupart des environnements avec des applications héritées.</span><span class="sxs-lookup"><span data-stu-id="22aa9-117">Configuring sites needing IE mode in the Enterprise Mode Site List will work well for most environments with legacy applications.</span></span> <span data-ttu-id="22aa9-118">Toutefois, dans certains cas, il ne s’agit pas de la meilleure approche pour configurer un sous-ensemble de sites afin qu’il s’ouvre en mode InternetExplorer sans afficher l’intégralité d’un domaine en mode InternetExplorer.</span><span class="sxs-lookup"><span data-stu-id="22aa9-118">However, in some cases this approach isn't the best to configure a subset of sites to open in IE mode without rendering an entire domain in IE mode.</span></span> <span data-ttu-id="22aa9-119">Par exemple, lorsque votre environnement contient des applications modernes et héritées qui s’exécutent sur un seul serveur, et que vous aimeriez afficher uniquement les applications héritées en mode Internet Explorer et les applications restantes en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="22aa9-119">For example, when your environment contains both modern and legacy applications running on a single server and you would like the flexibility to render only the legacy applications in IE mode and the remaining applications to render in Microsoft Edge mode.</span></span>

<span data-ttu-id="22aa9-120">La solution consiste à utiliser la fonctionnalité de sites configurables de la liste des sites en mode Entreprise.</span><span class="sxs-lookup"><span data-stu-id="22aa9-120">The solution is to use the Configurable sites feature of the Enterprise Mode Site List.</span></span> <span data-ttu-id="22aa9-121">Lorsque la fonctionnalité est activée, Microsoft Edge permet aux sites disposant de la balise «configurable» de participer à la détermination du moteur du mode Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="22aa9-121">When the feature is enabled, Microsoft Edge will allow sites with the "configurable" tag to participate in IE mode engine determination.</span></span>

## <span data-ttu-id="22aa9-122">Fonctionnement des sites configurables</span><span class="sxs-lookup"><span data-stu-id="22aa9-122">How Configurable sites works</span></span>

### <span data-ttu-id="22aa9-123">Basculement automatique du moteur Microsoft Edge vers le moteur du mode InternetExplorer</span><span class="sxs-lookup"><span data-stu-id="22aa9-123">Automatic switching from the Microsoft Edge engine to the IE mode engine</span></span>

<span data-ttu-id="22aa9-124">Pour utiliser la fonctionnalité de sites configurables et que l’option `<open-in>Configurable</open-in>` soit disponible, la liste des sites en mode Entreprise doit contenir au moins un site.</span><span class="sxs-lookup"><span data-stu-id="22aa9-124">To use the Configurable sites feature, you'll need one or more sites in the Enterprise Mode Site List to have the `<open-in>Configurable</open-in>` option.</span></span>

<span data-ttu-id="22aa9-125">Exemple:</span><span class="sxs-lookup"><span data-stu-id="22aa9-125">Example:</span></span>

```
<site-list version="1">
  <site url="app.com">
    <open-in>Configurable</open-in>
  </site>
</site-list>
```

<span data-ttu-id="22aa9-126">Lorsque la fonctionnalité de sites configurables est activée, le comportement suivant se produit:</span><span class="sxs-lookup"><span data-stu-id="22aa9-126">When the Configurable sites feature is enabled, the following behavior occurs:</span></span>

1. <span data-ttu-id="22aa9-127">Lorsque vous envoyez une demande à un site configurable, Microsoft Edge envoie l’en-tête de demande HTTP «`X-InternetExplorerModeConfigurable: 1`».</span><span class="sxs-lookup"><span data-stu-id="22aa9-127">When making a request to a Configurable site, Microsoft Edge will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`".</span></span>
2. <span data-ttu-id="22aa9-128">Un site configurable peut envoyer une réponse de redirection (par exemple, HTTP302) avec l’en-tête de réponse HTTP «`X-InternetExplorerMode: 1`» pour demander à Microsoft Edge de charger le site en mode Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="22aa9-128">A Configurable site may send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 1`" to request that Microsoft Edge loads the site in IE mode.</span></span>
3. <span data-ttu-id="22aa9-129">La cible de la redirection (autrement dit, la valeur de l’en-tête de réponse **Location**) doit également être un site **Configurable** ou **Neutre**, sans quoi l’en-tête de réponse du mode Internet Explorer ne sera pas pris en compte.</span><span class="sxs-lookup"><span data-stu-id="22aa9-129">The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored.</span></span> <span data-ttu-id="22aa9-130">De manière générale, il est attendu que la cible de la redirection soit identique à l’URL d’origine.</span><span class="sxs-lookup"><span data-stu-id="22aa9-130">It's expected that the target of the redirect will usually be the same as the original URL.</span></span> <span data-ttu-id="22aa9-131">Cela n’est toutefois pas une nécessité.</span><span class="sxs-lookup"><span data-stu-id="22aa9-131">However, it doesn't have to be.</span></span>

   > [!NOTE]
   > <span data-ttu-id="22aa9-132">La réponse de redirection fait l’objet d’une mise en cache HTTP normale de Microsoft Edge pour les redirections.</span><span class="sxs-lookup"><span data-stu-id="22aa9-132">The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.</span></span>

### <span data-ttu-id="22aa9-133">Rebasculement du moteur du mode Internet Explorer vers le moteur Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="22aa9-133">Switching back from IE mode engine to Microsoft Edge engine</span></span>

<span data-ttu-id="22aa9-134">L’activation de sites configurables dans Microsoft Edge active automatiquement les comportements suivants dans les onglets du mode InternetExplorer:</span><span class="sxs-lookup"><span data-stu-id="22aa9-134">Enabling Configurable sites in Microsoft Edge automatically enables the following behaviors in IE mode tabs:</span></span>

1. <span data-ttu-id="22aa9-135">Lorsque vous envoyez une demande à un site configurable, les onglets du mode Internet Explorer envoient l’en-tête de demande HTTP «`X-InternetExplorerModeConfigurable: 1`», le même que celui des onglets Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="22aa9-135">When making a request to a Configurable site, IE mode tabs will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`", the same as Microsoft Edge tabs.</span></span>
2. <span data-ttu-id="22aa9-136">Un site configurable peut envoyer une réponse de redirection (par exemple, HTTP302) avec l’en-tête de réponse HTTP «`X-InternetExplorerMode: 0`» pour demander le basculement de la navigation en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="22aa9-136">A Configurable site might send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 0`" to request that the navigation switch back to Microsoft Edge mode.</span></span>
3. <span data-ttu-id="22aa9-137">La cible de la redirection (autrement dit, la valeur de l’en-tête de réponse **Location**) doit également être un site **Configurable** ou **Neutre**, sans quoi l’en-tête de réponse du mode Internet Explorer ne sera pas pris en compte.</span><span class="sxs-lookup"><span data-stu-id="22aa9-137">The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored.</span></span> <span data-ttu-id="22aa9-138">De manière générale, il est attendu que la cible de la redirection soit identique à l’URL d’origine.</span><span class="sxs-lookup"><span data-stu-id="22aa9-138">It's expected that the target of the redirect will usually be the same as the original URL.</span></span> <span data-ttu-id="22aa9-139">Cela n’est toutefois pas une nécessité.</span><span class="sxs-lookup"><span data-stu-id="22aa9-139">However, it doesn't have to be.</span></span>

   > [!NOTE]
   > <span data-ttu-id="22aa9-140">La réponse de redirection fait l’objet d’une mise en cache HTTP normale de Microsoft Edge pour les redirections.</span><span class="sxs-lookup"><span data-stu-id="22aa9-140">The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.</span></span>

> [!TIP]
> <span data-ttu-id="22aa9-141">Les deux moteurs de navigateur envoient le même en-tête de demande «`X-InternetExplorerModeConfigurable: 1`» aux sites configurables.</span><span class="sxs-lookup"><span data-stu-id="22aa9-141">Both browser engines send the same "`X-InternetExplorerModeConfigurable: 1`" request header to Configurable sites.</span></span> <span data-ttu-id="22aa9-142">Vous devez utiliser l’en-tête de requête User-Agent pour faire la distinction entre les demandes en provenance du mode Microsoft Edge et celles du mode Internet Explorer, afin d’éviter la redirection lorsque le site est déjà chargé dans le bon moteur.</span><span class="sxs-lookup"><span data-stu-id="22aa9-142">You should use the User-Agent request header to distinguish between requests from Microsoft Edge mode vs. IE mode to avoid redirecting when the site is already loading in the correct engine.</span></span>

## <span data-ttu-id="22aa9-143">Voir également</span><span class="sxs-lookup"><span data-stu-id="22aa9-143">See also</span></span>

- [<span data-ttu-id="22aa9-144">À propos du mode Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="22aa9-144">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="22aa9-145">Informations supplémentaires sur le mode entreprise</span><span class="sxs-lookup"><span data-stu-id="22aa9-145">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="22aa9-146">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="22aa9-146">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)