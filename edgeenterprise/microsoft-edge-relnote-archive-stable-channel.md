---
title: Notes de publication archivées du canal stable Microsoft Edge
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 03/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notes de publication archivées du canal stable Microsoft Edge
ms.openlocfilehash: d8574e7b77babbf45a062ed9cadd4b60b616d972
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617954"
---
# <a name="archived-release-notes-for-microsoft-edge-stable-channel"></a>Notes de publication archivées du canal stable Microsoft Edge

Ces notes de publication fournissent des informations sur les nouvelles fonctionnalités et les mises à jour non liées à la sécurité qui sont incluses dans le canal stable Microsoft Edge. Toutes les mises à jour de sécurité sont listées [ici](microsoft-edge-relnotes-security.md).

## <a name="version-88070581-february-25"></a>Version 88.0.705.81 du 25 février

Résolution de divers bogues et de problèmes de performances.

## <a name="version-88070574-february-17"></a>Version 88.0.705.74 du 17 février

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](./microsoft-edge-relnotes-security.md#february-17-2021)

## <a name="version-88070568-february-11"></a>Version 88.0.705.68 du 11 février

Résolution de divers bogues et de problèmes de performances.

## <a name="version-88070563-february-5"></a>Version 88.0.705.63 du 5 février

> [!IMPORTANT]
> Cette mise à jour contient [CVE-2021-21148](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21148), qui a été signalé par l’équipe Chromium comme cible de code malveillant exploitant une faille de sécurité.

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](./microsoft-edge-relnotes-security.md#february-5-2021)

## <a name="version-88070562-february-4"></a>Version 88.0.705.62 du 4 février

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](./microsoft-edge-relnotes-security.md#february-4-2021)

Résolution de divers bogues et de problèmes de performances.

## <a name="version-88070556-january-28"></a>Version 88.0.705.56 : 28 janvier

Résolution de divers bogues et problèmes de performances.

## <a name="version-88070553-january-26"></a>Version 88.0.705.53 : 26 janvier

Résolution de divers bogues et problèmes de performances.

## <a name="version-88070550-january-21"></a>Version 88.0.705.50 du 21 janvier

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](./microsoft-edge-relnotes-security.md#january-21-2021)

<!--- begin major 88  --->
### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- **Fonctionnalités obsolètes :**

  - Prise en charge du protocole FTP obsolète. La prise en charge du protocole FTP hérité a été supprimée de Microsoft Edge. Toute tentative d’accès à un lien FTP entraînera l’ouverture par le système d’exploitation d’une application externe pour gérer le lien FTP. Une autre solution pour les administrateurs informatiques consiste à configurer Microsoft Edge afin qu’il utilise le mode IE pour les sites qui dépendent du protocole FTP.
  - La prise en charge d’Adobe Flash sera supprimé. À partir de la version 88 de Microsoft Edge Beta, la fonctionnalité et la prise en charge d’Adobe Flash seront supprimées. Pour en savoir plus : [Mise à jour concernant la fin de la prise en charge d’Adobe Flash Player – Blog Microsoft Edge (Windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentification :**

  - La signature unique (SSO) est désormais disponible pour les comptes Azure Active Directory (Azure AD) et le compte Microsoft (MSA) sur Windows de niveau inférieur. Un utilisateur se connectant à Microsoft Edge sur Microsoft Windows de niveau inférieur (7, 8.1) se connecte désormais automatiquement aux sites web configurés pour autoriser la connexion unique avec les comptes Professionnel et Microsoft (par exemple, bing.com, office.com, msn.com, outlook.com).<br>Remarque : il est possible que l’utilisateur doive se déconnecter et se reconnecter s’il se connecte à une version antérieure à la version 88 de Microsoft Edge pour utiliser cette fonctionnalité.
  
  - L’authentification unique (SSO) vers des sites professionnels à l’aide des comptes Windows Azure Active Directory (Azure AD) sur le système dans des profils Microsoft Edge non Azure AD. Cette fonctionnalité peut être activée pour n’importe quel profil qui n’est pas connecté avec un compte scolaire/professionnel et qui n’est pas invité ou en mode privé et permet l’utilisation de n’importe quel compte scolaire/professionnel sur le système d’exploitation avec ce profil. Cette fonctionnalité peut être configurée dans **Paramètres** > **Profils** > **Préférences de profil** > **Autoriser l'authentification unique pour les sites professionnels ou scolaires à l’aide de ce profil**.
  
    > [!NOTE]
    > « L’authentification unique (SSO) pour tous les comptes Windows utilisant le profil Microsoft Edge » est une mise à jour des notes de publication du 21 janvier.

- **Option du mode plein écran pour terminer la session**. Le bouton « Mettre fin à la session » est désormais disponible en mode plein écran dans l’expérience de navigation publique. Cette fonctionnalité permet de supprimer les données et paramètres du navigateur lorsque Microsoft Edge est fermé. Pour en savoir plus sur les fonctionnalités et la feuille de route du mode plein écran, voir [Configurer le mode plein écran Microsoft Edge](./microsoft-edge-configure-kiosk-mode.md).

- **Sécurité et confidentialité :**

  - Des alertes sont générées si le mot de passe d’un utilisateur est détecté dans une fuite en ligne. Les mots de passe des utilisateurs sont examinés par rapport à un référentiel d’informations d’identification connues qui ont été divulguées et envoient à l’utilisateur une alerte si une correspondance est trouvée. Pour garantir la sécurité et la confidentialité, les mots de passe des utilisateurs sont hachés et chiffrés lorsqu’ils sont vérifiés par rapport à la base de données des informations d’identification divulguées.
  - Mettre automatiquement à niveau le contenu mixte. Les pages sécurisées fournies via HTTPS peuvent contenir des images de référence fournies via HTTP non sécurisé. Pour améliorer la confidentialité et la sécurité dans Microsoft Edge 88, ces images seront récupérées via HTTPS. Si l’image n’est pas disponible via HTTPS, elle n’est pas chargée.
  - Afficher les autorisations de site par site et par activité récente. À partir de Microsoft Edge 88, les utilisateurs peuvent gérer plus facilement les autorisations de site. Ils peuvent afficher les autorisations par site web, et non plus seulement par type d’autorisation. Par ailleurs, nous avons ajouté une section activité récente qui permettra à l’utilisateur d’afficher les dernières modifications apportées à ses autorisations de site.
  - Amélioration des contrôles pour les cookies du navigateur. À partir de Microsoft Edge 88, les utilisateurs peuvent supprimer des cookies tiers sans affecter les cookies de première partie. Les utilisateurs peuvent également filtrer leurs cookies selon s’il s’agit d’une première ou tierce partie et les trier en fonction du nom, du nombre de cookies, de la quantité de données stockées et de la dernière modification.

- **Mots de passe :**

  - Générateur de mot de passe. Microsoft Edge offre un générateur de mot de passe fort intégré que vous pouvez utiliser lors de l’inscription d’un nouveau compte ou lors de la modification d’un mot de passe existant. Recherchez simplement la liste déroulante de mot de passe suggéré par le navigateur dans le champ mot de passe et, lorsqu’il est sélectionné, il sera automatiquement enregistrer dans le navigateur et synchronisé sur tous les appareils pour une utilisation facile à l’avenir.
  - Moniteur de mot de passe. Lorsque l’un de vos mots de passe enregistrés dans le navigateur correspond à ceux répertoriés dans la liste des informations d’identification divulguées, Microsoft Edge vous avertit et vous invite à mettre à jour votre mot de passe. Le moniteur de mot de passe analyse les correspondances en votre nom et est activé par défaut.
  - Modifier le mot de passe. Vous pouvez désormais modifier vos mots de passe enregistrés directement dans les paramètres Microsoft Edge. Chaque fois qu’un mot de passe a été mis à jour en dehors de Microsoft Edge, il est facile de remplacer l’ancien mot de passe enregistré par le nouveau en modifiant l’entrée enregistrée dans les Paramètres. 

- **Améliorer la vitesse de démarrage de Microsoft Edge grâce à l'accélération du démarrage**. Pour améliorer la vitesse de démarrage de Microsoft Edge, nous avons conçu une fonctionnalité appelée Accélérateur de démarrage. L’Accélérateur de démarrage accélère le lancement en permettant à Microsoft Edge de s’exécuter en arrière-plan. Remarque : cette fonctionnalité est limitée à un groupe d’utilisateurs sélectionnés de manière aléatoire et ayant activé l’expérimentation. Ces utilisateurs donnent des commentaires à l’équipe chargée de la fonctionnalité.

- **Productivité :**

  - Améliorez votre productivité et le travail multitâche grâce aux onglets verticaux. À mesure que vous ajoutez des onglets horizontaux, les titres de site sont tronqués et les commandes des onglets perdent en visibilité. Cela interrompt le flux de travail de l’utilisateur, car il passe plus de temps à rechercher, à passer de l’un à l’autre et à gérer ses onglets, et moins de temps sur la tâche en cours. Les onglets verticaux permettent aux utilisateurs de déplacer leurs onglets vers le côté, là où les icônes alignées à la verticale et les titres de sites plus longs permettent de jeter un coup d’œil rapide pour identifier l’onglet que vous voulez ouvrir et basculer vers celui-ci.
  - Remplissage automatique du champ de date de naissance. Microsoft Edge vous permet d’économiser du temps et de l’énergie lors du remplissage des formulaires et de la création de comptes en ligne à l’aide de la saisie semi-automatique des données utilisateur, telles que les adresses, les noms, les numéros de téléphone, etc. Microsoft Edge prend désormais en charge le champ Date de naissance que les utilisateurs peuvent enregistrer et remplir automatiquement. Un utilisateur peut afficher, modifier et supprimer ces informations à tout moment dans ses paramètres de profil.
  - Améliorations apportées à l’historique Récemment fermés. L’historique Récemment fermés conserve désormais les 25 derniers onglets et fenêtres de n’importe quelle session de navigation, et non plus seulement la session précédente. Les utilisateurs peuvent sélectionner Récemment fermés dans la nouvelle expérience d’Historique pour afficher tous les onglets qui ont été ouverts.
  - Fonction « votre journée en un clin d’œil » activée par défaut. À partir de la version 88 de Microsoft Edge, les travailleurs de l’information peuvent bénéficier de fonctionnalités de productivité intelligentes sur leur page Nouvel onglet (NTP). Les utilisateurs de Microsoft Edge 87 pourront également découvrir ces fonctionnalités dans les 2 semaines après la publication de Microsoft Edge 88. Nous offrons aux utilisateurs qui sont connectés à l’aide de leur compte professionnel ou scolaire du contenu personnalisé et pertinent optimisé par leur M365 Graph. Les utilisateurs peuvent rapidement parcourir leurs modules « votre journée en un clin d’œil » pour suivre facilement leurs réunions et leurs activités récentes, et lancer rapidement les applications qu’ils souhaitent utiliser.

- **Synchronisation de l'historique et des onglets ouverts**. La synchronisation de l'historique et des onglets ouverts est désormais disponible pour les utilisateurs. L’activation de ces fonctionnalités permet aux utilisateurs de reprendre là où ils en étaient en rendant leur historique de navigation et les onglets ouverts disponibles sur tous leurs appareils de synchronisation. Nous avons mis à jour les stratégies de synchronisation et d’historique des navigateurs, de sorte que les utilisateurs sont désormais connectés et productifs sur tous les appareils à l’aide de Microsoft Edge. [En savoir plus ](https://blogs.windows.com/windowsexperience/2021/01/21/this-year-lets-resolve-to-make-the-most-of-our-time-online-and-better-protect-ourselves-from-online-threats/).

- **PDF :**

  - Affichage d’un document PDF en mode livre (deux pages) À partir de la version 88 de Microsoft Edge, les utilisateurs peuvent consulter des documents PDF en affichage à une ou deux pages (mode livre). Pour modifier l’affichage, cliquez sur le bouton **Mode Page** dans la barre d’outils.
  - Prise en charge des notes de texte ancré pour les fichiers PDF. À partir de la version 87 de Microsoft Edge, les utilisateurs peuvent ajouter des notes de texte tapées sur n’importe quelle portion de texte dans des fichiers PDF.

- **Polices :**

  - Les icônes du navigateur sont mises à jour dans le système Fluent Design. Dans le cadre de nos efforts continus en termes de Fluent Design dans le navigateur, nous avons apporté des modifications de façon à aligner davantage les icônes sur le nouveau système d’icônes Microsoft. Ces modifications peuvent avoir une incidence sur un grand nombre de nos interfaces utilisateur avec une interaction tactile importante, y compris les onglets, la barre d’adresses, ainsi que les icônes de navigation et de recherche d’itinéraire dans nos différents menus.
  - Amélioration du rendu des polices. Le rendu du texte est amélioré pour améliorer la clarté et réduire le flou.

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

Dix-huit nouvelles stratégies ont été ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://www.microsoft.com/edge/business/download). Les nouvelles stratégies suivantes ont été ajoutées.

- [BasicAuthOverHttpEnabled](./microsoft-edge-policies.md#basicauthoverhttpenabled) : autoriser l’authentification de base pour HTTP.
- [BlockExternalExtensions](./microsoft-edge-policies.md#blockexternalextensions) : empêche l’installation d’extensions externes.
- [InternetExplorerIntegrationLocalFileAllowed](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileallowed) : autorise le lancement de fichiers locaux en mode Internet Explorer.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist) : ouvre les fichiers locaux dans la liste verte des extensions de fichier en mode Internet Explorer.
- [InternetExplorerIntegrationLocalFileShowContextMenu](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileshowcontextmenu) : afficher le menu contextuel pour ouvrir un lien en mode Internet Explorer.
- [IntranetRedirectBehavior](./microsoft-edge-policies.md#intranetredirectbehavior) : comportement de la redirection intranet.
- [PrinterTypeDenyList](./microsoft-edge-policies.md#printertypedenylist) : désactive les types d’imprimante dans la liste d’exclusion.
- [ShowMicrosoftRewards](./microsoft-edge-policies.md#showmicrosoftrewards) : affiche les expériences Microsoft Rewards.
- [SleepingTabsEnabled](./microsoft-edge-policies.md#sleepingtabsenabled) : configure les onglets en veille.
- [SleepingTabsTimeout](./microsoft-edge-policies.md#sleepingtabstimeout) : définit le délai d’inactivité des onglets en arrière-plan avant qu’ils ne soient mis en veille.
- [SleepingTabsBlockedForUrls](./microsoft-edge-policies.md#sleepingtabsblockedforurls) : bloque les onglets en veille sur des sites spécifiques.
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled) : active l’accélérateur de démarrage.
- [TargetBlankImpliesNoOpener](./microsoft-edge-policies.md#targetblankimpliesnoopener) : ne définissez pas window.opener pour les liens ciblant _blank.
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride) : indique comment Microsoft Edge Update gère les mises à jour disponibles à partir de Microsoft Edge.
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) : configure la disponibilité de la disposition verticale pour les onglets situés sur le côté du navigateur.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols) : autorise le passage à une version antérieure héritée de TLS/DTLS dans WebRTC.
- [WebWidgetAllowed](./microsoft-edge-policies.md#webwidgetallowed) : active le widget Web.
- [WebWidgetIsEnabledOnStartup](./microsoft-edge-policies.md#webwidgetisenabledonstartup) : autorise le widget web au démarrage de Windows.

#### <a name="deprecated-policies"></a>Stratégies déconseillées

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) : active l’authentification proactive.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist) : configure les règles de contournement du proxy.
- [ProxyMode](./microsoft-edge-policies.md#proxymode) : configure les paramètres du serveur proxy.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) : définit l’URL du fichier proxy .pac.
- [ProxyServer](./microsoft-edge-policies.md#proxyserver) : configure l’adresse ou l’URL du serveur proxy.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) : autorise WebDriver à remplacer les stratégies incompatibles.

### <a name="obsoleted-policies"></a>Stratégies obsolètes

- [AllowPopupsDuringPageUnload](./microsoft-edge-policies.md#allowpopupsduringpageunload) : permet à une page d’afficher des fenêtres contextuelles pendant son déchargement.
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) : paramètre Adobe Flash par défaut.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls) : autorise le plug-in Adobe Flash sur des sites spécifiques.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls) : bloque le plug-in Adobe Flash sur des sites spécifiques.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode) : étend le paramètre de contenu Adobe Flash à l’ensemble du contenu.
<!--- end major 88  --->
## <a name="version-87066475-january-7"></a>Version 87.0.664.75 du 7 janvier

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](./microsoft-edge-relnotes-security.md#january-7-2021)

## <a name="version-87066466-december-17"></a>Version 87.0.664.66 du 17 décembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-87066460-december-10"></a>Version 87.0.664.60 : 10 décembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-87066457-december-7"></a>Version 87.0.664.57 : 7 décembre

Résolution de divers bogues et de problèmes de performances. Les mises à jour de sécurité du canal stable sont répertoriées [ici.](./microsoft-edge-relnotes-security.md#december-7-2020)

## <a name="version-87066455-december-3"></a>Version 87.0.664.55 du 3 décembre

Résolution de divers bogues et problèmes de performances. La fonctionnalité suivante a été mise à jour pour cette version.

- **L’option achat est activée par défaut**. À partir de la version 87 de Microsoft Edge, les utilisateurs de l’entreprise peuvent profiter d’achats dans Microsoft Edge. Grâce aux fonctionnalités d’achat, Microsoft Edge permet aux utilisateurs de trouver des coupons et de meilleurs prix lors de leurs achats en ligne. (L’interface de coupon a été publiée avec la version stable 87.0.664.41). L’interface de comparaison des prix est désormais disponible dans cette mise à jour. Cette fonctionnalité peut être configurée à l’aide de la stratégie [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled). Consultez notre [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) et [En savoir plus](/microsoft-edge/privacy-whitepaper#shopping) sur les Achats Microsoft.

## <a name="version-87066452-november-30"></a>Version 87.0.664.52 : 30 novembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-87066447-november-23"></a>Version 87.0.664.47 : 23 novembre

Résolution de divers bogues et problèmes de performances.

<!-- begin major 87 --->
## <a name="version-87066441-november-19"></a>Version 87.0.664.41 du 19 novembre

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](./microsoft-edge-relnotes-security.md#november-19-2020)

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- **Redirection automatique pour les sites incompatibles d’Internet Explorer vers Microsoft Edge**. À partir de la mise à jour stable de Microsoft Edge 87, les sites web publics qui affichent un message d’incompatibilité sur Internet Explorer seront automatiquement redirigés vers Microsoft Edge. Pour en savoir plus et configurer cette interface, voir la [Redirection des sites incompatibles](./edge-learnmore-neededge.md).

- **Activation des fonctionnalités de confidentialité en mode plein écran**. À partir de la version 87 de Microsoft Edge, les fonctionnalités du mode plein écran seront activées et permettront aux entreprises de garantir la confidentialité des données utilisateur. Ces fonctionnalités activent les expériences telles que l’effacement des données utilisateur à la fermeture, la suppression des fichiers téléchargés et la réinitialisation de l’expérience de démarrage configurée après une durée inactivité déterminée. En savoir plus sur la [Configuration du mode plein écran Microsoft Edge](./microsoft-edge-configure-kiosk-mode.md).

- **Fonctionnalités d’achat activées par défaut**. À partir de la version 87 de Microsoft Edge, les utilisateurs entreprise peuvent également bénéficier des achats dans Microsoft Edge. Grâce aux fonctionnalités Achats, Microsoft Edge permet aux utilisateurs de trouver des bons de réduction et de meilleurs tarifs lors de leurs achats en ligne. La fonction des bons de réduction est disponible avec cette mise à jour et la fonctionnalité de comparaison des prix sera publiée dans les prochaines mises à jour de Microsoft Edge version 87. Vous pouvez configurer cette fonctionnalité via la stratégie [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) . Consultez notre [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) et [En savoir plus](/microsoft-edge/privacy-whitepaper#shopping) sur les Achats Microsoft.

- **Activation du déploiement ClickOnce par défaut**. L’activation de ClickOnce par défaut dans Microsoft Edge 87, réduit les difficultés des entreprises à déployer des logiciels et mieux s’aligner sur le comportement du navigateur Microsoft Edge Legacy. Au démarrage de Microsoft Edge 87, l’état « Non Configuré » de la stratégie ClickOnceEnabled reflète le nouvel état par défaut Activé de la stratégie ClickOnce (comparé à l’État par défaut Désactivé précédent).

- **La page nouvel onglet de l’entreprise (NTP) intègre la productivité avec un contenu de flux de travail personnalisable**. La Page Nouvel Onglet de l’Entreprise combine la page de productivité d’Office 365 que nous proposons aux utilisateurs connectés à leur compte professionnel ou scolaire, avec des flux professionnels personnalisés qui sont organisés en une seule page. Les utilisateurs reconnaîtront le contenu familier Office 365 et Microsoft Search pour les entreprises optimisé par Bing. Par ailleurs, il peuvent facilement personnaliser « Mon flux » en choisissant le contenu le plus pertinent pour eux à partir du contenu et des modules disponibles pour leur organisation. Les administrateurs informatiques peuvent contrôler les paramètres de flux d’actualités pour leur organisation, notamment le secteur sélectionné pour la nouvelle page d’onglets Microsoft Edge en accédant au Centre d’administration Microsoft 365. [Si vous souhaitez en savoir plus](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

- **Confidentialité et sécurité :**

  - Jeton TLS de support Obligatoire pour les sites configurés par une stratégie. Le jeton TLS obligatoire permet d’éviter les attaques par vol de jetons afin de s’assurer que les cookies ne peuvent pas être réutilisés à partir d’un autre appareil que l’appareil sur lequel ils ont été initialement définis. L’utilisation du jeton TLS obligatoire nécessite la définition de la stratégie [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) et nécessite que les sites répertoriés prennent en charge cette fonctionnalité.

- **Prise en charge du clavier pour le surligneur des fichiers PDF**. Les utilisateurs peuvent utiliser leurs touches de clavier pour surligner des textes de fichiers PDF.

- **Impression:**

  - Sélectionnez le côté à retourner lors de l’impression recto verso. Les utilisateurs peuvent choisir de retourner sur le côté long ou sur le côté court d’une feuille lors de l’impression recto verso.
  - Sélectionnez le mode de tramage de l’impression pour l’entreprise. Contrôlez l’impression Microsoft Edge sur une imprimante non-PostScript sur Windows. Parfois l’ impression sur des imprimantes non-PostScript doit être tramée pour imprimer correctement. Les options d’impression sont « Complètes » et « Rapides ».

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

Ajout de dix nouvelles stratégies. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://www.microsoft.com/edge/business/download). Les nouvelles stratégies suivantes ont été ajoutées.

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat) - Configurez le format de collage par défaut des URL copiées à partir de Microsoft Edge et déterminez si d’autres formats sont disponibles pour les utilisateurs.
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) -Achats activés dans Microsoft Edge.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled) - Masquez la boite de dialogue de redirection ponctuelle et la bannière sur Microsoft Edge.
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled) - Configurez la modification de la barre d’adresses pour l’expérience de navigation publique en mode plein écran.
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) - Supprimez des fichiers téléchargés sous la session plein écran lorsque Microsoft Edge se ferme.
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled) -Activez le bouton Affichage du mot de passe.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall) -Empêchez l’installation de l’objet d’assistance du navigateur (BHO) pour rediriger les sites incompatibles d’Internet Explorer vers Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode) - Redirigez les sites incompatibles de Internet Explorer vers Microsoft Edge.
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled) - Configurez la Reconnaissance vocale.
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled) -Activez la fonctionnalité de capture web dans Microsoft Edge.

#### <a name="deprecated-policy"></a>Stratégie Déconseillée

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) - Configurez l’expérience de la page nouvel onglet de Microsoft Edge.

