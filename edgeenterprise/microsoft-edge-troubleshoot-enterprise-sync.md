---
title: Diagnostiquer et résoudre les problèmes de synchronisation de MicrosoftEdge
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Conseils et outils qu’un administrateur MicrosoftEdge peut utiliser pour résoudre les problèmes courants de synchronisation d’entreprise
ms.openlocfilehash: 49fb0c5fc555e4f7ad4c728477387e931a5fbb5f
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447158"
---
# <a name="diagnose-and-fix-microsoft-edge-sync-issues"></a>Diagnostiquer et résoudre les problèmes de synchronisation de MicrosoftEdge

Cet article fournit des conseils de dépannage pour les problèmes de synchronisation les plus couramment rencontrés dans un environnement Azure Active Directory (Azure AD). Il inclut également les outils recommandés pour collecter les journaux nécessaires à la résolution d’un problème de synchronisation.

Si un utilisateur rencontre un problème de synchronisation des données de navigateur sur ses appareils, il peut essayer de [réinitialiser la synchronisation](edge-learnmore-reset-data-in-cloud.md). Si cela ne fonctionne pas, les administrateurs ou le personnel de support technique peuvent utiliser les instructions suivantes pour résoudre un problème de synchronisation.

> [!NOTE]
> S’applique à MicrosoftEdge version77 ou ultérieure sauf indication contraire.

## <a name="identity-issues-versus-sync-issues"></a>Problèmes d’identité et problèmes de synchronisation

Avant de commencer, il est important de comprendre la différence entre les problèmes d’identité et les problèmes de synchronisation. Un cas d’utilisation populaire pour la maintenance de l’identité de l’utilisateur dans le navigateur consiste à prendre en charge la synchronisation. Pour cette raison, les problèmes d’identité sont souvent confondus avec les problèmes de synchronisation. Comprenez la différence entre les problèmes d’identité et de synchronisation avant de commencer à résoudre les problèmes de synchronisation.

Avant de traiter un problème comme un problème de synchronisation, vérifiez si l’utilisateur est signé dans le navigateur avec un compte valide.

La capture d’écran suivante montre un exemple d’erreur d’identité. L’erreur est «**Dernière erreur de jeton, EDGE_AUTH_ERROR: 3, 54, 3ea**», qui se trouve dans *edge://sync-internals* sous **Informations d’identification**:

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Dernière erreur de jeton EDGE_AUTH_ERROR: 3,54, 3ea":::

## <a name="common-sync-issues"></a>Problèmes de synchronisation courants

### <a name="issue-cant-access-m365-or-azure-information-protection-subscription"></a>Problème: Ne peut pas accéder à l’abonnement M365 ou Azure Information Protection

Avez-vous un ancien abonnement M365 ou Azure Information Protection (AIP) qui a expiré que vous avez ensuite remplacé par un nouvel abonnement? Si c’est le cas, l’ID de locataire a changé et les données de service doivent être réinitialisées. Consultez les instructions de réinitialisation des données dans l’erreur **de chiffrement rencontrée**.

### <a name="issue-sync-is-not-available-for-this-account"></a>Problème: « La synchronisation n’est pas disponible pour ce compte. »

Si cette erreur est rencontrée pour un compte Azure Active Directory, ou si DISABLED_BY_ADMIN apparaît dans *edge://sync-internals*, suivez les étapes de la procédure suivante de manière séquentielle jusqu’à ce que le problème soit résolu.

> [!NOTE]
> Étant donné que la source de cette erreur nécessite généralement une modification de configuration dans un client Azure Active Directory, ces étapes de dépannage ne peuvent être effectuées que par un administrateur client et non par les utilisateurs finaux.

1. Vérifiez que le client d’entreprise dispose d’un abonnement M365 pris en charge. La liste actuelle des types d’abonnement disponibles [est fournie ici](/azure/information-protection/activate-office365). Si le client n’a pas d’abonnement pris en charge, il peut acheter Azure Information Protection séparément ou mettre à niveau vers l’un des abonnements pris en charge.
2. Si un abonnement pris en charge est disponible, vérifiez que le client dispose d’Azure Information Protection (AIP). Les instructions pour vérifier l’état d’Azure Information Protection et, si nécessaire, l’activation d’Azure Information Protection se trouvent [ici](/azure/information-protection/activate-office365).
3. Si l’étape2 indique qu’Azure Information Protection est actif mais que la synchronisation ne fonctionne toujours pas, activez Enterprise State Roaming (ESR). Les instructions d’activation du système ESR sont [ici](/azure/active-directory/devices/enterprise-state-roaming-enable). Notez qu’Enterprise State Roaming n’a pas besoin de rester en place. Vous pouvez désactiver Enterprise State Roaming si cette étape résout le problème.
4. Confirmez qu’Azure Information Protection n’est pas étendue via une stratégie d’intégration. Vous pouvez utiliser l’applet [Get-AadrmOnboardingControlPolicy](/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps) de PowerShell pour voir si l’étendue est activée. Les deux exemples suivants illustrent une configuration non étendue et une configuration étendue à un groupe de sécurité spécifique.

   ```powershell
    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False 
   ```

   ```powershell

    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False f1488a05-8196-40a6-9483-524948b90282   All
   ```

   Si l’étendue est activée, l’utilisateur affecté doit être ajouté au groupe de sécurité pour l’étendue ou l’étendue doit être supprimée. Dans l’exemple ci-dessous, l’intégration a étendu Azure Information Protection au groupe de sécurité indiqué et l’étendue doit être supprimée avec l’applet [PowerShell Set-AadrmOnboardingControlPolicy.](/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps)

