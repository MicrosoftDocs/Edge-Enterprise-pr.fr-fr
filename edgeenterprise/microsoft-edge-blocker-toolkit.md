---
title: Blocker Toolkit pour désactiver la distribution automatique de MicrosoftEdge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 12/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Blocker Toolkit pour désactiver la distribution automatique de MicrosoftEdge
ms.openlocfilehash: 9fb97d2dfec4822f8ce76dc3e37b85118c6572ad
ms.sourcegitcommit: 606282995b466a968bab40c16005a6653323c763
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/16/2020
ms.locfileid: "11229615"
---
# <span data-ttu-id="4eed9-103">Blocker Toolkit pour désactiver la distribution automatique de MicrosoftEdge (basé sur Chromium)</span><span class="sxs-lookup"><span data-stu-id="4eed9-103">Blocker Toolkit to disable automatic delivery of Microsoft Edge (Chromium-based)</span></span>

<span data-ttu-id="4eed9-104">Cet article décrit le Blocker Toolkit qui permet de désactiver la distribution et l’installation automatiques de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="4eed9-104">This article describes the Blocker Toolkit for disabling automatic delivery and installation of Microsoft Edge.</span></span>

<span data-ttu-id="4eed9-105">Mises à jour apportées à cet article:</span><span class="sxs-lookup"><span data-stu-id="4eed9-105">The following updates have been made to this article:</span></span>

- <span data-ttu-id="4eed9-106">**09/01/2020** contenant plus d’informations relatives aux appareils qui pourraient demander l’utilisation de Blocker Toolkit</span><span class="sxs-lookup"><span data-stu-id="4eed9-106">**01/09/2020** with more information about devices that might require you to use the Blocker Toolkit</span></span>
- <span data-ttu-id="4eed9-107">**28/02/2020** pour la suppression de l’option « géré par MDM » à partir des critères des appareils à exclure de cette mise à jour automatique</span><span class="sxs-lookup"><span data-stu-id="4eed9-107">**2/28/2020** to remove "MDM managed" from the criteria of devices to be excluded from this automatic update</span></span>
- <span data-ttu-id="4eed9-108">**30/06/2020** pour indiquer que tous les appareils connectés à Windows Update sont dans l’étendue de la réception de cette mise à jour. (effective au plus tôt le 30/07/2020)</span><span class="sxs-lookup"><span data-stu-id="4eed9-108">**6/30/2020** to reflect that all Windows Update connected devices are in scope to receive this update (effective no sooner than 7/30/2020)</span></span>
- <span data-ttu-id="4eed9-109">**10/12/2020** pour expliquer les situations préalables à 20H2 dans lesquelles les paramètres Blocker Toolkit sont ignorés</span><span class="sxs-lookup"><span data-stu-id="4eed9-109">**12/10/2020** to explain pre 20H2 situations in which the Blocker Toolkit settings will be ignored</span></span>

> [!NOTE]
> <span data-ttu-id="4eed9-110">Cet article concerne le canal Stable de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="4eed9-110">This applies to Microsoft Edge Stable channel.</span></span>

## <span data-ttu-id="4eed9-111">Présentation</span><span class="sxs-lookup"><span data-stu-id="4eed9-111">Overview</span></span>

<span data-ttu-id="4eed9-112">Pour aider nos clients à rester à jour et à assurer leur sécurité, Microsoft distribuera MicrosoftEdge (basé sur Chromium) sur tous les appareils connectés à Windows Update et exécutant Windows10 versions1803 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4eed9-112">To help our customers become more secure and up-to-date, Microsoft will distribute Microsoft Edge (Chromium-based) to all Windows Update-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="4eed9-113">Ce processus démarrera après le 15janvier2020, et des informations supplémentaires seront disponibles à cette date.</span><span class="sxs-lookup"><span data-stu-id="4eed9-113">This process will start after January 15, 2020 and more information will be available on that date.</span></span>

<span data-ttu-id="4eed9-114">Blocker Toolkit est destiné aux organisations qui souhaitent bloquer la distribution automatique de MicrosoftEdge (basée sur Chromium) sur les appareils connectés à Windows Update et exécutant Windows10 versions1803 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4eed9-114">The Blocker Toolkit is intended for organizations that would like to block automatic delivery of Microsoft Edge (Chromium-based) to Windows Updated-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="4eed9-115">Les appareils qui sont gérés par Windows Server Update Services (WSUS) ou Windows Update pour Entreprise (WUfB) sont exclus de cette mise à jour automatique de Windows Update, mais peuvent recevoir la nouvelle version de Microsoft Edge (basée sur Chromium) à travers leur organisation.</span><span class="sxs-lookup"><span data-stu-id="4eed9-115">Devices that are Windows Server Update Services (WSUS) or Windows Update for Business (WUfB) managed will be excluded from this automatic Windows Update, but may receive the new Microsoft Edge (Chromium-based) through their organization.</span></span>

