---
title: Notes de publication de Microsoft Edge pour le canal bêta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/15/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notes de publication de Microsoft Edge pour le canal bêta
ms.openlocfilehash: 99ec3764d433906dcf45e851c7bc62d4ec2483fa
ms.sourcegitcommit: 3bafa63c17f01fcec60d6297474a6a391034a8be
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/15/2021
ms.locfileid: "11271203"
---
# Notes de publication du canal Microsoft Edge Beta

Ces notes de publication fournissent des informations sur les nouvelles fonctionnalités et les mises à jour non liées à la sécurité qui sont incluses dans le canal Microsoft Edge Beta. Les versions archivées de ces notes de publication sont disponibles [ici](microsoft-edge-relnote-archive-beta-channel.md).

## Version 88.0.705.45 : 15 janvier

Résolution de divers bogues et problèmes de performances.

## Version 88.0.705.41 : 11 janvier

Résolution de divers bogues et problèmes de performances.

## Version 88.0.705.29 : 21 décembre

Résolution de divers bogues et problèmes de performances.

<!-- begin major 88 -->
## Version88.0.705.18: 9décembre

### Mises à jour des fonctionnalités

- **Fonctionnalités obsolètes:**

  - Prise en charge du protocole FTP obsolète. La prise en charge du protocole FTP hérité a été supprimée de Microsoft Edge. Toute tentative d’accès à un lien FTP entraînera l’ouverture par le système d’exploitation d’une application externe pour gérer le lien FTP. Une autre solution pour les administrateurs informatiques consiste à configurer Microsoft Edge afin qu’il utilise le mode IE pour les sites qui dépendent du protocole FTP.
  - La prise en charge d’Adobe Flash sera supprimé. À partir de la version88 de Microsoft Edge Beta, la fonctionnalité et la prise en charge d’Adobe Flash seront supprimées. Pour en savoir plus: [Mise à jour concernant la fin de la prise en charge d’Adobe Flash Player – Blog Microsoft Edge (Windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentification:**

  - L’authentification unique (SSO) est désormais disponible pour les comptes Azure Active Directory (Azure AD) et le compte Microsoft (MSA) sur macOS et les versions inférieures de Windows. Un utilisateur connecté à Microsoft Edge sur macOS ou Microsoft Windows de version inférieure (7 et 8.1) est désormais connecté automatiquement aux sites web configurés pour autoriser l’authentification unique avec des comptes professionnels et Microsoft (par exemple, bing.com, office.com, msn.com, outlook.com).<br>Remarque: il est possible que l’utilisateur doive se déconnecter et se reconnecter s’il se connecte à une version antérieure à la version88 de Microsoft Edge pour utiliser cette fonctionnalité.
  - Basculer automatiquement les utilisateurs sur macOS vers leur profil de travail pour les sites qui s’authentifient avec leur compte professionnel. À partir de la version88 de Microsoft Edge, nous offrons la possibilité de basculer entre les sites qui s’authentifient avec le profil de travail de l’utilisateur sur macOS.<br>Remarque: il est possible que l’utilisateur doive se déconnecter et se reconnecter s’il se connecte à une version antérieure à la version88 de Microsoft Edge pour utiliser cette fonctionnalité.

- Option du mode plein écran pour terminer la session. Le bouton Mettre fin à la session est désormais disponible en mode plein écran de navigation publique. Cette fonctionnalité permet de supprimer les données et paramètres du navigateur lorsque Microsoft Edge est fermé. Pour en savoir plus sur les fonctionnalités et la feuille de route du mode plein écran, voir [Configurer le mode plein écran Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).

- **Sécurité et confidentialité:**

  - Des alertes sont générées si le mot de passe d’un utilisateur est détecté dans une fuite en ligne. Les mots de passe des utilisateurs sont examinés par rapport à un référentiel d’informations d’identification connues qui ont été divulguées et envoient à l’utilisateur une alerte si une correspondance est trouvée. Pour garantir la sécurité et la confidentialité, les mots de passe des utilisateurs sont hachés et chiffrés lorsqu’ils sont vérifiés par rapport à la base de données des informations d’identification divulguées.
  - Mettre automatiquement à niveau le contenu mixte. Les pages sécurisées fournies via HTTPS peuvent contenir des images de référence fournies via HTTP non sécurisé. Pour améliorer la confidentialité et la sécurité dans Microsoft Edge88, ces images seront récupérées via HTTPS. Si l’image n’est pas disponible via HTTPS, elle n’est pas chargée.
  - Afficher les autorisations de site par site et par activité récente. À partir de Microsoft Edge88, les utilisateurs peuvent gérer plus facilement les autorisations de site. Ils peuvent afficher les autorisations par site web, et non plus seulement par type d’autorisation. Par ailleurs, nous avons ajouté une section activité récente qui permettra à l’utilisateur d’afficher les dernières modifications apportées à ses autorisations de site.
  - Amélioration des contrôles pour les cookies du navigateur. À partir de Microsoft Edge88, les utilisateurs peuvent supprimer des cookies tiers sans affecter les cookies de première partie. Les utilisateurs peuvent également filtrer leurs cookies selon s’il s’agit d’une première ou tierce partie et les trier en fonction du nom, du nombre de cookies, de la quantité de données stockées et de la dernière modification.

- **Performance:**

  - Améliorez les performances du navigateur grâce aux onglets en veille. Les onglets en veille améliorent les performances du navigateur en mettant les onglets inactifs en veille pour libérer des ressources système, telles que la mémoire et le processeur de sorte que les onglets actifs ou d’autres applications puissent les utiliser. Les utilisateurs peuvent empêcher la mise en veille de sites et configurer le délai avant qu’un onglet inactif ne soit mis en veille. Pour ne pas gêner les utilisateurs dans leur travail, il est également possible de faire en sorte que certains sites ne soient pas mis en veille, tels que les sites intranet. Cette fonctionnalité est limitée à un groupe d’utilisateurs sélectionnés de manière aléatoire et ayant activé l’expérimentation. Nous envisageons de faire en sorte que les onglets en veille soient activés par défaut avec MicrosoftEdge version89. Cette fonctionnalité peut être gérée avec des stratégies de groupe.
  - Améliorez la vitesse de démarrage de Microsoft Edge avec l’Accélérateur de démarrage. Pour améliorer la vitesse de démarrage de Microsoft Edge, nous avons conçu une fonctionnalité appelée Accélérateur de démarrage. L’Accélérateur de démarrage accélère le lancement en permettant à Microsoft Edge de s’exécuter en arrière-plan. Remarque: cette fonctionnalité est limitée à un groupe d’utilisateurs sélectionnés de manière aléatoire et ayant activé l’expérimentation. Ces utilisateurs donnent des commentaires à l’équipe chargée de la fonctionnalité.

- **Productivité:**

  - Améliorez votre productivité et le travail multitâche grâce aux onglets verticaux. À mesure que vous ajoutez des onglets horizontaux, les titres de site sont tronqués et les commandes des onglets perdent en visibilité. Cela interrompt le flux de travail de l’utilisateur, car il passe plus de temps à rechercher, à passer de l’un à l’autre et à gérer ses onglets, et moins de temps sur la tâche en cours. Les onglets verticaux permettent aux utilisateurs de déplacer leurs onglets vers le côté, là où les icônes alignées à la verticale et les titres de sites plus longs permettent de jeter un coup d’œil rapide pour identifier l’onglet que vous voulez ouvrir et basculer vers celui-ci.
  - Remplissage automatique du champ de date de naissance. Microsoft Edge vous permet d’économiser du temps et de l’énergie lors du remplissage des formulaires et de la création de comptes en ligne à l’aide de la saisie semi-automatique des données utilisateur, telles que les adresses, les noms, les numéros de téléphone, etc. Microsoft Edge prend désormais en charge le champ Date de naissance que les utilisateurs peuvent enregistrer et remplir automatiquement. Un utilisateur peut afficher, modifier et supprimer ces informations à tout moment dans ses paramètres de profil.
  - Améliorations apportées à l’historique Récemment fermés. L’historique Récemment fermés conserve désormais les 25derniers onglets et fenêtres de n’importe quelle session de navigation, et non plus seulement la session précédente. Les utilisateurs peuvent sélectionner Récemment fermés dans la nouvelle expérience d’Historique pour afficher tous les onglets qui ont été ouverts.
  - Fonction «votre journée en un clin d’œil» activée par défaut. À partir de la version88 de MicrosoftEdge, les travailleurs de l’information peuvent bénéficier de fonctionnalités de productivité intelligentes sur leur page Nouvel onglet (NTP). Nous offrons aux utilisateurs qui sont connectés à l’aide de leur compte professionnel ou scolaire du contenu pertinent optimisé par leur M365Graph. Les utilisateurs peuvent rapidement parcourir leurs modules «votre journée en un clin d’œil» pour suivre facilement leurs réunions et leurs activités récentes, et lancer rapidement les applications qu’ils souhaitent utiliser.

- **PDF:**

  - Affichage d’un document PDF en mode livre (deux pages) À partir de la version88 de Microsoft Edge, les utilisateurs peuvent consulter des documents PDF en affichage à une ou deux pages (mode livre). Pour modifier l’affichage, cliquez sur le bouton **Mode Page** dans la barre d’outils.
  - Prise en charge des notes de texte ancré pour les fichiers PDF. À partir de la version87 de Microsoft Edge, les utilisateurs peuvent ajouter des notes de texte tapées sur n’importe quelle portion de texte dans des fichiers PDF.
  - Expérience de sélection de texte plus fluide dans les documents PDF. Les utilisateurs bénéficient d’une expérience de sélection de texte plus fluide et cohérente sur les documents PDF ouverts dans Microsoft Edge.
  - Afficher les pages web enregistrées en tant que fichiers PDF dans la barre Téléchargements. Les utilisateurs peuvent désormais afficher les fichiers PDF générés en définissant Enregistrer en tant que PDF comme destination d’impression des pages web dans la barre Téléchargements.

- **Polices:**

  - Les icônes du navigateur sont mises à jour dans le système Fluent Design. Dans le cadre de nos efforts continus en termes de Fluent Design dans le navigateur, nous avons apporté des modifications de façon à aligner davantage les icônes sur le nouveau système d’icônes Microsoft. Ces modifications peuvent avoir une incidence sur un grand nombre de nos interfaces utilisateur avec une interaction tactile importante, y compris les onglets, la barre d’adresses, ainsi que les icônes de navigation et de recherche d’itinéraire dans nos différents menus.
  - Amélioration du rendu des polices. Le rendu du texte est amélioré pour améliorer la clarté et réduire le flou.

### Mises à jour de stratégies

#### Nouvelles stratégies

16nouvelles stratégies ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://www.microsoft.com/edge/business/download). Les nouvelles stratégies suivantes ont été ajoutées.

- [BlockExternalExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#blockexternalextensions): empêche l’installation d’extensions externes.
- [InternetExplorerIntegrationLocalFileAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileallowed): autorise le lancement de fichiers locaux en mode Internet Explorer.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist): ouvre les fichiers locaux dans la liste verte des extensions de fichier en mode Internet Explorer.
- [InternetExplorerIntegrationLocalFileShowContextMenu](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileshowcontextmenu): afficher le menu contextuel pour ouvrir un lien en mode Internet Explorer.
- [IntranetRedirectBehavior](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intranetredirectbehavior): comportement de la redirection intranet.
- [PrinterTypeDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printertypedenylist): désactive les types d’imprimante dans la liste d’exclusion.
- [ShowMicrosoftRewards](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showmicrosoftrewards): affiche les expériences Microsoft Rewards.
- [SleepingTabsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsenabled): configure les onglets en veille.
- [SleepingTabsTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabstimeout): définit le délai d’inactivité des onglets en arrière-plan avant qu’ils ne soient mis en veille.
- [SleepingTabsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsblockedforurls): bloque les onglets en veille sur des sites spécifiques.
- [StartupBoostEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#startupboostenabled): active l’accélérateur de démarrage.
- [UpdatePolicyOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#updatepolicyoverride): indique comment Microsoft Edge Update gère les mises à jour disponibles à partir de Microsoft Edge.
- [VerticalTabsAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#verticaltabsallowed): configure la disponibilité de la disposition verticale pour les onglets situés sur le côté du navigateur.
- [WebRtcAllowLegacyTLSProtocols](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtcallowlegacytlsprotocols): autorise le passage à une version antérieure héritée de TLS/DTLS dans WebRTC.

#### Stratégies déconseillées

Les stratégies suivantes sont déconseillées.

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled): active l’authentification proactive.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist): configure les règles de contournement du proxy.
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode): configure les paramètres du serveur proxy.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl): définit l’URL du fichier proxy .pac.
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver): configure l’adresse ou l’URL du serveur proxy.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies): autorise WebDriver à remplacer les stratégies incompatibles.

