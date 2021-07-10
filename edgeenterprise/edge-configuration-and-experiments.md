---
title: Configurations et expérimentation de Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Configurations et expérimentation de Microsoft Edge
ms.openlocfilehash: 1ebfe5fc1da107aa7e9e20b629f14aff468bdd6d
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641560"
---
# <a name="microsoft-edge-configurations-and-experimentation"></a>Configurations et expérimentation de Microsoft Edge

Cet article décrit l’interaction entre MicrosoftEdge et le Service d’expérimentation et de configuration (ECS). MicrosoftEdge communique avec ce service pour demander et recevoir différents types de charges utiles. Ces charges utiles sont notamment les configurations, les déploiements de fonctionnalités et les expériences.

> [!IMPORTANT]
> Veuillez vous assurer que les clients peuvent accéder à `https://config.edge.skype.com` afin que les charges utiles soient reçues.

> [!NOTE]
> Il concerne MicrosoftEdge version77 ou ultérieure.

## <a name="configurations"></a>Configurations

Les configurations sont la charge utile destinée à garantir l’intégrité du produit, la sécurité et la conformité de la confidentialité. Elles sont conçues pour avoir la même valeur pour tous les utilisateurs (en fonction des plateformes et des canaux.) Il peut s’agir de l’activation d’un indicateur de fonctionnalité pour une action de domaine, qui peut également être utilisée pour désactiver un indicateur de fonctionnalité en cas de bogue.

## <a name="controlled-feature-rollout"></a>Déploiement de fonctionnalités contrôlé

Le déploiement de fonctionnalités contrôlé (CFR) est une procédure qui permet d’augmenter lentement la taille du groupe d’utilisateurs qui reçoit une fonctionnalité. En distribuant une nouvelle fonctionnalité à un sous-ensemble de la population d’utilisateurs sélectionné de façon aléatoire, il est possible de comparer les commentaires utilisateur à un groupe de contrôle de taille égale sans la fonctionnalité, afin de mesurer l’impact de la fonctionnalité.

## <a name="experiments"></a>Expériences

Les builds MicrosoftEdge ont des fonctionnalités et fonctions qui sont toujours en développement ou qui sont expérimentales. Les expériences sont comme les CFR, mais la taille du groupe d’utilisateurs est plus petite pour tester le nouveau concept. Ces fonctionnalités sont masquées par défaut jusqu’à ce que la fonctionnalité déployée ou que l’expérience soit terminée. Les indicateurs d’expérience sont utilisés pour activer et désactiver ces fonctionnalités.

## <a name="about-the-ecs"></a>À propos de l’ECS

Dans tous les scénarios précédents, le service fournit les valeurs d’indicateur de fonctionnalité au client de navigateur afin qu’elles puissent être appliquées. En fonction de la mise à jour, les configurations sont appliquées immédiatement ou lorsque l’utilisateur redémarre le navigateur.

L’interaction de MicrosoftEdge avec ce service est contrôlée par les paramètres de la stratégie [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol). Vous pouvez configurer les paramètres de la stratégie de configuration de sorte à:

- Récupérer les configurations uniquement
- Récupérer les configurations et les expérimentations
- Désactiver la communication avec le service

  > [!CAUTION]
  > Si vous désactivez les communications avec le service, cela affectera la capacité de Microsoft à répondre à un bogue grave en temps et en heure.

## <a name="see-also"></a>Articles associés

- [Page d’accueil Microsoft Edge Entreprise](https://www.microsoftedgeinsider.com/enterprise)
- [Page d’accueil de la documentation MicrosoftEdge](./index.yml)