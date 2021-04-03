---
title: Configurer des stratégies de mode IE
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 03/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer des stratégies de mode IE
ms.openlocfilehash: a2abf6f6ef71c1f30786031ef19b9633bfafc43f
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470162"
---
# <a name="configure-ie-mode-policies"></a>Configurer des stratégies de mode IE

Cet article explique comment configurer des stratégies de mode IE.

> [!NOTE]
> Cet article concerne les canaux MicrosoftEdge **stable**, **Beta** et **Dev**, version77 ou ultérieures.

La configuration du mode IE passe par trois étapes:

1. [Configurer l’intégration d’Internet Explorer](#configure-internet-explorer-integration)
2. [Rediriger les sites de Microsoft Edge vers le mode IE](#redirect-sites-from-microsoft-edge-to-ie-mode)
3. (Facultatif) [Rediriger les sites d’IE vers Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)

    1. Si vous êtes prêt à désactiver l’application IE11, suivez les étapes de [Désactiver Internet Explorer 11](https://docs.microsoft.com/deployedge/edge-ie-disable-ie11)
    2. Sinon, suivez les autres étapes de la procédure [rediriger des sites d’IE à Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge)

> [!NOTE]
> Les stratégies permettant d’activer le mode IE peuvent être configurées via Intune. Pour plus d’informations, consultez[Ajouter Microsoft Edge à Microsoft Intune](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) et [Configurer les stratégies Microsoft Edge avec Microsoft Intune](./configure-edge-with-intune.md).

## <a name="configure-internet-explorer-integration"></a>Configurer l’intégration d’Internet Explorer

Vous pouvez configurer Internet Explorer pour qu’il s’ouvre directement dans Microsoft Edge (mode IE). Vous pouvez également configurer Internet Explorer pour l’ouvrir avec une fenêtre Internet Explorer 11 autonome. La plupart des utilisateurs préfèrent lorsque les sites sont ouverts directement dans Microsoft Edge en mode IE.

### <a name="enable-internet-explorer-integration-using-group-policy"></a>Activer l’intégration d’Internet Explorer en utilisant la fonctionnalité Stratégie de groupe

1. Téléchargez et utilisez le dernier [modèle de stratégie MicrosoftEdge](https://www.microsoft.com/en-us/edge/business/download).
2. Ouvrez l’Éditeur de stratégie de groupe.
3. Cliquez sur **Configuration ordinateur** > **Modèles d’administration** > **MicrosoftEdge**.
4. Double-cliquez sur **Configurer l’intégration d’Internet Explorer**.
5. Sélectionnez **Activé**.
6. Sous **Options**, définir la valeur de la liste déroulante sur 
   -  **Mode Internet Explorer** si vous voulez que les sites s’ouvrent en mode IE sur Microsoft Edge
   -  **Internet Explorer 11** si vous voulez que les sites s’ouvrent dans une fenêtre Internet Explorer 11 autonome
   -  **Aucun** si vous voulez empêcher les utilisateurs de configurer le mode Internet Explorer via edge://flags ou une ligne de commande

   > [!NOTE]
   > Le fait de définir la stratégie sur ** Désactivé** implique que le mode IE soit désactivé par la stratégie, mais qu’il soit possible de le définir via edge://flags ou les options de ligne de commande.
7. Cliquez sur **OK** ou sur **Appliquer** pour enregistrer ce paramètre de stratégie.

## <a name="redirect-sites-from-microsoft-edge-to-ie-mode"></a>Rediriger les sites de Microsoft Edge vers le mode IE

Il existe deuxoptions pour identifier les sites qui doivent s’ouvrir en modeIE:

- (Recommandé) [Configurer des sites dans la liste des sites d’entreprise](#configure-sites-on-the-enterprise-site-list)
- [Configurer tous les sites intranet](#configure-all-intranet-sites)

### <a name="configure-sites-on-the-enterprise-site-list"></a>Configurer des sites dans la liste des sites d’entreprise

Vous pouvez utiliser les stratégies de groupe suivantes pour configurer des sites spécifiques afin qu’ils s’ouvrent en mode IE:

- [Utiliser la liste des sitesweb en modeEntreprise](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)
- [Configurer la liste des sites en mode Entreprise](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (MicrosoftEdge, version78 ou ultérieures)<br/>Cette stratégie permet de créer une liste de sites en mode Entreprise distincte pour Microsoft Edge. L’activation de cette stratégie remplace les paramètres de la stratégie «Utiliser la liste des sitesweb en mode Entreprise d’Internet Explorer», si l’option «Configurer l’intégration d’Internet Explorer» est activée. La désactivation ou la non-configuration de cette stratégie n’affecte pas le comportement par défaut de la stratégie «Configurer l’intégration d’Internet Explorer».
    > [!NOTE]
    > Il n’est pas obligatoire de configurer la stratégie Microsoft Edge. De nombreuses organisations l’utilisent comme remplacement, ce qui leur permet de cibler la Liste de Sites actuelle auprès de tous les utilisateurs disposant de la stratégie IE, et de cibler plus facilement une version mise à jour vers les pilotes utilisés avec la stratégie Microsoft Edge.

Pour plus d’informations sur les listes de sites en mode entreprise, consultez:

- [Utiliser Enterprise Mode Site List Manager](/internet-explorer/ie11-deploy-guide/use-the-enterprise-mode-site-list-manager)
- [Ajouter plusieurs sites à la liste des sites en mode Entreprise à l’aide d’un fichier et de l’outil Enterprise Mode Site List Manager (schéma v.2)](/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool).

### <a name="configure-using-the-use-the-enterprise-mode-ie-website-list-policy"></a>Configurer la stratégieUtiliser la liste des sitesweb en mode Entreprise IE

Le mode IE peut utiliser la stratégie existante qui configure la Liste des Sites d’Entreprise dans Internet Explorer, ce qui vous permet de créer et de gérer une seule liste.

1. Créer ou réutiliser une liste de sites XML
    1. Tous les sites qui ont l’élément _\<open-in\>IE11\</open-in\>_ s’ouvrent désormais en modeIE.
2. Ouvrez l’Éditeur de stratégie de groupe.
3. Cliquez sur **Configuration ordinateur** > **Modèles d’administration** > **Composants Windows** > **Internet Explorer**.
4. Double-cliquez sur **Utiliser la liste des sitesweb en modeEntreprise d’Internet Explorer**.
5. Sélectionnez **Activé**.
6. Sous **Options**, tapez l’emplacement de la liste des sites web. Vous pouvez utiliser l’un des emplacements suivants:
    - (Recommandé) Emplacement HTTPS: **https**:**//iemode/sites.xml**
    - Fichier de réseau local: **\\\network\shares\sites.xml**
    - Fichier local: **file:///c:/Users/\<user\>>/Documents/sites.xml**
7. Cliquez sur **OK** ou **Appliquer** pour enregistrer ces paramètres.

### <a name="configure-using-the-configure-the-enterprise-mode-site-list-policy"></a>Configurer l’utilisation de la stratégie Configurer la Liste des Sites en Mode Entreprise

Vous pouvez également configurer le mode IE avec une stratégie distincte pour Microsoft Edge. Cette stratégie supplémentaire vous permet de remplacer la liste des sites IE. Par exemple, certaines organisations destinent la liste de sites de production à tous les utilisateurs. Vous pouvez ensuite déployer la liste des sites pilotes vers un petit groupe d’utilisateurs à l’aide de cette stratégie.

1. Créer ou réutiliser une liste de sites XML
    1. Tous les sites qui ont l’élément _\<open-in\>IE11\</open-in\>_ s’ouvrent désormais en modeIE.
2. Ouvrez l’Éditeur de stratégie de groupe.
3. Cliquez sur **Configuration ordinateur** > **Modèles d’administration** > **MicrosoftEdge**.
4. Double-cliquez sur **Configurer la liste des sites en mode Entreprise**.
5. Sélectionnez **Activé**.
6. Sous **Options**, tapez l’emplacement de la liste des sites web. Vous pouvez utiliser l’un des emplacements suivants:
    - (Recommandé) Emplacement HTTPS: **https**:**//iemode/sites.xml** <!--Trying to keep this from being an active link in MD -->
    - Fichier de réseau local: **\\\network\shares\sites.xml**
    - Fichier local: **file:///c:/Users/\<user\>>/Documents/sites.xml**
7. Cliquez sur **OK** ou **Appliquer** pour enregistrer ces paramètres.

### <a name="configure-all-intranet-sites"></a>Configurer tous les sites intranet

Le mode IE peut être configuré comme pour tous les sites dans la zone Intranet local. Vous pouvez supprimer des sites individuels du mode IE à l’aide d’une liste de sites en Mode Entreprise.

>[!NOTE]
>
> La zone Intranet local contient des sites ajoutés explicitement, mais affecte aussi les sites à cette zone à l’aide d’une méthode heuristique. Il peut s’agir de noms d’hôtes ne contenant pas de point (par exemple, **https**:**//salaire**) et de sites que le script de configuration proxy configure pour ignorer le proxy. Si une partie externe contrôle le DNS ou proxy, elle peut éventuellement forcer des sites web en mode IE.

1. Ouvrez l'Éditeur d'objets de stratégie de groupe.
2. Cliquez sur **Configuration ordinateur** > **Modèles d’administration** > **MicrosoftEdge**.
3. Double-cliquez sur **Envoyer tous les sites intranet vers InternetExplorer**.
4. Sélectionnez **Activé**, puis cliquez sur **OK** ou sur **Appliquer** pour enregistrer les paramètres de stratégie.

## <a name="redirect-sites-from-ie-to-microsoft-edge"></a>Rediriger des sites IE vers Microsoft Edge

Vous pouvez empêcher vos utilisateurs d’utiliser Internet Explorer pour les sites qui n’en ont pas besoin. Internet Explorer peut rediriger automatiquement les sites vers Microsoft Edge s’ils ne figurent pas dans votre liste de sites.

1. Ouvrez l’Éditeur de stratégie de groupe.
2. Cliquez sur **Configuration ordinateur** > **Outils d’administration** > **Composants Windows** > **Internet Explorer**.
3. Doublez-cliquez sur **Envoyer tous les sites non inclus dans la Liste des sites en mode Entreprise à Microsoft Edge**.
4. Sélectionnez **Activé**
5. Cliquez sur **OK** ou **Appliquer** pour enregistrer ces paramètres.
6. Double-cliquez sur **Configurer le canal de Microsoft Edge à utiliser pour ouvrir les sites redirigés**.
7. Sélectionnez **Activé**.
8. Sous **Options**, sélectionnez les trois principaux choix pour le canal à utiliser – Internet Explorer redirigera vers le choix le plus élevé que l’utilisateur a installé sur cet appareil:
   - Microsoft Edge Stable
   - Microsoft Edge Bêta version 77 ou ultérieure
   - Microsoft Edge Dev version 77 ou ultérieure
   - Microsoft Edge Canary version 77 ou ultérieure
   - Microsoft Edge version 45 ou précédente
9. Cliquez sur **OK** ou **Appliquer** pour enregistrer ces paramètres.

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [À propos du mode Internet Explorer](./edge-ie-mode.md)
- [Informations supplémentaires sur le mode entreprise](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)