---
title: Configurer les stratégies MicrosoftEdge sur macOS grâce à Jamf
ms.author: brianalt
author: dan-wesley
manager: laurawi
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer les paramètres de stratégie MicrosoftEdge sur les appareils Mac grâce à Jamf
ms.openlocfilehash: 1859d9fb1fd3ea8ff6908c41f75df21a8b338769
ms.sourcegitcommit: ed6a5afabf909df87bec48671c4c47bcdfaeb7bc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/02/2020
ms.locfileid: "11194712"
---
# <span data-ttu-id="7cb24-103">Configurer les paramètres de stratégie MicrosoftEdge sur macOS grâce à Jamf</span><span class="sxs-lookup"><span data-stu-id="7cb24-103">Configure Microsoft Edge policy settings on macOS with Jamf</span></span>

<span data-ttu-id="7cb24-104">Cet article explique la configuration de paramètres de stratégie sur macOS à l’aide d’un fichier de manifeste de stratégie Microsoft Edge sur Jamf Pro10.19.</span><span class="sxs-lookup"><span data-stu-id="7cb24-104">This article describes how to configure policy settings on macOS using a Microsoft Edge policy manifest file on Jamf Pro 10.19.</span></span>

<span data-ttu-id="7cb24-105">Vous pouvez également configurer les paramètres de stratégies MicrosoftEdge sur macOS à l’aide d’un fichier de liste de propriétés (.plist).</span><span class="sxs-lookup"><span data-stu-id="7cb24-105">You can also configure Microsoft Edge policy settings on macOS by using a property list (.plist) file.</span></span> <span data-ttu-id="7cb24-106">Pour plus d’informations, voir [Configuration pour macOS à l’aide d’un fichier .plist](configure-microsoft-edge-on-mac.md).</span><span class="sxs-lookup"><span data-stu-id="7cb24-106">For more information, see [Configure for macOS using a .plist](configure-microsoft-edge-on-mac.md)</span></span>


## <span data-ttu-id="7cb24-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="7cb24-107">Prerequisites</span></span>

<span data-ttu-id="7cb24-108">Le logiciel suivant est nécessaire:</span><span class="sxs-lookup"><span data-stu-id="7cb24-108">The following software is required:</span></span>

- <span data-ttu-id="7cb24-109">Microsoft Edge Stable canal8.1</span><span class="sxs-lookup"><span data-stu-id="7cb24-109">Microsoft Edge Stable channel 81</span></span>
- <span data-ttu-id="7cb24-110">Fichier de modèles de stratégie, version81.0.416.3</span><span class="sxs-lookup"><span data-stu-id="7cb24-110">Policy Templates file, version 81.0.416.3</span></span>
- <span data-ttu-id="7cb24-111">Jamf Pro version10.19</span><span class="sxs-lookup"><span data-stu-id="7cb24-111">Jamf Pro, Version 10.19</span></span>

## <span data-ttu-id="7cb24-112">À propos de l’application Jamf Pro & du menu Paramètres personnalisés</span><span class="sxs-lookup"><span data-stu-id="7cb24-112">About the Jamf Pro Application & Custom Settings menu</span></span>

<span data-ttu-id="7cb24-113">Avant la publication de Jamf Pro10.18, la gestion d’Office365 impliquait la création manuelle d’un fichier .plist.</span><span class="sxs-lookup"><span data-stu-id="7cb24-113">Before Jamf Pro 10.18, managing Office 365 involved manually building a .plist file.</span></span> <span data-ttu-id="7cb24-114">Le flux de travail était fastidieux et nécessitait une solide formation technique.</span><span class="sxs-lookup"><span data-stu-id="7cb24-114">This was a time-consuming workflow that required a strong technical background.</span></span> <span data-ttu-id="7cb24-115">Jamf Pro10.18 éliminait ces obstacles en rationalisant le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="7cb24-115">Jamf Pro 10.18 eliminated those barriers by streamlining the configuration process.</span></span> <span data-ttu-id="7cb24-116">Cependant, les administrateurs informatiques pouvaient seulement utiliser cette nouvelle interface utilisateur pour des applications spécifiques et des domaines de préférence spécifiés par Jamf.</span><span class="sxs-lookup"><span data-stu-id="7cb24-116">However, IT Admins could only use this new user interface for specific applications and preference domains specified by Jamf.</span></span>

