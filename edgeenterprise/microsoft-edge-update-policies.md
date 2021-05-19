---
title: Documentation relative aux stratégies Microsoft Edge Update
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 10/07/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentation relative à toutes les stratégies prises en charge par le programme de mise à jour Microsoft Edge
ms.openlocfilehash: feb7859f062ae39e2bbfe08d8e478386defb85cf
ms.sourcegitcommit: 4e6188ade942ca6fd599a4ce1c8e0d90d3d03399
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "11105568"
---
# <span data-ttu-id="1a802-103">Microsoft Edge - Stratégies de mise à jour</span><span class="sxs-lookup"><span data-stu-id="1a802-103">Microsoft Edge - Update policies</span></span>
<span data-ttu-id="1a802-104">La dernière version de Microsoft Edge comprend les stratégies suivantes que vous pouvez utiliser pour contrôler comment et quand Microsoft Edge est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="1a802-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

<span data-ttu-id="1a802-105">Pour plus d’informations sur les autres stratégies disponibles dans Microsoft Edge, consultez la [Référence de stratégies du navigateur Microsoft Edge](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="1a802-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="1a802-106">Cet article concerne Microsoft Edge version 77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1a802-106">This article applies to Microsoft Edge version 77 or later.</span></span>
## <span data-ttu-id="1a802-107">Stratégies disponibles</span><span class="sxs-lookup"><span data-stu-id="1a802-107">Available policies</span></span>
<span data-ttu-id="1a802-108">Ces tableaux répertorient toutes les stratégies de groupe relatives aux mises à jour disponibles dans cette version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1a802-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="1a802-109">Utilisez les liens dans le tableau pour obtenir plus de détails sur des stratégies données.</span><span class="sxs-lookup"><span data-stu-id="1a802-109">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="1a802-110">Applications</span><span class="sxs-lookup"><span data-stu-id="1a802-110">Applications</span></span>](#applications)|[<span data-ttu-id="1a802-111">Préférences</span><span class="sxs-lookup"><span data-stu-id="1a802-111">Preferences</span></span>](#preferences)|
|[<span data-ttu-id="1a802-112">Serveur proxy</span><span class="sxs-lookup"><span data-stu-id="1a802-112">Proxy Server</span></span>](#proxy-server)|[<span data-ttu-id="1a802-113">Affichage web Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-113">Microsoft Edge WebView</span></span>](#microsoft-edge-webview)|

### [<span data-ttu-id="1a802-114">Applications</span><span class="sxs-lookup"><span data-stu-id="1a802-114">Applications</span></span>](#applications-policies)
|<span data-ttu-id="1a802-115">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="1a802-115">Policy Name</span></span>|<span data-ttu-id="1a802-116">Caption</span><span class="sxs-lookup"><span data-stu-id="1a802-116">Caption</span></span>|
|-|-|
|[<span data-ttu-id="1a802-117">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="1a802-117">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="1a802-118">Autoriser l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="1a802-118">Allow installation default</span></span>|
|[<span data-ttu-id="1a802-119">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="1a802-119">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="1a802-120">Remplacer la stratégie de mise à jour par défaut</span><span class="sxs-lookup"><span data-stu-id="1a802-120">Update policy override default</span></span>|
|[<span data-ttu-id="1a802-121">Install</span><span class="sxs-lookup"><span data-stu-id="1a802-121">Install</span></span>](#install)|<span data-ttu-id="1a802-122">Autoriser l’installation (par canal)</span><span class="sxs-lookup"><span data-stu-id="1a802-122">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="1a802-123">Update</span><span class="sxs-lookup"><span data-stu-id="1a802-123">Update</span></span>](#update)|<span data-ttu-id="1a802-124">Remplacer la stratégie de mise à jour (par canal)</span><span class="sxs-lookup"><span data-stu-id="1a802-124">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="1a802-125">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="1a802-125">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="1a802-126">Autoriser l’expérience de navigateur côte à côte Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-126">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="1a802-127">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="1a802-127">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="1a802-128">Empêcher la création du Raccourci Bureau lors de l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="1a802-128">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="1a802-129">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="1a802-129">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="1a802-130">Empêcher la création du Raccourci Bureau lors de l’installation (par canal)</span><span class="sxs-lookup"><span data-stu-id="1a802-130">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="1a802-131">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="1a802-131">RollbackToTargetVersion</span></span>](#rollbacktotargetversion)|<span data-ttu-id="1a802-132">Restaurez la version Cible (par canal)</span><span class="sxs-lookup"><span data-stu-id="1a802-132">Rollback to Target version (per channel)</span></span>|
|[<span data-ttu-id="1a802-133">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="1a802-133">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="1a802-134">Remplacement de la version cible (par canal)</span><span class="sxs-lookup"><span data-stu-id="1a802-134">Target version override (per channel)</span></span>|

### [<span data-ttu-id="1a802-135">Préférences</span><span class="sxs-lookup"><span data-stu-id="1a802-135">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="1a802-136">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="1a802-136">Policy Name</span></span>|<span data-ttu-id="1a802-137">Caption</span><span class="sxs-lookup"><span data-stu-id="1a802-137">Caption</span></span>|
|-|-|
|[<span data-ttu-id="1a802-138">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="1a802-138">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="1a802-139">Remplacement de la période de vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="1a802-139">Auto-update check period override</span></span>|
|[<span data-ttu-id="1a802-140">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="1a802-140">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="1a802-141">Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="1a802-141">Time period in each day to suppress auto-update check</span></span>|

### [<span data-ttu-id="1a802-142">Serveur proxy</span><span class="sxs-lookup"><span data-stu-id="1a802-142">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="1a802-143">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="1a802-143">Policy Name</span></span>|<span data-ttu-id="1a802-144">Légende</span><span class="sxs-lookup"><span data-stu-id="1a802-144">Caption</span></span>|
|-|-|
|[<span data-ttu-id="1a802-145">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="1a802-145">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="1a802-146">Choisir comment spécifier les paramètres du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="1a802-146">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="1a802-147">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="1a802-147">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="1a802-148">URL d’un fichier proxy. pac</span><span class="sxs-lookup"><span data-stu-id="1a802-148">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="1a802-149">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="1a802-149">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="1a802-150">Adresse ou URL du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="1a802-150">Address or URL of proxy server</span></span>|

### [<span data-ttu-id="1a802-151">Affichage web Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-151">Microsoft Edge WebView</span></span>](#microsoft-edge-webview-policies)
|<span data-ttu-id="1a802-152">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="1a802-152">Policy Name</span></span>|<span data-ttu-id="1a802-153">Caption</span><span class="sxs-lookup"><span data-stu-id="1a802-153">Caption</span></span>|
|-|-|
|[<span data-ttu-id="1a802-154">Installer</span><span class="sxs-lookup"><span data-stu-id="1a802-154">Install</span></span>](#install-webview)|<span data-ttu-id="1a802-155">Autoriser l’installation</span><span class="sxs-lookup"><span data-stu-id="1a802-155">Allow installation</span></span>|
|[<span data-ttu-id="1a802-156">Mettre à jour/Mise à jour</span><span class="sxs-lookup"><span data-stu-id="1a802-156">Update</span></span>](#update-webview)|<span data-ttu-id="1a802-157">Remplacer la stratégie de mise à jour</span><span class="sxs-lookup"><span data-stu-id="1a802-157">Update policy override</span></span>|

## <span data-ttu-id="1a802-158">Stratégies d’applications</span><span class="sxs-lookup"><span data-stu-id="1a802-158">Applications policies</span></span>

[<span data-ttu-id="1a802-159">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-159">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="1a802-160">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="1a802-160">InstallDefault</span></span>
#### <span data-ttu-id="1a802-161">Autoriser l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="1a802-161">Allow installation default</span></span>
><span data-ttu-id="1a802-162">Microsoft Edge Update 1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-162">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="1a802-163">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-163">Description</span></span>
<span data-ttu-id="1a802-164">Vous pouvez spécifier le comportement par défaut de tous les canaux pour autoriser ou bloquer Microsoft Edge sur les appareils liés à un domaine.</span><span class="sxs-lookup"><span data-stu-id="1a802-164">You can specify the default behavior of all channels to allow or block Microsoft Edge on domain-joined devices.</span></span>

<span data-ttu-id="1a802-165">Vous pouvez remplacer cette stratégie pour des canaux individuels en spécifiant la stratégie « [Autoriser l’installation](#install) » pour des canaux spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1a802-165">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="1a802-166">Si vous désactivez cette stratégie, l’installation de Microsoft Edge est bloquée.</span><span class="sxs-lookup"><span data-stu-id="1a802-166">If you disable this policy, the installation of Microsoft Edge is blocked.</span></span> <span data-ttu-id="1a802-167">Cela affecte uniquement l’installation du logiciel Microsoft Edge lorsque la stratégie «[Autoriser l’installation](#install)» est définie Non Configurée.</span><span class="sxs-lookup"><span data-stu-id="1a802-167">This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.</span></span>

<span data-ttu-id="1a802-168">Cette stratégie n’empêche pas Microsoft Edge Update de s’exécuter, ni les utilisateurs d’installer le logiciel Microsoft Edge en utilisant d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="1a802-168">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>

<span data-ttu-id="1a802-169">Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="1a802-169">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="1a802-170">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-170">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-171">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-171">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-172">Nom unique de la stratégie de groupe : InstallDefault</span><span class="sxs-lookup"><span data-stu-id="1a802-172">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="1a802-173">Nom de la stratégie de groupe : Autoriser l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="1a802-173">GP name: Allow installation default</span></span>
- <span data-ttu-id="1a802-174">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="1a802-174">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="1a802-175">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-175">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-176">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-176">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-177">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-177">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-178">Nom de la valeur : InstallDefault</span><span class="sxs-lookup"><span data-stu-id="1a802-178">Value Name: InstallDefault</span></span>
- <span data-ttu-id="1a802-179">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1a802-179">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="1a802-180">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-180">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="1a802-181">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-181">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="1a802-182">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="1a802-182">UpdateDefault</span></span>
#### <span data-ttu-id="1a802-183">Remplacer la stratégie de mise à jour par défaut</span><span class="sxs-lookup"><span data-stu-id="1a802-183">Update policy override default</span></span>
><span data-ttu-id="1a802-184">Microsoft Edge Update 1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-184">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="1a802-185">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-185">Description</span></span>
<span data-ttu-id="1a802-186">Permet de spécifier le comportement par défaut de tous les canaux concernant la façon dont Microsoft Edge Update gère les mises à jour disponibles pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1a802-186">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="1a802-187">Peut être remplacé pour des canaux individuels en spécifiant la stratégie « [Remplacer la stratégie de mise à jour](#update) » pour ces canaux spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1a802-187">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="1a802-188">Si vous activez cette stratégie, Microsoft Edge Update gère les mises à jour de Microsoft Edge en fonction de la façon dont vous configurez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a802-188">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="1a802-189">Toujours autoriser les mises à jour : les mises à jour sont toujours appliquées lorsqu’elles sont trouvées, soit par une recherche de mise à jour périodique, soit par une recherche de mise à jour manuelle.</span><span class="sxs-lookup"><span data-stu-id="1a802-189">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="1a802-190">Mises à jour automatiques en mode silencieux uniquement : les mises à jour sont appliquées uniquement lorsqu’elles sont trouvées par la recherche de mise à jour périodique.</span><span class="sxs-lookup"><span data-stu-id="1a802-190">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="1a802-191">Mises à jour manuelles uniquement : les mises à jour sont appliquées uniquement lorsque l’utilisateur exécute une recherche de mise à jour manuelle.</span><span class="sxs-lookup"><span data-stu-id="1a802-191">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="1a802-192">Mises à jour désactivées : les mises à jour ne sont jamais appliquées.</span><span class="sxs-lookup"><span data-stu-id="1a802-192">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="1a802-193">Si vous sélectionnez les mises à jour manuelles, vérifiez régulièrement si des mises à jour sont disponibles à l’aide du mécanisme de mise à jour manuelle de l’application, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1a802-193">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="1a802-194">Si vous désactivez les mises à jour, recherchez régulièrement les mises à jour et distribuez-les aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1a802-194">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="1a802-195">Si vous n’activez pas et ne configurez pas cette stratégie, Microsoft Edge Update gère les mises à jour disponibles, comme spécifié par la stratégie « [Remplacer la stratégie de mise à jour](#update) ».</span><span class="sxs-lookup"><span data-stu-id="1a802-195">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>

  <span data-ttu-id="1a802-196">Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="1a802-196">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="1a802-197">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-197">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-198">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-198">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-199">Nom unique de la stratégie de groupe : UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="1a802-199">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="1a802-200">Nom de la stratégie de groupe : Remplacer la stratégie de mise à jour par défaut</span><span class="sxs-lookup"><span data-stu-id="1a802-200">GP name: Update policy override default</span></span>
- <span data-ttu-id="1a802-201">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="1a802-201">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="1a802-202">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-202">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-203">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-203">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-204">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-204">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-205">Nom de la valeur : UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="1a802-205">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="1a802-206">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1a802-206">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="1a802-207">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-207">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="1a802-208">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-208">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="1a802-209">Install</span><span class="sxs-lookup"><span data-stu-id="1a802-209">Install</span></span>
#### <span data-ttu-id="1a802-210">Autoriser l’installation</span><span class="sxs-lookup"><span data-stu-id="1a802-210">Allow installation</span></span>
><span data-ttu-id="1a802-211">Microsoft Edge Update 1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-211">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="1a802-212">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-212">Description</span></span>
<span data-ttu-id="1a802-213">Spécifie si un canal de Microsoft Edge peut être installé sur des appareils liés à un domaine.</span><span class="sxs-lookup"><span data-stu-id="1a802-213">Specifies whether a Microsoft Edge channel can be installed on domain-joined devices.</span></span>

  <span data-ttu-id="1a802-214">Si vous activez cette stratégie pour un canal, l’installation de Microsoft Edge ne sera pas bloquée.</span><span class="sxs-lookup"><span data-stu-id="1a802-214">If you enable this policy for a channel, Microsoft Edge will not be blocked from installation.</span></span>

  <span data-ttu-id="1a802-215">Si vous désactivez cette stratégie pour un canal, l’installation de Microsoft Edge sera bloquée.</span><span class="sxs-lookup"><span data-stu-id="1a802-215">If you disable this policy for a channel, Microsoft Edge will be blocked from installation.</span></span>

  <span data-ttu-id="1a802-216">Si vous ne configurez pas cette stratégie pour un canal, la configuration de la stratégie «[Autoriser l’installation par défaut](#installdefault)» détermine si les utilisateurs peuvent installer ce canal de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1a802-216">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.</span></span>

  <span data-ttu-id="1a802-217">Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="1a802-217">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="1a802-218">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-218">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-219">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-219">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-220">Nom unique de la stratégie de groupe : Install</span><span class="sxs-lookup"><span data-stu-id="1a802-220">GP unique name: Install</span></span>
- <span data-ttu-id="1a802-221">Nom de la stratégie de groupe : Autoriser l’installation</span><span class="sxs-lookup"><span data-stu-id="1a802-221">GP name: Allow installation</span></span>
- <span data-ttu-id="1a802-222">Chemin de la stratégie de groupe :</span><span class="sxs-lookup"><span data-stu-id="1a802-222">GP path:</span></span> 
  - <span data-ttu-id="1a802-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="1a802-224">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="1a802-224">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="1a802-225">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="1a802-225">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="1a802-226">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="1a802-226">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="1a802-227">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-227">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-228">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-228">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-229">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-229">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-230">Nom de la valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-230">Value Name:</span></span> 
  - <span data-ttu-id="1a802-231">(Stable) : install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="1a802-231">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="1a802-232">(Beta) : install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="1a802-232">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="1a802-233">(Canary) : Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="1a802-233">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="1a802-234">(Dev) : Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="1a802-234">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="1a802-235">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1a802-235">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="1a802-236">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-236">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="1a802-237">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-237">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="1a802-238">Update</span><span class="sxs-lookup"><span data-stu-id="1a802-238">Update</span></span>
#### <span data-ttu-id="1a802-239">Remplacer la stratégie de mise à jour</span><span class="sxs-lookup"><span data-stu-id="1a802-239">Update policy override</span></span>
><span data-ttu-id="1a802-240">Microsoft Edge Update 1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-240">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="1a802-241">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-241">Description</span></span>
<span data-ttu-id="1a802-242">Spécifie comment Microsoft Edge Update gère les mises à jour disponibles à partir de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1a802-242">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

<span data-ttu-id="1a802-243">Si vous activez cette stratégie, Microsoft Edge Update gère les mises à jour de Microsoft Edge en fonction de la façon dont vous configurez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a802-243">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="1a802-244">Toujours autoriser les mises à jour : les mises à jour sont toujours appliquées lorsqu’elles sont trouvées, soit par une recherche de mise à jour périodique, soit par une recherche de mise à jour manuelle.</span><span class="sxs-lookup"><span data-stu-id="1a802-244">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
  - <span data-ttu-id="1a802-245">Mises à jour automatiques en mode silencieux uniquement : les mises à jour sont appliquées uniquement lorsqu’elles sont trouvées par la recherche de mise à jour périodique.</span><span class="sxs-lookup"><span data-stu-id="1a802-245">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
  - <span data-ttu-id="1a802-246">Mises à jour manuelles uniquement : les mises à jour sont appliquées uniquement lorsque l’utilisateur exécute une recherche de mise à jour manuelle.</span><span class="sxs-lookup"><span data-stu-id="1a802-246">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="1a802-247">(Toutes les applications n’offrent pas une interface pour cette option.)</span><span class="sxs-lookup"><span data-stu-id="1a802-247">(Not all apps provide an interface for this option.)</span></span>
  - <span data-ttu-id="1a802-248">Mises à jour désactivées : les mises à jour ne sont jamais appliquées.</span><span class="sxs-lookup"><span data-stu-id="1a802-248">Updates disabled: Updates are never applied.</span></span>

<span data-ttu-id="1a802-249">Si vous sélectionnez les mises à jour manuelles, vérifiez régulièrement si des mises à jour sont disponibles à l’aide du mécanisme de mise à jour manuelle de l’application, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1a802-249">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="1a802-250">Si vous désactivez les mises à jour, recherchez régulièrement les mises à jour et distribuez-les aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1a802-250">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

<span data-ttu-id="1a802-251">Si vous n’activez pas et ne configurez pas cette stratégie, Microsoft Edge Update gère les mises à jour disponibles, comme spécifié par la stratégie « [Remplacer la stratégie de mise à jour par défaut](#updatedefault) ».</span><span class="sxs-lookup"><span data-stu-id="1a802-251">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>

<span data-ttu-id="1a802-252">Si vous souhaitez en savoir plus, consultez [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406).</span><span class="sxs-lookup"><span data-stu-id="1a802-252">See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.</span></span>

<span data-ttu-id="1a802-253">Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="1a802-253">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="1a802-254">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-254">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-255">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-255">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-256">Nom unique de la stratégie de groupe : Update</span><span class="sxs-lookup"><span data-stu-id="1a802-256">GP unique name: Update</span></span>
- <span data-ttu-id="1a802-257">Nom de la stratégie de groupe : Remplacer la stratégie de mise à jour</span><span class="sxs-lookup"><span data-stu-id="1a802-257">GP name: Update policy override</span></span>
- <span data-ttu-id="1a802-258">Chemin de la stratégie de groupe :</span><span class="sxs-lookup"><span data-stu-id="1a802-258">GP path:</span></span> 
  - <span data-ttu-id="1a802-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="1a802-260">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="1a802-260">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="1a802-261">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="1a802-261">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="1a802-262">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="1a802-262">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="1a802-263">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-263">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-264">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-264">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-265">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-265">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-266">Nom de la valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-266">Value Name:</span></span> 
  - <span data-ttu-id="1a802-267">(Stable) : Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="1a802-267">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="1a802-268">(Beta) : Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="1a802-268">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="1a802-269">(Canary) : Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="1a802-269">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="1a802-270">(Dev) : Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="1a802-270">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="1a802-271">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1a802-271">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="1a802-272">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-272">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="1a802-273">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-273">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="1a802-274">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="1a802-274">Allowsxs</span></span>
#### <span data-ttu-id="1a802-275">Autoriser l’expérience de navigateur côte à côte Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-275">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="1a802-276">Microsoft Edge Update 1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-276">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="1a802-277">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-277">Description</span></span>
<span data-ttu-id="1a802-278">Cette stratégie permet à un utilisateur d’exécuter Microsoft Edge (HTML Edge) et Microsoft Edge (basé sur Chromium) côte à côte.</span><span class="sxs-lookup"><span data-stu-id="1a802-278">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="1a802-279">Si cette stratégie est définie sur « Non configuré », Microsoft Edge (basée sur Chromium) remplace Microsoft Edge (Edge HTML) après installation du canal stable Microsoft Edge (basé sur Chromium) et des mises à jour de sécurité de novembre 2019.</span><span class="sxs-lookup"><span data-stu-id="1a802-279">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="1a802-280">C’est le même comportement que le paramètre « Désactivé ».</span><span class="sxs-lookup"><span data-stu-id="1a802-280">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="1a802-281">Le paramètre « Désactivé » bloque une expérience côte-à-côte et Microsoft Edge (basée sur Chromium) remplace Microsoft Edge (Edge HTML) après installation du canal stable Microsoft Edge (basé sur Chromium) et des mises à jour de sécurité de novembre 2019.</span><span class="sxs-lookup"><span data-stu-id="1a802-281">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="1a802-282">C’est le même comportement que le paramètre « Non configuré ».</span><span class="sxs-lookup"><span data-stu-id="1a802-282">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="1a802-283">Lorsque cette stratégie est « Activée », Microsoft Edge (basé sur Chromium) et Microsoft Edge (Edge HTML) peuvent s’exécuter côte à côte après l’installation de Microsoft Edge (basé sur Chromium).</span><span class="sxs-lookup"><span data-stu-id="1a802-283">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="1a802-284">Pour que cette stratégie de groupe prenne effet, elle doit être configurée avant l’installation automatique de Microsoft Edge (basé sur Chromium) par Windows Update.</span><span class="sxs-lookup"><span data-stu-id="1a802-284">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="1a802-285">Remarque : un utilisateur peut bloquer la mise à jour automatique de Microsoft Edge (basé sur Chromium) à l’aide du kit de ressources de bloqueur Microsoft Edge (basé sur Chromium).</span><span class="sxs-lookup"><span data-stu-id="1a802-285">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <span data-ttu-id="1a802-286">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-286">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-287">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-287">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-288">Nom unique de la stratégie de groupe : Allowsxs</span><span class="sxs-lookup"><span data-stu-id="1a802-288">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="1a802-289">Nom de la stratégie de groupe : Autoriser l’expérience de navigateur côte à côte Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-289">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="1a802-290">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="1a802-290">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="1a802-291">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-291">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-292">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-292">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-293">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-293">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-294">Nom de la valeur : Allowsxs</span><span class="sxs-lookup"><span data-stu-id="1a802-294">Value Name: Allowsxs</span></span>
- <span data-ttu-id="1a802-295">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1a802-295">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="1a802-296">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-296">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="1a802-297">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-297">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="1a802-298">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="1a802-298">CreateDesktopShortcutDefault</span></span>
#### <span data-ttu-id="1a802-299">Empêcher la création du Raccourci Bureau lors de l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="1a802-299">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="1a802-300">Microsoft Edge Update 1.3.128.0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-300">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="1a802-301">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-301">Description</span></span>
<span data-ttu-id="1a802-302">Vous permet de spécifier le comportement par défaut de tous les canaux pour créer un raccourci bureau lorsque Microsoft Edge est installé.</span><span class="sxs-lookup"><span data-stu-id="1a802-302">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="1a802-303">Si vous activez cette stratégie, un raccourci bureau est créé lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1a802-303">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="1a802-304">Si vous désactivez cette stratégie, aucun raccourci bureau n’est créé lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1a802-304">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="1a802-305">Si vous ne configurez pas cette stratégie, un raccourci bureau vers Microsoft Edge est créé pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="1a802-305">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="1a802-306">Si Microsoft Edge est déjà installé, cette stratégie n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="1a802-306">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <span data-ttu-id="1a802-307">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-307">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-308">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-308">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-309">Nom unique de stratégie de groupe : CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="1a802-309">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="1a802-310">Nom de stratégie de groupe : empêcher la création du Raccourci Bureau lors de l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="1a802-310">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="1a802-311">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="1a802-311">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="1a802-312">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-312">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-313">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-313">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-314">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-314">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-315">Nom de valeur : CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="1a802-315">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="1a802-316">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1a802-316">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="1a802-317">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-317">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="1a802-318">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-318">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="1a802-319">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="1a802-319">CreateDesktopShortcut</span></span>
#### <span data-ttu-id="1a802-320">Empêcher la création du Raccourci Bureau lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="1a802-320">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="1a802-321">Microsoft Edge Update 1.3.128.0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-321">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="1a802-322">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-322">Description</span></span>
<span data-ttu-id="1a802-323">Si vous activez cette stratégie, un raccourci bureau est créé lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1a802-323">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="1a802-324">Si vous désactivez cette stratégie, aucun raccourci bureau n’est créé lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1a802-324">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="1a802-325">Si vous ne configurez pas cette stratégie, un raccourci bureau vers Microsoft Edge est créé pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="1a802-325">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="1a802-326">Si Microsoft Edge est déjà installé, cette stratégie n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="1a802-326">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="1a802-327">Si vous ne configurez pas cette stratégie pour un canal, la configuration de stratégie « [Empêcher la création de raccourcis clavier lors de l’installation de la configuration de stratégie par défaut](#createdesktopshortcutdefault) » définit la création d’un raccourci lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1a802-327">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <span data-ttu-id="1a802-328">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-328">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-329">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-329">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-330">Nom unique de stratégie de groupe : CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="1a802-330">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="1a802-331">Nom de stratégie de groupe : empêcher la création du Raccourci Bureau lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="1a802-331">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="1a802-332">Chemin de la stratégie de groupe :</span><span class="sxs-lookup"><span data-stu-id="1a802-332">GP path:</span></span> 
  - <span data-ttu-id="1a802-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="1a802-334">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="1a802-334">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="1a802-335">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="1a802-335">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="1a802-336">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="1a802-336">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="1a802-337">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-337">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-338">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-338">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-339">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-339">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-340">Nom de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-340">Value Name:</span></span> 
  - <span data-ttu-id="1a802-341">(Stable) : CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="1a802-341">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="1a802-342">(Bêta) : CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="1a802-342">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="1a802-343">(Canary) : CreateDesktopShortcut {65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="1a802-343">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="1a802-344">(Dev) : CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="1a802-344">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="1a802-345">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1a802-345">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="1a802-346">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-346">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="1a802-347">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-347">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="1a802-348">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="1a802-348">RollbackToTargetVersion</span></span>
#### <span data-ttu-id="1a802-349">Restaurez la version Cible</span><span class="sxs-lookup"><span data-stu-id="1a802-349">Rollback to Target version</span></span>
><span data-ttu-id="1a802-350">Microsoft Edge Update 1.3.133.3 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-350">Microsoft Edge Update 1.3.133.3 and later</span></span>

#### <span data-ttu-id="1a802-351">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-351">Description</span></span>
<span data-ttu-id="1a802-352">Spécifie que Microsoft Edge Update doit restaurer les installations de Microsoft Edge à la version indiquée dans «[Remplacement de la version cible](#targetversionprefix)».</span><span class="sxs-lookup"><span data-stu-id="1a802-352">Specifies that Microsoft Edge Update should rollback installations of Microsoft Edge to the version indicated in '[Target version override](#targetversionprefix)'.</span></span>

<span data-ttu-id="1a802-353">Cette stratégie n’a aucun effet, sauf si «[Remplacement de la version cible](#targetversionprefix)» est défini et «[Remplacement de la stratégie de mise à jour](#update)» est défini à l’un des états d’activation (Toujours autoriser les mises à jour, Mises à jour automatiques silencieuses uniquement, Mises à jour manuelles uniquement).</span><span class="sxs-lookup"><span data-stu-id="1a802-353">This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).</span></span>

<span data-ttu-id="1a802-354">Si vous désactivez cette stratégie ou si vous ne la configurez pas, les installations dont la version est supérieure à celle spécifiée par «[Remplacement de la version cible](#targetversionprefix)» sont conservées.</span><span class="sxs-lookup"><span data-stu-id="1a802-354">If you disable this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.</span></span>

<span data-ttu-id="1a802-355">Si vous activez cette stratégie, les installations qui ont une version actuelle supérieure à celle spécifiée par «[Remplacement de la version cible](#targetversionprefix)» sont rétrogradées à la version cible.</span><span class="sxs-lookup"><span data-stu-id="1a802-355">If you enable this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.</span></span>

<span data-ttu-id="1a802-356">Nous recommandons aux utilisateurs d’installer la dernière version du navigateur Microsoft Edge afin de profiter de la protection offerte par les dernières mises à jour de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1a802-356">We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates.</span></span> <span data-ttu-id="1a802-357">La restauration à une version antérieure présente des risques d’exposition aux problèmes de sécurité connus.</span><span class="sxs-lookup"><span data-stu-id="1a802-357">Rollback to an earlier version risks exposure to known security issues.</span></span> <span data-ttu-id="1a802-358">Cette stratégie est destinée à être utilisée comme correctif temporaire pour résoudre les problèmes de mise à jour du navigateur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1a802-358">This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.</span></span>

<span data-ttu-id="1a802-359">Avant de restaurer temporairement la version de votre navigateur, nous vous recommandons d’activer la Synchronisation ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) pour tous les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1a802-359">Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization.</span></span> <span data-ttu-id="1a802-360">Si vous n’activez pas la Synchronisation, vous risquez de perdre définitivement les données de navigation.</span><span class="sxs-lookup"><span data-stu-id="1a802-360">If you don't turn on Sync, there is a risk of permanent browsing data loss.</span></span> <span data-ttu-id="1a802-361">L’ utilisation de cette stratégie comporte des risques.</span><span class="sxs-lookup"><span data-stu-id="1a802-361">Use this policy at your own risk.</span></span>

<span data-ttu-id="1a802-362">Remarque : Vous pouvez afficher toutes les versions disponibles pour la restauration ici [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="1a802-362">Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="1a802-363">Cette stratégie s’applique à Microsoft Edge version 86 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1a802-363">This policy applies to Microsoft Edge version 86 or later.</span></span>

<span data-ttu-id="1a802-364">Si vous souhaitez en savoir plus, consultez [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918).</span><span class="sxs-lookup"><span data-stu-id="1a802-364">See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.</span></span>

<span data-ttu-id="1a802-365">Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="1a802-365">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="1a802-366">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-366">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-367">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-367">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-368">Nom unique GP : RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="1a802-368">GP unique name: RollbackToTargetVersion</span></span>
- <span data-ttu-id="1a802-369">Nom GP: Restaurez la version Cible</span><span class="sxs-lookup"><span data-stu-id="1a802-369">GP name: Rollback to Target version</span></span>
- <span data-ttu-id="1a802-370">Chemin de la stratégie de groupe :</span><span class="sxs-lookup"><span data-stu-id="1a802-370">GP path:</span></span> 
  - <span data-ttu-id="1a802-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="1a802-372">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="1a802-372">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="1a802-373">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="1a802-373">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="1a802-374">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="1a802-374">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="1a802-375">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-375">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-376">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-376">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-377">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-377">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-378">Nom de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-378">Value Name:</span></span> 
  - <span data-ttu-id="1a802-379">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="1a802-379">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="1a802-380">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="1a802-380">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="1a802-381">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="1a802-381">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="1a802-382">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="1a802-382">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="1a802-383">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1a802-383">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="1a802-384">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-384">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="1a802-385">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-385">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="1a802-386">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="1a802-386">TargetVersionPrefix</span></span>
#### <span data-ttu-id="1a802-387">Remplacement de la version cible</span><span class="sxs-lookup"><span data-stu-id="1a802-387">Target version override</span></span>
><span data-ttu-id="1a802-388">Microsoft Edge Update 1.3.119.43 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-388">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <span data-ttu-id="1a802-389">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-389">Description</span></span>
<span data-ttu-id="1a802-390">Lorsque cette stratégie est activée et que la mise à jour automatique est activée, Microsoft Edge est mis à jour vers la version spécifiée par cette valeur de stratégie.</span><span class="sxs-lookup"><span data-stu-id="1a802-390">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="1a802-391">La valeur de la stratégie doit être une version spécifique de Microsoft Edge, par exemple, 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="1a802-391">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="1a802-392">Si la version de Microsoft Edge d’un appareil est plus récente que la valeur spécifiée, Microsoft Edge reste sur la version la plus récente et n’est pas rétrogradé vers la version spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1a802-392">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="1a802-393">Si la version spécifiée n’existe pas ou n’est pas mise en forme de manière correcte, Microsoft Edge reste sur sa version actuelle et ne sera pas mise à jour automatiquement vers les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1a802-393">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>

<span data-ttu-id="1a802-394">Si vous souhaitez en savoir plus, consultez [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707).</span><span class="sxs-lookup"><span data-stu-id="1a802-394">See [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) for more information.</span></span>

<span data-ttu-id="1a802-395">Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="1a802-395">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="1a802-396">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-396">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-397">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-397">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-398">Nom unique de stratégie de groupe : TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="1a802-398">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="1a802-399">Nom de stratégie de groupe : Remplacement de la version cible</span><span class="sxs-lookup"><span data-stu-id="1a802-399">GP name: Target version override</span></span>
- <span data-ttu-id="1a802-400">Chemin de la stratégie de groupe :</span><span class="sxs-lookup"><span data-stu-id="1a802-400">GP path:</span></span> 
  - <span data-ttu-id="1a802-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="1a802-402">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="1a802-402">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="1a802-403">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="1a802-403">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="1a802-404">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="1a802-404">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="1a802-405">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-405">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-406">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-406">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-407">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-407">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-408">Nom de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-408">Value Name:</span></span> 
  - <span data-ttu-id="1a802-409">(Stable) : TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="1a802-409">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="1a802-410">(Beta) : TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="1a802-410">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="1a802-411">(Canary) : TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="1a802-411">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="1a802-412">(Dev) : TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="1a802-412">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="1a802-413">Type de valeur : REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1a802-413">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="1a802-414">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-414">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="1a802-415">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-415">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="1a802-416">Stratégies de préférences</span><span class="sxs-lookup"><span data-stu-id="1a802-416">Preferences policies</span></span>

[<span data-ttu-id="1a802-417">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-417">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="1a802-418">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="1a802-418">AutoUpdateCheckPeriodMinutes</span></span>
#### <span data-ttu-id="1a802-419">Remplacement de la période de vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="1a802-419">Auto-update check period override</span></span>
><span data-ttu-id="1a802-420">Microsoft Edge Update 1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-420">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="1a802-421">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-421">Description</span></span>
<span data-ttu-id="1a802-422">Si elle est activée, cette stratégie vous permet de définir une valeur pour le nombre minimal de minutes entre les recherches automatiques de mises à jour.</span><span class="sxs-lookup"><span data-stu-id="1a802-422">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="1a802-423">Dans le cas contraire, par défaut, la mise à jour automatique recherche les mises à jour toutes les 10 heures.</span><span class="sxs-lookup"><span data-stu-id="1a802-423">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="1a802-424">Si vous souhaitez désactiver toutes les vérifications de mise à jour automatique, définissez la valeur sur 0 (non recommandé).</span><span class="sxs-lookup"><span data-stu-id="1a802-424">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <span data-ttu-id="1a802-425">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-425">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-426">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-426">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-427">Nom unique de la stratégie de groupe : AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="1a802-427">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="1a802-428">Nom de la stratégie de groupe : Remplacement de la période de vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="1a802-428">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="1a802-429">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Preferences</span><span class="sxs-lookup"><span data-stu-id="1a802-429">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="1a802-430">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-430">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-431">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-431">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-432">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-432">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-433">Nom de la valeur : AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="1a802-433">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="1a802-434">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1a802-434">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="1a802-435">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-435">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="1a802-436">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-436">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="1a802-437">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="1a802-437">UpdatesSuppressed</span></span>
#### <span data-ttu-id="1a802-438">Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="1a802-438">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="1a802-439">Microsoft Edge Update 1.3.33.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-439">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <span data-ttu-id="1a802-440">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-440">Description</span></span>
<span data-ttu-id="1a802-441">Si vous activez cette stratégie, les vérifications de mise à jour sont supprimées chaque jour à partir de Heure:Minute pendant une Durée (en minutes).</span><span class="sxs-lookup"><span data-stu-id="1a802-441">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="1a802-442">La durée n’est pas affectée par l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="1a802-442">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="1a802-443">Par exemple, si l’heure de début est 22:00 et que la durée est 480 minutes, les mises à jour seront supprimées pendant exactement 8 heures, même si l’heure d’été commence ou se termine pendant cette période.</span><span class="sxs-lookup"><span data-stu-id="1a802-443">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="1a802-444">Si vous désactivez ou que vous ne configurez pas cette stratégie, les vérifications de mise à jour ne sont pas supprimées pendant une période spécifique.</span><span class="sxs-lookup"><span data-stu-id="1a802-444">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <span data-ttu-id="1a802-445">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-445">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-446">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-446">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-447">Nom unique de la stratégie de groupe : UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="1a802-447">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="1a802-448">Nom de la stratégie de groupe : Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="1a802-448">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="1a802-449">Options { Hour, Minute, Duration }</span><span class="sxs-lookup"><span data-stu-id="1a802-449">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="1a802-450">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Preferences</span><span class="sxs-lookup"><span data-stu-id="1a802-450">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="1a802-451">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-451">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-452">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-452">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-453">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-453">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-454">Nom de la valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-454">Value Name:</span></span> 
  - <span data-ttu-id="1a802-455">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="1a802-455">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="1a802-456">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="1a802-456">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="1a802-457">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="1a802-457">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="1a802-458">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1a802-458">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="1a802-459">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-459">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="1a802-460">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-460">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="1a802-461">Stratégies de serveur proxy</span><span class="sxs-lookup"><span data-stu-id="1a802-461">Proxy Server policies</span></span>

[<span data-ttu-id="1a802-462">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-462">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="1a802-463">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="1a802-463">ProxyMode</span></span>
#### <span data-ttu-id="1a802-464">Choisir comment spécifier les paramètres du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="1a802-464">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="1a802-465">Microsoft Edge Update 1.3.21.81 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-465">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="1a802-466">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-466">Description</span></span>
<span data-ttu-id="1a802-467">Permet de spécifier les paramètres de serveur proxy qui sont utilisés par Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="1a802-467">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="1a802-468">Si vous activez cette stratégie, vous pouvez choisir l’une des options de serveur proxy suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a802-468">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="1a802-469">Si vous choisissez de ne jamais utiliser un serveur proxy et de toujours vous connecter directement, toutes les autres options sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="1a802-469">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="1a802-470">Si vous choisissez d’utiliser les paramètres de proxy système ou de détection automatique du serveur proxy, toutes les autres options sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="1a802-470">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="1a802-471">Si vous choisissez le mode de serveur proxy fixe, vous pouvez spécifier d’autres options dans la stratégie [« Adresse ou URL du serveur proxy »](#proxyserver).</span><span class="sxs-lookup"><span data-stu-id="1a802-471">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="1a802-472">Si vous choisissez d’utiliser un script de proxy .pac, vous devez spécifier l’URL du script dans la stratégie [« URL d’un fichier proxy. pac »](#proxypacurl).</span><span class="sxs-lookup"><span data-stu-id="1a802-472">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="1a802-473">Si vous activez cette stratégie, les utilisateurs de votre organisation ne peuvent pas modifier les paramètres du proxy dans Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="1a802-473">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="1a802-474">Si vous désactivez ou que vous ne configurez pas cette stratégie, aucun paramètre de serveur proxy n’est configuré, mais les utilisateurs de votre organisation peuvent choisir leurs propres paramètres de proxy pour Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="1a802-474">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <span data-ttu-id="1a802-475">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-475">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-476">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-476">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-477">Nom unique de la stratégie de groupe : ProxyMode</span><span class="sxs-lookup"><span data-stu-id="1a802-477">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="1a802-478">Nom de la stratégie de groupe : Choisir comment spécifier les paramètres du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="1a802-478">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="1a802-479">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="1a802-479">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="1a802-480">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-480">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-481">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-481">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-482">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-482">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-483">Nom de la valeur : ProxyMode</span><span class="sxs-lookup"><span data-stu-id="1a802-483">Value Name: ProxyMode</span></span>
- <span data-ttu-id="1a802-484">Type de valeur : REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1a802-484">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="1a802-485">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-485">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="1a802-486">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-486">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="1a802-487">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="1a802-487">ProxyPacUrl</span></span>
#### <span data-ttu-id="1a802-488">URL d’un fichier proxy. pac</span><span class="sxs-lookup"><span data-stu-id="1a802-488">URL to a proxy .pac file</span></span>
><span data-ttu-id="1a802-489">Microsoft Edge Update 1.3.21.81 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-489">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="1a802-490">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-490">Description</span></span>
<span data-ttu-id="1a802-491">Permet de spécifier une URL pour un fichier de configuration automatique de proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="1a802-491">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="1a802-492">Si vous activez cette stratégie, vous pouvez spécifier une URL pour un fichier PAC pour automatiser la façon dont Microsoft Edge Update sélectionne le serveur proxy approprié pour l’extraction d’un site web particulier.</span><span class="sxs-lookup"><span data-stu-id="1a802-492">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="1a802-493">Cette stratégie est appliquée uniquement si vous avez spécifié des paramètres de proxy manuels dans la stratégie « [Choisir comment spécifier les paramètres du serveur proxy](#proxymode) ».</span><span class="sxs-lookup"><span data-stu-id="1a802-493">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="1a802-494">Ne configurez pas cette stratégie si vous avez sélectionné un paramètre de proxy autre que manuel dans la stratégie « [Choisir comment spécifier les paramètres du serveur proxy](#proxymode) ».</span><span class="sxs-lookup"><span data-stu-id="1a802-494">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="1a802-495">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-495">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-496">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-496">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-497">Nom unique de la stratégie de groupe : ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="1a802-497">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="1a802-498">Nom de la stratégie de groupe : URL d’un fichier proxy. pac</span><span class="sxs-lookup"><span data-stu-id="1a802-498">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="1a802-499">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="1a802-499">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="1a802-500">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-500">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-501">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-501">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-502">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-502">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-503">Nom de la valeur : ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="1a802-503">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="1a802-504">Type de valeur : REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1a802-504">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="1a802-505">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-505">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="1a802-506">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-506">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="1a802-507">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="1a802-507">ProxyServer</span></span>
#### <span data-ttu-id="1a802-508">Adresse ou URL du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="1a802-508">Address or URL of proxy server</span></span>
><span data-ttu-id="1a802-509">Microsoft Edge Update 1.3.21.81 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-509">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="1a802-510">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-510">Description</span></span>
<span data-ttu-id="1a802-511">Permet de spécifier l’URL du serveur proxy que Microsoft Edge Update doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="1a802-511">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="1a802-512">Si vous activez cette stratégie, vous pouvez définir l’URL de serveur proxy utilisée par Microsoft Edge Update dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1a802-512">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="1a802-513">Cette stratégie est appliquée uniquement si vous avez sélectionné plusieurs paramètres de proxy manuels dans la stratégie « [Choisir comment spécifier les paramètres du serveur proxy](#proxymode) ».</span><span class="sxs-lookup"><span data-stu-id="1a802-513">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="1a802-514">Ne configurez pas cette stratégie si vous avez sélectionné un paramètre de proxy autre que manuel dans la stratégie « [Choisir comment spécifier les paramètres du serveur proxy](#proxymode) ».</span><span class="sxs-lookup"><span data-stu-id="1a802-514">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="1a802-515">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-515">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-516">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-516">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-517">Nom unique de la stratégie de groupe : ProxyServer</span><span class="sxs-lookup"><span data-stu-id="1a802-517">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="1a802-518">Nom de la stratégie de groupe : Adresse ou URL du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="1a802-518">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="1a802-519">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="1a802-519">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="1a802-520">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-520">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-521">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-521">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-522">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-522">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-523">Nom de la valeur : ProxyServer</span><span class="sxs-lookup"><span data-stu-id="1a802-523">Value Name: ProxyServer</span></span>
- <span data-ttu-id="1a802-524">Type de valeur : REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1a802-524">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="1a802-525">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-525">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="1a802-526">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-526">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="1a802-527">Stratégies d’affichage web Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-527">Microsoft Edge WebView policies</span></span>

[<span data-ttu-id="1a802-528">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-528">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="1a802-529">Installation (Affichage web)</span><span class="sxs-lookup"><span data-stu-id="1a802-529">Install (WebView)</span></span>
#### <span data-ttu-id="1a802-530">Autoriser l’installation</span><span class="sxs-lookup"><span data-stu-id="1a802-530">Allow installation</span></span>
><span data-ttu-id="1a802-531">Microsoft Edge Update 1.3.127.1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-531">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <span data-ttu-id="1a802-532">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-532">Description</span></span>
<span data-ttu-id="1a802-533">Vous permet de spécifier si un affichage web de Microsoft Edge peut être installé à l’aide de Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="1a802-533">Lets you specify whether Microsoft Edge WebView can be installed using Microsoft Edge Update.</span></span>

  - <span data-ttu-id="1a802-534">Si vous activez cette stratégie, les utilisateurs peuvent installer l’affichage web de Microsoft Edge via Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="1a802-534">If you enable this policy, users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="1a802-535">Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas installer l’affichage web de Microsoft Edge via Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="1a802-535">If you disable this policy, users cannot install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="1a802-536">Si vous ne configurez pas cette stratégie, la configuration de la stratégie «[Autoriser l’installation par défaut](#installdefault)» détermine si les utilisateurs peuvent installer l’Affichage web Microsoft Edge via Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="1a802-536">If you don't configure this policy, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
#### <span data-ttu-id="1a802-537">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-537">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-538">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-538">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-539">Nom unique de la stratégie de groupe : Install</span><span class="sxs-lookup"><span data-stu-id="1a802-539">GP unique name: Install</span></span>
- <span data-ttu-id="1a802-540">Nom de la stratégie de groupe : Autoriser l’installation</span><span class="sxs-lookup"><span data-stu-id="1a802-540">GP name: Allow installation</span></span>
- <span data-ttu-id="1a802-541">Chemin d’accès de la stratégie de groupe : Modèles administratifs/Microsoft Edge Update/Applications/Affichage web Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-541">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="1a802-542">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-542">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-543">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-543">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-544">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-544">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-545">Nom de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-545">Value Name:</span></span> 
  - <span data-ttu-id="1a802-546">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="1a802-546">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="1a802-547">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1a802-547">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="1a802-548">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-548">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="1a802-549">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-549">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="1a802-550">Mise à jour (Affichage web)</span><span class="sxs-lookup"><span data-stu-id="1a802-550">Update (WebView)</span></span>
#### <span data-ttu-id="1a802-551">Remplacer la stratégie de mise à jour</span><span class="sxs-lookup"><span data-stu-id="1a802-551">Update policy override</span></span>
><span data-ttu-id="1a802-552">Microsoft Edge Update 1.3.127.1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1a802-552">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <span data-ttu-id="1a802-553">Description</span><span class="sxs-lookup"><span data-stu-id="1a802-553">Description</span></span>
<span data-ttu-id="1a802-554">Vous permet de spécifier si les mises à jour automatiques sont activées pour l’affichage web de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1a802-554">Lets you specify whether or not automatic updates are enabled for Microsoft Edge WebView.</span></span> <span data-ttu-id="1a802-555">L’affichage web de Microsoft Edge est un composant utilisé par les applications pour afficher du contenu web.</span><span class="sxs-lookup"><span data-stu-id="1a802-555">Microsoft Edge WebView is a component used by applications to display web content.</span></span>
<span data-ttu-id="1a802-556">Les mises à jour automatiques sont activées par défaut.</span><span class="sxs-lookup"><span data-stu-id="1a802-556">Automatic updates are enabled by default.</span></span> <span data-ttu-id="1a802-557">La désactivation des mises à jour automatiques pour l’affichage web de Microsoft Edge peut entraîner des problèmes de compatibilité avec les applications qui dépendent de ce composant.</span><span class="sxs-lookup"><span data-stu-id="1a802-557">Disabling automatic updates for Microsoft Edge WebView might cause compatibility issues with applications that depend on this component.</span></span>

  <span data-ttu-id="1a802-558">Si vous activez cette stratégie, Microsoft Edge Update gère les mises à jour de l’affichage web de Microsoft Edge en fonction de la façon dont vous configurez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a802-558">If you enable this policy, Microsoft Edge Update handles Microsoft Edge WebView updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="1a802-559">Toujours autoriser les mises à jour : les mises à jour sont téléchargées et appliquées automatiquement</span><span class="sxs-lookup"><span data-stu-id="1a802-559">Always allow updates: Updates are automatically downloaded and applied</span></span>
  - <span data-ttu-id="1a802-560">Mises à jour désactivées : les mises à jour ne sont jamais téléchargées ou appliquées.</span><span class="sxs-lookup"><span data-stu-id="1a802-560">Updates disabled: Updates are never downloaded or applied</span></span>

  <span data-ttu-id="1a802-561">Si vous n’activez pas cette stratégie, les mises à jour sont automatiquement téléchargées et appliquées.</span><span class="sxs-lookup"><span data-stu-id="1a802-561">If you don't enable this policy, updates are automatically downloaded and applied.</span></span>
#### <span data-ttu-id="1a802-562">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-562">Windows information and settings</span></span>
##### <span data-ttu-id="1a802-563">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="1a802-563">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="1a802-564">Nom unique de la stratégie de groupe : Update</span><span class="sxs-lookup"><span data-stu-id="1a802-564">GP unique name: Update</span></span>
- <span data-ttu-id="1a802-565">Nom de la stratégie de groupe : Remplacer la stratégie de mise à jour</span><span class="sxs-lookup"><span data-stu-id="1a802-565">GP name: Update policy override</span></span>
- <span data-ttu-id="1a802-566">Chemin d’accès de la stratégie de groupe : Modèles administratifs/Microsoft Edge Update/Applications/Affichage web Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-566">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="1a802-567">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="1a802-567">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="1a802-568">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="1a802-568">Windows Registry Settings</span></span>
- <span data-ttu-id="1a802-569">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="1a802-569">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="1a802-570">Nom de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-570">Value Name:</span></span> 
  - <span data-ttu-id="1a802-571">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="1a802-571">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="1a802-572">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1a802-572">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="1a802-573">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="1a802-573">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="1a802-574">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1a802-574">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="1a802-575">Voir également</span><span class="sxs-lookup"><span data-stu-id="1a802-575">See also</span></span>
  - [<span data-ttu-id="1a802-576">Configuration de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a802-576">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="1a802-577">Page d’accueil Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="1a802-577">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)