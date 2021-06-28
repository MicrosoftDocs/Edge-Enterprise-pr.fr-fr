---
title: Désactiver Internet Explorer 11
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez comment désactiver Internet Explorer 11 et utiliser le mode Internet Explorer dans Microsoft Edge.
ms.openlocfilehash: ae4d936df7e432eee250e1c7327acfd206d86410
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617484"
---
# <a name="disable-internet-explorer-11"></a>Désactiver Internet Explorer11

>[!Note]
> L’application de bureau Internet Explorer11 sera retirée et ne sera plus prise en charge le 15juin2022 (pour obtenir la liste des applications dans l’étendue, [consultez le FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Les mêmes applications et sites Internet Explorer11 que vous utilisez aujourd’hui peuvent s’ouvrir dans MicrosoftEdge en mode Internet Explorer. [Plus d'informations ici](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Cet article explique comment désactiver Internet Explorer11 en tant que navigateur autonome dans votre environnement.

## <a name="prerequisites"></a>Prérequis

Les mises à jour Windows et les logiciels Microsoft Edge suivants sont requis :

- Mises à jour Windows

  - Windows 10, version 2004, Windows Server version 2004, Windows 10, version 20H2 : [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) ou version ultérieure
  - Windows 10 version 1909, Windows Server version 1909 : [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) ou version ultérieure
  - Windows 10 version 1809, Windows Server version 1809 et Windows Server 2019 : [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) ou version ultérieure
  - Windows 10, version 1607, Windows Server 2016 : [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) ou version ultérieure
   - Version initiale de Windows 10 (juillet 2015) : [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) ou version ultérieure
  - Windows 8.1 : [KB4601384 ou](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) ultérieur
  - Windows Server 2012 : [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) ou ultérieur
  
- Canal Stable Microsoft Edge


## <a name="overview"></a>Vue d'ensemble

Pour les organisations qui ont besoin d’Internet Explorer 11 (IE11) pour la compatibilité héritée, le mode Internet Explorer (mode IE) sur Microsoft Edge offre une expérience de navigateur unique et transparente. Les utilisateurs peuvent accéder aux applications héritées à partir de Microsoft Edge sans avoir à revenir à IE11.

Après avoir configuré le mode Internet Explorer, vous pouvez désactiver Internet Explorer 11 en tant que navigateur autonome**sans affecter les fonctionnalités du mode IE**au sein de votre organisation à l’aide de la stratégie de groupe.

> [!NOTE]
> Si vous avez besoin de l’application IE11 autonome pour des sites spécifiques et que vous souhaitez rediriger tout le trafic du navigateur vers Microsoft Edge, vous pouvez configurer la stratégie[Envoyer tous les sites non inclus dans la liste des sites vers Microsoft Edge](./edge-ie-mode-policies.md#redirect-sites-from-ie-to-microsoft-edge) pour rediriger les sites d’Internet Explorer vers Microsoft Edge.

## <a name="user-experience-after-redirecting-traffic-to-microsoft-edge"></a>Expérience utilisateur après la redirection du trafic vers Microsoft Edge

Lorsque vous activez la stratégie **Désactiver Internet Explorer 11 en tant que navigateur autonome**, toute l’activité Internet Explorer 11 est redirigée vers Microsoft Edge et les utilisateurs ont l’expérience suivante :

- L’icône IE11 du menu Démarrer sera supprimée, mais celle de la barre des tâches restera.
- Lorsque les utilisateurs tentent de lancer des raccourcis ou des associations de fichiers qui utilisent IE11, ils sont redirigés pour ouvrir le même fichier/URL dans Microsoft Edge.
- Lorsque les utilisateurs tentent de lancer IE11 en invoquant directement iexplore.exe binaire, Microsoft Edge se lance à la place.

Dans le cadre de la définition de la stratégie pour cette expérience, vous pouvez éventuellement afficher un message de redirection pour chaque utilisateur qui tente de lancer IE11. Ce message peut être affiché « Toujours » ou « Une fois par utilisateur ». Par défaut, le message de redirection affiché dans la capture d’écran suivante n’est jamais affiché.

:::image type="content" source="media/edge-ie-disable-ie11/disable-ie-redirect-msg.png" alt-text="Alerte lors de la tentative d’ouverture d’IE après qu’une redirection vers Microsoft Edge est active.":::

Si votre liste des sites en mode Entreprise contient des applications configurées pour s’ouvrir dans l’application IE11 et que vous désactivez IE11 avec cette stratégie, elles s’ouvrent en mode IE sur Microsoft Edge.
> [!NOTE]
> Un problème connu s’était créé avec le flux utilisateur lorsqu’un site est configuré pour s’ouvrir dans l’application IE11 et que la stratégie Désactiver InternetExplorer (IE11) est définie. Le problème a été résolu dans MicrosoftEdge versions 91.0.840.0 ou ultérieures.

## <a name="disable-internet-explorer-11-as-a-standalone-browser"></a>Désactiver Internet Explorer11 en tant que navigateur autonome

Pour désactiver Internet Explorer 11 à l’aide de la stratégie de groupe, suivez les étapes suivantes :

1. Assurez-vous que vous avez les mises à jour de système d’exploitation préalables. Cette étape met directement à jour les fichiers ADMX sur votre ordinateur (notamment inetréa.adml et inetrémx.admx). Si vous voulez mettre à jour votre magasin central, vous devrez copier les fichiers .adml et .admx à partir d’un ordinateur qui dispose des mises à jour préalables. Pour plus d’informations, voir [Créer et gérer des informations du Magasin central](/troubleshoot/windows-client/group-policy/create-and-manage-central-store)
2. Ouvrez l’Éditeur de stratégie de groupe.
3. Allez à ***Computer Configuration/Administrative Templates/Windows Components/Internet Explorer***. 
4. Double-cliquez **Désactiver Internet Explorer 11 en tant que navigateur autonome**.
5. Sélectionnez **Activé.**
6. Sous **Options,** sélectionnez l’une des valeurs suivantes :

   - **Jamais**   si vous ne souhaitez pas informer les utilisateurs qu’IE11 est désactivé.
   - **Toujours**   si vous souhaitez avertir les utilisateurs chaque fois qu’ils sont redirigés à partir d’Internet IE11.
   - **Une fois par utilisateur**   si vous souhaitez avertir les utilisateurs uniquement la première fois qu’ils sont redirigés.

7. Cliquez ** OK** ou  **Appliquez**   pour enregistrer ce paramètre de stratégie.

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [À propos du mode Internet Explorer](./edge-ie-mode.md)
- [Informations supplémentaires sur le mode entreprise](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
