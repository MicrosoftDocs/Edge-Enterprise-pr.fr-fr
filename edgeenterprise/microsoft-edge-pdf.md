---
title: Lecteur PDF dans Microsoft Edge
ms.author: adigan
author: dan-wesley
manager: balajek
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: En savoir plus sur le lecteur PDF dans Microsoft Edge.
ms.openlocfilehash: 0b1cffceb63c1829c39bdd3fa658df2e5f776584
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643180"
---
# <a name="pdf-reader-in-microsoft-edge"></a>Lecteur PDF dans Microsoft Edge

Les fichiers PDF constituent une partie importante de nos vies quotidiennes. Ils se présentent sous forme de contrats et d’accords, de bulletins d’informations, de formulaires, d’Articles de recherche, de CV, etc. Ces fichiers soulignent la nécessité d’utiliser un lecteur PDF fiable, sécurisé et performant, pouvant être adopté par les entreprises.

Microsoft Edge inclut un lecteur PDF intégré qui vous permet d’ouvrir des fichiers PDF locaux, des fichiers PDF en ligne ou des fichiers PDF incorporés dans des pages web. Vous pouvez annoter ces fichiers à l’aide d’entrées manuscrites et de surlignage. Ce lecteur PDF offre aux utilisateurs une application unique pour répondre aux besoins des pages web et des documents PDF. Le lecteur Microsoft Edge PDF est une application sécurisée et fiable qui fonctionne sur les plateformes de bureau Windows et macOS.

> [!NOTE]
> Cet article concerne Microsoft Edge version 77 ou ultérieure.

## <a name="prerequisites-support-and-constraints"></a>Conditions préalables, support et contraintes

Le tableau suivant indique les canaux et les versions de Microsoft Edge qui prennent en charge chaque fonctionnalité de lecteur PDF.

| Fonctionnalité | Version de canal stable |
|---------|------------------------|
| Afficher et imprimer des fichiers PDF locaux, en ligne et incorporés | 79.0.309.71                |
| Remplissage de formulaires de base<br>(Les formulaires JavaScript ne sont pas pris en charge) | 79.0.309.71           |
|Table des matières| 86.0.622.38 |
| Affichage de page |Actuellement en promotion dans les canaux de [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/) |
| Navigation en mode d’attention |87.0.664.41 |
| Entrée manuscrite  | 80.0.361.48            |
| Personnalisation de l’entrée manuscrite | 83.0.478.54  |
| Highlight  | 81.0.416.53         |
| Notes de texte | Actuellement en promotion dans les canaux de [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/) |
| Lire à haute voix | 84.0.522.63  |
| Afficher les fichiers protégés par Microsoft Information Protection (MIP) | Support Windows dans 80.0.361.48<br>Prise en charge par Mac dans 81.0.416.53 |
|  Afficher les fichiers protégés par IRM(Information Rights Management)  | 83.0.478.37            |
| Afficher et valider les signatures numériques | Disponible sur les canaux Canary et Dev. On y travaille activement. |

### <a name="constraints"></a>Contraintes

Notez les contraintes suivantes pour le lecteur PDF actuel :

-  L’architecture de formulaires XML (XFA) est un format hérité de formulaires qui ne sont pas pris en charge dans Microsoft Edge.
-  La documentation relative aux scénarios d’accessibilité qui ne sont pas pris en charge pour le moment est disponible sur le blog [Rapports de conformité de l’accessibilité Microsoft](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/).

## <a name="features"></a>Fonctionnalités

Le lecteur PDF, intégré à Microsoft Edge, est livré avec les fonctionnalités de lecture et de navigation de base, telles que Zoom, Rotation, Ajuster à la page/largeur, passer à la page et rechercher, entre autres. Ils sont accessibles via une barre d'outils à épingler située en haut du contenu du PDF. Cette section donne une vue d’ensemble de certaines fonctions importantes. La capture d’écran suivante montre la barre d’outils du lecteur PDF.

![Barre d’outils du lecteur PDF](media/microsoft-edge-pdf/pdf-reader-toolbar.png)

### <a name="table-of-contents"></a>Table des matières

