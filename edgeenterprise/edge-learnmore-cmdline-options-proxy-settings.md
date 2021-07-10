---
title: Paramètres de proxy Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 'Utiliser les options de ligne de commande pour configurer les paramètres de proxy '
ms.openlocfilehash: 99a5f0776ea42f1e26050e0d30adb48a63907b8c
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642160"
---
# <a name="how-to-use-microsoft-edge-command-line-options-to-configure-proxy-settings"></a>Procédure d’utilisation des options de ligne de commande Microsoft Edge pour configurer les paramètres de proxy

Cet article décrit comment vous pouvez utiliser les options de ligne de commande pour remplacer les paramètres réseau par défaut du système.

>[!NOTE]
>Cet article concerne Microsoft Edge version 77 ou ultérieure.

## <a name="system-network-settings"></a>Paramètres réseau du système

La pile réseau de Microsoft Edge utilise par défaut les paramètres réseau du système. Ces paramètres sont les *paramètres de proxy* et *magasins de certificats et de clés privées*.

Il existe des scénarios dans lesquels les utilisateurs demandent une alternative à l’utilisation des paramètres de proxy par défaut du système. En prévision de tels scénarios, Microsoft Edge prend en charge les options de ligne de commande que vous pouvez utiliser pour configurer des paramètres de proxy personnalisés.

Ces options de ligne de commande correspondent aux stratégies suivantes dans le groupe **Serveur proxy** :

- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist)
- [ProxyMode](./microsoft-edge-policies.md#proxymode)
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl)
- [ProxyServer](./microsoft-edge-policies.md#proxyserver)
- [ProxySettings](./microsoft-edge-policies.md#proxysettings)

## <a name="command-line-options-for-proxy-settings"></a>Options de ligne de commande pour les paramètres de proxy

Microsoft Edge prend en charge les options de ligne de commande liées au proxy suivantes.

 **`--no-proxy-server`**
 
Indique à Microsoft Edge de ne pas d’utiliser de proxy, même si le système est configuré pour en utiliser un. Tous les autres paramètres de proxy fournis sont ignorés.

**`--proxy-auto-detect`**

Indique à Microsoft Edge d’essayer de détecter automatiquement votre configuration de proxy. Cet argument est ignoré si `--proxy-server` est configuré.

**`--proxy-server=<scheme>=<uri>[:<port>][;...] | <uri>[:<port>] | "direct://"`**

Indique à Microsoft Edge d’utiliser une configuration de proxy personnalisée. Vous pouvez spécifier une configuration de proxy personnalisée de trois manières.

1. Fournissez un mappage séparé par des points-virgules du schéma de liste aux paires URL/port. Par exemple, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` indique à Microsoft Edge d’utiliser le proxy http « proxy1:8080 » pour les URL http et le proxy HTTP « ftpproxy:80 » pour les URL ftp.
2. En spécifiant un seul URI avec un port facultatif à utiliser pour toutes les URL. Par exemple, `--proxy-server="proxy2:8080"` utilise le proxy à « proxy2:8080 » pour tout le trafic.
3. En utilisant la valeur spéciale « direct:// ». Par exemple, `--proxy-server="direct://"` fait en sorte que toutes les connexions n’utilisent pas de proxy. 

>[!NOTE]
>Vous pouvez configurer Microsoft Edge pour qu’il tente d’utiliser un proxy et de revenir en directement si le proxy n’est pas disponible. Exemple : `--proxy-server="http://proxy2:8080,direct://`.

**`--proxy-bypass-list=(<trailing_domain>|<ip-address>)[:<port>][;...]`**

Indique à Microsoft Edge de contourner tout proxy spécifié pour la liste séparée par des points-virgules d’hôtes spécifiée. Cet indicateur doit être utilisé avec `--proxy-server`.

>[!NOTE]
>La correspondance de domaine final ne nécessite pas de séparateurs « . » ; « \*microsoft.com » correspondra à « imicrosoft.com ». Par exemple, `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` utilise le serveur proxy « Proxy2 » sur le port 8080 pour tous les hôtes, à l’exception des demandes de \*.microsoft.com, example.com et 127.0.0.1 sur le port 8080. Dans l’exemple précédent, les demandes imicrosoft.com sont toujours traitées par proxy. Toutefois, les demandes de iexample.com contournent le proxy car \*example.com a été spécifié au lieu de \*.example.com.

**`--proxy-pac-url=<pac-file-url>`**

Indique à Microsoft Edge d’utiliser le fichier PAC à l’URL spécifiée. Par exemple, `--proxy-pac-url="https://wpad/proxy.pac"` indique à Microsoft Edge de résoudre les informations de proxy pour les demandes d’URL utilisant le fichier **proxy. pac**.

## <a name="content-license"></a>Licence de contenu

> [!NOTE]
> Certaines parties de cette page sont des modifications basées sur le travail créé et partagé par Chromium.org et utilisé conformément aux conditions décrites dans la [Licence internationale Creative Commons Attribution 4.0](http://creativecommons.org/licenses/by/4.0/). La page d’origine est disponible [ici](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Ce travail est concédé sous une <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licence internationale Creative Commons Attribution 4.0</a>.

## <a name="see-also"></a>Voir également

- Pour connaître les paramètres de configuration avancés et les options supplémentaires, consultez la [documentation relative au proxy](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) dans le projet open source Chromium.
- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)