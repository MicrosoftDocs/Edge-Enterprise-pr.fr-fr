---
title: Microsoft Edge et Microsoft Defender Application Guard
ms.author: srugh
author: AndreaLBarr
manager: seanlyn
ms.date: 05/06/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Prise en charge de Microsoft Edge pour Microsoft Defender Application Guard
ms.openlocfilehash: 7374810eb19ada298963817844e52184c0271a8c
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617994"
---
# <a name="microsoft-edge-support-for-microsoft-defender-application-guard"></a>Prise en charge de Microsoft Edge pour Microsoft Defender Application Guard

Cet article décrit comment Microsoft Edge prend en charge Microsoft Defender Application Guard (Application Guard).

> [!NOTE]
> Cet article concerne Microsoft Edge version 77 ou ultérieure.

## <a name="overview"></a>Vue d'ensemble

Les architectes de la sécurité au sein de l’entreprise doivent composer avec la tension qui existe entre la productivité et la sécurité. Il est relativement simple de verrouiller un navigateur et de n’autoriser que quelques sites approuvés à se charger. Cette approche permet d’améliorer la sécurité de manière globale, mais elle est vraisemblablement moins productive. Si vous prenez des mesures moins restrictives pour améliorer la productivité, vous augmentez le profil de risque. Il est difficile de parvenir à un équilibre !

Il est encore plus difficile de face aux menaces émergentes dans ce contexte de menaces en constante évolution. Les navigateurs restent la surface d’attaque principale des appareils clients, car la fonction de base d’un navigateur est de permettre aux utilisateurs d’accéder, télécharger et ouvrir du contenu non approuvé à partir de sources non fiables. Les acteurs malveillants œuvrent en permanence pour créer de nouvelles formes d’attaques d’ingénierie sociale contre le navigateur. La prévention des incidents de sécurité ou les stratégies de détection/réponse ne peuvent pas garantir une sécurité à 100 %.

