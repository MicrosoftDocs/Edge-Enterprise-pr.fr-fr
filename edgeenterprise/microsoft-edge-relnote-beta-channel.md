---
title: Notes de publication de Microsoft Edge pour le canal bêta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 03/10/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notes de publication de Microsoft Edge pour le canal bêta
ms.openlocfilehash: 24fbf10b0b32ef4e64c74fdeaa4831bf01df7a87
ms.sourcegitcommit: 6d37cd6dc8618742f4729fc901fc66829dab462e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "11406245"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notes de publication du canal Microsoft Edge Beta

Ces notes de publication fournissent des informations sur les nouvelles fonctionnalités et les mises à jour non liées à la sécurité qui sont incluses dans le canal Microsoft Edge Beta. Les versions archivées de ces notes de publication sont disponibles [ici](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Nous avons mis à jour la note de mise à jour de la [version bêta de Microsoft Edge 89.0.774.18 : 3 février](#version-89077418-february-3) pour refléter les fonctionnalités qui ont été publiées.

## <a name="version-89077450-march-10"></a>Version 89.0.774.50 : 10 mars

Correction de divers bogues et problèmes de performance.

## <a name="version-89077448-march-8"></a>Version 89.0.774.48 : 8 mars

Correction de divers bogues et problèmes de performance.

## <a name="version-89077445-march-3"></a>Version 89.0.774.45 : 3 mars.

Résolution de divers bogues et problèmes de performances.

## <a name="version-89077439-february-26"></a>Version89.0.774.39: 26février

Résolution de divers bogues et problèmes de performances.

## <a name="version-89077434-february-22"></a>Version89.0.774.34: 22février

Résolution de divers bogues et problèmes de performances.

## <a name="version-89077427-february-12"></a>Version89.0.774.27: 12février

Résolution de divers bogues et de problèmes de performances.

## <a name="version-89077423-february-8"></a>Version 89.0.774.23: 8février

Résolution de divers bogues et de problèmes de performances.

<!-- begin major 89 -->
## <a name="version-89077418-february-3"></a>Version89.0.774.18 du 3février

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- **Le mode plein écran active des fonctionnalités de verrouillage supplémentaires.** À partir de la version89 de MicrosoftEdge, nous avons ajouté des fonctionnalités de verrouillage supplémentaires en mode plein écran pour permettre aux clients d’accomplir leur travail dans une expérience productive et plus sécurisée. [Si vous souhaitez en savoir plus](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **L’outil Enterprise Mode Site List Manager sera disponible dans le navigateur via la page *edge://compat* **. Vous pouvez utiliser cet outil pour créer, modifier et exporter votre liste de sites XML pour le mode Internet Explorer sur MicrosoftEdge. Vous pouvez activer l’accès à cet outil selon vos besoins par le biais de la stratégie de groupe. [Si vous souhaitez en savoir plus](https://docs.microsoft.com/deployedge/edge-ie-mode-site-list-manager).

- **Améliorer les performances du navigateur avec des onglets en veille**. Les onglets en veille améliorent les performances du navigateur en mettant les onglets inactifs en veille pour libérer des ressources système, telles que la mémoire et le processeur de sorte que les onglets actifs ou d’autres applications puissent les utiliser. Les utilisateurs peuvent empêcher la mise en veille de sites et configurer le délai avant qu’un onglet inactif ne soit mis en veille. Pour maintenir les utilisateurs dans leur flux, il existe également des [heuristiques](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) pour empêcher certains sites de passer en veille, tels que les sites intranet. Cette fonctionnalité peut être gérée avec des stratégies de groupe.

  > [!NOTE]
  > «Améliorer les performances du navigateur avec les onglets de mise en quarantaine» est une mise à jour des notes de publication du 3février pour la version majeure 89.0.774.18.

- **Réinitialisez manuellement vos données de synchronisation Microsoft Edge dans le cloud**. Nous introduisons un moyen de réinitialiser vos données de synchronisation MicrosoftEdge à partir du produit. Cela garantit que vos données sont effacées des services Microsoft, ainsi qu’une résolution de certains problèmes de produit qui nécessitaient auparavant un ticket de support.

- **Améliorations apportées à l’expérience de sélection de texte dans les documents PDF**. Les utilisateurs commenceront à obtenir une expérience de sélection de texte plus fluide et plus cohérente dans les documents PDF ouverts dans MicrosoftEdge à partir de la version89.

- **Date de naissance désormais prise en charge dans le remplissage automatique**. Aujourd’hui, MicrosoftEdge vous permet de gagner du temps et des efforts lors du remplissage de formulaires et de la création de comptes en ligne en remplissant automatiquement vos données telles que les adresses, les noms, les numéros de téléphone, etc. À partir de la version89 de MicrosoftEdge, nous ajoutons la prise en charge d’un autre champ que vous pouvez avoir enregistré et rempli automatiquement: la date de naissance. Vous pouvez afficher, modifier et supprimer ces informations à tout moment dans vos paramètres de profil.

- **Prise en charge de la recherche en langage naturel sur la barre d’adresses, la page de recherche de l’historique et le hub d’historique**. À partir de la version89 de MicrosoftEdge, la recherche d’un article/site web sera plus facile avec la recherche en langage naturel sur la barre d’adresses, la page d’historique et le concentrateur d’historique. Les utilisateurs peuvent rechercher le contenu/description/minutage des pages précédemment consultées (par exemple, «recette de gâteau de la semaine dernière») en plus des correspondances de mots clés de titres/URL. Cette fonctionnalité est limitée à un groupe d’utilisateurs sélectionnés de manière aléatoire et ayant activé l’expérimentation. Ces utilisateurs fournissent des commentaires à l’équipe chargée de la fonctionnalité.

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

- [BrowsingDataLifetime](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsingdatalifetime) - Paramètres de durée de vie des données de navigation
- [MAMEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#mamenabled) - Gestion des applications mobiles activée
- [DefinePreferredLanguages](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#definepreferredlanguages) : - Définir une liste ordonnée des langues préférées que les sites web doivent afficher si le site prend en charge la langue
- [ShowRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showrecommendationsenabled) : - Autoriser les recommandations et les notifications promotionnelles de Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingallowedbackgroundgraphicsmodes) : Restreindre le mode d’impression des graphiques d’arrière-plan
- [PrintingBackgroundGraphicsDefault](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingbackgroundgraphicsdefault): Mode d’impression des graphiques d’arrière-plan par défaut
- [SmartActionsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartactionsblocklist): Bloquer les actions intelligentes pour une liste de services

#### <a name="obsoleted-policies"></a>Stratégies obsolètes

- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy) : Utiliser une stratégie de référence par défaut de no-referrer-when-downgrade
- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) : Activer les rapports de données d’utilisation et d’incident
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices)|Envoyer des informations sur le site pour améliorer les services Microsoft
<!-- end major 89 -->

## <a name="version-88070556-january-29"></a>Version 88.0.705.56: 29janvier

Résolution de divers bogues et problèmes de performances.

## <a name="version-88070549-january-20"></a>Version 88.0.705.49 : 20 janvier

Résolution de divers bogues et problèmes de performances.

## <a name="version-88070545-january-15"></a>Version 88.0.705.45 : 15 janvier

Résolution de divers bogues et problèmes de performances.

## <a name="version-88070541-january-11"></a>Version 88.0.705.41 : 11 janvier

Résolution de divers bogues et problèmes de performances.

## <a name="version-88070529-december-21"></a>Version 88.0.705.29 : 21 décembre

Résolution de divers bogues et problèmes de performances.

<!-- begin major 88 -->
## <a name="version-88070518-december-9"></a>Version88.0.705.18: 9décembre

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- **Fonctionnalités obsolètes:**

  - Prise en charge du protocole FTP obsolète. La prise en charge du protocole FTP hérité a été supprimée de Microsoft Edge. Toute tentative d’accès à un lien FTP entraînera l’ouverture par le système d’exploitation d’une application externe pour gérer le lien FTP. Une autre solution pour les administrateurs informatiques consiste à configurer Microsoft Edge afin qu’il utilise le mode IE pour les sites qui dépendent du protocole FTP.
  - La prise en charge d’Adobe Flash sera supprimé. À partir de la version88 de Microsoft Edge Beta, la fonctionnalité et la prise en charge d’Adobe Flash seront supprimées. Pour en savoir plus: [Mise à jour concernant la fin de la prise en charge d’Adobe Flash Player – Blog Microsoft Edge (Windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentification:**

  - L’authentification unique (SSO) est désormais disponible pour les comptes Azure Active Directory (Azure AD) et le compte Microsoft (MSA) sur macOS et les versions inférieures de Windows. Un utilisateur connecté à Microsoft Edge sur macOS ou Microsoft Windows de version inférieure (7 et 8.1) est désormais connecté automatiquement aux sites web configurés pour autoriser l’authentification unique avec des comptes professionnels et Microsoft (par exemple, bing.com, office.com, msn.com, outlook.com).<br>Remarque: il est possible que l’utilisateur doive se déconnecter et se reconnecter s’il se connecte à une version antérieure à la version88 de Microsoft Edge pour utiliser cette fonctionnalité.
  - Basculer automatiquement les utilisateurs sur macOS vers leur profil de travail pour les sites qui s’authentifient avec leur compte professionnel. À partir de la version88 de Microsoft Edge, nous offrons la possibilité de basculer entre les sites qui s’authentifient avec le profil de travail de l’utilisateur sur macOS.<br>Remarque: il est possible que l’utilisateur doive se déconnecter et se reconnecter s’il se connecte à une version antérieure à la version88 de Microsoft Edge pour utiliser cette fonctionnalité.

- **Option du mode plein écran pour terminer la session.** Le bouton «Mettre fin à la session» est désormais disponible en mode plein écran dans l’expérience de navigation publique. Cette fonctionnalité permet de supprimer les données et paramètres du navigateur lorsque Microsoft Edge est fermé. Pour en savoir plus sur les fonctionnalités et la feuille de route du mode plein écran, voir [Configurer le mode plein écran Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).

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

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

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

#### <a name="deprecated-policies"></a>Stratégies déconseillées

Les stratégies suivantes sont déconseillées.

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled): active l’authentification proactive.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist): configure les règles de contournement du proxy.
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode): configure les paramètres du serveur proxy.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl): définit l’URL du fichier proxy .pac.
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver): configure l’adresse ou l’URL du serveur proxy.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies): autorise WebDriver à remplacer les stratégies incompatibles.

