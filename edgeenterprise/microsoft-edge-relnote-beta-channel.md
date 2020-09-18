---
title: Notes de publication de Microsoft Edge pour le canal bêta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 09/14/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notes de publication de Microsoft Edge pour le canal bêta
ms.openlocfilehash: 75ae113b7e4b39a76b70d9c0f85bc484f63e3c1a
ms.sourcegitcommit: 468b75d86803ad1531d7bed8e6c1a562a00ebe50
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "11026894"
---
# Notes de publication du canal Microsoft Edge Beta

Ces notes de publication fournissent des informations sur les nouvelles fonctionnalités et les mises à jour non liées à la sécurité qui sont incluses dans le canal Microsoft Edge Beta.

> [!IMPORTANT]
> Consultez cette [mise à jour sur les versions de canaux Microsoft Edge](https://blogs.windows.com/msedgedev/2020/03/20/update-stable-channel-releases/).

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
  * Microsoft Edge vous avertit si votre mot de passe est détecté dans une fuite en ligne. Microsoft Edge vérifie vos mots de passe par rapport à un référentiel d'informations d'identification connues et vous avertit si une correspondance est trouvée.

* **Ajoutez une image personnalisée à la nouvelle page d’onglet (NTP) à l’aide d’une stratégie de groupe.** À partir de la version 86 de Microsoft Edge, le protocole NTP offre une option permettant de remplacer l'image par défaut par une image personnalisée fournie par l'utilisateur. La possibilité de gérer les propriétés de cette image est également prise en charge par la stratégie de groupe.

* **Faites correspondre les raccourcis clavier personnalisés à VS Code.** MicrosoftEdgeDevTools prend désormais en charge la personnalisation des raccourcis clavier dans DevTools pour adapter à votre éditeur/IDE. (Dans MicrosoftEdge84, nous avons ajouté la possibilité de faire correspondre les raccourcis clavier DevTools à VSCode).

* **Remplacez les stratégies [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) et [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) pour les fenêtres de niveau inférieur et macOS.** Ces stratégies sont déconseillées dans Microsoft Edge version86 et deviendront obsolètes dans Microsoft Edge version89.<br>
Ces stratégies sont remplacées par [Autoriser la télémétrie](https://go.microsoft.com/fwlink/?linkid=2099569) sur Windows10, et la nouvelle stratégie [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) pour toutes les autres plateformes. Cela permet aux utilisateurs de gérer les données de diagnostic envoyées à Microsoft pour Windows7, 8, 8.1 et macOS.

### Mises à jour de stratégie

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

<!--- BEGIN 85 ---->
## Version85.0.564.18: 28juillet

### Mises à jour des fonctionnalités

- **Synchronisation locale des favoris et des paramètres**. Vous pouvez désormais synchroniser les favoris et paramètres d’un navigateur entre les profils ActiveDirectory au sein de votre propre environnement sans avoir besoin d’effectuer une synchronisation dans le cloud.

- **Prise en charge de la stratégie de groupe MicrosoftEdge pour l’approbation de combinaisons site+application à lancer sans invite de confirmation.** La prise en charge de la stratégie de groupe ajoutée permet aux administrateurs d’ajouter des combinaisons site+application dont le lancement est approuvé sans invite de confirmation. Cela ajoute la possibilité pour les administrateurs de configurer les combinaisons de protocoles/origines approuvées (par exemple, les applications Microsoft365) pour leurs utilisateurs finaux afin de supprimer l’invite de confirmation lors de la navigation vers uneURL qui contient un protocole d’application.

- **Outil de mise en surbrillancePDF**. Cet outil peut être ajouté à la barre d’outils pour les fichiers PDF afin de mettre en évidence le texte important.

- **L’API d’accès au stockage est disponible**. Cette API d’accès au stockage permet l’accès au stockage interne alors qu’un utilisateur tiers manifeste son intention directe d’autoriser un stockage qui sinon serait bloqué par la configuration actuelle du navigateur. Pour plus d’informations, voir [API d’accès au stockage](https://www.chromestatus.com/feature/5612590694662144).

- **Envoyer à OneNote est disponible pour les collections MicrosoftEdge**. Tout le monde a hâte de pouvoir envoyer des informations rassemblées dans des collections vers OneNote, où l’on peut l’ajouter à un projet plus important et collaborer avec d’autres personnes. Et encore plus important, dans MicrosoftEdge85, vous pourrez envoyer du contenu aux produits *Office pour Mac* (Word, Excel et OneNote) pour MSA et AzureActiveDirectory.

- **Mises à jour de DevTools**. Pour plus d’informations sur les mises à jour suivantes, voir [Nouveautés de DevTools (MicrosoftEdge85)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools).

   - MicrosoftEdgeDevTools prend en charge l’émulation SurfaceDuo. MicrosoftEdgeDevTools peut émuler le SurfaceDuo pour vous permettre de tester l’apparence de votre contenu Web sur les appareils à deux écran. Pour activer cette expérience dans DevTools, accédez au mode Appareil en appuyant sur Ctrl+Maj+M sur Windows ou cmd+Maj+M sur macOS, puis sélectionnez SurfaceDuo dans la liste déroulante des appareils.
   - MicrosoftEdgeDevTools vous permet de faire correspondre les raccourcis clavier à VSCode. MicrosoftEdgeDevTools prend en charge la personnalisation des raccourcis clavier dans DevTools pour reproduire votre éditeur/IDE. Dans MicrosoftEdge85, nous ajoutons la possibilité de faire correspondre les raccourcis clavier DevTools à VSCode. Cette modification permet de gagner en efficacité dans VSCode et DevTools.

### Mises à jour de stratégie

#### Nouvelles stratégies

Treize nouvelles stratégies ont été ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [AutoLaunchProtocolsFromOrigins](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autolaunchprotocolsfromorigins): définir une liste de protocoles qui peuvent lancer une application externe à partir d’origines, sans inviter l’utilisateur.
- [AutoOpenAllowedForURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenallowedforurls): les URL pour lesquels AutoOpenFileTypes peut s’appliquer.
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes): liste des types de fichiers qui doivent être automatiquement ouverts lors du téléchargement.
- [DefaultSearchProviderContextMenuAccessAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchprovidercontextmenuaccessallowed): autoriser la recherche d’accès au menu contextuel du moteur de recherche par défaut.
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors): autoriser les certificats signés à l’aide de l’algorithme SHA-1 lorsqu’ils sont émis par des ancres d’approbation locales.
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings): désactiver les avertissements basés sur l’extension de fichier de téléchargement pour les types de fichiers spécifiés sur des domaines.
- [IntensiveWakeUpThrottlingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intensivewakeupthrottlingenabled): contrôler la fonctionnalité IntensiveWakeUpThrottling.
- [NewTabPagePrerenderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageprerenderenabled): activer le préchargement de la nouvelle page d’onglet pour un rendu plus rapide.
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox): configurer l’expérience de zone de recherche de la page Nouvelonglet.
- [PasswordMonitorAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordmonitorallowed): autoriser les utilisateurs à être avertis si leur mot de passe est considéré comme non sécurisé.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): activer l’utilisation de copies itinérantes pour les données de profil MicrosoftEdge.
- [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation): définit le répertoire de profil itinérant.
- [TLSCipherSuiteDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tlsciphersuitedenylist): spécifiez les suites de chiffrementTLS à désactiver.

