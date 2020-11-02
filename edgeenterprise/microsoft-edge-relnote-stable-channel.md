---
title: Notes de publication de Microsoft Edge pour le canal stable
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 10/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notes de publication de Microsoft Edge pour le canal stable
ms.openlocfilehash: b26835eb53bfe6a327e2b0d8cb4f6a7180214530
ms.sourcegitcommit: 2a998c7ad37410267703a25f5feff5c0560c5efa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2020
ms.locfileid: "11145675"
---
# Notes de publication du canal stable Microsoft Edge

Ces notes de publication fournissent des informations sur les nouvelles fonctionnalités et les mises à jour non liées à la sécurité qui sont incluses dans le canal stable Microsoft Edge. Si vous souhaitez en savoir plus sur les canaux Microsoft Edge, veuillez consultez la rubrique [Vue d’ensemble des canaux Microsoft Edge](microsoft-edge-channels.md). L'ensemble des mises à jour de sécurité sont répertoriées [ici](microsoft-edge-relnotes-security.md).

> [!NOTE]
> Pour le canal stable, le déploiement des mises à jour sera progressif et durera un ou plusieurs jours. Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Déploiements progressifs pour les mises à jour de Microsoft Edge](microsoft-edge-update-progressive-rollout.md).

## Version86.0.622.58: 29octobre

Résolution de divers bogues et problèmes de performances.

## Version86.0.622.56: 27octobre

Résolution de divers bogues et problèmes de performances.

## Version86.0.622.51 : 22octobre

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-22-2020).

## Version86.0.622.48 : 20octobre

Résolution de divers bogues et problèmes de performances.

## Version 86.0.622.43 : 15 octobre

Résolution de divers bogues et problèmes de performances.

<!-- begin major 86 -->
## Version 86.0.622.38 : 9 octobre

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-9-2020).

### Mises à jour des fonctionnalités

* **Revenir à la version précédente de Microsoft Edge.** La fonctionnalité de restauration permet aux administrateurs de revenir à une version correcte connue de Microsoft Edge s’il existe un problème dans la dernière version de Microsoft Edge. **Remarque : ** la version stable 86.0.622.38 est la première version vers laquelle vous pouvez revenir, ce qui signifie que la version stable 87 est la première version prête à revenir. [En savoir plus](edge-learnmore-rollback.md).

* **Appliquer l’activation de la synchronisation par défaut au sein de l’entreprise.**  Les administrateurs peuvent activer la synchronisation pour les comptes Azure Active Directory (Azure AD) par défaut avec la stratégie [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync) .

