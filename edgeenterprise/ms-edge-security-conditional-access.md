---
title: Microsoft Edge et l’accès conditionnel
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 10/02/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge et l’accès conditionnel
ms.openlocfilehash: a81d39c15f418dab6565ee7acc45de17f66e3828
ms.sourcegitcommit: 3478cfcf2b03944213a7c7c61f05490bc37aa7c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/03/2020
ms.locfileid: "11094771"
---
# Microsoft Edge et l’accès conditionnel
  
Cet article décrit la prise en charge de l’accès conditionnel par Microsoft Edge et l’accès aux ressources protégées par ce biais.

> [!NOTE]
> Cet article concerne Microsoft Edge version 77 ou ultérieure.

L’un des aspects clés de la sécurité du cloud est l’identité et l’accès pour la gestion de vos ressources cloud. Dans un monde où la priorité est donnée aux appareils mobiles et au cloud, les utilisateurs peuvent accéder aux ressources de votre organisation via divers appareils et applications, où qu’ils se trouvent. En conséquence, se focaliser sur qui peut accéder à une ressource ne suffit pas. Vous devez également prendre en compte le mode d’accès à la ressource. L’accès conditionnel Azure Active Directory (Azure AD) vous aide à maîtriser l’équilibre entre sécurité et productivité.

## Accès aux ressources protégées par un accès conditionnel dans Microsoft Edge

Microsoft Edge prend en charge en mode natif l’accès conditionnel Azure AD. Il n’est pas nécessaire d’installer une extension distincte. Lorsque vous êtes connecté(e) à un profil Microsoft Edge avec des informations d’identification Azure AD d’entreprise, Microsoft Edge permet un accès transparent aux ressources cloud d’entreprise protégées par l’accès conditionnel.

Sur un appareil conforme, l’identité qui accède à la ressource doit correspondre à l’identité du profil.  Si ce n’est pas le cas, vous verrez un message semblable à celui de la capture d’écran suivante. Dans l’exemple de capture d’écran, « testadmin@evostsoneboxtest.com » est le compte de connexion nécessaire pour accéder à la ressource.

![Message d’accès conditionnel dans le navigateur](./media/edge-security/microsoft-edge-security-conditional-access.png)

Pour continuer, vous devez basculer vers le profil requis (si vous en possédez un) ou créer un profil avec une identité correspondante.

Pour vous connecter et utiliser votre profil, cliquez sur l’avatar du compte dans l’angle supérieur droit du navigateur. Le menu Gérer l’alerte vous permet d’effectuer les actions suivantes :

- Sélectionner un autre profil. Cliquer sur le nom du profil.
- Créer un profil. Cliquez sur **Ajouter un profil**.
- Gérer vos profils. Cliquez sur **Gérer les paramètres de profil**.

Cette prise en charge est disponible sur toutes les plateformes, y compris toutes les versions prises en charge de Windows et de macOS.

### Procédure de déploiement de l’accès conditionnel dans Azure Active Directory

[Déployer l’accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) fournit un guide détaillé pour vous aider à déployer l’accès conditionnel dans Azure Active Directory.

## Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Vidéo : sécurité, compatibilité et facilité de gestion](/microsoft-edge-video-security-compatibility-manageability.md)
