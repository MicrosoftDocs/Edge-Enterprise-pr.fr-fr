---
title: Configurer et résoudre les problèmes de synchronisation de MicrosoftEdge
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 01/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer et résoudre les problèmes de synchronisation de MicrosoftEdge
ms.openlocfilehash: 36912d2fd1c33a227ce1d4b7c912f6ef1dfdcc00
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297453"
---
# Configurer et résoudre les problèmes de synchronisation de MicrosoftEdge

Cet article explique comment configurer et utiliser MicrosoftEdge pour synchroniser vos favoris, mots de passe et autres données de navigateur sur tous vos appareils connectés. Cet article fournit également des étapes de résolution des problèmes de synchronisation les plus couramment rencontrés. Il inclut également les outils recommandés pour collecter les journaux nécessaires à la résolution des problèmes.

> [!NOTE]
> S’applique à MicrosoftEdge version77 ou ultérieure sauf indication contraire.

## Vue d’ensemble

La synchronisation de MicrosoftEdge permet aux utilisateurs d’accéder à leurs données de navigation sur tous leurs appareils connectés. Les données prises en charge par la synchronisation sont les suivantes:

- Favoris
- Mots de passe
- Adresses et autres (remplissage de formulaire)
- Regroupements
- Paramètres
- Extension
- Ouvrir des onglets (disponible dans la version88 de MicrosoftEdge)
- Historique (disponible dans la version88 de MicrosoftEdge)

La fonctionnalité de synchronisation est activée après accord de l’utilisateur et les utilisateurs peuvent activer ou désactiver la synchronisation pour chacun des types de données répertoriés ci-dessus.

> [!NOTE]
> Des données de configuration et de connectivité des appareils supplémentaires (telles que le nom, la marque et le modèle de l’appareil) sont téléchargées pour prendre en charge la fonctionnalité de synchronisation.

## Conditions préalables

La synchronisation MicrosoftEdge pour les comptes Azure Active Directory (Azure AD) est disponible pour les abonnements suivants:

- Azure AD Premium (P1 ou P2)
- M365 Business Premium
- Office365E1 et versions ultérieures
- Protection d’information d’Azure (AIP) (P1 ou P2)
- Tous les abonnements à EDU (Microsoft Apps pour les étudiants ou la faculté, Exchange Online pour les étudiants ou la faculté, O365 A1 ou supérieur, M365 A1 ou supérieur, ou Azure Information Protection P1 ou P2 pour les étudiants ou la faculté)

## Stratégies de groupe de synchronisation

Vous pouvez utiliser les stratégies de groupe suivantes pour configurer et gérer la synchronisation MicrosoftEdge:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): désactive complètement la synchronisation.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): désactive l’enregistrement de l’historique de navigation et la synchronisation. Cette stratégie permet également de désactiver la synchronisation des onglets ouverts.
- [AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): si cette stratégie est définie sur Désactivé, la synchronisation de l’historique sera également désactivée.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): permet de configurer la liste des types exclus de la synchronisation.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): permet aux profils Active Directory (AD) d'utiliser le stockage sur site. Pour plus d'informations, voir [Synchronisation sur site pour les utilisateurs d'Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): activez la synchronisation par défaut et n’exigez pas le consentement de l’utilisateur pour la synchronisation.  

## Configurer la synchronisation de MicrosoftEdge

Les options de configuration pour la synchronisation de MicrosoftEdge sont disponibles via le service Azure Information Protection (AIP). Lorsque l'AIP est activé pour un locataire, tous les utilisateurs peuvent synchroniser les données Microsoft Edge, quelle que soit leur licence. Vous trouverez les instructions relatives à l’activation d’AIP [ici](https://docs.microsoft.com/azure/information-protection/activate-office365).

Pour limiter la synchronisation à certains groupes d'utilisateurs, vous pouvez activer [la politique de contrôle à l'embarquement AIP ](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) pour ces utilisateurs. Si la synchronisation n'est toujours pas disponible après s'être assuré que tous les utilisateurs nécessaires sont embarqués, assurez-vous que le service IPCv3Service est activé en utilisant le cmdlet [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true) PowerShell.

