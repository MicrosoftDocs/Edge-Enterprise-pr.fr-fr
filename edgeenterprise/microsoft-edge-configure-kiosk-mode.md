---
title: Configurer le mode kiosque Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 04/26/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Apprenez les fonctionnalités du mode kiosque et comment configurer les options du mode kiosque de Microsoft Edge.
ms.openlocfilehash: 20cb32c0cd27ad6d7437ed8ae0440560f3ed71b2
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617854"
---
# <a name="configure-microsoft-edge-kiosk-mode"></a>Configurer le mode kiosque Microsoft Edge

Cet article décrit la configuration des options Microsoft Edge en mode plein écran que vous pouvez piloter. Il existe également une feuille de route des fonctionnalités que nous ciblons.

> [!NOTE]
> Cet article concerne Microsoft Edge version 87 ou ultérieure.

> [!IMPORTANT]
> Appelez les fonctionnalités du mode plein écran Microsoft Edge sur Windows 10 à l’aide des arguments de lignes de commande fournis dans [Utiliser les fonctionnalités du mode plein écran](#use-kiosk-mode-features).

## <a name="overview"></a>Vue d'ensemble

Microsoft Edge en mode plein écran offre deux expériences de verrouillage du navigateur afin de permettre aux organisations de créer, gérer et offrir une expérience optimale pour leurs clients. Les expériences de verrouillage suivantes sont disponibles :  

- **Expérience de connexion numérique/interactive** : affiche un site spécifique en mode plein écran.
- **Expérience de navigation publique** : exécute une version multi-onglet limitée de Microsoft Edge.

Les deux expériences exécutent une session Microsoft Edge InPrivate qui protège les données de l’utilisateur.

## <a name="set-up-microsoft-edge-kiosk-mode"></a>Configurer Microsoft Edge en mode plein écran

Un ensemble initial de fonctionnalités du mode plein écran est disponible pour le test avec le canal stable Microsoft Edge, version 87. Vous pouvez télécharger la dernière version à partir [de Microsoft Edge (canal stable officiel).](https://www.microsoft.com/edge)

### <a name="kiosk-mode-supported-features"></a>Fonctionnalités prise en charge en mode plein écran

Le tableau suivant répertorie les fonctionnalités prise en charge par le mode plein écran dans Microsoft Edge et Microsoft Edge hérité. Utilisez ce tableau comme guide pour passer à Microsoft Edge en comparant la prise en charge de ces fonctionnalités dans les deux versions de Microsoft Edge.

|Fonctionnalité|Connexion numérique/interactive|Navigation publique|Disponible avec la version de Microsoft Edge (et versions supérieures)|Disponible avec Microsoft Edge hérité|
|-|-|-|-|-|
|Navigation InPrivate|Y|Y|89|Y|
|Réinitialiser en période d’inactivité|Y|Y|89|Y|
|[Barre d’adresses en lecture seule](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (stratégie) |N|Y |89|N|
|[Supprimer les téléchargements à la sortie](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (stratégie)  | Y|Y |89|N|
|F11 bloqué (entrée/sortie en plein écran) | Y | Y |89|Y|
|F12 bloqué (lancer les outils de développement) | Y | Y |89|Y|
| Prise en charge de plusieurs onglets | N| Y|89|Y|
|[Autoriser la prise en charge des URL](./microsoft-edge-policies.md#urlallowlist) (stratégie)|Y|Y|89|N|
|[Bloquer la prise en charge des URL](./microsoft-edge-policies.md#urlblocklist) (stratégie)|Y|Y|89|N|
|[Afficher le bouton d’accueil](./microsoft-edge-policies.md#showhomebutton) (stratégie)|N|Y|89|Y|
|[Gérer les favoris](./microsoft-edge-policies.md#managedfavorites) (stratégie)|N|Y|89|Y|
|[Activer l’imprimante](./microsoft-edge-policies.md#printingenabled) (stratégie)|Y|Y|89|Y|
|[Configurer l’URL de la page Nouvel onglet](./microsoft-edge-policies.md#newtabpagelocation) (stratégie)|N|Y|89|Y|
|Bouton de fin de session * | N| Y|89|Y|
|Toutes les URL Microsoft Edge internes sont bloquées, à l’exception de *edge://downloads* et *edge://print* |N|Y|89|Y|
| CTRL+N bloqué (ouvrir une nouvelle fenêtre) * | Y | Y |89|Y|
| Ctrl+T bloqué (ouvrir un nouvel onglet) |Y | N |89|Y|
|Paramètres et plus (...) afficheront uniquement les options requises  |Y |Y |89|Y|
|Restreindre le lancement d’autres applications à partir du navigateur|Y|Y|90|Y|
|Verrouillage des paramètres d’impression de l’interface utilisateur|Y|Y|90|Y|
|[Définir la page Nouvel onglet comme page d’accueil](./microsoft-edge-policies.md#homepageisnewtabpage) (stratégie)|N|Y|90|Y|

> [!NOTE]
> Les fonctions suivies d'un « * » ne sont activées que dans un scénario d'accès assigné à une seule application.

## <a name="use-kiosk-mode-features"></a>Utiliser les fonctionnalités du mode kiosque

Les fonctionnalités du mode plein écran de Microsoft Edge peuvent être invoquées avec les options de ligne de commande Windows 10 suivantes pour la signalisation numérique/interactive et la navigation publique.

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

- **--kiosk-idle-timeout-minutes=**: modifiez l’heure (en minutes) de la dernière activité utilisateur avant que le mode plein écran de Microsoft Edge réinitialise la session de l’utilisateur. Remplacez « value » dans l’exemple suivant par le nombre de minutes.

   ```
   --kiosk-idle-timeout-minutes=value
   ``` 
   Les « valeurs » suivantes sont pris en charge :

     - Valeurs par défaut (en minutes)
       - Plein écran - 0 (désactivé)
       - Navigation publique : 5 minutes
    - Valeurs autorisées
      - 0 : désactive le minuteur
      - 1-1 440 minutes pour la réinitialisation du minuteur d’inactivité


    ```
    msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --kiosk-idle-timeout-minutes=1
   ```

   ```
   msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --kiosk-idle-timeout-minutes=1
   ```

## <a name="support-policies-for-kiosk-mode"></a>Stratégies de support pour le mode plein écran

Utilisez l’une des stratégies Microsoft Edge répertoriées dans le tableau suivant pour améliorer l’expérience plein écran pour le type de mode plein écran Microsoft Edge que vous configurez. Pour en savoir plus sur ces stratégies, voir [Microsoft Edge – Référence de stratégie de navigateur.](./microsoft-edge-policies.md)

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

## <a name="microsoft-edge-with-assigned-access"></a>Microsoft Edge avec accès affecté

### <a name="single-app-kiosk"></a>Borne d’application unique

MicrosoftEdge version90 du mode plein écran offre une liste complète de fonctionnalités. Consultez la section des fonctionnalités prises en charge du mode plein écran.
Avec les mises à jour Windows suivantes, vous pouvez configurer MicrosoftEdge via une application unique à accès affecté.

|Système d'exploitation|Version|Mises à jour|
|--|--|--|
|Windows10 | 2004 ou ultérieure|[KB4601382 ou ultérieure](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows10| 1909| [KB4601380 ou ultérieure](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

Vous pouvez gérer l’application unique à accès affecté du mode plein écran MicrosoftEdge via [Paramètres Windows](/deployedge/microsoft-edge-configure-kiosk-mode#configure-using-windows-settings) et Intune.

### <a name="multi-app-kiosk"></a>Borne à plusieurs applications

Vous pouvez exécuter Microsoft Edge avec un [accès attribué à plusieurs applications](/windows/configuration/lock-down-windows-10-to-specific-apps) sous Windows 10. Cela équivaut au type de mode plein écran « Navigation normale » de l’ancienne version de Microsoft Edge . Pour configurer Microsoft Edge avec un accès affecté à plusieurs applications, suivez les instructions sur la configuration d’une borne [multi-application](/windows/configuration/lock-down-windows-10-to-specific-apps). (L’AUMID du canal stable de MicrosoftEdge est **MSEdge**).

### <a name="configure-using-windows-settings"></a>Configuration à l’aide des paramètres Windows

Les paramètres Windows constituent le moyen le plus simple de configurer un ou deux appareils borne à une seule application. Procédez comme suit pour configurer un ordinateur de borne à une seule application.

1. Les mises à jour système minimales pour les systèmes d’exploitation sont indiqués dans le tableau suivant.

|Système d'exploitation|Version|Mises à jour|
|--|--|--|
|Windows10 | 2004 ou ultérieure|[KB4601382 ou ultérieure](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows10| 1909| [KB4601380 ou ultérieure](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

2. Pour tester les dernières fonctionnalités, vous pouvez télécharger le dernier [canal stable Microsoft Edge](https://www.microsoft.com/edge/business/download), version89 ou supérieure.

3. Sur l’ordinateur kiosque, ouvrez Paramètres Windows, puis tapez «borne» dans le champ de recherche. Sélectionnez  **Configurer une borne (accès attribué)**, illustré dans la capture d’écran suivante pour ouvrir la boîte de dialogue de création de la borne.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurer la borne avec l’accès attribué":::

4. Sur la page **Configurer une borne** , cliquez sur  **Prise en main**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Page borne : prise en main":::

5. Tapez un nom pour créer un nouveau compte borne ou sélectionnez un compte existant dans la liste déroulante rempli, puis cliquez sur **Suivant**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Mode plein écran : créer un compte":::

6. Dans la page **Choisir une application borne** , sélectionnez **Microsoft Edge**, puis cliquez sur  **Suivant**.

   > [!NOTE]
   > Cela s’applique uniquement aux canaux Microsoft Edge développement, bêta et stable.

     :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5c-choose-a-kiosk-app.png" alt-text="Affichage en mode plein écran: signature numérique plein écran":::

7. Sélectionnez l’une des options suivantes pour l’affichage de MicrosoftEdge en mode plein écran:

   - Connexion numérique/interactive : affiche un site spécifique en mode plein écran, exécutant Microsoft Edge.
   - Navigateur public: exécute une version multi-onglet limitée de MicrosoftEdge.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Mode d’utilisation de la borne : signe numérique plein écran":::

8. Sélectionnez **Suivant**.
9. Tapez l’URL à charger lors du lancement du kiosque.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Mode plein écran : entrer l’URL":::

10. Acceptez la valeur par défaut de 5 minutes pour le temps d’inactivité ou indiquez la valeur de votre choix.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Mode plein écran : entrer la durée d’inactivité":::

11. Cliquez sur  **Suivant**.
12. Fermez la fenêtre  **Paramètres**  pour enregistrer et appliquer vos choix.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Mode plein écran : terminer la configuration":::

13. Déconnectez-vous à partir de l’appareil kiosque et connectez-vous avec le compte kiosque local pour valider la configuration.

## <a name="functional-limitations"></a>Limitations fonctionnelles

Avec la publication de cette version d’évaluation du mode plein écran, nous continuons à travailler sur l’amélioration du produit et en ajoutant de nouvelles fonctionnalités.

Pour l’instant, nous ne supportons pas les fonctionnalités suivantes et vous recommandons de les désactiver :

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

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Planifier votre déploiement de MicrosoftEdge](deploy-edge-plan-deployment.md)
- [Configurer des bornes et enseignes numériques dans les éditions Windows de bureau](/windows/configuration/kiosk-methods)
- [Planifier votre transition en mode plein écran](microsoft-edge-kiosk-mode-transition-plan.md)