* **Changement de profil automatique sur Windows 7 et 8.1.** Le changement automatique de profil actuellement disponible dans Microsoft Edge sur Windows 10 est étendu aux niveaux inférieurs de Windows (Windows 7 et 8.1). Pour plus d’informations, consultez le billet de blog [changement automatique de profil](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **SameSite = Lax cookies par défaut**. Pour améliorer la sécurité et la confidentialité sur le Web, les cookies s’affichent désormais par défaut [SameSite = Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite) gestion par défaut. Cela signifie que les cookies sont uniquement envoyés dans un contexte tiers et sont omis pour les demandes envoyées aux tiers. Cette modification peut avoir un impact sur les sites Web qui requièrent des cookies pour que les ressources tierces fonctionnent correctement. Pour autoriser de tels cookies, les développeurs Web peuvent marquer les cookies qui doivent être définis de et envoyés à des contextes tiers en ajoutant des attributs `SameSite=none` et `Secure` explicites lorsque le cookie est défini. Les entreprises qui souhaitent exempter certains sites de cette modification peuvent le faire à l’aide de la stratégie de [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist). Vous pouvez également désactiver la modification sur tous les sites à l’aide de la stratégie [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) .

* **Supprimez l’API de cache de l’application HTML5.**  Depuis Microsoft Edge version86, l’API cache de l’application héritée qui permet d’utiliser en mode hors connexion des pages web est supprimée de Microsoft Edge. Les développeurs web doivent consulter la [documentation WebDev](https://web.dev/appcache-removal/) pour plus d’informations sur le remplacement de l’API cache de l’application avec les travailleurs de service.  Important: vous pouvez demander un [Jeton AppCache OriginTrial](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) qui permet aux sites de continuer à utiliser l’API de cache d’application déconseillée jusqu’à la version90 de Microsoft Edge.

* **Confidentialité et sécurité :**

  * **Remplacez les stratégies [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) et [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) pour les fenêtres de niveau inférieur et macOS.** Ces stratégies sont déconseillées dans Microsoft Edge version86 et deviendront obsolètes dans Microsoft Edge version89.<br>
Ces stratégies sont remplacées par [Autoriser la télémétrie](https://go.microsoft.com/fwlink/?linkid=2099569) sur Windows10, et la nouvelle stratégie [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) pour toutes les autres plateformes. Cela permet aux utilisateurs de gérer les données de diagnostic envoyées à Microsoft pour Windows7, 8, 8.1 et macOS.
  * Prise en charge du DNS sécurisé (DNS-sur-HTTPS).  À partir de la version86 de Microsoft Edge, les paramètres de contrôle de DNS sécurisé sur les appareils non gérés sont disponibles. Ces paramètres ne sont pas accessibles aux utilisateurs sur les appareils gérés, mais les administrateurs informatiques peuvent activer ou désactiver le DNS sécurisé à l’aide de la stratégie de groupe [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode).

* ** Mode Internet Explorer :** Permet aux utilisateurs d'utiliser l'interface utilisateur (IU) de Microsoft Edge pour tester des sites en mode Internet Explorer. À partir de la version86 de Microsoft Edge, les administrateurs peuvent activer une option d'interface utilisateur pour que leurs utilisateurs puissent charger un onglet en mode Internet Explorer à des fins de test ou comme palliatif jusqu'à ce que les sites soient ajoutés à la liste XML des sites.

* **Mises à jour PDF:**

  * Table des matières des documents PDF. À partir de la version86, Microsoft Edge a ajouté la prise en charge de la table des matières qui permet aux utilisateurs de parcourir facilement les documents PDF.
  * Accédez à toutes les fonctionnalités de PDF sur les écrans compacts. Accédez à toutes les fonctionnalités du lecteur PDF Microsoft Edge sur les appareils disposant de petites tailles d’écran.
  * Prise en charge du stylet pour le surligneur des fichiers PDF. Avec cette mise à jour, les utilisateurs peuvent utiliser leur stylet numérique pour mettre en surbrillance directement du texte dans les fichiers PDF, de la même manière qu’avec un surligneur physique et du papier.
  * Défilement PDF amélioré. Vous pourrez désormais faire défiler les documents au format PDF long.

* **Les suggestions de saisie semi-automatique s’affichent lorsque les utilisateurs commencent à taper une requête de recherche sur le site web des composants additionnels Microsoft Edge.** La saisie semi-automatique permet aux utilisateurs d’effectuer rapidement leur requête de recherche sans entrer l’intégralité de la chaîne. Ceci est utile, car les utilisateurs n’ont pas besoin de se souvenir des orthographes correctes, et peuvent choisir parmi les options disponibles qui s’affichent.

* **Ajoutez une image personnalisée à la nouvelle page d’onglet (NTP) à l’aide d’une stratégie de groupe.** À partir de la version 86 de Microsoft Edge, le protocole NTP offre une option permettant de remplacer l'image par défaut par une image personnalisée fournie par l'utilisateur. La possibilité de gérer les propriétés de cette image est également prise en charge par la stratégie de groupe.

* **Faites correspondre les raccourcis clavier personnalisés à VS Code.** MicrosoftEdgeDevTools prend désormais en charge la personnalisation des raccourcis clavier dans DevTools pour adapter à votre éditeur/IDE. (Dans MicrosoftEdge84, nous avons ajouté la possibilité de faire correspondre les raccourcis clavier DevTools à VSCode).

* **Supprimez les téléchargements à partir du disque à l’aide du gestionnaire de téléchargement.** Les utilisateurs peuvent désormais supprimer leurs fichiers téléchargés à partir de leur disque sans quitter le navigateur. La nouvelle fonctionnalité Supprimer les téléchargements figure dans le menu contextuel de l’étagère téléchargements ou de la page de téléchargement.

### Mises à jour de stratégies

#### Nouvelles stratégies

Vingt-trois nouvelles politiques ont été ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist) : Bloquer l’accès à une liste de services et de cibles d’exportation spécifiée dans Collections.
- [ DefaultFileSystemReadGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultfilesystemreadguardsetting)- Contrôle de l'utilisation de l'API du système de fichiers pour la lecture.
- [ DefaultFileSystemWriteGuardSetting ](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultfilesystemwriteguardsetting) - Contrôle de l'utilisation de l'API du système de fichiers pour l'écriture.
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting): paramètre par défaut des capteurs.
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting): contrôler l’utilisation de l’API Serial.
- [ DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) - Envoyer des données de diagnostic obligatoires et facultatives sur l'utilisation du navigateur.
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed): autoriser l’accès à l’outil Enterprise Mode Site List Manager.
- [FileSystemReadAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemreadaskforurls) - Autoriser l'accès en lecture via l'API du système de fichiers sur ces sites.
- [FileSystemReadBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemreadblockedforurls) - Bloquer l'accès en lecture via l'API du système de fichiers sur ces sites.
- [FileSystemWriteAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemwriteaskforurls) - Autoriser l'accès en écriture aux fichiers et aux répertoires de ces sites.
- [FileSystemWriteBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemwriteblockedforurls) - Bloquer l'accès en écriture aux fichiers et aux répertoires de ces sites.
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
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled): Activer la fonctionnalité User-Agent Client Hints.
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit): limite le nombre de captures instantanées des données utilisateur conservées qui sont utilisées en cas de restauration d’urgence.

#### Stratégies déconseillées

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled): activer les rapports de données d’utilisation et d’incident.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices): Envoyer des informations sur les sites pour améliorer les services Microsoft.

#### Stratégie obsolète

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled): active une fonctionnalité de sécurité TLS 1.3 pour les ancres d’approbation locales.

<!-- end 86 -->
## Version 85.0.564.70: 6octobre

Résolution de divers bogues et problèmes de performances.

