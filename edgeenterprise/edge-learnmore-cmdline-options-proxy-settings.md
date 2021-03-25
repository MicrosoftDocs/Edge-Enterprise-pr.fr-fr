---
title: Paramètres de proxy Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Utiliser les options de ligne de commande pour configurer les paramètres de proxy '
ms.openlocfilehash: d0924f723aab6832e5b4eb70c60e1d329d3c7a9d
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447638"
---
# <a name="how-to-use-microsoft-edge-command-line-options-to-configure-proxy-settings"></a><span data-ttu-id="cc47a-103">Procédure d’utilisation des options de ligne de commande MicrosoftEdge pour configurer les paramètres de proxy</span><span class="sxs-lookup"><span data-stu-id="cc47a-103">How to use Microsoft Edge command-line options to configure proxy settings</span></span>

<span data-ttu-id="cc47a-104">Cet article décrit comment vous pouvez utiliser les options de ligne de commande pour remplacer les paramètres réseau par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="cc47a-104">This article describes how you can use command-line options to override the default system network settings.</span></span>

>[!NOTE]
><span data-ttu-id="cc47a-105">Cet article concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cc47a-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="system-network-settings"></a><span data-ttu-id="cc47a-106">Paramètres réseau du système</span><span class="sxs-lookup"><span data-stu-id="cc47a-106">System network settings</span></span>

<span data-ttu-id="cc47a-107">La pile réseau de MicrosoftEdge utilise par défaut les paramètres réseau du système.</span><span class="sxs-lookup"><span data-stu-id="cc47a-107">The Microsoft Edge network stack uses the system network settings by default.</span></span> <span data-ttu-id="cc47a-108">Ces paramètres sont les *paramètres de proxy* et *magasins de certificats et de clés privées*.</span><span class="sxs-lookup"><span data-stu-id="cc47a-108">These settings include *proxy settings*, and *certificate and private key stores*.</span></span>

<span data-ttu-id="cc47a-109">Il existe des scénarios dans lesquels les utilisateurs demandent une alternative à l’utilisation des paramètres de proxy par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="cc47a-109">There are scenarios where users request an alternative to using the system's default proxy settings.</span></span> <span data-ttu-id="cc47a-110">En prévision de tels scénarios, MicrosoftEdge prend en charge les options de ligne de commande que vous pouvez utiliser pour configurer des paramètres de proxy personnalisés.</span><span class="sxs-lookup"><span data-stu-id="cc47a-110">To support these scenarios, Microsoft Edge supports command-line options that you can use to configure custom proxy settings.</span></span>

<span data-ttu-id="cc47a-111">Ces options de ligne de commande correspondent aux stratégies suivantes dans le groupe **Serveur proxy**:</span><span class="sxs-lookup"><span data-stu-id="cc47a-111">These command-line options correspond to the following policies in the **Proxy server** group:</span></span>

