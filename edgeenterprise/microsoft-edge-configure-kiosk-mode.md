---
title: Configurer le mode kiosque Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 03/16/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Apprenez les fonctionnalités du mode kiosque et comment configurer les options du mode kiosque de Microsoft Edge.
ms.openlocfilehash: 9d76bfcaebeaf56e627a401cc4f0375bce9d17a3
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448128"
---
# <a name="configure-microsoft-edge-kiosk-mode"></a>Configurer le mode kiosque Microsoft Edge

Cet article décrit la configuration des options Microsoft Edge en mode plein écran que vous pouvez piloter. Il existe également une feuille de route des fonctionnalités que nous ciblons.

> [!NOTE]
> Cet article concerne MicrosoftEdge version87 ou ultérieure.

> [!IMPORTANT]
> Appelez les fonctionnalités du mode plein écran MicrosoftEdge sur Windows10 à l’aide des arguments de lignes de commande fournis dans [Utiliser les fonctionnalités du mode plein écran](#use-kiosk-mode-features).

## <a name="overview"></a>Vue d'ensemble

Microsoft Edge en mode plein écran offre deux expériences de verrouillage du navigateur afin de permettre aux organisations de créer, gérer et offrir une expérience optimale pour leurs clients. Les expériences de verrouillage suivantes sont disponibles:  

- **Expérience de connexion numérique/interactive** : affiche un site spécifique en mode plein écran.
- **Expérience de navigation publique** : exécute une version multi-onglet limitée de MicrosoftEdge.

Les deux expériences exécutent une session MicrosoftEdge InPrivate qui protège les données de l’utilisateur.

## <a name="set-up-microsoft-edge-kiosk-mode"></a>Configurer MicrosoftEdge en mode plein écran

Un ensemble initial de fonctionnalités du mode plein écran est disponible pour le test avec le canal stable MicrosoftEdge, version87. Vous pouvez télécharger la dernière version à partir [de MicrosoftEdge (canal stable officiel).](https://www.microsoft.com/edge)

### <a name="kiosk-mode-supported-features"></a>Fonctionnalités prise en charge en mode plein écran

Le tableau suivant répertorie les fonctionnalités prise en charge par le mode plein écran dans Microsoft Edge et MicrosoftEdge hérité. Utilisez ce tableau comme guide pour passer à MicrosoftEdge en comparant la prise en charge de ces fonctionnalités dans les deux versions de Microsoft Edge.

|Fonctionnalité|Connexion numérique/interactive|Navigation publique|Disponible avec la version de MicrosoftEdge (et versions supérieures)|Disponible avec Microsoft Edge hérité|
|-|-|-|-|-|
|Navigation InPrivate|Y|Y|89|Y|
|Réinitialiser en période d’inactivité|Y|Y|89|Y|
|[Barre d’adresses en lecture seule](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (stratégie) |N|Y |89|N|
|[Supprimer les téléchargements à la sortie](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (stratégie)  | Y|Y |89|N|
|F11 bloqué (entrée/sortie en plein écran) | Y | Y | 89 |Y|
|F12 bloqué (lancer les outils de développement) | Y | Y | 89 |Y|
| Prise en charge de plusieurs onglets | N| Y| 89|Y|
|[Autoriser la prise en charge des URL](./microsoft-edge-policies.md#urlallowlist) (stratégie)|Y|Y|89|N|
|[Bloquer la prise en charge des URL](./microsoft-edge-policies.md#urlblocklist) (stratégie)|Y|Y|89|N|
|[Afficher le bouton d’accueil](./microsoft-edge-policies.md#showhomebutton) (stratégie)|N|Y|89|Y|
|[Gérer les favoris](./microsoft-edge-policies.md#managedfavorites) (stratégie)|N|Y|89|Y|
|[Activer l’imprimante](./microsoft-edge-policies.md#printingenabled) (stratégie)|Y|Y|89|Y|
|[Configurer l’URL de la page Nouvel onglet](./microsoft-edge-policies.md#newtabpagelocation) (stratégie)|N|Y||Y|
|Bouton de fin de session * | N| Y| 89|Y|
|Toutes les URL MicrosoftEdge internes sont bloquées, à l’exception de *edge://downloads* et *edge://print* |N|Y|89|Y|
| CTRL+N bloqué (ouvrir une nouvelle fenêtre) * | Y | Y | 89 |Y|
| Ctrl+T bloqué (ouvrir un nouvel onglet) |Y | N | 89 |Y|
|Paramètres et plus (...) afficheront uniquement les options requises  |Y |Y |89 |Y|
|Restreindre le lancement d’autres applications à partir du navigateur|Y|Y|90/91|Y|
|Verrouillage des paramètres d’impression de l’interface utilisateur|Y|Y|90/91|Y|
|[Définir la page Nouvel onglet comme page d’accueil](./microsoft-edge-policies.md#homepageisnewtabpage) (stratégie)|-|-|À déterminer|Y|

> [!NOTE]
> Les fonctions suivies d'un « * » ne sont activées que dans un scénario d'accès assigné à une seule application.

## <a name="use-kiosk-mode-features"></a>Utiliser les fonctionnalités du mode kiosque

Les fonctionnalités du mode plein écran de Microsoft Edge peuvent être invoquées avec les options de ligne de commande Windows10 suivantes pour la signalisation numérique/interactive et la navigation publique.

### <a name="kiosk-mode-digitalinteractive-signage"></a>Mode plein écran numérique/signalisation interactive
 
```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

### <a name="kiosk-mode-public-browsing"></a>Navigation publique en mode plein écran

```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing
```

### <a name="additional-command-line-options"></a>Autres options de la ligne de commande

- **--no-first-run**: désactiver la première expérience d’exécuter Microsoft Edge.

   ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --no-first-run
  ```

  ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --no-first-run
  ```

- **--kiosk-idle-timeout-minutes=**: modifiez l’heure (en minutes) de la dernière activité utilisateur avant que le mode plein écran de MicrosoftEdge réinitialise la session de l’utilisateur. Remplacez «value» dans l’exemple suivant par le nombre de minutes.

   ```
   --kiosk-idle-timeout-minutes=value
   ``` 
   Les «valeurs » suivantes sont pris en charge :

     - Valeurs par défaut (en minutes)
       - Plein écran - 0 (désactivé)
       - Navigation publique: 5minutes
    - Valeurs autorisées
      - 0: désactive le minuteur
      - 1-1440 minutes pour la réinitialisation du minuteur d’inactivité


    ```
    msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --kiosk-idle-timeout-minutes=1
   ```

   ```
   msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --kiosk-idle-timeout-minutes=1
   ```

## <a name="support-policies-for-kiosk-mode"></a>Stratégies de support pour le mode plein écran

Utilisez l’une des stratégies MicrosoftEdge répertoriées dans le tableau suivant pour améliorer l’expérience plein écran pour le type de mode plein écran MicrosoftEdge que vous configurez. Pour en savoir plus sur ces stratégies, voir [MicrosoftEdge – Référence de stratégie de navigateur.](./microsoft-edge-policies.md)

> [!NOTE]
> La configuration des stratégies n’est pas limitée aux stratégies répertoriées dans le tableau suivant, mais des stratégies supplémentaires doivent être testées pour s’assurer que les fonctionnalités du mode plein écran ne sont pas affectées.

|Stratégie de groupe|Connexion numérique/interactive|Navigation publique à application unique|
|--|--|--|
|[Impression](./microsoft-edge-policies.md#printing-policies) | Y|Y |
|[HomePageLocation](./microsoft-edge-policies.md#homepagelocation) |N | Y|
|[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton) |N | Y|
|[NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) |N |Y |
|[FavoritesBarEnabled](./microsoft-edge-policies.md#favoritesbarenabled) |N |Y |
|[URLAllowlist](./microsoft-edge-policies.md#urlallowlist) |Y |Y |
|[URLBlocklist](./microsoft-edge-policies.md#urlblocklist) |Y | Y|
|[ManagedSearchEngines](./microsoft-edge-policies.md#managedsearchengines) |N | Y|
|[UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed) |N | Y|
|[VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) | N|Y |
|[Paramètres SmartScreen](./microsoft-edge-policies.md#smartscreen-settings-policies) |Y |Y |
|[EdgeCollectionsEnabled](./microsoft-edge-policies.md#edgecollectionsenabled)|Y|Y|

## <a name="microsoft-edge-with-assigned-access"></a>MicrosoftEdge avec accès affecté

### <a name="single-app-kiosk"></a>Borne à application unique

MicrosoftEdge prend actuellement en charge un sous-ensemble des mêmes types de mode plein écran hérités de MicrosoftEdge pour l’accès affecté à une seule application avec les expériences de verrouillage suivantes: connexion numérique/interactive et navigation publique.  

Le mode plein écran de Microsoft Edge avec une seule application à accès affecté est actuellement disponible pour les tests avec la dernière version d’évaluation de [Windows 10 Insider Preview,](https://insider.windows.com/)version 20215 ou supérieure, et avec le  [canal bêta de Microsoft Edge](https://www.microsoftedgeinsider.com/download), version 89 ou supérieure.

**Comment puis-je obtenir l’aperçu de Windows Insider?**

Si vous souhaitez en savoir plus sur l’installation d’une version d'évaluation de Windows10 Insider sur un PC, veuillez consulter les instructions de la rubrique  [Prise en main des versions d'évaluation de Windows 10 Insider Preview](/windows-insider/get-started).

### <a name="multi-app-kiosk"></a>Borne à plusieurs applications

Vous pouvez exécuter MicrosoftEdge avec un [accès attribué à plusieurs applications](/windows/configuration/lock-down-windows-10-to-specific-apps) sous Windows10. Cela équivaut au type de mode plein écran «Navigation normale» de l’ancienne version de Microsoft Edge . Pour configurer MicrosoftEdge avec un accès affecté à plusieurs applications, suivez les instructions sur la configuration d’une borne [multi-application](/windows/configuration/lock-down-windows-10-to-specific-apps). (L’AUMID du canal stable de MicrosoftEdge est **MSEdge**).

Lorsque vous utilisez MicrosoftEdge avec un accès affecté à plusieurs applications, vous pouvez configurer MicrosoftEdge Kiosk pour utiliser les stratégies de navigateur[Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) afin de configurer l’expérience de navigation afin de répondre à vos besoins uniques.

### <a name="configure-using-windows-settings"></a>Configurer à l’aide des paramètres Windows

Les paramètres Windows constituent le moyen le plus simple de configurer un ou deux appareils borne à une seule application. Procédez comme suit pour configurer un ordinateur borne à une seul application.

1. Installez la version la plus récente de Windows10 Insider Preview, version 20215 ou ultérieure. Suivez les instructions de [Prise en main des versions d'évaluation de Windows10 Insider Preview](/windows-insider/get-started).
2. Pour tester les dernières fonctionnalités, vous pouvez télécharger la dernière version bêta de [Microsoft Edge](https://www.microsoftedgeinsider.com/download), version89 ou supérieure.
3. Sur l’ordinateur de borne, ouvrez Paramètres Windows, puis tapez «borne» dans le champ de recherche. Sélectionnez  **Configurer une borne (accès attribué)**, illustré dans la capture d’écran suivante pour ouvrir la boîte de dialogue de création de la borne.

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

## <a name="functional-limitations"></a>Limitations fonctionnelles

Avec la publication de cette version d’évaluation du mode plein écran, nous continuons à travailler sur l’amélioration du produit et en ajoutant de nouvelles fonctionnalités.

Pour l’instant, nous ne supportons pas les fonctionnalités suivantes et vous recommandons de les désactiver:

- [InPrivateModeAvailability](./microsoft-edge-policies.md#inprivatemodeavailability)
- [IsolateOrigins](./microsoft-edge-policies.md#isolateorigins)
- [ManagedFavorites](./microsoft-edge-policies.md#managedfavorites)
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled)
- [EdgeCollectionsEnabled](./microsoft-edge-policies.md#edgecollectionsenabled)
- [UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)
- [DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting)
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled)
- [InternetExplorerIntegrationLevel](./microsoft-edge-policies.md#internetexplorerintegrationlevel)
- [Extensions](./microsoft-edge-policies.md#extensions-policies)
- [BackgroundModeEnabled](./microsoft-edge-policies.md#backgroundmodeenabled)
- [UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)

## <a name="roadmap"></a>Feuille de route

### <a name="in-early-2021"></a>Début 2021

Nous allons ajouter la prise en charge et les fonctionnalités suivantes:

- Disponibilité générale du mode plein écran de MicrosoftEdge avec accès affecté à l’application unique sur Windows10 1909 et les plus élevés.
- Fonctionnalités supplémentaires pour la parité avec la version MicrosoftEdge hérité.
- Intégration avec Intune pour configurer les appareils à l’aide d’un profil en mode plein écran UX.
- Limiter le lancement d’autres applications à partir du navigateur.
- Verrouillage des paramètres d’impression de l’interface utilisateur.

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Planifier votre déploiement de MicrosoftEdge](deploy-edge-plan-deployment.md)
- [Configurer des bornes et enseignes numériques dans les éditions Windows de bureau](/windows/configuration/kiosk-methods)
- [Planifier votre transition en mode plein écran](microsoft-edge-kiosk-mode-transition-plan.md)