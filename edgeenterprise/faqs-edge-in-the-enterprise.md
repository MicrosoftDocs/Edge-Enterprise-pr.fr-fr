---
title: Forum aux questions sur Edge dans l’entreprise
ms.author: jwhit
author: jwhit-MSFT
manager: laurawi
ms.date: 11/04/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Forum aux questions sur le déploiement de MicrosoftEdge dans l’entreprise
ms.openlocfilehash: e689967cbad950e2969535bad0dd63d5d7081798
ms.sourcegitcommit: 12827458f6217f443128e826c1d18d36d401d03b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "11154319"
---
# Forum aux questions sur MicrosoftEdge dans l’entreprise

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

## Comment savoir de quelle version de MicrosoftEdge je dispose?

Dans l’angle supérieur droit de MicrosoftEdge, cliquez sur l’icône représentant des points de suspension(**…**), puis cliquez sur **Paramètres**. Sélectionnez **A propos de MicrosoftEdge** pour afficher votre version de MicrosoftEdge.

## Internet Explorer11 continuera-t-il à recevoir des mises à jour?

Nous nous engageons à ce qu’Internet Explorer reste un navigateur pris en charge, fiable et sécurisé. Internet Explorer reste un composant de Windows et suit le cycle de vie du support du système d’exploitation sur lequel il est installé. Pour plus d’informations, consultez [FAQ sur le cycle de vie: Internet Explorer](https://support.microsoft.com/help/17454/). Bien que nous continuions à prendre en charge et à mettre à jour Internet Explorer, les fonctionnalités et mises à jour de plateforme les plus récentes seront disponibles uniquement dans MicrosoftEdge.

## Puis-je exécuter la version actuelle de MicrosoftEdge (version héritée de MicrosoftEdge) côte à côte lorsque j’essaie la nouvelle version?

Oui, c’est possible. Après le 15janvier2020 la nouvelle version de MicrosoftEdge (basée sur Chromium) sera distribuée aux appareils d’édition familiale et professionnel exécutant Windows10 version1803 ou ultérieure. Les appareils joints à un domaine sont exclus de cette mise à jour. Pour plus d’informations, voir [Vue d’ensemble des mises à jour de MicrosoftEdge](https://docs.microsoft.com/deployedge/microsoft-edge-blocker-toolkit#overview). Vous pouvez disposer d’une installation côte à côte de la version héritée de MicrosoftEdge lorsque vous évaluez la version suivante de MicrosoftEdge. Pour plus d’informations, consultez [Comment accéder à l’ancienne version de MicrosoftEdge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge). En outre, chacun des nouveaux canaux de MicrosoftEdge prend également en charge les installations côte à côte. Pour plus d’informations, voir [Vue d’ensemble des canaux de MicrosoftEdge](https://docs.microsoft.com/deployedge/microsoft-edge-channels).

## MicrosoftEdge (basé sur Chrome) prend-il en charge les contrôles ActiveX ou les objets application d'assistance du navigateur comme Silverlight ou Java?

Non. MicrosoftEdge ne prend pas en charge les contrôles ActiveX et les BHOS comme Silverlight ou Java. Toutefois, si vous exécutez des applications web utilisant les contrôles ActiveX, BHOS ou des modes de document legacy sur Internet Explorer11, vous pouvez les configurer pour exécuter le mode IE sur le nouveau Microsoft Edge. Pour plus d’informations, voir [Configurer le mode IE sur Microsoft Edge](https://docs.microsoft.com/DeployEdge/edge-ie-mode).

## Les favoris seront-ils conservés à partir de la version actuelle de MicrosoftEdge ou devrai-je les ajouter à nouveau?

Actuellement, MicrosoftEdge prend en charge l’importation à partir d’installations existantes de MicrosoftEdge, Chrome, Internet Explorer et Firefox (sur Win10). Les paramètres suivants sont pris en charge pour l’importation: Signets, Historique, Mots de passe et remplissage automatique (Paiements, adresses et formulaires génériques). Vous pouvez choisir d’effectuer une importation à partir de la première utilisation ou à partir des paramètres du navigateur.  

## Quelle est la différence entre les canaux/builds stable, Beta, Dev et Canary?

La version stable suivante de MicrosoftEdge est le canal de version préliminaire le plus stable que nous proposons, avec des fonctionnalités axées sur l’entreprise,prêtes à être [testées et évaluées](https://aka.ms/EdgeEnterprise) au sein de votre organisation. Le canal bêta vous permet de valider la prochaine version stable avec un ensemble représentatif d’utilisateurs. Les canaux stable et bêta seront mis à jour environ toutes les six semaines. Les canaux Dev et Canary continueront à être mis à jour toutes les semaines et tous les jours, respectivement. Les programmes d’installation hors connexion (MSIs et fichiers PKG) ne sont disponibles que pour les canaux stables, bêta et de développement. Pour plus d’informations, voir [Vue d’ensemble des canaux de MicrosoftEdge](https://docs.microsoft.com/deployedge/microsoft-edge-channels).

## De quel type de prise en charge d’extension vais-je bénéficier avec la nouvelle version de MicrosoftEdge?

MicrosoftEdge prend en charge les extensions provenant des [Modules complémentaires Microsoft Edge Insider](https://go.microsoft.com/fwlink/?linkid=2081222) et du [Chrome Web Store](https://go.microsoft.com/fwlink/?linkid=2072338).

## Prenez-vous en charge la gestion des périphériques mobiles (GPM) et Microsoft Intune?

Oui. La configuration de MicrosoftEdge sur Windows10 avec MicrosoftIntune et la gestion des périphériques mobiles (GPM) est désormais prise en charge. Pour plus d’informations, consultez [Configurer MicrosoftEdge à l’aide de MicrosoftIntune](configure-edge-with-intune.md) et [Configurer Microsoft Edge à l’aide de Gestion des périphériques mobiles](configure-edge-with-mdm.md).

## Est-ce que WSUS prend en charge le déploiement initial du nouveau Microsoft Edge?

Oui. Le [catalogue Microsoft Update est inclus dans les packages](https://www.catalog.update.microsoft.com/Search.aspx?q=the%20new%20microsoft%20edge%20for%20windows) qui peuvent être utilisés pour le déploiement initial du nouveau MicrosoftEdge via WSUS. Après le déploiement initial, les mises à jour automatiques sont configurées par défaut. Pour plus d’informations, voir [mise à jour dans WSUS pour le nouveau Microsoft Edge pour Windows10, version1809, 1903, 1909 et 2004: 29octobre2020](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge).

Les mises à jour manuelles peuvent être effectuées à l’aide d’un outil de gestion de la configuration, tel que [ConfigMgr](https://docs.microsoft.com/configmgr/apps/deploy-use/deploy-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json).

## Voir également

- [Page d’accueil de la documentation MicrosoftEdge](https://docs.microsoft.com/DeployEdge/)
- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
