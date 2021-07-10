---
title: Planifier votre transition en mode plein écran
ms.author: aguta
author: aguta
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Planifier votre transition en mode plein écran
ms.openlocfilehash: 95c50b39eb6e844ae4309b260087931232276d45
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642910"
---
# <a name="plan-your-kiosk-mode-transition"></a>Planifier votre transition en mode plein écran

Cet article fournit des instructions sur la transition de votre kiosque de Microsoft Edge hérité vers Microsoft Edge.  

> [!NOTE]
> Cet article s’applique aux canaux stables, bêta et développement de Microsoft Edge, version 87 ou ultérieure.

> [!IMPORTANT]
> Lorsque la prise en charge de la version héritée de Microsoft Edge se termine le 9 mars 2021, elle sera supprimée et remplacée par Microsoft Edge sur Chromium dans le cadre de Windows Update en avril. Pour plus d’informations, voir [ce billet de blog](https://aka.ms/EdgeLegacyEOS). Pour continuer à utiliser vos scénarios de kiosque basés sur le navigateur, vous devez installer Microsoft Edge sur Chromium et configurer le mode plein écran avant la publication de Windows Update d’avril sur votre appareil.

## <a name="kiosk-setup-steps"></a>Étapes de configuration du kiosque

Utilisez les étapes suivantes comme guide pour configurer un kiosque dans Microsoft Edge.

**Étape 1 : évaluez vos besoins par rapport aux fonctionnalités publiées (et à venir) du mode plein écran.** Le tableau suivant répertorie les fonctionnalités prise en charge par le mode plein écran dans Microsoft Edge sur Chromium et Microsoft Edge hérité. Utilisez ce tableau comme guide pour passer à Microsoft Edge en comparant la prise en charge de ces fonctionnalités dans les deux versions de Microsoft Edge.

|Fonctionnalité|Connexion numérique/interactive|Navigation publique|Disponible avec la version de Microsoft Edge (et versions supérieures)|Disponible avec Microsoft Edge hérité|
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
|[Configurer l’URL de la page Nouvel onglet](./microsoft-edge-policies.md#newtabpagelocation) (stratégie)|N|Y|89|Y|
|Bouton Terminer la session | N| Y| 89|Y|
|Toutes les URL Microsoft Edge internes sont bloquées, à l’exception de *edge://downloads* et *edge://print* |N|Y|89|Y|
| Ctrl+N bloqué (ouvrir une nouvelle fenêtre) | Y | Y | 89 |Y|
| Ctrl+T bloqué (ouvrir un nouvel onglet) |Y | Y | 89 |Y|
|Paramètres et plus (...) afficheront uniquement les options requises  |Y |Y |89 |Y|
|Restreindre le lancement d’autres applications à partir du navigateur|Y|Y|90|Y|
|Verrouillage des paramètres d’impression de l’interface utilisateur|Y|Y|90|Y|
|[Définir la page Nouvel onglet comme page d’accueil](./microsoft-edge-policies.md#homepageisnewtabpage) (stratégie)|N|Y|90|Y|

> [!NOTE]
> Pour plus d’informations sur la planification des publication de Microsoft Edge, voir [la planification des publication de Microsoft Edge.](microsoft-edge-release-schedule.md)

**Étape 2 : testez le nouveau kiosque dans Microsoft Edge.** Nous vous recommandons de tester la configuration du mode plein écran dans Microsoft Edge. Un moyen rapide et facile de tester le mode plein écran consiste à configurer une application affectée à l’accès unique à l’aide des paramètres Windows, comme décrit ci-après.

1. Les mises à jour système minimales pour les systèmes d’exploitation sont indiquées dans le tableau suivant.

|Système d'exploitation|Version|Mises à jour|
|--|--|--|
|Windows 10 | 2004 ou ultérieure|[KB4601382 ou ultérieure](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 ou ultérieure](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

2. Pour tester les dernières fonctionnalités, vous pouvez télécharger le dernier [Microsoft Edge stable](https://www.microsoftedgeinsider.com/download), version 89 ou supérieure.

   > [!IMPORTANT]
   > Étant donné qu’une installation au niveau de l’appareil est requise, le canal Canary n’est pas pris en charge.

3. Sur l’ordinateur kiosque, ouvrez Paramètres Windows, puis tapez « kiosque » dans le champ de recherche. Sélectionnez  **Configurer une borne (accès attribué)**, illustré dans la capture d’écran suivante pour ouvrir la boîte de dialogue de création de la borne.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurer la borne avec l’accès attribué":::

4. Sur la page **Configurer une borne** , cliquez sur  **Prise en main**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Page borne : prise en main":::

5. Tapez un nom pour créer un nouveau compte borne ou sélectionnez un compte existant dans la liste déroulante rempli, puis cliquez sur **Suivant**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Mode plein écran : créer un compte":::

6. Dans la page **Choisir une application borne** , sélectionnez **Microsoft Edge**, puis cliquez sur  **Suivant**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5c-choose-a-kiosk-app.png" alt-text="Choisir une borne – Signe numérique plein écran":::

7. Sélectionnez l’une des options suivantes pour l’affichage de Microsoft Edge en mode plein écran :

   - Connexion numérique/interactive : affiche un site spécifique en mode plein écran, exécutant Microsoft Edge.
   - Navigateur public : exécute une version multi-onglet limitée de Microsoft Edge.
 
    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Affichage en mode plein écran : signature numérique plein écran":::

8. Sélectionnez **Suivant**.
9. Tapez l’URL à charger lors du lancement du kiosque.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Mode plein écran : entrer l’URL":::

10. Acceptez la valeur par défaut de 5 minutes pour le temps d’inactivité ou indiquez la valeur de votre choix.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Mode plein écran : entrer la durée d’inactivité":::

11. Cliquez sur  **Suivant**.
12. Fermez la fenêtre  **Paramètres**  pour enregistrer et appliquer vos choix.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Mode plein écran : terminer la configuration":::

13. Déconnectez-vous à partir de l’appareil kiosque et connectez-vous avec le compte kiosque local pour valider la configuration.

**Étape 3 : Développer un plan de transition.** En fonction de vos tests et de vos besoins organisationnels, nous vous recommandons de développer un plan de transition et de passer à Microsoft Edge sur Chromium avant la fin de la prise en charge de Microsoft Edge hérité le 9 mars 2021.

## <a name="additional-scenarios-that-require-you-to-recreate-an-existing-kiosk-mode"></a>Scénarios supplémentaires qui nécessitent la recréation d’un mode plein écran existant

Si vous mettez à jour vers Windows 10, version 20H2, Microsoft Edge sur Chromium sera installé et Microsoft Edge hérité sera masqué. Dans ce cas, vous devrez configurer à nouveau le mode plein écran dans Microsoft Edge sur Chromium.

## <a name="how-to-get-help"></a>Comment obtenir de l’aide

Le mode plein écran étant un élément important de votre activité quotidienne, nous voulons contribuer à rendre cette transition aussi fluide que possible et à éviter les perturbations. Si votre entreprise a besoin d’aide pour la transition vers Microsoft Edge sur Chromium :

- [Le support](https://support.serviceshub.microsoft.com/supportforbusiness/create?sapId=a77ee9b7-b6b6-aa08-d7b9-887ebe228207) est disponible auprès de Microsoft. 
- [Le support FastTrack](https://www.microsoft.com/fasttrack/microsoft-365/microsoft-edge?rtc=1) est également disponible sans frais supplémentaires pour les clients 150 ou plus de sièges payants de Windows 10 Entreprise.
- [L’application Assure](https://www.microsoft.com/en-us/fasttrack/microsoft-365/app-assure) est disponible si vous rencontrez des problèmes de compatibilité de site ou d’application.

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Nouveau Microsoft Edge pour remplacer la version héritée de Microsoft Edge par la version mardi de la mise à jour Windows 10 d’avril](https://techcommunity.microsoft.com/t5/microsoft-365-blog/new-microsoft-edge-to-replace-microsoft-edge-legacy-with-april-s/ba-p/2114224)