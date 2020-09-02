---
title: Configurer Microsoft Edge pour macOS à l'aide d'un fichier .plist
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 02/14/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer les paramètres de stratégie MicrosoftEdge sur macOS à l'aide d'un fichier .plist
ms.openlocfilehash: 84469a4f84deeee0e47b6d8899426fa36cf345aa
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979662"
---
# Configurer les paramètres de stratégie MicrosoftEdge pour macOS à l'aide d'un fichier .plist

Cet article explique comment configurer MicrosoftEdge sur macOS à l’aide d’un fichier de liste de propriétés (.plist). Découvrez la création et le déploiement de ce fichier dans Microsoft Intune.

Pour plus d’informations, consultez [À propos des fichiers de listes de propriétés d’informations](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (site web d’Apple) et [Paramètres de charge utile personnalisés](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

## Configurer les stratégies MicrosoftEdge sur macOS

La première étape consiste à créer une soumission. Vous pouvez créer le fichier plist avec n’importe quel éditeur de texte ou vous pouvez utiliser [Terminal pour créer le profil de configuration](#create-a-configuration-profile-using-terminal). Toutefois, il est plus facile de créer et de modifier un fichier plist à l’aide d’un outil qui met en forme le code XML à votre place. *Xcode* est un environnement de développement intégré gratuit que vous pouvez obtenir de l’une des manières suivantes:

- [Site web des développeurs Apple](https://developer.apple.com/xcode/)
- [AppStore Mac](https://apps.apple.com/app/xcode/id497799835?mt=12)

Pour obtenir la liste des stratégies prises en charge et leurs noms de clé de préférence, consultez [Référence sur les stratégies de navigateur MicrosoftEdge](microsoft-edge-policies.md). Le fichier de modèles de stratégie, qui peut être téléchargé à partir de la [page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise) contient un exemple de plist (*itadminexample.plist*) dans le dossier d’**exemples**. L’exemple de fichier contient tous les types de données pris en charge que vous pouvez personnaliser pour définir vos paramètres de stratégie. 

L’étape suivante, après la création du contenu de votre plist, consiste à la nommer en utilisant le domaine de préférence Microsoft Edge, *com.microsoft.Edge*. Le nom respecte la casse et ne doit pas contenir le canal que vous ciblez, car il s’applique à tous les canaux MicrosoftEdge. Le nom du fichier plist doit être **_com.microsoft.Edge.plist_**. 

> [!IMPORTANT]
> À partir de la build78.0.249.2, tous les canaux MicrosoftEdge sur macOS lisent à partir du domaine de préférence **com.microsoft.Edge**. Toutes les versions antérieures lisent à partir d’un domaine spécifique du canal, tel que **com.microsoft.Edge.Dev** pour le canal Dev.

La dernière étape consiste à déployer votre plist sur les appareils Mac de vos utilisateurs à l’aide de votre fournisseur GPM préféré, tel que MicrosoftIntune. Pour obtenir des instructions, consultez [Déployer votre plist](#deploy-your-plist).

### Créer un profil de configuration à l’aide de terminal

1. Dans Terminal, utilisez la commande suivante pour créer un plist MicrosoftEdge sur votre bureau avec vos paramètres préférés:

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. Convertissez la plist d’un format binaire en format texte brut:

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```
Après avoir converti le fichier, vérifiez que vos données de stratégie sont correctes et qu’elles contiennent les paramètres de votre choix pour votre profil de configuration.

> [!NOTE]
> Seules les paires de valeurs de clé doivent figurer dans le contenu du fichier plist ou XML. Avant de télécharger votre fichier dans Intune, supprimez toutes les valeurs \<plist> et \<dict>, ainsi que les en-têtes XML de votre fichier. Le fichier ne doit contenir que des paires clé-valeur.

## Déployer votre plist

Pour MicrosoftIntune créez un profil de configuration de périphérique ciblant la plateforme macOS et sélectionnez le type de profil *Fichier de préférence*. Ciblez **com.microsoft.Edge** comme nom de domaine de préférence et téléchargez votre plist. Pour plus d’informations, consultez [Ajouter un fichier de liste de propriétés à des périphériques macOS à l’aide de Microsoft Intune](https://docs.microsoft.com/intune/configuration/preference-file-settings-macos).

Pour Jamf, téléchargez le fichier plist en tant que charge utile des *Paramètres personnalisés*.

## Forum Aux Questions

### MicrosoftEdge peut-il être configuré pour utiliser les préférences principales?

Oui, vous pouvez configurer MicrosoftEdge pour qu’il utilise un fichier de préférences principales.

Un fichier de préférences principales vous permet de configurer les paramètres par défaut d’un profil utilisateur de navigateur lors du déploiement de MicrosoftEdge. Vous pouvez également utiliser un fichier de préférences principales pour appliquer des paramètres sur des ordinateurs qui ne sont pas gérés par un système de gestion des périphériques. Ces paramètres sont appliqués au profil de l’utilisateur la première fois que l’utilisateur exécute le navigateur. Une fois que l’utilisateur a exécuté le navigateur, les modifications apportées au fichier de préférences principales ne sont pas appliquées. Un utilisateur peut modifier les paramètres à partir des préférences principales dans le navigateur. Si vous souhaitez rendre un paramètre obligatoire ou modifier un paramètre après la première exécution du navigateur, vous devez utiliser une stratégie.

Un fichier de préférences principales vous permet de personnaliser de nombreux paramètres et préférences pour le navigateur, y compris ceux partagés avec d’autres navigateurs basés Chromium et spécifiques à MicrosoftEdge.  Les préférences liées à la stratégie peuvent être configurées à l’aide du fichier de préférences principales. Dans les cas où une stratégie est définie et qu’un jeu de préférences principales correspondant est défini, le paramètre de stratégie est prioritaire.

> [!IMPORTANT]
> Toutes les préférences disponibles peuvent ne pas être cohérentes avec la terminologie et les conventions d’affectation de noms de MicrosoftEdge.  Il n’est pas garanti que ces préférences continuent de fonctionner comme prévu dans les prochaines versions. Les préférences peuvent être modifiées ou ignorées dans les versions ultérieures.

Un fichier de préférences principales est un fichier texte mis en forme à l’aide du balisage JSON. Ce fichier doit être ajouté au même répertoire que le msedge.exe exécutable. Pour les déploiements à l’échelle du système sur macOS, c’est généralement: «*~/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*» ou «*/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*».

## Articles associés

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Configurer pour macOS avec Jamf](configure-microsoft-edge-on-mac-jamf.md)
- [Configurer pour Windows](configure-microsoft-edge.md)
- [Configurer pour Windows avec Intune](configure-edge-with-intune.md)
