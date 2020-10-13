---
title: MicrosoftEdge et MicrosoftDefenderApplicationGuard
ms.author: srugh
author: dan-wesley
manager: seanlyn
ms.date: 10/12/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Prise en charge de Microsoft Edge pour Microsoft Defender Application Guard
ms.openlocfilehash: fcf9bb6e36ddd5e014bd8176643554bfe3ff8fd4
ms.sourcegitcommit: b813f91803b8f0f27489634f49e7e0585b746d48
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2020
ms.locfileid: "11114362"
---
# Prise en charge de Microsoft Edge pour Microsoft Defender Application Guard

Cet article décrit comment Microsoft Edge prend en charge Microsoft Defender Application Guard (Application Guard).

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

## Vue d'ensemble

Les architectes de la sécurité au sein de l’entreprise doivent composer avec la tension qui existe entre la productivité et la sécurité. Il est relativement simple de verrouiller un navigateur et de n’autoriser que quelques sites approuvés à se charger. Cette approche permet d’améliorer la sécurité de manière globale, mais elle est vraisemblablement moins productive. Si vous prenez des mesures moins restrictives pour améliorer la productivité, vous augmentez le profil de risque. Il est difficile de parvenir à un équilibre!

Il est encore plus difficile de face aux menaces émergentes dans ce contexte de menaces en constante évolution. Les navigateurs restent la surface d’attaque principale des appareils clients, car la fonction de base d’un navigateur est de permettre aux utilisateurs d’accéder, télécharger et ouvrir du contenu non approuvé à partir de sources non fiables. Les acteurs malveillants œuvrent en permanence pour créer de nouvelles formes d’attaques d’ingénierie sociale contre le navigateur. La prévention des incidents de sécurité ou les stratégies de détection/réponse ne peuvent pas garantir une sécurité à 100%.

