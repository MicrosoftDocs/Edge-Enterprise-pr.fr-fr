---
title: Synchronisation de Microsoft Edge Entreprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 09/15/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Synchronisation de Microsoft Edge Entreprise
ms.openlocfilehash: d9cd643142d0f6744664a5071c5000b820583e41
ms.sourcegitcommit: 06c365faeea6070f103fe867cc2da13539ae4680
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2020
ms.locfileid: "11016343"
---
# <span data-ttu-id="caa41-103">Synchronisation de Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="caa41-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="caa41-104">Cet article explique comment utiliser MicrosoftEdge pour synchroniser vos favoris, vos mots de passe et d’autres données de navigateur sur tous vos appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="caa41-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="caa41-105">Cet article concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="caa41-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="caa41-106">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="caa41-106">Overview</span></span>

<span data-ttu-id="caa41-107">La synchronisation de MicrosoftEdge permet aux utilisateurs d’accéder à leurs données de navigation sur tous leurs appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="caa41-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="caa41-108">Les données prises en charge par la synchronisation sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="caa41-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="caa41-109">Favoris</span><span class="sxs-lookup"><span data-stu-id="caa41-109">Favorites</span></span>
- <span data-ttu-id="caa41-110">Mots de passe</span><span class="sxs-lookup"><span data-stu-id="caa41-110">Passwords</span></span>
- <span data-ttu-id="caa41-111">Adresses et autres (remplissage de formulaire)</span><span class="sxs-lookup"><span data-stu-id="caa41-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="caa41-112">Regroupements</span><span class="sxs-lookup"><span data-stu-id="caa41-112">Collections</span></span>
- <span data-ttu-id="caa41-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="caa41-113">Settings</span></span>
- <span data-ttu-id="caa41-114">Historique de navigation</span><span class="sxs-lookup"><span data-stu-id="caa41-114">Browsing history</span></span>
- <span data-ttu-id="caa41-115">Ouvrir les onglets</span><span class="sxs-lookup"><span data-stu-id="caa41-115">Open tabs</span></span>

<span data-ttu-id="caa41-116">La fonctionnalité de synchronisation est activée après accord de l’utilisateur et les utilisateurs peuvent activer ou désactiver la synchronisation pour chacun des types de données répertoriés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="caa41-116">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="caa41-117">Des données de configuration et de connectivité des appareils supplémentaires (telles que le nom, la marque et le modèle de l’appareil) sont téléchargées pour prendre en charge la fonctionnalité de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="caa41-117">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="caa41-118">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="caa41-118">Prerequisites</span></span>

<span data-ttu-id="caa41-119">La synchronisation Microsoft Edge pour les comptes Azure Active Directory (Azure AD) est disponible pour les abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="caa41-119">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="caa41-120">Azure AD Premium (P1 et P2)</span><span class="sxs-lookup"><span data-stu-id="caa41-120">Azure AD Premium (P1 and P2)</span></span>
- <span data-ttu-id="caa41-121">M365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="caa41-121">M365 Business Premium</span></span>
- <span data-ttu-id="caa41-122">Office365 E3 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="caa41-122">Office 365 E3 and above</span></span>
- <span data-ttu-id="caa41-123">Azure Information Protection (AIP) (P1& P2)</span><span class="sxs-lookup"><span data-stu-id="caa41-123">Azure Information Protection (AIP) (P1& P2)</span></span>
- <span data-ttu-id="caa41-124">Tous les abonnements à EDU (Microsoft Apps pour les étudiants ou la faculté, Exchange Online pour les étudiants ou la faculté, O365 A1 ou supérieur, M365 A1 ou supérieur, ou Azure Information Protection P1 ou P2 pour les étudiants ou la faculté)</span><span class="sxs-lookup"><span data-stu-id="caa41-124">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <span data-ttu-id="caa41-125">Configurer la synchronisation avec Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="caa41-125">Configuring Microsoft Edge sync</span></span>

