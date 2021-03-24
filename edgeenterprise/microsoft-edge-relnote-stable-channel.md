---
title: Notes de publication de Microsoft Edge pour le canal stable
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 03/18/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Notes de publication de Microsoft Edge pour le canal stable
ms.openlocfilehash: a0f33300d39f5ecaf48de114697c593a391dc052
ms.sourcegitcommit: 6a3787dead062e4a0860adbc570229974dcaee07
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "11442384"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Notes de publication du canal stable Microsoft Edge

Ces notes de publication fournissent des informations sur les nouvelles fonctionnalités et les mises à jour non liées à la sécurité qui sont incluses dans le canal stable Microsoft Edge.

- L'ensemble des mises à jour de sécurité est répertorié [ici](microsoft-edge-relnotes-security.md).
- Les notes de publication archivées pour le canal stable Microsoft Edge sont situées [ici](microsoft-edge-relnote-archive-stable-channel.md).

 Si vous souhaitez en savoir plus sur les canaux MicrosoftEdge, veuillez consultez la rubrique [Vue d’ensemble des canaux Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Pour le canal stable, le déploiement des mises à jour sera progressif et durera un ou plusieurs jours. Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Déploiements progressifs pour les mises à jour de MicrosoftEdge](microsoft-edge-update-progressive-rollout.md).

## <a name="version-89077457-march-18"></a>Version 89.0.774.57: 18mars

Résolution de divers bogues et problèmes de performances.

## <a name="version-89077454-march-13"></a>Version 89.0.774.54: 13mars

> [!IMPORTANT]
> Cette mise à jour contient le [CVE-2021-21193 ](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21193) qui a été signalé par l'équipe Chromium comme ayant fait l'objet d'un exploit dans la nature. Pour plus d'informations, [voir le Guide de mise à jour de la sécurité](https://msrc.microsoft.com/update-guide).

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-13-2021)

## <a name="version-89077450-march-10"></a>Version 89.0.774.50: 10 mars

Correction de divers bogues et problèmes de performance.

## <a name="version-89077448-march-8"></a>Version 89.0.774.48 : 8 mars

Résolution de divers bogues et problèmes de performances.

<!-- begin major 89 -->
## <a name="version-89077445-march-4"></a>Version89.0.774.45: 4mars

> [!IMPORTANT]
> Cette mise à jour contient [CVE-2021-21166](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166) qui a été signalé par l’équipe Chromium comme ayant une faille de sécurité. Pour plus d’informations, consultez le [Guide de mise à jour de sécurité](https://msrc.microsoft.com/update-guide).

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-4-2021)

### <a name="resolved-issues"></a>Problèmes résolus

