---
title: Blocker Toolkit pour désactiver la distribution automatique de MicrosoftEdge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Blocker Toolkit pour désactiver la distribution automatique de MicrosoftEdge
ms.openlocfilehash: 7563d2c94cf91a8434328699e46c75dbcfb77561
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979825"
---
# <span data-ttu-id="7c1b9-103">Blocker Toolkit pour désactiver la distribution automatique de MicrosoftEdge (basé sur Chromium)</span><span class="sxs-lookup"><span data-stu-id="7c1b9-103">Blocker Toolkit to disable automatic delivery of Microsoft Edge (Chromium-based)</span></span>

<span data-ttu-id="7c1b9-104">Cet article décrit le Blocker Toolkit qui permet de désactiver la distribution et l’installation automatiques de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-104">This article describes the Blocker Toolkit for disabling automatic delivery and installation of Microsoft Edge.</span></span> <span data-ttu-id="7c1b9-105">Nous avons mis à jour cet article le **09/01/2020** avec des informations sur les appareils susceptibles d’exiger l’utilisation de Blocker Toolkit, le **28/02/2020** pour supprimer «géré par GPM» des critères des appareils à exclure de cette mise à jour automatique, puis le **30/06/2020** pour intégrer le fait que cette mise à jour concerne tous les appareils connectés à Windows Update (en vigueur au plus tôt le 30/07/2020).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-105">This article was updated on **01/09/2020** with more information about devices that might require you to use the Blocker Toolkit, on **2/28/2020** to remove "MDM managed" from the criteria of devices to be excluded from this automatic update, and on **6/30/2020** to reflect that all Windows Update connected devices are in scope to receive this update (effective no sooner than 7/30/2020).</span></span>

> [!NOTE]
> <span data-ttu-id="7c1b9-106">Cet article concerne le canal Stable de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-106">This applies to Microsoft Edge Stable channel.</span></span>

## <span data-ttu-id="7c1b9-107">Présentation</span><span class="sxs-lookup"><span data-stu-id="7c1b9-107">Overview</span></span>

<span data-ttu-id="7c1b9-108">Pour aider nos clients à rester à jour et à assurer leur sécurité, Microsoft distribuera MicrosoftEdge (basé sur Chromium) sur tous les appareils connectés à Windows Update et exécutant Windows10 versions1803 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-108">To help our customers become more secure and up-to-date, Microsoft will distribute Microsoft Edge (Chromium-based) to all Windows Update-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="7c1b9-109">Ce processus démarrera après le 15janvier2020, et des informations supplémentaires seront disponibles à cette date.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-109">This process will start after January 15, 2020 and more information will be available on that date.</span></span>

<span data-ttu-id="7c1b9-110">Blocker Toolkit est destiné aux organisations qui souhaitent bloquer la distribution automatique de MicrosoftEdge (basée sur Chromium) sur les appareils connectés à Windows Update et exécutant Windows10 versions1803 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-110">The Blocker Toolkit is intended for organizations that would like to block automatic delivery of Microsoft Edge (Chromium-based) to Windows Updated-connected devices running Windows 10 version 1803 and newer.</span></span>
<span data-ttu-id="7c1b9-111">Cette mise à jour automatique ne concernera pas les appareils gérés par Windows Server Update Services (WSUS) ou Windows Update pour Entreprise.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-111">Devices that are Windows Server Update Services (WSUS) or Windows Update for Business (WUfB) managed will be excluded from this automatic update.</span></span>

**<span data-ttu-id="7c1b9-112">Il est important de noter que:</span><span class="sxs-lookup"><span data-stu-id="7c1b9-112">It's important to note that:</span></span>**

