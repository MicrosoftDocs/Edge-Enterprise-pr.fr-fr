---
title: Utiliser des stratégies de groupe pour gérer les extensions MicrosoftEdge
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Utiliser des stratégies de groupe pour gérer les extensions MicrosoftEdge dans l’entreprise
ms.openlocfilehash: a633b036c1733716dfb257b4711bca57bd6721f0
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618102"
---
# <a name="use-group-policies-to-manage-microsoft-edge-extensions"></a><span data-ttu-id="67fa6-103">Utiliser des stratégies de groupe pour gérer les extensions MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="67fa6-103">Use group policies to manage Microsoft Edge extensions</span></span>

<span data-ttu-id="67fa6-104">Cet article décrit les options et les étapes de gestion des extensions à l’aide de stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="67fa6-104">This article describes the options and steps for managing extensions by using group policies.</span></span> <span data-ttu-id="67fa6-105">Ces options supposent que vous avez déjà MicrosoftEdge géré pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="67fa6-105">These options  assume that you already have Microsoft Edge managed for your users.</span></span> <span data-ttu-id="67fa6-106">Si vous n’avez pas encore configuré la gestion de MicrosoftEdge par vos utilisateurs, suivez le lien ci-dessous pour le faire maintenant.</span><span class="sxs-lookup"><span data-stu-id="67fa6-106">If you have not already set up Microsoft Edge to be managed for your users please follow the below link to do so now.</span></span>

- [<span data-ttu-id="67fa6-107">Gérer les extensions MicrosoftEdge dans l’entreprise</span><span class="sxs-lookup"><span data-stu-id="67fa6-107">Manage Microsoft Edge extensions in the enterprise</span></span>](/deployedge/microsoft-edge-manage-extensions)

> [!NOTE]
> <span data-ttu-id="67fa6-108">Cet article concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="67fa6-108">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="block-extensions-based-on-their-permissions"></a><span data-ttu-id="67fa6-109">Bloquer les extensions en fonction de leurs autorisations</span><span class="sxs-lookup"><span data-stu-id="67fa6-109">Block extensions based on their permissions</span></span>

<span data-ttu-id="67fa6-110">Vous pouvez contrôler les extensions que vos utilisateurs peuvent installer en fonction des autorisations à l’aide de la [stratégie ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings).</span><span class="sxs-lookup"><span data-stu-id="67fa6-110">You can control what extensions your users can install based on permissions using the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy.</span></span> <span data-ttu-id="67fa6-111">Si une extension installée a besoin d’une autorisation bloquée, elle ne s’exécute pas.</span><span class="sxs-lookup"><span data-stu-id="67fa6-111">If an installed extension needs a permission that’s blocked, it just won't run.</span></span> <span data-ttu-id="67fa6-112">L’extension n’est pas supprimée, mais simplement désactivée.</span><span class="sxs-lookup"><span data-stu-id="67fa6-112">The extension isn't removed, just disabled.</span></span>

> [!NOTE]
> <span data-ttu-id="67fa6-113">Le paramètre d’autorisations bloquées peut uniquement être définie dans la stratégie de paramètres d’extension.</span><span class="sxs-lookup"><span data-stu-id="67fa6-113">The blocked permissions setting can only be set within the extension settings policy.</span></span>  

<span data-ttu-id="67fa6-114">Utilisez les étapes suivantes comme guide pour bloquer une extension.</span><span class="sxs-lookup"><span data-stu-id="67fa6-114">Use the following steps as a guide for blocking an extension.</span></span>

