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
# <span data-ttu-id="85247-103">Synchronisation de Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="85247-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="85247-104">Cet article explique comment utiliser MicrosoftEdge pour synchroniser vos favoris, vos mots de passe et d’autres données de navigateur sur tous vos appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="85247-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="85247-105">Cet article concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85247-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="85247-106">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="85247-106">Overview</span></span>

<span data-ttu-id="85247-107">La synchronisation de MicrosoftEdge permet aux utilisateurs d’accéder à leurs données de navigation sur tous leurs appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="85247-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="85247-108">Les données prises en charge par la synchronisation sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="85247-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="85247-109">Favoris</span><span class="sxs-lookup"><span data-stu-id="85247-109">Favorites</span></span>
- <span data-ttu-id="85247-110">Mots de passe</span><span class="sxs-lookup"><span data-stu-id="85247-110">Passwords</span></span>
- <span data-ttu-id="85247-111">Adresses et autres (remplissage de formulaire)</span><span class="sxs-lookup"><span data-stu-id="85247-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="85247-112">Regroupements</span><span class="sxs-lookup"><span data-stu-id="85247-112">Collections</span></span>
- <span data-ttu-id="85247-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85247-113">Settings</span></span>

<span data-ttu-id="85247-114">La fonctionnalité de synchronisation est activée après accord de l’utilisateur et les utilisateurs peuvent activer ou désactiver la synchronisation pour chacun des types de données répertoriés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="85247-114">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="85247-115">Des données de configuration et de connectivité des appareils supplémentaires (telles que le nom, la marque et le modèle de l’appareil) sont téléchargées pour prendre en charge la fonctionnalité de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="85247-115">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="85247-116">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="85247-116">Prerequisites</span></span>

<span data-ttu-id="85247-117">Actuellement, la synchronisation de MicrosoftEdge pour les comptes Azure Active Directory (Azure AD) est disponible pour les abonnements suivants:</span><span class="sxs-lookup"><span data-stu-id="85247-117">Currently Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for the following subscriptions:</span></span>

