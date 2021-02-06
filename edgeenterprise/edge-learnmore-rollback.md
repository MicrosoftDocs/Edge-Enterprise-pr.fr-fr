---
title: Restauration Microsoft Edge pour les entreprises
ms.author: v-danwes
author: dan-wesley
manager: srugh
ms.date: 02/04/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Comment restaurer Microsoft Edge à une version antérieure
ms.openlocfilehash: 2059ea04bf8ec3a03266fe95599ea3b515b78c12
ms.sourcegitcommit: c290b0b0fa6b7d7f94dcdfdda91302da733326ec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314567"
---
# Comment restaurer Microsoft Edge à une version antérieure

Cet article explique comment revenir à une version antérieure de Microsoft Edge à l’aide de la fonctionnalité de restauration. Pour en savoir plus sur cette fonctionnalité, regardez [la vidéo : Retour en arrière de la version Microsoft Edge](microsoft-edge-video-version-rollback.md).

>[!NOTE]
>Cet article concerne MicrosoftEdge version86 ou ultérieure.

## Présentation de la restauration

La restauration vous permet de remplacer la version de votre navigateur Microsoft Edge par une version antérieure. Cette fonctionnalité est conçue comme filet de sécurité pour les entreprises qui déploient Microsoft Edge. Elle offre la résolution de problèmes avec Microsoft Edge. Les avantages de la restauration sont la capacité de revenir facilement et rapidement à une version antérieure du navigateur. La restauration réduit l’impact potentiel qu’un problème lié à Microsoft Edge a sur les activités de l’entreprise.

## Avant de commencer

Il est important de comprendre comment la fonctionnalité de restauration est installée dans un environnement Microsoft Edge. Vous pouvez déployer la restauration à l’aide de deux méthodes différentes: manuellement avec un MSI ou en utilisant la méthode de groupe et de mise à jour de Microsoft Edge.  Nous encourageons également l’utilisation d’une sélection de méthodes de groupe pour un déploiement plus fluide.

### Recommandations

La fonctionnalité de restauration est un correctif temporaire pour résoudre les problèmes que vous pourriez rencontrer dans une mise à jour du navigateur Microsoft Edge. Nous recommandons aux utilisateurs d’installer la dernière version du navigateur Microsoft Edge afin d’utiliser la protection offerte par les dernières mises à jour de sécurité. La restauration à une version antérieure présente des risques d’exposition aux problèmes de sécurité connus.

Avant de restaurer temporairement la version de votre navigateur, nous vous recommandons fortement d’activer la synchronisation pour tous les utilisateurs de votre organisation également. Si vous n’activez pas la synchronisation, vous risquez de perdre permanemment les données de navigation. Pour plus d’informations sur la Synchronisation, voir [Synchronisation Microsoft Edge](microsoft-edge-enterprise-sync.md).

> [!CAUTION]
> Utilisez la restauration seulement lorsque cela s’avère nécessaire, il y a toujours the risque de perte de données.

## Activer la restauration manuelle avec un MSI

Procéder comme suit pour restaurer manuellement avec un fichier MSI.

1. Désactiver les mises à jour de Microsoft Edge.

   > [!NOTE]
   > Nous vous recommandons d’installer les modèles d’administration les plus courants. Pour plus d’informations, voir[ téléchargez et installez le modèle d’administration de MicrosoftEdge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).

   - Ouvrez l’éditeur de la méthode de groupe locale, puis accédez à *Configuration ordinateur > modèles d’administration>Mise à jour de Microsoft Edge> Applications>Microsoft Edge >*.
   - Sélectionnez Remplacement de la méthode de mise à jour puis sélectionnez **activé**.
   - Sous **options**, sélectionnez **mise à jour désactivée** dans la liste déroulante des méthodes.

