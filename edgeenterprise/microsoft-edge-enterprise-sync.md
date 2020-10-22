---
title: Synchronisation de Microsoft Edge Entreprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 10/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Synchronisation de Microsoft Edge Entreprise
ms.openlocfilehash: e51346d9bab83228c42a84a7a14ee45dc9b463a7
ms.sourcegitcommit: b32d8d64ae65dc5a46e47b7c34b0211097a0cc65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "11133129"
---
# Synchronisation de Microsoft Edge Entreprise

Cet article explique comment utiliser MicrosoftEdge pour synchroniser vos favoris, vos mots de passe et d’autres données de navigateur sur tous vos appareils connectés.

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

## Vue d'ensemble

La synchronisation de MicrosoftEdge permet aux utilisateurs d’accéder à leurs données de navigation sur tous leurs appareils connectés. Les données prises en charge par la synchronisation sont les suivantes:

- Favoris
- Mots de passe
- Adresses et autres (remplissage de formulaire)
- Regroupements
- Paramètres

La fonctionnalité de synchronisation est activée après accord de l’utilisateur et les utilisateurs peuvent activer ou désactiver la synchronisation pour chacun des types de données répertoriés ci-dessus.

> [!NOTE]
> Des données de configuration et de connectivité des appareils supplémentaires (telles que le nom, la marque et le modèle de l’appareil) sont téléchargées pour prendre en charge la fonctionnalité de synchronisation.

## Conditions préalables

La synchronisation Microsoft Edge pour les comptes Azure Active Directory (Azure AD) est disponible pour les abonnements suivants :

- Azure AD Premium (P1 et P2)
- M365 Business Premium
- Office365 E1 et versions ultérieures
- Azure Information Protection (AIP) (P1& P2)
- Tous les abonnements à EDU (Microsoft Apps pour les étudiants ou la faculté, Exchange Online pour les étudiants ou la faculté, O365 A1 ou supérieur, M365 A1 ou supérieur, ou Azure Information Protection P1 ou P2 pour les étudiants ou la faculté)

## Configurer la synchronisation avec Microsoft Edge

Les options de configuration pour Microsoft Edge se synchronisent via le service Azure Information Protection (AIP). Lorsque l'AIP est activé pour un locataire, tous les utilisateurs peuvent synchroniser les données Microsoft Edge, quelle que soit leur licence. Vous trouverez les instructions relatives à l’activation d’AIP [ici](https://docs.microsoft.com/azure/information-protection/activate-office365).

Pour limiter la synchronisation à certains groupes d'utilisateurs, vous pouvez activer [la politique de contrôle à l'embarquement AIP ](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) pour ces utilisateurs. Si la synchronisation n'est toujours pas disponible après s'être assuré que tous les utilisateurs nécessaires sont embarqués, assurez-vous que le service IPCv3Service est activé en utilisant le cmdlet [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps) PowerShell.

> [!CAUTION]
> L'activation de la protection des informations Azure permettra également à d'autres applications, telles que Microsoft Word ou Microsoft Outlook, de protéger les contenus grâce à l'AIP. En outre, toute politique de contrôle à l'embarquement utilisée pour restreindre la synchronisation Edge empêchera également d'autres applications de protéger le contenu utilisant l'AIP.

## MicrosoftEdge et Enterprise State Roaming

