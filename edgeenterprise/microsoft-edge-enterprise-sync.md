---
title: Configurer la synchronisation d’entreprise Microsoft Edge
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Options d'administration et d'utilisation pour configurer Microsoft Edge afin de synchroniser les favoris, les mots de passe et d'autres données du navigateur.
ms.openlocfilehash: 93af96bd864f08bb17bb1d6f0669f602a56fd8ca
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448118"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a><span data-ttu-id="b4c13-103">Configurer la synchronisation d’entreprise Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b4c13-103">Configure Microsoft Edge enterprise sync</span></span>

<span data-ttu-id="b4c13-104">Cet article explique comment les administrateurs peuvent configurer Microsoft Edge pour synchroniser les favoris des utilisateurs, les mots de passe et d'autres données de navigation sur tous les appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="b4c13-104">This article explains how admins can configure Microsoft Edge to sync user favorites, passwords, and other browser data across all signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="b4c13-105">S'applique à Microsoft Edge version 77 ou ultérieure, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="b4c13-105">Applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <a name="overview"></a><span data-ttu-id="b4c13-106">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="b4c13-106">Overview</span></span>

<span data-ttu-id="b4c13-107">La synchronisation de MicrosoftEdge permet aux utilisateurs d’accéder à leurs données de navigation sur tous leurs appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="b4c13-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="b4c13-108">Les données prises en charge par la synchronisation sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="b4c13-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="b4c13-109">Favoris</span><span class="sxs-lookup"><span data-stu-id="b4c13-109">Favorites</span></span>
- <span data-ttu-id="b4c13-110">Mots de passe</span><span class="sxs-lookup"><span data-stu-id="b4c13-110">Passwords</span></span>
- <span data-ttu-id="b4c13-111">Adresses et autres (remplissage de formulaire)</span><span class="sxs-lookup"><span data-stu-id="b4c13-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="b4c13-112">Regroupements</span><span class="sxs-lookup"><span data-stu-id="b4c13-112">Collections</span></span>
- <span data-ttu-id="b4c13-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4c13-113">Settings</span></span>
- <span data-ttu-id="b4c13-114">Extension</span><span class="sxs-lookup"><span data-stu-id="b4c13-114">Extension</span></span>
- <span data-ttu-id="b4c13-115">Ouvrir des onglets (disponible dans la version88 de MicrosoftEdge)</span><span class="sxs-lookup"><span data-stu-id="b4c13-115">Open tabs (available in Microsoft Edge version 88)</span></span>
- <span data-ttu-id="b4c13-116">Historique (disponible dans la version88 de MicrosoftEdge)</span><span class="sxs-lookup"><span data-stu-id="b4c13-116">History (available in Microsoft Edge version 88)</span></span>

<span data-ttu-id="b4c13-117">La fonctionnalité de synchronisation est activée après accord de l’utilisateur et les utilisateurs peuvent activer ou désactiver la synchronisation pour chacun des types de données répertoriés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="b4c13-117">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span> <span data-ttu-id="b4c13-118">Si un utilisateur rencontre un problème de synchronisation, il peut avoir besoin de réinitialiser la synchronisation dans **Paramètres** > \*\* Profils\*\* > \*\* Réinitialiser la synchronisation\*\*.</span><span class="sxs-lookup"><span data-stu-id="b4c13-118">If a user is experiencing a sync issue they might need to reset sync in **Settings** > **Profiles** > **Reset sync**.</span></span>

> [!NOTE]
> <span data-ttu-id="b4c13-119">Des données supplémentaires de connectivité et de configuration de l'appareil (telles que le nom, la marque et le modèle de l'appareil) sont téléchargées pour prendre en charge la fonctionnalité de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="b4c13-119">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b4c13-120">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="b4c13-120">Prerequisites</span></span>

<span data-ttu-id="b4c13-121">La synchronisation MicrosoftEdge pour les comptes Azure Active Directory (Azure AD) est disponible pour les abonnements suivants:</span><span class="sxs-lookup"><span data-stu-id="b4c13-121">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="b4c13-122">Azure AD Premium (P1 ou P2)</span><span class="sxs-lookup"><span data-stu-id="b4c13-122">Azure AD Premium (P1 or P2)</span></span>
- <span data-ttu-id="b4c13-123">M365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="b4c13-123">M365 Business Premium</span></span>
- <span data-ttu-id="b4c13-124">Office365E1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="b4c13-124">Office 365 E1 and above</span></span>
- <span data-ttu-id="b4c13-125">Protection d’information d’Azure (AIP) (P1 ou P2)</span><span class="sxs-lookup"><span data-stu-id="b4c13-125">Azure Information Protection (AIP) (P1 or P2)</span></span>
- <span data-ttu-id="b4c13-126">Tous les abonnements à EDU (Microsoft Apps pour les étudiants ou la faculté, Exchange Online pour les étudiants ou la faculté, O365 A1 ou supérieur, M365 A1 ou supérieur, ou Azure Information Protection P1 ou P2 pour les étudiants ou la faculté)</span><span class="sxs-lookup"><span data-stu-id="b4c13-126">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <a name="sync-group-policies"></a><span data-ttu-id="b4c13-127">Stratégies de groupe de synchronisation</span><span class="sxs-lookup"><span data-stu-id="b4c13-127">Sync group policies</span></span>

