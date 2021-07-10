---
title: Microsoft Edge et sites configurables en mode Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge et sites configurables en mode Internet Explorer
ms.openlocfilehash: 0248ecd394acee5773751c0685969e3d40940431
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641800"
---
# <a name="learn-about-configurable-sites-in-ie-mode"></a>Découvrez les sites configurables en mode Internet Explorer

Cet article décrit la fonctionnalité de sites configurables de la liste des sites en mode Entreprise lorsque vous utilisez le mode Internet Explorer dans Microsoft Edge.

## <a name="prerequisites"></a>Conditions préalables

- Mises à jour Windows

  - Windows 10 version 1909, Windows Server version 1909 – KB4550945 ou ultérieure
  - Windows 10 version 1903, Windows Server version 1903 – KB4550945 ou ultérieure
  - Windows 10 version 1809, Windows Server version 1809 et Windows Server 2019 – KB4550969 ou ultérieure
  - Windows 10 version 1803 – KB4550944 ou ultérieure
  - Windows 10 version 1607, Windows Server 2016 – KB4556826 ou ultérieure
  - Version initiale de Windows 10, juillet 2015 – KB4550947 ou ultérieure
  - Windows 8.1 – KB4556798 ou version ultérieure

- Microsoft Edge version 83 ou ultérieure
- [Mode Internet Explorer](./edge-ie-mode.md) configuré avec la liste des sites en mode Entreprise

## <a name="overview"></a>Vue d'ensemble

La configuration des sites nécessitant le mode Internet Explorer dans la liste des sites en mode Entreprise fonctionne parfaitement pour la plupart des environnements avec des applications héritées. Toutefois, dans certains cas, il ne s’agit pas de la meilleure approche pour configurer un sous-ensemble de sites afin qu’il s’ouvre en mode Internet Explorer sans afficher l’intégralité d’un domaine en mode Internet Explorer. Par exemple, lorsque votre environnement contient des applications modernes et héritées qui s’exécutent sur un seul serveur, et que vous aimeriez afficher uniquement les applications héritées en mode Internet Explorer et les applications restantes en mode Microsoft Edge.

La solution consiste à utiliser la fonctionnalité de sites configurables de la liste des sites en mode Entreprise. Lorsque la fonctionnalité est activée, Microsoft Edge permet aux sites disposant de la balise « configurable » de participer à la détermination du moteur du mode Internet Explorer.

## <a name="how-configurable-sites-works"></a>Fonctionnement des sites configurables

### <a name="automatic-switching-from-the-microsoft-edge-engine-to-the-ie-mode-engine"></a>Basculement automatique du moteur Microsoft Edge vers le moteur du mode Internet Explorer

Pour utiliser la fonctionnalité de sites configurables et que l’option `<open-in>Configurable</open-in>` soit disponible, la liste des sites en mode Entreprise doit contenir au moins un site.

Exemple :

```
<site-list version="1">
  <site url="app.com">
    <open-in>Configurable</open-in>
  </site>
</site-list>
```

Lorsque la fonctionnalité de sites configurables est activée, le comportement suivant se produit :

1. Lorsque vous envoyez une demande à un site configurable, Microsoft Edge envoie l’en-tête de demande HTTP « `X-InternetExplorerModeConfigurable: 1` ».
2. Un site configurable peut envoyer une réponse de redirection (par exemple, HTTP 302) avec l’en-tête de réponse HTTP « `X-InternetExplorerMode: 1` » pour demander à Microsoft Edge de charger le site en mode Internet Explorer.
3. La cible de la redirection (autrement dit, la valeur de l’en-tête de réponse **Location**) doit également être un site **Configurable** ou **Neutre**, sans quoi l’en-tête de réponse du mode Internet Explorer ne sera pas pris en compte. De manière générale, il est attendu que la cible de la redirection soit identique à l’URL d’origine. Cela n’est toutefois pas une nécessité.

   > [!NOTE]
   > La réponse de redirection fait l’objet d’une mise en cache HTTP normale de Microsoft Edge pour les redirections.

### <a name="switching-back-from-ie-mode-engine-to-microsoft-edge-engine"></a>Rebasculement du moteur du mode Internet Explorer vers le moteur Microsoft Edge

L’activation de sites configurables dans Microsoft Edge active automatiquement les comportements suivants dans les onglets du mode Internet Explorer :

1. Lorsque vous envoyez une demande à un site configurable, les onglets du mode Internet Explorer envoient l’en-tête de demande HTTP « `X-InternetExplorerModeConfigurable: 1` », le même que celui des onglets Microsoft Edge.
2. Un site configurable peut envoyer une réponse de redirection (par exemple, HTTP 302) avec l’en-tête de réponse HTTP « `X-InternetExplorerMode: 0` » pour demander le basculement de la navigation en mode Microsoft Edge.
3. La cible de la redirection (autrement dit, la valeur de l’en-tête de réponse **Location**) doit également être un site **Configurable** ou **Neutre**, sans quoi l’en-tête de réponse du mode Internet Explorer ne sera pas pris en compte. De manière générale, il est attendu que la cible de la redirection soit identique à l’URL d’origine. Cela n’est toutefois pas une nécessité.

   > [!NOTE]
   > La réponse de redirection fait l’objet d’une mise en cache HTTP normale de Microsoft Edge pour les redirections.

> [!TIP]
> Les deux moteurs de navigateur envoient le même en-tête de demande « `X-InternetExplorerModeConfigurable: 1` » aux sites configurables. Vous devez utiliser l’en-tête de requête User-Agent pour faire la distinction entre les demandes en provenance du mode Microsoft Edge et celles du mode Internet Explorer, afin d’éviter la redirection lorsque le site est déjà chargé dans le bon moteur.

## <a name="see-also"></a>Voir également

- [À propos du mode Internet Explorer](./edge-ie-mode.md)
- [Informations supplémentaires sur le mode entreprise](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)