1. <span data-ttu-id="67fa6-115">Ouvrez l’éditeur de gestion des stratégies de groupe et sélectionnez **Modèles d’administration > Microsoft Edge > Extensions**, puis sélectionnez **Configurer les paramètres de gestion des extensions**.</span><span class="sxs-lookup"><span data-stu-id="67fa6-115">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions**  and then select **Configure extension management settings**.</span></span>
2. <span data-ttu-id="67fa6-116">Activez la stratégie, puis entrez les autorisations que vous souhaitez autoriser ou bloquer, à l’aide d’une chaîne JSON qui est compressée.</span><span class="sxs-lookup"><span data-stu-id="67fa6-116">Enable the policy, then enter the permissions that you want allowed or blocked, by using a JSON string that gets compressed.</span></span> <span data-ttu-id="67fa6-117">La capture d’écran suivante montre comment bloquer une extension qui utilise l’autorisation «usb».</span><span class="sxs-lookup"><span data-stu-id="67fa6-117">The next screenshot shows how to block an extension that uses the permission "usb".</span></span>

    :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-1.png" alt-text="Configurez la stratégie de groupe pour bloquer une extension.":::

<span data-ttu-id="67fa6-119">L’exemple suivant montre le JSON pour bloquer toute extension qui nécessite l’utilisation de l’autorisation «usb» et de sa chaîne compressée.</span><span class="sxs-lookup"><span data-stu-id="67fa6-119">The following example shows the JSON to block any extension that needs the use of permission "usb" and its compressed string.</span></span>

### <a name="json-example"></a><span data-ttu-id="67fa6-120">Exemple JSON</span><span class="sxs-lookup"><span data-stu-id="67fa6-120">JSON example</span></span>

   ```json
   { 
        "*": { 
             "blocked_permissions": ["usb"] 
        } 
   } 
   ```

   ```json
   {"*":{"blocked_permissions":["usb"]}} 
   ```

   > [!NOTE]
   > <span data-ttu-id="67fa6-121">Pour bloquer toutes les extensions qui utilisent l’autorisation, utilisez un astérisque pour l’ID d’extension, comme illustré dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="67fa6-121">To block all extensions that use the permission, use an asterisk for the extension ID, as shown in the previous example.</span></span> <span data-ttu-id="67fa6-122">Si vous spécifiez un ID d’extension, la stratégie s’applique uniquement à cette extension.</span><span class="sxs-lookup"><span data-stu-id="67fa6-122">If you specify one extension ID, the policy will only apply to that extension.</span></span> <span data-ttu-id="67fa6-123">Vous pouvez en bloquer plusieurs, mais il doit s’y trouver des entrées distinctes.</span><span class="sxs-lookup"><span data-stu-id="67fa6-123">You can block more than one, but they need to be separate entries.</span></span>

## <a name="prevent-extensions-from-altering-web-pages"></a><span data-ttu-id="67fa6-124">Empêcher les extensions de modifier les pages web</span><span class="sxs-lookup"><span data-stu-id="67fa6-124">Prevent extensions from altering web pages</span></span>

<span data-ttu-id="67fa6-125">Ce paramètre empêche les extensions de lire et de modifier des données provenant de sites web et de domaines sensibles.</span><span class="sxs-lookup"><span data-stu-id="67fa6-125">This setting prevents extensions from reading and changing  data from sensitive websites and domains.</span></span> <span data-ttu-id="67fa6-126">Le blocage des actions indésirables s’effectuera en bloquant des actions telles que l’injection de scripts dans vos sites web, la lecture des cookies ou les modifications de demande web.</span><span class="sxs-lookup"><span data-stu-id="67fa6-126">Blocking unwanted actions is done by blocking actions such as script injection into your websites, reading the cookies, or making web-request modifications.</span></span> <span data-ttu-id="67fa6-127">Ce paramètre n’empêche pas vos utilisateurs d’installer ou de supprimer des extensions, il empêche uniquement les extensions de modifier les sites web spécifiés.</span><span class="sxs-lookup"><span data-stu-id="67fa6-127">This setting doesn’t prevent your users from installing or removing extensions, it only prevents extensions from altering the specified websites.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="67fa6-128">Le paramètre Hôtes autorisés/bloqués runtime peut uniquement être défini dans la stratégie de paramètres d’extension.</span><span class="sxs-lookup"><span data-stu-id="67fa6-128">The Runtime allowed/blocked hosts setting can only be set within the extension settings policy.</span></span>  

