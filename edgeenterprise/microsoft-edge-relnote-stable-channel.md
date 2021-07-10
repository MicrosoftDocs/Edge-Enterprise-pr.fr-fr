---
title: Notes de publication de Microsoft Edge pour le canal stable
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notes de publication de Microsoft Edge pour le canal stable
ms.openlocfilehash: ab599e3995641290ed806acc241b00e808f7fc1b
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642530"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Notes de publication du canal stable Microsoft Edge

Ces notes de publication fournissent des informations sur les nouvelles fonctionnalités et les mises à jour non liées à la sécurité qui sont incluses dans le canal stable Microsoft Edge.

- L'ensemble des mises à jour de sécurité est répertorié [ici](microsoft-edge-relnotes-security.md).
- Les notes de publication archivées pour le canal stable Microsoft Edge sont situées [ici](microsoft-edge-relnote-archive-stable-channel.md).

 Si vous souhaitez en savoir plus sur les canaux Microsoft Edge, veuillez consultez la rubrique [Vue d’ensemble des canaux Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Pour le canal stable, le déploiement des mises à jour sera progressif et durera un ou plusieurs jours. Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Déploiements progressifs pour les mises à jour de Microsoft Edge](microsoft-edge-update-progressive-rollout.md).
>
> La plateforme web Microsoft Edge évolue constamment pour améliorer l’expérience utilisateur, la sécurité et la confidentialité. Pour en savoir plus, consultez les [modifications qui ont un impact sur la compatibilité du prochain Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).


## <a name="version-91086464-july-2"></a>Version 91.0.864.64 : 2 juillet

Résolution de divers bogues et problèmes de performances.

## <a name="version-91086459-june-24"></a>Version 91.0.864.59 : 24 juin