#### Stratégies obsolètes

- [EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload): activer le téléchargement des actions de domaine à partir de Microsoft.
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) – Réactive les composants WebPart de l’API v0 jusqu’au M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies): autoriser WebDriver à remplacer les stratégies incompatibles.

<!--- END ---->

## Version84.0.522.35: 9juillet

Résolution de divers bogues et problèmes de performances.

## Version84.0.522.28: 26juin

Résolution de divers bogues et problèmes de performances.

## Version84.0.522.26: 24juin

Résolution de divers bogues et problèmes de performances.

## Version84.0.522.20: 15juin

Résolution de divers bogues et problèmes de performances.

## Version84.0.522.15: 8juin

Résolution de divers bogues et problèmes de performances.

## Version84.0.522.11: 2juin

### Mises à jour des fonctionnalités

- Cette version de Microsoft Edge permet un téléchargement plus rapide des listes de sites en mode Internet Explorer.  Nous avons réduit le délai de téléchargement des listes de sites en mode Internet Explorer à 0seconde (60secondes d’attente auparavant) en l’absence d’une liste de sites mis en cache. Nous avons également ajouté la prise en charge de la stratégie de groupe pour les cas où les navigations dans la page d’accueil en mode Internet Explorer doivent attendre le téléchargement de la liste des sites. Si vous souhaitez en savoir plus, veuillez consulter la stratégie [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload).