<span data-ttu-id="67fa6-129">Vous pouvez configurer les paramètres suivants dans la stratégie ExtensionSettings pour empêcher (ou autoriser) les modifications de sites web ou de domaines:</span><span class="sxs-lookup"><span data-stu-id="67fa6-129">You can configure the following settings in the ExtensionSettings policy to prevent (or allow) alterations of websites or domains:</span></span>

- <span data-ttu-id="67fa6-130">**Runtime_blocked_hosts**.</span><span class="sxs-lookup"><span data-stu-id="67fa6-130">**Runtime_blocked_hosts**.</span></span> <span data-ttu-id="67fa6-131">Ce paramètre empêche les extensions d’apporter des modifications ou de lire des données à partir des sites web que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="67fa6-131">This setting blocks extensions from making changes or reading data from the websites you specify.</span></span>
- <span data-ttu-id="67fa6-132">**Runtime_allowed_hosts**.</span><span class="sxs-lookup"><span data-stu-id="67fa6-132">**Runtime_allowed_hosts**.</span></span> <span data-ttu-id="67fa6-133">Ce paramètre permet aux extensions d’apporter des modifications ou de lire des données à partir des sites web que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="67fa6-133">This setting allows extensions to make changes or read data from the websites you specify.</span></span> <span data-ttu-id="67fa6-134">Le format suivant est utilisé pour spécifier vos sites dans la chaîne JSON de la stratégie:</span><span class="sxs-lookup"><span data-stu-id="67fa6-134">The following format is used for specifying your site(s) in the JSON string in the policy:</span></span>

  ```json
  [http|https|ftp|*]://[subdomain|*].[hostname|*].[eTLD|*] [http|https|ftp|*],
  ```

  > [!NOTE]
  > `[hostname|*], and [eTLD|*]` <span data-ttu-id="67fa6-135">les sections sont obligatoires, mais la section `[subdomain|*]` est facultative.</span><span class="sxs-lookup"><span data-stu-id="67fa6-135">sections are required, but `[subdomain|*]` section is optional.</span></span>

<span data-ttu-id="67fa6-136">Le tableau suivant présente des exemples de modèles d’hôte valides et de modèles correspondants.</span><span class="sxs-lookup"><span data-stu-id="67fa6-136">The following table shows examples of valid host patterns and matching patterns.</span></span>

|<span data-ttu-id="67fa6-137">Modèles d’hôte valides</span><span class="sxs-lookup"><span data-stu-id="67fa6-137">Valid host patterns</span></span>|<span data-ttu-id="67fa6-138">Correspond</span><span class="sxs-lookup"><span data-stu-id="67fa6-138">Matches</span></span>|<span data-ttu-id="67fa6-139">Ne correspond pas</span><span class="sxs-lookup"><span data-stu-id="67fa6-139">Doesn't match</span></span>|
|--|--|--|
|  `*://*.example.*` | `http://example.com`<br>`https://test.example.co.uk`   | `https://example.microsoft.com`<br>`http://example.microsoft.co.uk`  |
| `http://example.*` | `http://example.com`<br>`http://example.ly` | `https://example.com`<br>`http://test.example.com`   |
| `http://example.com`   | `http://example.com` | `https://example.com`<br>`http://test.example.co.uk` |
| `*://*`   | <span data-ttu-id="67fa6-140">Toutes les URL</span><span class="sxs-lookup"><span data-stu-id="67fa6-140">All URLs</span></span>  |   |

<span data-ttu-id="67fa6-141">Utilisez les étapes suivantes comme guide pour bloquer ou autoriser les extensions à accéder à un site web ou un domaine.</span><span class="sxs-lookup"><span data-stu-id="67fa6-141">Use the following steps as a guide to block or allow extensions to access a website or domain.</span></span>

