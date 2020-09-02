---
title: MicrosoftEdge et Enterprise State Roaming
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 02/14/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: MicrosoftEdge et Enterprise State Roaming
ms.openlocfilehash: a759b1d9d4be8dced7bfcc2ef8d0f23b514f4be0
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979828"
---
# MicrosoftEdge et Enterprise State Roaming

Cet article explique comment la participation de MicrosoftEdge participation à l’offre ESR (Enterprise State roaming) évolue pour une meilleure prise en charge de la synchronisation entre les plateformes et les appareils.

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

## Introduction

Avec Windows10, les utilisateurs d’[Azure ActiveDirectory (AzureAD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) ont obtenu la possibilité de synchroniser leurs données de paramètres utilisateur et de paramètres d’application dans le cloud. [Enterprise State Roaming (ESR)](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) offre aux utilisateurs une expérience unifiée sur leurs appareils Windows et réduit le temps nécessaire à la configuration d’un nouvel appareil.

Dans le cadre de l’adoption par MicrosoftEdge de la plateforme Chromium, sa solution de synchronisation est désormais déconnectée de la structure de synchronisation de Windows. Cela affecte la relation entre MicrosoftEdge et l’offre ESR.

> [!IMPORTANT]
> Le nouveau MicrosoftEdge ne fait pas partie de l’offre ESR.

## Qu’est-ce qui change pour MicrosoftEdge?

Avec le nouvelle version de MicrosoftEdge, la solution de synchronisation n’est pas liée à l’écosystème de synchronisation Windows. Cela nous permet d’offrir des versions de MicrosoftEdge sur toutes les plateformes, telles que Windows7, Windows8.1, iOS, Android et macOS. Cela nous permet également d’offrir une synchronisation pour les comptes non principaux sur Windows. En outre, nous pouvons fournir des versions de MicrosoftEdge à une cadence plus rapprochée et souple que Windows. Pour plus d’informations, consultez [Mises à jour Windows pour prendre en charge la prochaine version de MicrosoftEdge](microsoft-edge-sysupdate-windows-updates.md). Tous ces facteurs ont mis en évidence la nécessité de réévaluer la participation de MicrosoftEdge à l’offre ESR.

ESR est présenté comme une offre de produit Windows offrant des promesses quant au traitement des données provenant des appareils Windows, mais la synchronisation MicrosoftEdge s’étend au-delà des appareils Windows. En outre, lorsque les données sont itinérantes sur ces appareils, il est difficile de définir l’offre de synchronisation MicrosoftEdge dans le contexte d’ESR. Pour simplifier le fonctionnement et la gestion de la synchronisation, et afin de prendre en compte les modifications qui sont mises en évidence, il a été décidé de retirer MicrosoftEdge de l’offre ESR.

## Cela signifie-t-il que les entreprises perdront les fonctionnalités dont elles disposaient dans le cadre d’ESR?

Non. MicrosoftEdge continuera à prendre en charge la plupart des fonctionnalités proposées dans l’offre ESR.

### Expérience unifiée sur les appareils et nouveau temps de configuration des appareils

Lorsqu’un utilisateur est connecté à son appareil Windows à l’aide d’un compte Azure ActiveDirectory (Azure AD), MicrosoftEdge hérite implicitement de cette identité lors du premier lancement du nouveau navigateur.

Une fois qu’un utilisateur a autorisé explicitement l’activation de la synchronisation dans le nouveau MicrosoftEdge, le navigateur synchronise toutes les données du navigateur, telles que les favoris, les mots de passe et l’historique. Cela garantit une expérience unifiée sur tous les appareils et réduit le temps nécessaire pour personnaliser le navigateur.

### Séparation des données de l’entreprise et du grand public

Les organisations contrôlent leurs données et il n’existe pas de mélange de données d’entreprise dans un compte de cloud consommateur ou de données de grand public dans un compte cloud d’entreprise.

### Sécurité renforcée

Les données sont automatiquement chiffrées avant de quitter l’appareil Windows10 de l’utilisateur à l’aide d’Azure Information Protection et les données restent chiffrées au repos dans le cloud. Tout le contenu reste chiffré au repos dans le cloud, à l’exception des espaces de noms, comme les noms de paramètres.

### Surveillance

Nous offrirons un contrôle et une visibilité sur la personne qui synchronise les paramètres de votre organisation et sur les appareils, par le biais de l’intégration avec le portail AzureAD. Cette fonctionnalité sera activée dans une prochaine version.

### Gestion

Les administrateurs seront en mesure de contrôler les membres de votre organisation qui peuvent activer la synchronisation. Consultez [Options de configuration de la synchronisation de MicrosoftEdge](microsoft-edge-enterprise-sync.md#configuration-options-for-microsoft-edge-sync) et [Synchroniser les stratégies de groupe](microsoft-edge-enterprise-sync.md#sync-group-policies). En outre, les utilisateurs peuvent activer/désactiver la synchronisation pour chacun de leurs appareils, et basculer chaque attribut de données individuellement pour la synchronisation.

### Gestion des clés

La fonctionnalité de synchronisation tire parti d’Azure Information Protection (AIP) pour protéger les données synchronisées uniquement pour l’utilisateur et les administrateurs de l’entreprise. AIP prend en charge les deux Microsoft gérés (par défaut) et fournit votre propre clé pour la gestion des clés cloud. La stratégie de gestion de clé cloud utilisée par votre organisation est transparente pour MicrosoftEdge et n’a aucun impact sur la fonctionnalité de synchronisation.

> [!IMPORTANT]
> La fonctionnalité [Hold your own key (HYOK)](https://docs.microsoft.com/azure/information-protection/configure-adrms-restrictions) et le service AD RMS (Active Directory Rights Management Services) ne sont pas pris en charge.

## Résumé des attributs de synchronisation

Les attributs de données suivants seront synchronisés dans la nouvelle version de MicrosoftEdge lors du premier lancement:

- Favoris
- Mots de passe
- Remplissage de formulaire
- Historique
- Onglets ouverts (sessions)
- Paramètres (préférences)
- Extensions

La liste d’attributs précédente est différente des attributs qui peuvent être synchronisés dans MicrosoftEdge hérité. Pour plus d’informations sur les paramètres MicrosoftEdge hérités, consultez [Paramètres d’itinérance Windows10](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference). Les utilisateurs peuvent activer ou désactiver de manière sélective ces attributs à l’aide des paramètres MicrosoftEdge. Étant donné la différence d’attributs entre les deux versions (par exemple, l’historique), les utilisateurs peuvent être invités à accorder à nouveau l’autorisation de synchronisation.

> [!NOTE]
> À la différence de MicrosoftEdge hérité, le nouveau MicrosoftEdge n’utilise pas le gestionnaire d’informations d’identification Windows pour les mots de passe. Par conséquent, il ne synchronise pas les mots de passe avec Internet Explorer ou d’autres applications qui utilisent le gestionnaire d’informations d’identification Windows.

## Conditions d’utilisation

Les conditions d’utilisation de la synchronisation de MicrosoftEdge sont contenues dans la licence de logiciel Microsoft, disponible dans MicrosoftEdge sur *edge://terms*.

## Articles associés

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Synchronisation de MicrosoftEdge](microsoft-edge-enterprise-sync.md)