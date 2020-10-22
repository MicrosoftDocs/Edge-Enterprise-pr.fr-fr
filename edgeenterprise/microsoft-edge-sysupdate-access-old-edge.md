---
title: Accéder à l’ancienne version de MicrosoftEdge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 08/17/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez comment accéder à la version héritée de MicrosoftEdge.
ms.openlocfilehash: e4733d020f3a681ded50e5a087fe086d39362201
ms.sourcegitcommit: f7f7eb69d2298b0f9779a9fd28e3c4e297ef2e05
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125516"
---
# <span data-ttu-id="3746e-103">Accéder à la version héritée de MicrosoftEdge après avoir installé la nouvelle version de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="3746e-103">Access Microsoft Edge Legacy after installing the new version of Microsoft Edge</span></span>

<span data-ttu-id="3746e-104">Découvrez comment accéder à la version héritée de MicrosoftEdge après avoir installé la nouvelle version de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="3746e-104">Learn how to access Microsoft Edge Legacy after installing the new version of Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="3746e-105">Cet article concerne le [canal stable](microsoft-edge-channels.md) de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="3746e-105">This article applies to the Microsoft Edge [Stable channel](microsoft-edge-channels.md).</span></span>

<span data-ttu-id="3746e-106">Bien que la plupart des organisations souhaiteront remplacer l’héritage Microsoft Edge par la nouvelle version, il existe certaines situations dans lesquelles les utilisateurs auront besoin d’accéder à ces deux versions.</span><span class="sxs-lookup"><span data-stu-id="3746e-106">While most organizations will want to replace Microsoft Edge Legacy with the new version, there are some situations where users will need access to both versions.</span></span> <span data-ttu-id="3746e-107">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="3746e-107">For example:</span></span>

- <span data-ttu-id="3746e-108">Support technique et techniciens du support qui interagissent avec les utilisateurs qui utilisent la version de Microsoft Edge, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="3746e-108">Helpdesk and support staff who interact with users who are using either or both versions of Microsoft Edge.</span></span>
- <span data-ttu-id="3746e-109">Développeurs prenant en charge des clients qui utilisent la version de Microsoft Edge, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="3746e-109">Developers who support customers who are using either or both versions of Microsoft Edge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3746e-110">Il n’est pas recommandé d’utiliser l’application Microsoft Edge Legacy côte à côte avec la nouvelle version de Microsoft Edge en production.</span><span class="sxs-lookup"><span data-stu-id="3746e-110">Running Microsoft Edge Legacy side-by-side with the new version of Microsoft Edge is not recommended for use in production.</span></span> <span data-ttu-id="3746e-111">Cette configuration ne doit être utilisée que dans les cas spécifiques où des tests avec les deux versions du navigateur sont requis.</span><span class="sxs-lookup"><span data-stu-id="3746e-111">This configuration should only be used in specific cases where testing with both browser versions is required.</span></span>
>
> <span data-ttu-id="3746e-112">L’ Assistance pour l’application de bureau de Microsoft Edge arrivera à terme le 9 mars 2021 en faveur de la nouvelle application Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3746e-112">The Microsoft Edge Legacy desktop app will reach end of support on March 9, 2021 in favor of the new Microsoft Edge.</span></span> <span data-ttu-id="3746e-113">Cela signifie que Microsoft Edge Legacy ne recevra pas de mises à jour de sécurité après cette date.</span><span class="sxs-lookup"><span data-stu-id="3746e-113">This means that Microsoft Edge Legacy will not receive security updates after that date.</span></span> <span data-ttu-id="3746e-114">Ce changement est applicable à toutes les options qui sont exécutées dans l’application de bureau de Microsoft Edge Legacy.</span><span class="sxs-lookup"><span data-stu-id="3746e-114">This change is applicable to all experiences that run in the Microsoft Edge Legacy desktop app.</span></span> <span data-ttu-id="3746e-115">[En savoir plus](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span><span class="sxs-lookup"><span data-stu-id="3746e-115">[Learn more](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span></span>

## <span data-ttu-id="3746e-116">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="3746e-116">Before you begin</span></span>
> [!NOTE]
> <span data-ttu-id="3746e-117">À compter de Windows 10 version20H2, nous n’incluons plus l’ancienne version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3746e-117">Starting with Windows 10 version 20H2 Microsoft Edge Legacy is no longer included.</span></span> <span data-ttu-id="3746e-118">À compter de cette version de Windows 10, nous ne prenons plus en charge l’expérience côte à côte.</span><span class="sxs-lookup"><span data-stu-id="3746e-118">Starting with this version of Windows 10 the side-by-side experience is not supported.</span></span>