1. <span data-ttu-id="67fa6-142">Ouvrez l’éditeur de gestion des stratégies de groupe et sélectionnez **Modèles d’administration > Microsoft Edge > Extensions**, puis sélectionnez **Configurer les paramètres de gestion des extensions**.</span><span class="sxs-lookup"><span data-stu-id="67fa6-142">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions**, and then select **Configure extension management settings**.</span></span>  
2. <span data-ttu-id="67fa6-143">Activez la stratégie, puis entrez les autorisations que vous souhaitez autoriser ou bloquer, en compressant les autorisations sur une seule chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="67fa6-143">Enable the policy, then enter the permissions that you want allowed or blocked, compressing the permissions to a single JSON string.</span></span>

<span data-ttu-id="67fa6-144">Les exemples suivants montrent comment bloquer des extensions sur un nom d’hôte et comment bloquer des extensions sur le même domaine.</span><span class="sxs-lookup"><span data-stu-id="67fa6-144">The following examples show how to block extensions on a hostname and how to block extensions on the same domain.</span></span>

### <a name="json-example-to-block-hostname"></a><span data-ttu-id="67fa6-145">Exemple JSON pour bloquer le nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="67fa6-145">JSON example to block hostname</span></span>

<span data-ttu-id="67fa6-146">Cet exemple illustre le JSON et la chaîne JSON compressée pour empêcher toute extension d’accéder au nom d’hôte `www.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="67fa6-146">This example shows the JSON and compressed JSON string to block any extension from accessing the `www.microsoft.com` hostname.</span></span>

```json
{ 
    "*":{ 
            "runtime_blocked_hosts":["www.microsoft.com"] 
    } 
} 
```

```json
{"*":{"runtime_blocked_hosts":["www.microsoft.com"]}} 
```

> [!NOTE]
> <span data-ttu-id="67fa6-147">Pour empêcher toutes les extensions d’accéder à une page web, utilisez un astérisque pour l’ID d’extension, comme illustré dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="67fa6-147">To block all extensions from accessing a webpage, use an asterisk for the extension ID, as shown in the previous example.</span></span>  <span data-ttu-id="67fa6-148">Si vous spécifiez un ID d’extension au lieu d’un astérisque, la stratégie s’applique uniquement à cette extension.</span><span class="sxs-lookup"><span data-stu-id="67fa6-148">If you specify one extension ID instead of an asterisk, the policy will only apply to that extension.</span></span> <span data-ttu-id="67fa6-149">Vous pouvez bloquer plusieurs extensions, mais elles doivent être des entrées distinctes.</span><span class="sxs-lookup"><span data-stu-id="67fa6-149">You can block more than one extension, but they need to be separate entries.</span></span>

### <a name="json-example-to-block-extensions-on-same-domain"></a><span data-ttu-id="67fa6-150">Exemple JSON pour bloquer les extensions sur le même domaine</span><span class="sxs-lookup"><span data-stu-id="67fa6-150">JSON example to block extensions on same domain</span></span>

<span data-ttu-id="67fa6-151">Cet exemple montre la chaîne JSON et JSON compressée pour empêcher l’exécution d’extensions spécifiques sur le même domaine, «importantwebsite».</span><span class="sxs-lookup"><span data-stu-id="67fa6-151">This example shows the JSON and compressed JSON string to block specific extensions from running on the same domain, "importantwebsite".</span></span>

```json
{ 
    "aapbdbdomjkkjkaonfhkkikfgjllcleb": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    }, 
    "bfbmjmiodbnnpllbbbfblcplfjjepjdn": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    } 
} 
```

```json
{"aapbdbdomjkkjkaonfhkkikfgjllcleb": {"runtime_blocked_hosts": ["*://,*.importantwebsite"]},"bfbmjmiodbnnpllbbbfblcplfjjepjdn": {"runtime_blocked_hosts": ["*://*.importantwebsite"]}} 
```

## <a name="allow-or-block-extensions-in-group-policy"></a><span data-ttu-id="67fa6-152">Autoriser ou bloquer les extensions dans la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="67fa6-152">Allow or block extensions in group policy</span></span>

<span data-ttu-id="67fa6-153">Vous pouvez utiliser les stratégies [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist) et [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist) pour contrôler les extensions bloquées ou autorisées.</span><span class="sxs-lookup"><span data-stu-id="67fa6-153">You can use the [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist) and [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist) policies to control which extensions are blocked or allowed.</span></span> <span data-ttu-id="67fa6-154">Utilisez les étapes suivantes comme guide pour autoriser toutes les extensions à l’exception de celles que vous souhaitez bloquer.</span><span class="sxs-lookup"><span data-stu-id="67fa6-154">Use the following steps as a guide to allow all extensions except those you want to block.</span></span>

1. <span data-ttu-id="67fa6-155">Ouvrez l’éditeur de gestion des stratégies de groupe et sélectionnez Modèles d’administration **> Microsoft Edge > Extensions >**, puis sélectionnez **Contrôler les extensions qui ne peuvent pas être installées**.</span><span class="sxs-lookup"><span data-stu-id="67fa6-155">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions >** and then select **Control which extensions cannot be installed**.</span></span>
2. <span data-ttu-id="67fa6-156">Sélectionnez **Activé**.</span><span class="sxs-lookup"><span data-stu-id="67fa6-156">Select **Enabled**.</span></span>
3. <span data-ttu-id="67fa6-157">Cliquez sur **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="67fa6-157">Click **Show**.</span></span>
4. <span data-ttu-id="67fa6-158">Entrez l’ID d’application des extensions que vous souhaitez bloquer.</span><span class="sxs-lookup"><span data-stu-id="67fa6-158">Enter the app ID of the extensions that you want to block.</span></span> <span data-ttu-id="67fa6-159">Lorsque vous ajoutez plusieurs ID d’application, utilisez une ligne distincte pour chaque ID.</span><span class="sxs-lookup"><span data-stu-id="67fa6-159">When adding multiple app ID’s use a separate row for each ID.</span></span>
5. <span data-ttu-id="67fa6-160">Pour bloquer toutes les extensions, tapez **\*** dans la stratégie pour empêcher l’installation des extensions.</span><span class="sxs-lookup"><span data-stu-id="67fa6-160">To block all extensions, type **\*** into the policy to prevent any extensions from being installed.</span></span> <span data-ttu-id="67fa6-161">Vous pouvez l’utiliser conjointement avec la stratégie «Autoriser l’installation d’extensions spécifiques» pour autoriser uniquement l’installation de certaines extensions.</span><span class="sxs-lookup"><span data-stu-id="67fa6-161">You can use this in conjunction with the "Allow specific extensions to be installed" policy to only allow certain extensions to be installed.</span></span> <span data-ttu-id="67fa6-162">La capture d’écran suivante montre une extension qui sera bloquée en fonction de l’ID d’application fourni.</span><span class="sxs-lookup"><span data-stu-id="67fa6-162">The next screenshot shows an extension that will be blocked based on the app ID that's provided.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-2.png" alt-text="Utilisez l’ID d’application pour bloquer une extension.":::

   > [!TIP]
   > <span data-ttu-id="67fa6-164">Si vous ne trouvez pas l’ID d’application d’une extension, reportez-vous à l’extension sur le site web des modules complémentaires MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="67fa6-164">If you can’t find the app ID of an extension, look at the extension in the Microsoft Edge Add-ons website.</span></span> <span data-ttu-id="67fa6-165">Recherchez l’extension spécifique et l’ID de l’application s’affichera à la fin de l’URL dans l’omnibox.</span><span class="sxs-lookup"><span data-stu-id="67fa6-165">Find the specific extension and you will see the app ID at the end of the URL in the omnibox.</span></span>

> [!NOTE]
> <span data-ttu-id="67fa6-166">Vous pouvez ajouter une extension à la liste de blocage déjà installée sur l’ordinateur d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="67fa6-166">You can add an extension to the blocklist that’s already installed on a user’s computer.</span></span> <span data-ttu-id="67fa6-167">Cela désactive l’extension et empêche l’utilisateur de la réactiver.</span><span class="sxs-lookup"><span data-stu-id="67fa6-167">This will disable the extension and prevent the user from re-enabling it.</span></span> <span data-ttu-id="67fa6-168">Elle ne sera pas désinstallée, mais simplement désactivée.</span><span class="sxs-lookup"><span data-stu-id="67fa6-168">It won't be uninstalled, just disabled.</span></span>

## <a name="force-install-an-extension"></a><span data-ttu-id="67fa6-169">Forcer l’installation d’une extension</span><span class="sxs-lookup"><span data-stu-id="67fa6-169">Force-install an extension</span></span>

<span data-ttu-id="67fa6-170">Utilisez la [stratégie ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) pour contrôler les extensions bloquées ou autorisées.</span><span class="sxs-lookup"><span data-stu-id="67fa6-170">Use the [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) policy to control which extensions are blocked or allowed.</span></span> <span data-ttu-id="67fa6-171">Utilisez les étapes suivantes comme guide pour forcer l’installation d’une extension.</span><span class="sxs-lookup"><span data-stu-id="67fa6-171">Use the following steps as a guide to force-install an extension.</span></span>

1. <span data-ttu-id="67fa6-172">Dans l’Éditeur de stratégie de groupe, sélectionnez **Modèles d’administration> Microsoft Edge > Extensions >**, puis sélectionnez **Contrôler les extensions installées en mode silencieux**.</span><span class="sxs-lookup"><span data-stu-id="67fa6-172">In the Group Policy Editor, go to **Administrative Templates> Microsoft Edge >  Extensions >** and then select **Control which extensions are installed silently**.</span></span>
2. <span data-ttu-id="67fa6-173">Sélectionnez **Activé**.</span><span class="sxs-lookup"><span data-stu-id="67fa6-173">Select **Enabled**.</span></span>  
3. <span data-ttu-id="67fa6-174">Cliquez sur **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="67fa6-174">Click **Show**.</span></span>
4. <span data-ttu-id="67fa6-175">Entrez l’ID d’application ou les ID de l’extension ou des extensions pour lesquelles vous souhaitez forcer l’installation.</span><span class="sxs-lookup"><span data-stu-id="67fa6-175">Enter the app ID or IDs of the extension or extensions you want to force-install.</span></span>  

<span data-ttu-id="67fa6-176">L’extension sera installée sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="67fa6-176">The extension will be installed silently with no need for user interaction.</span></span> <span data-ttu-id="67fa6-177">L’utilisateur ne peut pas non plus désinstaller ou désactiver l’extension.</span><span class="sxs-lookup"><span data-stu-id="67fa6-177">The user also won’t be able to uninstall or disable the extension.</span></span> <span data-ttu-id="67fa6-178">Ce paramètre remplace toute stratégie de liste de blocage activée.</span><span class="sxs-lookup"><span data-stu-id="67fa6-178">This setting will overwrite over any blocklist policy that’s enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="67fa6-179">Pour les extensions hébergées dans le Chrome Web Store, utilisez une chaîne telle que: `pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`.</span><span class="sxs-lookup"><span data-stu-id="67fa6-179">For extensions hosted in the Chrome web store use a string such as: `pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`.</span></span>

## <a name="block-extensions-from-a-specific-store-or-update-url"></a><span data-ttu-id="67fa6-180">Bloquer les extensions à partir d’une URL de mise à jour ou de magasin spécifique</span><span class="sxs-lookup"><span data-stu-id="67fa6-180">Block extensions from a specific store or update URL</span></span>

<span data-ttu-id="67fa6-181">Pour bloquer les extensions d’un magasin ou d’une URL spécifique, vous devez uniquement bloquer la stratégie *update_url* pour ce magasin à l’aide de la stratégie [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings).</span><span class="sxs-lookup"><span data-stu-id="67fa6-181">To block extensions from a particular store or URL, you only need to block the *update_url* for that store using the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy.</span></span>

<span data-ttu-id="67fa6-182">Utilisez les étapes suivantes comme guide pour bloquer les extensions à partir d’un magasin ou d’une URL spécifique.</span><span class="sxs-lookup"><span data-stu-id="67fa6-182">Use the following steps as a guide to block extensions from an particular store or URL.</span></span>

1. <span data-ttu-id="67fa6-183">Ouvrez l’éditeur de gestion des stratégies de groupe et sélectionnez **Modèles d’administration > Microsoft Edge > Extensions >**, puis sélectionnez **Configurer les paramètres de gestion des extensions**.</span><span class="sxs-lookup"><span data-stu-id="67fa6-183">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions >** and then select **Configure extension management settings**.</span></span>  
2. <span data-ttu-id="67fa6-184">Activez la stratégie, puis entrez les autorisations que vous souhaitez autoriser ou bloquer, en la compressant en une seule chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="67fa6-184">Enable the policy, then enter the permissions that you want allowed or blocked, compressing it to a single JSON string.</span></span>

<span data-ttu-id="67fa6-185">L’exemple suivant montre JSON et la chaîne JSON compressée à bloquer à partir du Chrome Web Store à l’aide de son URL de mise à jour (`https://clients2.google.com/service/update2/crx`).</span><span class="sxs-lookup"><span data-stu-id="67fa6-185">The next example shows the JSON and compressed JSON string to block from the Chrome Web Store using its update URL (`https://clients2.google.com/service/update2/crx`).</span></span>