#### Stratégies obsolètes

Les stratégies suivantes sont obsolètes.

- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting): paramètre Adobe Flash par défaut.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls): autorise le plug-in Adobe Flash sur des sites spécifiques.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls): bloque le plug-in Adobe Flash sur des sites spécifiques.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode): étend le paramètre de contenu Adobe Flash à l’ensemble du contenu.

<!-- end major 88 -->

## Version87.0.664.55: 3décembre

Résolution de divers bogues et problèmes de performances. La nouvelle fonctionnalité suivante est prise en charge dans cette version.

- **Des alertes sont générées si le mot de passe d’un utilisateur est détecté dans une fuite en ligne**. Les mots de passe des utilisateurs sont examinés par rapport à un référentiel d’informations d’identification connues qui ont été violées et envoient à l’utilisateur une alerte si une correspondance est trouvée. Pour garantir la sécurité et la confidentialité, les mots de passe des utilisateurs sont chiffrés et cryptés lorsqu’ils sont vérifiés par rapport à la base de données des informations d’identification divulguées.

## Version 87.0.664.52: 30novembre

Résolution de divers bogues et problèmes de performances.

## Version 87.0.664.40: 18 novembre

Résolution de divers bogues et problèmes de performances.

## Version 87.0.664.36: 16 novembre

