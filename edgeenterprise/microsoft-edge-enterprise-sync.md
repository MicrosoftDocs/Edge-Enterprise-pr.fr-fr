---
title: Synchronisation de Microsoft Edge Entreprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 08/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Synchronisation de Microsoft Edge Entreprise
ms.openlocfilehash: a6d01356db478871a7c6b386bbb731b32dc4739a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979817"
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

Actuellement, la synchronisation de MicrosoftEdge pour les comptes Azure Active Directory (Azure AD) est disponible pour les abonnements suivants:

- Azure AD Premium (P1 et P2)
- M365 Business Premium
- Office365 E3 et versions ultérieures
- Azure Information Protection (AIP) (P1& P2)
- Tous les abonnements EDU (O365A1 ou version ultérieure, M365A1 version ultérieure, ou Azure Protection InformationP1 ou P2 pour étudiants ou université)

> [!NOTE]
> La synchronisation a une dépendance envers le service de protection offert par Azure Information Protection (AIP) pour protéger les données de synchronisation. Ce service est actuellement disponible pour les abonnements précédents. Pour afficher la liste complète des références SKU avec AIP consultez, [Tarification d’Information Protection](https://azure.microsoft.com/pricing/details/information-protection/).

## Options de configurations de la synchronisation de Microsoft Edge

Les options de configuration suivantes sont disponibles pour activer la synchronisation de MicrosoftEdge:

- Azure Information Protection (AIP)
- Azure AD Enterprise State Roaming (ESR)

Si les paramètres AIP et ESR sont désactivés, les utilisateurs verront un message d’erreur indiquant que la synchronisation n’est pas disponible pour leur compte.

### Azure Information Protection (AIP)

Si le service Azure Information Protection (AIP) est activé pour un client, tous les utilisateurs peuvent synchroniser les données MicrosoftEdge, quelle que soit la licence. Vous trouverez les instructions relatives à l’activation d’AIP [ici](https://docs.microsoft.com/azure/information-protection/activate-office365).

Pour limiter la synchronisation à certains ensembles d’utilisateurs, vous pouvez activer la [ méthode de contrôle d’intégration AADRM](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) pour ces utilisateurs. Si la synchronisation n’est toujours pas disponible après vous être assuré que tous les utilisateurs nécessaires sont intégrés, assurez-vous que le IPCv3Service est activé à l’aide de l’applet de commande PowerShell de [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps).

> [!CAUTION]
> L’activation de la Protection d’Information Azure limitera aussi l’accès pour d’autres applications utilisant AIP, telles que MicrosoftWord ou MicrosoftOutlook.

### Azure AD Enterprise State Roaming (ESR)

Si la fonctionnalité [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) d’Azure ActiveDirectory est activée pour un utilisateur ou un client, celui-ci peut utiliser la fonctionnalité de synchronisation de MicrosoftEdge, quel que soit le paramètre de stratégie de contrôle d’intégration.

## MicrosoftEdge et Enterprise State Roaming

Le nouveau MicrosoftEdge est une application multiplateforme avec une portée étendue pour la synchronisation des données utilisateur sur tous leurs appareils. Il ne fait plus partie d’Azure AD Enterprise State Roaming. Toutefois, la nouvelle version de MicrosoftEdge remplira les promesses de protection des données d’ESR, par exemple la possibilité de proposer votre propre clé. Pour plus d’informations, consultez [Microsoft Edge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Stratégies de groupe de synchronisation

Les stratégies de groupe suivantes affectent la synchronisation de MicrosoftEdge:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): désactive complètement la synchronisation.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): désactive l’enregistrement de l’historique de navigation et la synchronisation. Cette stratégie permet également de désactiver la synchronisation des onglets ouverts.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): permet de configurer la liste des types exclus de la synchronisation.

## Forum Aux Questions

### SÉCURITÉ et CONFORMITÉ DES DONNÉES/SERVEUR

#### Les données synchronisées sont-elles chiffrées? 

Les données sont chiffrées dans le transport à l’aide de TLS 1.2 ou plus, et en outre, au repos dans le service Microsoft en utilisant l’ AES256.

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
