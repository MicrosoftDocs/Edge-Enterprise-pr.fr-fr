---
title: Edge pour l’infrastructure de bureau de virtualisation
ms.author: anlake
author: AndreaLBarr
manager: collw
ms.date: 06/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge pour l’infrastructure bureau virtualisée.
ms.openlocfilehash: eaad1b72934b336ce86d14dd8da92a6984d21914
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618092"
---
# <a name="microsoft-edge-for-virtualized-desktop-infrastructure"></a>Microsoft Edge pour l’infrastructure bureau virtualisée

Cet article décrit les exigences et les limitations relatives à l’utilisation de Microsoft Edge dans un environnement virtualisé.

## <a name="what-is-vdi"></a>Qu’est-ce que VDI ?

L’infrastructure VDI (Virtual Desktop Infrastructure) est une technologie de virtualisation qui héberge un système d’exploitation de bureau et des applications sur un serveur centralisé dans un centre de données. Cela permet aux utilisateurs d’avoir une expérience de bureau entièrement personnalisée avec une source centralisée entièrement sécurisée et conforme.

Microsoft Edge peut être utilisé dans un environnement virtualisé de la même manière que sur l’appareil local, tout en s’exécutant à partir d’un environnement serveur sécurisé et contrôlé. En fonction de votre solution VDI choisie, il peut également être possible de donner à vos utilisateurs un accès transparent aux sites et applications intranet.

La plupart des fonctionnalités de Edge sont prises en charge dans les environnements VDI sans configuration spéciale. Toutefois, pour garantir une expérience optimale, il est recommandé de suivre les instructions ci-dessous.

## <a name="platforms-certified-for-edge"></a>Plateformes certifiées pour Edge

- Azure Virtual Desktop
- Citrix Virtual Apps and Desktops (anciennement XenApp et XenDesktop)

Bien que d’autres solutions VDI n’ont pas encore été vérifiées par l’équipe Edge, il est prévu que les flux de travail les plus courants dans Edge soient pris en charge. Les conseils fournis ci-dessous peuvent s’appliquer ou non à la solution que vous avez choisie.

## <a name="edge-on-vdi-performance-considerations"></a>Considérations des performances Edge sur VDI

Lors de la conception de votre environnement VDI, vous devez considérer attentivement les flux de travail et les besoins de vos utilisateurs pour obtenir des performances optimales, ainsi que les limites de votre configuration de serveur.

Edge recommande les exigences minimales suivantes pour le déploiement d’Edge dans des environnements VDI :

- vCPU – 2 à 4 cœurs par utilisateur
- RAM – 1 Go par utilisateur

Notez que les extensions et les applications web complexes de grande taille nécessitent davantage de mémoire et doivent être prises en compte lors de la configuration de votre environnement.

## <a name="edge-on-non-persisted-vdi-environments"></a>Edge sur les environnements VDI non persistants

De nombreuses solutions VDI permettent d’accéder à des environnements persistants, où les utilisateurs se voit attribuer un environnement virtuel qui persiste entre les sessions et des environnements non persistants, où les utilisateurs sont affectés à l’un des ordinateurs disponibles, éventuellement à un autre ordinateur chaque session, les données utilisateur peuvent ou non se synchroniser entre les sessions.

Lorsque vous utilisez un environnement non persistant, on crée généralement une « image de base » qui est utilisée pour chaque appareil qui inclut les applications et configurations nécessaires. Voici nos recommandations pour préparer Edge pour une telle image.

### <a name="deploy-edge"></a>Déployer Edge

Si vous êtes sur Windows 10 version 1803 et supérieure, vous devez avoir installé Microsoft Edge sur votre système. Toutefois, si vous êtes sur une version antérieure de Windows ou que vous souhaitez déployer un autre canal d’Edge, les étapes suivantes sont recommandées.