## Version 85.0.564.68: 1eroctobre

Résolution de divers bogues et problèmes de performances.

## Version 85.0.564.63: 23 septembre

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-23-2020).

## Version 85.0.564.51: 9 septembre

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-9-2020).

## Version 85.0.564.44: 31 août

Résolution de divers bogues et problèmes de performances.
<!-- begin 85 -->
## Version 85.0.564.41: 27août

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-27-2020).

### Mises à jour des fonctionnalités

- **Synchronisation locale des favoris et des paramètres**. Vous pouvez désormais synchroniser les favoris et paramètres d’un navigateur entre les profils ActiveDirectory au sein de votre propre environnement sans avoir besoin d’effectuer une synchronisation dans le cloud.

- **Prise en charge de la stratégie de groupe MicrosoftEdge pour l’approbation de combinaisons site + application à lancer sans invite de confirmation.**. La prise en charge de la stratégie de groupe ajoutée permet aux administrateurs d’ajouter des combinaisons site+application dont le lancement est approuvé sans invite de confirmation. Cela ajoute la possibilité pour les administrateurs de configurer les combinaisons de protocoles/origines approuvées (par exemple, les applications Microsoft365) pour leurs utilisateurs finaux afin de supprimer l’invite de confirmation lors de la navigation vers uneURL qui contient un protocole d’application.

- **Outil de mise en surbrillancePDF**. Cet outil peut être ajouté à la barre d’outils pour les fichiers PDF afin de mettre en évidence le texte important.

- **L’API d’accès au stockage est disponible**. Cette API d’accès au stockage permet l’accès au stockage interne alors qu’un utilisateur tiers manifeste son intention directe d’autoriser un stockage qui sinon serait bloqué par la configuration actuelle du navigateur. Pour plus d’informations, voir [API d’accès au stockage](https://www.chromestatus.com/feature/5612590694662144).

- **Envoyer à OneNote est disponible pour les collections MicrosoftEdge**. Tout le monde a hâte de pouvoir envoyer des informations rassemblées dans des collections vers OneNote, où l’on peut l’ajouter à un projet plus important et collaborer avec d’autres personnes. Et encore plus important, dans MicrosoftEdge85, vous pourrez envoyer du contenu aux produits *Office pour Mac* (Word, Excel et OneNote) pour le compte Microsoft et AzureActiveDirectory.

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
- [TLSCsipherSuiteDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tlsciphersuitedenylist): spécifier les suites de chiffrementTLS à désactiver.

#### Stratégies obsolètes

- [EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload): activer le téléchargement des actions de domaine à partir de Microsoft.
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) – Réactive les composants WebPart de l’API v0 jusqu’au M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies): autoriser WebDriver à remplacer les stratégies incompatibles.

<!--- END 85 ---->

## Version 84.0.522.63: août 2020

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-20-2020).

## Version 84.0.522.61: 17 août

Résolution de divers bogues et problèmes de performances.

## Version 84.0.522.59: 11 août

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-11-2020).

## Version 84.0.522.58: 10 août

Résolution de divers bogues et problèmes de performances.

## Version 84.0.522.52: 1er août

Résolution de divers bogues et problèmes de performances.

## Version84.0.522.50: 31juillet

Résolution de divers bogues et problèmes de performances.

## Version84.0.522.49: 29juillet

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#july-29-2020).

## Version84.0.522.48: 28juillet

Résolution de divers bogues et problèmes de performances.

## Version84.0.522.44: 23juillet

Résolution de divers bogues et problèmes de performances.

<!-- begin 84 -->
## Version84.0.522.40: 16juillet

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#july-16-2020).

### Mises à jour des fonctionnalités

- Cette version de Microsoft Edge permet un téléchargement plus rapide des listes de sites en mode Internet Explorer. Nous avons réduit le délai de téléchargement des listes de sites en mode Internet Explorer à 0seconde (60secondes d’attente auparavant) en l’absence d’une liste de sites mis en cache. Nous avons également ajouté la prise en charge de la stratégie de groupe pour les cas où les navigations dans la page d’accueil en mode Internet Explorer doivent attendre le téléchargement de la liste des sites. Si vous souhaitez en savoir plus, veuillez consulter la stratégie [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload).

- Microsoft Edge permet désormais aux utilisateurs de se connecter au navigateur lorsque celui-ci est en mode «Exécuter en tant qu’administrateur» sous Windows10. Cette fonctionnalité aide les clients à exécuter Microsoft Edge sur un serveur Windows ou dans les scénarios de bureau à distance et de bac à sable.

- Microsoft Edge fournit à présent une prise en charge complète de la souris en mode plein écran. Vous pouvez à présent utiliser la souris pour accéder aux onglets, à la barre d’adresses et aux autres éléments sans quitter le mode plein écran.

- Amélioration des achats en ligne. Ajoutez des pseudos personnalisés aux cartes de débit ou de crédit enregistrées. Vous pouvez à présent distinguer et différencier vos cartes de crédit lors de vos achats en ligne. L’attribution d’un pseudo à vos cartes de débit ou de crédit vous permet de choisir la carte appropriée lorsque vous utilisez le remplissage automatique pour sélectionner un mode de paiement.

