---
title: Documentation relative aux stratégies du navigateur Microsoft Edge
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 09/28/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentation relative à toutes les stratégies prises en charge par le navigateur MicrosoftEdge pour Windows et Mac
ms.openlocfilehash: dc780166f05afd7d667f901a1198ce125831d01b
ms.sourcegitcommit: 3478cfcf2b03944213a7c7c61f05490bc37aa7c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/03/2020
ms.locfileid: "11094608"
---
# MicrosoftEdge: Stratégies
La dernière version de MicrosoftEdge inclut les stratégies suivantes. Vous pouvez utiliser ces stratégies pour configurer le fonctionnement de MicrosoftEdge dans votre organisation.

Si vous souhaitez en savoir plus sur un autre groupe de stratégies, utilisé pour contrôler la mise à jour de MicrosoftEdge, consultez la page [Informations de référence sur les stratégies de mise à jour de MicrosoftEdge](microsoft-edge-update-policies.md).

Vous pouvez télécharger le [Kit des ressources de conformité en matière de sécurité Microsoft](https://www.microsoft.com/download/details.aspx?id=55319) pour les paramètres de base de la configuration en matière de sécurité, recommandés pour MicrosoftEdge. Si vous souhaitez en savoir plus, consultez le [blog sur les bases de la sécurité Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines).

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

## Stratégies disponibles
Ces tableaux répertorient toutes les stratégies de groupe relatives au navigateur, disponibles dans cette version de MicrosoftEdge. Utilisez les liens dans le tableau pour obtenir plus de détails sur des stratégies données.

|||
|-|-|
|[Paramètres de l’application Guard](#application-guard-settings)|[Cast](#cast)|
|[Paramètres du contenu](#content-settings)|[Moteur de recherche par défaut](#default-search-provider)|
|[Extensions](#extensions)|[Authentification HTTP](#http-authentication)|
|[Paramètres du mode kiosque](#kiosk-mode-settings)|[Messagerie native](#native-messaging)|
|[Gestionnaire et protection des mots de passe](#password-manager-and-protection)|[Impression](#printing)|
|[Serveur proxy](#proxy-server)|[Paramètres SmartScreen](#smartscreen-settings)|
|[Démarrage, page d’accueil et page Nouvel onglet](#startup-home-page-and-new-tab-page)|[Supplémentaire](#additional)|


### [*Paramètres de l’application Guard*](#application-guard-settings-policies)
|Nom de la stratégie|Caption|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Proxy conteneur de Application Guard|
### [*Cast*](#cast-policies)
|Nom de la stratégie|Caption|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|Activer Google Cast|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|Afficher l’icône Cast dans la barre d’outils|
### [*Paramètres du contenu*](#content-settings-policies)
|Nom de la stratégie|Caption|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|Sélectionner automatiquement les certificats clients pour ces sites|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|Autoriser les cookies sur des sites spécifiques|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|Bloquer les cookies sur des sites spécifiques|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|Limiter les cookies de sites web spécifiques à la session en cours|
|[DefaultCookiesSetting](#defaultcookiessetting)|Configurer les cookies|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|Contrôler l’utilisation de l’API du système de fichiers pour la lecture|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|Contrôler l’utilisation de l’API du système de fichiers pour l’écriture|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|Paramètre par défaut de la géolocalisation|
|[DefaultImagesSetting](#defaultimagessetting)|Paramètre par défaut des images|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|Contrôler l’utilisation des exceptions pour le contenu non sécurisé|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|Paramètre par défaut de JavaScript|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|Paramètre par défaut des notifications|
|[DefaultPluginsSetting](#defaultpluginssetting)|Paramètre par défaut de AdobeFlash|
|[DefaultPopupsSetting](#defaultpopupssetting)|Paramètre par défaut de la fenêtre contextuelle|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Contrôler l’utilisation de l’API Web Bluetooth|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|Contrôler l’utilisation de l’API WebUSB|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|Autoriser l’accès en lecture via l’API du système de fichiers sur ces sites|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|Bloquer l’accès en lecture via l’API du système de fichiers sur ces sites|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|Autoriser l’accès en écriture aux fichiers et aux répertoires sur ces sites|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|Bloquer l’accès en écriture aux fichiers et aux répertoires sur ces sites|
|[ImagesAllowedForUrls](#imagesallowedforurls)|Autoriser les images sur ces sites|
|[ImagesBlockedForUrls](#imagesblockedforurls)|Bloquer les images sur des sites spécifiques|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|Autoriser le contenu non sécurisé sur les sites spécifiés|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|Bloquer le contenu non sécurisé sur les sites spécifiés|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|Autoriser JavaScript sur des sites spécifiques|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|Bloquer JavaScript sur des sites spécifiques|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|Activer le paramètre de comportement hérité par défaut du cookie SameSite|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|Revenir au comportement hérité de SameSite pour les cookies sur des sites spécifiés|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|Autoriser les notifications sur des sites spécifiques|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|Bloquer les notifications sur des sites spécifiques|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|Autoriser le plug-in AdobeFlash sur des sites spécifiques|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|Bloquer le plug-in Adobe Flash sur des sites spécifiques|
|[PopupsAllowedForUrls](#popupsallowedforurls)|Autoriser les fenêtres contextuelles sur des sites spécifiques|
|[PopupsBlockedForUrls](#popupsblockedforurls)|Bloquer les fenêtres contextuelles sur des sites spécifiques|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|Enregistrer les gestionnaires de protocoles|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|Déterminer si les utilisateurs peuvent recevoir des images d’arrière-plan et du texte personnalisés, des suggestions, des notifications,
et des conseils pour les services Microsoft|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|Accorder l’accès à des sites spécifiques pour la connexion à des périphériques USB spécifiques|
|[WebUsbAskForUrls](#webusbaskforurls)|Autoriser WebUSB sur des sites spécifiques|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|Bloquer WebUSB sur des sites spécifiques|
### [*Moteur de recherche par défaut*](#default-search-provider-policies)
|Nom de la stratégie|Caption|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|Activer le moteur de recherche par défaut|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|Encodages du moteur de recherche par défaut|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|Définit la fonctionnalité de recherche par image pour le moteur de recherche par défaut|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|Paramètres pour une URL d’image utilisant la méthode POST|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|Mot clé du moteur de recherche par défaut|
|[DefaultSearchProviderName](#defaultsearchprovidername)|Nom du moteur de recherche par défaut|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|URL de recherche du moteur de recherche par défaut|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|URL de suggestions de recherche du moteur de recherche par défaut|
|[NewTabPageSearchBox](#newtabpagesearchbox)|Configurer l’expérience de zone de recherche dans la nouvelle page d’onglets|
### [*Extensions*](#extensions-policies)
|Nom de la stratégie|Caption|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|Configurer les types d’extension autorisés|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|Autoriser l’installation d’extensions spécifiques|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|Déterminer les extensions ne pouvant pas être installées|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|Contrôler l’installation silencieuse de certaines extensions|
|[ExtensionInstallSources](#extensioninstallsources)|Configurer les sources d’installation des extensions et des scripts d’utilisateur|
|[ExtensionSettings](#extensionsettings)|Configurer les paramètres de gestion des extensions|
### [*Authentification HTTP*](#http-authentication-policies)
|Nom de la stratégie|Caption|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|Autoriser les invites d’authentification HTTP à origines multiples|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Définit une liste des serveurs auxquels MicrosoftEdge peut déléguer les informations d’identification de l’utilisateur|
|[AuthSchemes](#authschemes)|Méthodes d’authentification prises en charge|
|[AuthServerAllowlist](#authserverallowlist)|Configurer la liste des serveurs d’authentification autorisés|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Désactiver la consultation CNAME lors de la négociation de l’authentification Kerberos|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Inclure un port non standard dans le SPN Kerberos|
|[NtlmV2Enabled](#ntlmv2enabled)|Contrôler l’activation de l’authentification NTLMv2|
### [*Paramètres du mode kiosque*](#kiosk-mode-settings-policies)
|Nom de la stratégie|Caption|
|-|-|
|[KioskDeleteDownloadsOnExit](#kioskdeletedownloadsonexit)|Supprimer les fichiers téléchargés dans le cadre d’une session kiosque lorsque MicrosoftEdge se ferme|
### [*Messagerie native*](#native-messaging-policies)
|Nom de la stratégie|Caption|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|Contrôler les hôtes de messagerie native que les utilisateurs peuvent utiliser|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|Configurer la liste rouge de la messagerie native|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|Autoriser les hôtes de messagerie native côté utilisateur (installés sans autorisation d’administrateur)|
### [*Gestionnaire et protection des mots de passe*](#password-manager-and-protection-policies)
|Nom de la stratégie|Caption|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|Activer l’enregistrement des mots de passe dans le gestionnaire de mots de passe|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|Autoriser les utilisateurs à être avertis si leur mot de passe est considéré comme dangereux|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|Configurer l’URL de modification du mot de passe|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|Configurer la liste des URL de connexion d’entreprise dans lesquelles le service de protection par mot de passe doit capturer les codes de hachage d’un mot de passe|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|Configurer le déclencheur d’avertissement de protection par mot de passe|
### [*Impression*](#printing-policies)
|Nom de la stratégie|Caption|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|Instructions de sélection de l’imprimante par défaut|
|[PrintHeaderFooter](#printheaderfooter)|Imprimer des en-têtes et des pieds de page|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|Définir l’imprimante par défaut du système comme imprimante par défaut|
|[PrintingEnabled](#printingenabled)|Activer l’impression|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|Taille de page par défaut pour l’impression|
|[UseSystemPrintDialog](#usesystemprintdialog)|Imprimer via la boîte de dialogue Imprimer du système|
### [*Serveur proxy*](#proxy-server-policies)
|Nom de la stratégie|Caption|
|-|-|
|[ProxyBypassList](#proxybypasslist)|Configurer les règles de contournement du proxy|
|[ProxyMode](#proxymode)|Configurer les paramètres du serveur proxy|
|[ProxyPacUrl](#proxypacurl)|Définir l’URL du fichier .pac du proxy|
|[ProxyServer](#proxyserver)|Configurer l’adresse ou l’URL du serveur proxy|
|[ProxySettings](#proxysettings)|Paramètres du proxy|
### [*Paramètres SmartScreen*](#smartscreen-settings-policies)
|Nom de la stratégie|Caption|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|Empêcher le contournement des avertissements de Microsoft Defender SmartScreen pour les sites|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|Empêcher le contournement des avertissements de Microsoft Defender SmartScreen pour les téléchargements|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|Configurer la liste des domaines pour lesquels Microsoft Defender SmartScreen ne déclenche pas d’avertissement|
|[SmartScreenEnabled](#smartscreenenabled)|Configurer Microsoft Defender SmartScreen|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|Forcer Microsoft Defender SmartScreen à vérifier les téléchargements provenant de sources approuvées|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|Configurer Microsoft Defender SmartScreen pour bloquer les applications potentiellement indésirables.|
### [*Démarrage&comma; page d’accueil et page Nouvel onglet*](#startup-home-page-and-new-tab-page-policies)
|Nom de la stratégie|Caption|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|Définir la page Nouvel onglet comme page d’accueil|
|[HomepageLocation](#homepagelocation)|Configurer l’URL de la page d’accueil|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|Configurer les types d’arrière-plan autorisés pour la disposition du nouvel onglet|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|Définir le logo de l’entreprise sur la page Nouvel onglet (obsolète)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|Masquer les sites populaires par défaut dans la page Nouvel onglet|
|[NewTabPageLocation](#newtabpagelocation)|Configurer l’URL de la page Nouvel onglet|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|Définir les liens rapides de la page Nouvel onglet|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|Activer le préchargement de la nouvelle page d’onglet pour un rendu plus rapide|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Configurer l’expérience de la page Nouvel onglet MicrosoftEdge|
|[RestoreOnStartup](#restoreonstartup)|Action à effectuer au démarrage|
|[RestoreOnStartupURLs](#restoreonstartupurls)|Sites à ouvrir lors du démarrage du navigateur|
|[ShowHomeButton](#showhomebutton)|Afficher le bouton Accueil sur la barre d’outils|
### [*Supplémentaire*](#additional-policies)
|Nom de la stratégie|Caption|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|Activer les suggestions de la Recherche Microsoft dans la barre d’adresse de Bing|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|Paramètres des annonces pour les sites contenant des annonces gênantes|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|Activer la suppression de l’historique du navigateur et de l’historique des téléchargements|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|Autoriser les boîtes de dialogue de sélection de fichier|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|Autorise une page à afficher les fenêtres contextuelles pendant son déchargement|
|[AllowSurfGame](#allowsurfgame)|Autoriser le jeu de surf|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|Autoriser les pages à envoyer des demandes XHR synchrones lors de l’opération de rejet de page (déconseillé)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|Configurer la liste des sites avec lesquels MicrosoftEdge tentera d’établir une liaison de jetons|
|[AllowTrackingForUrls](#allowtrackingforurls)|Configurer les exceptions de prévention du suivi pour des sites spécifiques|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|Suggérer des pages similaires lorsqu’une page web est introuvable|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|Toujours ouvrir les fichiers PDF en externe|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|Activer l’authentification par le bruit ambiant pour les profils d’invité et InPrivate|
|[AppCacheForceEnabled](#appcacheforceenabled)|Permet de réactiver la fonctionnalité AppCache, même si elle est désactivée par défaut.|
|[ApplicationLocaleValue](#applicationlocalevalue)|Définir les paramètres régionaux de l’application|
|[AudioCaptureAllowed](#audiocaptureallowed)|Autoriser ou bloquer la capture de sons|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|Sites autorisés à accéder aux appareils de capture audio sans autorisation préalable|
|[AudioSandboxEnabled](#audiosandboxenabled)|Autoriser l’exécution du bac à sable audio|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|Importer automatiquement les données et les paramètres d’un autre navigateur lors de la première exécution|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|Définir une liste de protocoles qui peuvent lancer une application externe à partir d’origines, sans inviter l’utilisateur|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|URL où AutoOpenFileTypes peut s’appliquer|
|[AutoOpenFileTypes](#autoopenfiletypes)|Liste des types de fichiers qui doivent être automatiquement ouverts au téléchargement|
|[AutofillAddressEnabled](#autofilladdressenabled)|Activer la saisie automatique pour les adresses|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|Activer la saisie automatique pour les cartes de crédit|
|[AutoplayAllowed](#autoplayallowed)|Autoriser la lecture automatique de média pour les sites web|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Poursuivre l’exécution des applications en arrière-plan après la fermeture de MicrosoftEdge|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|Active les mises à jour en arrière-plan dans la liste des modèles disponibles pour Collections et d’autres fonctionnalités qui utilisent des modèles|
|[BingAdsSuppression](#bingadssuppression)|Bloquer toutes les annonces dans les résultats de recherche Bing|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|Bloquer les cookies tiers|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|Activer la création de profil à partir du menu déroulant Identité ou de la page Paramètres|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|Activer le mode Invité|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|Autoriser l’envoi de requêtes à un service horaire du navigateur|
|[BrowserSignin](#browsersignin)|Paramètres de connexion du navigateur|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|Utiliser le client DNS intégré|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|Indique si le vérificateur de certificats intégré est utilisé pour la vérification des certificats de serveur (déconseillé)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|Désactiver l’application des règles de transparence des certificats pour une liste de hachages subjectPublicKeyInfo|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|Désactiver l’application des règles de transparence des certificats pour une liste d’autorités de certification héritées|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|Désactiver l’application des règles de transparence des certificats pour des URL spécifiques|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Effacer les données de navigation lors de la fermeture de MicrosoftEdge|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Effacer les images et les fichiers mis en cache lors de la fermeture de MicrosoftEdge|
|[ClickOnceEnabled](#clickonceenabled)|Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole ClickOnce|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|Bloquer l’accès à une liste spécifiée de services et de cibles d’exportations dans Collections|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|Activer les avertissements de sécurité pour les indicateurs de ligne de commande|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Activer les mises à jour des composants dans MicrosoftEdge|
|[ConfigureDoNotTrack](#configuredonottrack)|Configurer Ne pas me suivre|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Configurer la connexion automatique avec un compte de domaine Active Directory en l’absence de compte de domaine Azure AD|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|Configurer la synthèse vocale en ligne|
|[ConfigureShare](#configureshare)|Configurer l’expérience de partage|
|[CustomHelpLink](#customhelplink)|Spécifier le lien d’aide personnalisé|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|Vérifications d’interception DNS activées|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Définir MicrosoftEdge comme navigateur par défaut|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|Autoriser l’accès au menu contextuel du moteur de recherche par défaut|
|[DefaultSensorsSetting](#defaultsensorssetting)|Paramètre par défaut des capteurs|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Contrôler l’utilisation de l’API Serial|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|Exiger que la liste des sites en mode entreprise soit disponible avant la navigation à l’onglet|
|[DeleteDataOnMigration](#deletedataonmigration)|Supprimer les anciennes données de navigateur lors de la migration|
|[DeveloperToolsAvailability](#developertoolsavailability)|Contrôler où les outils de développement peuvent être utilisés|
|[DiagnosticData](#diagnosticdata)|Envoyer les données de diagnostic requises et facultatives relatives à l’utilisation du navigateur|
|[DirectInvokeEnabled](#directinvokeenabled)|Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole DirectInvoke|
|[Disable3DAPIs](#disable3dapis)|Désactiver la prise en charge des API graphiques 3D|
|[DisableScreenshots](#disablescreenshots)|Désactiver la création de captures d’écran|
|[DiskCacheDir](#diskcachedir)|Définir le répertoire du cache disque|
|[DiskCacheSize](#diskcachesize)|Définir la taille du cache disque, en octets|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|Contrôler le mode du protocole DNS-over-HTTPS|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|Spécifier le modèle d’URI du programme de résolution DNS-over-HTTPS souhaité|
|[DownloadDirectory](#downloaddirectory)|Définir le répertoire de téléchargement|
|[DownloadRestrictions](#downloadrestrictions)|Autoriser les restrictions de téléchargement|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|Activer la fonctionnalité Collections|
|[EditFavoritesEnabled](#editfavoritesenabled)|Autorise les utilisateurs à modifier les favoris|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|Réactiver les fonctionnalités des plateformes web déconseillées pendant une durée limitée|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|Activer le téléchargement des actions de domaine à partir de Microsoft|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|Activer les vérifications OCSP/CRL en ligne|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|Autoriser les certificats signés à l’aide de l’algorithme SHA-1 lorsqu’ils sont émis par des ancres d’approbation locales (obsolète)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|Autoriser les extensions gérées de manière à utiliser l’API de plateforme de matériel d’entreprise|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|Autoriser l’accès à l’outil Enterprise Mode Site List Manager|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|Désactiver le téléchargement des avertissements basés sur l’extension de fichier pour les types de fichiers spécifiés sur les domaines|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Contrôler la communication avec le service d’expérimentation et de configuration|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|Afficher une case à cocher «Toujours ouvrir» dans la boîte de dialogue de protocole externe|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|Autoriser les utilisateurs à configurer le contrôle parental|
|[FavoritesBarEnabled](#favoritesbarenabled)|Activer la barre des favoris|
|[ForceBingSafeSearch](#forcebingsafesearch)|Appliquer le filtre adulte Bing|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|Configurer la sélection automatique d’un certificat par MicrosoftEdge lorsqu’il existe plusieurs correspondances de certificats pour un site configuré avec «AutoSelectCertificateForUrls»|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|Activer l’utilisation des profils éphémères|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Appliquer le filtre adulte Google|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|Utiliser une stratégie de renvoi par défaut no-referrer-when-downgrade (déconseillé).|
|[ForceNetworkInProcess](#forcenetworkinprocess)|Forcer l’exécution du code de mise en réseau dans le processus du navigateur (obsolète)|
|[ForceSync](#forcesync)|Forcer la synchronisation des données du navigateur et ne pas afficher l’invite de consentement de synchronisation|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|Forcer le mode restreint minimal sur YouTube|
|[FullscreenAllowed](#fullscreenallowed)|Autoriser le mode plein écran|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|Activer le cache d’authentification HTTP de portée globale.|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|Forcer la navigation directe sur le site intranet au lieu de rechercher des entrées à mots uniques dans la barre d’adresses|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|Configurer la liste des noms qui vont contourner la vérification de stratégie HSTS|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|Utiliser l’accélération matérielle lorsque celle-ci est disponible|
|[HideFirstRunExperience](#hidefirstrunexperience)|Masquer l’expérience de première utilisation et l’écran de démarrage|
|[ImportAutofillFormData](#importautofillformdata)|Autoriser l’importation des données de saisie automatique|
|[ImportBrowserSettings](#importbrowsersettings)|Autoriser l’importation des paramètres du navigateur|
|[ImportCookies](#importcookies)|Autoriser l’importation des cookies|
|[ImportExtensions](#importextensions)|Autoriser l’importation des extensions|
|[ImportFavorites](#importfavorites)|Autoriser l’importation des favoris|
|[ImportHistory](#importhistory)|Autoriser l’importation de l’historique de navigation|
|[ImportHomepage](#importhomepage)|Autoriser l’importation des paramètres de la page d’accueil|
|[ImportOpenTabs](#importopentabs)|Autoriser l’importation des onglets ouverts|
|[ImportPaymentInfo](#importpaymentinfo)|Autoriser l’importation des informations de paiement|
|[ImportSavedPasswords](#importsavedpasswords)|Autoriser l’importation des mots de passe enregistrés|
|[ImportSearchEngine](#importsearchengine)|Autoriser l’importation des paramètres du moteur de recherche|
|[ImportShortcuts](#importshortcuts)|Autoriser l’importation des raccourcis|
|[InPrivateModeAvailability](#inprivatemodeavailability)|Configurer la disponibilité du mode InPrivate|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|Activer les avertissements pour les formulaires non sécurisés|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|Contrôler la fonctionnalité IntensiveWakeUpThrottling|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Configurer la détection de blocage avancée pour le mode Internet Explorer|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Configurer l’intégration d’Internet Explorer|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|Configurer la liste des sites en mode Entreprise|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Spécifier le comportement des navigations «sur la page» vers des sites non configurés lors du démarrage à partir des pages du mode Internet Explorer.|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Autoriser le test du mode InternetExplorer|
|[IsolateOrigins](#isolateorigins)|Activer l’isolation de site pour des origines spécifiques|
|[LocalProvidersEnabled](#localprovidersenabled)|Autoriser les suggestions des fournisseurs de services locaux|
|[ManagedFavorites](#managedfavorites)|Configurer les favoris|
|[ManagedSearchEngines](#managedsearchengines)|Gérer les moteurs de recherche|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|Nombre maximal de connexions simultanées au serveur proxy|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|Autoriser Google Cast à se connecter aux appareils Cast sur toutes les adresses IP|
|[MetricsReportingEnabled](#metricsreportingenabled)|Activer les rapports de données d’utilisation et d’incident (déconseillé)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|Activer l’occlusion de fenêtre native|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|Définition d’un délai d’expiration pour la navigation à l’onglet de la liste des sites en mode entreprise|
|[NetworkPredictionOptions](#networkpredictionoptions)|Activer la prédiction réseau|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|Configurer la connexion automatique du profil par défaut de l’utilisateur avec son compte professionnel ou scolaire|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|Contrôler l’application des restrictions de sécurité aux origines non sécurisées|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Autoriser les sites web à vérifier les modes de paiement disponibles|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|Autoriser la personnalisation des publicités, de la recherche et des actualités en envoyant un historique de navigation à Microsoft|
|[PinningWizardAllowed](#pinningwizardallowed)|Autoriser l’Assistant Épingler à la barre des tâches|
|[ProactiveAuthEnabled](#proactiveauthenabled)|Activer l’authentification proactive|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|Activer le contenu promotionnel dans les onglets|
|[PromptForDownloadLocation](#promptfordownloadlocation)|Demander où enregistrer les fichiers téléchargés|
|[QuicAllowed](#quicallowed)|Autoriser le protocole QUIC|
|[RelaunchNotification](#relaunchnotification)|Avertir un utilisateur qu’un redémarrage du navigateur est recommandé ou requis pour les mises à jour en attente|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|Définir la période d’affichage pour les notifications de mise à jour|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|Activer l’intégrité du code du convertisseur|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|Spécifier si les vérifications OCSP/CRL en ligne sont requises pour les ancres d’approbation locales|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Activer la résolution des erreurs de navigation à l’aide d’un service web|
|[RestrictSigninToPattern](#restrictsignintopattern)|Limiter les comptes qui peuvent être utilisés comme comptes principaux sur MicrosoftEdge|
|[RoamingProfileLocation](#roamingprofilelocation)|Définition du répertoire de profil itinérant|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Activer l’utilisation des copies itinérantes pour les données de profil Microsoft Edge|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Étendre le paramètre de contenu Adobe Flash à l’ensemble du contenu|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|Autoriser les utilisateurs à poursuivre la navigation depuis une page d’avertissement SSL|
|[SSLVersionMin](#sslversionmin)|Version TLS minimale activée|
|[SaveCookiesOnExit](#savecookiesonexit)|Enregistrer les cookies lors de la fermeture de MicrosoftEdge|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|Désactiver l’enregistrement de l’historique du navigateur|
|[ScreenCaptureAllowed](#screencaptureallowed)|Autoriser ou interdire la capture d’écran|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|Activer le défilement jusqu’au texte spécifié dans les fragments d’URL|
|[SearchSuggestEnabled](#searchsuggestenabled)|Activer les suggestions de recherche|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|Sites web ou domaines automatiquement autorisés à utiliser l’attestation de clé de sécurité directe|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|Envoyer tous les sites intranet vers Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Envoyer des informations sur les sites pour améliorer les services Microsoft (déconseillé)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|Autoriser l’accès aux capteurs sur des sites spécifiques|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|Bloquer l’accès aux capteurs sur des sites spécifiques|
|[SerialAskForUrls](#serialaskforurls)|Autoriser l’API Serial sur des sites spécifiques|
|[SerialBlockedForUrls](#serialblockedforurls)|Bloquer l’API Serial sur des sites spécifiques|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Afficher le raccourci MicrosoftOffice dans la barre des favoris (déconseillé)|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Activer la prise en charge de Signed HTTP Exchange (SXG) |
|[SitePerProcess](#siteperprocess)|Activer l’isolation de site pour tous les sites|
|[SpellcheckEnabled](#spellcheckenabled)|Activer la vérification orthographique|
|[SpellcheckLanguage](#spellchecklanguage)|Activer des langues spécifiques pour la vérification orthographique|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|Forcer la désactivation de langues spécifiques pour la vérification orthographique|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|Activer l’utilisation d’un traitement plus strict pour les contenus mixtes (déconseillé)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|Supprimer l’avertissement relatif au système d’exploitation non pris en charge|
|[SyncDisabled](#syncdisabled)|Désactiver la synchronisation des données à l’aide des services de synchronisation Microsoft|
|[SyncTypesListDisabled](#synctypeslistdisabled)|Configurer la liste des types exclus de la synchronisation|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|Activer une fonctionnalité de sécurité TLS1.3 pour les ancres d’approbation locales (obsolète)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|Spécifier les suites de chiffrement TLS à désactiver|
|[TabFreezingEnabled](#tabfreezingenabled)|Autoriser le gel des onglets d’arrière-plan|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|Activer la possibilité de mettre fin aux processus dans le gestionnaire des tâches|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|Définir une limite de mémoire en mégaoctets qu’une seule instance de MicrosoftEdge peut utiliser|
|[TrackingPrevention](#trackingprevention)|Bloquer le suivi de l’activité de navigation sur le web des utilisateurs|
|[TranslateEnabled](#translateenabled)|Activer la traduction|
|[URLAllowlist](#urlallowlist)|Définir une liste d’URL autorisées|
|[URLBlocklist](#urlblocklist)|Bloquer l’accès à une liste d’URL|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|Activer la fonctionnalité User-Agent Client Hints (déconseillé)|
|[UserDataDir](#userdatadir)|Définir le répertoire de données utilisateur|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|Limite le nombre de captures instantanées des données utilisateur conservées qui sont utilisées en cas de restauration d’urgence|
|[UserFeedbackAllowed](#userfeedbackallowed)|Autoriser les commentaires des utilisateurs|
|[VideoCaptureAllowed](#videocaptureallowed)|Autoriser ou bloquer la capture de vidéos|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|Sites autorisés à accéder aux appareils de capture vidéo sans autorisation préalable|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|Définir l’optimisation WPAD|
|[WebAppInstallForceList](#webappinstallforcelist)|Configurer la liste des applications web dont l’installation est forcée|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|Réactiver l'API Web Components v0 jusqu'à M84 (obsolète)|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|Autoriser WebDriver à remplacer les stratégies incompatibles (obsolète)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|Gérer l’exposition des adresses IP locales par WebRTC|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|Limiter l’exposition de l’adresse IP locale par WebRTC|
|[WebRtcUdpPortRange](#webrtcudpportrange)|Restreindre la portée des ports UDP locaux utilisés par WebRTC|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Utiliser la résolution du proxy Windows (déconseillée)|




  ## Stratégies de paramètres de Application Guard

  [Retour au début](#microsoft-edge---policies)

  ### ApplicationGuardContainerProxy
  #### Proxy conteneur de Application Guard
  
  
  #### Versions prises en charge:
  - Sur Windows depuis la version84 ou versions ultérieures

  #### Description
  Configure les paramètres de proxy pour Microsoft Edge Application Guard.
Si vous activez cette stratégie, Microsoft Edge Application Guard ignore les autres sources de configuration proxy.

Si vous ne configurez pas cette stratégie, Microsoft Edge Application Guard utilise la configuration proxy de l’hôte.

Cette stratégie n’affecte pas la configuration par proxy de Microsoft Edge en dehors de Application Guard (sur l’hôte).

Le champ ProxyMode vous permet de spécifier le serveur proxy utilisé par MicrosoftEdge Application Guard.

Le champ ProxyPacUrl est une URL d’un fichier .pac du proxy.

Le champ ProxyServer est une URL pour le serveur proxy.

Si vous choisissez la valeur ’direct’ comme ’ProxyMode’, tous les autres champs sont ignorés.

Si vous choisissez la valeur ’auto_detect’ comme ’ProxyMode’, tous les autres champs sont ignorés.

Si vous choisissez la valeur «fixed_servers» comme « ProxyMode », le champs « ProxyServer» est utilisé.

Si vous choisissez la valeur 'pac_script' comme 'ProxyMode', le champ 'ProxyPacUrl' est utilisé.

Pour plus d’informations sur l’identification du trafic Application Guard via un proxy double, visitez [https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Dictionary

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ApplicationGuardContainerProxy
  - Nom de stratégie de groupe : Proxy conteneur de Application Guard
  - Chemin d’accès de la stratégie de groupe(obligatoire): Paramètres des modèles administratifs/Microsoft Edge/Application Guard
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur : ApplicationGuardContainerProxy
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  

  [Retour au début](#microsoft-edge---policies)

  ## Stratégies Cast

  [Retour au début](#microsoft-edge---policies)

  ### EnableMediaRouter
  #### Activer Google Cast
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Activez cette stratégie pour activer Google Cast. Les utilisateurs pourront le lancer à partir du menu de l’application, des menus contextuels de la page, des commandes multimédias sur les sites web compatibles avec Cast, et (le cas échéant) de l’icône Cast sur la barre d’outils.

Désactivez cette stratégie pour désactiver Google Cast.

Par défaut, Google Cast est activé.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: EnableMediaRouter
  - Nom de la stratégie de groupe: Activer Google Cast
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Cast
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: EnableMediaRouter
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: EnableMediaRouter
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ShowCastIconInToolbar
  #### Afficher l’icône Cast dans la barre d’outils
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Attribuez la valeur true à cette stratégie pour afficher l’icône Cast dans la barre d’outils ou le menu latéral. Les utilisateurs ne pourront pas la supprimer.

Si cette stratégie n’est pas configurée ou si elle est désactivée, les utilisateurs peuvent épingler ou supprimer l’icône depuis son menu contextuel.

Si vous avez également configuré la stratégie [EnableMediaRouter](#enablemediarouter) sur false, cette stratégie est ignorée et l’icône de la barre d’outils n’apparaît pas.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ShowCastIconInToolbar
  - Nom de la stratégie de groupe: afficher l’icône Cast dans la barre d’outils
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Cast
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ShowCastIconInToolbar
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ShowCastIconInToolbar
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ## Stratégies des paramètres de contenu

  [Retour au début](#microsoft-edge---policies)

  ### AutoSelectCertificateForUrls
  #### Sélectionner automatiquement les certificats clients pour ces sites
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  La définition de stratégie vous permet de créer une liste de modèles d’URL spécifiant les sites pour lesquels MicrosoftEdge peut automatiquement sélectionner un certificat client. La valeur est un groupe de dictionnaires JSON à séquences, chacun ayant le format { «modèle»: «$URL_PATTERN», «filtre»: $FILTER }, où $URL_PATTERN correspond à un schéma de paramètres de contenu. $FILTER limite les certificats client à partir desquels le navigateur effectue une sélection automatique. Indépendamment du filtre, seuls les certificats correspondant à la demande de certificats du serveur sont sélectionnés.

Exemples d’utilisation de la section $FILTER:

* Lorsque $FILTER est défini sur { «ÉMETTEUR»: { «CN»: «$ISSUER_CN» } }, seuls les certificats client émis par un certificat dont la valeur CommonName est $ISSUER_CN sont sélectionnés.

* Lorsque $FILTER comprend les sections «ÉMETTEUR» et «OBJET», seuls les certificats clients répondant aux deux conditions sont sélectionnés.

* Lorsque $FILTER comprend une section «OBJET» avec la valeur «O», un certificat nécessite au moins une organisation qui correspond à la valeur spécifiée à sélectionner.

* Lorsque $FILTER comprend une section «OBJET» avec une valeur «OU», un certificat nécessite au moins une unité organisationnelle qui correspond à la valeur spécifiée à sélectionner.

* Lorsque $FILTER est défini sur {}, la sélection de certificats client ne fait pas l’objet de restrictions supplémentaires. Notez que les filtres fournis par le serveur web continuent de s’appliquer.

Si la stratégie reste non définie, il n’existe pas de sélection automatique des sites.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AutoSelectCertificateForUrls
  - Nom de la stratégie de groupe: sélectionner automatiquement les certificats clients pour ces sites
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AutoSelectCertificateForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### CookiesAllowedForUrls
  #### Autoriser les cookies sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez une liste des sites, basés sur des formats d’URL, qui sont autorisés à définir des cookies.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultCookiesSetting](#defaultcookiessetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

Si vous souhaitez en savoir plus, consultez les stratégies [CookiesBlockedForUrls](#cookiesblockedforurls) et [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls).

Il ne peut pas y avoir de modèles d’URL en conflit définis entre ces trois stratégies:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

Pour exclure la suppression des cookies lors de la fermeture, configurez la stratégie de [SaveCookiesOnExit](#savecookiesonexit).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: CookiesAllowedForUrls
  - Nom de la stratégie de groupe: autoriser les cookies sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: CookiesAllowedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### CookiesBlockedForUrls
  #### Bloquer les cookies sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez une liste des sites, basés sur des formats d’URL, qui ne sont pas autorisés à définir des cookies.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultCookiesSetting](#defaultcookiessetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

Si vous souhaitez en savoir plus, consultez les stratégies [CookiesAllowedForUrls](#cookiesallowedforurls) et [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls).

Il ne peut pas y avoir de modèles d’URL en conflit définis entre ces trois stratégies:

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: CookiesBlockedForUrls
  - Nom de la stratégie de groupe: bloquer les cookies sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: CookiesBlockedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### CookiesSessionOnlyForUrls
  #### Limiter les cookies de sites web spécifiques à la session en cours
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Les cookies, créés par les sites web qui correspondent à un modèle d’URL déterminés, sont supprimés à la fin de la session (lors de la fermeture de la fenêtre).

Les cookies créés par les sites web qui ne correspondent pas au modèle sont contrôlés par la stratégie [DefaultCookiesSetting](#defaultcookiessetting), si elle est définie, ou par la configuration personnelle de l’utilisateur. Il s’agit également du comportement par défaut si cette stratégie n’est pas configurée.

Si MicrosoftEdge s’exécute en mode arrière-plan, la session peut rester ouverte lors de la fermeture de la dernière fenêtre, ce qui signifie que les cookies ne seront pas effacés lors de la fermeture de la fenêtre. Si vous souhaitez en savoir plus sur la configuration de ce comportement, consultez la stratégie [BackgroundModeEnabled](#backgroundmodeenabled).

Vous pouvez également utiliser les stratégies [CookiesAllowedForUrls](#cookiesallowedforurls) et [CookiesBlockedForUrls](#cookiesblockedforurls) pour contrôler les sites web pouvant créer des cookies.

Il ne peut pas y avoir de modèles d’URL en conflit définis entre ces trois stratégies:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

Si vous définissez la stratégie [RestoreOnStartup](#restoreonstartup) de manière à restaurer les URL à partir des sessions précédentes, cette stratégie est ignorée et les cookies sont stockés définitivement pour ces sites. 

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: CookiesSessionOnlyForUrls
  - Nom de la stratégie de groupe: limiter les cookies de sites web spécifiques à la session en cours
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: CookiesSessionOnlyForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultCookiesSetting
  #### Configurer les cookies
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez si les sites web peuvent créer des cookies sur l’appareil de l’utilisateur. Il s’agit de la stratégie du «tout ou rien»: vous pouvez autoriser tous les sites web à créer des cookies, ou bien, aucun site web ne peut en créer. Vous ne pouvez pas utiliser cette stratégie pour activer les cookies provenant de sites web spécifiques.

Définissez la stratégie sur « SessionOnly » pour effacer les cookies à la fermeture de la session. Si MicrosoftEdge s’exécute en mode arrière-plan, la session peut rester ouverte lors de la fermeture de la dernière fenêtre, ce qui signifie que les cookies ne seront pas effacés lors de la fermeture de la fenêtre. Si vous souhaitez en savoir plus sur la configuration de ce comportement, consultez la stratégie [BackgroundModeEnabled](#backgroundmodeenabled).

Si cette stratégie n’est pas configurée, la valeur par défaut « AllowCookies » est utilisée ; les utilisateurs peuvent, en accédant aux paramètres de MicrosoftEdge, le modifier. (Si vous souhaitez que les utilisateurs ne puissent pas modifier ce paramètre, configurez la stratégie.)

Mappage des options de stratégie:

* AllowCookies (1)=Permettre à tous les sites de créer des cookies

* BlockCookies (2)=Ne permettre à aucun site de créer des cookies

* SessionOnly (4) = conserver les cookies pendant la durée de la session, sauf ceux listés dans [SaveCookiesOnExit](#savecookiesonexit)

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultCookiesSetting
  - Nom de la stratégie de groupe: configurer les cookies
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultCookiesSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultCookiesSetting
  - Exemple de valeur:
``` xml
<integer>1</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultFileSystemReadGuardSetting
  #### Contrôler l’utilisation de l’API du système de fichiers pour la lecture
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Si vous configurez cette stratégie sur 3, les sites web peuvent demander l’accès en lecture au système de fichiers du système d’exploitation hôte à l’aide de l’API du système de fichiers. Si vous attribuez la valeur 2 à cette stratégie, l’accès est refusé.

Si vous ne configurez pas cette stratégie, les sites web peuvent demander l’accès. Les utilisateurs peuvent modifier ce paramètre.

Mappage des options de stratégie:

* BlockFileSystemRead (2) = ne pas autoriser les sites à demander l’accès en lecture aux fichiers et aux répertoires via l’API du système de fichiers

* AskFileSystemRead (3) = autoriser les sites à demander à l’utilisateur d’accorder l’accès en lecture aux fichiers et aux répertoires via l’API du système de fichiers

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultFileSystemReadGuardSetting
  - Nom de stratégie de groupe:contrôler l’utilisation de l’API du système de fichiers pour la lecture
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultFileSystemReadGuardSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultFileSystemReadGuardSetting
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultFileSystemWriteGuardSetting
  #### Contrôler l’utilisation de l’API du système de fichiers pour l’écriture
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Si vous configurez cette stratégie sur 3, les sites web peuvent demander l’accès en écriture au système de fichiers du système d’exploitation hôte à l’aide de l’API du système de fichiers. Si vous attribuez la valeur 2 à cette stratégie, l’accès est refusé.

Si vous ne configurez pas cette stratégie, les sites web peuvent demander l’accès. Les utilisateurs peuvent modifier ce paramètre.

Mappage des options de stratégie:

* BlockFileSystemWrite (2) = ne pas autoriser les sites à demander l’accès en écriture aux fichiers et aux répertoires

* AskFileSystemWrite (3) = autoriser les sites à demander à l’utilisateur d’accorder l’accès en écriture aux fichiers et aux répertoires

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultFileSystemWriteGuardSetting
  - Nom de stratégie de groupe:contrôler l’utilisation de l’API du système de fichiers pour l’écriture
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultFileSystemWriteGuardSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: DefaultFileSystemWriteGuardSetting
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultGeolocationSetting
  #### Paramètre par défaut de la géolocalisation
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indiquez si les sites web sont autorisés à suivre la position géographique des utilisateurs. Vous pouvez autoriser le suivi par défaut (« AllowGeolocation »), le refuser par défaut (« BlockGeolocation ») ou faire en sorte que l’utilisateur reçoive un message chaque fois qu’un site Web demande sa localisation (« AskGeolocation »).

Si cette stratégie n’est pas configurée, l’option « AskGeolocation » est utilisée et l’utilisateur peut la modifier.

Mappage des options de stratégie:

* AllowGeolocation (1)=Autoriser les sites à suivre la position géographique des utilisateurs

* BlockGeolocation (2)=N’autoriser aucun site à suivre la position géographique des utilisateurs

* AskGeolocation (3)=Demander chaque fois qu’un site souhaite suivre la position géographique des utilisateurs

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultGeolocationSetting
  - Nom de la stratégie de groupe: paramètre par défaut de la géolocalisation
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultGeolocationSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultGeolocationSetting
  - Exemple de valeur:
``` xml
<integer>1</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultImagesSetting
  #### Paramètre par défaut des images
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indiquez si les sites web sont autorisés à afficher des images. Vous pouvez autoriser les images sur tous les sites (« AllowImages ») ou les bloquer sur tous les sites (« BlockImages »).

Si cette stratégie n’est pas configurée, les images sont autorisées par défaut et l’utilisateur peut modifier ce paramètre.

Mappage des options de stratégie:

* AllowImages (1)=Autoriser tous les sites à afficher toutes les images

* BlockImages (2)=N’autoriser aucun site à afficher les images

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultImagesSetting
  - Nom de la stratégie de groupe: paramètre par défaut des images
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultImagesSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultImagesSetting
  - Exemple de valeur:
``` xml
<integer>1</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultInsecureContentSetting
  #### Contrôler l’utilisation des exceptions pour le contenu non sécurisé
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Vous permet de définir si les utilisateurs peuvent ajouter ou non des exceptions qui autorisent l’affichage de contenu mixte sur des sites spécifiques. 

Cette stratégie peut être remplacée pour des modèles d’URL spécifiques par les stratégies [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) et [InsecureContentBlockedForUrls](#insecurecontentblockedforurls).

Si cette stratégie n’est pas définie, les utilisateurs peuvent ajouter des exceptions qui autorisent le contenu mixte blocable et peuvent désactiver les mises à niveau automatique pour le contenu mixte blocable en option.

Mappage des options de stratégie:

* BlockInsecureContent (2)=N’autoriser aucun site à charger le contenu mixte

* AllowExceptionsInsecureContent (3) = Autoriser les utilisateurs à ajouter des exceptions afin d’autoriser le contenu mixte

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultInsecureContentSetting
  - Nom de la stratégie de groupe: contrôler l’utilisation des exceptions pour le contenu non sécurisé
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultInsecureContentSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultInsecureContentSetting
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultJavaScriptSetting
  #### Paramètre par défaut de JavaScript
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indiquez si les sites web sont autorisés à exécuter JavaScript. Vous pouvez l’autoriser pour tous les sites («AllowJavaScript») ou le bloquer pour tous les sites («BlockJavaScript»).

Si cette stratégie n’est pas configurée, tous les sites peuvent exécuter JavaScript par défaut, et l’utilisateur peut modifier ce paramètre.

Mappage des options de stratégie:

* AllowJavaScript (1)=Autoriser tous les sites à exécuter JavaScript

* BlockJavaScript (2)=N’autoriser aucun site à exécuter JavaScript

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultJavaScriptSetting
  - Nom de la stratégie de groupe: paramètre par défaut de JavaScript
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultJavaScriptSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultJavaScriptSetting
  - Exemple de valeur:
``` xml
<integer>1</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultNotificationsSetting
  #### Paramètre par défaut des notifications
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indiquez si les sites web sont autorisés à afficher des notifications de bureau. Vous pouvez autoriser l’affichage des notifications par défaut (« AllowNotifications »), le refuser par défaut (« BlockNotifications ») ou l’utilisateur peut recevoir un message chaque fois qu’un site veut afficher une notification (« AskNotifications »).

Si cette stratégie n’est pas configurée, les notifications sont autorisées par défaut et l’utilisateur peut modifier ce paramètre.

Mappage des options de stratégie:

* AllowNotifications (1)=Autoriser les sites à afficher les notifications de bureau

* BlockNotifications (2)=N’autoriser aucun site à afficher les notifications de bureau

* AskNotifications (3)=Demander chaque fois qu’un site souhaite afficher les notifications de bureau

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultNotificationsSetting
  - Nom de la stratégie de groupe: paramètre par défaut des notifications
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultNotificationsSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultNotificationsSetting
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultPluginsSetting
  #### Paramètre par défaut de AdobeFlash
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  [PluginsAllowedForUrls](#pluginsallowedforurls) et [PluginsBlockedForUrls](#pluginsblockedforurls) sont vérifiés en premier, avant cette stratégie. Les options sont «ClickToPlay» et «BlockPlugins». Si vous définissez cette stratégie sur «BlockPlugins», ce plugin est refusé pour tous les sites web. «ClickToPlay» permet au plugin Flash de s’exécuter, mais les utilisateurs cliquent sur l’espace réservé pour le démarrer.

Si cette stratégie n’est pas configurée, l’utilisateur peut modifier ce paramètre manuellement.

Remarque: la lecture automatique est utilisée uniquement pour les domaines répertoriés explicitement dans la stratégie [PluginsAllowedForUrls](#pluginsallowedforurls). Pour activer la lecture automatique pour tous les sites, ajoutez http://* et https://* à la liste des URL autorisées.

Mappage des options de stratégie:

* BlockPlugins (2)=Bloquer le plug-in Adobe Flash

* ClickToPlay (3) = Cliquez pour exécuter

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultPluginsSetting
  - Nom de la stratégie de groupe: paramètre par défaut de Adobe Flash
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultPluginsSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultPluginsSetting
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultPopupsSetting
  #### Paramètre par défaut de la fenêtre contextuelle
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indiquez si les sites web sont autorisés à afficher des fenêtres contextuelles. Vous pouvez autoriser les fenêtres contextuelles sur tous les sites web (« AllowPopups ») ou les bloquer sur tous les sites (« BlockPopups »).

Si cette stratégie n’est pas configurée, les fenêtres contextuelles sont bloquées par défaut et les utilisateurs peuvent modifier ce paramètre.

Mappage des options de stratégie:

* AllowPopups (1)=Autoriser tous les sites à afficher des fenêtres contextuelles

* BlockPopups (2) = N’autoriser aucun site à afficher des fenêtres contextuelles

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultPopupsSetting
  - Nom de la stratégie de groupe: paramètre par défaut de la fenêtre contextuelle
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultPopupsSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultPopupsSetting
  - Exemple de valeur:
``` xml
<integer>1</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultWebBluetoothGuardSetting
  #### Contrôler l’utilisation de l’API Web Bluetooth
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez si les sites web sont autorisés à accéder aux appareils Bluetooth à proximité. Vous pouvez bloquer complètement l’accès ou obliger le site à demander à l’utilisateur chaque fois qu’il souhaite accéder à un appareil Bluetooth.

Si cette stratégie n’est pas configurée, la valeur par défaut (« AskWebBluetooth », c’est-à-dire que les utilisateurs sont interrogés à chaque fois) est utilisée et les utilisateurs peuvent la modifier.

Mappage des options de stratégie:

* BlockWebBluetooth (2)=N’autoriser aucun site à demander l’accès à des appareils Bluetooth à l’aide de l’API Web Bluetooth

* AskWebBluetooth (3)=Autoriser des sites à demander à l’utilisateur d’accorder l’accès à un appareil Bluetooth à proximité

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultWebBluetoothGuardSetting
  - Nom de la stratégie de groupe: contrôler l’utilisation de l’API Web Bluetooth
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultWebBluetoothGuardSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultWebBluetoothGuardSetting
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultWebUsbGuardSetting
  #### Contrôler l’utilisation de l’API WebUSB
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indiquez si les sites web sont autorisés à accéder à des périphériques USB connectés. Vous pouvez bloquer complètement l’accès ou interroger l’utilisateur chaque fois qu’un site web souhaite accéder à des appareils USB connectés.

Vous pouvez remplacer cette stratégie pour des modèles d’URL spécifiques par les stratégies [WebUsbAskForUrls](#webusbaskforurls) et [WebUsbBlockedForUrls](#webusbblockedforurls).

Si cette stratégie n’est pas configurée, des sites peuvent demander aux utilisateurs s’ils sont autorisés à accéder aux appareils USB connectés (« AskWebUsb ») par défaut, et les utilisateurs peuvent modifier ce paramètre.

Mappage des options de stratégie:

* BlockWebUsb (2)=N’autoriser aucun site à demander l’accès à des appareils USB via l’API WebUSB

* AskWebUsb (3)=Autoriser des sites à demander à l’utilisateur d’accorder l’accès à un appareil USB

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultWebUsbGuardSetting
  - Nom de la stratégie de groupe: contrôler l’utilisation de l’API WebUSB
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultWebUsbGuardSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultWebUsbGuardSetting
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### FileSystemReadAskForUrls
  #### Autoriser l’accès en lecture via l’API du système de fichiers sur ces sites
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  La définition de la stratégie vous permet de répertorier les modèles d’URL qui indiquent quels sites peuvent inviter les utilisateurs à leur octroyer l’accès en lecture aux fichiers ou aux répertoires dans le système de fichiers du système d’exploitation hôte via l’API du système de fichiers.

Laisser la stratégie en suspens signifie la [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) s’applique à tous les sites, s’il est défini. Si ce n'est pas le cas, les paramètres personnels des utilisateurs s'appliquent.

Les modèles d’URL ne peuvent pas entrer en conflit avec [FileSystemReadBlockedForUrls](#filesystemreadblockedforurls). Aucune stratégie n’est prioritaire si une URL correspond à la fois.

Si vous souhaitez obtenir plus d’informations sur les modèles d’URL valides, consultez https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Name unique de la stratégie de groupe: FileSystemReadAskForUrls
  - Nom de la stratégie de groupe: autoriser l’accès en lecture via l’API du système de fichiers sur ces sites
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\2 = "[*.]example.edu"

```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: FileSystemReadAskForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### FileSystemReadBlockedForUrls
  #### Bloquer l’accès en lecture via l’API du système de fichiers sur ces sites
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Si vous définissez cette stratégie, vous pouvez répertorier les modèles d’URL qui indiquent quels sites peuvent inviter les utilisateurs à leur octroyer l’accès en lecture aux fichiers ou aux répertoires dans le système de fichiers du système d’exploitation hôte via l’API du système de fichiers.

Si vous ne configurez pas cette stratégie, [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) s’applique à tous les sites, s’il est paramétré. Si ce n'est pas le cas, les paramètres personnels des utilisateurs s'appliquent.

Les modèles d’URL ne peuvent pas entrer en conflit avec [FileSystemReadAskForUrls](#filesystemreadaskforurls). Aucune stratégie n’est prioritaire si une URL correspond à la fois.

Si vous souhaitez obtenir plus d’informations sur les modèles d’URL valides, consultez https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Name unique de la stratégie de groupe: FileSystemReadBlockedForUrls
  - Nom de la stratégie de groupe: bloquer l’accès en lecture via l’API du système de fichiers sur ces sites
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\2 = "[*.]example.edu"

```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: FileSystemReadBlockedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### FileSystemWriteAskForUrls
  #### Autoriser l’accès en écriture aux fichiers et aux répertoires sur ces sites
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Si vous définissez cette stratégie, vous pouvez répertorier les modèles d’URL qui indiquent quels sites peuvent inviter les utilisateurs à leur octroyer l’accès en écriture aux fichiers ou aux répertoires dans le système de fichiers du système d’exploitation hôte.

Si vous ne configurez pas cette stratégie, [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) s’applique à tous les sites, s’il est paramétré. Si ce n'est pas le cas, les paramètres personnels des utilisateurs s'appliquent.

Les modèles d’URL ne peuvent pas entrer en conflit avec [FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls). Aucune stratégie n’est prioritaire si une URL correspond à la fois.

Si vous souhaitez obtenir plus d’informations sur les modèles d’URL valides, consultez https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Name unique de la stratégie de groupe: FileSystemWriteAskForUrls
  - Nom de la stratégie de groupe: Autoriser l’accès en écriture aux fichiers et aux répertoires sur ces sites
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\2 = "[*.]example.edu"

```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: FileSystemWriteAskForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### FileSystemWriteBlockedForUrls
  #### Bloquer l’accès en écriture aux fichiers et aux répertoires sur ces sites
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Si vous définissez cette stratégie, vous pouvez répertorier les modèles d’URL qui indiquent quels sites peuvent inviter les utilisateurs à leur octroyer l’accès en écriture aux fichiers ou aux répertoires dans le système de fichiers du système d’exploitation hôte.

Si vous ne configurez pas cette stratégie, [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) s’applique à tous les sites, s’il est paramétré. Si ce n'est pas le cas, les paramètres personnels des utilisateurs s'appliquent.

Les modèles d’URL ne peuvent pas entrer en conflit avec [FileSystemWriteAskForUrls](#filesystemwriteaskforurls). Aucune stratégie n’est prioritaire si une URL correspond à la fois.

Si vous souhaitez obtenir plus d’informations sur les modèles d’URL valides, consultez https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Name unique de la stratégie de groupe: FileSystemWriteBlockedForUrls
  - Nom de la stratégie de groupe: bloquer l’accès en écriture aux fichiers et aux répertoires sur ces sites
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\2 = "[*.]example.edu"

```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: FileSystemWriteBlockedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImagesAllowedForUrls
  #### Autoriser les images sur ces sites
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez une liste des sites, basés sur des formats d’URL, qui sont autorisés à afficher des images.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultImagesSetting](#defaultimagessetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImagesAllowedForUrls
  - Nom de la stratégie de groupe: autoriser les images sur ces sites
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImagesAllowedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImagesBlockedForUrls
  #### Bloquer les images sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez une liste des sites, basés sur des formats d’URL, qui ne sont pas autorisés à afficher des images.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultImagesSetting](#defaultimagessetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImagesBlockedForUrls
  - Nom de la stratégie de groupe: bloquer les images sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImagesBlockedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### InsecureContentAllowedForUrls
  #### Autoriser le contenu non sécurisé sur les sites spécifiés
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Créez une liste de modèles d’URL pour spécifier les sites pouvant afficher du contenu mixte non sécurisé (contenu HTTP sur les sites HTTPS).

Si cette stratégie n’est pas configurée, le contenu mixte pouvant être bloqué le sera et le contenu mixte pouvant facultativement être bloqué sera mis à jour. Toutefois, les utilisateurs seront autorisés à définir des exceptions pour autoriser du contenu mixte non sécurisé pour des sites spécifiques. 

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: InsecureContentAllowedForUrls
  - Nom de la stratégie de groupe: autoriser le contenu non sécurisé sur les sites spécifiés
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: InsecureContentAllowedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### InsecureContentBlockedForUrls
  #### Bloquer le contenu non sécurisé sur les sites spécifiés
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Créez une liste des modèles d’URL pour spécifier les sites qui ne sont pas autorisés à afficher du contenu mixte blocable, c’est-à-dire actif, (contenu HTTP sur des sites HTTPS) et pour lesquels les mises à jour du contenu mixte pouvant facultativement être bloqué vont être désactivées.

Si cette stratégie n’est pas configurée, le contenu mixte pouvant être bloqué le sera et le contenu mixte pouvant facultativement être bloqué sera mis à jour. Toutefois, les utilisateurs seront autorisés à définir des exceptions pour autoriser du contenu mixte non sécurisé pour des sites spécifiques. 

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: InsecureContentBlockedForUrls
  - Nom de la stratégie de groupe: bloquer le contenu non sécurisé sur les sites spécifiés
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: InsecureContentBlockedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### JavaScriptAllowedForUrls
  #### Autoriser JavaScript sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez une liste des sites, basés sur des formats d’URL, qui sont autorisés à exécuter JavaScript.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultJavaScriptSetting](#defaultjavascriptsetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: JavaScriptAllowedForUrls
  - Nom de la stratégie de groupe: autoriser JavaScript sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: JavaScriptAllowedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### JavaScriptBlockedForUrls
  #### Bloquer JavaScript sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez une liste des sites, basés sur des formats d’URL, qui ne sont pas autorisés à exécuter JavaScript.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultJavaScriptSetting](#defaultjavascriptsetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: JavaScriptBlockedForUrls
  - Nom de la stratégie de groupe: bloquer JavaScript sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: JavaScriptBlockedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### LegacySameSiteCookieBehaviorEnabled
  #### Activer le paramètre de comportement hérité par défaut du cookie SameSite
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Vous permet de rétablir le comportement SameSite hérité pour tous les cookies. Le rétablissement du comportement hérité entraîne le traitement des cookies qui ne spécifient pas d’attribut SameSite comme s’ils étaient «SameSite=None», supprime la condition requise pour que les cookies «SameSite=None» transportent l’attribut «Secure» et ignore la comparaison de schéma lorsque vous évaluez si deux sites sont same-site.

Si vous ne configurez pas cette stratégie, le comportement SameSite par défaut pour les cookies dépend d’autres sources de configuration pour la fonctionnalité SameSite par défaut, la fonctionnalité Cookies-without-SameSite-must-be-secure et la fonctionnalité Schemeful Same-Site. Ces fonctionnalités peuvent également être configurées à l’aide d’une version d’évaluation de terrain ou de l’indicateur same-site-by-default-cookies, l’indicateur cookies-without-same-site-must-be-secure ou l’indicateur schemeful-same-site dans edge://flags.

Mappage des options de stratégie:

* DefaultToLegacySameSiteCookieBehavior (1) = Rétablir le comportement SameSite hérité pour les cookies sur tous les sites

* DefaultToSameSiteByDefaultCookieBehavior (2) = Utiliser le comportement SameSite par défaut pour les cookies sur tous les sites

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: LegacySameSiteCookieBehaviorEnabled
  - Nom de la stratégie de groupe: activer le paramètre de comportement hérité par défaut du cookie SameSite
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: LegacySameSiteCookieBehaviorEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: LegacySameSiteCookieBehaviorEnabled
  - Exemple de valeur:
``` xml
<integer>1</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList
  #### Revenir au comportement hérité de SameSite pour les cookies sur des sites spécifiés
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Les cookies définis pour les domaines correspondant aux modèles spécifiés sont rétablis vers le comportement SameSite hérité. 

Le rétablissement du comportement hérité entraîne le traitement des cookies qui ne spécifient pas d’attribut SameSite comme s’ils étaient «SameSite=None», supprime la condition requise pour que les cookies «SameSite=None» transportent l’attribut «Secure» et ignore la comparaison de schéma lorsque vous évaluez si deux sites sont same-site.

Si cette stratégie n’est pas configurée, la valeur globale par défaut est utilisée. La valeur globale par défaut est également utilisée pour les cookies sur les domaines non couverts par les modèles que vous spécifiez.

La valeur globale par défaut peut être configurée à l’aide de la stratégie [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled). Si [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) n’est pas définie, la valeur globale par défaut revient aux autres sources de configuration.

Les modèles que vous répertoriez dans cette stratégie sont traités comme des domaines, et non comme des URL. Vous ne devez donc pas spécifier des schémas ou des ports.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Nom de la stratégie de groupe: revenir au comportement hérité de SameSite pour les cookies sur des sites spécifiés
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Exemple de valeur:
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NotificationsAllowedForUrls
  #### Autoriser les notifications sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Vous permet de créer une liste de modèles d’URL pour spécifier les sites autorisés à afficher les notifications.

Si cette stratégie n’est pas configurée, la valeur globale par défaut est utilisée pour tous les sites. Cette valeur par défaut est comprise dans la stratégie [DefaultNotificationsSetting](#defaultnotificationssetting) si elle est définie, ou à partir de la configuration personnelle de l’utilisateur. Pour plus d’informations sur les modèles d’URL valides, consultez [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: NotificationsAllowedForUrls
  - Nom de la stratégie de groupe: autoriser les notifications sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: NotificationsAllowedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NotificationsBlockedForUrls
  #### Bloquer les notifications sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Vous permet de créer une liste de modèles d’URL pour spécifier les sites non autorisés à afficher les notifications.

Si cette stratégie n’est pas configurée, la valeur globale par défaut est utilisée pour tous les sites. Cette valeur par défaut est comprise dans la stratégie [DefaultNotificationsSetting](#defaultnotificationssetting) si elle est définie, ou à partir de la configuration personnelle de l’utilisateur. Pour plus d’informations sur les modèles d’URL valides, consultez [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: NotificationsBlockedForUrls
  - Nom de la stratégie de groupe: bloquer les notifications sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: NotificationsBlockedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PluginsAllowedForUrls
  #### Autoriser le plug-in AdobeFlash sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez une liste des sites, basés sur des formats d’URL, qui sont autorisés à exécuter le plug-in Adobe Flash.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultPluginsSetting](#defaultpluginssetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

Pour plus d’informations sur les modèles d’URL valides, consultez [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Toutefois, à partir de M85, les motifs avec les caractères génériques «*» et «[*] » dans l’hôte ne sont plus pris en charge pour cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PluginsAllowedForUrls
  - Nom de la stratégie de groupe: autoriser le plug-in Adobe Flash sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PluginsAllowedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PluginsBlockedForUrls
  #### Bloquer le plug-in Adobe Flash sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez une liste des sites, basés sur des formats d’URL, qui ne sont pas autorisés à exécuter Adobe Flash.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultPluginsSetting](#defaultpluginssetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

Pour plus d’informations sur les modèles d’URL valides, consultez [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Toutefois, à partir de M85, les motifs avec les caractères génériques «*» et «[*] » dans l’hôte ne sont plus pris en charge pour cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PluginsBlockedForUrls
  - Nom de la stratégie de groupe: bloquer le plug-in Adobe Flash sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PluginsBlockedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PopupsAllowedForUrls
  #### Autoriser les fenêtres contextuelles sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez une liste des sites, basés sur des formats d’URL, qui sont autorisés à ouvrir des fenêtres contextuelles.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultPopupsSetting](#defaultpopupssetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PopupsAllowedForUrls
  - Nom de la stratégie de groupe: autoriser les fenêtres contextuelles sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PopupsAllowedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PopupsBlockedForUrls
  #### Bloquer les fenêtres contextuelles sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez une liste des sites, basés sur des formats d’URL, qui ne sont pas autorisés à ouvrir des fenêtres contextuelles.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultPopupsSetting](#defaultpopupssetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PopupsBlockedForUrls
  - Nom de la stratégie de groupe: bloquer les fenêtres contextuelles sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PopupsBlockedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### RegisteredProtocolHandlers
  #### Enregistrer les gestionnaires de protocoles
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Définissez cette stratégie (recommandé uniquement) pour inscrire une liste de gestionnaires de protocoles. Cette liste est fusionnée avec celles inscrites par l’utilisateur et toutes peuvent être utilisées.

Enregistrer un gestionnaire de protocoles :

- Attribuez la propriété de protocole au schéma (par exemple «mailto»)
- Définissez la propriété URL sur la propriété URL de l’application qui gère le schéma spécifié dans le champ « Protocole ». Le modèle peut inclure le paramètre substituable « %s », qui sera remplacé par l’URL traitée.

Les utilisateurs ne peuvent pas supprimer un gestionnaire de protocoles inscrit par cette stratégie. Ils peuvent toutefois installer un nouveau gestionnaire de protocoles par défaut pour outrepasser les gestionnaires de protocoles existants.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Non
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Dictionary

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: RegisteredProtocolHandlers
  - Nom de la stratégie de groupe: enregistrer les gestionnaires de protocoles
  - Chemin d’accès de la stratégie de groupe (obligatoire): N/A
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Content settings
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): N/A
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: RegisteredProtocolHandlers
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: RegisteredProtocolHandlers
  - Exemple de valeur:
``` xml
<key>RegisteredProtocolHandlers</key>
<array>
  <dict>
    <key>default</key>
    <true/>
    <key>protocol</key>
    <string>mailto</string>
    <key>url</key>
    <string>https://mail.contoso.com/mail/?extsrc=mailto&url=%s</string>
  </dict>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SpotlightExperiencesAndRecommendationsEnabled
  #### Déterminer si les utilisateurs peuvent recevoir des images d’arrière-plan et du texte personnalisés, des suggestions, des notifications,
et des conseils pour les services Microsoft
  
  
  #### Versions prises en charge:
  - Sur Windows depuis la version86 ou ultérieur

  #### Description
  Déterminer si les utilisateurs peuvent recevoir des images d’arrière-plan et du texte personnalisés, des suggestions, des notifications et des conseils pour les services Microsoft.

Si vous activez ou ne configurez pas ce paramètre, les expériences à la une et les recommandations sont activées.

Si vous désactivez ce paramètre, les expériences à la une et les recommandations sont désactivées.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SpotlightExperiencesAndRecommendationsEnabled
  - Nom de la stratégie de groupe: déterminer si les utilisateurs peuvent recevoir des images d’arrière-plan et du texte personnalisés, des suggestions, des notifications et des conseils pour les services Microsoft
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: SpotlightExperiencesAndRecommendationsEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)

  ### WebUsbAllowDevicesForUrls
  #### Accorder l’accès à des sites spécifiques pour la connexion à des périphériques USB spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Vous permet de définir une liste d’URL qui spécifient les sites qui seront automatiquement autorisés à accéder à un appareil USB avec les ID de produit et de fournisseur spécifiés. Chaque élément de la liste doit contenir à la fois les appareils et les URL pour que la stratégie soit valide. Chaque élément des appareils peut contenir un champ d’ID fournisseur et produit. Tout ID omis est traité comme un caractère générique avec une exception et cette exception indique qu’un ID produit ne peut pas être spécifié sans qu’un ID fournisseur soit également spécifié. Sinon, la stratégie n’est pas valide et est ignorée.

Le modèle d’autorisation USB utilise l’URL du site demandeur («URL de demande») et l’URL du site de niveau supérieur («URL d’incorporation») pour accorder l’autorisation à l’URL de demande d’accéder au périphérique USB. L’URL de demande peut être différente de l’URL d’incorporation si le site demandeur est chargé dans un iframe. Par conséquent, le champ «URL» peut contenir jusqu’à deux chaînes d’URL, séparées par une virgule, pour spécifier respectivement l’URL de demande et l’URL d’incorporation. Si une seule URL est spécifiée, l’accès aux périphériques USB correspondants est accordé lorsque l’URL du site demandeur correspond à cette URL, quel que soit le statut d’incorporation. Les URL dans «url» doivent être des URL valides, sinon la stratégie est ignorée.

Si cette stratégie n’est pas définie, la valeur globale par défaut est utilisée pour tous les sites à partir de la stratégie [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting), si elle est définie, ou de la configuration personnelle de l’utilisateur. 

Les modèles d’URL de cette stratégie ne doivent pas entrer en conflit avec ceux configurés via [WebUsbBlockedForUrls](#webusbblockedforurls). En cas de conflit, cette stratégie prévaut sur les stratégies [WebUsbBlockedForUrls](#webusbblockedforurls) et [WebUsbAskForUrls](#webusbaskforurls).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Dictionary

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: WebUsbAllowDevicesForUrls
  - Nom de la stratégie de groupe: accorder l’accès à des sites spécifiques pour la connexion à des périphériques USB spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: WebUsbAllowDevicesForUrls
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAllowDevicesForUrls = [
  {
    "devices": [
      {
        "product_id": 5678, 
        "vendor_id": 1234
      }
    ], 
    "urls": [
      "https://contoso.com", 
      "https://fabrikam.com"
    ]
  }
]
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: WebUsbAllowDevicesForUrls
  - Exemple de valeur:
``` xml
<key>WebUsbAllowDevicesForUrls</key>
<array>
  <dict>
    <key>devices</key>
    <array>
      <dict>
        <key>product_id</key>
        <integer>5678</integer>
        <key>vendor_id</key>
        <integer>1234</integer>
      </dict>
    </array>
    <key>urls</key>
    <array>
      <string>https://contoso.com</string>
      <string>https://fabrikam.com</string>
    </array>
  </dict>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### WebUsbAskForUrls
  #### Autoriser WebUSB sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Définissez une liste des sites, basés sur des formats d’URL, qui sont autorisés à demander à l’utilisateur l’accès à un périphérique USB.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

Les modèles d’URL définis dans cette stratégie ne peuvent pas entrer en conflit avec ceux configurés dans la stratégie [WebUsbBlockedForUrls](#webusbblockedforurls): vous ne pouvez pas à la fois autoriser et bloquer une URL. Pour plus d’informations sur les modèles d’URL valides, veuillez consulter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: WebUsbAskForUrls
  - Nom de la stratégie de groupe: autoriser WebUSB sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: WebUsbAskForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### WebUsbBlockedForUrls
  #### Bloquer WebUSB sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Définissez une liste des sites, basés sur des formats d’URL, qui ne sont pas autorisés à demander à l’utilisateur l’accès à un périphérique USB.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

Les modèles d’URL dans cette stratégie ne peuvent pas être en conflit avec ceux configurés dans la stratégie [WebUsbAskForUrls](#webusbaskforurls). Vous ne pouvez pas à la fois autoriser et bloquer une URL.   Pour plus d’informations sur les modèles d’URL valides, consultez [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: WebUsbBlockedForUrls
  - Nom de la stratégie de groupe: bloquer WebUSB sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Content settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: WebUsbBlockedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ## Stratégies du moteur de recherche par défaut

  [Retour au début](#microsoft-edge---policies)

  ### DefaultSearchProviderEnabled
  #### Activer le moteur de recherche par défaut
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet d’utiliser un moteur de recherche par défaut.

Si vous activez cette stratégie, un utilisateur peut rechercher un terme en le tapant dans la barre d’adresses (tant que ce n’est pas une URL).

Vous pouvez définir le moteur de recherche par défaut à utiliser en activant le reste des stratégies de recherche par défaut. Si celles-ci sont vides (non configurés) ou configurées de manière incorrecte, l’utilisateur peut choisir le moteur de recherche par défaut.

Si vous désactivez cette stratégie, l’utilisateur ne peut pas effectuer de recherche depuis la barre d’adresses.

Si vous activez ou désactivez cette stratégie, les utilisateurs ne peuvent ni la modifier, ni la remplacer.

Si vous ne configurez pas cette stratégie, le moteur de recherche par défaut est activé, et l’utilisateur peut le choisir et définir la liste des moteurs de recherche.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

À partir de Microsoft Edge 84, vous pouvez utiliser cette stratégie comme stratégie recommandée.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultSearchProviderEnabled
  - Nom de la stratégie de groupe: activer le moteur de recherche par défaut
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Default search provider
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Fournisseur de recherche par défaut
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: DefaultSearchProviderEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultSearchProviderEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultSearchProviderEncodings
  #### Encodages du moteur de recherche par défaut
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifiez les codages de caractères pris en charge par le moteur de recherche. Les encodages sont des noms de page de codes comme UTF-8, GB2312 et ISO-8859-1. Elles sont testées dans l’ordre indiqué.

Cette stratégie est facultative. Si cette option n’est pas configurée, la valeur par défaut UTF-8 est utilisée.

Cette stratégie est appliquée uniquement si vous activez les stratégies [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

À partir de Microsoft Edge 84, vous pouvez utiliser cette stratégie comme stratégie recommandée. Si l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée ne sera pas ajouté à la liste des fournisseurs de recherche parmi lesquels l’utilisateur peut faire son choix. S’il s’agit du comportement souhaité, utilisez la stratégie [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultSearchProviderEncodings
  - Nom de la stratégie de groupe: encodages du moteur de recherche par défaut
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Default search provider
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Fournisseur de recherche par défaut
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended\DefaultSearchProviderEncodings
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultSearchProviderEncodings
  - Exemple de valeur:
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultSearchProviderImageURL
  #### Définit la fonctionnalité de recherche par image pour le moteur de recherche par défaut
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indique l’URL du moteur de recherche utilisé pour la recherche d’images. Les requêtes de recherche sont envoyées à l’aide la méthode GET.

Cette stratégie est facultative. Si elle n’est pas configurée, la recherche d’images n’est pas disponible.

Définissez l’URL de recherche d’images Bing comme suit: '{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights'.

Définissez l’URL de recherche d’images Google comme suit: '{google:baseURL}searchbyimage/upload'.

Pour finaliser la configuration de la recherche d’images, consultez la stratégie [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams).

Cette stratégie est appliquée uniquement si vous activez les stratégies [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

À partir de Microsoft Edge 84, vous pouvez utiliser cette stratégie comme stratégie recommandée. Si l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée ne sera pas ajouté à la liste des fournisseurs de recherche parmi lesquels l’utilisateur peut faire son choix. S’il s’agit du comportement souhaité, utilisez la stratégie [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultSearchProviderImageURL
  - Nom de la stratégie de groupe: définit la fonctionnalité de recherche par image pour le moteur de recherche par défaut
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Default search provider
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Fournisseur de recherche par défaut
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: DefaultSearchProviderImageURL
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"https://search.contoso.com/searchbyimage/upload"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultSearchProviderImageURL
  - Exemple de valeur:
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultSearchProviderImageURLPostParams
  #### Paramètres pour une URL d’image utilisant la méthode POST
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Lorsqu’elle est activée, cette stratégie définit les paramètres utilisés lors de l’exécution d’une recherche d’images utilisant la méthode POST. La stratégie est constituée de paires de noms et de valeurs, séparées par des virgules. Si une valeur est un paramètre de modèle, comme par exemple {imageThumbnail}, elle est remplacée par des miniatures d’images réelles. Cette stratégie est appliquée uniquement si vous activez les stratégies [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Définissez l’URL de recherche d’images Bing post param comme suit: 'imageBin={google:imageThumbnailBase64}'.

Définissez l’URL de recherche d’images Bing post param comme suit: 'encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}'.

Si cette stratégie n’est pas configurée, les demandes de recherche d’images sont envoyées à l’aide de la méthode GET.

À partir de Microsoft Edge 84, vous pouvez utiliser cette stratégie comme stratégie recommandée. Si l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée ne sera pas ajouté à la liste des fournisseurs de recherche parmi lesquels l’utilisateur peut faire son choix. S’il s’agit du comportement souhaité, utilisez la stratégie [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultSearchProviderImageURLPostParams
  - Nom de la stratégie de groupe: paramètres pour une URL d’image utilisant la méthode POST
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Default search provider
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Fournisseur de recherche par défaut
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: DefaultSearchProviderImageURLPostParams
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultSearchProviderImageURLPostParams
  - Exemple de valeur:
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultSearchProviderKeyword
  #### Mot clé du moteur de recherche par défaut
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indique le mot clé, qui est le raccourci utilisé dans la barre d’adresses, pour déclencher la recherche de ce moteur de recherche.

Cette stratégie est facultative. Si elle n’est pas configurée, aucun mot clé n’active le moteur de recherche.

Cette stratégie est appliquée uniquement si vous activez les stratégies [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

À partir de Microsoft Edge 84, vous pouvez utiliser cette stratégie comme stratégie recommandée. Si l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée ne sera pas ajouté à la liste des fournisseurs de recherche parmi lesquels l’utilisateur peut faire son choix. S’il s’agit du comportement souhaité, utilisez la stratégie [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultSearchProviderKeyword
  - Nom de la stratégie de groupe: mot clé du moteur de recherche par défaut
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Default search provider
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Fournisseur de recherche par défaut
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: DefaultSearchProviderKeyword
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"mis"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultSearchProviderKeyword
  - Exemple de valeur:
``` xml
<string>mis</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultSearchProviderName
  #### Nom du moteur de recherche par défaut
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifie le nom du moteur de recherche par défaut.

Si vous activez cette stratégie, vous devez spécifier le nom du moteur de recherche par défaut.

Si vous n’activez pas cette stratégie ou si vous la laissez vide, le nom d’hôte, spécifié par l’URL de recherche, est utilisé.

«DefaultSearchProviderName» doit être défini sur un moteur de recherche chiffré, approuvé par l’organisation, qui correspond au moteur de recherche chiffré défini dans DTBC-0008. Cette stratégie est appliquée uniquement si vous activez les stratégies [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

À partir de Microsoft Edge 84, vous pouvez utiliser cette stratégie comme stratégie recommandée. Si l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée ne sera pas ajouté à la liste des fournisseurs de recherche parmi lesquels l’utilisateur peut faire son choix. S’il s’agit du comportement souhaité, utilisez la stratégie [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultSearchProviderName
  - Nom de la stratégie de groupe: nom du moteur de recherche par défaut
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Default search provider
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Fournisseur de recherche par défaut
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: DefaultSearchProviderName
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"My Intranet Search"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultSearchProviderName
  - Exemple de valeur:
``` xml
<string>My Intranet Search</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultSearchProviderSearchURL
  #### URL de recherche du moteur de recherche par défaut
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indique l’URL du moteur de recherche utilisé pour la recherche par défaut. L’URL contient la chaîne «{searchTerms}», qui est remplacée, au moment de la requête, par les termes recherchés par l’utilisateur.

Définissez l’URL de recherche Bing comme suit:

'{bing:baseURL}search?q={searchTerms}'.

Définissez l’URL de recherche Google comme suit: '{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}'.

Cette stratégie est requise lorsque vous activez la stratégie [DefaultSearchProviderEnabled](#defaultsearchproviderenabled). Si vous n’activez pas cette dernière, la stratégie est ignorée.

À partir de Microsoft Edge 84, vous pouvez utiliser cette stratégie comme stratégie recommandée. Si l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée ne sera pas ajouté à la liste des fournisseurs de recherche parmi lesquels l’utilisateur peut faire son choix. S’il s’agit du comportement souhaité, utilisez la stratégie [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultSearchProviderSearchURL
  - Nom de la stratégie de groupe: URL de recherche du moteur de recherche par défaut
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Default search provider
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Fournisseur de recherche par défaut
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: DefaultSearchProviderSearchURL
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"https://search.contoso.com/search?q={searchTerms}"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultSearchProviderSearchURL
  - Exemple de valeur:
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultSearchProviderSuggestURL
  #### URL de suggestions de recherche du moteur de recherche par défaut
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indique l’URL du moteur de recherche utilisé pour fournir des suggestions de recherche. L’URL contient la chaîne «{searchTerms}», qui est remplacée, au moment de la requête, par les termes déjà saisis par l’utilisateur.

Cette stratégie est facultative. Si elle n’est pas configurée, les utilisateurs ne voient pas les suggestions de recherche mais les suggestions provenant de l’historique de navigation et des favoris apparaissent.

L’URL de suggestion de Bing peut être définie comme suit:

'{bing:baseURL}qbox?query={searchTerms}'.

L’URL de suggestion de Google peut être définie comme suit: '{google:baseURL}complete/search?output=chrome&q={searchTerms}'.

Cette stratégie est appliquée uniquement si vous activez les stratégies [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

À partir de Microsoft Edge 84, vous pouvez utiliser cette stratégie comme stratégie recommandée. Si l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée ne sera pas ajouté à la liste des fournisseurs de recherche parmi lesquels l’utilisateur peut faire son choix. S’il s’agit du comportement souhaité, utilisez la stratégie [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultSearchProviderSuggestURL
  - Nom de la stratégie de groupe: URL de suggestions de recherche du moteur de recherche par défaut
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Default search provider
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Fournisseur de recherche par défaut
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: DefaultSearchProviderSuggestURL
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"https://search.contoso.com/suggest?q={searchTerms}"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultSearchProviderSuggestURL
  - Exemple de valeur:
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NewTabPageSearchBox
  #### Configurer l’expérience de zone de recherche dans la nouvelle page d’onglets
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version85 ou versions ultérieures

  #### Description
  Vous pouvez configurer la zone de recherche de la nouvelle page d’onglet pour utiliser «zone de recherche (recommandé)» ou «barre d’adresses» pour effectuer une recherche dans les nouveaux onglets. Cette stratégie fonctionne uniquement si vous définissez le moteur de recherche sur une valeur autre que Bing en définissant les deux stratégies suivantes: [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

 Si vous désactivez ou ne configurez pas cette stratégieet:

- Si le moteur de recherche par défaut de la barre d’adresse est Bing, la page nouvel onglet utilise la zone de recherche pour effectuer une recherche dans les nouveaux onglets.
- Si le moteur de recherche par défaut de la barre d’adresse n’est pas Bing, les utilisateurs sont invités à choisir une option supplémentaire (utilisez la «barre d’adresse») lors de la recherche sur de nouveaux onglets.


Si vous activez cette stratégie et configurez-la comme suit:

- «Zone de recherche (recommandé)» («Bing»), la page nouvel onglet utilise la zone de recherche pour effectuer une recherche dans les nouveaux onglets.
- «Barre d’adresses» («rediriger»), la zone de recherche de la nouvelle page de l’onglet utilise la barre d’adresses pour effectuer une recherche dans les nouveaux onglets.

Mappage des options de stratégie:

* bing (bing) = Zone de recherche (Recommandé)

* redirect (redirect) = Barre d’adresse

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: NewTabPageSearchBox
  - Nom de la stratégie de recherche: configurer l’expérience de zone de recherche nouvelle page
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Default search provider
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Fournisseur de recherche par défaut
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: NewTabPageSearchBox
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"bing"
```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: NewTabPageSearchBox
  - Exemple de valeur:
``` xml
<string>bing</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ## Stratégies des extensions

  [Retour au début](#microsoft-edge---policies)

  ### ExtensionAllowedTypes
  #### Configurer les types d’extension autorisés
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Détermine les types d’extensions pouvant être installés et limite l’accès pendant l’exécution.

Ce paramètre définit les types d’extensions autorisés et les hôtes avec lesquels ils peuvent interagir. La valeur est une liste composée de chaînes, chacune pouvant prendre l’une des suivantes: «extension», «theme», «user_script» et «hosted_app». Si vous souhaitez en savoir plus sur ces types, consultez la documentation sur les extensions MicrosoftEdge.

Cette stratégie affecte également les extensions dont l’installation est forcée à l’aide de la stratégie [ExtensionInstallForcelist](#extensioninstallforcelist).

Si vous activez cette stratégie, seules les extensions qui correspondent à un type répertorié dans la liste sont installées.

Si cette stratégie n’est pas configurée, aucune restriction n’est imposée concernant les types d’extensions pouvant être installés.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ExtensionAllowedTypes
  - Nom de la stratégie de groupe: configurer les types d’extension autorisés
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Extensions
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ExtensionAllowedTypes
  - Exemple de valeur:
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ExtensionInstallAllowlist
  #### Autoriser l’installation d’extensions spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Par défaut, toutes les extensions sont autorisées. Toutefois, si vous bloquez toutes les extensions en définissant la stratégie «ExtensionInstallBlockList» sur «*», les utilisateurs peuvent uniquement installer les extensions définies dans cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ExtensionInstallAllowlist
  - Nom de la stratégie de groupe: autoriser l’installation d’extensions spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Extensions
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ExtensionInstallAllowlist
  - Exemple de valeur:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ExtensionInstallBlocklist
  #### Déterminer les extensions ne pouvant pas être installées
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Répertoriez des extensions spécifiques que les utilisateurs ne peuvent PAS installer dans MicrosoftEdge. Lorsque vous déployez cette stratégie, toutes les extensions de cette liste, qui ont été installées précédemment, sont désactivées et l’utilisateur ne peut pas les activer. Si vous supprimez un élément de la liste des extensions bloquées, cette extension est automatiquement réactivée partout où elle a déjà été installée.

Utilisez «*» pour bloquer toutes les extensions qui ne sont pas répertoriées de façon explicite dans la liste verte. 

Si cette stratégie n’est pas configurée, les utilisateurs peuvent installer n’importe quelle extension dans MicrosoftEdge.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ExtensionInstallBlocklist
  - Nom de la stratégie de groupe: déterminer les extensions ne pouvant pas être installées
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Extensions
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ExtensionInstallBlocklist
  - Exemple de valeur:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ExtensionInstallForcelist
  #### Contrôler l’installation silencieuse de certaines extensions
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Définit la liste des applications et des extensions qui sont installées en arrière-plan, sans aucune intervention de l’utilisateur, et qui ne peuvent pas être désinstallées ou désactivées («installation forcée»). Toutes les autorisations demandées par les extensions sont accordées de manière implicite, sans intervention de l’utilisateur, y compris tout autre autorisation demandée par les futures versions de l’extension. En outre, les autorisations sont accordées pour les API d’extension enterprise.deviceAttributes et enterprise.platformKeys. (ces deux API sont disponibles uniquement pour les extensions dont l’installation est forcée).

Cette stratégie prévaut lors d’un conflit potentiel avec la stratégie [ExtensionInstallBlocklist](#extensioninstallblocklist). Lorsque vous retirez une extension de la liste des extensions dont l’installation est forcée, elle est automatiquement désinstallée par Microsoft Edge.

L’installation forcée est limitée aux applications et extensions répertoriées sur le site web des modules complémentaires de MicrosoftEdge pour les instances qui ne figurent pas parmi les instances suivantes: les instances Windows associées à un domaine Microsoft ActiveDirectory ou les instances Windows10Professionnel ou Entreprise, inscrites pour la gestion des périphériques et les instances macOS gérées via MDM ou jointes à un domaine via MCX.

Les utilisateurs peuvent modifier le code source de n’importe quelle extension à l’aide des outils de développement, ce qui peut potentiellement faire dysfonctionner l’extension. Si cela pose problème, configurez la stratégie [DeveloperToolsAvailability](#developertoolsavailability).

Utilisez le format suivant pour ajouter une extension à la liste:

[extensionID];[updateURL]

- extensionID: la chaîne de 32lettres qui se trouve sur edge://extensions lorsque vous êtes en mode développeur.

- updateURL (facultatif) est l’adresse du document XML du manifeste de mise à jour pour l’application ou l’extension, comme décrit dans [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043). Si vous voulez installer une extension à partir du magasin Web chrome, fournissez l’URL de mise à jour du magasin Web chrome, https://clients2.google.com/service/update2/crx. L’URL de mise à jour spécifiée dans cette stratégie n’est utilisée que pour l’installation initiale. Toute mise à jour ultérieure de l’extension est effectuée avec l’URL indiquée dans le fichier manifeste de l’extension. Si vous ne configurez pas la miseàjourURL, l’extension est supposée être hébergée dans le Microsoft Store et l’URL de mise à jour suivante est utilisée (https://edge.microsoft.com/extensionwebstorebase/v1/crx).

Par exemple, gggmmkjegpiggikcnhidnjjhmicpibll;https://edge.microsoft.com/extensionwebstorebase/v1/crx installe l’application Microsoft Online à partir de l’URL «mettre à jour» du Microsoft Store. Si vous souhaitez en savoir plus sur l’hébergement des extensions, consultez la page [https://go.microsoft.com/fwlink/?linkid=2095044](https://go.microsoft.com/fwlink/?linkid=2095044).

Si cette stratégie n’est pas configurée, les extensions ne sont pas installées automatiquement et les utilisateurs peuvent désinstaller toutes les extensions dans MicrosoftEdge.

Cette stratégie ne s’applique pas au mode InPrivate.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ExtensionInstallForcelist
  - Nom de la stratégie de groupe: contrôler l’installation silencieuse de certaines extensions
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Extensions
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ExtensionInstallForcelist
  - Exemple de valeur:
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ExtensionInstallSources
  #### Configurer les sources d’installation des extensions et des scripts d’utilisateur
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Définissez les URL qui peuvent installer des extensions et des thèmes.

Par défaut, les utilisateurs doivent télécharger un fichier *.crx pour chaque extension ou script qu’ils souhaitent installer, puis doivent le faire glisser sur la page des paramètres de MicrosoftEdge. Cette stratégie permet aux URL spécifiques d’utiliser l’option installer l’extension ou le script pour l’utilisateur.

Chaque élément de cette liste est un modèle correspondant au type extension (consultez [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039)). Les utilisateurs peuvent facilement installer des éléments à partir de n’importe quelle URL qui correspond à un élément de cette liste. L’emplacement du fichier *.crx et de la page à partir de laquelle le téléchargement est effectué (en d’autres termes, le référent) doit être autorisé par ces modèles.

La stratégie [ExtensionInstallBlocklist](#extensioninstallblocklist) prévaut sur cette stratégie. Les extensions figurant dans la liste rouge ne sont pas installées, même si elles proviennent d’un site figurant sur cette liste.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ExtensionInstallSources
  - Nom de la stratégie de groupe: configurer les sources d’installation des extensions et des scripts d’utilisateur
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Extensions
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ExtensionInstallSources
  - Exemple de valeur:
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ExtensionSettings
  #### Configurer les paramètres de gestion des extensions
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Configure les paramètres de gestion d’extension pour MicrosoftEdge.

Cette stratégie contrôle plusieurs paramètres, y compris ceux contrôlés par des stratégies associées à une extension. Cette stratégie remplace les stratégies héritées si elles sont toutes les deux définies.

Cette stratégie associe un ID d’extension ou une URL de mise à jour à sa configuration. Avec un ID d’extension, la configuration est appliquée uniquement à l’extension spécifiée. Définissez la configuration par défaut de l’ID spécial «*» pour qu’il s’applique à toutes les extensions qui ne sont pas spécifiquement répertoriées dans cette stratégie. Avec une URL de mise à jour, la configuration est appliquée à l’ensemble des extensions avec l’URL de mise à jour telle qu’elle est indiquée dans le fichier manifeste de cette extension, comme indiqué sur [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Dictionary

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ExtensionSettings
  - Nom de la stratégie de groupe: configurer les paramètres de gestion des extensions
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Extensions
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ExtensionSettings
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings = {
  "*": {
    "allowed_types": [
      "hosted_app"
    ], 
    "blocked_install_message": "Custom error message.", 
    "blocked_permissions": [
      "downloads", 
      "bookmarks"
    ], 
    "install_sources": [
      "https://company-intranet/apps"
    ], 
    "installation_mode": "blocked", 
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ], 
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ]
  }, 
  "abcdefghijklmnopabcdefghijklmnop": {
    "blocked_permissions": [
      "history"
    ], 
    "installation_mode": "allowed", 
    "minimum_version_required": "1.0.1"
  }, 
  "bcdefghijklmnopabcdefghijklmnopa": {
    "allowed_permissions": [
      "downloads"
    ], 
    "installation_mode": "force_installed", 
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ], 
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ], 
    "update_url": "https://contoso.com/update_url"
  }, 
  "cdefghijklmnopabcdefghijklmnopab": {
    "blocked_install_message": "Custom error message.", 
    "installation_mode": "blocked"
  }, 
  "defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd": {
    "blocked_install_message": "Custom error message.", 
    "installation_mode": "blocked"
  }, 
  "fghijklmnopabcdefghijklmnopabcde": {
    "blocked_install_message": "Custom removal message.", 
    "installation_mode": "removed"
  }, 
  "update_url:https://www.contoso.com/update.xml": {
    "allowed_permissions": [
      "downloads"
    ], 
    "blocked_permissions": [
      "wallpaper"
    ], 
    "installation_mode": "allowed"
  }
}
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ExtensionSettings
  - Exemple de valeur:
``` xml
<key>ExtensionSettings</key>
<dict>
  <key>*</key>
  <dict>
    <key>allowed_types</key>
    <array>
      <string>hosted_app</string>
    </array>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>blocked_permissions</key>
    <array>
      <string>downloads</string>
      <string>bookmarks</string>
    </array>
    <key>install_sources</key>
    <array>
      <string>https://company-intranet/apps</string>
    </array>
    <key>installation_mode</key>
    <string>blocked</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
  </dict>
  <key>abcdefghijklmnopabcdefghijklmnop</key>
  <dict>
    <key>blocked_permissions</key>
    <array>
      <string>history</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
    <key>minimum_version_required</key>
    <string>1.0.1</string>
  </dict>
  <key>bcdefghijklmnopabcdefghijklmnopa</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>installation_mode</key>
    <string>force_installed</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
    <key>update_url</key>
    <string>https://contoso.com/update_url</string>
  </dict>
  <key>cdefghijklmnopabcdefghijklmnopab</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>fghijklmnopabcdefghijklmnopabcde</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom removal message.</string>
    <key>installation_mode</key>
    <string>removed</string>
  </dict>
  <key>update_url:https://www.contoso.com/update.xml</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>blocked_permissions</key>
    <array>
      <string>wallpaper</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
  </dict>
</dict>
```
  

  [Retour au début](#microsoft-edge---policies)

  ## Stratégies d’authentificationHTTP

  [Retour au début](#microsoft-edge---policies)

  ### AllowCrossOriginAuthPrompt
  #### Autoriser les invites d’authentification HTTP à origines multiples
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Détermine si les images tierces d’une page peuvent afficher une invite d’authentification.

Cette option est habituellement désactivée dans le cadre de la protection contre l’hameçonnage. Si vous ne configurez pas cette stratégie, elle est désactivée et les images tierces ne peuvent pas afficher d’invite d’authentification.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AllowCrossOriginAuthPrompt
  - Nom de la stratégie de groupe: autorise les invites d’authentification HTTP à origines multiples
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/HTTP authentication
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AllowCrossOriginAuthPrompt
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AllowCrossOriginAuthPrompt
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AuthNegotiateDelegateAllowlist
  #### Définit une liste des serveurs auxquels MicrosoftEdge peut déléguer les informations d’identification de l’utilisateur
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Définit une liste des serveurs auxquels MicrosoftEdge peut déléguer.

Séparez les noms des serveurs par des virgules. Les caractères génériques (*) sont autorisés.

Si cette stratégie n’est pas configurée, MicrosoftEdge ne délègue pas les informations d’identification d’utilisateur, même si un serveur est détecté comme intranet.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AuthNegotiateDelegateAllowlist
  - Nom de la stratégie de groupe: définit une liste des serveurs auxquels MicrosoftEdge peut déléguer les informations d’identification de l’utilisateur
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/HTTP authentication
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AuthNegotiateDelegateAllowlist
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"contoso.com"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AuthNegotiateDelegateAllowlist
  - Exemple de valeur:
``` xml
<string>contoso.com</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AuthSchemes
  #### Méthodes d’authentification prises en charge
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indique les schémas d’authentification HTTP qui sont pris en charge.

Vous pouvez configurer la stratégie à l’aide des valeurs suivantes: «basic», «digest», «ntlm» et «negotiate». Séparez les valeurs par des virgules.

Si cette stratégie n’est pas configurée, les quatre schémas sont utilisés.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AuthSchemes
  - Nom de la stratégie de groupe: méthodes d’authentification prises en charge
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/HTTP authentication
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AuthSchemes
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"basic,digest,ntlm,negotiate"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AuthSchemes
  - Exemple de valeur:
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AuthServerAllowlist
  #### Configurer la liste des serveurs d’authentification autorisés
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifie les serveurs à activer pour l’authentification intégrée. L’authentification intégrée n’est activée que lorsque MicrosoftEdge reçoit une demande d’authentification à partir d’un proxy ou d’un serveur de cette liste.

Séparez les noms des serveurs par des virgules. Les caractères génériques (*) sont autorisés.

Si vous ne configurez pas cette stratégie, MicrosoftEdge essaie de détecter si un serveur se trouve sur l’intranet. Ce n’est qu’à ce moment-là qu’il répond aux requêtes IWA. Si le serveur se trouve sur Internet, les requêtes IWA émanant de celui-ci sont ignorées par MicrosoftEdge.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AuthServerAllowlist
  - Nom de la stratégie de groupe: configurer la liste des serveurs d’authentification autorisés
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/HTTP authentication
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AuthServerAllowlist
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"*contoso.com,contoso.com"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AuthServerAllowlist
  - Exemple de valeur:
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DisableAuthNegotiateCnameLookup
  #### Désactiver la consultation CNAME lors de la négociation de l’authentification Kerberos
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indique si le SPN Kerberos généré est basé sur le nom DNS canonique (CNAME) ou sur le nom d’origine saisi.

Si vous activez cette stratégie, la consultation CNAME sera ignorée et le nom du serveur sera utilisé tel qu’il a été saisi.

Si vous désactivez cette stratégie ou si elle n’est pas définie, le nom canonique du serveur est utilisé.  Celui-ci est déterminé par la consultation CNAME.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DisableAuthNegotiateCnameLookup
  - Nom de la stratégie de groupe: désactiver la consultation CNAME lors de la négociation de l’authentification Kerberos
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/HTTP authentication
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DisableAuthNegotiateCnameLookup
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DisableAuthNegotiateCnameLookup
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### EnableAuthNegotiatePort
  #### Inclure un port non standard dans le SPN Kerberos
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indique si le SPN Kerberos généré doit inclure un port non standard.

Si vous activez cette stratégie et qu’un utilisateur inclut un port non standard (c’est-à-dire, un port autre que 80 ou 443) dans une URL, ce port est inclus dans le SPN Kerberos généré.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, le SPN Kerberos généré ne comprend aucun port.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: EnableAuthNegotiatePort
  - Nom de la stratégie de groupe: inclure un port non standard dans le SPN Kerberos
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/HTTP authentication
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: EnableAuthNegotiatePort
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: EnableAuthNegotiatePort
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NtlmV2Enabled
  #### Contrôler l’activation de l’authentification NTLMv2
  
  
  #### Versions prises en charge:
  - sur macOS depuis la version77 ou versions ultérieures

  #### Description
  Contrôle si l’authentification NTLMv2 est activée.

Toutes les versions récentes des serveurs Samba et Windows prennent en charge l’authentification NTLMv2. Vous devez désactiver l’authentification NTLMv2 uniquement pour résoudre les problèmes de rétrocompatibilité, car cela réduit la sécurité de l’authentification.

Si cette stratégie n’est pas configurée, l’authentification NTLMv2 est activé par défaut.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  

  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: NtlmV2Enabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ## Stratégies des paramètres du mode kiosque

  [Retour au début](#microsoft-edge---policies)

  ### KioskDeleteDownloadsOnExit
  #### Supprimer les fichiers téléchargés dans le cadre d’une session kiosque lorsque MicrosoftEdge se ferme
  
  
  #### Versions prises en charge:
  - Sur Windows depuis la version87 ou versions ultérieures

  #### Description
  Remarque: cette stratégie est prise en charge uniquement lorsque MicrosoftEdge est lancée avec le paramètre command-line «--edge-kiosk-type».

Si vous activez cette stratégie, les fichiers téléchargés dans le cadre d’une session kiosque sont supprimés lors de chaque fermeture de MicrosoftEdge.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, les fichiers téléchargés dans le cadre d’une session kiosque ne sont pas supprimés lors de la fermeture de MicrosoftEdge.

Pour obtenir plus d’informations sur la configuration du mode kiosque, voir [https://go.microsoft.com/fwlink/?linkid=2137578](https://go.microsoft.com/fwlink/?linkid=2137578).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: KioskDeleteDownloadsOnExit
  - Nom de la stratégie de groupe: supprimer les fichiers téléchargés dans le cadre d’une session kiosque lorsque MicrosoftEdge se ferme
  - Chemin d’accès de la stratégie de groupe(obligatoire): paramètres Administrative Templates/Microsoft Edge/Kiosk Mode
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: KioskDeleteDownloadsOnExit
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)

  ## Stratégies de messagerie native

  [Retour au début](#microsoft-edge---policies)

  ### NativeMessagingAllowlist
  #### Contrôler les hôtes de messagerie native que les utilisateurs peuvent utiliser
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Répertoriez les hôtes de messagerie native spécifiques que les utilisateurs peuvent utiliser dans MicrosoftEdge.

Par défaut, tous les hôtes de messagerie native sont autorisés. Si la stratégie [NativeMessagingBlocklist](#nativemessagingblocklist) est définie sur *, tous les hôtes de messagerie native sont bloqués, et seuls les hôtes de messagerie native, répertoriés ici, sont chargés.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: NativeMessagingAllowlist
  - Nom de la stratégie de groupe: contrôler les hôtes de messagerie native que les utilisateurs peuvent utiliser
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Native Messaging
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: NativeMessagingAllowlist
  - Exemple de valeur:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NativeMessagingBlocklist
  #### Configurer la liste rouge de la messagerie native
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifie les hôtes de messagerie native qui ne doivent pas être utilisés.

Utilisez «*» pour bloquer tous les hôtes de messagerie native, sauf s’ils sont explicitement répertoriés dans la liste verte.

Si cette stratégie n’est pas configurée, MicrosoftEdge charge tous les hôtes de messagerie native installés.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: NativeMessagingBlocklist
  - Nom de la stratégie de groupe: configurer la liste rouge de la messagerie native
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Native Messaging
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: NativeMessagingBlocklist
  - Exemple de valeur:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NativeMessagingUserLevelHosts
  #### Autoriser les hôtes de messagerie native côté utilisateur (installés sans autorisation d’administrateur)
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet d’installer des hôtes de messagerie native côté utilisateur.

Si vous désactivez cette stratégie, MicrosoftEdge utilise uniquement les hôtes de messagerie native installés côté système.

Par défaut, si cette stratégie n’est pas configurée, MicrosoftEdge autorise l’utilisation d’hôtes de messagerie native installés côté utilisateur.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: NativeMessagingUserLevelHosts
  - Nom de la stratégie de groupe: autoriser les hôtes de messagerie native côté utilisateur (installés sans autorisation d’administrateur)
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Native Messaging
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: NativeMessagingUserLevelHosts
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: NativeMessagingUserLevelHosts
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ## Stratégies du gestionnaire et de la protection des mots de passe

  [Retour au début](#microsoft-edge---policies)

  ### PasswordManagerEnabled
  #### Activer l’enregistrement des mots de passe dans le gestionnaire de mots de passe
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Autoriser MicrosoftEdge à enregistrer les mots de passe des utilisateurs.

Si cette stratégie est activée, les utilisateurs peuvent enregistrer leurs mots de passe dans MicrosoftEdge. Lors de leur prochaine visite sur le site, MicrosoftEdge entrera automatiquement le mot de passe.

Si cette stratégie est désactivée, les utilisateurs ne peuvent pas enregistrer de nouveaux mots de passe, mais ils peuvent toujours utiliser les mots de passe préalablement enregistrés. 

Si cette règle est activée ou désactivée, les utilisateurs ne peuvent ni la modifier, ni la remplacer dans MicrosoftEdge. Si cette stratégie n’est pas configurée, les utilisateurs peuvent enregistrer des mots de passe, mais aussi désactiver cette fonctionnalité.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PasswordManagerEnabled
  - Nom de la stratégie de groupe: activer l’enregistrement des mots de passe dans le gestionnaire de mots de passe
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Password manager and protection
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Password manager and protection
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: PasswordManagerEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PasswordManagerEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PasswordMonitorAllowed
  #### Autoriser les utilisateurs à être avertis si leur mot de passe est considéré comme dangereux
  
  
  #### Versions prises en charge:
  - Sur Windows depuis la version85 ou versions ultérieures

  #### Description
  Autoriser Microsoft Edge à contrôler les mots de passe des utilisateurs.

Si vous activez cette stratégie et qu’un utilisateur a l’autorisation d’activer la stratégie, l’utilisateur reçoit une alerte si l’un de ses mots de passe stockés dans Microsoft Edge est considéré comme non sécurisé. Microsoft Edge affiche une alerte. ces informations sont également disponibles dans Paramètres > mots de passe > le moniteur des mots de passe.

Si vous désactivez cette stratégie, les utilisateurs ne sont pas invités à entrer l’autorisation d’activer cette fonctionnalité. Les mots de passe ne seront pas analysés et ne seront pas non plus signalés.

Si vous activez ou ne configurez pas la stratégie, les utilisateurs peuvent activer ou désactiver cette fonctionnalité.

Pour en savoir plus sur la manière dont Microsoft Edge trouve les mots de passe dangereux, voir [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

Autres recommandations:

Cette stratégie peut être activée à la fois comme recommandée et obligatoire, mais avec une légende importante.

Obligatoire activé: étant donné que le consentement d’un utilisateur individuel est une condition préalable à l’activation de cette fonctionnalité pour un utilisateur donné, cette stratégie ne possède pas de paramètre activé obligatoire. Si la stratégie est configurée sur obligatoire, l’interface utilisateur dans les paramètres ne change pas et le message d’erreur suivant s’affiche dans edge://policy

Exemple de message d’état d’erreur: «cette valeur de stratégie est ignorée, car le moniteur de mot de passe nécessite le consentement de l’utilisateur individuel pour qu’il soit activé. Vous pouvez demander aux utilisateurs au sein de votre organisation d’accéder aux paramètres > Profil > mot de passe et d’activer la fonctionnalité.»

Option recommandée: si la stratégie est définie sur recommandé activée, l’interface utilisateur dans les paramètres reste en mode «désactivé», mais une icône de porte-documents est affichée en regard de celle-ci en regard de celle-ci affichée sur Hover-«votre organisation recommande une valeur spécifique et vous avez choisi une autre valeur»

Obligatoire et recommandé Désactivé: ces deux États fonctionnent de façon normale, avec les légendes habituelles qui apparaissent aux utilisateurs.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: PasswordMonitorAllowed
  - Nom de la stratégie de sécurité: autoriser les utilisateurs à être avertis si leur mot de passe est considéré comme dangereux
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Password manager and protection
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Password manager and protection
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: PasswordMonitorAllowed
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)

  ### PasswordProtectionChangePasswordURL
  #### Configurer l’URL de modification du mot de passe
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Configure l’URL de modification du mot de passe (schémas HTTP et HTTPS uniquement).

Le service de protection par mot de passe redirige les utilisateurs vers cette URL pour modifier leur mot de passe après l’affichage d’un avertissement dans le navigateur.

Si vous activez cette stratégie, le service de protection par mot de passe redirige les utilisateurs vers cette URL pour modifier leur mot de passe. 

Si vous désactivez cette stratégie ou si vous ne la configurez pas, le service de protection par mot de passe ne redirige pas les utilisateurs vers une URL de modification du mot de passe.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PasswordProtectionChangePasswordURL
  - Nom de la stratégie de groupe: configurer l’URL de modification du mot de passe
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Password manager and protection
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: PasswordProtectionChangePasswordURL
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"https://contoso.com/change_password.html"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PasswordProtectionChangePasswordURL
  - Exemple de valeur:
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PasswordProtectionLoginURLs
  #### Configurer la liste des URL de connexion d’entreprise dans lesquelles le service de protection par mot de passe doit capturer les codes de hachage d’un mot de passe
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Configurez la liste des URL de connexion d’entreprise (schémas HTTP et HTTPS uniquement) où MicrosoftEdge doit capturer les code de hachage salés des mots de passe et l’utiliser pour la détection de la réutilisation des mots de passe.

Si vous activez cette stratégie, le service de protection par mot de passe capture les empreintes des mots de passe sur les URL définies.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, aucune empreinte de mot de passe n’est capturée.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PasswordProtectionLoginURLs
  - Non de la stratégie de groupe : configurer la liste des URL de connexion d’entreprise dans lesquelles le service de protection par mot de passe doit capturer les codes de hachage d’un mot de passe
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Password manager and protection
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PasswordProtectionLoginURLs
  - Exemple de valeur:
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PasswordProtectionWarningTrigger
  #### Configurer le déclencheur d’avertissement de protection par mot de passe
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Vous permet de contrôler quand déclencher l’avertissement de protection de mot de passe. La protection de mot de passe avertit les utilisateurs lorsqu’ils réutilisent leur mot de passe protégé sur des sites potentiellement suspects.

Vous pouvez utiliser les stratégies [PasswordProtectionLoginURLs](#passwordprotectionloginurls) et [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) pour configurer les mots de passe à protéger.

Exemptions: les mots de passe des sites répertoriés dans [PasswordProtectionLoginURLs](#passwordprotectionloginurls) et [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl), ainsi que ceux répertoriés dans [SmartScreenAllowListDomains](#smartscreenallowlistdomains), ne déclencheront pas d’avertissement de protection de mot de passe.

Définissez la stratégie sur «PasswordProtectionWarningOff» pour ne pas afficher les avertissements de protection de mot de passe.

Définissez la stratégie sur «PasswordProtectionWarningOnPasswordReuse» pour afficher les avertissements de protection de mot de passe lorsque l’utilisateur réutilise son mot de passe protégé sur un site ne se trouvant pas dans la liste de sites autorisés. 

Si vous désactivez ou ne configurez pas cette stratégie, le déclencheur d’avertissement ne s’affiche pas.

Mappage des options de stratégie:

* PasswordProtectionWarningOff (0) = L’avertissement de protection de mot de passe est désactivée

* PasswordProtectionWarningOnPasswordReuse (1) = L’avertissement de protection de mot de passe est déclenché par la réutilisation d’un mot de passe

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PasswordProtectionWarningTrigger
  - Nom de la stratégie de groupe: configurer le déclencheur d’avertissement de protection par mot de passe
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Password manager and protection
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: PasswordProtectionWarningTrigger
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PasswordProtectionWarningTrigger
  - Exemple de valeur:
``` xml
<integer>1</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ## Stratégies d’impression

  [Retour au début](#microsoft-edge---policies)

  ### DefaultPrinterSelection
  #### Instructions de sélection de l’imprimante par défaut
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Remplace les instructions de sélection de l’imprimante par défaut pour MicrosoftEdge. Cette stratégie détermine les instructions de sélection de l’imprimante par défaut dans MicrosoftEdge, la première fois qu’un utilisateur tente d’imprimer une page.

Lorsque cette stratégie est définie, Microsoft Edge tente de trouver une imprimante qui correspond à tous les attributs spécifiés et l’utilise comme imprimante par défaut. Si plusieurs imprimantes remplissent les critères, la première imprimante correspondante est utilisée. 

Si vous ne configurez pas cette stratégie ou si aucune imprimante correspondante n’est détectée dans le délai imparti, l’imprimante est définie par défaut sur l’imprimante PDF intégrée. Si l’imprimante PDF n’est pas disponible, aucune imprimante n’est sélectionnée.

La valeur est analysée en tant qu’objet JSON, conformément au schéma suivant: { "type": "object", "properties": { "idPattern": { "description": "Regular expression to match printer id.", "type": "string" }, "namePattern": { "description": "Regular expression to match printer display name.", "type": "string" } } }

L’omission d’un champ signifie que toutes les valeurs correspondent. Par exemple, si vous ne spécifiez pas la connectivité, l’Aperçu avant impression démarre la découverte de tous les types d’imprimantes locales. Les modèles d’expressions régulières doivent respecter la syntaxe JavaScript RegExp et les correspondances sont sensibles à la casse.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultPrinterSelection
  - Nom de la stratégie de groupe: instructions de sélection de l’imprimante par défaut
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Printing
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultPrinterSelection
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultPrinterSelection
  - Exemple de valeur:
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PrintHeaderFooter
  #### Imprimer des en-têtes et des pieds de page
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Forcer l’activation et la désactivation des en-têtes et des pieds de page dans la boîte de dialogue d’impression.

Si cette stratégie n’est pas configurée, les utilisateurs peuvent choisir d’imprimer les en-têtes et les pieds de page.

Si cette stratégie est désactivée, les utilisateurs ne peuvent pas imprimer les en-têtes et les pieds de page.

Si vous activez cette stratégie, les utilisateurs impriment toujours les en-têtes et les pieds de page.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PrintHeaderFooter
  - Nom de la stratégie de groupe: imprimer des en-têtes et des pieds de page
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Printing
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Printing
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: PrintHeaderFooter
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PrintHeaderFooter
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PrintPreviewUseSystemDefaultPrinter
  #### Définir l’imprimante par défaut du système comme imprimante par défaut
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indique à MicrosoftEdge d’utiliser l’imprimante par défaut du système comme choix par défaut dans l’aperçu avant impression au lieu de l’imprimante qui a été utilisée le plus récemment.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, l’aperçu avant impression utilise par défaut l’imprimante qui a servi le plus récemment.

Si vous activez cette stratégie, l’aperçu avant impression utilise l’imprimante par défaut du système d’exploitation.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PrintPreviewUseSystemDefaultPrinter
  - Nom de la stratégie de groupe: définir l’imprimante par défaut du système comme imprimante par défaut
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Printing
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Printing
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: PrintPreviewUseSystemDefaultPrinter
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PrintPreviewUseSystemDefaultPrinter
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PrintingEnabled
  #### Activer l’impression
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet d’imprimer dans MicrosoftEdge et empêche les utilisateurs de modifier ce paramètre.

Si cette stratégie n’est pas activée ou si elle n’est pas configurée, les utilisateurs sont autorisés à imprimer.

Si cette stratégie est désactivée, les utilisateurs ne sont pas autorisés à imprimer depuis MicrosoftEdge. L’impression est désactivée dans le menu clé à molette, les extensions, les applications JavaScript, etc. Les utilisateurs peuvent toujours imprimer à partir de plug-ins qui contournent MicrosoftEdge pendant l’impression. Par exemple, certaines applications AdobeFlash proposent, dans leur menu contextuel, des fonctionnalités d’impression qui ne sont pas affectées par cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PrintingEnabled
  - Nom de la stratégie de groupe: activer l’impression
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Printing
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: PrintingEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PrintingEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PrintingPaperSizeDefault
  #### Taille de page par défaut pour l’impression
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Remplacements de la taille de page par défaut pour l’impression.

le nom doit contenir l’une des mises en forme répertoriées ou «personnalisé» si la taille de papier requise ne figure pas dans la liste. Si la valeur «personnalisé» est fournie la propriété custom_size doit être spécifiée. Elle décrit la hauteur et la largeur souhaitées en micromètres. Sinon la propriété custom_size ne doit pas être spécifiée. La stratégie qui enfreint ces règles est ignorée.

Si la taille de page n’est pas disponible sur l’imprimante choisie par l’utilisateur, cette stratégie est ignorée.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Dictionary

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PrintingPaperSizeDefault
  - Nom de la stratégie de groupe: taille de page par défaut pour l’impression
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Printing
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: PrintingPaperSizeDefault
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {
  "custom_size": {
    "height": 297000, 
    "width": 210000
  }, 
  "name": "custom"
}
```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: PrintingPaperSizeDefault
  - Exemple de valeur:
``` xml
<key>PrintingPaperSizeDefault</key>
<dict>
  <key>custom_size</key>
  <dict>
    <key>height</key>
    <integer>297000</integer>
    <key>width</key>
    <integer>210000</integer>
  </dict>
  <key>name</key>
  <string>custom</string>
</dict>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### UseSystemPrintDialog
  #### Imprimer via la boîte de dialogue Imprimer du système
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Affiche la boîte de dialogue d’impression du système au lieu de l’aperçu avant impression.

Si vous activez cette stratégie, MicrosoftEdge ouvre la boîte de dialogue d’impression du système au lieu de l’aperçu avant impression intégré lorsque l’utilisateur imprime une page.

Si vous ne configurez pas ou désactivez cette stratégie, les commandes d’impression déclenchent l’écran de l’aperçu avant impression de MicrosoftEdge.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: UseSystemPrintDialog
  - Nom de la stratégie de groupe: imprimer via la boîte de dialogue Imprimer du système
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Printing
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: UseSystemPrintDialog
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: UseSystemPrintDialog
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ## Stratégies de serveur proxy

  [Retour au début](#microsoft-edge---policies)

  ### ProxyBypassList
  #### Configurer les règles de contournement du proxy
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Définit la liste des hôtes pour lesquels MicrosoftEdge contourne les proxy.

Cette stratégie est appliquée uniquement si vous avez sélectionné «Utiliser des serveurs proxy fixes» dans la stratégie [ProxyMode](#proxymode). Si vous avez sélectionné un autre mode pour la configuration des stratégies proxy, n’activez ou ne configurez pas cette stratégie.

Si vous activez cette stratégie, vous pouvez créer une liste d’hôtes pour lesquels MicrosoftEdge n’utilise pas de proxy.

Si vous ne configurez pas cette stratégie, aucune liste d’hôtes n’est créée et MicrosoftEdge ne contourne aucun proxy. Ne configurez pas cette stratégie si vous avez spécifié une autre méthode de configuration des stratégies de proxy.

Si vous souhaitez voir plus d’exemples plus détaillés, consultez [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ProxyBypassList
  - Nom de la stratégie de groupe: configurer les règles de contournement du proxy
  - Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge/Proxy server
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ProxyBypassList
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"https://www.contoso.com, https://www.fabrikam.com"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ProxyBypassList
  - Exemple de valeur:
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ProxyMode
  #### Configurer les paramètres du serveur proxy
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifiez les paramètres du serveur proxy utilisé par MicrosoftEdge. Si vous activez cette stratégie, les utilisateurs sont autorisés à modifier les paramètres du proxy.

Si vous choisissez de ne jamais utiliser un serveur proxy et de toujours vous connecter directement, toutes les autres options sont ignorées.

Si vous décidez d’utiliser les paramètres de proxy du système, toutes les autres options sont ignorées.

Si vous optez pour la détection automatique du serveur proxy, toutes les autres options sont ignorées.

Si vous choisissez le mode de serveur proxy fixe, vous pouvez spécifier d’autres options dans [ProxyServer](#proxyserver) et dans «Liste de règles de contournement de proxy séparées par des virgules».

Si vous décidez d’utiliser un script de proxy .pac, vous devez indiquer l’URL du script dans «URL d’un fichier .pac de proxy».

Si vous souhaitez voir des exemples plus détaillés, consultez [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

Si vous activez cette stratégie, MicrosoftEdge ignore toutes les options liées au proxy spécifiées à partir de la ligne de commande.

Si vous ne configurez pas cette stratégie, les utilisateurs peuvent choisir eux-mêmes leurs paramètres de proxy.

Mappage des options de stratégie:

* ProxyDisabled (direct)=Ne jamais utiliser de proxy

* ProxyAutoDetect (auto_detect)=Détecter automatiquement les paramètres du proxy

* ProxyPacScript (pac_script)=Utiliser un script proxy .pac

* ProxyFixedServers (fixed_servers)=Utiliser des serveurs proxy fixes

* ProxyUseSystem (system)=Utiliser les paramètres proxy du système

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ProxyMode
  - Nom de la stratégie de groupe: configurer les paramètres du serveur proxy
  - Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge/Proxy server
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ProxyMode
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"direct"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ProxyMode
  - Exemple de valeur:
``` xml
<string>direct</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ProxyPacUrl
  #### Définir l’URL du fichier .pac du proxy
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifie l’URL du fichier (PAC) de configuration automatique du proxy.

Cette stratégie est appliquée uniquement si vous sélectionnez «Utiliser un script proxy .pac» dans la stratégie [ProxyMode](#proxymode). Si vous avez sélectionné un autre mode pour la configuration des stratégies proxy, n’activez ou ne configurez pas cette stratégie.

Si vous activez cette stratégie, vous pouvez spécifier une URL pour un fichier PAC, qui définit la façon dont le navigateur choisit automatiquement le serveur proxy approprié pour l’extraction d’un site web particulier.

Si vous désactivez ou ne configurez pas cette stratégie, aucun fichier PAC n’est spécifié. Ne configurez pas cette stratégie si vous avez spécifié une autre méthode de configuration des stratégies de proxy.

Si vous souhaitez voir des exemples plus détaillés, consultez [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ProxyPacUrl
  - Nom de la stratégie de groupe: définir l’URL du fichier .pac du proxy
  - Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge/Proxy server
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ProxyPacUrl
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"https://internal.contoso.com/example.pac"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ProxyPacUrl
  - Exemple de valeur:
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ProxyServer
  #### Configurer l’adresse ou l’URL du serveur proxy
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifie l’URL du serveur proxy.

Cette stratégie est appliquée uniquement si vous avez sélectionné «Utiliser des serveurs proxy fixes» dans la stratégie [ProxyMode](#proxymode). Si vous avez sélectionné un autre mode pour la configuration des stratégies proxy, n’activez ou ne configurez pas cette stratégie.

Si vous activez cette stratégie, le serveur proxy configuré par cette stratégie sera utilisé pour toutes les URL.

Si vous désactivez ou ne configurez pas cette stratégie, les utilisateurs peuvent choisir eux-mêmes leurs paramètres de proxy dans le mode proxy. Ne configurez pas cette stratégie si vous avez spécifié une autre méthode de configuration des stratégies de proxy.

Si vous souhaitez voir plus d’options et plus d’exemples détaillés, consultez [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ProxyServer
  - Nom de la stratégie de groupe: configurer l’adresse ou l’URL du serveur proxy
  - Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge/Proxy server
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ProxyServer
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"123.123.123.123:8080"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ProxyServer
  - Exemple de valeur:
``` xml
<string>123.123.123.123:8080</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ProxySettings
  #### Paramètres du proxy
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Configure les paramètres de proxy pour MicrosoftEdge.

Si vous activez cette stratégie, MicrosoftEdge ignore toutes les options liées au proxy spécifiées à partir de la ligne de commande.

Si vous ne configurez pas cette stratégie, les utilisateurs peuvent choisir eux-mêmes leurs paramètres de proxy.

Cette stratégie remplace les stratégies individuelles suivantes:

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

Le champ ProxyMode vous permet de spécifier le serveur proxy utilisé par MicrosoftEdge et empêche les utilisateurs de modifier les paramètres du proxy.

Le champ ProxyPacUrl est une URL d’un fichier .pac du proxy.

Le champ ProxyServer est une URL pour le serveur proxy.

Le champ ProxyBypassList est une liste d’hôtes proxy que MicrosoftEdge contourne.

Si vous choisissez la valeur ’direct’ comme ’ProxyMode’, les proxy ne sont jamais utilisés et tous les autres champs sont ignorés.

Si vous choisissez la valeur ’direct’ comme ’ProxyMode’, le proxy du système est utilisé et tous les autres champs sont ignorés.

Si vous choisissez la valeur ’auto_detect’ comme ’ProxyMode’, tous les autres champs sont ignorés.

Si vous choisissez la valeur «fixed_server» comme 'ProxyMode', les champs 'ProxyServer' et 'ProxyBypassList' sont utilisés.

Si vous choisissez la valeur 'pac_script' comme 'ProxyMode', les champs 'ProxyPacUrl' et 'ProxyBypassList' sont utilisés.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Dictionary

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ProxySettings
  - Nom de la stratégie de groupe: paramètres du proxy
  - Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge/Proxy server
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ProxySettings
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ProxySettings
  - Exemple de valeur:
``` xml
<key>ProxySettings</key>
<dict>
  <key>ProxyBypassList</key>
  <string>https://www.example1.com,https://www.example2.com,https://internalsite/</string>
  <key>ProxyMode</key>
  <string>direct</string>
  <key>ProxyPacUrl</key>
  <string>https://internal.site/example.pac</string>
  <key>ProxyServer</key>
  <string>123.123.123.123:8080</string>
</dict>
```
  

  [Retour au début](#microsoft-edge---policies)

  ## Stratégies des paramètres SmartScreen

  [Retour au début](#microsoft-edge---policies)

  ### PreventSmartScreenPromptOverride
  #### Empêcher le contournement des avertissements de Microsoft Defender SmartScreen pour les sites
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Ce paramètre de stratégie indique si les utilisateurs peuvent ignorer les avertissements de MicrosoftDefenderSmartScreen concernant les sites web potentiellement malveillants.

Si vous activez ce paramètre, les utilisateurs ne peuvent pas ignorer les avertissements de WindowsDefenderSmartScreen et ne peuvent pas accéder au site.

Si vous désactivez ou ne configurez pas ce paramètre, les utilisateurs peuvent ignorer les avertissements de MicrosoftDefenderSmartScreen et accéder au site.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PreventSmartScreenPromptOverride
  - Nom de la stratégie de groupe: empêcher le contournement des avertissements de Microsoft Defender SmartScreen pour les sites
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/SmartScreen settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: PreventSmartScreenPromptOverride
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PreventSmartScreenPromptOverride
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PreventSmartScreenPromptOverrideForFiles
  #### Empêcher le contournement des avertissements de Microsoft Defender SmartScreen pour les téléchargements
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version77 ou versions ultérieures
  - sur macOS depuis la version79 ou versions ultérieures

  #### Description
  Cette stratégie vous permet de déterminer si les utilisateurs sont autorisés à ignorer les avertissements de Microsoft Defender SmartScreen pour le téléchargement de fichiers non vérifiés.

Si vous activez cette stratégie, les utilisateurs de votre organisation ne peuvent pas ignorer les avertissements de Microsoft Defender SmartScreen, et ne peuvent pas effectuer les téléchargements non vérifiés.

Si vous désactivez ou ne configurez pas cette stratégie, les utilisateurs peuvent ignorer les avertissements de MicrosoftDefenderSmartScreen et effectuer les téléchargements non vérifiés.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PreventSmartScreenPromptOverrideForFiles
  - Nom de la stratégie de groupe: empêcher le contournement des avertissements de Microsoft Defender SmartScreen pour les téléchargements
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/SmartScreen settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: PreventSmartScreenPromptOverrideForFiles
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PreventSmartScreenPromptOverrideForFiles
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SmartScreenAllowListDomains
  #### Configurer la liste des domaines pour lesquels Microsoft Defender SmartScreen ne déclenche pas d’avertissement
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Configurez la liste des domaines approuvés par Microsoft Defender SmartScreen. Cela signifie que Microsoft Defender SmartScreen ne recherche pas les ressources potentiellement malveillantes, telles que les logiciels d’hameçonnage et autres programmes malveillants, si les URL sources correspondent à ces domaines.
Le service de protection de téléchargement de Microsoft Defender SmartScreen ne vérifie pas les téléchargements hébergés sur ces domaines.

Si vous activez cette stratégie, Microsoft Defender SmartScreen approuve ces domaines.
Si vous désactivez ou ne configurez pas cette stratégie, la protection Microsoft Defender SmartScreen par défaut est appliquée à toutes les ressources.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.
Notez également que cette stratégie ne s’applique pas si votre organisation a activé Microsoft Defender - Protection avancée contre les menaces. Vous devez plutôt configurer vos listes verte et rouge dans le Centre de sécurité Microsoft Defender.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SmartScreenAllowListDomains
  - Nom de la stratégie de groupe: configurer la liste des domaines pour lesquels Microsoft Defender SmartScreen ne déclenche pas d’avertissement
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/SmartScreen settings
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SmartScreenAllowListDomains
  - Exemple de valeur:
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SmartScreenEnabled
  #### Configurer Microsoft Defender SmartScreen
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Ce paramètre de stratégie vous permet de configurer l’activation ou la désactivation de MicrosoftDefenderSmartScreen. MicrosoftDefenderSmartScreen envoie des messages d’avertissement pour protéger les utilisateurs contre d’éventuels courriers indésirables d’hameçonnage et logiciels malveillants. Par défaut, MicrosoftDefenderSmartScreen est activé.

Si vous activez ce paramètre, MicrosoftDefenderSmartScreen est activé.

Si vous désactivez ce paramètre, MicrosoftDefenderSmartScreen est désactivé.

Si vous ne configurez pas ce paramètre, les utilisateurs peuvent choisir d’utiliser ou non MicrosoftDefenderSmartScreen.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SmartScreenEnabled
  - Nom de la stratégie de groupe: configurer Microsoft Defender SmartScreen
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/SmartScreen settings
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/SmartScreen settings
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: SmartScreenEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SmartScreenEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SmartScreenForTrustedDownloadsEnabled
  #### Forcer Microsoft Defender SmartScreen à vérifier les téléchargements provenant de sources approuvées
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version78 ou versions ultérieures

  #### Description
  Ce paramètre de stratégie vous permet de configurer la vérification, par Microsoft Defender SmartScreen, de la réputation des téléchargements provenant d’une source approuvée.

Si vous activez ou ne configurez pas ce paramètre, Microsoft Defender SmartScreen vérifie la réputation du téléchargement quelle que soit la source.

Si vous désactivez ce paramètre, Microsoft Defender SmartScreen ne vérifie pas la réputation du téléchargement lors d’un téléchargement provenant d’une source approuvée.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise qui sont inscrites pour la gestion des appareils.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SmartScreenForTrustedDownloadsEnabled
  - Nom de la stratégie de groupe: forcer Microsoft Defender SmartScreen à vérifier les téléchargements provenant de sources approuvées
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/SmartScreen settings
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/SmartScreen settings
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: SmartScreenForTrustedDownloadsEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  

  [Retour au début](#microsoft-edge---policies)

  ### SmartScreenPuaEnabled
  #### Configurer Microsoft Defender SmartScreen pour bloquer les applications potentiellement indésirables.
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Ce paramètre de stratégie vous permet de configurer l’activation ou la désactivation du blocage des applications potentiellement indésirables dans MicrosoftDefenderSmartScreen. Le blocage d’applications potentiellement indésirables dans Microsoft Defender SmartScreen fournit des messages d’avertissement pour protéger les utilisateurs des logiciels de publicité, des minages de cryptomonnaie, des bundleware et autres applications à faible réputation, hébergées par des sites web. Le blocage d’applications potentiellement indésirables dans Microsoft Defender SmartScreen est désactivé par défaut.

Si vous activez ce paramètre, le blocage des applications potentiellement indésirables dans Microsoft Defender SmartScreen est activé.

Si vous désactivez ce paramètre, le blocage des applications potentiellement indésirables dans Microsoft Defender SmartScreen est désactivé.

Si vous ne configurez pas ce paramètre, les utilisateurs peuvent choisir s’ils souhaitent utiliser le blocage des applications potentiellement indésirables dans Microsoft Defender SmartScreen.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SmartScreenPuaEnabled
  - Nom de la stratégie de groupe: configurer Microsoft Defender SmartScreen pour bloquer les applications potentiellement indésirables.
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/SmartScreen settings
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/SmartScreen settings
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: SmartScreenPuaEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SmartScreenPuaEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ## Stratégies de démarrage&comma; page d’accueil et page Nouvel onglet

  [Retour au début](#microsoft-edge---policies)

  ### HomepageIsNewTabPage
  #### Définir la page Nouvel onglet comme page d’accueil
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Configure la page d’accueil par défaut dans MicrosoftEdge. Vous pouvez définir la page d’accueil sur une URL que vous spécifiez ou sur la page Nouvel onglet.

Si vous activez cette stratégie, la page Nouvel onglet est systématiquement utilisée comme page d’accueil, et l’adresse URL de la page d’accueil est ignorée.

Si vous désactivez cette stratégie, la page d’accueil de l’utilisateur ne peut pas être la page Nouvel onglet, sauf si l’URL de la page d’accueil est définie sur 'edge://newtab'.

Si la stratégie n’a pas été configurée, les utilisateurs peuvent choisir d’utiliser la page Nouvel onglet comme page d’accueil.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: HomepageIsNewTabPage
  - Nom de la stratégie de groupe: définir la page Nouvel onglet comme page d’accueil
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Startup, home page and new tab page
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: HomepageIsNewTabPage
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: HomepageIsNewTabPage
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### HomepageLocation
  #### Configurer l’URL de la page d’accueil
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Configure l’URL de la page d’accueil par défaut dans MicrosoftEdge.

La page d’accueil est la page qui s’ouvre lorsque le bouton Accueil est sélectionné. Les pages qui s’ouvrent au démarrage sont contrôlées par les stratégies [RestoreOnStartup](#restoreonstartup).

Vous pouvez spécifier une URL ici ou choisir la page d’accueil pour ouvrir la page Nouvel onglet. Si vous choisissez d’ouvrir la page Nouvel onglet, cette stratégie ne s’applique pas.

Si vous activez cette stratégie, les utilisateurs ne peuvent pas modifier l’URL de la page d’accueil, mais ils peuvent ils peuvent définir la page Nouvel onglet comme page d’accueil.

Si vous désactivez ou ne configurez pas cette stratégie, les utilisateurs peuvent choisir leur propre page d’accueil, tant que la stratégie [HomepageIsNewTabPage](#homepageisnewtabpage) n’est pas activée.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: HomepageLocation
  - Nom de la stratégie de groupe: configurer l’URL de la page d’accueil
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Startup, home page and new tab page
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: HomepageLocation
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"https://www.contoso.com"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: HomepageLocation
  - Exemple de valeur:
``` xml
<string>https://www.contoso.com</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NewTabPageAllowedBackgroundTypes
  #### Configurer les types d’arrière-plan autorisés pour la disposition du nouvel onglet
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Vous pouvez définir les types d’image d’arrière-plan qui sont autorisés dans la disposition du nouvel onglet dans Microsoft Edge.

Si vous ne configurez pas cette stratégie, tous les types d’images d’arrière-plan du nouvel onglet sont activés.

Mappage des options de stratégie:

* DisableImageOfTheDay (1) = Désactiver le type d’image d’arrière-plan quotidienne

* DisableCustomImage (2) = Désactiver le type d’image d’arrière-plan personnalisée

* DisableAll (3) = Désactiver tous types d’image d’arrière-plan

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP : NewTabPageAllowedBackgroundTypes
  - Nom GP : Définir les types d’arrière-plan autorisés pour la disposition du nouvel onglet
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur : NewTabPageAllowedBackgroundTypes
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom de clé préféré : NewTabPageAllowedBackgroundTypes
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NewTabPageCompanyLogo
  #### Définir le logo de l’entreprise sur la page Nouvel onglet (obsolète)
  
  >OBSOLÈTE: Cette stratégie est obsolète et ne fonctionne pas après la version85 de MicrosoftEdge.
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version79 et jusqu’à la version85

  #### Description
  Cette stratégie ne fonctionnait pas comme prévu en raison de modifications apportées aux besoins opérationnels. Par conséquent, elle est obsolète et ne doit pas être utilisée.

Spécifie le logo de l’entreprise à utiliser sur la page Nouvel onglet dans MicrosoftEdge.

La stratégie doit être configurée sous la forme d’une chaîne qui exprime le ou les logos au format JSON. Par exemple: { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

Pour configurer cette stratégie, spécifiez l’URL à partir de laquelle MicrosoftEdge peut télécharger le logo et son hachage de chiffrement (SHA-256), qui permet de vérifier l’intégrité du téléchargement. Le logo doit être au format PNG ou SVG et sa taille de fichier ne doit pas dépasser16 Mo. Le logo est téléchargé et mis en cache. Il est téléchargé à nouveau, à chaque modification de l’URL ou du hachage. L’URL doit être accessible sans authentification.

Le «default_logo» est obligatoire et est utilisé lorsqu’il n’y a pas d’image d’arrière-plan. Si «light_logo» est spécifié, il est utilisé lorsque le nouvel onglet de l’utilisateur a une image d’arrière-plan. Il est recommandé d’utiliser un logo horizontal, avec un arrière-plan transparent aligné à gauche, et centré verticalement. Le logo doit avoir une hauteur minimale de 32pixels et des proportions de 1:1 à 4:1. Le «default_logo» doit avoir un contraste approprié avec un arrière-plan blanc/noir, tandis que le «light_logo» doit avoir un contraste correct par rapport à une image d’arrière-plan.

Si vous activez cette stratégie, MicrosoftEdge télécharge et affiche le ou les logo spécifiés sur le nouvel onglet. Les utilisateurs ne peuvent ni remplacer ni masquer le ou les logos. 

Si vous désactivez cette stratégie ou si vous ne la configurez pas, MicrosoftEdge n’affiche pas le logo de l’entreprise, ni le logo Microsoft sur le nouvel onglet.

Pour obtenir de l’aide sur la détermination du hachage SHA-256, consultez https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Dictionary

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: NewTabPageCompanyLogo
  - Nom de la stratégie de groupe: définir le logo de l’entreprise sur la page Nouvel onglet (obsolète)
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: NewTabPageCompanyLogo
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageCompanyLogo = {
  "default_logo": {
    "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29", 
    "url": "https://www.contoso.com/logo.png"
  }, 
  "light_logo": {
    "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737", 
    "url": "https://www.contoso.com/light_logo.png"
  }
}
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: NewTabPageCompanyLogo
  - Exemple de valeur:
``` xml
<key>NewTabPageCompanyLogo</key>
<dict>
  <key>default_logo</key>
  <dict>
    <key>hash</key>
    <string>cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29</string>
    <key>url</key>
    <string>https://www.contoso.com/logo.png</string>
  </dict>
  <key>light_logo</key>
  <dict>
    <key>hash</key>
    <string>517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737</string>
    <key>url</key>
    <string>https://www.contoso.com/light_logo.png</string>
  </dict>
</dict>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NewTabPageHideDefaultTopSites
  #### Masquer les sites populaires par défaut dans la page Nouvel onglet
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Masque les sites populaires par défaut dans la page Nouvel onglet sur MicrosoftEdge.

Si vous attribuez la valeur true à cette stratégie, les vignettes de site populaire par défaut sont masquées.

Si vous attribuez la valeur false à cette stratégie ou si vous ne la configurez pas, les vignettes de site populaire par défaut restent visibles.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: NewTabPageHideDefaultTopSites
  - Nom de la stratégie de groupe: masquer les sites populaires par défaut dans la page Nouvel onglet
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: NewTabPageHideDefaultTopSites
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: NewTabPageHideDefaultTopSites
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NewTabPageLocation
  #### Configurer l’URL de la page Nouvel onglet
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Configure l’URL par défaut de la page Nouvel onglet.

Cette stratégie détermine la page qui s’ouvre lors de la création de nouveaux onglets (y compris lorsque de nouvelles fenêtres sont ouvertes). Elle affecte également la page de démarrage si celle-ci est configurée pour s’ouvrir sur la page Nouvel onglet.

Cette stratégie ne détermine pas la page qui s’ouvre au démarrage. Cette dernière est contrôlée par la stratégie [RestoreOnStartup](#restoreonstartup). Elle n’affecte pas non plus la page d’accueil si celle-ci est configurée pour s’ouvrir sur la page Nouvel onglet.

Si cette stratégie n’est pas configurée, la page Nouvel onglet par défaut est utilisée. 

Si vous configurez cette stratégie *et * la stratégie [NewTabPageSetFeedType](#newtabpagesetfeedtype), cette stratégie prévaut.

Si une URL non valide est fournie, les nouveaux onglets affichent about://blank.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: NewTabPageLocation
  - Nom de la stratégie de groupe: configurer l’URL de la page Nouvel onglet
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Startup, home page and new tab page
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: NewTabPageLocation
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"https://www.fabrikam.com"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: NewTabPageLocation
  - Exemple de valeur:
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NewTabPageManagedQuickLinks
  #### Définir les liens rapides de la page Nouvel onglet
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version79 ou versions ultérieures

  #### Description
  Par défaut, MicrosoftEdge affiche les liens rapides du nouvel onglet à partir des raccourcis ajoutés par l’utilisateur et des sites populaires en fonction de l’historique de navigation.  Grâce à cette stratégie, vous pouvez configurer jusqu’à trois vignettes de liens rapides sur la page Nouvel onglet, exprimées sous forme d’objet JSON:

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

Le champ «url» est obligatoire ; les éléments «title» et «pinned» sont facultatifs. Si «title» n’est pas spécifié, l’URL est utilisée comme titre par défaut. Si «pinned» n’est pas spécifié, la valeur par défaut est false.

MicrosoftEdge présente celles-ci dans l’ordre dans lequel elles sont répertoriées, de gauche à droite, avec toutes les vignettes épinglées affichées avant les vignettes non épinglées.

Si la stratégie est définie comme obligatoire, le champ «pinned» est ignoré et toutes les vignettes sont épinglées. Les vignettes ne peuvent pas être supprimées par l’utilisateur et apparaissent toujours au début de la liste des liens rapides.

Si la stratégie est définie comme recommandée, les vignettes épinglées sont conservées dans la liste, mais l’utilisateur peut les modifier et les supprimer. Les vignettes de lien rapide qui ne sont pas épinglées se comportent comme des sites populaires par défaut et sont exclues de la liste si d’autres sites web sont visités plus fréquemment. Lors de l’application de liens non épinglés via cette stratégie à un profil de navigateur existant, il est possible que les liens n’apparaissent pas du tout, suivant la façon dont ils sont classés par rapport à l’historique de navigation de l’utilisateur.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Dictionary

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: NewTabPageManagedQuickLinks
  - Nom de la stratégie de groupe: définir les liens rapides de la page Nouvel onglet
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Startup, home page and new tab page
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: NewTabPageManagedQuickLinks
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageManagedQuickLinks = [
  {
    "pinned": true, 
    "title": "Contoso Portal", 
    "url": "https://contoso.com"
  }, 
  {
    "title": "Fabrikam", 
    "url": "https://fabrikam.com"
  }
]
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: NewTabPageManagedQuickLinks
  - Exemple de valeur:
``` xml
<key>NewTabPageManagedQuickLinks</key>
<array>
  <dict>
    <key>pinned</key>
    <true/>
    <key>title</key>
    <string>Contoso Portal</string>
    <key>url</key>
    <string>https://contoso.com</string>
  </dict>
  <dict>
    <key>title</key>
    <string>Fabrikam</string>
    <key>url</key>
    <string>https://fabrikam.com</string>
  </dict>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NewTabPagePrerenderEnabled
  #### Activer le préchargement de la nouvelle page d’onglet pour un rendu plus rapide
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version85 ou versions ultérieures

  #### Description
  Si vous configurez cette stratégie, le préchargement de la page de l’onglet nouveau est activé, et les utilisateurs ne peuvent pas modifier ce paramètre. Si vous ne configurez pas cette stratégie, le préchargement est activé et un utilisateur peut modifier ce paramètre.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: NewTabPagePrerenderEnabled
  - Nom de la stratégie de contrôle: activer le préchargement de la nouvelle page d’onglet pour un rendu plus rapide
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Startup, home page and new tab page
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: NewTabPagePrerenderEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: NewTabPagePrerenderEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NewTabPageSetFeedType
  #### Configurer l’expérience de la page Nouvel onglet MicrosoftEdge
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version79 ou versions ultérieures

  #### Description
  Vous permet de choisir l’expérience de flux MicrosoftActualités ou Office365 pour la page Nouvel onglet.

Si vous définissez cette stratégie sur « News », les utilisateurs voient l’expérience de flux Microsoft Actualités sur le nouvel onglet.

Si vous définissez cette stratégie sur « Office », les utilisateurs disposant d’une session sur le navigateur AzureActiveDirectory voient l’expérience de flux Office365 sur le nouvel onglet.

Si vous désactivez ou ne configurez pas cette stratégie:

- les utilisateurs disposant d’une connexion au navigateur AzureActiveDirectory se voient proposer l’expérience de flux de la page Nouvel onglet Office365, ainsi que l’expérience standard de flux de la page Nouvel onglet.

- les utilisateurs sans connexion au navigateur AzureActiveDirectory voient l’expérience standard de la page Nouvel onglet.

Si vous configurez cette stratégie *et* la stratégie [NewTabPageLocation](#newtabpagelocation), [NewTabPageLocation](#newtabpagelocation) prévaut.

Paramètre par défaut: désactivé ou non configuré.

Mappage des options de stratégie:

* News (0)=Expérience de flux Microsoft Actualités

* Office (1)=Expérience de flux Office365

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: NewTabPageSetFeedType
  - Nom de la stratégie de groupe: configurer l’expérience de la page Nouvel onglet MicrosoftEdge
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Startup, home page and new tab page
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: NewTabPageSetFeedType
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: NewTabPageSetFeedType
  - Exemple de valeur:
``` xml
<integer>0</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### RestoreOnStartup
  #### Action à effectuer au démarrage
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifiez le comportement du navigateur au démarrage.

Si vous souhaitez qu’un nouvel onglet s’ouvre à chaque démarrage, choisissez «RestoreOnStartupIsNewTabPage».

Si vous souhaitez rouvrir les URL ouvertes à la dernière fermeture de MicrosoftEdge, choisissez «RestoreOnStartupIsLastSession». La session de navigation est restaurée telle que vous l’avez laissée. La sélection de cette option entraîne la désactivation de certains paramètres qui sont basés sur les sessions ou qui ont pour effet l’exécution d’actions lors de la fermeture du navigateur, comme la suppression des données de navigation ou des cookies d’une session.

Si vous souhaitez ouvrir un groupe d’URL particulier, choisissez «RestoreOnStartupIsURLs ».

La désactivation de ce paramètre revient à le laisser non configuré. Les utilisateurs pourront le modifier dans MicrosoftEdge.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

Mappage des options de stratégie:

* RestoreOnStartupIsNewTabPage (5) = Ouvrir un nouvel onglet

* RestoreOnStartupIsLastSession (1) = Restaurer la dernière session

* RestoreOnStartupIsURLs (4) = Ouvrir une liste d’URL

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: RestoreOnStartup
  - Nom de la stratégie de groupe: action à effectuer au démarrage
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Startup, home page and new tab page
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: RestoreOnStartup
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000004
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: RestoreOnStartup
  - Exemple de valeur:
``` xml
<integer>4</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### RestoreOnStartupURLs
  #### Sites à ouvrir lors du démarrage du navigateur
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifiez une liste de sites web à ouvrir automatiquement lors du démarrage du navigateur. Si vous ne configurez pas cette stratégie, aucun site n’est ouvert lors du démarrage.

Cette stratégie ne fonctionne que si vous avez également configuré la stratégie [RestoreOnStartup](#restoreonstartup) sur ’Ouvrir une liste d’URL' (4).

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: RestoreOnStartupURLs
  - Nom de la stratégie de groupe: sites à ouvrir lors du démarrage du navigateur
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Startup, home page and new tab page
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended\RestoreOnStartupURLs
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: RestoreOnStartupURLs
  - Exemple de valeur:
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ShowHomeButton
  #### Afficher le bouton Accueil sur la barre d’outils
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Affiche le bouton Accueil sur la barre d’outils de MicrosoftEdge.

Activez cette stratégie pour que le bouton Accueil soit toujours affiché. Désactivez-la pour que le bouton ne soit jamais affiché.

Si vous ne configurez pas la stratégie, les utilisateurs peuvent choisir d’afficher ou non le bouton Accueil.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ShowHomeButton
  - Nom de la stratégie de groupe: afficher le bouton Accueil sur la barre d’outils
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/Startup, home page and new tab page
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/Startup, home page and new tab page
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ShowHomeButton
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ShowHomeButton
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ## Stratégies supplémentaires

  [Retour au début](#microsoft-edge---policies)

  ### AddressBarMicrosoftSearchInBingProviderEnabled
  #### Activer les suggestions de la Recherche Microsoft dans la barre d’adresse de Bing
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version81 ou versions ultérieures

  #### Description
  Permet d’afficher les suggestions de Recherche Microsoft dans Bing appropriées dans la liste de suggestions de la barre d’adresse lorsque l’utilisateur tape une chaîne de recherche dans la barre d’adresse. Si vous activez cette stratégie ou si vous ne la configurez pas, les utilisateurs peuvent voir les résultats internes obtenus par la Recherche Microsoft dans Bing dans la liste de suggestions de la barre d’adresse de MicrosoftEdge. Pour afficher les résultats de Recherche Microsoft dans Bing, l’utilisateur doit être connecté à MicrosoftEdge avec son compte AzureAD pour cette organisation.
Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas voir les résultats internes dans la liste de suggestions de la barre d’adresse de MicrosoftEdge.
Si vous avez activé l’ensemble de stratégies qui force un moteur de recherche par défaut ([DefaultSearchProviderEnabled](#defaultsearchproviderenabled), [DefaultSearchProviderName](#defaultsearchprovidername) et [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)), et si le moteur de recherche spécifié n’est pas Bing, cette stratégie n’est pas applicable et aucune suggestion de Recherche Microsoft dans Bing n’apparaît dans la liste de suggestions de la barre d’adresse.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AddressBarMicrosoftSearchInBingProviderEnabled
  - Nom de la stratégie de groupe: activer les suggestions de la Recherche Microsoft dans la barre d’adresse de Bing
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AddressBarMicrosoftSearchInBingProviderEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AddressBarMicrosoftSearchInBingProviderEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AdsSettingForIntrusiveAdsSites
  #### Paramètres des annonces pour les sites contenant des annonces gênantes
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version78 ou versions ultérieures

  #### Description
  Détermine si les annonces sont bloquées sur les sites présentant des annonces intrusives.

Mappage des options de stratégie:

* AllowAds (1)=Autoriser les annonces sur tous les sites.

* BlockAds (2)=Bloquer les annonces sur les sites présentant des annonces intrusives. (Valeur par défaut)

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AdsSettingForIntrusiveAdsSites
  - Nom de la stratégie de groupe: paramètres des annonces pour les sites contenant des annonces gênantes
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AdsSettingForIntrusiveAdsSites
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AdsSettingForIntrusiveAdsSites
  - Exemple de valeur:
``` xml
<integer>1</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AllowDeletingBrowserHistory
  #### Activer la suppression de l’historique du navigateur et de l’historique des téléchargements
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet la suppression de l’historique du navigateur et de l’historique des téléchargements sans permettre à l’utilisateur de modifier ce paramètre.

Même si cette stratégie est désactivée, il n’est pas garanti que l’historique du navigateur et l’historique des téléchargements soient conservés: les utilisateurs peuvent modifier ou supprimer directement les fichiers de base de données de ces historiques. De même, le navigateur peut supprimer ou archiver, à tout moment, des éléments de l’historique.

Si vous activez cette stratégie ou que vous ne la configurez pas, les utilisateurs peuvent supprimer l’historique de navigation et de téléchargement.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas supprimer l’historique de navigation et de téléchargement.

Si vous activez cette stratégie, n’activez pas la stratégie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), car elles traitent toutes deux la suppression de données. Si vous activez toutes les deux, la stratégie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) prévaut et supprime toutes les données lors de la fermeture de MicrosoftEdge, quelle que soit la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AllowDeletingBrowserHistory
  - Nom de la stratégie de groupe: activer la suppression de l’historique du navigateur et de l’historique des téléchargements
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AllowDeletingBrowserHistory
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AllowDeletingBrowserHistory
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AllowFileSelectionDialogs
  #### Autoriser les boîtes de dialogue de sélection de fichier
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Autoriser l’accès aux fichiers locaux en laissant MicrosoftEdge afficher les boîtes de dialogue de sélection de fichier.

Si vous activez ou ne configurez pas cette stratégie, les utilisateurs peuvent ouvrir normalement les boîtes de dialogue de sélection des fichiers.

Si vous désactivez cette stratégie, chaque fois que l’utilisateur effectue une action entraînant l’ouverture d’une boîte de dialogue de sélection de fichiers (par exemple, une importation de favoris, un téléchargement de fichiers ou l’enregistrement de liens), un message s’affiche à la place et l’utilisateur est supposé avoir cliqué sur Annuler dans la boîte de dialogue de sélection de fichiers.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AllowFileSelectionDialogs
  - Nom de la stratégie de groupe: autoriser les boîtes de dialogue de sélection de fichier
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AllowFileSelectionDialogs
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AllowFileSelectionDialogs
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AllowPopupsDuringPageUnload
  #### Autorise une page à afficher les fenêtres contextuelles pendant son déchargement
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version78 ou versions ultérieures

  #### Description
  Cette stratégie permet à un administrateur de spécifier si une page peut afficher des fenêtres contextuelles pendant son déchargement.

Lorsque la stratégie est activée, les pages sont autorisées à afficher des fenêtres contextuelles pendant leur déchargement.

Lorsque la stratégie est désactivée ou n’est pas configurée, les pages ne sont pas autorisées à afficher des fenêtres contextuelles pendant leur déchargement. Ceci est conforme à la spécification: (https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name).

Cette stratégie sera supprimée à l’avenir.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AllowPopupsDuringPageUnload
  - Nom de la stratégie de groupe: autorise une page à afficher les fenêtres contextuelles pendant son déchargement
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AllowPopupsDuringPageUnload
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AllowPopupsDuringPageUnload
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AllowSurfGame
  #### Autoriser le jeu de surf
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version83 ou versions ultérieures

  #### Description
  Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas jouer au jeu de surf lorsque l’appareil est hors connexion ou si l’utilisateur accède à edge://surf.

Si cette stratégie est activée ou si elle n’est pas configurée, les utilisateurs peuvent jouer au jeu de surf.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AllowSurfGame
  - Nom de la stratégie de groupe: autoriser le jeu de surf
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AllowSurfGame
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AllowSurfGame
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AllowSyncXHRInPageDismissal
  #### Autoriser les pages à envoyer des demandes XHR synchrones lors de l’opération de rejet de page (déconseillé)
  >DÉCONSEILLÉ: cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version79 ou versions ultérieures

  #### Description
  Cette stratégie est déconseillée, car elle n’est destinée qu’à être un mécanisme à court terme qui permet aux entreprises de mettre à jour leur contenu web si et quand il est détecté comme étant incompatible avec la modification pour interdire les demandes XHR synchrones au cours du masquage de page. Il ne fonctionne pas dans la version 88 de Microsoft Edge.

Cette stratégie vous permet de spécifier si une page peut envoyer des demandes XHR synchrones lors de l’opération de rejet de page.

Si vous activez cette stratégie, les pages envoient des demandes XHR synchrones lors de l’opération de rejet de page.

Si vous désactivez cette stratégie ou ne la configurez pas, les pages ne sont pas autorisées à envoyer des demandes XHR synchrones lors de l’opération de rejet de page.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AllowSyncXHRInPageDismissal
  - Nom de la stratégie de groupe: Autoriser les pages à envoyer des demandes XHR synchrones lors de l’opération de rejet de page (déconseillé)
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AllowSyncXHRInPageDismissal
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AllowSyncXHRInPageDismissal
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AllowTokenBindingForUrls
  #### Configurer la liste des sites avec lesquels MicrosoftEdge tentera d’établir une liaison de jetons
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version83 ou versions ultérieures

  #### Description
  Configurez la liste des modèles d’URL pour les sites avec lesquels le navigateur tentera d’effectuer le protocole de liaison de jetons.
Pour les domaines de cette liste, le navigateur envoie la liaison de jeton ClientHello pour l’établissement d’une liaison TLS (consultez https://tools.ietf.org/html/rfc8472).
Si le serveur répond par une réponse ServerHello valide, le navigateur crée et envoie des messages de liaison de jetons aux requêtes http suivantes. Si vous souhaitez en savoir plus, consultez https://tools.ietf.org/html/rfc8471.

Si cette liste est vide, la liaison par jeton sera désactivée.

Cette stratégie est disponible uniquement sur les appareils Windows10 disposant de la fonctionnalité Virtual Secure Mode.

À compter de MicrosoftEdge86, cette stratégie ne prend plus en charge l’actualisation dynamique.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AllowTokenBindingForUrls
  - Nom de la stratégie de groupe: configurer la liste des sites avec lesquels MicrosoftEdge tentera d’établir une liaison de jeton
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```


  

  [Retour au début](#microsoft-edge---policies)

  ### AllowTrackingForUrls
  #### Configurer les exceptions de prévention du suivi pour des sites spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version78 ou versions ultérieures

  #### Description
  Configurez la liste des modèles d’URL qui sont exclus de la prévention du suivi. 

Si vous configurez cette stratégie, la liste des modèles d’URL configurés est exclue de la prévention du suivi.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie «Block tracking of users' web-browsing activity», si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AllowTrackingForUrls
  - Nom de la stratégie de groupe: configurer les exceptions de prévention du suivi pour des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AllowTrackingForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AlternateErrorPagesEnabled
  #### Suggérer des pages similaires lorsqu’une page web est introuvable
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Autorisez MicrosoftEdge à émettre une connexion à un service web pour générer des suggestions d’URL et de recherche pour les problèmes de connectivité tels que les erreurs DNS.

Si vous activez cette stratégie, un service web est utilisé pour générer des suggestions d’URL et de recherche pour les erreurs de réseau.

Si vous désactivez cette stratégie, aucun appel au service web n’est effectué et une page d’erreur standard s’affiche.

Si vous ne configurez pas cette stratégie, MicrosoftEdge respecte les préférences de l’utilisateur, définies dans Services sur edge://settings/privacy.
Plus précisément, il existe un bouton **Suggérer des pages similaires lorsqu’une page Web est introuvable**, que l’utilisateur peut activer ou désactiver. Si vous avez activé cette stratégie (AlternateErrorPagesEnabled), le paramètre Suggérer des pages similaires lorsqu’une page web est introuvable est activé, mais l’utilisateur ne peut pas modifier le paramètre à l’aide du bouton. Si vous avez désactivé cette stratégie, le paramètre Suggérer des pages similaires lorsqu’une page web est introuvable est désactivé, et l’utilisateur ne peut pas modifier le paramètre à l’aide du bouton.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AlternateErrorPagesEnabled
  - Nom de la stratégie de groupe: suggérer des pages similaires lorsqu’une page web est introuvable
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: AlternateErrorPagesEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AlternateErrorPagesEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AlwaysOpenPdfExternally
  #### Toujours ouvrir les fichiers PDF en externe
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Désactive la visionneuse de PDF intégrée dans MicrosoftEdge.

Si vous activez cette stratégie, Microsoft Edge traite les fichiers PDF de la même manière que les téléchargements et permet aux utilisateurs de les ouvrir avec l’application par défaut.

Si vous ne configurez pas cette stratégie ou si vous la désactivez, MicrosoftEdge ouvre les fichiers PDF (à moins que l’utilisateur ne le désactive).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AlwaysOpenPdfExternally
  - Nom de la stratégie de groupe: toujours ouvrir les fichiers PDF en externe
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AlwaysOpenPdfExternally
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AlwaysOpenPdfExternally
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AmbientAuthenticationInPrivateModesEnabled
  #### Activer l’authentification par le bruit ambiant pour les profils d’invité et InPrivate
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version81 ou versions ultérieures

  #### Description
  Configurez cette stratégie pour autoriser/refuser l’authentification par le bruit ambiant pour les profils InPrivate et Invité dans MicrosoftEdge.

L’authentification par le bruit ambient est une authentification http avec des informations d’identification par défaut lorsque les informations d’identification explicites ne sont pas disponibles via les schémas de stimulation/réponse NTLM/Kerberos/Negotiate.

Si vous définissez la stratégie sur « RegularOnly », l’authentification ambiante est autorisée pour les sessions normales uniquement. Les sessions InPrivate et invité ne sont pas autorisées à s’authentifier par le bruit ambiant.

Si vous définissez la stratégie sur « InPrivateAndRegular », l’authentification ambiante est autorisée pour les sessions InPrivate et les sessions normales. Les sessions Invité ne sont pas autorisées à s’authentifier par le bruit ambiant.

Si vous définissez la stratégie sur « GuestAndRegular », l’authentification ambiante est autorisée pour les sessions Invité et normales. Les sessions InPrivate ne sont pas autorisées à s’authentifier par le bruit ambiant.

Si vous définissez la stratégie sur « All », l’authentification ambiante est autorisée pour toutes les sessions.

Notez que l’authentification par le bruit ambiant est toujours autorisée sur les profils réguliers.

Dans les versions81 ou ultérieures de MicrosoftEdge, si la stratégie n’est pas configurée, l’authentification par le bruit ambiant est activée uniquement dans les sessions régulières.

Mappage des options de stratégie:

* RegularOnly (0)=Activer l’authentification ambiante dans les sessions normales uniquement

* InPrivateAndRegular (1)=Activer l’authentification ambiante dans les sessions InPrivate et normales

* GuestAndRegular (2)=Activer l’authentification ambiante dans les sessions Invité et normales

* All (3)=Activer l’authentification ambiante dans les sessions normales, InPrivate et Invité

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AmbientAuthenticationInPrivateModesEnabled
  - Nom de la stratégie de groupe: activer l’authentification par le bruit ambiant pour les profils d’invité et InPrivate
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AmbientAuthenticationInPrivateModesEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AmbientAuthenticationInPrivateModesEnabled
  - Exemple de valeur:
``` xml
<integer>0</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AppCacheForceEnabled
  #### Permet de réactiver la fonctionnalité AppCache, même si elle est désactivée par défaut.
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version84 ou versions ultérieures

  #### Description
  Si vous attribuez la valeur true à cette stratégie, la AppCache est activée, même si AppCache dans Microsoft Edge n’est pas disponible par défaut.

Si vous avez défini cette stratégie sur false ou que vous ne la configurez pas, AppCache suivra les valeurs par défaut de Microsoft Edge.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: AppCacheForceEnabled
  - Nom de la stratégie de protection: permet de réactiver la fonctionnalité AppCache, même si elle est désactivée par défaut.
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AppCacheForceEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: AppCacheForceEnabled
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ApplicationLocaleValue
  #### Définir les paramètres régionaux de l’application
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version77 ou versions ultérieures

  #### Description
  Configure les paramètres régionaux de l’application dans MicrosoftEdge et empêche les utilisateurs de modifier ces paramètres.

Si vous activez ce paramètre, MicrosoftEdge utilise les paramètres régionaux spécifiés. Si les paramètres régionaux configurés ne sont pas pris en charge, la valeur 'en-US' est utilisée à la place.

Si vous désactivez ou ne configurez pas ce paramètre, MicrosoftEdge utilise les paramètres régionaux favoris de l’utilisateur (s’ils ont été configurés), ou les paramètres régionaux de remplacement ("en-US").

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ApplicationLocaleValue
  - Nom de la stratégie de groupe: définir les paramètres régionaux de l’application
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ApplicationLocaleValue
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"en"
```


  

  [Retour au début](#microsoft-edge---policies)

  ### AudioCaptureAllowed
  #### Autoriser ou bloquer la capture de sons
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Vous permet de déterminer si un utilisateur est interrogé pour accorder aux sites web l’accès à son appareil de capture audio. Cette stratégie s’applique à toutes les URL, à l’exception de celles configurées dans la liste [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Si vous activez cette stratégie ou si vous ne la configurez pas (paramètre par défaut), l’utilisateur est interrogé pour l’accès à la capture audio, à l’exception des URL figurant dans la liste [AudioCaptureAllowedUrls](#audiocaptureallowedurls). Les URL répertoriées bénéficient d’un accès instantané.

Si vous désactivez cette stratégie, l’utilisateur n’est pas interrogé et la capture audio est accessible uniquement aux URL configurées dans [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Cette stratégie affecte tous les types d’entrées audio, et pas seulement le microphone intégré.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AudioCaptureAllowed
  - Nom de la stratégie de groupe: autoriser ou bloquer la capture de sons
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AudioCaptureAllowed
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AudioCaptureAllowed
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AudioCaptureAllowedUrls
  #### Sites autorisés à accéder aux appareils de capture audio sans autorisation préalable
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifiez les sites web, basés sur des formats d’URL, qui peuvent utiliser les appareils de capture audio sans autorisation préalable de la part de l’utilisateur. Les modèles de cette liste sont comparés à la source de sécurité de l’URL à l’origine de la demande. En cas de correspondance, l’accès aux appareils de capture audio est autorisé automatiquement. 

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AudioCaptureAllowedUrls
  - Nom de la stratégie de groupe: sites autorisés à accéder aux appareils de capture audio sans autorisation préalable
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AudioCaptureAllowedUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AudioSandboxEnabled
  #### Autoriser l’exécution du bac à sable audio
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version81 ou versions ultérieures

  #### Description
  Cette stratégie contrôle le bac à sable du processus audio.

Si vous activez cette stratégie, le processus audio s’exécute en mode bac à sable.

Si vous désactivez cette stratégie, le processus audio ne s’exécute pas en mode bac à sable, et le module de traitement audio WebRTC s’exécute lors du processus du convertisseur.
Cela expose les utilisateurs aux risques de sécurité liés à l’exécution du sous-système audio sans bac à sable.

Si vous ne configurez pas cette stratégie, la configuration par défaut pour le bac à sable audio est utilisée, ce qui peut varier en fonction de la plateforme.

Cette stratégie est destinée à offrir aux entreprises de la souplesse pour désactiver le bac à sable audio, s’ils utilisent des configurations de logiciels de sécurité qui interfèrent avec ce dernier.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AudioSandboxEnabled
  - Nom de la stratégie de groupe: autoriser l’exécution du bac à sable audio
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AudioSandboxEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AudioSandboxEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AutoImportAtFirstRun
  #### Importer automatiquement les données et les paramètres d’un autre navigateur lors de la première exécution
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Si vous activez cette stratégie, tous les types de données et paramètres pris en charge par le navigateur spécifié seront importés de façon silencieuse et automatique lors de la première exécution. Lors de la première exécution, la section d’importation est également ignorée.

Les données du navigateur de l’ancienne version de MicrosoftEdge sont toujours migrées silencieusement lors de la première exécution, quelle que soit la valeur de cette stratégie.

Si cette stratégie est définie sur « FromDefaultBrowser », les types de données correspondant au navigateur par défaut sur l’appareil géré sont importés.

Si le navigateur spécifié en tant que valeur de cette stratégie n’est pas présent dans l’appareil géré, MicrosoftEdge ignore simplement l’importation sans notification à l’utilisateur.

Si vous définissez cette stratégie sur «DisabledAutoImport», la section d’importation de l’expérience de première exécution est ignorée entièrement et MicrosoftEdge n’importe pas automatiquement les données et les paramètres du navigateur. 

Si cette stratégie est définie sur « FromInternetExplorer », les types de données suivants sont importés à partir d’Internet Explorer:
1. Favoris ou marque-pages
2. Mots de passe enregistrés
3. Moteurs de recherche
4. Historique de navigation
5. Page d’accueil

Si cette stratégie est définie sur « FromGoogleChrome », les types de données suivants sont importés à partir de Google Chrome:
1. Favoris
2. Mots de passe enregistrés
3. Adresses et bien plus
4. Informations de paiement
5. Historique de navigation
6. Paramètres
7. Onglets épinglés et ouverts
8. Extensions
9. Cookies

Remarque: si vous souhaitez obtenir plus d’informations sur les éléments importés à partir de Google Chrome, consultez [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835)

Si cette stratégie est définie sur « FromSafari », les données de l’utilisateur ne sont plus importées dans Microsoft Edge. Ceci est dû à la façon dont l’accès au disque complet fonctionne sur Mac.
Sur macOS Mojave et versions ultérieures, il n’est plus possible d’importer des données Safari de façon automatisée et autonome dans Microsoft Edge.

À partir de la version83 de MicrosoftEdge, si cette stratégie est définie sur « FromMozillaFirefox », les types de données suivants sont importés à partir de MozillaFirefox:
1. Favoris ou marque-pages
2. Mots de passe enregistrés
3. Adresses et bien plus
4. Historique de navigation

Si vous souhaitez limiter l’importation de types de données spécifiques sur les appareils gérés, vous pouvez utiliser cette stratégie avec d’autres stratégies, comme [ImportAutofillFormData](#importautofillformdata), [ImportBrowserSettings](#importbrowsersettings), [ImportFavorites](#importfavorites), etc.

Mappage des options de stratégie:

* FromDefaultBrowser (0) =Importer automatiquement tous les types de données et paramètres pris en charge à partir du navigateur par défaut

* FromInternetExplorer (1)=Importer automatiquement tous les types de données et paramètres pris en charge à partir d’InternetExplorer

* FromGoogleChrome (2)=Importer automatiquement tous les types de données et paramètres pris en charge à partir de GoogleChrome

* FromSafari (3)=Importer automatiquement tous les types de données et paramètres pris en charge à partir de Safari

* DisabledAutoImport (4)=Désactiver l’importation automatique et la section d’importation de l’expérience de première exécution est ignorée

* FromMozillaFirefox (5)=Importer automatiquement tous les types de données et paramètres pris en charge à partir de MozillaFirefox

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AutoImportAtFirstRun
  - Nom de la stratégie de groupe: importer automatiquement les données et les paramètres d’un autre navigateur lors de la première exécution
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AutoImportAtFirstRun
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AutoImportAtFirstRun
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AutoLaunchProtocolsFromOrigins
  #### Définir une liste de protocoles qui peuvent lancer une application externe à partir d’origines, sans inviter l’utilisateur
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version85 ou versions ultérieures

  #### Description
  Vous permet de créer une liste de protocoles et, pour chaque protocole, une liste associée de modèles d’origine autorisée, qui peut lancer une application externe sans inviter l’utilisateur. Le séparateur de fin ne doit pas être inclus lorsque vous répertoriez le protocole. Par exemple, la liste «Skype» au lieu de «Skype:» ou «skype://».

Si vous configurez cette stratégie, un protocole est uniquement autorisé à lancer une application externe sans qu’une invite soit demandée par la stratégie si:

- le protocole est répertorié

- l’origine du site qui tente de lancer le protocole correspond à l’un des modèles d’origine dans la liste de allowed_origins du protocole.

Si l’une ou l’autre condition est fausse, l’invite de lancement de protocole externe ne sera pas omise par une stratégie.

Si vous ne configurez pas cette stratégie, vous ne pouvez pas lancer d’autres protocoles sans invite de commandes. Les utilisateurs peuvent désactiver les invites sur une base par protocole ou par site, sauf si la stratégie de [ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) est désactivée. Cette stratégie n’a aucun impact sur les exemptions d’invite par protocole ou par site définis par les utilisateurs.

Les modèles de correspondance d’origine utilisent un format similaire à celui de la stratégie de [URLBlocklist](#urlblocklist), documentée dans [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Toutefois, les modèles de correspondance d’origine pour cette stratégie ne peuvent pas contenir d’éléments "/path" ou "@query". Tout modèle contenant un élément "/path" ou "@query" sera ignoré.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Dictionary

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: AutoLaunchProtocolsFromOrigins
  - Nom de la stratégie de protection: définissez une liste de protocoles qui peuvent lancer une application externe à partir d’origines, sans inviter l’utilisateur
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AutoLaunchProtocolsFromOrigins
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\AutoLaunchProtocolsFromOrigins = [
  {
    "allowed_origins": [
      "example.com", 
      "http://www.example.com:8080"
    ], 
    "protocol": "spotify"
  }, 
  {
    "allowed_origins": [
      "https://example.com", 
      "https://.mail.example.com"
    ], 
    "protocol": "teams"
  }, 
  {
    "allowed_origins": [
      "*"
    ], 
    "protocol": "outlook"
  }
]
```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: AutoLaunchProtocolsFromOrigins
  - Exemple de valeur:
``` xml
<key>AutoLaunchProtocolsFromOrigins</key>
<array>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>example.com</string>
      <string>http://www.example.com:8080</string>
    </array>
    <key>protocol</key>
    <string>spotify</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>https://example.com</string>
      <string>https://.mail.example.com</string>
    </array>
    <key>protocol</key>
    <string>teams</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>*</string>
    </array>
    <key>protocol</key>
    <string>outlook</string>
  </dict>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AutoOpenAllowedForURLs
  #### URL où AutoOpenFileTypes peut s’appliquer
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version85 ou versions ultérieures

  #### Description
  Liste d’URL auxquelles [AutoOpenFileTypes](#autoopenfiletypes) s’applique. Cette stratégie n’a aucun impact sur les valeurs ouvertes automatiquement définies par les utilisateurs via l’étagère de téléchargement... > Entrée de menu «toujours ouvrir les fichiers de ce type».

Si vous configurez des URL dans cette stratégie, les fichiers s’ouvrent automatiquement uniquement par stratégie si l’URL fait partie de ce groupe et le type de fichier est répertorié dans [AutoOpenFileTypes](#autoopenfiletypes). Si l’une ou l’autre condition est fausse, le téléchargement ne s’ouvre pas automatiquement par stratégie.

Si vous ne configurez pas cette stratégie, tous les téléchargements où se trouve le type de fichier dans [AutoOpenFileTypes](#autoopenfiletypes) s’ouvrent automatiquement.

Un modèle d’URL doit être mis en forme en fonction de [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: AutoOpenAllowedForURLs
  - Nom de la stratégie de protection: URL où AutoOpenFileTypes peut s’appliquer
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: AutoOpenAllowedForURLs
  - Exemple de valeur:
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AutoOpenFileTypes
  #### Liste des types de fichiers qui doivent être automatiquement ouverts au téléchargement
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version85 ou versions ultérieures

  #### Description
  Cette stratégie définit la liste des types de fichiers qui doivent être automatiquement ouverts lors du téléchargement. Remarque: le séparateur principal ne doit pas être inclus lorsque vous répertoriez le type de fichier. par conséquent, il vous suffit de répertorier «txt» au lieu de «. txt».

Par défaut, ces types de fichiers sont automatiquement ouverts sur toutes les URL. Vous pouvez utiliser la stratégie de [AutoOpenAllowedForURLs](#autoopenallowedforurls) pour restreindre les URL pour lesquelles ces types de fichiers seront ouverts automatiquement.

Les fichiers dont le type doit être ouvert automatiquement restent soumis aux vérifications Microsoft Defender SmartScreen activées et ne s’ouvrent pas s’ils ne fonctionnent pas.

Les types de fichiers qu’un utilisateur a déjà spécifié pour s’ouvrir automatiquement continueront à le faire lors du téléchargement. L’utilisateur continuera à pouvoir spécifier d’autres types de fichiers à ouvrir automatiquement.

Si vous ne configurez pas cette stratégie, seuls les types de fichiers qu’un utilisateur a déjà spécifié pour s’ouvrir automatiquement le sont lors du téléchargement.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: AutoOpenFileTypes
  - Nom de la stratégie de protection: liste des types de fichiers qui doivent être automatiquement ouverts lors du téléchargement
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: AutoOpenFileTypes
  - Exemple de valeur:
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AutofillAddressEnabled
  #### Activer la saisie automatique pour les adresses
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Active la fonctionnalité de saisie automatique, qui permet à l’utilisateur de remplir automatiquement des formulaires web à partir de données stockées précédemment, telles que des informations relatives à son adresse.

Si cette stratégie est désactivé, ces informations ne sont jamais suggérées ni saisies automatiquement. De même, les informations complémentaires relatives à l’adresse que l’utilisateur est susceptible de fournir sur une page web ne sont pas enregistrées.

Si cette stratégie est activée ou si elle n’est pas configurée, les utilisateurs peuvent contrôler la saisie automatique pour les adresses dans l’interface utilisateur.

Si vous désactivez cette stratégie, vous arrêtez également toutes les activités pour tous les formulaires web, à l’exception des formulaires de paiement et de mot de passe. Aucune autre entrée n’est enregistrée. MicrosoftEdge ne suggère ni ne remplit automatiquement aucune entrée précédente.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AutofillAddressEnabled
  - Nom de la stratégie de groupe: activer la saisie automatique pour les adresses
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: AutofillAddressEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AutofillAddressEnabled
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AutofillCreditCardEnabled
  #### Activer la saisie automatique pour les cartes de crédit
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Active la fonctionnalité de saisie automatique de MicrosoftEdge, qui permet à l’utilisateur de remplir automatiquement des formulaires web à partir de données stockées précédemment, telles que des informations relatives aux cartes de crédit.

Si cette stratégie est désactivé, ces informations ne sont jamais suggérées ni saisies automatiquement. De même, les informations complémentaires relatives aux cartes de crédit que l’utilisateur est susceptible de fournir sur une page web ne sont pas enregistrées.

Si vous activez cette stratégie ou ne la configurez pas, les utilisateurs contrôlent la fonctionnalité de saisie automatique pour les cartes de crédit.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AutofillCreditCardEnabled
  - Nom de la stratégie de groupe: activer la saisie automatique pour les cartes de crédit
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: AutofillCreditCardEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AutofillCreditCardEnabled
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### AutoplayAllowed
  #### Autoriser la lecture automatique de média pour les sites web
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version78 ou versions ultérieures

  #### Description
  Cette stratégie définit la stratégie de lecture automatique des médias pour les sites web.

Le paramètre par défaut, «Non configuré», respecte les paramètres actuels de lecture automatique des médias et permet aux utilisateurs de configurer leurs paramètres de lecture automatique.

Le paramètre «Activé» définit la lecture automatique des médias sur «Autoriser».  Tous les sites web sont autorisés à effectuer la lecture automatique des médias. Les utilisateurs ne peuvent pas remplacer cette stratégie.

Le paramètre «Désactivé» définit la lecture automatique des médias sur «Bloquer».  Aucun site web n’est autorisé à effectuer la lecture automatique des médias. Les utilisateurs ne peuvent pas remplacer cette stratégie.

Un onglet doit être fermé et rouvert pour que cette stratégie soit appliquée.


  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: AutoplayAllowed
  - Nom de la stratégie de groupe: autoriser la lecture automatique de média pour les sites web
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: AutoplayAllowed
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: AutoplayAllowed
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### BackgroundModeEnabled
  #### Poursuivre l’exécution des applications en arrière-plan après la fermeture de MicrosoftEdge
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version77 ou versions ultérieures

  #### Description
  Autorise un processus de MicrosoftEdge à démarrer lors de la connexion au système d’exploitation et à rester ouvert jusqu’à la fermeture de la dernière fenêtre du navigateur. Dans ce cas, les applications en arrière-plan et la session de navigation en cours restent actives, ainsi que les cookies de la session. Le processus exécuté en arrière-plan affiche une icône dans la barre d’état système et peut être fermé à tout moment à partir de cet emplacement.

Si vous activez cette stratégie, le mode arrière-plan est activé.

Si vous désactivez cette stratégie, le mode arrière-plan est désactivé.

Si vous ne configurez pas cette stratégie, le mode arrière-plan est désactivé initialement et peut être contrôlé par l’utilisateur dans edge://settings/system.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: BackgroundModeEnabled
  - Nom de la stratégie de groupe: poursuivre l’exécution des applications en arrière-plan après la fermeture de MicrosoftEdge
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: BackgroundModeEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)

  ### BackgroundTemplateListUpdatesEnabled
  #### Active les mises à jour en arrière-plan dans la liste des modèles disponibles pour Collections et d’autres fonctionnalités qui utilisent des modèles
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version79 ou versions ultérieures

  #### Description
  Vous permet d’activer ou de désactiver les mises à jour en arrière-plan pour la liste des modèles disponibles pour les collections et d’autres fonctionnalités qui utilisent des modèles.  Les modèles permettent d’extraire les métadonnées enrichies d’une page web lorsque la page est enregistrée dans une collection.

Si vous activez ce paramètre ou si celui-ci n’est pas configuré, la liste des modèles disponibles est téléchargée en arrière-plan à partir d’un service Microsoft toutes les 24heures.

Si vous désactivez ce paramètre, la liste des modèles disponibles est téléchargée à la demande. Ce type de téléchargement peut entraîner de légères altérations des performances pour les collections et d’autres fonctionnalités.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: BackgroundTemplateListUpdatesEnabled
  - Nom de la stratégie de groupe: active les mises à jour en arrière-plan dans la liste des modèles disponibles pour Collections et d’autres fonctionnalités qui utilisent des modèles
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: BackgroundTemplateListUpdatesEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: BackgroundTemplateListUpdatesEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### BingAdsSuppression
  #### Bloquer toutes les annonces dans les résultats de recherche Bing
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version83 ou versions ultérieures

  #### Description
  Permet une expérience de recherche sans publicité sur Bing.com

Si vous activez cette stratégie, un utilisateur peut effectuer une recherche sur bing.com et bénéficier d’une expérience de recherche sans publicité. En même temps, le paramètre Filtre adulte est défini sur «strict» et ne peut pas être modifié par l’utilisateur.

Si vous ne configurez pas cette stratégie, l’expérience par défaut affiche les publicités dans les résultats de la recherche sur bing.com. Le Filtre adulte est défini sur «Modéré» par défaut et pourra être modifié par l’utilisateur.

Cette stratégie est disponible uniquement pour les références SKUK-12 qui sont identifiées comme clients EDU par Microsoft.

Si vous souhaitez en apprendre plus sur cette stratégie ou si ces cas s’appliquent à votre situation, consultez [https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711):

* Vous avez un client EDU, mais la stratégie ne fonctionne pas.

* Votre adresse IP a été ajoutée à la liste verte pour une expérience de recherche sans publicité.

* Vous connaissez une expérience de recherche sans publicités sur l’ancienne version de Microsoft Edge et vous souhaitez effectuer la mise à jour vers la nouvelle version de MicrosoftEdge.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: BingAdsSuppression
  - Nom de la stratégie de groupe: bloquer toutes les annonces dans les résultats de recherche Bing
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: BingAdsSuppression
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: BingAdsSuppression
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### BlockThirdPartyCookies
  #### Bloquer les cookies tiers
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Empêchez les éléments d’une page web, qui ne proviennent pas du domaine figurant dans la barre d’adresses, de définir les cookies.

Si vous activez cette stratégie, les éléments d’une page web, qui ne proviennent pas du domaine figurant dans la barre d’adresses, ne peuvent pas configurer les cookies

Si vous désactivez cette stratégie, les éléments d’une page web, qui proviennent de domaines autres que la barre d’adresses, peuvent spécifier des cookies.

Si vous ne configurez pas cette stratégie, les cookies tiers sont activés, mais les utilisateurs peuvent modifier ce paramètre.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: BlockThirdPartyCookies
  - Nom de la stratégie de groupe: bloquer les cookies tiers
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: BlockThirdPartyCookies
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: BlockThirdPartyCookies
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### BrowserAddProfileEnabled
  #### Activer la création de profil à partir du menu déroulant Identité ou de la page Paramètres
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet aux utilisateurs de créer des profils à l’aide de l’option **Ajouter un profil**.
Si vous activez cette stratégie ou ne la configurez pas, MicrosoftEdge autorise les utilisateurs à utiliser **Ajouter un profil** dans le menu déroulant Identité ou sur la page Paramètres pour créer des profils.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas ajouter de nouveaux profils à partir du menu déroulant Identité ou de la page Paramètres.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: BrowserAddProfileEnabled
  - Nom de la stratégie de groupe: activer la création de profil à partir du menu déroulant Identité ou de la page Paramètres
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: BrowserAddProfileEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: BrowserAddProfileEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### BrowserGuestModeEnabled
  #### Activer le mode Invité
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Activez l’option permettant d’utiliser les profils invités dans MicrosoftEdge. Dans un profil invité, le navigateur n’importe pas les données de navigation à partir de profils existants et supprime les données de navigation lorsque tous les profils invités sont fermés.

Si vous activez cette stratégie ou si vous ne la configurez pas, MicrosoftEdge permet aux utilisateurs de parcourir les profils invités.

Si vous désactivez cette stratégie, MicrosoftEdge ne permet pas aux utilisateurs de parcourir les profils invités.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: BrowserGuestModeEnabled
  - Nom de la stratégie de groupe: activer le mode Invité
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: BrowserGuestModeEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: BrowserGuestModeEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### BrowserNetworkTimeQueriesEnabled
  #### Autoriser l’envoi de requêtes à un service horaire du navigateur
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Empêche MicrosoftEdge d’envoyer occasionnellement des requêtes à un service horaire du navigateur afin de récupérer un horodatage précis.

Si vous désactivez cette stratégie, MicrosoftEdge cesse d’envoyer des requêtes à un service horaire du navigateur.

Si vous activez cette stratégie ou si vous ne la configurez pas, MicrosoftEdge enverra parfois des requêtes à un service horaire du navigateur.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: BrowserNetworkTimeQueriesEnabled
  - Nom de la stratégie de groupe: autoriser l’envoi de requêtes à un service horaire du navigateur
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: BrowserNetworkTimeQueriesEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: BrowserNetworkTimeQueriesEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### BrowserSignin
  #### Paramètres de connexion du navigateur
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifiez si un utilisateur peut se connecter à MicrosoftEdge avec son compte et utiliser les services liés au compte, tels que la synchronisation et l’authentification unique. Pour contrôler la disponibilité de la synchronisation, utilisez plutôt la stratégie [SyncDisabled](#syncdisabled). 

Si vous définissez cette stratégie sur «Disable», veillez à également désactiver la stratégie [NonRemovableProfileEnabled](#nonremovableprofileenabled), car [NonRemovableProfileEnabled](#nonremovableprofileenabled) désactive la création d’un profil de navigateur automatiquement connecté. Si les deux stratégies sont définies, MicrosoftEdge utilise la stratégie «Désactiver la connexion au navigateur» et se comporte comme si [NonRemovableProfileEnabled](#nonremovableprofileenabled) était désactivée. 

Si vous définissez cette stratégie sur «Enable», les utilisateurs peuvent se connecter au navigateur. La connexion au navigateur ne signifie pas que la synchronisation est activée par défaut. L’utilisateur doit accepter séparément l’utilisation de cette fonctionnalité.

Si vous définissez cette stratégie sur «Force», les utilisateurs doivent se connecter à un profil pour utiliser le navigateur. Par défaut, cela permet à l’utilisateur de choisir s’il veut synchroniser son compte, sauf si la synchronisation est désactivée par l’administrateur de domaine ou avec la stratégie [SyncDisabled](#syncdisabled). La valeur par défaut de la stratégie [BrowserGuestModeEnabled](#browserguestmodeenabled) est définie sur false.

Si vous ne configurez pas cette stratégie, les utilisateurs peuvent décider s’ils souhaitent activer l’option de connexion au navigateur et l’utiliser au mieux.

Mappage des options de stratégie:

* Disable 0=Désactiver la connexion au navigateur

* Enable (1)=Activer la connexion au navigateur

* Force (2)=Forcer les utilisateurs à se connecter pour utiliser le navigateur

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: BrowserSignin
  - Nom de la stratégie de groupe: paramètres de connexion du navigateur
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: BrowserSignin
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: BrowserSignin
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### BuiltInDnsClientEnabled
  #### Utiliser le client DNS intégré
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Détermine si le client DNS intégré doit être utilisé.

Cette règle n’a aucune incidence sur les serveurs DNS utilisés, mais uniquement sur la pile logicielle utilisée pour communiquer avec eux. Par exemple, si le système d’exploitation est configuré pour utiliser un serveur DNS d’entreprise, ce même serveur sera utilisé par le client DNS intégré. Il est toutefois possible que le client DNS intégré gère les serveurs de différentes manières en utilisant des protocoles liés aux DNS plus modernes tels que DNS-over-TLS. 

Si vous activez cette stratégie, le client DNS intégré est utilisé, si disponible.

Si vous désactivez cette stratégie, le client n’est jamais utilisé.

Si vous ne configurez pas cette stratégie, le client DNS intégré est activé par défaut sur Mac OS, et les utilisateurs peuvent choisir si le client DNS intégré doit être utilisé ou non, en modifiant edge://flags, ou à l’aide d’un indicateur de ligne de commande.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: BuiltInDnsClientEnabled
  - Nom de la stratégie de groupe: utiliser le client DNS intégré
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: BuiltInDnsClientEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: BuiltInDnsClientEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### BuiltinCertificateVerifierEnabled
  #### Indique si le vérificateur de certificats intégré est utilisé pour la vérification des certificats de serveur (déconseillé)
  >DÉCONSEILLÉ: cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge:
  - sur macOS depuis la version83 ou versions ultérieures

  #### Description
  Cette stratégie est déconseillée, car elle a pour but de servir uniquement comme mécanisme à court terme afin d’offrir aux entreprises davantage de temps pour mettre à jour leurs environnements et signaler les problèmes s’ils sont détectés comme incompatibles avec le vérificateur de certificat intégré.

Il ne fonctionne pas dans Microsoft Edge version 87, lorsque la prise en charge du vérificateur de certificats hérité sur Mac OS X est prévue pour être supprimée.


  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  

  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: BuiltinCertificateVerifierEnabled
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForCas
  #### Désactiver l’application des règles de transparence des certificats pour une liste de hachages subjectPublicKeyInfo
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Désactive l’application des exigences de transparence du certificat pour obtenir la liste des hachages subjectPublicKeyInfo.

Cette stratégie vous permet de désactiver les exigences de divulgation de transparence de certificat pour les chaînes de certificat qui contiennent des certificats avec l’un des hachages subjectPublicKeyInfo spécifiés. Cela autorise les certificats qui ne seraient pas approuvés dans le cas contraire, car ils n’ont pas été correctement divulgués publiquement, de continuer à être utilisés pour les hôtes Entreprise.

Pour désactiver l’application de la transparence du certificat lorsque cette stratégie est définie, l’un des ensembles de conditions suivants doit être rempli:
1. Le hachage est celui de subjectPublicKeyInfo du certificat serveur. 
2. Le hachage est celui d’un subjectPublicKeyInfo qui s’affiche dans un certificat d’autorité de certification dans la chaîne de certificats, que le certificat d’autorité de certification est limité via l’extension nameConstraints X.509v3, au moins un nameConstraints est présent dans le permittedSubtrees et le directoryName contient un attribut organizationName. 
3. Le hachage est celui d’un subjectPublicKeyInfo qui s’affiche dans un certificat d’autorité de certification dans la chaîne de certificats, que le certificat d’autorité de certification a au moins un attribut organizationName dans le sujet du certificat et le certificat du serveur contient le même nombre d’attributs organizationName, dans le même ordre et avec des valeurs identiques (octet pour octet).

Un hachage subjectPublicKeyInfo est spécifié par la concaténation du nom d’algorithme de hachage, le caractère «/» et l’encodage Base64 de cet algorithme de hachage appliqué à la subjectPublicKeyInfo codée DER du certificat spécifié. Cet encodage Base64 est le même format qu’une empreinte digitale SPKI, telle que définie dans la RFC 7469, section 2.4. Les algorithmes de hachage non reconnus sont ignorés. Le seul algorithme de hachage pris en charge pour l’instant est «sha256».

Si vous désactivez ou ne configurez pas cette stratégie, tous les certificats obligatoires pour être divulgués via la transparence des certificats sont considérés comme non approuvés s’ils ne sont pas transmis conformément à la stratégie de transparence du certificat.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: CertificateTransparencyEnforcementDisabledForCas
  - Nom de la stratégie de groupe: désactiver l’application des règles de transparence des certificats pour une liste de hachages subjectPublicKeyInfo
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: CertificateTransparencyEnforcementDisabledForCas
  - Exemple de valeur:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas
  #### Désactiver l’application des règles de transparence des certificats pour une liste d’autorités de certification héritées
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Désactive l’application des exigences de transparence de certificat pour une liste d’autorités de certification (AC) héritées.

Cette stratégie vous permet de désactiver les exigences de divulgation de transparence de certificat pour les chaînes de certificat qui contiennent des certificats avec l’un des hachages subjectPublicKeyInfo spécifiés. Cela autorise les certificats qui ne seraient pas approuvés dans le cas contraire, car ils n’ont pas été correctement divulgués publiquement, d’être utilisés pour les hôtes Entreprise.

Pour pouvoir désactiver l’application de la transparence de certificat, vous devez définir le hachage sur un subjectPublicKeyInfo apparaissant dans un certificat d’autorité de certification qui n’est reconnu comme une autorité de certification (AC) héritée. Une autorité de certification héritée est une autorité de certification qui a été approuvée publiquement par défaut, par un ou plusieurs systèmes d’exploitation pris en charge par MicrosoftEdge.

Vous spécifiez un hachage subjectPublicKeyInfo par la concaténation du nom d’algorithme de hachage, le caractère «/» et l’encodage Base64 de cet algorithme de hachage appliqué à la subjectPublicKeyInfo codée DER du certificat spécifié. Cet encodage Base64 est le même format qu’une empreinte digitale SPKI, telle que définie dans la RFC 7469, section 2.4. Les algorithmes de hachage non reconnus sont ignorés. Le seul algorithme de hachage pris en charge pour l’instant est «sha256».

Si vous ne configurez pas cette stratégie, tous les certificats obligatoires pour être divulgués via la transparence des certificats sont considérés comme non approuvés s’ils ne sont pas transmis conformément à la stratégie de transparence du certificat.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Nom de la stratégie de groupe: désactiver l’application des règles de transparence des certificats pour une liste d’autorités de certification héritées
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Exemple de valeur:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForUrls
  #### Désactiver l’application des règles de transparence des certificats pour des URL spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Désactive l’application des règles de transparence des certificats pour les URL répertoriées.

Cette règle autorise à ne pas communiquer les certificats associés aux noms d’hôte dans la liste d’URL répertoriées via les règles de transparence des certificats. Cela vous permet d’utiliser des certificats qui, autrement, ne seraient pas fiables, car ils n’ont pas été correctement divulgués publiquement, mais il est plus difficile de détecter les certificats émis incorrectement pour ces hôtes.

Le format d’un modèle d’URL doit être conforme aux règles stipulées à l’adresse [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Comme les certificats sont valides pour un nom d’hôte donné, indépendamment du schéma, du port ou du chemin d’accès, seule la partie du nom d’hôte de l’URL est prise en compte. Les caractères génériques ne sont pas pris en charge.

Si vous ne configurez pas cette stratégie, tout certificat qui doit être communiqué tel que le prévoient les règles de transparence des certificats est considéré comme n’étant pas fiable s’il n’est pas communiqué comme il se doit.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: CertificateTransparencyEnforcementDisabledForUrls
  - Nom de la stratégie de groupe: désactiver l’application des règles de transparence des certificats pour des URL spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: CertificateTransparencyEnforcementDisabledForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ClearBrowsingDataOnExit
  #### Effacer les données de navigation lors de la fermeture de MicrosoftEdge
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version78 ou versions ultérieures

  #### Description
  MicrosoftEdge n’efface pas les données de navigation par défaut lors de sa fermeture. Les données de navigation incluent les informations entrées dans les formulaires, les mots de passe et même les sites web visités.

Si vous activez cette stratégie, toutes les données de navigation sont supprimées à chaque fermeture de MicrosoftEdge. Si vous activez cette stratégie, elle prévaut sur la configuration de [DefaultCookiesSetting](#defaultcookiessetting)

Si vous désactivez ou ne configurez pas cette stratégie, les utilisateurs peuvent configurer l’option Effacer les données de navigation dans les Paramètres.

Si vous activez cette stratégie, ne configurez pas la stratégie [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) ou la stratégie [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit), car elles traitent toutes la suppression de données de navigation. Si vous configurez les stratégies précédentes et cette stratégie, toutes les données de navigation sont supprimées à la fermeture de MicrosoftEdge, quelle que soit la façon dont vous avez configuré [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) ou [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

Pour exclure la suppression des cookies lors de la fermeture, configurez la stratégie de [SaveCookiesOnExit](#savecookiesonexit).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ClearBrowsingDataOnExit
  - Nom de la stratégie de groupe: effacer les données de navigation lors de la fermeture de MicrosoftEdge
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ClearBrowsingDataOnExit
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ClearBrowsingDataOnExit
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ClearCachedImagesAndFilesOnExit
  #### Effacer les images et les fichiers mis en cache lors de la fermeture de MicrosoftEdge
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version83 ou versions ultérieures

  #### Description
  MicrosoftEdge ne supprime pas les images et les fichiers mis en cache par défaut lors de sa fermeture.

Si vous activez cette stratégie, les images et les fichiers mis en cache sont supprimées à chaque fermeture de MicrosoftEdge.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas configurer l’option images et fichiers mis en cache dans edge://settings/clearBrowsingDataOnClose.

Si vous ne configurez pas cette stratégie, les utilisateurs peuvent choisir si les images et les fichiers mis en cache sont supprimés à la fermeture.

Si vous désactivez cette stratégie, n’activez pas la stratégie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), car elles traitent toutes deux la suppression de données. Si vous activez les deux stratégies, la stratégie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) prévaut et supprime toutes les données lors de la fermeture de MicrosoftEdge, quelle que soit la configuration de la stratégie [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ClearCachedImagesAndFilesOnExit
  - Nom de la stratégie de groupe: effacer les images et les fichiers mis en cache lors de la fermeture de MicrosoftEdge
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ClearCachedImagesAndFilesOnExit
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ClearCachedImagesAndFilesOnExit
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ClickOnceEnabled
  #### Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole ClickOnce
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version78 ou versions ultérieures

  #### Description
  Autorisez les utilisateurs à ouvrir des fichiers à l’aide du protocole ClickOnce. Le protocole ClickOnce permet aux sites web de demander au navigateur d’ouvrir les fichiers d’une URL spécifique à l’aide du gestionnaire de fichiers ClickOnce sur lordinateur ou l’appareil de l’utilisateur.

Si vous activez cette stratégie, les utilisateurs peuvent ouvrir des fichiers à l’aide du protocole ClickOnce. Cette stratégie remplace le paramètre ClickOnce de l'utilisateur sur la page edge://flags/.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas ouvrir de fichiers à l’aide du protocole ClickOnce. Au lieu de cela, le fichier est enregistré dans le système de fichiers utilisant le navigateur. Cette stratégie remplace le paramètre ClickOnce de l'utilisateur sur la page edge://flags/.

Si vous ne configurez pas cette stratégie, les utilisateurs disposant de Microsoft Edge dont la version précède Microsoft Edge 87 ne peuvent pas ouvrir les fichiers à l’aide du protocole ClickOnce par défaut. Les utilisateurs ont cependant la possibilité d’activer l’utilisation du protocole ClickOnce avec la page edge://flags/. Les utilisateurs de Microsoft Edge version 87 et ultérieures peuvent ouvrir les fichiers à l’aide du protocole ClickOnce par défaut, mais ont la possibilité de désactiver le protocole ClickOnce depuis la page edge://flags/.

La désactivation de ClickOnce peut empêcher le lancement correct des applications ClickOnce (fichiers .application).

Si vous souhaitez en savoir plus sur ClickOnce, consultez [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) et [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ClickOnceEnabled
  - Nom de la stratégie de groupe: autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole ClickOnce
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ClickOnceEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  

  [Retour au début](#microsoft-edge---policies)

  ### CollectionsServicesAndExportsBlockList
  #### Bloquer l’accès à une liste spécifiée de services et de cibles d’exportations dans Collections
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Lister les services et les cibles d’exportation spécifiques auxquels les utilisateurs ne peuvent pas accéder dans la fonctionnalité Collections de Microsoft Edge. Cela inclut l’affichage de données supplémentaires de Bing et l’exportation de collections vers des produits Microsoft ou des partenaires externes.

Si vous activez cette stratégie, les services et les cibles d’exportation qui correspondent à la liste donnée sont bloqués.

Si cette stratégie n’est pas configurée, aucune restriction n’est imposée concernant les services et cibles d’exportation acceptables.

Mappage des options de stratégie:

* pinterest_suggestions (pinterest_suggestions) = Suggestions Pinterest

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP : CollectionsServicesAndExportsBlockList
  - Nom GP : Bloquer l’accès à une liste de services et de cibles d’exportation spécifiée dans Collections
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"

```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: CollectionsServicesAndExportsBlockList
  - Exemple de valeur:
``` xml
<array>
  <string>pinterest_suggestions</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### CommandLineFlagSecurityWarningsEnabled
  #### Activer les avertissements de sécurité pour les indicateurs de ligne de commande
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version78 ou versions ultérieures

  #### Description
  Si cette stratégie est désactivée, elle empêche l’apparition des avertissements de sécurité lorsque MicrosoftEdge est lancé avec des indicateurs de ligne de commande potentiellement dangereux.

Si elle est activée ou non configurée, les avertissements de sécurité s’affichent lorsque ces indicateurs de ligne de commande sont utilisés pour lancer MicrosoftEdge.

Par exemple, l’indicateur --disable-gpu-sandbox génère l’avertissement suivant: Vous utilisez un indicateur de ligne de commande non pris en charge: --disable-gpu-sandbox.  Cela expose à des risques de sécurité et de stabilité.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: CommandLineFlagSecurityWarningsEnabled
  - Nom de la stratégie de groupe: activer les avertissements de sécurité pour les indicateurs de ligne de commande
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: CommandLineFlagSecurityWarningsEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: CommandLineFlagSecurityWarningsEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ComponentUpdatesEnabled
  #### Activer les mises à jour des composants dans MicrosoftEdge
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Si vous activez ou ne configurez pas cette stratégie, les mises à jour des composants sont activées dans MicrosoftEdge.

Si vous désactivez cette stratégie ou si vous la configurez sur false, les mises à jour des composants sont désactivées pour tous les composants dans MicrosoftEdge.

Toutefois, certains composants ne sont pas soumis à cette stratégie. Cela inclut les composants sans code exécutable, qui n’affectent pas de façon significative le comportement du navigateur ou qui sont essentiels à la sécurité du navigateur.  Autrement dit, les mises à jour considérées comme «essentielles à la sécurité» sont tout de même appliquées, même si vous désactivez cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ComponentUpdatesEnabled
  - Nom de la stratégie de groupe: activer les mises à jour des composants dans MicrosoftEdge
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ComponentUpdatesEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ComponentUpdatesEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ConfigureDoNotTrack
  #### Configurer Ne pas me suivre
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifiez si des requêtes Ne pas me suivre doivent être envoyées aux sites web demandant des informations de suivi. Les requêtes Ne pas me suivre indiquent aux sites web que vous visitez que vous ne souhaitez pas que votre activité de navigation soit suivie. Par défaut, les requêtes Ne pas me suivre ne sont pas envoyées, mais les utilisateurs peuvent décider d’activer cette fonctionnalité et d’envoyer des demandes.

Si vous activez ce paramètre, des requêtes Ne pas me suivre sont toujours envoyées aux sites web demandant des informations de suivi.

Si vous désactivez cette stratégie, les requêtes ne sont jamais envoyées.

Si vous ne configurez pas la stratégie, les utilisateurs peuvent choisir d’envoyer ou non les requêtes.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ConfigureDoNotTrack
  - Nom de la stratégie de groupe: configurer Ne pas me suivre
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ConfigureDoNotTrack
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ConfigureDoNotTrack
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ConfigureOnPremisesAccountAutoSignIn
  #### Configurer la connexion automatique avec un compte de domaine Active Directory en l’absence de compte de domaine Azure AD
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version81 ou versions ultérieures

  #### Description
  Activez l’utilisation des comptes ActiveDirectory pour la connexion automatique si les ordinateurs de vos utilisateurs sont joints au domaine et si votre environnement n’est pas joint de façon hybride. Si vous souhaitez que les utilisateurs soient connectés automatiquement avec leur compte AzureActiveDirectory, créez une jonction AzureAD (consultez [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197) si vous souhaitez en savoir plus) ou une jonction hybride (consultez [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365) si vous souhaitez en savoir plus) pour votre environnement.

Si vous avez désactivé la stratégie [BrowserSignin](#browsersignin), celle-ci n’a aucun effet.

Si vous activez cette stratégie et la définissez sur «SignInAndMakeDomainAccountNonRemovable», MicrosoftEdge connecte automatiquement les utilisateurs qui se trouvent sur des ordinateurs joints au domaine à l’aide de leur compte ActiveDirectory.

Si vous définissez cette stratégie sur « Disabled » ou ne la définissez pas, MicrosoftEdge ne connecte pas automatiquement les utilisateurs qui se trouvent sur des ordinateurs joints au domaine joint avec un compte Active Directory.

Mappage des options de stratégie:

* Disabled (0) = Désactivé

* SignInAndMakeDomainAccountNonRemovable (1) = Connecter et rendre le compte de domaine non supprimable

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ConfigureOnPremisesAccountAutoSignIn
  - Nom de la stratégie de groupe: configurer la connexion automatique avec un compte de domaine Active Directory en l’absence de compte de domaine Azure AD
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ConfigureOnPremisesAccountAutoSignIn
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  

  [Retour au début](#microsoft-edge---policies)

  ### ConfigureOnlineTextToSpeech
  #### Configurer la synthèse vocale en ligne
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez si le navigateur peut exploiter les polices vocales de la synthèse vocale en ligne, qui font partie des services cognitifs de Azure. Ces polices vocales sont de qualité supérieure à celle des polices vocales du système, qui sont déjà installées.

Si vous activez ou ne configurez pas cette stratégie, les applications web qui utilisent l’API SpeechSynthesis peuvent utiliser les polices vocales de la synthèse vocale en ligne.

Si vous désactivez cette stratégie, les polices vocales ne sont pas disponibles.

Si vous souhaitez en savoir plus sur cette fonctionnalité, consultez les articles: API SpeechSynthesis: [https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038) Services cognitifs: [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ConfigureOnlineTextToSpeech
  - Nom de la stratégie de groupe: configurer la conversion de texte par synthèse vocale en ligne
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ConfigureOnlineTextToSpeech
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ConfigureOnlineTextToSpeech
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ConfigureShare
  #### Configurer l’expérience de partage
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version83 ou versions ultérieures

  #### Description
  Si vous définissez cette stratégie sur « ShareAllowed » (valeur par défaut), les utilisateurs peuvent accéder à l’expérience de partage de Windows10 à partir des menus Paramètres et Plus dans MicrosoftEdge pour échanger avec d’autres applications sur le système.

Si vous définissez cette stratégie sur «ShareDisallowed», les utilisateurs ne peuvent pas accéder à l’expérience de partage de Windows10. Si le bouton Partager se trouve dans la barre d’outils, celui-ci est également masqué.

Mappage des options de stratégie:

* ShareAllowed (0)=Autoriser l’utilisation de l’expérience de partage

* ShareDisallowed (1)=Ne pas autoriser l’utilisation de l’expérience de partage

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ConfigureShare
  - Nom de la stratégie de groupe: configurer l’expérience de partage
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ConfigureShare
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)

  ### CustomHelpLink
  #### Spécifier le lien d’aide personnalisé
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version79 ou versions ultérieures

  #### Description
  Spécifiez un lien pour le menu Aide ou la touche F1.

Si vous activez cette stratégie, un administrateur peut spécifier un lien pour le menu Aide ou la touche F1.

Si vous désactivez ou ne configurez pas cette stratégie, le lien par défaut du menu Aide ou de la touche F1 est utilisé.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: CustomHelpLink
  - Nom de la stratégie de groupe: spécifier le lien d’aide personnalisé
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: CustomHelpLink
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: CustomHelpLink
  - Exemple de valeur:
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DNSInterceptionChecksEnabled
  #### Vérifications d’interception DNS activées
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Cette stratégie configure un commutateur local qui peut être utilisé pour désactiver les vérifications d’interception DNS. Ces vérifications essaient de déterminer si le navigateur se situe derrière un proxy qui redirige des noms d’hôtes inconnus.

Cette détection n’est peut-être pas nécessaire dans un environnement d’entreprise dans lequel la configuration réseau est connue. Elle peut être désactivée afin d’éviter tout trafic DNS et HTTP supplémentaire au démarrage et lors de chaque modification de la configuration DNS.

Si vous activez ou ne définissez pas cette stratégie, les vérifications d’interception DNS sont effectuées.

Si vous désactivez cette stratégie, les vérifications d’interception DNS ne sont pas effectuées.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DNSInterceptionChecksEnabled
  - Nom de la stratégie de groupe: vérifications d’interception DNS activées
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DNSInterceptionChecksEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DNSInterceptionChecksEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultBrowserSettingEnabled
  #### Définir MicrosoftEdge comme navigateur par défaut
  
  
  #### Versions prises en charge:
  - sur Windows7 et macOS depuis la version77 ou versions ultérieures

  #### Description
  Si vous attribuez la valeur true à cette stratégie, Microsoft Edge vérifie toujours qu’il s’agit du navigateur par défaut au démarrage et, si possible, s’inscrit automatiquement.

Si vous attribuez la valeur false à cette stratégie, Microsoft Edge cesse de vérifier si c’est la valeur par défaut et désactive les contrôles utilisateur pour cette option.

Si vous ne configurez pas cette stratégie, Microsoft Edge permet aux utilisateurs de contrôler s’il s’agit de la valeur par défaut. si ce n’est pas le cas, les notifications de l’utilisateur doivent s’afficher.

Remarque pour les administrateurs Windows: L’activation de cette stratégie ne fonctionne que pour les ordinateurs fonctionnant sous Windows7. Pour les versions ultérieures de Windows, vous devez déployer un fichier «associations d’applications par défaut» qui définit MicrosoftEdge comme gestionnaire des protocoles https et http (et, éventuellement, du protocole ftp et des formats de fichiers tels que .html, .htm, .pdf, .svg ou .webp). Si vous souhaitez en savoir plus, consultez [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultBrowserSettingEnabled
  - Nom de la stratégie de groupe: définir MicrosoftEdge comme navigateur par défaut
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultBrowserSettingEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultBrowserSettingEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultSearchProviderContextMenuAccessAllowed
  #### Autoriser l’accès au menu contextuel du moteur de recherche par défaut
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version85 ou versions ultérieures

  #### Description
  Active l’utilisation d’un moteur de recherche par défaut dans le menu contextuel.

Si vous désactivez cette stratégie, l’élément de recherche du menu contextuel qui dépend de votre moteur de recherche par défaut ainsi que de la barre latérale de recherche ne seront pas disponible.

Si cette stratégie est activée ou non définie, l’élément de recherche du menu contextuel qui dépend de votre moteur de recherche par défaut ainsi que de la barre latérale de recherche sont disponibles.

La valeur de la stratégie est uniquement prise en compte lorsque la stratégie [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) est activée, et ne l’est  pas dans le cas contraire.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP : DefaultSearchProviderContextMenuAccessAllowed
  - Nom GP : Autoriser l’accès au menu contextuel du moteur de recherche par défaut
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur : DefaultSearchProviderContextMenuAccessAllowed
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: DefaultSearchProviderContextMenuAccessAllowed
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultSensorsSetting
  #### Paramètre par défaut des capteurs
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Indiquer si les sites web peuvent accéder aux capteurs et utiliser les capteurs tels que les capteurs de mouvement et de luminosité. Vous pouvez bloquer ou autoriser complètement les sites web à accéder aux capteurs.

Définir la stratégie sur1 permet aux sites web d’accéder et d’utiliser des capteurs. Définir la stratégie sur2 refuse l’accès aux capteurs.

Vous pouvez remplacer cette stratégie pour des modèles d’URL spécifiques par les stratégies [SensorsAllowedForUrls](#sensorsallowedforurls) et [SensorsBlockedForUrls](#sensorsblockedforurls).

Si vous ne configurez pas cette stratégie, les sites web peuvent accéder et utiliser des capteurs, et les utilisateurs peuvent modifier ce paramètre. Il s’agit de la valeur par défaut globale pour [SensorsAllowedForUrls](#sensorsallowedforurls) et [SensorsBlockedForUrls](#sensorsblockedforurls).

Mappage des options de stratégie:

* AllowSensors (1) = autoriser les sites à accéder aux capteurs

* BlockSensors (2) = ne pas autoriser les sites à accéder aux capteurs

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultSensorsSetting
  - Nom de la stratégie de groupe: paramètre des capteurs par défaut
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultSensorsSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultSensorsSetting
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DefaultSerialGuardSetting
  #### Contrôler l’utilisation de l’API Serial
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Déterminer si les sites web peuvent accéder aux ports série. Vous pouvez bloquer complètement l’accès ou demander à l’utilisateur, chaque fois qu’un site web souhaite accéder à un port série.

Définir la stratégie sur3 permet aux sites web de demander l’accès aux ports série. Définir la stratégie sur2 refuse l’accès aux ports série.

Vous pouvez remplacer cette stratégie pour des modèles d’URL spécifiques par les stratégies [SerialAskForUrls](#serialaskforurls) et [SerialBlockedForUrls](#serialblockedforurls).

Si vous ne configurez pas cette stratégie, par défaut, les sites web peuvent demander aux utilisateurs s’ils peuvent accéder à un port série, et les utilisateurs peuvent modifier ce paramètre.

Mappage des options de stratégie:

* BlockSerial (2) = ne pas autoriser les sites à demander l’accès aux ports série via l’API Serial

* AskSerial (3) = autoriser les sites à demander l’autorisation de l’utilisateur à accéder à un port série

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DefaultSerialGuardSetting
  - Nom de la stratégie de groupe: contrôler l’utilisation de l’API Serial
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DefaultSerialGuardSetting
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DefaultWebUsbGuardSetting
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DelayNavigationsForInitialSiteListDownload
  #### Exiger que la liste des sites en mode entreprise soit disponible avant la navigation à l’onglet
  
  
  #### Versions prises en charge:
  - Sur Windows depuis la version84 ou versions ultérieures

  #### Description
  Vous permet de spécifier si les onglets Microsoft Edge doivent patienter jusqu’à ce que le navigateur ait téléchargé la liste initiale de sites de mode entreprise. Ce paramètre est destiné au scénario dans lequel la page d’accueil du navigateur doit être chargée en mode Internet Explorer. il est important que le navigateur s’exécute pour la première fois lorsque le mode IE est activé. Si ce scénario n’existe pas, nous vous recommandons de ne pas activer ce paramètre, car cela peut avoir un impact négatif sur les performances de chargement de la page d’accueil. Le paramètre s’applique uniquement lorsque Microsoft Edge ne possède pas de liste de sites en mode entreprise mis en cache, par exemple, sur le navigateur pour la première fois, lorsque le mode IE est activé.

Ce paramètre fonctionne conjointement avec: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) défini sur «IEMode» et [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) avec une liste comportant au moins une entrée.

Le comportement de cette stratégie peut être configuré avec la stratégie de [NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout).

Si vous définissez cette stratégie sur « All », lorsque Microsoft Edge ne possède pas de version mise en cache de la liste de sites en mode Entreprise, les onglets retardent la navigation jusqu’à ce que le navigateur ait téléchargé cette liste. Les sites configurés pour s’ouvrir en mode Internet Explorer par le biais de la liste des sites se chargent en mode Internet Explorer, même pendant la navigation initiale du navigateur. Sites qui ne peuvent pas être configurés pour s’ouvrir dans Internet Explorer, par exemple, les sites dont le modèle n’est pas http:, https:, fichier: ou FTP: ne retardez pas la navigation et le chargement immédiatement en mode Edge.

Si vous définissez cette stratégie sur « None » ou si vous ne la configurez pas, lorsque Microsoft Edge ne possède pas de version mise en cache de la liste de sites en mode Entreprise, les onglets permettent immédiatement la navigation sans attendre que le navigateur ait téléchargé cette liste. Les sites configurés pour s’ouvrir en mode Internet Explorer par le biais de la liste des sites s’ouvrent en mode Microsoft Edge jusqu’à ce que le navigateur ait terminé de télécharger la liste des sites en mode entreprise.

Mappage des options de stratégie:

* None (0) = Aucune

* All (1) = Toutes les navigations éligibles

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: DelayNavigationsForInitialSiteListDownload
  - Nom de la stratégie de protection: la liste des sites en mode entreprise est disponible avant la navigation à l’onglet
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DelayNavigationsForInitialSiteListDownload
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)

  ### DeleteDataOnMigration
  #### Supprimer les anciennes données de navigateur lors de la migration
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version83 ou versions ultérieures

  #### Description
  Cette stratégie détermine si les données de navigation, provenant des utilisateurs des versions antérieures de Microsoft Edge, sont supprimées après la migration vers la version81 de MicrosoftEdge ou une version ultérieure.

Si vous activé cette stratégie, toutes les données de navigation provenant des versions antérieures de MicrosoftEdge sont supprimées après la migration vers la version81 de MicrosoftEdge ou une version ultérieure. Cette stratégie doit être activée avant d’effectuer la migration vers la version81 de MicrosoftEdge ou une version ultérieure, pour qu’elle s’applique aux données de navigation existantes.

Si vous désactivez cette stratégie, ou si la stratégie n’est pas configurée, les données de navigation de l’utilisateur ne sont pas supprimées après la migration vers la version83 de MicrosoftEdge ou une version ultérieure.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DeleteDataOnMigration
  - Nom de la stratégie de groupe: supprimer les anciennes données de navigateur lors de la migration
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DeleteDataOnMigration
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  

  [Retour au début](#microsoft-edge---policies)

  ### DeveloperToolsAvailability
  #### Contrôler où les outils de développement peuvent être utilisés
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminer où les outils de développement peuvent être utilisés.

Si vous définissez cette stratégie sur «DeveloperToolsDisallowedForForceInstalledExtensions» (valeur par défaut), les utilisateurs peuvent accéder aux outils de développement et à la console JavaScript en général, mais pas dans le contexte des extensions installées par la stratégie d’entreprise.

Si vous définissez cette stratégie sur «DeveloperToolsAllowed», les utilisateurs peuvent accéder aux outils de développement et à la console JavaScript dans tous les contextes, y compris pour les extensions installées par la stratégie d’entreprise.

Si vous définissez cette stratégie sur «DeveloperToolsDisallowed», les utilisateurs ne peuvent pas accéder aux outils de développement ni inspecter les éléments du site web. Les raccourcis clavier et les entrées de menu ou de menu contextuel qui ouvrent les outils de développement ou la console JavaScript sont désactivées.

Mappage des options de stratégie:

* DeveloperToolsDisallowedForForceInstalledExtensions (0)=Bloquer les outils de développement sur les extensions installées par la stratégie d’entreprise, autoriser dans les autres contextes

* DeveloperToolsAllowed (1) = Autoriser l’utilisation des outils de développement

* DeveloperToolsDisallowed (2) = Ne pas autoriser l’utilisation des outils de développement

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DeveloperToolsAvailability
  - Nom de la stratégie de groupe: contrôler où les outils de développement peuvent être utilisés
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DeveloperToolsAvailability
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DeveloperToolsAvailability
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DiagnosticData
  #### Envoyer les données de diagnostic requises et facultatives relatives à l’utilisation du navigateur
  
  
  #### Versions prises en charge:
  - Sur Windows7 et macOS depuis la version86 ou versions ultérieures

  #### Description
  Cette stratégie contrôle l’envoi à Microsoft de données de diagnostic requises et facultatives relatives à l’utilisation du navigateur.

Les données de diagnostic requises sont collectées pour garantir le niveau attendu de sécurité, de mise à jour et de performance de MicrosoftEdge.

Les données de diagnostic facultatives incluent des données sur la façon dont vous utilisez le navigateur, les sites web que vous visitez et les rapports d’incident à Microsoft afin d’améliorer les produits et services.

Cette stratégie n’est pas prise en charge sur les appareils Windows10. Pour contrôler cette collecte de données sur Windows10, les administrateurs informatiques doivent utiliser la stratégie de groupe de données de diagnostic de Windows. Selon la version de Windows, cette stratégie est soit «Autoriser la télémétrie», soit «Autoriser les données de diagnostic». Si vous souhaitez en savoir plus sur la collecte de données de diagnostic Windows10: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Utilisez l’un des paramètres suivants pour configurer cette stratégie:

«Désactivé» désactive la collecte de données de diagnostic requises et facultatives. Cette option n'est pas conseillée.

«RequiredData» envoie les données de diagnostic requises, mais désactive la collecte de données de diagnostic facultatives. MicrosoftEdge envoie les données de diagnostic requises pour garantir le niveau attendu de sécurité, de mise à jour et de performance de MicrosoftEdge.

«OptionalData» envoie les données de diagnostic facultatives qui incluent des données relatives à l’utilisation du navigateur, les sites web visités et les rapports d’incidents envoyés à Microsoft afin d’améliorer les produits et services.

Sur Windows7/macOS, cette stratégie contrôle l’envoi à Microsoft de données de diagnostic requises et facultatives.

Si vous ne configurez pas cette stratégie ou si vous la désactivez, MicrosoftEdge est défini par défaut sur les préférences de l’utilisateur.

Mappage des options de stratégie:

* Désactivé (0) = Désactivé (non recommandé)

* RequiredData (1) = Données requises

* OptionalData (2) = Données facultatives

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DiagnosticData
  - Nom de la stratégie de groupe: Envoyer les données de diagnostic requises et facultatives relatives à l’utilisation du navigateur
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de valeur: DiagnosticData
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: DiagnosticData
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DirectInvokeEnabled
  #### Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole DirectInvoke
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version78 ou versions ultérieures

  #### Description
  Autorisez les utilisateurs à ouvrir des fichiers à l’aide du protocole DirectInvoke. Le protocole DirectInvoke permet aux sites web de demander au navigateur d’ouvrir les fichiers d’une URL spécifique à l’aide du gestionnaire de fichiers DirectInvoke sur l’ordinateur ou l’appareil de l’utilisateur.

Si vous activez ou ne configurez pas cette stratégie, les utilisateurs peuvent ouvrir des fichiers à l’aide du protocole DirectInvoke.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas ouvrir de fichiers à l’aide du protocole DirectInvoke. Au lieu de cela, le fichier est enregistré dans le système de fichiers. 

Remarque : la désactivation de DirectInvoke peut empêcher certaines fonctionnalités de Microsoft SharePoint Online d’être utilisées correctement.

Si vous souhaitez en savoir plus sur DirectInvoke, consultez [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) et [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DirectInvokeEnabled
  - Nom de la stratégie de groupe: autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole DirectInvoke
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DirectInvokeEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  

  [Retour au début](#microsoft-edge---policies)

  ### Disable3DAPIs
  #### Désactiver la prise en charge des API graphiques 3D
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Empêcher les pages web d’accéder au processeur graphique (GPU) Plus précisément, les pages web ne peuvent pas accéder à l’API WebGL, et les plug-ins ne peuvent pas utiliser l’API Pepper 3D.

Si vous ne configurez pas ou si vous désactivez cette stratégie, les pages web peuvent utiliser l’API WebGL et les plug-ins ont accès à l’API Pepper 3D. Par défaut, MicrosoftEdge peut exiger que les arguments de la ligne de commande soient transmis pour pouvoir utiliser ces API.

Si la stratégie [HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) est définie sur false, la configuration de ’Disable3DAPIs’ est ignorée, ce qui équivaut à définir ’Disable3DAPIs’ sur true.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: Disable3DAPIs
  - Nom de la stratégie de groupe: désactiver la prise en charge des API graphiques 3D
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: Disable3DAPIs
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: Disable3DAPIs
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DisableScreenshots
  #### Désactiver la création de captures d’écran
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Détermine si les utilisateurs peuvent effectuer des captures d’écran de la page du navigateur.

Si elle est activée, l’utilisateur ne peut pas effectuer de captures d’écran à l’aide des raccourcis clavier ou des API d’extension.

Si elle est désactivée ou si elle n’est pas configurée, les utilisateurs peuvent effectuer des captures d’écran.

Cette stratégie contrôle les captures d’écran effectuées dans le navigateur proprement dit. Même si vous activez cette stratégie, les utilisateurs peuvent toujours prendre des captures d’écran à l’aide d’une méthode extérieure au navigateur (par l’intermédiaire d’une fonctionnalité du système d’exploitation ou d’une autre application).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DisableScreenshots
  - Nom de la stratégie de groupe: désactiver la création de captures d'écran
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DisableScreenshots
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DisableScreenshots
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DiskCacheDir
  #### Définir le répertoire du cache disque
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Configure le répertoire utilisé pour stocker les fichiers mis en cache. 

Si vous activez cette stratégie, MicrosoftEdge utilise le répertoire fourni, que l'utilisateur ait ou non spécifié l'indicateur "--disk-cache-dir". Pour éviter la perte de données ou d'autres erreurs inattendues, ne configurez pas cette stratégie sur le répertoire racine d'un volume ni sur un répertoire utilisé à d'autres fins, car MicrosoftEdge gère son contenu.

Consultez la page [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) pour obtenir la liste des variables qui peuvent être utilisées pour spécifier des répertoires ou des chemin d'accès.

Si vous ne configurez pas cette stratégie, le répertoire cache par défaut est utilisé et les utilisateurs peuvent remplacer ce paramètre par défaut par l’indicateur de ligne de commande «--disk-cache-dir».

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DiskCacheDir
  - Nom de la stratégie de groupe: définir le répertoire du cache disque
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DiskCacheDir
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"${user_home}/Edge_cache"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DiskCacheDir
  - Exemple de valeur:
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DiskCacheSize
  #### Définir la taille du cache disque, en octets
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Configure la taille du cache utilisé, en octets, pour stocker les fichiers en cache. 

Si vous définissez cette règle, Microsoft Edge utilise le cache en fonction de la taille indiquée, que l'utilisateur ait spécifié l'indicateur "--disk-cache-size" ou non. La valeur définie dans cette stratégie ne constitue pas une limite absolue, il s'agit plutôt d'une suggestion pour le système de mise en cache. En effet, toute valeur inférieure à quelques mégaoctets est trop faible et est arrondie pour atteindre un minimum acceptable. 

Si la valeur de cette stratégie est définie sur 0, la taille du cache par défaut est utilisée, mais l'utilisateur ne peut pas la modifier.

Si cette stratégie n'est pas configurée, la taille par défaut est utilisée, et l'utilisateur peut la remplacer à l'aide de l'indicateur "--disk-cache-size".

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DiskCacheSize
  - Nom de la stratégie de groupe: définir la taille du cache disque, en octets
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DiskCacheSize
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x06400000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DiskCacheSize
  - Exemple de valeur:
``` xml
<integer>104857600</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DnsOverHttpsMode
  #### Contrôler le mode du protocole DNS-over-HTTPS
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version83 ou versions ultérieures

  #### Description
  Contrôlez le mode du programme de résolution du protocole DNS-over-HTTPS. Cette stratégie permet uniquement de choisir le mode par défaut pour chaque requête. Le mode peut être remplacé pour les types de requêtes spéciaux, tels que les demandes de résolution d’un nom d’hôte du serveur DNS-over-HTTPS.

Le mode «désactivé» désactive DNS-over-HTTPS.

Le mode «automatique» envoie d’abord les requêtes DNS-over-HTTPS si un serveur DNS-over-HTTPS est disponible et peut envoyer des requêtes non sécurisées en cas d’erreur.

Le mode «sécurisé» envoie uniquement les requêtes DNS-over-HTTPS et ne peut pas se résoudre en cas d’erreur.

Si vous ne configurez pas cette stratégie, le navigateur peut envoyer des requêtes DNS-over-HTTPS à un programme de résolution associé au programme de résolution système configuré de l’utilisateur.

Mappage des options de stratégie:

* off (off) = Désactiver DNS over HTTPs

* automatic (automatic) = Activer DNS over HTTPs avec un secours non sécurisé

* secure (secure) = Activer DNS over HTTPs sans secours non sécurisé

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DnsOverHttpsMode
  - Nom de la stratégie de groupe: contrôler le mode du protocole DNS-over-HTTPS
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DnsOverHttpsMode
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"off"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DnsOverHttpsMode
  - Exemple de valeur:
``` xml
<string>off</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DnsOverHttpsTemplates
  #### Spécifier le modèle d’URI du programme de résolution DNS-over-HTTPS souhaité
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version83 ou versions ultérieures

  #### Description
  L modèle d’URI du programme de résolution DNS-over-HTTPS souhaité. Pour spécifier plusieurs programmes de résolution DNS-over-HTTPS, séparez les modèles d’URI correspondants par des espaces.

Si vous avez définissez [DnsOverHttpsMode](#dnsoverhttpsmode) sur «sécurisé», alors cette stratégie doit être configurée et ne peut pas être vide.

Si vous définissez [DnsOverHttpsMode](#dnsoverhttpsmode) sur «automatique» et que cette stratégie est définie, les modèles d’URI spécifiés sont utilisés. Si vous ne configurez pas cette stratégie, les mappages codés en dur seront utilisés pour tenter de mettre à jour la résolution DNS en cours de l’utilisateur vers un programme de résolution DoH, géré par le même fournisseur.

Si le modèle d’URI contient une variable DNS, les requêtes adressées au programme de résolution utilisent la méthode GET. dans le cas contraire, les requêtes utilisent la méthode POST.

Les modèles au format incorrect sont ignorés.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DnsOverHttpsTemplates
  - Nom de la stratégie de groupe: spécifier le modèle d’URI du programme de résolution DNS-over-HTTPS souhaité
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: DnsOverHttpsTemplates
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"https://dns.example.net/dns-query{?dns}"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DnsOverHttpsTemplates
  - Exemple de valeur:
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DownloadDirectory
  #### Définir le répertoire de téléchargement
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Configure le répertoire utilisé pour télécharger les fichiers.

Si vous définissez cette stratégie, MicrosoftEdge utilise le répertoire fourni, que l'utilisateur en ait spécifié un ou non, ou qu'il ait ou non activé l'indicateur permettant d'être invité à renseigner l'emplacement du téléchargement à chaque fois. Vous pouvez consulter la liste des variables utilisables sur [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041). 

Si vous désactivez ou ne configurez pas cette stratégie, le répertoire de téléchargement par défaut est utilisé et l’utilisateur peut le modifier.

Si vous avez défini un chemin d’accès non valide, MicrosoftEdge utilise, par défaut, le répertoire de téléchargement de l’utilisateur.

Si le dossier spécifié par le chemin d’accès n’existe pas, le téléchargement déclenche une invite demandant à l’utilisateur où il souhaite enregistrer son téléchargement.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DownloadDirectory
  - Nom de la stratégie de groupe: définir le répertoire de téléchargement
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: DownloadDirectory
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DownloadDirectory
  - Exemple de valeur:
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### DownloadRestrictions
  #### Autoriser les restrictions de téléchargement
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Configure les types de téléchargements que MicrosoftEdge bloque complètement, et pour lesquels les utilisateurs ne sont pas autorisés à ignorer l'avertissement de sécurité.

Si vous sélectionnez l'option « BlockDangerousDownloads », tous les téléchargements sont autorisés, sauf ceux déclenchant un avertissement Microsoft Defender SmartScreen.

Si vous sélectionnez l'option «BlockPotentiallyDangerousDownloads», tous les téléchargements sont autorisés, sauf ceux déclenchant un avertissement Microsoft Defender SmartScreen pour des téléchargements potentiellement dangereux ou indésirables.

Si vous sélectionnez l'option « BlockAllDownloads », tous les téléchargements sont bloqués.

Si cette stratégie n'est pas configurée ou si vous la définissez sur « DefaultDownloadSecurity », les restrictions de sécurité habituelles basées sur les résultats de l'analyse de Microsoft Defender SmartScreen s'appliquent aux téléchargements. 

Ces restrictions s'appliquent aux téléchargements déclenchés à partir du contenu d'une page web et de l'option de menu contextuel "Télécharger le lien...". Elles ne s'appliquent pas à l'enregistrement ni au téléchargement de la page actuellement affichée, ni à l'enregistrement au format PDF depuis les options d'impression.

Consultez la page [https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934) pour en savoir plus sur Microsoft Defender SmartScreen.

Mappage des options de stratégie:

* DefaultDownloadSecurity (0) = Aucune restriction spéciale

* BlockDangerousDownloads (1) = Bloquer les téléchargements dangereux

* BlockPotentiallyDangerousDownloads (2) = Bloquer les téléchargements potentiellement dangereux ou indésirables

* BlockAllDownloads (3) = Bloquer tous les téléchargements

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: DownloadRestrictions
  - Nom de la stratégie de groupe: autoriser les restrictions de téléchargement
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: DownloadRestrictions
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: DownloadRestrictions
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### EdgeCollectionsEnabled
  #### Activer la fonctionnalité Collections
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version78 ou versions ultérieures

  #### Description
  Vous permet d'autoriser les utilisateurs à accéder à la fonctionnalité Collections afin de pouvoir collecter, organiser, partager et exporter du contenu de manière plus efficace et avec l'intégration d'Office.

Si vous activez ou ne configurez pas cette stratégie, les utilisateurs peuvent accéder à la fonctionnalité Collections et l'utiliser dans MicrosoftEdge.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas accéder à la fonctionnalité Collections et ne peuvent pas l'utiliser dans MicrosoftEdge.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: EdgeCollectionsEnabled
  - Nom de la stratégie de groupe: activer la fonctionnalité Collections
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: EdgeCollectionsEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: EdgeCollectionsEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### EditFavoritesEnabled
  #### Autorise les utilisateurs à modifier les favoris
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Activez cette stratégie pour permettre aux utilisateurs d'ajouter, de supprimer et de modifier des favoris. Il s'agit du comportement par défaut si vous ne configurez pas la stratégie. 

Désactivez cette stratégie pour empêcher les utilisateurs d'ajouter, de supprimer et de modifier des favoris. Ils peuvent toujours utiliser des favoris existants.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: EditFavoritesEnabled
  - Nom de la stratégie de groupe: autorise les utilisateurs à modifier les favoris
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: EditFavoritesEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: EditFavoritesEnabled
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### EnableDeprecatedWebPlatformFeatures
  #### Réactiver les fonctionnalités des plateformes web déconseillées pendant une durée limitée
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifiez une liste de fonctionnalités de plateforme web déconseillées à réactiver temporairement.

Cette stratégie vous permet de réactiver des fonctionnalités déconseillées de la plateforme en ligne pendant une durée limitée. Les fonctionnalités sont identifiées par une balise de chaîne.

Si vous ne configurez pas cette stratégie, si la liste est vide ou si une fonctionnalité ne correspond pas à l’une des balises de chaîne prises en charge, toutes les fonctionnalités de plateforme web déconseillées restent désactivées.

Bien que la stratégie elle-même soit compatible avec les plateformes citées, la fonctionnalité qu'elle active peut n'être disponible que sur un nombre plus restreint de plateformes. Les fonctionnalités déconseillées de la plateforme web ne peuvent pas toutes être réactivées. Seules celles qui sont énumérées ci-dessous peuvent l'être pendant une durée limitée, qui varie en fonction de la fonctionnalité. Vous pouvez découvrir les raisons pour lesquelles des motivations ont été apportées aux fonctionnalités des plates-formes en ligne en consultant la page https://bit.ly/blinkintents.

Le format général de la balise de chaîne est [DeprecatedFeatureName]_EffectiveUntil[yyyymmdd].

Mappage des options de stratégie:

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = Activer l'API ExampleDeprecatedFeature jusqu'au 02/09/2008

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: EnableDeprecatedWebPlatformFeatures
  - Nom de la stratégie de groupe: réactiver les fonctionnalités des plateformes web déconseillées pendant une durée limitée
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: EnableDeprecatedWebPlatformFeatures
  - Exemple de valeur:
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### EnableDomainActionsDownload
  #### Activer le téléchargement des actions de domaine à partir de Microsoft
  
  >OBSOLÈTE: Cette stratégie est obsolète et ne fonctionne pas après la version 84 de Microsoft Edge.
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 et jusqu’à la version84

  #### Description
  Cette stratégie ne fonctionne pas, car les États conflictuels doivent être évités. Cette stratégie était utilisée pour activer/désactiver le téléchargement de la liste des actions de domaine, mais elle n’a pas toujours atteint l’état souhaité. Le service d’expérimentation et de configuration, qui gère le téléchargement, a sa propre stratégie pour configurer les éléments téléchargés à partir du service. Utilisez plutôt la stratégie [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol).

Dans MicrosoftEdge, les actions de domaine représentent une série de fonctionnalités de compatibilité permettant au navigateur de fonctionner correctement sur le web. 

Microsoft conserve la liste des actions à entreprendre sur certains domaines pour des raisons de compatibilité. Par exemple, le navigateur peut remplacer la chaîne Agent utilisateur sur un site web si ce site web a été bloqué en raison de la nouvelle chaîne Agent utilisateur dans MicrosoftEdge. Chacune de ces actions est destinée à être temporaire, tandis que Microsoft tente de résoudre le problème avec le propriétaire du site.

Au démarrage du navigateur, puis régulièrement par la suite, le navigateur va contacter le service de Configuration et d'Expérimentation qui contient la liste la plus à jour des actions de compatibilité a exécuter. Cette liste est enregistrée localement une fois qu'elle a été récupérée afin que les demandes ultérieures ne mettent à jour que la liste, si la copie du serveur a été modifiée. 

Si vous activez cette stratégie, la liste des actions de domaine continue à être téléchargée à partir du service de Configuration et d'Expérimentation.

Si vous désactivez cette stratégie, la liste des actions de domaine n'est plus téléchargée à partir du service de Configuration et d'Expérimentation. 

Si vous ne configurez pas cette stratégie, la liste des actions de domaine continue à être téléchargés à partir du service de Configuration et d'Expérimentation.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: EnableDomainActionsDownload
  - Nom GP: Activer le téléchargement des actions de domaine à partir de Microsoft (obsolète)
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: EnableDomainActionsDownload
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: EnableDomainActionsDownload
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### EnableOnlineRevocationChecks
  #### Activer les vérifications OCSP/CRL en ligne
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Les contrôles de révocation en ligne étant sujets à erreur, ils ne présentent aucun avantage concret en termes de sécurité, ils sont désactivés par défaut.

Si vous activez cette stratégie, MicrosoftEdge effectue des contrôles de vérification OCSP/CRL en ligne. «Soft fail» signifie que si le serveur de révocation n'est pas accessible, le certificat sera considéré comme valide.

Si vous désactivez ou ne configurez pas la stratégie, MicrosoftEdge n’effectue pas de vérifications de révocation en ligne.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: EnableOnlineRevocationChecks
  - Nom de la stratégie de groupe: activer les vérifications OCSP/CRL en ligne
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: EnableOnlineRevocationChecks
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: EnableOnlineRevocationChecks
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### EnableSha1ForLocalAnchors
  #### Autoriser les certificats signés à l’aide de l’algorithme SHA-1 lorsqu’ils sont émis par des ancres d’approbation locales (obsolète)
  >DÉCONSEILLÉ: cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version85 ou versions ultérieures

  #### Description
  Lorsque ce paramètre est activé, Microsoft Edge autorise les connexions sécurisées par des certificats signés SHA-1 tant que le certificat est lié à un certificat racine installé localement et est en outre valide.

Notez que cette stratégie dépend de ce que la pile de vérification du certificat de système d’exploitation autorise les signatures SHA-1. Si une mise à jour de système d’exploitation modifie son traitement des certificats SHA-1, cette stratégie risque de ne plus être appliquée.  De plus, cette stratégie est conçue comme une solution de contournement temporaire pour offrir aux entreprises davantage de temps pour abandonner SHA-1. Cette stratégie sera supprimée dans Microsoft Edge 92 disponible mi-2021.

Si vous ne configurez pas cette stratégie ou si vous la définissez sur « false », ou si le certificat SHA-1 est lié à une racine de certificat approuvé publiquement, Microsoft Edge n’autorise pas les certificats signés par SHA-1.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP : EnableSha1ForLocalAnchors
  - Nom GP : Autoriser les certificats signés à l’aide de l’algorithme SHA-1 lorsqu’ils sont émis par des ancres d’approbation locales (déconseillé)
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur : EnableSha1ForLocalAnchors
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: EnableSha1ForLocalAnchors
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### EnterpriseHardwarePlatformAPIEnabled
  #### Autoriser les extensions gérées de manière à utiliser l’API de plateforme de matériel d’entreprise
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version78 ou versions ultérieures

  #### Description
  Lorsque cette stratégie est activée, les extensions installées par la stratégie d'entreprise sont autorisées à utiliser l'API de plateforme de matériel d'entreprise.
Lorsque cette stratégie est désactivée ou si elle n’est pas configurée, laucune extension n'est autorisée à utiliser l'API de plateforme de matériel d'entreprise.
Cette stratégie s'applique également aux extensions de composant.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: EnterpriseHardwarePlatformAPIEnabled
  - Nom de la stratégie de groupe: autoriser les extensions gérées de manière à utiliser l'API de plateforme de matériel d'entreprise
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: EnterpriseHardwarePlatformAPIEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: EnterpriseHardwarePlatformAPIEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### EnterpriseModeSiteListManagerAllowed
  #### Autoriser l’accès à l’outil Enterprise Mode Site List Manager
  
  
  #### Versions prises en charge:
  - Sur Windows depuis la version86 ou ultérieur

  #### Description
  Vous permet de définir si Enterprise Mode Site List Manager est disponible pour les utilisateurs.

Si vous activez cette stratégie, les utilisateurs peuvent voir le bouton de navigation Enterprise Mode Site List Manager sur la page edge://compat, accéder à l’outil et l’utiliser.

Si vous désactivez ou ne configurez pas cette stratégie, les utilisateurs ne voient pas le bouton de navigation Enterprise Mode Site List Manager et ne peuvent pas l’utiliser.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP : EnterpriseModeSiteListManagerAllowed
  - Nom GP : Autoriser l’accès à l’outil Enterprise Mode Site List Manager
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur : EnterpriseModeSiteListManagerAllowed
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  

  [Retour au début](#microsoft-edge---policies)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  #### Désactiver le téléchargement des avertissements basés sur l’extension de fichier pour les types de fichiers spécifiés sur les domaines
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version85 ou versions ultérieures

  #### Description
  Vous pouvez activer cette stratégie pour créer un dictionnaire d’extensions de type de fichier avec une liste correspondante de domaines qui seront exemptés des avertissements de téléchargement basés sur une extension de type de fichier. Ainsi, les administrateurs d’entreprise bloquent les avertissements de téléchargement basés sur l’extension de type de fichier pour les fichiers associés à un domaine répertorié. Par exemple, si l’extension «JNLP» est associée à «website1.com», les utilisateurs ne verront pas d’avertissement lors du téléchargement de fichiers «JNLP» de «website1.com», mais un avertissement de téléchargement apparaît lorsque vous téléchargez des fichiers «JNLP» de «website2.com».

Les fichiers avec les extensions de type de fichier spécifiées pour les domaines identifiés par cette stratégie sont néanmoins soumis à des avertissements de sécurité basés sur une extension de type non-fichier, tels que des avertissements de téléchargement de contenu mixte et des avertissements Microsoft Defender SmartScreen.

Si vous désactivez ou ne configurez pas cette stratégie, les types de fichiers déclenchant des avertissements de téléchargement basés sur une extension affichent des avertissements à l’utilisateur.

Si vous activez cette stratégie:

* Le modèle d’URL doit être mis en forme en fonction de [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).
* L’extension de type de fichier entrée doit être en minuscules ASCII. Il n’est pas possible d’inclure le séparateur principal dans la liste des types de fichiers. par conséquent, vous devez utiliser la liste «JNLP» à la place de «. jnlp».

Exemple:

La valeur d’exemple suivante empêche les avertissements de téléchargement basés sur l’extension de type de fichier sur les extensions SWF, exe et JNLP pour les domaines *. contoso.com. L’utilisateur affiche un avertissement de téléchargement basé sur une extension de type de fichier sur un autre domaine pour les fichiers exe et JNLP, mais pas pour les fichiers SWF.

[{"file_extension": "JNLP", "Domains": ["contoso.com"]}, {"file_extension": "exe", "Domains": ["contoso.com"]}, {"file_extension": "swf", "Domains": ["*"]}]

Notez que, bien que l’exemple précédent montre la suppression des avertissements de téléchargement basés sur l’extension de type de fichier pour les fichiers «SWF» pour tous les domaines, il n’est pas recommandé d’appliquer la suppression de tels avertissements pour tous les domaines pour toute extension de type de fichier dangereuse en raison de problèmes de sécurité. Il s’affiche dans l’exemple simplement pour illustrer la possibilité de le faire.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Nom de la stratégie de protection: désactiver le téléchargement des avertissements basés sur l’extension de fichier pour les types de fichiers spécifiés sur les domaines
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Exemple de valeur:
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ExperimentationAndConfigurationServiceControl
  #### Contrôler la communication avec le service d’expérimentation et de configuration
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Dans Microsoft Edge, le service d'expérimentation et de configuration permet de déployer la charge utile d'expérimentation et de configuration.

La charge utile de l'expérimentation consiste en une liste des fonctionnalités à un stade précoce de développement qui sont activées par Microsoft à des fins de test et de commentaires.

La charge utile de la configuration consiste en une liste de paramètres que Microsoft souhaite déployer pour MicrosoftEdge afin d'optimiser l'expérience utilisateur. Par exemple, la charge utile de la configuration peut spécifier la fréquence à laquelle MicrosoftEdge envoie des demandes au service d'expérimentation et de configuration pour récupérer la charge utile la plus récente.

De plus, la charge utile de configuration peut également contenir une liste des actions à effectuer sur certains domaines pour des raisons de compatibilité. Par exemple, le navigateur peut remplacer la chaîne Agent utilisateur sur un site web si ce site web a été bloqué en raison de la nouvelle chaîne Agent utilisateur dans MicrosoftEdge. Chacune de ces actions est destinée à être temporaire, tandis que Microsoft tente de résoudre le problème avec le propriétaire du site.

Si vous définissez cette stratégie sur le mode «FullMode», la charge utile complète est téléchargée à partir du service d'expérimentation et de configuration. Cela inclut les charges utiles de l'expérimentation et celles de la configuration.

Si vous définissez cette stratégie sur le mode «ConfigurationsOnlyMode», seule la charge utile de la configuration est livrée.

Si vous définissez cette stratégie sur «RestrictedMode», la communication avec le service d’expérimentation et de configuration est arrêtée complètement.

Si vous ne configurez pas cette stratégie, le comportement sur un appareil géré sur des canaux stables et bêta est le même qu'avec le mode «ConfigurationsOnlyMode».

Si vous ne configurez pas cette stratégie, le comportement sur un appareil non géré est le même qu'avec le mode «FullMode».

Mappage des options de stratégie:

* FullMode (2)=Récupérer les configurations et les expérimentations

* ConfigurationsOnlyMode (1) = Récupérer les configurations uniquement

* RestrictedMode (0)=Désactiver la communication avec le service d'expérimentation et de configuration

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ExperimentationAndConfigurationServiceControl
  - Nom de la stratégie de groupe: contrôler la communication avec le service d'expérimentation et de configuration
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ExperimentationAndConfigurationServiceControl
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ExperimentationAndConfigurationServiceControl
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox
  #### Afficher une case à cocher «Toujours ouvrir» dans la boîte de dialogue de protocole externe
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version79 ou versions ultérieures

  #### Description
  Cette stratégie contrôle si la case à cocher «Toujours autoriser ce site à ouvrir des liens de ce type» est affichée dans les invites de confirmation de lancement du protocole externe. Cette stratégie s’applique uniquement aux liens https://.

Si vous activez cette stratégie, lorsqu'une invite de confirmation de protocole externe s'affiche, l'utilisateur peut sélectionner «Toujours ouvrir». L'utilisateur ne reçoit pas les invites de confirmation futures de ce protocole sur ce site.

Si vous désactivez cette stratégie, la case à cocher «Toujours ouvrir» n'est pas affichée. L'utilisateur est invité à confirmer chaque fois qu'un protocole externe est appelé.

Avant Microsoft Edge83, si vous ne configurez pas cette stratégie, la case à cocher «Toujours ouvrir» ne s’affiche pas. L'utilisateur est invité à confirmer chaque fois qu'un protocole externe est appelé.

Dans MicrosoftEdge83, si vous ne configurez pas cette stratégie, la visibilité de la case à cocher est contrôlée par l'indicateur «Activer la mémorisation des préférences d'invite de lancement de protocole» dans edge://flags

En ce qui concerne MicrosoftEdge84, si vous ne configurez pas cette stratégie, lorsqu'une invite de confirmation de protocole externe s'affiche, l'utilisateur peut sélectionner «Toujours ouvrir». L'utilisateur ne reçoit pas les invites de confirmation futures de ce protocole sur ce site.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Nom de la stratégie de groupe: afficher une case à cocher «Toujours ouvrir» dans la boîte de dialogue de protocole externe
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### FamilySafetySettingsEnabled
  #### Autoriser les utilisateurs à configurer le contrôle parental
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version83 ou versions ultérieures

  #### Description
  Cette stratégie désactive et masque complètement la page du contrôle parentale dans les Paramètres. La navigation sur edge://settings/familysafety est également bloquée. La page du contrôle parental décrit quelles fonctionnalités sont disponibles pour les groupes familiaux et comment rejoindre l’un de ces groupes. Consultez ces articles pour en savoir plus sur le contrôle parental: ([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432)).

Si vous activez cette stratégie ou que vous ne la configurez pas, la page du contrôle parental apparaît.

Si vous désactivez cette stratégie, la page du contrôle parental n’apparaît pas.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: FamilySafetySettingsEnabled
  - Nom de la stratégie de groupe: autoriser les utilisateurs à configurer le contrôle parental
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: FamilySafetySettingsEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: FamilySafetySettingsEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### FavoritesBarEnabled
  #### Activer la barre des favoris
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Active ou désactive la barre des favoris.

Si vous activez cette stratégie, les utilisateurs voient la barre des favoris.

Si vous désactivez cette stratégie, les utilisateurs ne voient pas la barre des favoris.

Si cette stratégie n’est pas configurée, l’utilisateur peut décider d’utiliser ou non la barre des favoris.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: FavoritesBarEnabled
  - Nom de la stratégie de groupe: activer la barre des favoris
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: FavoritesBarEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: FavoritesBarEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ForceBingSafeSearch
  #### Appliquer le filtre adulte Bing
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Vérifiez que les requêtes de recherche sur le web Bing sont effectuées avec le Filtre adulte définie sur la valeur spécifiée.  Les utilisateurs ne peuvent pas modifier ce paramètre.

Si vous définissez cette stratégie sur «BingSafeSearchNoRestrictionsMode», le Filtre adulte de recherche Bing revient à la valeur bing.com.

Si vous configurez cette stratégie sur «BingSafeSearchModerateMode», le paramètre modéré est utilisé dans le Filtre adulte. Le paramètre modéré filtre les vidéos pour adultes et les images, mais pas le texte, des résultats de recherche. 

Si vous configurez cette stratégie sur «BingSafeSearchStrictMode», le paramètre strict du Filtre adulte est utilisé. Le paramètre strict filtre le texte, les images et les vidéos pour adultes.

Si vous désactivez cette stratégie ou ne la configurez pas, le Filtre adulte de Recherche Bing n'est pas appliquée et les utilisateurs peuvent définir la valeur de leur choix sur bing.com. 

Mappage des options de stratégie:

* BingSafeSearchNoRestrictionsMode (0) = Ne pas configurer de restrictions de recherche dans Bing

* BingSafeSearchModerateMode (1)=Configurer des restrictions de recherche modérées dans Bing 

* BingSafeSearchStrictMode (2)=Configurer des restrictions de recherche strictes dans Bing

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ForceBingSafeSearch
  - Nom de la stratégie de groupe: appliquer le filtre adulte Bing
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ForceBingSafeSearch
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ForceBingSafeSearch
  - Exemple de valeur:
``` xml
<integer>0</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ForceCertificatePromptsOnMultipleMatches
  #### Configurer la sélection automatique d’un certificat par MicrosoftEdge lorsqu’il existe plusieurs correspondances de certificats pour un site configuré avec «AutoSelectCertificateForUrls»
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version81 ou versions ultérieures

  #### Description
  vIndique si les utilisateurs sont invités à sélectionner un certificat si plusieurs certificats sont disponibles et qu'un site est configuré avec [AutoSelectCertificateForUrls](#autoselectcertificateforurls). Si vous ne configurez pas [AutoSelectCertificateForUrls](#autoselectcertificateforurls) pour un site, l'utilisateur est toujours invité à sélectionner un certificat. 

Si vous définissez cette stratégie sur True, MicrosoftEdge invite un utilisateur à sélectionner un certificat pour les sites de la liste définie dans [AutoSelectCertificateForUrls](#autoselectcertificateforurls) si et seulement s'il y a plusieurs certificats. 

Si vous définissez cette stratégie sur False ou si vous ne la configurez pas, MicrosoftEdge sélectionne automatiquement un certificat, même s'il existe plusieurs correspondances pour un certificat.  L'utilisateur n'est pas invité à sélectionner un certificat pour les sites de la liste définie dans [AutoSelectCertificateForUrls](#autoselectcertificateforurls).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ForceCertificatePromptsOnMultipleMatches
  - Nom de la stratégie de groupe: configurer la sélection automatique d’un certificat par MicrosoftEdge lorsqu'il existe plusieurs correspondances de certificats pour un site configuré avec «AutoSelectCertificateForUrls»
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ForceCertificatePromptsOnMultipleMatches
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ForceCertificatePromptsOnMultipleMatches
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ForceEphemeralProfiles
  #### Activer l’utilisation des profils éphémères
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Détermine si les profils utilisateur sont basculés en mode éphémère. Un profil éphémère est créé lorsqu’une session commence, est supprimé lorsque la session se termine, et est associé au profil d’origine de l’utilisateur.

Si vous activez cette stratégie, les profils s’exécutent en mode éphémère. Cela permet aux utilisateurs de travailler à partir de leurs propres appareils sans enregistrer les données de navigation sur ces appareils. Si vous activez cette stratégie en tant que stratégie de système d’exploitation (à l’aide de GPO sur Windows, par exemple), elle s’applique à tous les profils sur le système.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, les utilisateurs reçoivent leurs profils habituels lorsqu’ils se connectent au navigateur.

En mode éphémère, les données de profil ne sont enregistrées sur le disque uniquement le temps de la session utilisateur. Des fonctionnalités telles que l'historique du navigateur, les extensions et leurs données, les données web comme les cookies et les bases de données web ne sont pas enregistrées après la fermeture du navigateur. Cela n'empêche pas un utilisateur de télécharger manuellement des données sur le disque, ni d'enregistrer des pages ou de les imprimer. Si l'utilisateur a activé la synchronisation, toutes les données sont conservées dans leurs comptes de synchronisation, de la même manière que les profils standard. Les utilisateurs peuvent également utiliser la navigation InPrivate en mode éphémère, sauf si vous désactivez explicitement cette possibilité.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ForceEphemeralProfiles
  - Nom de la stratégie de groupe: activer l’utilisation des profils éphémères
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ForceEphemeralProfiles
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ForceEphemeralProfiles
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ForceGoogleSafeSearch
  #### Appliquer le filtre adulte Google
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Force l’exécution des requêtes dans la recherche sur le web Google avec le Filtre adulte activé, et empêche les utilisateurs de modifier ce paramètre.

Si vous activez ce paramètre, le Filtre adulte est toujours activé dans la recherche Google.

Si vous désactivez ce paramètre ou ne définissez pas de valeur, le Filtre adulte n'est pas activé dans la recherche Google.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ForceGoogleSafeSearch
  - Nom de la stratégie de groupe: appliquer le filtre adulte Google
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ForceGoogleSafeSearch
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ForceGoogleSafeSearch
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ForceLegacyDefaultReferrerPolicy
  #### Utiliser une stratégie de renvoi par défaut no-referrer-when-downgrade (déconseillé).
  >DÉCONSEILLÉ: cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version81 ou versions ultérieures

  #### Description
  Cette stratégie est déconseillée, car elle a pour but de servir uniquement comme mécanisme à court terme afin d’offrir aux entreprises davantage de temps pour mettre à jour leurs environnements si et quand ils sont détectés comme étant incompatibles avec la stratégie actuelles de point d’accès par défaut. Il ne fonctionne pas dans la version 88 de Microsoft Edge.

La stratégie de renvoie par défaut de MicrosoftEdge est renforcée à partir de sa valeur actuelle no-referrer-when-downgrade vers la valeur strict-origin-when-cross-origin, plus sécurisée dans le cadre d'un lancement graduel.

Avant le lancement, cette stratégie d'entreprise n'a aucun effet. Après le lancement, lorsque cette stratégie d'entreprise est activée, la stratégie de renvoi par défaut de Microsoft Edge sera définie sur l’ancienne valeur définie, c’est-à-dire la valeur no-referrer-when-downgrade. 

Cette stratégie d’entreprise est désactivée par défaut.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ForceLegacyDefaultReferrerPolicy
  - Nom de la stratégie de groupe: utiliser une stratégie de renvoi par défaut no-referrer-when-downgrade.
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ForceLegacyDefaultReferrerPolicy
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ForceLegacyDefaultReferrerPolicy
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ForceNetworkInProcess
  #### Forcer l’exécution du code de mise en réseau dans le processus du navigateur (obsolète)
  
  >OBSOLÈTE: Cette stratégie est obsolète et ne fonctionne pas après la version 83 de Microsoft Edge.
  #### Versions prises en charge:
  - Sur Windows depuis 78, jusqu’à 83

  #### Description
  Cette stratégie ne fonctionne pas, car elle n’a pour but qu’être un mécanisme à court terme pour offrir aux entreprises davantage de temps pour la migration vers des logiciels tiers qui ne dépendent pas de l’accrochage des API réseau. Les serveurs proxy sont recommandés via la mise à jour corrective des API LSP et Win32.

Cette stratégie force l'exécution du code réseaux dans le processus du navigateur.

Cette stratégie est désactivée par défaut. Si elle est activée, les utilisateurs risquent d'être confrontés à des problèmes de sécurité une fois le processus réseaux isolé.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ForceNetworkInProcess
  - Nom de la stratégie de groupe: forcer l’exécution du code de mise en réseau dans le processus du navigateur
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ForceNetworkInProcess
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  

  [Retour au début](#microsoft-edge---policies)

  ### ForceSync
  #### Forcer la synchronisation des données du navigateur et ne pas afficher l’invite de consentement de synchronisation
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Force la synchronisation des données dans MicrosoftEdge. Cette stratégie empêche également l’utilisateur de désactiver la synchronisation.

Si vous ne configurez pas cette stratégie, les utilisateurs pourront activer ou désactiver la synchronisation. Si vous activez cette stratégie, les utilisateurs ne pourront pas désactiver la synchronisation.

Pour que cette stratégie fonctionne correctement, la stratégie [BrowserSignin](#browsersignin) ne doit pas être configurée ou doit être activée. Si [BrowserSignin](#browsersignin) est désactivée, [ForceSync](#forcesync) ne sera pas prise en compte.

[SyncDisabled](#syncdisabled) ne doit pas être configurée ou doit être définie sur False. Si ce paramètre est défini sur True, [ForceSync](#forcesync) ne sera pas prise en compte.

0 = ne pas démarrer automatiquement la synchronisation et afficher le consentement de synchronisation (par défaut) 1 = forcer l’activation de la synchronisation pour le profil utilisateur AzureAD/Azure AD-Degraded et ne pas afficher l’invite de consentement de synchronisation

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ForceSync
  - Nom de la stratégie de groupe: forcer la synchronisation des données du navigateur et ne pas afficher l’invite de consentement de synchronisation
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ForceSync
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ForceSync
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ForceYouTubeRestrict
  #### Forcer le mode restreint minimal sur YouTube
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Applique un mode restreint minimal sur YouTube et empêche l'utilisateur de choisir un mode moins restrictif.

Définissez la stratégie sur «Strict» pour appliquer le mode restreint strict sur YouTube.

Définissez la stratégie sur «Moderate» pour obliger les utilisateurs a utiliser les modes restreints strict ou modéré sur YouTube. Ils ne peuvent pas désactiver le mode restreint.

Si vous définissez la stratégie sur « Off » ou ne la configurez pas, le mode restreint n’est pas appliqué sur YouTube. Des stratégies externes comme les stratégies de YouTube peuvent toujours appliquer le mode restreint.

Mappage des options de stratégie:

* Off (0)=Ne pas appliquer le mode restreint sur YouTube

* Moderate (1)=Appliquer au moins le mode restreint modéré sur YouTube

* Strict (2)=Appliquer le mode restreint strict sur YouTube

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ForceYouTubeRestrict
  - Nom de la stratégie de groupe: forcer le mode restreint minimal sur YouTube
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ForceYouTubeRestrict
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ForceYouTubeRestrict
  - Exemple de valeur:
``` xml
<integer>0</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### FullscreenAllowed
  #### Autoriser le mode plein écran
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version77 ou versions ultérieures

  #### Description
  Définissez la disponibilité du mode plein écran: toute l'interface utilisateur de MicrosoftEdge est masquée et seul le contenu web est visible.

Si vous activez cette stratégie ou ne la configurez pas, l’utilisateur, les applications et les extensions disposant des autorisations appropriées peuvent passer en mode plein écran.

Si vous désactivez cette stratégie, les utilisateurs, les applications et les extensions ne peuvent pas passer en mode plein écran.

L'ouverture de Microsoft Edge en mode kiosque à l'aide de la ligne de commande n'est pas disponible lorsque le mode plein écran est désactivé.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: FullscreenAllowed
  - Nom de la stratégie de groupe: autoriser le mode plein écran
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: FullscreenAllowed
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)

  ### GloballyScopeHTTPAuthCacheEnabled
  #### Activer le cache d’authentification HTTP de portée globale.
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version81 ou versions ultérieures

  #### Description
  Cette stratégie configure un cache global unique par profil avec les informations d'identification du serveur HTTP.

Si vous désactivez ce paramètre de stratégie ou si vous ne le configurez pas, le navigateur utilise le comportement par défaut de l'authentification intersite, qui, à partir de la version80, comprendra toutes les informations d'authentification du serveur HTTP en commençant par le site de meilleur niveau. Par conséquent, si deux sites utilisent des ressources provenant du même domaine d'authentification, les informations d'identification devront être renseignées indépendamment dans le contexte des deux sites.  Les informations d'identification du proxy mis en cache seront réutilisées sur les sites. 

Si vous activez ce paramètre, les informations d'authentification HTTP de stratégie entrées dans le contexte d'un site sont automatiquement utilisées dans le contexte d'un autre site. 

L'activation de cette stratégie laisse les sites ouverts à certains types d'attaques intersite et permet d'effectuer le suivi des utilisateurs sur les sites, même sans cookies, en ajoutant des entrées au cache d'authentification HTTP à l'aide d'informations d'identification incorporées dans les URL.

Cette stratégie est destinée à fournir aux entreprises, en fonction du comportement hérité, une possibilité de mettre à jour leurs procédures de connexion et elle sera supprimée à l'avenir.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: GloballyScopeHTTPAuthCacheEnabled
  - Nom de la stratégie de groupe: activer le cache d'authentification HTTP de portée globale.
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: GloballyScopeHTTPAuthCacheEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: GloballyScopeHTTPAuthCacheEnabled
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar
  #### Forcer la navigation directe sur le site intranet au lieu de rechercher des entrées à mots uniques dans la barre d’adresses
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version78 ou versions ultérieures

  #### Description
  Si vous activez cette stratégie, le premier résultat de la suggestion automatique dans la liste de suggestions de la barre d'adresses navigue vers les sites intranet si le texte entré dans la barre d'adresses est un mot unique sans ponctuation.

La navigation par défaut lors de la saisie d'un mot unique sans ponctuation effectue une navigation vers un site intranet correspondant au texte saisi.

Si vous activez cette stratégie, le deuxième résultat de la suggestion automatique dans la liste de suggestions de la barre d'adresses mène à une recherche sur le web exactement telle qu'elle a été entrée, à condition que ce texte ne comporte qu'un seul mot sans ponctuation.  Le moteur de recherche par défaut est utilisé, sauf si une stratégie empêchant la recherche sur le web a également été activée.

L'activation de cette stratégie peut avoir deux effets: 

La navigation vers les sites en réponse à des requêtes avec un seul mot se concentrant sur un seul élément de l'historique n'apparaît plus. Au lieu de cela, le navigateur tente de naviguer vers des sites internes qui n'existent peut-être plus dans le réseau intranet d'une organisation. Cette action génère une erreur 404.

Les termes de recherche populaires à mot unique nécessitent une sélection manuelle des suggestions de recherche pour mener une recherche de manière correcte.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Nom de la stratégie de groupe: forcer la navigation directe sur le site intranet au lieu de rechercher des entrées à mots uniques dans la barre d'adresses
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### HSTSPolicyBypassList
  #### Configurer la liste des noms qui vont contourner la vérification de stratégie HSTS
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version79 ou versions ultérieures

  #### Description
  Les noms d'hôte spécifiés dans cette liste seront dispensés de la vérification de stratégie HSTS qui pourrait éventuellement mettre à niveau les demandes de «http://» vers «https://». Seuls les noms d'hôte en une seule partie sont autorisés dans cette stratégie. Les noms d'hôte doivent être au format canonique. Toutes les IDN doivent être convertis au format d'étiquette A et toutes les lettres ASCII doivent être en minuscule. Cette stratégie ne s'applique qu'aux noms d'hôte spécifiques indiqués ; elle ne s'applique pas aux sous-domaines des noms de la liste.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: HSTSPolicyBypassList
  - Nom de la stratégie de groupe: configurer la liste des noms qui vont contourner la vérification de stratégie HSTS
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: HSTSPolicyBypassList
  - Exemple de valeur:
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### HardwareAccelerationModeEnabled
  #### Utiliser l’accélération matérielle lorsque celle-ci est disponible
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indiquez si vous souhaitez utiliser l’accélération matérielle, si celle-ci est disponible. Si vous activez cette stratégie ou si vous ne la configurez pas, l'accélération matérielle est activée, sauf si une certaine fonctionnalité GPU figure sur la liste noire. 

Si vous désactivez cette stratégie, l'accélération matérielle est désactivée.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: HardwareAccelerationModeEnabled
  - Nom de la stratégie de groupe: utiliser l’accélération matérielle lorsque celle-ci est disponible
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: HardwareAccelerationModeEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: HardwareAccelerationModeEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### HideFirstRunExperience
  #### Masquer l’expérience de première utilisation et l’écran de démarrage
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Si vous activez cette stratégie, l'expérience de première exécution et l'écran de démarrage ne sont pas affichés aux utilisateurs lorsqu'ils exécutent MicrosoftEdge pour la première fois.

Pour les options de configuration affichées dans l'expérience de première exécution, le navigateur prend par défaut les valeurs suivantes:

- Sous la page Nouvel onglet, le type de flux est défini sur MSN News et la mise en page sur Source d'inspiration. 

- L'utilisateur est toujours connecté automatiquement à MicrosoftEdge si le compte Windows est de type AAD ou MSA.

-La synchronisation n’est pas activée par défaut et les utilisateurs sont invités à décider s’ils souhaitent effectuer une synchronisation au démarrage du navigateur. Vous pouvez utiliser la stratégie [ForceSync](#forcesync) ou [SyncDisabled](#syncdisabled) pour configurer la synchronisation et l’invite de consentement à la synchronisation.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, l'expérience de première exécution et l'écran de démarrage s'affichent.

Remarque : les options de configuration spécifiques qui s'affichent à l'utilisateur lors de la première utilisation peuvent également être gérées à l'aide d'autres stratégies spécifiques. Vous pouvez utiliser la stratégie HideFirstRunExperience en association avec ces stratégies pour configurer une expérience de navigateur spécifique sur vos appareils gérés. Voici quelques-unes de ces autres stratégies:

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[ForceSync](#forcesync)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: HideFirstRunExperience
  - Nom de la stratégie de groupe: masquer l'expérience de première utilisation et l'écran de démarrage
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: HideFirstRunExperience
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: HideFirstRunExperience
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImportAutofillFormData
  #### Autoriser l’importation des données de saisie automatique
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet aux utilisateurs d’importer des données de saisie automatique à partir d’un autre navigateur dans MicrosoftEdge.

Si vous activez cette stratégie, l'option d'importation manuelle des données de saisie automatique est automatiquement sélectionnée.

Si vous désactivez cette stratégie, les données du formulaire de saisie automatique ne sont pas importées lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les données de saisie automatique sont importées lors de la première exécution et les utilisateurs peuvent choisir d'importer ces données manuellement lors des sessions de navigation ultérieures.

Vous pouvez définir cette stratégie comme une recommandation. Cela signifie que MicrosoftEdge importera les données de saisie automatique lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou effacer l'option de **saisie automatique des données** lors de l'importation manuelle.

**Remarque**: cette stratégie gère actuellement l'importation des navigateurs Google Chrome (sur Windows7, 8 et 10 et sur macOS) et Mozilla Firefox (sur Windows7, 8 et 10 et sur macOS).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImportAutofillFormData
  - Nom de la stratégie de groupe: autoriser l’importation des données de saisie automatique
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ImportAutofillFormData
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImportAutofillFormData
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImportBrowserSettings
  #### Autoriser l’importation des paramètres du navigateur
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version78 ou versions ultérieures

  #### Description
  Permet aux utilisateurs d'importer les paramètres du navigateur à partir d'un autre navigateur dans MicrosoftEdge.

Si vous activez cette stratégie, la case **Paramètres du navigateur** est automatiquement cochée dans la boîte de dialogue **Importer des données du navigateur**. 

Si vous désactivez cette stratégie, les paramètres du navigateur ne sont pas importés lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les paramètres du navigateur sont importés lors de la première exécution et les utilisateurs peuvent choisir s'ils souhaitent les importer manuellement lors des sessions de navigation ultérieures.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les paramètres lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l'option **Paramètres du navigateur** pendant l'importation manuelle. 

**Remarque**: cette stratégie gère actuellement l'importation de Google Chrome (sous Windows7, 8 et 10 et sous macOS).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImportBrowserSettings
  - Nom de la stratégie de groupe: autoriser l'importation des paramètres du navigateur
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ImportBrowserSettings
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImportBrowserSettings
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImportCookies
  #### Autoriser l’importation des cookies
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version81 ou versions ultérieures

  #### Description
  Permet aux utilisateurs d'importer des cookies à partir d'un autre navigateur dans MicrosoftEdge.

Si vous désactivez cette stratégie, les cookies ne sont pas importés lors de la première utilisation.

Si vous ne configurez pas cette stratégie, les cookies sont importés lors de la première utilisation.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que MicrosoftEdge importe les cookies lors de la première utilisation.

**Remarque**: cette stratégie gère actuellement l'importation de Google Chrome (sous Windows7, 8 et 10 et sous macOS).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImportCookies
  - Nom de la stratégie de groupe: autoriser l’importation des cookies
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ImportCookies
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImportCookies
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImportExtensions
  #### Autoriser l’importation des extensions
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version81 ou versions ultérieures

  #### Description
  Permet aux utilisateurs d'importer des extensions à partir d'un autre navigateur dans MicrosoftEdge.

Si vous activez cette stratégie, la case **Extensions** est automatiquement cochée dans la boîte de dialogue **Importer des données du navigateur**. 

Si vous désactivez cette stratégie, les extensions ne sont pas importées lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les extensions sont importées lors de la première exécution et les utilisateurs peuvent choisir s'ils souhaitent les importer manuellement lors des sessions de navigation ultérieures.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les extensions lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l'option **Favoris** pendant l'importation manuelle. 

**Remarque**: cette stratégie prend uniquement en charge l'importation de Google Chrome (sous Windows7, 8 et 10 et sous macOS).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImportExtensions
  - Nom de la stratégie de groupe: autoriser l’importation des extensions
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ImportExtensions
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImportExtensions
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImportFavorites
  #### Autoriser l’importation des favoris
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet aux utilisateurs d'importer des favoris à partir d'un autre navigateur dans MicrosoftEdge.

Si vous activez cette stratégie, la case **Favoris** est automatiquement cochée dans la boîte de dialogue **Importer des données du navigateur**. 

Si vous désactivez cette stratégie, les favoris ne sont pas importés lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les favoris sont importés lors de la première exécution et les utilisateurs peuvent choisir s'ils souhaitent les importer manuellement lors des sessions de navigation ultérieures.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les favoris lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l'option **Favoris** pendant l'importation manuelle. 

**Remarque**: cette stratégie gère actuellement l'importation des navigateurs Internet Explorer (sur Windows7, 8, and 10), Google Chrome (sur Windows7, 8, et 10 and sur macOS), Mozilla Firefox (sur Windows7, 8, and 10 et sur macOS), and Apple Safari (sur macOS).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImportFavorites
  - Nom de la stratégie de groupe: autoriser l’importation des favoris
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ImportFavorites
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImportFavorites
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImportHistory
  #### Autoriser l’importation de l’historique de navigation
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet aux utilisateurs d'importer leur historique de navigation à partir d'un autre navigateur dans MicrosoftEdge.

Si vous activez cette stratégie, la case **Historique de navigation** est automatiquement cochée dans la boîte de dialogue **Importer des données du navigateur**. 

Si vous désactivez cette stratégie, les données de l’historique de navigation ne sont pas importées lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les données de l’historique de navigation sont importées lors de la première exécution et les utilisateurs peuvent choisir d'importer ces données manuellement lors des sessions de navigation ultérieures.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe l’historique de navigation lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l'option **Historique** pendant l'importation manuelle. 

**Remarque**: cette stratégie gère actuellement l'importation des navigateurs Internet Explorer (sur Windows7, 8, and 10), Google Chrome (sur Windows7, 8, et 10 and sur macOS), Mozilla Firefox (sur Windows7, 8, and 10 et sur macOS), and Apple Safari (macOS).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImportHistory
  - Nom de la stratégie de groupe: autoriser l'importation de l’historique de navigation
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ImportHistory
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImportHistory
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImportHomepage
  #### Autoriser l’importation des paramètres de la page d’accueil
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet aux utilisateurs d'importer leur page d’accueil à partir d'un autre navigateur dans MicrosoftEdge.

Si vous activez cette stratégie, l'option d'importation manuelle de la page d’accueil est automatiquement sélectionnée.

Si vous désactivez cette stratégie, les paramètres de la page d’accueil ne sont pas importés lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les paramètres de la page d’accueil sont importés lors de la première exécution et les utilisateurs peuvent choisir d'importer ces données manuellement lors des sessions de navigation ultérieures.

Vous pouvez définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les paramètres de la page d’accueil lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l'option **Page d'accueil** pendant l'importation manuelle. 

**Remarque**: cette stratégie gère actuellement l'importation de Internet Explorer (sous Windows7, 8 et 10). 

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImportHomepage
  - Nom de la stratégie de groupe: autoriser l'importation des paramètres de la page d'accueil
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ImportHomepage
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImportHomepage
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImportOpenTabs
  #### Autoriser l’importation des onglets ouverts
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version79 ou versions ultérieures

  #### Description
  Permet aux utilisateurs d'importer les onglets ouverts et épinglés à partir d'un autre navigateur dans MicrosoftEdge.

Si vous activez cette stratégie, la case **Onglets ouverts** est automatiquement cochée dans la boîte de dialogue **Importer des données du navigateur**.

Si vous désactivez cette stratégie, les onglets ouverts ne sont pas importés lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement. 

Si vous ne configurez pas cette stratégie, les onglets ouverts sont importés lors de la première exécution et les utilisateurs peuvent choisir s'ils souhaitent les importer manuellement lors des sessions de navigation ultérieures. 

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que MicrosoftEdge importe les onglets ouverts lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l'option **Onglets ouverts** pendant l'importation manuelle.

**Remarque**: cette stratégie prend uniquement en charge l'importation de Google Chrome (sous Windows7, 8 et 10 et sous macOS).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImportOpenTabs
  - Nom de la stratégie de groupe: autoriser l'importation des onglets ouverts
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ImportOpenTabs
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImportOpenTabs
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImportPaymentInfo
  #### Autoriser l’importation des informations de paiement
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet aux utilisateurs d’importer des infos de paiement à partir d'un autre navigateur dans MicrosoftEdge.

Si vous activez cette stratégie, la case à cocher **Infos de paiement** est automatiquement activée dans la boîte de dialogue **Importer les données du navigateur**.

Si vous désactivez cette stratégie, les infos de paiement ne sont pas importées lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les infos de paiement sont importées lors de la première exécution et les utilisateurs peuvent décider de les importer manuellement lors des sessions de navigation ultérieures.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que MicrosoftEdge importe les infos de paiement lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou effacer l'option **infos de paiement** pendant l'importation manuelle.

**Remarque:** cette stratégie gère actuellement l'importation à partir de Google Chrome (sous Windows7, 8 et 10 et sous macOS).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImportPaymentInfo
  - Nom de la stratégie de groupe: autoriser l'importation des informations de paiement
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ImportPaymentInfo
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImportPaymentInfo
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImportSavedPasswords
  #### Autoriser l’importation des mots de passe enregistrés
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet aux utilisateurs d'importer des mots de passe enregistrés à partir d'un autre navigateur dans MicrosoftEdge.

Si vous activez cette stratégie, l'option d'importation manuelle des mots de passe enregistrés est automatiquement sélectionnée.

Si vous désactivez cette stratégie, les mots de passe enregistrés ne sont pas importés lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement. 

Si vous ne configurez pas cette stratégie, les mots de passe enregistrés sont importés lors de la première exécution et les utilisateurs peuvent choisir s'ils souhaitent les importer manuellement lors des sessions de navigation ultérieures. 

Vous pouvez définir cette stratégie comme une recommandation. Cela signifie que MicrosoftEdge importe les onglets ouverts lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l'option **mots de passe enregistrés** pendant l'importation manuelle.

**Remarque**: cette stratégie gère actuellement l'importation des navigateurs Internet Explorer (sur Windows7, 8, and 10), Google Chrome (sur Windows7, 8, et 10 and sur macOS) et Mozilla Firefox (sur Windows7, 8, and 10 et sur macOS).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImportSavedPasswords
  - Nom de la stratégie de groupe: autoriser l’importation des mots de passe enregistrés
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ImportSavedPasswords
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImportSavedPasswords
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImportSearchEngine
  #### Autoriser l’importation des paramètres du moteur de recherche
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet aux utilisateurs d'importer les paramètres du moteur de recherche à partir d'un autre navigateur dans MicrosoftEdge.

Si vous activez cette stratégie, l'option d'importation du moteur de recherche est automatiquement sélectionnée.

Si vous désactivez cette stratégie, les paramètres du moteur de recherche ne sont pas importés lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les paramètres du moteur de recherche sont importés lors de la première exécution et les utilisateurs peuvent choisir d'importer ces données manuellement lors des sessions de navigation ultérieures.

Vous pouvez définir cette stratégie comme une recommandation. Cela signifie que MicrosoftEdge importe les paramètres du moteur de recherche lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l'option **moteur de recherche** pendant l'importation manuelle. 

**Remarque**: cette stratégie gère actuellement l'importation de Internet Explorer (sous Windows7, 8 et 10). 

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImportSearchEngine
  - Nom de la stratégie de groupe: autoriser l’importation des paramètres du moteur de recherche
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ImportSearchEngine
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImportSearchEngine
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ImportShortcuts
  #### Autoriser l’importation des raccourcis
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version81 ou versions ultérieures

  #### Description
  Permet aux utilisateurs d'importer les raccourcis à partir d'un autre navigateur dans MicrosoftEdge.

Si vous désactivez cette stratégie, les raccourcis ne sont pas importés lors de la première exécution.

Si vous ne configurez pas cette stratégie, les raccourcis sont importés lors de la première exécution.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que MicrosoftEdge importe les raccourcis lors de la première exécution. 

**Remarque**: cette stratégie gère actuellement l'importation depuis Google Chrome (sous Windows7, 8 et 10 et sous macOS).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ImportShortcuts
  - Nom de la stratégie de groupe: autoriser l’importation des raccourcis
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ImportShortcuts
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ImportShortcuts
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### InPrivateModeAvailability
  #### Configurer la disponibilité du mode InPrivate
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indique si l'utilisateur peut ouvrir des pages en mode InPrivate dans MicrosoftEdge.

Si vous ne configurez cette stratégie ou si vous la définissez sur «Enabled», les utilisateurs peuvent ouvrir des pages en mode InPrivate.

Définissez cette stratégie sur «Disabled» pour empêcher les utilisateurs d'utiliser le mode InPrivate.

Définissez cette stratégie sur «Forced» pour toujours utiliser le mode InPrivate.

Mappage des options de stratégie:

* Enabled (0)=Mode InPrivate disponible

* Disabled (1)=Mode InPrivate désactivé 

* Forced (2)=Mode InPrivate obligatoire

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: InPrivateModeAvailability
  - Nom de la stratégie de groupe: configurer la disponibilité du mode InPrivate
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: InPrivateModeAvailability
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: InPrivateModeAvailability
  - Exemple de valeur:
``` xml
<integer>1</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### InsecureFormsWarningsEnabled
  #### Activer les avertissements pour les formulaires non sécurisés
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Cette stratégie contrôle la gestion des formulaires non sécurisés (formulaires soumis via HTTP) intégrés dans des sites sécurisés (HTTPS) dans le navigateur.
Si vous activez cette stratégie ou ne la définissez pas, un avertissement en plein écran s’affiche lorsqu’un formulaire non sécurisé est soumis. De plus, une bulle d’avertissement s’affiche à côté des champs de formulaire lorsqu’ils sont sélectionnés et la saisie automatique est désactivée pour ces formulaires.
Si vous désactivez cette stratégie, les avertissements ne seront pas affichés pour les formulaires non sécurisés et la saisie automatique fonctionnera normalement.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: InsecureFormsWarningsEnabled
  - Nom de la stratégie de groupe: activer les avertissements pour les formulaires non sécurisés
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: InsecureFormsWarningsEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: InsecureFormsWarningsEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### IntensiveWakeUpThrottlingEnabled
  #### Contrôler la fonctionnalité IntensiveWakeUpThrottling
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version85 ou versions ultérieures

  #### Description
  Lorsque la fonctionnalité IntensiveWakeUpThrottling est activée, les timers JavaScript dans les onglets d’arrière-plan sont considérablement accélérés et fusionnés, et ne s’exécutent pas plus d’une fois par minute après qu’une page ait été mise en arrière-plan pendant 5 minutes ou plus.

Il s’agit d’une fonctionnalité conforme aux normes Web, mais elle risque de rompre la fonctionnalité de certains sites Web en forçant certaines actions à être différées de quelques minutes. Cependant, l’utilisation de la CPU et de la batterie entraîne une économie considérable. Voir https://bit.ly/30b1XR4 pour plus d’informations.

Si vous activez cette stratégie, la fonctionnalité est activée et les utilisateurs ne peuvent pas modifier ce paramètre.
Si vous désactivez cette stratégie, la fonctionnalité sera désactivée et les utilisateurs ne pourront pas modifier ce paramètre.
Si vous ne configurez pas cette stratégie, la fonctionnalité est contrôlée par sa propre logique interne. Les utilisateurs peuvent configurer manuellement ce paramètre.

Notez que la stratégie est appliquée par processus de convertisseur, et la valeur la plus récente du paramètre de stratégie est appliquée au démarrage du processus de rendu. Un redémarrage complet est nécessaire pour s’assurer que tous les onglets chargés reçoivent un paramètre de stratégie cohérent. Il est inoffensif pour les processus qui s’exécutent avec différentes valeurs de cette stratégie.


  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: IntensiveWakeUpThrottlingEnabled
  - Nom de la stratégie de protection: contrôler la fonctionnalité IntensiveWakeUpThrottling
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: IntensiveWakeUpThrottlingEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: IntensiveWakeUpThrottlingEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### InternetExplorerIntegrationEnhancedHangDetection
  #### Configurer la détection de blocage avancée pour le mode Internet Explorer
  
  
  #### Versions prises en charge:
  - Sur Windows depuis la version84 ou versions ultérieures

  #### Description
  La détection améliorée des blocages est une approche plus granulaire pour la détection de pages Web bloquées en mode Internet, plutôt que d’utiliser la version autonome d’Internet Explorer. Lorsqu’une page Web suspendue est détectée, le navigateur applique une atténuation pour empêcher le blocage du reste du navigateur.

Ce paramètre vous permet de configurer l’utilisation de la détection de blocage renforcée au cas où vous rencontriez des problèmes d’incompatibilité avec vos sites Web. Nous vous recommandons de désactiver cette stratégie uniquement si les notifications telles que «(site Web) ne répondent pas» en mode Internet Explorer, mais pas dans la version autonome d’Internet Explorer.

Ce paramètre fonctionne conjointement avec: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) défini sur «IEMode» et [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) avec une liste comportant au moins une entrée.

Si vous définissez cette stratégie sur «Enabled» ou si vous ne la configurez pas, les sites Web en mode Internet Explorer utilisent la détection d’arrêt intempestif améliorée.

Si vous configurez cette stratégie sur «Disabled», la détection d’arrêt intempestif renforcée est désactivée et les utilisateurs obtiendront le comportement de détection d’arrêt intempestif de base d’Internet Explorer.

Si vous souhaitez en savoir plus sur le mode Internet Explorer, consultez la page [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Mappage des options de stratégie:

* Disabled (0) = Détection d’arrêt intempestif améliorée désactivée

* Enabled (1) = Détection d’arrêt intempestif améliorée activée

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: InternetExplorerIntegrationEnhancedHangDetection
  - Nom de la stratégie de protection: configurer la détection de blocage avancée pour le mode Internet Explorer
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: InternetExplorerIntegrationEnhancedHangDetection
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)

  ### InternetExplorerIntegrationLevel
  #### Configurer l’intégration d’Internet Explorer
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version77 ou versions ultérieures

  #### Description
  Si vous souhaitez obtenir des instructions sur la configuration optimale de l'expérience pour Internet Explorer, consultez [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Mappage des options de stratégie:

* None (0) = Aucune

* IEMode (1) = Mode InternetExplorer

* NeedIE (2) = Internet Explorer 11

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: InternetExplorerIntegrationLevel
  - Nom de la stratégie de groupe: configurer l’intégration d’Internet Explorer
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: InternetExplorerIntegrationLevel
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)

  ### InternetExplorerIntegrationSiteList
  #### Configurer la liste des sites en mode Entreprise
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version78 ou versions ultérieures

  #### Description
  Si vous souhaitez obtenir des instructions sur la configuration optimale de l'expérience pour Internet Explorer, consultez [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: InternetExplorerIntegrationSiteList
  - Nom de la stratégie de groupe: configurer la liste des sites en mode Entreprise
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: InternetExplorerIntegrationSiteList
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"https://internal.contoso.com/sitelist.xml"
```


  

  [Retour au début](#microsoft-edge---policies)

  ### InternetExplorerIntegrationSiteRedirect
  #### Spécifier le comportement des navigations «sur la page» vers des sites non configurés lors du démarrage à partir des pages du mode Internet Explorer.
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version81 ou versions ultérieures

  #### Description
  Une navigation «entre les pages» est lancée à partir d'un lien, d'un script ou d'un formulaire de la page active. Il peut également s'agir d'une redirection côté serveur d'une tentative de navigation «entre les pages» précédente. À l’inverse, un utilisateur peut démarrer une navigation qui n'est pas «entre les pages» et qui est indépendante de la page active de plusieurs façons en utilisant les contrôles du navigateur. Par exemple, à l'aide de la barre d'adresses, du bouton précédent ou d'un lien favori.

Ce paramètre vous permet de spécifier si les navigations à partir de pages chargées en mode Internet Explorer sur des sites non configurés (qui ne sont pas configurés dans la liste de sites en mode Entreprise) basculent vers MicrosoftEdge ou restent en mode Internet Explorer.

Ce paramètre fonctionne conjointement avec: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) défini sur «IEMode» et [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) avec une liste comportant au moins une entrée.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, seuls les sites configurés pour s'ouvrir en mode Internet Explorer s'ouvrent dans ce mode. Les sites non configurés pour être ouverts en mode Internet Explorer sont redirigés vers MicrosoftEdge. 

Si vous définissez cette stratégie sur « Default », seuls les sites configurés pour être ouverts en mode Internet Explorer s'ouvrent dans ce mode. Les sites non configurés pour être ouverts en mode Internet Explorer sont redirigés vers MicrosoftEdge. 

Si vous définissez cette stratégie sur « AutomaticNavigationsOnly », vous bénéficiez de l'expérience par défaut, mais toutes les navigations automatiques (par exemple, les redirections 302) vers des sites non configurés restent en mode Internet Explorer. 

Si vous configurez cette stratégie sur « AllInPageNavigations », toutes les navigations depuis les pages chargées en mode IE vers des sites non configurés restent en mode Internet Explorer (le moins recommandé). 

Si vous souhaitez en savoir plus sur le mode Internet Explorer, consultez la page [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

Mappage des options de stratégie:

* Default (0) = Par défaut

* AutomaticNavigationsOnly (1)=Conserver les navigations automatiques en mode Internet Explorer

* AllInPageNavigations (2)=Conserver toutes les navigations en page en mode Internet Explorer

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: InternetExplorerIntegrationSiteRedirect
  - Nom de la stratégie de groupe: spécifier le comportement des navigations «sur la page» vers des sites non configurés lors du démarrage à partir des pages du mode Internet Explorer.
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: InternetExplorerIntegrationSiteRedirect
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  

  [Retour au début](#microsoft-edge---policies)

  ### InternetExplorerIntegrationTestingAllowed
  #### Autoriser le test du mode InternetExplorer
  
  
  #### Versions prises en charge:
  - Sur Windows depuis la version86 ou ultérieur

  #### Description
  Cette stratégie remplace la stratégie d’indicateur ie-mode-test. Elle permet aux utilisateurs d’ouvrir un onglet de mode IE à partir de l’option de menu de l’interface utilisateur.

Ce paramètre fonctionne conjointement avec: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) défini sur «IEMode» et [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) avec une liste comportant au moins une entrée.

Si vous activez cette stratégie, les utilisateurs peuvent ouvrir l’onglet du mode IE à partir de l’option de l’interface utilisateur et naviguer du site actuel vers un site en mode IE.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas voir directement l’option de l’interface utilisateur dans le menu.

Si vous ne configurez pas cette stratégie, vous pouvez configurer l’indicateur ie-mode-test manuellement.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: InternetExplorerIntegrationTestingAllowed
  - Nom de la stratégie: autoriser le test du mode InternetExplorer
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: InternetExplorerIntegrationTestingAllowed
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  

  [Retour au début](#microsoft-edge---policies)

  ### IsolateOrigins
  #### Activer l’isolation de site pour des origines spécifiques
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifiez les origines à exécuter dans une isolation, dans leur propre processus.

Cette stratégie isole également les origines nommées par sous-domaine. Par exemple, la définition de https://contoso.com/ provoque l'isolation de https://foo.contoso.com/ dans le cadre du site https://contoso.com/.

Si la stratégie est activée, chacune des origines nommées dans une liste séparée par des virgules s'exécute dans son propre processus.

Si vous désactivez cette stratégie, les fonctionnalités «IsolateOrigins» et «SitePerProcess» sont désactivées. Les utilisateurs peuvent toujours activer la stratégie «IsolateOrigins» manuellement, via les indicateurs de ligne de commande.

Si vous ne configurez pas la stratégie, l'utilisateur peut modifier ce paramètre.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: IsolateOrigins
  - Nom de la stratégie de groupe: activer l’isolation de site pour des origines spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: IsolateOrigins
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"https://contoso.com/,https://fabrikam.com/"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: IsolateOrigins
  - Exemple de valeur:
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### LocalProvidersEnabled
  #### Autoriser les suggestions des fournisseurs de services locaux
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version83 ou versions ultérieures

  #### Description
  Autoriser les suggestions des fournisseurs de suggestion sur l’appareil (fournisseurs locaux), comme par exemple, les favoris et l’historique de navigation, dans la barre d’adresse de MicrosoftEdge et la liste de suggestions automatiques.

Si vous activez cette stratégie, des suggestions provenant de fournisseurs locaux sont utilisées.

Si vous désactivez cette stratégie, les suggestions des fournisseurs locaux ne sont jamais utilisées. Les suggestions de l’historique local et des favoris locaux n’apparaissent pas.

Si vous ne configurez pas cette stratégie, les suggestions des fournisseurs locaux sont autorisées, mais l’utilisateur peut modifier ce paramètre à l’aide du bouton bascule.

Certaines fonctionnalités ne sont pas disponibles si une stratégie de désactivation de cette fonctionnalité a été appliquée. Par exemple, les suggestions d’historique de navigation ne sont pas disponibles si vous activez la stratégie [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled).

Cette stratégie nécessite un redémarrage du navigateur pour finaliser l’application.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: LocalProvidersEnabled
  - Nom de la stratégie de groupe: autoriser les suggestions des fournisseurs de services locaux
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: LocalProvidersEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: LocalProvidersEnabled
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ManagedFavorites
  #### Configurer les favoris
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Configure la liste des favoris gérés.

La stratégie crée une liste de favoris. Chaque favori contient les clés «nom» et «URL», qui contiennent le nom du favori et sa cible. Vous pouvez configurer un sous-dossier en définissant un favori sans clé «URL», mais avec une clé supplémentaire «enfants» qui contient une liste de favoris définie ci-dessus (certains peuvent être de nouveau des dossiers). MicrosoftEdge modifie les URL incomplètes comme si elles étaient envoyées par le biais de la barre d'adresses, par exemple, «microsoft.com» devient «https://microsoft.com/». 

Ces favoris sont placés dans un dossier qui ne peut pas être modifié par l'utilisateur (mais l'utilisateur peut choisir de le masquer dans la barre des favoris). Par défaut, le nom du dossier est « Favoris gérés », mais vous pouvez le modifier en ajoutant à la liste des favoris un dictionnaire contenant la clé « toplevel_name » avec le nom de dossier souhaité comme valeur.

Les favoris gérés ne sont pas synchronisés avec le compte d'utilisateur et ne peuvent pas être modifiés par des extensions.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Dictionary

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ManagedFavorites
  - Nom de la stratégie de groupe: configurer les favoris
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ManagedFavorites
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\ManagedFavorites = [
  {
    "toplevel_name": "My managed favorites folder"
  }, 
  {
    "name": "Microsoft", 
    "url": "microsoft.com"
  }, 
  {
    "name": "Bing", 
    "url": "bing.com"
  }, 
  {
    "children": [
      {
        "name": "Microsoft Edge Insiders", 
        "url": "www.microsoftedgeinsider.com"
      }, 
      {
        "name": "Microsoft Edge", 
        "url": "www.microsoft.com/windows/microsoft-edge"
      }
    ], 
    "name": "Microsoft Edge links"
  }
]
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ManagedFavorites
  - Exemple de valeur:
``` xml
<key>ManagedFavorites</key>
<array>
  <dict>
    <key>toplevel_name</key>
    <string>My managed favorites folder</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Microsoft</string>
    <key>url</key>
    <string>microsoft.com</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Bing</string>
    <key>url</key>
    <string>bing.com</string>
  </dict>
  <dict>
    <key>children</key>
    <array>
      <dict>
        <key>name</key>
        <string>Microsoft Edge Insiders</string>
        <key>url</key>
        <string>www.microsoftedgeinsider.com</string>
      </dict>
      <dict>
        <key>name</key>
        <string>Microsoft Edge</string>
        <key>url</key>
        <string>www.microsoft.com/windows/microsoft-edge</string>
      </dict>
    </array>
    <key>name</key>
    <string>Microsoft Edge links</string>
  </dict>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ManagedSearchEngines
  #### Gérer les moteurs de recherche
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet de configurer une liste de 10moteurs de recherche maximum, dont un doit être défini comme moteur de recherche par défaut.
Vous ne devez pas spécifier l'encodage. À partir de MicrosoftEdge80, les paramètres suggest_url et image_search_url sont facultatifs. Le paramètre facultatif, image_search_post_params, (qui est constitué de paires de noms/valeurs séparés par des virgules) est disponible à partir de MicrosoftEdge80.

À partir de MicrosoftEdge83, vous pouvez activer la découverte de moteurs de recherche avec le paramètre facultatif allow_search_engine_discovery. Ce paramètre doit être le premier élément de la liste. Si allow_search_engine_discovery n’est pas spécifié, la découverte des moteurs de recherche est désactivée par défaut. À partir de Microsoft Edge84, vous pouvez utiliser cette stratégie comme stratégie recommandée pour autoriser la découverte de fournisseurs de recherche. Vous n’avez pas besoin d’ajouter le paramètre facultatif allow_search_engine_discovery.

Si cette stratégie est activée, les utilisateurs ne peuvent pas ajouter, supprimer ou modifier un moteur de recherche de la liste. Les utilisateurs peuvent définir leur moteur de recherche par défaut sur n'importe quel moteur de recherche de la liste.

Si vous désactivez ou ne configurez pas cette stratégie, les utilisateurs peuvent modifier la liste des moteurs de recherche en cas de besoin.

Si la stratégie [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) est définie, cette stratégie (ManagedSearchEngines) est ignorée. L'utilisateur doit redémarrer son navigateur pour terminer l'application de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Dictionary

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ManagedSearchEngines
  - Nom de la stratégie de groupe: gérer les moteurs de recherche
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ManagedSearchEngines
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\ManagedSearchEngines = [
  {
    "allow_search_engine_discovery": true
  }, 
  {
    "is_default": true, 
    "keyword": "example1.com", 
    "name": "Example1", 
    "search_url": "https://www.example1.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example1.com/qbox?query={searchTerms}"
  }, 
  {
    "image_search_post_params": "content={imageThumbnail},url={imageURL},sbisrc={SearchSource}", 
    "image_search_url": "https://www.example2.com/images/detail/search?iss=sbiupload", 
    "keyword": "example2.com", 
    "name": "Example2", 
    "search_url": "https://www.example2.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example2.com/qbox?query={searchTerms}"
  }, 
  {
    "encoding": "UTF-8", 
    "image_search_url": "https://www.example3.com/images/detail/search?iss=sbiupload", 
    "keyword": "example3.com", 
    "name": "Example3", 
    "search_url": "https://www.example3.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example3.com/qbox?query={searchTerms}"
  }, 
  {
    "keyword": "example4.com", 
    "name": "Example4", 
    "search_url": "https://www.example4.com/search?q={searchTerms}"
  }
]
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ManagedSearchEngines
  - Exemple de valeur:
``` xml
<key>ManagedSearchEngines</key>
<array>
  <dict>
    <key>allow_search_engine_discovery</key>
    <true/>
  </dict>
  <dict>
    <key>is_default</key>
    <true/>
    <key>keyword</key>
    <string>example1.com</string>
    <key>name</key>
    <string>Example1</string>
    <key>search_url</key>
    <string>https://www.example1.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example1.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>image_search_post_params</key>
    <string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
    <key>image_search_url</key>
    <string>https://www.example2.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example2.com</string>
    <key>name</key>
    <string>Example2</string>
    <key>search_url</key>
    <string>https://www.example2.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example2.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>encoding</key>
    <string>UTF-8</string>
    <key>image_search_url</key>
    <string>https://www.example3.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example3.com</string>
    <key>name</key>
    <string>Example3</string>
    <key>search_url</key>
    <string>https://www.example3.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example3.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>keyword</key>
    <string>example4.com</string>
    <key>name</key>
    <string>Example4</string>
    <key>search_url</key>
    <string>https://www.example4.com/search?q={searchTerms}</string>
  </dict>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### MaxConnectionsPerProxy
  #### Nombre maximal de connexions simultanées au serveur proxy
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indique le nombre maximal de connexions simultanées à un serveur proxy.

Certains serveurs proxy ne peuvent pas gérer un grand nombre de connexions simultanées par client. La définition d'une valeur inférieure pour cette règle peut résoudre ce problème. 

La valeur de cette règle doit être inférieure à 100 et supérieure à 6. La valeur par défaut est 32.

Certaines applications Web consomment de nombreuses connexions avec blocage des opérations GET. Par conséquent, le fait de définir une valeur inférieure à 32 peut entraîner des blocages de l'accès réseau du navigateur si un trop grand nombre d'applications Web de ce type sont ouvertes.

Si vous ne configurez pas cette stratégie, la valeur par défaut (32) est utilisée.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: MaxConnectionsPerProxy
  - Nom de la stratégie de groupe: nombre maximal de connexions simultanées au serveur proxy
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: MaxConnectionsPerProxy
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000020
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: MaxConnectionsPerProxy
  - Exemple de valeur:
``` xml
<integer>32</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### MediaRouterCastAllowAllIPs
  #### Autoriser Google Cast à se connecter aux appareils Cast sur toutes les adresses IP
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Activez cette stratégie pour permettre à Google Cast de se connecter à tous les appareils Cast sur toutes les adresses IP, sans se limiter aux adresses privées RFC1918/RFC4193.

Désactivez cette stratégie pour limiter Google Cast aux appareils Cast sur les adresses privées RFC1918/RFC4193.

Si vous ne configurez pas cette stratégie, Google Cast se connecte aux appareils Cast uniquement sur les adresses privées RFC1918/RFC4193, à moins que vous n'activiez la fonctionnalité CastAllowAllIPs.

Si la stratégie [EnableMediaRouter](#enablemediarouter) est désactivée, cette stratégie n'a aucun effet.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: MediaRouterCastAllowAllIPs
  - Nom de la stratégie de groupe: autoriser Google Cast à se connecter aux appareils Cast sur toutes les adresses IP
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: MediaRouterCastAllowAllIPs
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: MediaRouterCastAllowAllIPs
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### MetricsReportingEnabled
  #### Activer les rapports de données d’utilisation et d’incident (déconseillé)
  >DÉCONSEILLÉ: cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans la version MicrosoftEdge89. Cette stratégie est remplacée par la nouvelle stratégie:  [DiagnosticData](#diagnosticdata) pour Windows7, Windows8 et macOS. Cette stratégie est remplacée par Autoriser la télémétrie sur Windows10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

Cette stratégie permet l’envoi à Microsoft de rapports sur l’utilisation et les incidents liés à MicrosoftEdge.

Activez cette stratégie pour envoyer des rapports sur l’utilisation et les incidents à Microsoft. Désactivez cette stratégie pour ne pas envoyer les données à Microsoft. Dans un cas comme dans l’autre, les utilisateurs ne peuvent pas modifier ou remplacer le paramètre.

Dans Windows10, MicrosoftEdge prendra par défaut le paramètre de données de diagnostic Windows, si vous ne configurez cette stratégie. Si cette stratégie est activée, MicrosoftEdge envoie des données d’utilisation uniquement si le paramètre de données de Diagnostic Windows est défini sur Avancé ou Complet. Si cette stratégie est désactivée, MicrosoftEdge n’enverra pas de données d’utilisation. Les données liées aux incidents sont envoyées en fonction du paramètre de données de diagnostic Windows. Si vous souhaitez en savoir plus sur les paramètres de données de diagnostic Windows, consultez [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Sur Windows7, Windows8 et macOS, cette stratégie contrôle l’envoi des données relatives à l’utilisation et aux incidents. Si vous ne configurez pas cette stratégie, MicrosoftEdge est défini par défaut sur les préférences de l’utilisateur.

Pour activer cette stratégie,[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) doit être configuré sur Activé. Si [MetricsReportingEnabled](#metricsreportingenabled) ou [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) est défini comme Non configuré ou Désactivé, ces données ne sont pas envoyées à Microsoft.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise inscrites pour la gestion des appareils ou des instances macOS gérées via la Gestion des périphériques mobiles ou jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: MetricsReportingEnabled
  - Nom de la stratégie de groupe: Activer les rapports de données d’utilisation et d’incident (déconseillé)
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: MetricsReportingEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: MetricsReportingEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NativeWindowOcclusionEnabled
  #### Activer l’occlusion de fenêtre native
  
  
  #### Versions prises en charge:
  - Sur Windows depuis la version84 ou versions ultérieures

  #### Description
  Active l’occlusion de fenêtre native dans Microsoft Edge.

Si vous activez ce paramètre pour réduire la consommation du processeur et d’énergie, MicrosoftEdge détecte quand une fenêtre est couverte par d’autres fenêtres et suspend les pixels de peinture.

Si vous désactivez ce paramètre, MicrosoftEdge ne détecte pas les fenêtres couvertes par d’autres fenêtres.

Si cette stratégie n’est pas configurée, la détection du masquage des fenêtres est activée.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: NativeWindowOcclusionEnabled
  - Nom GP: Activer l’occlusion de fenêtre native
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: NativeWindowOcclusionEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)

  ### NavigationDelayForInitialSiteListDownloadTimeout
  #### Définition d’un délai d’expiration pour la navigation à l’onglet de la liste des sites en mode entreprise
  
  
  #### Versions prises en charge:
  - Sur Windows depuis la version84 ou versions ultérieures

  #### Description
  Vous permet de spécifier un délai d’expiration (en secondes) pour les onglets Microsoft Edge en attente de navigation jusqu’à ce que le navigateur ait téléchargé la liste initiale des sites de mode entreprise.

Ce paramètre fonctionne conjointement avec: [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) défini sur «IEMode», [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) avec une liste comportant au moins une entrée et [DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) défini sur «Toutes les navigations éligibles» (1).

Les onglets n’attendent pas plus longtemps que ce délai pour la liste des sites en mode entreprise à télécharger. Si le navigateur n’a pas terminé de télécharger la liste des sites en mode entreprise à l’expiration du délai d’expiration, les onglets Microsoft Edge continueront à se déplacer. La valeur du délai d’expiration ne doit pas excéder 20 secondes et pas moins de 1 seconde.

Si vous configurez le délai d’expiration dans cette stratégie sur une valeur supérieure à la valeur par défaut de 2 secondes, une barre d’informations est affichée à l’utilisateur après 2 secondes. La barre d’informations contient un bouton qui permet à l’utilisateur de quitter l’attente de la fin du téléchargement de la liste de sites en mode entreprise.

Si vous ne configurez pas cette stratégie, le délai d’expiration par défaut de 2 secondes est utilisé. Cette valeur par défaut est susceptible d’être modifiée à l’avenir.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: NavigationDelayForInitialSiteListDownloadTimeout
  - Nom de la stratégie de groupe: définition d’un délai d’expiration pour la navigation dans les onglets de la liste des sites en entreprise
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: NavigationDelayForInitialSiteListDownloadTimeout
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x0000000a
```


  

  [Retour au début](#microsoft-edge---policies)

  ### NetworkPredictionOptions
  #### Activer la prédiction réseau
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Active la prédiction réseau dans Google Chrome et empêche les utilisateurs de modifier ce paramètre.

Cela contrôle la prélecture des DNS, ainsi que la préconnexion et le préchargement TCP et SSL des pages Web.

Si vous ne configurez pas cette règle, la prédiction réseau est activée, mais les utilisateurs peuvent la modifier.

Mappage des options de stratégie:

* NetworkPredictionAlways (0)=Prédire les actions réseau sur toute connexion réseau

* NetworkPredictionWifiOnly (1) = Non pris en charge, l’option «Prédire les actions réseau sur toute connexion réseau» (0) est appliquée si cette valeur est utilisée

* NetworkPredictionNever (2)=Ne prédire les actions réseau sur aucune connexion réseau

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: NetworkPredictionOptions
  - Nom de la stratégie de groupe: activer la prédiction réseau
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: NetworkPredictionOptions
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: NetworkPredictionOptions
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### NonRemovableProfileEnabled
  #### Configurer la connexion automatique du profil par défaut de l’utilisateur avec son compte professionnel ou scolaire
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version78 ou versions ultérieures

  #### Description
  Cette stratégie détermine si un utilisateur peut supprimer le profil MicrosoftEdge connecté automatiquement dans le compte professionnel ou scolaire d'un utilisateur.

Si vous activez cette stratégie, un profil impossible à supprimer est créé avec le compte professionnel ou scolaire de l'utilisateur sous Windows. Ce profil ne peut pas être déconnecté ni supprimé.

Si vous désactivez cette stratégie ou ne la configurez pas, le profil connecté automatiquement avec le compte professionnel ou scolaire d'un utilisateur sous Windows peut être déconnecté ou supprimé par l'utilisateur.

Si vous souhaitez configurer la connexion du navigateur, utilisez la stratégie [BrowserSignin](#browsersignin).

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft ActiveDirectory, des instances de Windows10 Professionnel ou Entreprise qui sont inscrites pour la gestion des appareils.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: NonRemovableProfileEnabled
  - Nom de la stratégie de groupe: configurer la connexion automatique du profil par défaut de l’utilisateur avec son compte professionnel ou scolaire
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: NonRemovableProfileEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)

  ### OverrideSecurityRestrictionsOnInsecureOrigin
  #### Contrôler l’application des restrictions de sécurité aux origines non sécurisées
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifie la liste des origines (URL) ou des modèles de nom d'hôte (tels que «*.contoso.com») pour lesquels des restrictions de sécurité ne s'appliquent pas.

Cette stratégie vous permet de spécifier des origines autorisées pour les applications héritées qui ne peuvent pas déployer TLS ni définir de serveur de gestion intermédiaire pour le développement web interne afin que les développeurs puissent tester les fonctions nécessitant des contextes de sécurité sans devoir déployer TLS sur le serveur de gestion intermédiaire. Cette stratégie empêche également l'origine d'être étiquetée « Non sécurisé » dans l'omnibox.

La définition d'une liste d'URL dans cette stratégie a le même effet que la définition de l'indicateur de ligne de commande «--unsafely-treat-insecure-origin-as-secure» dans une liste d'URL identiques séparées par des virgules. Si vous activez cette stratégie, elle remplace l'indicateur de ligne de commande.

Si vous souhaitez en savoir plus sur les contextes de sécurité, consultez https://www.w3.org/TR/secure-contexts/.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: OverrideSecurityRestrictionsOnInsecureOrigin
  - Nom de la stratégie de groupe: contrôler l'application des restrictions de sécurité aux origines non sécurisées
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: OverrideSecurityRestrictionsOnInsecureOrigin
  - Exemple de valeur:
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PaymentMethodQueryEnabled
  #### Autoriser les sites web à vérifier les modes de paiement disponibles
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Permet de déterminer si les sites web peuvent vérifier si l'utilisateur a enregistré des modes de paiement.

Si vous désactivez cette stratégie, les sites web qui utilisent les API PaymentRequest.canMakePayment ou PaymentRequest.hasEnrolledInstrument seront informés qu'aucun mode de paiement n'est disponible.

Si vous activez cette stratégie ou si vous ne la définissez pas, les sites web peuvent vérifier si les modes de paiement de l'utilisateur sont enregistrés.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PaymentMethodQueryEnabled
  - Nom de la stratégie de groupe: autoriser les sites web à vérifier les modes de paiement disponibles
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: PaymentMethodQueryEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PaymentMethodQueryEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PersonalizationReportingEnabled
  #### Autoriser la personnalisation des publicités, de la recherche et des actualités en envoyant un historique de navigation à Microsoft
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Cette stratégie empêche Microsoft de collecter l'historique de navigation MicrosoftEdge d'un utilisateur pour personnaliser la publicité, la recherche, les actualités et d'autres services Microsoft.

Ce paramètre n'est disponible que pour les utilisateurs disposant d'un compte Microsoft. Ce paramètre n'est pas disponible pour les comptes enfants ou les comptes d'entreprise.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas modifier ou remplacer le paramètre. Si vous activez cette stratégie ou si vous ne la configurez pas, MicrosoftEdge sera par défaut la préférence de l'utilisateur.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PersonalizationReportingEnabled
  - Nom de la stratégie de groupe: autoriser la personnalisation des publicités, de la recherche et des actualités en envoyant un historique de navigation à Microsoft
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: PersonalizationReportingEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PersonalizationReportingEnabled 
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PinningWizardAllowed
  #### Autoriser l’Assistant Épingler à la barre des tâches
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version80 ou versions ultérieures

  #### Description
  MicrosoftEdge utilise l'Assistant Épingler à la barre des tâches pour aider les utilisateurs à épingler les sites suggérés dans la barre des tâches. La fonctionnalité d'Assistant Épingler à la barre des tâches est activée par défaut et accessible par l'utilisateur via le menu Paramètres et plus. 

Si vous activez cette stratégie ou si vous ne la configurez pas, les utilisateurs peuvent appeler l'Assistant Épingler à la barre des tâches à partir du menu Paramètres et plus. L'Assistant peut également être appelé via le lancement d'un protocole.

Si vous désactivez cette stratégie, l'Assistant Épingler à la barre des tâches est désactivé dans le menu et ne peut pas être appelé via le lancement d'un protocole.

Les paramètres utilisateur permettant d'activer ou de désactiver l'Assistant Épingler à la barre des tâches ne sont pas disponibles.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PinningWizardAllowed
  - Nom de la stratégie de groupe: autoriser l'Assistant Épingler à la barre des tâches
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: PinningWizardAllowed
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  

  [Retour au début](#microsoft-edge---policies)

  ### ProactiveAuthEnabled
  #### Activer l’authentification proactive
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Vous permet de configurer l'activation et la désactivation de l'Authentification proactive.

Si vous activez cette stratégie, MicrosoftEdge tente d'authentifier de manière proactive l'utilisateur connecté aux services Microsoft. À intervalles réguliers, MicrosoftEdge recherche sur le service en ligne un manifeste mis à jour contenant la configuration régissant ce comportement.

Si vous désactivez cette stratégie, MicrosoftEdge ne tente pas d'authentifier de manière proactive l'utilisateur connecté aux services Microsoft. MicrosoftEdge ne recherche pas sur le service en ligne un manifeste mis à jour contenant la configuration régissant ce comportement.

Si vous ne configurez pas cette stratégie, l'authentification proactive est activée.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ProactiveAuthEnabled
  - Nom de la stratégie de groupe: activer l'authentification proactive
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ProactiveAuthEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ProactiveAuthEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PromotionalTabsEnabled
  #### Activer le contenu promotionnel dans les onglets
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Contrôler la présentation de contenu pédagogique ou promotionnel dans des onglets. Ce paramètre contrôle la présentation des pages d'accueil qui aident les utilisateurs à se connecter à MicrosoftEdge, à choisir leur navigateur par défaut ou à en savoir plus sur les fonctionnalités du produit.

Si vous activez cette stratégie (définie sur true) ou si vous ne la configurez pas, MicrosoftEdge peut afficher le contenu dans des onglets pour fournir des informations sur le produit.

Si vous désactivez (définissez sur false) cette stratégie, MicrosoftEdge ne peut pas afficher le contenu dans des onglets aux utilisateurs.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PromotionalTabsEnabled
  - Nom de la stratégie de groupe: activer le contenu promotionnel dans les onglets
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: PromotionalTabsEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PromotionalTabsEnabled
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### PromptForDownloadLocation
  #### Demander où enregistrer les fichiers téléchargés
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Indiquez si vous souhaitez demander où un fichier doit être enregistré avant de le télécharger.

Si vous activez cette stratégie, l’utilisateur est interrogé sur l’emplacement d’enregistrement d’un fichier avant chaque téléchargement. Si vous ne la configurez pas, les fichiers sont enregistrés automatiquement dans l’emplacement par défaut, sans demande préalable à l’utilisateur.

Si cette stratégie n’est pas configurée, l’utilisateur peut modifier ce paramètre.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: PromptForDownloadLocation
  - Nom de la stratégie de groupe: demander où enregistrer les fichiers téléchargés
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: PromptForDownloadLocation
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: PromptForDownloadLocation
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### QuicAllowed
  #### Autoriser le protocole QUIC
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Permet d’utiliser le protocole QUIC dans MicrosoftEdge.

Si cette stratégie n’est pas activée ou si elle n’est pas configurée, l'utilisation du protocole QUIC est autorisée.

Si vous désactivez cette stratégie, l'utilisation du protocole QUIC n'est pas autorisée.

QUIC est un protocole réseau de couche de transport qui permet d’améliorer les performances des applications web utilisant actuellement TCP.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: QuicAllowed
  - Nom de la stratégie de groupe: autoriser le protocole QUIC
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: QuicAllowed
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: QuicAllowed
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### RelaunchNotification
  #### Avertir un utilisateur qu’un redémarrage du navigateur est recommandé ou requis pour les mises à jour en attente
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Informez les utilisateurs qu'ils doivent redémarrer MicrosoftEdge pour appliquer une mise à jour en attente. 

Si vous ne configurez pas cette stratégie, MicrosoftEdge ajoute une icône de recyclage à l'extrême droite de la barre de menus supérieure pour inviter les utilisateurs à redémarrer le navigateur afin d'appliquer la mise à jour.

Si vous activez cette stratégie et la définissez sur «Recommended», un avertissement périodique informe les utilisateurs qu'un redémarrage est recommandé. Les utilisateurs peuvent ignorer cet avertissement et reporter le redémarrage.

Si vous définissez la stratégie sur «Required», un avertissement périodique informe les utilisateurs que le navigateur sera redémarré automatiquement dès que la période de notification est passée. La période par défaut est de sept jours. Vous pouvez configurer cette période avec la stratégie [RelaunchNotificationPeriod](#relaunchnotificationperiod). 

La session de l'utilisateur est restaurée au redémarrage du navigateur.

Mappage des options de stratégie:

* Recommended (1)=Recommandé : Afficher un avertissement périodique pour l'utilisateur indiquant qu'un redémarrage est recommandé

* Required (2)=Obligatoire : Afficher un avertissement périodique pour l'utilisateur indiquant qu'un redémarrage est obligatoire

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: RelaunchNotification
  - Nom de la stratégie de groupe: avertir un utilisateur qu'un redémarrage du navigateur est recommandé ou requis pour les mises à jour en attente
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: RelaunchNotification
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: RelaunchNotification
  - Exemple de valeur:
``` xml
<integer>1</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### RelaunchNotificationPeriod
  #### Définir la période d’affichage pour les notifications de mise à jour
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Vous permet de définir la période, en millisecondes, au cours de laquelle les utilisateurs sont avertis que MicrosoftEdge doit être relancé pour appliquer une mise à jour en attente.

Au cours de cette période, l'utilisateur est informé à plusieurs reprises qu'une mise à jour est nécessaire. Dans MicrosoftEdge, le menu de l'application change pour indiquer qu'un redémarrage est nécessaire une fois qu'un tiers de la période de notification est écoulé. Cette notification change de couleur une fois que les deux tiers de la période de notification sont écoulés, puis de nouveau lorsque toute la période de notification est écoulée. Les notifications supplémentaires activées par la stratégie [RelaunchNotification](#relaunchnotification) suivent ce même schéma. 

Si cette valeur n'est pas définie, la période par défaut de 604 800 000 millisecondes (une semaine) est utilisée.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: RelaunchNotificationPeriod
  - Nom de la stratégie de groupe: définir la période d’affichage pour les notifications de mise à jour
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: RelaunchNotificationPeriod
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x240c8400
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: RelaunchNotificationPeriod
  - Exemple de valeur:
``` xml
<integer>604800000</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### RendererCodeIntegrityEnabled
  #### Activer l’intégrité du code du convertisseur
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version78 ou versions ultérieures

  #### Description
  Si cette stratégie est activée ou si elle n'est pas définie, la règle d'intégrité du code du moteur de rendu est activée. Cette stratégie ne doit être désactivée qu'en cas de problèmes de compatibilité avec le logiciel tiers qui doit s'exécuter dans les processus du moteur de rendu de MicrosoftEdge.

Désactiver cette stratégie affectera la sécurité et la stabilité de MicrosoftEdge, car des codes inconnus et potentiellement dangereux pourront être chargés dans les processus de son moteur de rendu.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: RendererCodeIntegrityEnabled
  - Nom de la stratégie de groupe: activer l’intégrité du code du convertisseur
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: RendererCodeIntegrityEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  

  [Retour au début](#microsoft-edge---policies)

  ### RequireOnlineRevocationChecksForLocalAnchors
  #### Spécifier si les vérifications OCSP/CRL en ligne sont requises pour les ancres d’approbation locales
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version77 ou versions ultérieures

  #### Description
  Contrôler la nécessité d’effectuer des vérifications de révocation (OCSP/CRL) en ligne. Si MicrosoftEdge ne peut pas obtenir d’informations sur l’état de la révocation, ces certificats sont traités comme révoqués («échec»).

Si vous activez cette stratégie, MicrosoftEdge exécute toujours une vérification de la révocation des certificats de serveur qui sont correctement validés et qui sont signés par des certificats de signature installés localement.

Si cette stratégie n'est pas configurée ou si elle est désactivée, les paramètres de vérification en ligne de la révocation sont utilisés dans MicrosoftEdge.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: RequireOnlineRevocationChecksForLocalAnchors
  - Nom de la stratégie de groupe: spécifier si les vérifications OCSP/CRL en ligne sont requises pour les ancres d’approbation locales
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: RequireOnlineRevocationChecksForLocalAnchors
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  

  [Retour au début](#microsoft-edge---policies)

  ### ResolveNavigationErrorsUseWebService
  #### Activer la résolution des erreurs de navigation à l’aide d’un service web
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Autorisez MicrosoftEdge à émettre une connexion sans donnée vers un service web pour sonder les réseaux afin de détecter la connectivité, par exemple dans le cas du réseau Wi-Fi d'un hôtel ou d'un aéroport.

Si vous activez cette stratégie, un service web est utilisé pour les tests de connectivité.

Si vous désactivez cette stratégie, MicrosoftEdge utilise les API natives pour tenter de résoudre les problèmes de connectivité au réseau et de navigation.

**Remarque**: sauf dans le cas de Windows8 ou des versions ultérieures de Windows, MicrosoftEdge utilise *toujours* les API natives pour résoudre les problèmes de connectivité.

Si vous ne configurez pas cette stratégie, MicrosoftEdge respecte les préférences de l’utilisateur, définies dans Services sur edge://settings/privacy.
De manière spécifique, il existe un bouton bascule **Utiliser un service web pour résoudre les erreurs de navigation** qui peut être activé ou désactivé par l'utilisateur. Sachez que si vous avez activé cette stratégie (ResolveNavigationErrorsUseWebService), le bouton bascule **Utiliser un service web pour résoudre les erreurs de navigation** est activé, mais l'utilisateur n'est pas en mesure de modifier ce paramètre en utilisant le bouton bascule. Si vous avez désactivé cette stratégie, le paramètre the **Utiliser un service web pour résoudre les erreurs de navigation** est désactivé et l'utilisateur n'est pas en mesure de modifier ce paramètre en utilisant le bouton bascule.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ResolveNavigationErrorsUseWebService
  - Nom de la stratégie de groupe: activer la résolution des erreurs de navigation à l'aide d'un service web
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: ResolveNavigationErrorsUseWebService
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ResolveNavigationErrorsUseWebService
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### RestrictSigninToPattern
  #### Limiter les comptes qui peuvent être utilisés comme comptes principaux sur MicrosoftEdge
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Détermine quels comptes peuvent être configurés comme comptes de navigation principaux sur MicrosoftEdge (par exemple, le compte choisi au moment d'activer la synchronisation).

Le message d'erreur approprié s'affiche et l’utilisateur est bloqué si celui-ci essaie de définir un compte de navigation principal dont l'identifiant ne correspond pas à ce format. Vous pouvez configurer cette stratégie pour qu’elle corresponde à plusieurs comptes à l’aide d’une expression régulière de style Perl pour le motif. Notez que les correspondances de motif respectent la casse. Pour plus d’informations sur les règles d’expression régulière utilisées, voir https://go.microsoft.com/fwlink/p/?linkid=2133903.

Si cette stratégie est laissée vide ou n'est pas configurée, l'utilisateur peut utiliser n'importe quel compte comme compte de navigation principal sur MicrosoftEdge.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: RestrictSigninToPattern
  - Nom de la stratégie de groupe: limiter les comptes qui peuvent être utilisés comme comptes principaux sur MicrosoftEdge
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: RestrictSigninToPattern
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
".*@contoso.com"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: RestrictSigninToPattern
  - Exemple de valeur:
``` xml
<string>.*@contoso.com</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### RoamingProfileLocation
  #### Définition du répertoire de profil itinérant
  
  
  #### Versions prises en charge:
  - Sur Windows depuis la version85 ou versions ultérieures

  #### Description
  Configure l’annuaire à utiliser pour stocker la copie itinérante des profils.

Si vous activez cette stratégie, Microsoft Edge utilise l’annuaire fourni pour stocker une copie itinérante des profils, à partir du moment où vous avez également activé la stratégie de [RoamingProfileSupportEnabled](#roamingprofilesupportenabled). Si vous désactivez la stratégie de [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) ou si vous ne la configurez pas, la valeur stockée dans cette stratégie n’est pas utilisée.

Pour obtenir la liste des variables que vous pouvez utiliser, voir [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Si vous ne configurez pas cette stratégie, le chemin d’accès du profil itinérant par défaut est utilisé.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: RoamingProfileLocation
  - Nom de la stratégie de groupe: définition du répertoire de profil itinérant
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: RoamingProfileLocation
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"${roaming_app_data}\\edge-profile"
```


  

  [Retour au début](#microsoft-edge---policies)

  ### RoamingProfileSupportEnabled
  #### Activer l’utilisation des copies itinérantes pour les données de profil Microsoft Edge
  
  
  #### Versions prises en charge:
  - Sur Windows depuis la version85 ou versions ultérieures

  #### Description
  Activez cette stratégie pour utiliser les profils itinérants sur Windows. Les paramètres stockés dans les profils Microsoft Edge (favoris et préférences) sont également enregistrés dans un fichier stocké dans le dossier de profil utilisateur itinérant (ou l’emplacement spécifié par l’administrateur par le biais de la stratégie de [RoamingProfileLocation](#roamingprofilelocation)).

Si vous désactivez cette stratégie ou si vous ne la configurez pas, seuls les profils locaux standard sont utilisés.

La stratégie [SyncDisabled](#syncdisabled) désactive toute synchronisation de données, en remplaçant la stratégie.

Pour plus d’informations sur l’utilisation des profils utilisateur itinérant, voir https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: RoamingProfileSupportEnabled
  - Nom de la stratégie de protection: activer à l’aide de copies itinérantes pour les données de profil Microsoft Edge
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: RoamingProfileSupportEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)

  ### RunAllFlashInAllowMode
  #### Étendre le paramètre de contenu Adobe Flash à l’ensemble du contenu
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Si vous activez cette stratégie, la totalité du contenu Adobe Flash incorporé dans les sites web définis de manière à autoriser Adobe Flash dans les paramètres de contenu, que ce soit par l'utilisateur ou par la stratégie d'entreprise, est exécutée. Ceci inclut le contenu provenant d'autres origines et/ou du contenu de petite taille.

Pour contrôler les sites web autorisés à exécuter Adobe Flash, consultez les spécifications dans les stratégies [DefaultPluginsSetting](#defaultpluginssetting), [PluginsAllowedForUrls](#pluginsallowedforurls) et [PluginsBlockedForUrls](#pluginsblockedforurls). 

Si vous désactivez cette stratégie ou si vous ne la configurez pas, le contenu Adobe Flash provenant d'autres origines (provenant de sites qui ne sont pas spécifiés dans les trois stratégies mentionnées ci-dessus) ou le contenu de petite taille risque d'être bloqué.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: RunAllFlashInAllowMode
  - Nom de la stratégie de groupe: étendre le paramètre de contenu Adobe Flash à l'ensemble du contenu
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: RunAllFlashInAllowMode
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: RunAllFlashInAllowMode
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SSLErrorOverrideAllowed
  #### Autoriser les utilisateurs à poursuivre la navigation depuis une page d’avertissement SSL
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  MicrosoftEdge affiche une page d'avertissement lorsque les utilisateurs consultent des sites présentant des erreurs SSL.

Si vous activez ou ne configurée par cette stratégie (configuration par défaut), les utilisateurs sont autorisés à poursuivre leur navigation vers la page concernée.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas poursuivre leur navigation au-delà de la page d'avertissement.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SSLErrorOverrideAllowed
  - Nom de la stratégie de groupe: autoriser les utilisateurs à poursuivre la navigation depuis une page d'avertissement SSL
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: SSLErrorOverrideAllowed
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SSLErrorOverrideAllowed
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SSLVersionMin
  #### Version TLS minimale activée
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Définit la version minimale de TLS prise en charge. Si vous ne configurez pas cette stratégie, MicrosoftEdge utilise la version minimale par défaut qui est TLS 1.0. 

Si vous activez cette stratégie, MicrosoftEdge n'utilise pas de versions SSL/TLS antérieures à la version précisée. Toute valeur non reconnue sera ignorée.

Mappage des options de stratégie:

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SSLVersionMin
  - Nom de la stratégie de groupe: version TLS minimale activée
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: SSLVersionMin
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"tls1"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SSLVersionMin
  - Exemple de valeur:
``` xml
<string>tls1</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SaveCookiesOnExit
  #### Enregistrer les cookies lors de la fermeture de MicrosoftEdge
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Lorsque cette stratégie est activée, le groupe de cookies spécifié est exempt de la suppression lorsque le navigateur se ferme. Cette stratégie ne s’applique que lorsque:
- L’activation/désactivation de «Cookies et autres données de site» est configurée dans Paramètres/Confidentialité et services/Effacer les données de navigation à la fermeture ou
- La stratégie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) est activée ou
- La stratégie [DefaultCookiesSetting](#defaultcookiessetting) est définie sur «Conserver les cookies pendant la durée de la session».

Vous pouvez définir une liste de sites sur la base des modèles d’URL dont les cookies seront conservés entre les sessions.

Remarque: Les utilisateurs peuvent encore modifier la liste des sites de cookies pour ajouter ou supprimer des URL. Toutefois, ils ne peuvent pas supprimer les URL ajoutées par un administrateur.

Si vous activez cette stratégie, la liste de cookies n’est pas supprimée lorsque le navigateur se ferme.

Si vous désactivez ou ne configurez pas cette stratégie, la configuration personnelle de l’utilisateur est utilisée.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom de la stratégie de groupe: SaveCookiesOnExit
  - Nom la stratégie de groupe: Enregistrer les cookies lors de la fermeture de MicrosoftEdge
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: SaveCookiesOnExit
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SavingBrowserHistoryDisabled
  #### Désactiver l’enregistrement de l’historique du navigateur
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Désactive l'enregistrement de l'historique du navigateur et empêche les utilisateurs de modifier ce paramètre.

Si cette stratégie est activée, l'historique de navigation n'est pas enregistré. Elle désactive également la synchronisation des onglets. 

Si cette stratégie est désactivée ou n'est pas configurée, l'historique de navigation est enregistré.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SavingBrowserHistoryDisabled
  - Nom de la stratégie de groupe: désactiver l’enregistrement de l’historique du navigateur
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: SavingBrowserHistoryDisabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SavingBrowserHistoryDisabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ScreenCaptureAllowed
  #### Autoriser ou interdire la capture d’écran
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version83 ou versions ultérieures

  #### Description
  Si vous activez cette stratégie ou ne la configurez pas, une page web peut utiliser des API de partage d’écran (par exemple, getDisplayMedia() ou l’API d’extension de capture de bureau) pour faire une capture d’écran.
Si vous désactivez cette stratégie, les appels aux API de partage d'écran échoueront. Par exemple, si vous organisez une réunion en ligne sur le web, le partage de vidéo ou d'écran ne fonctionnera pas.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ScreenCaptureAllowed
  - Nom de la stratégie de groupe: autoriser ou interdire la capture d’écran
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ScreenCaptureAllowed
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ScreenCaptureAllowed
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ScrollToTextFragmentEnabled
  #### Activer le défilement jusqu’au texte spécifié dans les fragments d’URL
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version83 ou versions ultérieures

  #### Description
  Cette fonctionnalité permet aux hyperliens et aux URL de la barre d'adresse de cibler du texte spécifique sur une page web, sur lequel l’utilisateur sera amené à la fin du chargement de la page web.

Si vous activez ou ne configurez pas cette stratégie, le défilement de pages web vers des fragments de texte spécifiques via une URL est activé.

Si vous désactivez cette stratégie, le défilement de pages web vers des fragments de texte spécifiques via une URL est désactivé.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ScrollToTextFragmentEnabled
  - Nom de la stratégie de groupe: activer le défilement jusqu’au texte spécifié dans les fragments d’URL
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ScrollToTextFragmentEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ScrollToTextFragmentEnabled
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SearchSuggestEnabled
  #### Activer les suggestions de recherche
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Active les suggestions de recherche dans la barre d'adresse de MicrosoftEdge et empêche les utilisateurs de modifier ce paramètre.

Si vous activez cette stratégie, les suggestions de recherche web sont utilisées.

Si vous désactivez cette stratégie, les suggestions de recherche web ne sont jamais utilisées mais l'historique local et les suggestions de favoris locaux apparaissent toujours. Si vous désactivez cette stratégie, ni les caractères tapés, ni les URL visitées ne sont inclus dans la télémétrie vers Microsoft.

Si cette règle n'est pas configurée, ce paramètre est activé, mais l'utilisateur est en mesure de le modifier.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SearchSuggestEnabled
  - Nom de la stratégie de groupe: activer les suggestions de recherche
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: SearchSuggestEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SearchSuggestEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SecurityKeyPermitAttestation
  #### Sites web ou domaines automatiquement autorisés à utiliser l’attestation de clé de sécurité directe
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifie les sites web et les domaines qui ne nécessitent pas d'autorisation utilisateur explicite lorsque des certificats d'attestation provenant des clés de sécurité sont obligatoires. En outre, un signal est envoyé à la clé de sécurité indiquant qu'elle peut utiliser l'attestation individuelle. Sans cela, les utilisateurs sont invités chaque fois qu'un site demande une attestation de clés de sécurité. 

Les sites (par exemple, https://contoso.com/some/path)) ne correspondent qu'en tant qu'appID U2F. Les domaines (par exemple, contoso.com) ne correspondent qu'en tant qu'ID RP webauthn. Pour couvrir à la fois les API U2F et webauthn pour un site donné, vous devez répertorier les domaines et URL appID.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SecurityKeyPermitAttestation
  - Nom de la stratégie de groupe: sites web ou domaines automatiquement autorisés à utiliser l'attestation de clé de sécurité directe
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SecurityKeyPermitAttestation
  - Exemple de valeur:
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SendIntranetToInternetExplorer
  #### Envoyer tous les sites intranet vers Internet Explorer
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version77 ou versions ultérieures

  #### Description
  Si vous souhaitez obtenir des instructions sur la configuration optimale de l'expérience pour Internet Explorer, consultez [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SendIntranetToInternetExplorer
  - Nom de la stratégie de groupe: envoyer tous les sites intranet vers Internet Explorer
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: SendIntranetToInternetExplorer
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)

  ### SendSiteInfoToImproveServices
  #### Envoyer des informations sur les sites pour améliorer les services Microsoft (déconseillé)
  >DÉCONSEILLÉ: cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans la version MicrosoftEdge89. Cette stratégie est remplacée par la nouvelle stratégie:  [DiagnosticData](#diagnosticdata) pour Windows7, Windows8 et macOS. Cette stratégie est remplacée par Autoriser la télémétrie sur Windows10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

Cette stratégie permet d'envoyer à Microsoft des informations sur les sites web visités dans MicrosoftEdge afin d'améliorer les services, tels que la recherche.

Activez cette stratégie pour envoyer à Microsoft des informations sur les sites web visités dans MicrosoftEdge. Désactivez cette stratégie pour ne pas envoyer à Microsoft d'informations sur les sites web visités dans MicrosoftEdge. Dans un cas comme dans l’autre, les utilisateurs ne peuvent pas modifier ou remplacer le paramètre.

Dans Windows10, MicrosoftEdge prendra par défaut le paramètre de données de diagnostic Windows, si vous ne configurez cette stratégie. Si cette stratégie est activée, MicrosoftEdge n'envoie que des informations sur les sites web visités dans MicrosoftEdge si le paramètre Données de diagnostic Windows est défini sur Complet. Si cette stratégie est désactivée, MicrosoftEdge n’enverra pas d’informations concernant les sites web visités. Si vous souhaitez en savoir plus sur les paramètres de données de diagnostic Windows, rendez-vous sur: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Sous Windows7, Windows8 et macOS, cette stratégie contrôle l'envoi d'informations sur les sites web visités. Si vous ne configurez pas cette stratégie, MicrosoftEdge est défini par défaut sur les préférences de l’utilisateur.

Pour activer cette stratégie, [MetricsReportingEnabled](#metricsreportingenabled) doit être défini sur Activé. Si [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) ou [MetricsReportingEnabled](#metricsreportingenabled) est défini comme Non configuré ou Désactivé, ces données ne sont pas envoyées à Microsoft.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SendSiteInfoToImproveServices
  - Nom de la stratégie de groupe: Envoyer des informations sur les sites pour améliorer les services Microsoft (déconseillé)
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: SendSiteInfoToImproveServices
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SendSiteInfoToImproveServices
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SensorsAllowedForUrls
  #### Autoriser l’accès aux capteurs sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Déterminer une liste de sites, basée sur des modèles d’URL, qui peuvent accéder et utiliser des capteurs tels que des capteurs de mouvement et de luminosité.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultSensorsSetting](#defaultsensorssetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

Pour les modèles d’URL qui ne correspondent pas à cette stratégie, l’ordre de priorité suivant est utilisé: la stratégie [SensorsBlockedForUrls](#sensorsblockedforurls) (s’il y a une correspondance), la stratégie [DefaultSensorsSetting](#defaultsensorssetting) (si elle est définie) ou les paramètres personnels de l’utilisateur.

Les modèles d’URL définis dans cette stratégie ne peuvent pas entrer en conflit avec ceux configurés dans la stratégie [SensorsBlockedForUrls](#sensorsblockedforurls). Vous ne pouvez pas autoriser et bloquer une URL.

Si vous souhaitez obtenir plus d’informations concernant les modèles d’URL valides, consultez [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SensorsAllowedForUrls
  - Nom de la stratégie de groupe: autoriser l’accès aux capteurs sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de préférence: SensorsAllowedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SensorsBlockedForUrls
  #### Bloquer l’accès aux capteurs sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Déterminer une liste de sites, basée sur des modèles d’URL, qui ne peuvent pas accéder aux capteurs tels que les capteurs de mouvement et de luminosité.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultSensorsSetting](#defaultsensorssetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

Pour les modèles d’URL qui ne correspondent pas à cette stratégie, l’ordre de priorité suivant est utilisé: la stratégie [SensorsAllowedForUrls](#sensorsallowedforurls) (s’il existe une correspondance), la stratégie [DefaultSensorsSetting](#defaultsensorssetting) (si définie) ou les paramètres personnels de l’utilisateur.

Les modèles d’URL définis dans cette stratégie ne peuvent pas entrer en conflit avec ceux configurés dans la stratégie [SensorsAllowedForUrls](#sensorsallowedforurls). Vous ne pouvez pas autoriser et bloquer une URL.

Si vous souhaitez obtenir plus d’informations concernant les modèles d’URL valides, consultez [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SensorsBlockedForUrls
  - Nom de la stratégie: bloquer l’accès aux capteurs sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de préférence: SensorsBlockedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SerialAskForUrls
  #### Autoriser l’API Serial sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Déterminer une liste de sites, basée sur des modèles d’URL, qui peuvent demander à l’utilisateur d’accéder à un port série.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultSerialGuardSetting](#defaultserialguardsetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

Pour les modèles d’URL qui ne correspondent pas à cette stratégie, l’ordre de priorité suivant est utilisé: la stratégie [SerialBlockedForUrls](#serialblockedforurls) (s’il y a une correspondance), la stratégie [DefaultSerialGuardSetting](#defaultserialguardsetting) (si elle est définie) ou les paramètres personnels de l’utilisateur.

Les modèles d’URL définis dans cette stratégie ne peuvent pas entrer en conflit avec ceux configurés dans la stratégie [SerialBlockedForUrls](#serialblockedforurls). Vous ne pouvez pas autoriser et bloquer une URL.

Si vous souhaitez obtenir plus d’informations sur les modèles d’URL valides, consultez [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SerialAskForUrls
  - Nom de la stratégie: autoriser l’API Serial sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de préférence: SerialAskForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SerialBlockedForUrls
  #### Bloquer l’API Serial sur des sites spécifiques
  
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Déterminer une liste de sites, basée sur des modèles d’URL, qui ne peuvent pas demander à l’utilisateur de lui accorder l’accès à un port série.

Si cette stratégie n’est pas configurée, la valeur par défaut globale sera utilisée pour tous les sites à partir de la stratégie [DefaultSerialGuardSetting](#defaultserialguardsetting), si elle est définie, ou à défaut, à partir de la configuration personnelle de l’utilisateur.

Pour les modèles d’URL qui ne correspondent pas à cette stratégie, l’ordre de priorité suivant est utilisé: la stratégie [SerialAskForUrls](#serialaskforurls) (s’il y a une correspondance), la stratégie [DefaultSerialGuardSetting](#defaultserialguardsetting) (si elle est définie) ou les paramètres personnels de l’utilisateur.

Les modèles d’URL dans cette stratégie ne peuvent pas être en conflit avec ceux configurés dans la stratégie [SerialAskForUrls](#serialaskforurls). Vous ne pouvez pas autoriser et bloquer une URL.

Si vous souhaitez obtenir plus d’informations sur les modèles d’URL valides, consultez [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SerialBlockedForUrls
  - Nom de la stratégie: bloquer l’API Serial sur des sites spécifiques
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informations et paramètres sur Mac
  - Nom clé de préférence: SerialBlockedForUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### ShowOfficeShortcutInFavoritesBar
  #### Afficher le raccourci MicrosoftOffice dans la barre des favoris (déconseillé)
  >DÉCONSEILLÉ: cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Cette stratégie ne fonctionnait pas comme prévu en raison de modifications apportées aux besoins opérationnels. Therefore it's deprecated and should not be used.

Indique s'il faut inclure un raccourci vers Office.com dans la barre des favoris. For users signed into Microsoft Edge the shortcut takes users to their Microsoft Office apps and docs. If you enable or don't configure this policy, users can choose whether to see the shortcut by changing the toggle in the favorites bar context menu.
Si vous désactivez cette stratégie, le raccourci n’apparaît pas.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: ShowOfficeShortcutInFavoritesBar
  - Nom de la stratégie de groupe: afficher le raccourci MicrosoftOffice dans la barre des favoris (déconseillé)
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: ShowOfficeShortcutInFavoritesBar
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: ShowOfficeShortcutInFavoritesBar
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SignedHTTPExchangeEnabled
  #### Activer la prise en charge de Signed HTTP Exchange (SXG) 
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version78 ou versions ultérieures

  #### Description
  Activez la prise en charge pour Signed HTTP Exchange (SXG).

Si cette stratégie n'est pas définie ou activée, MicrosoftEdge accepte les contenus web servis en tant que Signed HTTP Exchanges.

Si cette stratégie est désactivée, Signed HTTP Exchanges ne peut pas être chargé.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SignedHTTPExchangeEnabled
  - Nom de la stratégie de groupe: activer la prise en charge de Signed HTTP Exchange (SXG) 
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: SignedHTTPExchangeEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SignedHTTPExchangeEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SitePerProcess
  #### Activer l’isolation de site pour tous les sites
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  La stratégie SitePerProcess peut être employée pour empêcher les utilisateurs de désactiver le comportement par défaut qui isole tous les sites. Vous pouvez également utiliser la stratégie [IsolateOrigins](#isolateorigins) pour isoler d'autres origines de manière plus précise. 

Si la règle est activée, les utilisateurs ne peuvent pas désactiver le comportement par défaut, dans lequel chaque site exécute son propre processus.

Si cette règle n'est pas configurée ou si elle est désactivée, les utilisateurs peuvent désactiver l'isolation de sites.  (Par exemple, en accédant à l'option «Désactiver l'isolation de sites» sur edge://flags.) Le fait de désactiver cette règle, ou de ne pas la configurer, ne désactive pas l'isolation de sites. 


  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SitePerProcess
  - Nom de la stratégie de groupe: activer l'isolation de site pour tous les sites
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: SitePerProcess
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SitePerProcess
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SpellcheckEnabled
  #### Activer la vérification orthographique
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Si cette stratégie est activée ou si elle n’est pas configurée, les utilisateurs peuvent utiliser la vérification orthographique.

Si vous désactivez cette stratégie, l’utilisateur ne peut pas utiliser la vérification orthographique et les stratégies [SpellcheckLanguage](#spellchecklanguage) et [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) sont également désactivées.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SpellcheckEnabled
  - Nom de la stratégie de groupe: activer la vérification orthographique
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: SpellcheckEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SpellcheckEnabled
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SpellcheckLanguage
  #### Activer des langues spécifiques pour la vérification orthographique
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version77 ou versions ultérieures

  #### Description
  Active des langues différentes pour la vérification orthographique. Les langues spécifiées qui ne sont pas reconnues sont ignorées.

Si vous activez cette stratégie, la vérification orthographique est activée pour les langues spécifiées, ainsi que pour les langues que l'utilisateur a activées.

Si vous ne configurez pas ou si vous désactivez cette stratégie, aucune modification n'est apportée aux préférences de vérification orthographique de l'utilisateur.

Si la stratégie [SpellcheckEnabled](#spellcheckenabled) est désactivée, cette stratégie n'aura aucun effet.

Si une langue est incluse dans les deux stratégies «SpellcheckLanguage» et [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist), la langue du vérificateur orthographique est activée.

Les langues prises en charge sont les suivantes : af, bg, ca, cs, cy, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SpellcheckLanguage
  - Nom de la stratégie de groupe: activer des langues spécifiques pour la vérification orthographique
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```


  

  [Retour au début](#microsoft-edge---policies)

  ### SpellcheckLanguageBlocklist
  #### Forcer la désactivation de langues spécifiques pour la vérification orthographique
  
  
  #### Versions prises en charge:
  - sur Windows depuis la version78 ou versions ultérieures

  #### Description
  Désactive de force les langues de la vérification orthographique. Les langues non reconnues dans cette liste seront ignorées.

Si vous activez cette stratégie, la vérification orthographique est désactivée pour les langues spécifiées. L'utilisateur peut toujours activer ou désactiver la vérification orthographique pour les langues qui ne sont pas dans la liste.

Si vous ne définissez pas cette stratégie ou si vous la désactivez, les préférences de la vérification orthographique de l'utilisateur ne sont pas modifiées.

Si la stratégie [SpellcheckEnabled](#spellcheckenabled) est désactivée, cette stratégie n'a aucun effet. 

Si une langue est incluse, à la fois, dans les stratégies [SpellcheckLanguage](#spellchecklanguage) et «SpellcheckLanguageBlocklist», la langue de la vérification orthographique est activée.

Les langues actuellement prises en charge sont les suivantes: af, bg, ca, cs, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SpellcheckLanguageBlocklist
  - Nom de la stratégie de groupe: forcer la désactivation de langues spécifiques pour la vérification orthographique
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```


  

  [Retour au début](#microsoft-edge---policies)

  ### StricterMixedContentTreatmentEnabled
  #### Activer l’utilisation d’un traitement plus strict pour les contenus mixtes (déconseillé)
  >DÉCONSEILLÉ: cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version81 ou versions ultérieures

  #### Description
  Cette stratégie est déconseillée, car elle n’est destinée qu’à être un mécanisme à court terme permettant aux entreprises de mettre à jour leur contenu web si et quand il est jugé incompatible avec un traitement de contenu mixte plus strict. Il ne fonctionne pas dans la version 85 de Microsoft Edge.

Cette stratégie contrôle le traitement du contenu mixte (contenu HTTP dans les sites HTTPS) dans le navigateur.

Si vous définissez cette stratégie sur true ou si vous ne la configurez pas, le contenu mixte audio et vidéo est automatiquement mis à jour vers HTTPS (c'est-à-dire que l'URL sera réécrite en tant que HTTPS, sans substitution si la ressource n'est pas disponible via HTTPS) et un avertissement «non sécurisé» s'affiche dans la barre d'URL pour le contenu d'image mixte.

Si vous définissez la stratégie sur false, les mises à jour automatiques sont désactivées pour l'audio et la vidéo, et aucun avertissement ne s'affiche pour les images.

Cette stratégie n'affecte pas les autres types de contenu mixte autres que l'audio, la vidéo et les images. 

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: StricterMixedContentTreatmentEnabled
  - Nom de stratégie de groupe: Activer l’utilisation d’un traitement plus strict pour les contenus mixtes (déconseillé)
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: StricterMixedContentTreatmentEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: StricterMixedContentTreatmentEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SuppressUnsupportedOSWarning
  #### Supprimer l’avertissement relatif au système d’exploitation non pris en charge
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Supprime l'avertissement qui s'affiche lorsque MicrosoftEdge s'exécute sur un ordinateur ou un système d'exploitation qui n'est plus accepté.

Si cette stratégie est définie sur false ou si elle n'est pas définie, les avertissements s'affichent sur les ordinateurs ou les systèmes d'exploitation non pris en charge.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SuppressUnsupportedOSWarning
  - Nom de la stratégie de groupe: supprimer l'avertissement relatif au système d'exploitation non pris en charge
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: SuppressUnsupportedOSWarning
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SuppressUnsupportedOSWarning
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SyncDisabled
  #### Désactiver la synchronisation des données à l’aide des services de synchronisation Microsoft
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Désactive la synchronisation des données dans MicrosoftEdge. Cette stratégie empêche également l'invite de consentement de synchronisation d'apparaître.

Si vous configurez pas cette stratégie, ou si vous ne la configurez pas de la façon recommandée, les utilisateurs peuvent activer ou désactiver la synchronisation. Si vous définissez cette stratégie comme étant obligatoire, les utilisateurs ne pourront pas activer la synchronisation.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SyncDisabled
  - Nom de la stratégie de groupe: désactiver la synchronisation des données à l'aide des services de synchronisation Microsoft
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: SyncDisabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SyncDisabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### SyncTypesListDisabled
  #### Configurer la liste des types exclus de la synchronisation
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version83 ou versions ultérieures

  #### Description
  Si vous activez cette stratégie, tous les types de données spécifiés sont exclus de la synchronisation. Cette stratégie peut être utiliser pour limiter le type de données téléchargées vers le service de synchronisation MicrosoftEdge.

Vous pouvez définir l’un des types de données suivants pour cette stratégie: «favoris», «paramètres», «mots de passe», «addressesAndMore», «extensions», «historique», «openTabs» et «Collections». Les noms des types de données sont sensibles à la casse.

Les utilisateurs ne peuvent pas remplacer les types de données désactivés.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: SyncTypesListDisabled
  - Nom de la stratégie de groupe: configurer la liste des types exclus de la synchronisation
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: SyncTypesListDisabled
  - Exemple de valeur:
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### TLS13HardeningForLocalAnchorsEnabled
  #### Activer une fonctionnalité de sécurité TLS1.3 pour les ancres d’approbation locales (obsolète)
  
  >OBSOLÈTE: Cette stratégie est obsolète et ne fonctionne pas après la version85 de MicrosoftEdge.
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version81 et jusqu’à la version85

  #### Description
  Cette stratégie ne fonctionne pas, car elle n’a pour but qu’être un mécanisme à court terme pour offrir aux entreprises davantage de temps pour la mise à niveau des proxys affectés.

Cette stratégie contrôle une fonctionnalité de sécurité TLS 1.3 qui protège les connexions contre les attaques par déclassement. Elle est rétrocompatible et n'affecte pas les connexions à des serveurs ou proxys conformes aux normes TLS 1.2. Toutefois, les versions plus anciennes de certains proxys interceptant les paramètres TLS sont incompatibles en raison de défauts d'intégration. 

Si vous activez cette stratégie ou si vous ne la configurez pas, MicrosoftEdge active ces protections de sécurité pour toutes les connexions. 

Si vous désactivez cette stratégie, MicrosoftEdge désactive ces protections de sécurité pour les connexions authentifiées par des certificats de signature installés localement. Ces protections sont toujours activées pour les connexions authentifiées par des certificats de signature reconnus publiquement. 

Cette stratégie peut être utilisée pour tester les proxys concernés et les mettre à jour. En principe, les proxys affectés provoqueront un échec de connexion avec le code d'erreur "ERR_TLS13_DOWNGRADE_DETECTED".

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: TLS13HardeningForLocalAnchorsEnabled
  - Nom de la stratégie de groupe: Activer une fonctionnalité de sécurité TLS1.3 pour les ancres d’approbation locales (obsolète)
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: TLS13HardeningForLocalAnchorsEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: TLS13HardeningForLocalAnchorsEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### TLSCipherSuiteDenyList
  #### Spécifier les suites de chiffrement TLS à désactiver
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version85 ou versions ultérieures

  #### Description
  Configurez la liste des suites de chiffrement désactivées pour les connexions TLS.

Si vous configurez cette stratégie, la liste des suites de chiffrement configurées ne sera pas utilisée lors de l’établissement de connexions TLS.

Si vous ne configurez pas cette stratégie, le navigateur choisit les suites de chiffrement TLS à utiliser.

Les valeurs de la suite de chiffrement à désactiver sont spécifiées en tant que valeurs hexadécimales 16 bits. Les valeurs sont affectées par le registre IANA (Internet Assigned Numbers Authority).

La suite de chiffrement TLS 1,3 TLS_AES_128_GCM_SHA256 (0x1301) est nécessaire pour TLS 1,3 et ne peut pas être désactivée par cette stratégie.

Cette stratégie n’affecte pas les connexions basées sur QUIC. QUIC peut être désactivé par le biais de la stratégie [QuicAllowed](#quicallowed).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: TLSCipherSuiteDenyList
  - Nom de la stratégie de protection: spécifier les suites de chiffrement TLS à désactiver
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: TLSCipherSuiteDenyList
  - Exemple de valeur:
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### TabFreezingEnabled
  #### Autoriser le gel des onglets d’arrière-plan
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version79 ou versions ultérieures

  #### Description
  Détermine si MicrosoftEdge peut geler ou non des onglets qui sont en arrière-plan depuis au moins cinq minutes. 

Le gel des onglets permet de moins solliciter le processeur, la batterie et la mémoire. MicrosoftEdge utilise des heuristiques pour ne pas figer les onglets qui exécutent une tâche utile en arrière-plan, comme l'affichage de notifications, la lecture audio et la diffusion d'une vidéo en streaming. 

Si vous activez ou ne configurez pas cette stratégie, les onglets qui s’affichent en arrière-plan pendant au moins 5 minutes peuvent être figés.

Si vous désactivez cette stratégie, aucun onglet n’est figé.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: TabFreezingEnabled
  - Nom de la stratégie de groupe: autoriser le gel des onglets d'arrière-plan
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: TabFreezingEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: TabFreezingEnabled
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### TaskManagerEndProcessEnabled
  #### Activer la possibilité de mettre fin aux processus dans le gestionnaire des tâches
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Si vous activez ou ne configurez pas cette stratégie, les utilisateurs peuvent arrêter les processus dans le gestionnaire de tâches du navigateur. Si vous la désactivez, les utilisateurs ne peuvent pas terminer les processus, et le bouton terminer le processus est désactivé dans le gestionnaire de tâches du navigateur.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: TaskManagerEndProcessEnabled
  - Nom de la stratégie de groupe: activer la possibilité de mettre fin aux processus dans le gestionnaire des tâches
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: TaskManagerEndProcessEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: TaskManagerEndProcessEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### TotalMemoryLimitMb
  #### Définir une limite de mémoire en mégaoctets qu’une seule instance de MicrosoftEdge peut utiliser
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Configure la quantité de mémoire qu'une instance de MicrosoftEdge peut utiliser avant que des onglets ne commencent à être ignorés afin d'économiser de la mémoire.  La mémoire utilisée par l’onglet est libérée et l’onglet doit être réactualisé lorsqu’il sera sélectionné.

Si vous activez cette stratégie, le navigateur commence à ignorer des onglets pour économiser de la mémoire lorsque la limite est dépassée. Il n'est cependant pas garanti que le navigateur fonctionne toujours en deçà de cette limite. Toute valeur inférieure à 1024 est arrondie à ce nombre.

Si vous ne configurez pas cette stratégie, le navigateur ne commence à économiser de la mémoire que s'il détecte que la quantité de mémoire physique sur l'ordinateur est faible.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: TotalMemoryLimitMb
  - Nom de la stratégie de groupe: définir une limite de mémoire en mégaoctets qu'une seule instance de MicrosoftEdge peut utiliser
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: TotalMemoryLimitMb
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000800
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: TotalMemoryLimitMb
  - Exemple de valeur:
``` xml
<integer>2048</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### TrackingPrevention
  #### Bloquer le suivi de l’activité de navigation sur le web des utilisateurs
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version78 ou versions ultérieures

  #### Description
  Vous permet de décider de bloquer les sites web effectuant le suivi des activités de navigation des utilisateurs.

Si vous désactivez cette stratégie ou ne la configurez pas, les utilisateurs peuvent définir leur propre niveau de prévention du suivi.

Mappage des options de stratégie:

* TrackingPreventionOff (0) = Désactivé (pas de prévention de suivi)

* TrackingPreventionBasic (1)=Basique (bloque les suivis malveillants, le contenu et les publicités seront personnalisés)

* TrackingPreventionBalanced (2)=Équilibré (bloque les suivis malveillants et les suivis des sites Web que l'utilisateur n'a pas visités ; le contenu et les publicités seront moins personnalisés)

* TrackingPreventionStrict (3)=Strict (bloque les suivis malveillants et la majorité des suivis de tous les sites ; le contenu et les publicités auront une personnalisation minimale) Certaines parties des sites pourront ne pas fonctionner) 

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: TrackingPrevention
  - Nom de la stratégie de groupe: bloquer le suivi de l'activité de navigation sur le web des utilisateurs
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: TrackingPrevention
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000002
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: TrackingPrevention
  - Exemple de valeur:
``` xml
<integer>2</integer>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### TranslateEnabled
  #### Activer la traduction
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Active le service de traduction Microsoft intégré sur MicrosoftEdge.

Si vous activez cette stratégie, MicrosoftEdge propose à l’utilisateur une fonctionnalité intégrée de traduction, qui s’affiche grâce à un menu déroulant de traduction intégré, le cas échéant, ou une option de traduction disponible dans le menu contextuel que l'utilisateur peut afficher en effectuant un clic droit.

Si vous désactivez cette stratégie, toutes les fonctionnalités intégrées de traduction sont désactivées.

Si vous ne configurez pas la stratégie, les utilisateurs peuvent décider d'utiliser ou non la fonctionnalité de traduction.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Oui
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: TranslateEnabled
  - Nom de la stratégie de groupe: activer la traduction
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): Administrative Templates/Microsoft Edge - Default Settings (peut être remplacé par les utilisateurs)/
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Nom de la valeur: TranslateEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: TranslateEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### URLAllowlist
  #### Définir une liste d’URL autorisées
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Autorisez l'accès aux URL répertoriées comme des exceptions à la liste rouge des URL.

Le format d'un modèle d’URL doit être conforme aux règles stipulées à l'adresse [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Vous pouvez utiliser cette stratégie pour ouvrir des exceptions aux listes rouges restrictives. Par exemple, vous pouvez inclure «*» dans la liste rouge pour bloquer toutes les requêtes, puis utiliser cette stratégie pour autoriser l'accès à une liste limitée d'URL. Vous pouvez utiliser cette stratégie pour ouvrir des exceptions pour certains schémas, sous-domaines d'autres domaines, ports ou chemins d'accès spécifiques.

Le filtre plus spécifique détermine si une URL est bloquée ou autorisée. La liste verte prévaut sur la liste rouge.

Cette stratégie est limitée à 1000 entrées. Les entrées suivantes sont ignorées. 

Cette stratégie permet également au navigateur d’appeler automatiquement les applications externes enregistrées comme gestionnaires de protocoles pour des protocoles tels que «tel:» ou «ssh:».

Si vous ne configurez pas cette stratégie, il n'existe aucune exception à la liste rouge dans la stratégie [URLBlocklist](#urlblocklist).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: URLAllowlist
  - Nom de la stratégie de groupe: définir une liste d’URL autorisées
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: URLAllowlist
  - Exemple de valeur:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### URLBlocklist
  #### Bloquer l’accès à une liste d’URL
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Définissez la liste des sites, en fonction des modèles d'URL, qui sont bloqués (les utilisateurs ne peuvent pas les charger).

Le format d'un modèle d’URL doit être conforme aux règles stipulées à l'adresse [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Vous pouvez définir des exceptions dans la stratégie [URLAllowlist](#urlallowlist). Ces stratégies sont limitées à 1000 entrées. Les entrées suivantes sont ignorées.

Notez qu'il est déconseillé de bloquer les URL internes «edge://*» car cela peut entraîner des erreurs inattendues.

Cette stratégie n'empêche pas la mise à jour dynamique de la page par le biais de JavaScript. Par exemple, si vous bloquez «contoso.com/abc», les utilisateurs pourront toujours visiter «contoso.com» et cliquer sur un lien pour accéder à «contoso.com/abc» tant que la page n'a pas été actualisée. 

Si vous ne configurez pas cette stratégie, aucune URL n'est bloquée.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: URLBlocklist
  - Nom de la stratégie de groupe: bloquer l’accès à une liste d’URL
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\3 = "hosting.com/bad_path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\5 = ".exact.hostname.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\6 = "file://*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\7 = "custom_scheme:*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\8 = "*"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: URLBlocklist
  - Exemple de valeur:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/bad_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
  <string>file://*</string>
  <string>custom_scheme:*</string>
  <string>*</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### UserAgentClientHintsEnabled
  #### Activer la fonctionnalité User-Agent Client Hints (déconseillé)
  >DÉCONSEILLÉ: cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge:
  - Sur Windows et macOS depuis la version86 ou ultérieur

  #### Description
  Cette stratégie est déconseillée, car elle a pour but de servir uniquement comme mécanisme à court terme afin d’offrir aux entreprises davantage de temps pour mettre à jour leurs environnements si et quand ils sont détectés comme étant incompatibles avec la fonctionnalité User-Agent Client Hints. Elle ne fonctionne pas dans la version89 de MicrosoftEdge.

Lorsque la fonctionnalité User-Agent Client Hints est activée, des en-têtes de demande granulaires sont envoyés, ils fournissent des informations sur le navigateur de l’utilisateur (par exemple la version du navigateur) et l’environnement (par exemple l’architecture système).

Il s’agit d’une fonctionnalité supplémentaire, mais les nouveaux en-têtes peuvent provoquer des disfonctionnements sur certains sites Web qui restreignent les caractères que les demandes peuvent contenir.

Si vous activez ou ne configurez pas cette stratégie, la fonctionnalité User-Agent Client Hints est activée. Si vous désactivez cette stratégie, cette fonctionnalité n’est pas disponible.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP : UserAgentClientHintsEnabled
  - Nom de la stratégie de groupe: Activer la fonctionnalité User-Agent Client Hints (déconseillé)
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur : UserAgentClientHintsEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom de la clé de préférence: UserAgentClientHintsEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### UserDataDir
  #### Définir le répertoire de données utilisateur
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Définit l’annuaire à utiliser pour stocker les données de l’utilisateur.

Si vous activez cette stratégie, MicrosoftEdge utilise le répertoire fourni, que l'utilisateur ait ou non spécifié l'indicateur de ligne de commande "--disk-cache-dir".

Si vous n’activez pas cette stratégie, le chemin d’accès du profil par défaut est utilisé, mais l’utilisateur peut le remplacer à l’aide de l’indicateur «--User-Data-dir». Les utilisateurs peuvent trouver le répertoire associé au profil sur edge://version/ sous le chemin d’accès du profil.

Pour éviter la perte de données ou d'autres erreurs inattendues, ne définissez pas cette stratégie sur le répertoire racine d'un volume ni sur un répertoire utilisé à d'autres fins, car MicrosoftEdge gère son contenu. 

Vous pouvez consulter la liste des variables utilisables sur [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041). 

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: UserDataDir
  - Nom de la stratégie de groupe: définir le répertoire de données utilisateur
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: UserDataDir
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"${users}/${user_name}/Edge"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: UserDataDir
  - Exemple de valeur:
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### UserDataSnapshotRetentionLimit
  #### Limite le nombre de captures instantanées des données utilisateur conservées qui sont utilisées en cas de restauration d’urgence
  
  
  #### Versions prises en charge:
  - Sur Windows depuis la version86 ou ultérieur

  #### Description
  Après chaque mise à jour de version importante, MicrosoftEdge créera une capture instantanée des parties des données de navigation de l’utilisateur à utiliser en cas d’urgence ultérieure nécessitant une restauration temporaire de la version. Si une restauration temporaire est effectuée vers une version pour laquelle un utilisateur dispose d’une capture instantanée correspondante, les données de la capture instantanée sont restaurées. Cela permet aux utilisateurs de conserver des paramètres comme les signets et les données de saisie automatique.

Si vous ne définissez pas cette stratégie, la valeur par défaut du nombre de captures instantanées est définie sur 3.

Si vous définissez cette stratégie, les anciennes captures instantanées sont supprimées si nécessaire, pour respecter la limite que vous avez définie. Si vous définissez cette stratégie sur 0, aucune capture instantanée n’est prise.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - entier.

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: UserDataSnapshotRetentionLimit
  - Nom de la stratégie: limite le nombre de captures instantanées des données utilisateur conservées qui sont utilisées en cas de restauration d’urgence
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: UserDataSnapshotRetentionLimit
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000003
```


  

  [Retour au début](#microsoft-edge---policies)

  ### UserFeedbackAllowed
  #### Autoriser les commentaires des utilisateurs
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  MicrosoftEdge utilise la fonctionnalité de commentaires Edge (activée par défaut) pour permettre aux utilisateurs d'envoyer des commentaires, des suggestions ou des enquêtes client et de signaler des problèmes liés au navigateur. En outre, par défaut, les utilisateurs ne peuvent pas désactiver la fonctionnalité de commentaires Edge.

Si vous activez cette stratégie ou ne la configurez pas, les utilisateurs peuvent appeler des commentaires Edge.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas invoquer les commentaires Edge.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: UserFeedbackAllowed
  - Nom de la stratégie de groupe: autoriser les commentaires des utilisateurs
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: UserFeedbackAllowed
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: UserFeedbackAllowed
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### VideoCaptureAllowed
  #### Autoriser ou bloquer la capture de vidéos
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Déterminez si les sites peuvent faire des captures de vidéo.

Si cette stratégie est activée ou n'est pas configurée (par défaut), l'utilisateur est invité à accepter l'accès à la capture vidéo, excepté pour les URL configurées dans la liste de la stratégie [VideoCaptureAllowedUrls](#videocaptureallowedurls), qui bénéficient d'un accès instantané. 

Si vous désactivez cette stratégie, l’utilisateur n’est pas interrogé et la capture vidéo est accessible uniquement aux URL configurées dans la stratégie [VideoCaptureAllowedUrls](#videocaptureallowedurls).

Cette stratégie a une incidence sur tous les types d'entrée vidéo, et pas uniquement sur la caméra intégrée.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: VideoCaptureAllowed
  - Nom de la stratégie de groupe: autoriser ou bloquer la capture de vidéos
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: VideoCaptureAllowed
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000000
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: VideoCaptureAllowed
  - Exemple de valeur:
``` xml
<false/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### VideoCaptureAllowedUrls
  #### Sites autorisés à accéder aux appareils de capture vidéo sans autorisation préalable
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Spécifiez les sites web, basés sur des formats d’URL, qui peuvent utiliser les appareils de capture vidéo sans autorisation préalable de la part de l’utilisateur. Les modèles de cette liste sont comparés à la source de sécurité de l’URL à l’origine de la demande. En cas de correspondance, l'accès aux appareils de capture vidéo est autorisé automatiquement.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: VideoCaptureAllowedUrls
  - Nom de la stratégie de groupe: sites autorisés à accéder aux appareils de capture vidéo sans autorisation préalable
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: VideoCaptureAllowedUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### WPADQuickCheckEnabled
  #### Définir l’optimisation WPAD
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Vous permet de désactiver l’optimisation WPAD (Web Proxy Auto-Discovery) dans MicrosoftEdge.

Si vous désactivez cette stratégie, l’optimisation WPAD est désactivée. Par conséquent, l'attente est plus longue pour obtenir une réponse des serveurs WPAD basés sur le DNS.

Si vous activez ou ne configurez pas la stratégie, l’optimisation WPAD est activée.

Quelle que soit la façon dont cette stratégie est activée, le paramètre d’optimisation WPAD ne peut pas être modifié par les utilisateurs.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: WPADQuickCheckEnabled
  - Nom de la stratégie de groupe: définir l'optimisation WPAD
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: WPADQuickCheckEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: WPADQuickCheckEnabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### WebAppInstallForceList
  #### Configurer la liste des applications web dont l’installation est forcée
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Configurez cette stratégie pour spécifier la liste d’applications web qui s’installent de manière silencieuse, sans intervention de l’utilisateur, et les utilisateurs qui ne peuvent pas effectuer une désinstallation ou une désactivation.

Chaque élément dans la liste de la stratégie est un objet avec un membre obligatoire: URL (URL de l’application web à installer) et 2membres facultatifs: default_launch_container (spécifie au mode fenêtre que l’application web s’ouvre with-a nouvel onglet est la valeur par défaut) et create_desktop_shortcut (True si vous voulez créer des raccourcis Linux et Windows Desktop).

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### Type de données:
  - Dictionary

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: WebAppInstallForceList
  - Nom de la stratégie de groupe: configurer la liste des applications web dont l’installation est forcée
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: WebAppInstallForceList
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\WebAppInstallForceList = [
  {
    "create_desktop_shortcut": true, 
    "default_launch_container": "window", 
    "url": "https://www.contoso.com/maps"
  }, 
  {
    "default_launch_container": "tab", 
    "url": "https://app.contoso.edu"
  }
]
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: WebAppInstallForceList
  - Exemple de valeur:
``` xml
<key>WebAppInstallForceList</key>
<array>
  <dict>
    <key>create_desktop_shortcut</key>
    <true/>
    <key>default_launch_container</key>
    <string>window</string>
    <key>url</key>
    <string>https://www.contoso.com/maps</string>
  </dict>
  <dict>
    <key>default_launch_container</key>
    <string>tab</string>
    <key>url</key>
    <string>https://app.contoso.edu</string>
  </dict>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### WebComponentsV0Enabled
  #### Réactiver l'API Web Components v0 jusqu'à M84 (obsolète)
  
  >OBSOLÈTE: Cette stratégie est obsolète et ne fonctionne pas après la version 84 de Microsoft Edge.
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 et jusqu’à la version84

  #### Description
  Cette stratégie ne fonctionne pas, car cette stratégie permettait de réactiver sélectivement ces fonctionnalités jusqu’à la version 85 de Microsoft Edge. Les API Web Components v0 (Shadow DOM v0, Custom Elements v0 et HTML Imports) sont obsolètes depuis 2018 et ont été désactivées par défaut à partir de Microsoft Edge versionM80.

Si elle est définie sur True, les fonctionnalités de Web Components v0 sont activées pour tous les sites.

Si elle est définie sur False ou si elle n'est pas définie, les fonctionnalités de Web Components v0 sont désactivées par défaut à compter de Microsoft Edge versionM80.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: WebComponentsV0Enabled
  - Nom de la stratégie de groupe: réactiver l'API Web Components v0 jusqu'à M84.
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: WebComponentsV0Enabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: WebComponentsV0Enabled
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### WebDriverOverridesIncompatiblePolicies
  #### Autoriser WebDriver à remplacer les stratégies incompatibles (obsolète)
  
  >OBSOLÈTE: Cette stratégie est obsolète et ne fonctionne pas après la version 84 de Microsoft Edge.
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 et jusqu’à la version84

  #### Description
  Cette stratégie ne fonctionne pas, car WebDriver est désormais compatible avec toutes les stratégies existantes.

Cette stratégie permet aux utilisateurs de la fonctionnalité WebDriver de remplacer des stratégies pouvant interférer avec son fonctionnement.

Actuellement, cette stratégie désactive les stratégies [SitePerProcess](#siteperprocess) et [IsolateOrigins](#isolateorigins).

Si la stratégie est activée, WebDriver peut remplacer les stratégies incompatibles.
Si la stratégie est désactivée ou n'est pas configurée, WebDriver n'est pas autorisé à remplacer les stratégies incompatibles.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: WebDriverOverridesIncompatiblePolicies
  - Nom de la stratégie de groupe: autoriser WebDriver à remplacer les stratégies incompatibles (déconseillé)
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: WebDriverOverridesIncompatiblePolicies
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: WebDriverOverridesIncompatiblePolicies
  - Exemple de valeur:
``` xml
<true/>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### WebRtcLocalIpsAllowedUrls
  #### Gérer l’exposition des adresses IP locales par WebRTC
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version80 ou versions ultérieures

  #### Description
  Spécifie une liste d'origines (URL) ou de modèles de noms d'hôte (par exemple, «*contoso.com*») pour laquelle l'adresse IP locale doit être exposée par WebRTC. 

Si vous activez cette stratégie et définissez une liste d'origines (URL) ou des modèles de noms d'hôte, lorsque edge://flags/#enable-webrtc-hide-local-ips-with-mdns est activé, WebRTC expose l'adresse IP locale pour les cas qui correspondent aux modèles dans la liste.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, et si edge://flags/#enable-webrtc-hide-local-ips-with-mdns est activé, WebRTC n'expose pas les adresses IP locales. L'adresse IP locale est cachée avec un nom d'hôte mDNS. 

Si vous activez, désactivez ou ne configurez pas cette stratégie, et si edge://flags/#enable-webrtc-hide-local-ips-with-mdns est désactivé, WebRTC expose les adresses IP locales.

Veuillez noter que cette stratégie affaiblit la protection des adresses IP locales qui peuvent être nécessaires aux administrateurs.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste composée de chaînes

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: WebRtcLocalIpsAllowedUrls
  - Nom de la stratégie de groupe: gérer l’exposition des adresses IP locales par WebRTC
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de valeur: liste composée de REG_SZ
  ##### Exemple de valeur:
```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: WebRtcLocalIpsAllowedUrls
  - Exemple de valeur:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### WebRtcLocalhostIpHandling
  #### Limiter l’exposition de l’adresse IP locale par WebRTC
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Vous permet de définir si WebRTC expose son l'adresse IP locale de l'utilisateur. 

Si vous définissez cette stratégie sur «AllowAllInterfaces» ou sur «AllowPublicAndPrivateInterfaces», WebRTC expose l'adresse IP locale.

Si vous définissez cette stratégie sur «AllowPublicInterfaceOnly » ou  sur «DisableNonProxiedUdp», WebRTC n'expose pas l'adresse IP locale.

Si vous ne définissez pas cette stratégie ou si vous la désactivez, WebRTC expose l'adresse IP locale.

Mappage des options de stratégie:

* AllowAllInterfaces (default) = Autoriser toutes les interfaces. Ceci expose l'adresse IP locale. 

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces)=Autoriser les interfaces publiques et privées sur l'itinéraire http par défaut. Ceci expose l'adresse IP locale. 

* AllowPublicInterfaceOnly (default_public_interface_only)=Autoriser l'interface publique sur l'itinéraire http par défaut. Ceci n'expose pas l'adresse IP locale.

* DisableNonProxiedUdp (disable_non_proxied_udp)=Utiliser TCP, sauf si le serveur proxy prend en charge UDP. Ceci n'expose pas l'adresse IP locale.

Utilisez les informations précédentes lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: WebRtcLocalhostIpHandling
  - Nom de la stratégie de groupe: limiter l’exposition de l’adresse IP locale par WebRTC
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: WebRtcLocalhostIpHandling
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"default"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: WebRtcLocalhostIpHandling
  - Exemple de valeur:
``` xml
<string>default</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### WebRtcUdpPortRange
  #### Restreindre la portée des ports UDP locaux utilisés par WebRTC
  
  
  #### Versions prises en charge:
  - sur Windows et macOS depuis la version77 ou versions ultérieures

  #### Description
  Restreint la portée des ports UDP utilisés par WebRTC à un intervalle de ports spécifié (points de terminaison inclus).

La configuration de cette stratégie vous permet de spécifier la portée des ports UDP locaux que WebRTC peut utiliser.

Si vous ne configurez pas cette stratégie, ou si vous définissez une chaîne vide ou une portée de ports non valide, WebRTC peut utiliser n’importe quel port UDP local disponible.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique de la stratégie de groupe: WebRtcUdpPortRange
  - Nom de la stratégie de groupe: restreindre la portée des ports UDP locaux utilisés par WebRTC
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: WebRtcUdpPortRange
  - Type de valeur: REG_SZ
  ##### Exemple de valeur:
```
"10000-11999"
```


  #### Informations et paramètres sur Mac
  - Nom clé de la préférence: WebRtcUdpPortRange
  - Exemple de valeur:
``` xml
<string>10000-11999</string>
```
  

  [Retour au début](#microsoft-edge---policies)

  ### WinHttpProxyResolverEnabled
  #### Utiliser la résolution du proxy Windows (déconseillée)
  >DÉCONSEILLÉ: cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge:
  - Sur Windows depuis la version84 ou versions ultérieures

  #### Description
  Cette stratégie est déconseillée car elle sera remplacée par une fonctionnalité similaire dans une version ultérieure. Consultez https://crbug.com/1032820.

Utilisez Windows pour résoudre les proxys pour tout le réseau de navigation, au lieu du solveur proxy intégré à Microsoft Edge. Le solveur Windows proxy active les fonctionnalités de proxy Windows telles que DirectAccess/NRPT.

Cette stratégie inclut les problèmes décrits par https://crbug.com/644030. Il entraîne l’extraction et l’exécution des fichiers PAC par le code Windows, y compris les fichiers PAC définis via la stratégie [ProxyPacUrl](#proxypacurl). Étant donné que les récupérations de réseau pour le fichier PAC se produisent par le biais de Windows à la place du code Microsoft Edge, les stratégies réseau telles que [DnsOverHttpsMode](#dnsoverhttpsmode) ne s’appliquent pas aux récupérations de réseau pour un fichier PAC.

Si vous activez cette stratégie, le résolveur proxy Windows est utilisé.

Si vous désactivez ou ne configurez pas cette stratégie, le solveur Microsoft Edge proxy est utilisé.

  #### Fonctionnalités prises en charge:
  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Non, nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations relatives à la stratégie de groupe (ADMX)
  - Nom unique GP: WinHttpProxyResolverEnabled
  - Nom de la stratégie de protection: utiliser la résolution du proxy Windows (déconseillée)
  - Chemin d’accès de la stratégie de groupe(obligatoire): Administrative Templates/Microsoft Edge/
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier ADMX de la stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin d’accès (obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur: WinHttpProxyResolverEnabled
  - Type de valeur: REG_DWORD
  ##### Exemple de valeur:
```
0x00000001
```


  

  [Retour au début](#microsoft-edge---policies)


## Voir également
- [Configuration de MicrosoftEdge](configure-microsoft-edge.md)
- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Blog sur les bases de la sécurité Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)