La table des matières permet aux utilisateurs de parcourir facilement les documents PDF qui ont une table des matières. Lorsqu’un utilisateur clique sur l’icône Table des matières, un volet de navigation qui affiche la liste des sections et sous-sections étiquetées dans le document PDF s’affiche. L’utilisateur peut ensuite cliquer sur l’une des étiquettes du volet pour accéder à cette section du document. Le volet reste ouvert aussi longtemps que nécessaire et peut être fermé lorsque l’utilisateur souhaite revenir à la lecture du document. La capture d’écran suivante montre le volet de navigation d’un document ouvert.

![Navigation du lecteur PDF avec la table des matières](media/microsoft-edge-pdf/pdf-reader-toc.png)

### <a name="page-view"></a>Affichage de page

Microsoft Edge prend en charge différents affichages pour les documents PDF dans nos canaux développement et canary. Les utilisateurs peuvent modifier la mise en page d'un document en passant d'une vue de page unique à deux pages affichées côte à côte. Pour modifier l’affichage du document PDF, les utilisateurs peuvent cliquer sur le bouton Affichage de page dans la barre d’outils PDF, puis choisir l’une ou l’autre des vues qu’ils souhaitent utiliser. La vue des deux pages est affichée dans la capture d’écran suivante.

![Lecteur PDF utilisant l’affichage deux pages du document.](media/microsoft-edge-pdf/pdf-reader-page-view.png)

### <a name="caret-mode-browsing"></a>Navigation en mode d’attention

La navigation rapide est disponible pour les fichiers PDF ouverts dans Microsoft Edge, ce qui signifie que les utilisateurs peuvent interagir avec les fichiers PDF à l’aide du clavier. Si un utilisateur appuie sur la touche F7 n'importe où dans le navigateur, on lui demande si la navigation au clavier doit être activée. Si elle est activée, la navigation au clavier est disponible pour tout contenu ouvert dans le navigateur, qu’il s’agit de fichiers PDF ou de pages web. Lorsqu’un utilisateur appuie de nouveau sur F7, la navigation au clavier est désactivée. Lorsque la navigation au clavier est active et que le contenu est actif, les utilisateurs voient un curseur clignoter dans le fichier PDF. Le curseur peut également être utilisé pour naviguer dans le fichier ou pour sélectionner du texte en appuyant sur la touche Maj tout en déplaçant le curseur. Cette capacité permet aux utilisateurs de créer facilement des éléments en tant que surlignages, ou d'interagir avec des éléments en tant que liens, de remplir des champs avec le clavier. La capture d'écran suivante montre le menu contextuel permettant d'activer le mode de navigation au clavier.

![Menu lecteur PDF pour la navigation en mode Clavier.](media/microsoft-edge-pdf/pdf-reader-caret-mode.png)

### <a name="inking"></a>Entrée manuscrite

L’entrée manuscrite dans les fichiers PDF est utile pour prendre des notes rapides afin de référencer, signer ou remplir des formulaires PDF facilement. Cette fonctionnalité est désormais disponible dans Microsoft Edge. En plus des fichiers PDF pour l’entrée manuscrite, vous pouvez utiliser des couleurs et une épaisseur de trait pour attirer l’attention sur différentes parties du fichier PDF. La capture d’écran suivante montre comment un utilisateur peut ajouter l’entrée manuscrite à une page PDF.

![Page Ajouter l’entrée manuscrite au format PDF](media/microsoft-edge-pdf/pdf-reader-inking.png)

### <a name="highlight"></a>Highlight

Le lecteur PDF dans Microsoft Edge inclut la prise en charge de l’ajout et de la modification des éléments en surbrillance. Pour créer un surlignage, l’utilisateur doit simplement sélectionner le texte, cliquer avec le bouton droit sur celui-ci, sélectionner surlignages dans le menu et choisir la couleur souhaitée. Vous pouvez également créer des zones lumineuses à l’aide d’un stylet ou d’un clavier. La capture d’écran suivante montre les options disponibles.

