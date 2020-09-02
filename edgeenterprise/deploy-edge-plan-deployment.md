---
title: Planifier votre déploiement de MicrosoftEdge
ms.author: cjacks
author: appcompatguy
manager: saudm
ms.date: 04/23/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Planifier votre déploiement de MicrosoftEdge
ms.openlocfilehash: 3ac3d050578ca4f230ed7e775aefb73f11abb3c0
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979732"
---
# Planifier votre déploiement de MicrosoftEdge

Cet article décrit les pratiques recommandées pour le déploiement de MicrosoftEdge dans un environnement d’entreprise.

>[!NOTE]
>Cet article concerne MicrosoftEdge version77 ou ultérieure.

## Évaluer votre environnement de navigateur et vos besoins de navigateur existants

Prenez le temps de comprendre l’état actuel de votre navigateur et votre vision du projet pour vous assurer que toutes les parties prenantes du projet sont au diapason et qu’elles travaillent en vue du même objectif.

Commencez par définir votre état actuel:

- Quels navigateurs sont actuellement déployés dans votre environnement?
- Quel navigateur est défini comme navigateur par défaut?
- Avez-vous besoin d’utiliser Internet Explorer pour certaines de vos applications?
- Utilisez-vous une liste de sites en mode entreprise pour configurer Internet Explorer aujourd’hui?
- Quelles plateformes de système d’exploitation sont prises en charge dans votre environnement? (Windows10, macOS, Windows7, Windows Server, etc.)
- Quels outils de gestion utilisez-vous pour la gestion du navigateur?
- Qui est responsable de la configuration et de la gestion du navigateur?
- Quel est votre procédure de validation de la compatibilité du navigateur?

Une fois que vous avez pris connaissance de l’état actuel, vous pouvez déterminer les objectifs de votre choix pour le déploiement de votre navigateur, en tenant compte des éléments suivants:

