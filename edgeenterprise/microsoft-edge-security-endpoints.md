---
title: Liste verte pour les points de terminaison de MicrosoftEdge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Liste verte pour les points de terminaison de MicrosoftEdge
ms.openlocfilehash: 76186524a708861432199d5da7eec7573ebecb96
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979853"
---
# Liste verte pour les points de terminaison de MicrosoftEdge

MicrosoftEdge nécessite une connectivité à Internet pour prendre en charge ses fonctionnalités. Cet article identifie les URL de domaine que vous devez ajouter à la liste verte pour garantir les communications via des pare-feu et d’autres mécanismes de sécurité.

> [!NOTE]
> Ceci concerne MicrosoftEdge version77 ou ultérieure.

## URL de domaine à autoriser

Autorisez les URL de domaine suivantes pour MicrosoftEdge.

### Service de mise à jour

Service que MicrosoftEdge utilise pour rechercher les nouvelles mises à jour.

- `https://msedge.api.cdp.microsoft.com`

### Service d’expérimentation et de configuration

- `https://config.ecs.skype.com`

### Télécharger les emplacements pour MicrosoftEdge

Les emplacements MicrosoftEdge peuvent être téléchargés à partir d’une installation initiale ou lorsqu’une mise à jour est disponible. L’emplacement de téléchargement est déterminé par le service de mise à jour.

#### HTTP

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Pour simplifier la liste verte des emplacements de téléchargement, vous pouvez utiliser un caractère générique: `*.dl.delivery.mp.microsoft.com`

### Télécharger les emplacements pour les extensions MicrosoftEdge

Les emplacements des extensions MicrosoftEdge peuvent être téléchargés à partir d’une installation initiale ou lorsqu’une mise à jour est disponible. L’emplacement de téléchargement est déterminé par le service de mise à jour.

#### HTTP

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Pour simplifier la liste verte des emplacements de téléchargement, vous pouvez utiliser un caractère générique: `*.dl.delivery.mp.microsoft.com`

### Éventuellement pour l’optimisation de la distribution des téléchargements

Pour plus d’informations sur l’optimisation de la distribution, consultez [Optimisation de la distribution pour les mises à jour de Windows10](https://aka.ms/waas-do).

- Communication client à service: `*.do.dsp.mp.microsoft.com` (HTTP Port80, HTTPS Port443)
- Communication client à client: le port TCP7680 doit être ouvert pour le trafic entrant

### Sync

Ces points de terminaison gèrent la lecture et l’écriture de données synchronisées, la gestion des droits pour sécuriser les données et l’envoi d’une notification au navigateur lorsque de nouvelles données de synchronisation sont disponibles.

- Points de terminaison du service de synchronisation Edge:

  - `https://enterprise.edge.activity.windows.com`
  - `https://edge.activity.windows.com`

- Points de terminaison Azure Information Protection:

  - `https://api.aadrm.com` (pour la plupart des locataires)
  - `https://api.aadrm.de` (pour les locataires résidant en Allemagne)
  - `https://api.aadrm.cn` (pour les locataires résidant en Chine)

- [Points de terminaison des services de notifications Windows.](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## Autres services de prise en charge de navigateur

Fournir des métadonnées pour les fonctionnalités de navigateur telles que la protection contre le suivi, les listes de révocation de certificats et d’autres mises à jour de composants de navigateur. Fournir des dictionnaires de vérification orthographique téléchargeables et des listes rouges de blocage de publicités. Fournir des services pour prendre en charge des fonctionnalités de navigateur telles que les collections, le remplissage automatique et le magasin d’extensions.

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## Articles associés

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Page d’accueil de la documentation MicrosoftEdge](https://docs.microsoft.com/DeployEdge/)
- [Gérer les points de terminaison de connexion pour Windows10 Entreprise, version1903](https://docs.microsoft.com/windows/privacy/manage-windows-1903-endpoints)
