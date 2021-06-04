---
title: Redirection d’Internet Explorer vers Microsoft Edge pour assurer une compatibilité avec les sites web modernes
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 11/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Redirection d’Internet Explorer vers Microsoft Edge pour assurer une compatibilité avec les sites web modernes
ms.openlocfilehash: c9c64a55df3aeecaebaab3675296c5594612b94f
ms.sourcegitcommit: fc0ac6bb6655d1f6e2de7c838f275779cd7a5de6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "11175197"
---
# Redirection d’Internet Explorer vers Microsoft Edge pour assurer une compatibilité avec les sites web modernes

> [!NOTE]
> Cet article concerne le canal stable Microsoft Edge version 87 ou ultérieure.

##  <a name="overview"></a>Vue d'ensemble

De nombreux sites web modernes comportent des conceptions incompatibles avec Internet Explorer. Chaque fois qu’un utilisateur d’Internet Explorer visite un site public incompatible, il reçoit un message l’informant que le site est incompatible avec son navigateur et qu’il doit basculer manuellement vers un autre navigateur.

Vous devez basculer manuellement vers d’autres navigateurs à partir de la version 87 du canal stable de Microsoft Edge.

Lorsqu’un utilisateur accède à un site incompatible avec Internet Explorer, il est automatiquement redirigé vers Microsoft Edge. Cet article décrit l’expérience utilisateur pour la redirection et les stratégies de groupe utilisées pour configurer ou désactiver la redirection automatique.