- <span data-ttu-id="85247-118">Azure AD Premium (P1 et P2)</span><span class="sxs-lookup"><span data-stu-id="85247-118">Azure AD Premium (P1 and P2)</span></span>
- <span data-ttu-id="85247-119">M365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="85247-119">M365 Business Premium</span></span>
- <span data-ttu-id="85247-120">Office365 E3 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="85247-120">Office 365 E3 and above</span></span>
- <span data-ttu-id="85247-121">Azure Information Protection (AIP) (P1& P2)</span><span class="sxs-lookup"><span data-stu-id="85247-121">Azure Information Protection (AIP) (P1& P2)</span></span>
- <span data-ttu-id="85247-122">Tous les abonnements EDU (O365A1 ou version ultérieure, M365A1 version ultérieure, ou Azure Protection InformationP1 ou P2 pour étudiants ou université)</span><span class="sxs-lookup"><span data-stu-id="85247-122">All EDU subscriptions (O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

> [!NOTE]
> <span data-ttu-id="85247-123">La synchronisation a une dépendance envers le service de protection offert par Azure Information Protection (AIP) pour protéger les données de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="85247-123">Sync has a dependency on the protection service offered by Azure Information Protection (AIP) to protect sync data.</span></span> <span data-ttu-id="85247-124">Ce service est actuellement disponible pour les abonnements précédents.</span><span class="sxs-lookup"><span data-stu-id="85247-124">This service is currently available to the preceding subscriptions.</span></span> <span data-ttu-id="85247-125">Pour afficher la liste complète des références SKU avec AIP consultez, [Tarification d’Information Protection](https://azure.microsoft.com/pricing/details/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="85247-125">To see the full list of SKUs with AIP, see [Information Protection Pricing](https://azure.microsoft.com/pricing/details/information-protection/).</span></span>

## <span data-ttu-id="85247-126">Options de configurations de la synchronisation de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="85247-126">Configuration options for Microsoft Edge sync</span></span>

<span data-ttu-id="85247-127">Les options de configuration suivantes sont disponibles pour activer la synchronisation de MicrosoftEdge:</span><span class="sxs-lookup"><span data-stu-id="85247-127">The following configuration options are available for enabling Microsoft Edge sync:</span></span>

- <span data-ttu-id="85247-128">Azure Information Protection (AIP)</span><span class="sxs-lookup"><span data-stu-id="85247-128">Azure Information Protection (AIP)</span></span>
- <span data-ttu-id="85247-129">Azure AD Enterprise State Roaming (ESR)</span><span class="sxs-lookup"><span data-stu-id="85247-129">Azure AD Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="85247-130">Si les paramètres AIP et ESR sont désactivés, les utilisateurs verront un message d’erreur indiquant que la synchronisation n’est pas disponible pour leur compte.</span><span class="sxs-lookup"><span data-stu-id="85247-130">If both AIP and ESR are disabled, users will see an error message indicating that sync is not available for their account.</span></span>

### <span data-ttu-id="85247-131">Azure Information Protection (AIP)</span><span class="sxs-lookup"><span data-stu-id="85247-131">Azure Information Protection (AIP)</span></span>

<span data-ttu-id="85247-132">Si le service Azure Information Protection (AIP) est activé pour un client, tous les utilisateurs peuvent synchroniser les données MicrosoftEdge, quelle que soit la licence.</span><span class="sxs-lookup"><span data-stu-id="85247-132">If the Azure Information Protection (AIP) service is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="85247-133">Vous trouverez les instructions relatives à l’activation d’AIP [ici](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="85247-133">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="85247-134">Pour limiter la synchronisation à certains ensembles d’utilisateurs, vous pouvez activer la [ méthode de contrôle d’intégration AADRM](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) pour ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="85247-134">To restrict sync to certain set of users, you can enable the [AADRM onboarding control policy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) for those users.</span></span> <span data-ttu-id="85247-135">Si la synchronisation n’est toujours pas disponible après vous être assuré que tous les utilisateurs nécessaires sont intégrés, assurez-vous que le IPCv3Service est activé à l’aide de l’applet de commande PowerShell de [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps).</span><span class="sxs-lookup"><span data-stu-id="85247-135">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps) PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="85247-136">L’activation de la Protection d’Information Azure limitera aussi l’accès pour d’autres applications utilisant AIP, telles que MicrosoftWord ou MicrosoftOutlook.</span><span class="sxs-lookup"><span data-stu-id="85247-136">Activating Azure Information Protection will also restrict access for other applications using AIP, such as Microsoft Word or Microsoft Outlook.</span></span>

### <span data-ttu-id="85247-137">Azure AD Enterprise State Roaming (ESR)</span><span class="sxs-lookup"><span data-stu-id="85247-137">Azure AD Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="85247-138">Si la fonctionnalité [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) d’Azure ActiveDirectory est activée pour un utilisateur ou un client, celui-ci peut utiliser la fonctionnalité de synchronisation de MicrosoftEdge, quel que soit le paramètre de stratégie de contrôle d’intégration.</span><span class="sxs-lookup"><span data-stu-id="85247-138">If the Azure Active Directory [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) feature is enabled for any user or tenant, they can use the Microsoft Edge sync feature regardless of the onboarding control policy setting.</span></span>

## <span data-ttu-id="85247-139">MicrosoftEdge et Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="85247-139">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="85247-140">Le nouveau MicrosoftEdge est une application multiplateforme avec une portée étendue pour la synchronisation des données utilisateur sur tous leurs appareils. Il ne fait plus partie d’Azure AD Enterprise State Roaming.</span><span class="sxs-lookup"><span data-stu-id="85247-140">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="85247-141">Toutefois, la nouvelle version de MicrosoftEdge remplira les promesses de protection des données d’ESR, par exemple la possibilité de proposer votre propre clé.</span><span class="sxs-lookup"><span data-stu-id="85247-141">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="85247-142">Pour plus d’informations, consultez [Microsoft Edge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="85247-142">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="85247-143">Stratégies de groupe de synchronisation</span><span class="sxs-lookup"><span data-stu-id="85247-143">Sync group policies</span></span>

<span data-ttu-id="85247-144">Les stratégies de groupe suivantes affectent la synchronisation de MicrosoftEdge:</span><span class="sxs-lookup"><span data-stu-id="85247-144">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="85247-145">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): désactive complètement la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="85247-145">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="85247-146">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): désactive l’enregistrement de l’historique de navigation et la synchronisation. Cette stratégie permet également de désactiver la synchronisation des onglets ouverts.</span><span class="sxs-lookup"><span data-stu-id="85247-146">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="85247-147">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): permet de configurer la liste des types exclus de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="85247-147">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>