Les mises à jour de sécurité du canal stable sont répertoriées [ici](/deployedge/microsoft-edge-relnotes-security#june-24-2021).

## <a name="version-91086454-june-18"></a>Version 91.0.864.54 : 18 juin

> [!Important]
> Cette mise à jour contient [CVE-2021-30554](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554) qui a été signalé par l’équipe Chromium comme ayant une faille dans la nature. Pour plus d'informations, voir le [Guide de mise à jour de la sécurité](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Les mises à jour de sécurité du canal stable sont répertoriées [ici](/deployedge/microsoft-edge-relnotes-security#june-18-2021).

## <a name="version-91086448-june-11"></a>Version 91.0.864.48 : 11 juin

> [!Important]
>Cette mise à jour contient [CVE-2021-30551](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551) qui a été signalé par l’équipe Chromium comme ayant une faille dans la nature. Pour plus d'informations, voir le [Guide de mise à jour de la sécurité](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Les mises à jour de sécurité du canal stable sont répertoriées [ici](/deployedge/microsoft-edge-relnotes-security#june-11-2021).

## <a name="version-91086441-june-3"></a>Version 91.0.864.41 : 3 juin

Les mises à jour de sécurité du canal stable sont répertoriées [ici](/deployedge/microsoft-edge-relnotes-security#june-3-2021).

## <a name="version-91086437-may-27"></a>Version 91.0.864.37 : 27 mai

Les mises à jour de sécurité du canal stable sont répertoriées [ici](/deployedge/microsoft-edge-relnotes-security#may-27-2021).

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- **Identifiez le trafic réseau provenant des conteneurs Microsoft Defender Application Guard au niveau du proxy.** À partir Microsoft Edge version 91, la prise en charge intégrée permet de baliser le trafic réseau provenant de conteneurs Application Guard, ce qui permet aux entreprises de les identifier et d’appliquer des stratégies spécifiques.

- **Option de prise en charge permettant de synchroniser les Favoris de l’hôte vers le conteneur Edge Application Guard.** À partir Microsoft Edge version 91, les utilisateurs ont la possibilité de configurer Application Guard pour synchroniser leurs favoris entre l’hôte et le conteneur. Cela garantit que les nouveaux favoris apparaissent également sur le conteneur.

- À partir de **Microsoft Edge version 91,** le navigateur interrompt automatiquement les téléchargements de types qui pourraient endommager votre ordinateur si ces téléchargements sont démarrés sans intervention de l’utilisateur et ne sont pas pris en charge par la vérification de Réputation d’application SmartScreen. Les utilisateurs peuvent remplacer et continuer à télécharger en cliquant avec le bouton droit et en choisissant « Conserver » sur l’élément de téléchargement. Enterprise administrateurs peuvent refuser ce comportement en configurant la stratégie suivante :
  - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md) : désactiver les avertissements basés sur l’extension de type de fichier de téléchargement pour les types de fichiers spécifiés sur les domaines

    Pour plus d’informations, voir [Interruptions des téléchargement de sécurité Microsoft Edge](microsoft-edge-security-downloads-interruptions.md).

- **Prise en charge des API de reconnaissance vocale**. À partir Microsoft Edge version 91, la prise en charge de l’API pour les commandes de reconnaissance vocale sur Google.com et sites similaires est ajoutée. Cette fonctionnalité est limitée à un groupe d’utilisateurs sélectionnés de manière aléatoire et ayant activé l’expérimentation. Ces utilisateurs fournissent des commentaires à l’équipe chargée de la fonctionnalité.

- **Personnalisez votre navigateur avec de nouvelles couleurs de thème.** Faites Microsoft Edge vous-même avec l’une des dix-neuf nouvelles couleurs de thème sur la page Paramètres -> Apparence. Vous pouvez également installer des thèmes personnalisés à partir du site des composants additionnels Microsoft Edge. [En savoir plus](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

### <a name="policy-updates"></a>Mises à jour de stratégie

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

## <a name="version-90081866-may-20"></a>Version 90.0.818.66 : 20 mai

Résolution de divers bogues et problèmes de performances.

## <a name="version-90081862-may-13"></a>Version 90.0.818.62 : 13 mai

Les mises à jour de sécurité du canal stable sont répertoriées [ici](/deployedge/microsoft-edge-relnotes-security#may-13-2021).

## <a name="version-90081856-may-6"></a>Version 90.0.818.56 : 6 mai

Résolution de divers bogues et problèmes de performances.

## <a name="version-90081851-april-29"></a>Version 90.0.818.51 : 29 avril

Les mises à jour de sécurité du canal stable sont répertoriées [ici](/deployedge/microsoft-edge-relnotes-security#april-29-2021).

## <a name="version-90081849-april-26"></a>Version 90.0.818.49 : 26 avril

Résolution de divers bogues et problèmes de performances.

## <a name="version-90081846-april-22"></a>Version 90.0.818.46 : 22 avril ##

Les mises à jour de sécurité du canal stable sont répertoriées [ici](/deployedge/microsoft-edge-relnotes-security#april-22-2021).

## <a name="version-90081842-april-19"></a>Version 90.0.818.42 : 19 avril

Résolution de divers bogues et problèmes de performances.

## <a name="version-90081841-april-16"></a>Version 90.0.818.41 : 16 avril ##

> [!Important]
>Cette mise à jour contient [CVE-2021-21224](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21224) qui a été signalé par l’équipe Chromium comme ayant une faille dans la nature. Pour plus d'informations, voir le [Guide de mise à jour de la sécurité](https://msrc.microsoft.com/update-guide).

Les mises à jour de sécurité du canal stable sont répertoriées [ici](/deployedge/microsoft-edge-relnotes-security#april-16-2021).

## <a name="version-90081839-april-15"></a>Version 90.0.818.39 : 15 avril ##

Les mises à jour de sécurité du canal stable sont répertoriées [ici](/deployedge/microsoft-edge-relnotes-security#april-15-2021).

## <a name="feature-updates"></a>Mises à jour des fonctionnalités ##

-    **L'authentification unique (SSO) est désormais disponible pour les comptes Azure Active Directory (Azure AD) et le compte Microsoft (MSA) sur macOS.** Un utilisateur connecté sur Microsoft Edge sur macOS se connecte désormais automatiquement aux sites web qui sont configurés pour autoriser l'authentification unique avec les comptes Professionnels et Microsoft (par exemple, bing.com, office.com, msn.com et outlook.com).

- **Mode plein écran.** À partir Microsoft Edge version 90, nous avons verrouillé les paramètres d’impression de l’interface utilisateur pour autoriser uniquement les imprimantes configurées et les options « Imprimer au format PDF ». Nous avons également effectué des améliorations dans le mode plein écran de l’application unique à accès affecté pour limiter le lancement d’autres applications à partir du navigateur. Pour plus d’informations sur les fonctionnalités du mode plein écran, cliquez [ici.](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features)

- **Interrompre les téléchargements** À partir de Microsoft Edge version 91, le navigateur interrompt automatiquement les téléchargements de types qui pourraient endommager votre ordinateur si ces téléchargements sont démarrés sans intervention de l’utilisateur et ne sont pas pris en charge par la vérification de réputation de l’application SmartScreen. Les utilisateurs peuvent remplacer et continuer à télécharger en cliquant avec le bouton droit et en choisissant « Conserver » sur l’élément de téléchargement.
Enterprise administrateurs peuvent refuser ce comportement, l’une des deux stratégies ci-après :
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) : désactiver les avertissements basés sur l’extension de type de fichier de téléchargement pour les types de fichiers spécifiés sur les domaines Pour plus d’informations, voir [Interruptions de téléchargements de sécurité Microsoft Edge](/deployedge/microsoft-edge-security-downloads-interruptions)

- **Impression** :

    - **Nouveau mode de rastérisation d’impression pour les imprimantes non PostScript.** À partir de Microsoft Edge version 90, les administrateurs peuvent utiliser une nouvelle stratégie pour définir le mode de rastérisation d’impression pour leurs utilisateurs. Cette stratégie contrôle la façon dont Microsoft Edge imprime sur des imprimantes non PostScript sur Windows. L’ impression sur des imprimantes non-PostScript doit parfois être rastérisée pour imprimer correctement. Les options d’impression sont Complète et Rapide.
    
  - **Options de mise à l’échelle de page supplémentaires pour l’impression.** Les utilisateurs peuvent désormais personnaliser la mise à l’échelle lors de l’impression de pages web et de documents PDF à l’aide d’options supplémentaires. L’option Ajuster à la page permet de s’assurer que la page web ou le document est adapté à l’espace disponible dans le « Format de papier » sélectionné pour l’impression. L’option « Taille réelle » garantit qu’aucune modification n’a été apportée à la taille du contenu en cours d’impression, quelle que soit la « Taille du papier » sélectionnée.

-   **Productivité :**

    -   **Les suggestions de remplissage automatique sont étendues pour inclure le contenu des champs d’adresse à partir du Presse-papiers.** Le contenu du Presse-papiers est interrogé lorsque vous cliquez sur un champ de profil/adresse (par exemple, téléphone, e-mail, code postal, ville, état, etc.) pour afficher des suggestions de remplissage automatique.

    -   **Les utilisateurs peuvent rechercher des suggestions de remplissage automatique même si un formulaire ou un champ n’est pas détecté.** Aujourd’hui, si vos informations sont enregistrées sur Microsoft Edge, les suggestions de remplissage automatique s’affichent automatiquement et vous permettent de gagner du temps lors du remplissage des formulaires. Dans les cas où le remplissage automatique manque un formulaire, ou si vous souhaitez récupérer des données dans des formulaires qui n’ont généralement pas de remplissage automatique (comme les formulaires temporaires), vous pouvez rechercher vos informations à l’utilisation du remplissage automatique.

-   **Accédez aux téléchargements à partir d’un menu volant dans la barre de menus.** Les téléchargements s’affichent dans le coin supérieur droit avec tous les téléchargements actifs au même endroit. Ce menu est facile à ignorer, de sorte que les utilisateurs continuent à naviguer sans interruption et qu’ils peuvent surveiller la progression globale du téléchargement directement à partir de la barre d’outils. [Si vous souhaitez en savoir plus](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

-   **Améliorations apportées au rendu des polices.** À partir de la version 90 de Microsoft Edge, nous avons apporté des améliorations au rendu du texte afin d’améliorer la clarté et de réduire le flou. Une partie des améliorations apportées au rendu des polices sera apportée à la version 90 bêta, mais elle sera désactivée par défaut.

- **Mode Enfant.** Nous avons mis à jour la stratégie afin que, lorsque la stratégie est activée, elle désactive la fonctionnalité Mode Enfant en plus de la sécurité de la famille. En savoir plus sur le mode [Enfant ici](https://go.microsoft.com/fwlink/?linkid=2146910)

## <a name="policy-updates"></a>Mises à jour de stratégies

## <a name="new-policies"></a>Nouvelles stratégies

Huit nouvelles stratégies ont été ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://www.microsoft.com/edge/business/download). Les nouvelles stratégies suivantes ont été ajoutées :
-   [ApplicationGuardFavoritesSyncEnabled](/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled) : synchronisation des Favoris d’Application Guard activée
- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) Identification du trafic Application Guard
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) Ports réseau explicitement autorisés
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) Autoriser l’importation des paramètres de page de démarrage
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) Laissez les utilisateurs capturer un problème mathématique et obtenir la solution avec une explication pas à pas dans Microsoft Edge
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) Autoriser le contenu Microsoft News sur la page Nouvel onglet
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) Autoriser les liens rapides sur la page Nouvel onglet
-   [FetchKeepaliveDurationSecondsOnShutdown](/DeployEdge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown) : Durée de mise à jour continue à l’arrêt
-   [ManagedConfigurationPerOrigin](/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin) : définit des valeurs de configuration gérées pour des sites web avec des origines spécifiques
-   [PrintRasterizationMode](/DeployEdge/microsoft-edge-policies#printrasterizationmode) : mode de rastérisation d’impression
-   [QuickViewOfficeFilesEnabled](/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) : gérer la fonctionnalité de fichiers QuickView Office dans Microsoft Edge
-   [SSLErrorOverrideAllowedForOrigins](/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) : autoriser les utilisateurs à passer de la page d’avertissement HTTPS pour des origines spécifiques
-   [WindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#windowocclusionenabled) : activer l’occlusion de fenêtre
-   [WindowsHelloForHTTPAuthEnabled](/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) : Windows Hello Pour l’authentification HTTP activé

## <a name="deprecated-policies"></a>Stratégies déconseillées

- [ProactiveAuthEnabled](/DeployEdge/microsoft-edge-policies#proactiveauthenabled) Activer l’authentification proactive
-   [NativeWindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) : activer l’occlusion de fenêtre native
-   [SSLVersionMin](/DeployEdge/microsoft-edge-policies#sslversionmin) : version TLS minimale activée

## <a name="version-89077477-april-14"></a>Version 89.0.774.77 : 14 avril

> [!Important]
>Cette mise à jour contient [CVE-2021-21206](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21206) et [CVE-2021-21220](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21220) qui ont été signalés par l’équipe Chromium comme ayant une faille dans la nature.  Pour plus d'informations, voir le [Guide de mise à jour de la sécurité](https://msrc.microsoft.com/update-guide).

Les mises à jour de sécurité du canal stable sont répertoriées [ici](/deployedge/microsoft-edge-relnotes-security#april-14-2021).

## <a name="version-89077476-april-12"></a>Version 89.0.774.76 : 12 avril

Résolution de divers bogues et problèmes de performances.

## <a name="version-89077475-april-8"></a>Version 89.0.774.75 : 8 avril

Résolution de divers bogues et problèmes de performances.

## <a name="version-89077468-april-1"></a>Version 89.0.774.68 : 1er avril

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](./microsoft-edge-relnotes-security.md#april-1-2021)

## <a name="version-89077463-march-25"></a>Version 89.0.774.63 : 25 mars

Résolution de divers bogues et problèmes de performances.

## <a name="version-89077457-march-18"></a>Version 89.0.774.57 : 18 mars

Résolution de divers bogues et problèmes de performances.

## <a name="version-89077454-march-13"></a>Version 89.0.774.54 : 13 mars

> [!IMPORTANT]
> Cette mise à jour contient le [CVE-2021-21193 ](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21193) qui a été signalé par l'équipe Chromium comme ayant fait l'objet d'un exploit dans la nature. Pour plus d'informations, [voir le Guide de mise à jour de la sécurité](https://msrc.microsoft.com/update-guide).

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](./microsoft-edge-relnotes-security.md#march-13-2021)

## <a name="version-89077450-march-10"></a>Version 89.0.774.50 : 10 mars

Correction de divers bogues et problèmes de performance.

## <a name="version-89077448-march-8"></a>Version 89.0.774.48 : 8 mars

Résolution de divers bogues et problèmes de performances.

<!-- begin major 89 -->
## <a name="version-89077445-march-4"></a>Version 89.0.774.45 : 4 mars

> [!IMPORTANT]
> Cette mise à jour contient [CVE-2021-21166](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166) qui a été signalé par l’équipe Chromium comme ayant une faille de sécurité. Pour plus d’informations, consultez le [Guide de mise à jour de sécurité](https://msrc.microsoft.com/update-guide).

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](./microsoft-edge-relnotes-security.md#march-4-2021)

### <a name="resolved-issues"></a>Problèmes résolus

- **Mises à jour et correctifs des raccourcis de la Barre des tâches et du menu Démarrer :**
  - Un clic avec le bouton droit sur le raccourci Microsoft Edge dans le menu Démarrer affiche désormais correctement l’option d’épinglage de Microsoft Edge de la barre des tâches lorsqu’il est épinglé.
  - Les dispositions de l’écran de démarrage qui incluent une [configuration de la barre des tâches](/windows/configuration/configure-windows-10-taskbar) pour épingler Microsoft Edge à la barre des tâches n’entraînent plus l’épinglage d’un deuxième raccourci Microsoft Edge à la barre des tâches.
  - Les organisations qui utilisent des profils d’itinérance Windows ne voient plus une icône blanche vide à la place de l’icône Microsoft Edge dans la barre des tâches lorsque leurs utilisateurs se connectent à Windows.

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- **Le mode plein écran active des fonctionnalités de verrouillage supplémentaires.** À partir de la version 89 de Microsoft Edge, nous avons ajouté des fonctionnalités de verrouillage supplémentaires en mode plein écran pour permettre aux clients d’accomplir leur travail dans une expérience productive et plus sécurisée. [Si vous souhaitez en savoir plus](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **L’outil Enterprise Mode Site List Manager sera disponible dans le navigateur via la page *edge://compat* **. Vous pouvez utiliser cet outil pour créer, modifier et exporter votre liste de sites XML pour le mode Internet Explorer sur Microsoft Edge. Vous pouvez activer l’accès à cet outil selon vos besoins par le biais de la stratégie de groupe. [Si vous souhaitez en savoir plus](./edge-ie-mode-site-list-manager.md).

- **Améliorer les performances du navigateur avec des onglets en veille**. Les onglets en veille améliorent les performances du navigateur en mettant les onglets inactifs en veille pour libérer des ressources système, telles que la mémoire et le processeur de sorte que les onglets actifs ou d’autres applications puissent les utiliser. Les utilisateurs peuvent empêcher la mise en veille de sites et configurer le délai avant qu’un onglet inactif ne soit mis en veille. Pour maintenir les utilisateurs dans leur flux, il existe également des [heuristiques](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) pour empêcher certains sites de passer en veille, tels que les sites intranet. Cette fonctionnalité peut être gérée avec des stratégies de groupe.

- **Réinitialisez manuellement vos données de synchronisation Microsoft Edge dans le cloud**. Nous introduisons un moyen de réinitialiser vos données de synchronisation Microsoft Edge à partir du produit. Cela garantit que vos données sont effacées des services Microsoft, ainsi que la résolution de certains problèmes de produit qui nécessitaient auparavant un ticket de support.

- **Activation intelligente de l'authentification unique (SSO) pour tous les comptes Active Directory (Azure AD) Windows Azure pour les utilisateurs avec un seul profil Microsoft Edge non Azure AD**.  Activez automatiquement ce paramètre pour les utilisateurs qui peuvent tirer le meilleur parti de cette fonctionnalité. Si un utilisateur n’a qu’un seul profil Microsoft Edge (et qu’il ne s’agit pas d’Azure AD ou du mode Enfants), le paramètre est automatiquement allumé au lancement de Microsoft Edge. Ce basculement automatique est également automatiquement éteint si un utilisateur choisit ultérieurement de se connecter à un autre profil Microsoft Edge avec un compte Azure AD. Les utilisateurs peuvent mettre à jour manuellement leurs préférences pour cette fonctionnalité dans **Paramètres > Profils >Préférences de profil > Autoriser l'authentification unique pour les sites professionnels ou scolaires à l’aide de ce profil**.

- **Améliorations apportées à l’expérience de sélection de texte dans les documents PDF**. Les utilisateurs commenceront à obtenir une expérience de sélection de texte plus fluide et plus cohérente dans les documents PDF ouverts dans Microsoft Edge à partir de la version 89.

- **Date de naissance désormais prise en charge dans le remplissage automatique**. Aujourd’hui, Microsoft Edge vous permet de gagner du temps et des efforts lors du remplissage de formulaires et de la création de comptes en ligne en remplissant automatiquement vos données telles que les adresses, les noms, les numéros de téléphone, etc. À partir de la version 89 de Microsoft Edge, nous ajoutons la prise en charge d’un autre champ que vous pouvez avoir enregistré et rempli automatiquement : la date de naissance. Vous pouvez afficher, modifier et supprimer ces informations à tout moment dans vos paramètres de profil.

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

Nous avons ajouté sept nouvelles stratégies. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://www.microsoft.com/edge/business/download). Les nouvelles stratégies suivantes ont été ajoutées.

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) : paramètres de durée de vie des données de navigation
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) - Gestion des applications mobiles activée
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) : définir une liste ordonnée des langues préférées que les sites web doivent afficher si le site prend en charge la langue
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) : autoriser les recommandations et les notifications promotionnelles à partir d’Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) : restreindre le mode d’impression des graphiques d’arrière-plan
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault) : mode d’impression des graphiques d’arrière-plan par défaut
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist) : bloquer les actions intelligentes pour une liste de services

#### <a name="obsoleted-policies"></a>Stratégies obsolètes

Les stratégies suivantes sont obsolètes.

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) : utiliser une stratégie de référence par défaut de no-referrer-when-downgrade
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) : activer les rapports de données d’utilisation et d’incident
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) : envoyer des informations sur le site pour améliorer les services Microsoft
<!-- end major 89 -->

<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