> [!NOTE]
> Microsoft gère une liste de tous les sites connus comme incompatibles avec Internet Explorer. Pour plus d’informations, voir [Demander une mise à jour de la liste de compatibilité d’Internet Explorer](https://docs.microsoft.com/microsoft-edge/web-platform/ie-to-microsoft-edge-redirection#request-an-update-to-the-ie-compatibility-list)

##  <a name="redirection-experience"></a>Expérience de redirection

Lors de la redirection vers Microsoft Edge, une boîte de dialogue ponctuelle s’affiche aux utilisateurs dans la capture d’écran suivante. Cette boîte de dialogue explique les raisons de leur redirection et les invite à consentir à la copie de leurs données de navigation et préférences d’Internet Explorer vers Microsoft Edge. Les données de navigation suivantes sont importées : les favoris, mots de passe, moteurs de recherche, onglets ouverts, l’historique, les paramètres, cookies et la page d’accueil.

![Notification de navigation et invite à importer les données et les préférences.](media/edge-learnmore-neededge/neededge-dialog1.png)

Même s’ils n’accordent pas leur consentement en cochant « Toujours récupérer les données et préférences de navigation à partir d’Internet Explorer », les utilisateurs peuvent cliquer sur **Poursuivre la navigation** pour continuer leur session.

Enfin, une bannière d’incompatibilité de site web, illustrée dans la capture d’écran suivante, apparaît sous la barre d’adresses lors de chaque redirection.

![Notification sur les sites modernes et invite de configuration de Microsoft Edge en tant que navigateur par défaut ou exploration de Microsoft Edge.](media/edge-learnmore-neededge/neededge-banner.png)

Bannière d’incompatibilité du site web :

- encourage l’utilisateur à basculer vers Microsoft Edge
- propose la définition de Microsoft Edge en tant que navigateur par défaut
- donne à l’utilisateur la possibilité d’explorer Microsoft Edge

Lors de la redirection d’un site depuis Internet Explorer vers Microsoft Edge, l’onglet Internet Explorer qui a commencé le chargement du site est fermé s’il ne dispose pas de contenu antérieur. Dans le cas contraire, l’onglet actif permet d’accéder à la page de un support [support](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) de Microsoft qui explique la raison de la redirection du site vers Microsoft Edge.

> [!NOTE]
> Après la redirection, les utilisateurs peuvent revenir à l’utilisation d’Internet Explorer pour les sites qui ne figurent pas dans la liste d’incompatibilités d’Internet Explorer.  

##  <a name="policies-to-configure-redirection-to-microsoft-edge"></a>Stratégies de configuration de la redirection vers Microsoft Edge

> [!NOTE]
> Ces stratégies sont disponibles sous forme de mises à jour de fichiers ADMX à partir du 26 octobre 2020 et seront disponibles dans Intune d’ici au 9 novembre 2020.

Trois stratégies de groupe doivent être configurées pour activer la redirection automatique vers Microsoft Edge. Ces stratégies sont les suivantes :

- RedirectSitesFromInternetExplorerPreventBHOInstall
- RedirectSitesFromInternetExplorerRedirectMode
- HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

###  <a name="policy:-redirectsitesfrominternetexplorerpreventbhoinstall"></a>Stratégie : RedirectSitesFromInternetExplorerPreventBHOInstall

La redirection d’Internet Explorer vers Microsoft Edge nécessite un Objet Application d’assistance du navigateur (BHO) d’Internet Explorer nommé « BHO IEtoEdge ». La stratégie **RedirectSitesFromInternetExplorerPreventBHOInstall** détermine si cet Objet Application d’assistance du navigateur (BHO) est installé ou non.  

- Si vous activez cette stratégie, l’Objet Application d’assistance du navigateur (BHO) nécessaire à la redirection ne sera pas installé et vos utilisateurs continueront à voir les messages d’incompatibilité relatifs à certains sites web sur Internet Explorer. Si l’Objet Application d’assistance du navigateur (BHO) est déjà installé, il sera désinstallé lors de la prochaine mise à jour du canal stable de Microsoft Edge.
- Si vous désactivez ou ne configurez pas cette stratégie, l’Objet Application d’assistance du navigateur (BHO) est installé. Il s’agit du comportement par défaut.

Outre la nécessité de l’Objet Application d’assistance du navigateur (BHO), il existe une dépendance sur **RedirectSitesFromInternetExplorerRedirectMode**, qui doit être définie sur « Rediriger les sites en fonction de la liste des sites incompatibles » ou « Non configuré ».

###  <a name="policy:-redirectsitesfrominternetexplorerredirectmode"></a>Stratégie : RedirectSitesFromInternetExplorerRedirectMode

 Cette stratégie correspond au paramètre **Navigateur par défaut** « Laisser Internet Explorer ouvrir les sites dans Microsoft Edge » de Microsoft Edge. Vous pouvez accéder à ce paramètre en accédant à l’URL *edge://settings/defaultbrowser*.  

- Si vous ne configurez pas cette stratégie ou si vous la définissez-la sur « Liste de sites », Internet Explorer redirige les sites incompatibles vers Microsoft Edge. Il s’agit du comportement par défaut.
- Pour désactiver cette stratégie, sélectionnez **Activé** puis, dans la liste déroulante sous Options : rediriger les sites incompatibles d’Internet Explorer vers Microsoft Edge, sélectionnez **Désactiver**. Dans ce cas, les sites incompatibles ne sont pas redirigés vers Microsoft Edge.

> [!NOTE]
> Si vous utilisez un appareil personnel non géré par votre organisation, un autre paramètre s’affiche intitulé « Autoriser le chargement de sites en mode Internet Explorer » sous **Compatibilité d’Internet Explorer**.
>
>Si vous utilisez un ordinateur joint à un domaine ou inscrit à la Gestion des appareils mobiles (MDM), cette option ne sera pas visible.
>
> Au lieu de cela, si vous voulez laisser vos utilisateurs charger des sites en mode Internet Explorer, vous pouvez le faire en configurant la stratégie [Autoriser le test du mode Internet Explorer](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing).

###  <a name="policy:-hideinternetexplorerredirectuxforincompatiblesitesenabled"></a>Stratégie : HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

Cette stratégie configure l’expérience utilisateur pour la redirection de sites incompatibles vers Microsoft Edge.  

- Si vous activez cette stratégie, les utilisateurs ne verront jamais la boîte de dialogue de redirection ponctuelle et la bannière de redirection. Les données du navigateur ou les préférences utilisateur ne sont pas importées.
- Si vous désactivez ou ne configurez pas cette stratégie, la boîte de dialogue de redirection s’affiche lors de la première redirection et la bannière de redirection permanente apparaît pour les sessions commençant par une redirection.

  > [!NOTE]
  > Les données de navigation utilisateur sont importées chaque fois qu’un utilisateur rencontre une nouvelle redirection. Cela ne se produit toutefois que si l’utilisateur a consenti à l’importation dans la boîte de dialogue de redirection ponctuelle.

##  <a name="disable-redirection-to-microsoft-edge"></a>Désactiver la redirection vers Microsoft Edge

Si vous voulez désactiver la redirection AVANT de procéder à la mise à jour vers la version 87 du canal stable de Microsoft Edge, procédez comme suit :

1. Définissez la stratégie **RedirectSitesFromInternetExplorerPreventBHOInstall** sur **Activé**.

Si vous voulez désactiver la redirection APRÈS la mise à jour vers la version 87 du canal stable de Microsoft Edge, procédez comme suit :

1. Définissez la stratégie **RedirectSitesFromInternetExplorerRedirectMode** sur **Activé**puis, dans la liste déroulante sous Options : rediriger les sites incompatibles d’Internet Explorer vers Microsoft Edge, sélectionnez **Désactiver**. Ce paramètre arrête la redirection dès que la stratégie prend effet.
2. Définissez la stratégie **RedirectSitesFromInternetExplorerPreventBHOInstall** sur **Activé**. Cette opération désinstalle l’Objet Application d’assistance du navigateur (BHO) après la prochaine mise à jour de Microsoft Edge.

##  <a name="see-also"></a>Voir également

- [Demander une mise à jour de la liste de compatibilité d’Internet Explorer](https://docs.microsoft.com/microsoft-edge/web-platform/ie-to-microsoft-edge-redirection#request-an-update-to-the-ie-compatibility-list)
- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Stratégies Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-policies)