## <span data-ttu-id="85247-148">Forum Aux Questions</span><span class="sxs-lookup"><span data-stu-id="85247-148">Frequently Asked Questions</span></span>

### <span data-ttu-id="85247-149">SÉCURITÉ et CONFORMITÉ DES DONNÉES/SERVEUR</span><span class="sxs-lookup"><span data-stu-id="85247-149">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="85247-150">Les données synchronisées sont-elles chiffrées?</span><span class="sxs-lookup"><span data-stu-id="85247-150">Is the synced data encrypted?</span></span> 

<span data-ttu-id="85247-151">Les données sont chiffrées dans le transport à l’aide de TLS 1.2 ou plus, et en outre, au repos dans le service Microsoft en utilisant l’ AES256.</span><span class="sxs-lookup"><span data-stu-id="85247-151">The data is encrypted in transport using TLS 1.2 or greater, and additionally at rest in Microsoft's service using AES256.</span></span>

#### <span data-ttu-id="85247-152">Où les données Microsoft Edge synchronisées de sont-elles stockées?</span><span class="sxs-lookup"><span data-stu-id="85247-152">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="85247-153">Les données synchronisées pour les comptes Azure AD sont stockées dans des serveurs sécurisés en fonction de l’ID de client.</span><span class="sxs-lookup"><span data-stu-id="85247-153">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="85247-154">Par exemple, les données d’un client enregistré aux États-Unis sont stockées dans des serveurs géolocalisés pour cette région et utilisent la même solution de stockage que celle des applications Office.</span><span class="sxs-lookup"><span data-stu-id="85247-154">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="85247-155">Les données quittent-elles le cloud de Microsoft, en dehors de la synchronisation avec Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="85247-155">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="85247-156">Non.</span><span class="sxs-lookup"><span data-stu-id="85247-156">No.</span></span>

#### <span data-ttu-id="85247-157">Les administrateurs client peuvent-ils incorporer leur propre clé?</span><span class="sxs-lookup"><span data-stu-id="85247-157">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="85247-158">Oui, activer [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="85247-158">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="85247-159">À quelles conditions de service la synchronisation d’entreprise répond-elle?</span><span class="sxs-lookup"><span data-stu-id="85247-159">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="85247-160">Les conditions de service sont identiques à celles de votre abonnement Azure AD.</span><span class="sxs-lookup"><span data-stu-id="85247-160">The terms of service are the same terms as your Azure AD subscription.</span></span> <span data-ttu-id="85247-161">Toutes les conditions de service Azure AD vont répondre aux [Conditions de service en ligne](https://www.microsoft.com/licensing/product-licensing/products) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="85247-161">All the Azure AD terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="85247-162">Microsoft Edge prend-il en charge le cloud de la communauté du secteur public Community Cloud (GCC) High Compliance?</span><span class="sxs-lookup"><span data-stu-id="85247-162">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="85247-163">Pas à la date d'aujourd'hui.</span><span class="sxs-lookup"><span data-stu-id="85247-163">Not today.</span></span> <span data-ttu-id="85247-164">GCC High est de niveau D, tandis que Microsoft Edge prend en charge le niveau C.</span><span class="sxs-lookup"><span data-stu-id="85247-164">GCC High is Tier D, while Microsoft Edge supports up to Tier C.</span></span>

### <span data-ttu-id="85247-165">APPLICATION DE LA SYNCHRONISATION</span><span class="sxs-lookup"><span data-stu-id="85247-165">APPLYING SYNC</span></span>