- TLS/1.0 et TLS/1.1 sont désactivés par défaut.  La stratégie [SSLVersionMin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sslversionmin) permet de réactiver TLS/1.0 et TLS/1.1. Cette stratégie reste disponible au moins jusqu’à Microsoft Edge version88. Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Modifications apportées à Microsoft Edge ayant un impact sur la compatibilité des sites](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

- Améliorations des collections:

  - Nous avons ajouté une fonctionnalité d’ajout de note ou de commentaire à un élément d’une collection. Les notes sont regroupées et restent associées à un élément, même si vous triez les éléments d’une collection. Pour essayer cette nouvelle fonctionnalité, cliquez avec le bouton droit sur un élément, puis sélectionnez «Ajouter une note».
  - Vous pouvez modifier la couleur d’arrière-plan des notes dans les collections. Vous pouvez utiliser un codage en couleurs pour vous aider à organiser vos informations et augmenter votre productivité.
  - Des améliorations de performances sont perceptibles, ce qui vous permet d’exporter vos collections vers Excel en moins de temps que dans les versions précédentes de Microsoft Edge.

- Prise en charge supplémentaire de l’API Microsoft Edge:

  - L’API accès au stockage est activée pour les expérimentations. Cette fonctionnalité est activée pour les utilisateurs particuliers et les utilisateurs d’entreprise avec la stratégie de [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/deployedge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) définie sur «Full». Cette fonctionnalité sera activée par défaut pour tous les utilisateurs de la version 85 du canal stable Microsoft Edge.
  
    À mesure que la confidentialité revêt une importance grandissante pour les utilisateurs, ces dernier recherchent, de plus en plus, des valeurs par défaut du navigateur et des paramètres plus stricts de consentement des utilisateurs (blocage de l’accès au stockage tiers, par exemple). Ces paramètres permettent d’améliorer la confidentialité et de bloquer l’accès indésirable de la part d’utilisateurs inconnus ou non approuvés. Cependant, ils peuvent également avoir des effets secondaires indésirables, tels que le blocage de l’accès au contenu nécessaire à l’utilisateur (par exemple, les réseaux sociaux et le contenu multimédia incorporé).

    Cette API d’accès au stockage permet l’accès au stockage interne alors qu’un utilisateur tiers manifeste son intention directe d’autoriser un stockage qui sinon serait bloqué par la configuration actuelle du navigateur. Pour plus d’informations, voir [API d’accès au stockage](https://www.chromestatus.com/feature/5612590694662144).

  - L’API de système de fichiers natif vous permet d’autoriser les sites à modifier des fichiers ou des dossiers.

- Améliorations apportées au contenu PDF:

  - La lecture à voix haute pour PDF permet aux utilisateurs d’écouter du contenu PDF tout en effectuant d’autres tâches éventuellement importantes pour eux. Cela permet également aux apprenants au profil auditif et visuel de se concentrer sur la lecture du contenu, d’où un apprentissage facilité.
  - La modification des fichiers PDF est améliorée. Vous pouvez à présent enregistrer une modification directement dans le fichier PDF au lieu d’enregistrer une copie de ce dernier à chaque modification.

- Microsoft Edge permet à présent la traduction dans le lecteur immersif. Lorsqu’un utilisateur ouvre la vue Lecteur immersif, il peut choisir de traduire la page dans la langue de son choix.

- Plusieurs mises à jour DevTools comprennent notamment la personnalisation des raccourcis clavier pour faire correspondre le code VS et l’affichage du DevTools en contraste élevé.  Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Nouveautés de DevTools (Microsoft Edge 84)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/05/devtools).

### Mises à jour de stratégies

#### Nouvelles stratégies

Nous avons ajouté sept nouvelles stratégies. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [AppCacheForceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#appcacheforceenabled): permet de réactiver la fonctionnalité AppCache, même si elle est désactivée par défaut.
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy): configure les paramètres du proxy conteneur Application Guard.
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload): la liste des sites en mode entreprise doit être disponible avant la navigation par onglets.
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled): utilise le programme de résolution du proxy Windows.
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection): configure la détection améliorée des blocages pour le mode Internet Explorer.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)-pour réduire l’UC et la consommation d’énergie, Microsoft Edge détecte quand une fenêtre est couverte par d’autres fenêtres et suspend les pixels de peinture.
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout): définit un délai d’expiration de la navigation par onglets pour la liste des sites en mode entreprise.

#### Stratégies déconseillées

- [AllowSyncXHRInPageDismissal](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal): autorise les pages à envoyer des demandes XHR synchrones lors de l’opération de rejet de page.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) – Indique si le vérificateur de certificats intégré est utilisé pour la vérification des certificats de serveur.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled): active un traitement plus strict pour des contenus mixtes.

#### Stratégie obsolète

[ForceNetworkInProcess](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcenetworkinprocess): force l’exécution du code de mise en réseau dans le processus du navigateur.

<!-- End 84 -->
## Version83.0.478.64: 13juillet

Résolution de divers bogues et problèmes de performances.

## Version83.0.478.61: 7juillet

Résolution de divers bogues et problèmes de performances.

## Version83.0.478.58: 30juin

Résolution de divers bogues et problèmes de performances.

