---
title: Prise en charge et configuration des identités Microsoft Edge
ms.author: avvaid
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Prise en charge et configuration des identités Microsoft Edge
ms.openlocfilehash: 05dc0fabe212f31fe9207c72d097913d5765915f
ms.sourcegitcommit: c290b0b0fa6b7d7f94dcdfdda91302da733326ec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314607"
---
# Prise en charge et configuration des identités Microsoft Edge

Cet article décrit comment Microsoft Edge utilise les identités pour prendre en charge des fonctionnalités telles que la synchronisation et l’authentification unique (SSO). Microsoft Edge prend en charge la connexion avec Active Directory Domain Services (AD DS), Azure Active Directory (Azure AD) et les comptes Microsoft (MSA). Pour l’instant, Microsoft Edge prend uniquement en charge les comptes Azure Active Directory (Azure AD) appartenant au cloud global ou au cloud souverain GCC. Nous travaillons à l’ajout d’une prise en charge des autres clouds souverains.

> [!NOTE]
> Ceci concerne Microsoft Edge version 77 ou ultérieure.

##  <a name="browser-sign-in-and-authenticated-features"></a>Connexion au navigateur et fonctionnalités basées sur l’authentification

Microsoft Edge prend en charge la connexion à un profil de navigateur avec un compte Azure AD, MSA ou de domaine. Le type de compte utilisé pour la connexion détermine les fonctionnalités basées sur l’authentification disponibles pour l’utilisateur dans Microsoft Edge. Le tableau suivant résume la prise en charge des fonctionnalités pour chaque type de compte.

| Fonctionnalité   | Azure AD Premium | Azure AD Free | Services AD DS en local | MSA     |
|----|------------------|---------------|----------------|---------|
| Synchronisation | Oui | Non | Non | Oui |
| SSO avec jeton d’actualisation principal | Oui | Oui | Non | Oui |
| SSO transparente | Oui | Oui | Oui | Non applicable |
| Authentification Windows intégrée | Oui | Oui | Oui | Non applicable |
| Page de nouvel onglet Entreprise | Nécessite O365 |   Nécessite O365 | Non | Non applicable |
| Recherche Microsoft | Nécessite O365 | Nécessite O365 | Non | Non applicable |

##  <a name="how-users-can-sign-into-microsoft-edge"></a>Comment les utilisateurs se connectent à Microsoft Edge

###  <a name="automatic-sign-in"></a>Connexion automatique

Microsoft Edge utilise le compte par défaut du système d’exploitation pour se connecter automatiquement au navigateur. En fonction de la configuration de l’appareil, les utilisateurs peuvent se connecter automatiquement à Microsoft Edge en utilisant l’une des approches suivantes.

