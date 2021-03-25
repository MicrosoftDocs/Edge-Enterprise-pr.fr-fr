---
title: Configurer des Sites dans la Liste des Sites en Mode Entreprise
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 05/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer la Liste des Sites d’Entreprise
ms.openlocfilehash: 9b1943e4d50dcc770b4a634b99ecbd001d1ffbcc
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447648"
---
# <a name="configure-sites-on-the-enterprise-mode-site-list"></a><span data-ttu-id="3687d-103">Configurer des Sites dans la Liste des Sites en Mode Entreprise</span><span class="sxs-lookup"><span data-stu-id="3687d-103">Configure Sites on the Enterprise Mode Site List</span></span>

<span data-ttu-id="3687d-104">Cet article décrit les modifications apportées à la Liste des Sites en Mode Entreprise qui prennent en charge la configuration du mode IE pour Microsoft Edge version 77 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3687d-104">This article describes changes to the Enterprise Mode Site List that support configuring IE mode for Microsoft Edge version 77 and later.</span></span>

<span data-ttu-id="3687d-105">Pour plus d’informations sur le schéma du fichier XML de Liste des Sites en Mode Entreprise, voir [Guide de schéma Mode Enterprise v.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="3687d-105">For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

> [!NOTE]
> <span data-ttu-id="3687d-106">Cet article concerne les canaux MicrosoftEdge **stable**, **Beta** et **Dev**, version77 ou ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3687d-106">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>

## <a name="updated-schema-elements"></a><span data-ttu-id="3687d-107">Éléments de schéma mis à jour</span><span class="sxs-lookup"><span data-stu-id="3687d-107">Updated schema elements</span></span>

<span data-ttu-id="3687d-108">Le tableau suivant décrit l’élément \<open-in app\> ajouté au schéma de mode entreprisev.2:</span><span class="sxs-lookup"><span data-stu-id="3687d-108">The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:</span></span>

| **<span data-ttu-id="3687d-109">Élément</span><span class="sxs-lookup"><span data-stu-id="3687d-109">Element</span></span>** | **<span data-ttu-id="3687d-110">Description</span><span class="sxs-lookup"><span data-stu-id="3687d-110">Description</span></span>** |
| --- | --- |
| \<open-in app="**true**"\> | <span data-ttu-id="3687d-111">Un élément enfant qui contrôle quel navigateur est utilisé pour les sites.</span><span class="sxs-lookup"><span data-stu-id="3687d-111">A child element that controls what browser is used for sites.</span></span> <span data-ttu-id="3687d-112">Cet élément est requis pour les sites qui doivent s’**ouvrir dans Internet Explorer11**.</span><span class="sxs-lookup"><span data-stu-id="3687d-112">This element is required for sites that need to **open in IE11**.</span></span>|

**<span data-ttu-id="3687d-113">Exemple:</span><span class="sxs-lookup"><span data-stu-id="3687d-113">Example:</span></span>**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

<span data-ttu-id="3687d-114">Le tableau suivant présente les valeurs possibles de l’élément \<open-in\>:</span><span class="sxs-lookup"><span data-stu-id="3687d-114">The following table shows the possible values of the \<open-in\> element:</span></span>

| **<span data-ttu-id="3687d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3687d-115">Value</span></span>** | **<span data-ttu-id="3687d-116">Description</span><span class="sxs-lookup"><span data-stu-id="3687d-116">Description</span></span>** |
| --- | --- |
| **\<open-in\><span data-ttu-id="3687d-117">IE11</span><span class="sxs-lookup"><span data-stu-id="3687d-117">IE11</span></span>\</open-in\>** | <span data-ttu-id="3687d-118">Ouvre le site en mode IE ou une fenêtre IE11 complète.</span><span class="sxs-lookup"><span data-stu-id="3687d-118">Opens the site in IE mode or a full IE11 window.</span></span> <span data-ttu-id="3687d-119">Pour activer le mode IE, voir [Configurer les stratégies de mode IE](./edge-ie-mode-policies.md)</span><span class="sxs-lookup"><span data-stu-id="3687d-119">To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)</span></span>|
| **\<open-in app="**true**"\><span data-ttu-id="3687d-120">IE11</span><span class="sxs-lookup"><span data-stu-id="3687d-120">IE11</span></span>\</open-in\>** | <span data-ttu-id="3687d-121">Ouvre le site dans une fenêtre IE11 complète</span><span class="sxs-lookup"><span data-stu-id="3687d-121">Opens the site in a full IE11 window</span></span> |
| **\<open-in\><span data-ttu-id="3687d-122">MSEdge</span><span class="sxs-lookup"><span data-stu-id="3687d-122">MSEdge</span></span>\</open-in\>** | <span data-ttu-id="3687d-123">Ouvre le site dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3687d-123">Opens the site in Microsoft Edge</span></span> |
| **\<open-in\><span data-ttu-id="3687d-124">Aucun ou non spécifié</span><span class="sxs-lookup"><span data-stu-id="3687d-124">None or not specified</span></span>\</open-in\>** | <span data-ttu-id="3687d-125">Ouvre le site dans le navigateur par défaut ou dans le navigateur où la navigation a été initialisée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3687d-125">Opens the site in the default browser or in the browser where the user navigated to the site.</span></span> |
|**\<open-in\><span data-ttu-id="3687d-126">Configurable</span><span class="sxs-lookup"><span data-stu-id="3687d-126">Configurable</span></span>\</open-in\>** | <span data-ttu-id="3687d-127">Permet au site de participer à la détermination du moteur du mode IE.</span><span class="sxs-lookup"><span data-stu-id="3687d-127">Allows the site to participate in IE mode engine determination.</span></span> <span data-ttu-id="3687d-128">Pour plus d’informations, consultez[En savoir plus sur les sites configurables en mode Internet Explorer](edge-learnmore-configurable-sites-ie-mode.md).</span><span class="sxs-lookup"><span data-stu-id="3687d-128">To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).</span></span>  |

