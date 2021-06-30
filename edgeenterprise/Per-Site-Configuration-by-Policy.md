---
title: 'Configuration par site par stratégie '
ms.author: collw
author: AndreaLBarr
manager: laurawi
ms.date: 05/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Configuration par site par stratégie '
ms.openlocfilehash: 6bba2c9b1d691c338a3146ef246de9f94e262a03
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618093"
---
# <a name="persite-configuration-by-policy"></a>Configuration par site par stratégie

## <a name="introduction-browsers-as-decision-makers"></a>Introduction: Navigateurs en tant que décideurs

Dans le cadre de chaque chargement de page, les navigateurs prennent de nombreuses décisions: une API particulière doit-elle être disponible? Une charge de ressources doit-elle être autorisée? Le script doit-il être autorisé à s’exécuter? La liste est longue.

Dans la plupart des cas, les décisions sont régies par deux entrées: un paramètre utilisateur et l’URL de la page pour laquelle la décision est prise.

Dans la plateforme web InternetExplorer héritée, chacune de ces décisions était appelée [URLAction](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178%28v%3dvs.85%29)et les paramètres utilisateur et stratégie de groupe Entreprise dans le Panneau de configuration Internet contrôlaient la façon dont le navigateur gérait chaque décision.  

Dans MicrosoftEdge, la plupart des autorisations par site sont contrôlées par des paramètres et des stratégies exprimés à l’aide d’une syntaxe simple avec une prise en charge limitée aux caractères génériques. Les zones Sécurité Windows sont toujours utilisées uniquement pour un petit nombre de décisions de configuration.

## <a name="background-windows-security-zones"></a>Contexte: Zones Sécurité Windows

Pour simplifier la configuration de l’utilisateur ou de l’administrateur, la plateforme héritée a classé les sites en cinq **zones de sécurité** différentes: Ordinateur local, Intranet local, Approuvé, Internet et Sites restreints.

Lors de la prise de décision, le navigateur mappe d’abord le site web sur une zone, puis consulte le paramètre de cette URLAction pour cette zone pour décider de l’action à effectuer. Les valeurs par défaut raisonnables telles que «Satisfaire automatiquement les défis d’authentification de mon intranet» signifient que la plupart des utilisateurs n’ont jamais eu besoin de modifier les paramètres par rapport à leurs valeurs par défaut.

Les utilisateurs peuvent utiliser le Panneau de configuration Internet pour affecter des sites spécifiques aux zones et configurer les résultats des autorisations pour chaque zone. Dans les environnements gérés, les administrateurs peuvent utiliser la stratégie de groupe pour affecter des sites spécifiques à des zones (via la stratégie «Liste d’affectations de site à zone» ) et spécifier les paramètres d’URLActions par zone. Au-delà de l’affectation manuelle d’utilisateurs ou d’administration de sites à des zones, des heuristiques supplémentaires peuvent [affecter des sites à la zone Intranet local](/archive/blogs/ieinternals/the-intranet-zone). En particulier, les noms d’hôte pointillés (par exemple, `http://payroll`) ont été affectés à la zone Intranet. Si un script de configuration de proxy a été utilisé, tous les sites configurés pour contourner le proxy sont mappés à la zone Intranet.

L’ancienne version de Microsoft Edge a hérité de l’architecture Zones de son prédécesseur InternetExplorer avec quelques modifications de simplification:

- Les cinq zones Windows intégrées ont été réduites à trois: Internet (Internet), Approuvé (Intranet+Approuvé) et Ordinateur local. La zone Sites restreints a été supprimée.

- Les mappages zone vers URLAction ont été codés en dur dans le navigateur, en ignorant les stratégies de groupe et les paramètres du Panneau de configuration Internet.

## <a name="per-site-permissions-in-the-microsoft-edge"></a>Autorisations par site dans Microsoft Edge

Contrairement à ses prédécesseurs, le nouveau Microsoft Edge fait un usage très limité des zones Sécurité Windows. Au lieu de cela, la plupart des autorisations et des fonctionnalités qui offrent aux administrateurs une configuration par site via la  [stratégie](/deployedge/microsoft-edge-policies) s’appuient sur des listes de règles au  [format de filtre d’URL](/DeployEdge/edge-learnmmore-url-list-filter%20format).

Lorsque les utilisateurs finaux ouvrent <code>edge://settings/content/siteDetails?site=https://example.com</code>, ils trouvent une longue liste de commutateurs de configuration et de listes pour différentes autorisations. Les utilisateurs utilisent rarement la page Paramètres directement, faisant des choix lors de la navigation à l’aide de divers widgets et boutons bascules dans la barre d’ **Informations de page** (qui s’affiche lorsque vous cliquez sur l’icône de verrouillage dans la barre d’adresses) ou via différentes invites ou boutons sur le bord droit de la barre d’adresses.

