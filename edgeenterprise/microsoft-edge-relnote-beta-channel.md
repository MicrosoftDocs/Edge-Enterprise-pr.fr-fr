---
title: Notes de publication de Microsoft Edge pour le canal bêta
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 07/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Notes de publication de Microsoft Edge pour le canal bêta
ms.openlocfilehash: d5e4a4807a12cfd50cd0efaeab672361c68a1508
ms.sourcegitcommit: e3a30351b02226aa042153f17636d64a12c4518b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "11643940"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Notes de publication du canal Microsoft Edge Beta

Ces notes de publication fournissent des informations sur les nouvelles fonctionnalités et les mises à jour non liées à la sécurité qui sont incluses dans le canal Microsoft Edge Beta. Les versions archivées de ces notes de publication sont disponibles [ici](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> La plateforme web Microsoft Edge évolue constamment pour améliorer l’expérience utilisateur, la sécurité et la confidentialité. Pour en savoir plus, consultez les [modifications qui ont un impact sur la compatibilité du prochain Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-92090245-july-12"></a>Version 92.0.902.45 : 12 juillet

Résolution de divers bogues et problèmes de performances.

## <a name="version-92090240-july-6"></a>Version 92.0.902.40 : 6 juillet

Résolution de divers bogues et problèmes de performances.

## <a name="version-92090222-june-21"></a>Version 92.0.902.22 : 21 juin

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- **Recherche en langage naturel pour l’historique du navigateur dans la barre d’adresses.** La recherche de l’article/site web que vous recherchez est désormais plus facile grâce à la recherche en langage naturel directement à partir de la barre d’adresses. Vous pouvez trouver des résultats de recherche basés sur le contenu/description/minutage de la page (par exemple, « recette de recette de la semaine dernière ») en plus des titres/url par correspondances de mots clés.
Veuillez noter qu’il s’agit d’un déploiement de fonctionnalités contrôlé. Si cette fonctionnalité n’est pas présente, consultez-la prochainement lorsque nous continuerons notre déploiement.

- **Les utilisateurs peuvent facilement passer en mode Internet Explorer sur Microsoft Edge**. À partir de Microsoft Edge version 92, les utilisateurs peuvent recharger un site en mode Internet Explorer sur Microsoft Edge au lieu de s’appuyer sur l’application Autonome Internet Explorer 11 en attendant qu’un site soit configuré dans la liste des sites en mode Enterprise. Les utilisateurs sont invités à ajouter le site à leur liste de sites locale afin que la navigation vers la même page dans Microsoft Edge s’effectue automatiquement en mode IE pendant les 30 prochains jours. Vous pouvez utiliser la stratégie *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)* pour configurer cette expérience et autoriser l’accès aux points d’entrée du mode Internet Explorer, ainsi que la possibilité d’ajouter des sites à la liste des sites locale. Vous pouvez utiliser la stratégie *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)* pour ajuster le nombre de jours afin de conserver les sites dans la liste des sites locale.
Notez que KB5003698 ou version ultérieure est nécessaire pour Windows 10 version 1909 ; ou KB5003690 ou version ultérieure est requis pour Windows 10, version 2004, Windows 10, version 20H2 ou Windows 10, version 21H1 pour l’expérience de bout en bout.