- <span data-ttu-id="7c1b9-113">Blocker Toolkit n’empêche pas les utilisateurs d’installer manuellement MicrosoftEdge (basé sur Chromium) à partir d’un téléchargement Internet ou à partir d’un support externe.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-113">The Blocker Toolkit will not prevent users from manually installing Microsoft Edge (Chromium-based) from Internet download, or from external media.</span></span>
- <span data-ttu-id="7c1b9-114">Les organisations dont les mises à jour sont gérées via Windows Update pour Entreprise (WUfB) ne recevront pas automatiquement cette mise à jour et n’ont pas besoin de déployer Blocker Toolkit.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-114">Organizations with updates managed through Windows Update for Business (WUfB) will not automatically receive this update and do not need to deploy the blocker toolkit.</span></span>
- <span data-ttu-id="7c1b9-115">Les entreprises dotées d’environnements gérés avec une solution de gestion des mises à jour telle que WindowsServerUpdateServices (WSUS) ou SystemCenter ConfigurationManager (SCCM) n’ont pas besoin de déployer Blocker Toolkit.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-115">Organizations with environments managed with an update management solution such as Windows Server Update Services (WSUS) or System Center Configuration Manager (SCCM) do not have to deploy the Blocker Toolkit.</span></span> <span data-ttu-id="7c1b9-116">Elles peuvent utiliser ces produits pour gérer entièrement le déploiement des mises à jour publiées via Windows Update et Microsoft Update, notamment MicrosoftEdge (basé sur Chromium), au sein de leur environnement.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-116">They can use those products to fully manage deployment of updates released through Windows Update and Microsoft Update, including Microsoft Edge (Chromium-based), within their environment.</span></span>
- <span data-ttu-id="7c1b9-117">Cette mise à jour est une mise à jour autonome (qui ne fait pas partie de la mise à jour cumulative mensuelle) pour offrir aux clients d’entreprise une flexibilité et un contrôle maximal sur le déploiement de cette mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-117">This update is a stand-alone update (not part of the monthly cumulative update) to give Enterprise customers flexibility and maximum control over deploying this update.</span></span>
- <span data-ttu-id="7c1b9-118">Le nouveau Microsoft Edge (basé sur Chromium) fera partie de la mise à jour des fonctionnalités de Windows10 version20H2 au second semestre 2020.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-118">The new Microsoft Edge (Chromium-based) will be included as part of the Windows 10, version 20H2 feature update in the second half of 2020.</span></span> <span data-ttu-id="7c1b9-119">Blocker Toolkit n’a aucun impact sur les comportements ou le déploiement de 20H2.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-119">The Blocker toolkit does not impact 20H2 behaviors or deployment.</span></span> <span data-ttu-id="7c1b9-120">Si vous souhaitez en savoir plus d’informations sur Windows10 version20H2, veuillez cliquer [ici](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-120">See more information about Windows 10, version 20H2 [here](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span></span>

<span data-ttu-id="7c1b9-121">Vous pouvez télécharger le fichier exécutable de Blocker Toolkit à partir de [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span><span class="sxs-lookup"><span data-stu-id="7c1b9-121">You can download the Blocker Toolkit executable file from [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span></span>

### <span data-ttu-id="7c1b9-122">Composants de Blocker Toolkit</span><span class="sxs-lookup"><span data-stu-id="7c1b9-122">Toolkit components</span></span>

<span data-ttu-id="7c1b9-123">Ce kit de ressources comprend les composants suivants:</span><span class="sxs-lookup"><span data-stu-id="7c1b9-123">This toolkit contains the following components:</span></span>

- <span data-ttu-id="7c1b9-124">Script de bloqueur exécutable (.CMD)</span><span class="sxs-lookup"><span data-stu-id="7c1b9-124">Executable blocker script (.CMD)</span></span>
- <span data-ttu-id="7c1b9-125">Modèle d’administration de la stratégie de groupe (.ADMX et .ADML)</span><span class="sxs-lookup"><span data-stu-id="7c1b9-125">Group Policy Administrative Template (.ADMX and .ADML)</span></span>

### <span data-ttu-id="7c1b9-126">Systèmes d’exploitation pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c1b9-126">Supported Operating Systems</span></span>

<span data-ttu-id="7c1b9-127">Windows10, version1803 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-127">Windows 10 version 1803 and newer.</span></span>

## <span data-ttu-id="7c1b9-128">Script de bloqueur</span><span class="sxs-lookup"><span data-stu-id="7c1b9-128">Blocker script</span></span>

<span data-ttu-id="7c1b9-129">Le script crée une clé de registre et définit la valeur associée à bloquer ou débloquer (selon l’option de ligne de commande utilisée) de la distribution automatique de MicrosoftEdge (basé sur Chromium) sur l’ordinateur local ou sur un ordinateur cible distant.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-129">The script creates a registry key and sets the associated value to block or unblock (depending on the command-line option used) automatic delivery of Microsoft Edge (Chromium-based) on either the local machine or a remote target machine.</span></span>

**<span data-ttu-id="7c1b9-130">Clé de Registre:</span><span class="sxs-lookup"><span data-stu-id="7c1b9-130">Registry key:</span></span>** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**<span data-ttu-id="7c1b9-131">Nom de la valeur de clé:</span><span class="sxs-lookup"><span data-stu-id="7c1b9-131">Key value name:</span></span>** `DoNotUpdateToEdgeWithChromium`

| <span data-ttu-id="7c1b9-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c1b9-132">Value</span></span>                | <span data-ttu-id="7c1b9-133">Résultat</span><span class="sxs-lookup"><span data-stu-id="7c1b9-133">Result</span></span>                         |
|----------------------|--------------------------------|
| *<span data-ttu-id="7c1b9-134">La clé n’est pas définie</span><span class="sxs-lookup"><span data-stu-id="7c1b9-134">Key is not defined</span></span>* | <span data-ttu-id="7c1b9-135">La distribution n’est *pas* bloquée.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-135">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="7c1b9-136">0</span><span class="sxs-lookup"><span data-stu-id="7c1b9-136">0</span></span>                    | <span data-ttu-id="7c1b9-137">La distribution n’est *pas* bloquée.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-137">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="7c1b9-138">1</span><span class="sxs-lookup"><span data-stu-id="7c1b9-138">1</span></span>                    | <span data-ttu-id="7c1b9-139">La distribution est bloquée.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-139">Distribution is blocked.</span></span>       |

<span data-ttu-id="7c1b9-140">Le script possède la syntaxe de ligne de commande suivante:</span><span class="sxs-lookup"><span data-stu-id="7c1b9-140">The script has the following command-line syntax:</span></span><br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### <span data-ttu-id="7c1b9-141">Nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="7c1b9-141">Machine name</span></span>

<span data-ttu-id="7c1b9-142">Le paramètre `<machine name>` est facultatif.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-142">The `<machine name>` parameter is optional.</span></span> <span data-ttu-id="7c1b9-143">Si ce paramètre n’est pas spécifié, l’action est effectuée sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-143">If not specified, the action is performed on the local machine.</span></span> <span data-ttu-id="7c1b9-144">Dans le cas contraire, l’ordinateur distant est accessible par le biais des fonctionnalités de Registre distant de la commande `REG`.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-144">Otherwise, the remote machine is accessed through the remote registry capabilities of the `REG` command.</span></span> <span data-ttu-id="7c1b9-145">Si le Registre distant est inaccessible en raison d’autorisations de sécurité ou si l’ordinateur distant est introuvable, un message d’erreur est renvoyé par la commande `REG`.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-145">If the remote registry can't be accessed due to security permissions or the remote machine can't be found, an error message is returned from the `REG` command.</span></span>

### <span data-ttu-id="7c1b9-146">Commutateurs</span><span class="sxs-lookup"><span data-stu-id="7c1b9-146">Switches</span></span>

<span data-ttu-id="7c1b9-147">Les commutateurs utilisés par le script s’excluent mutuellement et seul le premier commutateur valide d’une commande donnée est traité.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-147">Switches used by the script are mutually exclusive and only the first valid switch from a given command is acted on.</span></span> <span data-ttu-id="7c1b9-148">Le script peut être exécuté plusieurs fois sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-148">The script can be run multiple times on the same machine.</span></span>

| <span data-ttu-id="7c1b9-149">Commutateur</span><span class="sxs-lookup"><span data-stu-id="7c1b9-149">Switch</span></span>       | <span data-ttu-id="7c1b9-150">Description</span><span class="sxs-lookup"><span data-stu-id="7c1b9-150">Description</span></span>                              |
|--------------|------------------------------------------|
| `/B`         | <span data-ttu-id="7c1b9-151">Bloque la distribution</span><span class="sxs-lookup"><span data-stu-id="7c1b9-151">Blocks distribution</span></span>                      |
| `/U`         | <span data-ttu-id="7c1b9-152">Débloque la distribution</span><span class="sxs-lookup"><span data-stu-id="7c1b9-152">Unblocks distribution</span></span>                    |
| `/H` <span data-ttu-id="7c1b9-153">ou</span><span class="sxs-lookup"><span data-stu-id="7c1b9-153">or</span></span> `/?` | <span data-ttu-id="7c1b9-154">Affiche l’aide récapitulative suivante:</span><span class="sxs-lookup"><span data-stu-id="7c1b9-154">Displays the following summary help:</span></span><br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## <span data-ttu-id="7c1b9-155">Modèle d’administration de la stratégie de groupe (fichiers .ADMX et .ADML)</span><span class="sxs-lookup"><span data-stu-id="7c1b9-155">Group Policy Administrative Template (.ADMX and .ADML files)</span></span>

<span data-ttu-id="7c1b9-156">Le modèle d’administration de la stratégie de groupe (fichiers .ADMX et.ADML) permet aux administrateurs d’importer les nouveaux paramètres de stratégie de groupe pour bloquer ou débloquer la distribution automatique de MicrosoftEdge (basé sur Chromium) dans leur environnement de stratégie de groupe, et d’utiliser une stratégie de groupe pour exécuter l’action de manière centralisée sur les différents systèmes au sein de leur environnement.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-156">The Group Policy Administrative Template (.ADMX  and .ADML files) allows administrators to import the new Group Policy settings to block or unblock automatic delivery of Microsoft Edge (Chromium-based) into their Group Policy environment, and use Group Policy to centrally execute the action across systems in their environment.</span></span>

<span data-ttu-id="7c1b9-157">Les utilisateurs qui exécutent Windows10RS3Entreprise/EDU et RS4 et versions ultérieures verront la stratégie sous le chemin d’accès suivant:</span><span class="sxs-lookup"><span data-stu-id="7c1b9-157">Users running Windows 10 RS3 Enterprise/EDU and RS4 and newer, will see the policy under the following path:</span></span>

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

<span data-ttu-id="7c1b9-158">Ce paramètre est disponible uniquement en tant que paramètre d’ordinateur; il n’existe aucun paramètre par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-158">This setting is available only as a Computer setting; there is no Per-User setting.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c1b9-159">Ce paramètre de Registre n’est pas stocké dans une clé de stratégies, il est considéré comme une *préférence*.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-159">This registry setting isn't stored in a policies key and is considered a *preference*.</span></span> <span data-ttu-id="7c1b9-160">Par conséquent, si l’objet de stratégie de groupe qui implémente le paramètre est supprimé ou si la stratégie est définie sur **non configurée**, le paramètre est conservé.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-160">Therefore, if the Group Policy Object that implements the setting is ever removed or the policy is set to **Not Configured**, the setting will remain.</span></span> <span data-ttu-id="7c1b9-161">Pour débloquer la distribution de MicrosoftEdge (basé sur Chromium) à l’aide d’une stratégie de groupe, définissez la stratégie sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="7c1b9-161">To unblock distribution of Microsoft Edge (Chromium-based) by using Group Policy, set the policy to **Disabled**.</span></span>

## <span data-ttu-id="7c1b9-162">Articles associés</span><span class="sxs-lookup"><span data-stu-id="7c1b9-162">See also</span></span>

- [<span data-ttu-id="7c1b9-163">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="7c1b9-163">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="7c1b9-164">Mises à jour Windows pour prendre en charge MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="7c1b9-164">Windows updates to support Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [<span data-ttu-id="7c1b9-165">Comment accéder à l’ancienne version de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="7c1b9-165">How to access the old version of Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