2. Obtenir le MSI.

   - Téléchargez le MSI de la version que vous souhaitez restaurer [à partir d’ici](https://www.microsoft.com/edge/business/download).
   - Enregistrez le MSI sur le bureau de votre ordinateur.

3. Exécutez la commande restaurer.

   - Ouvrez l’invite de commandes Windows avec **exécuter en tant qu’administrateur**.
   - Tapez la commande suivante, où: *C:\Utilisateurs\nom d’utilisateur\Bureau\test* est le chemin d’accès au MSI que vous avez téléchargé et nom du fichier est le nom du .fichier msi:<br>
 `C:\Users\username\Desktop\test>msiexec /I FileName.msi /qn ALLOWDOWNGRADE=1`<br>
     > [!NOTE]
     > Pour plus d’informations sur msiexec, voir [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).
   - Fermez et rouvrez Microsoft Edge pour vérifier que la restauration a fonctionné. Sous **paramètres et plus** (ALT + F), accédez à paramètres puis sélectionnez sur Microsoft Edge.

## Activer la restauration avec la mise à jour de Microsoft Edge et de la méthode de groupe

Procédez comme suit pour activer la restauration avec la mise à jour de Microsoft Edge et de la méthode de groupe.

1. Ouvrez l’éditeur de la méthode de groupe locale, puis accédez à *Configuration ordinateur > modèles d’administration>Mise à jour de Microsoft Edge> Applications>Microsoft Edge >*.
2. Sélectionnez restaurer la version cible puis sélectionnez **activé**.
3. Sélectionnez **Remplacement de la version cible** et sélectionnez la version du navigateur que vous souhaitez restaurer.
4. Sélectionnez Remplacement de la méthode de mise à jour puis sélectionnez **activé**. Sous **options**, sélectionnez l’une des options suivantes dans la liste déroulante de méthodes (à l’exception de **mise à jour désactivée**):

   - Autoriser toujours les mises à jour
   - Mises à jour silencieuses automatiques uniquement

     > [!NOTE]
     > Pour forcer une mise à jour de stratégie de groupe, tapez `gpupdate /force` dans l’invite de commande de l’administrateur Windows (Exécuter en tant qu’administrateur).

5. Cliquez sur **OK** pour enregistrer le paramètre. La restauration aura lieu la prochaine fois que Microsoft Edge Update recherchera une mise à jour. Si vous souhaitez que la mise à jour se produise plus tôt, vous pouvez modifier l’intervalle d’interrogation de MicrosoftEdgeUpdate ou activer la restauration avec un MSI.

### Erreurs de restauration courantes

Les erreurs suivantes peuvent empêcher la restauration:

- L’entrée est une version cible non prise en charge
- L’entrée est une version cible inexistante
- La mise en forme de l’entrée est incorrecte

### Méthodes de groupe recommandées

Les méthodes de groupe et les paramètres suivants sont fortement recommandés pour l’utilisation de la restauration.

#### Méthodes de groupe de synchronisation

- ForceSync. Activez ForceSync. Cette méthode force l’activation de la synchronisation sur tous les utilisateurs Azure Active Directory (Azure AD). Cette méthode est applicable uniquement aux versions 86 et ultérieures de Microsoft Edge.
- La fonctionnalité *configurer la liste des types exclus de la méthode de synchronisation* permet aux administrateurs de contrôler les données qui peuvent être synchronisées par les utilisateurs.

#### Les méthodes de groupe de redémarrage du navigateur

Nous vous recommandons de forcer un redémarrage sur les utilisateurs après l’activation de la restauration.

- Activer *Avertir un utilisateur qu'un redémarrage du navigateur est recommandé ou requis pour les mises à jour en attente*. Sous options, sélectionnez **requis**.
- Activez *Définir l’intervalle de temps pour les notifications de mise à jour* puis configurez le temps souhaité en millisecondes.

## Capture instantanée

Une capture instantanée est une copie estampillée du dossier des données utilisateur. Lors d’une mise à niveau d’une version, une capture instantanée de la version précédente est créée et stockée dans le dossier des captures instantanées. Une fois la restauration effectuée, une capture instantanée correspondant à la version est copiée dans le nouveau dossier des données utilisateur et est supprimée du dossier des captures instantanées. Si aucune capture instantanée correspondant à la version n’est disponible lors du retour à la version antérieure, la restauration s’appuiera sur la synchronisation pour remplir les données utilisateur dans la nouvelle version de MicrosoftEdge.

La stratégie de groupe [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userdatasnapshotretentionlimit) vous permet de définir une limite pour le nombre d’instantanés qui peuvent être conservés à tout moment. Par défaut, trois captures instantanées sont conservées. Vous pouvez configurer cette stratégie pour conserver de 0à5captures instantanées.

## Forum Aux Questions

### Restauration manuelle de MSI

#### Quelles sont les défaillances MSI génériques qui peuvent se produire?

1. Si la méthode de groupe installer mise à jour est désactivée, la restauration sera impossible.

   - Pour utiliser la restauration, assurez-vous que l’option Installer est configurée en mode **activé**. Lorsque cette méthode est désactivée, les canaux Microsoft Edge ne sont pas installés. Pour plus d'informations, consultez [Installer](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).

2. Si les mises à jour de veille n’apparaissent pas, les installations Microsoft Edge seront bloquées, sauf si *l’option Autoriser l’ Utilisation du navigateur Côte à Côte de Microsoft Edge * est activée.

   - Pour les versions 1903 et 1909 de Windows: Si votre dernière mise à jour est antérieure au mois d’octobre 2019, vous pouvez rencontrer ce problème.
   - Pour les versions 1709, 1803 et 1809 de Windows: Si votre dernière mise à jour est antérieure au mois d’octobre 2019, vous pouvez rencontrer ce problème.<br>
Pour plus d’informations, consultez [Mises à jour Windows pour prendre en charge la prochaine version de MicrosoftEdge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)

#### Le message d’erreur suivant s’est affiché après l’utilisation de l’invite de commandes et la restauration n’a pas eu lieu. Qu'est-ce qui ne va pas?

![Message de l’état de restauration](./media/edge-learnmore-rollback/edge-rollback-cmd-flag-error.png)

*Autoriser le passage à une version antérieure= 1* n’a pas été exécuté.

### Mise à jour de Microsoft Edge et restauration de la Méthode de Groupe

#### J’ai défini *restaurer à la version cible*, activé *Remplacement de la méthode de mise à jour*, entré ma version de navigateur souhaitée pour *Remplacement de la version cible*, mais la version du navigateur n’était pas celle que je souhaitais. Qu'est-ce qui ne va pas?

Voici quelques erreurs courantes qui empêchent la restauration:

- Si la restauration de la version cible n’est pas activée, la restauration ne sera pas exécutée.
- Le paramètre remplacer la version cible présente l’un des problèmes suivants:

  - Le remplacement de la version cible est défini pour une version cible non prise en charge.
  - Le remplacement de la version cible est défini pour une version cible non existante.
  - La mise en forme du remplacement de la version cible est incorrecte.

- Si le remplacement de la stratégie de mise à jour est défini sur «Mises à jour désactivées», MicrosoftEdgeUpdate n’accepte aucune mise à jour et la restauration n’est pas exécutée.

### J’ai défini toutes les méthodes de groupe correctement, mais la restauration n’a pas été exécutée. que se passe-t-il?

Microsoft Edge Update n’a pas encore exécuté de recherche de mises à jour. Définir par défaut, la mise à jour automatique de recherche des mises à jour toutes les 10heures. Vous pouvez résoudre ce problème en modifiant l’intervalle d’interrogation de MicrosoftEdgeUpdate avec la stratégie de groupe de remplacement de période de vérification des mises à jour automatiques. Pour plus d’informations, consultez la méthode [ Des Minutes de la Période de Recherche des Mises à jour](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes) Automatiques.

### En tant qu’administrateur informatique, j’ai suivi toutes les étapes de la restauration correctement. Seule une partie de mon groupe d’utilisateurs a été restaurée. Pourquoi les autres utilisateurs n’ont pas encore été restaurés?

Le paramètre de la méthode de groupe n’a pas encore été synchronisé avec tous les clients. Lorsque les administrateurs définissent une méthode de groupe, les clients ne reçoivent pas ces paramètres instantanément. Vous pouvez [Forcer une actualisation de la stratégie de groupe à distance](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj134201(v=ws.11)).

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Vidéo: Restauration de version de Microsoft Edge](microsoft-edge-video-version-rollback.md)