![Utiliser l’option surlignage dans le lecteur PDF](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### <a name="text-notes"></a>Notes de texte

Lors de la lecture d’un fichier PDF, des notes de texte peuvent être ajoutées au texte du fichier pour ajouter des idées pour faciliter la référence ultérieurement.

Les utilisateurs peuvent ajouter une note en sélectionnant l’élément de texte pour lequel ils souhaitent ajouter une note et en appelant le menu contextuel de clic droit. La sélection de l’option **Ajouter un commentaire** dans le menu ouvre une zone de texte dans laquelle les utilisateurs peuvent ajouter leurs commentaires. Ils peuvent taper le commentaire, puis cliquer sur la coche pour enregistrer le commentaire.

Une fois qu'une note a été ajoutée, le texte sélectionné est mis en surbrillance et une icône de commentaire s’affiche pour indiquer le commentaire. Les utilisateurs peuvent survoler cette icône pour afficher un aperçu du commentaire ou cliquer dessus pour ouvrir et modifier la note.

La capture d'écran suivante montre une note ajoutée au texte mis en surbrillance.

![Le lecteur PDF ajoute une note de texte au document.](media/microsoft-edge-pdf/pdf-reader-text-note.png)

### <a name="read-aloud"></a>Lire à haute voix

La lecture à voix haute pour PDF ajoute la commodité d’écouter du contenu PDF tout en faisant d’autres tâches qui peuvent être importantes pour les utilisateurs. Elle permet également aux apprenants de se concentrer sur le contenu, ce qui facilite l’apprentissage. La capture d’écran suivante montre un exemple de lecture à voix haute. Le surlignage indique le texte qui est en cours de lecture.

![Utiliser l’option surlignable pour lire à voix haute dans un lecteur PDF](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### <a name="protected-pdfs"></a>Fichiers PDF protégés

[Microsoft Information Protection (MIP)](/microsoft-365/compliance/protect-information?preserve-view=true&view=o365-worldwide) permet aux utilisateurs de collaborer en toute sécurité avec d’autres personnes, conformément aux stratégies de conformité de votre organisation. Une fois un fichier protégé, les actions que les utilisateurs peuvent effectuer sont déterminées par les autorisations qui leur sont affectées.

> [!IMPORTANT]
> Une licence est requise pour MIP. Pour plus d’informations, consultez ces [conseils concernant les licences Microsoft 365](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection).

Ces fichiers peuvent être ouverts directement dans le navigateur, sans qu’il soit nécessaire de télécharger d’autres logiciels ou d’installer un complément. Cette fonctionnalité intègre la sécurité fournie par MIP directement dans le navigateur, offrant un flux de travail transparent.

![Document PDF protégé.](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

Outre les fichiers protégés par MIP, les fichiers PDF dans des bibliothèques SharePoint protégées par[Gestion des droits relatifs à l'information (IRM)](/microsoft-365/compliance/set-up-irm-in-sp-admin-center?preserve-view=true&view=o365-worldwide) peuvent également être ouverts en mode natif dans le navigateur.

Avec Microsoft Edge, les utilisateurs peuvent afficher les fichiers protégés par MIP enregistrés localement ou dans le cloud. Si vous l’enregistrez en local, le fichier peut être ouvert directement dans le navigateur. Si le fichier est ouvert à partir d’un service cloud sous SharePoint, l’utilisateur peut avoir besoin d’utiliser l’option « Ouvrir dans le navigateur ».

Si le profil que l’utilisateur est connecté à Microsoft Edge avec dispose au minimum des autorisations d’affichage sur le fichier, le fichier s’ouvre dans Microsoft Edge.

![Invite à enregistrer la page PDF SharePoint protégé par MIP](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

### <a name="view-and-validate-certificate-based-digital-signatures"></a>Afficher et valider des signatures numériques basées sur des certificats

Dans ce monde numérique, il devient important d’établir l’authenticité et la propriété du contenu du document. Les signatures numériques basées sur des certificats sont couramment utilisées dans les documents PDF pour s’assurer que le contenu du document est identique à celui prévu par l’auteur et qu’il n’a pas été modifié. Avec Microsoft Edge, vous pouvez afficher et valider des signatures numériques de certificat dans des formats PDF.

Nous travaillons activement sur l’amélioration de la prise en charge pour répondre à d’autres scénarios et attendons des commentaires sur le même scénario.

## <a name="accessibility"></a>Accessibilité

Le lecteur PDF inclut la prise en charge de l’accessibilité du clavier, du mode contraste élevé et de la prise en charge du lecteur d’écran sur les appareils Windows et macOS.

### <a name="keyboard-accessibility"></a>Accessibilité du clavier

Les utilisateurs peuvent utiliser la navigation vers différentes parties du document avec lequel un utilisateur peut interagir (par exemple, champs de formulaire et surlignages) à l’aide du clavier. Les utilisateurs peuvent également utiliser le mode Clavier pour naviguer et interagir avec les fichiers PDF à l’aide du clavier.

### <a name="high-contrast-mode"></a>Mode contraste élevé

Le lecteur PDF utilise les paramètres définis au niveau du système d’exploitation pour afficher le contenu PDF en mode contraste élevé.

### <a name="screen-reader-support"></a>Prise en charge du lecteur d’écran

Les utilisateurs peuvent parcourir et lire les fichiers PDF à l’aide de lecteurs d’écran sur les ordinateurs Windows et Mac.

## <a name="security-and-reliability"></a>Sécurité et fiabilité

La sécurité est parmi les principes les plus importants pour toutes les organisations. La sécurité du lecteur PDF fait partie intégrante de la conception de la sécurité Microsoft Edge. Deux des fonctionnalités de sécurité les plus importantes de la perspective lecteur PDF, deux fonctionnalités de sécurité importantes sont l’isolation de processus et Microsoft Defender Application Guard (Application Guard).

- Isolation des processus. Les fichiers PDF ouverts à partir de différents sites web sont totalement isolés. Il n’est pas nécessaire de communiquer avec des sites web ou des fichiers PDF ouverts à partir d’une autre source. La navigation au format PDF est sécurisée contre toutes les attaques qui envisagent d’utiliser des fichiers PDF compromis comme une surface d’attaque.

- Application Guard. Avec Application Guard, les administrateurs peuvent établir une liste de sites approuvés par leur organisation. Si les utilisateurs ouvrent d’autres sites, ils sont ouverts dans une fenêtre Application Guard distincte qui s’exécute dans son propre conteneur. Le conteneur permet de protéger le réseau d’entreprise et les données sur l’ordinateur d’un utilisateur contre la compromission de celui-ci.<br><br>
Cette protection s’applique également aux fichiers PDF en ligne consultés. De plus, tous les fichiers PDF téléchargés à partir d’une fenêtre Application Guard sont stockés, et le cas échéant, rouvert dans le conteneur. Cela permet de maintenir la sécurité de votre environnement non seulement lors du téléchargement du fichier, mais tout au long de son cycle de vie. Pour plus d’informations, voir [Application Guard](./microsoft-edge-security-windows-defender-application-guard.md).

### <a name="reliability"></a>Fiabilité

Étant donné que Microsoft Edge est basé sur le chrome, les utilisateurs peuvent s’attendre à ce que leur niveau de fiabilité soit utilisé pour les voir dans d’autres navigateurs basés sur Chromium.

## <a name="deploy-and-update-pdf-reader"></a>Déployer et mettre à jour le lecteur PDF

Le lecteur PDF est déployé et mis à jour avec le reste du navigateur Microsoft Edge. Pour en savoir plus sur le déploiement de Microsoft Edge, Regardez la vidéo [Déploiement de Microsoft Edge sur des centaines ou des milliers d’appareils](microsoft-edge-video-deploy.md) vidéo. Vous pouvez également consulter d’autres informations de déploiement sur la page d’accueil [Documentation Microsoft Edge](./index.yml).

> [!TIP]
> Vous pouvez définir Microsoft Edge comme lecteur PDF par défaut pour votre organisation. Pour ce faire, [procédez comme suit](./edge-default-browser.md).

## <a name="roadmap-and-feedback"></a>Feuille de route et commentaires

La feuille de route pour le lecteur PDF dans Microsoft Edge est disponible [ici.](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667)

Nous recherchons activement les commentaires des fonctionnalités que vous trouvez importantes. N’hésitez pas à nous envoyer vos commentaires via le forum [Microsoft Edge Insider.](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider)

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Feuille de route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap)
- [Vidéo : lecteur PDF de qualité professionnelle Microsoft Edge](microsoft-edge-video-pdf-reader.md)