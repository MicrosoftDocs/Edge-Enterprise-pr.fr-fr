---
title: Lecteur PDF dans Microsoft Edge
ms.author: adigan
author: dan-wesley
manager: balajek
ms.date: 08/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: En savoir plus sur le lecteur PDF dans Microsoft Edge.
ms.openlocfilehash: c189bc08d4af0c9d5c4d9c573e0b5b7ef32a7fb3
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979833"
---
# Lecteur PDF dans Microsoft Edge

Les fichiers PDF constituent une partie importante de nos vies quotidiennes. Ils se présentent sous forme de contrats et d’accords, de bulletins d’informations, de formulaires, d’Articles de recherche, de CV, etc. Ces fichiers soulignent la nécessité d’utiliser un lecteur PDF fiable, sécurisé et performant, pouvant être adopté par les entreprises.

Microsoft Edge inclut un lecteur PDF intégré qui vous permet d’ouvrir des fichiers PDF locaux, des fichiers PDF en ligne ou des fichiers PDF incorporés dans des pages web. Vous pouvez annoter ces fichiers à l’aide d’entrées manuscrites et de surlignage. Ce lecteur PDF offre aux utilisateurs une application unique pour répondre aux besoins des pages web et des documents PDF. Le lecteur Microsoft Edge PDF est une application sécurisée et fiable qui fonctionne sur les plateformes de bureau Windows et macOS.

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

## Conditions préalables, support et contraintes

Le tableau suivant indique les canaux et les versions de Microsoft Edge qui prennent en charge chaque fonctionnalité de lecteur PDF.

| Fonctionnalité | Version de canal stable |
|---------|------------------------|
| Afficher et imprimer des fichiers PDF locaux, en ligne et incorporés | 79.0.309.71                |
| Remplissage de formulaires de base<br>(Les formulaires JavaScript ne sont pas pris en charge) | 79.0.309.71           |
| Entrée manuscrite  | 80.0.361.48            |
| Personnalisation de l’entrée manuscrite | 83.0.478.54  |
| Highlight  | 81.0.416.53         |
| Lire à haute voix | Actuellement en promotion dans les canaux de [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/) |
| Afficher les fichiers protégés par MIP | Support Windows dans 80.0.361.48<br>Prise en charge par Mac dans 81.0.416.53 |
|  Afficher les fichiers protégés par IRM  | 83.0.478.37            |

### Contraintes

Notez les contraintes suivantes pour le lecteur PDF actuel:

-  L’architecture de formulaires XML (XFA) est un format hérité de formulaires qui ne sont pas pris en charge dans Microsoft Edge.
-  La documentation relative aux scénarios d’accessibilité qui ne sont pas pris en charge pour le moment est disponible sur le blog [Rapports de conformité de l’accessibilité Microsoft](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/).

## Fonctionnalités

### Entrée manuscrite

L’entrée manuscrite dans les fichiers PDF est utile pour prendre des notes rapides afin de référencer, signer ou remplir des formulaires PDF facilement. Cette fonctionnalité est désormais disponible dans Microsoft Edge. En plus des fichiers PDF pour l’entrée manuscrite, vous pouvez utiliser des couleurs et une épaisseur de trait pour attirer l’attention sur différentes parties du fichier PDF. La capture d’écran suivante montre comment un utilisateur peut ajouter l’entrée manuscrite à une page PDF.

<!-- SCREENSHOT -->
![Page Ajouter l’entrée manuscrite au format PDF](media/microsoft-edge-pdf/pdf-reader-inking.png)

### Highlight

Le lecteur PDF dans Microsoft Edge inclut la prise en charge de l’ajout et de la modification des éléments en surbrillance. Pour créer un surlignage, l’utilisateur doit simplement sélectionner le texte, cliquer avec le bouton droit sur celui-ci, sélectionner surlignages dans le menu et choisir la couleur souhaitée. La capture d’écran suivante montre les options disponibles.