<span data-ttu-id="b4c13-128">Les administrateurs peuvent utiliser les stratégies de groupe suivantes pour configurer et gérer la synchronisation de Microsoft Edge :</span><span class="sxs-lookup"><span data-stu-id="b4c13-128">Admins can use the following group policies to configure and manage Microsoft Edge sync:</span></span>

- <span data-ttu-id="b4c13-129">[SyncDisabled](./microsoft-edge-policies.md#syncdisabled): désactive complètement la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="b4c13-129">[SyncDisabled](./microsoft-edge-policies.md#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="b4c13-130">[SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): désactive l’enregistrement de l’historique de navigation et la synchronisation. Cette stratégie permet également de désactiver la synchronisation des onglets ouverts.</span><span class="sxs-lookup"><span data-stu-id="b4c13-130">[SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="b4c13-131">[AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): si cette stratégie est définie sur Désactivé, la synchronisation de l’historique sera également désactivée.</span><span class="sxs-lookup"><span data-stu-id="b4c13-131">[AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.</span></span>
- <span data-ttu-id="b4c13-132">[SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): permet de configurer la liste des types exclus de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="b4c13-132">[SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="b4c13-133">[RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): permet aux profils Active Directory (AD) d'utiliser le stockage sur site.</span><span class="sxs-lookup"><span data-stu-id="b4c13-133">[RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="b4c13-134">Pour plus d'informations, voir [Synchronisation sur site pour les utilisateurs d'Active Directory (AD)](./microsoft-edge-on-premises-sync.md).</span><span class="sxs-lookup"><span data-stu-id="b4c13-134">For more information, see [On-premises sync for Active Directory (AD) users](./microsoft-edge-on-premises-sync.md).</span></span>
- <span data-ttu-id="b4c13-135">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): activez la synchronisation par défaut et n’exigez pas le consentement de l’utilisateur pour la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="b4c13-135">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn on sync by default and do not require user consent to sync.</span></span>  

## <a name="configure-microsoft-edge-sync"></a><span data-ttu-id="b4c13-136">Configurer la synchronisation de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="b4c13-136">Configure Microsoft Edge sync</span></span>

<span data-ttu-id="b4c13-137">Les options de configuration pour la synchronisation de MicrosoftEdge sont disponibles via le service Azure Information Protection (AIP).</span><span class="sxs-lookup"><span data-stu-id="b4c13-137">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="b4c13-138">Lorsque l'AIP est activé pour un locataire, tous les utilisateurs peuvent synchroniser les données Microsoft Edge, quelle que soit leur licence.</span><span class="sxs-lookup"><span data-stu-id="b4c13-138">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="b4c13-139">Vous trouverez les instructions relatives à l’activation d’AIP [ici](/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="b4c13-139">Instructions on how to enable AIP can be found [here](/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="b4c13-140">Pour limiter la synchronisation à certains groupes d'utilisateurs, vous pouvez activer [la politique de contrôle à l'embarquement AIP ](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) pour ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b4c13-140">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) for those users.</span></span> <span data-ttu-id="b4c13-141">Si la synchronisation n'est toujours pas disponible après s'être assuré que tous les utilisateurs nécessaires sont embarqués, assurez-vous que le service IPCv3Service est activé en utilisant le cmdlet [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps) PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4c13-141">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="b4c13-142">L'activation de la protection des informations Azure permettra également à d'autres applications, telles que Microsoft Word ou Microsoft Outlook, de protéger les contenus grâce à l'AIP.</span><span class="sxs-lookup"><span data-stu-id="b4c13-142">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="b4c13-143">En outre, toute politique de contrôle à l'embarquement utilisée pour restreindre la synchronisation MicrosoftEdge empêchera également d'autres applications de protéger le contenu utilisant AzureInformationProtection (AIP).</span><span class="sxs-lookup"><span data-stu-id="b4c13-143">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a><span data-ttu-id="b4c13-144">MicrosoftEdge et Enterprise State Roaming (ESR)</span><span class="sxs-lookup"><span data-stu-id="b4c13-144">Microsoft Edge and Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="b4c13-145">MicrosoftEdge est une application multiplateforme avec une étendue développée pour la synchronisation des données utilisateur sur tous leurs appareils et ne fait plus partie d’Azure AD Enterprise State Roaming.</span><span class="sxs-lookup"><span data-stu-id="b4c13-145">Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="b4c13-146">Toutefois, MicrosoftEdge remplit les promesses de protection des données d’Enterprise State Roaming, telles que la possibilité d’apporter votre propre clé.</span><span class="sxs-lookup"><span data-stu-id="b4c13-146">However, the Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="b4c13-147">Pour plus d’informations, consultez [MicrosoftEdge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="b4c13-147">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b4c13-148">Voir également</span><span class="sxs-lookup"><span data-stu-id="b4c13-148">See also</span></span>

- [<span data-ttu-id="b4c13-149">Synchronisation de MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="b4c13-149">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="b4c13-150">Diagnostiquer et résoudre les problèmes de synchronisation de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b4c13-150">Diagnose and fix Microsoft Edge sync issues</span></span>](microsoft-edge-troubleshoot-enterprise-sync.md)
- [<span data-ttu-id="b4c13-151">MicrosoftEdge et Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="b4c13-151">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="b4c13-152">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="b4c13-152">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)