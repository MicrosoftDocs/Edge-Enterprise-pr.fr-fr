---
title: Partage de cookies de Microsoft Edge vers Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Mode de partage de cookies de Microsoft Edge vers Internet Explorer '
ms.openlocfilehash: ddd9d34b5e2b0ee49093734da82e4a4fa7aa6a69
ms.sourcegitcommit: 306582403d4272831bcac390154c7cc7041a9b7e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/21/2020
ms.locfileid: "11238181"
---
# <span data-ttu-id="12681-103">Partage de cookies de Microsoft Edge vers Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="12681-103">Cookie sharing from Microsoft Edge to Internet Explorer</span></span>

<span data-ttu-id="12681-104">Cet article décrit la configuration du partage de cookies de session d’un processus Microsoft Edge vers un processus Internet Explorer, en utilisant le mode Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="12681-104">This article explains explains how to configure session cookie sharing from a Microsoft Edge process to Internet Explorer process, while using Internet Explorer mode.</span></span>

> [!NOTE]
> <span data-ttu-id="12681-105">Cet article concerne MicrosoftEdge version87 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="12681-105">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="12681-106">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="12681-106">Prerequisites</span></span>

- <span data-ttu-id="12681-107">Mises à jour Windows</span><span class="sxs-lookup"><span data-stu-id="12681-107">Windows updates</span></span>

  - <span data-ttu-id="12681-108">Windows 10 version 2004, Windows Server version 2004-KB4571744 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="12681-108">Windows 10 version 2004, Windows Server version 2004 - KB4571744 or higher</span></span>
  - <span data-ttu-id="12681-109">Windows 10 version 1909, Windows Server version 1909 – KB4566116 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="12681-109">Windows 10 version 1909, Windows Server version 1909 – KB4566116 or higher</span></span>
  - <span data-ttu-id="12681-110">Windows 10 version 1903, Windows Server version 1903 – KB4566116 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="12681-110">Windows 10 version 1903, Windows Server version 1903 – KB4566116 or higher</span></span>
  - <span data-ttu-id="12681-111">Windows10 version1809, Windows Server version1809 et Windows Server2019 – KB4571748 ou plus</span><span class="sxs-lookup"><span data-stu-id="12681-111">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4571748 or higher</span></span>
  - <span data-ttu-id="12681-112">Windows10 version1803: KB4577032 ou plus</span><span class="sxs-lookup"><span data-stu-id="12681-112">Windows 10 version 1803 – KB4577032 or higher</span></span>

