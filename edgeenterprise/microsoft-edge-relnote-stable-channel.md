---
title: Notes de publication de Microsoft Edge pour le canal stable
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/13/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notes de publication de Microsoft Edge pour le canal stable
ms.openlocfilehash: a69b6cd7ab1fa077f2a72c01fa363fcc0efdcf24
ms.sourcegitcommit: 498a62144b099a1198c06f98ad010cf95aa33727
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/13/2021
ms.locfileid: "11268235"
---
# Notes de publication du canal stable Microsoft Edge

Ces notes de publication fournissent des informations sur les nouvelles fonctionnalités et les mises à jour non liées à la sécurité qui sont incluses dans le canal stable Microsoft Edge.

- L'ensemble des mises à jour de sécurité est répertorié [ici](microsoft-edge-relnotes-security.md).
- Les notes de publication archivées pour le canal stable Microsoft Edge sont situées [ici](microsoft-edge-relnote-archive-stable-channel.md).

 Si vous souhaitez en savoir plus sur les canaux MicrosoftEdge, veuillez consultez la rubrique [Vue d’ensemble des canaux Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Pour le canal stable, le déploiement des mises à jour sera progressif et durera un ou plusieurs jours. Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Déploiements progressifs pour les mises à jour de Microsoft Edge](microsoft-edge-update-progressive-rollout.md).

## Version87.0.664.75: 7janvier

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-7-2021).

## Version 87.0.664.66: 17 décembre

Résolution de divers bogues et problèmes de performances.

## Version 87.0.664.60 : 10 décembre

Résolution de divers bogues et problèmes de performances.

## Version 87.0.664.57 : 7 décembre

Résolution de divers bogues et problèmes de performances. Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#december-7-2020).

## Version 87.0.664.55: 3 décembre

Résolution de divers bogues et problèmes de performances. La fonctionnalité suivante a été mise à jour pour cette version.

- **L’option achat est activée par défaut**. À partir de la version 87 de Microsoft Edge, les utilisateurs de l’entreprise peuvent profiter d’achats dans Microsoft Edge. Grâce aux fonctionnalités d’achat, Microsoft Edge permet aux utilisateurs de trouver des coupons et de meilleurs prix lors de leurs achats en ligne. (L’interface de coupon a été publiée avec la version stable 87.0.664.41). L’interface de comparaison des prix est désormais disponible dans cette mise à jour. Cette fonctionnalité peut être configurée à l’aide de la stratégie [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgeshoppingassistantenabled). Consultez notre [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) et [En savoir plus](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) sur les Achats Microsoft.

## Version 87.0.664.52: 30 novembre

Résolution de divers bogues et problèmes de performances.

## Version 87.0.664.47: 23novembre

Résolution de divers bogues et problèmes de performances.

<!-- begin major 87 --->
## Version87.0.664.41: 19novembre

Nous avons répertorié les mises à jour de sécurité [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-19-2020).

### Mises à jour des fonctionnalités

