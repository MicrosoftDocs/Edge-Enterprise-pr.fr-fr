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
ms.openlocfilehash: 898a86c8c268a8c46e80dbd5ef3a435c300fb04e
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447138"
---
# <a name="microsoft-edge-and-conditional-access"></a>Microsoft Edge et l’accès conditionnel
  
Cet article décrit la prise en charge de l’accès conditionnel par Microsoft Edge et l’accès aux ressources protégées par ce biais.

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

L’un des aspects clés de la sécurité du cloud est l’identité et l’accès pour la gestion de vos ressources cloud. Dans un monde où la priorité est donnée aux appareils mobiles et au cloud, les utilisateurs peuvent accéder aux ressources de votre organisation via divers appareils et applications, où qu’ils se trouvent. En conséquence, se focaliser sur qui peut accéder à une ressource ne suffit pas. Vous devez également prendre en compte le mode d’accès à la ressource. L’accès conditionnel Azure ActiveDirectory (Azure AD) vous aide à maîtriser l’équilibre entre sécurité et productivité.

## <a name="accessing-conditional-access-protected-resources-in-microsoft-edge"></a>Accès aux ressources protégées par un accès conditionnel dans MicrosoftEdge

MicrosoftEdge prend en charge en mode natif l’accès conditionnel AzureAD. Il n’est pas nécessaire d’installer une extension distincte. Lorsque vous êtes connecté(e) à un profil MicrosoftEdge avec des informations d’identification Azure AD d’entreprise, MicrosoftEdge permet un accès transparent aux ressources cloud d’entreprise protégées par l’accès conditionnel.

Sur un appareil conforme, l’identité qui accède à la ressource doit correspondre à l’identité du profil.  Si ce n’est pas le cas, vous verrez un message semblable à celui de la capture d’écran suivante. Dans l’exemple de capture d’écran, «testadmin@evostsoneboxtest.com» est le compte de connexion nécessaire pour accéder à la ressource.

![Message d’accès conditionnel dans le navigateur](./media/edge-security/microsoft-edge-security-conditional-access.png)

Pour continuer, vous devez basculer vers le profil requis (si vous en possédez un) ou créer un profil avec une identité correspondante.

Pour vous connecter et utiliser votre profil, cliquez sur l’avatar du compte dans l’angle supérieur droit du navigateur. Le menu Gérer l’alerte vous permet d’effectuer les actions suivantes:

- Sélectionner un autre profil. Cliquer sur le nom du profil.
- Créer un profil. Cliquez sur **Ajouter un profil**.
- Gérer vos profils. Cliquez sur **Gérer les paramètres de profil**.

Cette prise en charge est disponible sur toutes les plateformes, y compris toutes les versions prises en charge de Windows et de macOS.

### <a name="how-to-deploy-conditional-access-in-azure-active-directory"></a>Procédure de déploiement de l’accès conditionnel dans Azure Active Directory

[Déployer l’accès conditionnel](/azure/active-directory/conditional-access/plan-conditional-access) fournit un guide détaillé pour vous aider à déployer l’accès conditionnel dans Azure ActiveDirectory.

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Vidéo: sécurité, compatibilité et facilité de gestion](/microsoft-edge-video-security-compatibility-manageability.md)