### <a name="json-example-for-blocking-on-update-url"></a><span data-ttu-id="67fa6-186">Exemple JSON pour le blocage sur l’URL de mise à jour</span><span class="sxs-lookup"><span data-stu-id="67fa6-186">JSON example for blocking on update URL</span></span>

```json
{ 
"update_url:https://clients2.google.com/service/update2/crx":{ 
                                                             " installation_mode":"blocked" 
                                                             } 
} 
```

```json
{"update_url:https://clients2.google.com/service/update2/crx":{"installation_mode":"blocked"}} 
```

> [!NOTE]
> <span data-ttu-id="67fa6-187">Vous pouvez toujours utiliser **ExtensionInstallForceList** et **ExtensionInstallAllowList** pour autoriser/forcer l’installation d’extensions spécifiques, même si le magasin est bloqué à l’aide du JSON dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="67fa6-187">You can still use **ExtensionInstallForceList** and **ExtensionInstallAllowList** to allow/force install specific extensions even if the store is blocked using the JSON in the previous example.</span></span>

## <a name="see-also"></a><span data-ttu-id="67fa6-188">Voir également</span><span class="sxs-lookup"><span data-stu-id="67fa6-188">See also</span></span>

- [<span data-ttu-id="67fa6-189">Gérer les extensions MicrosoftEdge dans l’entreprise</span><span class="sxs-lookup"><span data-stu-id="67fa6-189">Manage Microsoft Edge extensions in the enterprise</span></span>](microsoft-edge-manage-extensions.md)
- [<span data-ttu-id="67fa6-190">Créer un magasin web pour héberger les extensions MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="67fa6-190">Create a web store to host Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-webstore.md)
- [<span data-ttu-id="67fa6-191">Guide de référence pour la stratégie ExtensionSettings</span><span class="sxs-lookup"><span data-stu-id="67fa6-191">Reference guide for the ExtensionSettings policy</span></span>](microsoft-edge-manage-extensions-ref-guide.md)
- [<span data-ttu-id="67fa6-192">FAQ sur les extensions Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="67fa6-192">FAQ for Microsoft Edge Extensions</span></span>](microsoft-edge-manage-extensions-faq.md)
- [<span data-ttu-id="67fa6-193">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="67fa6-193">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