- **Redirection automatique pour les sites incompatibles d’InternetExplorer vers MicrosoftEdge**. À partir de la mise à jour stable de MicrosoftEdge87, les sites web publics qui affichent un message d’incompatibilité sur InternetExplorer seront automatiquement redirigés vers MicrosoftEdge. Pour en savoir plus et configurer cette interface, voir la [Redirection des sites incompatibles](https://docs.microsoft.com/deployedge/edge-learnmore-neededge).

- **Activation des fonctionnalités de confidentialité en mode plein écran**. À partir de la version87 de MicrosoftEdge, les fonctionnalités du mode plein écran seront activées et permettront aux entreprises de garantir la confidentialité des données utilisateur. Ces fonctionnalités activent les expériences telles que l’effacement des données utilisateur à la fermeture, la suppression des fichiers téléchargés et la réinitialisation de l’expérience de démarrage configurée après une durée inactivité déterminée. En savoir plus sur la [Configuration du mode plein écran MicrosoftEdge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).

- **Fonctionnalités d’achat activées par défaut**. À partir de la version87 de MicrosoftEdge, les utilisateurs entreprise peuvent également bénéficier des achats dans MicrosoftEdge. Grâce aux fonctionnalités Achats, MicrosoftEdge permet aux utilisateurs de trouver des bons de réduction et de meilleurs tarifs lors de leurs achats en ligne. La fonction des bons de réduction est disponible avec cette mise à jour et la fonctionnalité de comparaison des prix sera publiée dans les prochaines mises à jour de MicrosoftEdge version87. Vous pouvez configurer cette fonctionnalité via la stratégie [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) . Consultez notre [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) et [En savoir plus](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) sur les Achats Microsoft.

- **Activation du déploiement ClickOnce par défaut**. L’activation de ClickOnce par défaut dans Microsoft Edge 87, réduit les difficultés des entreprises à déployer des logiciels et mieux s’aligner sur le comportement du navigateur Microsoft Edge Legacy. Au démarrage de Microsoft Edge 87, l’état «Non Configuré» de la stratégie ClickOnceEnabled reflète le nouvel état par défaut Activé de la stratégie ClickOnce (comparé à l’État par défaut Désactivé précédent).

- **La page nouvel onglet de l’entreprise (NTP) intègre la productivité avec un contenu de flux de travail personnalisable**. La Page Nouvel Onglet de l’Entreprise combine la page de productivité d’Office 365 que nous proposons aux utilisateurs connectés à leur compte professionnel ou scolaire, avec des flux professionnels personnalisés qui sont organisés en une seule page. Les utilisateurs reconnaîtront le contenu familier Office365 et MicrosoftSearch pour les entreprises optimisé par Bing. Par ailleurs, il peuvent facilement personnaliser «Mon flux» en choisissant le contenu le plus pertinent pour eux à partir du contenu et des modules disponibles pour leur organisation. Les administrateurs informatiques peuvent contrôler les paramètres de flux d’actualités pour leur organisation, notamment le secteur sélectionné pour la nouvelle page d’onglets MicrosoftEdge en accédant au Centre d’administration Microsoft365. [Si vous souhaitez en savoir plus](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

- **Confidentialité et sécurité:**

  - Jeton TLS de support Obligatoire pour les sites configurés par une stratégie. Le jeton TLS obligatoire permet d’éviter les attaques par vol de jetons afin de s’assurer que les cookies ne peuvent pas être réutilisés à partir d’un autre appareil que l’appareil sur lequel ils ont été initialement définis. L’utilisation du jeton TLS obligatoire nécessite la définition de la stratégie [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) et nécessite que les sites répertoriés prennent en charge cette fonctionnalité.

- **Prise en charge du clavier pour le surligneur des fichiers PDF**. Les utilisateurs peuvent utiliser leurs touches de clavier pour surligner des textes de fichiers PDF.

- **Impression:**

  - Sélectionnez le côté à retourner lors de l’impression recto verso. Les utilisateurs peuvent choisir de retourner sur le côté long ou sur le côté court d’une feuille lors de l’impression recto verso.
  - Sélectionnez le mode de tramage de l’impression pour l’entreprise. Contrôlez l’impression Microsoft Edge sur une imprimante non-PostScript sur Windows. Parfois l’ impression sur des imprimantes non-PostScript doit être tramée pour imprimer correctement. Les options d’impression sont «Complètes» et «Rapides».

### Mises à jour de stratégies

#### Nouvelles stratégies

Ajout de dix nouvelles stratégies. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://www.microsoft.com/edge/business/download). Les nouvelles stratégies suivantes ont été ajoutées.

- [ConfigureFriendlyURLFormat](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configurefriendlyurlformat) - Configurez le format de collage par défaut des URL copiées à partir de MicrosoftEdge et déterminez si d’autres formats sont disponibles pour les utilisateurs.
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) -Achats activés dans MicrosoftEdge.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hideinternetexplorerredirectuxforincompatiblesitesenabled) - Masquez la boite de dialogue de redirection ponctuelle et la bannière sur MicrosoftEdge.
- [KioskAddressBarEditingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) - Configurez la modification de la barre d’adresses pour l’expérience de navigation publique en mode plein écran.
- [KioskDeleteDownloadsOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) - Supprimez des fichiers téléchargés sous la session plein écran lorsque MicrosoftEdge se ferme.
- [PasswordRevealEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordrevealenabled) -Activez le bouton Affichage du mot de passe.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerpreventbhoinstall) -Empêchez l’installation de l’objet d’assistance du navigateur (BHO) pour rediriger les sites incompatibles d’InternetExplorer vers MicrosoftEdge.
- [RedirectSitesFromInternetExplorerRedirectMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerredirectmode) - Redirigez les sites incompatibles de InternetExplorer vers MicrosoftEdge.
- [SpeechRecognitionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#speechrecognitionenabled) - Configurez la Reconnaissance vocale.
- [WebCaptureEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcaptureenabled) -Activez la fonctionnalité de capture web dans MicrosoftEdge.

#### Stratégie Déconseillée

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) - Configurez l’expérience de la page nouvel onglet de Microsoft Edge.

#### Stratégie obsolète

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) - Réactivez les fonctionnalités de plateforme web déconseillées pendant une période limitée.

<!-- end major 87 -->

## Version86.0.622.69: 13novembre

Nous avons répertorié les mises à jour de sécurité [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-13-2020). Cette mise à jour contient [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) et [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), signalés par l’équipe Chromium comme cible code malveillant exploitant une faille de sécurité.

## Version 86.0.622.68: 11 novembre

Les mises à jour de sécurité sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-11-2020).

## Version 86.0.622.63: 4novembre

Nous avons répertorié les mises à jour de sécurité [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-4-2020). Cette mise à jour contient [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), signalé par l’équipe Chromium comme cible de code malveillant exploitant une faille de sécurité.

## Version 86.0.622.61: 2novembre

Résolution de divers bogues et problèmes de performances.

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

<!-- Archived to version 84.0.522.40: July 16 -->

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