Les entreprises peuvent utiliser la stratégie de groupe pour mettre en service des listes de sites pour des stratégies individuelles qui contrôlent le comportement du navigateur. Pour rechercher ces stratégies, ouvrez simplement la [documentation de la stratégie de groupe Microsoft Edge](/deployedge/microsoft-edge-policies) , puis recherchez **ForUrls** pour trouver les stratégies qui autorisent et bloquent le comportement en fonction de l’URL du site chargée. La plupart des paramètres pertinents sont répertoriés dans la section  [Stratégie de groupe pour les Paramètres de contenu](/deployedge/microsoft-edge-policies#content-settings).

Il existe également un certain nombre de stratégies (dont les noms contiennent **Par défaut**) qui contrôlent le comportement par défaut d’un paramètre donné.

La plupart des paramètres sont très obscurs (WebSerial, WebMIDI) et il n’y a très souvent aucune raison de modifier un paramètre par rapport à la valeur par défaut (Images).

## <a name="common-questions"></a>Questions courantes

## <a name="q-can-the-url-filter-format-match-on-a-sites-ip-address"></a>Q: Le format de filtre d’URL peut-il correspondre à l’adresse IP d’un site?

Non, le format ne prend pas en charge la spécification d’une plage d’adresses IP pour les listes vert et rouge. Il prend en charge la spécification de  **littéraux** d’IP individuels, mais ces règles sont uniquement respectées si l’utilisateur navigue vers le site à l’aide du littéral (par exemple,  <http://127.0.0.1/>). Si un nom d’hôte est utilisé (<http://localhost>), la règle de littéral d’IP n’est pas respectée, même si l’adresse IP résolue de l’hôte correspond à l’adresse IP répertoriée par le filtre.

## <a name="q-can-url-filters-matchjustdotless-host-names"></a>Q: Les filtres d’URL peuvent-ils correspondre uniquement aux noms d’hôtes pointillés?

Non. Vous devez lister individuellement chaque nom d’hôte souhaité, par exemple (`https://payroll`, `https://stock`, `https://who`, etc.).

Si vous avez été suffisamment visionnaire pour structurer votre intranet de telle sorte que vos noms d’hôte soient de la forme:

- <div style="display: inline">`https://payroll.contoso-intranet.com`</div>

- <div style="display: inline">`https://timecard.contoso-intranet.com`</div>

- <div style="display: inline">`https://sharepoint.contoso-intranet.com`</div>

Félicitations, vous avez implémenté une meilleure pratique. Vous pouvez configurer chaque stratégie souhaitée avec une entrée ***.contoso-intranet.com** et l’ensemble de votre intranet sera accepté.

## <a name="use-of-security-zones-inthe-microsoft-edge"></a>Utilisation des zones de sécurité dans Microsoft Edge

Bien que MicrosoftEdge s’appuie principalement sur des stratégies individuelles utilisant le format de filtre d’URL, il continue d’utiliser les zones de Sécurité Windows par défaut dans un petit nombre d’endroits afin de simplifier le déploiement au sein des entreprises qui se basent toujours sur la configuration des zones. Les comportements suivants sont contrôlés par la stratégie de zone:

1. Lorsque vous décidez de libérer ou non automatiquement les informations d’identification de l’Authentification intégrée Windows (Kerberos/NTLM)

2. Lorsque vous décidez comment gérer les téléchargements de fichiers

3. Pour le mode Internet Explorer

## <a name="credential-release"></a>Version des informations d’identification

Par défaut, Microsoft Edge évaluera URLACTION_CREDENTIALS_USE pour déterminer si l’Authentification intégrée Windows est utilisée automatiquement ou si l’utilisateur doit voir une invite d’authentification manuelle. La configuration [d’une stratégie de liste de sites AuthServerAllowlist](/deployedge/microsoft-edge-policies#authserverallowlist) empêche la consultation de la stratégie de zone.

## <a name="file-downloads"></a>Téléchargements de fichiers

Preuve sur les origines d’un téléchargement de fichier (appelée «[Marque du web](https://textslashplain.com/2016/04/04/downloads-and-the-mark-of-the-web/)» est enregistrée pour les fichiers téléchargés à partir de la zone Internet. D’autres applications (par exemple, WindowsShell, MicrosoftOffice, etc.) peuvent prendre en compte cette preuve d’origine lors du choix du traitement d’un fichier.

Si la stratégie de zone Sécurité Windows est configurée pour désactiver le paramètre Lancement des applications et des fichiers non sécurisés, le gestionnaire de téléchargement MicrosoftEdge bloquera les téléchargements de fichiers à partir des sites de cette zone avec une note: «Impossible de télécharger – Bloqué».  

## <a name="ie-mode"></a>Mode Internet Explorer

Le mode IE peut être configuré pour ouvrir tous [les sites Intranet en mode IE](/deployedge/edge-ie-mode#configure-all-intranet-sites). Dans cette configuration, Edge évalue la zone d’une URL lors du choix de son ouverture en mode IE. Au-delà de cette décision initiale, les onglets du mode IE exécutent vraiment Internet Explorer et, par conséquent, ils évaluent les paramètres de zones pour chaque décision de stratégie, tout comme Internet Explorer lui-même.

## <a name="summary"></a>Résumé

Dans la plupart des cas, les paramètres Microsoft Edge peuvent être laissés à leurs valeurs par défaut. Les administrateurs qui souhaitent modifier les valeurs par défaut de tous les sites ou de sites spécifiques peuvent utiliser les stratégies de groupe appropriées pour spécifier des listes de sites ou des comportements par défaut. Dans de nombreux cas (publication des informations d’identification, téléchargement de fichiers et mode IE), les administrateurs continueront à contrôler le comportement en configurant les paramètres des zones Sécurité Windows.