> [!CAUTION]
> L'activation de la protection des informations Azure permettra également à d'autres applications, telles que Microsoft Word ou Microsoft Outlook, de protéger les contenus grâce à l'AIP. En outre, toute politique de contrôle à l'embarquement utilisée pour restreindre la synchronisation MicrosoftEdge empêchera également d'autres applications de protéger le contenu utilisant AzureInformationProtection (AIP).

## MicrosoftEdge et Enterprise State Roaming (ESR)

MicrosoftEdge est une application inter-plateforme avec une étendue développée pour la synchronisation des données utilisateur sur tous leurs appareils et ne fait plus partie intégrante d’Azure AD Enterprise State Roaming. Toutefois, MicrosoftEdge remplit les promesses de protection des données d’Enterprise State Roaming, telles que la possibilité d’apporter votre propre clé. Pour plus d’informations, consultez [MicrosoftEdge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Résoudre les problèmes de synchronisation

Cette section fournit les étapes de résolution des problèmes de synchronisation les plus rencontrés. Il inclut également les outils recommandés pour collecter les journaux nécessaires à la résolution des problèmes.

### Problèmes d’identité et problèmes de synchronisation

Un cas d’utilisation populaire pour la maintenance de l’identité de l’utilisateur dans le navigateur consiste à prendre en charge la synchronisation. Pour cette raison, les problèmes d’identité sont souvent confondus avec les problèmes de synchronisation. Comprenez la différence entre les problèmes d’identité et de synchronisation avant de commencer à résoudre les problèmes de synchronisation.

Avant de traiter un problème comme un problème de synchronisation, vérifiez si l’utilisateur est signé dans le navigateur avec un compte valide.

La capture d’écran suivante montre un exemple d’erreur d’identité. L’erreur est «**Dernière erreur de jeton, EDGE_AUTH_ERROR: 3, 54, 3ea**», qui se trouve dans *edge://sync-internals* sous **Informations d’identification**:

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Dernière erreur de jeton EDGE_AUTH_ERROR: 3,54, 3ea":::

### Problèmes de synchronisation courants

#### Problème: Ne peut pas accéder à l’abonnement M365 ou Azure Information Protection

Avez-vous un ancien abonnement M365 ou Azure Information Protection (AIP) qui a expiré que vous avez ensuite remplacé par un nouvel abonnement? Si c’est le cas, l’ID de locataire a changé et les données de service doivent être réinitialisées. Consultez les instructions de réinitialisation des données dans l’erreur **de chiffrement rencontrée**.

#### Problème: « La synchronisation n’est pas disponible pour ce compte. »

Si cette erreur est rencontrée pour un compte Azure Active Directory, ou si DISABLED_BY_ADMIN apparaît dans *edge://sync-internals*, suivez les étapes de la procédure suivante de manière séquentielle jusqu’à ce que le problème soit résolu.

> [!NOTE]
> Étant donné que la source de cette erreur nécessite généralement une modification de configuration dans un client Azure Active Directory, ces étapes de dépannage ne peuvent être effectuées que par un administrateur client et non par les utilisateurs finaux.

1. Vérifiez que le client d’entreprise dispose d’un abonnement M365 pris en charge. La liste actuelle des types d’abonnement disponibles [est fournie ici](https://docs.microsoft.com/azure/information-protection/activate-office365). Si le client n’a pas d’abonnement pris en charge, il peut acheter Azure Information Protection séparément ou mettre à niveau vers l’un des abonnements pris en charge.
2. Si un abonnement pris en charge est disponible, vérifiez que le client dispose d’Azure Information Protection (AIP). Les instructions pour vérifier l’état d’Azure Information Protection et, si nécessaire, l’activation d’Azure Information Protection se trouvent [ici](https://docs.microsoft.com/azure/information-protection/activate-office365).
3. Si l’étape2 indique qu’Azure Information Protection est actif mais que la synchronisation ne fonctionne toujours pas, activez Enterprise State Roaming (ESR). Les instructions d’activation du système ESR sont [ici](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable). Notez qu’Enterprise State Roaming n’a pas besoin de rester en place. Vous pouvez désactiver Enterprise State Roaming si cette étape résout le problème.
4. Confirmez qu’Azure Information Protection n’est pas étendue via une stratégie d’intégration. Vous pouvez utiliser l’applet [PowerShell Get-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps)  pour voir si l’application d’une portée est activée. Les deux exemples suivants illustrent une configuration non étendue et une configuration limitée à un groupe de sécurité spécifique.

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


   Si l’étendue est activée, l’utilisateur affecté doit être ajouté au groupe de sécurité pour l’étendue ou l’étendue doit être supprimée. Dans l’exemple ci-dessous, l’intégration a étendu Azure Information Protection au groupe de sécurité indiqué et l’étendue doit être supprimée avec l’applet [PowerShell Set-AadrmOnboardingControlPolicy.](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps)

5. Confirmez que IPCv3Service est activé dans le client. [L’applet PowerShell Get-AadrmConfiguration](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) affiche l’état du service.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Vérifiez si IPCv3Service est activé.":::

6. Si le problème n’est pas résolu, contactez le [support Microsoft Edge](https://www.microsoftedgeinsider.com/support).

#### Problème : bloqué sur «Configuration de la synchronisation...» ou «Impossible de se connecter au serveur de synchronisation. Nouvelle tentative...»

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
   - [Points de terminaison du service de notification Windows](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).

5. Si le problème n’est toujours pas résolu, contactez le [support Microsoft Edge](https://www.microsoftedgeinsider.com/support).

### Problème: erreur de chiffrement rencontrée

Cette erreur est visible sous **Type d’informations** dans *edge://sync-internals* et peut signifier que les données côté service de l’utilisateur doivent être réinitialisées. L’exemple suivant montre un message d’erreur de chiffrement:
<br>«Error:GenerateCryptoErrorsForTypes@.. /.. /components/sync/driver/data_type_manager_impl.cc:42, une erreur de chiffrement s’est produite».

1. Redémarrez MicrosoftEdge et accédez à *edge://sync-internals*, puis consultez la section «**État de la clé de compte AAD**»
   - «Réussite» dans «Dernier résultat MIP»: l’erreur de chiffrement signifie que les données du serveur peuvent être chiffrées avec une clé perdue. La réinitialisation des données est nécessaire pour reprendre la synchronisation.
   - «Aucune autorisation» dans «Résultat du dernier MIP»: il est possible qu’il soit dû à une modification d’AzureAD ou à des modifications d’abonnement client. La réinitialisation des données est nécessaire pour reprendre la synchronisation.
   - D’autres erreurs peuvent signifier des problèmes de configuration du serveur.
2. Si la réinitialisation des données est nécessaire, voir [Réinitialiser les données Microsoft Edge dans le cloud](edge-learnmore-reset-data-in-cloud.md).

#### Problème: «La synchronisation a été désactivée par votre administrateur».

Assurez-vous que la [stratégie SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled) n’est pas définie.

## Forum Aux Questions

### SÉCURITÉ et CONFORMITÉ DES DONNÉES/SERVEUR

#### Les données synchronisées sont-elles chiffrées?

Les données sont cryptées lors du transport en utilisant TLS1.2 ou version ultérieure. Tous les types de données sont également chiffrés sur REST dans le service de Microsoft à l’aide de AES128. Tous les types de données, à l’exception de ceux utilisés pour la synchronisation de l’onglet ouvert et de l’historique, sont chiffrés avant de laisser l’appareil de l’utilisateur avec des clés gérées via la stratégie [Azure Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

#### Pourquoi les données d’historique et d’onglets ouverts n’ont-elles pas davantage de chiffrement côté client?

Pour réduire l’utilisation des ressources sur les appareils des utilisateurs finaux, les données d’historique sont générées côté serveur en fonction des données d’itinérance de l’onglet ouvert. Ce processus n’est pas possible avec le chiffrement côté client de ces données. Pour désactiver la synchronisation des onglets et de l’historique, appliquez les stratégies [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) ou [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) .

#### Les administrateurs client peuvent-ils incorporer leur propre clé?

Oui, via [Azure information protection](https://azure.microsoft.com/services/information-protection/).

#### Où les données synchronisées de Microsoft Edge sont-elles stockées?

Les données synchronisées pour les comptes Azure AD sont stockées dans des serveurs sécurisés en fonction de l’ID de client. Par exemple, les données d’un client enregistré aux États-Unis sont stockées dans des serveurs géolocalisés pour cette région et utilisent la même solution de stockage que celle des applications Office.

#### Les données quittent-elles le cloud de Microsoft, en dehors de la synchronisation avec Microsoft Edge?

Non.

#### À quelles conditions d’utilisation la synchronisation d’entreprise répond-elle?

Les conditions d’utilisation de la synchronisation de Microsoft Edge relèvent du contrat de licence logiciel Microsoft affichable dans MicrosoftEdge sur *Edge://Terms*. Votre abonnement Azure AD et les conditions d’utilisation sont relèvent en dernier ressort des [conditions générales de service en ligne](https://www.microsoft.com/licensing/product-licensing/products)de Microsoft.

#### Microsoft Edge prend-il en charge le cloud de la communauté du secteur public Community Cloud (GCC) High Compliance?

Pas à la date d'aujourd'hui. Pour les clients qui utilisent le Cloud HD de GCC, la synchronisation Microsoft Edge est désactivée.

### APPLICATION DE LA SYNCHRONISATION

#### Pourquoi la synchronisation MicrosoftEdge n’est-elle pas prise en charge dans tous les abonnements M365?

La synchronisation d’entreprise dépend [d’Azure Information Protection,](https://azure.microsoft.com/services/information-protection/)qui n’est pas disponible dans tous les abonnements M365.

#### Est-ce que la synchronisation de MicrosoftEdge se base sur Enterprise State Roaming?

Non. Enterprise State Roaming (ESR) peut être utilisé pour activer la synchronisation, mais Microsoft Edge Sync ne fait pas partie de ESR. Pour plus d’informations, consultez la [Synchronisation Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) et [Microsoft Edge et Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).

#### Microsoft Edge prend-il en charge la synchronisation entre Microsoft Edge et Internet Explorer?

Il n’existe pas d’offre pour la prise en charge de cette synchronisation. Si vous avez encore besoin d’Internet Explorer dans votre environnement pour prendre en charge des applications héritées, nous vous conseillons le [Nouveau mode Internet Explorer](https://docs.microsoft.com/deployedge/edge-ie-mode).

#### Est-ce que Microsoft Edge se synchronise avec Microsoft Edge hérité?

Non. Nous pensons que la connexion de ces deux écosystèmes entraîne la compromission de la fiabilité de la synchronisation dans Microsoft Edge. Nous allons garantir la migration des données existantes vers MicrosoftEdge. Les utilisateurs pourront également importer des données à partir du navigateur de leur choix, ce qui signifie également que MicrosoftEdge ne pourra pas se synchroniser avec InternetExplorer.

### GÉRER LA SYNCHRONISATION

#### Est-il possible d’empêcher la synchronisation de mes utilisateurs avec un client personnel?

Pas directement, mais vous pouvez déterminer quels profils peuvent se connecter à Microsoft Edge à l’aide de la stratégie [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

## Voir également

- [Synchronisation de MicrosoftEdge Entreprise](microsoft-edge-enterprise-sync.md)
- [MicrosoftEdge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
