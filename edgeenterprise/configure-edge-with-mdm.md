---
title: Configurer Microsoft Edge à l’aide de Gestion des périphériques mobiles
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 10/25/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer Microsoft Edge à l’aide de Gestion des périphériques mobiles.
ms.openlocfilehash: dda35199f653b3dfb8f20b33b068c59621222b36
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979687"
---
# <span data-ttu-id="04c3a-103">Configurer Microsoft Edge à l’aide de Gestion des périphériques mobiles</span><span class="sxs-lookup"><span data-stu-id="04c3a-103">Configure Microsoft Edge using Mobile Device Management</span></span>

<span data-ttu-id="04c3a-104">Cet article explique comment configurer MicrosoftEdge sur Windows10 à l’aide de [Gestion des périphériques mobiles (GPM)](https://docs.microsoft.com/windows/client-management/mdm/) au moyen de l’[Ingestion ADMX](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span><span class="sxs-lookup"><span data-stu-id="04c3a-104">This article explains how to configure Microsoft Edge on Windows 10 using [Mobile Device Management (MDM)](https://docs.microsoft.com/windows/client-management/mdm/) by means of [ADMX Ingestion](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span></span> <span data-ttu-id="04c3a-105">Cet article présente également:</span><span class="sxs-lookup"><span data-stu-id="04c3a-105">This article also describes:</span></span>

- <span data-ttu-id="04c3a-106">Procédure de [création d’un identifiant OMA-URI (Open Mobile Alliance Uniform Resource Identifier) pour les stratégies MicrosoftEdge](#create-an-oma-uri-for-microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="04c3a-106">How to [create Open Mobile Alliance Uniform Resource Identifier (OMA-URI) for Microsoft Edge policies](#create-an-oma-uri-for-microsoft-edge-policies).</span></span>
- <span data-ttu-id="04c3a-107">Procédure de [configuration de MicrosoftEdge dans Intune à l’aide de l’ingestion ADMX et d’un OMA-URI personnalisé](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span><span class="sxs-lookup"><span data-stu-id="04c3a-107">How to [configure Microsoft Edge in Intune using ADMX ingestion and custom OMA-URI](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span></span>

> [!NOTE]
> <span data-ttu-id="04c3a-108">Cet article concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="04c3a-108">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="04c3a-109">Éléments prérequis</span><span class="sxs-lookup"><span data-stu-id="04c3a-109">Prerequisites</span></span>

<span data-ttu-id="04c3a-110">Windows10, avec la configuration minimale requise suivante:</span><span class="sxs-lookup"><span data-stu-id="04c3a-110">Windows 10, with the following minimum system requirements:</span></span>

- <span data-ttu-id="04c3a-111">Windows10, version1903 avec les mises à jour [KB4512941](https://support.microsoft.com/help/4512941/) et [KB4517211](https://support.microsoft.com/help/4517211/) installées</span><span class="sxs-lookup"><span data-stu-id="04c3a-111">Windows 10, version 1903 with [KB4512941](https://support.microsoft.com/help/4512941/) and [KB4517211](https://support.microsoft.com/help/4517211/) installed</span></span>
- <span data-ttu-id="04c3a-112">Windows10, version1809 avec les mises à jour [KB4512534](https://support.microsoft.com/help/4512534/) et [KB4520062](https://support.microsoft.com/help/4520062/) installées</span><span class="sxs-lookup"><span data-stu-id="04c3a-112">Windows 10, version 1809 with [KB4512534](https://support.microsoft.com/help/4512534/) and [KB4520062](https://support.microsoft.com/help/4520062/) installed</span></span>
- <span data-ttu-id="04c3a-113">Windows10, version1803 avec les mises à jour [KB4512509](https://support.microsoft.com/help/4512509/) et [KB4519978](https://support.microsoft.com/help/4519978) installées</span><span class="sxs-lookup"><span data-stu-id="04c3a-113">Windows 10, version 1803 with [KB4512509](https://support.microsoft.com/help/4512509/) and [KB4519978](https://support.microsoft.com/help/4519978) installed</span></span>
- <span data-ttu-id="04c3a-114">Windows10, version1709 avec les mises à jour [KB4516071](https://support.microsoft.com/help/4516071/) et [KB4520006](https://support.microsoft.com/help/4520006) installées</span><span class="sxs-lookup"><span data-stu-id="04c3a-114">Windows 10, version 1709 with [KB4516071](https://support.microsoft.com/help/4516071/) and [KB4520006](https://support.microsoft.com/help/4520006) installed</span></span>

## <span data-ttu-id="04c3a-115">Présentation</span><span class="sxs-lookup"><span data-stu-id="04c3a-115">Overview</span></span>

<span data-ttu-id="04c3a-116">Vous pouvez configurer MicrosoftEdge sur Windows10 à l’aide de GPM avec votre fournisseur préféré de Gestion de la mobilité d’entreprise ou GPM qui prend en charge l’[Ingestion ADMX](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span><span class="sxs-lookup"><span data-stu-id="04c3a-116">You can configure Microsoft Edge on Windows 10 using MDM with your preferred Enterprise Mobility Management (EMM) or MDM provider that supports [ADMX Ingestion](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span></span>

<span data-ttu-id="04c3a-117">La configuration de MicrosoftEdge avec GPM est un processus en deux parties:</span><span class="sxs-lookup"><span data-stu-id="04c3a-117">Configuring Microsoft Edge with MDM is a two part process:</span></span>

1. <span data-ttu-id="04c3a-118">Intégration du fichier ADMX MicrosoftEdge dans votre fournisseur EMM ou GPM.</span><span class="sxs-lookup"><span data-stu-id="04c3a-118">Ingesting the Microsoft Edge ADMX file into your EMM or MDM provider.</span></span> <span data-ttu-id="04c3a-119">Pour obtenir des instructions sur l’ingestion d’un fichier ADMX, consultez votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="04c3a-119">See your provider for instructions on how to ingest an ADMX file.</span></span>

   > [!NOTE]
   > <span data-ttu-id="04c3a-120">Pour MicrosoftIntune, consultez [Configurer MicrosoftEdge dans Intune à l’aide de l’ingestion ADMX](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span><span class="sxs-lookup"><span data-stu-id="04c3a-120">For Microsoft Intune, see [Configure Microsoft Edge in Intune using ADMX ingestion](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span></span>

2. <span data-ttu-id="04c3a-121">[Création d’un OMA-URI pour une stratégie MicrosoftEdge](#create-an-oma-uri-for-microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="04c3a-121">[Creating an OMA-URI for a Microsoft Edge policy](#create-an-oma-uri-for-microsoft-edge-policies).</span></span>

## <span data-ttu-id="04c3a-122">Créer un OMA-URI pour les stratégies MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="04c3a-122">Create an OMA-URI for Microsoft Edge policies</span></span>

<span data-ttu-id="04c3a-123">Les sections suivantes décrivent la procédure de création du chemin d’accès OMA-URI et la procédure de recherche et de définition de la valeur au format XML pour les stratégies de navigateur obligatoires et recommandées.</span><span class="sxs-lookup"><span data-stu-id="04c3a-123">The following sections describe how to create the OMA-URI path and look up and define the value in XML format for mandatory and recommended browser polices.</span></span>

<span data-ttu-id="04c3a-124">Avant de commencer, téléchargez le fichier de modèles de stratégie MicrosoftEdge (MicrosoftEdgePolicyTemplates.cab) à partir de [la page d’accueil de MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise) et extrayez le contenu.</span><span class="sxs-lookup"><span data-stu-id="04c3a-124">Before you get started download the Microsoft Edge policy templates file (MicrosoftEdgePolicyTemplates.cab) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise) and extract the contents.</span></span>

<span data-ttu-id="04c3a-125">Il existe trois étapes pour définir l’OMA-URI:</span><span class="sxs-lookup"><span data-stu-id="04c3a-125">There are three steps for defining the OMA-URI:</span></span>

1. [<span data-ttu-id="04c3a-126">Créer le chemin d’accès OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-126">Create the OMA-URI path</span></span>](#create-the-oma-uri-path)
2. [<span data-ttu-id="04c3a-127">Spécifier le type de données OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-127">Specify the OMA-URI data type</span></span>](#specify-the-data-type)
3. [<span data-ttu-id="04c3a-128">Définir la valeur OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-128">Set the OMA-URI value</span></span>](#set-the-value-for-a-browser-policy)

### <span data-ttu-id="04c3a-129">Créer le chemin d’accès OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-129">Create the OMA-URI path</span></span>

<span data-ttu-id="04c3a-130">Utilisez la formule suivante comme guide pour la création des chemins d’accès OMA-URI.</span><span class="sxs-lookup"><span data-stu-id="04c3a-130">Use the following formula as a guide for creating the OMA-URI paths.</span></span> <br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`* <br/><br/>

| <span data-ttu-id="04c3a-131">Paramètre</span><span class="sxs-lookup"><span data-stu-id="04c3a-131">Parameter</span></span>         | <span data-ttu-id="04c3a-132">Description</span><span class="sxs-lookup"><span data-stu-id="04c3a-132">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| \<ADMXIngestName> | <span data-ttu-id="04c3a-133">Utilisez «Edge» ou ce que vous avez défini lors de l’ingestion du modèle d’administration.</span><span class="sxs-lookup"><span data-stu-id="04c3a-133">Use "Edge" or what you defined when ingesting the administrative template.</span></span> <span data-ttu-id="04c3a-134">Par exemple, si vous avez utilisé «./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx», utilisez «MicrosoftEdge».</span><span class="sxs-lookup"><span data-stu-id="04c3a-134">For example, if you used "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx", then use "MicrosoftEdge".</span></span><br/><br/> <span data-ttu-id="04c3a-135">Le `<ADMXIngestionName>` doit correspondre à celui utilisé lors de l’ingestion du fichier ADMX.</span><span class="sxs-lookup"><span data-stu-id="04c3a-135">The `<ADMXIngestionName>` must match what was used when you ingested the ADMX file.</span></span> |
| \<ADMXNamespace>  | <span data-ttu-id="04c3a-136">«microsoft_edge» ou «microsoft_edge_recommended», selon que vous définissez une stratégie obligatoire ou recommandée.</span><span class="sxs-lookup"><span data-stu-id="04c3a-136">Either "microsoft_edge" or "microsoft_edge_recommended" depending on whether you're setting a mandatory or recommended policy.</span></span> |
| \<ADMXCategory>   | <span data-ttu-id="04c3a-137">La catégorie «parentCategory» de la stratégie est définie dans le fichier ADMX.</span><span class="sxs-lookup"><span data-stu-id="04c3a-137">The "parentCategory" of the policy is defined in the ADMX file.</span></span> <span data-ttu-id="04c3a-138">Omettez `<ADMXCategory>` si la stratégie n’est pas groupée (aucune «parentCategory» définie).</span><span class="sxs-lookup"><span data-stu-id="04c3a-138">Omit the `<ADMXCategory>` if the policy isn't grouped (No "parentCategory" defined).</span></span> |
| \<PolicyName>     | <span data-ttu-id="04c3a-139">Le nom de la stratégie est indiqué dans l’article [Référence de la stratégie du navigateur](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="04c3a-139">The policy name can be found in the [Browser policy reference](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies) article.</span></span> |

#### <span data-ttu-id="04c3a-140">Exemple de chemin d’URI:</span><span class="sxs-lookup"><span data-stu-id="04c3a-140">URI path example:</span></span>

<span data-ttu-id="04c3a-141">Pour cet exemple, supposons que le nœud `<ADMXIngestName>` est nommé «Edge» et que vous définissez une stratégie obligatoire.</span><span class="sxs-lookup"><span data-stu-id="04c3a-141">For this example, assume the `<ADMXIngestName>` node was named “Edge" and you're setting a mandatory policy.</span></span> <span data-ttu-id="04c3a-142">Le chemin d’URI serait:</span><span class="sxs-lookup"><span data-stu-id="04c3a-142">The URI path would be:</span></span><br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~<ADMXCategory>/<PolicyName>`*

<span data-ttu-id="04c3a-143">Si la stratégie n’est pas dans un groupe (par exemple, DiskCacheSize), supprimez «`~<ADMXCategory>`».</span><span class="sxs-lookup"><span data-stu-id="04c3a-143">If the policy isn't in a group (for example, DiskCacheSize) remove "`~<ADMXCategory>`".</span></span> <span data-ttu-id="04c3a-144">Remplacez `<PolicyName>` par le nom de la stratégie, DiskCacheSize.</span><span class="sxs-lookup"><span data-stu-id="04c3a-144">Replace `<PolicyName>` with the name of the policy, DiskCacheSize.</span></span> <span data-ttu-id="04c3a-145">Le chemin d’URI serait:</span><span class="sxs-lookup"><span data-stu-id="04c3a-145">The URI path would be:</span></span><br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`*

<span data-ttu-id="04c3a-146">Si la stratégie se trouve dans un groupe, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="04c3a-146">If the policy is in a group, follow these steps:</span></span>

1. <span data-ttu-id="04c3a-147">Ouvrez **msedge.admx** avec n’importe quel éditeur xml.</span><span class="sxs-lookup"><span data-stu-id="04c3a-147">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="04c3a-148">Recherchez le nom de la stratégie que vous souhaitez définir.</span><span class="sxs-lookup"><span data-stu-id="04c3a-148">Search for the policy name you want to set.</span></span> <span data-ttu-id="04c3a-149">Par exemple, «ExtensionInstallForceList».</span><span class="sxs-lookup"><span data-stu-id="04c3a-149">For example, "ExtensionInstallForceList".</span></span>
3. <span data-ttu-id="04c3a-150">Utilisez la valeur de l’attribut *ref* de l’élément *parentCategory*.</span><span class="sxs-lookup"><span data-stu-id="04c3a-150">Use the value of the *ref* attribute from the *parentCategory* element.</span></span> <span data-ttu-id="04c3a-151">Par exemple, «Extensions» de \<parentCategory ref=" Extensions"/>.</span><span class="sxs-lookup"><span data-stu-id="04c3a-151">For example, "Extensions" from \<parentCategory ref=" Extensions"/>.</span></span>
4. <span data-ttu-id="04c3a-152">Remplacez `<ADMXCategory>` par la valeur *ref* de l’attribut pour construire le chemin d’accès de l’URI.</span><span class="sxs-lookup"><span data-stu-id="04c3a-152">Replace `<ADMXCategory>` with the *ref* attribute value to construct the URI path.</span></span> <span data-ttu-id="04c3a-153">Le chemin d’URI serait:</span><span class="sxs-lookup"><span data-stu-id="04c3a-153">The URI path would be:</span></span><br/><br/>
*`/Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`*

### <span data-ttu-id="04c3a-154">Spécifier le type de données</span><span class="sxs-lookup"><span data-stu-id="04c3a-154">Specify the data type</span></span>

<span data-ttu-id="04c3a-155">Le type de données OMA-URI est toujours «chaîne».</span><span class="sxs-lookup"><span data-stu-id="04c3a-155">The OMA-URI data type is always “String”.</span></span>

### <span data-ttu-id="04c3a-156">Définir la valeur d’une stratégie de navigateur</span><span class="sxs-lookup"><span data-stu-id="04c3a-156">Set the value for a browser policy</span></span>

<span data-ttu-id="04c3a-157">Cette section décrit comment définir la valeur, au format XML, pour chaque type de données.</span><span class="sxs-lookup"><span data-stu-id="04c3a-157">This section describes how to set the value, in XML format, for each data type.</span></span> <span data-ttu-id="04c3a-158">Accédez à la [Référence de stratégie du navigateur](https://docs.microsoft.com/deployedge/microsoft-edge-policies) pour rechercher le type de données de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="04c3a-158">Go to [Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies) to look up the data type of the policy.</span></span>

> [!NOTE]
> <span data-ttu-id="04c3a-159">Pour les données de type non booléen, la valeur commence toujours par `<enabled/>`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-159">For non-Boolean data types, the value always starts with `<enabled/>`.</span></span>

#### <span data-ttu-id="04c3a-160">Données de type booléen</span><span class="sxs-lookup"><span data-stu-id="04c3a-160">Boolean data type</span></span>

<span data-ttu-id="04c3a-161">Pour les stratégies qui sont des types booléens, utilisez `<enabled/>` ou `<disabled/>`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-161">For policies that are Boolean types use `<enabled/>` or `<disabled/>`.</span></span>

#### <span data-ttu-id="04c3a-162">Données de type entier</span><span class="sxs-lookup"><span data-stu-id="04c3a-162">Integer data type</span></span>

<span data-ttu-id="04c3a-163">La valeur doit toujours commencer par l’élément `<enabled/>` suivi de `<data id="[valueName]" value="[decimal value]"/>`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-163">The value always needs to start with the `<enabled/>` element followed by `<data id="[valueName]" value="[decimal value]"/>`.</span></span>

<span data-ttu-id="04c3a-164">Pour rechercher le nom de la valeur et la valeur décimale d’une nouvelle page d’onglets, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="04c3a-164">To find the value name and decimal value for a new tab page, use the following steps:</span></span>

1. <span data-ttu-id="04c3a-165">Ouvrez **msedge.admx** avec n’importe quel éditeur xml.</span><span class="sxs-lookup"><span data-stu-id="04c3a-165">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="04c3a-166">Recherchez l’élément `<policy>` dans lequel l’attribut Name correspond au nom de la stratégie que vous souhaitez définir.</span><span class="sxs-lookup"><span data-stu-id="04c3a-166">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="04c3a-167">Pour «RestoreOnStartup», recherchez `name="RestoreOnStartup"`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-167">For "RestoreOnStartup", search for `name="RestoreOnStartup"`.</span></span>
3. <span data-ttu-id="04c3a-168">Dans le nœud `<elements>`, recherchez la valeur que vous souhaitez définir.</span><span class="sxs-lookup"><span data-stu-id="04c3a-168">In the `<elements>` node, find the value you want to set.</span></span>
4. <span data-ttu-id="04c3a-169">Utilisez la valeur de l’attribut «valueName» dans le nœud `<elements>`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-169">Use the value in the "valueName" attribute in the `<elements>` node.</span></span> <span data-ttu-id="04c3a-170">Pour «RestoreOnStartup», «valueName» est «RestoreOnStartup».</span><span class="sxs-lookup"><span data-stu-id="04c3a-170">For "RestoreOnStartup" the "valueName" is "RestoreOnStartup".</span></span>
5. <span data-ttu-id="04c3a-171">Utilisez la valeur de l’attribut «value» dans le nœud `<decimal>`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-171">Use the value in the "value" attribute in the `<decimal>` node.</span></span> <span data-ttu-id="04c3a-172">Pour «RestoreOnStartup» pour ouvrir la page de nouvel onglet, la valeur est «5».</span><span class="sxs-lookup"><span data-stu-id="04c3a-172">For "RestoreOnStartup" to open the new tab page the value is "5".</span></span>

<span data-ttu-id="04c3a-173">Pour ouvrir la page de nouvel onglet au démarrage, utilisez:</span><span class="sxs-lookup"><span data-stu-id="04c3a-173">To open the new tab page on startup use:</span></span><br>
`<enabled/> <data id="RestoreOnStartup" value="5"/>`

#### <span data-ttu-id="04c3a-174">Données de type liste de chaînes</span><span class="sxs-lookup"><span data-stu-id="04c3a-174">List of strings data type</span></span>

<span data-ttu-id="04c3a-175">La valeur doit toujours commencer par l’élément `<enabled/>` suivi de `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-175">The value always needs to start with the `<enabled/>` element followed by `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.</span></span>

> [!NOTE]
> <span data-ttu-id="04c3a-176">Le nom d’attribut «id» n’est pas le nom de la stratégie, même si, dans la plupart des cas, il correspond au nom de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="04c3a-176">The "id=" attribute name isn't the policy name, even though in most cases it matches the policy name.</span></span> <span data-ttu-id="04c3a-177">Il s’agit de la valeur de l’attribut de nœud \<list>, qui se trouve dans le fichier ADMX.</span><span class="sxs-lookup"><span data-stu-id="04c3a-177">It's the \<list> node id attribute value, which is found in the ADMX file.</span></span>

<span data-ttu-id="04c3a-178">Pour rechercher le listID et définir la valeur pour bloquer une URL, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="04c3a-178">To find the listID and define the value to block a URL, follow these steps:</span></span>

1. <span data-ttu-id="04c3a-179">Ouvrez **msedge.admx** avec n’importe quel éditeur xml.</span><span class="sxs-lookup"><span data-stu-id="04c3a-179">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="04c3a-180">Recherchez l’élément `<policy>` dans lequel l’attribut Name correspond au nom de la stratégie que vous souhaitez définir.</span><span class="sxs-lookup"><span data-stu-id="04c3a-180">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="04c3a-181">Pour «URLBlocklist», recherchez `name="URLBlocklist"`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-181">For "URLBlocklist", search for `name="URLBlocklist"`.</span></span>
3. <span data-ttu-id="04c3a-182">Utilisez la valeur de l’attribut «id» du nœud `<list> node for [listID]`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-182">Use the value in the "id" attribute of the `<list> node for [listID]`.</span></span>
4. <span data-ttu-id="04c3a-183">La «valeur» est une liste d’URL séparées par un point-virgule (;)</span><span class="sxs-lookup"><span data-stu-id="04c3a-183">The "value" is a list of URLs separated by a semicolon (;)</span></span>

<span data-ttu-id="04c3a-184">Par exemple, pour bloquer l’accès à `contoso.com` et à `https://ssl.server.com`:</span><span class="sxs-lookup"><span data-stu-id="04c3a-184">For example, to block access to `contoso.com` and `https://ssl.server.com`:</span></span><br>
`<enabled/> <data id=" URLBlocklistDesc" value="contoso.com;https://ssl.server.com"/>`

#### <span data-ttu-id="04c3a-185">Type de données dictionnaire ou chaîne</span><span class="sxs-lookup"><span data-stu-id="04c3a-185">Dictionary or String data type</span></span>

<span data-ttu-id="04c3a-186">La valeur doit toujours commencer par l’élément `<enabled/>` suivi de `<data id="[textID]" value="[string]"/>`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-186">The value always needs to start with the `<enabled/>` followed by `<data id="[textID]" value="[string]"/>` .</span></span>

<span data-ttu-id="04c3a-187">Pour rechercher le textID et définir la valeur définie par les paramètres régionaux, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="04c3a-187">To find the textID and define the value set the locale, follow these steps:</span></span>

1. <span data-ttu-id="04c3a-188">Ouvrez **msedge.admx** avec n’importe quel éditeur xml.</span><span class="sxs-lookup"><span data-stu-id="04c3a-188">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="04c3a-189">Recherchez l’élément `<policy>` dans lequel l’attribut Name correspond au nom de la stratégie que vous souhaitez définir.</span><span class="sxs-lookup"><span data-stu-id="04c3a-189">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="04c3a-190">Pour «ApplicationLocaleValue», recherchez `name="ApplicationLocaleValue"`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-190">For "ApplicationLocaleValue", search for `name="ApplicationLocaleValue"`.</span></span>
3. <span data-ttu-id="04c3a-191">Utilisez la valeur de l’attribut «id» du nœud `<text>` pour `[textID]`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-191">Use the value in the "id" attribute of the `<text>` node for `[textID]`.</span></span>
4. <span data-ttu-id="04c3a-192">Définissez la «valeur» sur le code de culture.</span><span class="sxs-lookup"><span data-stu-id="04c3a-192">Set the "value" to the culture code.</span></span>

<span data-ttu-id="04c3a-193">Pour définir les paramètres régionaux sur «es-US» avec la stratégie «ApplicationLocaleValue»:</span><span class="sxs-lookup"><span data-stu-id="04c3a-193">To set the locale to "es-US" with the "ApplicationLocaleValue" policy:</span></span><br>
`<enabled/> <data id="ApplicationLocaleValue" value="es-US"/>`

### <span data-ttu-id="04c3a-194">Créer l’OMA-URI pour une stratégie recommandée</span><span class="sxs-lookup"><span data-stu-id="04c3a-194">Create the OMA-URI for a recommended policies</span></span>

<span data-ttu-id="04c3a-195">La définition du chemin d’URI pour les stratégies recommandées dépend de la stratégie que vous souhaitez configurer.</span><span class="sxs-lookup"><span data-stu-id="04c3a-195">Defining the URI path for recommended policies depends on the policy you want to configure.</span></span>

#### <span data-ttu-id="04c3a-196">Pour définir le chemin d’URI d’une stratégie recommandée</span><span class="sxs-lookup"><span data-stu-id="04c3a-196">To define the URI path for a recommended policy</span></span>

<span data-ttu-id="04c3a-197">Utilisez la formule de chemin d’URI (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) et les étapes suivantes pour définir le chemin d’accès de l’URI:</span><span class="sxs-lookup"><span data-stu-id="04c3a-197">Use the URI path formula (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) and the following steps to define the URI path:</span></span>

1. <span data-ttu-id="04c3a-198">Ouvrez **msedge.admx** avec n’importe quel éditeur xml.</span><span class="sxs-lookup"><span data-stu-id="04c3a-198">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="04c3a-199">Si la stratégie que vous souhaitez configurer ne figure pas dans un groupe, passez à l’étape4 et supprimez `~<ADMXCategory>` du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="04c3a-199">If the policy you want to configure isn't in a group, skip to step 4 and remove `~<ADMXCategory>` from the path.</span></span>
3. <span data-ttu-id="04c3a-200">Si la stratégie que vous souhaitez configurer se trouve dans un groupe:</span><span class="sxs-lookup"><span data-stu-id="04c3a-200">If the policy you want to configure is in a group:</span></span>

   - <span data-ttu-id="04c3a-201">Pour consulter la catégorie `<ADMXCategory>`, recherchez la stratégie que vous souhaitez définir.</span><span class="sxs-lookup"><span data-stu-id="04c3a-201">To look up the `<ADMXCategory>`, search for the policy you want to set.</span></span> <span data-ttu-id="04c3a-202">Lors de la recherche, ajoutez «_recommended» au nom de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="04c3a-202">When searching append "_recommended" to the policy name.</span></span> <span data-ttu-id="04c3a-203">Par exemple, une recherche de «RegisteredProtocolHandlers_recommended» a le résultat suivant:</span><span class="sxs-lookup"><span data-stu-id="04c3a-203">For example, a search for "RegisteredProtocolHandlers_recommended” has the following result:</span></span>

        ```xml
         <policy class="Both" displayName="$(string.RegisteredProtocolHandlers)" explainText="$(string.RegisteredProtocolHandlers_Explain)" key="Software\Policies\Microsoft\Edge\Recommended" name="RegisteredProtocolHandlers_recommended" presentation="$(presentation.RegisteredProtocolHandlers)">
           <parentCategory ref="ContentSettings_recommended"/>
           <supportedOn ref="SUPPORTED_WIN7_V77"/>
           <elements>
             <text id="RegisteredProtocolHandlers" maxLength="1000000" valueName="RegisteredProtocolHandlers"/>
           </elements>
         </policy>
        ```

   - <span data-ttu-id="04c3a-204">Copiez la valeur de l’attribut *ref* de l’élément `<parentCategory>`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-204">Copy the value of the *ref* attribute from the `<parentCategory>` element.</span></span> <span data-ttu-id="04c3a-205">Pour «ContentSettings», copiez «ContentSettings_recommended» à partir de `<parentCategory ref=" ContentSettings_recommended"/>`.</span><span class="sxs-lookup"><span data-stu-id="04c3a-205">For "ContentSettings", copy "ContentSettings_recommended" from `<parentCategory ref=" ContentSettings_recommended"/>`.</span></span>
   - <span data-ttu-id="04c3a-206">Remplacez `<ADMXCategory>` par la valeur de l’attribut *ref* pour construire le chemin d’accès de l’URI dans la formule de chemin d’URI.</span><span class="sxs-lookup"><span data-stu-id="04c3a-206">Replace `<ADMXCategory>` with the *ref* attribute value to construct the URI path in the URI path formula.</span></span>

4. <span data-ttu-id="04c3a-207">`<PolicyName>` est le nom de la stratégie, auquel est ajouté «_recommended».</span><span class="sxs-lookup"><span data-stu-id="04c3a-207">The `<PolicyName>` is the name of the policy with "_recommended" appended to it.</span></span>

#### <span data-ttu-id="04c3a-208">Exemples de chemin d’accès OMA-URI pour les stratégies recommandées</span><span class="sxs-lookup"><span data-stu-id="04c3a-208">OMA-URI path examples for recommended policies</span></span>

<span data-ttu-id="04c3a-209">Le tableau suivant présente des exemples de chemins d’accès OMA-URI pour les stratégies recommandées.</span><span class="sxs-lookup"><span data-stu-id="04c3a-209">The following table shows examples of OMA-URI paths for recommended policies.</span></span>

|              <span data-ttu-id="04c3a-210">Stratégie</span><span class="sxs-lookup"><span data-stu-id="04c3a-210">Policy</span></span>               |             <span data-ttu-id="04c3a-211">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-211">OMA-URI</span></span>                      |
|-----------------------------------|------------------------------------------|
| [<span data-ttu-id="04c3a-212">RegisteredProtocolHandlers</span><span class="sxs-lookup"><span data-stu-id="04c3a-212">RegisteredProtocolHandlers</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#registeredprotocolhandlers)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~ContentSettings_recommended/RegisteredProtocolHandlers_recommended`                        |
| [<span data-ttu-id="04c3a-213">PasswordManagerEnabled</span><span class="sxs-lookup"><span data-stu-id="04c3a-213">PasswordManagerEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordmanagerenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~PasswordManager_recommended/PasswordManagerEnabled_recommended`                        |
| [<span data-ttu-id="04c3a-214">PrintHeaderFooter</span><span class="sxs-lookup"><span data-stu-id="04c3a-214">PrintHeaderFooter</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printheaderfooter)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Printing_recommended/PrintHeaderFooter_recommended`                        |
| [<span data-ttu-id="04c3a-215">SmartScreenEnabled</span><span class="sxs-lookup"><span data-stu-id="04c3a-215">SmartScreenEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreenenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~SmartScreen_recommended/SmartScreenEnabled_recommended`                        |
| [<span data-ttu-id="04c3a-216">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="04c3a-216">HomePageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/HomepageLocation_recommended`                        |
| [<span data-ttu-id="04c3a-217">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="04c3a-217">ShowHomeButton</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/ShowHomeButton_recommended`                        |
| [<span data-ttu-id="04c3a-218">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="04c3a-218">FavoritesBarEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~/FavoritesBarEnabled_recommended`                        |

### <span data-ttu-id="04c3a-219">Exemples d’OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-219">OMA-URI examples</span></span>

<span data-ttu-id="04c3a-220">Exemples d’OMA-URI avec leur chemin d’URI, le type et un exemple de valeur.</span><span class="sxs-lookup"><span data-stu-id="04c3a-220">OMA-URI examples with their URI path, type, and an example value.</span></span>

#### <span data-ttu-id="04c3a-221">Exemples de données de type booléen</span><span class="sxs-lookup"><span data-stu-id="04c3a-221">Boolean data type examples</span></span>

*<span data-ttu-id="04c3a-222">[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ShowHomeButton):</span><span class="sxs-lookup"><span data-stu-id="04c3a-222">[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ShowHomeButton):</span></span>*

| <span data-ttu-id="04c3a-223">Champ</span><span class="sxs-lookup"><span data-stu-id="04c3a-223">Field</span></span>   | <span data-ttu-id="04c3a-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-224">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04c3a-225">Nom</span><span class="sxs-lookup"><span data-stu-id="04c3a-225">Name</span></span>    | <span data-ttu-id="04c3a-226">Microsoft Edge: ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="04c3a-226">Microsoft Edge: ShowHomeButton</span></span>                                                       |
| <span data-ttu-id="04c3a-227">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-227">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton` |
| <span data-ttu-id="04c3a-228">type</span><span class="sxs-lookup"><span data-stu-id="04c3a-228">type</span></span>    | <span data-ttu-id="04c3a-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="04c3a-229">String</span></span>                                                                               |
| <span data-ttu-id="04c3a-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-230">Value</span></span>   | `<enabled/>`                                                                          |

*<span data-ttu-id="04c3a-231">[DefaultSearchProviderEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultSearchProviderEnabled):</span><span class="sxs-lookup"><span data-stu-id="04c3a-231">[DefaultSearchProviderEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultSearchProviderEnabled):</span></span>*

| <span data-ttu-id="04c3a-232">Champ</span><span class="sxs-lookup"><span data-stu-id="04c3a-232">Field</span></span>   | <span data-ttu-id="04c3a-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-233">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04c3a-234">Nom</span><span class="sxs-lookup"><span data-stu-id="04c3a-234">Name</span></span>    | <span data-ttu-id="04c3a-235">Microsoft Edge: DefaultSearchProviderEnabled</span><span class="sxs-lookup"><span data-stu-id="04c3a-235">Microsoft Edge: DefaultSearchProviderEnabled</span></span>                                         |
| <span data-ttu-id="04c3a-236">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-236">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~DefaultSearchProvider/DefaultSearchProviderEnabled`    |
| <span data-ttu-id="04c3a-237">type</span><span class="sxs-lookup"><span data-stu-id="04c3a-237">type</span></span>    | <span data-ttu-id="04c3a-238">Chaîne</span><span class="sxs-lookup"><span data-stu-id="04c3a-238">String</span></span>                                                                               |
| <span data-ttu-id="04c3a-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-239">Value</span></span>   | `<disable/>`                                                                          |

### <span data-ttu-id="04c3a-240">Exemples de données de type entier</span><span class="sxs-lookup"><span data-stu-id="04c3a-240">Integer data type examples</span></span>

*<span data-ttu-id="04c3a-241">[AutoImportAtFirstRun](https://docs.microsoft.com/deployedge/microsoft-edge-policies#AutoImportAtFirstRun):</span><span class="sxs-lookup"><span data-stu-id="04c3a-241">[AutoImportAtFirstRun](https://docs.microsoft.com/deployedge/microsoft-edge-policies#AutoImportAtFirstRun):</span></span>*

| <span data-ttu-id="04c3a-242">Champ</span><span class="sxs-lookup"><span data-stu-id="04c3a-242">Field</span></span>   | <span data-ttu-id="04c3a-243">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-243">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04c3a-244">Nom</span><span class="sxs-lookup"><span data-stu-id="04c3a-244">Name</span></span>    | <span data-ttu-id="04c3a-245">Microsoft Edge: AutoImportAtFirstRun</span><span class="sxs-lookup"><span data-stu-id="04c3a-245">Microsoft Edge: AutoImportAtFirstRun</span></span>                                                 |
| <span data-ttu-id="04c3a-246">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-246">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/AutoImportAtFirstRun`   |
| <span data-ttu-id="04c3a-247">type</span><span class="sxs-lookup"><span data-stu-id="04c3a-247">type</span></span>    | <span data-ttu-id="04c3a-248">Chaîne</span><span class="sxs-lookup"><span data-stu-id="04c3a-248">String</span></span>                                                                               |
| <span data-ttu-id="04c3a-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-249">Value</span></span>   | `<enabled/><data id="AutoImportAtFirstRun" value="1"/>`                             |

*<span data-ttu-id="04c3a-250">[DefaultImagesSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultImagesSetting):</span><span class="sxs-lookup"><span data-stu-id="04c3a-250">[DefaultImagesSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultImagesSetting):</span></span>*

| <span data-ttu-id="04c3a-251">Champ</span><span class="sxs-lookup"><span data-stu-id="04c3a-251">Field</span></span>   | <span data-ttu-id="04c3a-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-252">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04c3a-253">Nom</span><span class="sxs-lookup"><span data-stu-id="04c3a-253">Name</span></span>    | <span data-ttu-id="04c3a-254">Microsoft Edge: DefaultImagesSetting</span><span class="sxs-lookup"><span data-stu-id="04c3a-254">Microsoft Edge: DefaultImagesSetting</span></span>                                                 |
| <span data-ttu-id="04c3a-255">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-255">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/DefaultImagesSetting`    |
| <span data-ttu-id="04c3a-256">type</span><span class="sxs-lookup"><span data-stu-id="04c3a-256">type</span></span>    | <span data-ttu-id="04c3a-257">Chaîne</span><span class="sxs-lookup"><span data-stu-id="04c3a-257">String</span></span>                                                                               |
| <span data-ttu-id="04c3a-258">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-258">Value</span></span>   | `<enabled/><data id="DefaultImagesSetting" value="2"/>`                             |

*<span data-ttu-id="04c3a-259">[DiskCacheSize](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DiskCacheSize):</span><span class="sxs-lookup"><span data-stu-id="04c3a-259">[DiskCacheSize](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DiskCacheSize):</span></span>*

| <span data-ttu-id="04c3a-260">Champ</span><span class="sxs-lookup"><span data-stu-id="04c3a-260">Field</span></span>   | <span data-ttu-id="04c3a-261">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-261">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04c3a-262">Nom</span><span class="sxs-lookup"><span data-stu-id="04c3a-262">Name</span></span>    | <span data-ttu-id="04c3a-263">Microsoft Edge: DiskCacheSize</span><span class="sxs-lookup"><span data-stu-id="04c3a-263">Microsoft Edge: DiskCacheSize</span></span>                                                        |
| <span data-ttu-id="04c3a-264">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-264">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`        |
| <span data-ttu-id="04c3a-265">type</span><span class="sxs-lookup"><span data-stu-id="04c3a-265">type</span></span>    | <span data-ttu-id="04c3a-266">Chaîne</span><span class="sxs-lookup"><span data-stu-id="04c3a-266">String</span></span>                                                                               |
| <span data-ttu-id="04c3a-267">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-267">Value</span></span>   | `<enabled/><data id="DiskCacheSize" value="1000000"/>`                               |

#### <span data-ttu-id="04c3a-268">Exemples de données de type liste de chaînes</span><span class="sxs-lookup"><span data-stu-id="04c3a-268">List of strings data type examples</span></span>
<!--
*[NotificationsAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#NotificationsAllowedForUrls):*

| Field   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: NotificationsAllowedForUrls                                          |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/NotificationsAllowedForUrls`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com"/>`<br>For multiple list items: `<data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com;[*.]contoso.edu"/>`                               |
-->
*<span data-ttu-id="04c3a-269">[RestoreOnStartupURLS](https://docs.microsoft.com/deployedge/microsoft-edge-policies#RestoreOnStartupURLS):</span><span class="sxs-lookup"><span data-stu-id="04c3a-269">[RestoreOnStartupURLS](https://docs.microsoft.com/deployedge/microsoft-edge-policies#RestoreOnStartupURLS):</span></span>*

| <span data-ttu-id="04c3a-270">Champ</span><span class="sxs-lookup"><span data-stu-id="04c3a-270">Field</span></span>   | <span data-ttu-id="04c3a-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-271">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04c3a-272">Nom</span><span class="sxs-lookup"><span data-stu-id="04c3a-272">Name</span></span>    | <span data-ttu-id="04c3a-273">Microsoft Edge: RestoreOnStartupURLS</span><span class="sxs-lookup"><span data-stu-id="04c3a-273">Microsoft Edge: RestoreOnStartupURLS</span></span>                                                 |
| <span data-ttu-id="04c3a-274">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-274">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/RestoreOnStartupURLs`    |
| <span data-ttu-id="04c3a-275">Type</span><span class="sxs-lookup"><span data-stu-id="04c3a-275">Type</span></span>    | <span data-ttu-id="04c3a-276">Chaîne</span><span class="sxs-lookup"><span data-stu-id="04c3a-276">String</span></span>                                                                               |
| <span data-ttu-id="04c3a-277">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-277">Value</span></span>   | `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com"/>`<br><span data-ttu-id="04c3a-278">Pour les éléments de listes multiples:</span><span class="sxs-lookup"><span data-stu-id="04c3a-278">For multiple list items:</span></span> `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com&#xF000;2&#xF000;http://www.microsoft.com"/>`  |

*<span data-ttu-id="04c3a-279">[ExtensionInstallForcelist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ExtensionInstallForcelist):</span><span class="sxs-lookup"><span data-stu-id="04c3a-279">[ExtensionInstallForcelist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ExtensionInstallForcelist):</span></span>*

| <span data-ttu-id="04c3a-280">Champ</span><span class="sxs-lookup"><span data-stu-id="04c3a-280">Field</span></span>   | <span data-ttu-id="04c3a-281">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-281">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04c3a-282">Nom</span><span class="sxs-lookup"><span data-stu-id="04c3a-282">Name</span></span>    | <span data-ttu-id="04c3a-283">Microsoft Edge: ExtensionInstallForcelist</span><span class="sxs-lookup"><span data-stu-id="04c3a-283">Microsoft Edge: ExtensionInstallForcelist</span></span>                                            |
| <span data-ttu-id="04c3a-284">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-284">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`    |
| <span data-ttu-id="04c3a-285">Type</span><span class="sxs-lookup"><span data-stu-id="04c3a-285">Type</span></span>    | <span data-ttu-id="04c3a-286">Chaîne</span><span class="sxs-lookup"><span data-stu-id="04c3a-286">String</span></span>                                                                               |
| <span data-ttu-id="04c3a-287">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-287">Value</span></span>   | `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000;gbchcmhmhahfdphkhkmpfmihenigjmpp;https://extensionwebstorebase.edgesv.net/v1/crx"/>`                               |

#### <span data-ttu-id="04c3a-288">Exemple de données de type dictionnaire et chaîne</span><span class="sxs-lookup"><span data-stu-id="04c3a-288">Dictionary and String data type example</span></span>

*<span data-ttu-id="04c3a-289">[ProxyMode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ProxyMode):</span><span class="sxs-lookup"><span data-stu-id="04c3a-289">[ProxyMode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ProxyMode):</span></span>*

| <span data-ttu-id="04c3a-290">Champ</span><span class="sxs-lookup"><span data-stu-id="04c3a-290">Field</span></span>   | <span data-ttu-id="04c3a-291">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-291">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04c3a-292">Nom</span><span class="sxs-lookup"><span data-stu-id="04c3a-292">Name</span></span>    | <span data-ttu-id="04c3a-293">Microsoft Edge: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="04c3a-293">Microsoft Edge: ProxyMode</span></span>                                                            |
| <span data-ttu-id="04c3a-294">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="04c3a-294">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ProxyMode/ProxyMode`  |
| <span data-ttu-id="04c3a-295">Type</span><span class="sxs-lookup"><span data-stu-id="04c3a-295">Type</span></span>    | <span data-ttu-id="04c3a-296">Chaîne</span><span class="sxs-lookup"><span data-stu-id="04c3a-296">String</span></span>                                                                               |
| <span data-ttu-id="04c3a-297">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c3a-297">Value</span></span>   | `<enabled/><data id="ProxyMode" value="auto_detect"/>`                               |

## <span data-ttu-id="04c3a-298">Configurer MicrosoftEdge dans Intune à l’aide de l’ingestion ADMX</span><span class="sxs-lookup"><span data-stu-id="04c3a-298">Configure Microsoft Edge in Intune using ADMX ingestion</span></span>

<span data-ttu-id="04c3a-299">La méthode recommandée pour configurer MicrosoftEdge avec MicrosoftIntune consiste à utiliser le profil de modèles d’administration comme décrit dans [Configurer les paramètres de stratégie MicrosoftEdge avec MicrosoftIntune](https://docs.microsoft.com/deployedge/configure-edge-with-intune).</span><span class="sxs-lookup"><span data-stu-id="04c3a-299">The recommended way to configure Microsoft Edge with Microsoft Intune is to use the Administrative Templates profile as described in [Configure Microsoft Edge policy settings with Microsoft Intune](https://docs.microsoft.com/deployedge/configure-edge-with-intune).</span></span> <span data-ttu-id="04c3a-300">Si vous souhaitez évaluer une stratégie qui n’est actuellement pas disponible dans les modèles d’administration MicrosoftEdge dans Intune, vous pouvez configurer MicrosoftEdge avec des [paramètres personnalisés pour les appareils Windows10 dans Intune](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10).</span><span class="sxs-lookup"><span data-stu-id="04c3a-300">If you want to evaluate a policy that is currently not available in the Microsoft Edge Administrative Templates in Intune you can configure Microsoft Edge using  [custom settings for Windows 10 devices in Intune](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10).</span></span>

<span data-ttu-id="04c3a-301">Cette section décrit comment fournir des ressources de multiplexage aux pilotes clients.</span><span class="sxs-lookup"><span data-stu-id="04c3a-301">This section describes how to:</span></span>

1. [<span data-ttu-id="04c3a-302">Ingérer le fichier ADMX MicrosoftEdge dans Intune</span><span class="sxs-lookup"><span data-stu-id="04c3a-302">Ingest the Microsoft Edge ADMX file into Intune</span></span>](#ingest-the-microsoft-edge-admx-file-into-intune)
2. [<span data-ttu-id="04c3a-303">Définir une stratégie à l’aide d’un OMA-URI personnalisé dans Intune</span><span class="sxs-lookup"><span data-stu-id="04c3a-303">Set a policy using custom OMA-URI in Intune</span></span>](#set-a-policy-using-custom-oma-uri-in-intune)

> [!IMPORTANT]
> <span data-ttu-id="04c3a-304">Il est recommandé d’utiliser un profil OMA-URI personnalisé et un profil de modèles d’administration pour configurer le même paramètre MicrosoftEdge dans Intune.</span><span class="sxs-lookup"><span data-stu-id="04c3a-304">As a best practice, don’t use a custom OMA-URI profile and an Administration templates profile to configure the same Microsoft Edge setting in Intune.</span></span> <span data-ttu-id="04c3a-305">Si vous déployez la même stratégie à l’aide d’un OMA-URI personnalisé et d’un profil de modèle d’administration, mais avec des valeurs différentes, les utilisateurs obtiendront des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="04c3a-305">If you deploy the same policy using both a custom OMA-URI  and an Administrative template profile, but with different values, users will get unpredictable results.</span></span> <span data-ttu-id="04c3a-306">Nous vous recommandons vivement de supprimer votre profil OMA-URI avant d’utiliser un profil de modèles d’administration.</span><span class="sxs-lookup"><span data-stu-id="04c3a-306">We strongly recommend removing your OMA-URI profile before using an Administration templates profile.</span></span>

### <span data-ttu-id="04c3a-307">Ingérer le fichier ADMX MicrosoftEdge dans Intune</span><span class="sxs-lookup"><span data-stu-id="04c3a-307">Ingest the Microsoft Edge ADMX file into Intune</span></span>

<span data-ttu-id="04c3a-308">Cette section décrit la procédure d’ingestion du modèle d’administration MicrosoftEdge (**fichier msedge.admx**) dans Intune.</span><span class="sxs-lookup"><span data-stu-id="04c3a-308">This section describes how to ingest the Microsoft Edge administrative template (**msedge.admx** file) into Intune.</span></span>

> [!WARNING]
> <span data-ttu-id="04c3a-309">Ne modifiez pas le fichier ADMX avant d’ingérer le fichier.</span><span class="sxs-lookup"><span data-stu-id="04c3a-309">Don't modify the ADMX file before ingesting the file.</span></span>

<span data-ttu-id="04c3a-310">Pour ingérer le fichier ADMX, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="04c3a-310">To ingest the ADMX file, follow these steps:</span></span>

1. <span data-ttu-id="04c3a-311">Téléchargez le fichier de modèles de stratégie MicrosoftEdge (MicrosoftEdgePolicyTemplates.cab) à partir de [la page d’accueil de MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise) et extrayez le contenu.</span><span class="sxs-lookup"><span data-stu-id="04c3a-311">Download the Microsoft Edge policy templates file (MicrosoftEdgePolicyTemplates.cab) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise) and extract the contents.</span></span> <span data-ttu-id="04c3a-312">Le fichier que vous souhaitez ingérer est **msedge.admx**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-312">The file that you want to ingest is **msedge.admx**.</span></span>
2. <span data-ttu-id="04c3a-313">Connectez-vous au [portail MicrosoftAzure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="04c3a-313">Sign in to the [Microsoft Azure portal](https://portal.azure.com).</span></span>
3. <span data-ttu-id="04c3a-314">Sélectionnez **Intune** dans _Tous les services_ ou recherchez Intune dans la zone de recherche du portail.</span><span class="sxs-lookup"><span data-stu-id="04c3a-314">Select **Intune** from _All Services_, or search for Intune in the portal search box.</span></span>
4. <span data-ttu-id="04c3a-315">Dans _MicrosoftIntune - Vue d’ensemble_, sélectionnez **Configuration du périphérique** | **Profils**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-315">From _Microsoft Intune - Overview_, select **Device configuration** | **Profiles**.</span></span>
5. <span data-ttu-id="04c3a-316">Dans la barre de commandes supérieure, sélectionnez **+ Créer profil**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-316">On the top command bar, select **+ Create profile**.</span></span>

   ![Créer un profil d’appareil](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile.png)

6. <span data-ttu-id="04c3a-318">Fournissez les informations de profil suivantes:</span><span class="sxs-lookup"><span data-stu-id="04c3a-318">Provide the following profile information:</span></span>

   - <span data-ttu-id="04c3a-319">**Nom**: entrez un nom descriptif.</span><span class="sxs-lookup"><span data-stu-id="04c3a-319">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="04c3a-320">Pour cet exemple, « Configuration ingérée MicrosoftEdge».</span><span class="sxs-lookup"><span data-stu-id="04c3a-320">For this example, "Microsoft Edge ADMX ingested configuration".</span></span>
   - <span data-ttu-id="04c3a-321">**Description**: entrez une description facultative du profil.</span><span class="sxs-lookup"><span data-stu-id="04c3a-321">**Description**: Enter an optional description for the profile.</span></span>
   - <span data-ttu-id="04c3a-322">**Plateforme**: sélectionnez «Windows10 et versions ultérieures»</span><span class="sxs-lookup"><span data-stu-id="04c3a-322">**Platform**: Select "Windows 10 and later"</span></span>
   - <span data-ttu-id="04c3a-323">**Type de profil**: sélectionnez «Personnalisé»</span><span class="sxs-lookup"><span data-stu-id="04c3a-323">**Profile type**: Select "Custom"</span></span>

7. <span data-ttu-id="04c3a-324">Sur **Paramètres OMA-URI personnalisés**, cliquez sur **Ajouter** pour ajouter une ingestion ADMX.</span><span class="sxs-lookup"><span data-stu-id="04c3a-324">On **Custom OMA-URI Settings**, click **Add** to add an ADMX ingestion.</span></span>

   ![Ajouter l’ingestion pour OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-add-omauri.png)

8. <span data-ttu-id="04c3a-326">Sur **Ajouter une ligne**, indiquez les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="04c3a-326">On **Add Row**, provide the following information:</span></span>

   - <span data-ttu-id="04c3a-327">**Nom**: entrez un nom descriptif.</span><span class="sxs-lookup"><span data-stu-id="04c3a-327">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="04c3a-328">Pour cet exemple, utilisez «IngestionADMX MicrosoftEdge».</span><span class="sxs-lookup"><span data-stu-id="04c3a-328">For this example, use "Microsoft Edge ADMX ingestion".</span></span>
   - <span data-ttu-id="04c3a-329">**Description**: entrez une description facultative du paramètre.</span><span class="sxs-lookup"><span data-stu-id="04c3a-329">**Description**: Enter an optional description for the setting.</span></span>
   - <span data-ttu-id="04c3a-330">**OMA-URI**: entrez «*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*»</span><span class="sxs-lookup"><span data-stu-id="04c3a-330">**OMA-URI**: Enter "*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"</span></span>
   - <span data-ttu-id="04c3a-331">**Type de données**: sélectionnez «chaîne».</span><span class="sxs-lookup"><span data-stu-id="04c3a-331">**Data type**: Select "String"</span></span>
   - <span data-ttu-id="04c3a-332">**Valeur**: cette zone d’entrée s’affiche une fois que vous avez sélectionné le **Type de données**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-332">**Value**: This input area appears after you select the **Data type**.</span></span> <span data-ttu-id="04c3a-333">Ouvrez le fichier msedge.admx à partir du fichier de modèles de stratégie MicrosoftEdge que vous avez extrait à l’étape1.</span><span class="sxs-lookup"><span data-stu-id="04c3a-333">Open the msedge.admx file from the Microsoft Edge policy templates file you extracted in step 1.</span></span> <span data-ttu-id="04c3a-334">Copiez **TOUT le texte** du fichier msedge.admx et collez-le dans la zone de texte **Valeur** illustrée dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="04c3a-334">Copy **ALL the text** from the msedge.admx file and paste it in the **Value** text area shown in the following screenshot.</span></span>

        ![Ajouter une ingestion ADMX](./media/edge-cfg-with-mdm/configure-edge-intune-mdm-omauri-addrow-ingest.png)

   - <span data-ttu-id="04c3a-336">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-336">Click **OK**.</span></span>

9. <span data-ttu-id="04c3a-337">Sous **Paramètres OMA-URI personnalisés**, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-337">On **Custom OMA-URI Settings**, click **OK**.</span></span>
10. <span data-ttu-id="04c3a-338">Sur **Créer un profil**, cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-338">On **Create profile**, click **Create**.</span></span> <span data-ttu-id="04c3a-339">La capture d’écran suivante présente des informations sur le profil nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="04c3a-339">The next screenshot shows information about the newly created profile.</span></span>

    ![<span data-ttu-id="04c3a-340">Informations sur le nouveau profil de périphérique</span><span class="sxs-lookup"><span data-stu-id="04c3a-340">New device profile information</span></span> ](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-done.png)

<!--
> [!NOTE]
> You can use the preceding steps to ingest the msedgeupate.admx policy template file.
-->
### <span data-ttu-id="04c3a-341">Définir une stratégie à l’aide d’un OMA-URI personnalisé dans Intune</span><span class="sxs-lookup"><span data-stu-id="04c3a-341">Set a policy using custom OMA-URI in Intune</span></span>

> [!NOTE]
> <span data-ttu-id="04c3a-342">Avant d’utiliser les étapes de cette section, vous devez appliquer les étapes présentées dans [Ingérer le fichier ADMX MicrosoftEdge dans Intune](#ingest-the-microsoft-edge-admx-file-into-intune).</span><span class="sxs-lookup"><span data-stu-id="04c3a-342">Before using the steps in this section you must complete the steps described in [Ingest the Microsoft Edge ADMX file into Intune](#ingest-the-microsoft-edge-admx-file-into-intune).</span></span>

1. <span data-ttu-id="04c3a-343">Connectez-vous au [portail MicrosoftAzure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="04c3a-343">Sign in to the [Microsoft Azure portal](https://portal.azure.com).</span></span>
2. <span data-ttu-id="04c3a-344">Sélectionnez **Intune** dans _Tous les services_ ou recherchez Intune dans la zone de recherche du portail.</span><span class="sxs-lookup"><span data-stu-id="04c3a-344">Select **Intune** from _All Services_, or search for Intune in the portal search box.</span></span>
3. <span data-ttu-id="04c3a-345">Accédez à **Intune**>**Configuration du périphérique**>**Profils**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-345">Go to **Intune**>**Device configuration**>**Profiles**.</span></span>
4. <span data-ttu-id="04c3a-346">Sélectionnez le profil «Configuration ingérée de MicrosoftEdge ADMX» ou le nom que vous avez utilisé pour le profil.</span><span class="sxs-lookup"><span data-stu-id="04c3a-346">Select the "Microsoft Edge ADMX ingested configuration" profile or the name you used for the profile.</span></span>
5. <span data-ttu-id="04c3a-347">Pour ajouter des paramètres de stratégie MicrosoftEdge, vous devez ouvrir **Paramètres OMA-URI personnalisés**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-347">To add Microsoft Edge policy settings, you have to open **Custom OMA-URI Settings**.</span></span> <span data-ttu-id="04c3a-348">Sous **Gérer**, cliquez sur **Propriétés**, puis sur **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-348">Under **Manage**, click **Properties**, and then click **Settings**.</span></span>

    ![Configurer les paramètres de profil](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings.png)

6. <span data-ttu-id="04c3a-350">Sur **Paramètres OMA-URI personnalisés**, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-350">On **Custom OMA-URI Settings**, click **Add**.</span></span>

    ![Ajouter une ligne aux paramètres OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings-add-row.png)

7. <span data-ttu-id="04c3a-352">Sur **Ajouter une ligne**, indiquez les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="04c3a-352">On **Add Row**, provide the following information:</span></span>

   - <span data-ttu-id="04c3a-353">**Nom**: entrez un nom descriptif.</span><span class="sxs-lookup"><span data-stu-id="04c3a-353">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="04c3a-354">Nous vous suggérons d’utiliser le nom de stratégie que vous souhaitez configurer.</span><span class="sxs-lookup"><span data-stu-id="04c3a-354">We suggest using the policy name you want to configure.</span></span> <span data-ttu-id="04c3a-355">Pour cet exemple, utilisez «ShowHomeButton».</span><span class="sxs-lookup"><span data-stu-id="04c3a-355">For this example, use "ShowHomeButton".</span></span>
   - <span data-ttu-id="04c3a-356">**Description** (facultatif): entrez une description du paramètre.</span><span class="sxs-lookup"><span data-stu-id="04c3a-356">**Description** (Optional): Enter a description for the setting.</span></span>
   - <span data-ttu-id="04c3a-357">**OMA-URI**: entrez l’OMA-URI pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="04c3a-357">**OMA-URI**: Enter the OMA-URI for the policy.</span></span> <span data-ttu-id="04c3a-358">En prenant la stratégie «ShowHomeButton» comme exemple, utilisez la chaîne suivante: «*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*»</span><span class="sxs-lookup"><span data-stu-id="04c3a-358">Using the for "ShowHomeButton" policy as an example, use this string: "*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"</span></span>
   - <span data-ttu-id="04c3a-359">**Type de données**: sélectionnez le type de données des paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="04c3a-359">**Data type**: Select the policy settings data type.</span></span> <span data-ttu-id="04c3a-360">Pour la stratégie «ShowHomeButton», utilisez «chaîne».</span><span class="sxs-lookup"><span data-stu-id="04c3a-360">For the "ShowHomeButton" policy, use "String"</span></span>
   - <span data-ttu-id="04c3a-361">**Valeur**: entrez le paramètre que vous souhaitez configurer pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="04c3a-361">**Value**: Enter the setting that you want to configure for the policy.</span></span> <span data-ttu-id="04c3a-362">Pour l’exemple «ShowHomeButton», entrez «\<enabled/>».</span><span class="sxs-lookup"><span data-stu-id="04c3a-362">For "ShowHomeButton" example, enter "\<enabled/>".</span></span> <span data-ttu-id="04c3a-363">La capture d’écran suivante présente les paramètres de configuration d’une stratégie.</span><span class="sxs-lookup"><span data-stu-id="04c3a-363">The following screenshot shows the settings for configuring a policy.</span></span>

        ![Ajouter une ligne, Paramètres OMA-URI personnalisés](./media/edge-cfg-with-mdm/configure-edge-mdm-custom-omauri-setting.png)

   - <span data-ttu-id="04c3a-365">Cliquez sur**OK**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-365">Click **OK**.</span></span>

8. <span data-ttu-id="04c3a-366">Sous **Paramètres OMA-URI personnalisés**, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-366">On **Custom OMA-URI Settings**, click **OK**.</span></span>
9. <span data-ttu-id="04c3a-367">Dans le profil «**Configuration ingérée de MicrosoftEdge ADMX - Propriétés**» (ou le nom que vous avez utilisé), cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="04c3a-367">On the "**Microsoft Edge ADMX ingested configuration - Properties**" profile (or the name you used), click **Save**.</span></span>

<span data-ttu-id="04c3a-368">Une fois le profil créé et les propriétés définies, vous devez [attribuer le profil dans MicrosoftIntune](https://docs.microsoft.com/intune/configuration/device-profile-assign).</span><span class="sxs-lookup"><span data-stu-id="04c3a-368">After the profile is created and the properties set, you have to [assign the profile in Microsoft Intune](https://docs.microsoft.com/intune/configuration/device-profile-assign).</span></span>

#### <span data-ttu-id="04c3a-369">Vérifiez que la stratégie a été créée.</span><span class="sxs-lookup"><span data-stu-id="04c3a-369">Confirm that the policy was set</span></span>

<span data-ttu-id="04c3a-370">Procédez comme suit pour confirmer que la stratégie MicrosoftEdge utilise le profil que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="04c3a-370">Use the following steps to confirm that the Microsoft Edge policy is using the profile you created.</span></span> <span data-ttu-id="04c3a-371">(Laissez à MicrosoftIntune le temps de propager la stratégie sur un périphérique que vous avez attribué dans l’exemple de profil «Configuration ingérée de MicrosoftEdge ADMX».)</span><span class="sxs-lookup"><span data-stu-id="04c3a-371">(Give Microsoft Intune time to propagate the policy to a device you assigned in the "Microsoft Edge ADMX ingested configuration" profile example.)</span></span>

1. <span data-ttu-id="04c3a-372">Ouvrez MicrosoftEdge et accédez à *edge://policy*.</span><span class="sxs-lookup"><span data-stu-id="04c3a-372">Open Microsoft Edge and go to *edge://policy*.</span></span>
2. <span data-ttu-id="04c3a-373">Sur la page **Stratégies**, vérifiez si la stratégie que vous avez définie dans le profil est répertoriée.</span><span class="sxs-lookup"><span data-stu-id="04c3a-373">On the **Policies** page, see if the policy you set in the profile is listed.</span></span>
3. <span data-ttu-id="04c3a-374">Si ce n’est pas le cas, consultez [Diagnostiquer les échecs GPM dans Windows10](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) ou [Résoudre les problèmes liés à un paramètre de stratégie](#troubleshoot-a-policy-setting).</span><span class="sxs-lookup"><span data-stu-id="04c3a-374">If your policy isn't shown, see [Diagnose MDM failures in Windows 10](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) or [Troubleshoot a policy setting](#troubleshoot-a-policy-setting).</span></span>

#### <span data-ttu-id="04c3a-375">Résoudre les problèmes liés à un paramètre de stratégie</span><span class="sxs-lookup"><span data-stu-id="04c3a-375">Troubleshoot a policy setting</span></span>

<span data-ttu-id="04c3a-376">Si une stratégie MicrosoftEdge ne prend pas effet, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="04c3a-376">If a Microsoft Edge policy isn’t taking effect, try the following steps:</span></span>

<span data-ttu-id="04c3a-377">Ouvrez la page *edge://policy* sur le périphérique cible (un périphérique auquel vous avez affecté le profil dans MicrosoftIntune) et recherchez la stratégie.</span><span class="sxs-lookup"><span data-stu-id="04c3a-377">Open the *edge://policy* page on the target device (a device you assigned the profile to in Microsoft Intune) and search for the policy.</span></span> <span data-ttu-id="04c3a-378">Si la stratégie ne figure pas sur la page *edge://policy*, essayez ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="04c3a-378">If the policy isn’t on the *edge://policy* page, try the following:</span></span>

- <span data-ttu-id="04c3a-379">Vérifiez que la stratégie est bien dans le registre et qu’elle est correcte.</span><span class="sxs-lookup"><span data-stu-id="04c3a-379">Check that the policy is in the registry and is correct.</span></span> <span data-ttu-id="04c3a-380">Sur le périphérique cible, ouvrez l’Éditeur du Registre Windows10 (**touche Windows +r**, entrez «*regedit*», puis appuyez sur **Entrée**.) Vérifiez que la stratégie est correctement définie dans le chemin d’accès *\Software\Policies\ Microsoft\Edge*.</span><span class="sxs-lookup"><span data-stu-id="04c3a-380">On the target device open the Windows 10 Registry Editor (**Windows key + r**, enter “*regedit*” and then press **Enter**.) Check that the policy is correctly defined in the *\Software\Policies\ Microsoft\Edge* path.</span></span> <span data-ttu-id="04c3a-381">Si vous ne trouvez pas la stratégie dans le chemin d’accès attendu, cela signifie qu’elle n’a pas été envoyée correctement au périphérique.</span><span class="sxs-lookup"><span data-stu-id="04c3a-381">If you don’t find the policy in the expected path, then the policy wasn’t pushed to the device correctly.</span></span>
- <span data-ttu-id="04c3a-382">Vérifiez que le chemin d’accès OMA-URI est correct et que la valeur est une chaîne XML valide.</span><span class="sxs-lookup"><span data-stu-id="04c3a-382">Check that the OMA-URI path is correct, and the value is a valid XML string.</span></span> <span data-ttu-id="04c3a-383">Si l’une de ces conditions est incorrecte, la stratégie ne sera pas envoyée vers l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="04c3a-383">If either of these are incorrect the policy won’t be pushed to the target device.</span></span>

<span data-ttu-id="04c3a-384">Pour plus de conseils sur la résolution de problèmes, consultez [Installer MicrosoftIntune](https://docs.microsoft.com/intune/fundamentals/setup-steps) et [Synchroniser les périphériques](https://docs.microsoft.com/intune/remote-actions/device-sync).</span><span class="sxs-lookup"><span data-stu-id="04c3a-384">For more trouble shooting tips, see [Set up Microsoft Intune](https://docs.microsoft.com/intune/fundamentals/setup-steps) and [Sync devices](https://docs.microsoft.com/intune/remote-actions/device-sync).</span></span>

## <span data-ttu-id="04c3a-385">Articles associés</span><span class="sxs-lookup"><span data-stu-id="04c3a-385">See also</span></span>

- [<span data-ttu-id="04c3a-386">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="04c3a-386">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="04c3a-387">Configurer les paramètres de stratégie MicrosoftEdge avec MicrosoftIntune</span><span class="sxs-lookup"><span data-stu-id="04c3a-387">Configure Microsoft Edge policy settings with Microsoft Intune</span></span>](configure-edge-with-intune.md)
- [<span data-ttu-id="04c3a-388">Gestion des périphériques mobiles</span><span class="sxs-lookup"><span data-stu-id="04c3a-388">Mobile device management</span></span>](https://docs.microsoft.com/windows/client-management/mdm/)
- [<span data-ttu-id="04c3a-389">Utiliser les paramètres personnalisés pour les appareils Windows10 dans Intune</span><span class="sxs-lookup"><span data-stu-id="04c3a-389">Use custom settings for Windows 10 devices in Intune</span></span>](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10)
- [<span data-ttu-id="04c3a-390">Configuration de stratégie d’applications Win32 et Pont du bureau</span><span class="sxs-lookup"><span data-stu-id="04c3a-390">Win32 and Desktop Bridge app policy configuration</span></span>](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)
- [<span data-ttu-id="04c3a-391">Fonctionnement des stratégies ADMX</span><span class="sxs-lookup"><span data-stu-id="04c3a-391">Understanding ADMX-backed policies</span></span>](https://docs.microsoft.com/windows/client-management/mdm/understanding-admx-backed-policies)