## Version83.0.478.56: 24juin

Résolution de divers bogues et problèmes de performances.

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-24-2020).

## Version83.0.478.54: 17juin

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-17-2020).

## Version83.0.478.50: 15juin

Résolution de divers bogues et problèmes de performances.

## Version83.0.478.45: 4juin

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-4-2020).

## Version83.0.478.44: 1erjuin

Résolution de divers bogues et problèmes de performances.

## Version83.0.478.37: 21mai

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#may-21-2020).

### Mises à jour des fonctionnalités

- Les mises à jour de Microsoft Edge se déploient à présent progressivement. À l’avenir, le déploiement des mises à jour de Microsoft Edge s’effectuera sur les systèmes de nos utilisateurs en quelques jours. Cela nous permet de mieux vous protéger contre les mises à jour boguées accidentelles, ce qui améliore votre expérience de mise à jour. En tant qu’utilisateur, vous continuerez à bénéficier de mises à jour automatiques transparentes. Si votre organisation n’est pas inscrite aux mises à jour automatiques, cette modification ne vous concernera pas. Pour en savoir plus, veuillez consulter l’[article sur les déploiements progressifs](microsoft-edge-update-progressive-rollout.md).
- Améliorations apportées à Microsoft Defender SmartScreen: améliorations apportées au service Microsoft Defender SmartScreen, telles que la protection améliorée contre les sites malveillants qui redirigent au chargement et le blocage de trames de niveau supérieur, qui remplace complètement les sites malveillants avec la page de sécurité Microsoft Defender SmartScreen. Le blocage de trames de niveau supérieur empêche la lecture du contenu audio et d’autres éléments multimédias du site malveillant, ce qui permet d’obtenir une expérience plus facile et moins confuse.

- En réponse aux commentaires des utilisateurs, vous pouvez désormais exempter certains cookies de l’effacement automatiquement lorsque le navigateur se ferme. Cette option est utile s’il existe un site dont les utilisateurs ne souhaitent pas être déconnectés, mais souhaitent tout de même que tous les autres cookies soient supprimés lorsque le navigateur se ferme. Pour utiliser cette fonctionnalité, accédez à *edge://settings/clearBrowsingDataOnClose* et activez le bouton bascule «cookies et autres données de site».

- Le basculement de profil automatique est désormais disponible pour vous aider à accéder à votre contenu professionnel plus facilement dans les profils. Si vous utilisez plusieurs profils au travail, vous pouvez les consulter en accédant à un site nécessitant une authentification à partir de votre compte professionnel ou scolaire sur votre profil personnel. Lorsque nous détectons ce problème, vous êtes invité à basculer vers votre profil de travail pour accéder à ce site sans devoir s’y authentifier. Lorsque vous choisissez le profil de travail vers lequel vous voulez basculer, le site Web s’ouvre simplement dans votre profil de travail. Cette fonctionnalité de commutation de profil vous permet de séparer vos données professionnelles et personnelles et d’accéder à votre contenu professionnel plus facilement. Si vous ne souhaitez pas que la fonctionnalité vous invite à changer de profil, vous pouvez choisir l’option ne plus poser de message.

- Améliorations des fonctionnalités de recouvrement:
  - Vous pouvez utiliser la fonction glisser-déplacer pour ajouter un élément à une collection sans ouvrir la collection. Pendant le glisser-déplacer, vous pouvez également choisir un emplacement dans la liste des collections où vous voulez placer l’élément.
  - Vous pouvez ajouter plusieurs éléments à une collection au lieu d’y ajouter un élément à la fois. Pour ajouter plusieurs éléments, sélectionnez les éléments, puis faites-les glisser vers une collection. Vous pouvez également sélectionner les éléments, cliquer avec le bouton droit et choisir la collection dans laquelle vous voulez placer les éléments.

- Vous pouvez ajouter tous les onglets d’une fenêtre de bord dans une nouvelle collection sans les ajouter individuellement. Pour ce faire, cliquez avec le bouton droit sur un onglet, puis sélectionnez «Ajouter tous les onglets à une nouvelle collection».

- La synchronisation d’extension est désormais disponible. Vous pouvez désormais synchroniser vos extensions sur tous vos appareils. Les extensions des magasins Microsoft et chrome sont synchronisées avec Microsoft Edge. Pour utiliser cette fonctionnalité: cliquez sur les points de suspension (**…**) dans la barre de menus, puis sélectionnez **Paramètres**. Sous votre profil, cliquez sur **Synchroniser** pour afficher les options de synchronisation. Sous **Profils/synchronisation** utilisez le bouton bascule pour activer les extensions. Vous pouvez utiliser la stratégie de groupe [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) pour désactiver la synchronisation des extensions.

- Message amélioré sur la page gestion des téléchargements pour les téléchargements non sécurisés qui ont été bloqués.

- Améliorations du lecteur immersif:
  - Ajout d’une prise en charge des adverbes dans les parties de l’expérience de reconnaissance vocale dans le lecteur immersif. Lors de la lecture d’un article dans le lecteur immersif, ouvrez les outils de vérification de la grammaire et activez les adverbes dans certains secteurs vocaux pour mettre en surbrillance toutes les adverbes de la page.
  - Ajout de la possibilité de sélectionner le contenu d’une page Web et de l’ouvrir dans le lecteur immersif. Cette possibilité permet aux utilisateurs d’utiliser le lecteur immersif et tous les outils d’apprentissage, tels que le focus de ligne et la lecture à haute voix sur tous les sites Web.

