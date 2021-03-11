---
title: Synchronisation de MicrosoftEdge Entreprise FAQ
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Questions fréquemment posées sur la synchronisation d’entreprise Microsoft Edge.
ms.openlocfilehash: 51f6dfc4cd8f308815ee111c30d5501ec0e44f59
ms.sourcegitcommit: 86e0de9b27ad4297a6d5a57c866d7ef4fc7bb0cd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "11400188"
---
# <a name="microsoft-edge-enterprise-sync-faq"></a><span data-ttu-id="8e63c-103">Synchronisation de MicrosoftEdge Entreprise FAQ</span><span class="sxs-lookup"><span data-stu-id="8e63c-103">Microsoft Edge enterprise sync FAQ</span></span>

<span data-ttu-id="8e63c-104">Cet article répond à des questions fréquentes sur la synchronisation d’entreprise pour Microsoft Edge version 77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8e63c-104">This article answers frequently asked questions about enterprise sync for Microsoft Edge version 77 or later.</span></span>

## <a name="security-and-serverdata-compliance"></a><span data-ttu-id="8e63c-105">Sécurité et conformité des données/serveur</span><span class="sxs-lookup"><span data-stu-id="8e63c-105">Security and Server/Data Compliance</span></span>

### <a name="is-the-synced-data-encrypted"></a><span data-ttu-id="8e63c-106">Les données synchronisées sont-elles chiffrées?</span><span class="sxs-lookup"><span data-stu-id="8e63c-106">Is the synced data encrypted?</span></span>

<span data-ttu-id="8e63c-107">Les données sont cryptées lors du transport en utilisant TLS1.2 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8e63c-107">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="8e63c-108">Tous les types de données sont également chiffrés sur REST dans le service de Microsoft à l’aide de AES128.</span><span class="sxs-lookup"><span data-stu-id="8e63c-108">All data types are additionally encrypted at rest in Microsoft's service using AES128.</span></span> <span data-ttu-id="8e63c-109">Tous les types de données, à l’exception de ceux utilisés pour la synchronisation de l’onglet ouvert et de l’historique, sont chiffrés avant de laisser l’appareil de l’utilisateur avec des clés gérées via la stratégie [Azure Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="8e63c-109">All data types except those used for open tab and history sync are additionally encrypted before leaving the user’s device with keys managed via the [Azure Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

### <a name="why-dont-open-tab-and-history-data-have-more-client-side-encryption"></a><span data-ttu-id="8e63c-110">Pourquoi les données d’historique et d’onglets ouverts n’ont-elles pas davantage de chiffrement côté client?</span><span class="sxs-lookup"><span data-stu-id="8e63c-110">Why don’t open tab and history data have more client-side encryption?</span></span>

