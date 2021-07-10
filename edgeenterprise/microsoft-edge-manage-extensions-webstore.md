---
title: Extensions d’auto-hébergement Microsoft Edge
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Découvrez comment empaqueter et auto-héberger les extensions Microsoft Edge dans l’entreprise.
ms.openlocfilehash: aef4438212829006e39572fa938462f13721c580
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642870"
---
# <a name="self-host-microsoft-edge-extensions"></a><span data-ttu-id="08700-103">Extensions d’auto-hébergement Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="08700-103">Self-host Microsoft Edge extensions</span></span>

<span data-ttu-id="08700-104">Cet article fournit des instructions de base pour empaqueter une extension à héberger sur votre propre site web.</span><span class="sxs-lookup"><span data-stu-id="08700-104">This article provides basic guidance for packaging an extension to host on your own webstore.</span></span> <span data-ttu-id="08700-105">Il inclut également des instructions sur la façon de déployer des extensions sur les appareils et les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="08700-105">It also includes instructions on how to deploy extensions to devices and users in your organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="08700-106">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="08700-106">Prerequisites</span></span>

<span data-ttu-id="08700-107">Pour auto-héberger vos propres extensions, vous devrez fournir vos propres services d’hébergement web pour les extensions et leurs fichiers manifestes.</span><span class="sxs-lookup"><span data-stu-id="08700-107">To self-host your own extensions, you will need to provide your own web hosting services for the extensions and their manifest files.</span></span>

 <span data-ttu-id="08700-108">Les étapes suivantes supposent que vous avez déjà créé votre extension, que vous avez de l’expérience avec les fichiers XML, que vous avez une connaissance approfondie de la configuration de la stratégie de groupe et que vous savez comment utiliser le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="08700-108">The following steps assume that you’ve already created your extension, have some experience with XML files, have a working knowledge of configuring group policy, and know how to use the Windows registry.</span></span>

## <a name="publish-an-extension"></a><span data-ttu-id="08700-109">Publier une extension</span><span class="sxs-lookup"><span data-stu-id="08700-109">Publish an extension</span></span>

<span data-ttu-id="08700-110">Avant de publier une extension, elle doit être empaquetée dans un fichier CRX (extension Chrome).</span><span class="sxs-lookup"><span data-stu-id="08700-110">Before you publish an extension it needs to be packed into a CRX (Chrome extension) file.</span></span> <span data-ttu-id="08700-111">Utilisez les étapes suivantes pour empaqueter une extension en tant que fichier CRX.</span><span class="sxs-lookup"><span data-stu-id="08700-111">Use the following steps as a guide to packing an extension as a CRX file.</span></span>

1. <span data-ttu-id="08700-112">Dans la barre d'adresses de Microsoft Edge, allez à\* edge://extensions\* et activez **Développeur Mode**s’il n’est pas déjà activé.</span><span class="sxs-lookup"><span data-stu-id="08700-112">In the Microsoft Edge address bar, go to *edge://extensions* and turn on **Developer mode** if it’s not already enabled.</span></span>
2. <span data-ttu-id="08700-113">Sous **Extensions installées**cliquez sur **Pack Extension** pour créer le fichier CRX.</span><span class="sxs-lookup"><span data-stu-id="08700-113">Under **Installed extensions**, click **Pack Extension** to create the CRX file.</span></span>
3. <span data-ttu-id="08700-114">Utilisez la boîte de dialogue **Pack Extension**pour rechercher le répertoire qui possède la source de l’extension.</span><span class="sxs-lookup"><span data-stu-id="08700-114">Use the **Pack extension** dialog to find the directory that has the source for the extension.</span></span> <span data-ttu-id="08700-115">Sélectionnez le répertoire, puis cliquez sur **Pack Extension**.</span><span class="sxs-lookup"><span data-stu-id="08700-115">Select the directory and then click **Pack extension**.</span></span>  <span data-ttu-id="08700-116">Cela crée votre fichier CRX, ainsi qu’un fichier PEM.</span><span class="sxs-lookup"><span data-stu-id="08700-116">This will create your CRX file, along with a PEM file.</span></span> <span data-ttu-id="08700-117">Enregistrez le fichier PEM, car il est nécessaire pour faire les mises à jour des versions de l’extension.</span><span class="sxs-lookup"><span data-stu-id="08700-117">Save the PEM file because it’s needed for making version updates to the extension.</span></span> <span data-ttu-id="08700-118">La capture d’écran suivante montre la boîte de dialogue **Extension Pack**pour localiser le répertoire racine de l’extension.</span><span class="sxs-lookup"><span data-stu-id="08700-118">The next screenshot shows the **Pack extension** dialog for locating the root directory of the extension.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-pack-dialog.png" alt-text="Boîte de dialogue Extension Pack pour trouver le code source d’une extension.":::

   > [!IMPORTANT]
   > <span data-ttu-id="08700-120">Stockez le fichier PEM dans un emplacement sûr, car il s’agit de la clé de l’extension et est nécessaire pour les futures mises à jour.</span><span class="sxs-lookup"><span data-stu-id="08700-120">Store the PEM file in a safe location because it’s the key for the extension and it’s needed for future updates.</span></span>

