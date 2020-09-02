---
title: Format de filtre pour les stratégies d’URL de MicrosoftEdge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez le format de filtre utilisé pour les stratégies URLBlocklist et URLAllowlist de MicrosoftEdge.
ms.openlocfilehash: 5a0eff1ca7be17fccd1087716d426b13ea302847
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979755"
---
# <span data-ttu-id="77ded-103">Format de filtre pour les stratégies basées sur une liste d’URL</span><span class="sxs-lookup"><span data-stu-id="77ded-103">Filter format for URL list-based policies</span></span>

<span data-ttu-id="77ded-104">Cet article décrit le format de filtre utilisé pour les stratégies basées sur les listes d’URL de MicrosoftEdge (par exemple, [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist) et [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls).</span><span class="sxs-lookup"><span data-stu-id="77ded-104">This article describes the filter format used for the Microsoft Edge URL list-based policies (For example, [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist), and [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls) policies.</span></span>

> [!NOTE]
> <span data-ttu-id="77ded-105">Cet article concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="77ded-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="77ded-106">Format de filtre</span><span class="sxs-lookup"><span data-stu-id="77ded-106">The filter format</span></span>

<span data-ttu-id="77ded-107">Le format de filtre est:</span><span class="sxs-lookup"><span data-stu-id="77ded-107">The filter format is:</span></span>

```
    [scheme://][.]host[:port][/path][@query]
```

<span data-ttu-id="77ded-108">Les champs de format de filtre sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="77ded-108">The fields in the filter format are:</span></span>

| <span data-ttu-id="77ded-109">Champ</span><span class="sxs-lookup"><span data-stu-id="77ded-109">Field</span></span> | <span data-ttu-id="77ded-110">Description</span><span class="sxs-lookup"><span data-stu-id="77ded-110">Description</span></span> |
| --- | --- |
| <span data-ttu-id="77ded-111">**schéma** (*facultatif*)</span><span class="sxs-lookup"><span data-stu-id="77ded-111">**scheme** (*optional*)</span></span> | <span data-ttu-id="77ded-112">Il peut s’agir de http://, https://, ftp://, edge://, etc.</span><span class="sxs-lookup"><span data-stu-id="77ded-112">It can be http://, https://, ftp://, edge://, etc.</span></span> |
| <span data-ttu-id="77ded-113">**hôte** (*obligatoire*)</span><span class="sxs-lookup"><span data-stu-id="77ded-113">**host** (*required*)</span></span> | <span data-ttu-id="77ded-114">Il doit s’agir d’un nom d’hôte ou d’une adresse IP valides, et vous pouvez utiliser un caractère générique («\*»).</span><span class="sxs-lookup"><span data-stu-id="77ded-114">It must be a valid host name or IP address and you can use a wildcard ("\*").</span></span> <span data-ttu-id="77ded-115">Pour désactiver la correspondance de sous-domaines, vous pouvez insérer un point facultatif («.») devant l’**hôte**.</span><span class="sxs-lookup"><span data-stu-id="77ded-115">To disable subdomain matching, include an optional dot (".") before **host**.</span></span> |
| <span data-ttu-id="77ded-116">**port** (*facultatif*)</span><span class="sxs-lookup"><span data-stu-id="77ded-116">**port** (*optional*)</span></span> | <span data-ttu-id="77ded-117">Les valeurs valides sont comprises entre 1 et 65535.</span><span class="sxs-lookup"><span data-stu-id="77ded-117">Valid values range from 1 to 65535.</span></span> |
| <span data-ttu-id="77ded-118">**chemin d’accès** (*facultatif*)</span><span class="sxs-lookup"><span data-stu-id="77ded-118">**path** (*optional*)</span></span> | <span data-ttu-id="77ded-119">Vous pouvez utiliser n’importe quelle chaîne dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="77ded-119">You can use any string in the path.</span></span> |
| <span data-ttu-id="77ded-120">**requête** (*facultatif*)</span><span class="sxs-lookup"><span data-stu-id="77ded-120">**query** (*optional*)</span></span> | <span data-ttu-id="77ded-121">La **requête** est constituée de jetons de paire clé-valeur ou de clé uniquement séparés par une esperluette («&»).</span><span class="sxs-lookup"><span data-stu-id="77ded-121">The **query** is either key-value or key-only tokens separated by an ampersand ("&").</span></span> <span data-ttu-id="77ded-122">Séparez les jetons de paire clé-valeur par un signe égal («=»).</span><span class="sxs-lookup"><span data-stu-id="77ded-122">Separate key-value tokens with an equal sign ("=").</span></span> <span data-ttu-id="77ded-123">Pour indiquer une correspondance de préfixe, vous pouvez utiliser un astérisque («\*») à la fin de la **requête**.</span><span class="sxs-lookup"><span data-stu-id="77ded-123">To indicate a prefix match, you can use an asterisk ("\*") at the end of the **query**.</span></span> |

## <span data-ttu-id="77ded-124">Comparaison du format de filtre au format URL</span><span class="sxs-lookup"><span data-stu-id="77ded-124">Comparing the filter format to the URL format</span></span>

<span data-ttu-id="77ded-125">Le format de filtre ressemble au format d’URL, à l’exception des différences suivantes:</span><span class="sxs-lookup"><span data-stu-id="77ded-125">The filter format resembles the URL format, except for the following differences:</span></span>

- <span data-ttu-id="77ded-126">Si vous incluez «user:pass», il est ignoré.</span><span class="sxs-lookup"><span data-stu-id="77ded-126">If you include "user:pass", it will be ignored.</span></span> <span data-ttu-id="77ded-127">Exemple : http://user:pass@ftp.contoso.com/pub/example.iso.</span><span class="sxs-lookup"><span data-stu-id="77ded-127">For example, http://user:pass@ftp.contoso.com/pub/example.iso.</span></span>
- <span data-ttu-id="77ded-128">Si vous ajoutez un identifiant de fragment («#»), tout ce qui suit l’identifiant est ignoré.</span><span class="sxs-lookup"><span data-stu-id="77ded-128">If you include a fragment identifier ("#"), it and everything that follows the identifier is ignored.</span></span>
- <span data-ttu-id="77ded-129">Vous pouvez utiliser un caractère générique («\*») comme **hôte** et le faire précéder d’un point («.»).</span><span class="sxs-lookup"><span data-stu-id="77ded-129">You can use a wildcard ("\*") as the **host** and you can prefix it with a dot (".").</span></span>
- <span data-ttu-id="77ded-130">Vous pouvez utiliser une barre oblique («/») ou un point («.») comme suffixe pour l’**hôte**.</span><span class="sxs-lookup"><span data-stu-id="77ded-130">You can use a forward slash ("/") or a dot (".") as a suffix for the **host**.</span></span> <span data-ttu-id="77ded-131">Dans ce cas, le suffixe est ignoré.</span><span class="sxs-lookup"><span data-stu-id="77ded-131">In this case, the suffix is ignored.</span></span>

## <span data-ttu-id="77ded-132">Critères de sélection du filtre</span><span class="sxs-lookup"><span data-stu-id="77ded-132">Filter selection criteria</span></span>

<span data-ttu-id="77ded-133">Le filtre sélectionné pour une URL est la correspondance la plus précise trouvée après le traitement des règles de sélection de filtre suivantes:</span><span class="sxs-lookup"><span data-stu-id="77ded-133">The filter selected for a URL is the most specific match found after processing the following filter selection rules:</span></span>

1. <span data-ttu-id="77ded-134">Les filtres avec l’**hôte** correspondant le plus long sont sélectionnés en premier.</span><span class="sxs-lookup"><span data-stu-id="77ded-134">Filters with the longest **host** match are selected first.</span></span>
2. <span data-ttu-id="77ded-135">À partir des filtres sélectionnés, tout filtre doté d’un schéma ou d’un port ne correspondant pas est ignoré.</span><span class="sxs-lookup"><span data-stu-id="77ded-135">From the selected filters, any filter with a non-matching scheme or port is discarded.</span></span>
3. <span data-ttu-id="77ded-136">Dans les filtres restants, le filtre avec le **chemin** correspondant le plus long est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="77ded-136">From the remaining filters, the filter with the longest matching **path** is selected.</span></span>
4. <span data-ttu-id="77ded-137">Dans les filtres restants, le filtre avec le jeu de jetons de requête le plus long est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="77ded-137">From the remaining filters, the filter with the longest set of query tokens is selected.</span></span> <span data-ttu-id="77ded-138">À cette étape, le filtre de liste verte est prioritaire sur le filtre de liste rouge si les deux filtres ont la même longueur de **chemin d’accès** et le même nombre de jetons de **requête**.</span><span class="sxs-lookup"><span data-stu-id="77ded-138">At this step, the allow list filter takes precedence over the block list filter if both filters have the same **path** length and number of **query** tokens.</span></span>
5. <span data-ttu-id="77ded-139">S’il ne reste aucun filtre valide, le sous-domaine le plus à gauche est supprimé de l’**hôte** et le processus de sélection reprend à l’étape1.</span><span class="sxs-lookup"><span data-stu-id="77ded-139">If there's no valid filter remaining, then the left-most subdomain is removed from **host** and the selection process starts over at step 1.</span></span> <span data-ttu-id="77ded-140">L’ordinateur **hôte** assorti d’un astérisque spécial («\*» ) est le dernier recherché, et correspond à tous les ordinateurs hôtes.</span><span class="sxs-lookup"><span data-stu-id="77ded-140">The special asterisk ("\*") **host** is the last searched and it matches all hosts.</span></span>
6. <span data-ttu-id="77ded-141">Si un filtre est disponible, il bloque ou autorise la demande d’URL.</span><span class="sxs-lookup"><span data-stu-id="77ded-141">If a filter's available, it blocks or allows the URL request.</span></span>

   >[!NOTE]
   ><span data-ttu-id="77ded-142">Le comportement par défaut consiste à autoriser la demande d’URL si aucun filtre n’a de correspondance.</span><span class="sxs-lookup"><span data-stu-id="77ded-142">The default behavior is to allow the URL request if no filter is matched.</span></span>

## <span data-ttu-id="77ded-143">Exemple de critère de sélection du filtre</span><span class="sxs-lookup"><span data-stu-id="77ded-143">Example filter selection criteria</span></span>

<span data-ttu-id="77ded-144">Dans cet exemple, lors de la recherche d’une correspondance à «https://sub.contoso.com/docs», la sélection de filtre effectue les actions suivantes:</span><span class="sxs-lookup"><span data-stu-id="77ded-144">In this example, when searching for a match to "https://sub.contoso.com/docs" the filter selection will:</span></span>

1. <span data-ttu-id="77ded-145">Rechercher un filtre pour «sub.contoso.com».</span><span class="sxs-lookup"><span data-stu-id="77ded-145">Search for a filter for "sub.contoso.com".</span></span> <span data-ttu-id="77ded-146">Si elle trouve un filtre, la recherche passe à l’étape2.</span><span class="sxs-lookup"><span data-stu-id="77ded-146">If it finds a filter, the search moves to step 2.</span></span> <span data-ttu-id="77ded-147">Si aucun filtre n’est trouvé, elle effectue une nouvelle tentative avec «contoso.com», «com» et enfin «».</span><span class="sxs-lookup"><span data-stu-id="77ded-147">If a filter isn't found, then it tries again with "contoso.com", "com", and finally "".</span></span>
2. <span data-ttu-id="77ded-148">Parmi les filtres sélectionnés, tout filtre dont le **schéma** ne contient pas «http» est supprimé.</span><span class="sxs-lookup"><span data-stu-id="77ded-148">From the selected filters, any that don't have "http" in the **scheme** are removed.</span></span>
3. <span data-ttu-id="77ded-149">Dans les filtres restants, tous ceux dont le numéro de port exact n’est pas «80» sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="77ded-149">From the remaining filters, any that have an exact port number that isn't "80" are removed.</span></span>
4. <span data-ttu-id="77ded-150">Dans les filtres restants, tous les éléments qui n’ont pas «/docs" comme préfixe du **chemin d’accès** sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="77ded-150">From the remaining filters, any that don't have "/docs" as a prefix of the **path** are removed.</span></span>
5. <span data-ttu-id="77ded-151">Dans les filtres restants, le filtre avec le préfixe de chemin correspondant le plus long est sélectionné et appliqué.</span><span class="sxs-lookup"><span data-stu-id="77ded-151">From the remaining filters, the filter with the longest path prefix is selected and applied.</span></span> <span data-ttu-id="77ded-152">Si aucun filtre n’est trouvé, le processus de sélection reprend à l’étape1.</span><span class="sxs-lookup"><span data-stu-id="77ded-152">If a filter isn't found, the selection process starts over again at step 1.</span></span> <span data-ttu-id="77ded-153">Le processus est répété avec le sous-domaine suivant.</span><span class="sxs-lookup"><span data-stu-id="77ded-153">The process is repeated with the next subdomain.</span></span>

### <span data-ttu-id="77ded-154">Informations de filtre complémentaires</span><span class="sxs-lookup"><span data-stu-id="77ded-154">Additional filter information</span></span>

<span data-ttu-id="77ded-155">Si un filtre a un point («.») comme préfixe de l’**hôte**, seules les correspondances exactes d’**hôte** sont filtrées.</span><span class="sxs-lookup"><span data-stu-id="77ded-155">If a filter has a dot (".") prefixing the **host** then only exact **host** matches are filtered.</span></span> <span data-ttu-id="77ded-156">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="77ded-156">For example:</span></span>

- <span data-ttu-id="77ded-157">«contoso.com» (aucun point) correspond à «contoso.com», «www.contoso.com» et «sub.www.contoso.com».</span><span class="sxs-lookup"><span data-stu-id="77ded-157">"contoso.com" (no dot) will match "contoso.com", "www.contoso.com", and "sub.www.contoso.com"</span></span>
- <span data-ttu-id="77ded-158">«.www.contoso.com» (avec un préfixe point) ne correspond qu’à «www.contoso.com».</span><span class="sxs-lookup"><span data-stu-id="77ded-158">".www.contoso.com" (with a dot prefix) will only match "www.contoso.com"</span></span>

<span data-ttu-id="77ded-159">Vous pouvez utiliser un **schéma** standard ou client.</span><span class="sxs-lookup"><span data-stu-id="77ded-159">You can use either a standard or customer **schema**.</span></span> <span data-ttu-id="77ded-160">Les schémas standard pris en charge sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="77ded-160">Supported standard schemas include:</span></span>

- <span data-ttu-id="77ded-161">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_ et _wss_.</span><span class="sxs-lookup"><span data-stu-id="77ded-161">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_, and _wss_.</span></span>

<span data-ttu-id="77ded-162">Tout autre **schéma** est traité comme un **schéma**personnalisé, mais seuls les modèles _schema:\*_ et _schema://\*_ \* sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="77ded-162">Any other **schema** is treated as a custom **schema**, but only the _schema:\*_ and _schema://\*_ patterns are allowed.</span></span> <span data-ttu-id="77ded-163">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="77ded-163">For example:</span></span>

- <span data-ttu-id="77ded-164">«custom:*» ou «custom://*» correspondent à «custom:app».</span><span class="sxs-lookup"><span data-stu-id="77ded-164">"custom:*" or "custom://*" will match "custom:app"</span></span>
- <span data-ttu-id="77ded-165">«custom:app» ou «custom://app» ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="77ded-165">"custom:app" or "custom://app" are invalid</span></span>

<span data-ttu-id="77ded-166">Le **schéma** et l’**hôte** ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="77ded-166">**schema** and **host** aren't case-sensitive.</span></span> <span data-ttu-id="77ded-167">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="77ded-167">For example:</span></span>

- <span data-ttu-id="77ded-168">Le filtre «http://contoso.com» correspond à «HTTP://contoso.com», «http://contoso.COM» et «http://contoso.com».</span><span class="sxs-lookup"><span data-stu-id="77ded-168">"http://contoso.com" filter matches "HTTP://contoso.com", "http://contoso.COM", and "http://contoso.com"</span></span>

<span data-ttu-id="77ded-169">Le **chemin** et la **requête** respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="77ded-169">**path** and **query** are case-sensitive.</span></span> <span data-ttu-id="77ded-170">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="77ded-170">For example:</span></span>

- <span data-ttu-id="77ded-171">Le filtre «http://contoso.com/path?query=A» ne correspond pas à «http://contoso.com/Path?query=A» ou «http://contoso.com/path?Query=A».</span><span class="sxs-lookup"><span data-stu-id="77ded-171">"http://contoso.com/path?query=A" filter doesn't match "http://contoso.com/Path?query=A" or "http://contoso.com/path?Query=A".</span></span> <span data-ttu-id="77ded-172">Mais il correspond à «http://contoso.COM/path?query=A».</span><span class="sxs-lookup"><span data-stu-id="77ded-172">It does match "http://contoso.COM/path?query=A".</span></span>

## <span data-ttu-id="77ded-173">Licence de contenu</span><span class="sxs-lookup"><span data-stu-id="77ded-173">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="77ded-174">Certaines parties de cette page sont des modifications basées sur le travail créé et partagé par Chromium.org et utilisé conformément aux conditions décrites dans la [Licence internationale Creative Commons Attribution4.0](http://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="77ded-174">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="77ded-175">La [page Chromium d’origine est disponible ici](https://www.chromium.org/administrators/url-blacklist-filter-format).</span><span class="sxs-lookup"><span data-stu-id="77ded-175">The original [Chromium page can be found here](https://www.chromium.org/administrators/url-blacklist-filter-format).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="77ded-176">Ce travail est concédé sous une <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licence internationale Creative Commons Attribution4.0</a>.</span><span class="sxs-lookup"><span data-stu-id="77ded-176">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <span data-ttu-id="77ded-177">Voir également</span><span class="sxs-lookup"><span data-stu-id="77ded-177">See also</span></span>

- [<span data-ttu-id="77ded-178">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="77ded-178">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