5. Confirmez que IPCv3Service est activé dans le client. [L’applet PowerShell Get-AadrmConfiguration](/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) affiche l’état du service.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Vérifiez si IPCv3Service est activé.":::

6. Si le problème n’est pas résolu, contactez le [support Microsoft Edge](https://www.microsoftedgeinsider.com/support).

### <a name="issue-stuck-at-setting-up-sync-or-couldnt-connect-to-the-sync-server-retrying"></a>Problème : bloqué sur «Configuration de la synchronisation...» ou «Impossible de se connecter au serveur de synchronisation. Nouvelle tentative...»

1. Essayez de vous déconnecter, puis de vous connecter.
2. Go to *edge://sync-internals*. Si, sous la section «**Informations sur le type**», l’erreur suivante est présente, ignorez alors le problème suivant, **Une erreur de chiffrement s’est produite**.

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. Essayez d’envoyer un test ping au point de terminaison du serveur. Le point de terminaison du serveur pour un client est disponible *dans edge://sync-internals*. La capture d’écran suivante montre les informations du point de terminaison sous **Informations sur l’environnement**.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="Informations sur le point de terminaison":::

4. Si le point de terminaison du serveur est vide ou si le serveur ne peut pas être ping et qu’un pare-feu est présent dans l’environnement, confirmez que les points de terminaison de service nécessaires sont disponibles pour l’ordinateur client.

   - Points de terminaison du service de synchronisation MicrosoftEdge:
     - [https://edge-enterprise.activity.windows.com](https://edge-enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - Points de terminaison Azure Information Protection:
      - [https://api.aadrm.com](https://api.aadrm.com) (pour la plupart des locataires)
      - [https://api.aadrm.de](https://api.aadrm.de) (pour les locataires en Allemagne)
      - [https://api.aadrm.cn](https://api.aadrm.cn) (pour les locataires en Chine)
   - [Points de terminaison du service de notification Windows](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).

5. Si le problème n’est toujours pas résolu, contactez le [support Microsoft Edge](https://www.microsoftedgeinsider.com/support).

### <a name="issue-cryptographer-error-encountered"></a>Problème: erreur de chiffrement rencontrée

Cette erreur est visible sous **Type d’informations** dans *edge://sync-internals* et peut signifier que les données côté service de l’utilisateur doivent être réinitialisées. L’exemple suivant montre un message d’erreur de chiffrement:
<br>«Error:GenerateCryptoErrorsForTypes@.. /.. /components/sync/driver/data_type_manager_impl.cc:42, une erreur de chiffrement s’est produite».

1. Redémarrez MicrosoftEdge et accédez à *edge://sync-internals*, puis consultez la section «**État de la clé de compte AAD**»
   - «Réussite» dans «Dernier résultat MIP»: l’erreur de chiffrement signifie que les données du serveur peuvent être chiffrées avec une clé perdue. La réinitialisation des données est nécessaire pour reprendre la synchronisation.
   - «Aucune autorisation» dans «Résultat du dernier MIP»: il est possible qu’il soit dû à une modification d’AzureAD ou à des modifications d’abonnement client. La réinitialisation des données est nécessaire pour reprendre la synchronisation.
   - D’autres erreurs peuvent signifier des problèmes de configuration du serveur.
2. Si la réinitialisation des données est nécessaire, voir [Réinitialiser les données Microsoft Edge dans le cloud](edge-learnmore-reset-data-in-cloud.md).

### <a name="issue-sync-has-been-turned-off-by-your-administrator"></a>Problème: «La synchronisation a été désactivée par votre administrateur».

Assurez-vous que la [stratégie SyncDisabled](./microsoft-edge-policies.md#syncdisabled) n’est pas définie.

## <a name="see-also"></a>Voir également

- [Synchronisation de MicrosoftEdge Entreprise](microsoft-edge-enterprise-sync.md)
- [MicrosoftEdge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)