---
title: Configurer Microsoft Edge en mode plein écran
ms.author: aguta
author: aguta
manager: srugh
ms.date: 01/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer Microsoft Edge en mode plein écran
ms.openlocfilehash: be353a0e13e9234de40296a2e8dcc31b1b800f52
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297470"
---
# Configurer Microsoft Edge en mode plein écran

Cet article décrit la configuration des options Microsoft Edge en mode plein écran que vous pouvez piloter. Il existe également une feuille de route des fonctionnalités que nous ciblons.

> [!NOTE]
> Cet article concerne MicrosoftEdge version87 ou ultérieure.

## Vue d'ensemble

Microsoft Edge en mode plein écran offre deux expériences de verrouillage du navigateur afin de permettre aux organisations de créer, gérer et offrir une expérience optimale pour leurs clients. Les expériences de verrouillage suivantes sont disponibles:  

- **Expérience de connexion numérique/interactive** : affiche un site spécifique en mode plein écran.
- **Expérience de navigation publique** : exécute une version multi-onglet limitée de MicrosoftEdge.

Les deux expériences exécutent une session MicrosoftEdge InPrivate qui protège les données de l’utilisateur.

## Configurer MicrosoftEdge en mode plein écran

Un ensemble initial de fonctionnalités du mode plein écran est disponible pour le test avec le canal stable MicrosoftEdge, version87. Vous pouvez télécharger la dernière version à partir [de MicrosoftEdge (canal stable officiel).](https://www.microsoft.com/edge)

### Fonctionnalités prise en charge en mode plein écran

Le tableau suivant répertorie les fonctionnalités prises en charge par le mode plein écran.

|Fonctionnalité|Connexion numérique/interactive|Navigation publique|Disponible avec la version de MicrosoftEdge (et versions supérieures)|
|-|-|-|-|
|Navigation InPrivate|Y|Y|87|
|Réinitialiser en période d’inactivité|Y|Y|87|
|[Barre d’adresses en lecture seule](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (stratégie) |N|Y |87|
|[Supprimer les téléchargements à la sortie](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (stratégie)  | Y|Y |87|
|F11 bloqué (entrée/sortie en plein écran) | Y | Y | 87 |
|F12 bloqué (lancer les outils de développement) | Y | Y | 87 |
| Prise en charge de plusieurs onglets | N| Y| 87|
|Bouton Terminer la session | N| Y| 88|
|Toutes les URL MicrosoftEdge internes sont bloquées, à l’exception de *edge://downloads* et *edge://print* |N|Y|88|
| Ctrl+N bloqué (ouvrir une nouvelle fenêtre) | Y | Y | 89 |
| Ctrl+T bloqué (ouvrir un nouvel onglet) | N | Y | 89 |
|Paramètres et plus (...) afficheront uniquement les options requises  |N |Y |89 |

> [!NOTE]
> Lorsque le mode plein écran évolue, d’autres fonctionnalités sont disponibles.

## Utiliser les fonctionnalités du mode plein écran

Les fonctionnalités du mode plein écran de MicrosoftEdge peuvent être invoquées avec les options de ligne de commande Windows10 suivantes:

- Connexion numérique/interactive du mode plein écran: `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
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

## Stratégies de support pour le mode plein écran

Utilisez l’une des stratégies MicrosoftEdge répertoriées dans le tableau suivant pour améliorer l’expérience plein écran pour le type de mode plein écran MicrosoftEdge que vous configurez. Pour en savoir plus sur ces stratégies, voir [MicrosoftEdge – Référence de stratégie de navigateur.](https://docs.microsoft.com/deployedge/microsoft-edge-policies)

> [!NOTE]
> La configuration des stratégies n’est pas limitée aux stratégies répertoriées dans le tableau suivant, mais des stratégies supplémentaires doivent être testées pour s’assurer que les fonctionnalités du mode plein écran ne sont pas affectées.

|Stratégie de groupe|Connexion numérique/interactive|Navigation publique à application unique|
|--|--|--|
|[Impression](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | Y|Y |
|[HomePageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |N | Y|
|[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |N | Y|
|[NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |N |Y |
|[FavoritesBarEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |N |Y |
|[URLAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |Y |Y |
|[URLBlocklist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |Y | Y|
|[ManagedSearchEngines](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |N | Y|
|[UserFeedbackAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |N | Y|
|[VerticalTabsAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | N|Y |
|[Paramètres SmartScreen](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |Y |Y |

## MicrosoftEdge avec accès affecté

### Borne à application unique

MicrosoftEdge prend actuellement en charge un sous-ensemble des mêmes types de mode plein écran hérités de MicrosoftEdge pour l’accès affecté à une seule application avec les expériences de verrouillage suivantes: connexion numérique/interactive et navigation publique.  

Le mode plein écran avec accès attribué est actuellement disponible pour le test avec la version la plus récente de la  [version d'évaluation Windows10Insider](https://insider.windows.com/), version 20215 ou ultérieure, et avec le  [canal de développement Microsoft Edge](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 ou ultérieure.

**Comment puis-je obtenir l’aperçu de Windows Insider?**

Si vous souhaitez en savoir plus sur l’installation d’une version d'évaluation de Windows10 Insider sur un PC, veuillez consulter les instructions de la rubrique  [Prise en main des versions d'évaluation de Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).

### Borne à plusieurs applications

Vous pouvez exécuter MicrosoftEdge avec un [accès attribué à plusieurs applications](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) sous Windows10. Cela équivaut au type de mode plein écran «Navigation normale» de l’ancienne version de Microsoft Edge . Pour configurer MicrosoftEdge avec un accès affecté à plusieurs applications, suivez les instructions sur la configuration d’une borne [multi-application](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). (L’AUMID du canal stable de MicrosoftEdge est **MSEdge**).

Lorsque vous utilisez MicrosoftEdge avec un accès affecté à plusieurs applications, vous pouvez configurer MicrosoftEdge Kiosk pour utiliser les stratégies de navigateur[Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) afin de configurer l’expérience de navigation afin de répondre à vos besoins uniques.

### Configurer à l’aide des paramètres Windows

Les paramètres Windows constituent le moyen le plus simple de configurer un ou deux appareils borne à une seule application. Procédez comme suit pour configurer un ordinateur borne à une seul application.

1. Installez la version la plus récente de Windows10 Insider Preview, version 20215 ou ultérieure. Suivez les instructions de [Prise en main des versions d'évaluation de Windows10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).
2. Installez la dernière version du canal [stable MicrosoftEdge,](https://www.microsoft.com/edge)version 87 ou supérieure.  Pour tester les dernières fonctionnalités, vous pouvez télécharger le dernier [canal de développement Microsoft Edge,](https://www.microsoftedgeinsider.com/download)version89 ou supérieure.

   > [!IMPORTANT]
   > Une installation au niveau des appareils étant requise, seul un canal non-Canary est pris en charge.

3. Sur l’ordinateur borne, ouvrez Paramètres Windows, puis tapez «borne» dans le champ de recherche. Sélectionnez  **Configurer une borne (accès attribué)**, illustré dans la capture d’écran suivante pour ouvrir la boîte de dialogue de création de la borne.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurer la borne avec l’accès attribué":::

4. Sur la page **Configurer une borne** , cliquez sur  **Prise en main**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Page borne: prise en main":::

5. Tapez un nom pour créer un nouveau compte borne ou sélectionnez un compte existant dans la liste déroulante rempli, puis cliquez sur **Suivant**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Mode plein écran: créer un compte":::

6. Dans la page **Choisir une application borne** , sélectionnez **Microsoft Edge**, puis cliquez sur  **Suivant**.

   > [!NOTE]
   > Cela s’applique uniquement aux canaux Microsoft Edge dev, Beta et stable.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Mode plein écran: choisir une application":::

7. Sélectionnez l’une des options suivantes pour l’affichage de Microsoft Edge en mode plein écran:

   - Connexion numérique/interactive: affiche un site spécifique en mode plein écran, exécutant Microsoft Edge.
   - Navigateur public: exécute une version multi-onglet limitée de Microsoft Edge.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Affichage en mode plein écran: signature numérique plein écran":::

8. Sélectionnez **Suivant**.
9. Tapez l’URL à charger lors du lancement du kiosque.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Mode plein écran: entrer l’URL":::

10. Acceptez la valeur par défaut de 5 minutes pour le temps d’inactivité ou indiquez la valeur de votre choix.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Mode plein écran: entrer la durée d’inactivité":::

11. Cliquez sur  **Suivant**.
12. Fermez la fenêtre  **Paramètres**  pour enregistrer et appliquer vos choix.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Mode plein écran: terminer la configuration":::

13. Déconnectez-vous à partir de l’appareil kiosque et connectez-vous avec le compte kiosque local pour valider la configuration.

## Limitations fonctionnelles

Avec la publication de cette version d’évaluation du mode plein écran, nous continuons à travailler sur l’amélioration du produit et en ajoutant de nouvelles fonctionnalités.

Nous vous recommandons de désactiver :

- [StartupBoostEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [Extensions](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)
- [BackgroundModeEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)

## Feuille de route

### Début 2021

Nous allons ajouter la prise en charge et les fonctionnalités suivantes:

- Disponibilité générale du mode plein écran de MicrosoftEdge avec accès affecté à l’application unique sur Windows10 1909 et les plus élevés.
- Fonctionnalités supplémentaires pour la parité avec la version MicrosoftEdge hérité.
- Intégration avec Intune pour configurer les appareils à l’aide d’un profil en mode plein écran UX.
- Les raccourcis clavier supplémentaires seront bloqués.
- Limiter le lancement d’autres applications à partir du navigateur.

## Voir également

- [Configurer des bornes et enseignes numériques dans les éditions Windows de bureau](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Déployer la version héritée du mode plein écran de MicrosoftEdge](https://aka.ms/edgekioskmode)
- [Planifier votre déploiement de MicrosoftEdge](deploy-edge-plan-deployment.md)
- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