4. <span data-ttu-id="08700-121">Faites glisser le fichier CRX dans la fenêtre d’extensions et assurez-vous qu’il se charge.</span><span class="sxs-lookup"><span data-stu-id="08700-121">Drag the CRX file into your extensions window and make sure that it loads.</span></span>
5. <span data-ttu-id="08700-122">Testez l’extension et notez le champ ID (il s’agit de l’ID CRX) et le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="08700-122">Test the extension and take note of the ID field (this is the CRX ID) and version number.</span></span> <span data-ttu-id="08700-123">Vous aurez besoin de ces informations ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="08700-123">You’ll need this information later.</span></span> <span data-ttu-id="08700-124">La capture d’écran suivante montre une extension de test avec son ID CRX.</span><span class="sxs-lookup"><span data-stu-id="08700-124">The next screenshot shows a test extension with its CRX ID.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-test-extension.png" alt-text="Exemple d’extension affichant l’ID CRX":::

6. <span data-ttu-id="08700-126">Téléchargez le fichier CRX sur l’hôte et notez l’URL de l’emplacement à partir duquel il sera téléchargé.</span><span class="sxs-lookup"><span data-stu-id="08700-126">Upload the the CRX file to the host and note the URL of the location it will be downloaded from.</span></span> <span data-ttu-id="08700-127">Ces informations sont nécessaires pour le fichier manifeste XML.</span><span class="sxs-lookup"><span data-stu-id="08700-127">This information is needed for the XML manifest file.</span></span>
7. <span data-ttu-id="08700-128">Pour créer un fichier manifeste XML avec l’ID d’application/extension, téléchargez l’URL, et la version, définissez les champs suivants:</span><span class="sxs-lookup"><span data-stu-id="08700-128">To create a manifest XML file with the app/extension ID, download URL, and version, define the following fields:</span></span>  

   - <span data-ttu-id="08700-129">**appid**: L’ID d’extension de l’étape 5</span><span class="sxs-lookup"><span data-stu-id="08700-129">**appid** - The extension ID from step 5</span></span>
   - <span data-ttu-id="08700-130">**codebase**: L’emplacement du téléchargement du fichier CRX de l’étape 6</span><span class="sxs-lookup"><span data-stu-id="08700-130">**codebase** - The download location for the CRX file from step 6</span></span>
   - <span data-ttu-id="08700-131">**version**: La version de l’application/extension, qui doit correspondre à la version spécifiée dans le manifeste de l’extension.</span><span class="sxs-lookup"><span data-stu-id="08700-131">**version** - The version of the app/extension, which should match the version specified in the manifest of the extension.</span></span>

   <span data-ttu-id="08700-132">L’extrait de code suivant montre un exemple de fichier manifeste XML.</span><span class="sxs-lookup"><span data-stu-id="08700-132">The next code snippet shows an example of an XML manifest file.</span></span>

   ```xml
   <?xml version='1.0' encoding='UTF-8'?> 
   <gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'> 
     <app appid='ekilpdeokbpjmminmhfcgkncmmohmfeb'> 
     <updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.0' /> 
     </app> 
   </gupdate> 
   ```

   <span data-ttu-id="08700-133">Pour plus d’informations voir[Extensions de mise à jour automatique dans Microsoft Edge Microsoft Edge Développement](/microsoft-edge/extensions-chromium/enterprise/auto-update).</span><span class="sxs-lookup"><span data-stu-id="08700-133">For more information, see [Auto-update extensions in Microsoft Edge - Microsoft Edge Development](/microsoft-edge/extensions-chromium/enterprise/auto-update).</span></span>

