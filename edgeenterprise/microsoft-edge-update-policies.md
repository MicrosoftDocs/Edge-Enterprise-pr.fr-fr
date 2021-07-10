---
title: Documentation relative aux stratégies Microsoft Edge Update
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 06/29/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentation relative à toutes les stratégies prises en charge par le programme de mise à jour Microsoft Edge
ms.openlocfilehash: a9808981acad544042c6e0ccb59ff755a670c848
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642320"
---
# <a name="microsoft-edge---update-policies"></a><span data-ttu-id="e1b16-103">Microsoft Edge - Stratégies de mise à jour</span><span class="sxs-lookup"><span data-stu-id="e1b16-103">Microsoft Edge - Update policies</span></span>

<span data-ttu-id="e1b16-104">La dernière version de Microsoft Edge comprend les stratégies suivantes que vous pouvez utiliser pour contrôler comment et quand Microsoft Edge est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="e1b16-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

<span data-ttu-id="e1b16-105">Pour plus d’informations sur les autres stratégies disponibles dans Microsoft Edge, consultez la [Référence de stratégies du navigateur Microsoft Edge](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="e1b16-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="e1b16-106">Cet article concerne Microsoft Edge version 77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e1b16-106">This article applies to Microsoft Edge version 77 or later.</span></span>
## <a name="available-policies"></a><span data-ttu-id="e1b16-107">Stratégies disponibles</span><span class="sxs-lookup"><span data-stu-id="e1b16-107">Available policies</span></span>
<span data-ttu-id="e1b16-108">Ces tableaux répertorient toutes les stratégies de groupe relatives aux mises à jour disponibles dans cette version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e1b16-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="e1b16-109">Utilisez les liens dans le tableau pour obtenir plus de détails sur des stratégies données.</span><span class="sxs-lookup"><span data-stu-id="e1b16-109">Use the links in the table to get more details about specific policies.</span></span>

<span data-ttu-id="e1b16-110">|&nbsp;|&nbsp;| |**-**|-| |[](#preferences)| |**[Appications](#applications)**|[Préférences](#preferences)| |**[Serveur proxy](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|</span><span class="sxs-lookup"><span data-stu-id="e1b16-110">|&nbsp;|&nbsp;| |**-**|-| |**[Applications](#applications)**|[Preferences](#preferences)| |**[Proxy Server](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|</span></span>
### [<a name="applications"></a><span data-ttu-id="e1b16-111">Applications</span><span class="sxs-lookup"><span data-stu-id="e1b16-111">Applications</span></span>](#applications-policies)
|<span data-ttu-id="e1b16-112">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="e1b16-112">Policy Name</span></span>|<span data-ttu-id="e1b16-113">Caption</span><span class="sxs-lookup"><span data-stu-id="e1b16-113">Caption</span></span>|
|-|-|
|[<span data-ttu-id="e1b16-114">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="e1b16-114">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="e1b16-115">Autoriser l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="e1b16-115">Allow installation default</span></span>|
|[<span data-ttu-id="e1b16-116">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="e1b16-116">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="e1b16-117">Remplacer la stratégie de mise à jour par défaut</span><span class="sxs-lookup"><span data-stu-id="e1b16-117">Update policy override default</span></span>|
|[<span data-ttu-id="e1b16-118">Install</span><span class="sxs-lookup"><span data-stu-id="e1b16-118">Install</span></span>](#install)|<span data-ttu-id="e1b16-119">Autoriser l’installation (par canal)</span><span class="sxs-lookup"><span data-stu-id="e1b16-119">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="e1b16-120">Update</span><span class="sxs-lookup"><span data-stu-id="e1b16-120">Update</span></span>](#update)|<span data-ttu-id="e1b16-121">Remplacer la stratégie de mise à jour (par canal)</span><span class="sxs-lookup"><span data-stu-id="e1b16-121">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="e1b16-122">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="e1b16-122">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="e1b16-123">Autoriser l’expérience de navigateur côte à côte Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1b16-123">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="e1b16-124">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="e1b16-124">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="e1b16-125">Empêcher la création du Raccourci Bureau lors de l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="e1b16-125">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="e1b16-126">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="e1b16-126">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="e1b16-127">Empêcher la création du Raccourci Bureau lors de l’installation (par canal)</span><span class="sxs-lookup"><span data-stu-id="e1b16-127">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="e1b16-128">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="e1b16-128">RollbackToTargetVersion</span></span>](#rollbacktotargetversion)|<span data-ttu-id="e1b16-129">Restaurez la version Cible (par canal)</span><span class="sxs-lookup"><span data-stu-id="e1b16-129">Rollback to Target version (per channel)</span></span>|
|[<span data-ttu-id="e1b16-130">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="e1b16-130">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="e1b16-131">Remplacement de la version cible (par canal)</span><span class="sxs-lookup"><span data-stu-id="e1b16-131">Target version override (per channel)</span></span>|

### [<a name="preferences"></a><span data-ttu-id="e1b16-132">Préférences</span><span class="sxs-lookup"><span data-stu-id="e1b16-132">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="e1b16-133">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="e1b16-133">Policy Name</span></span>|<span data-ttu-id="e1b16-134">Caption</span><span class="sxs-lookup"><span data-stu-id="e1b16-134">Caption</span></span>|
|-|-|
|[<span data-ttu-id="e1b16-135">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="e1b16-135">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="e1b16-136">Remplacement de la période de vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="e1b16-136">Auto-update check period override</span></span>|
|[<span data-ttu-id="e1b16-137">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="e1b16-137">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="e1b16-138">Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="e1b16-138">Time period in each day to suppress auto-update check</span></span>|

### [<a name="proxy-server"></a><span data-ttu-id="e1b16-139">Serveur proxy</span><span class="sxs-lookup"><span data-stu-id="e1b16-139">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="e1b16-140">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="e1b16-140">Policy Name</span></span>|<span data-ttu-id="e1b16-141">Légende</span><span class="sxs-lookup"><span data-stu-id="e1b16-141">Caption</span></span>|
|-|-|
|[<span data-ttu-id="e1b16-142">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="e1b16-142">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="e1b16-143">Choisir comment spécifier les paramètres du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="e1b16-143">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="e1b16-144">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="e1b16-144">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="e1b16-145">URL d’un fichier proxy. pac</span><span class="sxs-lookup"><span data-stu-id="e1b16-145">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="e1b16-146">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="e1b16-146">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="e1b16-147">Adresse ou URL du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="e1b16-147">Address or URL of proxy server</span></span>|

### [<a name="microsoft-edge-webview"></a><span data-ttu-id="e1b16-148">Affichage web Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1b16-148">Microsoft Edge WebView</span></span>](#microsoft-edge-webview-policies)
|<span data-ttu-id="e1b16-149">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="e1b16-149">Policy Name</span></span>|<span data-ttu-id="e1b16-150">Caption</span><span class="sxs-lookup"><span data-stu-id="e1b16-150">Caption</span></span>|
|-|-|
|[<span data-ttu-id="e1b16-151">Installer</span><span class="sxs-lookup"><span data-stu-id="e1b16-151">Install</span></span>](#install-webview)|<span data-ttu-id="e1b16-152">Autoriser l’installation</span><span class="sxs-lookup"><span data-stu-id="e1b16-152">Allow installation</span></span>|
|[<span data-ttu-id="e1b16-153">Mettre à jour/Mise à jour</span><span class="sxs-lookup"><span data-stu-id="e1b16-153">Update</span></span>](#update-webview)|<span data-ttu-id="e1b16-154">Remplacer la stratégie de mise à jour</span><span class="sxs-lookup"><span data-stu-id="e1b16-154">Update policy override</span></span>|

## <a name="applications-policies"></a><span data-ttu-id="e1b16-155">Stratégies d’applications</span><span class="sxs-lookup"><span data-stu-id="e1b16-155">Applications policies</span></span>

[<span data-ttu-id="e1b16-156">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-156">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="installdefault"></a><span data-ttu-id="e1b16-157">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="e1b16-157">InstallDefault</span></span>
#### <a name="allow-installation-default"></a><span data-ttu-id="e1b16-158">Autoriser l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="e1b16-158">Allow installation default</span></span>
><span data-ttu-id="e1b16-159">Microsoft Edge Update 1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-159">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-160">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-160">Description</span></span>
<span data-ttu-id="e1b16-161">Vous pouvez spécifier le comportement par défaut de tous les canaux pour autoriser ou bloquer Microsoft Edge sur les appareils liés à un domaine.</span><span class="sxs-lookup"><span data-stu-id="e1b16-161">You can specify the default behavior of all channels to allow or block Microsoft Edge on domain-joined devices.</span></span>

<span data-ttu-id="e1b16-162">Vous pouvez remplacer cette stratégie pour des canaux individuels en spécifiant la stratégie « [Autoriser l’installation](#install) » pour des canaux spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e1b16-162">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="e1b16-163">Si vous désactivez cette stratégie, l’installation de Microsoft Edge est bloquée.</span><span class="sxs-lookup"><span data-stu-id="e1b16-163">If you disable this policy, the installation of Microsoft Edge is blocked.</span></span> <span data-ttu-id="e1b16-164">Cela affecte uniquement l’installation du logiciel Microsoft Edge lorsque la stratégie «[Autoriser l’installation](#install)» est définie Non Configurée.</span><span class="sxs-lookup"><span data-stu-id="e1b16-164">This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.</span></span>

<span data-ttu-id="e1b16-165">Cette stratégie n’empêche pas Microsoft Edge Update de s’exécuter, ni les utilisateurs d’installer le logiciel Microsoft Edge en utilisant d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="e1b16-165">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>

<span data-ttu-id="e1b16-166">Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="e1b16-166">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-167">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-167">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-168">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-168">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-169">Nom unique de la stratégie de groupe : InstallDefault</span><span class="sxs-lookup"><span data-stu-id="e1b16-169">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="e1b16-170">Nom de la stratégie de groupe : Autoriser l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="e1b16-170">GP name: Allow installation default</span></span>
- <span data-ttu-id="e1b16-171">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="e1b16-171">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="e1b16-172">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-172">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-173">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-173">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-174">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-174">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-175">Nom de la valeur : InstallDefault</span><span class="sxs-lookup"><span data-stu-id="e1b16-175">Value Name: InstallDefault</span></span>
- <span data-ttu-id="e1b16-176">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e1b16-176">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-177">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-177">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e1b16-178">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-178">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="updatedefault"></a><span data-ttu-id="e1b16-179">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="e1b16-179">UpdateDefault</span></span>
#### <a name="update-policy-override-default"></a><span data-ttu-id="e1b16-180">Remplacer la stratégie de mise à jour par défaut</span><span class="sxs-lookup"><span data-stu-id="e1b16-180">Update policy override default</span></span>
><span data-ttu-id="e1b16-181">Microsoft Edge Update 1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-181">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-182">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-182">Description</span></span>
<span data-ttu-id="e1b16-183">Permet de spécifier le comportement par défaut de tous les canaux concernant la façon dont Microsoft Edge Update gère les mises à jour disponibles pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e1b16-183">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="e1b16-184">Peut être remplacé pour des canaux individuels en spécifiant la stratégie « [Remplacer la stratégie de mise à jour](#update) » pour ces canaux spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e1b16-184">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="e1b16-185">Si vous activez cette stratégie, Microsoft Edge Update gère les mises à jour de Microsoft Edge en fonction de la façon dont vous configurez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1b16-185">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="e1b16-186">Toujours autoriser les mises à jour : les mises à jour sont toujours appliquées lorsqu’elles sont trouvées, soit par une recherche de mise à jour périodique, soit par une recherche de mise à jour manuelle.</span><span class="sxs-lookup"><span data-stu-id="e1b16-186">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="e1b16-187">Mises à jour automatiques en mode silencieux uniquement : les mises à jour sont appliquées uniquement lorsqu’elles sont trouvées par la recherche de mise à jour périodique.</span><span class="sxs-lookup"><span data-stu-id="e1b16-187">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="e1b16-188">Mises à jour manuelles uniquement : les mises à jour sont appliquées uniquement lorsque l’utilisateur exécute une recherche de mise à jour manuelle.</span><span class="sxs-lookup"><span data-stu-id="e1b16-188">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="e1b16-189">Mises à jour désactivées : les mises à jour ne sont jamais appliquées.</span><span class="sxs-lookup"><span data-stu-id="e1b16-189">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="e1b16-190">Si vous sélectionnez les mises à jour manuelles, vérifiez régulièrement si des mises à jour sont disponibles à l’aide du mécanisme de mise à jour manuelle de l’application, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e1b16-190">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="e1b16-191">Si vous désactivez les mises à jour, recherchez régulièrement les mises à jour et distribuez-les aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e1b16-191">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="e1b16-192">Si vous n’activez pas et ne configurez pas cette stratégie, Microsoft Edge Update gère les mises à jour disponibles, comme spécifié par la stratégie « [Remplacer la stratégie de mise à jour](#update) ».</span><span class="sxs-lookup"><span data-stu-id="e1b16-192">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>

  <span data-ttu-id="e1b16-193">Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="e1b16-193">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-194">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-194">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-195">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-195">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-196">Nom unique de la stratégie de groupe : UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="e1b16-196">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="e1b16-197">Nom de la stratégie de groupe : Remplacer la stratégie de mise à jour par défaut</span><span class="sxs-lookup"><span data-stu-id="e1b16-197">GP name: Update policy override default</span></span>
- <span data-ttu-id="e1b16-198">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="e1b16-198">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="e1b16-199">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-199">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-200">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-200">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-201">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-201">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-202">Nom de la valeur : UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="e1b16-202">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="e1b16-203">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e1b16-203">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-204">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-204">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="e1b16-205">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-205">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="install"></a><span data-ttu-id="e1b16-206">Install</span><span class="sxs-lookup"><span data-stu-id="e1b16-206">Install</span></span>
#### <a name="allow-installation"></a><span data-ttu-id="e1b16-207">Autoriser l’installation</span><span class="sxs-lookup"><span data-stu-id="e1b16-207">Allow installation</span></span>
><span data-ttu-id="e1b16-208">Microsoft Edge Update 1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-208">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-209">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-209">Description</span></span>
<span data-ttu-id="e1b16-210">Spécifie si un canal de Microsoft Edge peut être installé sur des appareils liés à un domaine.</span><span class="sxs-lookup"><span data-stu-id="e1b16-210">Specifies whether a Microsoft Edge channel can be installed on domain-joined devices.</span></span>

  <span data-ttu-id="e1b16-211">Si vous activez cette stratégie pour un canal, l’installation de Microsoft Edge ne sera pas bloquée.</span><span class="sxs-lookup"><span data-stu-id="e1b16-211">If you enable this policy for a channel, Microsoft Edge will not be blocked from installation.</span></span>

  <span data-ttu-id="e1b16-212">Si vous désactivez cette stratégie pour un canal, l’installation de Microsoft Edge sera bloquée.</span><span class="sxs-lookup"><span data-stu-id="e1b16-212">If you disable this policy for a channel, Microsoft Edge will be blocked from installation.</span></span>

  <span data-ttu-id="e1b16-213">Si vous ne configurez pas cette stratégie pour un canal, la configuration de la stratégie «[Autoriser l’installation par défaut](#installdefault)» détermine si les utilisateurs peuvent installer ce canal de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e1b16-213">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.</span></span>

  <span data-ttu-id="e1b16-214">Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="e1b16-214">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-215">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-215">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-216">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-216">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-217">Nom unique de la stratégie de groupe : Install</span><span class="sxs-lookup"><span data-stu-id="e1b16-217">GP unique name: Install</span></span>
- <span data-ttu-id="e1b16-218">Nom de la stratégie de groupe : Autoriser l’installation</span><span class="sxs-lookup"><span data-stu-id="e1b16-218">GP name: Allow installation</span></span>
- <span data-ttu-id="e1b16-219">Chemin de la stratégie de groupe :</span><span class="sxs-lookup"><span data-stu-id="e1b16-219">GP path:</span></span> 
  - <span data-ttu-id="e1b16-220">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1b16-220">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="e1b16-221">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="e1b16-221">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="e1b16-222">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="e1b16-222">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="e1b16-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="e1b16-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="e1b16-224">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-224">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-225">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-225">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-226">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-226">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-227">Nom de la valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-227">Value Name:</span></span> 
  - <span data-ttu-id="e1b16-228">(Stable) : install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="e1b16-228">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="e1b16-229">(Beta) : install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="e1b16-229">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="e1b16-230">(Canary) : Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="e1b16-230">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="e1b16-231">(Dev) : Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="e1b16-231">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="e1b16-232">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e1b16-232">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-233">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-233">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e1b16-234">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-234">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="update"></a><span data-ttu-id="e1b16-235">Update</span><span class="sxs-lookup"><span data-stu-id="e1b16-235">Update</span></span>
#### <a name="update-policy-override"></a><span data-ttu-id="e1b16-236">Remplacer la stratégie de mise à jour</span><span class="sxs-lookup"><span data-stu-id="e1b16-236">Update policy override</span></span>
><span data-ttu-id="e1b16-237">Microsoft Edge Update 1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-237">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-238">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-238">Description</span></span>
<span data-ttu-id="e1b16-239">Spécifie comment Microsoft Edge Update gère les mises à jour disponibles à partir de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e1b16-239">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

<span data-ttu-id="e1b16-240">Si vous activez cette stratégie, Microsoft Edge Update gère les mises à jour de Microsoft Edge en fonction de la façon dont vous configurez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1b16-240">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="e1b16-241">Toujours autoriser les mises à jour : les mises à jour sont toujours appliquées lorsqu’elles sont trouvées, soit par une recherche de mise à jour périodique, soit par une recherche de mise à jour manuelle.</span><span class="sxs-lookup"><span data-stu-id="e1b16-241">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
  - <span data-ttu-id="e1b16-242">Mises à jour automatiques en mode silencieux uniquement : les mises à jour sont appliquées uniquement lorsqu’elles sont trouvées par la recherche de mise à jour périodique.</span><span class="sxs-lookup"><span data-stu-id="e1b16-242">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
  - <span data-ttu-id="e1b16-243">Mises à jour manuelles uniquement : les mises à jour sont appliquées uniquement lorsque l’utilisateur exécute une recherche de mise à jour manuelle.</span><span class="sxs-lookup"><span data-stu-id="e1b16-243">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="e1b16-244">(Toutes les applications n’offrent pas une interface pour cette option.)</span><span class="sxs-lookup"><span data-stu-id="e1b16-244">(Not all apps provide an interface for this option.)</span></span>
  - <span data-ttu-id="e1b16-245">Mises à jour désactivées : les mises à jour ne sont jamais appliquées.</span><span class="sxs-lookup"><span data-stu-id="e1b16-245">Updates disabled: Updates are never applied.</span></span>

<span data-ttu-id="e1b16-246">Si vous sélectionnez les mises à jour manuelles, vérifiez régulièrement si des mises à jour sont disponibles à l’aide du mécanisme de mise à jour manuelle de l’application, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e1b16-246">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="e1b16-247">Si vous désactivez les mises à jour, recherchez régulièrement les mises à jour et distribuez-les aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e1b16-247">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

<span data-ttu-id="e1b16-248">Si vous n’activez pas et ne configurez pas cette stratégie, Microsoft Edge Update gère les mises à jour disponibles, comme spécifié par la stratégie « [Remplacer la stratégie de mise à jour par défaut](#updatedefault) ».</span><span class="sxs-lookup"><span data-stu-id="e1b16-248">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>

<span data-ttu-id="e1b16-249">Si vous souhaitez en savoir plus, consultez [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406).</span><span class="sxs-lookup"><span data-stu-id="e1b16-249">See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.</span></span>

<span data-ttu-id="e1b16-250">Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="e1b16-250">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-251">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-251">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-252">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-252">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-253">Nom unique de la stratégie de groupe : Update</span><span class="sxs-lookup"><span data-stu-id="e1b16-253">GP unique name: Update</span></span>
- <span data-ttu-id="e1b16-254">Nom de la stratégie de groupe : Remplacer la stratégie de mise à jour</span><span class="sxs-lookup"><span data-stu-id="e1b16-254">GP name: Update policy override</span></span>
- <span data-ttu-id="e1b16-255">Chemin de la stratégie de groupe :</span><span class="sxs-lookup"><span data-stu-id="e1b16-255">GP path:</span></span> 
  - <span data-ttu-id="e1b16-256">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1b16-256">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="e1b16-257">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="e1b16-257">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="e1b16-258">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="e1b16-258">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="e1b16-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="e1b16-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="e1b16-260">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-260">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-261">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-261">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-262">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-262">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-263">Nom de la valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-263">Value Name:</span></span> 
  - <span data-ttu-id="e1b16-264">(Stable) : Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="e1b16-264">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="e1b16-265">(Beta) : Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="e1b16-265">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="e1b16-266">(Canary) : Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="e1b16-266">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="e1b16-267">(Dev) : Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="e1b16-267">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="e1b16-268">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e1b16-268">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-269">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-269">Example value:</span></span>
```
always allow updates 0x00000001
Automatic silent updates only 0x00000003
manual updates only 0x00000002
updates disabled 0x00000000
```
[<span data-ttu-id="e1b16-270">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-270">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="allowsxs"></a><span data-ttu-id="e1b16-271">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="e1b16-271">Allowsxs</span></span>
#### <a name="allow-microsoft-edge-side-by-side-browser-experience"></a><span data-ttu-id="e1b16-272">Autoriser l’expérience de navigateur côte à côte Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1b16-272">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="e1b16-273">Microsoft Edge Update 1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-273">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-274">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-274">Description</span></span>
<span data-ttu-id="e1b16-275">Cette stratégie permet à un utilisateur d’exécuter Microsoft Edge (HTML Edge) et Microsoft Edge (basé sur Chromium) côte à côte.</span><span class="sxs-lookup"><span data-stu-id="e1b16-275">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="e1b16-276">Si cette stratégie est définie sur « Non configuré », Microsoft Edge (basée sur Chromium) remplace Microsoft Edge (Edge HTML) après installation du canal stable Microsoft Edge (basé sur Chromium) et des mises à jour de sécurité de novembre 2019.</span><span class="sxs-lookup"><span data-stu-id="e1b16-276">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="e1b16-277">C’est le même comportement que le paramètre « Désactivé ».</span><span class="sxs-lookup"><span data-stu-id="e1b16-277">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="e1b16-278">Le paramètre « Désactivé » bloque une expérience côte-à-côte et Microsoft Edge (basée sur Chromium) remplace Microsoft Edge (Edge HTML) après installation du canal stable Microsoft Edge (basé sur Chromium) et des mises à jour de sécurité de novembre 2019.</span><span class="sxs-lookup"><span data-stu-id="e1b16-278">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="e1b16-279">C’est le même comportement que le paramètre « Non configuré ».</span><span class="sxs-lookup"><span data-stu-id="e1b16-279">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="e1b16-280">Lorsque cette stratégie est « Activée », Microsoft Edge (basé sur Chromium) et Microsoft Edge (Edge HTML) peuvent s’exécuter côte à côte après l’installation de Microsoft Edge (basé sur Chromium).</span><span class="sxs-lookup"><span data-stu-id="e1b16-280">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="e1b16-281">Pour que cette stratégie de groupe prenne effet, elle doit être configurée avant l’installation automatique de Microsoft Edge (basé sur Chromium) par Windows Update.</span><span class="sxs-lookup"><span data-stu-id="e1b16-281">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="e1b16-282">Remarque : un utilisateur peut bloquer la mise à jour automatique de Microsoft Edge (basé sur Chromium) à l’aide du kit de ressources de bloqueur Microsoft Edge (basé sur Chromium).</span><span class="sxs-lookup"><span data-stu-id="e1b16-282">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-283">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-283">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-284">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-284">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-285">Nom unique de la stratégie de groupe : Allowsxs</span><span class="sxs-lookup"><span data-stu-id="e1b16-285">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="e1b16-286">Nom de la stratégie de groupe : Autoriser l’expérience de navigateur côte à côte Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1b16-286">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="e1b16-287">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="e1b16-287">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="e1b16-288">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-288">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-289">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-289">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-290">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-290">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-291">Nom de la valeur : Allowsxs</span><span class="sxs-lookup"><span data-stu-id="e1b16-291">Value Name: Allowsxs</span></span>
- <span data-ttu-id="e1b16-292">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e1b16-292">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-293">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-293">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e1b16-294">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-294">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="createdesktopshortcutdefault"></a><span data-ttu-id="e1b16-295">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="e1b16-295">CreateDesktopShortcutDefault</span></span>
#### <a name="prevent-desktop-shortcut-creation-upon-install-default"></a><span data-ttu-id="e1b16-296">Empêcher la création du Raccourci Bureau lors de l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="e1b16-296">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="e1b16-297">Microsoft Edge Update 1.3.128.0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-297">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-298">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-298">Description</span></span>
<span data-ttu-id="e1b16-299">Vous permet de spécifier le comportement par défaut de tous les canaux pour créer un raccourci bureau lorsque Microsoft Edge est installé.</span><span class="sxs-lookup"><span data-stu-id="e1b16-299">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="e1b16-300">Si vous activez cette stratégie, un raccourci bureau est créé lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e1b16-300">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="e1b16-301">Si vous désactivez cette stratégie, aucun raccourci bureau n’est créé lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e1b16-301">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="e1b16-302">Si vous ne configurez pas cette stratégie, un raccourci bureau vers Microsoft Edge est créé pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="e1b16-302">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="e1b16-303">Si Microsoft Edge est déjà installé, cette stratégie n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="e1b16-303">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-304">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-304">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-305">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-305">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-306">Nom unique de stratégie de groupe : CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="e1b16-306">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="e1b16-307">Nom de stratégie de groupe : empêcher la création du Raccourci Bureau lors de l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="e1b16-307">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="e1b16-308">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="e1b16-308">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="e1b16-309">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-309">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-310">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-310">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-311">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-311">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-312">Nom de valeur : CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="e1b16-312">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="e1b16-313">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e1b16-313">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-314">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-314">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e1b16-315">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-315">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="createdesktopshortcut"></a><span data-ttu-id="e1b16-316">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="e1b16-316">CreateDesktopShortcut</span></span>
#### <a name="prevent-desktop-shortcut-creation-upon-install"></a><span data-ttu-id="e1b16-317">Empêcher la création du Raccourci Bureau lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="e1b16-317">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="e1b16-318">Microsoft Edge Update 1.3.128.0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-318">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-319">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-319">Description</span></span>
<span data-ttu-id="e1b16-320">Si vous activez cette stratégie, un raccourci bureau est créé lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e1b16-320">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="e1b16-321">Si vous désactivez cette stratégie, aucun raccourci bureau n’est créé lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e1b16-321">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="e1b16-322">Si vous ne configurez pas cette stratégie, un raccourci bureau vers Microsoft Edge est créé pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="e1b16-322">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="e1b16-323">Si Microsoft Edge est déjà installé, cette stratégie n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="e1b16-323">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="e1b16-324">Si vous ne configurez pas cette stratégie pour un canal, la configuration de stratégie « [Empêcher la création de raccourcis clavier lors de l’installation de la configuration de stratégie par défaut](#createdesktopshortcutdefault) » définit la création d’un raccourci lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e1b16-324">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-325">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-325">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-326">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-326">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-327">Nom unique de stratégie de groupe : CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="e1b16-327">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="e1b16-328">Nom de stratégie de groupe : empêcher la création du Raccourci Bureau lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="e1b16-328">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="e1b16-329">Chemin de la stratégie de groupe :</span><span class="sxs-lookup"><span data-stu-id="e1b16-329">GP path:</span></span> 
  - <span data-ttu-id="e1b16-330">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1b16-330">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="e1b16-331">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="e1b16-331">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="e1b16-332">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="e1b16-332">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="e1b16-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="e1b16-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="e1b16-334">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-334">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-335">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-335">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-336">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-336">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-337">Nom de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-337">Value Name:</span></span> 
  - <span data-ttu-id="e1b16-338">(Stable) : CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="e1b16-338">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="e1b16-339">(Bêta) : CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="e1b16-339">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="e1b16-340">(Canary) : CreateDesktopShortcut {65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="e1b16-340">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="e1b16-341">(Dev) : CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="e1b16-341">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="e1b16-342">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e1b16-342">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-343">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-343">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e1b16-344">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-344">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="rollbacktotargetversion"></a><span data-ttu-id="e1b16-345">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="e1b16-345">RollbackToTargetVersion</span></span>
#### <a name="rollback-to-target-version"></a><span data-ttu-id="e1b16-346">Restaurez la version Cible</span><span class="sxs-lookup"><span data-stu-id="e1b16-346">Rollback to Target version</span></span>
><span data-ttu-id="e1b16-347">Microsoft Edge Update 1.3.133.3 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-347">Microsoft Edge Update 1.3.133.3 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-348">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-348">Description</span></span>
<span data-ttu-id="e1b16-349">Spécifie que Microsoft Edge Update doit restaurer les installations de Microsoft Edge à la version indiquée dans «[Remplacement de la version cible](#targetversionprefix)».</span><span class="sxs-lookup"><span data-stu-id="e1b16-349">Specifies that Microsoft Edge Update should rollback installations of Microsoft Edge to the version indicated in '[Target version override](#targetversionprefix)'.</span></span>

<span data-ttu-id="e1b16-350">Cette stratégie n’a aucun effet, sauf si «[Remplacement de la version cible](#targetversionprefix)» est défini et «[Remplacement de la stratégie de mise à jour](#update)» est défini à l’un des états d’activation (Toujours autoriser les mises à jour, Mises à jour automatiques silencieuses uniquement, Mises à jour manuelles uniquement).</span><span class="sxs-lookup"><span data-stu-id="e1b16-350">This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).</span></span>

<span data-ttu-id="e1b16-351">Si vous désactivez cette stratégie ou si vous ne la configurez pas, les installations dont la version est supérieure à celle spécifiée par «[Remplacement de la version cible](#targetversionprefix)» sont conservées.</span><span class="sxs-lookup"><span data-stu-id="e1b16-351">If you disable this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.</span></span>

<span data-ttu-id="e1b16-352">Si vous activez cette stratégie, les installations qui ont une version actuelle supérieure à celle spécifiée par «[Remplacement de la version cible](#targetversionprefix)» sont rétrogradées à la version cible.</span><span class="sxs-lookup"><span data-stu-id="e1b16-352">If you enable this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.</span></span>

<span data-ttu-id="e1b16-353">Nous recommandons aux utilisateurs d’installer la dernière version du navigateur Microsoft Edge afin de profiter de la protection offerte par les dernières mises à jour de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e1b16-353">We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates.</span></span> <span data-ttu-id="e1b16-354">La restauration à une version antérieure présente des risques d’exposition aux problèmes de sécurité connus.</span><span class="sxs-lookup"><span data-stu-id="e1b16-354">Rollback to an earlier version risks exposure to known security issues.</span></span> <span data-ttu-id="e1b16-355">Cette stratégie est destinée à être utilisée comme correctif temporaire pour résoudre les problèmes de mise à jour du navigateur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e1b16-355">This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.</span></span>

<span data-ttu-id="e1b16-356">Avant de restaurer temporairement la version de votre navigateur, nous vous recommandons d’activer la Synchronisation ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) pour tous les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e1b16-356">Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization.</span></span> <span data-ttu-id="e1b16-357">Si vous n’activez pas la Synchronisation, vous risquez de perdre définitivement les données de navigation.</span><span class="sxs-lookup"><span data-stu-id="e1b16-357">If you don't turn on Sync, there is a risk of permanent browsing data loss.</span></span> <span data-ttu-id="e1b16-358">L’ utilisation de cette stratégie comporte des risques.</span><span class="sxs-lookup"><span data-stu-id="e1b16-358">Use this policy at your own risk.</span></span>

<span data-ttu-id="e1b16-359">Remarque : Vous pouvez afficher toutes les versions disponibles pour la restauration ici [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="e1b16-359">Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="e1b16-360">Cette stratégie s’applique à Microsoft Edge version 86 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e1b16-360">This policy applies to Microsoft Edge version 86 or later.</span></span>

<span data-ttu-id="e1b16-361">Si vous souhaitez en savoir plus, consultez [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918).</span><span class="sxs-lookup"><span data-stu-id="e1b16-361">See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.</span></span>

<span data-ttu-id="e1b16-362">Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="e1b16-362">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-363">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-363">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-364">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-364">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-365">Nom unique GP : RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="e1b16-365">GP unique name: RollbackToTargetVersion</span></span>
- <span data-ttu-id="e1b16-366">Nom GP: Restaurez la version Cible</span><span class="sxs-lookup"><span data-stu-id="e1b16-366">GP name: Rollback to Target version</span></span>
- <span data-ttu-id="e1b16-367">Chemin de la stratégie de groupe :</span><span class="sxs-lookup"><span data-stu-id="e1b16-367">GP path:</span></span> 
  - <span data-ttu-id="e1b16-368">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1b16-368">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="e1b16-369">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="e1b16-369">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="e1b16-370">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="e1b16-370">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="e1b16-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="e1b16-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="e1b16-372">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-372">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-373">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-373">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-374">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-374">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-375">Nom de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-375">Value Name:</span></span> 
  - <span data-ttu-id="e1b16-376">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="e1b16-376">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="e1b16-377">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="e1b16-377">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="e1b16-378">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="e1b16-378">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="e1b16-379">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="e1b16-379">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="e1b16-380">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e1b16-380">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-381">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-381">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e1b16-382">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-382">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="targetversionprefix"></a><span data-ttu-id="e1b16-383">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="e1b16-383">TargetVersionPrefix</span></span>
#### <a name="target-version-override"></a><span data-ttu-id="e1b16-384">Remplacement de la version cible</span><span class="sxs-lookup"><span data-stu-id="e1b16-384">Target version override</span></span>
><span data-ttu-id="e1b16-385">Microsoft Edge Update 1.3.119.43 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-385">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-386">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-386">Description</span></span>
<span data-ttu-id="e1b16-387">Lorsque cette stratégie est activée et que la mise à jour automatique est activée, Microsoft Edge est mis à jour vers la version spécifiée par cette valeur de stratégie.</span><span class="sxs-lookup"><span data-stu-id="e1b16-387">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="e1b16-388">La valeur de la stratégie doit être une version spécifique de Microsoft Edge, par exemple, 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="e1b16-388">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="e1b16-389">Si la version de Microsoft Edge d’un appareil est plus récente que la valeur spécifiée, Microsoft Edge reste sur la version la plus récente et n’est pas rétrogradé vers la version spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e1b16-389">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="e1b16-390">Si la version spécifiée n’existe pas ou n’est pas mise en forme de manière correcte, Microsoft Edge reste sur sa version actuelle et ne sera pas mise à jour automatiquement vers les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1b16-390">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>

<span data-ttu-id="e1b16-391">Si vous souhaitez en savoir plus, consultez [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707).</span><span class="sxs-lookup"><span data-stu-id="e1b16-391">See [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) for more information.</span></span>

<span data-ttu-id="e1b16-392">Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="e1b16-392">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-393">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-393">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-394">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-394">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-395">Nom unique de stratégie de groupe : TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="e1b16-395">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="e1b16-396">Nom de stratégie de groupe : Remplacement de la version cible</span><span class="sxs-lookup"><span data-stu-id="e1b16-396">GP name: Target version override</span></span>
- <span data-ttu-id="e1b16-397">Chemin de la stratégie de groupe :</span><span class="sxs-lookup"><span data-stu-id="e1b16-397">GP path:</span></span> 
  - <span data-ttu-id="e1b16-398">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1b16-398">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="e1b16-399">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="e1b16-399">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="e1b16-400">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="e1b16-400">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="e1b16-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="e1b16-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="e1b16-402">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-402">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-403">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-403">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-404">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-404">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-405">Nom de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-405">Value Name:</span></span> 
  - <span data-ttu-id="e1b16-406">(Stable) : TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="e1b16-406">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="e1b16-407">(Beta) : TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="e1b16-407">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="e1b16-408">(Canary) : TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="e1b16-408">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="e1b16-409">(Dev) : TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="e1b16-409">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="e1b16-410">Type de valeur : REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e1b16-410">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-411">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-411">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="e1b16-412">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-412">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="preferences-policies"></a><span data-ttu-id="e1b16-413">Stratégies de préférences</span><span class="sxs-lookup"><span data-stu-id="e1b16-413">Preferences policies</span></span>

[<span data-ttu-id="e1b16-414">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-414">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="autoupdatecheckperiodminutes"></a><span data-ttu-id="e1b16-415">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="e1b16-415">AutoUpdateCheckPeriodMinutes</span></span>
#### <a name="auto-update-check-period-override"></a><span data-ttu-id="e1b16-416">Remplacement de la période de vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="e1b16-416">Auto-update check period override</span></span>
><span data-ttu-id="e1b16-417">Microsoft Edge Update 1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-417">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-418">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-418">Description</span></span>
<span data-ttu-id="e1b16-419">Si elle est activée, cette stratégie vous permet de définir une valeur pour le nombre minimal de minutes entre les recherches automatiques de mises à jour.</span><span class="sxs-lookup"><span data-stu-id="e1b16-419">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="e1b16-420">Dans le cas contraire, par défaut, la mise à jour automatique recherche les mises à jour toutes les 10 heures.</span><span class="sxs-lookup"><span data-stu-id="e1b16-420">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="e1b16-421">Si vous souhaitez désactiver toutes les vérifications de mise à jour automatique, définissez la valeur sur 0 (non recommandé).</span><span class="sxs-lookup"><span data-stu-id="e1b16-421">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-422">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-422">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-423">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-423">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-424">Nom unique de la stratégie de groupe : AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="e1b16-424">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="e1b16-425">Nom de la stratégie de groupe : Remplacement de la période de vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="e1b16-425">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="e1b16-426">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Preferences</span><span class="sxs-lookup"><span data-stu-id="e1b16-426">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="e1b16-427">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-427">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-428">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-428">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-429">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-429">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-430">Nom de la valeur : AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="e1b16-430">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="e1b16-431">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e1b16-431">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-432">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-432">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="e1b16-433">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-433">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="updatessuppressed"></a><span data-ttu-id="e1b16-434">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="e1b16-434">UpdatesSuppressed</span></span>
#### <a name="time-period-in-each-day-to-suppress-auto-update-check"></a><span data-ttu-id="e1b16-435">Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="e1b16-435">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="e1b16-436">Microsoft Edge Update 1.3.33.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-436">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-437">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-437">Description</span></span>
<span data-ttu-id="e1b16-438">Si vous activez cette stratégie, les vérifications de mise à jour sont supprimées chaque jour à partir de Heure:Minute pendant une Durée (en minutes).</span><span class="sxs-lookup"><span data-stu-id="e1b16-438">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="e1b16-439">La durée n’est pas affectée par l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="e1b16-439">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="e1b16-440">Par exemple, si l’heure de début est 22:00 et que la durée est 480 minutes, les mises à jour seront supprimées pendant exactement 8 heures, même si l’heure d’été commence ou se termine pendant cette période.</span><span class="sxs-lookup"><span data-stu-id="e1b16-440">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="e1b16-441">Si vous désactivez ou que vous ne configurez pas cette stratégie, les vérifications de mise à jour ne sont pas supprimées pendant une période spécifique.</span><span class="sxs-lookup"><span data-stu-id="e1b16-441">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-442">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-442">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-443">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-443">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-444">Nom unique de la stratégie de groupe : UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="e1b16-444">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="e1b16-445">Nom de la stratégie de groupe : Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="e1b16-445">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="e1b16-446">Options { Hour, Minute, Duration }</span><span class="sxs-lookup"><span data-stu-id="e1b16-446">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="e1b16-447">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Preferences</span><span class="sxs-lookup"><span data-stu-id="e1b16-447">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="e1b16-448">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-448">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-449">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-449">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-450">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-450">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-451">Nom de la valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-451">Value Name:</span></span> 
  - <span data-ttu-id="e1b16-452">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="e1b16-452">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="e1b16-453">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="e1b16-453">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="e1b16-454">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="e1b16-454">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="e1b16-455">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e1b16-455">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-456">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-456">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="e1b16-457">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-457">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="proxy-server-policies"></a><span data-ttu-id="e1b16-458">Stratégies de serveur proxy</span><span class="sxs-lookup"><span data-stu-id="e1b16-458">Proxy Server policies</span></span>

[<span data-ttu-id="e1b16-459">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-459">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="proxymode"></a><span data-ttu-id="e1b16-460">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="e1b16-460">ProxyMode</span></span>
#### <a name="choose-how-to-specify-proxy-server-settings"></a><span data-ttu-id="e1b16-461">Choisir comment spécifier les paramètres du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="e1b16-461">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="e1b16-462">Microsoft Edge Update 1.3.21.81 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-462">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-463">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-463">Description</span></span>
<span data-ttu-id="e1b16-464">Permet de spécifier les paramètres de serveur proxy qui sont utilisés par Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e1b16-464">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="e1b16-465">Si vous activez cette stratégie, vous pouvez choisir l’une des options de serveur proxy suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1b16-465">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="e1b16-466">Si vous choisissez de ne jamais utiliser un serveur proxy et de toujours vous connecter directement, toutes les autres options sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="e1b16-466">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="e1b16-467">Si vous choisissez d’utiliser les paramètres de proxy système ou de détection automatique du serveur proxy, toutes les autres options sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="e1b16-467">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="e1b16-468">Si vous choisissez le mode de serveur proxy fixe, vous pouvez spécifier d’autres options dans la stratégie [« Adresse ou URL du serveur proxy »](#proxyserver).</span><span class="sxs-lookup"><span data-stu-id="e1b16-468">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="e1b16-469">Si vous choisissez d’utiliser un script de proxy .pac, vous devez spécifier l’URL du script dans la stratégie [« URL d’un fichier proxy. pac »](#proxypacurl).</span><span class="sxs-lookup"><span data-stu-id="e1b16-469">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="e1b16-470">Si vous activez cette stratégie, les utilisateurs de votre organisation ne peuvent pas modifier les paramètres du proxy dans Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e1b16-470">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="e1b16-471">Si vous désactivez ou que vous ne configurez pas cette stratégie, aucun paramètre de serveur proxy n’est configuré, mais les utilisateurs de votre organisation peuvent choisir leurs propres paramètres de proxy pour Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e1b16-471">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-472">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-472">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-473">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-473">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-474">Nom unique de la stratégie de groupe : ProxyMode</span><span class="sxs-lookup"><span data-stu-id="e1b16-474">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="e1b16-475">Nom de la stratégie de groupe : Choisir comment spécifier les paramètres du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="e1b16-475">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="e1b16-476">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="e1b16-476">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="e1b16-477">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-477">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-478">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-478">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-479">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-479">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-480">Nom de la valeur : ProxyMode</span><span class="sxs-lookup"><span data-stu-id="e1b16-480">Value Name: ProxyMode</span></span>
- <span data-ttu-id="e1b16-481">Type de valeur : REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e1b16-481">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-482">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-482">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="e1b16-483">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-483">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="proxypacurl"></a><span data-ttu-id="e1b16-484">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="e1b16-484">ProxyPacUrl</span></span>
#### <a name="url-to-a-proxy-pac-file"></a><span data-ttu-id="e1b16-485">URL d’un fichier proxy. pac</span><span class="sxs-lookup"><span data-stu-id="e1b16-485">URL to a proxy .pac file</span></span>
><span data-ttu-id="e1b16-486">Microsoft Edge Update 1.3.21.81 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-486">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-487">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-487">Description</span></span>
<span data-ttu-id="e1b16-488">Permet de spécifier une URL pour un fichier de configuration automatique de proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="e1b16-488">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="e1b16-489">Si vous activez cette stratégie, vous pouvez spécifier une URL pour un fichier PAC pour automatiser la façon dont Microsoft Edge Update sélectionne le serveur proxy approprié pour l’extraction d’un site web particulier.</span><span class="sxs-lookup"><span data-stu-id="e1b16-489">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="e1b16-490">Cette stratégie est appliquée uniquement si vous avez spécifié des paramètres de proxy manuels dans la stratégie « [Choisir comment spécifier les paramètres du serveur proxy](#proxymode) ».</span><span class="sxs-lookup"><span data-stu-id="e1b16-490">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="e1b16-491">Ne configurez pas cette stratégie si vous avez sélectionné un paramètre de proxy autre que manuel dans la stratégie « [Choisir comment spécifier les paramètres du serveur proxy](#proxymode) ».</span><span class="sxs-lookup"><span data-stu-id="e1b16-491">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-492">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-492">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-493">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-493">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-494">Nom unique de la stratégie de groupe : ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="e1b16-494">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="e1b16-495">Nom de la stratégie de groupe : URL d’un fichier proxy. pac</span><span class="sxs-lookup"><span data-stu-id="e1b16-495">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="e1b16-496">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="e1b16-496">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="e1b16-497">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-497">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-498">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-498">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-499">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-499">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-500">Nom de la valeur : ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="e1b16-500">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="e1b16-501">Type de valeur : REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e1b16-501">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-502">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-502">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="e1b16-503">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-503">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="proxyserver"></a><span data-ttu-id="e1b16-504">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="e1b16-504">ProxyServer</span></span>
#### <a name="address-or-url-of-proxy-server"></a><span data-ttu-id="e1b16-505">Adresse ou URL du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="e1b16-505">Address or URL of proxy server</span></span>
><span data-ttu-id="e1b16-506">Microsoft Edge Update 1.3.21.81 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-506">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-507">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-507">Description</span></span>
<span data-ttu-id="e1b16-508">Permet de spécifier l’URL du serveur proxy que Microsoft Edge Update doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="e1b16-508">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="e1b16-509">Si vous activez cette stratégie, vous pouvez définir l’URL de serveur proxy utilisée par Microsoft Edge Update dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e1b16-509">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="e1b16-510">Cette stratégie est appliquée uniquement si vous avez sélectionné plusieurs paramètres de proxy manuels dans la stratégie « [Choisir comment spécifier les paramètres du serveur proxy](#proxymode) ».</span><span class="sxs-lookup"><span data-stu-id="e1b16-510">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="e1b16-511">Ne configurez pas cette stratégie si vous avez sélectionné un paramètre de proxy autre que manuel dans la stratégie « [Choisir comment spécifier les paramètres du serveur proxy](#proxymode) ».</span><span class="sxs-lookup"><span data-stu-id="e1b16-511">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-512">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-512">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-513">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-513">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-514">Nom unique de la stratégie de groupe : ProxyServer</span><span class="sxs-lookup"><span data-stu-id="e1b16-514">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="e1b16-515">Nom de la stratégie de groupe : Adresse ou URL du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="e1b16-515">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="e1b16-516">Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="e1b16-516">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="e1b16-517">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-517">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-518">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-518">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-519">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-519">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-520">Nom de la valeur : ProxyServer</span><span class="sxs-lookup"><span data-stu-id="e1b16-520">Value Name: ProxyServer</span></span>
- <span data-ttu-id="e1b16-521">Type de valeur : REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e1b16-521">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-522">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-522">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="e1b16-523">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-523">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="microsoft-edge-webview-policies"></a><span data-ttu-id="e1b16-524">Stratégies d’affichage web Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1b16-524">Microsoft Edge WebView policies</span></span>

[<span data-ttu-id="e1b16-525">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-525">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="install-webview"></a><span data-ttu-id="e1b16-526">Installation (Affichage web)</span><span class="sxs-lookup"><span data-stu-id="e1b16-526">Install (WebView)</span></span>
#### <a name="allow-installation"></a><span data-ttu-id="e1b16-527">Autoriser l’installation</span><span class="sxs-lookup"><span data-stu-id="e1b16-527">Allow installation</span></span>
><span data-ttu-id="e1b16-528">Microsoft Edge Update 1.3.127.1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-528">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-529">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-529">Description</span></span>
<span data-ttu-id="e1b16-530">Vous permet de spécifier si un affichage web de Microsoft Edge peut être installé à l’aide de Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e1b16-530">Lets you specify whether Microsoft Edge WebView can be installed using Microsoft Edge Update.</span></span>

  - <span data-ttu-id="e1b16-531">Si vous activez cette stratégie, les utilisateurs peuvent installer l’affichage web de Microsoft Edge via Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e1b16-531">If you enable this policy, users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="e1b16-532">Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas installer l’affichage web de Microsoft Edge via Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e1b16-532">If you disable this policy, users cannot install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="e1b16-533">Si vous ne configurez pas cette stratégie, la configuration de la stratégie «[Autoriser l’installation par défaut](#installdefault)» détermine si les utilisateurs peuvent installer l’Affichage web Microsoft Edge via Microsoft Edge Update.</span><span class="sxs-lookup"><span data-stu-id="e1b16-533">If you don't configure this policy, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-534">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-534">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-535">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-535">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-536">Nom unique de la stratégie de groupe : Install</span><span class="sxs-lookup"><span data-stu-id="e1b16-536">GP unique name: Install</span></span>
- <span data-ttu-id="e1b16-537">Nom de la stratégie de groupe : Autoriser l’installation</span><span class="sxs-lookup"><span data-stu-id="e1b16-537">GP name: Allow installation</span></span>
- <span data-ttu-id="e1b16-538">Chemin d’accès de la stratégie de groupe : Modèles administratifs/Microsoft Edge Update/Applications/Affichage web Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1b16-538">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="e1b16-539">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-539">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-540">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-540">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-541">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-541">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-542">Nom de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-542">Value Name:</span></span> 
  - <span data-ttu-id="e1b16-543">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="e1b16-543">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="e1b16-544">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e1b16-544">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-545">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-545">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e1b16-546">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-546">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="update-webview"></a><span data-ttu-id="e1b16-547">Mise à jour (Affichage web)</span><span class="sxs-lookup"><span data-stu-id="e1b16-547">Update (WebView)</span></span>
#### <a name="update-policy-override"></a><span data-ttu-id="e1b16-548">Remplacer la stratégie de mise à jour</span><span class="sxs-lookup"><span data-stu-id="e1b16-548">Update policy override</span></span>
><span data-ttu-id="e1b16-549">Microsoft Edge Update 1.3.127.1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e1b16-549">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <a name="description"></a><span data-ttu-id="e1b16-550">Description</span><span class="sxs-lookup"><span data-stu-id="e1b16-550">Description</span></span>
<span data-ttu-id="e1b16-551">Vous permet de spécifier si les mises à jour automatiques sont activées pour l’affichage web de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e1b16-551">Lets you specify whether or not automatic updates are enabled for Microsoft Edge WebView.</span></span> <span data-ttu-id="e1b16-552">L’affichage web de Microsoft Edge est un composant utilisé par les applications pour afficher du contenu web.</span><span class="sxs-lookup"><span data-stu-id="e1b16-552">Microsoft Edge WebView is a component used by applications to display web content.</span></span>
<span data-ttu-id="e1b16-553">Les mises à jour automatiques sont activées par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1b16-553">Automatic updates are enabled by default.</span></span> <span data-ttu-id="e1b16-554">La désactivation des mises à jour automatiques pour l’affichage web de Microsoft Edge peut entraîner des problèmes de compatibilité avec les applications qui dépendent de ce composant.</span><span class="sxs-lookup"><span data-stu-id="e1b16-554">Disabling automatic updates for Microsoft Edge WebView might cause compatibility issues with applications that depend on this component.</span></span>

  <span data-ttu-id="e1b16-555">Si vous activez cette stratégie, Microsoft Edge Update gère les mises à jour de l’affichage web de Microsoft Edge en fonction de la façon dont vous configurez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1b16-555">If you enable this policy, Microsoft Edge Update handles Microsoft Edge WebView updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="e1b16-556">Toujours autoriser les mises à jour : les mises à jour sont téléchargées et appliquées automatiquement</span><span class="sxs-lookup"><span data-stu-id="e1b16-556">Always allow updates: Updates are automatically downloaded and applied</span></span>
  - <span data-ttu-id="e1b16-557">Mises à jour désactivées : les mises à jour ne sont jamais téléchargées ou appliquées.</span><span class="sxs-lookup"><span data-stu-id="e1b16-557">Updates disabled: Updates are never downloaded or applied</span></span>

  <span data-ttu-id="e1b16-558">Si vous n’activez pas cette stratégie, les mises à jour sont automatiquement téléchargées et appliquées.</span><span class="sxs-lookup"><span data-stu-id="e1b16-558">If you don't enable this policy, updates are automatically downloaded and applied.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="e1b16-559">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-559">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="e1b16-560">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e1b16-560">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="e1b16-561">Nom unique de la stratégie de groupe : Update</span><span class="sxs-lookup"><span data-stu-id="e1b16-561">GP unique name: Update</span></span>
- <span data-ttu-id="e1b16-562">Nom de la stratégie de groupe : Remplacer la stratégie de mise à jour</span><span class="sxs-lookup"><span data-stu-id="e1b16-562">GP name: Update policy override</span></span>
- <span data-ttu-id="e1b16-563">Chemin d’accès de la stratégie de groupe : Modèles administratifs/Microsoft Edge Update/Applications/Affichage web Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1b16-563">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="e1b16-564">Nom du fichier GP ADMX: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="e1b16-564">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="e1b16-565">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="e1b16-565">Windows Registry Settings</span></span>
- <span data-ttu-id="e1b16-566">Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="e1b16-566">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="e1b16-567">Nom de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-567">Value Name:</span></span> 
  - <span data-ttu-id="e1b16-568">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="e1b16-568">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="e1b16-569">Type de valeur : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e1b16-569">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="e1b16-570">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="e1b16-570">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="e1b16-571">Retour au début</span><span class="sxs-lookup"><span data-stu-id="e1b16-571">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="see-also"></a><span data-ttu-id="e1b16-572">Voir également</span><span class="sxs-lookup"><span data-stu-id="e1b16-572">See also</span></span>
  - [<span data-ttu-id="e1b16-573">Configuration de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1b16-573">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="e1b16-574">Page d’accueil Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="e1b16-574">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