- **Mises à jour et correctifs des raccourcis de la Barre des tâches et du menu Démarrer:**
  - Un clic avec le bouton droit sur le raccourci Microsoft Edge dans le menu Démarrer affiche désormais correctement l’option d’épinglage de MicrosoftEdge de la barre des tâches lorsqu’il est épinglé.
  - Les dispositions de l’écran de démarrage qui incluent une [configuration de la barre des tâches](https://docs.microsoft.com/windows/configuration/configure-windows-10-taskbar) pour épingler Microsoft Edge à la barre des tâches n’entraînent plus l’épinglage d’un deuxième raccourci Microsoft Edge à la barre des tâches.
  - Les organisations qui utilisent des profils d’itinérance Windows ne voient plus une icône blanche vide à la place de l’icône MicrosoftEdge dans la barre des tâches lorsque leurs utilisateurs se connectent à Windows.

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- **Le mode plein écran active des fonctionnalités de verrouillage supplémentaires.** À partir de la version89 de MicrosoftEdge, nous avons ajouté des fonctionnalités de verrouillage supplémentaires en mode plein écran pour permettre aux clients d’accomplir leur travail dans une expérience productive et plus sécurisée. [Si vous souhaitez en savoir plus](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **L’outil Enterprise Mode Site List Manager sera disponible dans le navigateur via la page *edge://compat* **. Vous pouvez utiliser cet outil pour créer, modifier et exporter votre liste de sites XML pour le mode Internet Explorer sur MicrosoftEdge. Vous pouvez activer l’accès à cet outil selon vos besoins par le biais de la stratégie de groupe. [Si vous souhaitez en savoir plus](https://docs.microsoft.com/deployedge/edge-ie-mode-site-list-manager).

- **Améliorer les performances du navigateur avec des onglets en veille**. Les onglets en veille améliorent les performances du navigateur en mettant les onglets inactifs en veille pour libérer des ressources système, telles que la mémoire et le processeur de sorte que les onglets actifs ou d’autres applications puissent les utiliser. Les utilisateurs peuvent empêcher la mise en veille de sites et configurer le délai avant qu’un onglet inactif ne soit mis en veille. Pour maintenir les utilisateurs dans leur flux, il existe également des [heuristiques](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) pour empêcher certains sites de passer en veille, tels que les sites intranet. Cette fonctionnalité peut être gérée avec des stratégies de groupe.

- **Réinitialisez manuellement vos données de synchronisation MicrosoftEdge dans le cloud**. Nous introduisons un moyen de réinitialiser vos données de synchronisation MicrosoftEdge à partir du produit. Cela garantit que vos données sont effacées des services Microsoft, ainsi que la résolution de certains problèmes de produit qui nécessitaient auparavant un ticket de support.

- **Activation intelligente de l'authentification unique (SSO) pour tous les comptes Active Directory (Azure AD) Windows Azure pour les utilisateurs avec un seul profil Microsoft Edge non Azure AD**.  Activez automatiquement ce paramètre pour les utilisateurs qui peuvent tirer le meilleur parti de cette fonctionnalité. Si un utilisateur n’a qu’un seul profil Microsoft Edge (et qu’il ne s’agit pas d’Azure AD ou du mode Enfants), le paramètre est automatiquement allumé au lancement de Microsoft Edge. Ce basculement automatique est également automatiquement éteint si un utilisateur choisit ultérieurement de se connecter à un autre profil Microsoft Edge avec un compte Azure AD. Les utilisateurs peuvent mettre à jour manuellement leurs préférences pour cette fonctionnalité dans **Paramètres > Profils >Préférences de profil > Autoriser l'authentification unique pour les sites professionnels ou scolaires à l’aide de ce profil**.

- **Améliorations apportées à l’expérience de sélection de texte dans les documents PDF**. Les utilisateurs commenceront à obtenir une expérience de sélection de texte plus fluide et plus cohérente dans les documents PDF ouverts dans MicrosoftEdge à partir de la version89.

- **Date de naissance désormais prise en charge dans le remplissage automatique**. Aujourd’hui, MicrosoftEdge vous permet de gagner du temps et des efforts lors du remplissage de formulaires et de la création de comptes en ligne en remplissant automatiquement vos données telles que les adresses, les noms, les numéros de téléphone, etc. À partir de la version89 de MicrosoftEdge, nous ajoutons la prise en charge d’un autre champ que vous pouvez avoir enregistré et rempli automatiquement: la date de naissance. Vous pouvez afficher, modifier et supprimer ces informations à tout moment dans vos paramètres de profil.

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

Nous avons ajouté sept nouvelles stratégies. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil Microsoft Edge Entreprise](https://www.microsoft.com/edge/business/download). Les nouvelles stratégies suivantes ont été ajoutées.

- [BrowsingDataLifetime](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsingdatalifetime): paramètres de durée de vie des données de navigation
- [MAMEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#mamenabled) - Gestion des applications mobiles activée
- [DefinePreferredLanguages](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#definepreferredlanguages): définir une liste ordonnée des langues préférées que les sites web doivent afficher si le site prend en charge la langue
- [ShowRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showrecommendationsenabled): autoriser les recommandations et les notifications promotionnelles à partir d’Edge
- [PrintingAllowedBackgroundGraphicsModes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingallowedbackgroundgraphicsmodes): restreindre le mode d’impression des graphiques d’arrière-plan
- [PrintingBackgroundGraphicsDefault](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingbackgroundgraphicsdefault): mode d’impression des graphiques d’arrière-plan par défaut
- [SmartActionsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartactionsblocklist): bloquer les actions intelligentes pour une liste de services

#### <a name="obsoleted-policies"></a>Stratégies obsolètes

Les stratégies suivantes sont obsolètes.

- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy): utiliser une stratégie de référence par défaut de no-referrer-when-downgrade
- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled): activer les rapports de données d’utilisation et d’incident
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices): envoyer des informations sur le site pour améliorer les services Microsoft
<!-- end major 89 -->
## <a name="version-88070581-february-25"></a>Version88.0.705.81 du 25février

Résolution de divers bogues et de problèmes de performances.

## <a name="version-88070574-february-17"></a>Version88.0.705.74du 17février

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#February-17-2021)

## <a name="version-88070568-february-11"></a>Version88.0.705.68 du 11février

Résolution de divers bogues et de problèmes de performances.

## <a name="version-88070563-february-5"></a>Version88.0.705.63 du 5février

> [!IMPORTANT]
> Cette mise à jour contient [CVE-2021-21148](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21148), qui a été signalé par l’équipe Chromium comme cible de code malveillant exploitant une faille de sécurité.

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#February-5-2021)

## <a name="version-88070562-february-4"></a>Version88.0.705.62 du 4février

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#February-4-2021)

Résolution de divers bogues et de problèmes de performances.

## <a name="version-88070556-january-28"></a>Version 88.0.705.56: 28janvier

Résolution de divers bogues et problèmes de performances.

## <a name="version-88070553-january-26"></a>Version 88.0.705.53 : 26janvier

Résolution de divers bogues et problèmes de performances.

## <a name="version-88070550-january-21"></a>Version88.0.705.50 du 21janvier

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-21-2021)

