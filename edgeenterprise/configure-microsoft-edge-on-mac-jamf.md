---
title: Configurer les stratégies MicrosoftEdge sur macOS grâce à Jamf
ms.author: brianalt
author: dan-wesley
manager: laurawi
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer les paramètres de stratégie MicrosoftEdge sur les appareils Mac grâce à Jamf
ms.openlocfilehash: 336bdfed2c53811615b0183dc5ca7db916cd7428
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979668"
---
# <span data-ttu-id="2508f-103">Configurer les paramètres de stratégie MicrosoftEdge sur macOS grâce à Jamf</span><span class="sxs-lookup"><span data-stu-id="2508f-103">Configure Microsoft Edge policy settings on macOS with Jamf</span></span>

<span data-ttu-id="2508f-104">Cet article explique la configuration de paramètres de stratégie sur macOS à l’aide d’un fichier de manifeste de stratégie Microsoft Edge sur Jamf Pro10.19.</span><span class="sxs-lookup"><span data-stu-id="2508f-104">This article describes how to configure policy settings on macOS using a Microsoft Edge policy manifest file on Jamf Pro 10.19.</span></span>

<span data-ttu-id="2508f-105">Vous pouvez également configurer les paramètres de stratégies MicrosoftEdge sur macOS à l’aide d’un fichier de liste de propriétés (.plist).</span><span class="sxs-lookup"><span data-stu-id="2508f-105">You can also configure Microsoft Edge policy settings on macOS by using a property list (.plist) file.</span></span> <span data-ttu-id="2508f-106">Pour plus d’informations, voir [Configuration pour macOS à l’aide d’un fichier .plist](configure-microsoft-edge-on-mac.md).</span><span class="sxs-lookup"><span data-stu-id="2508f-106">For more information, see [Configure for macOS using a .plist](configure-microsoft-edge-on-mac.md)</span></span>


## <span data-ttu-id="2508f-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="2508f-107">Prerequisites</span></span>

<span data-ttu-id="2508f-108">Le logiciel suivant est nécessaire:</span><span class="sxs-lookup"><span data-stu-id="2508f-108">The following software is required:</span></span>

- <span data-ttu-id="2508f-109">Microsoft Edge Stable canal8.1</span><span class="sxs-lookup"><span data-stu-id="2508f-109">Microsoft Edge Stable channel 81</span></span>
- <span data-ttu-id="2508f-110">Fichier de modèles de stratégie, version81.0.416.3</span><span class="sxs-lookup"><span data-stu-id="2508f-110">Policy Templates file, version 81.0.416.3</span></span>
- <span data-ttu-id="2508f-111">Jamf Pro version10.19</span><span class="sxs-lookup"><span data-stu-id="2508f-111">Jamf Pro, Version 10.19</span></span>

## <span data-ttu-id="2508f-112">À propos de l’application Jamf Pro & du menu Paramètres personnalisés</span><span class="sxs-lookup"><span data-stu-id="2508f-112">About the Jamf Pro Application & Custom Settings menu</span></span>

<span data-ttu-id="2508f-113">Avant la publication de Jamf Pro10.18, la gestion d’Office365 impliquait la création manuelle d’un fichier .plist.</span><span class="sxs-lookup"><span data-stu-id="2508f-113">Before Jamf Pro 10.18, managing Office 365 involved manually building a .plist file.</span></span> <span data-ttu-id="2508f-114">Le flux de travail était fastidieux et nécessitait une solide formation technique.</span><span class="sxs-lookup"><span data-stu-id="2508f-114">This was a time-consuming workflow that required a strong technical background.</span></span> <span data-ttu-id="2508f-115">Jamf Pro10.18 éliminait ces obstacles en rationalisant le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="2508f-115">Jamf Pro 10.18 eliminated those barriers by streamlining the configuration process.</span></span> <span data-ttu-id="2508f-116">Cependant, les administrateurs informatiques pouvaient seulement utiliser cette nouvelle interface utilisateur pour des applications spécifiques et des domaines de préférence spécifiés par Jamf.</span><span class="sxs-lookup"><span data-stu-id="2508f-116">However, IT Admins could only use this new user interface for specific applications and preference domains specified by Jamf.</span></span>