<span data-ttu-id="8e63c-111">Pour réduire l’utilisation des ressources sur les appareils des utilisateurs finaux, les données d’historique sont générées côté serveur en fonction des données d’itinérance de l’onglet ouvert.</span><span class="sxs-lookup"><span data-stu-id="8e63c-111">To reduce resource utilization on end-user devices, history data is generated server-side based on open tab roaming data.</span></span> <span data-ttu-id="8e63c-112">Ce processus n’est pas possible avec le chiffrement côté client de ces données.</span><span class="sxs-lookup"><span data-stu-id="8e63c-112">This process would not be possible with client-side encryption of this data.</span></span> <span data-ttu-id="8e63c-113">Pour désactiver la synchronisation des onglets et de l’historique, appliquez les stratégies [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) ou [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) .</span><span class="sxs-lookup"><span data-stu-id="8e63c-113">To disable open tab and history sync, apply the [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) or [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policies.</span></span>

### <a name="can-tenant-admins-bring-their-own-key"></a><span data-ttu-id="8e63c-114">Les administrateurs client peuvent-ils incorporer leur propre clé?</span><span class="sxs-lookup"><span data-stu-id="8e63c-114">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="8e63c-115">Oui, via [Azure information protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="8e63c-115">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

### <a name="where-is-microsoft-edge-sync-data-stored"></a><span data-ttu-id="8e63c-116">Où les données synchronisées de Microsoft Edge sont-elles stockées?</span><span class="sxs-lookup"><span data-stu-id="8e63c-116">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="8e63c-117">Les données synchronisées pour les comptes Azure AD sont stockées dans des serveurs sécurisés en fonction de l’ID de client.</span><span class="sxs-lookup"><span data-stu-id="8e63c-117">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="8e63c-118">Par exemple, les données d’un client enregistré aux États-Unis sont stockées dans des serveurs géolocalisés pour cette région et utilisent la même solution de stockage que celle des applications Office.</span><span class="sxs-lookup"><span data-stu-id="8e63c-118">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

### <a name="does-the-data-ever-leave-microsofts-cloud-aside-from-syncing-to-microsoft-edge"></a><span data-ttu-id="8e63c-119">Les données quittent-elles le cloud de Microsoft, en dehors de la synchronisation avec Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="8e63c-119">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="8e63c-120">Non.</span><span class="sxs-lookup"><span data-stu-id="8e63c-120">No.</span></span>

### <a name="what-terms-of-service-does-enterprise-sync-fall-under"></a><span data-ttu-id="8e63c-121">À quelles conditions d’utilisation la synchronisation d’entreprise répond-elle?</span><span class="sxs-lookup"><span data-stu-id="8e63c-121">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="8e63c-122">Les conditions d’utilisation de la synchronisation de Microsoft Edge relèvent du contrat de licence logiciel Microsoft affichable dans MicrosoftEdge sur *Edge://Terms*.</span><span class="sxs-lookup"><span data-stu-id="8e63c-122">Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.</span></span> <span data-ttu-id="8e63c-123">Votre abonnement Azure AD et les conditions d’utilisation sont relèvent en dernier ressort des [conditions générales de service en ligne](https://www.microsoft.com/licensing/product-licensing/products)de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8e63c-123">Your Azure AD subscription and terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

### <a name="does-microsoft-edge-support-government-community-cloud-gcc-high-compliance"></a><span data-ttu-id="8e63c-124">Microsoft Edge prend-il en charge le cloud de la communauté du secteur public Community Cloud (GCC) High Compliance?</span><span class="sxs-lookup"><span data-stu-id="8e63c-124">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="8e63c-125">Pas à la date d'aujourd'hui.</span><span class="sxs-lookup"><span data-stu-id="8e63c-125">Not today.</span></span> <span data-ttu-id="8e63c-126">Pour les clients qui utilisent le Cloud HD de GCC, la synchronisation Microsoft Edge est désactivée.</span><span class="sxs-lookup"><span data-stu-id="8e63c-126">For customers in the GCC High cloud, Microsoft Edge sync is disabled.</span></span>

## <a name="applying-sync"></a><span data-ttu-id="8e63c-127">Application de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="8e63c-127">Applying Sync</span></span>

### <a name="why-isnt-microsoft-edge-sync-supported-in-all-m365-subscriptions"></a><span data-ttu-id="8e63c-128">Pourquoi la synchronisation MicrosoftEdge n’est-elle pas prise en charge dans tous les abonnements M365?</span><span class="sxs-lookup"><span data-stu-id="8e63c-128">Why isn’t Microsoft Edge sync supported in all M365 subscriptions?</span></span>

<span data-ttu-id="8e63c-129">La synchronisation d’entreprise dépend [d’Azure Information Protection,](https://azure.microsoft.com/services/information-protection/)qui n’est pas disponible dans tous les abonnements M365.</span><span class="sxs-lookup"><span data-stu-id="8e63c-129">Enterprise sync depends on [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), which is not available in all M365 subscriptions.</span></span>

### <a name="is-microsoft-edge-sync-based-on-enterprise-state-roaming"></a><span data-ttu-id="8e63c-130">Est-ce que la synchronisation de MicrosoftEdge se base sur Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="8e63c-130">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="8e63c-131">Non.</span><span class="sxs-lookup"><span data-stu-id="8e63c-131">No.</span></span> <span data-ttu-id="8e63c-132">Enterprise State Roaming (ESR) peut être utilisé pour activer la synchronisation, mais Microsoft Edge Sync ne fait pas partie de ESR.</span><span class="sxs-lookup"><span data-stu-id="8e63c-132">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="8e63c-133">Pour plus d’informations, consultez la [Synchronisation Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) et [Microsoft Edge et Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).</span><span class="sxs-lookup"><span data-stu-id="8e63c-133">For more information, see [Microsoft Edge Sync](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) and [Microsoft Edge and Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).</span></span>

### <a name="will-microsoft-edge-ever-support-syncing-between-microsoft-edge-and-ie"></a><span data-ttu-id="8e63c-134">Microsoft Edge prend-il en charge la synchronisation entre Microsoft Edge et Internet Explorer?</span><span class="sxs-lookup"><span data-stu-id="8e63c-134">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="8e63c-135">Il n’existe pas d’offre pour la prise en charge de cette synchronisation.</span><span class="sxs-lookup"><span data-stu-id="8e63c-135">There are no plans to support this syncing.</span></span> <span data-ttu-id="8e63c-136">Si vous avez encore besoin d’Internet Explorer dans votre environnement pour prendre en charge des applications héritées, nous vous conseillons le [Nouveau mode Internet Explorer](https://docs.microsoft.com/deployedge/edge-ie-mode).</span><span class="sxs-lookup"><span data-stu-id="8e63c-136">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

### <a name="will-microsoft-edge-sync-with-microsoft-edge-legacy"></a><span data-ttu-id="8e63c-137">Est-ce que Microsoft Edge se synchronise avec Microsoft Edge hérité?</span><span class="sxs-lookup"><span data-stu-id="8e63c-137">Will Microsoft Edge sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="8e63c-138">Non.</span><span class="sxs-lookup"><span data-stu-id="8e63c-138">No, it won't.</span></span> <span data-ttu-id="8e63c-139">Nous pensons que la connexion de ces deux écosystèmes entraîne la compromission de la fiabilité de la synchronisation dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8e63c-139">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the Microsoft Edge.</span></span> <span data-ttu-id="8e63c-140">Nous allons garantir la migration des données existantes vers MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="8e63c-140">We will ensure that existing data is migrated to the Microsoft Edge.</span></span> <span data-ttu-id="8e63c-141">Les utilisateurs pourront également importer des données à partir du navigateur de leur choix, ce qui signifie également que MicrosoftEdge ne pourra pas se synchroniser avec InternetExplorer.</span><span class="sxs-lookup"><span data-stu-id="8e63c-141">Users will also be able to import data from browser of their choice, which also means that Microsoft Edge won't have a way to sync with IE.</span></span>

## <a name="managing-sync"></a><span data-ttu-id="8e63c-142">Gérer la synchronisation</span><span class="sxs-lookup"><span data-stu-id="8e63c-142">Managing Sync</span></span>

### <a name="is-it-possible-to-stop-my-users-from-syncing-with-a-personal-tenant"></a><span data-ttu-id="8e63c-143">Est-il possible d’empêcher la synchronisation de mes utilisateurs avec un client personnel?</span><span class="sxs-lookup"><span data-stu-id="8e63c-143">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="8e63c-144">Pas directement, mais vous pouvez déterminer quels profils peuvent se connecter à Microsoft Edge à l’aide de la stratégie [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="8e63c-144">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e63c-145">Voir également</span><span class="sxs-lookup"><span data-stu-id="8e63c-145">See also</span></span>

- [<span data-ttu-id="8e63c-146">Synchronisation de MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="8e63c-146">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="8e63c-147">MicrosoftEdge et Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="8e63c-147">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="8e63c-148">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="8e63c-148">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