<span data-ttu-id="7cb24-117">Avec Jamf Pro10.19, un utilisateur peut télécharger un manifeste JSON en tant que «schéma personnalisé» pour cibler tout domaine de préférence, et l’interface utilisateur graphique est générée à partir de ce manifeste.</span><span class="sxs-lookup"><span data-stu-id="7cb24-117">In Jamf Pro 10.19, a user can upload a JSON manifest as a "custom schema" to target any preference domain, and the graphical user interface will be generated from this manifest.</span></span> <span data-ttu-id="7cb24-118">Le schéma personnalisé créé respecte la spécification de schéma JSON.</span><span class="sxs-lookup"><span data-stu-id="7cb24-118">The custom schema that's created follows the JSON Schema specification.</span></span>

<span data-ttu-id="7cb24-119">Pour plus d’informations, voir [Profils de configuration d’ordinateur](https://jamf.it/computer-configuration-profiles) dans le Guide de l’administrateur Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="7cb24-119">For more information, see [Computer Configuration Profiles](https://jamf.it/computer-configuration-profiles) in the Jamf Pro Administrator's Guide.</span></span>

## <span data-ttu-id="7cb24-120">Obtenir le manifeste de stratégie pour une version spécifique de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7cb24-120">Get the policy manifest for a specific version of Microsoft Edge</span></span>

<span data-ttu-id="7cb24-121">Pour obtenir le manifeste de stratégie:</span><span class="sxs-lookup"><span data-stu-id="7cb24-121">To get the policy manifest:</span></span>

- <span data-ttu-id="7cb24-122">Accédez à la [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="7cb24-122">Go to the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="7cb24-123">Dans la liste déroulante Canal/Version, sélectionnez **n’importe quel canal avec la version 81 ou une version ultérieure.**_.</span><span class="sxs-lookup"><span data-stu-id="7cb24-123">On the Channel/Version dropdown list, select **any channel with version 81 or later.**_.</span></span>
- <span data-ttu-id="7cb24-124">Dans la liste déroulante Build, sélectionnez n’importe quel _ \*build 81 ou une version ultérieure.\*\*_.</span><span class="sxs-lookup"><span data-stu-id="7cb24-124">On the Build dropdown list, select any _*81 build or later.*\*_.</span></span>
- <span data-ttu-id="7cb24-125">Cliquez sur OBTENIR DES FICHIERS DE STRATÉGIE pour télécharger notre ensemble de modèles de stratégie.</span><span class="sxs-lookup"><span data-stu-id="7cb24-125">Click GET POLICY FILES to download our policy templates bundle.</span></span>

  > [!NOTE]
  > <span data-ttu-id="7cb24-126">L'ensemble de modèles de stratégie est signé en tant que fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="7cb24-126">Currently, the policy templates bundle is signed as a CAB file.</span></span> <span data-ttu-id="7cb24-127">Vous devez utiliser un outil tiers, tel que Unarchiver, pour ouvrir le fichier sur macOS.</span><span class="sxs-lookup"><span data-stu-id="7cb24-127">You'll need to use a 3rd party tool, such as The Unarchiver to open the file on macOS.</span></span>

<span data-ttu-id="7cb24-128">Une fois le fichier CAB décompressé, décompressez le fichier ZIP et accédez au répertoire «mac» de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="7cb24-128">After you unpack the CAB file, unpack the ZIP file and navigate to the "mac" top level directory.</span></span> <span data-ttu-id="7cb24-129">Le manifeste appelé «policy_manifest.json» figure dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="7cb24-129">The manifest, which is named "policy_manifest.json", is in this directory.</span></span>

<span data-ttu-id="7cb24-130">Ce manifeste est publié dans chaque ensemble de stratégies à compter de la build81.0.416.3.</span><span class="sxs-lookup"><span data-stu-id="7cb24-130">This manifest will be published in every policy bundle starting with build 81.0.416.3.</span></span> <span data-ttu-id="7cb24-131">Si vous souhaitez tester des stratégies dans le canal de développement, vous pouvez prendre le manifeste associé à chaque publication de développement et le tester dans Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="7cb24-131">If you want to test policies in the Dev channel, you can take the manifest associated with each Dev release and test it in Jamf Pro.</span></span>  

## <span data-ttu-id="7cb24-132">Utilisation du manifeste de stratégie dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="7cb24-132">Use the policy manifest in Jamf Pro</span></span>

<span data-ttu-id="7cb24-133">Utilisez la procédure suivante pour télécharger le manifeste de stratégie dans Jamf Pro et créer un profil de stratégie pour macOS.</span><span class="sxs-lookup"><span data-stu-id="7cb24-133">Use the following steps to upload the policy manifest to Jamf Pro and then create a policy profile for macOS.</span></span>

1. <span data-ttu-id="7cb24-134">Connectez-vous à Jamf.</span><span class="sxs-lookup"><span data-stu-id="7cb24-134">Sign in to Jamf.</span></span>
2. <span data-ttu-id="7cb24-135">Sélectionnez l’onglet _\*Ordinateur\*\*.</span><span class="sxs-lookup"><span data-stu-id="7cb24-135">Select the _*Computer*\* tab.</span></span>
3. <span data-ttu-id="7cb24-136">Sous **Gestion de contenu**, sélectionnez **Profils de configuration**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-136">Under **Content Management**, select **Configuration Profiles**.</span></span>
4. <span data-ttu-id="7cb24-137">Sur la page **Profils de configuration**, cliquez sur **+ Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-137">On the **Configuration Profiles** page, click **+ New**.</span></span>

   ![Ajout d'un nouveau profil dans Jamf](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles.png)

5. <span data-ttu-id="7cb24-139">Sur **Nouveau profil de configuration macOS**>**Options**, sélectionnez **Application & paramètres personnalisés**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-139">On **New macOS Configuration Profile**>**Options**, select **Application & Custom Settings**.</span></span>
6. <span data-ttu-id="7cb24-140">Dans la fenêtre contextuelle **Application & paramètres personnalisés**, cliquez sur **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-140">On the **Application & Custom Settings** popup window, click **Configure**.</span></span>

   ![Configurer les Application et paramètres personnalisés](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom.png)

7. <span data-ttu-id="7cb24-142">Dans la section **Application & paramètres personnalisés**, configurez les valeurs affichées dans la capture d’écran ci-après.</span><span class="sxs-lookup"><span data-stu-id="7cb24-142">In the **Application & Custom Settings** section, set the values shown in the following screen shot.</span></span>

   ![Source du profil et schéma personnalisé](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-schema.png)

   - <span data-ttu-id="7cb24-144">Pour la **Méthode de création**, sélectionnez **Configurer les paramètres**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-144">For **Creation Method**, pick **Configure settings**.</span></span>
   - <span data-ttu-id="7cb24-145">Pour la **Source**, sélectionnez **Schéma personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-145">For **Source**, pick **Custom Schema**.</span></span>
   - <span data-ttu-id="7cb24-146">Pour le **Domaine de préférence**, indiquez votre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="7cb24-146">For **Preference Domain**, provide the name of your domain.</span></span> <span data-ttu-id="7cb24-147">Cet exemple utilise *com.microsoft.Edge* en tant que domaine.</span><span class="sxs-lookup"><span data-stu-id="7cb24-147">This example uses *com.microsoft.Edge* as the domain.</span></span>
   - <span data-ttu-id="7cb24-148">Pour le **Schéma personnalisé**, collez le contenu du fichier manifeste «policy_manifest.json».</span><span class="sxs-lookup"><span data-stu-id="7cb24-148">For **Custom Schema**, paste the contents of the "policy_manifest.json" manifest file.</span></span>
   - <span data-ttu-id="7cb24-149">Cliquez sur **Save**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-149">Click **Save**.</span></span>

8. <span data-ttu-id="7cb24-150">Une fois le profil enregistré, Jamf affiche la section **Général** présentée dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="7cb24-150">After you save the profile, Jamf displays the **General** section shown in the next screen shot.</span></span>

   ![Configuration de la section Général](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-general-setting.png)

   - <span data-ttu-id="7cb24-152">Spécifiez un **Nom** d'affichage pour le profil et une **Description**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-152">Provide a display **Name** for the profile and a **Description**.</span></span>
   - <span data-ttu-id="7cb24-153">Conservez le paramètre par défaut pour la **Catégorie**, c'est-à-dire **Aucune**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-153">Keep the default setting for **Category**, which is **None**.</span></span>
   - <span data-ttu-id="7cb24-154">Pour la **Méthode de distribution**, les options sont **Installer automatiquement** ou **Rendre disponible dans le libre-service**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-154">For **Distribution Method**, the options are **Install Automatically** or **Make Available in Self Service**.</span></span>
   - <span data-ttu-id="7cb24-155">Pour le **Niveau**, les options sont **Niveau utilisateur** ou **Niveau ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-155">For **Level**, the options are **User Level** or **Computer Level**.</span></span>
   - <span data-ttu-id="7cb24-156">Cliquez sur **Save**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-156">Click **Save**.</span></span>

9. <span data-ttu-id="7cb24-157">Après enregistrement de la section Général, Jamf affiche le profil de configuration «Canal Bêta Microsoft Edge» configuré pour notre exemple.</span><span class="sxs-lookup"><span data-stu-id="7cb24-157">After you save the General section, Jamf shows the "Microsoft Edge Beta Channel" configuration profile set up for our example.</span></span> <span data-ttu-id="7cb24-158">Dans la capture d’écran suivante, veuillez prendre note que vous pouvez continuer à travailler sur le profil en cliquant sur **Modifier** ou si vous avez terminé, cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-158">In the next screen shot, note that you can keep working the profile by clicking **Edit** or if you're finished, click **Done**.</span></span>

   ![Nouveau profil de configuration avec options](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel.png)

   > [!NOTE]
   > <span data-ttu-id="7cb24-160">Vous pouvez modifier ce profil après son enregistrement et lors d'une autre session Jamf.</span><span class="sxs-lookup"><span data-stu-id="7cb24-160">You can edit this profile after it's been saved and in another Jamf session.</span></span> <span data-ttu-id="7cb24-161">Par exemple, vous pouvez décider de modifier la Méthode de distribution pour la Rendre disponible dans le libre-service.</span><span class="sxs-lookup"><span data-stu-id="7cb24-161">For example, you might decide to change the Distribution Method to Make Available in Self Service.</span></span>

   <span data-ttu-id="7cb24-162">Pour effectuer un suivi des modifications sur le canal Microsoft Edge Stable ou le supprimer, sélectionnez le nom du profil, tel qu'illustré dans la capture d’écran Profils de configuration suivante.</span><span class="sxs-lookup"><span data-stu-id="7cb24-162">To do a follow up edit on the Microsoft Edge Stable Channel, or delete it, select the profile name, shown in the following Configuration Profiles screen shot.</span></span>

   ![Liste Profils de configuration](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel-done.png)

<span data-ttu-id="7cb24-164">Une fois le nouveau profil de configuration créé, vous devez configurer l’**Étendue** du profil.</span><span class="sxs-lookup"><span data-stu-id="7cb24-164">After you create the new configuration profile you still have to configure the **Scope** for the profile.</span></span>

### <span data-ttu-id="7cb24-165">Configuration de l'étendue</span><span class="sxs-lookup"><span data-stu-id="7cb24-165">To configure the scope</span></span>

1. <span data-ttu-id="7cb24-166">Pour les **Cibles**, fournissez les paramètres minimaux suivants:</span><span class="sxs-lookup"><span data-stu-id="7cb24-166">For **Targets**, provide the following minimum settings:</span></span>

   - <span data-ttu-id="7cb24-167">ORDINATEURS CIBLES.</span><span class="sxs-lookup"><span data-stu-id="7cb24-167">TARGET COMPUTERS.</span></span> <span data-ttu-id="7cb24-168">Les options sont: Ordinateurs spécifiques ou Tous les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="7cb24-168">The options are Specific Computers or All Computers.</span></span>
   - <span data-ttu-id="7cb24-169">UTILISATEURS CIBLES.</span><span class="sxs-lookup"><span data-stu-id="7cb24-169">TARGET USERS.</span></span> <span data-ttu-id="7cb24-170">Les options sont: Utilisateurs spécifiques ou Tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7cb24-170">The options are Specific Users or All Users.</span></span>
   - <span data-ttu-id="7cb24-171">Cliquez sur **Save**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-171">Click **Save**.</span></span>
2. <span data-ttu-id="7cb24-172">Pour les **Limitations**, conservez le paramètre par défaut, à savoir Aucune.</span><span class="sxs-lookup"><span data-stu-id="7cb24-172">For **Limitations**, keep the default setting: None.</span></span> <span data-ttu-id="7cb24-173">Cliquez sur **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-173">Click **Cancel**.</span></span>
3. <span data-ttu-id="7cb24-174">Pour les **Exclusions**, conservez le paramètre par défaut, à savoir Aucune.</span><span class="sxs-lookup"><span data-stu-id="7cb24-174">For **Exclusions**, keep the default setting: None.</span></span> <span data-ttu-id="7cb24-175">Cliquez sur **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="7cb24-175">Click **Cancel**.</span></span>

## <span data-ttu-id="7cb24-176">Voir également</span><span class="sxs-lookup"><span data-stu-id="7cb24-176">See also</span></span>

- [<span data-ttu-id="7cb24-177">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="7cb24-177">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="7cb24-178">Configurer pour macOS avec Intune</span><span class="sxs-lookup"><span data-stu-id="7cb24-178">Configure for macOS with Intune</span></span>](configure-microsoft-edge-on-mac.md)
- [<span data-ttu-id="7cb24-179">Configurer pour Windows</span><span class="sxs-lookup"><span data-stu-id="7cb24-179">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="7cb24-180">Configurer pour Windows avec Intune</span><span class="sxs-lookup"><span data-stu-id="7cb24-180">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)