1. Téléchargez le package Edge MSI correspondant au système d’exploitation de votre machine virtuelle VDI à partir de :

    - [Télécharger Microsoft Edge pour les entreprises – Microsoft](https://www.microsoft.com/edge/business/download)

2. Installez MSI sur la machine virtuelle VDI en exécutant la commande suivante :

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### <a name="disable-automatic-updates"></a>Désactiver les mises à jour automatiques

Pour les ordinateurs non persistants, il est préférable de désactiver les mises à jour automatiques et de mettre à jour Edge en mettant à jour l'« image de base » pour s’assurer qu’il n’y a pas de version non correspondante parmi le groupe d’ordinateurs.

Consultez les stratégies suivantes pour désactiver les mises à jour automatiques :

- [Remplacer la stratégie de mise à jour par défaut](/deployedge/microsoft-edge-update-policies#updatedefault)

- [Remplacer la stratégie de mise à jour](/deployedge/microsoft-edge-update-policies#update)

### <a name="profile-management"></a>Gestion des profils

Sur les configurations non persistantes, il est important de prendre en compte le fait que les ordinateurs virtuels peuvent ne pas maintenir l’état utilisateur entre les sessions ou qu’un ordinateur personnel qu’ils n’ont jamais utilisé auparavant peut ne pas avoir de données utilisateur.

Edge prend en charge plusieurs méthodes de synchronisation des données utilisateur de telle manière qu’elles soient disponibles, quelle que soit la façon dont ils accèdent à Edge.

### <a name="azure-ad-sync"></a>Azure AD Sync

Si votre plan Azure AD le prend en charge, la synchronisation Entreprise est la méthode la plus rapide et la plus simple pour vous assurer que les données utilisateur Edge sont synchronisées avec tous les appareils des utilisateurs.  

Pour plus d’informations sur les conditions requises et la configuration, voir les informations suivantes.  

- [Configurer la synchronisation Microsoft Edge Entreprise | Microsoft Docs](/deployedge/microsoft-edge-enterprise-sync)

### <a name="on-premise-sync-for-active-directory-users"></a>Synchronisation sur site pour les utilisateurs Active Directory

Avec la synchronisation sur site, Microsoft Edge enregistre les favoris et les paramètres d’un utilisateur Active Directory dans un fichier qui peut facilement être déplacé entre différents ordinateurs.  

Pour plus d’informations sur les conditions requises et la configuration, voir les informations suivantes.  

- [Synchronisation locale pour les utilisateurs Active Directory (AD) | Microsoft Docs](/deployedge/microsoft-edge-on-premises-sync)

### <a name="user-profile-redirection"></a>Redirection de profil utilisateur  

Il existe plusieurs solutions pour migrer et rediriger l’intégralité du dossier utilisateur afin de garantir que le contexte utilisateur est conservé dans ces environnements non persistants. Consultez votre fournisseur VDI pour déterminer la solution recommandée.

Voici quelques solutions populaires :

- [Vue d’ensemble de FSLogix – FSLogix | Microsoft Docs](/fslogix/overview)
- [Comment configurer la gestion des profils Citrix](https://support.citrix.com/article/CTX222893)

Il est également recommandé d’exclure, lors de l’utilisation de cette méthode, les dossiers inutiles du dossier utilisateur sauvegardé afin de réduire les temps de chargement initiaux lorsque les utilisateurs se connectent à un ordinateur et que le profil est en cours de migration. Si c’est le cas, nous vous recommandons d’exclure les dossiers suivants de votre sauvegarde pour réduire la taille.

- %LocalAppData%\Microsoft\Edge\User Data\Default\Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed

## <a name="known-issues"></a>Problèmes connus

### <a name="microsoft-edge-crashes-in-older-versions-of-xenapp-and-xendesktop"></a>Microsoft Edge se bloque dans les versions antérieures de XenApp et XenDesktop

Ce problème doit être corrigé dans les versions plus récentes. Cependant, si vous rencontrez ce problème dans votre environnement, vous pouvez le contourner en désactivant les Hooks d’API Citrix pour Edge. Consultez [Comment désactiver les hooks d’API Citrix par application.](https://support.citrix.com/article/CTX107825)

### <a name="degraded-performance-when-rendering-pages-with-exceptionally-large-html-tables"></a>Performances dégradées lors du rendu de pages avec des tableaux HTML exceptionnellement grands

Les stratégies Citrix suivantes sont connues pour ralentir le rendu des pages html avec des tableaux très grands (plus de 30 000 lignes).

- Affichage automatique du clavier
- Distant du contrôle zone de liste déroulante

Voir [paramètres de stratégie d’expérience mobile (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) pour plus d’informations. La désactivation de ces stratégies doit atténuer le problème.

### <a name="windows-account-manager-authorization-scenarios-ie--azure-sync-fail-in-edge-when-run-as-a-citrix-seamless-application"></a>Les scénarios d’autorisation Windows Account Manger (c’est-à-dire,  la synchronisation) sont en échec dans Edge lorsqu’ils sont exécutés en tant qu’application transparente Citrix

Il s’agit d’un problème connu dans Edge et dans d’autres applications qui utilisent WAM (c’est-à-dire, Office) en raison des composants Windows nécessaires pour ces scénarios qui ne sont pas initialisés lors de l’exécution en mode « transparent ». Pour contourner ce problème :

- Utilisez Edge via un Bureau à distance vers l’hôte Citrix au lieu d’une application distante transparente.
- Utilisez plutôt les applications distantes Azure Virtual Desktop, qui ont des atténuations pour ce problème.