#### <a name="obsoleted-policies"></a>Stratégies obsolètes

Les stratégies suivantes sont obsolètes.

- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting): paramètre Adobe Flash par défaut.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls): autorise le plug-in Adobe Flash sur des sites spécifiques.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls): bloque le plug-in Adobe Flash sur des sites spécifiques.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode): étend le paramètre de contenu Adobe Flash à l’ensemble du contenu.

<!-- end major 88 -->

## <a name="version-87066455-december-3"></a>Version87.0.664.55: 3décembre

Résolution de divers bogues et problèmes de performances. La nouvelle fonctionnalité suivante est prise en charge dans cette version.

- **Des alertes sont générées si le mot de passe d’un utilisateur est détecté dans une fuite en ligne**. Les mots de passe des utilisateurs sont examinés par rapport à un référentiel d’informations d’identification connues qui ont été violées et envoient à l’utilisateur une alerte si une correspondance est trouvée. Pour garantir la sécurité et la confidentialité, les mots de passe des utilisateurs sont chiffrés et cryptés lorsqu’ils sont vérifiés par rapport à la base de données des informations d’identification divulguées.

## <a name="version-87066452-november-30"></a>Version 87.0.664.52: 30novembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-87066440-november-18"></a>Version 87.0.664.40: 18 novembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-87066436-november-16"></a>Version 87.0.664.36: 16 novembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-87066430-november-9"></a>Version 87.0.664.30: 9 novembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-87066424-november-2"></a>Version 87.0.664.24: 2 novembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-87066418-october-26"></a>Version87.0.664.18: 26octobre

