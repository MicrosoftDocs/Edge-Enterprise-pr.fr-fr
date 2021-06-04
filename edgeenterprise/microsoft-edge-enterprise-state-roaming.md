---
title: Microsoft Edge et Enterprise State Roaming
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 02/14/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge et Enterprise State Roaming
ms.openlocfilehash: 6090ecfda2f792d49e452771943bc6348066a3d8
ms.sourcegitcommit: 90b8eab62edbed0e0a84780abd7d3854bf95c130
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2021
ms.locfileid: "11328056"
---
# Microsoft Edge et Enterprise State Roaming

Cet article explique comment la participation de Microsoft Edge participation à l’offre ESR (Enterprise State roaming) évolue pour une meilleure prise en charge de la synchronisation entre les plateformes et les appareils.

> [!NOTE]
> Cet article concerne Microsoft Edge version 77 ou ultérieure.

##  <a name="introduction"></a>Introduction

Avec Windows 10, les utilisateurs d’[Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) ont obtenu la possibilité de synchroniser leurs données de paramètres utilisateur et de paramètres d’application dans le cloud. [Enterprise State Roaming (ESR)](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) offre aux utilisateurs une expérience unifiée sur leurs appareils Windows et réduit le temps nécessaire à la configuration d’un nouvel appareil.

Dans le cadre de l’adoption par Microsoft Edge de la plateforme Chromium, sa solution de synchronisation est désormais déconnectée de la structure de synchronisation de Windows. Cela affecte la relation entre Microsoft Edge et l’offre ESR.

> [!IMPORTANT]
> Le nouveau Microsoft Edge ne fait pas partie de l’offre ESR.

##  <a name="what’s-changing-with-microsoft-edge"></a>Qu’est-ce qui change pour Microsoft Edge ?

Avec le nouvelle version de Microsoft Edge, la solution de synchronisation n’est pas liée à l’écosystème de synchronisation Windows. Cela nous permet d’offrir des versions de Microsoft Edge sur toutes les plateformes, telles que Windows 7, Windows 8.1, iOS, Android et macOS. Cela nous permet également d’offrir une synchronisation pour les comptes non principaux sur Windows. En outre, nous pouvons fournir des versions de Microsoft Edge à une cadence plus rapprochée et souple que Windows. Pour plus d’informations, consultez [Mises à jour Windows pour prendre en charge la prochaine version de Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md). Tous ces facteurs ont mis en évidence la nécessité de réévaluer la participation de Microsoft Edge à l’offre ESR.

ESR est présenté comme une offre de produit Windows offrant des promesses quant au traitement des données provenant des appareils Windows, mais la synchronisation Microsoft Edge s’étend au-delà des appareils Windows. En outre, lorsque les données sont itinérantes sur ces appareils, il est difficile de définir l’offre de synchronisation Microsoft Edge dans le contexte d’ESR. Pour simplifier le fonctionnement et la gestion de la synchronisation, et afin de prendre en compte les modifications qui sont mises en évidence, il a été décidé de retirer Microsoft Edge de l’offre ESR.

##  <a name="does-this-mean-enterprises-will-lose-the-abilities-they-had-as-part-of-esr"></a>Cela signifie-t-il que les entreprises perdront les fonctionnalités dont elles disposaient dans le cadre d’ESR ?

Non. Microsoft Edge continuera à prendre en charge la plupart des fonctionnalités proposées dans l’offre ESR.

###  <a name="unified-experience-across-devices-and-new-device-configuration-time"></a>Expérience unifiée sur les appareils et nouveau temps de configuration des appareils

Lorsqu’un utilisateur est connecté à son appareil Windows à l’aide d’un compte Azure Active Directory (Azure AD), Microsoft Edge hérite implicitement de cette identité lors du premier lancement du nouveau navigateur.

Une fois qu’un utilisateur a autorisé explicitement l’activation de la synchronisation dans le nouveau Microsoft Edge, le navigateur synchronise toutes les données du navigateur, telles que les favoris, les mots de passe et l’historique. Cela garantit une expérience unifiée sur tous les appareils et réduit le temps nécessaire pour personnaliser le navigateur.

