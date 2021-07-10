---
title: Déploiements progressifs pour les mises à jour du canal stable Microsoft Edge
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Déploiements progressifs pour les mises à jour du canal stable Microsoft Edge
ms.openlocfilehash: bdcefdc118125d67057fa77513bd732cff6882e3
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642290"
---
# <a name="progressive-rollouts-for-microsoft-edge-stable-channel-updates"></a>Déploiements progressifs pour les mises à jour du canal stable Microsoft Edge

À compter de la version 83 de Microsoft Edge, nous allons effectuer un déploiement progressif des mises à jour majeures du canal stable Microsoft Edge sur une période de quelques jours. Ce déploiement progressif nous permet de contrôler les mises à niveau et de mettre à jour le navigateur en toute sécurité au sein de l’organisation.

> [!NOTE]
> Cela concerne la version 83 ou ultérieure du canal stable Microsoft Edge.

## <a name="why-do-we-need-progressive-rollout"></a>Pourquoi un déploiement progressif ?

En surveillant étroitement l’intégrité de nos mises à jour et en les déployant sur plusieurs jours, nous pouvons limiter l’impact des problèmes liés aux nouvelles mises à jour. Avec Microsoft Edge version 83, le déploiement progressif est activé pour toutes les versions Windows 7, Windows 8 et 8.1, et Windows 10 de Microsoft Edge. Nous prendrons en charge Microsoft Edge sur Mac dès qu’il sera prêt.

## <a name="how-will-the-updates-work"></a>Comment se dérouleront les mises à jour ?

Une valeur de mise à niveau est attribuée à chaque installation de Microsoft Edge. Lorsque nous lançons le déploiement par incréments, la mise à jour s’affiche lorsque la valeur de votre appareil est comprise dans la plage de valeurs de mise à niveau. Au fur et à mesure du déploiement (dans un délai de quelques jours), tous les utilisateurs finissent par obtenir la mise à jour. Les mises à jour de navigateur incluant des correctifs de sécurité critiques auront une cadence de déploiement plus rapide que les mises à jour qui en sont dépourvu. Cela permet de garantir une protection rapide contre les vulnérabilités.

## <a name="how-does-this-affect-enterprises"></a>En quoi les grandes entreprises sont-elles affectées ?

Les artefacts Microsoft Edge sont distribués aux grandes entreprises à l’aide de plusieurs mécanismes tels que Microsoft Intune, Windows Server Update Service (WSUS) et le gestionnaire de configuration. Ces outils de déploiement se comportent différemment en ce qui concerne le déploiement progressif :

- Les grandes entreprises qui gèrent la distribution via Microsoft Intune sont inscrites aux mises à jour automatiques. Le déploiement progressif est utilisé et tous les utilisateurs verront une mise à jour dans quelques jours.
- Les entreprises qui gèrent la distribution via WSUS (Windows Server Update Services) ou le gestionnaire de configuration ne sont pas inscrites aux mises à jour automatiques. Les administrateurs gèrent et appliquent les mises à jour disponibles dès le début. Le déploiement progressif n’affecte pas ce processus.

Partagez vos précieux commentaires par le biais de UserVoice, du bouton Commentaires dans les applications ou ci-dessous dans la section Commentaires si vous avez des questions ou des remarques.

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