- Souhaitez-vous [définir MicrosoftEdge comme navigateur par défaut](https://docs.microsoft.com/DeployEdge/edge-default-browser)?
- Voulez-vous masquer la version héritée de MicrosoftEdge ou souhaitez-vous la [laisser à disposition des utilisateurs?](https://docs.microsoft.com/DeployEdge/microsoft-edge-sysupdate-access-old-edge)
- Comment allez-vous [configurer MicrosoftEdge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge)?
- Quelles fonctionnalités est-il essentiel de configurer dans le cadre de votre déploiement initial?
- Quelle est la procédure de résolution d’éventuels problèmes de compatibilité ou de configuration identifiés?

Vous devez également connaître les **conditions préalables** pour les fonctionnalités qui vous intéressent, par exemple:

- [WindowsDefenderApplicationGuard](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-guard/reqs-wd-app-guard)
- [Mode InternetExplorer](https://docs.microsoft.com/DeployEdge/edge-ie-mode)
- [Authentification et synchronisation](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-identity)

Une fois que vous disposez de ces réponses, vous êtes prêt à planifier votre déploiement de MicrosoftEdge.
<!--bookmark -->

## Vous assurer que vos appareils Windows10 sont prêts

La dernière mise à jour cumulative (LCU) est requise pour le canal stable MicrosoftEdge à partir d’octobre2019 (ou version ultérieure). Si vous tentez le déploiement vers un appareil Windows10 contenant une ancienne LCU, l’installation échouera. Si vous souhaitez obtenir plus d’informations sur la LCU minimale à appliquer avant de déployer MicrosoftEdge, consultez [Mises à jour Windows pour prendre en charge la prochaine version de MicrosoftEdge](https://docs.microsoft.com/DeployEdge/microsoft-edge-sysupdate-windows-updates).

## Définir votre méthodologie de déploiement

Lorsque vous connaissez l’état final souhaité, vous pouvez commencer à planifier la façon d’y parvenir. Les deux principales façons de déployer MicrosoftEdge consistent à procéder par rôle et par site.

### Déployer vers les utilisateurs finaux par rôle

Si la compatibilité des applications est votre principale préoccupation et que vous n’avez pas de véritable emprise sur les applications à tester, vous pouvez envisager de déployer les utilisateurs finaux par rôle. Cela permet, à chaque vague d’un déploiement progressif, de recueillir des commentaires et des informations sur les applications dont la configuration peut être modifiée pour résoudre les problèmes de compatibilité.

### Déployer vers les utilisateurs finaux par site

Si la bande passante est votre principale préoccupation, vous pouvez envisager d’effectuer des tests de compatibilité des applications à l’avance. Après avoir terminé les tests, déployez vers les utilisateurs finaux par site pour pouvoir tirer profit de la mise en cache d’autres optimisations de la distribution de logiciels.

## Effectuer une détection du site

Si vous êtes dépendant des applications web héritées et que vous envisagez d’utiliser le mode Internet Explorer (ce que fait la plupart des clients), vous devrez probablement effectuer une découverte de site supplémentaire.

### Si vous avez déjà déployé et configuré la version héritée de MicrosoftEdge

Si vous avez déjà configuré votre liste de sites d’entreprise pour qu’elle fonctionne pour la version héritée de MicrosoftEdge, votre travail est presque terminé. La seule chose que vous devrez peut-être ajouter est les sites neutres.

Les sites neutres sont généralement des sites qui fournissent une authentification unique (SSO). Si vous accédez à un site neutre à partir de MicrosoftEdge, mieux vaut rester dans MicrosoftEdge pour vous authentifier. Si vous accédez à un site neutre en mode Internet Explorer, mieux vaut rester en mode InternetExplorer pour vous authentifier.

Identifiez les sites SSO (ou autres sites neutres) que vous utilisez et ajoutez-les à votre liste de sites d’entreprise.

### Si vous avez configuré Internet Explorer comme navigateur par défaut

Si vous utilisez actuellement Internet Explorer, vous ne savez peut-être pas quels sites ont été mis à niveau vers les normes web modernes qui nécessitent toujours Internet Explorer. Vous pouvez rechercher ces sites et les ajouter à la liste de sites d’entreprise. Cela vous permet d’utiliser le mode Internet Explorer uniquement sur les sites qui en ont besoin.

> [!TIP]
> Utilisez les outils de [recherche de sites d’entreprise](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery?redirectedfrom=MSDN) pour découvrir les sites qui peuvent nécessiter le mode Internet Explorer. Vous pouvez également collecter des données sur les ordinateurs exécutant Windows Internet Explorer8 à 11 sur Windows10, Windows8.1 ou Windows7.

### Analyser les données de détection de site

Une fois que vous avez collecté les données de site, nous recommandons d’utiliser la procédure en 4étapes suivante pour analyser les données:

1. Triez les données par domaine, puis par URL.
2. Définissez les limites d’une «application» à configurer pour le mode Internet Explorer. Vous pouvez inclure tous les sites et contrôles Web qui définissent l’application. En revanche, mieux vaut ne pas inclure de sites et de contrôles supplémentaires en définissant l’application trop largement. Certains sites peuvent être simples, comme «http://contoso.com/app1», mais d’autres peuvent nécessiter la définition de plusieurs sites et pages.
3. Testez l’application pour vérifier qu’elle ne fonctionne pas en mode natif. De nombreux sites proposent un contenu moderne lorsqu’ils détectent un navigateur moderne et n’offrent qu’un contenu hérité lorsqu’ils détectent Internet Explorer.
4. Ajoutez l’application à votre liste de sites d’entreprise en cas d’échec du test.

   > [!NOTE]
   > Il est recommandé de regrouper tous les sites qui composent une application. Si les sites doivent être utilisés pour accomplir une tâche et s’ils sont mis à jour ensemble, c’est une bonne indication qu’ils doivent être regroupés. Ainsi, lorsque vous mettez à niveau une application, il est plus facile de supprimer l’intégralité du site du mode Internet Explorer et de commencer à utiliser un navigateur moderne pour cette application.

## Déterminer votre stratégie de canal

MicrosoftEdge est publié dans [plusieurs canaux](https://docs.microsoft.com/DeployEdge/microsoft-edge-channels).

> [!NOTE]
> Vous pouvez installer plusieurs canaux sur un appareil

Le canal stable est celui que vous devez déployer sur la plupart des appareils. Toutefois, vous devez envisager une stratégie de déploiement qui comprend plusieurs appareils et plusieurs canaux.

### Plusieurs appareils et canaux

Nous recommandons de disposer d’un sous-ensemble représentatif d’appareils configurés pour utiliser le canal bêta. Cela vous permet d’avoir un aperçu des modifications à venir dans le navigateur. Vous pouvez voir si ces modifications vont affecter vos utilisateurs finaux ou vos applications.

Vous souhaiterez peut-être également rendre le canal Microsoft Edge Dev (ou même le canal Microsoft Edge Canary) disponible pour certains rôles, tels que les développeurs Web. Déterminez si vous souhaitez cibler certains appareils avec des canaux plus fluides et évoluant rapidement, ou si vous souhaitez simplement que ces canaux soient disponibles pour les utilisateurs qui choisissent de les installer.

Étant donné qu’il est possible d’installer plusieurs canaux sur un appareil, vous pouvez réduire le risque lié au test pour les utilisateurs qui ont choisi d’installer un canal de version préliminaire. Par exemple, si vous avez un utilisateur qui utilise le canal bêta et qu’un problème se produit, celui-ci peut basculer vers le canal stable et continuer à travailler. Cela le débloque jusqu’à ce que le problème soit résolu.

> [!NOTE]
> Si l’utilisateur a activé la synchronisation, sa configuration est synchronisée entre les canaux, ce qui facilite la transition entre les canaux.

## Définir et configurer des stratégies

Après avoir créé votre liste de sites d’entreprise, nous vous recommandons d’identifier et de configurer les stratégies que vous envisagez de déployer avec MicrosoftEdge. Cela permet de s’assurer que ces stratégies sont appliquées lorsque vous effectuez vos tests.

Tout d’abord, envisagez l’expérience de première utilisation que vos utilisateurs doivent avoir. Si vous souhaitez importer automatiquement les paramètres à partir du navigateur actuel, configurez la stratégie pour [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun).

Pour les stratégies de sécurité, nous vous recommandons de commencer par la ligne de base de sécurité de MicrosoftEdge. La ligne de base de sécurité peut être appliquée au moyen des [paramètres de ligne de base de configuration de la sécurité recommandée](https://techcommunity.microsoft.com/t5/Microsoft-Security-Baselines/Security-baseline-DRAFT-for-Chromium-based-Microsoft-Edge/ba-p/949991) ou grâce à [MicrosoftIntune](https://docs.microsoft.com/intune/protect/security-baseline-settings-edge).

Pour les autres stratégies, nous vous recommandons de consulter les configurations de stratégie pour [Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-policies) et les mises à jour [Microsoft Edge Update](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies).

### Définir votre stratégie et vos règles de mise à jour

Vous souhaitez également déterminer la façon dont vous souhaitez effectuer les mises à jour après avoir déployé MicrosoftEdge:

- **Autoriser MicrosoftEdge à se mettre à jour automatiquement** (option par défaut). Si vous choisissez d’autoriser les mises à jour automatiques de MicrosoftEdge, celui-ci sera mis à jour automatiquement à la fréquence déterminée par les canaux que vous avez déployés.
- **Mettre à jour Microsoft Edge à votre rythme**. Si vous préférez avoir le contrôle explicite sur le moment où les mises à jour sont déployées, vous pouvez désactiver les mises à jour automatiques et les déployer vous-même (consultez la [Référence de stratégie de mise à jour](https://docs.microsoft.com/DeployEdge/microsoft-edge-update-policies)). Après avoir désactivé les mises à jour automatiques, vous pouvez déployer des mises à jour pour chaque canal à l’aide de l’un des outils suivants:

- [Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)
- [Configuration Manager](https://docs.microsoft.com/DeployEdge/deploy-edge-with-configuration-manager)
- l’outil de déploiement de votre choix.

Quelle que soit votre stratégie de mise à jour, nous vous recommandons d’adopter une stratégie de déploiement en boucle. Avec les mises à jour automatiques, cela implique de faire appel à un échantillon représentatif d’utilisateurs exécutant le canal bêta, afin d’identifier les problèmes affectant ce qui deviendra le canal stable. Avec les mises à jour manuelles, cela peut également comprendre une validation supplémentaire d’un groupe pilote après la publication d’une nouvelle build du canal stable. Cette étape est suivie d’un déploiement à grande échelle.

>[!NOTE]
>La prise en charge de MicrosoftEdge s’applique uniquement à la version la plus récente de MicrosoftEdge dans chaque canal

## Effectuer des tests de compatibilité des applications

La compatibilité des applications pour MicrosoftEdge est extrêmement élevée, à tel point que Microsoft s’engage à assurer les compatibilités suivantes:

1. Si elle fonctionne sur MicrosoftEdge *version45 et antérieure*, elle fonctionnera sur MicrosoftEdge *version77 et ultérieures*.
2. Si elle fonctionne sur Internet Explorer, elle fonctionnera sur MicrosoftEdge en mode InternetExplorer.
3. Si elle fonctionne sur Google Chrome, elle fonctionnera sur MicrosoftEdge.

Si vous possédez d’une application où nous ne répondons pas à cet engagement, nous résoudrons le problèmes avec [Microsoft App Assure](https://www.microsoft.com/fasttrack/microsoft-365/desktop-app-assure).

Malgré cet engagement, nous savons que de nombreuses organisations doivent valider certaines applications pour leurs propres raisons de conformité ou de gestion des risques. Même si cette procédure est très simple, il est important d’être organisé et rigoureux lors des tests d’applications.

Il existe deux façons d’effectuer des tests de compatibilité des applications:

1. Tests en laboratoire. Les applications sont validées dans un environnement étroitement contrôlé avec des configurations spécifiques.
2. Test pilote. Les applications sont validées par un nombre limité d’utilisateurs dans leur environnement de travail quotidien à l’aide de leurs propres appareils.

Choisissez la méthode qui convient le mieux à chaque application pour gérer les risques sans surinvestissement dans les tests de compatibilité.

## Déployer MicrosoftEdge vers un groupe pilote

Après avoir défini vos stratégies et réalisé le test de compatibilité des applications initial, vous êtes prêt à effectuer le déploiement vers votre groupe pilote. Déployez dans votre groupe pilote à l’aide de l’un des outils suivants:

- [Microsoft Intune for Windows](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json) ou [Microsoft Intune for macOS](https://docs.microsoft.com/intune/apps/apps-edge-macos?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)
- [Configuration Manager](https://docs.microsoft.com/DeployEdge/deploy-edge-with-configuration-manager).
- Un autre outil de gestion, téléchargez et déployez le [fichier MSI pour MicrosoftEdge](https://www.microsoftedgeinsider.com/enterprise).

## Valider votre déploiement

Après avoir déployé votre pilote, vous devez capturer tous les commentaires que vous envoient vos utilisateurs.

- Capturez les commentaires concernant la compatibilité. Identifiez les sites qui figurent sur la liste de sites d’entreprise qui n’ont pas été identifiés lors de la détection du site.
- Capturez les commentaires concernant la configuration de stratégie. Assurez-vous que les utilisateurs peuvent utiliser les fonctionnalités clés et effectuer leur travail tout en suivant les recommandations de sécurité.
- Capturez vos commentaires sur la facilité d’utilisation et les nouvelles fonctionnalités. Identifiez les domaines dans lesquels une formation doit être mise au point et proposée en fonction des questions de l’utilisateur.

## Déploiement large de MicrosoftEdge

Après avoir terminé le projet pilote et mis à jour votre plan de déploiement avec les leçons tirées du projet pilote, vous êtes prêt à effectuer un déploiement complet de MicrosoftEdge à tous vos utilisateurs.  Félicitations!

## Articles associés

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Vidéo: Déployer Microsoft Edge](microsoft-edge-video-deploy.md)

