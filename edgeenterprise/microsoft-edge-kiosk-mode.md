---
title: Microsoft Edge en mode plein écran
ms.author: brianalt
author: brianalt
manager: seanlynd
ms.date: 01/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge en mode plein écran
ms.openlocfilehash: 7a690820752b5361349bf394055a737bd8175215
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979830"
---
# Microsoft Edge en mode plein écran

Cet article fournit une vue d’ensemble des options du mode plein écran MicrosoftEdge (version77 ou ultérieure). Elle présente également les conditions requises pour continuer à utiliser la version héritée du mode plein écran de MicrosoftEdge (version45 et antérieure).

Pour plus d’informations sur la version héritée du mode plein écran de MicrosoftEdge (version45 et antérieure , consultez [Déployer Microsoft Edge en mode plein écran](https://aka.ms/edgekioskmode).

## MicrosoftEdge avec accès affecté

MicrosoftEdge peut être exécuté avec un [accès affecté à plusieurs applications](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) sur Windows10, ce qui équivaut à la version héritée du type de mode plein écran de MicrosoftEdge «Navigation normale. Pour configurer MicrosoftEdge avec accès affecté à plusieurs applications, suivez les instructions sur la façon de [Configurer une borne à plusieurs applications](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). l’ID de modèle utilisateur de l’application pour le canal stable de MicrosoftEdge est **MSEdge**.

Lorsque vous utilisez MicrosoftEdge avec accès affecté à plusieurs applications, vous pouvez utiliser les [stratégies de navigateur MicrosoftEdge](microsoft-edge-policies.md) pour configurer l’expérience de navigation en fonction de vos besoins spécifiques.

Actuellement, MicrosoftEdge ne prend pas en charge les mêmes types de mode plein écran hérités de MicrosoftEdge pour l’accès affecté à une application unique et le type de mode plein écran «Navigation publique» dans un accès affecté à plusieurs applications. Si vous avez besoin d’un navigateur pour votre appareil en mode plein écran avec accès affecté à une application unique, nous vous conseillons d’utiliser la [version héritée du mode plein écran de MicrosoftEdge](https://aka.ms/edgekioskmode) ou l’[application navigateur en mode plein écran Microsoft](https://www.microsoft.com/p/kiosk-browser/9ngb5s5xg2kp?activetab=pivot:overviewtab). 

## Paramètre de ligne de commande «--kiosk» de MicrosoftEdge

Vous pouvez lancer MicrosoftEdge en mode plein écran à l’aide du paramètre de ligne de commande «`--kiosk`». Le navigateur s’ouvre en mode plein écran avec le raccourci clavier plein écran désactivé (F11). Pour ce faire, créez un raccourci avec la cible définie sur:<br>
*`"<local path>\msedge.exe" --kiosk http://bing.com`*

> [!NOTE]
> Le paramètre «`--kiosk`» n’empêche pas l’utilisateur d’accéder aux raccourcis clavier Windows et n’empêche pas les autres applications de s’exécuter. Pour effectuer ce type de contrôle, utilisez [AppLocker pour créer un mode plein écran Windows10](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-applocker) et un [filtre clavier](https://docs.microsoft.com/windows-hardware/customize/enterprise/keyboardfilter).

Pour quitter le mode plein écran et fermer le navigateur, utilisez Alt+F4.

## Prise en charge de la version héritée du mode plein écran MicrosoftEdge

Lorsque la nouvelle version de MicrosoftEdge canal stable est installée, la version héritée de MicrosoftEdge est masquée et toutes les tentatives de lancement de la version héritée de MicrosoftEdge sont redirigées vers la nouvelle version. Pour plus d’informations sur:

- la configuration requise pour la mise à jour de Windows, consultez [Mises à jour Windows pour prendre en charge la prochaine version de MicrosoftEdge](microsoft-edge-sysupdate-windows-updates.md) 
- l’accès à la version héritée de MicrosoftEdge après l’installation de MicrosoftEdge, consultez [Accéder à la version héritée de MicrosoftEdge après avoir installé la nouvelle version de MicrosoftEdge](microsoft-edge-sysupdate-access-old-edge.md)
 
Pour continuer à utiliser la version héritée du mode plein écran de MicrosoftEdge, effectuez l’une des opérations suivantes: 

- Si vous envisagez d’installer MicrosoftEdge canal stable, que vous voulez autoriser son installation, ou s’il est déjà installé sur votre appareil en mode plein écran, déployez la stratégie MicrosoftEdge [Autoriser l’expérience de navigateur côte à côte MicrosoftEdge](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs).
- Pour empêcher l’installation du canal stable de MicrosoftEdge sur vos appareils en mode plein écran, déployez la stratégie MicrosoftEdge [Autoriser l’installation par défaut](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allow-installation-default) pour le canal stable ou envisagez d’utiliser [Blocker Toolkit pour désactiver la distribution automatique de MicrosoftEdge](microsoft-edge-blocker-toolkit.md). 

## Articles associés

- [Configurer des bornes et enseignes numériques dans les éditions Windows de bureau](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Déployer la version héritée du mode plein écran de MicrosoftEdge](https://aka.ms/edgekioskmode) 
- [Planifier votre déploiement de MicrosoftEdge](deploy-edge-plan-deployment.md)
- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