- Microsoft Edge permet désormais aux utilisateurs de se connecter au navigateur lorsque celui-ci est en mode «Exécuter en tant qu’administrateur» sous Windows10. Cette fonctionnalité aide les clients à exécuter Microsoft Edge sur un serveur Windows ou dans les scénarios de bureau à distance et de bac à sable.

- Microsoft Edge fournit à présent une prise en charge complète de la souris en mode plein écran. Vous pouvez à présent utiliser la souris pour accéder aux onglets, à la barre d’adresses et aux autres éléments sans quitter le mode plein écran.

- Amélioration des achats en ligne. Ajoutez des pseudos personnalisés aux cartes de débit ou de crédit enregistrées. Vous pouvez à présent distinguer et différencier vos cartes de crédit lors de vos achats en ligne. L’attribution d’un pseudo à vos cartes de débit ou de crédit vous permet de choisir la carte appropriée lorsque vous utilisez le remplissage automatique pour sélectionner un mode de paiement.

- TLS/1.0 et TLS/1.1 sont désactivés par défaut. Pour vous aider à découvrir les sites impactés, vous pouvez régler l’indicateur *edge://flags/#display-legacy-tls-warnings* pour que Microsoft Edge affiche une notification non bloquante «non sécurisée» lors du chargement de pages qui nécessitent des protocoles TLS hérités. La stratégie [SSLVersionMin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sslversionmin) permet de réactiver TLS/1.0 et TLS/1.1. Cette stratégie reste disponible au moins jusqu’à Microsoft Edge version88. Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Modifications apportées à Microsoft Edge ayant un impact sur la compatibilité des sites](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

- Améliorations des collections:

  - Nous avons ajouté une fonctionnalité d’ajout de note ou de commentaire à un élément d’une collection. Les notes sont regroupées et restent associées à un élément, même si vous triez les éléments d’une collection. Pour essayer cette nouvelle fonctionnalité, cliquez avec le bouton droit sur un élément, puis sélectionnez «Ajouter une note».
  - Vous pouvez modifier la couleur d’arrière-plan des notes dans les collections. Vous pouvez utiliser un codage en couleurs pour vous aider à organiser vos informations et augmenter votre productivité.
  - Des améliorations de performances sont perceptibles, ce qui vous permet d’exporter vos collections vers Excel en moins de temps que dans les versions précédentes de Microsoft Edge.

- Prise en charge supplémentaire de l’API Microsoft Edge:

  - API d’accès au stockage. Cette API permet d’accéder au stockage interne alors qu’un utilisateur tiers manifeste son intention d’autoriser un stockage bloqué à défaut par la configuration actuelle du navigateur.

    À mesure que la confidentialité revêt une importance grandissante pour les utilisateurs, ces dernier recherchent, de plus en plus, des valeurs par défaut du navigateur et des paramètres plus stricts de consentement des utilisateurs (blocage de l’accès au stockage tiers, par exemple). Ces paramètres permettent d’améliorer la confidentialité et de bloquer l’accès indésirable de la part d’utilisateurs inconnus ou non approuvés. Cependant, ils peuvent également avoir des effets secondaires indésirables, tels que le blocage de l’accès au contenu nécessaire à l’utilisateur (par exemple, les réseaux sociaux et le contenu multimédia incorporé).

  - L’API de système de fichiers natif vous permet d’autoriser les sites à modifier des fichiers ou des dossiers.

- Améliorations apportées au contenu PDF:

  - La lecture à voix haute pour PDF permet aux utilisateurs d’écouter du contenu PDF tout en effectuant d’autres tâches éventuellement importantes pour eux. Cela permet également aux apprenants au profil auditif et visuel de se concentrer sur la lecture du contenu, d’où un apprentissage facilité.
  - La modification des fichiers PDF est améliorée. Vous pouvez à présent enregistrer une modification directement dans le fichier PDF au lieu d’enregistrer une copie de ce dernier à chaque modification.

- Microsoft Edge permet à présent la traduction dans le lecteur immersif. Lorsqu’un utilisateur ouvre la vue Lecteur immersif, il peut choisir de traduire la page dans la langue de son choix.

- DevTools prend en charge la personnalisation des raccourcis clavier en fonction de votre éditeur/IDE, code VS inclus.

### Mises à jour de stratégies

#### Nouvelles stratégies