Une stratégie de sécurité clé à prendre en considération est d’[Adopter une méthodologie de violation](https://docs.microsoft.com/office365/Enterprise/office-365-monitoring-and-testing#assume-breach-methodology), ce qui signifie que l’on accepte l’idée qu’une attaque aboutisse au moins une fois, quels que soient les efforts déployés pour l’empêcher. Cette façon de penser exige l’élaboration de défenses pour limiter les dommages, ce qui garantit que le réseau de l’entreprise et d’autres ressources restent protégés dans ce scénario.  Le déploiement d’Application Guard pour Microsoft Edge s’inscrit parfaitement dans cette stratégie.

## À propos d’ApplicationGuard

Conçu pour Windows10 et Microsoft Edge, Application Guard utilise une approche d’isolation du matériel. Cette approche autorise le lancement de sites non approuvés à l’intérieur d’un conteneur lors de la navigation. L’isolation du matériel permet aux entreprises de protéger leur réseau et leurs données en cas de visite par un utilisateur d’un site compromis ou malveillant.

L’administrateur d’entreprise définit les sites approuvés, les ressources de cloud et les réseaux internes. Tout ce qui n’apparaît pas dans la liste des sites de confiance est considéré comme non fiable. Ces sites sont isolés du réseau et des données de l’entreprise sur l’appareil de l’utilisateur.

Pour obtenir plus d’informations, consultez [Qu’est-ce qu’ApplicationGuard et comment fonctionne-t-il?](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview#what-is-application-guard-and-how-does-it-work).

La capture d’écran suivante affiche un exemple de message de l’Application Guard montrant que l’utilisateur navigue dans un espace sécurisé.

![Message de parcours sécurisé de l’Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-1.png)

## Nouveautés

La prise en charge d’Application Guard dans le nouveau navigateur Microsoft Edge dispose d’une parité fonctionnelle avec Microsoft Edge Legacy et inclut plusieurs améliorations.

### Prise en charge de l’extension dans le conteneur

La prise en charge d’extension dans le conteneur a été l’une des principales demandes de la part des clients. Les scénarios vont de la possibilité d’exécuter des bloqueurs de publicités à l’intérieur du conteneur pour améliorer les performances d’un navigateur jusqu’à la possibilité d’exécuter des extensions personnalisées dans le conteneur.

Les installations d’extension dans le conteneur sont désormais prises en charge, à partir de MicrosoftEdge version81. Cette prise en charge peut être contrôlée par l’intermédiaire d’une stratégie. La `updateURL` utilisée dans la stratégie [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) doit être ajoutée en tant que ressources neutres dans les stratégies d’isolement réseau utilisées par Application Guard.

Voici quelques exemples de scénarios de prise en charge du conteneur:

- Forcer l’installation d’une extension sur l’hôte
- Suppression d’une extension dans l’hôte
- Extensions bloquées sur l’hôte

> [!NOTE]
> Il est également possible d’installer manuellement des extensions individuelles dans le conteneur à partir du magasin d’extension. Les extensions installées manuellement persisteront dans le conteneur uniquement lorsque la stratégie [Autoriser la persistance](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard#application-specific-settings) est activée.

### Identification du trafic Application Guard via un proxy double

Certains clients d’entreprise déploient Application Guard avec un cas d’utilisation spécifique où ils doivent identifier le trafic web sortant d’un conteneur Microsoft Defender Application Guard au niveau du proxy. À partir du canal stable version84, Microsoft Edge prend en charge le serveur proxy double pour répondre à cette exigence. Vous pouvez configurer cette fonctionnalité à l’aide de la stratégie [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy) .

Le schéma suivant illustre l’architecture double proxy pour Microsoft Edge.

![Architecture de proxy double pour Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-dual-proxy.png)

### Page Diagnostics pour la résolution de problèmes

L’autre difficulté d’un utilisateur est de résoudre les problèmes de configuration d’Application Guard sur un appareil lorsqu’un problème est signalé. Microsoft Edge dispose d’une page de diagnostics (`edge://application-guard-internals`) pour résoudre les problèmes rencontrés par les utilisateurs. L’un de ces diagnostics est en mesure de vérifier le degré de confiance d’une URL en fonction de la configuration sur l’appareil de l’utilisateur.

La capture d’écran suivante affiche une page de diagnostic avec plusieurs onglets pour vous permettre de diagnostiquer les problèmes de l’appareil signalés par les utilisateurs.

![Page de diagnostic d’Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-2.png)

### Mises à jour de Microsoft Edge dans le conteneur

Les mises à jour de la version héritée de Microsoft Edge dans le conteneur font partie du cycle de mise à jour du système d’exploitation Windows. Les mises à jour de la nouvelle version de Microsoft Edge s’opérant indépendamment du système d’exploitation Windows, il n’existe plus de dépendance sur les mises à jour de conteneur. Le canal et la version de l’hôte Microsoft Edge sont répliqués dans le conteneur.

## Conditions préalables

Les conditions suivantes s’appliquent aux appareils utilisant Application Guard avec Microsoft Edge:

- Windows101809 (RS5) et versions ultérieures.
- Uniquement les références SKU client Windows

  > [!NOTE]
  > Application Guard est uniquement pris en charge sur les références SKU Windows10 Professionnel et Windows10 Entreprise.

- Une des solutions de gestion est décrite dans la section [Configuration logicielle](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard#software-requirements)

## Comment installer Application Guard

Les articles suivants fournissent les informations nécessaires pour installer, configurer et tester Application Guard avec Microsoft Edge.

- [Configuration requise](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard)
- [Installer Microsoft Defender Application Guard](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard)
- [Configurer les paramètres de stratégie de groupe Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard)
- [Tester ApplicationGuard](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/test-scenarios-md-app-guard)

## Forum Aux Questions

### Est-ce que application Guard fonctionne en mode Internet Explorer?

Le mode IE prend en charge les fonctionnalités d’Application Guard, mais nous ne prévoyons pas l’utilisation de cette fonctionnalité en mode IE. Le mode IE est recommandé pour être déployé pour une liste de sites internes approuvés, tandis qu’Application Guard s’applique aux sites non approuvés uniquement. Assurez-vous que tous les sites ou adresses IP en mode IE sont également ajoutés à la stratégie d’isolement réseau afin qu’ils soient considérés comme des ressources approuvées par Application Guard.

### Ai-je besoin d’installer l’extension Chrome d’Application Guard?

Non, la fonctionnalité Application Guard est nativement prise en charge dans Microsoft Edge. En effet, l’extension Chrome d’Application Guard n’est pas une configuration prise en charge dans Microsoft Edge.

### Y a-t-il d’autres forums aux questions liés à cette plateforme?

Oui. [Forum aux questions - MicrosoftDefenderApplicationGuard](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/faq-md-app-guard) 

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Microsoft Defender-Protection avancée contre les menaces](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [Vidéo: isolation du navigateur Microsoft Edge avec Application Guard](https://www.youtube.com/watch?v=zQjaRqNXMqw&t=3s)
