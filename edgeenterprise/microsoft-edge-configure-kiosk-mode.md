---
title: Configurer Microsoft Edge en mode plein écran
ms.author: aguta
author: aguta
manager: srugh
ms.date: 10/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer Microsoft Edge en mode plein écran
ms.openlocfilehash: 799b3dd4b7fc96f0b8e5cb718bca98fd4f38ec15
ms.sourcegitcommit: 78905f66f4a6590a57c8f2bf808af92106b62996
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/05/2020
ms.locfileid: "11094861"
---
# Configurer Microsoft Edge en mode plein écran

Cet article décrit la configuration des options Microsoft Edge en mode plein écran que vous pouvez piloter. Il existe également une feuille de route des fonctionnalités que nous mettons en cible.

> [!NOTE]
> Cet article concerne MicrosoftEdge version87 ou ultérieure.

## Vue d'ensemble

Microsoft Edge en mode plein écran offre deux expériences de verrouillage du navigateur afin de permettre aux organisations de créer, gérer et offrir une expérience optimale pour leurs clients. Les expériences de verrouillage suivantes sont disponibles:  

- L’expérience de signalement numérique/interactif affiche un site spécifique en mode plein écran.
- L’expérience de navigation publique exécute une version multi-onglet limitée de Microsoft Edge.

Les deux expériences exécutent une session Microsoft Edge InPrivate qui protège les données de l’utilisateur.

## Configurer Microsoft Edge en mode plein écran

Un groupe initial de fonctionnalités du mode plein écran est désormais disponible pour tester avec le canal Microsoft Edge Canary (version87). Vous pouvez télécharger Microsoft Edge Canary à partir de la page [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) .

### Fonctionnalités du mode plein écran

Les composants suivants sont disponibles:

- La navigation InPrivate protège les données des utilisateurs en supprimant les données du navigateur et les téléchargements à la fin de la session.
- Stratégie permettant de configurer la fonctionnalité Supprimer les téléchargements à la fermeture.
- Option permettant de réinitialiser une session utilisateur après une certaine période d’inactivité.
- Ensemble initial de fonctionnalités de verrouillage. Les fonctions suivantes sont disponibles:

  - Menu contextuel de la souris
  - F12: outils de développement
  - F11: quitter le mode plein écran (en mode plein écran)
  - Blocage du groupe initial des pages *Edge://*

> [!NOTE]
> Lorsque le mode plein écran évolue, d’autres fonctionnalités sont disponibles.

## Utiliser les fonctionnalités du mode plein écran

Vous pouvez appeler les fonctionnalités de Microsoft Edge en mode plein écran grâce aux options de ligne de commande suivantes de Windows10 :

- Signalisation numérique/interactive du mode plein écran `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- Navigation publique en mode plein écran: `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### Autres options de la ligne de commande

- `--no-first-run` : désactivez la première expérience d’exécution de Microsoft Edge.
- `--kiosk-idle-timeout-minutes` : modifiez l’heure (en minutes) de la dernière activité d’utilisateur avant la réinitialisation de la session de l’utilisateur par la version du mode plein écran de MicrosoftEdge. Les valeurs suivantes sont prises en charge:

  - Valeurs par défaut
    - Plein écran: désactivé
    - Navigation publique: 5minutes
  - Valeurs autorisées
    - 0: désactive le minuteur
    - 1-1440 minutes pour la réinitialisation du minuteur d’inactivité

## MicrosoftEdge avec accès affecté

### Borne à application unique

Microsoft Edge prend actuellement en charge un sous-ensemble des mêmes types de mode plein écran de l’ancienne version de Microsoft Edge pour un accès attribué à une application unique avec les expériences de verrouillage, la signalisation numérique/interactive et la navigation publique ci-après.  

Le mode plein écran avec accès attribué est actuellement disponible pour le test avec la version la plus récente de la  [version d'évaluation Windows10Insider](https://insider.windows.com/), version 20215 ou ultérieure, et avec le  [canal de développement Microsoft Edge](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 ou ultérieure.

**Comment puis-je obtenir l’aperçu de Windows Insider?**

Si vous souhaitez en savoir plus sur l’installation d’une version d'évaluation de Windows10 Insider sur un PC, veuillez consulter les instructions de la rubrique  [Prise en main des versions d'évaluation de Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).

### Borne à plusieurs applications

Vous pouvez exécuter MicrosoftEdge avec un [accès attribué à plusieurs applications](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) sous Windows10. Cela équivaut au type de mode plein écran «Navigation normale» de l’ancienne version de Microsoft Edge . Pour configurer MicrosoftEdge avec accès affecté à plusieurs applications, suivez les instructions sur la façon de [Configurer une borne à plusieurs applications](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). (L’AUMID du canal stable de MicrosoftEdge est **MSEdge**).