Résolution de divers bogues et problèmes de performances.

<!-- begin major 87 -->
## <a name="version-87066412-october-20"></a>Version87.0.664.12: 20octobre

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- **Activation des fonctionnalités de confidentialité en mode plein écran**. Le démarrage des fonctionnalités du mode plein écran de Microsoft Edge version 87 qui permettront aux entreprises de respecter la confidentialité des données utilisateur, sera  activée. Ces fonctionnalités activent les expériences telles que l’effacement des données utilisateur à la fermeture, la suppression des fichiers téléchargés et la réinitialisation de l’expérience de démarrage configurée après une durée inactivité déterminée. En savoir plus sur la [Configuration du mode plein écran Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).
- **Activation du déploiement ClickOnce par défaut**. L’activation de ClickOnce par défaut dans Microsoft Edge 87, réduit les difficultés des entreprises à déployer des logiciels et mieux s’aligner sur le comportement du navigateur Microsoft Edge Legacy. Au démarrage de Microsoft Edge 87, l’état «Non Configuré» de la stratégie ClickOnceEnabled reflète le nouvel état par défaut Activé de la stratégie ClickOnce (comparé à l’État par défaut Désactivé précédent).
- **La page nouvel onglet de l’entreprise (NTP) intègre la productivité avec un contenu de flux de travail personnalisable**. La Page Nouvel Onglet de l’Entreprise combine la page de productivité d’Office 365 que nous proposons aux utilisateurs connectés à leur compte professionnel ou scolaire, avec des flux professionnels personnalisés qui sont organisés en une seule page. Les utilisateurs reconnaîtront le contenu Office 365 familier et Microsoft Search pour Entreprises offert par Bing. De plus, ils peuvent facilement retourner à «Mon Flux» personnalisable avec du contenu et des modules pertinents pour l’utilisateur, sa société ou son industrie, et à une sélection d’autres flux mis à disposition par l’organisation. [En savoir plus](https://docs.microsoft.com/microsoft-365/admin/manage/manage-industry-news?view=o365-worldwide&preserve-view=true).

- **Confidentialité et sécurité :**

  - Jeton TLS de support Obligatoire pour les sites configurés par une stratégie. Le jeton TLS obligatoire permet d’éviter les attaques par vol de jetons afin de s’assurer que les cookies ne peuvent pas être réutilisés à partir d’un autre appareil que l’appareil sur lequel ils ont été initialement définis. L’utilisation du jeton TLS obligatoire nécessite la définition de la stratégie [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) et nécessite que les sites répertoriés prennent en charge cette fonctionnalité.

- **Prise en charge du clavier pour le surligneur des fichiers PDF**. Les utilisateurs peuvent utiliser leurs touches de clavier pour surligner des textes de fichiers PDF.

- **Impression:**

  - Sélectionnez le côté à retourner lors de l’impression recto verso. Les utilisateurs peuvent choisir de retourner sur le côté long ou sur le côté court d’une feuille lors de l’impression recto verso.
  - Sélectionnez le mode de tramage de l’impression pour l’entreprise. Contrôlez l’impression Microsoft Edge sur une imprimante non-PostScript sur Windows. Parfois l’ impression sur des imprimantes non-PostScript doit être tramée pour imprimer correctement. Les options d’impression sont «Complètes» et «Rapides».

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

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

#### <a name="deprecated-policy"></a>Stratégie Déconseillée

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) - Configurez l’expérience de la page nouvel onglet de Microsoft Edge.

#### <a name="obsoleted-policy"></a>Stratégie obsolète

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) - Réactivez les fonctionnalités de plateforme web déconseillées pour une période limitée.

<!-- end major 87 -->

## <a name="version-86062243-october-16"></a>Version86.0.622.43: 16octobre

Résolution de divers bogues et problèmes de performances.

## <a name="version-86062236-october-7"></a>Version86.0.622.36: 7octobre

Résolution de divers bogues et problèmes de performances.

## <a name="version-86062231-october-1"></a>Version86.0.622.31: 1octobre

Résolution de divers bogues et problèmes de performances.

## <a name="version-86062228-september-28"></a>Version 86.0.622.28: 28 septembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-86062215-september-14"></a>Version 86.0.622.15: 14 septembre

Résolution de divers bogues et problèmes de performances.

<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
