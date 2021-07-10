---
title: Réinitialisation de données Microsoft Edge
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Comment réinitialiser des données Microsoft Edge dans le cloud
ms.openlocfilehash: 19ee60926e36371bd710937fcafc43de7ea035f4
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642040"
---
# <a name="reset-microsoft-edge-data-in-the-cloud"></a>Réinitialisation de données Microsoft Edge dans le cloud

Cet article décrit la procédure de réinitialisation de vos données Microsoft Edge dans le cloud.

> [!NOTE]
> Cet article s’applique à MicrosoftEdge version88 ou ultérieure, sauf mention contraire.

> [!NOTE]
> Si votre locataire se trouve dans un environnement GCC Mod, votre administrateur de locataire doit déposer une demande de support auprès de Microsoft pour réinitialiser vos données.

## <a name="overview"></a>Vue d'ensemble

Il peut arriver que vous souhaitiez réinitialiser vos données Microsoft Edge dans le cloud. Par exemple, vous voulez synchroniser vos données, mais Microsoft Edge signale qu’il n’est pas en mesure de synchroniser les données. Vous pouvez également faire en sorte que vos données soient supprimées du cloud de Microsoft. Dans les deux cas, Microsoft Edge vous permet d’effectuer une réinitialisation des données cloud.

## <a name="back-up-your-favorites"></a>Sauvegarder vos favoris

Avant d’effectuer une réinitialisation, nous vous recommandons de sauvegarder vos favoris. Suivez les étapes ci-dessous pour sauvegarder vos favoris.

1. Dans Microsoft Edge, sélectionnez **Paramètres et plus > Favoris > Autres options > Exporter des favoris**.
2. Choisissez le fichier dans lequel vous voulez enregistrer vos favoris. Vous pouvez taper votre propre nom de fichier ou utiliser le nom fourni par défaut par Microsoft Edge, « favorites_month_day_year.html » en tant que nom de fichier. Par exemple, « favorites_12_17_20.html ». Si vous avez besoin de restaurer vos favoris ultérieurement, vous pouvez le faire à partir de ce fichier.
3. Cliquez sur **Enregistrer**.

## <a name="perform-a-reset-to-fix-a-synchronization-problem"></a>Effectuer une réinitialisation pour résoudre un problème de synchronisation

Si Microsoft Edge signale qu’il ne peut pas synchroniser vos données et suggère de réinitialiser vos données, effectuez une réinitialisation pour résoudre le problème.

Pour effectuer une réinitialisation, procédez comme suit.

1. Tout d’abord, assurez-vous que vous êtes déconnecté de Microsoft Edge sur tous vos appareils, y compris les appareils mobiles, à l’exception de l’appareil sur lequel vous effectuez la réinitialisation. Pour vous déconnecter de Microsoft Edge, sélectionnez **Paramètres et autres > Paramètres > Se déconnecter**. Lorsque vous vous déconnectez, ne sélectionnez pas l’option d’effacement des favoris, paramètres, etc. de votre appareil local.
2. Une fois que vous êtes déconnecté de tous les autres appareils, ouvrez Microsoft Edge sur votre ordinateur de bureau. **Sélectionnez Paramètres et autres > Synchroniser > Réinitialiser la synchronisation**. Dans la boîte de dialogue qui en résulte, choisissez de reprendre la synchronisation après la réinitialisation des données, puis cliquez sur **Réinitialiser**.

## <a name="perform-a-reset-to-remove-your-data-from-microsofts-cloud"></a>Effectuer une réinitialisation pour supprimer vos données du cloud de Microsoft

Si vous voulez supprimer vos données du cloud de Microsoft, procédez comme suit pour effectuer une réinitialisation.

1. Arrêtez la synchronisation sur les appareils à l’exception de l’appareil sur lequel vous exécutez la réinitialisation.  Dans Microsoft Edge, sélectionnez **Paramètres et autres > Paramètres > Synchroniser > Désactiver la synchronisation**.  
2. Après votre arrêt de la synchronisation, sélectionnez **Paramètres et autres > Synchroniser > Réinitialiser la synchronisation**. Dans la boîte de dialogue qui en résulte, **ne sélectionnez pas** l’option pour reprendre la synchronisation après la réinitialisation des données. Sélectionnez **Réinitialiser**.

## <a name="what-to-expect-during-and-after-a-data-reset"></a>Ce à quoi vous pouvez vous attendre pendant et après la réinitialisation des données

La réinitialisation des données peut prendre de quelques secondes à quelques minutes, en fonction de la quantité de données stockées dans le cloud de Microsoft. Dans certains cas, vous verrez peut-être un message indiquant qu’une réinitialisation n’a pas pu être effectuée et une suggestion pour réinitialiser à nouveau. Le cas échéant, patientez quelques heures et réessayez de réinitialiser les données. Si vous ne parvenez toujours pas à réinitialiser vos données, contactez le support technique de Microsoft Edge.

Après la réinitialisation correcte des données, les données sont de nouveau synchronisées à partir de votre appareil si vous choisissez de reprendre la synchronisation après la réinitialisation. Vous devrez vous reconnecter sur vos autres appareils si vous voulez effectuer une synchronisation à partir de ces appareils. Toutefois, si vous n’avez pas choisi de reprendre la synchronisation, vos données Microsoft Edge sont supprimées du cloud et vos données ne seront plus synchronisées.

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Synchronisation de Microsoft Edge Entreprise](microsoft-edge-enterprise-sync.md)