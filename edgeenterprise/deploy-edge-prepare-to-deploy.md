---
title: Microsoft Edge dans votre environnement
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge dans votre environnement
ms.openlocfilehash: 2381380cb399f6a1fbb5efa9378ffeba20fa774f
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641600"
---
# <a name="microsoft-edge-in-your-environment"></a>Microsoft Edge dans votre environnement

Cet article explique comment préparer le déploiement de Microsoft Edge lorsque l’ancienne version de Microsoft Edge atteint sa fin de service.

Comme le permet [le billet de blog](https://aka.ms/EdgeLegacyEOS) de l’équipe produit Microsoft Edge, la prise en charge de l’application de bureau de l’ancienne version de Microsoft Edge prendra fin le 9 mars 2021. Lorsque vous appliquez la version Update Tuesday (ou « B ») en avril, elle supprimera l’ancienne version de Microsoft Edge des appareils exécutant Windows 10 RS4 à 20H1 et la remplacera par Microsoft Edge.

## <a name="how-to-prepare"></a>Comment se préparer

Pour préparer l’installation de Microsoft Edge sur les appareils Windows 10 RS4 à 20H1 avec la version Update Tuesday en avril, nous vous recommandons de lire [Planifier votre déploiement de Microsoft Edge](deploy-edge-plan-deployment.md).

Après avoir planifié votre déploiement, utilisez l’une des approches suivantes pour préparer le déploiement de Microsoft Edge.

- **Installez des stratégies de groupe pour personnaliser votre approche de mise à jour Microsoft Edge**. Pour plus d’informations, voir [Configurer les paramètres de stratégie Microsoft Edge sur Windows](configure-microsoft-edge.md) et prêter une attention particulière au document [de référence de la stratégie de mise à jour](microsoft-edge-update-policies.md). Si vous installez des stratégies de groupe pour gérer vos mises à jour avant d’installer la version Update Tuesday d’avril, Microsoft Edge commencera immédiatement à respecter votre stratégie. S’il n’existe aucune stratégie de groupe installée, Microsoft Edge se mettra automatiquement à jour.

- **Supprimez l’application de bureau de l’ancienne version de Microsoft Edge avant sa date de fin de service du 9 mars 2021 et déployez Microsoft Edge**. Pour Windows 10 RS4 à 20H1, vous pouvez le faire à l’aide des mises à jour Windows. Pour plus d’informations, voir [Déployer Microsoft Edge avec les mises à jour Windows 10](deploy-edge-with-windows-10-updates.md).

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Planifier votre déploiement de Microsoft Edge](deploy-edge-plan-deployment.md)