###  <a name="separation-of-corporate-and-consumer-data"></a>Séparation des données de l’entreprise et du grand public

Les organisations contrôlent leurs données et il n’existe pas de mélange de données d’entreprise dans un compte de cloud consommateur ou de données de grand public dans un compte cloud d’entreprise.

###  <a name="enhanced-security"></a>Sécurité renforcée

Les données sont automatiquement chiffrées avant de quitter l’appareil Windows 10 de l’utilisateur à l’aide d’Azure Information Protection et les données restent chiffrées au repos dans le cloud. Tout le contenu reste chiffré au repos dans le cloud, à l’exception des espaces de noms, comme les noms de paramètres.

###  <a name="monitoring"></a>Surveillance

Nous offrirons un contrôle et une visibilité sur la personne qui synchronise les paramètres de votre organisation et sur les appareils, par le biais de l’intégration avec le portail Azure AD. Cette fonctionnalité sera activée dans une prochaine version.

###  <a name="management"></a>Gestion

Les administrateurs pourront contrôler quels membres de votre organisation peuvent activer la synchronisation.Voir[Configurer les stratégies de groupe Microsoft Edge](microsoft-edge-enterprise-sync.md#configure-microsoft-edge-sync) et [ Synchronisation](microsoft-edge-enterprise-sync.md#sync-group-policies). En outre, les utilisateurs peuvent activer/désactiver la synchronisation pour chacun de leurs appareils, et basculer chaque attribut de données individuellement pour la synchronisation.

###  <a name="key-management"></a>Gestion des clés

La fonctionnalité de synchronisation tire parti d’Azure Information Protection (AIP) pour protéger les données synchronisées uniquement pour l’utilisateur et les administrateurs de l’entreprise. AIP prend en charge les deux Microsoft gérés (par défaut) et fournit votre propre clé pour la gestion des clés cloud. La stratégie de gestion de clé cloud utilisée par votre organisation est transparente pour Microsoft Edge et n’a aucun impact sur la fonctionnalité de synchronisation.

> [!IMPORTANT]
> La fonctionnalité [Hold your own key (HYOK)](https://docs.microsoft.com/azure/information-protection/configure-adrms-restrictions) et le service AD RMS (Active Directory Rights Management Services) ne sont pas pris en charge.

##  <a name="summary-of-sync-attributes"></a>Résumé des attributs de synchronisation

Les attributs de données suivants seront synchronisés dans la nouvelle version de Microsoft Edge lors du premier lancement :

- Favoris
- Mots de passe
- Remplissage de formulaire
- Historique
- Onglets ouverts (sessions)
- Paramètres (préférences)
- Extensions

La liste d’attributs précédente est différente des attributs qui peuvent être synchronisés dans Microsoft Edge hérité. Pour plus d’informations sur les paramètres Microsoft Edge hérités, consultez [Paramètres d’itinérance Windows 10](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference). Les utilisateurs peuvent activer ou désactiver de manière sélective ces attributs à l’aide des paramètres Microsoft Edge. Étant donné la différence d’attributs entre les deux versions (par exemple, l’historique), les utilisateurs peuvent être invités à accorder à nouveau l’autorisation de synchronisation.

> [!NOTE]
> À la différence de Microsoft Edge hérité, le nouveau Microsoft Edge n’utilise pas le gestionnaire d’informations d’identification Windows pour les mots de passe. Par conséquent, il ne synchronise pas les mots de passe avec Internet Explorer ou d’autres applications qui utilisent le gestionnaire d’informations d’identification Windows.

##  <a name="terms-of-service"></a>Conditions d’utilisation

Les conditions d’utilisation de la synchronisation de Microsoft Edge sont contenues dans la licence de logiciel Microsoft, disponible dans Microsoft Edge sur *edge://terms*.

##  <a name="see-also"></a>Articles associés

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Synchronisation de Microsoft Edge](microsoft-edge-enterprise-sync.md)