<!--- begin major 88  --->
### <a name="feature-updates"></a>Mises à jour des fonctionnalités

- **Fonctionnalités obsolètes:**

  - Prise en charge du protocole FTP obsolète. La prise en charge du protocole FTP hérité a été supprimée de Microsoft Edge. Toute tentative d’accès à un lien FTP entraînera l’ouverture par le système d’exploitation d’une application externe pour gérer le lien FTP. Une autre solution pour les administrateurs informatiques consiste à configurer Microsoft Edge afin qu’il utilise le mode IE pour les sites qui dépendent du protocole FTP.
  - La prise en charge d’Adobe Flash sera supprimé. À partir de la version88 de Microsoft Edge Beta, la fonctionnalité et la prise en charge d’Adobe Flash seront supprimées. Pour en savoir plus: [Mise à jour concernant la fin de la prise en charge d’Adobe Flash Player – Blog Microsoft Edge (Windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentification:**

  - La signature unique (SSO) est désormais disponible pour les comptes Azure Active Directory (Azure AD) et le compte Microsoft (MSA) sur Windows de niveau inférieur. Un utilisateur se connectant à Microsoft Edge sur Microsoft Windows de niveau inférieur (7, 8.1) se connecte désormais automatiquement aux sites web configurés pour autoriser la connexion unique avec les comptes Professionnel et Microsoft (par exemple, bing.com, office.com, msn.com, outlook.com).<br>Remarque: il est possible que l’utilisateur doive se déconnecter et se reconnecter s’il se connecte à une version antérieure à la version88 de Microsoft Edge pour utiliser cette fonctionnalité.
  
  - L’authentification unique (SSO) vers des sites professionnels à l’aide des comptes Windows Azure Active Directory (Azure AD) sur le système dans des profils Microsoft Edge non Azure AD. Cette fonctionnalité peut être activée pour n’importe quel profil qui n’est pas connecté avec un compte scolaire/professionnel et qui n’est pas invité ou en mode privé et permet l’utilisation de n’importe quel compte scolaire/professionnel sur le système d’exploitation avec ce profil. Cette fonctionnalité peut être configurée dans **Paramètres** > **Profils** > **Préférences de profil** > **Autoriser l'authentification unique pour les sites professionnels ou scolaires à l’aide de ce profil**.
  
    > [!NOTE]
    > «L’authentification unique (SSO) pour tous les comptes Windows utilisant le profil Microsoft Edge» est une mise à jour des notes de publication du 21janvier.

- **Option du mode plein écran pour terminer la session**. Le bouton «Mettre fin à la session» est désormais disponible en mode plein écran dans l’expérience de navigation publique. Cette fonctionnalité permet de supprimer les données et paramètres du navigateur lorsque Microsoft Edge est fermé. Pour en savoir plus sur les fonctionnalités et la feuille de route du mode plein écran, voir [Configurer le mode plein écran Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).

- **Sécurité et confidentialité:**

  - Des alertes sont générées si le mot de passe d’un utilisateur est détecté dans une fuite en ligne. Les mots de passe des utilisateurs sont examinés par rapport à un référentiel d’informations d’identification connues qui ont été divulguées et envoient à l’utilisateur une alerte si une correspondance est trouvée. Pour garantir la sécurité et la confidentialité, les mots de passe des utilisateurs sont hachés et chiffrés lorsqu’ils sont vérifiés par rapport à la base de données des informations d’identification divulguées.
  - Mettre automatiquement à niveau le contenu mixte. Les pages sécurisées fournies via HTTPS peuvent contenir des images de référence fournies via HTTP non sécurisé. Pour améliorer la confidentialité et la sécurité dans Microsoft Edge88, ces images seront récupérées via HTTPS. Si l’image n’est pas disponible via HTTPS, elle n’est pas chargée.
  - Afficher les autorisations de site par site et par activité récente. À partir de Microsoft Edge88, les utilisateurs peuvent gérer plus facilement les autorisations de site. Ils peuvent afficher les autorisations par site web, et non plus seulement par type d’autorisation. Par ailleurs, nous avons ajouté une section activité récente qui permettra à l’utilisateur d’afficher les dernières modifications apportées à ses autorisations de site.
  - Amélioration des contrôles pour les cookies du navigateur. À partir de Microsoft Edge88, les utilisateurs peuvent supprimer des cookies tiers sans affecter les cookies de première partie. Les utilisateurs peuvent également filtrer leurs cookies selon s’il s’agit d’une première ou tierce partie et les trier en fonction du nom, du nombre de cookies, de la quantité de données stockées et de la dernière modification.

- **Mots de passe :**

  - Générateur de mot de passe. Microsoft Edge offre un générateur de mot de passe fort intégré que vous pouvez utiliser lors de l’inscription d’un nouveau compte ou lors de la modification d’un mot de passe existant. Recherchez simplement la liste déroulante de mot de passe suggéré par le navigateur dans le champ mot de passe et, lorsqu’il est sélectionné, il sera automatiquement enregistrer dans le navigateur et synchronisé sur tous les appareils pour une utilisation facile à l’avenir.
  - Moniteur de mot de passe. Lorsque l’un de vos mots de passe enregistrés dans le navigateur correspond à ceux répertoriés dans la liste des informations d’identification divulguées, Microsoft Edge vous avertit et vous invite à mettre à jour votre mot de passe. Le moniteur de mot de passe analyse les correspondances en votre nom et est activé par défaut.
  - Modifier le mot de passe. Vous pouvez désormais modifier vos mots de passe enregistrés directement dans les paramètres MicrosoftEdge. Chaque fois qu’un mot de passe a été mis à jour en dehors de MicrosoftEdge, il est facile de remplacer l’ancien mot de passe enregistré par le nouveau en modifiant l’entrée enregistrée dans les Paramètres. 

- **Améliorer la vitesse de démarrage de Microsoft Edge grâce à l'accélération du démarrage**. Pour améliorer la vitesse de démarrage de Microsoft Edge, nous avons conçu une fonctionnalité appelée Accélérateur de démarrage. L’Accélérateur de démarrage accélère le lancement en permettant à Microsoft Edge de s’exécuter en arrière-plan. Remarque: cette fonctionnalité est limitée à un groupe d’utilisateurs sélectionnés de manière aléatoire et ayant activé l’expérimentation. Ces utilisateurs donnent des commentaires à l’équipe chargée de la fonctionnalité.

- **Productivité:**

  - Améliorez votre productivité et le travail multitâche grâce aux onglets verticaux. À mesure que vous ajoutez des onglets horizontaux, les titres de site sont tronqués et les commandes des onglets perdent en visibilité. Cela interrompt le flux de travail de l’utilisateur, car il passe plus de temps à rechercher, à passer de l’un à l’autre et à gérer ses onglets, et moins de temps sur la tâche en cours. Les onglets verticaux permettent aux utilisateurs de déplacer leurs onglets vers le côté, là où les icônes alignées à la verticale et les titres de sites plus longs permettent de jeter un coup d’œil rapide pour identifier l’onglet que vous voulez ouvrir et basculer vers celui-ci.
  - Remplissage automatique du champ de date de naissance. Microsoft Edge vous permet d’économiser du temps et de l’énergie lors du remplissage des formulaires et de la création de comptes en ligne à l’aide de la saisie semi-automatique des données utilisateur, telles que les adresses, les noms, les numéros de téléphone, etc. Microsoft Edge prend désormais en charge le champ Date de naissance que les utilisateurs peuvent enregistrer et remplir automatiquement. Un utilisateur peut afficher, modifier et supprimer ces informations à tout moment dans ses paramètres de profil.
  - Améliorations apportées à l’historique Récemment fermés. L’historique Récemment fermés conserve désormais les 25derniers onglets et fenêtres de n’importe quelle session de navigation, et non plus seulement la session précédente. Les utilisateurs peuvent sélectionner Récemment fermés dans la nouvelle expérience d’Historique pour afficher tous les onglets qui ont été ouverts.
  - Fonction «votre journée en un clin d’œil» activée par défaut. À partir de la version88 de MicrosoftEdge, les travailleurs de l’information peuvent bénéficier de fonctionnalités de productivité intelligentes sur leur page Nouvel onglet (NTP). Les utilisateurs de MicrosoftEdge87 pourront également découvrir ces fonctionnalités dans les 2semaines après la publication de MicrosoftEdge88. Nous offrons aux utilisateurs qui sont connectés à l’aide de leur compte professionnel ou scolaire du contenu personnalisé et pertinent optimisé par leur M365Graph. Les utilisateurs peuvent rapidement parcourir leurs modules «votre journée en un clin d’œil» pour suivre facilement leurs réunions et leurs activités récentes, et lancer rapidement les applications qu’ils souhaitent utiliser.

- **Synchronisation de l'historique et des onglets ouverts**. La synchronisation de l'historique et des onglets ouverts est désormais disponible pour les utilisateurs. L’activation de ces fonctionnalités permet aux utilisateurs de reprendre là où ils en étaient en rendant leur historique de navigation et les onglets ouverts disponibles sur tous leurs appareils de synchronisation. Nous avons mis à jour les stratégies de synchronisation et d’historique des navigateurs, de sorte que les utilisateurs sont désormais connectés et productifs sur tous les appareils à l’aide de Microsoft Edge. [En savoir plus ](https://blogs.windows.com/windowsexperience/2021/01/21/this-year-lets-resolve-to-make-the-most-of-our-time-online-and-better-protect-ourselves-from-online-threats/).

- **PDF:**

  - Affichage d’un document PDF en mode livre (deux pages) À partir de la version88 de Microsoft Edge, les utilisateurs peuvent consulter des documents PDF en affichage à une ou deux pages (mode livre). Pour modifier l’affichage, cliquez sur le bouton **Mode Page** dans la barre d’outils.
  - Prise en charge des notes de texte ancré pour les fichiers PDF. À partir de la version87 de MicrosoftEdge, les utilisateurs peuvent ajouter des notes de texte tapées sur n’importe quelle portion de texte dans des fichiers PDF.

- **Polices:**

  - Les icônes du navigateur sont mises à jour dans le système Fluent Design. Dans le cadre de nos efforts continus en termes de Fluent Design dans le navigateur, nous avons apporté des modifications de façon à aligner davantage les icônes sur le nouveau système d’icônes Microsoft. Ces modifications peuvent avoir une incidence sur un grand nombre de nos interfaces utilisateur avec une interaction tactile importante, y compris les onglets, la barre d’adresses, ainsi que les icônes de navigation et de recherche d’itinéraire dans nos différents menus.
  - Amélioration du rendu des polices. Le rendu du texte est amélioré pour améliorer la clarté et réduire le flou.

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

Dix-huit nouvelles stratégies ont été ajoutées. Téléchargez les modèles d’administration mis à jour à partir de la [Page d’accueil MicrosoftEdgeEntreprise](https://www.microsoft.com/edge/business/download). Les nouvelles stratégies suivantes ont été ajoutées.

- [BasicAuthOverHttpEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#basicauthoverhttpenabled) : autoriser l’authentification de base pour HTTP.
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
- [TargetBlankImpliesNoOpener](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#targetblankimpliesnoopener) : ne définissez pas window.opener pour les liens ciblant _blank.
- [UpdatePolicyOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#updatepolicyoverride): indique comment Microsoft Edge Update gère les mises à jour disponibles à partir de MicrosoftEdge.
- [VerticalTabsAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#verticaltabsallowed): configure la disponibilité de la disposition verticale pour les onglets situés sur le côté du navigateur.
- [WebRtcAllowLegacyTLSProtocols](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtcallowlegacytlsprotocols): autorise le passage à une version antérieure héritée de TLS/DTLS dans WebRTC.
- [WebWidgetAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webwidgetallowed): active le widget Web.
- [WebWidgetIsEnabledOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webwidgetisenabledonstartup): autorise le widget web au démarrage de Windows.

#### <a name="deprecated-policies"></a>Stratégies déconseillées

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled): active l’authentification proactive.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist): configure les règles de contournement du proxy.
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode): configure les paramètres du serveur proxy.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl): définit l’URL du fichier proxy .pac.
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver): configure l’adresse ou l’URL du serveur proxy.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies): autorise WebDriver à remplacer les stratégies incompatibles.

### <a name="obsoleted-policies"></a>Stratégies obsolètes

- [AllowPopupsDuringPageUnload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowpopupsduringpageunload) : permet à une page d’afficher des fenêtres contextuelles pendant son déchargement.
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting): paramètre Adobe Flash par défaut.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls): autorise le plug-in Adobe Flash sur des sites spécifiques.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls): bloque le plug-in Adobe Flash sur des sites spécifiques.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode): étend le paramètre de contenu Adobe Flash à l’ensemble du contenu.
<!--- end major 88  --->
## <a name="version-87066475-january-7"></a>Version87.0.664.75du 7janvier

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-7-2021)