Nous avons ajouté cinq nouvelles stratégies. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [AppCacheForceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#appcacheforceenabled): permet de réactiver la fonctionnalité AppCache, même si elle est désactivée par défaut.
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy): proxy conteneur Application Guard.
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload): la liste des sites en mode entreprise doit être disponible avant la navigation par onglets.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) – Activer le masquage de fenêtres natives.
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout): définit un délai d’expiration de la navigation par onglets pour la liste des sites en mode entreprise.

#### Stratégies déconseillées

- [AllowSyncXHRInPageDismissal](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal): autorise les pages à envoyer des demandes XHR synchrones lors de l’opération de rejet de page.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) – Indique si le vérificateur de certificats intégré est utilisé pour la vérification des certificats de serveur.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled): active un traitement plus strict pour des contenus mixtes.

#### Stratégie obsolète

[ForceNetworkInProcess](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcenetworkinprocess): force l’exécution du code de mise en réseau dans le processus du navigateur.

<!-- end 84 -->

## Version83.0.478.44: 1erjuin

Résolution de divers bogues et problèmes de performances.

## Version83.0.478.37: 20 mai

Résolution de divers bogues et problèmes de performances.

## Version83.0.478.33: 15mai

Résolution de divers bogues et problèmes de performances.

## Version83.0.478.28: 7mai

Résolution de divers bogues et problèmes de performances.

## Version 83.0.478.25: 4 mai

Résolution de divers bogues et problèmes de performances.

## Version 83.0.478.18: 27avril

Résolution de divers bogues et problèmes de performances.

## Version 83.0.478.13: 22avril

### Mises à jour des fonctionnalités

- Améliorations apportées à Microsoft Defender SmartScreen: améliorations apportées au service Microsoft Defender SmartScreen, telles que la protection améliorée contre les sites malveillants qui redirigent au chargement et le blocage de trames de niveau supérieur, qui remplace complètement les sites malveillants avec la page de sécurité Microsoft Defender SmartScreen. Le blocage de trames de niveau supérieur empêche la lecture du contenu audio et d’autres éléments multimédias du site malveillant, ce qui permet d’obtenir une expérience plus facile et moins confuse.

- En réponse aux commentaires des utilisateurs, vous pouvez désormais exempter certains cookies de l’effacement automatiquement lorsque le navigateur se ferme. Cette option est utile s’il existe un site dont les utilisateurs ne souhaitent pas être déconnectés, mais souhaitent tout de même que tous les autres cookies soient supprimés lorsque le navigateur se ferme. Pour utiliser cette fonctionnalité, accédez à *edge://settings/clearBrowsingDataOnClose* et activez le bouton bascule «cookies et autres données de site».

- Le basculement de profil automatique est désormais disponible pour vous aider à accéder à votre contenu professionnel plus facilement dans les profils. Si vous utilisez plusieurs profils au travail, vous pouvez les consulter en accédant à un site nécessitant une authentification à partir de votre compte professionnel ou scolaire sur votre profil personnel. Lorsque nous détectons une modification, nous vous demandons, via une invite, de basculer vers votre profil de travail pour accéder à ce site sans devoir vous y authentifier. Lorsque vous choisissez le profil de travail vers lequel vous voulez basculer, le site Web s’ouvre dans votre profil de travail. Cette fonctionnalité de commutation de profil vous permet de séparer vos données professionnelles et personnelles et d’accéder à votre contenu professionnel plus facilement. Si vous ne souhaitez pas que la fonctionnalité vous invite à changer de profil, vous pouvez choisir l’option ne plus poser de message.

- Améliorations des fonctionnalités de recouvrement:
  - Vous pouvez utiliser la fonction glisser-déplacer pour ajouter un élément à une collection sans ouvrir la collection. Pendant le glisser-déplacer, vous pouvez également choisir un emplacement dans la liste des collections où vous voulez placer l’élément.
  - Vous pouvez ajouter plusieurs éléments à une collection au lieu d’y ajouter un élément à la fois. Pour ajouter plusieurs éléments, sélectionnez les éléments, puis faites-les glisser vers une collection. Vous pouvez également sélectionner les éléments, cliquer avec le bouton droit et choisir la collection dans laquelle vous voulez placer les éléments.

- Vous pouvez ajouter tous les onglets d’une fenêtre de bord dans une nouvelle collection sans les ajouter individuellement. Pour ajouter tous les onglets, cliquez avec le bouton droit sur un onglet, puis sélectionnez «Ajouter tous les onglets à une nouvelle collection».