**<span data-ttu-id="4eed9-116">Il est important de noter que:</span><span class="sxs-lookup"><span data-stu-id="4eed9-116">It's important to note that:</span></span>**

- <span data-ttu-id="4eed9-117">Blocker Toolkit n’empêche pas les utilisateurs d’installer manuellement MicrosoftEdge (basé sur Chromium) à partir d’un téléchargement Internet ou à partir d’un support externe.</span><span class="sxs-lookup"><span data-stu-id="4eed9-117">The Blocker Toolkit will not prevent users from manually installing Microsoft Edge (Chromium-based) from Internet download, or from external media.</span></span>
- <span data-ttu-id="4eed9-118">Les organisations dont les mises à jour sont gérées via Windows Update pour Entreprise (WUfB) ne recevront pas automatiquement cette mise à jour et n’ont pas besoin de déployer Blocker Toolkit.</span><span class="sxs-lookup"><span data-stu-id="4eed9-118">Organizations with updates managed through Windows Update for Business (WUfB) will not automatically receive this update and do not need to deploy the blocker toolkit.</span></span>
- <span data-ttu-id="4eed9-119">Les entreprises dotées d’environnements gérés avec une solution de gestion des mises à jour telle que WindowsServerUpdateServices (WSUS) ou SystemCenter ConfigurationManager (SCCM) n’ont pas besoin de déployer Blocker Toolkit.</span><span class="sxs-lookup"><span data-stu-id="4eed9-119">Organizations with environments managed with an update management solution such as Windows Server Update Services (WSUS) or System Center Configuration Manager (SCCM) do not have to deploy the Blocker Toolkit.</span></span> <span data-ttu-id="4eed9-120">Ils peuvent utiliser ces produits pour gérer pleinement le déploiement des mises à jour publiées par le biais de Windows Update et Microsoft Update, y compris la [mise à jour de WSUS pour la nouvelle version de Microsoft Edge](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge), au sein de leur environnement.</span><span class="sxs-lookup"><span data-stu-id="4eed9-120">They can use those products to fully manage deployment of updates released through Windows Update and Microsoft Update, including the [Update in WSUS for the new Microsoft Edge](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge), within their environment.</span></span>
- <span data-ttu-id="4eed9-121">Cette mise à jour est une mise à jour autonome (qui ne fait pas partie de la mise à jour cumulative mensuelle) pour offrir aux clients d’entreprise une flexibilité et un contrôle maximal sur le déploiement de cette mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4eed9-121">This update is a stand-alone update (not part of the monthly cumulative update) to give Enterprise customers flexibility and maximum control over deploying this update.</span></span>
- <span data-ttu-id="4eed9-122">La nouvelle version de Microsoft Edge (basée sur Chromium) est incluse dans la mise à jour des fonctionnalités de la version 20H2 de Windows 10 dans la deuxième moitié de 2020.</span><span class="sxs-lookup"><span data-stu-id="4eed9-122">The new Microsoft Edge (Chromium-based) is included as part of the Windows 10, version 20H2 feature update in the second half of 2020.</span></span> <span data-ttu-id="4eed9-123">Blocker Toolkit n’a aucun impact sur les comportements ou le déploiement de 20H2.</span><span class="sxs-lookup"><span data-stu-id="4eed9-123">The Blocker toolkit does not impact 20H2 behaviors or deployment.</span></span> <span data-ttu-id="4eed9-124">Si vous souhaitez en savoir plus d’informations sur Windows10 version20H2, veuillez cliquer [ici](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span><span class="sxs-lookup"><span data-stu-id="4eed9-124">See more information about Windows 10, version 20H2 [here](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span></span>

<span data-ttu-id="4eed9-125">Vous pouvez télécharger le fichier exécutable de Blocker Toolkit à partir de [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span><span class="sxs-lookup"><span data-stu-id="4eed9-125">You can download the Blocker Toolkit executable file from [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span></span>

### <span data-ttu-id="4eed9-126">Composants de Blocker Toolkit</span><span class="sxs-lookup"><span data-stu-id="4eed9-126">Toolkit components</span></span>

<span data-ttu-id="4eed9-127">Ce kit de ressources comprend les composants suivants:</span><span class="sxs-lookup"><span data-stu-id="4eed9-127">This toolkit contains the following components:</span></span>

- <span data-ttu-id="4eed9-128">Script de bloqueur exécutable (.CMD)</span><span class="sxs-lookup"><span data-stu-id="4eed9-128">Executable blocker script (.CMD)</span></span>
- <span data-ttu-id="4eed9-129">Modèle d’administration de la stratégie de groupe (.ADMX et .ADML)</span><span class="sxs-lookup"><span data-stu-id="4eed9-129">Group Policy Administrative Template (.ADMX and .ADML)</span></span>

### <span data-ttu-id="4eed9-130">Systèmes d’exploitation pris en charge</span><span class="sxs-lookup"><span data-stu-id="4eed9-130">Supported Operating Systems</span></span>

<span data-ttu-id="4eed9-131">Windows10, version1803 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4eed9-131">Windows 10 version 1803 and newer.</span></span>

## <span data-ttu-id="4eed9-132">Script de bloqueur</span><span class="sxs-lookup"><span data-stu-id="4eed9-132">Blocker script</span></span>

<span data-ttu-id="4eed9-133">Le script crée une clé de registre et définit la valeur associée à bloquer ou débloquer (selon l’option de ligne de commande utilisée) de la distribution automatique de MicrosoftEdge (basé sur Chromium) sur l’ordinateur local ou sur un ordinateur cible distant.</span><span class="sxs-lookup"><span data-stu-id="4eed9-133">The script creates a registry key and sets the associated value to block or unblock (depending on the command-line option used) automatic delivery of Microsoft Edge (Chromium-based) on either the local machine or a remote target machine.</span></span>

**<span data-ttu-id="4eed9-134">Clé de Registre:</span><span class="sxs-lookup"><span data-stu-id="4eed9-134">Registry key:</span></span>** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**<span data-ttu-id="4eed9-135">Nom de la valeur de clé:</span><span class="sxs-lookup"><span data-stu-id="4eed9-135">Key value name:</span></span>** `DoNotUpdateToEdgeWithChromium`

| <span data-ttu-id="4eed9-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="4eed9-136">Value</span></span>                | <span data-ttu-id="4eed9-137">Résultat</span><span class="sxs-lookup"><span data-stu-id="4eed9-137">Result</span></span>                         |
|----------------------|--------------------------------|
| *<span data-ttu-id="4eed9-138">La clé n’est pas définie</span><span class="sxs-lookup"><span data-stu-id="4eed9-138">Key is not defined</span></span>* | <span data-ttu-id="4eed9-139">La distribution n’est *pas* bloquée.</span><span class="sxs-lookup"><span data-stu-id="4eed9-139">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="4eed9-140">0</span><span class="sxs-lookup"><span data-stu-id="4eed9-140">0</span></span>                    | <span data-ttu-id="4eed9-141">La distribution n’est *pas* bloquée.</span><span class="sxs-lookup"><span data-stu-id="4eed9-141">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="4eed9-142">1</span><span class="sxs-lookup"><span data-stu-id="4eed9-142">1</span></span>                    | <span data-ttu-id="4eed9-143">La distribution est bloquée.</span><span class="sxs-lookup"><span data-stu-id="4eed9-143">Distribution is blocked.</span></span>       |

<span data-ttu-id="4eed9-144">Le script possède la syntaxe de ligne de commande suivante:</span><span class="sxs-lookup"><span data-stu-id="4eed9-144">The script has the following command-line syntax:</span></span><br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### <span data-ttu-id="4eed9-145">Nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="4eed9-145">Machine name</span></span>

<span data-ttu-id="4eed9-146">Le paramètre `<machine name>` est facultatif.</span><span class="sxs-lookup"><span data-stu-id="4eed9-146">The `<machine name>` parameter is optional.</span></span> <span data-ttu-id="4eed9-147">Si ce paramètre n’est pas spécifié, l’action est effectuée sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4eed9-147">If not specified, the action is performed on the local machine.</span></span> <span data-ttu-id="4eed9-148">Dans le cas contraire, l’ordinateur distant est accessible par le biais des fonctionnalités de Registre distant de la commande `REG`.</span><span class="sxs-lookup"><span data-stu-id="4eed9-148">Otherwise, the remote machine is accessed through the remote registry capabilities of the `REG` command.</span></span> <span data-ttu-id="4eed9-149">Si le Registre distant est inaccessible en raison d’autorisations de sécurité ou si l’ordinateur distant est introuvable, un message d’erreur est renvoyé par la commande `REG`.</span><span class="sxs-lookup"><span data-stu-id="4eed9-149">If the remote registry can't be accessed due to security permissions or the remote machine can't be found, an error message is returned from the `REG` command.</span></span>

### <span data-ttu-id="4eed9-150">Commutateurs</span><span class="sxs-lookup"><span data-stu-id="4eed9-150">Switches</span></span>

<span data-ttu-id="4eed9-151">Les commutateurs utilisés par le script s’excluent mutuellement et seul le premier commutateur valide d’une commande donnée est traité.</span><span class="sxs-lookup"><span data-stu-id="4eed9-151">Switches used by the script are mutually exclusive and only the first valid switch from a given command is acted on.</span></span> <span data-ttu-id="4eed9-152">Le script peut être exécuté plusieurs fois sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4eed9-152">The script can be run multiple times on the same machine.</span></span>

| <span data-ttu-id="4eed9-153">Commutateur</span><span class="sxs-lookup"><span data-stu-id="4eed9-153">Switch</span></span>       | <span data-ttu-id="4eed9-154">Description</span><span class="sxs-lookup"><span data-stu-id="4eed9-154">Description</span></span>                              |
|--------------|------------------------------------------|
| `/B`         | <span data-ttu-id="4eed9-155">Bloque la distribution</span><span class="sxs-lookup"><span data-stu-id="4eed9-155">Blocks distribution</span></span>                      |
| `/U`         | <span data-ttu-id="4eed9-156">Débloque la distribution</span><span class="sxs-lookup"><span data-stu-id="4eed9-156">Unblocks distribution</span></span>                    |
| `/H` <span data-ttu-id="4eed9-157">ou</span><span class="sxs-lookup"><span data-stu-id="4eed9-157">or</span></span> `/?` | <span data-ttu-id="4eed9-158">Affiche l’aide récapitulative suivante:</span><span class="sxs-lookup"><span data-stu-id="4eed9-158">Displays the following summary help:</span></span><br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## <span data-ttu-id="4eed9-159">Modèle d’administration de la stratégie de groupe (fichiers .ADMX et .ADML)</span><span class="sxs-lookup"><span data-stu-id="4eed9-159">Group Policy Administrative Template (.ADMX and .ADML files)</span></span>

<span data-ttu-id="4eed9-160">Le modèle d’administration de la stratégie de groupe (fichiers .ADMX et.ADML) permet aux administrateurs d’importer les nouveaux paramètres de stratégie de groupe pour bloquer ou débloquer la distribution automatique de MicrosoftEdge (basé sur Chromium) dans leur environnement de stratégie de groupe, et d’utiliser une stratégie de groupe pour exécuter l’action de manière centralisée sur les différents systèmes au sein de leur environnement.</span><span class="sxs-lookup"><span data-stu-id="4eed9-160">The Group Policy Administrative Template (.ADMX  and .ADML files) allows administrators to import the new Group Policy settings to block or unblock automatic delivery of Microsoft Edge (Chromium-based) into their Group Policy environment, and use Group Policy to centrally execute the action across systems in their environment.</span></span>

<span data-ttu-id="4eed9-161">Les utilisateurs qui exécutent Windows10RS3Entreprise/EDU et RS4 et versions ultérieures verront la stratégie sous le chemin d’accès suivant:</span><span class="sxs-lookup"><span data-stu-id="4eed9-161">Users running Windows 10 RS3 Enterprise/EDU and RS4 and newer, will see the policy under the following path:</span></span>

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

<span data-ttu-id="4eed9-162">Ce paramètre est disponible uniquement en tant que paramètre d’ordinateur; il n’existe aucun paramètre par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4eed9-162">This setting is available only as a Computer setting; there is no Per-User setting.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4eed9-163">Ce paramètre de Registre n’est pas stocké dans une clé de stratégies, il est considéré comme une *préférence*.</span><span class="sxs-lookup"><span data-stu-id="4eed9-163">This registry setting isn't stored in a policies key and is considered a *preference*.</span></span> <span data-ttu-id="4eed9-164">Par conséquent, si l’objet de stratégie de groupe qui implémente le paramètre est supprimé ou si la stratégie est définie sur **non configurée**, le paramètre est conservé.</span><span class="sxs-lookup"><span data-stu-id="4eed9-164">Therefore, if the Group Policy Object that implements the setting is ever removed or the policy is set to **Not Configured**, the setting will remain.</span></span> <span data-ttu-id="4eed9-165">Pour débloquer la distribution de MicrosoftEdge (basé sur Chromium) à l’aide d’une stratégie de groupe, définissez la stratégie sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="4eed9-165">To unblock distribution of Microsoft Edge (Chromium-based) by using Group Policy, set the policy to **Disabled**.</span></span>

## <span data-ttu-id="4eed9-166">Articles associés</span><span class="sxs-lookup"><span data-stu-id="4eed9-166">See also</span></span>

- [<span data-ttu-id="4eed9-167">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="4eed9-167">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="4eed9-168">Mises à jour Windows pour prendre en charge MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="4eed9-168">Windows updates to support Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [<span data-ttu-id="4eed9-169">Comment accéder à l’ancienne version de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="4eed9-169">How to access the old version of Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
