---
title: Synchronisation de Microsoft Edge Entreprise FAQ
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Questions fréquemment posées sur la synchronisation d’entreprise Microsoft Edge.
ms.openlocfilehash: a13e1f02f6e871004d45f81159d5cf0a3397b6ad
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643140"
---
# <a name="microsoft-edge-enterprise-sync-faq"></a>Synchronisation de Microsoft Edge Entreprise FAQ

Cet article répond à des questions fréquentes sur la synchronisation d’entreprise pour Microsoft Edge version 77 ou ultérieure.

## <a name="security-and-serverdata-compliance"></a>Sécurité et conformité des données/serveur

### <a name="is-the-synced-data-encrypted"></a>Les données synchronisées sont-elles chiffrées ?

Les données sont cryptées lors du transport en utilisant TLS 1.2 ou version ultérieure. Tous les types de données sont également chiffrés sur REST dans le service de Microsoft à l’aide de AES128. Tous les types de données, à l’exception de ceux utilisés pour la synchronisation de l’onglet ouvert et de l’historique, sont chiffrés avant de laisser l’appareil de l’utilisateur avec des clés gérées via la stratégie [Azure Information Protection](./microsoft-edge-policies.md#restrictsignintopattern).

### <a name="why-dont-open-tab-and-history-data-have-more-client-side-encryption"></a>Pourquoi les données d’historique et d’onglets ouverts n’ont-elles pas davantage de chiffrement côté client ?

Pour réduire l’utilisation des ressources sur les appareils des utilisateurs finaux, les données d’historique sont générées côté serveur en fonction des données d’itinérance de l’onglet ouvert. Ce processus n’est pas possible avec le chiffrement côté client de ces données. Pour désactiver la synchronisation des onglets et de l’historique, appliquez les stratégies [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) ou [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) .

### <a name="can-tenant-admins-bring-their-own-key"></a>Les administrateurs client peuvent-ils incorporer leur propre clé ?

Oui, via [Azure information protection](https://azure.microsoft.com/services/information-protection/).

### <a name="where-is-microsoft-edge-sync-data-stored"></a>Où les données synchronisées de Microsoft Edge sont-elles stockées ?

Les données synchronisées pour les comptes Azure AD sont stockées dans des serveurs sécurisés en fonction de l’ID de client. Par exemple, les données d’un client enregistré aux États-Unis sont stockées dans des serveurs géolocalisés pour cette région et utilisent la même solution de stockage que celle des applications Office.

### <a name="does-the-data-ever-leave-microsofts-cloud-aside-from-syncing-to-microsoft-edge"></a>Les données quittent-elles le cloud de Microsoft, en dehors de la synchronisation avec Microsoft Edge ?

Non.

### <a name="what-terms-of-service-does-enterprise-sync-fall-under"></a>À quelles conditions d’utilisation la synchronisation d’entreprise répond-elle ?

Les conditions d’utilisation de la synchronisation de Microsoft Edge relèvent du contrat de licence logiciel Microsoft affichable dans Microsoft Edge sur *Edge://Terms*. Votre abonnement Azure AD et les conditions d’utilisation sont relèvent en dernier ressort des [conditions générales de service en ligne](https://www.microsoft.com/licensing/product-licensing/products)de Microsoft.

### <a name="does-microsoft-edge-support-government-community-cloud-gcc-high-compliance"></a>Microsoft Edge prend-il en charge le cloud de la communauté du secteur public Community Cloud (GCC) High Compliance ?

Pas à la date d'aujourd'hui. Pour les clients qui utilisent le Cloud HD de GCC, la synchronisation Microsoft Edge est désactivée.

## <a name="applying-sync"></a>Application de la synchronisation

### <a name="why-isnt-microsoft-edge-sync-supported-in-all-m365-subscriptions"></a>Pourquoi la synchronisation Microsoft Edge n’est-elle pas prise en charge dans tous les abonnements M365 ?

La synchronisation d’entreprise dépend [d’Azure Information Protection,](https://azure.microsoft.com/services/information-protection/)qui n’est pas disponible dans tous les abonnements M365.

### <a name="is-microsoft-edge-sync-based-on-enterprise-state-roaming"></a>Est-ce que la synchronisation de Microsoft Edge se base sur Enterprise State Roaming ?

Non. Enterprise State Roaming (ESR) peut être utilisé pour activer la synchronisation, mais Microsoft Edge Sync ne fait pas partie de ESR. Pour plus d’informations, consultez la [Synchronisation Microsoft Edge](/DeployEdge/microsoft-edge-enterprise-sync) et [Microsoft Edge et Enterprise State Roaming](/DeployEdge/microsoft-edge-enterprise-state-roaming).

### <a name="will-microsoft-edge-ever-support-syncing-between-microsoft-edge-and-ie"></a>Microsoft Edge prend-il en charge la synchronisation entre Microsoft Edge et Internet Explorer ?

Il n’existe pas d’offre pour la prise en charge de cette synchronisation. Si vous avez encore besoin d’Internet Explorer dans votre environnement pour prendre en charge des applications héritées, nous vous conseillons le [Nouveau mode Internet Explorer](./edge-ie-mode.md).

### <a name="will-microsoft-edge-sync-with-microsoft-edge-legacy"></a>Est-ce que Microsoft Edge se synchronise avec Microsoft Edge hérité ?

Non. Nous pensons que la connexion de ces deux écosystèmes entraîne la compromission de la fiabilité de la synchronisation dans Microsoft Edge. Nous allons garantir la migration des données existantes vers Microsoft Edge. Les utilisateurs pourront également importer des données à partir du navigateur de leur choix, ce qui signifie également que Microsoft Edge ne pourra pas se synchroniser avec Internet Explorer.

## <a name="managing-sync"></a>Gérer la synchronisation

### <a name="is-it-possible-to-stop-my-users-from-syncing-with-a-personal-tenant"></a>Est-il possible d’empêcher la synchronisation de mes utilisateurs avec un client personnel ?

Pas directement, mais vous pouvez déterminer quels profils peuvent se connecter à Microsoft Edge à l’aide de la stratégie [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern).

## <a name="see-also"></a>Voir également

- [Synchronisation de Microsoft Edge Entreprise](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)