![Utiliser l’option surlignage dans le lecteur PDF](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### Lire à haute voix

La lecture à voix haute pour PDF ajoute la commodité d’écouter du contenu PDF tout en effectuant d’autres tâches susceptibles d’être importantes pour les utilisateurs. Elle permet également aux apprenants de se concentrer sur le contenu, ce qui facilite l’apprentissage. La capture d’écran suivante montre un exemple de lecture à voix haute. Le surlignage indique le texte qui est en cours de lecture.

![Utiliser l’option surlignage dans le lecteur PDF](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### Fichiers PDF protégés

[Microsoft Information Protection (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide) permet aux utilisateurs de collaborer en toute sécurité avec d’autres personnes, conformément aux stratégies de conformité de votre organisation. Une fois un fichier protégé, les actions que les utilisateurs peuvent effectuer sont déterminées par les autorisations qui leur sont affectées.

Ces fichiers peuvent être ouverts directement dans le navigateur, sans qu’il soit nécessaire de télécharger d’autres logiciels ou d’installer un complément. Cette opération intègre la sécurité fournie par MIP directement dans le navigateur, offrant un flux de travail transparent.

<!-- SCREENSHOT -->
![Document PDF protégé.](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

Outre les fichiers protégés par MIP, les fichiers PDF dans des bibliothèques SharePoint protégées par[Gestion des droits relatifs à l'information (IRM)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide) peuvent également être ouverts en mode natif dans le navigateur.

Avec Microsoft Edge, les utilisateurs peuvent afficher les fichiers protégés par MIP enregistrés localement ou dans le cloud. Si vous l’enregistrez en local, le fichier peut être ouvert directement dans le navigateur. Si le fichier est ouvert à partir d’un service cloud sous SharePoint, l’utilisateur peut avoir besoin d’utiliser l’option «Ouvrir dans le navigateur».

Si le profil que l’utilisateur est connecté à Microsoft Edge avec dispose au minimum des autorisations d’affichage sur le fichier, le fichier s’ouvre dans Microsoft Edge.

<!-- SCREENSHOT -->
![Invite à enregistrer la page PDF SharePoint protégé par MIP](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

## Accessibilité

Le lecteur PDF inclut la prise en charge de l’accessibilité du clavier, du mode contraste élevé et de la prise en charge du lecteur d’écran sur les appareils Windows et macOS.

### Accessibilité du clavier

Les utilisateurs peuvent utiliser la navigation vers différentes parties du document avec lequel un utilisateur peut interagir (par exemple, champs de formulaire et surlignages) à l’aide du clavier.

<!-- SCREENSHOT -->

### Mode contraste élevé

Le lecteur PDF utilise les paramètres définis au niveau du système d’exploitation pour afficher le contenu PDF en mode contraste élevé.

<!-- SCREENSHOT -->
<!--![High contrast mode for pdf file](media/microsoft-edge-pdf/pdf-reader-high-contrast.png)-->

### Prise en charge du lecteur d’écran

Les utilisateurs peuvent parcourir et lire les fichiers PDF à l’aide de lecteurs d’écran sur les ordinateurs Windows et Mac. <!--The next screenshot shows the toolbar that users can use for audio settings when they're using the Read Aloud option in PDF reader. -->

<!-- SCREENSHOT -->
<!--
![Screen reader toolbar](media/microsoft-edge-pdf/pdf-reader-read-aloud.png) -->

## Sécurité et fiabilité

La sécurité est parmi les principes les plus importants pour toutes les organisations. La sécurité du lecteur PDF fait partie intégrante de la conception de la sécurité Microsoft Edge. Deux des fonctionnalités de sécurité les plus importantes de la perspective lecteur PDF, deux fonctionnalités de sécurité importantes sont l’isolation de processus et Microsoft Defender Application Guard (Application Guard).

- Isolation des processus. Les fichiers PDF ouverts à partir de différents sites web sont totalement isolés. Il n’est pas nécessaire de communiquer avec des sites web ou des fichiers PDF ouverts à partir d’une autre source. La navigation au format PDF est sécurisée contre toutes les attaques qui envisagent d’utiliser des fichiers PDF compromis comme une surface d’attaque.

- ApplicationGuard. Avec Application Guard, les administrateurs peuvent établir une liste de sites approuvés par leur organisation. Si les utilisateurs ouvrent d’autres sites, ils sont ouverts dans une fenêtre Application Guard distincte qui s’exécute dans son propre conteneur. Le conteneur permet de protéger le réseau d’entreprise et les données sur l’ordinateur d’un utilisateur contre la compromission de celui-ci.<br><br>
Cette protection s’applique également aux fichiers PDF en ligne consultés. De plus, tous les fichiers PDF téléchargés à partir d’une fenêtre Application Guard sont stockés, et le cas échéant, rouvert dans le conteneur. Cela permet de maintenir la sécurité de votre environnement non seulement lors du téléchargement du fichier, mais tout au long de son cycle de vie. Pour plus d’informations, voir [Application Guard](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).

### Fiabilité

Étant donné que Microsoft Edge est basé sur le chrome, les utilisateurs peuvent s’attendre à ce que leur niveau de fiabilité soit utilisé pour les voir dans Google Chrome.

## Déployer et mettre à jour le lecteur PDF

Le lecteur PDF est déployé et mis à jour avec le reste du navigateur Microsoft Edge. Pour en savoir plus sur le déploiement de Microsoft Edge, Regardez la vidéo [Déploiement de Microsoft Edge sur des centaines ou des milliers d’appareils](microsoft-edge-video-deploy.md) vidéo. Vous pouvez également consulter d’autres informations de déploiement sur la page d’accueil [Documentation Microsoft Edge](https://docs.microsoft.com/DeployEdge/).

> [!TIP]
> Vous pouvez définir Microsoft Edge comme lecteur PDF par défaut pour votre organisation. Pour ce faire, [procédez comme suit](https://docs.microsoft.com/deployedge/edge-default-browser).

## Feuille de route et commentaires

La feuille de route pour le lecteur PDF dans Microsoft Edge est disponible [ici](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667).

Nous recherchons activement les commentaires des fonctionnalités que vous trouvez importants. N’hésitez pas à nous envoyer des commentaires via [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/) et sur le forum [Microsoft Edge Insider](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider).

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)