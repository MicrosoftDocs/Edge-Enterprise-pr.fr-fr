---
title: Configurer les stratégies MicrosoftEdge sur macOS grâce à Jamf
ms.author: brianalt
author: dan-wesley
manager: laurawi
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer les paramètres de stratégie MicrosoftEdge sur les appareils Mac grâce à Jamf
ms.openlocfilehash: 336bdfed2c53811615b0183dc5ca7db916cd7428
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979668"
---
# Configurer les paramètres de stratégie MicrosoftEdge sur macOS grâce à Jamf

Cet article explique la configuration de paramètres de stratégie sur macOS à l’aide d’un fichier de manifeste de stratégie Microsoft Edge sur Jamf Pro10.19.

Vous pouvez également configurer les paramètres de stratégies MicrosoftEdge sur macOS à l’aide d’un fichier de liste de propriétés (.plist). Pour plus d’informations, voir [Configuration pour macOS à l’aide d’un fichier .plist](configure-microsoft-edge-on-mac.md).


## Conditions préalables

Le logiciel suivant est nécessaire:

- Microsoft Edge Stable canal8.1
- Fichier de modèles de stratégie, version81.0.416.3
- Jamf Pro version10.19

## À propos de l’application Jamf Pro & du menu Paramètres personnalisés

Avant la publication de Jamf Pro10.18, la gestion d’Office365 impliquait la création manuelle d’un fichier .plist. Le flux de travail était fastidieux et nécessitait une solide formation technique. Jamf Pro10.18 éliminait ces obstacles en rationalisant le processus de configuration. Cependant, les administrateurs informatiques pouvaient seulement utiliser cette nouvelle interface utilisateur pour des applications spécifiques et des domaines de préférence spécifiés par Jamf.

Avec Jamf Pro10.19, un utilisateur peut télécharger un manifeste JSON en tant que «schéma personnalisé» pour cibler tout domaine de préférence, et l’interface utilisateur graphique est générée à partir de ce manifeste. Le schéma personnalisé créé respecte la spécification de schéma JSON.