- **Par défaut, les fichiers MHTML s’ouvrent en mode Internet Explorer**. À partir de Microsoft Edge version 92 stable, les types de fichiers MHTML s’ouvrent automatiquement en mode Internet Explorer sur Microsoft Edge au lieu de l’application Internet Explorer (IE11). Cela est le plus souvent observé lors de la tentative d’affichage des courriers Outlook dans un navigateur. Cette modification se produit uniquement si IE11 est le gestionnaire par défaut pour ce type de fichier. Si vous préférez modifier cela, vous pouvez le faire avant d’installer la mise à jour stable version 92 à l’aide [de ces conseils](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

- **Les instruments de paiement sont désormais synchronisés sur plusieurs appareils**. À partir Microsoft Edge version 92, vous avez la possibilité de synchroniser vos informations de paiement sur vos appareils connectés.
Veuillez noter qu’il s’agit d’un déploiement de fonctionnalités contrôlé. Si cette fonctionnalité n’est pas présente, consultez-la prochainement lorsque nous continuerons notre déploiement.

- **L’avertissement « Désactiver les extensions du mode développeur » peut être définitivement ignoré**. À partir Microsoft Edge version 92, vous pouvez désactiver l’avertissement « Désactiver les extensions du mode développeur » en cliquant sur l’option « Ne plus afficher cette option ».
Veuillez noter qu’il s’agit d’un déploiement de fonctionnalités contrôlé. Si cette fonctionnalité n’est pas présente, consultez-la prochainement lorsque nous continuerons notre déploiement.

- **Gérez vos extensions directement à partir de la barre d’outils**. Le menu des toutes nouvelles extensions de la barre d’outils vous permet de masquer/épingler facilement les extensions. Les liens rapides pour gérer les extensions et trouver de nouvelles extensions vous permettra de trouver facilement de nouvelles extensions et de gérer vos extensions existantes.
Veuillez noter qu’il s’agit d’un déploiement de fonctionnalités contrôlé. Si cette fonctionnalité n’est pas présente, consultez-la prochainement lorsque nous continuerons notre déploiement.

- **HTTPS automatique**. Les utilisateurs auront la possibilité de mettre à niveau la navigation de HTTP vers HTTPS sur les domaines susceptibles de prendre en charge ce protocole plus sécurisé. Cette prise en charge peut également être configurée pour tenter la remise sur HTTPS pour tous les domaines.
Veuillez noter : nous expérimentons cette fonctionnalité et ce comportement n’est pas visible si vous avez refusé d’expérimenter.

- **Améliorations apportées au rendu des polices**. Des améliorations ont été apportées au rendu du texte afin d’améliorer la clarté et de réduire le flou.
Veuillez noter qu’il s’agit d’un déploiement de fonctionnalités contrôlé. Si cette fonctionnalité n’est pas présente, consultez-la prochainement lorsque nous continuerons notre déploiement.

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

Huit nouvelles stratégies ont été ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://www.microsoft.com/edge/business/download). Les nouvelles stratégies suivantes ont été ajoutées :

- [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) Authentification unique pour les sites professionnels ou scolaires en utilisant ce profil activé.
- [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) Configurer le protocole HTTPS automatique
- [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) Contrôler l’utilisation du mode sans affichage
- [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) Spécifie s’il faut autoriser les sites web non sécurisés à effectuer des demandes vers des points de terminaison de réseau plus privés
- [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) Autoriser les sites répertoriés à effectuer des demandes vers des points de terminaison de réseau plus privés à partir de contextes non sécurisés
- [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) Spécifier le nombre de jours pendant lequel un site reste dans la liste des sites en mode IE local
- [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) Autoriser le rechargement des sites non configurés en mode Internet Explorer
- [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) Spécifie si SharedArrayBuffers peut être utilisé dans un contexte non isolé inter-origines

#### <a name="obsoleted-policy"></a>Stratégie obsolète

- [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) Autoriser les certificats signés à l’aide de SHA-1 lorsqu’ils sont émis par des ancres d’approbation locales.

## <a name="version-9209029-june-8"></a>Version 92.0.902.9 : 8 juin

Résolution de divers bogues et problèmes de performances.

## <a name="version-91086441-june-3"></a>Version 91.0.864.41 : 3 juin

Résolution de divers bogues et problèmes de performances.

## <a name="version-91086437-may-27"></a>Version 91.0.864.37 : 27 mai

Résolution de divers bogues et problèmes de performances.

## <a name="version-91086436-may-26"></a>Version 91.0.864.36 : 26 mai

Résolution de divers bogues et problèmes de performances.

## <a name="version-91086433-may-21"></a>Version 91.0.864.33 : 21 mai

Résolution de divers bogues et problèmes de performances.

## <a name="version-91086427-may-14"></a>Version 91.0.864.27 : 14 mai

Résolution de divers bogues et problèmes de performances.

## <a name="version-91086419-may-7"></a>Version 91.0.864.19 : 7 mai

Résolution de divers bogues et problèmes de performances.

## <a name="version-91086415-may-3"></a>Version 91.0.864.15 : 3 mai

Résolution de divers bogues et problèmes de performances.

## <a name="version-91086411-april-30"></a>Version 91.0.864.11 : 30 avril

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- **Identifiez le trafic réseau provenant des conteneurs Microsoft Defender Application Guard au niveau du proxy.** À partir Microsoft Edge version 91, la prise en charge intégrée permet de baliser le trafic réseau provenant de conteneurs Application Guard, ce qui permet aux entreprises de les identifier et d’appliquer des stratégies spécifiques.

- **Option de prise en charge permettant de synchroniser les Favoris de l’hôte vers le conteneur Edge Application Guard.** À partir Microsoft Edge version 91, les utilisateurs ont la possibilité de configurer Application Guard pour synchroniser leurs favoris entre l’hôte et le conteneur. Cela garantit que les nouveaux favoris apparaissent également sur le conteneur.

- **Prise en charge des API de reconnaissance vocale**. À partir Microsoft Edge version 91, la prise en charge de l’API pour les commandes de reconnaissance vocale sur Google.com et sites similaires est ajoutée. Cette fonctionnalité est limitée à un groupe d’utilisateurs sélectionnés de manière aléatoire et ayant activé l’expérimentation. Ces utilisateurs fournissent des commentaires à l’équipe chargée de la fonctionnalité.

- **Personnalisez votre navigateur avec de nouvelles couleurs de thème.** Faites Microsoft Edge vous-même avec l’une des dix-neuf nouvelles couleurs de thème sur la page Paramètres -> Apparence. Vous pouvez également installer des thèmes personnalisés à partir du site des composants additionnels Microsoft Edge. [En savoir plus](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

- **Interrompre les téléchargements** À partir de Microsoft Edge version 91, le navigateur interrompt automatiquement les téléchargements de types qui pourraient endommager votre ordinateur si ces téléchargements sont démarrés sans intervention de l’utilisateur et ne sont pas pris en charge par la vérification de réputation de l’application SmartScreen. Les utilisateurs peuvent remplacer et continuer à télécharger en cliquant avec le bouton droit et en choisissant « Conserver » sur l’élément de téléchargement.
Enterprise administrateurs peuvent refuser ce comportement, l’une des deux stratégies ci-après :
    - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) : désactiver les avertissements basés sur l’extension de type de fichier de téléchargement pour les types de fichiers spécifiés sur les domaines. Pour plus d’informations, voir [Interruptions de téléchargements de sécurité Microsoft Edge](/deployedge/microsoft-edge-security-downloads-interruptions)

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

Six nouvelles stratégies ont été ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://www.microsoft.com/edge/business/download). Les nouvelles stratégies suivantes ont été ajoutées :

- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) : Identification du trafic Application Guard
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) : ports réseau explicitement autorisés
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) : autoriser l’importation des paramètres de page de démarrage
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) : permet aux utilisateurs de capturer un problème mathématique et d’obtenir la solution avec une explication pas à pas dans Microsoft Edge
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) : autoriser le contenu Microsoft News sur la page Nouvel onglet
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) : autoriser les liens rapides sur la page Nouvel onglet

