---
title: Vue d’ensemble de la sécurité de MicrosoftEdge
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 04/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Vue d’ensemble du déploiement de la sécurité de MicrosoftEdge
ms.openlocfilehash: f22f2dcbace00cd535d201950c2af488c708525b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979846"
---
# Vue d’ensemble de la sécurité de MicrosoftEdge
  
Les administrateurs informatiques de l’entreprise sont constamment confrontés à une myriade de défis de sécurité existants et émergents lorsqu’ils tentent de protéger le réseau et les périphériques de leur entreprise des attaques malveillantes et d’empêcher les accès non autorisés et les fuites de données d’entreprise. MicrosoftEdge offre plusieurs fonctionnalités natives uniques qui permettent de relever ces défis.

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

## Accès conditionnel

L’un des aspects clés de la sécurité du cloud est l’identité et l’accès pour la gestion de vos ressources cloud. Dans un monde où la priorité est donnée aux appareils mobiles et au cloud, les utilisateurs peuvent accéder aux ressources de votre organisation via divers appareils et applications, où qu’ils se trouvent. En conséquence, se focaliser sur qui peut accéder à une ressource ne suffit pas. Vous devez également prendre en compte le mode d’accès à la ressource. L’accès conditionnel Azure ActiveDirectory (Azure AD) vous aide à maîtriser l’équilibre entre sécurité et productivité.

### Accès aux ressources protégées par un accès conditionnel dans MicrosoftEdge

MicrosoftEdge prend en charge en mode natif l’accès conditionnel AzureAD. Il n’est pas nécessaire d’installer une extension distincte. Lorsque vous êtes connecté(e) à un profil MicrosoftEdge avec des informations d’identification Azure AD d’entreprise, MicrosoftEdge permet un accès transparent aux ressources cloud d’entreprise protégées par l’accès conditionnel.

Sur un appareil conforme, l’identité qui accède à la ressource doit correspondre à l’identité du profil.  Si ce n’est pas le cas, vous verrez un message semblable à celui de la capture d’écran suivante. Dans l’exemple de capture d’écran, «testadmin@evostsoneboxtest.com» est le compte de connexion nécessaire pour accéder à la ressource.

![Message d’accès conditionnel dans le navigateur](./media/edge-security/microsoft-edge-security-conditional-access.png)

Pour continuer, vous devez basculer vers le profil requis (si vous en possédez un) ou créer un profil avec une identité correspondante.

Pour vous connecter et utiliser votre profil, cliquez sur l’avatar du compte dans l’angle supérieur droit du navigateur. Le menu Gérer l’alerte vous permet d’effectuer les actions suivantes:

- Sélectionner un autre profil. Cliquer sur le nom du profil.
- Créer un profil. Cliquez sur **Ajouter un profil**.
- Gérer vos profils. Cliquez sur **Gérer les paramètres de profil**.

Cette prise en charge est disponible sur toutes les plateformes, y compris toutes les versions prises en charge de Windows et de macOS.

### Procédure de déploiement de l’accès conditionnel dans Azure Active Directory

[Déployer l’accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) fournit un guide détaillé pour vous aider à déployer l’accès conditionnel dans Azure ActiveDirectory.

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Vidéo: sécurité, compatibilité et facilité de gestion](/microsoft-edge-video-security-compatibility-manageability.md)
