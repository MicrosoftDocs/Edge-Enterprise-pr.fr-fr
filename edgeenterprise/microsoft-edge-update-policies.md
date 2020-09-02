---
title: Documentation relative aux stratégies Microsoft Edge Update
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 06/10/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentation relative à toutes les stratégies prises en charge par le programme de mise à jour MicrosoftEdge
ms.openlocfilehash: d772d8dd6f60b89e9bd12a77b740e5fad699756a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979782"
---
# <span data-ttu-id="0f52a-103">Microsoft Edge - Stratégies de mise à jour</span><span class="sxs-lookup"><span data-stu-id="0f52a-103">Microsoft Edge - Update policies</span></span>
<span data-ttu-id="0f52a-104">La dernière version de MicrosoftEdge comprend les stratégies suivantes que vous pouvez utiliser pour contrôler comment et quand MicrosoftEdge est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="0f52a-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

           
<span data-ttu-id="0f52a-105">Pour plus d’informations sur les autres stratégies disponibles dans MicrosoftEdge, consultez la [Référence de stratégies du navigateur MicrosoftEdge](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="0f52a-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="0f52a-106">Cet article concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0f52a-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="0f52a-107">Stratégies disponibles</span><span class="sxs-lookup"><span data-stu-id="0f52a-107">Available policies</span></span>
<span data-ttu-id="0f52a-108">Ces tableaux répertorient toutes les stratégies de groupe relatives aux mises à jour disponibles dans cette version de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="0f52a-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="0f52a-109">Utilisez les liens dans le tableau pour obtenir plus de détails sur des stratégies données.</span><span class="sxs-lookup"><span data-stu-id="0f52a-109">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="0f52a-110">Applications</span><span class="sxs-lookup"><span data-stu-id="0f52a-110">Applications</span></span>](#applications)|[<span data-ttu-id="0f52a-111">Préférences</span><span class="sxs-lookup"><span data-stu-id="0f52a-111">Preferences</span></span>](#preferences)|
|[<span data-ttu-id="0f52a-112">Serveur proxy</span><span class="sxs-lookup"><span data-stu-id="0f52a-112">Proxy Server</span></span>](#proxy-server)||

### [<span data-ttu-id="0f52a-113">Applications</span><span class="sxs-lookup"><span data-stu-id="0f52a-113">Applications</span></span>](#applications-policies)
|<span data-ttu-id="0f52a-114">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="0f52a-114">Policy Name</span></span>|<span data-ttu-id="0f52a-115">Caption</span><span class="sxs-lookup"><span data-stu-id="0f52a-115">Caption</span></span>|
|-|-|
|[<span data-ttu-id="0f52a-116">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="0f52a-116">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="0f52a-117">Autoriser l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="0f52a-117">Allow installation default</span></span>|
|[<span data-ttu-id="0f52a-118">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="0f52a-118">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="0f52a-119">Remplacer la stratégie de mise à jour par défaut</span><span class="sxs-lookup"><span data-stu-id="0f52a-119">Update policy override default</span></span>|
|[<span data-ttu-id="0f52a-120">Installer</span><span class="sxs-lookup"><span data-stu-id="0f52a-120">Install</span></span>](#install)|<span data-ttu-id="0f52a-121">Autoriser l’installation (par canal)</span><span class="sxs-lookup"><span data-stu-id="0f52a-121">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="0f52a-122">Update</span><span class="sxs-lookup"><span data-stu-id="0f52a-122">Update</span></span>](#update)|<span data-ttu-id="0f52a-123">Remplacer la stratégie de mise à jour (par canal)</span><span class="sxs-lookup"><span data-stu-id="0f52a-123">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="0f52a-124">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="0f52a-124">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="0f52a-125">Autoriser l’expérience de navigateur côte à côte MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="0f52a-125">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="0f52a-126">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="0f52a-126">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="0f52a-127">Empêcher la création du Raccourci Bureau lors de l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="0f52a-127">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="0f52a-128">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="0f52a-128">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="0f52a-129">Empêcher la création du Raccourci Bureau lors de l’installation (par canal)</span><span class="sxs-lookup"><span data-stu-id="0f52a-129">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="0f52a-130">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="0f52a-130">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="0f52a-131">Remplacement de la version cible (par canal)</span><span class="sxs-lookup"><span data-stu-id="0f52a-131">Target version override (per channel)</span></span>|

### [<span data-ttu-id="0f52a-132">Préférences</span><span class="sxs-lookup"><span data-stu-id="0f52a-132">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="0f52a-133">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="0f52a-133">Policy Name</span></span>|<span data-ttu-id="0f52a-134">Caption</span><span class="sxs-lookup"><span data-stu-id="0f52a-134">Caption</span></span>|
|-|-|
|[<span data-ttu-id="0f52a-135">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="0f52a-135">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="0f52a-136">Remplacement de la période de vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="0f52a-136">Auto-update check period override</span></span>|
|[<span data-ttu-id="0f52a-137">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="0f52a-137">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="0f52a-138">Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="0f52a-138">Time period in each day to suppress auto-update check</span></span>|

### [<span data-ttu-id="0f52a-139">Serveur proxy</span><span class="sxs-lookup"><span data-stu-id="0f52a-139">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="0f52a-140">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="0f52a-140">Policy Name</span></span>|<span data-ttu-id="0f52a-141">Légende</span><span class="sxs-lookup"><span data-stu-id="0f52a-141">Caption</span></span>|
|-|-|
|[<span data-ttu-id="0f52a-142">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="0f52a-142">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="0f52a-143">Choisir comment spécifier les paramètres du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="0f52a-143">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="0f52a-144">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="0f52a-144">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="0f52a-145">URL d’un fichier proxy. pac</span><span class="sxs-lookup"><span data-stu-id="0f52a-145">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="0f52a-146">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="0f52a-146">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="0f52a-147">Adresse ou URL du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="0f52a-147">Address or URL of proxy server</span></span>|

                 
      
  
             
            
                  

## <span data-ttu-id="0f52a-148">Stratégies d’applications</span><span class="sxs-lookup"><span data-stu-id="0f52a-148">Applications policies</span></span>

[<span data-ttu-id="0f52a-149">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-149">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="0f52a-150">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="0f52a-150">InstallDefault</span></span>
#### <span data-ttu-id="0f52a-151">Autoriser l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="0f52a-151">Allow installation default</span></span>
><span data-ttu-id="0f52a-152">MicrosoftEdge Update1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f52a-152">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="0f52a-153">Description</span><span class="sxs-lookup"><span data-stu-id="0f52a-153">Description</span></span>
<span data-ttu-id="0f52a-154">Vous pouvez spécifier le comportement par défaut de tous les canaux pour autoriser ou bloquer les mises à jour Microsoft Edge lorsque Microsoft Edge Update est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0f52a-154">You can specify the default behavior of all channels to allow or block Microsoft Edge updates when Microsoft Edge Update is used.</span></span>

<span data-ttu-id="0f52a-155">Vous pouvez remplacer cette stratégie pour des canaux individuels en spécifiant la stratégie «[Autoriser l’installation](#install)» pour des canaux spécifiques.</span><span class="sxs-lookup"><span data-stu-id="0f52a-155">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="0f52a-156">Si vous désactivez cette stratégie, l’installation de MicrosoftEdge via MicrosoftEdge Update est bloquée.</span><span class="sxs-lookup"><span data-stu-id="0f52a-156">If you disable this policy, the installation of Microsoft Edge through Microsoft Edge Update is blocked.</span></span> <span data-ttu-id="0f52a-157">Ceci affecte l’installation du logiciel MicrosoftEdge uniquement lorsque les utilisateurs exécutent MicrosoftEdge Update et s’ils n’ont pas configuré la stratégie «[Autoriser l’installation](#install)».</span><span class="sxs-lookup"><span data-stu-id="0f52a-157">This only affects the installation of Microsoft Edge software only when users are running Microsoft Edge Update and when they haven't configured the '[Allow installation](#install)' policy.</span></span>

<span data-ttu-id="0f52a-158">Cette stratégie n’empêche pas MicrosoftEdge Update de s’exécuter, ni les utilisateurs d’installer le logiciel MicrosoftEdge en utilisant d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="0f52a-158">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>
#### <span data-ttu-id="0f52a-159">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-159">Windows information and settings</span></span>
##### <span data-ttu-id="0f52a-160">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0f52a-160">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="0f52a-161">Nom unique de la stratégie de groupe: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="0f52a-161">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="0f52a-162">Nom de la stratégie de groupe: Autoriser l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="0f52a-162">GP name: Allow installation default</span></span>
- <span data-ttu-id="0f52a-163">Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="0f52a-163">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="0f52a-164">Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="0f52a-164">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="0f52a-165">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-165">Windows Registry Settings</span></span>
- <span data-ttu-id="0f52a-166">Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="0f52a-166">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="0f52a-167">Nom de la valeur: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="0f52a-167">Value Name: InstallDefault</span></span>
- <span data-ttu-id="0f52a-168">Type de valeur: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="0f52a-168">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="0f52a-169">Exemple de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-169">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="0f52a-170">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-170">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="0f52a-171">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="0f52a-171">UpdateDefault</span></span>
#### <span data-ttu-id="0f52a-172">Remplacer la stratégie de mise à jour par défaut</span><span class="sxs-lookup"><span data-stu-id="0f52a-172">Update policy override default</span></span>
><span data-ttu-id="0f52a-173">MicrosoftEdge Update1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f52a-173">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="0f52a-174">Description</span><span class="sxs-lookup"><span data-stu-id="0f52a-174">Description</span></span>
<span data-ttu-id="0f52a-175">Permet de spécifier le comportement par défaut de tous les canaux concernant la façon dont MicrosoftEdge Update gère les mises à jour disponibles pour MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="0f52a-175">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="0f52a-176">Peut être remplacé pour des canaux individuels en spécifiant la stratégie «[Remplacer la stratégie de mise à jour](#update)» pour ces canaux spécifiques.</span><span class="sxs-lookup"><span data-stu-id="0f52a-176">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="0f52a-177">Si vous activez cette stratégie, MicrosoftEdge Update gère les mises à jour de MicrosoftEdge en fonction de la façon dont vous configurez les options suivantes:</span><span class="sxs-lookup"><span data-stu-id="0f52a-177">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="0f52a-178">Toujours autoriser les mises à jour: les mises à jour sont toujours appliquées lorsqu’elles sont trouvées, soit par une recherche de mise à jour périodique, soit par une recherche de mise à jour manuelle.</span><span class="sxs-lookup"><span data-stu-id="0f52a-178">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="0f52a-179">Mises à jour automatiques en mode silencieux uniquement: les mises à jour sont appliquées uniquement lorsqu’elles sont trouvées par la recherche de mise à jour périodique.</span><span class="sxs-lookup"><span data-stu-id="0f52a-179">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="0f52a-180">Mises à jour manuelles uniquement: les mises à jour sont appliquées uniquement lorsque l’utilisateur exécute une recherche de mise à jour manuelle.</span><span class="sxs-lookup"><span data-stu-id="0f52a-180">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="0f52a-181">Mises à jour désactivées: les mises à jour ne sont jamais appliquées.</span><span class="sxs-lookup"><span data-stu-id="0f52a-181">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="0f52a-182">Si vous sélectionnez les mises à jour manuelles, vérifiez régulièrement si des mises à jour sont disponibles à l’aide du mécanisme de mise à jour manuelle de l’application, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="0f52a-182">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="0f52a-183">Si vous désactivez les mises à jour, recherchez régulièrement les mises à jour et distribuez-les aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0f52a-183">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="0f52a-184">Si vous n’activez pas et ne configurez pas cette stratégie, MicrosoftEdge Update gère les mises à jour disponibles, comme spécifié par la stratégie «[Remplacer la stratégie de mise à jour](#update)».</span><span class="sxs-lookup"><span data-stu-id="0f52a-184">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>
#### <span data-ttu-id="0f52a-185">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-185">Windows information and settings</span></span>
##### <span data-ttu-id="0f52a-186">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0f52a-186">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="0f52a-187">Nom unique de la stratégie de groupe: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="0f52a-187">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="0f52a-188">Nom de la stratégie de groupe: Remplacer la stratégie de mise à jour par défaut</span><span class="sxs-lookup"><span data-stu-id="0f52a-188">GP name: Update policy override default</span></span>
- <span data-ttu-id="0f52a-189">Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="0f52a-189">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="0f52a-190">Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="0f52a-190">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="0f52a-191">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-191">Windows Registry Settings</span></span>
- <span data-ttu-id="0f52a-192">Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="0f52a-192">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="0f52a-193">Nom de la valeur: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="0f52a-193">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="0f52a-194">Type de valeur: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="0f52a-194">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="0f52a-195">Exemple de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-195">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="0f52a-196">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-196">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="0f52a-197">Install</span><span class="sxs-lookup"><span data-stu-id="0f52a-197">Install</span></span>
#### <span data-ttu-id="0f52a-198">Autoriser l’installation</span><span class="sxs-lookup"><span data-stu-id="0f52a-198">Allow installation</span></span>
><span data-ttu-id="0f52a-199">MicrosoftEdge Update1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f52a-199">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="0f52a-200">Description</span><span class="sxs-lookup"><span data-stu-id="0f52a-200">Description</span></span>
<span data-ttu-id="0f52a-201">Spécifie si un canal de MicrosoftEdge peut être installé à l’aide de MicrosoftEdge Update.</span><span class="sxs-lookup"><span data-stu-id="0f52a-201">Specifies whether a Microsoft Edge channel can be installed using Microsoft Edge Update.</span></span>

  <span data-ttu-id="0f52a-202">Si vous activez cette stratégie pour un canal, les utilisateurs peuvent installer ce canal de MicrosoftEdge via MicrosoftEdge Update.</span><span class="sxs-lookup"><span data-stu-id="0f52a-202">If you enable this policy for a channel, users can install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>

  <span data-ttu-id="0f52a-203">Si vous désactivez cette stratégie pour un canal, les utilisateurs ne peuvent pas installer ce canal de MicrosoftEdge via MicrosoftEdge Update.</span><span class="sxs-lookup"><span data-stu-id="0f52a-203">If you disable this policy for a channel, users cannot install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>

  <span data-ttu-id="0f52a-204">Si vous ne configurez pas cette stratégie pour un canal, la configuration de la stratégie «[Autoriser l’installation par défaut](#installdefault)» détermine si les utilisateurs peuvent installer ce canal de MicrosoftEdge via MicrosoftEdge Update.</span><span class="sxs-lookup"><span data-stu-id="0f52a-204">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>
#### <span data-ttu-id="0f52a-205">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-205">Windows information and settings</span></span>
##### <span data-ttu-id="0f52a-206">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0f52a-206">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="0f52a-207">Nom unique de la stratégie de groupe: Install</span><span class="sxs-lookup"><span data-stu-id="0f52a-207">GP unique name: Install</span></span>
- <span data-ttu-id="0f52a-208">Nom de la stratégie de groupe: Autoriser l’installation</span><span class="sxs-lookup"><span data-stu-id="0f52a-208">GP name: Allow installation</span></span>
- <span data-ttu-id="0f52a-209">Chemin de la stratégie de groupe:</span><span class="sxs-lookup"><span data-stu-id="0f52a-209">GP path:</span></span> 
  - <span data-ttu-id="0f52a-210">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0f52a-210">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="0f52a-211">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="0f52a-211">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="0f52a-212">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="0f52a-212">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="0f52a-213">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="0f52a-213">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="0f52a-214">Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="0f52a-214">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="0f52a-215">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-215">Windows Registry Settings</span></span>
- <span data-ttu-id="0f52a-216">Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="0f52a-216">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="0f52a-217">Nom de la valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-217">Value Name:</span></span> 
  - <span data-ttu-id="0f52a-218">(Stable): install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="0f52a-218">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="0f52a-219">(Beta): install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="0f52a-219">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="0f52a-220">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="0f52a-220">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="0f52a-221">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="0f52a-221">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="0f52a-222">Type de valeur: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="0f52a-222">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="0f52a-223">Exemple de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-223">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="0f52a-224">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-224">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="0f52a-225">Update</span><span class="sxs-lookup"><span data-stu-id="0f52a-225">Update</span></span>
#### <span data-ttu-id="0f52a-226">Remplacer la stratégie de mise à jour</span><span class="sxs-lookup"><span data-stu-id="0f52a-226">Update policy override</span></span>
><span data-ttu-id="0f52a-227">MicrosoftEdge Update1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f52a-227">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="0f52a-228">Description</span><span class="sxs-lookup"><span data-stu-id="0f52a-228">Description</span></span>
<span data-ttu-id="0f52a-229">Spécifie comment MicrosoftEdge Update gère les mises à jour disponibles à partir de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="0f52a-229">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

  <span data-ttu-id="0f52a-230">Si vous activez cette stratégie, MicrosoftEdge Update gère les mises à jour de MicrosoftEdge en fonction de la façon dont vous configurez les options suivantes:</span><span class="sxs-lookup"><span data-stu-id="0f52a-230">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="0f52a-231">Toujours autoriser les mises à jour: les mises à jour sont toujours appliquées lorsqu’elles sont trouvées, soit par une recherche de mise à jour périodique, soit par une recherche de mise à jour manuelle.</span><span class="sxs-lookup"><span data-stu-id="0f52a-231">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="0f52a-232">Mises à jour automatiques en mode silencieux uniquement: les mises à jour sont appliquées uniquement lorsqu’elles sont trouvées par la recherche de mise à jour périodique.</span><span class="sxs-lookup"><span data-stu-id="0f52a-232">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="0f52a-233">Mises à jour manuelles uniquement: les mises à jour sont appliquées uniquement lorsque l’utilisateur exécute une recherche de mise à jour manuelle.</span><span class="sxs-lookup"><span data-stu-id="0f52a-233">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="0f52a-234">(Toutes les applications n’offrent pas une interface pour cette option.)</span><span class="sxs-lookup"><span data-stu-id="0f52a-234">(Not all apps provide an interface for this option.)</span></span>
   - <span data-ttu-id="0f52a-235">Mises à jour désactivées: les mises à jour ne sont jamais appliquées.</span><span class="sxs-lookup"><span data-stu-id="0f52a-235">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="0f52a-236">Si vous sélectionnez les mises à jour manuelles, vérifiez régulièrement si des mises à jour sont disponibles à l’aide du mécanisme de mise à jour manuelle de l’application, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="0f52a-236">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="0f52a-237">Si vous désactivez les mises à jour, recherchez régulièrement les mises à jour et distribuez-les aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0f52a-237">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="0f52a-238">Si vous n’activez pas et ne configurez pas cette stratégie, MicrosoftEdge Update gère les mises à jour disponibles, comme spécifié par la stratégie «[Remplacer la stratégie de mise à jour par défaut](#updatedefault)».</span><span class="sxs-lookup"><span data-stu-id="0f52a-238">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>
#### <span data-ttu-id="0f52a-239">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-239">Windows information and settings</span></span>
##### <span data-ttu-id="0f52a-240">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0f52a-240">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="0f52a-241">Nom unique de la stratégie de groupe: Update</span><span class="sxs-lookup"><span data-stu-id="0f52a-241">GP unique name: Update</span></span>
- <span data-ttu-id="0f52a-242">Nom de la stratégie de groupe: Remplacer la stratégie de mise à jour</span><span class="sxs-lookup"><span data-stu-id="0f52a-242">GP name: Update policy override</span></span>
- <span data-ttu-id="0f52a-243">Chemin de la stratégie de groupe:</span><span class="sxs-lookup"><span data-stu-id="0f52a-243">GP path:</span></span> 
  - <span data-ttu-id="0f52a-244">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0f52a-244">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="0f52a-245">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="0f52a-245">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="0f52a-246">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="0f52a-246">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="0f52a-247">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="0f52a-247">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="0f52a-248">Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="0f52a-248">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="0f52a-249">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-249">Windows Registry Settings</span></span>
- <span data-ttu-id="0f52a-250">Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="0f52a-250">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="0f52a-251">Nom de la valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-251">Value Name:</span></span> 
  - <span data-ttu-id="0f52a-252">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="0f52a-252">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="0f52a-253">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="0f52a-253">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="0f52a-254">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="0f52a-254">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="0f52a-255">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="0f52a-255">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="0f52a-256">Type de valeur: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="0f52a-256">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="0f52a-257">Exemple de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-257">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="0f52a-258">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-258">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="0f52a-259">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="0f52a-259">Allowsxs</span></span>
#### <span data-ttu-id="0f52a-260">Autoriser l’expérience de navigateur côte à côte MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="0f52a-260">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="0f52a-261">MicrosoftEdge Update1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f52a-261">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="0f52a-262">Description</span><span class="sxs-lookup"><span data-stu-id="0f52a-262">Description</span></span>
<span data-ttu-id="0f52a-263">Cette stratégie permet à un utilisateur d’exécuter MicrosoftEdge (HTML Edge) et MicrosoftEdge (basé sur Chromium) côte à côte.</span><span class="sxs-lookup"><span data-stu-id="0f52a-263">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="0f52a-264">Si cette stratégie est définie sur «Non configuré», MicrosoftEdge (basée sur Chromium) remplace MicrosoftEdge (Edge HTML) après installation du canal stable MicrosoftEdge (basé sur Chromium) et des mises à jour de sécurité de novembre2019.</span><span class="sxs-lookup"><span data-stu-id="0f52a-264">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="0f52a-265">C’est le même comportement que le paramètre «Désactivé».</span><span class="sxs-lookup"><span data-stu-id="0f52a-265">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="0f52a-266">Le paramètre «Désactivé» bloque une expérience côte-à-côte et MicrosoftEdge (basée sur Chromium) remplace MicrosoftEdge (Edge HTML) après installation du canal stable MicrosoftEdge (basé sur Chromium) et des mises à jour de sécurité de novembre2019.</span><span class="sxs-lookup"><span data-stu-id="0f52a-266">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="0f52a-267">C’est le même comportement que le paramètre «Non configuré».</span><span class="sxs-lookup"><span data-stu-id="0f52a-267">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="0f52a-268">Lorsque cette stratégie est «Activée», MicrosoftEdge (basé sur Chromium) et MicrosoftEdge (Edge HTML) peuvent s’exécuter côte à côte après l’installation de MicrosoftEdge (basé sur Chromium).</span><span class="sxs-lookup"><span data-stu-id="0f52a-268">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="0f52a-269">Pour que cette stratégie de groupe prenne effet, elle doit être configurée avant l’installation automatique de MicrosoftEdge (basé sur Chromium) par Windows Update.</span><span class="sxs-lookup"><span data-stu-id="0f52a-269">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="0f52a-270">Remarque: un utilisateur peut bloquer la mise à jour automatique de MicrosoftEdge (basé sur Chromium) à l’aide du kit de ressources de bloqueur MicrosoftEdge (basé sur Chromium).</span><span class="sxs-lookup"><span data-stu-id="0f52a-270">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <span data-ttu-id="0f52a-271">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-271">Windows information and settings</span></span>
##### <span data-ttu-id="0f52a-272">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0f52a-272">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="0f52a-273">Nom unique de la stratégie de groupe: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="0f52a-273">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="0f52a-274">Nom de la stratégie de groupe: Autoriser l’expérience de navigateur côte à côte MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="0f52a-274">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="0f52a-275">Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="0f52a-275">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="0f52a-276">Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="0f52a-276">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="0f52a-277">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-277">Windows Registry Settings</span></span>
- <span data-ttu-id="0f52a-278">Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="0f52a-278">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="0f52a-279">Nom de la valeur: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="0f52a-279">Value Name: Allowsxs</span></span>
- <span data-ttu-id="0f52a-280">Type de valeur: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="0f52a-280">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="0f52a-281">Exemple de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-281">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="0f52a-282">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-282">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="0f52a-283">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="0f52a-283">CreateDesktopShortcutDefault</span></span>
#### <span data-ttu-id="0f52a-284">Empêcher la création du Raccourci Bureau lors de l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="0f52a-284">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="0f52a-285">MicrosoftEdge Update1.3.128.0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f52a-285">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="0f52a-286">Description</span><span class="sxs-lookup"><span data-stu-id="0f52a-286">Description</span></span>
<span data-ttu-id="0f52a-287">Vous permet de spécifier le comportement par défaut de tous les canaux pour créer un raccourci bureau lorsque Microsoft Edge est installé.</span><span class="sxs-lookup"><span data-stu-id="0f52a-287">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="0f52a-288">Si vous activez cette stratégie, un raccourci bureau est créé lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0f52a-288">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="0f52a-289">Si vous désactivez cette stratégie, aucun raccourci bureau n’est créé lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0f52a-289">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="0f52a-290">Si vous ne configurez pas cette stratégie, un raccourci bureau vers Microsoft Edge est créé pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="0f52a-290">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="0f52a-291">Si Microsoft Edge est déjà installé, cette stratégie n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="0f52a-291">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <span data-ttu-id="0f52a-292">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-292">Windows information and settings</span></span>
##### <span data-ttu-id="0f52a-293">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0f52a-293">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="0f52a-294">Nom unique de stratégie de groupe: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="0f52a-294">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="0f52a-295">Nom de stratégie de groupe: empêcher la création du Raccourci Bureau lors de l’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="0f52a-295">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="0f52a-296">Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="0f52a-296">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="0f52a-297">Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="0f52a-297">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="0f52a-298">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-298">Windows Registry Settings</span></span>
- <span data-ttu-id="0f52a-299">Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="0f52a-299">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="0f52a-300">Nom de valeur: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="0f52a-300">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="0f52a-301">Type de valeur: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="0f52a-301">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="0f52a-302">Exemple de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-302">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="0f52a-303">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-303">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="0f52a-304">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="0f52a-304">CreateDesktopShortcut</span></span>
#### <span data-ttu-id="0f52a-305">Empêcher la création du Raccourci Bureau lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="0f52a-305">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="0f52a-306">MicrosoftEdge Update1.3.128.0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f52a-306">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="0f52a-307">Description</span><span class="sxs-lookup"><span data-stu-id="0f52a-307">Description</span></span>
<span data-ttu-id="0f52a-308">Si vous activez cette stratégie, un raccourci bureau est créé lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0f52a-308">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="0f52a-309">Si vous désactivez cette stratégie, aucun raccourci bureau n’est créé lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0f52a-309">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="0f52a-310">Si vous ne configurez pas cette stratégie, un raccourci bureau vers Microsoft Edge est créé pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="0f52a-310">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="0f52a-311">Si Microsoft Edge est déjà installé, cette stratégie n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="0f52a-311">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="0f52a-312">Si vous ne configurez pas cette stratégie pour un canal, la configuration de stratégie «[Empêcher la création de raccourcis clavier lors de l’installation de la configuration de stratégie par défaut](#createdesktopshortcutdefault)» définit la création d’un raccourci lors de l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0f52a-312">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <span data-ttu-id="0f52a-313">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-313">Windows information and settings</span></span>
##### <span data-ttu-id="0f52a-314">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0f52a-314">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="0f52a-315">Nom unique de stratégie de groupe: CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="0f52a-315">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="0f52a-316">Nom de stratégie de groupe: empêcher la création du Raccourci Bureau lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="0f52a-316">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="0f52a-317">Chemin de la stratégie de groupe:</span><span class="sxs-lookup"><span data-stu-id="0f52a-317">GP path:</span></span> 
  - <span data-ttu-id="0f52a-318">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0f52a-318">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="0f52a-319">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="0f52a-319">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="0f52a-320">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="0f52a-320">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="0f52a-321">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="0f52a-321">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="0f52a-322">Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="0f52a-322">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="0f52a-323">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-323">Windows Registry Settings</span></span>
- <span data-ttu-id="0f52a-324">Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="0f52a-324">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="0f52a-325">Nom de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-325">Value Name:</span></span> 
  - <span data-ttu-id="0f52a-326">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="0f52a-326">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="0f52a-327">(Bêta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="0f52a-327">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="0f52a-328">(Canary): CreateDesktopShortcut {65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="0f52a-328">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="0f52a-329">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="0f52a-329">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="0f52a-330">Type de valeur: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="0f52a-330">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="0f52a-331">Exemple de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-331">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="0f52a-332">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-332">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="0f52a-333">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="0f52a-333">TargetVersionPrefix</span></span>
#### <span data-ttu-id="0f52a-334">Remplacement de la version cible</span><span class="sxs-lookup"><span data-stu-id="0f52a-334">Target version override</span></span>
><span data-ttu-id="0f52a-335">MicrosoftEdge Update1.3.119.43 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f52a-335">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <span data-ttu-id="0f52a-336">Description</span><span class="sxs-lookup"><span data-stu-id="0f52a-336">Description</span></span>
<span data-ttu-id="0f52a-337">Lorsque cette stratégie est activée et que la mise à jour automatique est activée, Microsoft Edge est mis à jour vers la version spécifiée par cette valeur de stratégie.</span><span class="sxs-lookup"><span data-stu-id="0f52a-337">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="0f52a-338">La valeur de la stratégie doit être une version spécifique de Microsoft Edge, par exemple, 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="0f52a-338">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="0f52a-339">Si la version de Microsoft Edge d’un appareil est plus récente que la valeur spécifiée, Microsoft Edge reste sur la version la plus récente et n’est pas rétrogradé vers la version spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0f52a-339">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="0f52a-340">Si la version spécifiée n’existe pas ou n’est pas mise en forme de manière correcte, Microsoft Edge reste sur sa version actuelle et ne sera pas mise à jour automatiquement vers les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0f52a-340">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>
#### <span data-ttu-id="0f52a-341">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-341">Windows information and settings</span></span>
##### <span data-ttu-id="0f52a-342">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0f52a-342">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="0f52a-343">Nom unique de stratégie de groupe: TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="0f52a-343">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="0f52a-344">Nom de stratégie de groupe: Remplacement de la version cible</span><span class="sxs-lookup"><span data-stu-id="0f52a-344">GP name: Target version override</span></span>
- <span data-ttu-id="0f52a-345">Chemin de la stratégie de groupe:</span><span class="sxs-lookup"><span data-stu-id="0f52a-345">GP path:</span></span> 
  - <span data-ttu-id="0f52a-346">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0f52a-346">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="0f52a-347">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="0f52a-347">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="0f52a-348">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="0f52a-348">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="0f52a-349">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="0f52a-349">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="0f52a-350">Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="0f52a-350">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="0f52a-351">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-351">Windows Registry Settings</span></span>
- <span data-ttu-id="0f52a-352">Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="0f52a-352">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="0f52a-353">Nom de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-353">Value Name:</span></span> 
  - <span data-ttu-id="0f52a-354">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="0f52a-354">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="0f52a-355">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="0f52a-355">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="0f52a-356">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="0f52a-356">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="0f52a-357">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="0f52a-357">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="0f52a-358">Type de valeur: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0f52a-358">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="0f52a-359">Exemple de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-359">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="0f52a-360">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-360">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="0f52a-361">Stratégies de préférences</span><span class="sxs-lookup"><span data-stu-id="0f52a-361">Preferences policies</span></span>

[<span data-ttu-id="0f52a-362">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-362">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="0f52a-363">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="0f52a-363">AutoUpdateCheckPeriodMinutes</span></span>
#### <span data-ttu-id="0f52a-364">Remplacement de la période de vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="0f52a-364">Auto-update check period override</span></span>
><span data-ttu-id="0f52a-365">MicrosoftEdge Update1.2.145.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f52a-365">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="0f52a-366">Description</span><span class="sxs-lookup"><span data-stu-id="0f52a-366">Description</span></span>
<span data-ttu-id="0f52a-367">Si elle est activée, cette stratégie vous permet de définir une valeur pour le nombre minimal de minutes entre les recherches automatiques de mises à jour.</span><span class="sxs-lookup"><span data-stu-id="0f52a-367">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="0f52a-368">Dans le cas contraire, par défaut, la mise à jour automatique recherche les mises à jour toutes les 10heures.</span><span class="sxs-lookup"><span data-stu-id="0f52a-368">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="0f52a-369">Si vous souhaitez désactiver toutes les vérifications de mise à jour automatique, définissez la valeur sur 0 (non recommandé).</span><span class="sxs-lookup"><span data-stu-id="0f52a-369">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <span data-ttu-id="0f52a-370">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-370">Windows information and settings</span></span>
##### <span data-ttu-id="0f52a-371">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0f52a-371">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="0f52a-372">Nom unique de la stratégie de groupe: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="0f52a-372">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="0f52a-373">Nom de la stratégie de groupe: Remplacement de la période de vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="0f52a-373">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="0f52a-374">Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Preferences</span><span class="sxs-lookup"><span data-stu-id="0f52a-374">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="0f52a-375">Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="0f52a-375">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="0f52a-376">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-376">Windows Registry Settings</span></span>
- <span data-ttu-id="0f52a-377">Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="0f52a-377">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="0f52a-378">Nom de la valeur: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="0f52a-378">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="0f52a-379">Type de valeur: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="0f52a-379">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="0f52a-380">Exemple de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-380">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="0f52a-381">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-381">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="0f52a-382">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="0f52a-382">UpdatesSuppressed</span></span>
#### <span data-ttu-id="0f52a-383">Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="0f52a-383">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="0f52a-384">MicrosoftEdge Update1.3.33.5 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f52a-384">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <span data-ttu-id="0f52a-385">Description</span><span class="sxs-lookup"><span data-stu-id="0f52a-385">Description</span></span>
<span data-ttu-id="0f52a-386">Si vous activez cette stratégie, les vérifications de mise à jour sont supprimées chaque jour à partir de Heure:Minute pendant une Durée (en minutes).</span><span class="sxs-lookup"><span data-stu-id="0f52a-386">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="0f52a-387">La durée n’est pas affectée par l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="0f52a-387">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="0f52a-388">Par exemple, si l’heure de début est 22:00 et que la durée est 480minutes, les mises à jour seront supprimées pendant exactement 8heures, même si l’heure d’été commence ou se termine pendant cette période.</span><span class="sxs-lookup"><span data-stu-id="0f52a-388">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="0f52a-389">Si vous désactivez ou que vous ne configurez pas cette stratégie, les vérifications de mise à jour ne sont pas supprimées pendant une période spécifique.</span><span class="sxs-lookup"><span data-stu-id="0f52a-389">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <span data-ttu-id="0f52a-390">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-390">Windows information and settings</span></span>
##### <span data-ttu-id="0f52a-391">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0f52a-391">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="0f52a-392">Nom unique de la stratégie de groupe: UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="0f52a-392">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="0f52a-393">Nom de la stratégie de groupe: Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="0f52a-393">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="0f52a-394">Options { Hour, Minute, Duration }</span><span class="sxs-lookup"><span data-stu-id="0f52a-394">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="0f52a-395">Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Preferences</span><span class="sxs-lookup"><span data-stu-id="0f52a-395">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="0f52a-396">Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="0f52a-396">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="0f52a-397">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-397">Windows Registry Settings</span></span>
- <span data-ttu-id="0f52a-398">Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="0f52a-398">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="0f52a-399">Nom de la valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-399">Value Name:</span></span> 
  - <span data-ttu-id="0f52a-400">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="0f52a-400">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="0f52a-401">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="0f52a-401">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="0f52a-402">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="0f52a-402">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="0f52a-403">Type de valeur: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="0f52a-403">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="0f52a-404">Exemple de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-404">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="0f52a-405">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-405">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="0f52a-406">Stratégies de serveur proxy</span><span class="sxs-lookup"><span data-stu-id="0f52a-406">Proxy Server policies</span></span>
  
  

[<span data-ttu-id="0f52a-407">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-407">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="0f52a-408">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="0f52a-408">ProxyMode</span></span>
#### <span data-ttu-id="0f52a-409">Choisir comment spécifier les paramètres du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="0f52a-409">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="0f52a-410">MicrosoftEdge Update1.3.21.81 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f52a-410">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="0f52a-411">Description</span><span class="sxs-lookup"><span data-stu-id="0f52a-411">Description</span></span>
<span data-ttu-id="0f52a-412">Permet de spécifier les paramètres de serveur proxy qui sont utilisés par MicrosoftEdge Update.</span><span class="sxs-lookup"><span data-stu-id="0f52a-412">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="0f52a-413">Si vous activez cette stratégie, vous pouvez choisir l’une des options de serveur proxy suivantes:</span><span class="sxs-lookup"><span data-stu-id="0f52a-413">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="0f52a-414">Si vous choisissez de ne jamais utiliser un serveur proxy et de toujours vous connecter directement, toutes les autres options sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="0f52a-414">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="0f52a-415">Si vous choisissez d’utiliser les paramètres de proxy système ou de détection automatique du serveur proxy, toutes les autres options sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="0f52a-415">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="0f52a-416">Si vous choisissez le mode de serveur proxy fixe, vous pouvez spécifier d’autres options dans la stratégie [«Adresse ou URL du serveur proxy»](#proxyserver).</span><span class="sxs-lookup"><span data-stu-id="0f52a-416">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="0f52a-417">Si vous choisissez d’utiliser un script de proxy .pac, vous devez spécifier l’URL du script dans la stratégie [«URL d’un fichier proxy. pac»](#proxypacurl).</span><span class="sxs-lookup"><span data-stu-id="0f52a-417">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="0f52a-418">Si vous activez cette stratégie, les utilisateurs de votre organisation ne peuvent pas modifier les paramètres du proxy dans MicrosoftEdge Update.</span><span class="sxs-lookup"><span data-stu-id="0f52a-418">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="0f52a-419">Si vous désactivez ou que vous ne configurez pas cette stratégie, aucun paramètre de serveur proxy n’est configuré, mais les utilisateurs de votre organisation peuvent choisir leurs propres paramètres de proxy pour MicrosoftEdge Update.</span><span class="sxs-lookup"><span data-stu-id="0f52a-419">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <span data-ttu-id="0f52a-420">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-420">Windows information and settings</span></span>
##### <span data-ttu-id="0f52a-421">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0f52a-421">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="0f52a-422">Nom unique de la stratégie de groupe: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="0f52a-422">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="0f52a-423">Nom de la stratégie de groupe: Choisir comment spécifier les paramètres du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="0f52a-423">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="0f52a-424">Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="0f52a-424">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="0f52a-425">Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="0f52a-425">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="0f52a-426">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-426">Windows Registry Settings</span></span>
- <span data-ttu-id="0f52a-427">Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="0f52a-427">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="0f52a-428">Nom de la valeur: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="0f52a-428">Value Name: ProxyMode</span></span>
- <span data-ttu-id="0f52a-429">Type de valeur: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0f52a-429">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="0f52a-430">Exemple de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-430">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="0f52a-431">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-431">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="0f52a-432">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="0f52a-432">ProxyPacUrl</span></span>
#### <span data-ttu-id="0f52a-433">URL d’un fichier proxy. pac</span><span class="sxs-lookup"><span data-stu-id="0f52a-433">URL to a proxy .pac file</span></span>
><span data-ttu-id="0f52a-434">MicrosoftEdge Update1.3.21.81 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f52a-434">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="0f52a-435">Description</span><span class="sxs-lookup"><span data-stu-id="0f52a-435">Description</span></span>
<span data-ttu-id="0f52a-436">Permet de spécifier une URL pour un fichier de configuration automatique de proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="0f52a-436">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="0f52a-437">Si vous activez cette stratégie, vous pouvez spécifier une URL pour un fichier PAC pour automatiser la façon dont MicrosoftEdge Update sélectionne le serveur proxy approprié pour l’extraction d’un site web particulier.</span><span class="sxs-lookup"><span data-stu-id="0f52a-437">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="0f52a-438">Cette stratégie est appliquée uniquement si vous avez spécifié des paramètres de proxy manuels dans la stratégie «[Choisir comment spécifier les paramètres du serveur proxy](#proxymode)».</span><span class="sxs-lookup"><span data-stu-id="0f52a-438">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="0f52a-439">Ne configurez pas cette stratégie si vous avez sélectionné un paramètre de proxy autre que manuel dans la stratégie «[Choisir comment spécifier les paramètres du serveur proxy](#proxymode)».</span><span class="sxs-lookup"><span data-stu-id="0f52a-439">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="0f52a-440">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-440">Windows information and settings</span></span>
##### <span data-ttu-id="0f52a-441">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0f52a-441">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="0f52a-442">Nom unique de la stratégie de groupe: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="0f52a-442">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="0f52a-443">Nom de la stratégie de groupe: URL d’un fichier proxy. pac</span><span class="sxs-lookup"><span data-stu-id="0f52a-443">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="0f52a-444">Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="0f52a-444">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="0f52a-445">Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="0f52a-445">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="0f52a-446">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-446">Windows Registry Settings</span></span>
- <span data-ttu-id="0f52a-447">Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="0f52a-447">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="0f52a-448">Nom de la valeur: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="0f52a-448">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="0f52a-449">Type de valeur: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0f52a-449">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="0f52a-450">Exemple de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-450">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="0f52a-451">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-451">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="0f52a-452">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="0f52a-452">ProxyServer</span></span>
#### <span data-ttu-id="0f52a-453">Adresse ou URL du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="0f52a-453">Address or URL of proxy server</span></span>
><span data-ttu-id="0f52a-454">MicrosoftEdge Update1.3.21.81 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f52a-454">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="0f52a-455">Description</span><span class="sxs-lookup"><span data-stu-id="0f52a-455">Description</span></span>
<span data-ttu-id="0f52a-456">Permet de spécifier l’URL du serveur proxy que MicrosoftEdge Update doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="0f52a-456">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="0f52a-457">Si vous activez cette stratégie, vous pouvez définir l’URL de serveur proxy utilisée par MicrosoftEdge Update dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0f52a-457">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="0f52a-458">Cette stratégie est appliquée uniquement si vous avez sélectionné plusieurs paramètres de proxy manuels dans la stratégie «[Choisir comment spécifier les paramètres du serveur proxy](#proxymode)».</span><span class="sxs-lookup"><span data-stu-id="0f52a-458">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="0f52a-459">Ne configurez pas cette stratégie si vous avez sélectionné un paramètre de proxy autre que manuel dans la stratégie «[Choisir comment spécifier les paramètres du serveur proxy](#proxymode)».</span><span class="sxs-lookup"><span data-stu-id="0f52a-459">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="0f52a-460">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-460">Windows information and settings</span></span>
##### <span data-ttu-id="0f52a-461">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0f52a-461">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="0f52a-462">Nom unique de la stratégie de groupe: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="0f52a-462">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="0f52a-463">Nom de la stratégie de groupe: Adresse ou URL du serveur proxy</span><span class="sxs-lookup"><span data-stu-id="0f52a-463">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="0f52a-464">Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="0f52a-464">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="0f52a-465">Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="0f52a-465">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="0f52a-466">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="0f52a-466">Windows Registry Settings</span></span>
- <span data-ttu-id="0f52a-467">Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="0f52a-467">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="0f52a-468">Nom de la valeur: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="0f52a-468">Value Name: ProxyServer</span></span>
- <span data-ttu-id="0f52a-469">Type de valeur: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0f52a-469">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="0f52a-470">Exemple de valeur:</span><span class="sxs-lookup"><span data-stu-id="0f52a-470">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="0f52a-471">Retour au début</span><span class="sxs-lookup"><span data-stu-id="0f52a-471">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="0f52a-472">Voir également</span><span class="sxs-lookup"><span data-stu-id="0f52a-472">See also</span></span>
  - [<span data-ttu-id="0f52a-473">Configuration de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="0f52a-473">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="0f52a-474">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="0f52a-474">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
