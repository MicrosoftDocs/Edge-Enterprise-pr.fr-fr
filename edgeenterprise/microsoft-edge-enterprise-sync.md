---
title: Configurer la synchronisation d’entreprise Microsoft Edge
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Options d'administration et d'utilisation pour configurer Microsoft Edge afin de synchroniser les favoris, les mots de passe et d'autres données du navigateur.
ms.openlocfilehash: 99edc97bd5f4bab7bf421e0d15e512c5f6f76cc0
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617754"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a>Configurer la synchronisation d’entreprise Microsoft Edge

Cet article explique comment les administrateurs peuvent configurer Microsoft Edge pour synchroniser les favoris, mots de passe et autres données de navigateur de l’utilisateur sur tous les appareils connectés. Si vous n’êtes pas un administrateur, consultez cet article pour savoir comment vous connecter et synchroniser Microsoft Edge sur plusieurs appareils. [Connectez-vous pour synchroniser Microsoft Edge sur plusieurs appareils](https://support.microsoft.com/microsoft-edge/sign-in-to-sync-microsoft-edge-across-devices-e6ffa79b-ed52-aa32-47e2-5d5597fe4674).

> [!NOTE]
> S'applique à Microsoft Edge version 77 ou ultérieure, sauf indication contraire.

## <a name="overview"></a>Vue d’ensemble

La synchronisation de Microsoft Edge permet aux utilisateurs d’accéder à leurs données de navigation sur tous leurs appareils connectés. Les données prises en charge par la synchronisation sont les suivantes :

- Favoris
- Mots de passe
- Adresses et autres (remplissage de formulaire)
- Regroupements
- Paramètres
- Extension
- Ouvrir des onglets (disponible dans la version 88 de Microsoft Edge)
- Historique (disponible dans la version 88 de Microsoft Edge)

La fonctionnalité de synchronisation est activée après accord de l’utilisateur et les utilisateurs peuvent activer ou désactiver la synchronisation pour chacun des types de données répertoriés ci-dessus. Si un utilisateur rencontre un problème de synchronisation, il peut avoir besoin de réinitialiser la synchronisation dans **Paramètres** > ** Profils** > ** Réinitialiser la synchronisation**.

> [!NOTE]
> Des données supplémentaires de connectivité et de configuration de l'appareil (telles que le nom, la marque et le modèle de l'appareil) sont téléchargées pour prendre en charge la fonctionnalité de synchronisation.

## <a name="prerequisites"></a>Conditions préalables

La synchronisation Microsoft Edge pour les comptes Azure Active Directory (Azure AD) est disponible pour les abonnements suivants :

- Azure AD Premium (P1 ou P2)
- M365 Business Premium
- Office 365 E1 et versions ultérieures
- Protection d’information d’Azure (AIP) (P1 ou P2)
- Tous les abonnements à EDU (Microsoft Apps pour les étudiants ou la faculté, Exchange Online pour les étudiants ou la faculté, O365 A1 ou supérieur, M365 A1 ou supérieur, ou Azure Information Protection P1 ou P2 pour les étudiants ou la faculté)

## <a name="sync-group-policies"></a>Stratégies de groupe de synchronisation

Les administrateurs peuvent utiliser les stratégies de groupe suivantes pour configurer et gérer la synchronisation de Microsoft Edge :

- [SyncDisabled](./microsoft-edge-policies.md#syncdisabled) : désactive complètement la synchronisation.
- [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) : désactive l’enregistrement de l’historique de navigation et la synchronisation. Cette stratégie permet également de désactiver la synchronisation des onglets ouverts.
- [AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): si cette stratégie est définie sur Désactivé, la synchronisation de l’historique sera également désactivée.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) : permet de configurer la liste des types exclus de la synchronisation.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): permet aux profils Active Directory (AD) d'utiliser le stockage sur site. Pour plus d'informations, voir [Synchronisation sur site pour les utilisateurs d'Active Directory (AD)](./microsoft-edge-on-premises-sync.md).
- [ForceSync](/deployedge/microsoft-edge-policies#forcesync) : activez la synchronisation par défaut et n’exigez pas le consentement de l’utilisateur pour la synchronisation.  

## <a name="configure-microsoft-edge-sync"></a>Configurer la synchronisation de Microsoft Edge

Les options de configuration pour la synchronisation de Microsoft Edge sont disponibles via le service Azure Information Protection (AIP). Lorsque l'AIP est activé pour un locataire, tous les utilisateurs peuvent synchroniser les données Microsoft Edge, quelle que soit leur licence. Vous trouverez les instructions relatives à l’activation d’AIP [ici](/azure/information-protection/activate-office365).

Pour limiter la synchronisation à certains groupes d'utilisateurs, vous pouvez activer [la politique de contrôle à l'embarquement AIP ](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) pour ces utilisateurs. Si la synchronisation n'est toujours pas disponible après s'être assuré que tous les utilisateurs nécessaires sont embarqués, assurez-vous que le service IPCv3Service est activé en utilisant le cmdlet [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps) PowerShell.

> [!CAUTION]
> L'activation de la protection des informations Azure permettra également à d'autres applications, telles que Microsoft Word ou Microsoft Outlook, de protéger les contenus grâce à l'AIP. En outre, toute politique de contrôle à l'embarquement utilisée pour restreindre la synchronisation Microsoft Edge empêchera également d'autres applications de protéger le contenu utilisant Azure Information Protection (AIP).

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a>Microsoft Edge et Enterprise State Roaming (ESR)

Microsoft Edge est une application multiplateforme avec une étendue développée pour la synchronisation des données utilisateur sur tous leurs appareils et ne fait plus partie d’Azure AD Enterprise State Roaming. Toutefois, Microsoft Edge remplit les promesses de protection des données d’Enterprise State Roaming, telles que la possibilité d’apporter votre propre clé. Pour plus d’informations, consultez [Microsoft Edge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## <a name="see-also"></a>Voir également

- [Synchronisation de Microsoft Edge Entreprise](microsoft-edge-enterprise-sync.md)
- [Diagnostiquer et résoudre les problèmes de synchronisation de Microsoft Edge](microsoft-edge-troubleshoot-enterprise-sync.md)
- [Microsoft Edge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)