- Le docteur de lien fournit une correction de l’hôte et une requête de recherche aux utilisateurs lorsqu’ils ne tapent pas une URL. Par exemple: <br>
Un utilisateur saisit «powerbi» comme «powerbbi».com. Le docteur de lien suggère «powerbi».com comme correction et crée un lien pour rechercher « powerbbi» au cas où l’utilisateur cherche quelque chose d’autre.

- Autoriser les utilisateurs à enregistrer leur décision de lancement d’un protocole externe pour un site spécifique. Les utilisateurs peuvent configurer la stratégie de [ExternalProtocolDialogShowAlwaysOpenCheckbox]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) pour activer ou désactiver cette fonctionnalité.

- Les utilisateurs peuvent régler Microsoft Edge comme navigateur par défaut directement à partir de Microsoft Edge **Paramètres**. Cela permet aux utilisateurs de modifier facilement leur navigateur par défaut, dans le contexte du navigateur lui-même, au lieu d’effectuer une recherche dans les paramètres du système d’exploitation. Pour utiliser cette fonctionnalité, accédez à *edge://settings/defaultBrowser*, puis cliquez sur **Utiliser par défaut**.

- Plusieurs mises à jour de DevTools, y compris la prise en charge du débogage distant, l’amélioration de l’interface utilisateur et bien plus encore. Pour plus d’informations, consultez [Nouveautés de DevTools (Microsoft Edge 83)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

- Le scénario d’avertissement MCAS (Microsoft Cloud Access Security) est à présent disponible. Ainsi, les administrateurs peuvent configurer l’avertissement, nouvelle catégorie de blocs MCAS, où l’utilisateur peut remplacer une page de bloc MCAS. Nous avons intégré les blocs MDATP E5 en mode natif avec les blocs SmartScreen dans Microsoft Edge pour offrir une expérience transparente. Cette expérience permet d’utiliser un bloc rouge de page complète avec le message «ce site web est bloqué par votre organisation», au lieu d’une simple notification toast.

- Ne pas autoriser les XmlHttpRequest synchrones lors du rejet de page. L’envoi de XmlHttpRequest asynchrones lors du déchargement d’une page web sera supprimé. Cette modification améliore les performances et la fiabilité du navigateur. Cependant, elle peut avoir un impact sur les applications web non mises à jour pour utiliser des API web plus modernes, notamment sendBeacon et FETCH. La stratégie de groupe permettant de désactiver cette modification et d’autoriser les XHR synchrones lors du rejet de page sera disponible jusqu’à Migrosoft Edge88. Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Modifications apportées à Microsoft Edge ayant un impact sur la compatibilité des sites](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

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

<!-- end 83 -->

## Version81.0.416.77: 18mai

Résolution de divers bogues et problèmes de performances.

## Version 81.0.416.72: 7mai

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#may-7-2020).

## Version 81.0.416.68: 29avril

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-29-2020).

## Version81.0.416.64: 23avril

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-23-2020).

## Version 81.0.416.58: 17avril

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-17-2020).

## Version 81.0.416.53: 13avril

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-13-2020).

### Mises à jour des fonctionnalités

- Ajout de la prise en charge de la Protection des données Windows (WIP), qui permet aux entreprises de protéger les données sensibles contre toute divulgation non autorisée. [En savoir plus](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection).

