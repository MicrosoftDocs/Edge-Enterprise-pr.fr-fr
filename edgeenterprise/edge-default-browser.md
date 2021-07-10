---
title: Définir MicrosoftEdge comme navigateur par défaut sur Windows et macOS
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Découvrez comment définir MicrosoftEdge comme navigateur par défaut
ms.openlocfilehash: 191d7835a0c4aacfc2fde409c57622ff5a351926
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641540"
---
# <a name="set-microsoft-edge-as-the-default-browser"></a><span data-ttu-id="394e7-103">Définir MicrosoftEdge comme navigateur par défaut</span><span class="sxs-lookup"><span data-stu-id="394e7-103">Set Microsoft Edge as the default browser</span></span>

<span data-ttu-id="394e7-104">Cet article explique comment vous pouvez définir MicrosoftEdge comme navigateur par défaut sur Windows et macOS.</span><span class="sxs-lookup"><span data-stu-id="394e7-104">This article explains how you can set Microsoft Edge as the default browser on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="394e7-105">Cet article concerne MicrosoftEdge version77 ou ultérieure sur Windows8 et Windows10.</span><span class="sxs-lookup"><span data-stu-id="394e7-105">This article applies to Microsoft Edge version 77 or later on Windows 8 and Windows 10.</span></span> <span data-ttu-id="394e7-106">Pour Windows7 et macOS, consultez la stratégie [Définir MicrosoftEdge comme navigateur par défaut](./microsoft-edge-policies.md#defaultbrowsersettingenabled).</span><span class="sxs-lookup"><span data-stu-id="394e7-106">For Windows 7 and macOS, see the [Set Microsoft Edge as default browser](./microsoft-edge-policies.md#defaultbrowsersettingenabled) policy.</span></span>

## <a name="introduction"></a><span data-ttu-id="394e7-107">Introduction</span><span class="sxs-lookup"><span data-stu-id="394e7-107">Introduction</span></span>

<span data-ttu-id="394e7-108">Vous pouvez utiliser la stratégie de groupe **Définir un fichier de configuration des associations par défaut** ou le paramètre de Gestion des appareils mobiles [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) pour définir MicrosoftEdge comme navigateur par défaut pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="394e7-108">You can use the **Set a default associations configuration file** Group Policy or the [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) Mobile Device Management setting to set Microsoft Edge as the default browser for your organization.</span></span>

<span data-ttu-id="394e7-109">Pour définir MicrosoftEdge Stable comme navigateur par défaut pour les fichiers html et les liens http/https et les fichiers PDF, utilisez l’exemple de fichier d’association d’application suivant:</span><span class="sxs-lookup"><span data-stu-id="394e7-109">To set Microsoft Edge Stable as the default browser for html files, http/https links, and PDF files use the following application association file example:</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations> 
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> <span data-ttu-id="394e7-110">Pour définir MicrosoftEdge Beta en tant que navigateur par défaut, définissez **ApplicationName** sur «MicrosoftEdge Dev» et **ProgId** sur «MSEdgeBHTML».</span><span class="sxs-lookup"><span data-stu-id="394e7-110">To set Microsoft Edge Beta as the default browser, set **ApplicationName** to "Microsoft Edge Beta" and **ProgId** to "MSEdgeBHTML".</span></span> <span data-ttu-id="394e7-111">Pour définir MicrosoftEdge Dev en tant que navigateur par défaut, définissez **ApplicationName** sur «MicrosoftEdge Dev» et **ProgId** sur «MSEdgeDHTML».</span><span class="sxs-lookup"><span data-stu-id="394e7-111">To set Microsoft Edge Dev as the default browser, set **ApplicationName** to "Microsoft Edge Dev" and **ProgId** to "MSEdgeDHTML".</span></span>


> [!NOTE]
> <span data-ttu-id="394e7-112">Les associations de fichiers par défaut ne sont pas appliquées si MicrosoftEdge n’est pas installé sur le périphérique cible.</span><span class="sxs-lookup"><span data-stu-id="394e7-112">The default file associations aren't applied if Microsoft Edge isn't installed on the target device.</span></span> <span data-ttu-id="394e7-113">Dans ce scénario, les utilisateurs sont invités à sélectionner leur application par défaut lorsqu’ils ouvrent un lien ou un fichier htm/html.</span><span class="sxs-lookup"><span data-stu-id="394e7-113">In this scenario, users are prompted to select their default application when they open a link or a htm/html file.</span></span>

## <a name="set-microsoft-edge-as-the-default-browser-on-domain-joined-devices"></a><span data-ttu-id="394e7-114">Définir MicrosoftEdge comme navigateur par défaut</span><span class="sxs-lookup"><span data-stu-id="394e7-114">Set Microsoft Edge as the default browser on domain-joined devices</span></span>

<span data-ttu-id="394e7-115">Vous pouvez définir Microsoft Edge comme navigateur par défaut sur les périphériques joints par domaine en configurant la stratégie de groupe **Définir un fichier de configuration des associations par défaut**.</span><span class="sxs-lookup"><span data-stu-id="394e7-115">You can set Microsoft Edge as the default browser on domain-joined devices by configuring the **Set a default associations configuration file** group policy.</span></span> <span data-ttu-id="394e7-116">Si vous activez ce paramètre, vous devez également créer et stocker un fichier de configuration des associations par défaut, en local ou sur un partage réseau.</span><span class="sxs-lookup"><span data-stu-id="394e7-116">Turning this group policy on requires you to create and store a default associations configuration file.</span></span> <span data-ttu-id="394e7-117">Ce fichier est stocké localement ou sur un partage réseau.</span><span class="sxs-lookup"><span data-stu-id="394e7-117">This file is stored locally or on a network share.</span></span> <span data-ttu-id="394e7-118">Pour en savoir plus sur la création de ce fichier, consultez [Exporter ou importer des associations d’applications par défaut](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).</span><span class="sxs-lookup"><span data-stu-id="394e7-118">For more information about creating this file, see [Export or Import Default Application Associations](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).</span></span>

### <a name="to-configure-the-group-policy-for-a-default-file-type-and-protocol-associations-configuration-file"></a><span data-ttu-id="394e7-119">Pour configurer la stratégie de groupe pour un type de fichier par défaut et un fichier de configuration d’associations de protocoles:</span><span class="sxs-lookup"><span data-stu-id="394e7-119">To configure the group policy for a default file type and protocol associations configuration file:</span></span>

1. <span data-ttu-id="394e7-120">Ouvrez l’éditeur de stratégie de groupe et accédez à **Configuration de l’ordinateur\Modèles d’administration\Composants Windows\Explorateur de fichiers**.</span><span class="sxs-lookup"><span data-stu-id="394e7-120">Open the Group Policy editor and go to the **Computer Configuration\Administrative Templates\Windows Components\File Explorer**.</span></span>
2. <span data-ttu-id="394e7-121">Sélectionnez **Définir un fichier de configuration des associations par défaut**.</span><span class="sxs-lookup"><span data-stu-id="394e7-121">Select **Set a default associations configuration file**.</span></span>
3. <span data-ttu-id="394e7-122">Cliquez sur **Paramètre de stratégie**, puis sur **Activé**.</span><span class="sxs-lookup"><span data-stu-id="394e7-122">Click **policy setting**, and then click **Enabled**.</span></span>
4. <span data-ttu-id="394e7-123">Cliquez sur **Activé** puis, dans la zone Options, saisissez l’emplacement dans votre fichier de configuration des associations par défaut.</span><span class="sxs-lookup"><span data-stu-id="394e7-123">Under **Options:**, type the location to your default associations configuration file.</span></span>
5. <span data-ttu-id="394e7-124">Cliquez sur **OK** pour enregistrer le paramètre.</span><span class="sxs-lookup"><span data-stu-id="394e7-124">Click **OK** to save the policy settings.</span></span>

<span data-ttu-id="394e7-125">L’exemple de la capture d’écran suivante montre un fichier d’associations nommé *appassoc.xml* sur un partage réseau qui est accessible à partir du périphérique cible.</span><span class="sxs-lookup"><span data-stu-id="394e7-125">The example in the next screenshot shows an associations file named *appassoc.xml* on a network share that is accessible from the target device.</span></span>

   ![Activer l’association de fichiers dans la stratégie de groupe](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > <span data-ttu-id="394e7-127">Si ce paramètre est activé et que le périphérique de l’utilisateur est joint au domaine, le fichier de configuration des associations est traité la fois suivante où l’utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="394e7-127">If this setting is enabled and the user's device is domain-joined, the associations configuration file is processed the next time the user signs on.</span></span>

## <a name="set-microsoft-edge-as-the-default-browser-on-azure-active-directory-joined-devices"></a><span data-ttu-id="394e7-128">Définir MicrosoftEdge comme navigateur par défaut sur les périphériques Azure Active Directory joints</span><span class="sxs-lookup"><span data-stu-id="394e7-128">Set Microsoft Edge as the default browser on Azure Active Directory joined devices</span></span>

<span data-ttu-id="394e7-129">Pour définir MicrosoftEdge comme navigateur par défaut sur les périphériques Azure ActiveDirectory joints, suivez la procédure présentée dans le paramètre [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) de Gestion des appareils mobiles en utilisant l’exemple de fichier d’association d’application suivant.</span><span class="sxs-lookup"><span data-stu-id="394e7-129">To set Microsoft Edge as the default browser on Azure Active Directory joined devices follow the steps in the [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) Mobile Device Management setting using the following application association file as an example.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> <span data-ttu-id="394e7-130">Pour définir MicrosoftEdge Beta en tant que navigateur par défaut, définissez **ApplicationName** sur «MicrosoftEdge Dev» et **ProgId** sur «MSEdgeBHTML».</span><span class="sxs-lookup"><span data-stu-id="394e7-130">To set Microsoft Edge Beta as the default browser, set **ApplicationName** to "Microsoft Edge Beta" and **ProgId** to "MSEdgeBHTML".</span></span> <span data-ttu-id="394e7-131">Pour définir MicrosoftEdge Dev en tant que navigateur par défaut, définissez **ApplicationName** sur «MicrosoftEdge Dev» et **ProgId** sur «MSEdgeDHTML».</span><span class="sxs-lookup"><span data-stu-id="394e7-131">To set Microsoft Edge Dev as the default browser, set **ApplicationName** to "Microsoft Edge Dev" and **ProgId** to "MSEdgeDHTML".</span></span>

## <a name="set-microsoft-edge-as-the-default-browser-on-macos"></a><span data-ttu-id="394e7-132">Définir MicrosoftEdge comme navigateur par défaut sur macOS</span><span class="sxs-lookup"><span data-stu-id="394e7-132">Set Microsoft Edge as the default browser on macOS</span></span>

<span data-ttu-id="394e7-133">Si vous tentez de définir par programmation le navigateur par défaut sur macOS, une invite s’affiche pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="394e7-133">Attempting to programmatically set the default browser on macOS causes a prompt to appear for the end user.</span></span> <span data-ttu-id="394e7-134">Cette invite est une fonctionnalité de sécurité macOS qui ne peut être automatisée qu’à l’aide d’un AppleScript.</span><span class="sxs-lookup"><span data-stu-id="394e7-134">This prompt is a macOS security feature that can only be automated away by using an AppleScript.</span></span>

<span data-ttu-id="394e7-135">En raison de cette limitation, il existe deux méthodes principales pour définir MicrosoftEdge comme navigateur par défaut sur un macOS.</span><span class="sxs-lookup"><span data-stu-id="394e7-135">Because of this limitation, there are two main methods for setting Microsoft Edge as the default browser on a macOS.</span></span> <span data-ttu-id="394e7-136">La première option consiste à flasher l’appareil avec une image de macOS où MicrosoftEdge a déjà été défini comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="394e7-136">The first option is to flash the device with an image of macOS where Microsoft Edge has already been set as the default browser.</span></span> <span data-ttu-id="394e7-137">L’autre option consiste à utiliser la stratégie  [Définir MicrosoftEdge comme navigateur par défaut](./microsoft-edge-policies.md#defaultbrowsersettingenabled) , qui invite l’utilisateur à définir MicrosoftEdge comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="394e7-137">The other option is to use the [Set Microsoft Edge as default browser](./microsoft-edge-policies.md#defaultbrowsersettingenabled) policy, which prompts the user to set Microsoft Edge as the default browser.</span></span>

<span data-ttu-id="394e7-138">Lorsque vous utilisez l’une de ces méthodes, il est toujours possible pour un utilisateur de modifier le navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="394e7-138">When using either of these methods, it is still possible for a user to change the default browser.</span></span> <span data-ttu-id="394e7-139">Cela est dû au fait que, pour des raisons de sécurité, la préférence de navigateur par défaut ne peut pas être bloquée par programmation.</span><span class="sxs-lookup"><span data-stu-id="394e7-139">This is because for security reasons, the default browser preference can’t be blocked programmatically.</span></span> <span data-ttu-id="394e7-140">Pour cette raison, nous vous recommandons de déployer la stratégie **Définir MicrosoftEdge comme navigateur par défaut** , même si vous créez une image avec MicrosoftEdge comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="394e7-140">For this reason, we recommend that you deploy the **Set Microsoft Edge as default browser** policy even if you create an image with Microsoft Edge as the default browser.</span></span> <span data-ttu-id="394e7-141">Si la stratégie est définie et qu’un utilisateur change le navigateur par défaut la prochaine fois qu’il ouvrira MicrosoftEdge, il sera invité à le définir comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="394e7-141">If the policy is set and a user changes the default browser from Microsoft Edge the next time they open Microsoft Edge, they will be prompted to set it as the default.</span></span>

## <a name="see-also"></a><span data-ttu-id="394e7-142">Articles associés</span><span class="sxs-lookup"><span data-stu-id="394e7-142">See also</span></span>

- [<span data-ttu-id="394e7-143">Planifier votre déploiement de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="394e7-143">Plan your deployment of Microsoft Edge</span></span>](./deploy-edge-plan-deployment.md)
- [<span data-ttu-id="394e7-144">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="394e7-144">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="394e7-145">Définir MicrosoftEdge comme navigateur par défaut (Windows7 et macOS)</span><span class="sxs-lookup"><span data-stu-id="394e7-145">Set Microsoft Edge as default browser (Windows 7 and macOS)</span></span>](./microsoft-edge-policies.md#defaultbrowsersettingenabled)
- [<span data-ttu-id="394e7-146">Windows10: comment configurer des associations de fichiers pour les professionnels de l’informatique?</span><span class="sxs-lookup"><span data-stu-id="394e7-146">Windows 10 – How to configure file associations for IT Pros?</span></span>](/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [<span data-ttu-id="394e7-147">Pour en savoir plus sur la création de ce fichier, voir Exporter ou importer des associations d’applications par défaut.</span><span class="sxs-lookup"><span data-stu-id="394e7-147">Export or Import Default Application Associations</span></span>](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [<span data-ttu-id="394e7-148">Vue d’ensemble du module de plateforme sécurisée (DISM)</span><span class="sxs-lookup"><span data-stu-id="394e7-148">DISM Overview</span></span>](/windows-hardware/manufacture/desktop/what-is-dism)
  - [<span data-ttu-id="394e7-149">DISM (Deployment Image Servicing and Management) - Gestion et maintenance des images de déploiement</span><span class="sxs-lookup"><span data-stu-id="394e7-149">DISM - Deployment Image Servicing and Management</span></span>](/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)