<span data-ttu-id="3746e-119">Les procédures présentées dans cet article s’appliquent aux systèmes qui ont été mis à jour avec les dernières mises à jour de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3746e-119">The procedures in this article apply to systems that have been updated with the latest security updates.</span></span> <span data-ttu-id="3746e-120">Lorsque la nouvelle version de MicrosoftEdge est installée, l’ancienne version (MicrosoftEdge héritée) est masquée.</span><span class="sxs-lookup"><span data-stu-id="3746e-120">When the new version of Microsoft Edge is installed, the old version (Microsoft Edge Legacy) will be hidden.</span></span> <span data-ttu-id="3746e-121">Par défaut, toutes les tentatives de lancement de l’ancienne version de MicrosoftEdge redirigent l’utilisateur vers la nouvelle version de MicrosoftEdge installée.</span><span class="sxs-lookup"><span data-stu-id="3746e-121">By default, all attempts to launch the old version will redirect the user to the newly installed version of Microsoft Edge.</span></span> <span data-ttu-id="3746e-122">Cet article décrit la manière dont vous pouvez continuer à utiliser le langage hérité Microsoft Edge après l’installation de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3746e-122">This article describes how you can keep using Microsoft Edge Legacy after you install Microsoft Edge.</span></span>

## <span data-ttu-id="3746e-123">Démarrage rapide: Option côte à côte avec la Chaine Beta de Microsoft Edge et Microsoft Edge Legacy</span><span class="sxs-lookup"><span data-stu-id="3746e-123">Quickstart: Side-by-side experience with Microsoft Edge Beta Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="3746e-124">Avant d’utiliser les instructions détaillées de cet article, prenez en compte les deux étapes suivantes pour permettre à vos utilisateurs d’exécuter Microsoft Edge Legacy et la chaine Beta de [ Microsoft Edge](microsoft-edge-channels.md) cote à cote.</span><span class="sxs-lookup"><span data-stu-id="3746e-124">Before using the detailed instructions in this article, consider the following two steps to let your users run Microsoft Edge Legacy and the Microsoft Edge [Beta channel](microsoft-edge-channels.md) side-by-side.</span></span>

1. <span data-ttu-id="3746e-125">Empêchez l’installation automatique du canal stable MicrosoftEdge par [Windows Update.](https://support.microsoft.com/help/12373/windows-update-faq)</span><span class="sxs-lookup"><span data-stu-id="3746e-125">Prevent the automatic install of the Stable Channel of Microsoft Edge by [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).</span></span>

   > [!TIP]
   > <span data-ttu-id="3746e-126">Utilisez [Blocker Toolkit](microsoft-edge-blocker-toolkit.md) pour désactiver la distribution automatique de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="3746e-126">Use the [Blocker Toolkit](microsoft-edge-blocker-toolkit.md) to disable automatic delivery of Microsoft Edge.</span></span>

2. <span data-ttu-id="3746e-127">Installez le [canal bêta](https://www.microsoft.com/edge/business/download) de la nouvelle version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3746e-127">Install the [Beta channel](https://www.microsoft.com/edge/business/download) of the new version of Microsoft Edge.</span></span>

   > [!NOTE]
   > <span data-ttu-id="3746e-128">Lisez [informations supplémentaires](#additional-information) pour plus d’informations sur les paramètres de clé de registre.</span><span class="sxs-lookup"><span data-stu-id="3746e-128">Read [Additional information](#additional-information) for information about Registry Key settings.</span></span>

<span data-ttu-id="3746e-129">Cette solution côte à côte est moins complexe et nécessite moins de gestion que la solution détaillée décrite dans cet article.</span><span class="sxs-lookup"><span data-stu-id="3746e-129">This side-by-side solution is less complex and requires less management than the detailed solution described in this article.</span></span> <span data-ttu-id="3746e-130">Toutefois, cette solution signifie que vous exécutez la Chaine Beta, plutôt que la Chaine Stable.</span><span class="sxs-lookup"><span data-stu-id="3746e-130">However, this solution does mean that you'll be running the Beta Channel rather than the Stable Channel.</span></span>

## <span data-ttu-id="3746e-131">L’option côte à côte avec la Chaine Stable de Microsoft Edge et Microsoft Edge Legacy</span><span class="sxs-lookup"><span data-stu-id="3746e-131">Side-by-side experience with Microsoft Edge Stable Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="3746e-132">L’installation du canal stable de la nouvelle version de Microsoft Edge au niveau système entraînera le masquage de la version actuelle (le contrôle de l’ancienne version de Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="3746e-132">Installing the Stable Channel of the next version of Microsoft Edge at the system-level will cause the current version (Microsoft Edge Legacy) to be hidden.</span></span> <span data-ttu-id="3746e-133">Si vous voulez permettre aux utilisateurs de voir les deux versions de Microsoft Edge côte à côte dans Windows, vous pouvez activer cette option en définissant l’option **autoriser le navigateur Microsoft Edge côte** à côte sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="3746e-133">If you want to let your users see both versions of Microsoft Edge side by side in Windows, you can enable this experience by setting the **Allow Microsoft Edge Side by Side browser experience** group policy to **Enabled**.</span></span>

<span data-ttu-id="3746e-134">Cette stratégie de groupe est documentée [ici](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)</span><span class="sxs-lookup"><span data-stu-id="3746e-134">This group policy is documented [here](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)</span></span>

### <span data-ttu-id="3746e-135">Pour configurer la stratégie d’interface de navigateur côte à côte:</span><span class="sxs-lookup"><span data-stu-id="3746e-135">To set up the side-by-side browser experience policy:</span></span>

1. <span data-ttu-id="3746e-136">Installez les définitions de stratégie à partir de [Microsoft Edge pour les entreprises](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="3746e-136">Install the Policy Definitions from [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span></span>

   - <span data-ttu-id="3746e-137">Choisissez le canal/la construction et la plateforme que vous voulez utiliser, puis cliquez sur obtenir des fichiers de stratégie.</span><span class="sxs-lookup"><span data-stu-id="3746e-137">Pick the CHANNEL/BUILD and PLATFORM you want to use, and then click GET POLICY FILES.</span></span>
   - <span data-ttu-id="3746e-138">Extrayez les fichiers zip.</span><span class="sxs-lookup"><span data-stu-id="3746e-138">Extract the zipped files.</span></span>
   - <span data-ttu-id="3746e-139">Copiez msedge.admx et msedgeupdate.admx dans le répertoire `C:\Windows\PolicyDefinitions`.</span><span class="sxs-lookup"><span data-stu-id="3746e-139">Copy msedge.admx and msedgeupdate.admx to the `C:\Windows\PolicyDefinitions` directory.</span></span>
   - <span data-ttu-id="3746e-140">Copiez msedge. adml et msedgeupdate. adml (à partir du répertoire Language/locale approprié) vers `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` le répertoire.</span><span class="sxs-lookup"><span data-stu-id="3746e-140">Copy msedge.adml and msedgeupdate.adml (from the appropriate language/locale directory) to the `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` directory.</span></span>

2. <span data-ttu-id="3746e-141">Ouvrez l’éditeur de stratégies de groupe (gpedit.msc).</span><span class="sxs-lookup"><span data-stu-id="3746e-141">Open the Group Policy Editor (gpedit.msc).</span></span>
3. <span data-ttu-id="3746e-142">Sous **Configuration de l’ordinateur**, accédez à *Modèles d’administration > Microsoft Edge Update > Applications*.</span><span class="sxs-lookup"><span data-stu-id="3746e-142">Under **Computer Configuration**, go to *Administrative Templates>Microsoft Edge Update>Applications*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3746e-143">Si vous ne voyez pas le dossier *Microsoft Edge Update* , vérifiez que l’étape 1 s’est correctement effectuée.</span><span class="sxs-lookup"><span data-stu-id="3746e-143">If you don't see the *Microsoft Edge Update* folder, verify that step 1 was completed correctly.</span></span>

4. <span data-ttu-id="3746e-144">Sous **Applications**, double-cliquez sur «Autoriser l’expérience de navigateur côte à côte MicrosoftEdge».</span><span class="sxs-lookup"><span data-stu-id="3746e-144">Under **Applications**, double-click "Allow Microsoft Edge Side by Side browser experience".</span></span> <span data-ttu-id="3746e-145">Consultez notre [guide des bonnes pratiques](#best-practice-guidance) avant de passer à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="3746e-145">See our [best practice guidance](#best-practice-guidance) before continuing to the next step.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3746e-146">Par défaut, cette stratégie de groupe est définie sur «Non configurée», ce qui entraîne le masquage de la version héritée de MicrosoftEdge lors de l’installation de la nouvelle version de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="3746e-146">By default, this group policy is set to "Not configured", which results in Microsoft Edge Legacy being hidden when the new version of Microsoft Edge is installed.</span></span>

5. <span data-ttu-id="3746e-147">Sélectionnez **Activé**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3746e-147">Select **Enabled** and then click **OK**.</span></span>  

<span data-ttu-id="3746e-148">La définition de cette stratégie définira la clé de Registre suivante sur «00000001»:</span><span class="sxs-lookup"><span data-stu-id="3746e-148">Setting this policy will set the following Registry Key  to '00000001':</span></span>

- <span data-ttu-id="3746e-149">Clé:</span><span class="sxs-lookup"><span data-stu-id="3746e-149">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- <span data-ttu-id="3746e-150">Nom de valeur:</span><span class="sxs-lookup"><span data-stu-id="3746e-150">Value Name:</span></span> `Allowsxs`
- <span data-ttu-id="3746e-151">Type de la valeur:</span><span class="sxs-lookup"><span data-stu-id="3746e-151">Value Type:</span></span> `'REG_DWORD'`

#### <span data-ttu-id="3746e-152">Guide des bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="3746e-152">Best practice guidance</span></span>

<span data-ttu-id="3746e-153">Pour une expérience optimale, la stratégie **Autoriser l’expérience de navigateur côte à côte MicrosoftEdge** doit être activée avant le déploiement de la nouvelle version de MicrosoftEdge sur les appareils de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="3746e-153">For the best experience, the **Allow Microsoft Edge Side by Side browser experience** should be enabled before the new version of Microsoft Edge is deployed to your users' devices.</span></span>

<span data-ttu-id="3746e-154">Si elle est activée après le déploiement de MicrosoftEdge, les effets secondaires suivants se produisent et les actions suivantes sont requises:</span><span class="sxs-lookup"><span data-stu-id="3746e-154">If the group policy is enabled after Microsoft Edge is deployed, there are the following side effects and required actions:</span></span>

1. <span data-ttu-id="3746e-155">**Autoriser l’expérience de navigateur côte à côte MicrosoftEdge** ne prend effet que lorsque le programme d’installation de la nouvelle version de MicrosoftEdge est exécuté à nouveau.</span><span class="sxs-lookup"><span data-stu-id="3746e-155">**Allow Microsoft Edge Side by Side browser experience** won't take effect until after the installer for the new version of Microsoft Edge is run again.</span></span>

   > [!NOTE]
   > <span data-ttu-id="3746e-156">Le programme d’installation peut être exécuté directement ou automatiquement lorsque la nouvelle version de MicrosoftEdge est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3746e-156">The installer can be run directly or automatically when the new version of Microsoft Edge updates.</span></span>

2. <span data-ttu-id="3746e-157">La version héritée de MicrosoftEdge doit être épinglée à nouveau à l’écran de démarrage ou à la barre des tâches, car l’épinglage est migré lors du déploiement de la nouvelle version de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="3746e-157">Microsoft Edge Legacy will need to be re-pinned to Start or the Taskbar because the pin is migrated when the new version of Microsoft Edge is deployed.</span></span>
3. <span data-ttu-id="3746e-158">Les sites qui étaient épinglés à l’écran de démarrage ou à la barre des tâches pour la version héritée de MicrosoftEdge seront migrés vers la nouvelle version de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="3746e-158">Sites that were pinned to Start or the Taskbar for Microsoft Edge Legacy will be migrated to the new version of Microsoft Edge.</span></span>

## <span data-ttu-id="3746e-159">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="3746e-159">Additional information</span></span>

<span data-ttu-id="3746e-160">Une fois que les systèmes sont entièrement mis à jour et que le canal stable de la version suivante de MicrosoftEdge est installé, la clé de Registre et la valeur de Registre suivantes sont définies:</span><span class="sxs-lookup"><span data-stu-id="3746e-160">After the systems are fully updated and the Stable channel of the next version of Microsoft Edge is installed, the following registry key and value is set:</span></span>

- <span data-ttu-id="3746e-161">Clé:</span><span class="sxs-lookup"><span data-stu-id="3746e-161">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- <span data-ttu-id="3746e-162">Valeur de clé:</span><span class="sxs-lookup"><span data-stu-id="3746e-162">Key value:</span></span> `BrowserReplacement`

  > [!IMPORTANT]
  > <span data-ttu-id="3746e-163">Cette clé est écrasée chaque fois que le canal stable MicrosoftEdge est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3746e-163">This key is over-written every time the Microsoft Edge Stable channel is updated.</span></span> <span data-ttu-id="3746e-164">Il est recommandé de NE PAS supprimer cette clé, afin de permettre aux utilisateurs d’accéder aux deux versions de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="3746e-164">As a best practice, we recommend that you DO NOT delete this key to allow users to access both versions of Microsoft Edge.</span></span>

## <span data-ttu-id="3746e-165">Voir également</span><span class="sxs-lookup"><span data-stu-id="3746e-165">See also</span></span>

- [<span data-ttu-id="3746e-166">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="3746e-166">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="3746e-167">Mises à jour Windows pour prendre en charge MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="3746e-167">Windows updates to support Microsoft Edge</span></span>](microsoft-edge-sysupdate-windows-updates.md)
