---
title: Stratégie de configuration de site d’entreprise
ms.author: shisub
author: shisub
manager: srugh
ms.date: 03/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Guide pas à pas de la configuration de la liste des sites en mode Entreprise pour le mode Internet Explorer.
ms.openlocfilehash: 1d0b80950439fce77513413c3f5d1143538487d1
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470152"
---
# <a name="enterprise-site-configuration-strategy"></a><span data-ttu-id="2e478-103">Stratégie de configuration de site d’entreprise</span><span class="sxs-lookup"><span data-stu-id="2e478-103">Enterprise site configuration strategy</span></span>

<span data-ttu-id="2e478-104">Cet article décrit les modifications apportées à la liste des sites en mode Entreprise pour prendre en charge le mode Internet Explorer pour Microsoft Edge version77 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2e478-104">This article describes changes to the Enterprise Mode Site List to support Internet Explorer mode for Microsoft Edge version 77 and later.</span></span>

<span data-ttu-id="2e478-105">Pour plus d’informations sur le schéma du fichier XML de liste des sites en mode Entreprise, voir [Guide de schéma Mode Enterprise v.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="2e478-105">For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

> [!NOTE]
> <span data-ttu-id="2e478-106">Cet article concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2e478-106">This article applies to Microsoft Edge version 77 or later.</span></span>
<!--
## Updated schema elements

The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:

| **Element** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | A child element that controls what browser is used for sites. This element is required for sites that need to **open in IE11**.|

**Example:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

The following table shows the possible values of the \<open-in\> element:

| **Value** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Opens the site in IE mode or a full IE11 window. To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Opens the site in a full IE11 window |
| **\<open-in\>MSEdge\</open-in\>** | Opens the site in Microsoft Edge |
| **\<open-in\>None or not specified\</open-in\>** | Opens the site in the default browser or in the browser where the user navigated to the site. |
|**\<open-in\>Configurable\</open-in\>** | Allows the site to participate in IE mode engine determination. To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_. Adding it to the other 'open-in' elements won't change browser behavior.   -->

## <a name="configuration-strategy"></a><span data-ttu-id="2e478-107">Stratégie de configuration</span><span class="sxs-lookup"><span data-stu-id="2e478-107">Configuration strategy</span></span>

<span data-ttu-id="2e478-108">Les étapes suivantes font partie d’une stratégie de configuration de site pour le mode IE :</span><span class="sxs-lookup"><span data-stu-id="2e478-108">The following steps are part of a site configuration strategy for IE mode:</span></span>
1. <span data-ttu-id="2e478-109">Préparer votre liste des sites</span><span class="sxs-lookup"><span data-stu-id="2e478-109">Prepare your site list</span></span>
2. <span data-ttu-id="2e478-110">Configurer des sites neutres</span><span class="sxs-lookup"><span data-stu-id="2e478-110">Configure neutral sites</span></span>
3. <span data-ttu-id="2e478-111">(Facultatif) Utiliser le partage de cookies si nécessaire</span><span class="sxs-lookup"><span data-stu-id="2e478-111">(Optional) Use cookie sharing if necessary</span></span>

<!--
Step 1.  – if you don’t have one use Site Discovery Step-by-Step
Step 2 – Neutral sites + sticky mode
        Use more examples and explain sticky mode better
Step 3 – If that doesn’t cover your needs, then use Cookie sharing -->

## <a name="prepare-your-site-list"></a><span data-ttu-id="2e478-112">Préparer votre liste des sites</span><span class="sxs-lookup"><span data-stu-id="2e478-112">Prepare your site list</span></span>

<span data-ttu-id="2e478-113">Si vous avez déjà une liste des sites en mode Entreprise pour IE11 ou Microsoft Edge Hérité, vous pouvez la réutiliser pour configurer le mode IE.</span><span class="sxs-lookup"><span data-stu-id="2e478-113">If you already have an Enterprise Mode site list for IE11 or Microsoft Edge Legacy, you can reuse it to configure IE mode.</span></span>

<span data-ttu-id="2e478-114">Toutefois, si vous n’avez pas de liste des sites, vous pouvez utiliser [l’outil de découverte de site d’entreprise](https://docs.microsoft.com/deployedge/edge-ie-mode-site-discovery) pour remplir votre liste des sites.</span><span class="sxs-lookup"><span data-stu-id="2e478-114">However, if you don't have a site list, you can use the [Enterprise Site Discovery tool](https://docs.microsoft.com/deployedge/edge-ie-mode-site-discovery) to populate your site list.</span></span>

## <a name="configure-neutral-sites"></a><span data-ttu-id="2e478-115">Configurer des sites neutres</span><span class="sxs-lookup"><span data-stu-id="2e478-115">Configure neutral sites</span></span>

<span data-ttu-id="2e478-116">Pour que le mode IE fonctionne correctement, les serveurs d’authentification/authentification unique (SSO) doivent être explicitement configurés en tant que sites neutres.</span><span class="sxs-lookup"><span data-stu-id="2e478-116">In order for IE mode to work properly, authentication / Single Sign-On (SSO) servers will need to be explicitly configured as neutral sites.</span></span> <span data-ttu-id="2e478-117">Dans le cas contraire, les pages du mode IE tenteront d’effectuer une redirection vers Microsoft Edge, et l’authentification échouera.</span><span class="sxs-lookup"><span data-stu-id="2e478-117">Otherwise, IE mode pages will try to redirect to Microsoft Edge, and authentication will fail.</span></span>

<span data-ttu-id="2e478-118">Un site neutre utilise le navigateur dans lequel la navigation a commencé, soit Microsoft Edge, soit le mode IE.</span><span class="sxs-lookup"><span data-stu-id="2e478-118">A neutral site will use the browser where the navigation started - either Microsoft Edge or IE mode.</span></span> <span data-ttu-id="2e478-119">La configuration de sites neutres garantit que toutes les applications utilisant ces serveurs d’authentification, modernes et héritées, continuent de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="2e478-119">Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.</span></span>

<span data-ttu-id="2e478-120">Vous pouvez configurer des sites neutres en paramétrant le menu déroulant *Ouvrir dans* sur «Note»dans l’outil Gestionnaire de liste de sites en mode entreprise ou en mettant directement à jour le fichier XML de liste de sites:</span><span class="sxs-lookup"><span data-stu-id="2e478-120">You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:</span></span>

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

<span data-ttu-id="2e478-121">Pour identifier les serveurs d’authentification, examinez le trafic réseau d’une application à l’aide des outils de développement IE11.</span><span class="sxs-lookup"><span data-stu-id="2e478-121">To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools.</span></span> <span data-ttu-id="2e478-122">Si vous avez besoin de plus de temps pour identifier vos serveurs d’authentification, vous pouvez configurer une stratégie pour conserver toutes les navigations dans la page en mode IE afin de permettre à vos utilisateurs de poursuivre leurs flux de travail sans interruption.</span><span class="sxs-lookup"><span data-stu-id="2e478-122">If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigations in IE mode to allow your users to continue their workflows uninterrupted.</span></span> <span data-ttu-id="2e478-123">Pour réduire l’utilisation du mode IE lorsque cela est inutile, désactivez ce paramètre une fois que vous avez identifié et ajouté vos serveurs d’authentification à la liste des sites.</span><span class="sxs-lookup"><span data-stu-id="2e478-123">To minimize the use of IE mode when unnecessary, disable this setting once you've identified and added your authentication servers to the site list.</span></span> <span data-ttu-id="2e478-124">Pour plus d’informations, voir [Conserver la navigation dans la page en mode IE.](https://docs.microsoft.com/deployedge/edge-learnmore-inpage-nav)</span><span class="sxs-lookup"><span data-stu-id="2e478-124">For more information, see [Keep in-page navigation in IE mode](https://docs.microsoft.com/deployedge/edge-learnmore-inpage-nav).</span></span>

>[!NOTE]
   ><span data-ttu-id="2e478-125">Le schéma du mode entreprisev.1 n’est pas pris en charge pour l’intégration du mode IE.</span><span class="sxs-lookup"><span data-stu-id="2e478-125">Enterprise Mode schema v.1 isn't supported for IE mode integration.</span></span> <span data-ttu-id="2e478-126">Si vous utilisez actuellement le schémav.1 avec Internet Explorer11, vous devez effectuer la mise à niveau vers le schémav.2.</span><span class="sxs-lookup"><span data-stu-id="2e478-126">If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2.</span></span> <span data-ttu-id="2e478-127">Pour plus d’informations, consultez [Recommandations sur le schéma du mode Entreprisev.2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="2e478-127">For more information, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

## <a name="optional-use-cookie-sharing-if-necessary"></a><span data-ttu-id="2e478-128">(Facultatif) Utiliser le partage de cookies si nécessaire</span><span class="sxs-lookup"><span data-stu-id="2e478-128">(Optional) Use cookie sharing if necessary</span></span>

<span data-ttu-id="2e478-129">Par défaut, les processus Microsoft Edge et Internet Explorer ne partagent pas les cookies de session, et ce manque de partage peut être peu pratique dans certains cas lors de l’utilisation du mode IE.</span><span class="sxs-lookup"><span data-stu-id="2e478-129">By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this lack of sharing can be inconvenient in some cases while using IE mode.</span></span> <span data-ttu-id="2e478-130">Par exemple, lorsqu’un utilisateur doit s’authentifier à nouveau en mode IE alors qu’auparavant il était habitué à le faire ou lors de la connexion d’une session Microsoft Edge, il ne se déconnecte pas de la session en mode Internet Explorer pour les transactions critiques.</span><span class="sxs-lookup"><span data-stu-id="2e478-130">For example, when a user has to reauthenticate in IE mode when previously they are accustomed to doing so or when signing out of a Microsoft Edge session doesn’t sign out of the Internet Explorer mode session for critical transactions.</span></span> <span data-ttu-id="2e478-131">Dans ces scénarios, vous pouvez configurer des cookies spécifiques définis par l’authentification unique pour qu’ils soient envoyés de Microsoft Edge à Internet Explorer afin que l’expérience d’authentification devienne plus transparente en éliminant la nécessité de s’authentifier à nouveau.</span><span class="sxs-lookup"><span data-stu-id="2e478-131">In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to reauthenticate.</span></span> <span data-ttu-id="2e478-132">Pour plus d’informations, voir [Partage de cookies de Microsoft Edge vers Internet Explorer](https://docs.microsoft.com/deployedge/edge-ie-mode-add-guidance-cookieshare).</span><span class="sxs-lookup"><span data-stu-id="2e478-132">For more information, see [Cookie sharing from Microsoft Edge to Internet Explorer](https://docs.microsoft.com/deployedge/edge-ie-mode-add-guidance-cookieshare).</span></span>

## <a name="see-also"></a><span data-ttu-id="2e478-133">Voir également</span><span class="sxs-lookup"><span data-stu-id="2e478-133">See also</span></span>

- [<span data-ttu-id="2e478-134">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="2e478-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="2e478-135">À propos du mode Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="2e478-135">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="2e478-136">Informations supplémentaires sur le mode entreprise</span><span class="sxs-lookup"><span data-stu-id="2e478-136">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
