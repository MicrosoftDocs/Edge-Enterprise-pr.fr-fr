---
title: Guide pas à pas pour la découverte de site d’entreprise
ms.author: collw
author: appcompatguy
manager: saudm
ms.date: 05/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Utiliser la découverte de site d’entreprise pour préparer le mode IE
ms.openlocfilehash: f6298b801cceeb96d9285f3597de2a6abe8ee36e
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617474"
---
# <a name="enterprise-site-discovery-step-by-step-guide"></a>Guide pas à pas pour la découverte de site d’entreprise

>[!Note]
> L’application de bureau Internet Explorer11 sera retirée et ne sera plus prise en charge le 15juin2022 (pour obtenir la liste des applications dans l’étendue, [consultez le FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Les mêmes applications et sites Internet Explorer11 que vous utilisez aujourd’hui peuvent s’ouvrir dans MicrosoftEdge en mode Internet Explorer. [Plus d'informations ici](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Cet article fournit un guide pas à pas sur l’utilisation de la découverte de site d’entreprise avec Microsoft Endpoint Configuration Manager.

La découverte de site d’entreprise peut vous aider à configurer votre liste de sites en mode entreprise. La découverte de site d’entreprise vous permet d’effectuer les opérations suivantes:

- Découvrir les sites qui utilisent des modes de documents hérités. À moins que ces sites ne détectent des navigateurs modernes et fournissent des codes HTML différents, ils doivent probablement utiliser le mode IE.
- Découvrir les sites qui utilisent des contrôles ActiveX. Microsoft Edge ne prend pas en charge les contrôles ActiveX. À moins que ces sites ne détectent des navigateurs modernes et fournissent des codes HTML différents, ils doivent probablement utiliser le mode IE.

> [!NOTE]
> Cet article concerne les canaux MicrosoftEdge **stable**, **Beta** et **Dev**, version77 ou ultérieures.

## <a name="prerequisites"></a>Conditions préalables

Ce guide part du principe que vous avez de l'expérience dans l'utilisation de Microsoft Endpoint Configuration Manager et que les services et rôles suivants sont installés :

1. Microsoft Endpoint Configuration Manager
2. Microsoft SQL Server Reporting Services
3. (Facultatif) Configuration du rôle Point de Reporting Services du Gestionnaire de configuration

## <a name="download-enterprise-site-discovery-tools"></a>Télécharger les outils de découverte de site d’entreprise

Télécharger les outils suivants:

- [Configuration de la découverte de site d’entreprise et package de configuration](https://go.microsoft.com/fwlink/p/?LinkId=517719)
- [Générateur de rapports Microsoft](https://www.microsoft.com/download/details.aspx?id=53613)

## <a name="enable-enterprise-site-discovery"></a>Activer la découverte de site d’entreprise

Avant de pouvoir vous connecter à Windows Management Instrumentation (WMI) pour récupérer les données de découverte de site, vous devez commencer par déployer le fournisseur de classes WMI sur l’appareil.

Dans la rubrique **Configuration de la découverte de site d’entreprise et package de configuration**, extrayez le contenu vers un dossier dans le partage de fichiers de la bibliothèque logicielle définitive. Exemple : **\\\\DSL\\EnterpriseSiteDiscovery**.

Créez ensuite un package dans Microsoft Endpoint Configuration Manager, comme décrit dans la [documentation](/configmgr/apps/deploy-use/packages-and-programs), en sélectionnant les options suivantes:

- Dans la page **Package**, sélectionnez **Nom** et spécifiez le nom **Activer la découverte de site**
- Dans la page **Package**, sélectionnez **Ce package contient des fichiers source**
- Dans la page **Package**, spécifiez le dossier source dans lequel vous avez extrait les fichiers (par exemple, **\\\\DSL\\EnterpriseSiteDiscovery**)
- Dans la page **Type de programme**, choisissez **Programme standard**
- Dans la page **Programme standard**, entrez la ligne de commande pour configurer la découverte de site sur l’appareil comme suit:
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1
  ```
  > [!NOTE]
  > Le script prend en charge l’utilisation des commutateurs de ligne de commande pour `-ZoneAllowList` et `-SiteAllowList`. Pour ce pas à pas, nous allons configurer ces options via la stratégie de groupe (ci-dessous).
- Dans la page **Programme standard**, sélectionnez l’option pour exécuter **Masquée**.
- Dans la page **Programme standard**, sous **Le programme peut s'exécuter**, sélectionnez l’option **Connexion ou non d'un utilisateur**

Après la création du package, double-cliquez sur le nom du package **Activer la découverte de site** pour afficher ses propriétés. Dans la propriété **Après l’exécution**, sélectionnez **Le gestionnaire de configuration redémarre l'ordinateur**. La collecte de données WMI commence après le redémarrage des appareils.

> [!NOTE]
> Vous pouvez configurer le temps dont dispose un utilisateur pour redémarrer l'appareil comme décrit dans la [documentation des paramètres du client](/configmgr/core/clients/deploy/about-client-settings#computer-restart).

## <a name="configure-enterprise-site-discovery-via-group-policy"></a>Configurer la découverte de site d’entreprise via la stratégie de groupe

Lorsque la découverte de site d’entreprise est activée, vous pouvez configurer les données à collecter. Tenez compte de la législation locale et des exigences réglementaires décrites [ici](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery#what-data-is-collected).

1. Ouvrez l’Éditeur de stratégie de groupe
2. Cliquez sur **Configuration ordinateur** > **Modèles d’administration** > **Composants Windows** > **Internet Explorer** 
3. Double-cliquez sur **Activer la sortieWMI de découverte de site**
4. Sélectionnez **Activé**
5. Cliquez sur **OK** ou sur **Appliquer** pour enregistrer ce paramètre de stratégie

Vous pouvez limiter les zones dans lesquelles vous collectez les données de site:

1. Double-cliquez sur **Limiter la sortie de découverte de site par zone**
2. Sélectionnez **Activé**
3. Entrez un masque de bits indiquant les zones pour lesquelles activer la découverte de site :
    1. Zone Sites sensibles
    2. ZoneInternet
    3. Zone Sites de confiance
    4. Zone Intranet local
    5. Zone Ordinateur local
    
    Exemple 1: **00010** recueille les données pour la zone Intranet local uniquement

    Exemple 2: **10111** recueille les données pour toutes les zones, à l'exception de la zone Internet
4. Cliquez sur **OK** ou sur **Appliquer** pour enregistrer ce paramètre de stratégie

Vous pouvez limiter les zones pour lesquelles vous collectez les données de site:

1. Double-cliquez sur **Limiter la sortie de découverte de site par domaine**
2. Sélectionnez **Activé**
3. Entrez les domaines pour lesquels vous souhaitez collecter des données, un domaine par ligne
4. Cliquez sur **OK** ou sur **Appliquer** pour enregistrer ce paramètre de stratégie

## <a name="collect-site-discovery-data-using-configuration-manager"></a>Collecter des données de découverte de site à l’aide du Gestionnaire de configuration

À présent que vos appareils génèrent des données, vous pouvez collecter ces données dans le Gestionnaire de configuration.

1. Dans la console Gestionnaire de configuration, sélectionnez **Administration** > **Paramètres du client** > **Paramètres du client par défaut**
2. Sous l'onglet **Accueil**, dans le groupe **Propriétés**, choisissez **Propriétés**
3. Dans la boîte de dialogue **Paramètres du client par défaut**, choisissez **Inventaire matériel**
4. Dans la liste **Paramètres du périphérique**, choisissez **Définir des classes**
5. Dans la boîte de dialogue **Classes d'inventaire matériel**, choisissez **Ajouter**
6. Dans la boîte de dialogue **Ajouter une classe d'inventaire matériel**, cliquez sur **Se connecter**
7. Dans la boîte de dialogue **Se connecter à Windows Management Instrumentation (WMI)**, entrez le nom d’un ordinateur sur lequel est configurée la découverte de site d’entreprise. Si vous vous connectez à un autre ordinateur, vous devez disposer des informations d’identification avec l’autorisation d’accès à WMI.
8. Dans la zone de texte **Espace de noms WMI**, entrez **root\cimv2\IETelemetry**
9. Choisissez **Se connecter**
10. Dans la boîte de dialogue **Ajouter une classe d’inventaire matériel**, dans la liste **Classes d’inventaire**, sélectionnez les classes WMI **IESystemINfo**, **IEUrlInfo** et **IECountInfo*.
11. Cliquez sur **OK** pour fermer la boîte de dialogue **Qualificateurs de classe** et les autres boîtes de dialogue ouvertes.

Une fois que le client a mis à jour les paramètres à partir du point de gestion, les données sont signalées lors de l’exécution du prochain inventaire matériel (par défaut, tous les sept jours).

## <a name="import-site-discovery-reports"></a>Importer des rapports de découverte de site

Le package de découverte de site d’entreprise inclut deux exemples de rapports. Un rapport affiche les sites utilisant des contrôles ActiveX, tandis qu’un autre affiche les sites utilisant des modes de documents hérités.

### <a name="configure-the-site-discovery-sample-report"></a>Configurer l’exemple de rapport de découverte de site

Pour créer un exemple de rapport qui utilise trois sources de données, utilisez la procédure suivante: les sites visités par les utilisateurs, les informations sur leur système et les modes de document utilisés par les sites. Ce rapport vous permet d’identifier les sites susceptibles de dépendre des modes de documents hérités.

1. Copiez le rapport **SCCM_Report-Site_Discovery.rdl** sur votre serveur Gestionnaire de configuration.
2. Installer le [Générateur de rapports Microsoft](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15).
3. Double-cliquez sur **SCCM_Report Site_Discovery.rdl** pour ouvrir le rapport dans le Générateur de rapports.
4. La première fois que vous essayez d’ouvrir le rapport, celui-ci tente de contacter le serveur où il a été créé. Lorsque le système affiche l'invite **Se connecter au serveur de rapports**, cliquez sur **Non**.
5. Une fois le rapport ouvert, développez **Sources de données**, puis double-cliquez sur **DataSource1**.
6. Dans la fenêtre **Propriétés de source de données**, sélectionnez **Utiliser une connexion incorporée dans mon rapport**, puis cliquez sur le bouton **Générer...**.
7. Dans la fenêtre **Propriétés de connexion**, sélectionnez **Nom du serveur**, puis entrez le nom du serveur Gestionnaire de configuration. Ensuite dans **Sélectionner ou entrer un nom de base de données**, sélectionnez le nom de la base de données du Gestionnaire de configuration dans la liste déroulante.
8. Cliquez sur **OK** pour fermer la fenêtre **Propriétés de connexion**.
9. Cliquez sur **Tester la connexion** pour tester la connexion. Si la connexion est établie, cliquez sur **OK** pour fermer la fenêtre **Propriétés de source de données**.
10. Répétez les étapes5 à 9 pour **Source de données 2**.
11. Développez **Jeux de données**, puis double-cliquez sur **Jeu de données 1**.
12. Dans la fenêtre **Propriétés de jeu de données**, cliquez dans la zone de texte **Requête :**, puis remplacez **UTILISER CM_A1B** par le nom de la base de données que vous avez sélectionné à l’étape 7.
13. Répétez les étapes 11 à 12 pour **Jeu de données 2**, **Jeu de données 3** et **Jeu de données 4**.
14. Dans l’onglet **Accueil** du ruban, cliquez sur le bouton **Exécuter** pour tester le rapport.
15. Enregistrez le rapport.
16. Fermez le générateur de rapports Microsoft.
17. Renommez le fichier en **Site Discovery.rdl**

### <a name="configure-the-activex-sample-report"></a>Configurer l’exemple de rapport ActiveX

Pour créer un exemple de rapport qui utilise une seule source de données, utilisez la procédure suivante: les sites qui utilisent des contrôles ActiveX. Dans la mesure où Internet Explorer est le seul navigateur qui prend en charge les contrôles ActiveX, ces sites peuvent nécessiter le mode IE.

1. Copiez le rapport **Exemple de rapport SCCM – ActiveX.rdl** sur votre serveur Gestionnaire de configuration.
2. Installer le [Générateur de rapports Microsoft](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15).
3. Double-cliquez sur **Exemple de rapport SCCM – ActiveX.rdl** pour ouvrir le rapport dans le Générateur de rapports.
4. La première fois que vous essayez d’ouvrir le rapport, celui-ci tente de contacter le serveur où il a été créé. Lorsque le système affiche l'invite **Se connecter au serveur de rapports**, cliquez sur **Non**.
5. Après l’ouverture du rapport, développez **Sources de données**, puis double-cliquez sur **AutoGen__5C6358F2_4BB6_4a1b_A16E_8D96795D8602_**.
6. Dans la fenêtre **Propriétés de source de données**, sélectionnez **Utiliser une connexion incorporée dans mon rapport**, puis cliquez sur le bouton **Générer...**.
7. Dans la fenêtre **Propriétés de connexion**, sélectionnez **Nom du serveur**, puis entrez le nom du serveur Gestionnaire de configuration. Ensuite dans **Sélectionner ou entrer un nom de base de données**, sélectionnez le nom de la base de données du Gestionnaire de configuration dans la liste déroulante.
8. Cliquez sur **OK** pour fermer la fenêtre **Propriétés de connexion**.
9. Cliquez sur **Tester la connexion** pour tester la connexion. Si la connexion est établie, cliquez sur **OK** pour fermer la fenêtre **Propriétés de source de données**.
10. Développez **Jeux de données**, puis double-cliquez sur **Jeu de données 1**.
11. Dans la fenêtre **Propriétés de jeu de données**, cliquez dans la zone de texte **Requête :**, puis remplacez **UTILISER CM_A1B** par le nom de la base de données que vous avez sélectionné à l’étape 7.
12. Dans l’onglet **Accueil** du ruban, cliquez sur le bouton **Exécuter** pour tester le rapport.
13. Enregistrez le rapport.
14. Fermez le générateur de rapports Microsoft.
15. Renommez le fichier en **ActiveX**

### <a name="upload-configured-reports-to-microsoft-sql-server-reporting-services"></a>Charger des rapports configurés dans Microsoft SQL Server Reporting Services

Une fois que vous avez configuré les rapports pour votre environnement, chargez-les sur le serveur de rapports.

1. Lancez l’application **Reporting Services Configuration Manager**.
2. Dans la fenêtre **Connexion au serveur de rapports**, cliquez sur **Se connecter**, puis sur l’URL figurant dans la liste sous **Identification de site du portail Web**
3. Dans la fenêtre du navigateur qui s’ouvre, vous devez vous trouver dans la **Page SQL Server Reporting Services** – cliquez sur le dossier **ConfigMgr_SCCMSiteCode** pour votre code de site SCCM.
4. Dans le ruban, placez le pointeur de la souris sur **+ Nouveau**, puis cliquez sur l’élément de menu **Dossier**.
5. Entrez un nom de dossier, tel que **Découverte de site d’entreprise**, puis cliquez sur le bouton **Créer**.
6. Cliquez sur le dossier **Découverte de site d’entreprise**.
7. Dans le ruban, cliquez sur le bouton **Charger**.
8. Sélectionnez le rapport **Découverte de site**, puis cliquez sur **OK**.
9. Répétez les étapes7 et 8 pour le rapport **ActiveX**.

### <a name="view-reports-in-configuration-manager"></a>Afficher les rapports dans le Gestionnaire de configuration

À présent que vous avez personnalisé et chargé les rapports, vous pouvez les afficher dans le Gestionnaire de configuration.

1. Dans la console Gestionnaire de configuration, sélectionnez **Surveillance** > **Création de rapports** > ** Rapports** > **Découverte de site d’entreprise**
2. Double-cliquez sur un rapport pour l’afficher.

## <a name="disable-enterprise-site-discovery"></a>Désactiver la découverte de site d’entreprise

Lorsque vous avez terminé la collecte des données, désactivez la découverte de site d’entreprise. Créez un deuxième package pour désactiver la découverte de site d’entreprise dans Microsoft Endpoint Configuration Manager, comme décrit dans la [documentation](/configmgr/apps/deploy-use/packages-and-programs), en sélectionnant les options suivantes:

- Dans la page **Package**, sélectionnez **Nom** et spécifiez le nom **Désactiver la découverte de site**
- Dans la page **Package**, sélectionnez **Ce package contient des fichiers source**
- Dans la page **Package**, spécifiez le dossier source dans lequel vous avez extrait les fichiers (par exemple, **\\\\DSL\\EnterpriseSiteDiscovery**)
- Dans la page **Type de programme**, choisissez **Programme standard**
- Dans la page **Programme standard**, entrez la ligne de commande qui désactive la découverte de site sur l’appareil comme suit:
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1 -IEFeatureOff
  ```
- Dans la page **Programme standard**, sélectionnez l’option pour exécuter **Masquée**
- Dans la page **Programme standard**, sous **Le programme peut s'exécuter**, sélectionnez l’option **Connexion ou non d'un utilisateur**

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [À propos du mode Internet Explorer](./edge-ie-mode.md)
- [Informations supplémentaires sur le mode entreprise](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Informations supplémentaires concernant la découverte de site d’entreprise](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery)