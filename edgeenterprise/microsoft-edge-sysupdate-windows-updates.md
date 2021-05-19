---
title: Mises à jour Windows pour Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Mises à jour Windows pour Microsoft Edge.
ms.openlocfilehash: 953becc459fe729f84d54da419481b3c6e26cc47
ms.sourcegitcommit: 16a92a51560fdba6f6480e4533453348f026c7ef
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313904"
---
# <span data-ttu-id="5d123-103">Mises à jour Windows pour prendre en charge la prochaine version de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5d123-103">Windows updates to support the next version of Microsoft Edge</span></span>

<span data-ttu-id="5d123-104">Cet article décrit comment Windows sera mis à jour pour prendre en charge la prochaine version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5d123-104">This article describes how Windows will be updated to support the next version of Microsoft Edge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d123-105">Reportez-vous au [billet de blog](https://aka.ms/EdgeLegacyEOS) de l’équipe produit Microsoft Edge sur la fin de service de l’ancienne version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5d123-105">Refer to the Microsoft Edge product team [blog post](https://aka.ms/EdgeLegacyEOS) about Microsoft Edge Legacy end of service.</span></span>

> [!NOTE]
> <span data-ttu-id="5d123-106">Cet article concerne le canal Microsoft Edge Stable.</span><span class="sxs-lookup"><span data-stu-id="5d123-106">This article applies to the Microsoft Edge Stable channel.</span></span>

## <span data-ttu-id="5d123-107">Microsoft Edge et le cycle de publication Windows</span><span class="sxs-lookup"><span data-stu-id="5d123-107">Microsoft Edge and the Windows release cycle</span></span>

<span data-ttu-id="5d123-108">La prochaine version de Microsoft Edge offre des fonctionnalités des mise à jour plus fréquentes et flexibles.</span><span class="sxs-lookup"><span data-stu-id="5d123-108">The next version of Microsoft Edge features more frequent and more flexible updating capabilities.</span></span> <span data-ttu-id="5d123-109">Les versions de navigateur n’étant pas liées aux versions majeures de Windows, des modifications seront apportées au système d’exploitation pour garantir que la prochaine version de Microsoft Edge s’adapte de façon transparente à Windows.</span><span class="sxs-lookup"><span data-stu-id="5d123-109">Because browser releases aren't bound to the Windows major releases, changes will be made to the operating system to ensure that the next version of Microsoft Edge fits seamlessly into Windows.</span></span> <span data-ttu-id="5d123-110">Par conséquent, les mises à jour des fonctionnalités seront publiées sur un cycle de 6 semaines (environ).</span><span class="sxs-lookup"><span data-stu-id="5d123-110">As a result, feature updates will be released on a 6-week cycle (approximately).</span></span> <span data-ttu-id="5d123-111">Les mises à jour de sécurité et de compatibilité seront livrées selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="5d123-111">Security and compatibility updates will be shipped as needed.</span></span>

## <span data-ttu-id="5d123-112">Mises à jour et expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="5d123-112">Updates and the user experience</span></span>

<span data-ttu-id="5d123-113">Les mises à jour ne modifieront pas l’expérience utilisateur tant que le canal Stable de la version suivante de Microsoft Edge ne sera pas installé.</span><span class="sxs-lookup"><span data-stu-id="5d123-113">Updates won’t change the user experience until the Stable channel of the next version of Microsoft Edge is installed.</span></span> <span data-ttu-id="5d123-114">L’installation de Microsoft Edge Beta, Dev ou Canary ne déclenche pas de modifications dans Windows.</span><span class="sxs-lookup"><span data-stu-id="5d123-114">Installing Microsoft Edge Beta, Dev, or Canary won’t trigger any changes in Windows.</span></span> <span data-ttu-id="5d123-115">Ces versions du navigateur seront installées à côté des navigateurs existants.</span><span class="sxs-lookup"><span data-stu-id="5d123-115">These browser releases will be installed alongside existing browsers.</span></span>

<span data-ttu-id="5d123-116">Lorsque toutes les mises à jour sont appliquées ET que le canal Stable de la version suivante de Microsoft Edge est installé au niveau du système, les modifications suivantes prennent effet sur le système :</span><span class="sxs-lookup"><span data-stu-id="5d123-116">When all the updates are applied AND the Stable channel of the next version of Microsoft Edge is installed at the system-level, the following changes will take effect on the system:</span></span>

- <span data-ttu-id="5d123-117">Tous les codes confidentiels du menu démarrer, les vignettes et les raccourcis de la version actuelle de Microsoft Edge sont migrés vers la version suivante de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5d123-117">All start menu pins, tiles, and shortcuts for the current version of Microsoft Edge will migrate to the next version of Microsoft Edge.</span></span>
- <span data-ttu-id="5d123-118">Tous les codes confidentiels et raccourcis de la barre des tâches pour la version actuelle de Microsoft Edge sont migrés vers la version suivante de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5d123-118">All taskbar pins and shortcuts for the current version of Microsoft Edge will migrate to the next version of Microsoft Edge.</span></span>
- <span data-ttu-id="5d123-119">La prochaine version de Microsoft Edge sera épinglée à la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="5d123-119">The next version of Microsoft Edge will be pinned to the taskbar.</span></span> <span data-ttu-id="5d123-120">Si la version actuelle de Microsoft Edge est déjà épinglée, elle sera remplacée.</span><span class="sxs-lookup"><span data-stu-id="5d123-120">If the current version of Microsoft Edge is already pinned, it will be replaced.</span></span>
- <span data-ttu-id="5d123-121">La prochaine version de Microsoft Edge ajoutera un raccourci sur le Bureau.</span><span class="sxs-lookup"><span data-stu-id="5d123-121">The next version of Microsoft Edge will add a shortcut to the desktop.</span></span> <span data-ttu-id="5d123-122">Si la version actuelle de Microsoft Edge possède déjà un raccourci, celui-ci sera remplacé.</span><span class="sxs-lookup"><span data-stu-id="5d123-122">If the current version of Microsoft Edge already has a shortcut, it will be replaced.</span></span>
- <span data-ttu-id="5d123-123">La plupart des protocoles que Microsoft Edge gère par défaut seront migrés vers la version suivante de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5d123-123">Most protocols that Microsoft Edge handles by default will be migrated to the next version of Microsoft Edge.</span></span>
- <span data-ttu-id="5d123-124">La version actuelle de Microsoft Edge sera masquée sur toutes les surfaces d’expérience utilisateur du système d’exploitation, y compris les paramètres, toutes les applications et les boîtes de dialogue de prise en charge de fichiers ou de protocoles.</span><span class="sxs-lookup"><span data-stu-id="5d123-124">Current Microsoft Edge will be hidden from all UX surfaces in the OS, including settings, all apps, and any file or protocol support dialogs.</span></span>
- <span data-ttu-id="5d123-125">Toutes les tentatives de lancement de la version actuelle de Microsoft Edge seront redirigées vers la version suivante de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5d123-125">All attempts to launch the current version of Microsoft Edge will redirect to the next version of Microsoft Edge.</span></span>

  > [!NOTE]
  > <span data-ttu-id="5d123-126">Les installations de niveau utilisateur ne déclencheront pas ces comportements.</span><span class="sxs-lookup"><span data-stu-id="5d123-126">User-level installs won’t trigger these behaviors.</span></span>

<span data-ttu-id="5d123-127">Avec les modifications précédentes, des modifications seront apportées, que le canal Stable de la version suivante de Microsoft Edge soit installé ou non.</span><span class="sxs-lookup"><span data-stu-id="5d123-127">Along with the previous changes, there are changes that will happen regardless of whether the Stable channel of the next version of Microsoft Edge is installed.</span></span>

- <span data-ttu-id="5d123-128">Microsoft Edge annulera l’inscription aux livres et protocoles XML que la version suivante de Microsoft Edge ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="5d123-128">Microsoft Edge will de-register for the books and XML protocols that the next version of Microsoft Edge doesn't support.</span></span> <span data-ttu-id="5d123-129">Les utilisateurs qui essaient d’ouvrir ces protocoles verront s’afficher une boîte de dialogue les invitant à choisir une application par défaut.</span><span class="sxs-lookup"><span data-stu-id="5d123-129">Users attempting to open these protocols will get a dialog that prompts them to choose a default app.</span></span> <span data-ttu-id="5d123-130">Pour en savoir plus sur les modifications de la prise en charge des livres, consultez [Téléchargez une application ePub pour continuer à lire des livres électroniques](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsupport.microsoft.com%2Fhelp%2F4517840&data=02%7C01%7Cv-danwes%40microsoft.com%7Cc9f8571b880549c30fcf08d72be5eaf9%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637026138803983526&sdata=qtb3DvVZQ6H%2FFXnBievkl%2B%2BngAQXwl340PcH8kRc3y4%3D&reserved=0).</span><span class="sxs-lookup"><span data-stu-id="5d123-130">Learn more about changes to books support at [Download an ePub app to keep reading e-books](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsupport.microsoft.com%2Fhelp%2F4517840&data=02%7C01%7Cv-danwes%40microsoft.com%7Cc9f8571b880549c30fcf08d72be5eaf9%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637026138803983526&sdata=qtb3DvVZQ6H%2FFXnBievkl%2B%2BngAQXwl340PcH8kRc3y4%3D&reserved=0).</span></span>

## <span data-ttu-id="5d123-131">Chronologie</span><span class="sxs-lookup"><span data-stu-id="5d123-131">Timeline</span></span>

<span data-ttu-id="5d123-132">Les modifications nécessaires à la prise en charge de l’expérience décrite seront fournies avec trois mises à jour pour différentes versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="5d123-132">The changes needed to support the described experience will be delivered with three updates for different versions of Windows.</span></span>

### <span data-ttu-id="5d123-133">Windows versions 1903 et 1909</span><span class="sxs-lookup"><span data-stu-id="5d123-133">Windows versions 1903 and 1909</span></span>

- <span data-ttu-id="5d123-134">Premier ensemble de modifications dans la mise à jour facultative de juillet 2019, compris dans la mise à jour de sécurité d’août 2019.</span><span class="sxs-lookup"><span data-stu-id="5d123-134">First set of changes in optional July 2019 update, delivered with the August 2019 security update.</span></span>
- <span data-ttu-id="5d123-135">Deuxième ensemble de modifications dans la mise à jour facultative d’août 2019, compris dans la mise à jour de sécurité de septembre 2019.</span><span class="sxs-lookup"><span data-stu-id="5d123-135">Second set of changes in the optional August 2019 update, delivered with the September 2019 security update.</span></span>

  > [!NOTE]
  > <span data-ttu-id="5d123-136">Il s’agit de la mise à jour dans laquelle Microsoft Edge annule l’inscription du protocole XML.</span><span class="sxs-lookup"><span data-stu-id="5d123-136">This is the update where Microsoft Edge will de-register for the XML protocol.</span></span>

- <span data-ttu-id="5d123-137">Troisième ensemble de modifications dans la mise à jour facultative de septembre 2019, compris dans la mise à jour de sécurité d’octobre 2019.</span><span class="sxs-lookup"><span data-stu-id="5d123-137">Third set of changes in the optional September 2019 update, delivered with the October 2019 security update.</span></span>

  > [!NOTE]
  > <span data-ttu-id="5d123-138">Il s’agit de la mise à jour dans laquelle Microsoft Edge ne prend plus en charge les e-books.</span><span class="sxs-lookup"><span data-stu-id="5d123-138">This is the update where Microsoft Edge will no longer support eBooks.</span></span>

### <span data-ttu-id="5d123-139">Windows versions 1709, 1803 et 1809</span><span class="sxs-lookup"><span data-stu-id="5d123-139">Windows versions 1709, 1803, and 1809</span></span>

- <span data-ttu-id="5d123-140">Premier ensemble de modifications dans une mise à jour facultative d’août 2019, compris dans la mise à jour de sécurité de septembre 2019.</span><span class="sxs-lookup"><span data-stu-id="5d123-140">First set of changes in an optional August 2019 update, delivered with the September 2019 security update.</span></span>
- <span data-ttu-id="5d123-141">Deuxième ensemble de modifications dans une mise à jour facultative de septembre 2019, compris dans la mise à jour de sécurité d’octobre 2019.</span><span class="sxs-lookup"><span data-stu-id="5d123-141">Second set of changes in an optional September 2019 update, delivered with the October 2019 security update.</span></span>

  > [!NOTE]
  > <span data-ttu-id="5d123-142">Il s’agit de la mise à jour dans laquelle Microsoft Edge annule l’inscription du protocole XML.</span><span class="sxs-lookup"><span data-stu-id="5d123-142">This is the update where Microsoft Edge will de-register for the XML protocol.</span></span>

- <span data-ttu-id="5d123-143">Troisième ensemble de modifications dans une mise à jour facultative d’octobre 2019, compris dans la mise à jour de sécurité de novembre 2019.</span><span class="sxs-lookup"><span data-stu-id="5d123-143">Third set of changes in an optional October 2019 update, delivered with the November 2019 security update.</span></span>

  > [!NOTE]
  > <span data-ttu-id="5d123-144">Il s’agit de la mise à jour dans laquelle Microsoft Edge ne prend plus en charge les e-books.</span><span class="sxs-lookup"><span data-stu-id="5d123-144">This is the update where Microsoft Edge will no longer support eBooks.</span></span>

<span data-ttu-id="5d123-145">Le tableau suivant fournit des détails sur les mises à jour spécifiques de chaque ensemble de modifications.</span><span class="sxs-lookup"><span data-stu-id="5d123-145">The following table gives the details for specific updates in each set of changes.</span></span>

| <span data-ttu-id="5d123-146">Windows 10</span><span class="sxs-lookup"><span data-stu-id="5d123-146">Windows 10</span></span> | <span data-ttu-id="5d123-147">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5d123-147">More Information</span></span> | <span data-ttu-id="5d123-148">Téléchargement requis</span><span class="sxs-lookup"><span data-stu-id="5d123-148">Required Download</span></span> |
|--|--|--|
| <span data-ttu-id="5d123-149">Version 1709</span><span class="sxs-lookup"><span data-stu-id="5d123-149">Version 1709</span></span> | [<span data-ttu-id="5d123-150">KB4525241</span><span class="sxs-lookup"><span data-stu-id="5d123-150">KB4525241</span></span>](https://support.microsoft.com/help/4525241/windows-10-update-kb4525241) | [<span data-ttu-id="5d123-151">Mise à jour de sécurité cumulative pour Windows 10, version 1709</span><span class="sxs-lookup"><span data-stu-id="5d123-151">Cumulative Update for Windows 10 Version 1709</span></span>](https://www.catalog.update.microsoft.com/Search.aspx?q=4525241) |
| <span data-ttu-id="5d123-152">Version 1803</span><span class="sxs-lookup"><span data-stu-id="5d123-152">Version 1803</span></span>  | [<span data-ttu-id="5d123-153">KB4525237</span><span class="sxs-lookup"><span data-stu-id="5d123-153">KB4525237</span></span>](https://support.microsoft.com/help/4525237/windows-10-update-kb4525237) | [<span data-ttu-id="5d123-154">Mise à jour de sécurité cumulative pour Windows 10, version 1803</span><span class="sxs-lookup"><span data-stu-id="5d123-154">Cumulative Update for Windows 10 Version 1803</span></span>](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4525237) |
| <span data-ttu-id="5d123-155">Version 1809</span><span class="sxs-lookup"><span data-stu-id="5d123-155">Version 1809</span></span>  | [<span data-ttu-id="5d123-156">KB4523205</span><span class="sxs-lookup"><span data-stu-id="5d123-156">KB4523205</span></span>](https://support.microsoft.com/help/4523205/windows-10-update-kb4523205) | [<span data-ttu-id="5d123-157">Mise à jour de sécurité cumulative pour Windows 10, version 1809</span><span class="sxs-lookup"><span data-stu-id="5d123-157">Cumulative Update for Windows 10 Version 1809</span></span>](https://www.catalog.update.microsoft.com/Search.aspx?q=4523205) |
| <span data-ttu-id="5d123-158">Version 1903 et 1909</span><span class="sxs-lookup"><span data-stu-id="5d123-158">Version 1903 and 1909</span></span> |[<span data-ttu-id="5d123-159">KB4517389</span><span class="sxs-lookup"><span data-stu-id="5d123-159">KB4517389</span></span>](https://support.microsoft.com/help/4517389/windows-10-update-kb4517389)  | [<span data-ttu-id="5d123-160">Mise à jour de sécurité cumulative pour Windows 10, version 1903 et 1909</span><span class="sxs-lookup"><span data-stu-id="5d123-160">Cumulative Update for Windows 10 Version 1903 and 1909</span></span>](https://www.catalog.update.microsoft.com/Search.aspx?q=4517389) |

## <span data-ttu-id="5d123-161">Articles associés</span><span class="sxs-lookup"><span data-stu-id="5d123-161">See also</span></span>

- [<span data-ttu-id="5d123-162">Page d’accueil Microsoft Edge Entreprise</span><span class="sxs-lookup"><span data-stu-id="5d123-162">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="5d123-163">Documentation Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5d123-163">Microsoft Edge documentation</span></span>](https://docs.microsoft.com/DeployEdge/)
