---
title: Prise en charge des plateformes pour les fonctionnalités de Microsoft Edge
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 03/25/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Résumé de la prise en charge de la plateforme pour les fonctionnalités de Microsoft Edge
ms.openlocfilehash: 3fb4fc0bc2671bdee5055fa650f191c5d3821963
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617724"
---
# <a name="platform-support-for-microsoft-edge-features"></a>Prise en charge des plateformes pour les fonctionnalités de Microsoft Edge

Cet article récapitule la prise en charge de la plateforme pour les fonctionnalités de Microsoft Edge.

> [!NOTE]
> Cet article concerne Microsoft Edge version 77 ou ultérieure.

## <a name="feature-matrix-for-platforms"></a>Matrice de fonctionnalités pour les plateformes

Les tableaux suivants résument la prise en charge des fonctionnalités pour les plateformes Windows et macOS.

> [!NOTE]
> Android et iOS ne sont actuellement pas représentés dans les tables de support, mais nous continuons à travailler sur ces informations et nous allons les mettre à jour en conséquence.

| Fonctionnalités de sécurité |Win 10|Win 8.1|Win 7|macOS|URL|
|--------|-------|--------|-----|-------|---|
|Accès conditionnel à Azure Active Directory (Azure AD)|Oui|Oui|Oui|Oui|[Accès conditionnel Azure AD](/deployedge/ms-edge-security-conditional-access#accessing-conditional-access-protected-resources-in-microsoft-edge)|
|Microsoft Defender Application Guard|Oui (1890+)|Non|Non|Non|[Microsoft Defender Application Guard](/deployedge/microsoft-edge-security-windows-defender-application-guard) |
|Microsoft Defender SmartScreen|Oui|Oui|Oui|Oui|[Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) |
|Microsoft Endpoint DLP|Oui|Non|Non|Non|[Microsoft Endpoint DLP](/deployedge/microsoft-edge-security-dlp#microsoft-endpoint-data-loss-prevention-endpoint-dlp)|
|Moniteur de mots de passe|Oui|Oui|Oui|Oui|[Moniteur de mots de passe](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Générateur de mot de passe|Oui|Oui|Oui|Oui|[Générateur de mot de passe](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Protection des informations Windows (WIP)|Oui (1607+)|Non|Non|Non|[TEC](/deployedge/microsoft-edge-security-windows-information-protection#system-requirements)|

|Fonctionnalités d’identité| Win 10 | Win 8.1 | Win 7 | macOS | URL |
|--|--|--|--|--|--|
|Connexion automatique (hybride/AAD-J)|Oui|Oui|Oui|Non|[hybride/AAD-J](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Connexion automatique (joint au domaine)|Oui|Oui|Oui|Non|[joint au domaine](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Connexion automatique (le compte par défaut du système d’exploitation est MSA)|Oui (1709+)|Non|Non|Non|[MSA](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Navigateur vers l’authentification unique via le web (SSO)|Oui|Oui|Oui|Oui|[Browser-Web SSO](https://www.microsoft.com/microsoft-365/roadmap?featureid=66332)|
|Commutateur guidé/« Changement de profil automatique »|Oui|Oui|Oui|Oui|[Utilisation de plusieurs profils au travail et à la maison](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Profils multiples|Oui|Oui|Oui|Oui|[Utilisation de plusieurs profils au travail et à la maison](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Synchronisation locale pour Active Directory (AD)|Oui|Oui|Oui|Non|[Synchronisation locale pour les utilisateurs de Active Directory (AD)](/deployedge/microsoft-edge-on-premises-sync) |
|SSO transparente|Oui (1709+)|Oui|Oui|Oui|[SSO transparente](/deployedge/microsoft-edge-security-identity#seamless-sso)|
|SSO avec jeton d’actualisation principal (PRT)|Oui (1709+)|Oui|Oui|Non|[SSO avec PRT](/deployedge/microsoft-edge-security-identity#sso-with-primary-refresh-token-prt)|
|Authentification Windows intégrée (WIA)|Oui|Oui|Oui|Oui* (stratégie requise)|[WIA](/deployedge/microsoft-edge-security-identity#windows-integrated-authentication-wia)|

|Fonctionnalités supplémentaires|Win 10|Win 8.1|Win 7|macOS|URL|
|--------|-------|--------|-----|-------|---|
|Collections|Oui|Oui|Oui|Oui|[Collections](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/) |
|Page Nouvel onglet Entreprise|Oui|Oui|Oui|Oui|[Page Nouvel onglet](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/) |
|Mode Internet Explorer|Oui|Oui|Oui|Non|[Mode Internet Explorer](/deployedge/edge-ie-mode#prerequisites)|
|Mode plein écran|Oui|Non|Non|Non|[Mode plein écran](/deployedge/microsoft-edge-configure-kiosk-mode)|
|Recherche Microsoft dans Bing|Oui|Oui|Oui|Oui|[Recherche intelligente dans Bing](https://www.microsoft.com/edge/business/intelligent-search-with-bing) |
|Lecteur PDF|Oui|Oui|Oui|Oui|[Lecteur PDF](/deployedge/microsoft-edge-pdf) |
|Achats|Oui|Oui|Oui|Oui|[Achats](https://techcommunity.microsoft.com/t5/articles/introducing-shopping-with-microsoft-edge/m-p/1870080) |
|Onglets en veille|Oui|Oui|Oui|Oui|[Vue d’ensemble des fonctionnalités](/deployedge/microsoft-edge-relnote-stable-channel)<br>[Dernier billet de blog](https://blogs.windows.com/msedgedev/2021/03/04/edge-89-performance/)<br>[Stratégies de groupe](/deployedge/microsoft-edge-policies#sleeping-tabs-settings)|
|Synchronisation|Oui|Oui|Oui|Oui| [Synchronisation d’entreprise](/deployedge/microsoft-edge-enterprise-sync) |
|Restauration de version|Oui|Oui|Oui|Non|[Restauration de version](/deployedge/edge-learnmore-rollback) |
|Onglets verticaux|Oui|Oui|Oui|Oui| |

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)