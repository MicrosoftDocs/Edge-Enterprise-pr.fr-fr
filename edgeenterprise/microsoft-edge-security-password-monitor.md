---
title: Surveillance de mot de passe activée automatiquement pour les utilisateurs
ms.author: supalsul
author: AndreLBarr
manager: tulasim
ms.date: 07/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Surveillance de mot de passe activée automatiquement pour les utilisateurs
ms.openlocfilehash: bd1fe390b972c66cd9b4c20ab3a9fabde76c7e03
ms.sourcegitcommit: 65530c0bad3097a510f507503eae9c5c67db47a0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "11643881"
---
# <a name="password-monitor-auto-enabled-for-users"></a>Surveillance de mot de passe activée automatiquement pour les utilisateurs

Cet article explique comment la Surveillance de mot de passe dans Microsoft Edge sera activée pour certains utilisateurs et indique aux administrateurs les étapes à suivre pour contrôler la façon dont la surveillance est activée.

> [!NOTE]
> Cet article s’applique à Microsoft Edge version 88 ou ultérieure.

## <a name="introduction-benefits-and-availability"></a>Introduction, avantages et disponibilité

La Surveillance de mot de passe permet aux utilisateurs de Microsoft Edge de protéger leurs comptes en ligne en les informant si l’un de leurs mots de passe a été trouvé dans une fuite en ligne. Les fuites en ligne ou les violations de données se produisent lorsque des acteurs malveillants volent des données à partir d’applications ou de sites web tiers. Pour en savoir plus, voir la [Surveillance de mot de passe : protection des mots de passe dans le livre Microsoft Edge](https://www.microsoft.com/research/blog/password-monitor-safeguarding-passwords-in-microsoft-edge/) sur le blog Microsoft Research.

### <a name="benefits"></a>Avantages

Étant donné la fréquence et l’étendue de ces attaques en ligne, avoir ce type de protection est devenu nécessaire pour tout le monde. Microsoft Edge a la possibilité intégrée de vérifier en toute sécurité les mots de passe enregistrés d’un utilisateur par rapport aux mots de passe connus comme compromis et les avertit si une correspondance est trouvée.  

## <a name="configure-group-policy-for-password-monitor"></a>Configurer la stratégie de groupe pour la Surveillance de mot de passe

Cette fonctionnalité est contrôlée via la stratégie de groupe [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed).

Une fois la stratégie activée, les utilisateurs doivent toujours donner leur consentement pour activer la fonctionnalité. Le consentement est obligatoire, car la fonctionnalité contient les données sensibles et personnelles de l’utilisateur (mots de passe). Si la fonctionnalité est désactivée à l’aide de la stratégie de groupe, les utilisateurs ne peuvent pas remplacer ce paramètre.  

## <a name="enabling-password-monitor-for-users"></a>Activation de la Surveillance de mot de passe pour les utilisateurs

Une fois la stratégie de la surveillance de mot de passe activée, il existe différentes façons de mettre cette fonctionnalité à la disposition des utilisateurs.

- Activation automatique. Les utilisateurs qui sont connectés à l’aide de leur compte professionnel (Active Directory ou Azure Active Directory) et qui synchronisent leurs mots de passe seront automatiquement activés pour cette fonctionnalité. Ils voient la notification dans la capture d’écran suivante les informant que la fonctionnalité est activée.

  :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-enabled-notice.png" alt-text="Avis activé pour la Surveillance de mot de passe":::

-  Obtention d’un consentement explicite. Les utilisateurs qui n’ont pas la synchronisation des mots de passe sont invités à activer la Surveillance de mot de passe. Ils sont invités lorsque les actions suivantes se produisent :
   - Lorsqu’un utilisateur sauvegarde un nouveau mot de passe.
 
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-save-pw-prompt.png" alt-text="Invite à enregistrer le mot de passe":::

   - Lorsqu’un utilisateur s’est connecté au navigateur à l’aide d’un mot de passe enregistré.
  
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-after-signin.png" alt-text="Invite de confirmation après la signature":::
   
- Activation directe. Les utilisateurs peuvent utiliser **Paramètres** > **Mot de passe** à tout moment et activer ou désactiver la fonctionnalité.

## <a name="user-scenarios-with-password-monitor-auto-enabled"></a>Scénarios utilisateur avec la Surveillance de mot de passe activée automatiquement

Le tableau suivant présente les scénarios dans lequel la Surveillance de mot de passe est activée automatiquement et comment elle fonctionne sur les appareils des utilisateurs.

| Scénario | Conditions de base | Impact |
|--|--|--|
| 1 avec synchronisation sur | Synchronisation ACTIVÉ<br>Fonctionnalité activée précédemment : Non<br>Réponse à l’interface utilisateur de consentement : Aucune | Fonctionnalité activée par défaut et une bulle d’avis s’affiche 2 minutes après le démarrage du navigateur.<br>- Si la synchronisation est désactivée après cela, la fonctionnalité est désactivée.<br>- Fonctionnalité désactivée avant la modification de la synchronisation, la synchronisation n’affectera plus la fonctionnalité.   |
| 2 avec synchronisation sur | Synchronisation ACTIVÉ<br>Fonctionnalité activée précédemment : Oui<br>Réponse à l’interface utilisateur de consentement : Aucune | La fonctionnalité reste identique au choix de l’utilisateur.  La bulle d’avis n’est pas affichée et il n’y a aucune incidence sur la modification de la synchronisation sur la valeur de la fonctionnalité.|
| 3 avec synchronisation désactivée | Synchroniser Désactivé<br>Fonctionnalité activée précédemment : Non<br>Réponse à l’interface utilisateur de consentement : Aucune | La synchronisation est désactivée et la fonctionnalité reste désactivée.<br>- À tout moment après cela, si l’utilisateur active la synchronisation sans modifier la fonctionnalité : la fonctionnalité est activée et la notification d’activer automatiquement s’affiche 2 minutes après l’activation. <br> - Si la synchronisation est désactivée à nouveau, la fonctionnalité est désactivée <br>- Si la fonctionnalité est modifiée avant d’activer la synchronisation, la synchronisation n’affecte plus la Surveillance de mot de passe.  |  
| 4 avec synchronisation désactivée | Synchronisation DÉSACTIVÉ<br>Fonctionnalité activée précédemment : Oui<br>Réponse à l’interface utilisateur de consentement : Aucune | La fonctionnalité reste la même que le choix de l’utilisateur, la bulle de notification n’est pas affichée et il n’y a aucun effet de changement de synchronisation sur la valeur de la fonctionnalité.  |

En outre, si un utilisateur est connecté à l’aide d’un compte professionnel restreint via des stratégies pour l’une des fonctionnalités suivantes, la fonctionnalité ne sera PAS activée automatiquement pour lui :

- Le moniteur de mot de passe est désactivé  
- La synchronisation des mots de passe est désactivée
- Le partage de données avec des serveurs Microsoft est désactivé

## <a name="frequently-asked-questions"></a>Forum Aux Questions

### <a name="how-can-password-monitor-be-disabled-for-my-organization"></a>Comment la Surveillance de mot de passe peut-elle être désactivée pour mon organisation ?

Vous pouvez désactiver la Surveillance de mot de passe pour votre organisation en :
- Utilisant la stratégie de groupe PasswordMonitorAllowed.
- Arrêtant la synchronisation et l’envoi des données aux serveurs Microsoft.

  > [!NOTE]
  > La Surveillance de mot de passe peut fonctionner même si la synchronisation des mots de passe est désactivée, tant que l’utilisateur a donné son consentement explicite pour activer la fonctionnalité ou l’avoir lui-même via les paramètres.

### <a name="what-happens-if-a-user-for-whom-the-feature-has-been-auto-enabled-turns-password-monitor-off-via-settings"></a>Que se passe-t-il si un utilisateur pour lequel la fonctionnalité a été activée automatiquement, active le moniteur de mot de passe via paramètres ?

Le paramètre utilisateur est honoré et la fonctionnalité reste désactivée pour cet utilisateur. Toutefois, il se peut qu’une boîte de dialogue de consentement s’affiche à nouveau au cas où il n’a jamais répondu à l’invite de consentement.

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)