Résolution de divers bogues et problèmes de performances.

## Version 87.0.664.30: 9 novembre

Résolution de divers bogues et problèmes de performances.

## Version 87.0.664.24: 2 novembre

Résolution de divers bogues et problèmes de performances.

## Version87.0.664.18: 26octobre

Résolution de divers bogues et problèmes de performances.

<!-- begin major 87 -->
## Version87.0.664.12: 20octobre

### Mises à jour des fonctionnalités

- **Activation des fonctionnalités de confidentialité en mode plein écran**. Le démarrage des fonctionnalités du mode plein écran de Microsoft Edge version 87 qui permettront aux entreprises de respecter la confidentialité des données utilisateur, sera  activée. Ces fonctionnalités activent les expériences telles que l’effacement des données utilisateur à la fermeture, la suppression des fichiers téléchargés et la réinitialisation de l’expérience de démarrage configurée après une durée inactivité déterminée. En savoir plus sur la [Configuration du mode plein écran Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).
- **Activation du déploiement ClickOnce par défaut**. L’activation de ClickOnce par défaut dans Microsoft Edge 87, réduit les difficultés des entreprises à déployer des logiciels et mieux s’aligner sur le comportement du navigateur Microsoft Edge Legacy. Au démarrage de Microsoft Edge 87, l’état «Non Configuré» de la stratégie ClickOnceEnabled reflète le nouvel état par défaut Activé de la stratégie ClickOnce (comparé à l’État par défaut Désactivé précédent).
- **La page nouvel onglet de l’entreprise (NTP) intègre la productivité avec un contenu de flux de travail personnalisable**. La Page Nouvel Onglet de l’Entreprise combine la page de productivité d’Office 365 que nous proposons aux utilisateurs connectés à leur compte professionnel ou scolaire, avec des flux professionnels personnalisés qui sont organisés en une seule page. Les utilisateurs reconnaîtront le contenu Office 365 familier et Microsoft Search pour Entreprises offert par Bing. De plus, ils peuvent facilement retourner à «Mon Flux» personnalisable avec du contenu et des modules pertinents pour l’utilisateur, sa société ou son industrie, et à une sélection d’autres flux mis à disposition par l’organisation. [En savoir plus](https://docs.microsoft.com/microsoft-365/admin/manage/manage-industry-news?view=o365-worldwide&preserve-view=true).

- **Confidentialité et sécurité :**

  - Jeton TLS de support Obligatoire pour les sites configurés par une stratégie. Le jeton TLS obligatoire permet d’éviter les attaques par vol de jetons afin de s’assurer que les cookies ne peuvent pas être réutilisés à partir d’un autre appareil que l’appareil sur lequel ils ont été initialement définis. L’utilisation du jeton TLS obligatoire nécessite la définition de la stratégie [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) et nécessite que les sites répertoriés prennent en charge cette fonctionnalité.

- **Prise en charge du clavier pour le surligneur des fichiers PDF**. Les utilisateurs peuvent utiliser leurs touches de clavier pour surligner des textes de fichiers PDF.

- **Impression:**

  - Sélectionnez le côté à retourner lors de l’impression recto verso. Les utilisateurs peuvent choisir de retourner sur le côté long ou sur le côté court d’une feuille lors de l’impression recto verso.
  - Sélectionnez le mode de tramage de l’impression pour l’entreprise. Contrôlez l’impression Microsoft Edge sur une imprimante non-PostScript sur Windows. Parfois l’ impression sur des imprimantes non-PostScript doit être tramée pour imprimer correctement. Les options d’impression sont «Complètes» et «Rapides».

### Mises à jour de stratégies

#### Nouvelles stratégies

Ajout de dix nouvelles stratégies. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://www.microsoft.com/edge/business/download). Les nouvelles stratégies suivantes ont été ajoutées.

- [ConfigureFriendlyURLFormat](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configurefriendlyurlformat) - Configurez le format de collage par défaut des URL copiées à partir de Microsoft Edge, et déterminez si d’autres formats sont disponibles pour les utilisateurs.
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) - Activation des Achats dans Microsoft Edge.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hideinternetexplorerredirectuxforincompatiblesitesenabled) - Masquez la boite de dialogue redirection et la bannière sur Microsoft Edge.
- [KioskAddressBarEditingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) - Configurez la modification de la barre d’adresses pour l’expérience de navigation publique en mode plein écran.
- [KioskDeleteDownloadsOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) - Supprimez les fichiers téléchargés sous la session plein écran lorsque Microsoft Edge se ferme.
- [PasswordRevealEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordrevealenabled) - Activez le bouton d’affichage de mot de passe.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerpreventbhoinstall) - Empêchez l’installation BHO pour rediriger les sites incompatibles de Internet Explorer vers Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerredirectmode) - Redirigez les sites incompatibles de Internet Explorer vers Microsoft Edge.
- [SpeechRecognitionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#speechrecognitionenabled) - Configurez la Reconnaissance Vocale.
- [WebCaptureEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcaptureenabled) - Activez la fonctionnalité de capture web dans Microsoft Edge.

#### Stratégie Déconseillée

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) - Configurez l’expérience de la page nouvel onglet de Microsoft Edge.