Une stratégie de sécurité clé à prendre en considération est d’[Adopter une méthodologie de violation](/office365/Enterprise/office-365-monitoring-and-testing#assume-breach-methodology), ce qui signifie que l’on accepte l’idée qu’une attaque aboutisse au moins une fois, quels que soient les efforts déployés pour l’empêcher. Cette façon de penser exige l’élaboration de défenses pour limiter les dommages, ce qui garantit que le réseau de l’entreprise et d’autres ressources restent protégés dans ce scénario.  Le déploiement d’Application Guard pour Microsoft Edge s’inscrit parfaitement dans cette stratégie.

## <a name="about-application-guard"></a>À propos d’Application Guard

Conçu pour Windows 10 et Microsoft Edge, Application Guard utilise une approche d’isolation du matériel. Cette approche autorise le lancement de sites non approuvés à l’intérieur d’un conteneur lors de la navigation. L’isolation du matériel permet aux entreprises de protéger leur réseau et leurs données en cas de visite par un utilisateur d’un site compromis ou malveillant.

L’administrateur d’entreprise définit les sites approuvés, les ressources de cloud et les réseaux internes. Tout ce qui n’apparaît pas dans la liste des sites de confiance est considéré comme non fiable. Ces sites sont isolés du réseau et des données de l’entreprise sur l’appareil de l’utilisateur.

Pour plus d'informations :

- regardez notre vidéo [Isolation du navigateur Microsoft Edge à l'aide d'Application Guard](microsoft-edge-video-security-application-guard.md)
- lisez [Qu’est-ce qu’Application Guard et comment fonctionne-t-il ?](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview#what-is-application-guard-and-how-does-it-work)

La capture d’écran suivante affiche un exemple de message de l’Application Guard montrant que l’utilisateur navigue dans un espace sécurisé.

![Message de parcours sécurisé de l’Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-1.png)

## <a name="whats-new"></a>Nouveautés

La prise en charge d’ApplicationGuard dans le nouveau navigateur MicrosoftEdge dispose d’une parité fonctionnelle avec l’Ancienne version de MicrosoftEdge et inclut plusieurs améliorations.

### <a name="favorites-synchronizing-from-the-host-to-the-container"></a>Synchronisation des favoris à partir de l’hôte dans le conteneur

Certains de nos clients ont demandé la synchronisation des favoris entre le navigateur hôte et le conteneur dans ApplicationGuard. À partir Microsoft Edge version91, les utilisateurs ont désormais la possibilité de configurer ApplicationGuard pour synchroniser leurs favoris entre l’hôte et le conteneur. Cela garantit que les nouveaux favoris apparaissent également sur le conteneur.

Cette prise en charge peut être contrôlée par l’intermédiaire d’une stratégie. Vous pouvez mettre à jour la stratégie Edge [ApplicationGuardFavoritesSyncEnabled](/deployedge/microsoft-edge-policies#applicationguardfavoritessyncenabled) pour activer ou désactiver la synchronisation des favoris.

> [!Note]
> Pour des raisons de sécurité, la synchronisation des favoris est uniquement possible à partir de l’hôte vers le conteneur et non dans l’autre sens. Pour garantir une liste unifiée des favoris sur l’hôte et le conteneur, nous avons désactivé la gestion des favoris à l’intérieur du conteneur.

### <a name="identify-network-traffic-originating-from-the-container"></a>Identifier le trafic réseau provenant du conteneur

Plusieurs clients utilisent WDAG dans une configuration spécifique où ils souhaitent identifier le trafic réseau provenant du conteneur. Voici quelques exemples de scénarios:

- Pour restreindre l’accès à quelques sites non confiance uniquement
- Pour autoriser l’accès à Internet à partir du conteneur uniquement

À partir de Microsoft Edge version91, la prise en charge intégrée permet de baliser le trafic réseau provenant de conteneurs ApplicationGuard, ce qui permet aux entreprises d’utiliser un proxy pour filtrer le trafic et appliquer des stratégies spécifiques. Vous pouvez utiliser l’en-tête pour identifier le trafic qui passe par le conteneur ou l’hôte à l’aide de [ApplicationGuardTrafficIdentificationEnabled](/deployedge/microsoft-edge-policies#applicationguardtrafficidentificationenabled).

### <a name="extension-support-inside-the-container"></a>Prise en charge de l’extension dans le conteneur

La prise en charge d’extension dans le conteneur a été l’une des principales demandes de la part des clients. Les scénarios vont de la possibilité d’exécuter des bloqueurs de publicités à l’intérieur du conteneur pour améliorer les performances d’un navigateur jusqu’à la possibilité d’exécuter des extensions personnalisées dans le conteneur.

Les installations d’extension dans le conteneur sont désormais prises en charge, à partir de Microsoft Edge version 81. Cette prise en charge peut être contrôlée par l’intermédiaire d’une stratégie. La `updateURL` utilisée dans la stratégie [ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist) doit être ajoutée en tant que ressources neutres dans les stratégies d’isolement réseau utilisées par Application Guard.

Voici quelques exemples de scénarios de prise en charge du conteneur :

- Forcer l’installation d’une extension sur l’hôte
- Suppression d’une extension dans l’hôte
- Extensions bloquées sur l’hôte

> [!NOTE]
> Il est également possible d’installer manuellement des extensions individuelles dans le conteneur à partir du magasin d’extension. Les extensions installées manuellement persisteront dans le conteneur uniquement lorsque la stratégie [Autoriser la persistance](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard#application-specific-settings) est activée.

### <a name="identifying-application-guard-traffic-via-dual-proxy"></a>Identification du trafic Application Guard via un proxy double

Certains clients d’entreprise déploient Application Guard avec un cas d’utilisation spécifique où ils doivent identifier le trafic web sortant d’un conteneur Microsoft Defender Application Guard au niveau du proxy. À partir du canal stable version 84, Microsoft Edge prend en charge le serveur proxy double pour répondre à cette exigence. Vous pouvez configurer cette fonctionnalité à l’aide de la stratégie [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy) .

Le schéma suivant illustre l’architecture double proxy pour Microsoft Edge.

![Architecture de proxy double pour Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-dual-proxy.png)

### <a name="diagnostic-page-for-troubleshooting"></a>Page Diagnostics pour la résolution de problèmes

L’autre difficulté d’un utilisateur est de résoudre les problèmes de configuration d’Application Guard sur un appareil lorsqu’un problème est signalé. Microsoft Edge dispose d’une page de diagnostics (`edge://application-guard-internals`) pour résoudre les problèmes rencontrés par les utilisateurs. L’un de ces diagnostics est en mesure de vérifier le degré de confiance d’une URL en fonction de la configuration sur l’appareil de l’utilisateur.

La capture d’écran suivante affiche une page de diagnostic avec plusieurs onglets pour vous permettre de diagnostiquer les problèmes de l’appareil signalés par les utilisateurs.

![Page de diagnostic d’Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-2.png)

### <a name="microsoft-edge-updates-in-the-container"></a>Mises à jour de Microsoft Edge dans le conteneur

Les mises à jour de la version héritée de Microsoft Edge dans le conteneur font partie du cycle de mise à jour du système d’exploitation Windows. Les mises à jour de la nouvelle version de Microsoft Edge s’opérant indépendamment du système d’exploitation Windows, il n’existe plus de dépendance sur les mises à jour de conteneur. Le canal et la version de l’hôte Microsoft Edge sont répliqués dans le conteneur.

## <a name="prerequisites"></a>Conditions préalables

Les conditions suivantes s’appliquent aux appareils utilisant Application Guard avec Microsoft Edge :

- Windows 10 1809 (RS5) et versions ultérieures.
- Uniquement les références SKU client Windows

  > [!NOTE]
  > Application Guard est uniquement pris en charge sur les références SKU Windows 10 Professionnel et Windows 10 Entreprise.

- Une des solutions de gestion est décrite dans la section [Configuration logicielle](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard#software-requirements)

## <a name="how-to-install-application-guard"></a>Comment installer Application Guard

Les articles suivants fournissent les informations nécessaires pour installer, configurer et tester Application Guard avec Microsoft Edge.

- [Configuration requise](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard)
- [Installer Microsoft Defender Application Guard](/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard)
- [Configurer les paramètres de stratégie de groupe Microsoft Defender](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard)
- [Tester Application Guard](/windows/security/threat-protection/microsoft-defender-application-guard/test-scenarios-md-app-guard)

## <a name="frequently-asked-questions"></a>Forum Aux Questions

### <a name="does-application-guard-work-in-ie-mode"></a>ApplicationGuard fonctionne-t-elle en mode InternetExplorer?

Le mode InternetExplorer prend en charge les fonctionnalités d’ApplicationGuard, mais nous ne prévoyons pas une utilisation importante de cette fonctionnalité en mode InternetExplorer. Il est recommandé de déployer le mode InternetExplorer pour une liste de sites internes de confiance, et ApplicationGuard pour les sites non approuvés uniquement. Assurez-vous que tous les sites ou adresses IP en mode IE sont également ajoutés à la stratégie d’isolement réseau afin qu’ils soient considérés comme des ressources approuvées par Application Guard.

### <a name="do-i-need-to-install-the-application-guard-chrome-extension"></a>Ai-je besoin d’installer l’extension Chrome d’Application Guard ?

Non, la fonctionnalité Application Guard est nativement prise en charge dans Microsoft Edge. En effet, l’extension Chrome d’Application Guard n’est pas une configuration prise en charge dans Microsoft Edge.

### <a name="are-there-any-other-platform-related-faqs"></a>Y a-t-il d’autres forums aux questions liés à cette plateforme ?

Oui. [Forum aux questions - Microsoft Defender Application Guard](/windows/security/threat-protection/microsoft-defender-application-guard/faq-md-app-guard) 

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Microsoft Defender - Protection avancée contre les menaces](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [Vidéo : isolation du navigateur Microsoft Edge avec Application Guard](https://www.youtube.com/watch?v=zQjaRqNXMqw&t=3s)