Configurer le mode plein écran de Microsoft Edge
Lorsque vous utilisez MicrosoftEdge avec accès attribué à plusieurs applications, vous pouvez utiliser les [stratégies de navigateur MicrosoftEdge](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) pour configurer l’expérience de navigation en fonction de vos besoins spécifiques.

### Configurer à l’aide des paramètres Windows

Les paramètres Windows constituent le moyen le plus simple de configurer un ou deux appareils borne à une seule application. Procédez comme suit pour configurer un ordinateur borne à une seul application.

1. Installez la version la plus récente de Windows10 Insider Preview, version 20215 ou ultérieure. Suivez les instructions de [Prise en main des versions d'évaluation de Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).
2. Installez la dernière version du [canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), 87.0.644.4 ou une version ultérieure.

   > [!IMPORTANT]
   > Une installation au niveau des appareils étant requise, seul un canal non-Canary est pris en charge.

3. Sur l’ordinateur borne, ouvrez Paramètres Windows, puis tapez «borne» dans le champ de recherche. Sélectionnez  **Configurer une borne (accès attribué)**, illustré dans la capture d’écran suivante pour ouvrir la boîte de dialogue de création de la borne.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurer la borne avec l’accès attribué":::

4. Sur la page **Configurer une borne** , cliquez sur  **Prise en main**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Configurer la borne avec l’accès attribué":::

5. Tapez un nom pour créer un nouveau compte borne ou sélectionnez un compte existant dans la liste déroulante rempli, puis cliquez sur **Suivant**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Configurer la borne avec l’accès attribué":::

6. Dans la page **Choisir une application borne** , sélectionnez **Microsoft Edge**, puis cliquez sur  **Suivant**.

   > [!NOTE]
   > Cela s’applique uniquement aux canaux Microsoft Edge dev, Beta et stable.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Configurer la borne avec l’accès attribué":::

7. Sélectionnez l’une des options suivantes pour l’affichage de Microsoft Edge en mode plein écran:

   - Connexion numérique/interactive: affiche un site spécifique en mode plein écran, exécutant Microsoft Edge.
   - Navigateur public: exécute une version multi-onglet limitée de Microsoft Edge.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Configurer la borne avec l’accès attribué":::

8. Sélectionnez **Suivant**.
9. Tapez l’URL à charger lors du lancement du kiosque.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Configurer la borne avec l’accès attribué":::

10. Acceptez la valeur par défaut de 5 minutes pour le temps d’inactivité ou indiquez la valeur de votre choix.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Configurer la borne avec l’accès attribué":::

11. Cliquez sur  **Suivant**.
12. Fermez la fenêtre  **Paramètres**  pour enregistrer et appliquer vos choix.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Configurer la borne avec l’accès attribué":::

13. Redémarrez l’appareil borne et connectez-vous avec le compte borne local pour valider la configuration.

## Limitations fonctionnelles

Avec la publication de cette version d’évaluation du mode plein écran, nous continuons à travailler sur l’amélioration du produit et en ajoutant de nouvelles fonctionnalités.

Bien que le mode plein écran ne prenne pas en charge les fonctionnalités suivantes, le travail est actuellement en cours sur les fonctionnalités suivantes:

- Regroupements
- Extensions
- Mode InternetExplorer
- WindowsDefenderApplicationGuard (WDAG)

## Feuille de route

### Plus tard cette année (2020)

Nous allons ajouter les fonctionnalités suivantes:

- Bouton terminer la session
- Barre d’adresse en lecture seule  
  - Configurable avec une stratégie de groupe
  - Lorsque cette option est activée, les utilisateurs ne peuvent pas modifier la barre d’adresse, ni accéder à une autre page.

- Autres fonctions de verrouillage:

  - Les accélérateurs supplémentaires sont bloqués (par exemple, CTRL + N).
  - Le menu paramètres «...» permet d’activer uniquement les options requises (par exemple, imprimer, aide, commentaires et lire à haute voix)
  - Verrouillage des pages supplémentaires *edge://* (par exemple, *edge://settings*)
  - Configurer l’interface utilisateur des options d’impression
  - Limiter l’Explorateur de fichiers au dossier de téléchargement uniquement.

### Début 2021

Nous allons ajouter la prise en charge et les fonctionnalités suivantes:

- Disponibilité générale de Microsoft Edge en mode plein écran avec accès affecté à une seule application sur Windows.
- Fonctionnalités supplémentaires pour la parité avec l’Ancienne version de Microsoft Edge.
- Intégration avec Intune pour configurer les appareils à l’aide d’un profil en mode plein écran UX.

## Voir également

- [Configurer des bornes et enseignes numériques dans les éditions Windows de bureau](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Déployer la version héritée du mode plein écran de MicrosoftEdge](https://aka.ms/edgekioskmode)
- [Planifier votre déploiement de MicrosoftEdge](deploy-edge-plan-deployment.md)
- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