- <span data-ttu-id="12681-113">Microsoft Edge version87 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="12681-113">Microsoft Edge version 87 or later</span></span>
- <span data-ttu-id="12681-114">[Mode Internet Explorer](https://aka.ms/iemodeonedge)  configuré avec la liste des sites en mode Entreprise</span><span class="sxs-lookup"><span data-stu-id="12681-114">[IE mode](https://aka.ms/iemodeonedge) configured with Enterprise Mode Site List</span></span>

## <span data-ttu-id="12681-115">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="12681-115">Overview</span></span>

<span data-ttu-id="12681-116">Une configuration courante dans les grandes organisations consiste à lier une application qui fonctionne sur un navigateur moderne à une autre application, configurable pour s’ouvrir en mode Internet Explorer avec l’authentification unique (SSO) activée dans le flux de travail.</span><span class="sxs-lookup"><span data-stu-id="12681-116">A common configuration in large organizations is to have an application that works on a modern browser link to another application, which might be configured to open in Internet Explorer mode with Single Sign On (SSO) enabled as part of the workflow.</span></span>

<span data-ttu-id="12681-117">Par défaut, les processus Microsoft Edge et Internet Explorer ne partagent pas de cookies de session, ce qui peut s’avérer gênant dans certains cas.</span><span class="sxs-lookup"><span data-stu-id="12681-117">By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this can be inconvenient in some cases.</span></span> <span data-ttu-id="12681-118">Par exemple, lorsqu’un utilisateur doit s’authentifier de nouveau en mode Internet Explorer ou lorsque la déconnexion d’une session Microsoft Edge n’entraîne pas celle de la session en mode Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="12681-118">For example, when a user has to re-authenticate in Internet Explorer mode or when signing out of an Microsoft Edge session doesn’t sign out of the Internet Explorer mode session.</span></span> <span data-ttu-id="12681-119">Dans ces scénarios, vous pouvez configurer des cookies spécifiques définis par l’authentification unique pour qu’ils soient envoyés à partir de Microsoft Edge vers Internet Explorer pour que l’expérience d’authentification devienne plus transparente en éliminant la nécessité de s’authentifier à nouveau.</span><span class="sxs-lookup"><span data-stu-id="12681-119">In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to re-authenticate.</span></span>

> [!NOTE]
> <span data-ttu-id="12681-120">Vous pouvez partager des cookies de session uniquement de Microsoft Edge vers Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="12681-120">Session cookies can only be shared from Microsoft Edge to Internet Explorer.</span></span> <span data-ttu-id="12681-121">Vous ne pouvez pas partager de cookies de session dans le sens inverse (d’Internet Explorer vers Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="12681-121">Sharing session cookies in reverse (from Internet Explorer to Microsoft Edge) isn't possible.</span></span>

## <span data-ttu-id="12681-122">Fonctionnement du partage de cookies</span><span class="sxs-lookup"><span data-stu-id="12681-122">How cookie sharing works</span></span>

<span data-ttu-id="12681-123">Nous avons étendu le fichier XML de liste de sites en mode entreprise pour autoriser des éléments supplémentaires à spécifier des cookies à partager depuis une session Microsoft Edge avec Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="12681-123">The Enterprise Mode site list XML has been extended to allow additional elements to specify cookies that need to be shared from a Microsoft Edge session with Internet Explorer.</span></span>  

<span data-ttu-id="12681-124">Lors de la première création d’un onglet de mode Internet Explorer dans une session Microsoft Edge, le partage de tous les cookies correspondants s’effectue vers la session Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="12681-124">The first time an Internet Explorer mode tab is created in a Microsoft Edge session, all matching cookies are shared to the Internet Explorer session.</span></span> <span data-ttu-id="12681-125">Par la suite, chaque fois à chaque ajout, suppression ou modification d’un cookie qui correspond à une règle, l’application envoie ce cookie sous forme de mise à jour à la session Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="12681-125">Subsequently, any time a cookie that matches a rule is added, deleted, or modified it is sent as an update to the Internet Explorer session.</span></span> <span data-ttu-id="12681-126">L’ensemble de cookies partagés fait également l’objet d’une réévaluation lors de la mise à jour de la liste de sites.</span><span class="sxs-lookup"><span data-stu-id="12681-126">The set of shared cookies is also re-evaluated when the site list is updated.</span></span>

### <span data-ttu-id="12681-127">Éléments de schéma mis à jour</span><span class="sxs-lookup"><span data-stu-id="12681-127">Updated schema elements</span></span>

<span data-ttu-id="12681-128">Le tableau suivant décrit l’élément \<shared-cookie\> ajouté pour la prise en charge de la fonctionnalité de partage de cookies.</span><span class="sxs-lookup"><span data-stu-id="12681-128">The following table describes the \<shared-cookie\> element added to support the cookie sharing feature.</span></span>

| <span data-ttu-id="12681-129">Élément</span><span class="sxs-lookup"><span data-stu-id="12681-129">Element</span></span>| <span data-ttu-id="12681-130">Description</span><span class="sxs-lookup"><span data-stu-id="12681-130">Description</span></span> |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br><span data-ttu-id="12681-131">OU</span><span class="sxs-lookup"><span data-stu-id="12681-131">OR</span></span><br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |<span data-ttu-id="12681-132">**(obligatoire)** Un élément \<shared-cookie\> nécessite au minimum un attribut de *domaine* (pour les cookies de domaine) ou un attribut d’*hôte* (pour les cookies hôtes uniquement) et un attribut de *nom*.</span><span class="sxs-lookup"><span data-stu-id="12681-132">**(Required)** A \<shared-cookie\> element requires, at minimum, a *domain* (for domain cookies) or a *host* (for host-only cookies) attribute and a *name* attribute.</span></span><br><span data-ttu-id="12681-133">Il doit s’agir de correspondances exactes avec le domaine et le nom du cookie, respectivement.</span><span class="sxs-lookup"><span data-stu-id="12681-133">These must be exact matches to the cookie's domain and name respectively.</span></span> <span data-ttu-id="12681-134">**Notez** que les sous-domaines ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="12681-134">**Note** that subdomains do not match.</span></span><br><br><span data-ttu-id="12681-135">Nous utilisons l’attribut de *domaine* pour les cookies de domaine (et nous autorisons un point de début, cependant facultatif).</span><span class="sxs-lookup"><span data-stu-id="12681-135">The *domain* attribute is used for domain cookies (and a leading dot is allowed but optional).</span></span><br><span data-ttu-id="12681-136">Nous utilisons l’attribut d’*hôte* pour les cookies hôtes uniquement (et un point de début correspond à une erreur).</span><span class="sxs-lookup"><span data-stu-id="12681-136">The *host* attribute is used for host-only cookies (and a leading dot is an error).</span></span> <span data-ttu-id="12681-137">Le fait de ne spécifier aucun de ces attributs ou les deux attributs génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="12681-137">Specifying neither or both will result in an error.</span></span><br><span data-ttu-id="12681-138">\* Un cookie est un cookie de domaine si la chaîne de cookie comprend un domaine spécifié (par le biais de l’en-tête de réponse HTTP Set-Cookie ou de l’API document.cookie JS).</span><span class="sxs-lookup"><span data-stu-id="12681-138">\* A cookie is a domain cookie if a domain was specified in the cookie string (via HTTP Set-Cookie response header or document.cookie JS API).</span></span> <span data-ttu-id="12681-139">Un cookie de domaine s’applique au domaine spécifié et à tous les sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="12681-139">A domain cookie applies to the specified domain and all subdomains.</span></span> <span data-ttu-id="12681-140">Si la chaîne de cookie ne comprend aucun domaine spécifié, le cookie est un cookie d’hôte uniquement qui s’applique uniquement à l’hôte spécifique pour lequel il a été défini.</span><span class="sxs-lookup"><span data-stu-id="12681-140">If a domain was not specified in the cookie string, the cookie is a host-only cookie and only applies to the specific host that it was set for.</span></span> <span data-ttu-id="12681-141">Notez que certaines classes d’URL telles que les noms d’hôte en un seul mot (par exemple, http://intranetsite) et les adresses IP (par exemple, http://10.0.0.1) ne peuvent définir que des cookies d’hôte uniquement.</span><span class="sxs-lookup"><span data-stu-id="12681-141">Note that some classes of URLs such as single-word hostnames (e.g. http://intranetsite) and IP addresses (e.g. http://10.0.0.1) can only set host-only cookies.</span></span>    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | <span data-ttu-id="12681-142">\*\* (facultatif)\*\* Vous pouvez spécifier un attribut de *chemin d’accès*.</span><span class="sxs-lookup"><span data-stu-id="12681-142">**(Optional)** A *path* attribute may be specified.</span></span> <span data-ttu-id="12681-143">Si vous ne spécifiez aucun attribut de chemin d'accès (ou si cet attribut est vide), les cookies qui correspondent à un domaine/hôte et à un nom correspondent à la stratégie, quel que soit le chemin d’accès (règle de caractère générique).</span><span class="sxs-lookup"><span data-stu-id="12681-143">If no path attribute is specified (or if the path attribute is empty), any cookies matching domain/host and name match the policy, regardless of path (wildcard rule).</span></span><br><br><span data-ttu-id="12681-144">Si vous spécifiez un chemin d’accès, celui-ci doit être une correspondance exacte.</span><span class="sxs-lookup"><span data-stu-id="12681-144">If a path is specified, it must be an exact match.</span></span><br><span data-ttu-id="12681-145">Les cookie correspondant à une règle avec un chemin d’accès ont priorité sur les règles sans chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="12681-145">If a cookie matches a rule with a path, that takes precedence over a rule without a path.</span></span> |

#### <span data-ttu-id="12681-146">Exemple de partage</span><span class="sxs-lookup"><span data-stu-id="12681-146">Sharing example</span></span>

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## <span data-ttu-id="12681-147">Voir également</span><span class="sxs-lookup"><span data-stu-id="12681-147">See also</span></span>

- [<span data-ttu-id="12681-148">À propos du mode IE</span><span class="sxs-lookup"><span data-stu-id="12681-148">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="12681-149">Informations sur les sites configurables</span><span class="sxs-lookup"><span data-stu-id="12681-149">Configurable sites information</span></span>](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [<span data-ttu-id="12681-150">Informations supplémentaires sur le mode entreprise</span><span class="sxs-lookup"><span data-stu-id="12681-150">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="12681-151">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="12681-151">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