- Les collections sont désormais disponibles. Pour démarrer, cliquez sur l’icône Collections située près de la barre d’adresses. Cette action ouvre le volet Collections dans lequel vous pouvez créer, modifier et afficher des collections. Les Collections ont été conçues en fonction de votre activité sur le web. Si vous êtes un client, un voyageur, un enseignant ou un étudiant, les Collections peuvent vous être utiles. [En savoir plus](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Autoriser la suppression (Masquer dans la barre d’outils) du bouton Collections de la barre d’outils Microsoft Edge par souci de cohérence.

- La connexion automatique d'un compte Active Directory local est ciblée uniquement pour les organisations qui l’activent.  Si des utilisateurs ont déjà ouvert une session avec un compte Active Directory local, ils pourront se déconnecter. Les utilisateurs se connectent automatiquement au compte principal de leur système d’exploitation uniquement s’il s’agit d’un compte Microsoft ou Azure Active Directory. Les administrateurs peuvent activer la connexion automatique à l’aide d’un compte Azure Active Directory local utilisant la stratégie ConfigureOnPremisesAccountAutoSignIn.

- ApplicationGuard. La prise en charge des extensions est désormais disponible dans le conteneur.

- Nous avons ajouté un message pour informer les utilisateurs qu’Internet Explorer n'est pas installé lorsqu’ils naviguent vers une page configurée pour s’ouvrir en mode Internet Explorer.

- Mise à jour de l’outil d'affichage3D dans Microsoft Edge DevTools avec une nouvelle fonctionnalité permettant de déboguer le contexte d'empilement de l’index-Z. L’affichage3D affiche une représentation de la profondeur de Document Object Model (DOM) à l’aide de la couleur et de l’empilement et l’affichage index-Z vous permet d’isoler les différents contextes d’empilage de votre page. [En savoir plus](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- Les outils F12 Dev sont localisés dans 10nouvelles langues pour qu'ils correspondent à la langue utilisée dans le reste du navigateur. [En savoir plus](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Ajout de la prise en charge de la lecture Dolby Vision. Sur la Build 17134 (mise à jour d'avril2018) de Windows10 compatible Dolby Vision, les sites web peuvent désormais afficher le contenu Dolby Vision. Découvrez comment activer le contenu Dolby Vision sur [Netflix](https://help.netflix.com/en/node/42384).

- Microsoft Edge peut désormais identifier et supprimer des favoris dupliqués et fusionner des dossiers portant le même nom. Pour accéder à cet outil, cliquez sur l’étoile dans la barre d’outils du navigateur, puis sélectionnez «Supprimer les favoris dupliqués».  Vous pouvez confirmer les modifications et les mises à jour apportées à vos favoris seront synchronisées sur tous les appareils.

- Des utilisateurs ont signalé qu'il peut être difficile de distinguer une fenêtre de navigation normale dans un thème foncé d’une fenêtre InPrivate, car les deux cadres de fenêtre sont sombres. La nouvelle icône pilule bleue InPrivate dans le coin supérieur droit permet de garantir aux utilisateurs qu'ils naviguent en mode InPrivate.

- Ouvrir des liens externes dans le profil de navigateur adéquat. Sélectionnez un profil par défaut pour les liens ouverts afin que les applications externes s’ouvrent à partir de *edge://settings/multiProfileSettings*.

- Ajout d'un avertissement informant les utilisateurs qui se connectent à un profil de navigateur avec un compte après s’être précédemment connectés avec un compte différent. Cet avertissement permet d'empêcher la fusion involontaire de données.

- Si vous avez enregistré des cartes de paiement dans votre compte Microsoft, vous pouvez les utiliser dans Microsoft Edge lorsque vous saisissez des formulaires de paiement. Les cartes de votre compte Microsoft sont synchronisées sur tous les appareils de bureau et les informations détaillées sont partagées avec le site web après une authentification à deux facteurs (code CVC et votre identité Microsoft). Pour plus de commodité, vous pouvez choisir d’enregistrer, de manière sécurisée, une copie de la carte sur l’appareil durant l’authentification.

- La fonctionnalité Focus sur lignes est conçue pour les utilisateurs qui aiment se concentrer sur une partie limitée du contenu qu'ils lisent. Elle permet aux utilisateurs de se concentrer sur une, trois ou cinqlignes à la fois et assombrit le reste de la page pour leur permettre de lire sans aucune distraction. Les utilisateurs peuvent faire défiler l’écran à l’aide de l'interaction tactile ou des touches de direction pour que la concentration se déplace en conséquence.

- Microsoft Edge est désormais intégré au vérificateur d'orthographe de Windows sur les plateformes Windows8.1 et ultérieures. Cette intégration offre une prise en charge linguistique accrue, avec un accès à d’autres dictionnaires linguistiques et la possibilité d’utiliser des dictionnaires personnalisés de Windows. Aucune action supplémentaire n’est requise de la part des utilisateurs lorsqu’une langue a été ajoutée dans les paramètres de langue du système d’exploitation. De plus, une touche bascule de vérification orthographique dans la langue est activée dans les paramètres de Microsoft Edge.

- Lorsque des documents PDF sont ouverts à l’aide de Microsoft Edge, les utilisateurs peuvent désormais créer ou supprimer des surbrillances et modifier la couleur. Cette fonctionnalité vous permet de référencer par la suite les parties importantes d'un document et de travailler en collaboration.

- Lors du chargement de longs documents PDF optimisés pour le web, les pages consultées par l’utilisateur sont chargées plus rapidement, parallèlement au chargement du reste du document.

- Il est désormais plus simple de démarrer le lecteur immersif pour un site web en appuyant sur la touche F9.

- Il est désormais plus facile de démarrer la lecture à haute voix à l’aide d’un raccourci clavier (Ctrl+Maj+U).

- Ajout d’un paramètre de ligne de commande MSI qui vous permet de supprimer la création d’une icône de bureau lors de l’installation de Microsoft Edge. L’exemple suivant montre comment utiliser ce nouveau paramètre: <br>
`MicrosoftEdgeEnterpriseX64.msi DONOTCREATEDESKTOPSHORTCUT=true`<br>
Une stratégie de groupe prendra en charge cette fonctionnalité dans une prochaine publication.

### Mises à jour de stratégies

#### Nouvelles stratégies

11 nouvelles stratégies ont été ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled): active l’authentification ambiante pour les profils InPrivate et Invité. 
- [AudioSandboxEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#audiosandboxenabled): autorise l’exécution du bac à sable audio.
- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy): utiliser une stratégie de référent par défaut de no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#globallyscopehttpauthcacheenabled): active le cache d’authentification HTTP de portée globale.
- [ImportExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importextensions): autorise l’importation d’extensions.
- [ImportCookies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importcookies): autorise l’importation de cookies.
- [ImportShortcuts](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importshortcuts): autorise l’importation de raccourcis.
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect): spécifie la manière dont les navigations «dans la page» vers les sites non configurés se comportent lorsque vous démarrez à partir des pages du mode Internet Explorer.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled): active un traitement plus strict pour des contenus mixtes.
- [TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled): active une fonctionnalité de sécurité TLS 1.3 pour les ancres d’approbation locales.
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin): configure la connexion automatique avec un compte de domaine Azure Active Directory lorsqu'il n'existe pas de compte de domaine Azure Active Directory.