8. <span data-ttu-id="08700-134">Chargez le fichier XML terminé à un emplacement à partir de lequel il peut être téléchargé, en notant l’URL.</span><span class="sxs-lookup"><span data-stu-id="08700-134">Upload the completed XML file to a location where it can be downloaded from, noting the URL.</span></span> <span data-ttu-id="08700-135">Cette URL sera nécessaire lorsque vous installerez l’extension à l’aide d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="08700-135">This URL will be needed when you install the extension using a group policy.</span></span> <span data-ttu-id="08700-136">Consultez [Distribuer une extension hébergée en privé](#distribute-a-privately-hosted-extension).</span><span class="sxs-lookup"><span data-stu-id="08700-136">See [Distribute a privately hosted extension](#distribute-a-privately-hosted-extension).</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="08700-137">L’emplacement d’hébergement de l’extension n’a pas besoin d’authentification.</span><span class="sxs-lookup"><span data-stu-id="08700-137">The hosting location for the extension doesn’t need authentication.</span></span> <span data-ttu-id="08700-138">Il doit être accessible par les appareils des utilisateurs où qu’ils soient.</span><span class="sxs-lookup"><span data-stu-id="08700-138">It needs to be accessible by user devices wherever they might be used.</span></span>

## <a name="publish-updates-to-an-extension"></a><span data-ttu-id="08700-139">Publiez les mises à jour sur une extension</span><span class="sxs-lookup"><span data-stu-id="08700-139">Publish updates to an extension</span></span>

<span data-ttu-id="08700-140">Après avoir changé et testé l’extension mise à jour, vous pouvez la publier.</span><span class="sxs-lookup"><span data-stu-id="08700-140">After you change and test the updated extension you can publish it.</span></span> <span data-ttu-id="08700-141">Utilisez les étapes suivantes comme guide pour publier une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="08700-141">Use the following steps as a guide for publishing an update.</span></span>

1. <span data-ttu-id="08700-142">Modifiez le numéro de version dans le manifeste de votre extension. Le fichier JSON à un nombre supérieur à l’aide de la syntaxe suivante:`"version":"versionString"`.</span><span class="sxs-lookup"><span data-stu-id="08700-142">Change the version number in your extension's manifest.JSON file to a higher number using the following syntax: `"version":"versionString"`.</span></span> <span data-ttu-id="08700-143">Si la « version »:« 1.0 », vous pouvez mettre à jour vers « version »:« 1.1 » ou tout nombre supérieur à « 1.0 ».</span><span class="sxs-lookup"><span data-stu-id="08700-143">If the "version":"1.0", then you can update to "version":"1.1" or any number higher than "1.0".</span></span>
2. <span data-ttu-id="08700-144">Mettez à jour la « version » de `<updatecheck>`dans le fichier XML pour correspondre au numéro que vous avez placé dans le fichier manifeste à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="08700-144">Update the "version" of `<updatecheck>` in the XML file to match the number that you put in the manifest file in the previous step.</span></span> <span data-ttu-id="08700-145">Exemple:</span><span class="sxs-lookup"><span data-stu-id="08700-145">For example:</span></span><br>`<updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.1' />`
3. <span data-ttu-id="08700-146">Créez un fichier CRX qui inclut les nouvelles modifications.</span><span class="sxs-lookup"><span data-stu-id="08700-146">Create a CRX file that includes the new changes.</span></span> <span data-ttu-id="08700-147">Accédez à *edge://extensions* et activez **Mode Developeur**.</span><span class="sxs-lookup"><span data-stu-id="08700-147">Go to *edge://extensions* and enable **Developer mode**.</span></span>
4. <span data-ttu-id="08700-148">Cliquez sur**Extension Pack** et allez dans le répertoire de la source de l’extension.</span><span class="sxs-lookup"><span data-stu-id="08700-148">Click **Pack extension** and go to the directory for the extension source.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="08700-149">Utilisez le même fichier PEM qui a été généré et enregistré la première fois que le fichier CRX a été créé.</span><span class="sxs-lookup"><span data-stu-id="08700-149">Use the same PEM file that was generated and saved the first time the CRX file was created.</span></span> <span data-ttu-id="08700-150">Si vous n’utilisez pas le même fichier PEM, l’ID d’application de l’extension change et la mise à jour est traitée comme une nouvelle extension.</span><span class="sxs-lookup"><span data-stu-id="08700-150">If you don't use the same PEM file the app ID of the extension will change and the update will be treated as a new extension.</span></span>

5. <span data-ttu-id="08700-151">Faites glisser et déposez le fichier CRX dans la fenêtre d’extensions et vérifiez qu’il se charge.</span><span class="sxs-lookup"><span data-stu-id="08700-151">Drag and drop the CRX file into the extensions window and verify that it loads.</span></span>
6. <span data-ttu-id="08700-152">Testez l’extension mise à jour.</span><span class="sxs-lookup"><span data-stu-id="08700-152">Test the updated extension.</span></span>
7. <span data-ttu-id="08700-153">Remplacez l’ancien fichier CRX et le fichier XML par les nouveaux fichiers pour l’extension mise à jour.</span><span class="sxs-lookup"><span data-stu-id="08700-153">Replace the old CRX file and XML file with the new files for the updated extension.</span></span>

<span data-ttu-id="08700-154">Les modifications de l’extension seront récupérées pendant le prochain cycle de synchronisation de stratégie.</span><span class="sxs-lookup"><span data-stu-id="08700-154">The extension's changes will be picked up during the next policy sync cycle.</span></span> <span data-ttu-id="08700-155">Pour plus d’informations sur la mise à jour des extensions, consultez: [Mise à jour de l’URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) et[Mise à jour de manifeste](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).</span><span class="sxs-lookup"><span data-stu-id="08700-155">For more information about updating extensions, see: [Update URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) and [Update manifest](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).</span></span>

## <a name="distribute-a-privately-hosted-extension"></a><span data-ttu-id="08700-156">Distribuez une extension hébergée en privé</span><span class="sxs-lookup"><span data-stu-id="08700-156">Distribute a privately hosted extension</span></span>

<span data-ttu-id="08700-157">Vous pouvez partager le lien de l’emplacement où le fichier CRX est hébergé, et dès que les utilisateurs entrent l’URL dans leur navigateur, l’extension est téléchargée et installée.</span><span class="sxs-lookup"><span data-stu-id="08700-157">You can share the link of the location where the CRX file is hosted, and as soon as users enter the URL in their browser the extension will be downloaded and installed.</span></span> <span data-ttu-id="08700-158">Les utilisateurs peuvent activer l’extension à partir de edge://extensions page.</span><span class="sxs-lookup"><span data-stu-id="08700-158">Users can enable the extension from the edge://extensions page.</span></span> <span data-ttu-id="08700-159">Pour permettre aux utilisateurs d’installer des extensions auto-hébergées, ajoutez les IDs CRX d’extension à la stratégie [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist).</span><span class="sxs-lookup"><span data-stu-id="08700-159">To allow users to install self-hosted extensions, you need to add the extension CRX IDs to the [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist) policy.</span></span>

<span data-ttu-id="08700-160">Vous pouvez également utiliser la stratégie de groupe [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) pour forcer l’installation d’une extension sur les appareils de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="08700-160">Alternatively, you can use group policy [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) to Force-install an extension on your users’ devices.</span></span>

<span data-ttu-id="08700-161">Vous pouvez appliquer ces stratégies à vos utilisateurs, appareils sélectionnés ou les deux.</span><span class="sxs-lookup"><span data-stu-id="08700-161">You can apply these policies to your selected users, devices, or both.</span></span> <span data-ttu-id="08700-162">N’oubliez pas que les mises à jour de stratégie ne sont pas instantanées et qu’il faudra du temps aux paramètres de stratégie pour prendre effet.</span><span class="sxs-lookup"><span data-stu-id="08700-162">Remember though that policy updates are not instantaneous, and it will take time for the policy settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="08700-163">Voir également</span><span class="sxs-lookup"><span data-stu-id="08700-163">See also</span></span>

- [<span data-ttu-id="08700-164">Gérer les extensions Microsoft Edge dans l’entreprise</span><span class="sxs-lookup"><span data-stu-id="08700-164">Manage Microsoft Edge extensions in the enterprise</span></span>](microsoft-edge-manage-extensions.md)
- [<span data-ttu-id="08700-165">Utiliser des stratégies de groupe pour gérer les extensions Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="08700-165">Use group policies to manage Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-policies.md)
- [<span data-ttu-id="08700-166">Guide détaillé de la stratégie ExtensionSettings</span><span class="sxs-lookup"><span data-stu-id="08700-166">Detailed guide to the ExtensionSettings policy</span></span>](microsoft-edge-manage-extensions-ref-guide.md)
- [<span data-ttu-id="08700-167">FAQ sur les extensions Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="08700-167">FAQ for Microsoft Edge Extensions</span></span>](microsoft-edge-manage-extensions-faq.md)
- [<span data-ttu-id="08700-168">Page d’accueil Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="08700-168">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