Pour plus d’informations, voir [Profils de configuration d’ordinateur](https://jamf.it/computer-configuration-profiles) dans le Guide de l’administrateur Jamf Pro.

## Obtenir le manifeste de stratégie pour une version spécifique de Microsoft Edge

Pour obtenir le manifeste de stratégie:

- Accédez à la [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise).
- Dans la liste déroulante Canal/Version, sélectionnez **tout canal avec la version 81 ou ultérieure.***.
- Dans la liste déroulante Build, sélectionnez toute **version 81 ou ultérieure.***.
- Cliquez sur OBTENIR DES FICHIERS DE STRATÉGIE pour télécharger notre ensemble de modèles de stratégie.

  > [!NOTE]
  > L'ensemble de modèles de stratégie est signé en tant que fichier CAB. Vous devez utiliser un outil tiers, tel que Unarchiver, pour ouvrir le fichier sur macOS.

Une fois le fichier CAB décompressé, décompressez le fichier ZIP et accédez au répertoire «mac» de niveau supérieur. Le manifeste appelé «policy_manifest.json» figure dans ce répertoire.

Ce manifeste est publié dans chaque ensemble de stratégies à compter de la build81.0.416.3. Si vous souhaitez tester des stratégies dans le canal de développement, vous pouvez prendre le manifeste associé à chaque publication de développement et le tester dans Jamf Pro.  

## Utilisation du manifeste de stratégie dans Jamf Pro

Utilisez la procédure suivante pour télécharger le manifeste de stratégie dans Jamf Pro et créer un profil de stratégie pour macOS.

1. Connectez-vous à Jamf.
2. Sélectionnez l'onglet **Ordinateur**.
3. Sous **Gestion de contenu**, sélectionnez **Profils de configuration**.
4. Sur la page **Profils de configuration**, cliquez sur **+ Nouveau**.

   ![Ajout d'un nouveau profil dans Jamf](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles.png)

5. Sur **Nouveau profil de configuration macOS**>**Options**, sélectionnez **Application & paramètres personnalisés**.
6. Dans la fenêtre contextuelle **Application & paramètres personnalisés**, cliquez sur **Configurer**.

   ![Configurer les Application et paramètres personnalisés](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom.png)

7. Dans la section **Application & paramètres personnalisés**, configurez les valeurs affichées dans la capture d’écran ci-après.

   ![Source du profil et schéma personnalisé](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-schema.png)

   - Pour la **Méthode de création**, sélectionnez **Configurer les paramètres**.
   - Pour la **Source**, sélectionnez **Schéma personnalisé**.
   - Pour le **Domaine de préférence**, indiquez votre nom de domaine. Cet exemple utilise *com.microsoft.Edge* en tant que domaine.
   - Pour le **Schéma personnalisé**, collez le contenu du fichier manifeste «policy_manifest.json».
   - Cliquez sur **Save**.

8. Une fois le profil enregistré, Jamf affiche la section **Général** présentée dans la capture d’écran suivante.

   ![Configuration de la section Général](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-general-setting.png)

   - Spécifiez un **Nom** d'affichage pour le profil et une **Description**.
   - Conservez le paramètre par défaut pour la **Catégorie**, c'est-à-dire **Aucune**.
   - Pour la **Méthode de distribution**, les options sont **Installer automatiquement** ou **Rendre disponible dans le libre-service**.
   - Pour le **Niveau**, les options sont **Niveau utilisateur** ou **Niveau ordinateur**.
   - Cliquez sur **Save**.

9. Après enregistrement de la section Général, Jamf affiche le profil de configuration «Canal Bêta Microsoft Edge» configuré pour notre exemple. Dans la capture d’écran suivante, veuillez prendre note que vous pouvez continuer à travailler sur le profil en cliquant sur **Modifier** ou si vous avez terminé, cliquez sur **Terminé**.

   ![Nouveau profil de configuration avec options](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel.png)

   > [!NOTE]
   > Vous pouvez modifier ce profil après son enregistrement et lors d'une autre session Jamf. Par exemple, vous pouvez décider de modifier la Méthode de distribution pour la Rendre disponible dans le libre-service.

   Pour effectuer un suivi des modifications sur le canal Microsoft Edge Stable ou le supprimer, sélectionnez le nom du profil, tel qu'illustré dans la capture d’écran Profils de configuration suivante.

   ![Liste Profils de configuration](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel-done.png)

Une fois le nouveau profil de configuration créé, vous devez configurer l’**Étendue** du profil.

### Configuration de l'étendue

1. Pour les **Cibles**, fournissez les paramètres minimaux suivants:

   - ORDINATEURS CIBLES. Les options sont: Ordinateurs spécifiques ou Tous les ordinateurs.
   - UTILISATEURS CIBLES. Les options sont: Utilisateurs spécifiques ou Tous les utilisateurs.
   - Cliquez sur **Save**.
2. Pour les **Limitations**, conservez le paramètre par défaut, à savoir Aucune. Cliquez sur **Annuler**.
3. Pour les **Exclusions**, conservez le paramètre par défaut, à savoir Aucune. Cliquez sur **Annuler**.

## Forum Aux Questions

### MicrosoftEdge peut-il être configuré pour utiliser les préférences principales?

Oui, vous pouvez configurer MicrosoftEdge pour qu’il utilise un fichier de préférences principales.

Un fichier de préférences principales vous permet de configurer les paramètres par défaut d’un profil utilisateur de navigateur lors du déploiement de MicrosoftEdge. Vous pouvez également utiliser un fichier de préférences principales pour appliquer des paramètres sur des ordinateurs qui ne sont pas gérés par un système de gestion des périphériques. Ces paramètres sont appliqués au profil de l’utilisateur la première fois que l’utilisateur exécute le navigateur. Une fois que l’utilisateur a exécuté le navigateur, les modifications apportées au fichier de préférences principales ne sont pas appliquées. Un utilisateur peut modifier les paramètres à partir des préférences principales dans le navigateur. Si vous souhaitez rendre un paramètre obligatoire ou modifier un paramètre après la première exécution du navigateur, vous devez utiliser une stratégie.

Un fichier de préférences principales vous permet de personnaliser de nombreux paramètres et préférences pour le navigateur, y compris ceux partagés avec d’autres navigateurs basés Chromium et spécifiques à MicrosoftEdge.  Les préférences liées à la stratégie peuvent être configurées à l’aide du fichier de préférences principales. Dans les cas où une stratégie est définie et qu’un jeu de préférences principales correspondant est défini, le paramètre de stratégie est prioritaire.

> [!IMPORTANT]
> Toutes les préférences disponibles peuvent ne pas être cohérentes avec la terminologie et les conventions d’affectation de noms de MicrosoftEdge.  Il n’est pas garanti que ces préférences continuent de fonctionner comme prévu dans les prochaines versions. Les préférences peuvent être modifiées ou ignorées dans les versions ultérieures.

Un fichier de préférences principales est un fichier texte mis en forme à l’aide du balisage JSON. Ce fichier doit être ajouté au même répertoire que le msedge.exe exécutable. Pour les déploiements à l’échelle du système sur macOS, c’est généralement: «*~/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*» ou «*/Library/Microsoft/Microsoft Edge Master Preferences*».

## Articles associés

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Configurer pour macOS avec Intune](configure-microsoft-edge-on-mac.md)
- [Configurer pour Windows](configure-microsoft-edge.md)
- [Configurer pour Windows avec Intune](configure-edge-with-intune.md)