#### Nom de la stratégie et modifications des légendes

La stratégie `OmniboxMSBProviderEnabled` est remplacée par [AddressBarMicrosoftSearchInBingProviderEnabled](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled). La légende de la stratégie est «activer la recherche Microsoft dans les suggestions de Bing dans la barre d’adresses».

#### Stratégies déconseillées

Les stratégies suivantes fonctionnent encore dans cette version. Elles deviendront «obsolètes» dans une prochaine version.

- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled): réactive les composants WebPart de l’API v0 jusqu’au M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies): autorise WebDriver à substituer Incompatible.

#### Problèmes résolus

- Résolution d’un problème dans lequel le mode IE dans Microsoft Edge provoquait l’affichage d’une boîte de dialogue de téléchargement continu, même une fois le fichier téléchargé.
- Résolution d’un problème dans lequel Microsoft Edge supprimait les cookies de session lorsqu’une page déjà en mode IE était déclenchée pour ouvrir un nouvel onglet de mode IE.

## Version 80.0.361.111: 7avril

Résolution de divers bogues et problèmes de performances.

## Version 80.0.361.109: 1eravril

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-1-2020).

## Version80.0.361.69: 19mars

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-19-2020).

## Version80.0.361.66 du 4mars

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-4-2020).

## Version80.0.361.62 du 25février

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#february-25-2020).

## Version80.0.361.57 du 20février

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#february-20-2020).

## Version80.0.361.56 du 19février

Résolution de divers bogues et problèmes de performances.

## Version80.0.361.54 du 14février

### Problèmes résolus

- Résolution d'un problème lié à un échec de l'importation du mot de passe, du paiement et des cookies dans Microsoft Edge.

## Version80.0.361.50 du 11février

Résolution de divers bogues et correctifs de performances.

## Version80.0.361.48 du 7février

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#february-7-2020).

### Mises à jour des fonctionnalités

- Ajout de la protection SmartScreen lors du téléchargement d’applications potentiellement indésirables. [En savoir plus](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus)
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

### Mises à jour de stratégie

#### Nouvelles stratégies

16 nouvelles stratégies ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Les nouvelles stratégies suivantes ont été ajoutées.

- [AlternateErrorPagesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#alternateerrorpagesenabled): suggère des pages similaires lorsqu’une page web est introuvable.
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting) – Contrôle de l’utilisation d’exceptions de contenu non sécurisées.
- [DNSInterceptionChecksEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsinterceptionchecksenabled) – Tests d’interception de DNS activés.
- [HideFirstRunExperience](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hidefirstrunexperience) – Masque l’utilisation de la première exécution et l’écran de démarrage.
- [InsecureContentAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecurecontentallowedforurls) Autorise le contenu non sécurisé sur des sites spécifiques.
- [InsecureContentBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecurecontentblockedforurls) – Bloque le contenu non sécurisé sur des sites spécifiques.
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) – Active le paramètre de comportement de cookie SameSite hérité par défaut.
- [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) – Rétablissement du comportement SameSite hérité pour les cookies sur des sites spécifiques.
- [PaymentMethodQueryEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#paymentmethodqueryenabled) – Permet aux sites Web d’interroger les modes de paiement disponibles.
- [PersonalizationReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#personalizationreportingenabled) – Permet de personnaliser des publicités, des recherches et des actualités en envoyant un historique de navigation à Microsoft.
- [PinningWizardAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pinningwizardallowed) – Autorise l’assistant épingler à la barre des tâches.
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled) – Configure Microsoft Defender SmartScreen pour bloquer les applications potentiellement indésirables.
- [TotalMemoryLimitMb](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#totalmemorylimitmb) – Définit une limite en mégaoctets de mémoire qu’une seule instance de Microsoft Edge peut utiliser.
- [WebAppInstallForceList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webappinstallforcelist) – Configure la liste des applications Web installées en force.
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) – Réactive les composants WebPart de l’API v0 jusqu’au M84.
- [WebRtcLocalIpsAllowedUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalipsallowedurls) – Gère l’exposition des adresses IP locales par WebRTC.

#### Stratégies déconseillées

La stratégie suivante a été déconseillée.

- [NewTabPageCompanyLogo](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagecompanylogo) – Définit le logo de la société sur l’onglet nouveau.

### Problèmes résolus

- Résolution d’un problème qui empêchait l’audio de fonctionner dans un environnement Citrix.
- Résolution d’un problème dans lequel l’expérience de Microsoft Edge et l’ancienne version de Microsoft Edge côte à côte généraient des liens hérités rompus et des blocages.

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