- La synchronisation d’extension est désormais disponible. Vous pouvez désormais synchroniser vos extensions sur tous vos appareils. Les extensions des magasins Microsoft et chrome sont synchronisées avec Microsoft Edge. Pour utiliser cette fonctionnalité: cliquez sur les points de suspension (**…**) dans la barre de menus, puis sélectionnez **Paramètres**. Sous votre profil, cliquez sur **Synchroniser** pour afficher les options de synchronisation. Sous **Profils/synchronisation** utilisez le bouton bascule pour activer les extensions. Vous pouvez utiliser la stratégie de groupe [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) pour désactiver la synchronisation des extensions.

- Message amélioré sur la page gestion des téléchargements pour les téléchargements non sécurisés qui ont été bloqués.

- Améliorations du lecteur immersif:
  - Ajout d’une prise en charge des adverbes dans les parties de l’expérience de reconnaissance vocale dans le lecteur immersif. Lors de la lecture d’un article dans le lecteur immersif, ouvrez les outils de vérification de la grammaire et activez les adverbes dans certains secteurs vocaux pour mettre en surbrillance toutes les adverbes de la page.
  - Ajout de la possibilité de sélectionner le contenu d’une page Web et de l’ouvrir dans le lecteur immersif. Cette possibilité permet aux utilisateurs d’utiliser le lecteur immersif et tous les outils d’apprentissage, tels que le focus de ligne et la lecture à haute voix sur tous les sites Web.

- Le docteur de lien fournit une correction de l’hôte et une requête de recherche aux utilisateurs lorsqu’ils ne tapent pas une URL. Par exemple: <br>
Un utilisateur saisit «powerbi» comme «powerbbi».com. Le docteur de lien suggère «powerbi».com comme correction et crée un lien pour rechercher « powerbbi» au cas où l’utilisateur cherche quelque chose d’autre.

- Autoriser les utilisateurs à enregistrer leur décision de lancement d’un protocole externe pour un site spécifique. Les utilisateurs peuvent configurer la stratégie de [ExternalProtocolDialogShowAlwaysOpenCheckbox]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) pour activer ou désactiver cette fonctionnalité.

- Les utilisateurs peuvent régler Microsoft Edge comme navigateur par défaut directement à partir de Microsoft Edge **Paramètres**. Cette fonctionnalité permet aux utilisateurs de modifier facilement leur navigateur par défaut, dans le contexte du navigateur lui-même, au lieu d’effectuer une recherche dans les paramètres du système d’exploitation. Pour utiliser cette fonctionnalité, accédez à *edge://settings/defaultBrowser*, puis cliquez sur **Utiliser par défaut**.

- Plusieurs mises à jour de DevTools, y compris la prise en charge du débogage distant, l’amélioration de l’interface utilisateur et bien plus encore. Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Nouveautés de DevTools (Microsoft Edge 83)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

### Mises à jour de stratégies

#### Nouvelles stratégies

