---
title: Documentation relative aux stratégies WebView2 Microsoft Edge
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 10/27/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentation relative à toutes les stratégies prises en charge par le navigateur Microsoft Edge pour Windows et Mac
ms.openlocfilehash: 3ca9adb18ef41581bb016451015cf0aca0aa63c9
ms.sourcegitcommit: 91abbcdd4918065d4ec1151587fc1fa92486dbf3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "11136213"
---
# <span data-ttu-id="c8826-103">Microsoft Edge WebView2 - Politiques</span><span class="sxs-lookup"><span data-stu-id="c8826-103">Microsoft Edge WebView2 - Policies</span></span>

<span data-ttu-id="c8826-104">La dernière version de Microsoft Edge WebView2 comprend les politiques suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8826-104">The latest version of Microsoft Edge WebView2 includes the following policies.</span></span> <span data-ttu-id="c8826-105">Vous pouvez utiliser ces politiques pour configurer le fonctionnement de Microsoft Edge WebView2 dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c8826-105">You can use these policies to configure how Microsoft Edge WebView2 runs in your organization.</span></span>

<span data-ttu-id="c8826-106">Pour plus d'informations sur un ensemble supplémentaire de politiques utilisées pour contrôler quand et comment Microsoft Edge WebView2 est mis à jour, consultez la [référence des politiques de mise à jour de Microsoft Edge](microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c8826-106">For information about an additional set of policies used to control how and when Microsoft Edge WebView2 is updated, check out [Microsoft Edge update policy reference](microsoft-edge-update-policies.md).</span></span>


> [!NOTE]
> <span data-ttu-id="c8826-107">Cet article concerne Microsoft Edge version 87 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c8826-107">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="c8826-108">Stratégies disponibles</span><span class="sxs-lookup"><span data-stu-id="c8826-108">Available policies</span></span>

<span data-ttu-id="c8826-109">Ces tableaux répertorient toutes les politiques de groupe disponibles dans cette version de Microsoft Edge WebView2.</span><span class="sxs-lookup"><span data-stu-id="c8826-109">These tables list all of the group policies available in this release of Microsoft Edge WebView2.</span></span> <span data-ttu-id="c8826-110">Utilisez les liens dans le tableau pour obtenir plus de détails sur des stratégies données.</span><span class="sxs-lookup"><span data-stu-id="c8826-110">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="c8826-111">Paramètres d'annulation du chargeur</span><span class="sxs-lookup"><span data-stu-id="c8826-111">Loader Override Settings</span></span>](#loader-override-settings)|

### [*<span data-ttu-id="c8826-112">Paramètres d'annulation du chargeur</span><span class="sxs-lookup"><span data-stu-id="c8826-112">Loader Override Settings</span></span>*](#loader-override-settings-policies)