Le nouveau MicrosoftEdge est une application multiplateforme avec une portée étendue pour la synchronisation des données utilisateur sur tous leurs appareils. Il ne fait plus partie d’Azure AD Enterprise State Roaming. Toutefois, la nouvelle version de MicrosoftEdge remplira les promesses de protection des données d’ESR, par exemple la possibilité de proposer votre propre clé. Pour plus d’informations, consultez [Microsoft Edge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Stratégies de groupe de synchronisation

Les stratégies de groupe suivantes affectent la synchronisation de MicrosoftEdge:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): désactive complètement la synchronisation.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): désactive l’enregistrement de l’historique de navigation et la synchronisation. Cette stratégie permet également de désactiver la synchronisation des onglets ouverts.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): permet de configurer la liste des types exclus de la synchronisation.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): permet aux profils Active Directory (AD) d'utiliser le stockage sur site. Pour plus d'informations, voir [Synchronisation sur site pour les utilisateurs d'Active Directory (AD) ](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync) :  Active la synchronisation par défaut et ne nécessite pas le consentement de l'utilisateur pour la synchronisation.  

## Forum Aux Questions

### SÉCURITÉ et CONFORMITÉ DES DONNÉES/SERVEUR

#### Les données synchronisées sont-elles chiffrées? 

Les données sont cryptées lors du transport en utilisant TLS 1.2 ou plus. La plupart des types de données sont également chiffrés au repos dans le service Microsoft à l’aide de la fonction AES256. 

#### Où les données Microsoft Edge synchronisées de sont-elles stockées?

Les données synchronisées pour les comptes Azure AD sont stockées dans des serveurs sécurisés en fonction de l’ID de client. Par exemple, les données d’un client enregistré aux États-Unis sont stockées dans des serveurs géolocalisés pour cette région et utilisent la même solution de stockage que celle des applications Office.

#### Les données quittent-elles le cloud de Microsoft, en dehors de la synchronisation avec Microsoft Edge?

Non.

#### Les administrateurs client peuvent-ils incorporer leur propre clé?

Oui, activer [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).

#### À quelles conditions de service la synchronisation d’entreprise répond-elle?

Les conditions de service sont identiques à celles de votre abonnement Azure AD. Toutes les conditions de service Azure AD vont répondre aux [Conditions de service en ligne](https://www.microsoft.com/licensing/product-licensing/products) de Microsoft.

#### Microsoft Edge prend-il en charge le cloud de la communauté du secteur public Community Cloud (GCC) High Compliance?

Pas à la date d'aujourd'hui. GCC High est de niveau D, tandis que Microsoft Edge prend en charge le niveau C.

### APPLICATION DE LA SYNCHRONISATION

#### Que se passe-t-il avec les clients entreprise et éducation qui décident de conserver la version héritée de MicrosoftEdge?

La version actuelle du navigateur MicrosoftEdge continuera à faire partie de l’offre ESR.

#### Pourquoi ai-je besoin d’un abonnement Azure AD Premium pour la synchronisation?

La synchronisation d’entreprise dépend d’Azure Information Protection, qui n’est pas disponible dans les niveaux Azure AD.

#### Est-ce que la synchronisation de MicrosoftEdge se base sur Enterprise State Roaming?

Non. Enterprise State Roaming (ESR) peut être utilisé pour activer la synchronisation, mais Microsoft Edge Sync ne fait pas partie de ESR. Pour plus d’informations, consultez la [Synchronisation Microsoft Edge](microsoft-edge-enterprise-sync.md) et [Microsoft Edge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

#### Microsoft Edge prend-il en charge la synchronisation entre Microsoft Edge et Internet Explorer?

Il n’existe pas d’offre pour la prise en charge de cette synchronisation. Si vous avez encore besoin d’IE dans votre environnement pour prendre en charge des applications héritées, nous vous conseillons le [Nouveau mode IE](https://docs.microsoft.com/deployedge/edge-ie-mode).

#### Le nouveau navigateur Microsoft Edge sera-t-il synchronisé avec Microsoft Edge Legacy?

Non. Nous pensons que la connexion de ces deux écosystèmes entraînera des problèmes de fiabilité de la synchronisation dans le nouveau MicrosoftEdge. Nous nous assurerons que les données existantes seront migrées vers le nouveau MicrosoftEdge. Les utilisateurs pourront également importer des données à partir du navigateur de leur choix. Cela signifie également que le nouveau navigateur MicrosoftEdge ne disposera d’aucune méthode de synchronisation avec Internet Explorer.

### GÉRER LA SYNCHRONISATION

#### Est-il possible d’empêcher la synchronisation de mes utilisateurs avec un client personnel?

Pas directement, mais vous pouvez déterminer quels profils peuvent se connecter à Microsoft Edge à l’aide de la stratégie [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [MicrosoftEdge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