15 nouvelles stratégies ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [AllowSurfGame](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsurfgame) –  Autoriser le jeu de surf.
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls) – Configurer la liste des sites avec lesquels MicrosoftEdge tentera d’établir une liaison de jeton.
- [BingAdsSuppression](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#bingadssuppression) – Bloquer toutes les annonces dans les résultats de recherche Bing.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) – Indique si le vérificateur de certificats intégré est utilisé pour la vérification des certificats de serveur.
- [ClearCachedImagesAndFilesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearcachedimagesandfilesonexit) – Effacer les images et les fichiers mis en cache lors de la fermeture de MicrosoftEdge.
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare) – Configurer l’expérience de partage.
- [DeleteDataOnMigration](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#deletedataonmigration) – Supprimer les anciennes données de navigateur lors de la migration.
- [DnsOverHttpsMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpsmode) – Contrôler le mode du protocole DNS-over-HTTPS.
- [DnsOverHttpsTemplates](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpstemplates) – Spécifier le modèle d’URI du programme de résolution DNS-over-HTTPS souhaité.
- [FamilySafetySettingsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#familysafetysettingsenabled) – Autoriser les utilisateurs à configurer la sécurité des membres de la famille.
- [LocalProvidersEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#localprovidersenabled) – Autoriser les suggestions des fournisseurs de services locaux.
- [ScrollToTextFragmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#scrolltotextfragmentenabled) – Activer le défilement jusqu’au texte spécifié dans les fragments d’URL.
- [ScreenCaptureAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#screencaptureallowed) – Autoriser ou refuser la capture d’écran.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) – Configurer la liste des types exclus de la synchronisation.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) – Activer le masquage de fenêtres natives.

#### Stratégie déconseillée

La stratégie suivante continuera à fonctionner dans cette version. Il deviendra «obsolète» dans une prochaine version.

[EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload) – Activer le téléchargement des actions de domaine à partir de Microsoft

<!--  end 83 -->

## Version 81.0.416.60: 20avril

Résolution de divers bogues et problèmes de performances.

## Version 81.0.416.58: 17avril

Mises à jour de sécurité.

## Version81.0.416.50: 10avril

Résolution de divers bogues et problèmes de performances.

## Version 81.0.416.45: 3avril

Résolution de divers bogues et problèmes de performances.

## Version81.0.416.41: 30mars

Résolution de divers bogues et problèmes de performances.

## Version81.0.416.34: 17mars

Résolution de divers bogues et problèmes de performances.

## Version81.0.416.31: 12mars

Résolution de divers bogues et problèmes de performances.

## Version81.0.416.28: 9mars

Résolution de divers bogues et problèmes de performances.

## Version81.0.416.20: 28février

Résolution de divers bogues et problèmes de performances.

## Version 81.0.416.12: 20février

### Mises à jour des fonctionnalités

- Les collections sont désormais disponibles. Vous pouvez démarrer en cliquant sur l’icône Collections située près de la barre d’adresses. Cette action ouvre le volet Collections dans lequel vous pouvez créer, modifier et afficher des collections. Les Collections ont été conçues en fonction de votre activité sur le web. Si vous êtes un client, un voyageur, un enseignant ou un étudiant, les Collections peuvent vous être utiles. [En savoir plus](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Autoriser la suppression (Masquer dans la barre d’outils) du bouton Collections de la barre d’outils Microsoft Edge par souci de cohérence.

- La connexion automatique d'un compte Active Directory local est ciblée uniquement pour les organisations qui l’activent.  Si des utilisateurs ont déjà ouvert une session avec un compte Active Directory local, ils pourront maintenant se déconnecter. Les utilisateurs sont désormais automatiquement connectés au compte principal de leur système d’exploitation s’il s’agit d’un compte MSA ou Azure Active Directory. Les administrateurs peuvent activer la connexion automatique à l’aide d’un compte Azure Active Directory local utilisant la stratégie ConfigureOnPremisesAccountAutoSignIn.

- ApplicationGuard. La prise en charge des extensions est désormais disponible dans le conteneur.

- Nous avons ajouté un message pour informer les utilisateurs qu’Internet Explorer n'est pas installée lorsqu’ils naviguent vers une page configurée pour s’ouvrir en mode Internet Explorer.

- Mise à jour de l’outil d'affichage3D dans Microsoft Edge DevTools avec une nouvelle fonctionnalité permettant de déboguer le contexte d'empilement de l’index-Z. L’affichage3D affiche une représentation de la profondeur de Document Object Model (DOM) à l’aide de la couleur et de l’empilement et l’affichage index-Z vous permet d’isoler les différents contextes d’empilage de votre page. [En savoir plus](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- Localisation des outils F12 Dev dans 10 nouvelles langues pour qu'ils correspondent à la langue utilisée dans le reste du navigateur. [En savoir plus](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Ajout de la prise en charge de la lecture Dolby Vision. Sur la Build 17134 (mise à jour d'avril2018) de Windows10 compatible Dolby Vision, les sites web peuvent désormais afficher le contenu Dolby Vision. Découvrez comment activer le contenu Dolby Vision sur [Netflix](https://help.netflix.com/en/node/42384).

- Microsoft Edge peut désormais identifier et supprimer des favoris dupliqués et fusionner des dossiers portant le même nom. Pour accéder à cet outil, cliquez sur l’étoile dans la barre d’outils du navigateur, puis sélectionnez «Supprimer les favoris dupliqués».  Vous pourrez confirmer les modifications et les mises à jour apportées à vos favoris seront synchronisées sur tous les appareils.

- Des utilisateurs ont signalé qu'il peut être difficile de distinguer une fenêtre de navigation normale dans un thème foncé d’une fenêtre InPrivate, car les deux cadres de fenêtre sont sombres. La nouvelle icône pilule bleue InPrivate dans le coin supérieur droit permet de garantir aux utilisateurs qu'ils naviguent en mode InPrivate.

- Ouvrir des liens externes dans le profil de navigateur adéquat. Sélectionnez un profil par défaut pour les liens ouverts afin que les applications externes s’ouvrent à partir de *edge://settings/multiProfileSettings*.

- Ajout d'un avertissement pour informer les utilisateurs qui se connectent à un profil de navigateur avec un compte après s’être précédemment connectés avec un compte différent. Ceci permet d'empêcher la fusion involontaire de données.

- Si vous avez enregistré des cartes de paiement dans votre compte Microsoft, vous pouvez les utiliser dans Microsoft Edge lorsque vous saisissez des formulaires de paiement. Les cartes de votre compte Microsoft sont synchronisées sur tous les appareils de bureau et les informations détaillées sont partagées avec le site web après une authentification à deux facteurs (code CVC et votre identité Microsoft). Pour plus de commodité, vous pouvez choisir d’enregistrer, de manière sécurisée, une copie de la carte sur l’appareil durant l’authentification.

- La fonctionnalité Focus sur lignes est conçue pour les utilisateurs qui aiment se concentrer sur une partie limitée du contenu qu'ils lisent. Elle permet aux utilisateurs de se concentrer sur 1, 3 ou 5lignes à la fois, et d'assombrir le reste de la page pour leur permettre de lire sans aucune distraction. Les utilisateurs peuvent faire défiler l’écran à l’aide de l'interaction tactile ou des touches de direction pour que la concentration se déplace en conséquence.

- Microsoft Edge est désormais intégré au vérificateur d'orthographe de Windows sur les plateformes Windows8.1 et ultérieures. Cette intégration offre une prise en charge linguistique accrue, avec un accès à d’autres dictionnaires linguistiques et la possibilité d’utiliser des dictionnaires personnalisés de Windows. Aucune action supplémentaire n’est exigée de la part des utilisateurs lorsqu’une langue a été ajoutée aux paramètres de langue du système d’exploitation et qu’un bouton bascule de vérification linguistique est activé dans les paramètres de Microsoft Edge.

- Lorsque des documents PDF sont ouverts à l’aide de Microsoft Edge, les utilisateurs peuvent désormais créer ou supprimer des surbrillances et modifier la couleur. Cela vous permet de référencer par la suite les parties importantes d'un document et de travailler en collaboration.

- Lors du chargement de longs documents PDF optimisés pour le web, les pages consultées par l’utilisateur sont chargées plus rapidement, parallèlement au chargement du reste du document.

- Il est désormais plus simple de démarrer le lecteur immersif pour un site web en appuyant sur la touche F9.

- Il est désormais plus facile de démarrer la lecture à haute voix à l’aide d’un raccourci clavier (Ctrl+Maj+U).

### Mises à jour de stratégies

#### Nouvelles stratégies

12 nouvelles stratégies ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled): active l’authentification ambiante pour les profils InPrivate et Invité. 
- [AudioSandboxEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#audiosandboxenabled): autorise l’exécution du bac à sable audio.
- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy): utiliser une stratégie de référent par défaut de no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#globallyscopehttpauthcacheenabled): active le cache d’authentification HTTP de portée globale.
- [ImportExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importextensions): autorise l’importation d’extensions.
- [ImportCookies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importcookies): autorise l’importation de cookies.
- [ImportShortcuts](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importshortcuts): autorise l’importation de raccourcis.
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect): spécifie la manière dont les navigations «dans la page» vers les sites non configurés se comportent lorsque vous démarrez à partir des pages du mode Internet Explorer.
- [OmniboxMSBProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#omniboxmsbproviderenabled): active le fournisseur Microsoft Search pour le fournisseur Entreprise dans omnibox. 
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled): active un traitement plus strict pour des contenus mixtes.
- [TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled): active une fonctionnalité de sécurité TLS 1.3 pour les ancres d’approbation locales.
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin): configure la connexion automatique avec un compte de domaine Azure Active Directory lorsqu'il n'existe pas de compte de domaine Azure Active Directory.

#### Stratégies déconseillées

Les stratégies suivantes fonctionnent encore dans cette version. Elles deviendront «obsolètes» dans une prochaine version.

- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled): réactive les composants WebPart de l’API v0 jusqu’au M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies): autorise WebDriver à substituer Incompatible.

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