<span data-ttu-id="caa41-126">Les options de configuration pour Microsoft Edge se synchronisent via le service Azure Information Protection (AIP).</span><span class="sxs-lookup"><span data-stu-id="caa41-126">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="caa41-127">Lorsque l'AIP est activé pour un locataire, tous les utilisateurs peuvent synchroniser les données Microsoft Edge, quelle que soit leur licence.</span><span class="sxs-lookup"><span data-stu-id="caa41-127">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="caa41-128">Vous trouverez les instructions relatives à l’activation d’AIP [ici](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="caa41-128">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="caa41-129">Pour limiter la synchronisation à certains groupes d'utilisateurs, vous pouvez activer [la politique de contrôle à l'embarquement AIP ](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) pour ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="caa41-129">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) for those users.</span></span> <span data-ttu-id="caa41-130">Si la synchronisation n'est toujours pas disponible après s'être assuré que tous les utilisateurs nécessaires sont embarqués, assurez-vous que le service IPCv3Service est activé en utilisant le cmdlet [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps) PowerShell.</span><span class="sxs-lookup"><span data-stu-id="caa41-130">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="caa41-131">L'activation de la protection des informations Azure permettra également à d'autres applications, telles que Microsoft Word ou Microsoft Outlook, de protéger les contenus grâce à l'AIP.</span><span class="sxs-lookup"><span data-stu-id="caa41-131">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="caa41-132">En outre, toute politique de contrôle à l'embarquement utilisée pour restreindre la synchronisation Edge empêchera également d'autres applications de protéger le contenu utilisant l'AIP.</span><span class="sxs-lookup"><span data-stu-id="caa41-132">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <span data-ttu-id="caa41-133">MicrosoftEdge et Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="caa41-133">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="caa41-134">Le nouveau MicrosoftEdge est une application multiplateforme avec une portée étendue pour la synchronisation des données utilisateur sur tous leurs appareils. Il ne fait plus partie d’Azure AD Enterprise State Roaming.</span><span class="sxs-lookup"><span data-stu-id="caa41-134">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="caa41-135">Toutefois, la nouvelle version de MicrosoftEdge remplira les promesses de protection des données d’ESR, par exemple la possibilité de proposer votre propre clé.</span><span class="sxs-lookup"><span data-stu-id="caa41-135">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="caa41-136">Pour plus d’informations, consultez [Microsoft Edge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="caa41-136">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="caa41-137">Stratégies de groupe de synchronisation</span><span class="sxs-lookup"><span data-stu-id="caa41-137">Sync group policies</span></span>

<span data-ttu-id="caa41-138">Les stratégies de groupe suivantes affectent la synchronisation de MicrosoftEdge:</span><span class="sxs-lookup"><span data-stu-id="caa41-138">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="caa41-139">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): désactive complètement la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="caa41-139">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="caa41-140">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): désactive l’enregistrement de l’historique de navigation et la synchronisation. Cette stratégie permet également de désactiver la synchronisation des onglets ouverts.</span><span class="sxs-lookup"><span data-stu-id="caa41-140">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="caa41-141">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): permet de configurer la liste des types exclus de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="caa41-141">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="caa41-142">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): permet aux profils Active Directory (AD) d'utiliser le stockage sur site.</span><span class="sxs-lookup"><span data-stu-id="caa41-142">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="caa41-143">Pour plus d'informations, voir [Synchronisation sur site pour les utilisateurs d'Active Directory (AD) ](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span><span class="sxs-lookup"><span data-stu-id="caa41-143">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="caa41-144">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync) :  Active la synchronisation par défaut et ne nécessite pas le consentement de l'utilisateur pour la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="caa41-144">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn sync on by default and do not require user consent to sync.</span></span>  

## <span data-ttu-id="caa41-145">Forum Aux Questions</span><span class="sxs-lookup"><span data-stu-id="caa41-145">Frequently Asked Questions</span></span>

### <span data-ttu-id="caa41-146">SÉCURITÉ et CONFORMITÉ DES DONNÉES/SERVEUR</span><span class="sxs-lookup"><span data-stu-id="caa41-146">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="caa41-147">Les données synchronisées sont-elles chiffrées?</span><span class="sxs-lookup"><span data-stu-id="caa41-147">Is the synced data encrypted?</span></span> 

<span data-ttu-id="caa41-148">Les données sont cryptées lors du transport en utilisant TLS 1.2 ou plus.</span><span class="sxs-lookup"><span data-stu-id="caa41-148">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="caa41-149">La plupart des types de données sont en outre cryptés au repos dans le service de Microsoft à l'aide d'AES256, à l'exception des types de données de l'historique du navigateur et des onglets ouverts.</span><span class="sxs-lookup"><span data-stu-id="caa41-149">Most data types are additionally encrypted at rest in Microsoft's service using AES256, with the exception of the browser history and open tabs datatypes.</span></span> <span data-ttu-id="caa41-150">Pour empêcher ces types de données de se synchroniser, vous pouvez appliquer la politique [SavingBrowserHistoryDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#savingbrowserhistorydisabled).</span><span class="sxs-lookup"><span data-stu-id="caa41-150">To prevent these data types from syncing, you can apply the [SavingBrowserHistoryDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#savingbrowserhistorydisabled) policy.</span></span>

#### <span data-ttu-id="caa41-151">Où les données Microsoft Edge synchronisées de sont-elles stockées?</span><span class="sxs-lookup"><span data-stu-id="caa41-151">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="caa41-152">Les données synchronisées pour les comptes Azure AD sont stockées dans des serveurs sécurisés en fonction de l’ID de client.</span><span class="sxs-lookup"><span data-stu-id="caa41-152">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="caa41-153">Par exemple, les données d’un client enregistré aux États-Unis sont stockées dans des serveurs géolocalisés pour cette région et utilisent la même solution de stockage que celle des applications Office.</span><span class="sxs-lookup"><span data-stu-id="caa41-153">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="caa41-154">Les données quittent-elles le cloud de Microsoft, en dehors de la synchronisation avec Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="caa41-154">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="caa41-155">Non.</span><span class="sxs-lookup"><span data-stu-id="caa41-155">No.</span></span>

#### <span data-ttu-id="caa41-156">Les administrateurs client peuvent-ils incorporer leur propre clé?</span><span class="sxs-lookup"><span data-stu-id="caa41-156">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="caa41-157">Oui, activer [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="caa41-157">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="caa41-158">À quelles conditions de service la synchronisation d’entreprise répond-elle?</span><span class="sxs-lookup"><span data-stu-id="caa41-158">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="caa41-159">Les conditions de service sont identiques à celles de votre abonnement Azure AD.</span><span class="sxs-lookup"><span data-stu-id="caa41-159">The terms of service are the same terms as your Azure AD subscription.</span></span> <span data-ttu-id="caa41-160">Toutes les conditions de service Azure AD vont répondre aux [Conditions de service en ligne](https://www.microsoft.com/licensing/product-licensing/products) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="caa41-160">All the Azure AD terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="caa41-161">Microsoft Edge prend-il en charge le cloud de la communauté du secteur public Community Cloud (GCC) High Compliance?</span><span class="sxs-lookup"><span data-stu-id="caa41-161">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="caa41-162">Pas à la date d'aujourd'hui.</span><span class="sxs-lookup"><span data-stu-id="caa41-162">Not today.</span></span> <span data-ttu-id="caa41-163">GCC High est de niveau D, tandis que Microsoft Edge prend en charge le niveau C.</span><span class="sxs-lookup"><span data-stu-id="caa41-163">GCC High is Tier D, while Microsoft Edge supports up to Tier C.</span></span>

### <span data-ttu-id="caa41-164">APPLICATION DE LA SYNCHRONISATION</span><span class="sxs-lookup"><span data-stu-id="caa41-164">APPLYING SYNC</span></span>

#### <span data-ttu-id="caa41-165">Que se passe-t-il avec les clients entreprise et éducation qui décident de conserver la version héritée de MicrosoftEdge?</span><span class="sxs-lookup"><span data-stu-id="caa41-165">What happens with enterprise and educational customers who decide to stay with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="caa41-166">La version actuelle du navigateur MicrosoftEdge continuera à faire partie de l’offre ESR.</span><span class="sxs-lookup"><span data-stu-id="caa41-166">The current version of Microsoft Edge browser will continue to participate in the ESR offering.</span></span>

#### <span data-ttu-id="caa41-167">Pourquoi ai-je besoin d’un abonnement Azure AD Premium pour la synchronisation?</span><span class="sxs-lookup"><span data-stu-id="caa41-167">Why do I need a premium Azure AD subscription to sync?</span></span>

<span data-ttu-id="caa41-168">La synchronisation d’entreprise dépend d’Azure Information Protection, qui n’est pas disponible dans les niveaux Azure AD.</span><span class="sxs-lookup"><span data-stu-id="caa41-168">Enterprise sync depends on Azure Information Protection, which is not available in all Azure AD tiers.</span></span>

#### <span data-ttu-id="caa41-169">Est-ce que la synchronisation de MicrosoftEdge se base sur Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="caa41-169">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="caa41-170">Non.</span><span class="sxs-lookup"><span data-stu-id="caa41-170">No.</span></span> <span data-ttu-id="caa41-171">Enterprise State Roaming (ESR) peut être utilisé pour activer la synchronisation, mais Microsoft Edge Sync ne fait pas partie de ESR.</span><span class="sxs-lookup"><span data-stu-id="caa41-171">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="caa41-172">Pour plus d’informations, consultez la [Synchronisation Microsoft Edge](microsoft-edge-enterprise-sync.md) et [Microsoft Edge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="caa41-172">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="caa41-173">Microsoft Edge prend-il en charge la synchronisation entre Microsoft Edge et Internet Explorer?</span><span class="sxs-lookup"><span data-stu-id="caa41-173">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="caa41-174">Il n’existe pas d’offre pour la prise en charge de cette synchronisation.</span><span class="sxs-lookup"><span data-stu-id="caa41-174">There are no plans to support this syncing.</span></span> <span data-ttu-id="caa41-175">Si vous avez encore besoin d’IE dans votre environnement pour prendre en charge des applications héritées, nous vous conseillons le [Nouveau mode IE](https://docs.microsoft.com/deployedge/edge-ie-mode).</span><span class="sxs-lookup"><span data-stu-id="caa41-175">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="caa41-176">Le nouveau navigateur Microsoft Edge sera-t-il synchronisé avec Microsoft Edge Legacy?</span><span class="sxs-lookup"><span data-stu-id="caa41-176">Will the new Microsoft Edge browser sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="caa41-177">Non.</span><span class="sxs-lookup"><span data-stu-id="caa41-177">No, it won't.</span></span> <span data-ttu-id="caa41-178">Nous pensons que la connexion de ces deux écosystèmes entraînera des problèmes de fiabilité de la synchronisation dans le nouveau MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="caa41-178">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the new Microsoft Edge.</span></span> <span data-ttu-id="caa41-179">Nous nous assurerons que les données existantes seront migrées vers le nouveau MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="caa41-179">We will ensure that existing data is migrated to the new Microsoft Edge.</span></span> <span data-ttu-id="caa41-180">Les utilisateurs pourront également importer des données à partir du navigateur de leur choix.</span><span class="sxs-lookup"><span data-stu-id="caa41-180">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="caa41-181">Cela signifie également que le nouveau navigateur MicrosoftEdge ne disposera d’aucune méthode de synchronisation avec Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="caa41-181">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="caa41-182">GÉRER LA SYNCHRONISATION</span><span class="sxs-lookup"><span data-stu-id="caa41-182">MANAGING SYNC</span></span>

#### <span data-ttu-id="caa41-183">Est-il possible d’empêcher la synchronisation de mes utilisateurs avec un client personnel?</span><span class="sxs-lookup"><span data-stu-id="caa41-183">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="caa41-184">Pas directement, mais vous pouvez déterminer quels profils peuvent se connecter à Microsoft Edge à l’aide de la stratégie [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="caa41-184">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="caa41-185">Voir également</span><span class="sxs-lookup"><span data-stu-id="caa41-185">See also</span></span>

- [<span data-ttu-id="caa41-186">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="caa41-186">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="caa41-187">MicrosoftEdge et Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="caa41-187">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