## <a name="version-87066466-december-17"></a>Version87.0.664.66du 17 décembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-87066460-december-10"></a>Version 87.0.664.60 : 10 décembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-87066457-december-7"></a>Version 87.0.664.57 : 7 décembre

Résolution de divers bogues et de problèmes de performances. Les mises à jour de sécurité du canal stable sont répertoriées [ici.](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#december-7-2020)

## <a name="version-87066455-december-3"></a>Version87.0.664.55du 3décembre

Résolution de divers bogues et problèmes de performances. La fonctionnalité suivante a été mise à jour pour cette version.

- **L’option achat est activée par défaut**. À partir de la version 87 de Microsoft Edge, les utilisateurs de l’entreprise peuvent profiter d’achats dans Microsoft Edge. Grâce aux fonctionnalités d’achat, Microsoft Edge permet aux utilisateurs de trouver des coupons et de meilleurs prix lors de leurs achats en ligne. (L’interface de coupon a été publiée avec la version stable 87.0.664.41). L’interface de comparaison des prix est désormais disponible dans cette mise à jour. Cette fonctionnalité peut être configurée à l’aide de la stratégie [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgeshoppingassistantenabled). Consultez notre [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) et [En savoir plus](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) sur les Achats Microsoft.

## <a name="version-87066452-november-30"></a>Version 87.0.664.52: 30 novembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-87066447-november-23"></a>Version 87.0.664.47: 23novembre

Résolution de divers bogues et problèmes de performances.

<!-- begin major 87 --->
## <a name="version-87066441-november-19"></a>Version87.0.664.41du 19novembre

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-19-2020)