#### <a name="obsoleted-policy"></a>Stratégie obsolète

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) : activer l’authentification proactive
<!-- end major 91 -->

## <a name="version-90081846-april-22"></a>Version 90.0.818.46 : 22 avril

Résolution de divers bogues et problèmes de performances.

## <a name="version-90081842-april-20"></a>Version 90.0.818.42 : 20 avril

Résolution de divers bogues et problèmes de performances.

## <a name="version-90081841-april-16"></a>Version 90.0.818.41 : 16 avril

Résolution de divers bogues et problèmes de performances.

## <a name="version-90081838-april-14"></a>Version 90.0.818.38 : 14 avril

Résolution de divers bogues et problèmes de performances.

## <a name="version-90081836-april-12"></a>Version 90.0.818.36 : 12 avril

Résolution de divers bogues et problèmes de performances.

## <a name="version-90081827-april-2"></a>Version 90.0.818.27 : 2 avril

Résolution de divers bogues et problèmes de performances.

## <a name="version-90081822-march-29"></a>Version 90.0.818.22 : 29 mars

Résolution de divers bogues et problèmes de performances.

## <a name="version-90081814-march-22"></a>Version 90.0.818.14 : 22 mars

Résolution de divers bogues et problèmes de performances.
<!-- begin major 90 -->
## <a name="version-9008188-march-16"></a>Version 90.0.818.8 : 16 mars

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- **L'authentification unique (SSO) est désormais disponible pour les comptes Azure Active Directory (Azure AD) et le compte Microsoft (MSA) sur macOS**. Un utilisateur connecté sur Microsoft Edge sur macOS se connecte désormais automatiquement aux sites web qui sont configurés pour autoriser l'authentification unique avec les comptes Professionnels et Microsoft (par exemple, bing.com, office.com, msn.com et outlook.com).

- **Mode plein écran.** À partir Microsoft Edge version 90, nous avons verrouillé les paramètres d’impression de l’interface utilisateur pour autoriser uniquement les imprimantes configurées et les options « Imprimer au format PDF ». Nous avons également effectué des améliorations dans le mode plein écran de l’application unique à accès affecté pour limiter le lancement d’autres applications à partir du navigateur. Pour plus d’informations sur les fonctionnalités du mode plein écran, cliquez [ici.](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features)