<span data-ttu-id="2508f-117">Avec Jamf Pro10.19, un utilisateur peut télécharger un manifeste JSON en tant que «schéma personnalisé» pour cibler tout domaine de préférence, et l’interface utilisateur graphique est générée à partir de ce manifeste.</span><span class="sxs-lookup"><span data-stu-id="2508f-117">In Jamf Pro 10.19, a user can upload a JSON manifest as a "custom schema" to target any preference domain, and the graphical user interface will be generated from this manifest.</span></span> <span data-ttu-id="2508f-118">Le schéma personnalisé créé respecte la spécification de schéma JSON.</span><span class="sxs-lookup"><span data-stu-id="2508f-118">The custom schema that's created follows the JSON Schema specification.</span></span>

<span data-ttu-id="2508f-119">Pour plus d’informations, voir [Profils de configuration d’ordinateur](https://jamf.it/computer-configuration-profiles) dans le Guide de l’administrateur Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="2508f-119">For more information, see [Computer Configuration Profiles](https://jamf.it/computer-configuration-profiles) in the Jamf Pro Administrator's Guide.</span></span>

## <span data-ttu-id="2508f-120">Obtenir le manifeste de stratégie pour une version spécifique de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2508f-120">Get the policy manifest for a specific version of Microsoft Edge</span></span>

<span data-ttu-id="2508f-121">Pour obtenir le manifeste de stratégie:</span><span class="sxs-lookup"><span data-stu-id="2508f-121">To get the policy manifest:</span></span>

- <span data-ttu-id="2508f-122">Accédez à la [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="2508f-122">Go to the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="2508f-123">Dans la liste déroulante Canal/Version, sélectionnez \*\*tout canal avec la version 81 ou ultérieure.\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="2508f-123">On the Channel/Version dropdown list, select \*\*any channel with version 81 or later.\*\*\*.</span></span>
- <span data-ttu-id="2508f-124">Dans la liste déroulante Build, sélectionnez toute \*\*version 81 ou ultérieure.\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="2508f-124">On the Build dropdown list, select any \*\*81 build or later.\*\*\*.</span></span>
- <span data-ttu-id="2508f-125">Cliquez sur OBTENIR DES FICHIERS DE STRATÉGIE pour télécharger notre ensemble de modèles de stratégie.</span><span class="sxs-lookup"><span data-stu-id="2508f-125">Click GET POLICY FILES to download our policy templates bundle.</span></span>

  > [!NOTE]
  > <span data-ttu-id="2508f-126">L'ensemble de modèles de stratégie est signé en tant que fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="2508f-126">Currently, the policy templates bundle is signed as a CAB file.</span></span> <span data-ttu-id="2508f-127">Vous devez utiliser un outil tiers, tel que Unarchiver, pour ouvrir le fichier sur macOS.</span><span class="sxs-lookup"><span data-stu-id="2508f-127">You'll need to use a 3rd party tool, such as The Unarchiver to open the file on macOS.</span></span>

<span data-ttu-id="2508f-128">Une fois le fichier CAB décompressé, décompressez le fichier ZIP et accédez au répertoire «mac» de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="2508f-128">After you unpack the CAB file, unpack the ZIP file and navigate to the "mac" top level directory.</span></span> <span data-ttu-id="2508f-129">Le manifeste appelé «policy_manifest.json» figure dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="2508f-129">The manifest, which is named "policy_manifest.json", is in this directory.</span></span>

<span data-ttu-id="2508f-130">Ce manifeste est publié dans chaque ensemble de stratégies à compter de la build81.0.416.3.</span><span class="sxs-lookup"><span data-stu-id="2508f-130">This manifest will be published in every policy bundle starting with build 81.0.416.3.</span></span> <span data-ttu-id="2508f-131">Si vous souhaitez tester des stratégies dans le canal de développement, vous pouvez prendre le manifeste associé à chaque publication de développement et le tester dans Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="2508f-131">If you want to test policies in the Dev channel, you can take the manifest associated with each Dev release and test it in Jamf Pro.</span></span>  

## <span data-ttu-id="2508f-132">Utilisation du manifeste de stratégie dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="2508f-132">Use the policy manifest in Jamf Pro</span></span>

<span data-ttu-id="2508f-133">Utilisez la procédure suivante pour télécharger le manifeste de stratégie dans Jamf Pro et créer un profil de stratégie pour macOS.</span><span class="sxs-lookup"><span data-stu-id="2508f-133">Use the following steps to upload the policy manifest to Jamf Pro and then create a policy profile for macOS.</span></span>

1. <span data-ttu-id="2508f-134">Connectez-vous à Jamf.</span><span class="sxs-lookup"><span data-stu-id="2508f-134">Sign in to Jamf.</span></span>
2. <span data-ttu-id="2508f-135">Sélectionnez l'onglet **Ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="2508f-135">Select the **Computer** tab.</span></span>
3. <span data-ttu-id="2508f-136">Sous **Gestion de contenu**, sélectionnez **Profils de configuration**.</span><span class="sxs-lookup"><span data-stu-id="2508f-136">Under **Content Management**, select **Configuration Profiles**.</span></span>
4. <span data-ttu-id="2508f-137">Sur la page **Profils de configuration**, cliquez sur **+ Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="2508f-137">On the **Configuration Profiles** page, click **+ New**.</span></span>

   ![Ajout d'un nouveau profil dans Jamf](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles.png)

5. <span data-ttu-id="2508f-139">Sur **Nouveau profil de configuration macOS**>**Options**, sélectionnez **Application & paramètres personnalisés**.</span><span class="sxs-lookup"><span data-stu-id="2508f-139">On **New macOS Configuration Profile**>**Options**, select **Application & Custom Settings**.</span></span>
6. <span data-ttu-id="2508f-140">Dans la fenêtre contextuelle **Application & paramètres personnalisés**, cliquez sur **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="2508f-140">On the **Application & Custom Settings** popup window, click **Configure**.</span></span>

   ![Configurer les Application et paramètres personnalisés](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom.png)

7. <span data-ttu-id="2508f-142">Dans la section **Application & paramètres personnalisés**, configurez les valeurs affichées dans la capture d’écran ci-après.</span><span class="sxs-lookup"><span data-stu-id="2508f-142">In the **Application & Custom Settings** section, set the values shown in the following screen shot.</span></span>

   ![Source du profil et schéma personnalisé](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-schema.png)

   - <span data-ttu-id="2508f-144">Pour la **Méthode de création**, sélectionnez **Configurer les paramètres**.</span><span class="sxs-lookup"><span data-stu-id="2508f-144">For **Creation Method**, pick **Configure settings**.</span></span>
   - <span data-ttu-id="2508f-145">Pour la **Source**, sélectionnez **Schéma personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="2508f-145">For **Source**, pick **Custom Schema**.</span></span>
   - <span data-ttu-id="2508f-146">Pour le **Domaine de préférence**, indiquez votre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="2508f-146">For **Preference Domain**, provide the name of your domain.</span></span> <span data-ttu-id="2508f-147">Cet exemple utilise *com.microsoft.Edge* en tant que domaine.</span><span class="sxs-lookup"><span data-stu-id="2508f-147">This example uses *com.microsoft.Edge* as the domain.</span></span>
   - <span data-ttu-id="2508f-148">Pour le **Schéma personnalisé**, collez le contenu du fichier manifeste «policy_manifest.json».</span><span class="sxs-lookup"><span data-stu-id="2508f-148">For **Custom Schema**, paste the contents of the "policy_manifest.json" manifest file.</span></span>
   - <span data-ttu-id="2508f-149">Cliquez sur **Save**.</span><span class="sxs-lookup"><span data-stu-id="2508f-149">Click **Save**.</span></span>

8. <span data-ttu-id="2508f-150">Une fois le profil enregistré, Jamf affiche la section **Général** présentée dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="2508f-150">After you save the profile, Jamf displays the **General** section shown in the next screen shot.</span></span>

   ![Configuration de la section Général](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-general-setting.png)

   - <span data-ttu-id="2508f-152">Spécifiez un **Nom** d'affichage pour le profil et une **Description**.</span><span class="sxs-lookup"><span data-stu-id="2508f-152">Provide a display **Name** for the profile and a **Description**.</span></span>
   - <span data-ttu-id="2508f-153">Conservez le paramètre par défaut pour la **Catégorie**, c'est-à-dire **Aucune**.</span><span class="sxs-lookup"><span data-stu-id="2508f-153">Keep the default setting for **Category**, which is **None**.</span></span>
   - <span data-ttu-id="2508f-154">Pour la **Méthode de distribution**, les options sont **Installer automatiquement** ou **Rendre disponible dans le libre-service**.</span><span class="sxs-lookup"><span data-stu-id="2508f-154">For **Distribution Method**, the options are **Install Automatically** or **Make Available in Self Service**.</span></span>
   - <span data-ttu-id="2508f-155">Pour le **Niveau**, les options sont **Niveau utilisateur** ou **Niveau ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="2508f-155">For **Level**, the options are **User Level** or **Computer Level**.</span></span>
   - <span data-ttu-id="2508f-156">Cliquez sur **Save**.</span><span class="sxs-lookup"><span data-stu-id="2508f-156">Click **Save**.</span></span>

9. <span data-ttu-id="2508f-157">Après enregistrement de la section Général, Jamf affiche le profil de configuration «Canal Bêta Microsoft Edge» configuré pour notre exemple.</span><span class="sxs-lookup"><span data-stu-id="2508f-157">After you save the General section, Jamf shows the "Microsoft Edge Beta Channel" configuration profile set up for our example.</span></span> <span data-ttu-id="2508f-158">Dans la capture d’écran suivante, veuillez prendre note que vous pouvez continuer à travailler sur le profil en cliquant sur **Modifier** ou si vous avez terminé, cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="2508f-158">In the next screen shot, note that you can keep working the profile by clicking **Edit** or if you're finished, click **Done**.</span></span>

   ![Nouveau profil de configuration avec options](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel.png)

   > [!NOTE]
   > <span data-ttu-id="2508f-160">Vous pouvez modifier ce profil après son enregistrement et lors d'une autre session Jamf.</span><span class="sxs-lookup"><span data-stu-id="2508f-160">You can edit this profile after it's been saved and in another Jamf session.</span></span> <span data-ttu-id="2508f-161">Par exemple, vous pouvez décider de modifier la Méthode de distribution pour la Rendre disponible dans le libre-service.</span><span class="sxs-lookup"><span data-stu-id="2508f-161">For example, you might decide to change the Distribution Method to Make Available in Self Service.</span></span>

   <span data-ttu-id="2508f-162">Pour effectuer un suivi des modifications sur le canal Microsoft Edge Stable ou le supprimer, sélectionnez le nom du profil, tel qu'illustré dans la capture d’écran Profils de configuration suivante.</span><span class="sxs-lookup"><span data-stu-id="2508f-162">To do a follow up edit on the Microsoft Edge Stable Channel, or delete it, select the profile name, shown in the following Configuration Profiles screen shot.</span></span>

   ![Liste Profils de configuration](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel-done.png)

<span data-ttu-id="2508f-164">Une fois le nouveau profil de configuration créé, vous devez configurer l’**Étendue** du profil.</span><span class="sxs-lookup"><span data-stu-id="2508f-164">After you create the new configuration profile you still have to configure the **Scope** for the profile.</span></span>

### <span data-ttu-id="2508f-165">Configuration de l'étendue</span><span class="sxs-lookup"><span data-stu-id="2508f-165">To configure the scope</span></span>

1. <span data-ttu-id="2508f-166">Pour les **Cibles**, fournissez les paramètres minimaux suivants:</span><span class="sxs-lookup"><span data-stu-id="2508f-166">For **Targets**, provide the following minimum settings:</span></span>

   - <span data-ttu-id="2508f-167">ORDINATEURS CIBLES.</span><span class="sxs-lookup"><span data-stu-id="2508f-167">TARGET COMPUTERS.</span></span> <span data-ttu-id="2508f-168">Les options sont: Ordinateurs spécifiques ou Tous les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="2508f-168">The options are Specific Computers or All Computers.</span></span>
   - <span data-ttu-id="2508f-169">UTILISATEURS CIBLES.</span><span class="sxs-lookup"><span data-stu-id="2508f-169">TARGET USERS.</span></span> <span data-ttu-id="2508f-170">Les options sont: Utilisateurs spécifiques ou Tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2508f-170">The options are Specific Users or All Users.</span></span>
   - <span data-ttu-id="2508f-171">Cliquez sur **Save**.</span><span class="sxs-lookup"><span data-stu-id="2508f-171">Click **Save**.</span></span>
2. <span data-ttu-id="2508f-172">Pour les **Limitations**, conservez le paramètre par défaut, à savoir Aucune.</span><span class="sxs-lookup"><span data-stu-id="2508f-172">For **Limitations**, keep the default setting: None.</span></span> <span data-ttu-id="2508f-173">Cliquez sur **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="2508f-173">Click **Cancel**.</span></span>
3. <span data-ttu-id="2508f-174">Pour les **Exclusions**, conservez le paramètre par défaut, à savoir Aucune.</span><span class="sxs-lookup"><span data-stu-id="2508f-174">For **Exclusions**, keep the default setting: None.</span></span> <span data-ttu-id="2508f-175">Cliquez sur **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="2508f-175">Click **Cancel**.</span></span>

## <span data-ttu-id="2508f-176">Forum Aux Questions</span><span class="sxs-lookup"><span data-stu-id="2508f-176">Frequently Asked Questions</span></span>

### <span data-ttu-id="2508f-177">MicrosoftEdge peut-il être configuré pour utiliser les préférences principales?</span><span class="sxs-lookup"><span data-stu-id="2508f-177">Can Microsoft Edge be configured to use master preferences?</span></span>

<span data-ttu-id="2508f-178">Oui, vous pouvez configurer MicrosoftEdge pour qu’il utilise un fichier de préférences principales.</span><span class="sxs-lookup"><span data-stu-id="2508f-178">Yes, you can configure Microsoft Edge to use a master preferences file.</span></span>

<span data-ttu-id="2508f-179">Un fichier de préférences principales vous permet de configurer les paramètres par défaut d’un profil utilisateur de navigateur lors du déploiement de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="2508f-179">A master preferences file lets you configure default settings for a browser user profile when Microsoft Edge is deployed.</span></span> <span data-ttu-id="2508f-180">Vous pouvez également utiliser un fichier de préférences principales pour appliquer des paramètres sur des ordinateurs qui ne sont pas gérés par un système de gestion des périphériques.</span><span class="sxs-lookup"><span data-stu-id="2508f-180">You can also use a master preferences file to apply settings on computers that aren't managed by a device management system.</span></span> <span data-ttu-id="2508f-181">Ces paramètres sont appliqués au profil de l’utilisateur la première fois que l’utilisateur exécute le navigateur.</span><span class="sxs-lookup"><span data-stu-id="2508f-181">These settings are applied to the user’s profile the first time the user runs the browser.</span></span> <span data-ttu-id="2508f-182">Une fois que l’utilisateur a exécuté le navigateur, les modifications apportées au fichier de préférences principales ne sont pas appliquées.</span><span class="sxs-lookup"><span data-stu-id="2508f-182">After the user runs the browser, changes to the master preferences file aren’t applied.</span></span> <span data-ttu-id="2508f-183">Un utilisateur peut modifier les paramètres à partir des préférences principales dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="2508f-183">A user can change settings from the master preferences in the browser.</span></span> <span data-ttu-id="2508f-184">Si vous souhaitez rendre un paramètre obligatoire ou modifier un paramètre après la première exécution du navigateur, vous devez utiliser une stratégie.</span><span class="sxs-lookup"><span data-stu-id="2508f-184">If you want to make a setting mandatory or change a setting after the first run of the browser, you must use a policy.</span></span>

<span data-ttu-id="2508f-185">Un fichier de préférences principales vous permet de personnaliser de nombreux paramètres et préférences pour le navigateur, y compris ceux partagés avec d’autres navigateurs basés Chromium et spécifiques à MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="2508f-185">A master preferences file lets you to customize many different settings and preferences for the browser, including those shared with other Chromium based browsers and specific to Microsoft Edge.</span></span>  <span data-ttu-id="2508f-186">Les préférences liées à la stratégie peuvent être configurées à l’aide du fichier de préférences principales.</span><span class="sxs-lookup"><span data-stu-id="2508f-186">Policy related preferences can be configured using the master preferences file.</span></span> <span data-ttu-id="2508f-187">Dans les cas où une stratégie est définie et qu’un jeu de préférences principales correspondant est défini, le paramètre de stratégie est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="2508f-187">In cases where a policy is set and there’s a corresponding master preference set, the policy setting takes precedence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2508f-188">Toutes les préférences disponibles peuvent ne pas être cohérentes avec la terminologie et les conventions d’affectation de noms de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="2508f-188">All the available preferences might not be consistent with Microsoft Edge terminology and naming conventions.</span></span>  <span data-ttu-id="2508f-189">Il n’est pas garanti que ces préférences continuent de fonctionner comme prévu dans les prochaines versions.</span><span class="sxs-lookup"><span data-stu-id="2508f-189">There’s no guarantee that these preferences will continue to work as expected in future releases.</span></span> <span data-ttu-id="2508f-190">Les préférences peuvent être modifiées ou ignorées dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2508f-190">Preferences might be changed or ignored in later versions.</span></span>

<span data-ttu-id="2508f-191">Un fichier de préférences principales est un fichier texte mis en forme à l’aide du balisage JSON.</span><span class="sxs-lookup"><span data-stu-id="2508f-191">A master preferences file is a text file that’s formatted using JSON markup.</span></span> <span data-ttu-id="2508f-192">Ce fichier doit être ajouté au même répertoire que le msedge.exe exécutable.</span><span class="sxs-lookup"><span data-stu-id="2508f-192">This file needs to be added to the same directory as the msedge.exe executable.</span></span> <span data-ttu-id="2508f-193">Pour les déploiements à l’échelle du système sur macOS, c’est généralement: «*~/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*» ou «*/Library/Microsoft/Microsoft Edge Master Preferences*».</span><span class="sxs-lookup"><span data-stu-id="2508f-193">For system wide enterprise deployments on macOS this is typically: “*~/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*" or "*/Library/Microsoft/Microsoft Edge Master Preferences*”.</span></span>

## <span data-ttu-id="2508f-194">Articles associés</span><span class="sxs-lookup"><span data-stu-id="2508f-194">See also</span></span>

- [<span data-ttu-id="2508f-195">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="2508f-195">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="2508f-196">Configurer pour macOS avec Intune</span><span class="sxs-lookup"><span data-stu-id="2508f-196">Configure for macOS with Intune</span></span>](configure-microsoft-edge-on-mac.md)
- [<span data-ttu-id="2508f-197">Configurer pour Windows</span><span class="sxs-lookup"><span data-stu-id="2508f-197">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="2508f-198">Configurer pour Windows avec Intune</span><span class="sxs-lookup"><span data-stu-id="2508f-198">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)