### <a name="feature-updates"></a>Mises à jour des fonctionnalités

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

### <a name="policy-updates"></a>Mises à jour de stratégies

#### <a name="new-policies"></a>Nouvelles stratégies

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

#### <a name="deprecated-policy"></a>Stratégie Déconseillée

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) - Configurez l’expérience de la page nouvel onglet de Microsoft Edge.

#### <a name="obsoleted-policy"></a>Stratégie obsolète

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) - Réactivez les fonctionnalités de plateforme web déconseillées pendant une période limitée.

<!-- end major 87 -->

## <a name="version-86062269-november-13"></a>Version86.0.622.69du 13novembre

> [!IMPORTANT]
> Cette mise à jour contient [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) et [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), signalés par l’équipe Chromium comme cible code malveillant exploitant une faille de sécurité.

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-13-2020)

## <a name="version-86062268-november-11"></a>Version86.0.622.68du 11novembre

Les mises à jour de sécurité du canal stable sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-11-2020)

## <a name="version-86062263-november-4"></a>Version 86.0.622.63 du 4novembre

> [!IMPORTANT]
> Cette mise à jour contient [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), signalé par l’équipe Chromium comme cible de code malveillant exploitant une faille de sécurité.

Les mises à jour de sécurité du canal stable sont répertoriées [ici.](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-4-2020)

## <a name="version-86062261-november-2"></a>Version 86.0.622.61du 2novembre

Résolution de divers bogues et problèmes de performances.

## <a name="version-86062258-october-29"></a>Version86.0.622.58: 29octobre

Résolution de divers bogues et problèmes de performances.

## <a name="version-86062256-october-27"></a>Version86.0.622.56: 27octobre

Résolution de divers bogues et problèmes de performances.

## <a name="version-86062251-october-22"></a>Version86.0.622.51 du 22octobre

Les mises à jour de sécurité du canal stable sont répertoriées [ici](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-22-2020)

## <a name="version-86062248-october-20"></a>Version86.0.622.48 du 20octobre

Résolution de divers bogues et problèmes de performances.

## <a name="version-86062243-october-15"></a>Version 86.0.622.43 : 15 octobre

Résolution de divers bogues et problèmes de performances.

<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