#### Stratégie obsolète

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) - Réactivez les fonctionnalités de plateforme web déconseillées pour une période limitée.

<!-- end major 87 -->

## Version86.0.622.43: 16octobre

Résolution de divers bogues et problèmes de performances.

## Version86.0.622.36: 7octobre

Résolution de divers bogues et problèmes de performances.

## Version86.0.622.31: 1octobre

Résolution de divers bogues et problèmes de performances.

## Version 86.0.622.28: 28 septembre

Résolution de divers bogues et problèmes de performances.

## Version 86.0.622.15: 14 septembre

Résolution de divers bogues et problèmes de performances.

## Version 86.0.622.11: 9 septembre

### Mises à jour des fonctionnalités

* **Mode InternetExplorer:**

   * Permettre aux utilisateurs d’utiliser l’interface utilisateur de Microsoft Edge pour tester les sites en mode Internet Explorer. À partir de la version86 de Microsoft Edge, les administrateurs peuvent activer une option d'interface utilisateur pour que leurs utilisateurs puissent charger un onglet en mode Internet Explorer à des fins de test ou comme palliatif jusqu'à ce que les sites soient ajoutés à la liste XML des sites.

* **Supprimez les téléchargements à partir du disque à l’aide du gestionnaire de téléchargement.** Les utilisateurs peuvent désormais supprimer leurs fichiers téléchargés à partir de leur disque sans quitter le navigateur. La nouvelle fonctionnalité Supprimer les téléchargements figure dans le menu contextuel de l’étagère téléchargements ou de la page de téléchargement.