|<span data-ttu-id="c8826-113">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="c8826-113">Policy Name</span></span>|<span data-ttu-id="c8826-114">Caption</span><span class="sxs-lookup"><span data-stu-id="c8826-114">Caption</span></span>|
|-|-|
|[<span data-ttu-id="c8826-115">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="c8826-115">BrowserExecutableFolder</span></span>](#browserexecutablefolder)|<span data-ttu-id="c8826-116">Configurer l'emplacement du dossier de l'exécutable du navigateur</span><span class="sxs-lookup"><span data-stu-id="c8826-116">Configure the location of the browser executable folder</span></span>|
|[<span data-ttu-id="c8826-117">ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="c8826-117">ReleaseChannelPreference</span></span>](#releasechannelpreference)|<span data-ttu-id="c8826-118">Définir la préférence de l'ordre de recherche du canal de diffusion</span><span class="sxs-lookup"><span data-stu-id="c8826-118">Set the release channel search order preference</span></span>|




  ## <span data-ttu-id="c8826-119">Politiques d'annulation des paramètres du chargeur</span><span class="sxs-lookup"><span data-stu-id="c8826-119">Loader Override Settings policies</span></span>

  [<span data-ttu-id="c8826-120">Retour au début</span><span class="sxs-lookup"><span data-stu-id="c8826-120">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="c8826-121">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="c8826-121">BrowserExecutableFolder</span></span>

  #### <span data-ttu-id="c8826-122">Configurer l'emplacement du dossier de l'exécutable du navigateur</span><span class="sxs-lookup"><span data-stu-id="c8826-122">Configure the location of the browser executable folder</span></span>

  
  
  #### <span data-ttu-id="c8826-123">Versions prises en charge :</span><span class="sxs-lookup"><span data-stu-id="c8826-123">Supported versions:</span></span>

  - <span data-ttu-id="c8826-124">Sur Windows depuis la version 87 ou versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="c8826-124">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="c8826-125">Description</span><span class="sxs-lookup"><span data-stu-id="c8826-125">Description</span></span>

  <span data-ttu-id="c8826-126">Cette politique configure les applications WebView2 pour qu'elles utilisent le runtime WebView2 dans le chemin spécifié.</span><span class="sxs-lookup"><span data-stu-id="c8826-126">This policy configures WebView2 applications to use the WebView2 Runtime in the specified path.</span></span> <span data-ttu-id="c8826-127">Le dossier doit contenir les fichiers suivants : msedgewebview2.exe, msedge.dll, etc.</span><span class="sxs-lookup"><span data-stu-id="c8826-127">The folder should contain the following files: msedgewebview2.exe, msedge.dll, and so on.</span></span>

<span data-ttu-id="c8826-128">Pour définir la valeur du chemin d'accès au dossier, fournissez un nom de valeur et une paire de valeurs.</span><span class="sxs-lookup"><span data-stu-id="c8826-128">To set the value for the folder path, provide a Value name and Value pair.</span></span> <span data-ttu-id="c8826-129">Définissez le nom de la valeur à l'ID du modèle d'utilisateur de l'application ou au nom du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="c8826-129">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="c8826-130">Vous pouvez utiliser le « \* » joker comme nom de valeur à appliquer à toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="c8826-130">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="c8826-131">Fonctionnalités prises en charge :</span><span class="sxs-lookup"><span data-stu-id="c8826-131">Supported features:</span></span>

  - <span data-ttu-id="c8826-132">Peut être obligatoire : Oui</span><span class="sxs-lookup"><span data-stu-id="c8826-132">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="c8826-133">Peut être recommandée : Non</span><span class="sxs-lookup"><span data-stu-id="c8826-133">Can be recommended: No</span></span>
  - <span data-ttu-id="c8826-134">Actualisation dynamique de la stratégie : Oui</span><span class="sxs-lookup"><span data-stu-id="c8826-134">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="c8826-135">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c8826-135">Data Type:</span></span>

  - <span data-ttu-id="c8826-136">Liste composée de chaînes</span><span class="sxs-lookup"><span data-stu-id="c8826-136">List of strings</span></span>

  #### <span data-ttu-id="c8826-137">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="c8826-137">Windows information and settings</span></span>

  ##### <span data-ttu-id="c8826-138">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c8826-138">Group Policy (ADMX) info</span></span>

  - <span data-ttu-id="c8826-139">Nom unique de GP : BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="c8826-139">GP unique name: BrowserExecutableFolder</span></span>
  - <span data-ttu-id="c8826-140">Nom du GP : Configurer l'emplacement du dossier de l'exécutable du navigateur</span><span class="sxs-lookup"><span data-stu-id="c8826-140">GP name: Configure the location of the browser executable folder</span></span>
  - <span data-ttu-id="c8826-141">Parcours GP (Obligatoire) : Modèles d'administration/Microsoft Edge WebView2/Loader Paramètres de remplacement</span><span class="sxs-lookup"><span data-stu-id="c8826-141">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="c8826-142">Chemin d’accès de la stratégie de groupe (recommandé) : N/A</span><span class="sxs-lookup"><span data-stu-id="c8826-142">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="c8826-143">Nom du fichier GP ADMX : MSEdgeWebView2.admx</span><span class="sxs-lookup"><span data-stu-id="c8826-143">GP ADMX file name: MSEdgeWebView2.admx</span></span>

  ##### <span data-ttu-id="c8826-144">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="c8826-144">Windows Registry Settings</span></span>

  - <span data-ttu-id="c8826-145">Chemin (Obligatoire) : SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="c8826-145">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder</span></span>
  - <span data-ttu-id="c8826-146">Chemin d’accès (recommandé) : N/A</span><span class="sxs-lookup"><span data-stu-id="c8826-146">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="c8826-147">Nom de la valeur : liste des REG_SZ</span><span class="sxs-lookup"><span data-stu-id="c8826-147">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="c8826-148">Type de valeur : liste composée de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="c8826-148">Value Type: list of REG_SZ</span></span>

  ##### <span data-ttu-id="c8826-149">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="c8826-149">Example value:</span></span>

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [<span data-ttu-id="c8826-150">Retour au début</span><span class="sxs-lookup"><span data-stu-id="c8826-150">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="c8826-151">ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="c8826-151">ReleaseChannelPreference</span></span>

  #### <span data-ttu-id="c8826-152">Définir la préférence de l'ordre de recherche du canal de diffusion</span><span class="sxs-lookup"><span data-stu-id="c8826-152">Set the release channel search order preference</span></span>

  
  
  #### <span data-ttu-id="c8826-153">Versions prises en charge :</span><span class="sxs-lookup"><span data-stu-id="c8826-153">Supported versions:</span></span>

  - <span data-ttu-id="c8826-154">Sur Windows depuis la version 87 ou versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="c8826-154">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="c8826-155">Description</span><span class="sxs-lookup"><span data-stu-id="c8826-155">Description</span></span>

  <span data-ttu-id="c8826-156">L'ordre de recherche des chaînes par défaut est le suivant : WebView2 Runtime, Beta, Dev et Canary.</span><span class="sxs-lookup"><span data-stu-id="c8826-156">The default channel search order is WebView2 Runtime, Beta, Dev, and Canary.</span></span>

<span data-ttu-id="c8826-157">Pour inverser l'ordre de recherche par défaut, réglez cette politique sur 1.</span><span class="sxs-lookup"><span data-stu-id="c8826-157">To reverse the default search order, set this policy to 1.</span></span>

<span data-ttu-id="c8826-158">Pour définir la valeur de la préférence de canal de diffusion, fournissez un nom de valeur et une paire de valeurs.</span><span class="sxs-lookup"><span data-stu-id="c8826-158">To set the value for the release channel preference, provide a Value name and Value pair.</span></span> <span data-ttu-id="c8826-159">Définissez le nom de la valeur à l'ID du modèle d'utilisateur de l'application ou au nom du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="c8826-159">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="c8826-160">Vous pouvez utiliser le « \* » joker comme nom de valeur à appliquer à toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="c8826-160">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="c8826-161">Fonctionnalités prises en charge :</span><span class="sxs-lookup"><span data-stu-id="c8826-161">Supported features:</span></span>

  - <span data-ttu-id="c8826-162">Peut être obligatoire : Oui</span><span class="sxs-lookup"><span data-stu-id="c8826-162">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="c8826-163">Peut être recommandée : Non</span><span class="sxs-lookup"><span data-stu-id="c8826-163">Can be recommended: No</span></span>
  - <span data-ttu-id="c8826-164">Actualisation dynamique de la stratégie : Oui</span><span class="sxs-lookup"><span data-stu-id="c8826-164">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="c8826-165">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c8826-165">Data Type:</span></span>

  - <span data-ttu-id="c8826-166">Liste composée de chaînes</span><span class="sxs-lookup"><span data-stu-id="c8826-166">List of strings</span></span>

  #### <span data-ttu-id="c8826-167">Informations et paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="c8826-167">Windows information and settings</span></span>

  ##### <span data-ttu-id="c8826-168">Informations relatives à la stratégie de groupe (ADMX)</span><span class="sxs-lookup"><span data-stu-id="c8826-168">Group Policy (ADMX) info</span></span>

  - <span data-ttu-id="c8826-169">Nom unique de GP : ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="c8826-169">GP unique name: ReleaseChannelPreference</span></span>
  - <span data-ttu-id="c8826-170">Nom du GP : Définir la préférence de l'ordre de recherche du canal de diffusion</span><span class="sxs-lookup"><span data-stu-id="c8826-170">GP name: Set the release channel search order preference</span></span>
  - <span data-ttu-id="c8826-171">Parcours GP (Obligatoire) : Modèles d'administration/Microsoft Edge WebView2/Loader Paramètres de remplacement</span><span class="sxs-lookup"><span data-stu-id="c8826-171">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="c8826-172">Chemin d’accès de la stratégie de groupe (recommandé) : N/A</span><span class="sxs-lookup"><span data-stu-id="c8826-172">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="c8826-173">Nom du fichier GP ADMX : MSEdgeWebView2.admx</span><span class="sxs-lookup"><span data-stu-id="c8826-173">GP ADMX file name: MSEdgeWebView2.admx</span></span>

  ##### <span data-ttu-id="c8826-174">Paramètres du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="c8826-174">Windows Registry Settings</span></span>

  - <span data-ttu-id="c8826-175">Chemin (Obligatoire) : SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="c8826-175">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference</span></span>
  - <span data-ttu-id="c8826-176">Chemin d’accès (recommandé) : N/A</span><span class="sxs-lookup"><span data-stu-id="c8826-176">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="c8826-177">Nom de la valeur : liste des REG_SZ</span><span class="sxs-lookup"><span data-stu-id="c8826-177">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="c8826-178">Type de valeur : liste composée de REG_SZ</span><span class="sxs-lookup"><span data-stu-id="c8826-178">Value Type: list of REG_SZ</span></span>

  ##### <span data-ttu-id="c8826-179">Exemple de valeur :</span><span class="sxs-lookup"><span data-stu-id="c8826-179">Example value:</span></span>

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [<span data-ttu-id="c8826-180">Retour au début</span><span class="sxs-lookup"><span data-stu-id="c8826-180">Back to top</span></span>](#microsoft-edge-webview2---policies)


## <span data-ttu-id="c8826-181">Voir également</span><span class="sxs-lookup"><span data-stu-id="c8826-181">See also</span></span>

- [<span data-ttu-id="c8826-182">Configuration de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c8826-182">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="c8826-183">Page d’accueil Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="c8826-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="c8826-184">Blog sur les bases de la sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="c8826-184">Microsoft Security Baselines Blog</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)