- **Impression :**

  - **Nouveau mode de rastérisation d’impression pour les imprimantes non-PostScript**. À partir de Microsoft Edge version 90, les administrateurs peuvent utiliser une nouvelle stratégie pour définir le mode de rastérisation d’impression pour leurs utilisateurs. Cette stratégie contrôle la façon dont Microsoft Edge imprime vers des imprimantes non-PostScript sur Windows.  L’ impression sur des imprimantes non-PostScript doit parfois être rastérisée pour imprimer correctement. Les options d’impression sont Complète et Rapide.

  - **Options de mise à l’échelle de page supplémentaires pour l’impression**. Les utilisateurs peuvent désormais personnaliser la mise à l’échelle lors de l’impression de pages web et de documents PDF à l’aide d’options supplémentaires. L’option Ajuster à la page permet de s’assurer que la page web ou le document est adapté à l’espace disponible dans le « Format de papier » sélectionné pour l’impression. L’option « Taille réelle » garantit qu’aucune modification n’a été apportée à la taille du contenu en cours d’impression, quelle que soit la « Taille du papier » sélectionnée.

- **Productivité :**

  - **Les suggestions de remplissage automatique sont étendues pour inclure le contenu des champs d’adresse à partir du Presse-papiers**. Le contenu du Presse-papiers est interrogé lorsque vous cliquez sur un champ de profil/adresse (par exemple, téléphone, e-mail, code postal, ville, état, etc.) pour afficher des suggestions de remplissage automatique.

  - **Les utilisateurs peuvent rechercher des suggestions de remplissage automatique même si un formulaire ou un champ n’est pas détecté**. Aujourd’hui, si vos informations sont enregistrées sur Microsoft Edge, les suggestions de remplissage automatique s’affichent automatiquement et vous permettent de gagner du temps lors du remplissage des formulaires. Dans les cas où le remplissage automatique manque un formulaire, ou si vous souhaitez récupérer des données dans des formulaires qui n’ont généralement pas de remplissage automatique (comme les formulaires temporaires), vous pouvez rechercher vos informations à l’aide du remplissage automatique.

- **Accédez aux téléchargements à partir d’un menu volant dans la barre de menus**. Les téléchargements s’affichent dans le coin supérieur droit avec tous les téléchargements actifs au même endroit. Ce menu est facile à ignorer, de sorte que les utilisateurs continuent à naviguer sans interruption et qu’ils peuvent surveiller la progression globale du téléchargement directement à partir de la barre d’outils. [Si vous souhaitez en savoir plus](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).


### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

Nous avons ajouté sept nouvelles stratégies. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://www.microsoft.com/edge/business/download). Les nouvelles stratégies suivantes ont été ajoutées :

- [ApplicationGuardFavoritesSyncEnabled](./microsoft-edge-policies.md#applicationguardfavoritessyncenabled) : synchronisation des Favoris d’Application Guard activée
- [ManagedConfigurationPerOrigin](./microsoft-edge-policies.md#managedconfigurationperorigin) : définit des valeurs de configuration gérées pour des sites web avec des origines spécifiques
- [PrintRasterizationMode](./microsoft-edge-policies.md#printrasterizationmode) : mode de rastérisation d’impression
- [QuickViewOfficeFilesEnabled](./microsoft-edge-policies.md#quickviewofficefilesenabled) : gérer la fonctionnalité de fichiers QuickView Office dans Microsoft Edge
- [SSLErrorOverrideAllowedForOrigins](./microsoft-edge-policies.md#sslerroroverrideallowedfororigins) : autoriser les utilisateurs à passer de la page d’avertissement HTTPS pour des origines spécifiques
- [WindowOcclusionEnabled](./microsoft-edge-policies.md#windowocclusionenabled) : activer l’occlusion de fenêtre
- [WindowsHelloForHTTPAuthEnabled](./microsoft-edge-policies.md#windowshelloforhttpauthenabled) : Windows Hello Pour l’authentification HTTP activé

#### <a name="deprecated-policies"></a>Stratégies déconseillées

- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) : activer l’occlusion de fenêtre native
- [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) : version TLS minimale activée
<!-- end major 90 -->

## <a name="version-89077454-march-13"></a>Version 89.0.774.54 : 13 mars

Résolution de divers bogues et problèmes de performances.

## <a name="version-89077450-march-10"></a>Version 89.0.774.50 : 10 mars

Correction de divers bogues et problèmes de performance.

## <a name="version-89077448-march-8"></a>Version 89.0.774.48 : 8 mars

Correction de divers bogues et problèmes de performance.

## <a name="version-89077445-march-3"></a>Version 89.0.774.45 : 3 mars.

Résolution de divers bogues et problèmes de performances.

## <a name="version-89077439-february-26"></a>Version 89.0.774.39 : 26 février

Résolution de divers bogues et problèmes de performances.

## <a name="version-89077434-february-22"></a>Version 89.0.774.34 : 22 février

Résolution de divers bogues et problèmes de performances.

## <a name="version-89077427-february-12"></a>Version 89.0.774.27 : 12 février

Résolution de divers bogues et de problèmes de performances.

## <a name="version-89077423-february-8"></a>Version 89.0.774.23 : 8 février

Résolution de divers bogues et problèmes de performances.

<!-- begin major 89 -->

<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