* **Revenir à la version précédente de Microsoft Edge.** La fonctionnalité de restauration permet aux administrateurs de revenir à une version correcte connue de Microsoft Edge s’il existe un problème dans la dernière version de Microsoft Edge.
[En savoir plus](edge-learnmore-rollback.md).

* **Appliquer l’activation de la synchronisation par défaut au sein de l’entreprise.**  Les administrateurs peuvent activer la synchronisation pour les comptes Azure Active Directory (Azure AD) par défaut avec la stratégie [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync) .

* **Mises à jour PDF:**

  * Table des matières des documents PDF. À partir de la version86, Microsoft Edge a ajouté la prise en charge de la table des matières qui permet aux utilisateurs de parcourir facilement les documents PDF.
  * Accédez à toutes les fonctionnalités de PDF sur les écrans compacts. Accédez à toutes les fonctionnalités du lecteur PDF Microsoft Edge sur les appareils disposant de petites tailles d’écran.
  * Prise en charge du stylet pour le surligneur des fichiers PDF. Avec cette mise à jour, les utilisateurs peuvent utiliser leur stylet numérique pour mettre en surbrillance directement du texte dans les fichiers PDF, de la même manière qu’avec un surligneur physique et du papier.
  * Défilement PDF amélioré. Vous pourrez désormais faire défiler les documents au format PDF long.