>[!NOTE]
> <span data-ttu-id="3687d-129">L’attribut app=**"true"** est reconnu uniquement lorsqu’il est associé à _’open-in’ IE11_.</span><span class="sxs-lookup"><span data-stu-id="3687d-129">The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_.</span></span> <span data-ttu-id="3687d-130">Le fait de l’ajouter aux autres éléments «open-in» ne modifie pas le comportement du navigateur.</span><span class="sxs-lookup"><span data-stu-id="3687d-130">Adding it to the other 'open-in' elements won't change browser behavior.</span></span>   

## <a name="configure-neutral-sites"></a><span data-ttu-id="3687d-131">Configuration de sites neutres</span><span class="sxs-lookup"><span data-stu-id="3687d-131">Configure neutral sites</span></span>

<span data-ttu-id="3687d-132">Afin que le mode IE fonctionne correctement, l’authentification/les Serveurs à connexion unique doivent être expressément configurés en tant que sites neutres.</span><span class="sxs-lookup"><span data-stu-id="3687d-132">In order for IE mode to work properly, authentication / Single Sign-On servers will need to be explicitly configured as neutral sites.</span></span> <span data-ttu-id="3687d-133">Dans le cas contraire, les pages du mode IE tenteront d’effectuer une redirection vers Microsoft Edge, et l’authentification échouera.</span><span class="sxs-lookup"><span data-stu-id="3687d-133">Otherwise, IE mode pages will try to redirect to Microsoft Edge, and authentication will fail.</span></span>

<span data-ttu-id="3687d-134">Un site neutre utilise le navigateur dans lequel la navigation a commencé, soit Microsoft Edge, soit le mode IE.</span><span class="sxs-lookup"><span data-stu-id="3687d-134">A neutral site will use the browser where the navigation started - either Microsoft Edge or IE mode.</span></span> <span data-ttu-id="3687d-135">La configuration de sites neutres garantit que toutes les applications utilisant ces serveurs d’authentification, modernes et héritées, continuent de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="3687d-135">Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.</span></span>

<span data-ttu-id="3687d-136">Vous pouvez configurer des sites neutres en paramétrant le menu déroulant *Ouvrir dans* sur «Note»dans l’outil Gestionnaire de liste de sites en mode entreprise ou en mettant directement à jour le fichier XML de liste de sites:</span><span class="sxs-lookup"><span data-stu-id="3687d-136">You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:</span></span>

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

<span data-ttu-id="3687d-137">Pour identifier les serveurs d’authentification, examinez le trafic réseau d’une application à l’aide des outils de développement IE11.</span><span class="sxs-lookup"><span data-stu-id="3687d-137">To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools.</span></span> <span data-ttu-id="3687d-138">Si vous avez besoin de davantage de temps pour identifier vos serveurs d’authentification, vous pouvez configurer une stratégie pour conserver toute la navigation dans la page en mode IE.</span><span class="sxs-lookup"><span data-stu-id="3687d-138">If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigation in IE mode.</span></span> <span data-ttu-id="3687d-139">Pour réduire l’utilisation du mode IE, désactivez ce paramètre une fois que vous avez identifié et ajouté vos serveurs d’authentification à la liste des sites.</span><span class="sxs-lookup"><span data-stu-id="3687d-139">To minimize the use of IE mode, disable this setting once you've identified and added your authentication servers to the site list.</span></span> <span data-ttu-id="3687d-140">Pour plus d’informations, voir [Configurer la navigation dans des pages pour qu'elles restent en mode IE](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect).</span><span class="sxs-lookup"><span data-stu-id="3687d-140">For more information, see [Configure in-page navigation to remain in IE mode](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect).</span></span>

>[!NOTE]
   ><span data-ttu-id="3687d-141">Le schéma du mode entreprisev.1 n’est pas pris en charge pour l’intégration du mode IE.</span><span class="sxs-lookup"><span data-stu-id="3687d-141">Enterprise Mode schema v.1 isn't supported for IE mode integration.</span></span> <span data-ttu-id="3687d-142">Si vous utilisez actuellement le schémav.1 avec Internet Explorer11, vous devez effectuer la mise à niveau vers le schémav.2.</span><span class="sxs-lookup"><span data-stu-id="3687d-142">If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2.</span></span> <span data-ttu-id="3687d-143">Pour plus d’informations, consultez [Recommandations sur le schéma du mode Entreprisev.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="3687d-143">For more information, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

## <a name="see-also"></a><span data-ttu-id="3687d-144">Voir également</span><span class="sxs-lookup"><span data-stu-id="3687d-144">See also</span></span>

- [<span data-ttu-id="3687d-145">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="3687d-145">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="3687d-146">À propos du mode Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="3687d-146">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="3687d-147">Informations supplémentaires sur le mode entreprise</span><span class="sxs-lookup"><span data-stu-id="3687d-147">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)