- **L’appareil est hybride/AAD-J :** disponible sur Win10, les versions antérieures de Windows et les versions de serveur correspondantes.
L’utilisateur est connecté automatiquement avec son compte Azure AD.
- **L’appareil est une jonction de domaine :** disponible sur Win10, les versions antérieures de Windows et les versions de serveur correspondantes.
Par défaut, l’utilisateur n’est pas connecté automatiquement. Si vous souhaitez connecter automatiquement les utilisateurs avec des comptes de domaine, utilisez la stratégie [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/deployedge/microsoft-edge-policies#configureonpremisesaccountautosignin). Si vous souhaitez connecter automatiquement les utilisateurs avec leur compte Azure AD, utilisez la jonction hybride de vos appareils.
- **Le compte par défaut du système d’exploitation est un MSA :** Win10 RS3 (version 1709/build 10.0.16299) et les versions ultérieures. Ce cas est peu probable pour les appareils professionnels. En revanche, si le compte par défaut du système d’exploitation est un MSA, Microsoft Edge se connectera automatiquement avec le compte MSA.

###  <a name="manual-sign-in"></a>Connexion manuelle

Si l’utilisateur n’est pas automatiquement connecté à Microsoft Edge, il peut se connecter manuellement lors de la première utilisation, dans les paramètres du navigateur ou en ouvrant le menu volant identité.

###  <a name="managing-browser-sign-in"></a>Gestion de la connexion au navigateur

Si vous souhaitez gérer la connexion au navigateur, vous pouvez utiliser les stratégies suivantes :

- vérifier que les utilisateurs disposent toujours d’un profil professionnel sur Microsoft Edge. [Consulter NonRemovableProfileEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#nonremovableprofileenabled)
- limiter la connexion à un ensemble de comptes approuvés. [consulter RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern)
- désactiver ou forcez la connexion au navigateur. [Consulter BrowserSignin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#browsersignin)

##  <a name="browser-to-web-single-sign-on-(sso)"></a>Authentification unique (SSO) du navigateur vers le web

Sur certaines plateformes, vous pouvez configurer Microsoft Edge afin que la connexion aux sites web des utilisateurs soit automatique. Cette option leur évite d’avoir à ressaisir leurs informations d’identification pour accéder à leurs sites web professionnels et augmente ainsi leur productivité.

###  <a name="sso-with-primary-refresh-token-(prt)"></a>SSO avec jeton d’actualisation principal (PRT)

Microsoft Edge a une prise en charge native de l’authentification unique basée sur un PRT, et vous n’avez pas besoin d’une extension. Sur Windows 10 RS3 et versions ultérieures, si un utilisateur est connecté à son profil de navigateur, il obtiendra l’authentification unique avec le mécanisme PRT sur les sites web qui prennent en charge l’authentification unique basée sur un PRT.

Un jeton d’actualisation principal (PRT) est une clé Azure AD utilisée pour l’authentification sur les appareils Windows 10, iOS et Android. Il permet d’activer l’authentification unique (SSO) dans les applications utilisées sur ces appareils. Pour plus d’informations, consultez [Qu’est-ce qu’un jeton d’actualisation principal ?](https://docs.microsoft.com/azure/active-directory/devices/concept-primary-refresh-token).

###  <a name="seamless-sso"></a>SSO transparente

Tout comme l’authentification unique avec un PRT, Microsoft Edge dispose d’une prise en charge native de l’authentification unique transparente, sans avoir besoin d’une extension. Sur Windows 10 RS3 et versions ultérieures, si un utilisateur est connecté à son profil de navigateur, il obtiendra l’authentification unique avec le mécanisme PRT sur les sites web qui prennent en charge l’authentification unique basée sur un PRT.

L’authentification unique transparente connecte automatiquement les utilisateurs lorsqu’ils utilisent des appareils d’entreprise connectés à un réseau d’entreprise. Lorsque cette option est activée, les utilisateurs n’ont pas besoin de taper leurs mots de passe pour se connecter à Azure AD. En règle générale, ils n’ont pas non plus besoin de taper leur nom d’utilisateur. Pour plus d’informations, consultez [Authentification unique Active Directory transparente](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sso).

###  <a name="windows-integrated-authentication-(wia)"></a>Authentification Windows intégrée (WIA)

Microsoft Edge prend également en charge l’authentification Windows intégrée pour les demandes d’authentification au sein du réseau interne d’une organisation pour les applications qui utilisent un navigateur pour leur authentification. Cette option est prise en charge sur toutes les versions de Windows 10 et les versions antérieures de Windows. Par défaut, Microsoft Edge utilise la zone Intranet comme liste verte pour WIA. Vous pouvez également personnaliser la liste des serveurs activés pour l’authentification intégrée à l’aide de la stratégie [AuthServerAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#authserverallowlist) . Sur macOS, cette stratégie est nécessaire pour activer l’authentification intégrée.

Pour prendre en charge l’authentification unique basée sur WIA sur Microsoft Edge (version 77 et ultérieure), vous devrez également effectuer une configuration côté serveur. Vous devrez probablement configurer la propriété de services de fédération Active Directory (AD FS) **WiaSupportedUserAgents** pour ajouter la prise en charge de la nouvelle chaîne d’agent utilisateur Microsoft Edge. Si vous souhaitez obtenir des instructions concernant la configuration de la propriété, consultez [Afficher les paramètre WIASupportedUserAgent](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia#view-wiasupporteduseragent-settings) et [Modifier les paramètres WIASupportedUserAgent](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia#change-wiasupporteduseragent-settings). Un exemple de la chaîne d’agent utilisateur Microsoft Edge sur Windows 10 est illustré ci-dessous. Si vous souhaitez en savoir plus, consultez l’article sur la [chaine de l’agent utilisateur Microsoft Edge](https://docs.microsoft.com/microsoft-edge/web-platform/user-agent-string). 

L’exemple suivant de chaîne UA est destiné à la build du canal Dev la plus récente au moment de la publication de cet article :<br> `"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3951.0 Safari/537.36 Edg/80.0.334.2"`

Pour les services qui nécessitent la délégation des informations d’identification de négociation, Microsoft Edge prend en charge la délégation contrainte à l’aide de la stratégie [AuthNegotiateDelegateAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#authnegotiatedelegateallowlist) .

##  <a name="additional-authentication-concepts"></a>Concepts d’authentification supplémentaires

###  <a name="proactive-authentication"></a>Authentification proactive

L’authentification proactive est une optimisation de l’authentification unique du navigateur vers le site web qui charge l’authentification sur certains sites web propriétaires. Les performances de la barre d’adresses sont ainsi améliorées si l’utilisateur utilise Bing comme moteur de recherche. Ainsi, les utilisateurs ont des résultats personnalisés et des résultats de recherche Microsoft pour les entreprises(MSB). Cela permet également d’autoriser l’authentification à des services clés comme la page Office Nouvel onglet. Vous pouvez contrôler celle-ci en utilisant la stratégie [ProactiveAuthEnabled]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#proactiveauthenabled).

###  <a name="windows-hello-credui-for-ntlm-authentication"></a>Windows Hello CredUI pour l’authentification NTLM

Lorsqu’un site Web essaie de connecter des utilisateurs à l’aide des mécanismes NTLM ou Negotiate et que l’authentification unique n’est pas disponible, nous offrons aux utilisateurs une expérience dans laquelle ils peuvent partager leurs informations d’identification de système d’exploitation avec le site web pour répondre au test d’authentification à l’aide de Windows Hello Cred UI. Ce flux de connexion n’apparaîtra que pour les utilisateurs de Windows 10 qui n’obtiennent pas de connexion unique lors d’un test NTLM ou Negotiate.

###  <a name="sign-in-automatically-using-saved-passwords"></a>Se connecter automatiquement en utilisant des mots de passe enregistrés

Si un utilisateur enregistre des mots de passe dans Microsoft Edge, il peut activer une fonctionnalité qui le connecte automatiquement aux sites web dans lesquels ses informations d’identification sont enregistrées. Les utilisateurs peuvent activer et désactiver cette fonctionnalité en se rendant sur *edge://settings/passwords*. Si vous souhaitez configurer cette fonctionnalité, vous pouvez utiliser les stratégies du [gestionnaire de mot de passe](https://docs.microsoft.com/deployedge/microsoft-edge-policies#password-manager-and-protection).

##  <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Vidéo : Microsoft Edge et identité](microsoft-edge-video-identity.md)
- [Gestion des identités et des accès](https://www.microsoft.com/security/technology/identity-access-management)
- [Plateforme d’identité](https://developer.microsoft.com/identity)
- [Quatre étapes pour une fondation d’identité forte avec Azure Active Directory](https://docs.microsoft.com/azure/active-directory/hybrid/four-steps)