* **Changement automatique de profil sur Windows7, 8 et 8.1.** Le changement automatique de profil actuellement disponible dans Microsoft Edge sur Windows10 est étendu aux fenêtres de niveau inférieur (Windows7, 8 et 8.1). Pour plus d’informations, consultez le billet de blog [changement automatique de profil](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **Les suggestions de saisie semi-automatique s’affichent lorsque les utilisateurs commencent à taper une requête de recherche sur le site web des composants additionnels Microsoft Edge.** La saisie semi-automatique permet aux utilisateurs d’effectuer rapidement leur requête de recherche sans entrer l’intégralité de la chaîne. Ceci est utile, car les utilisateurs n’ont pas besoin de se souvenir des orthographes correctes, et peuvent choisir parmi les options disponibles qui s’affichent.

* **Supprimez l’API de cache de l’application HTML5.**  Depuis Microsoft Edge version86, l’API cache de l’application héritée qui permet d’utiliser en mode hors connexion des pages web est supprimée de Microsoft Edge. Les développeurs web doivent consulter la [documentation WebDev](https://web.dev/appcache-removal/) pour plus d’informations sur le remplacement de l’API cache de l’application avec les travailleurs de service.  Important: vous pouvez demander un [Jeton AppCache OriginTrial](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) qui permet aux sites de continuer à utiliser l’API de cache d’application déconseillée jusqu’à la version90 de Microsoft Edge.

* **Sécurité:**

  * Prise en charge de DNS sécurisé (DNS-HTTPs).  À partir de la version86 de Microsoft Edge, les paramètres de contrôle de DNS sécurisé sur les appareils non gérés sont disponibles. Ces paramètres ne sont pas accessibles aux utilisateurs sur les appareils gérés, mais les administrateurs informatiques peuvent activer ou désactiver le DNS sécurisé à l’aide de la stratégie de groupe [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode).


* **Ajoutez une image personnalisée à la nouvelle page d’onglet (NTP) à l’aide d’une stratégie de groupe.** À partir de la version 86 de Microsoft Edge, le protocole NTP offre une option permettant de remplacer l'image par défaut par une image personnalisée fournie par l'utilisateur. La possibilité de gérer les propriétés de cette image est également prise en charge par la stratégie de groupe.

* **Faites correspondre les raccourcis clavier personnalisés à VS Code.** MicrosoftEdgeDevTools prend désormais en charge la personnalisation des raccourcis clavier dans DevTools pour adapter à votre éditeur/IDE. (Dans MicrosoftEdge84, nous avons ajouté la possibilité de faire correspondre les raccourcis clavier DevTools à VSCode).

* **Remplacez les stratégies [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) et [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) pour les fenêtres de niveau inférieur et macOS.** Ces stratégies sont déconseillées dans Microsoft Edge version86 et deviendront obsolètes dans Microsoft Edge version89.<br>
Ces stratégies sont remplacées par [Autoriser la télémétrie](https://go.microsoft.com/fwlink/?linkid=2099569) sur Windows10, et la nouvelle stratégie [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) pour toutes les autres plateformes. Cela permet aux utilisateurs de gérer les données de diagnostic envoyées à Microsoft pour Windows7, 8, 8.1 et macOS.

* **SameSite = Lax cookies par défaut**. Pour améliorer la sécurité et la confidentialité sur le Web, les cookies s’affichent désormais par défaut [SameSite = Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite) gestion par défaut. Cela signifie que les cookies sont uniquement envoyés dans un contexte tiers et sont omis pour les demandes envoyées aux tiers. Cette modification peut avoir un impact sur les sites Web qui requièrent des cookies pour que les ressources tierces fonctionnent correctement. Pour autoriser de tels cookies, les développeurs Web peuvent marquer les cookies qui doivent être définis de et envoyés à des contextes tiers en ajoutant des attributs `SameSite=none` et `Secure` explicites lorsque le cookie est défini. Les entreprises qui souhaitent exempter certains sites de cette modification peuvent le faire à l’aide de la stratégie de [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist). Vous pouvez également désactiver la modification sur tous les sites à l’aide de la stratégie [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) .

### Mises à jour de stratégies

#### Nouvelles stratégies

Dix-neuf nouvelles stratégies ont été ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist) : Bloquer l’accès à une liste de services et de cibles d’exportation spécifiée dans Collections.
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting): paramètre par défaut des capteurs.
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting): contrôler l’utilisation de l’API Serial.
- [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata): envoyer les données de diagnostic requises et facultatives relatives à l’utilisation du navigateur.
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed): autoriser l’accès à l’outil Enterprise Mode Site List Manager.
- [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync): forcer la synchronisation des données du navigateur et ne pas afficher l’invite de consentement de synchronisation.
- [InsecureFormsWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecureformswarningsenabled): activer les avertissements pour les formulaires non sécurisés.
- [InternetExplorerIntegrationTestingAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed): autoriser le test du mode Internet Explorer.
- [SpotlightExperiencesAndRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#spotlightexperiencesandrecommendationsenabled): déterminer si les utilisateurs peuvent recevoir des images d’arrière-plan et du texte personnalisés, des suggestions, des notifications et des conseils pour les services Microsoft.
- [NewTabPageAllowedBackgroundTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageallowedbackgroundtypes): Définir les types d’arrière-plan autorisés pour la disposition du nouvel onglet.
- [SaveCookiesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#savecookiesonexit): Enregistrer les cookies lors de la fermeture de MicrosoftEdge.
- [SensorsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsallowedforurls): autoriser l’accès aux capteurs sur des sites spécifiques.
- [SensorsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsblockedforurls): bloquer l’accès aux capteurs sur des sites spécifiques.
- [SerialAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialaskforurls): autoriser l’API Serial sur des sites spécifiques.
- [SerialBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialblockedforurls): bloquer l’API Serial sur des sites spécifiques.
- [URLBlocklist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlblocklist): bloquer l’accès à une liste d’URL.
- [URLAllowlist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlallowlist): définir une liste d’URL autorisées.
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled): Activer la fonctionnalité User-Agent Client Hints.
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit): limite le nombre de captures instantanées des données utilisateur conservées qui sont utilisées en cas de restauration d’urgence.