- [<span data-ttu-id="cc47a-112">ProxyBypassList</span><span class="sxs-lookup"><span data-stu-id="cc47a-112">ProxyBypassList</span></span>](./microsoft-edge-policies.md#proxybypasslist)
- [<span data-ttu-id="cc47a-113">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="cc47a-113">ProxyMode</span></span>](./microsoft-edge-policies.md#proxymode)
- [<span data-ttu-id="cc47a-114">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="cc47a-114">ProxyPacUrl</span></span>](./microsoft-edge-policies.md#proxypacurl)
- [<span data-ttu-id="cc47a-115">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="cc47a-115">ProxyServer</span></span>](./microsoft-edge-policies.md#proxyserver)
- [<span data-ttu-id="cc47a-116">ProxySettings</span><span class="sxs-lookup"><span data-stu-id="cc47a-116">ProxySettings</span></span>](./microsoft-edge-policies.md#proxysettings)

## <a name="command-line-options-for-proxy-settings"></a><span data-ttu-id="cc47a-117">Options de ligne de commande pour les paramètres de proxy</span><span class="sxs-lookup"><span data-stu-id="cc47a-117">Command-line options for proxy settings</span></span>

<span data-ttu-id="cc47a-118">MicrosoftEdge prend en charge les options de ligne de commande liées au proxy suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc47a-118">Microsoft Edge supports the following proxy-related command-line options.</span></span>

 **`--no-proxy-server`**
 
<span data-ttu-id="cc47a-119">Indique à MicrosoftEdge de ne pas d’utiliser de proxy, même si le système est configuré pour en utiliser un.</span><span class="sxs-lookup"><span data-stu-id="cc47a-119">Tells Microsoft Edge not to use a Proxy, even if the system is otherwise configured to use one.</span></span> <span data-ttu-id="cc47a-120">Tous les autres paramètres de proxy fournis sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="cc47a-120">It overrides any other proxy settings that are provided.</span></span>

**`--proxy-auto-detect`**

<span data-ttu-id="cc47a-121">Indique à Microsoft Edge d’essayer de détecter automatiquement votre configuration de proxy.</span><span class="sxs-lookup"><span data-stu-id="cc47a-121">Tells Microsoft Edge to try and automatically detect your proxy configuration.</span></span> <span data-ttu-id="cc47a-122">Cet argument est ignoré si `--proxy-server` est configuré.</span><span class="sxs-lookup"><span data-stu-id="cc47a-122">This argument is ignored if `--proxy-server` is configured.</span></span>

**`--proxy-server=<scheme>=<uri>[:<port>][;...] | <uri>[:<port>] | "direct://"`**

<span data-ttu-id="cc47a-123">Indique à MicrosoftEdge d’utiliser une configuration de proxy personnalisée.</span><span class="sxs-lookup"><span data-stu-id="cc47a-123">Tells Microsoft Edge to use a custom proxy configuration.</span></span> <span data-ttu-id="cc47a-124">Vous pouvez spécifier une configuration de proxy personnalisée de trois manières.</span><span class="sxs-lookup"><span data-stu-id="cc47a-124">You can specify a custom proxy configuration in three ways.</span></span>

1. <span data-ttu-id="cc47a-125">Fournissez un mappage séparé par des points-virgules du schéma de liste aux paires URL/port.</span><span class="sxs-lookup"><span data-stu-id="cc47a-125">Provide a semicolon-separated mapping of list scheme to url/port pairs.</span></span> <span data-ttu-id="cc47a-126">Par exemple, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` indique à MicrosoftEdge d’utiliser le proxy http «proxy1:8080» pour les URL http et le proxy HTTP «ftpproxy:80» pour les URL ftp.</span><span class="sxs-lookup"><span data-stu-id="cc47a-126">For example, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` tells Microsoft Edge to use HTTP proxy "proxy1:8080" for http URLs and HTTP proxy "ftpproxy:80" for ftp URLs.</span></span>
2. <span data-ttu-id="cc47a-127">En spécifiant un seul URI avec un port facultatif à utiliser pour toutes les URL.</span><span class="sxs-lookup"><span data-stu-id="cc47a-127">By providing a single uri with optional port to use for all URLs.</span></span> <span data-ttu-id="cc47a-128">Par exemple, `--proxy-server="proxy2:8080"` utilise le proxy à «proxy2:8080» pour tout le trafic.</span><span class="sxs-lookup"><span data-stu-id="cc47a-128">For example, `--proxy-server="proxy2:8080"` will use the proxy at "proxy2:8080" for all traffic.</span></span>
3. <span data-ttu-id="cc47a-129">En utilisant la valeur spéciale «direct://».</span><span class="sxs-lookup"><span data-stu-id="cc47a-129">By using the special "direct://" value.</span></span> <span data-ttu-id="cc47a-130">Par exemple, `--proxy-server="direct://"` fait en sorte que toutes les connexions n’utilisent pas de proxy.</span><span class="sxs-lookup"><span data-stu-id="cc47a-130">For example, `--proxy-server="direct://"` will make all connections not use a proxy.</span></span> 

>[!NOTE]
><span data-ttu-id="cc47a-131">Vous pouvez configurer MicrosoftEdge pour qu’il tente d’utiliser un proxy et de revenir en directement si le proxy n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="cc47a-131">You can configure Microsoft Edge to try using a proxy and fallback to going direct if the proxy isn't available.</span></span> <span data-ttu-id="cc47a-132">Exemple : `--proxy-server="http://proxy2:8080,direct://`.</span><span class="sxs-lookup"><span data-stu-id="cc47a-132">For example, `--proxy-server="http://proxy2:8080,direct://`.</span></span>

**`--proxy-bypass-list=(<trailing_domain>|<ip-address>)[:<port>][;...]`**

<span data-ttu-id="cc47a-133">Indique à MicrosoftEdge de contourner tout proxy spécifié pour la liste séparée par des points-virgules d’hôtes spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cc47a-133">Tells Microsoft Edge to bypass any specified proxy for the specified semicolon-separated list of hosts.</span></span> <span data-ttu-id="cc47a-134">Cet indicateur doit être utilisé avec `--proxy-server`.</span><span class="sxs-lookup"><span data-stu-id="cc47a-134">This flag must be used with `--proxy-server`.</span></span>

>[!NOTE]
><span data-ttu-id="cc47a-135">La correspondance de domaine final ne nécessite pas de séparateurs «.»; «\*microsoft.com» correspondra à «imicrosoft.com».</span><span class="sxs-lookup"><span data-stu-id="cc47a-135">Trailing-domain matching doesn't require "." separators, "\*microsoft.com" will match "imicrosoft.com".</span></span> <span data-ttu-id="cc47a-136">Par exemple, `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` utilise le serveur proxy «Proxy2» sur le port 8080 pour tous les hôtes, à l’exception des demandes de \*.microsoft.com, example.com et 127.0.0.1 sur le port8080.</span><span class="sxs-lookup"><span data-stu-id="cc47a-136">For example, `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` will use the proxy server "proxy2" on port 8080 for all hosts except requests for \*.microsoft.com, example.com, and 127.0.0.1 on port 8080.</span></span> <span data-ttu-id="cc47a-137">Dans l’exemple précédent, les demandes imicrosoft.com sont toujours traitées par proxy.</span><span class="sxs-lookup"><span data-stu-id="cc47a-137">In the previous example, imicrosoft.com requests will still be proxied.</span></span> <span data-ttu-id="cc47a-138">Toutefois, les demandes de iexample.com contournent le proxy car \*example.com a été spécifié au lieu de \*.example.com.</span><span class="sxs-lookup"><span data-stu-id="cc47a-138">However, iexample.com requests will bypass the proxy because \*example.com was specified instead of \*.example.com.</span></span>

**`--proxy-pac-url=<pac-file-url>`**

<span data-ttu-id="cc47a-139">Indique à MicrosoftEdge d’utiliser le fichier PAC à l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cc47a-139">Tells Microsoft Edge to use the PAC file at the specified URL.</span></span> <span data-ttu-id="cc47a-140">Par exemple, `--proxy-pac-url="https://wpad/proxy.pac"` indique à MicrosoftEdge de résoudre les informations de proxy pour les demandes d’URL utilisant le fichier **proxy. pac**.</span><span class="sxs-lookup"><span data-stu-id="cc47a-140">For example, `--proxy-pac-url="https://wpad/proxy.pac"` tells Microsoft Edge to resolve proxy information for URL requests using the **proxy.pac** file.</span></span>

## <a name="content-license"></a><span data-ttu-id="cc47a-141">Licence de contenu</span><span class="sxs-lookup"><span data-stu-id="cc47a-141">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="cc47a-142">Certaines parties de cette page sont des modifications basées sur le travail créé et partagé par Chromium.org et utilisé conformément aux conditions décrites dans la [Licence internationale Creative Commons Attribution4.0](http://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="cc47a-142">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="cc47a-143">La page d’origine est disponible [ici](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).</span><span class="sxs-lookup"><span data-stu-id="cc47a-143">The original page can be found [here](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="cc47a-144">Ce travail est concédé sous une <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licence internationale Creative Commons Attribution4.0</a>.</span><span class="sxs-lookup"><span data-stu-id="cc47a-144">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc47a-145">Voir également</span><span class="sxs-lookup"><span data-stu-id="cc47a-145">See also</span></span>

- <span data-ttu-id="cc47a-146">Pour connaître les paramètres de configuration avancés et les options supplémentaires, consultez la [documentation relative au proxy](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) dans le projet open source Chromium.</span><span class="sxs-lookup"><span data-stu-id="cc47a-146">To see advanced configuration settings and additional options, consult the [proxy documentation](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) in the Chromium Open Source project.</span></span>
- [<span data-ttu-id="cc47a-147">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="cc47a-147">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)