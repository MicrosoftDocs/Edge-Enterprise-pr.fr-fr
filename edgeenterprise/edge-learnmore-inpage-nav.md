---
title: Conserver la navigation dans la page en mode Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Conserver la navigation dans la page en mode Internet Explorer
ms.openlocfilehash: 20b18d121c3babfaacffd4a08316b25be714d95e
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641360"
---
# <a name="keep-in-page-navigation-in-internet-explorer-mode"></a>Conserver la navigation dans la page en mode Internet Explorer

Vous pouvez utiliser cette stratégie comme solution temporaire pour forcer toute navigation dans la page des sites en mode Internet Explorer (mode IE) à conserver ce mode.

Une navigation dans la page est lancée à partir d'un lien, d'un script ou d'un formulaire de la page en cours. Il peut également s'agir d'une redirection côté serveur d'une précédente tentative de navigation dans la page. À l’inverse, un utilisateur peut démarrer une navigation qui n’est pas «dans la page» et qui est indépendante de la page active de plusieurs façons en utilisant les contrôles du navigateur. Par exemple, à l’aide de la barre d’adresses, du bouton précédent ou d’un lien favori.

>[!NOTE]
>Cet article concerne MicrosoftEdge version81 ou ultérieure.

## <a name="prerequisites"></a>Conditions préalables

Les mises à jour Windows suivantes sont nécessaires pour cette stratégie:

- Windows 10 version 1909 et 1903, Windows Server version 1909 et 1903  ([KB4532695](https://support.microsoft.com/help/4532695))
- Windows 10 version 1809, Windows Server version 1809, Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))
- Windows 10 version 1803 ([KB4534308](https://support.microsoft.com/help/4534308))
- Windows 10 version 1709 ([KB4534318](https://support.microsoft.com/help/4534318))


## <a name="about-this-policy"></a>À propos de cette stratégie

Cette stratégie vous indique le temps d’identification et de configuration de tous les serveurs d’authentification utilisés par vos sites de mode IE. Toutefois, cette stratégie peut se traduire par une expérience de navigation incohérente dans laquelle certains sites sont affichés en mode IE et à d’autres moments affichés en mode Microsoft Edge. Cette expérience dépend selon que la navigation vers le site à partir a commencé ou non dans une page en mode IE. Les sites qui ne sont pas explicitement configurés pour s’ouvrir dans un moteur de rendu spécifique sont soumis à cette incohérence.

Si vous activez cette stratégie, nous vous recommandons de la désactiver une fois que vous avez identifié tous les serveurs d’authentification et que vous les avez ajoutés à la liste des sites comme étant neutres. Cette action garantit que vos sites modernes ne s’affichent jamais en mode IE par inadvertance.

## <a name="keep-in-page-navigation-in-ie-mode"></a>Conserver la navigation dans la page en mode InternetExplorer

Pour conserver la navigation automatique ou dans toutes les navigations dans la page en mode Internet Explorer, procédez comme suit:

1. Ouvrez l'Éditeur d'objets de stratégie de groupe.
2. Cliquez sur **Configuration ordinateur** > **Modèles d’administration** > **MicrosoftEdge**.
3. Sous **Paramètre**, double-cliquez sur **Spécifier la manière dont les navigations «dans la page» vers les sites non configurés se comportent lorsque vous lancez à partir des pages du mode Internet Explorer**.

   ![Paramètre de la stratégie dans la page](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-settings.png)

4. Sélectionnez **Activé** 

   ![Activer la stratégie dans la page](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-enable.png)

5. Choisissez l'une des options suivantes dans la liste déroulante:

   - **Par défaut** : sites uniquement configurés pour s’ouvrir en mode Internet Explorer s’ouvrent dans ce mode. Tout site non configuré pour s’ouvrir en mode Internet Explorer est redirigé vers Microsoft Edge.
   - **Garder uniquement les navigations automatiques en mode Internet Explorer** : utilisez cette option si vous souhaitez utiliser l’expérience par défaut, sauf que toutes les navigations automatiques (telles que les redirections 302) vers des sites non configurés continuent en mode Internet Explorer.
   - **Conserver toute la navigation dans la page en mode**  * Internet Explorer *_(Le moins recommandé)_*_ Toutes les navigations à partir de pages chargées en mode IE vers des sites non configurés sont conservées en mode Internet Explorer.

6. Cliquez sur _*OK** ou **appliquez pour** enregistrer les paramètres de stratégie.

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