#### <a name="obsoleted-policy"></a>Stratégie obsolète

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures) - Réactivez les fonctionnalités de plateforme web déconseillées pendant une période limitée.

<!-- end major 87 -->

## <a name="version-86062269-november-13"></a>Version 86.0.622.69 du 13 novembre

> [!IMPORTANT]
> Cette mise à jour contient [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) et [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), signalés par l’équipe Chromium comme cible code malveillant exploitant une faille de sécurité.

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](./microsoft-edge-relnotes-security.md#november-13-2020)

## <a name="version-86062268-november-11"></a>Version 86.0.622.68 du 11 novembre

Les mises à jour de sécurité du canal stable sont répertoriées [ici](./microsoft-edge-relnotes-security.md#november-11-2020)

## <a name="version-86062263-november-4"></a>Version 86.0.622.63 du 4 novembre

> [!IMPORTANT]
> Cette mise à jour contient [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), signalé par l’équipe Chromium comme cible de code malveillant exploitant une faille de sécurité.

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](./microsoft-edge-relnotes-security.md#november-4-2020)

## <a name="version-86062261-november-2"></a>Version 86.0.622.61 du 2 novembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-86062258-october-29"></a>Version 86.0.622.58 : 29 octobre

Résolution de divers bogues et problèmes de performances.

## <a name="version-86062256-october-27"></a>Version 86.0.622.56 : 27 octobre

Résolution de divers bogues et problèmes de performances.

## <a name="version-86062251-october-22"></a>Version 86.0.622.51 du 22 octobre

Les mises à jour de sécurité du canal stable sont répertoriées [ici](./microsoft-edge-relnotes-security.md#october-22-2020)

## <a name="version-86062248-october-20"></a>Version 86.0.622.48 du 20 octobre

Résolution de divers bogues et problèmes de performances.

## <a name="version-86062243-october-15"></a>Version 86.0.622.43 : 15 octobre

Résolution de divers bogues et problèmes de performances.

## <a name="version-86062238-october-9"></a>Version 86.0.622.38 : 9 octobre

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#october-9-2020).

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

* **Revenir à la version précédente de Microsoft Edge.** La fonctionnalité de restauration permet aux administrateurs de revenir à une version correcte connue de Microsoft Edge s’il existe un problème dans la dernière version de Microsoft Edge. **Remarque : ** la version stable 86.0.622.38 est la première version vers laquelle vous pouvez revenir, ce qui signifie que la version stable 87 est la première version prête à revenir. [En savoir plus](edge-learnmore-rollback.md).

* **Appliquer l’activation de la synchronisation par défaut au sein de l’entreprise.**  Les administrateurs peuvent activer la synchronisation pour les comptes Azure Active Directory (Azure AD) par défaut avec la stratégie [ForceSync](./microsoft-edge-policies.md#forcesync) .

* **Changement de profil automatique sur Windows 7 et 8.1.** Le changement automatique de profil actuellement disponible dans Microsoft Edge sur Windows 10 est étendu aux niveaux inférieurs de Windows (Windows 7 et 8.1). Pour plus d’informations, consultez le billet de blog [changement automatique de profil](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **SameSite = Lax cookies par défaut**. Pour améliorer la sécurité et la confidentialité sur le Web, les cookies s’affichent désormais par défaut [SameSite = Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite) gestion par défaut. Cela signifie que les cookies sont uniquement envoyés dans un contexte tiers et sont omis pour les demandes envoyées aux tiers. Cette modification peut avoir un impact sur les sites Web qui requièrent des cookies pour que les ressources tierces fonctionnent correctement. Pour autoriser de tels cookies, les développeurs Web peuvent marquer les cookies qui doivent être définis de et envoyés à des contextes tiers en ajoutant des attributs `SameSite=none` et `Secure` explicites lorsque le cookie est défini. Les entreprises qui souhaitent exempter certains sites de cette modification peuvent le faire à l’aide de la stratégie de [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist). Vous pouvez également désactiver la modification sur tous les sites à l’aide de la stratégie [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) .

* **Supprimez l’API de cache de l’application HTML5.**  Depuis Microsoft Edge version 86, l’API cache de l’application héritée qui permet d’utiliser en mode hors connexion des pages web est supprimée de Microsoft Edge. Les développeurs web doivent consulter la [documentation WebDev](https://web.dev/appcache-removal/) pour plus d’informations sur le remplacement de l’API cache de l’application avec les travailleurs de service.  Important : vous pouvez demander un [Jeton AppCache OriginTrial](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) qui permet aux sites de continuer à utiliser l’API de cache d’application déconseillée jusqu’à la version 90 de Microsoft Edge.

* **Confidentialité et sécurité :**

  * Remplacez les stratégies [MetricsReportingEnabled](/DeployEdge/microsoft-edge-policies#metricsreportingenabled) et [SendSiteInformationToImproveServices](/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) pour les fenêtres de niveau inférieur et macOS. Ces stratégies sont déconseillées dans Microsoft Edge version 86 et deviendront obsolètes dans Microsoft Edge version 89.<br>
Ces stratégies sont remplacées par [Autoriser la télémétrie](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) sur Windows 10, et la nouvelle stratégie [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) pour toutes les autres plateformes. Cela permet aux utilisateurs de gérer les données de diagnostic envoyées à Microsoft pour Windows 7, 8, 8.1 et macOS.
  * Prise en charge du DNS sécurisé (DNS-sur-HTTPS).  À partir de la version 86 de Microsoft Edge, les paramètres de contrôle de DNS sécurisé sur les appareils non gérés sont disponibles. Ces paramètres ne sont pas accessibles aux utilisateurs sur les appareils gérés, mais les administrateurs informatiques peuvent activer ou désactiver le DNS sécurisé à l’aide de la stratégie de groupe [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode).

* ** Mode Internet Explorer :** Permet aux utilisateurs d'utiliser l'interface utilisateur (IU) de Microsoft Edge pour tester des sites en mode Internet Explorer. À partir de la version 86 de Microsoft Edge, les administrateurs peuvent activer une option d'interface utilisateur pour que leurs utilisateurs puissent charger un onglet en mode Internet Explorer à des fins de test ou comme palliatif jusqu'à ce que les sites soient ajoutés à la liste XML des sites.

* **Mises à jour PDF :**

  * Table des matières des documents PDF. À partir de la version 86, Microsoft Edge a ajouté la prise en charge de la table des matières qui permet aux utilisateurs de parcourir facilement les documents PDF.
  * Accédez à toutes les fonctionnalités de PDF sur les écrans compacts. Accédez à toutes les fonctionnalités du lecteur PDF Microsoft Edge sur les appareils disposant de petites tailles d’écran.
  * Prise en charge du stylet pour le surligneur des fichiers PDF. Avec cette mise à jour, les utilisateurs peuvent utiliser leur stylet numérique pour mettre en surbrillance directement du texte dans les fichiers PDF, de la même manière qu’avec un surligneur physique et du papier.
  * Défilement PDF amélioré. Vous pourrez désormais faire défiler les documents au format PDF long.

* **Les suggestions de saisie semi-automatique s’affichent lorsque les utilisateurs commencent à taper une requête de recherche sur le site web des composants additionnels Microsoft Edge.** La saisie semi-automatique permet aux utilisateurs d’effectuer rapidement leur requête de recherche sans entrer l’intégralité de la chaîne. Ceci est utile, car les utilisateurs n’ont pas besoin de se souvenir des orthographes correctes, et peuvent choisir parmi les options disponibles qui s’affichent.

* **Ajoutez une image personnalisée à la nouvelle page d’onglet (NTP) à l’aide d’une stratégie de groupe.** À partir de la version 86 de Microsoft Edge, le protocole NTP offre une option permettant de remplacer l'image par défaut par une image personnalisée fournie par l'utilisateur. La possibilité de gérer les propriétés de cette image est également prise en charge par la stratégie de groupe.

* **Faites correspondre les raccourcis clavier personnalisés à VS Code.** Microsoft Edge DevTools prend désormais en charge la personnalisation des raccourcis clavier dans DevTools pour adapter à votre éditeur/IDE. (Dans Microsoft Edge 84, nous avons ajouté la possibilité de faire correspondre les raccourcis clavier DevTools à VS Code).

* **Supprimez les téléchargements à partir du disque à l’aide du gestionnaire de téléchargement.** Les utilisateurs peuvent désormais supprimer leurs fichiers téléchargés à partir de leur disque sans quitter le navigateur. La nouvelle fonctionnalité Supprimer les téléchargements figure dans le menu contextuel de l’étagère téléchargements ou de la page de téléchargement.

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

Vingt-trois nouvelles politiques ont été ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist) : Bloquer l’accès à une liste de services et de cibles d’exportation spécifiée dans Collections.
- [ DefaultFileSystemReadGuardSetting](./microsoft-edge-policies.md#defaultfilesystemreadguardsetting)- Contrôle de l'utilisation de l'API du système de fichiers pour la lecture.
- [ DefaultFileSystemWriteGuardSetting ](./microsoft-edge-policies.md#defaultfilesystemwriteguardsetting) - Contrôle de l'utilisation de l'API du système de fichiers pour l'écriture.
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting) : paramètre par défaut des capteurs.
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting) : contrôler l’utilisation de l’API Serial.
- [ DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) - Envoyer des données de diagnostic obligatoires et facultatives sur l'utilisation du navigateur.
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) : autoriser l’accès à l’outil Enterprise Mode Site List Manager.
- [FileSystemReadAskForUrls](./microsoft-edge-policies.md#filesystemreadaskforurls) - Autoriser l'accès en lecture via l'API du système de fichiers sur ces sites.
- [FileSystemReadBlockedForUrls](./microsoft-edge-policies.md#filesystemreadblockedforurls) - Bloquer l'accès en lecture via l'API du système de fichiers sur ces sites.
- [FileSystemWriteAskForUrls](./microsoft-edge-policies.md#filesystemwriteaskforurls) - Autoriser l'accès en écriture aux fichiers et aux répertoires de ces sites.
- [FileSystemWriteBlockedForUrls](./microsoft-edge-policies.md#filesystemwriteblockedforurls) - Bloquer l'accès en écriture aux fichiers et aux répertoires de ces sites.
- [ForceSync](./microsoft-edge-policies.md#forcesync) : forcer la synchronisation des données du navigateur et ne pas afficher l’invite de consentement de synchronisation.
- [InsecureFormsWarningsEnabled](./microsoft-edge-policies.md#insecureformswarningsenabled) : activer les avertissements pour les formulaires non sécurisés.
- [InternetExplorerIntegrationTestingAllowed](./microsoft-edge-policies.md#internetexplorerintegrationtestingallowed) : autoriser le test du mode Internet Explorer.
- [SpotlightExperiencesAndRecommendationsEnabled](./microsoft-edge-policies.md#spotlightexperiencesandrecommendationsenabled) : déterminer si les utilisateurs peuvent recevoir des images d’arrière-plan et du texte personnalisés, des suggestions, des notifications et des conseils pour les services Microsoft.
- [NewTabPageAllowedBackgroundTypes](./microsoft-edge-policies.md#newtabpageallowedbackgroundtypes) : Définir les types d’arrière-plan autorisés pour la disposition du nouvel onglet.
- [SaveCookiesOnExit](./microsoft-edge-policies.md#savecookiesonexit) : Enregistrer les cookies lors de la fermeture de Microsoft Edge.
- [SensorsAllowedForUrls](./microsoft-edge-policies.md#sensorsallowedforurls) : autoriser l’accès aux capteurs sur des sites spécifiques.
- [SensorsBlockedForUrls](./microsoft-edge-policies.md#sensorsblockedforurls) : bloquer l’accès aux capteurs sur des sites spécifiques.
- [SerialAskForUrls](./microsoft-edge-policies.md#serialaskforurls) : autoriser l’API Serial sur des sites spécifiques.
- [SerialBlockedForUrls](./microsoft-edge-policies.md#serialblockedforurls) : bloquer l’API Serial sur des sites spécifiques.
- [UserAgentClientHintsEnabled](./microsoft-edge-policies.md#useragentclienthintsenabled) : Activer la fonctionnalité User-Agent Client Hints.
- [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit) : limite le nombre de captures instantanées des données utilisateur conservées qui sont utilisées en cas de restauration d’urgence.

#### <a name="deprecated-policies"></a>Stratégies déconseillées

- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) : activer les rapports de données d’utilisation et d’incident.
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) : Envoyer des informations sur les sites pour améliorer les services Microsoft.

#### <a name="obsoleted-policy"></a>Stratégie obsolète

[TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) : active une fonctionnalité de sécurité TLS 1.3 pour les ancres d’approbation locales.

## <a name="version-85056470-october-6"></a>Version 85.0.564.70 : 6 octobre

Résolution de divers bogues et problèmes de performances.

## <a name="version-85056468-october-1"></a>Version 85.0.564.68 : 1er octobre

Résolution de divers bogues et problèmes de performances.

## <a name="version-85056463-september-23"></a>Version 85.0.564.63 : 23 septembre

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#september-23-2020).

## <a name="version-85056451-september-9"></a>Version 85.0.564.51 : 9 septembre

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#september-9-2020).

## <a name="version-85056444-august-31"></a>Version 85.0.564.44 : 31 août

Résolution de divers bogues et problèmes de performances.

<!-- 85.0.564.41: August 27 -->

## <a name="version-85056441-august-27"></a>Version 85.0.564.41 : 27 août

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#august-27-2020).

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- **Synchronisation locale des favoris et des paramètres**. Vous pouvez désormais synchroniser les favoris et paramètres d’un navigateur entre les profils Active Directory au sein de votre propre environnement sans avoir besoin d’effectuer une synchronisation dans le cloud.

- **Prise en charge de la stratégie de groupe Microsoft Edge pour l’approbation de combinaisons site + application à lancer sans invite de confirmation.**. La prise en charge de la stratégie de groupe ajoutée permet aux administrateurs d’ajouter des combinaisons site + application dont le lancement est approuvé sans invite de confirmation. Cela ajoute la possibilité pour les administrateurs de configurer les combinaisons de protocoles/origines approuvées (par exemple, les applications Microsoft 365) pour leurs utilisateurs finaux afin de supprimer l’invite de confirmation lors de la navigation vers une URL qui contient un protocole d’application.

- **Outil de mise en surbrillance PDF**. Cet outil peut être ajouté à la barre d’outils pour les fichiers PDF afin de mettre en évidence le texte important.

- **L’API d’accès au stockage est disponible**. Cette API d’accès au stockage permet l’accès au stockage interne alors qu’un utilisateur tiers manifeste son intention directe d’autoriser un stockage qui sinon serait bloqué par la configuration actuelle du navigateur. Pour plus d’informations, voir [API d’accès au stockage](https://www.chromestatus.com/feature/5612590694662144).

- **Envoyer à OneNote est disponible pour les collections Microsoft Edge**. Tout le monde a hâte de pouvoir envoyer des informations rassemblées dans des collections vers OneNote, où l’on peut l’ajouter à un projet plus important et collaborer avec d’autres personnes. Et encore plus important, dans Microsoft Edge 85, vous pourrez envoyer du contenu aux produits *Office pour Mac* (Word, Excel et OneNote) pour le compte Microsoft et Azure Active Directory.

- **Mises à jour de DevTools**. Pour plus d’informations sur les mises à jour suivantes, voir [Nouveautés de DevTools (Microsoft Edge 85)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools).

   - Microsoft Edge DevTools prend en charge l’émulation Surface Duo. Microsoft Edge DevTools peut émuler le Surface Duo pour vous permettre de tester l’apparence de votre contenu Web sur les appareils à deux écran. Pour activer cette expérience dans DevTools, accédez au mode Appareil en appuyant sur Ctrl + Maj + M sur Windows ou cmd + Maj + M sur macOS, puis sélectionnez Surface Duo dans la liste déroulante des appareils.
   - Microsoft Edge DevTools vous permet de faire correspondre les raccourcis clavier à VS Code. Microsoft Edge DevTools prend en charge la personnalisation des raccourcis clavier dans DevTools pour reproduire votre éditeur/IDE. Dans Microsoft Edge 85, nous ajoutons la possibilité de faire correspondre les raccourcis clavier DevTools à VS Code. Cette modification permet de gagner en efficacité dans VS Code et DevTools.

### <a name="policy-updates"></a>Mises à jour de stratégie

#### <a name="new-policies"></a>Nouvelles stratégies

Treize nouvelles stratégies ont été ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [AutoLaunchProtocolsFromOrigins](./microsoft-edge-policies.md#autolaunchprotocolsfromorigins) : définir une liste de protocoles qui peuvent lancer une application externe à partir d’origines, sans inviter l’utilisateur.
- [AutoOpenAllowedForURLs](./microsoft-edge-policies.md#autoopenallowedforurls) : les URL pour lesquels AutoOpenFileTypes peut s’appliquer.
- [AutoOpenFileTypes](./microsoft-edge-policies.md#autoopenfiletypes) : liste des types de fichiers qui doivent être automatiquement ouverts lors du téléchargement.
- [DefaultSearchProviderContextMenuAccessAllowed](./microsoft-edge-policies.md#defaultsearchprovidercontextmenuaccessallowed) : autoriser la recherche d’accès au menu contextuel du moteur de recherche par défaut.
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors) : autoriser les certificats signés à l’aide de l’algorithme SHA-1 lorsqu’ils sont émis par des ancres d’approbation locales.
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](./microsoft-edge-policies.md#exemptdomainfiletypepairsfromfiletypedownloadwarnings) : désactiver les avertissements basés sur l’extension de fichier de téléchargement pour les types de fichiers spécifiés sur des domaines.
- [IntensiveWakeUpThrottlingEnabled](./microsoft-edge-policies.md#intensivewakeupthrottlingenabled) : contrôler la fonctionnalité IntensiveWakeUpThrottling.
- [NewTabPagePrerenderEnabled](./microsoft-edge-policies.md#newtabpageprerenderenabled) : activer le préchargement de la nouvelle page d’onglet pour un rendu plus rapide.
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox) : configurer l’expérience de zone de recherche de la page Nouvel onglet.
- [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed) : autoriser les utilisateurs à être avertis si leur mot de passe est considéré comme non sécurisé.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled) : activer l’utilisation de copies itinérantes pour les données de profil Microsoft Edge.
- [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation) : définit le répertoire de profil itinérant.
- [TLSCsipherSuiteDenyList](./microsoft-edge-policies.md#tlsciphersuitedenylist) : spécifier les suites de chiffrement TLS à désactiver.

#### <a name="obsoleted-policies"></a>Stratégies obsolètes

- [EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) : activer le téléchargement des actions de domaine à partir de Microsoft.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) – Réactive les composants WebPart de l’API v0 jusqu’au M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) : autoriser WebDriver à remplacer les stratégies incompatibles.

## <a name="version-84052263-august-20"></a>Version 84.0.522.63 : août 2020

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#august-20-2020).

## <a name="version-84052261-august-17"></a>Version 84.0.522.61: 17 août

Résolution de divers bogues et problèmes de performances.

## <a name="version-84052259-august-11"></a>Version 84.0.522.59 : 11 août

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#august-11-2020).

## <a name="version-84052258-august-10"></a>Version 84.0.522.58 : 10 août

Résolution de divers bogues et problèmes de performances.

## <a name="version-84052252-august-1"></a>Version 84.0.522.52 : 1er août

Résolution de divers bogues et problèmes de performances.

## <a name="version-84052250-july-31"></a>Version 84.0.522.50 : 31 juillet

Résolution de divers bogues et problèmes de performances.

## <a name="version-84052249-july-29"></a>Version 84.0.522.49 : 29 juillet

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#july-29-2020).

## <a name="version-84052248-july-28"></a>Version 84.0.522.48 : 28 juillet

Résolution de divers bogues et problèmes de performances.

## <a name="version-84052244-july-23"></a>Version 84.0.522.44 : 23 juillet

Résolution de divers bogues et problèmes de performances.

## <a name="version-84052240-july-16"></a>Version 84.0.522.40 : 16 juillet

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#july-16-2020).

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- Cette version de Microsoft Edge permet un téléchargement plus rapide des listes de sites en mode Internet Explorer. Nous avons réduit le délai de téléchargement des listes de sites en mode Internet Explorer à 0 seconde (60 secondes d’attente auparavant) en l’absence d’une liste de sites mis en cache. Nous avons également ajouté la prise en charge de la stratégie de groupe pour les cas où les navigations dans la page d’accueil en mode Internet Explorer doivent attendre le téléchargement de la liste des sites. Si vous souhaitez en savoir plus, veuillez consulter la stratégie [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload).

- Microsoft Edge permet désormais aux utilisateurs de se connecter au navigateur lorsque celui-ci est en mode « Exécuter en tant qu’administrateur » sous Windows 10. Cette fonctionnalité aide les clients à exécuter Microsoft Edge sur un serveur Windows ou dans les scénarios de bureau à distance et de bac à sable.

- Microsoft Edge fournit à présent une prise en charge complète de la souris en mode plein écran. Vous pouvez à présent utiliser la souris pour accéder aux onglets, à la barre d’adresses et aux autres éléments sans quitter le mode plein écran.

- Amélioration des achats en ligne. Ajoutez des pseudos personnalisés aux cartes de débit ou de crédit enregistrées. Vous pouvez à présent distinguer et différencier vos cartes de crédit lors de vos achats en ligne. L’attribution d’un pseudo à vos cartes de débit ou de crédit vous permet de choisir la carte appropriée lorsque vous utilisez le remplissage automatique pour sélectionner un mode de paiement.

- TLS/1.0 et TLS/1.1 sont désactivés par défaut.  La stratégie [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) permet de réactiver TLS/1.0 et TLS/1.1. Cette stratégie reste disponible au moins jusqu’à Microsoft Edge version 88. Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Modifications apportées à Microsoft Edge ayant un impact sur la compatibilité des sites](/microsoft-edge/web-platform/site-impacting-changes).

- Améliorations des collections :

  - Nous avons ajouté une fonctionnalité d’ajout de note ou de commentaire à un élément d’une collection. Les notes sont regroupées et restent associées à un élément, même si vous triez les éléments d’une collection. Pour essayer cette nouvelle fonctionnalité, cliquez avec le bouton droit sur un élément, puis sélectionnez « Ajouter une note ».
  - Vous pouvez modifier la couleur d’arrière-plan des notes dans les collections. Vous pouvez utiliser un codage en couleurs pour vous aider à organiser vos informations et augmenter votre productivité.
  - Des améliorations de performances sont perceptibles, ce qui vous permet d’exporter vos collections vers Excel en moins de temps que dans les versions précédentes de Microsoft Edge.

- Prise en charge supplémentaire de l’API Microsoft Edge :

  - L’API accès au stockage est activée pour les expérimentations. Cette fonctionnalité est activée pour les utilisateurs particuliers et les utilisateurs d’entreprise avec la stratégie de [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) définie sur « Full ». Cette fonctionnalité sera activée par défaut pour tous les utilisateurs de la version 85 du canal stable Microsoft Edge.
  
    À mesure que la confidentialité revêt une importance grandissante pour les utilisateurs, ces dernier recherchent, de plus en plus, des valeurs par défaut du navigateur et des paramètres plus stricts de consentement des utilisateurs (blocage de l’accès au stockage tiers, par exemple). Ces paramètres permettent d’améliorer la confidentialité et de bloquer l’accès indésirable de la part d’utilisateurs inconnus ou non approuvés. Cependant, ils peuvent également avoir des effets secondaires indésirables, tels que le blocage de l’accès au contenu nécessaire à l’utilisateur (par exemple, les réseaux sociaux et le contenu multimédia incorporé).

    Cette API d’accès au stockage permet l’accès au stockage interne alors qu’un utilisateur tiers manifeste son intention directe d’autoriser un stockage qui sinon serait bloqué par la configuration actuelle du navigateur. Pour plus d’informations, voir [API d’accès au stockage](https://www.chromestatus.com/feature/5612590694662144).

  - L’API de système de fichiers natif vous permet d’autoriser les sites à modifier des fichiers ou des dossiers.

- Améliorations apportées au contenu PDF :

  - La lecture à voix haute pour PDF permet aux utilisateurs d’écouter du contenu PDF tout en effectuant d’autres tâches éventuellement importantes pour eux. Cela permet également aux apprenants au profil auditif et visuel de se concentrer sur la lecture du contenu, d’où un apprentissage facilité.
  - La modification des fichiers PDF est améliorée. Vous pouvez à présent enregistrer une modification directement dans le fichier PDF au lieu d’enregistrer une copie de ce dernier à chaque modification.

- Microsoft Edge permet à présent la traduction dans le lecteur immersif. Lorsqu’un utilisateur ouvre la vue Lecteur immersif, il peut choisir de traduire la page dans la langue de son choix.

- Plusieurs mises à jour DevTools comprennent notamment la personnalisation des raccourcis clavier pour faire correspondre le code VS et l’affichage du DevTools en contraste élevé.  Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Nouveautés de DevTools (Microsoft Edge 84)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/05/devtools).

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

Nous avons ajouté sept nouvelles stratégies. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [AppCacheForceEnabled](./microsoft-edge-policies.md#appcacheforceenabled) : permet de réactiver la fonctionnalité AppCache, même si elle est désactivée par défaut.
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy) : configure les paramètres du proxy conteneur Application Guard.
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) : la liste des sites en mode entreprise doit être disponible avant la navigation par onglets.
- [WinHttpProxyResolverEnabled](./microsoft-edge-policies.md#winhttpproxyresolverenabled) : utilise le programme de résolution du proxy Windows.
- [InternetExplorerIntegrationEnhancedHangDetection](./microsoft-edge-policies.md#internetexplorerintegrationenhancedhangdetection) : configure la détection améliorée des blocages pour le mode Internet Explorer.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled)-pour réduire l’UC et la consommation d’énergie, Microsoft Edge détecte quand une fenêtre est couverte par d’autres fenêtres et suspend les pixels de peinture.
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout) : définit un délai d’expiration de la navigation par onglets pour la liste des sites en mode entreprise.

#### <a name="deprecated-policies"></a>Stratégies déconseillées

- [AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal) : autorise les pages à envoyer des demandes XHR synchrones lors de l’opération de rejet de page.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) – Indique si le vérificateur de certificats intégré est utilisé pour la vérification des certificats de serveur.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) : active un traitement plus strict pour des contenus mixtes.

#### <a name="obsoleted-policy"></a>Stratégie obsolète

[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess) : force l’exécution du code de mise en réseau dans le processus du navigateur.

<!-- End 84 -->
## <a name="version-83047864-july-13"></a>Version 83.0.478.64 : 13 juillet

Résolution de divers bogues et problèmes de performances.

## <a name="version-83047861-july-7"></a>Version 83.0.478.61 : 7 juillet

Résolution de divers bogues et problèmes de performances.

## <a name="version-83047858-june-30"></a>Version 83.0.478.58 : 30 juin

Résolution de divers bogues et problèmes de performances.

## <a name="version-83047856-june-24"></a>Version 83.0.478.56 : 24 juin

Résolution de divers bogues et problèmes de performances.

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#june-24-2020).

## <a name="version-83047854-june-17"></a>Version 83.0.478.54 : 17 juin

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#june-17-2020).

## <a name="version-83047850-june-15"></a>Version 83.0.478.50 : 15 juin

Résolution de divers bogues et problèmes de performances.

## <a name="version-83047845-june-4"></a>Version 83.0.478.45 : 4 juin

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#june-4-2020).

## <a name="version-83047844-june-1"></a>Version 83.0.478.44 : 1er juin

Résolution de divers bogues et problèmes de performances.

## <a name="version-83047837-may-21"></a>Version 83.0.478.37 : 21 mai

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#may-21-2020).

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- Les mises à jour de Microsoft Edge se déploient à présent progressivement. À l’avenir, le déploiement des mises à jour de Microsoft Edge s’effectuera sur les systèmes de nos utilisateurs en quelques jours. Cela nous permet de mieux vous protéger contre les mises à jour boguées accidentelles, ce qui améliore votre expérience de mise à jour. En tant qu’utilisateur, vous continuerez à bénéficier de mises à jour automatiques transparentes. Si votre organisation n’est pas inscrite aux mises à jour automatiques, cette modification ne vous concernera pas. Pour en savoir plus, veuillez consulter l’[article sur les déploiements progressifs](microsoft-edge-update-progressive-rollout.md).
- Améliorations apportées à Microsoft Defender SmartScreen : améliorations apportées au service Microsoft Defender SmartScreen, telles que la protection améliorée contre les sites malveillants qui redirigent au chargement et le blocage de trames de niveau supérieur, qui remplace complètement les sites malveillants avec la page de sécurité Microsoft Defender SmartScreen. Le blocage de trames de niveau supérieur empêche la lecture du contenu audio et d’autres éléments multimédias du site malveillant, ce qui permet d’obtenir une expérience plus facile et moins confuse.

- En réponse aux commentaires des utilisateurs, vous pouvez désormais exempter certains cookies de l’effacement automatiquement lorsque le navigateur se ferme. Cette option est utile s’il existe un site dont les utilisateurs ne souhaitent pas être déconnectés, mais souhaitent tout de même que tous les autres cookies soient supprimés lorsque le navigateur se ferme. Pour utiliser cette fonctionnalité, accédez à *edge://settings/clearBrowsingDataOnClose* et activez le bouton bascule « cookies et autres données de site ».

- Le basculement de profil automatique est désormais disponible pour vous aider à accéder à votre contenu professionnel plus facilement dans les profils. Si vous utilisez plusieurs profils au travail, vous pouvez les consulter en accédant à un site nécessitant une authentification à partir de votre compte professionnel ou scolaire sur votre profil personnel. Lorsque nous détectons ce problème, vous êtes invité à basculer vers votre profil de travail pour accéder à ce site sans devoir s’y authentifier. Lorsque vous choisissez le profil de travail vers lequel vous voulez basculer, le site Web s’ouvre simplement dans votre profil de travail. Cette fonctionnalité de commutation de profil vous permet de séparer vos données professionnelles et personnelles et d’accéder à votre contenu professionnel plus facilement. Si vous ne souhaitez pas que la fonctionnalité vous invite à changer de profil, vous pouvez choisir l’option ne plus poser de message.

- Améliorations des fonctionnalités de recouvrement :
  - Vous pouvez utiliser la fonction glisser-déplacer pour ajouter un élément à une collection sans ouvrir la collection. Pendant le glisser-déplacer, vous pouvez également choisir un emplacement dans la liste des collections où vous voulez placer l’élément.
  - Vous pouvez ajouter plusieurs éléments à une collection au lieu d’y ajouter un élément à la fois. Pour ajouter plusieurs éléments, sélectionnez les éléments, puis faites-les glisser vers une collection. Vous pouvez également sélectionner les éléments, cliquer avec le bouton droit et choisir la collection dans laquelle vous voulez placer les éléments.

- Vous pouvez ajouter tous les onglets d’une fenêtre de bord dans une nouvelle collection sans les ajouter individuellement. Pour ce faire, cliquez avec le bouton droit sur un onglet, puis sélectionnez « Ajouter tous les onglets à une nouvelle collection ».

- La synchronisation d’extension est désormais disponible. Vous pouvez désormais synchroniser vos extensions sur tous vos appareils. Les extensions des magasins Microsoft et chrome sont synchronisées avec Microsoft Edge. Pour utiliser cette fonctionnalité : cliquez sur les points de suspension (**…**) dans la barre de menus, puis sélectionnez **Paramètres**. Sous votre profil, cliquez sur **Synchroniser** pour afficher les options de synchronisation. Sous **Profils/synchronisation** utilisez le bouton bascule pour activer les extensions. Vous pouvez utiliser la stratégie de groupe [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) pour désactiver la synchronisation des extensions.

- Message amélioré sur la page gestion des téléchargements pour les téléchargements non sécurisés qui ont été bloqués.

- Améliorations du lecteur immersif :
  - Ajout d’une prise en charge des adverbes dans les parties de l’expérience de reconnaissance vocale dans le lecteur immersif. Lors de la lecture d’un article dans le lecteur immersif, ouvrez les outils de vérification de la grammaire et activez les adverbes dans certains secteurs vocaux pour mettre en surbrillance toutes les adverbes de la page.
  - Ajout de la possibilité de sélectionner le contenu d’une page Web et de l’ouvrir dans le lecteur immersif. Cette possibilité permet aux utilisateurs d’utiliser le lecteur immersif et tous les outils d’apprentissage, tels que le focus de ligne et la lecture à haute voix sur tous les sites Web.

- Le docteur de lien fournit une correction de l’hôte et une requête de recherche aux utilisateurs lorsqu’ils ne tapent pas une URL. Par exemple : <br>
Un utilisateur saisit « powerbi » comme « powerbbi ».com. Le docteur de lien suggère « powerbi ».com comme correction et crée un lien pour rechercher « powerbbi » au cas où l’utilisateur cherche quelque chose d’autre.

- Autoriser les utilisateurs à enregistrer leur décision de lancement d’un protocole externe pour un site spécifique. Les utilisateurs peuvent configurer la stratégie de [ExternalProtocolDialogShowAlwaysOpenCheckbox](/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) pour activer ou désactiver cette fonctionnalité.

- Les utilisateurs peuvent régler Microsoft Edge comme navigateur par défaut directement à partir de Microsoft Edge **Paramètres**. Cela permet aux utilisateurs de modifier facilement leur navigateur par défaut, dans le contexte du navigateur lui-même, au lieu d’effectuer une recherche dans les paramètres du système d’exploitation. Pour utiliser cette fonctionnalité, accédez à *edge://settings/defaultBrowser*, puis cliquez sur **Utiliser par défaut**.

- Plusieurs mises à jour de DevTools, y compris la prise en charge du débogage distant, l’amélioration de l’interface utilisateur et bien plus encore. Pour plus d’informations, consultez [Nouveautés de DevTools (Microsoft Edge 83)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

- Le scénario d’avertissement MCAS (Microsoft Cloud Access Security) est à présent disponible. Ainsi, les administrateurs peuvent configurer l’avertissement, nouvelle catégorie de blocs MCAS, où l’utilisateur peut remplacer une page de bloc MCAS. Nous avons intégré les blocs MDATP E5 en mode natif avec les blocs SmartScreen dans Microsoft Edge pour offrir une expérience transparente. Cette expérience permet d’utiliser un bloc rouge de page complète avec le message « ce site web est bloqué par votre organisation », au lieu d’une simple notification toast.

- Ne pas autoriser les XmlHttpRequest synchrones lors du rejet de page. L’envoi de XmlHttpRequest asynchrones lors du déchargement d’une page web sera supprimé. Cette modification améliore les performances et la fiabilité du navigateur. Cependant, elle peut avoir un impact sur les applications web non mises à jour pour utiliser des API web plus modernes, notamment sendBeacon et FETCH. La stratégie de groupe permettant de désactiver cette modification et d’autoriser les XHR synchrones lors du rejet de page sera disponible jusqu’à Migrosoft Edge 88. Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Modifications apportées à Microsoft Edge ayant un impact sur la compatibilité des sites](/microsoft-edge/web-platform/site-impacting-changes).

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

15 nouvelles stratégies ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [AllowSurfGame](./microsoft-edge-policies.md#allowsurfgame) –  Autoriser le jeu de surf.
- [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) – Configurer la liste des sites avec lesquels Microsoft Edge tentera d’établir une liaison de jeton.
- [BingAdsSuppression](./microsoft-edge-policies.md#bingadssuppression) – Bloquer toutes les annonces dans les résultats de recherche Bing.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) – Indique si le vérificateur de certificats intégré est utilisé pour la vérification des certificats de serveur.
- [ClearCachedImagesAndFilesOnExit](./microsoft-edge-policies.md#clearcachedimagesandfilesonexit) – Effacer les images et les fichiers mis en cache lors de la fermeture de Microsoft Edge.
- [ConfigureShare](./microsoft-edge-policies.md#configureshare) – Configurer l’expérience de partage.
- [DeleteDataOnMigration](./microsoft-edge-policies.md#deletedataonmigration) – Supprimer les anciennes données de navigateur lors de la migration.
- [DnsOverHttpsMode](./microsoft-edge-policies.md#dnsoverhttpsmode) – Contrôler le mode du protocole DNS-over-HTTPS.
- [DnsOverHttpsTemplates](./microsoft-edge-policies.md#dnsoverhttpstemplates) – Spécifier le modèle d’URI du programme de résolution DNS-over-HTTPS souhaité.
- [FamilySafetySettingsEnabled](./microsoft-edge-policies.md#familysafetysettingsenabled) – Autoriser les utilisateurs à configurer la sécurité des membres de la famille.
- [LocalProvidersEnabled](./microsoft-edge-policies.md#localprovidersenabled) – Autoriser les suggestions des fournisseurs de services locaux.
- [ScrollToTextFragmentEnabled](./microsoft-edge-policies.md#scrolltotextfragmentenabled) – Activer le défilement jusqu’au texte spécifié dans les fragments d’URL.
- [ScreenCaptureAllowed](./microsoft-edge-policies.md#screencaptureallowed) – Autoriser ou refuser la capture d’écran.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) – Configurer la liste des types exclus de la synchronisation.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) – Activer le masquage de fenêtres natives.

#### <a name="deprecated-policy"></a>Stratégie déconseillée

La stratégie suivante continuera à fonctionner dans cette version. Il deviendra « obsolète » dans une prochaine version.

[EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) – Activer le téléchargement des actions de domaine à partir de Microsoft

<!-- end 83 -->

## <a name="version-81041677-may-18"></a>Version 81.0.416.77 : 18 mai

Résolution de divers bogues et problèmes de performances.

## <a name="version-81041672-may-7"></a>Version 81.0.416.72 : 7 mai

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#may-7-2020).

## <a name="version-81041668-april-29"></a>Version 81.0.416.68 : 29 avril

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#april-29-2020).

## <a name="version-81041664-april-23"></a>Version 81.0.416.64 : 23 avril

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#april-23-2020).

## <a name="version-81041658-april-17"></a>Version 81.0.416.58 : 17 avril

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#april-17-2020).

## <a name="version-81041653-april-13"></a>Version 81.0.416.53 : 13 avril

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#april-13-2020).

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- Ajout de la prise en charge de la Protection des données Windows (WIP), qui permet aux entreprises de protéger les données sensibles contre toute divulgation non autorisée. [En savoir plus](./microsoft-edge-security-windows-information-protection.md).

- Les collections sont désormais disponibles. Pour démarrer, cliquez sur l’icône Collections située près de la barre d’adresses. Cette action ouvre le volet Collections dans lequel vous pouvez créer, modifier et afficher des collections. Les Collections ont été conçues en fonction de votre activité sur le web. Si vous êtes un client, un voyageur, un enseignant ou un étudiant, les Collections peuvent vous être utiles. [En savoir plus](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Autoriser la suppression (Masquer dans la barre d’outils) du bouton Collections de la barre d’outils Microsoft Edge par souci de cohérence.

- La connexion automatique d'un compte Active Directory local est ciblée uniquement pour les organisations qui l’activent.  Si des utilisateurs ont déjà ouvert une session avec un compte Active Directory local, ils pourront se déconnecter. Les utilisateurs se connectent automatiquement au compte principal de leur système d’exploitation uniquement s’il s’agit d’un compte Microsoft ou Azure Active Directory. Les administrateurs peuvent activer la connexion automatique à l’aide d’un compte Azure Active Directory local utilisant la stratégie ConfigureOnPremisesAccountAutoSignIn.

- Application Guard. La prise en charge des extensions est désormais disponible dans le conteneur.

- Nous avons ajouté un message pour informer les utilisateurs qu’Internet Explorer n'est pas installé lorsqu’ils naviguent vers une page configurée pour s’ouvrir en mode Internet Explorer.

- Mise à jour de l’outil d'affichage 3D dans Microsoft Edge DevTools avec une nouvelle fonctionnalité permettant de déboguer le contexte d'empilement de l’index-Z. L’affichage 3D affiche une représentation de la profondeur de Document Object Model (DOM) à l’aide de la couleur et de l’empilement et l’affichage index-Z vous permet d’isoler les différents contextes d’empilage de votre page. [En savoir plus](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- Les outils F12 Dev sont localisés dans 10 nouvelles langues pour qu'ils correspondent à la langue utilisée dans le reste du navigateur. [En savoir plus](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Ajout de la prise en charge de la lecture Dolby Vision. Sur la Build 17134 (mise à jour d'avril 2018) de Windows 10 compatible Dolby Vision, les sites web peuvent désormais afficher le contenu Dolby Vision. Découvrez comment activer le contenu Dolby Vision sur [Netflix](https://help.netflix.com/en/node/42384).

- Microsoft Edge peut désormais identifier et supprimer des favoris dupliqués et fusionner des dossiers portant le même nom. Pour accéder à cet outil, cliquez sur l’étoile dans la barre d’outils du navigateur, puis sélectionnez « Supprimer les favoris dupliqués ».  Vous pouvez confirmer les modifications et les mises à jour apportées à vos favoris seront synchronisées sur tous les appareils.

- Des utilisateurs ont signalé qu'il peut être difficile de distinguer une fenêtre de navigation normale dans un thème foncé d’une fenêtre InPrivate, car les deux cadres de fenêtre sont sombres. La nouvelle icône pilule bleue InPrivate dans le coin supérieur droit permet de garantir aux utilisateurs qu'ils naviguent en mode InPrivate.

- Ouvrir des liens externes dans le profil de navigateur adéquat. Sélectionnez un profil par défaut pour les liens ouverts afin que les applications externes s’ouvrent à partir de *edge://settings/multiProfileSettings*.

- Ajout d'un avertissement informant les utilisateurs qui se connectent à un profil de navigateur avec un compte après s’être précédemment connectés avec un compte différent. Cet avertissement permet d'empêcher la fusion involontaire de données.

- Si vous avez enregistré des cartes de paiement dans votre compte Microsoft, vous pouvez les utiliser dans Microsoft Edge lorsque vous saisissez des formulaires de paiement. Les cartes de votre compte Microsoft sont synchronisées sur tous les appareils de bureau et les informations détaillées sont partagées avec le site web après une authentification à deux facteurs (code CVC et votre identité Microsoft). Pour plus de commodité, vous pouvez choisir d’enregistrer, de manière sécurisée, une copie de la carte sur l’appareil durant l’authentification.

- La fonctionnalité Focus sur lignes est conçue pour les utilisateurs qui aiment se concentrer sur une partie limitée du contenu qu'ils lisent. Elle permet aux utilisateurs de se concentrer sur une, trois ou cinq lignes à la fois et assombrit le reste de la page pour leur permettre de lire sans aucune distraction. Les utilisateurs peuvent faire défiler l’écran à l’aide de l'interaction tactile ou des touches de direction pour que la concentration se déplace en conséquence.

- Microsoft Edge est désormais intégré au vérificateur d'orthographe de Windows sur les plateformes Windows 8.1 et ultérieures. Cette intégration offre une prise en charge linguistique accrue, avec un accès à d’autres dictionnaires linguistiques et la possibilité d’utiliser des dictionnaires personnalisés de Windows. Aucune action supplémentaire n’est requise de la part des utilisateurs lorsqu’une langue a été ajoutée dans les paramètres de langue du système d’exploitation. De plus, une touche bascule de vérification orthographique dans la langue est activée dans les paramètres de Microsoft Edge.

- Lorsque des documents PDF sont ouverts à l’aide de Microsoft Edge, les utilisateurs peuvent désormais créer ou supprimer des surbrillances et modifier la couleur. Cette fonctionnalité vous permet de référencer par la suite les parties importantes d'un document et de travailler en collaboration.

- Lors du chargement de longs documents PDF optimisés pour le web, les pages consultées par l’utilisateur sont chargées plus rapidement, parallèlement au chargement du reste du document.

- Il est désormais plus simple de démarrer le lecteur immersif pour un site web en appuyant sur la touche F9.

- Il est désormais plus facile de démarrer la lecture à haute voix à l’aide d’un raccourci clavier (Ctrl+Maj+U).

- Ajout d’un paramètre de ligne de commande MSI qui vous permet de supprimer la création d’une icône de bureau lors de l’installation de Microsoft Edge. L’exemple suivant montre comment utiliser ce nouveau paramètre : <br>
`MicrosoftEdgeEnterpriseX64.msi DONOTCREATEDESKTOPSHORTCUT=true`<br>
Une stratégie de groupe prendra en charge cette fonctionnalité dans une prochaine publication.

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

11 nouvelles stratégies ont été ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled) : active l’authentification ambiante pour les profils InPrivate et Invité. 
- [AudioSandboxEnabled](./microsoft-edge-policies.md#audiosandboxenabled) : autorise l’exécution du bac à sable audio.
- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) : utiliser une stratégie de référent par défaut de no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](./microsoft-edge-policies.md#globallyscopehttpauthcacheenabled) : active le cache d’authentification HTTP de portée globale.
- [ImportExtensions](./microsoft-edge-policies.md#importextensions) : autorise l’importation d’extensions.
- [ImportCookies](./microsoft-edge-policies.md#importcookies) : autorise l’importation de cookies.
- [ImportShortcuts](./microsoft-edge-policies.md#importshortcuts) : autorise l’importation de raccourcis.
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect) : spécifie la manière dont les navigations « dans la page » vers les sites non configurés se comportent lorsque vous démarrez à partir des pages du mode Internet Explorer.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) : active un traitement plus strict pour des contenus mixtes.
- [TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) : active une fonctionnalité de sécurité TLS 1.3 pour les ancres d’approbation locales.
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) : configure la connexion automatique avec un compte de domaine Azure Active Directory lorsqu'il n'existe pas de compte de domaine Azure Active Directory.

#### <a name="policy-name-and-caption-changes"></a>Nom de la stratégie et modifications des légendes

La stratégie `OmniboxMSBProviderEnabled` est remplacée par [AddressBarMicrosoftSearchInBingProviderEnabled](//DeployEdge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled). La légende de la stratégie est « activer la recherche Microsoft dans les suggestions de Bing dans la barre d’adresses ».

#### <a name="deprecated-policies"></a>Stratégies déconseillées

Les stratégies suivantes fonctionnent encore dans cette version. Elles deviendront « obsolètes » dans une prochaine version.

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) : réactive les composants WebPart de l’API v0 jusqu’au M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) : autorise WebDriver à substituer Incompatible.

#### <a name="resolved-issues"></a>Problèmes résolus

- Résolution d’un problème dans lequel le mode IE dans Microsoft Edge provoquait l’affichage d’une boîte de dialogue de téléchargement continu, même une fois le fichier téléchargé.
- Résolution d’un problème dans lequel Microsoft Edge supprimait les cookies de session lorsqu’une page déjà en mode IE était déclenchée pour ouvrir un nouvel onglet de mode IE.

## <a name="version-800361111-april-7"></a>Version 80.0.361.111 : 7 avril

Résolution de divers bogues et problèmes de performances.

## <a name="version-800361109-april-1"></a>Version 80.0.361.109 : 1er avril

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#april-1-2020).

## <a name="version-80036169-march-19"></a>Version 80.0.361.69 : 19 mars

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#march-19-2020).

## <a name="version-80036166-march-4"></a>Version 80.0.361.66 du 4 mars

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#march-4-2020).

## <a name="version-80036162-february-25"></a>Version 80.0.361.62 du 25 février

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#february-25-2020).

## <a name="version-80036157-february-20"></a>Version 80.0.361.57 du 20 février

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#february-20-2020).

## <a name="version-80036156-february-19"></a>Version 80.0.361.56 du 19 février

Résolution de divers bogues et problèmes de performances.

## <a name="version-80036154-february-14"></a>Version 80.0.361.54 du 14 février

### <a name="resolved-issues"></a>Problèmes résolus

- Résolution d'un problème lié à un échec de l'importation du mot de passe, du paiement et des cookies dans Microsoft Edge.

## <a name="version-80036150-february-11"></a>Version 80.0.361.50 du 11 février

Résolution de divers bogues et correctifs de performances.

## <a name="version-80036148-february-7"></a>Version 80.0.361.48 du 7 février

Les mises à jour de sécurité sont répertoriées [ici](./microsoft-edge-relnotes-security.md#february-7-2020).

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- Ajout de la protection SmartScreen lors du téléchargement d’applications potentiellement indésirables. [En savoir plus](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus)
- Ajout de la prise en charge de la lecture Dolby vision.
- A activé les utilisateurs de Windows Mixed Reality pour afficher les vidéos de 360 ° sur les casques VR.
- Une option est ajoutée au mode lecture pour augmenter l’espacement du texte.
- Ajout de la prise en charge pour l’effacement du lien à l’aide de la gomme Stylet Surface.
- Ajout de la prise en charge de l’utilisation des touches de direction et de la barre d’espace pour dessiner sur les captures d’écran de commentaires en mode éditeur.
- Amélioration de la fiabilité des captures d’écran, afin qu’elles cessent d’apparaître en noir lors de la soumission de commentaires.
- Ajout de la prise en charge du thème sombre à la page locale du nouvel onglet qui s’affiche lorsque l’appareil n’est pas connecté à Internet.
- Ajout de la possibilité de restaurer les sites web installés en tant qu’applications de restauration lorsqu’une session de navigateur est restaurée après une mise à jour, un blocage, etc.
- Ajout d’une prise en charge de thème foncé à l’interface utilisateur PDF lorsque le navigateur est géré par une stratégie de groupe.
- Mise à jour d’Adobe Flash vers la version 32.0.0.321. [En savoir plus](https://helpx.adobe.com/flash-player/release-note/fp_32_air_32_release_notes.html)

### <a name="policy-updates"></a>Mises à jour de stratégie

#### <a name="new-policies"></a>Nouvelles stratégies

16 nouvelles stratégies ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [AlternateErrorPagesEnabled](./microsoft-edge-policies.md#alternateerrorpagesenabled) : suggère des pages similaires lorsqu’une page web est introuvable.
- [DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting) – Contrôle de l’utilisation d’exceptions de contenu non sécurisées.
- [DNSInterceptionChecksEnabled](./microsoft-edge-policies.md#dnsinterceptionchecksenabled) – Tests d’interception de DNS activés.
- [HideFirstRunExperience](./microsoft-edge-policies.md#hidefirstrunexperience) – Masque l’utilisation de la première exécution et l’écran de démarrage.
- [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) Autorise le contenu non sécurisé sur des sites spécifiques.
- [InsecureContentBlockedForUrls](./microsoft-edge-policies.md#insecurecontentblockedforurls) – Bloque le contenu non sécurisé sur des sites spécifiques.
- [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) – Active le paramètre de comportement de cookie SameSite hérité par défaut.
- [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) – Rétablissement du comportement SameSite hérité pour les cookies sur des sites spécifiques.
- [PaymentMethodQueryEnabled](./microsoft-edge-policies.md#paymentmethodqueryenabled) – Permet aux sites Web d’interroger les modes de paiement disponibles.
- [PersonalizationReportingEnabled](./microsoft-edge-policies.md#personalizationreportingenabled) – Permet de personnaliser des publicités, des recherches et des actualités en envoyant un historique de navigation à Microsoft.
- [PinningWizardAllowed](./microsoft-edge-policies.md#pinningwizardallowed) – Autorise l’assistant épingler à la barre des tâches.
- [SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled) – Configure Microsoft Defender SmartScreen pour bloquer les applications potentiellement indésirables.
- [TotalMemoryLimitMb](./microsoft-edge-policies.md#totalmemorylimitmb) – Définit une limite en mégaoctets de mémoire qu’une seule instance de Microsoft Edge peut utiliser.
- [WebAppInstallForceList](./microsoft-edge-policies.md#webappinstallforcelist) – Configure la liste des applications Web installées en force.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) – Réactive les composants WebPart de l’API v0 jusqu’au M84.
- [WebRtcLocalIpsAllowedUrls](./microsoft-edge-policies.md#webrtclocalipsallowedurls) – Gère l’exposition des adresses IP locales par WebRTC.

#### <a name="deprecated-policies"></a>Stratégies déconseillées

La stratégie suivante a été déconseillée.

- [NewTabPageCompanyLogo](./microsoft-edge-policies.md#newtabpagecompanylogo) – Définit le logo de la société sur l’onglet nouveau.

### <a name="resolved-issues"></a>Problèmes résolus

- Résolution d’un problème qui empêchait l’audio de fonctionner dans un environnement Citrix.
- Résolution d’un problème dans lequel l’expérience de Microsoft Edge et l’ancienne version de Microsoft Edge côte à côte généraient des liens hérités rompus et des blocages.

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)