#### <span data-ttu-id="85247-166">Que se passe-t-il avec les clients entreprise et éducation qui décident de conserver la version héritée de MicrosoftEdge?</span><span class="sxs-lookup"><span data-stu-id="85247-166">What happens with enterprise and educational customers who decide to stay with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="85247-167">La version actuelle du navigateur MicrosoftEdge continuera à faire partie de l’offre ESR.</span><span class="sxs-lookup"><span data-stu-id="85247-167">The current version of Microsoft Edge browser will continue to participate in the ESR offering.</span></span>

#### <span data-ttu-id="85247-168">Pourquoi ai-je besoin d’un abonnement Azure AD Premium pour la synchronisation?</span><span class="sxs-lookup"><span data-stu-id="85247-168">Why do I need a premium Azure AD subscription to sync?</span></span>

<span data-ttu-id="85247-169">La synchronisation d’entreprise dépend d’Azure Information Protection, qui n’est pas disponible dans les niveaux Azure AD.</span><span class="sxs-lookup"><span data-stu-id="85247-169">Enterprise sync depends on Azure Information Protection, which is not available in all Azure AD tiers.</span></span>

#### <span data-ttu-id="85247-170">Est-ce que la synchronisation de MicrosoftEdge se base sur Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="85247-170">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="85247-171">Non.</span><span class="sxs-lookup"><span data-stu-id="85247-171">No.</span></span> <span data-ttu-id="85247-172">Enterprise State Roaming (ESR) peut être utilisé pour activer la synchronisation, mais Microsoft Edge Sync ne fait pas partie de ESR.</span><span class="sxs-lookup"><span data-stu-id="85247-172">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="85247-173">Pour plus d’informations, consultez la [Synchronisation Microsoft Edge](microsoft-edge-enterprise-sync.md) et [Microsoft Edge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="85247-173">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="85247-174">Microsoft Edge prend-il en charge la synchronisation entre Microsoft Edge et Internet Explorer?</span><span class="sxs-lookup"><span data-stu-id="85247-174">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="85247-175">Il n’existe pas d’offre pour la prise en charge de cette synchronisation.</span><span class="sxs-lookup"><span data-stu-id="85247-175">There are no plans to support this syncing.</span></span> <span data-ttu-id="85247-176">Si vous avez encore besoin d’IE dans votre environnement pour prendre en charge des applications héritées, nous vous conseillons le [Nouveau mode IE](https://docs.microsoft.com/deployedge/edge-ie-mode).</span><span class="sxs-lookup"><span data-stu-id="85247-176">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="85247-177">Le nouveau navigateur Microsoft Edge sera-t-il synchronisé avec Microsoft Edge Legacy?</span><span class="sxs-lookup"><span data-stu-id="85247-177">Will the new Microsoft Edge browser sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="85247-178">Non.</span><span class="sxs-lookup"><span data-stu-id="85247-178">No, it won't.</span></span> <span data-ttu-id="85247-179">Nous pensons que la connexion de ces deux écosystèmes entraînera des problèmes de fiabilité de la synchronisation dans le nouveau MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="85247-179">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the new Microsoft Edge.</span></span> <span data-ttu-id="85247-180">Nous nous assurerons que les données existantes seront migrées vers le nouveau MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="85247-180">We will ensure that existing data is migrated to the new Microsoft Edge.</span></span> <span data-ttu-id="85247-181">Les utilisateurs pourront également importer des données à partir du navigateur de leur choix.</span><span class="sxs-lookup"><span data-stu-id="85247-181">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="85247-182">Cela signifie également que le nouveau navigateur MicrosoftEdge ne disposera d’aucune méthode de synchronisation avec Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="85247-182">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="85247-183">GÉRER LA SYNCHRONISATION</span><span class="sxs-lookup"><span data-stu-id="85247-183">MANAGING SYNC</span></span>

#### <span data-ttu-id="85247-184">Est-il possible d’empêcher la synchronisation de mes utilisateurs avec un client personnel?</span><span class="sxs-lookup"><span data-stu-id="85247-184">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="85247-185">Pas directement, mais vous pouvez déterminer quels profils peuvent se connecter à Microsoft Edge à l’aide de la stratégie [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="85247-185">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="85247-186">Voir également</span><span class="sxs-lookup"><span data-stu-id="85247-186">See also</span></span>

- [<span data-ttu-id="85247-187">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="85247-187">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="85247-188">MicrosoftEdge et Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="85247-188">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