#### Stratégies déconseillées

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled): activer les rapports de données d’utilisation et d’incident.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices): Envoyer des informations sur les sites pour améliorer les services Microsoft.

#### Stratégie obsolète

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled): active une fonctionnalité de sécurité TLS 1.3 pour les ancres d’approbation locales.

#### Légende de stratégie modifiée

[NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled): activer l’occlusion de fenêtre native.

#### Description de stratégie modifiée

- [AdsSettingForIntrusiveAdsSites](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun)
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes)
- [BrowserSignin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsersignin)
- [ClearBrowsingDataOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearbrowsingdataonexit) 
- [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare)
- [CookiesAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#cookiesallowedforurls)
- [CustomHelpLink](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#customhelplink)
- [DefaultCookiesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultcookiessetting)
- [DefaultGeolocationSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultgeolocationsetting)
- [DefaultImagesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultimagessetting)
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultjavascriptsetting)
- [DefaultNotificationsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultnotificationssetting)
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting)
- [DefaultPopupsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpopupssetting)
- [DefaultSearchProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#developertoolsavailability)
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors)
- [DownloadRestrictions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ForceBingSafeSearch](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcebingsafesearch)
- [ForceYouTubeRestrict](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forceyoutuberestrict)
- [HomepageIsNewTabPage](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepageisnewtabpage)
- [HomepageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepagelocation)
- [InPrivateModeAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#networkpredictionoptions)
- [NewTabPageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation)
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox)
- [NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls)
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode)
- [RegisteredProtocolHandlers](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#registeredprotocolhandlers)
- [RelaunchNotification](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#relaunchnotification)
- [RestoreOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartup)
- [RestoreOnStartupURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartupurls)
- [RestrictSigninToPattern](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restrictsignintopattern)
- [SSLVersionMin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslversionmin)
- [SmartScreenAllowListDomains](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenallowlistdomains)
- [SmartScreenEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled)
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)
- [TrackingPrevention](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#trackingprevention)
- [WebRtcLocalhostIpHandling](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalhostiphandling)

<!-- end 86 -->

## Version 85.0.564.41: 25 août

Résolution de divers bogues et problèmes de performances.

## Version 85.0.564.40: 21 août

Résolution de divers bogues et problèmes de performances.

## Version 85.0.564.36: 17 août

Résolution de divers bogues et problèmes de performances.

## Version 85.0.564.30: 10 août

Résolution de divers bogues et problèmes de performances.

## Version 85.0.564.23: 3 août

Résolution de divers bogues et problèmes de performances.

<!--- Archived to version 85.0.564.18: July 28 ---->

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
