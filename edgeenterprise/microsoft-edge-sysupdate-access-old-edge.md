---
title: Accéder à l’ancienne version de MicrosoftEdge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez comment accéder à la version héritée de MicrosoftEdge.
ms.openlocfilehash: b521ab9ea093b62db7268e6bf2f4d656b3dc8d4b
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447088"
---
# <a name="access-microsoft-edge-legacy-after-installing-the-new-version-of-microsoft-edge"></a><span data-ttu-id="bfb7e-103">Accéder à la version héritée de MicrosoftEdge après avoir installé la nouvelle version de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="bfb7e-103">Access Microsoft Edge Legacy after installing the new version of Microsoft Edge</span></span>

<span data-ttu-id="bfb7e-104">L’ancienne version de Microsoft Edge cessera de recevoir les mises à jour de sécurité le 9 mars 2021.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-104">Microsoft Edge Legacy will stop receiving security updates on March 9, 2021.</span></span> <span data-ttu-id="bfb7e-105">Vous pouvez accéder à l’ancienne version de Microsoft Edge jusqu’au 13 avril.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-105">You can access Microsoft Edge Legacy until April 13.</span></span> <span data-ttu-id="bfb7e-106">Pour plus d’informations, consultez [le billet de blog](https://aka.ms/EdgeLegacyEOS)de l’équipe produit Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-106">For more information, see Microsoft Edge Product Team’s [blog post](https://aka.ms/EdgeLegacyEOS).</span></span>

> [!NOTE]
> <span data-ttu-id="bfb7e-107">Cet article concerne le [canal stable](microsoft-edge-channels.md) de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-107">This article applies to the Microsoft Edge [Stable channel](microsoft-edge-channels.md).</span></span>

<span data-ttu-id="bfb7e-108">Bien que la plupart des organisations souhaiteront remplacer l’héritage Microsoft Edge par la nouvelle version, il existe certaines situations dans lesquelles les utilisateurs auront besoin d’accéder à ces deux versions.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-108">While most organizations will want to replace Microsoft Edge Legacy with the new version, there are some situations where users will need access to both versions.</span></span> <span data-ttu-id="bfb7e-109">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="bfb7e-109">For example:</span></span>

- <span data-ttu-id="bfb7e-110">Support technique et techniciens du support qui interagissent avec les utilisateurs qui utilisent la version de Microsoft Edge, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-110">Helpdesk and support staff who interact with users who are using either or both versions of Microsoft Edge.</span></span>
- <span data-ttu-id="bfb7e-111">Développeurs prenant en charge des clients qui utilisent la version de Microsoft Edge, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-111">Developers who support customers who are using either or both versions of Microsoft Edge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bfb7e-112">Il n’est pas recommandé d’utiliser l’application Microsoft Edge Legacy côte à côte avec la nouvelle version de Microsoft Edge en production.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-112">Running Microsoft Edge Legacy side-by-side with the new version of Microsoft Edge is not recommended for use in production.</span></span> <span data-ttu-id="bfb7e-113">Cette configuration ne doit être utilisée que dans les cas spécifiques où des tests avec les deux versions du navigateur sont requis.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-113">This configuration should only be used in specific cases where testing with both browser versions is required.</span></span>
>
> <span data-ttu-id="bfb7e-114">L’ Assistance pour l’application de bureau de Microsoft Edge arrivera à terme le 9 mars 2021 en faveur de la nouvelle application Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-114">The Microsoft Edge Legacy desktop app will reach end of support on March 9, 2021 in favor of the new Microsoft Edge.</span></span> <span data-ttu-id="bfb7e-115">Cela signifie que Microsoft Edge Legacy ne recevra pas de mises à jour de sécurité après cette date.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-115">This means that Microsoft Edge Legacy will not receive security updates after that date.</span></span> <span data-ttu-id="bfb7e-116">Ce changement est applicable à toutes les options qui sont exécutées dans l’application de bureau de Microsoft Edge Legacy.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-116">This change is applicable to all experiences that run in the Microsoft Edge Legacy desktop app.</span></span> <span data-ttu-id="bfb7e-117">[En savoir plus](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span><span class="sxs-lookup"><span data-stu-id="bfb7e-117">[Learn more](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="bfb7e-118">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="bfb7e-118">Before you begin</span></span>
> [!NOTE]
> <span data-ttu-id="bfb7e-119">À compter de Windows 10 version20H2, nous n’incluons plus l’ancienne version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-119">Starting with Windows 10 version 20H2 Microsoft Edge Legacy is no longer included.</span></span> <span data-ttu-id="bfb7e-120">À compter de cette version de Windows 10, nous ne prenons plus en charge l’expérience côte à côte.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-120">Starting with this version of Windows 10 the side-by-side experience is not supported.</span></span>

<span data-ttu-id="bfb7e-121">Les procédures présentées dans cet article s’appliquent aux systèmes qui ont été mis à jour avec les dernières mises à jour de sécurité.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-121">The procedures in this article apply to systems that have been updated with the latest security updates.</span></span> <span data-ttu-id="bfb7e-122">Lorsque la nouvelle version de MicrosoftEdge est installée, l’ancienne version (MicrosoftEdge héritée) est masquée.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-122">When the new version of Microsoft Edge is installed, the old version (Microsoft Edge Legacy) will be hidden.</span></span> <span data-ttu-id="bfb7e-123">Par défaut, toutes les tentatives de lancement de l’ancienne version de MicrosoftEdge redirigent l’utilisateur vers la nouvelle version de MicrosoftEdge installée.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-123">By default, all attempts to launch the old version will redirect the user to the newly installed version of Microsoft Edge.</span></span> <span data-ttu-id="bfb7e-124">Cet article décrit la manière dont vous pouvez continuer à utiliser le langage hérité Microsoft Edge après l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-124">This article describes how you can keep using Microsoft Edge Legacy after you install Microsoft Edge.</span></span>

## <a name="quickstart-side-by-side-experience-with-microsoft-edge-beta-channel-and-microsoft-edge-legacy"></a><span data-ttu-id="bfb7e-125">Démarrage rapide: Option côte à côte avec la Chaine Beta de Microsoft Edge et Microsoft Edge Legacy</span><span class="sxs-lookup"><span data-stu-id="bfb7e-125">Quickstart: Side-by-side experience with Microsoft Edge Beta Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="bfb7e-126">Avant d’utiliser les instructions détaillées de cet article, prenez en compte les deux étapes suivantes pour permettre à vos utilisateurs d’exécuter Microsoft Edge Legacy et la chaine Beta de [ Microsoft Edge](microsoft-edge-channels.md) cote à cote.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-126">Before using the detailed instructions in this article, consider the following two steps to let your users run Microsoft Edge Legacy and the Microsoft Edge [Beta channel](microsoft-edge-channels.md) side-by-side.</span></span>

1. <span data-ttu-id="bfb7e-127">Empêchez l’installation automatique du canal stable MicrosoftEdge par [Windows Update.](https://support.microsoft.com/help/12373/windows-update-faq)</span><span class="sxs-lookup"><span data-stu-id="bfb7e-127">Prevent the automatic install of the Stable Channel of Microsoft Edge by [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).</span></span>
2. <span data-ttu-id="bfb7e-128">Installez le [canal bêta](https://www.microsoft.com/edge/business/download) de la nouvelle version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-128">Install the [Beta channel](https://www.microsoft.com/edge/business/download) of the new version of Microsoft Edge.</span></span>

   > [!NOTE]
   > <span data-ttu-id="bfb7e-129">Lisez [informations supplémentaires](#additional-information) pour plus d’informations sur les paramètres de clé de registre.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-129">Read [Additional information](#additional-information) for information about Registry Key settings.</span></span>

<span data-ttu-id="bfb7e-130">Cette solution côte à côte est moins complexe et nécessite moins de gestion que la solution détaillée décrite dans cet article.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-130">This side-by-side solution is less complex and requires less management than the detailed solution described in this article.</span></span> <span data-ttu-id="bfb7e-131">Toutefois, cette solution signifie que vous exécutez la Chaine Beta, plutôt que la Chaine Stable.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-131">However, this solution does mean that you'll be running the Beta Channel rather than the Stable Channel.</span></span>

## <a name="side-by-side-experience-with-microsoft-edge-stable-channel-and-microsoft-edge-legacy"></a><span data-ttu-id="bfb7e-132">L’option côte à côte avec la Chaine Stable de Microsoft Edge et Microsoft Edge Legacy</span><span class="sxs-lookup"><span data-stu-id="bfb7e-132">Side-by-side experience with Microsoft Edge Stable Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="bfb7e-133">L’installation du canal stable de la nouvelle version de Microsoft Edge au niveau système entraînera le masquage de la version actuelle (le contrôle de l’ancienne version de Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="bfb7e-133">Installing the Stable Channel of the next version of Microsoft Edge at the system-level will cause the current version (Microsoft Edge Legacy) to be hidden.</span></span> <span data-ttu-id="bfb7e-134">Si vous voulez permettre aux utilisateurs de voir les deux versions de Microsoft Edge côte à côte dans Windows, vous pouvez activer cette option en définissant l’option **autoriser le navigateur Microsoft Edge côte** à côte sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-134">If you want to let your users see both versions of Microsoft Edge side by side in Windows, you can enable this experience by setting the **Allow Microsoft Edge Side by Side browser experience** group policy to **Enabled**.</span></span>

<span data-ttu-id="bfb7e-135">Cette stratégie de groupe est documentée [ici](./microsoft-edge-update-policies.md#allowsxs)</span><span class="sxs-lookup"><span data-stu-id="bfb7e-135">This group policy is documented [here](./microsoft-edge-update-policies.md#allowsxs)</span></span>

### <a name="to-set-up-the-side-by-side-browser-experience-policy"></a><span data-ttu-id="bfb7e-136">Pour configurer la stratégie d’interface de navigateur côte à côte:</span><span class="sxs-lookup"><span data-stu-id="bfb7e-136">To set up the side-by-side browser experience policy:</span></span>

1. <span data-ttu-id="bfb7e-137">Installez les définitions de stratégie à partir de [Microsoft Edge pour les entreprises](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="bfb7e-137">Install the Policy Definitions from [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span></span>

   - <span data-ttu-id="bfb7e-138">Choisissez le canal/la construction et la plateforme que vous voulez utiliser, puis cliquez sur obtenir des fichiers de stratégie.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-138">Pick the CHANNEL/BUILD and PLATFORM you want to use, and then click GET POLICY FILES.</span></span>
   - <span data-ttu-id="bfb7e-139">Extrayez les fichiers zip.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-139">Extract the zipped files.</span></span>
   - <span data-ttu-id="bfb7e-140">Copiez msedge.admx et msedgeupdate.admx dans le répertoire `C:\Windows\PolicyDefinitions`.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-140">Copy msedge.admx and msedgeupdate.admx to the `C:\Windows\PolicyDefinitions` directory.</span></span>
   - <span data-ttu-id="bfb7e-141">Copiez msedge. adml et msedgeupdate. adml (à partir du répertoire Language/locale approprié) vers `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` le répertoire.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-141">Copy msedge.adml and msedgeupdate.adml (from the appropriate language/locale directory) to the `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` directory.</span></span>

2. <span data-ttu-id="bfb7e-142">Ouvrez l’éditeur de stratégies de groupe (gpedit.msc).</span><span class="sxs-lookup"><span data-stu-id="bfb7e-142">Open the Group Policy Editor (gpedit.msc).</span></span>
3. <span data-ttu-id="bfb7e-143">Sous **Configuration de l’ordinateur**, accédez à *Modèles d’administration > Microsoft Edge Update > Applications*.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-143">Under **Computer Configuration**, go to *Administrative Templates>Microsoft Edge Update>Applications*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bfb7e-144">Si vous ne voyez pas le dossier *Microsoft Edge Update* , vérifiez que l’étape 1 s’est correctement effectuée.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-144">If you don't see the *Microsoft Edge Update* folder, verify that step 1 was completed correctly.</span></span>

4. <span data-ttu-id="bfb7e-145">Sous **Applications**, double-cliquez sur «Autoriser l’expérience de navigateur côte à côte MicrosoftEdge».</span><span class="sxs-lookup"><span data-stu-id="bfb7e-145">Under **Applications**, double-click "Allow Microsoft Edge Side by Side browser experience".</span></span> <span data-ttu-id="bfb7e-146">Consultez notre [guide des bonnes pratiques](#best-practice-guidance) avant de passer à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-146">See our [best practice guidance](#best-practice-guidance) before continuing to the next step.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bfb7e-147">Par défaut, cette stratégie de groupe est définie sur «Non configurée», ce qui entraîne le masquage de la version héritée de MicrosoftEdge lors de l’installation de la nouvelle version de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-147">By default, this group policy is set to "Not configured", which results in Microsoft Edge Legacy being hidden when the new version of Microsoft Edge is installed.</span></span>

5. <span data-ttu-id="bfb7e-148">Sélectionnez **Activé**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-148">Select **Enabled** and then click **OK**.</span></span>  

<span data-ttu-id="bfb7e-149">La définition de cette stratégie définira la clé de Registre suivante sur «00000001»:</span><span class="sxs-lookup"><span data-stu-id="bfb7e-149">Setting this policy will set the following Registry Key  to '00000001':</span></span>

- <span data-ttu-id="bfb7e-150">Clé:</span><span class="sxs-lookup"><span data-stu-id="bfb7e-150">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- <span data-ttu-id="bfb7e-151">Nom de valeur:</span><span class="sxs-lookup"><span data-stu-id="bfb7e-151">Value Name:</span></span> `Allowsxs`
- <span data-ttu-id="bfb7e-152">Type de la valeur:</span><span class="sxs-lookup"><span data-stu-id="bfb7e-152">Value Type:</span></span> `'REG_DWORD'`

#### <a name="best-practice-guidance"></a><span data-ttu-id="bfb7e-153">Guide des bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="bfb7e-153">Best practice guidance</span></span>

<span data-ttu-id="bfb7e-154">Pour une expérience optimale, la stratégie **Autoriser l’expérience de navigateur côte à côte MicrosoftEdge** doit être activée avant le déploiement de la nouvelle version de MicrosoftEdge sur les appareils de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-154">For the best experience, the **Allow Microsoft Edge Side by Side browser experience** should be enabled before the new version of Microsoft Edge is deployed to your users' devices.</span></span>

<span data-ttu-id="bfb7e-155">Si elle est activée après le déploiement de MicrosoftEdge, les effets secondaires suivants se produisent et les actions suivantes sont requises:</span><span class="sxs-lookup"><span data-stu-id="bfb7e-155">If the group policy is enabled after Microsoft Edge is deployed, there are the following side effects and required actions:</span></span>

1. <span data-ttu-id="bfb7e-156">**Autoriser l’expérience de navigateur côte à côte MicrosoftEdge** ne prend effet que lorsque le programme d’installation de la nouvelle version de MicrosoftEdge est exécuté à nouveau.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-156">**Allow Microsoft Edge Side by Side browser experience** won't take effect until after the installer for the new version of Microsoft Edge is run again.</span></span>

   > [!NOTE]
   > <span data-ttu-id="bfb7e-157">Le programme d’installation peut être exécuté directement ou automatiquement lorsque la nouvelle version de MicrosoftEdge est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-157">The installer can be run directly or automatically when the new version of Microsoft Edge updates.</span></span>

2. <span data-ttu-id="bfb7e-158">La version héritée de MicrosoftEdge doit être épinglée à nouveau à l’écran de démarrage ou à la barre des tâches, car l’épinglage est migré lors du déploiement de la nouvelle version de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-158">Microsoft Edge Legacy will need to be re-pinned to Start or the Taskbar because the pin is migrated when the new version of Microsoft Edge is deployed.</span></span>
3. <span data-ttu-id="bfb7e-159">Les sites qui étaient épinglés à l’écran de démarrage ou à la barre des tâches pour la version héritée de MicrosoftEdge seront migrés vers la nouvelle version de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-159">Sites that were pinned to Start or the Taskbar for Microsoft Edge Legacy will be migrated to the new version of Microsoft Edge.</span></span>

## <a name="additional-information"></a><span data-ttu-id="bfb7e-160">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="bfb7e-160">Additional information</span></span>

<span data-ttu-id="bfb7e-161">Une fois que les systèmes sont entièrement mis à jour et que le canal stable de la version suivante de MicrosoftEdge est installé, la clé de Registre et la valeur de Registre suivantes sont définies:</span><span class="sxs-lookup"><span data-stu-id="bfb7e-161">After the systems are fully updated and the Stable channel of the next version of Microsoft Edge is installed, the following registry key and value is set:</span></span>

- <span data-ttu-id="bfb7e-162">Clé:</span><span class="sxs-lookup"><span data-stu-id="bfb7e-162">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- <span data-ttu-id="bfb7e-163">Valeur de clé:</span><span class="sxs-lookup"><span data-stu-id="bfb7e-163">Key value:</span></span> `BrowserReplacement`

  > [!IMPORTANT]
  > <span data-ttu-id="bfb7e-164">Cette clé est écrasée chaque fois que le canal stable MicrosoftEdge est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-164">This key is over-written every time the Microsoft Edge Stable channel is updated.</span></span> <span data-ttu-id="bfb7e-165">Il est recommandé de NE PAS supprimer cette clé, afin de permettre aux utilisateurs d’accéder aux deux versions de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="bfb7e-165">As a best practice, we recommend that you DO NOT delete this key to allow users to access both versions of Microsoft Edge.</span></span>

## <a name="see-also"></a><span data-ttu-id="bfb7e-166">Voir également</span><span class="sxs-lookup"><span data-stu-id="bfb7e-166">See also</span></span>

- [<span data-ttu-id="bfb7e-167">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="bfb7e-167">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="bfb7e-168">Mises à jour Windows pour prendre en charge MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="bfb7e-168">Windows updates to support Microsoft Edge</span></span>](microsoft-edge-sysupdate-windows-updates.md)