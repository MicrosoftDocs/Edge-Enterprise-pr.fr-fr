---
title: Configurer Microsoft Edge pour macOS à l'aide d'un fichier .plist
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer les paramètres de stratégie MicrosoftEdge sur macOS à l'aide d'un fichier .plist
ms.openlocfilehash: 3f297c11d8009c85a1bc5e17447681ee2b9ef1e2
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447448"
---
# <a name="configure-microsoft-edge-policy-settings-for-macos-using-a-plist"></a><span data-ttu-id="a3aac-103">Configurer les paramètres de stratégie MicrosoftEdge pour macOS à l'aide d'un fichier .plist</span><span class="sxs-lookup"><span data-stu-id="a3aac-103">Configure Microsoft Edge policy settings for macOS using a .plist</span></span>

<span data-ttu-id="a3aac-104">Cet article explique comment configurer MicrosoftEdge sur macOS à l’aide d’un fichier de liste de propriétés (.plist).</span><span class="sxs-lookup"><span data-stu-id="a3aac-104">This article describes how to configure Microsoft Edge on macOS using a property list (.plist) file.</span></span> <span data-ttu-id="a3aac-105">Découvrez la création et le déploiement de ce fichier dans Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="a3aac-105">You'll learn how to create this file and then deploy it to Microsoft Intune.</span></span>

<span data-ttu-id="a3aac-106">Pour plus d’informations, consultez [À propos des fichiers de listes de propriétés d’informations](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (site web d’Apple) et [Paramètres de charge utile personnalisés](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).</span><span class="sxs-lookup"><span data-stu-id="a3aac-106">For more information, see [About Information Property List Files](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple's website) and [Custom payload settings](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).</span></span>

> [!NOTE]
> <span data-ttu-id="a3aac-107">Cet article concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a3aac-107">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="configure-microsoft-edge-policies-on-macos"></a><span data-ttu-id="a3aac-108">Configurer les stratégies MicrosoftEdge sur macOS</span><span class="sxs-lookup"><span data-stu-id="a3aac-108">Configure Microsoft Edge policies on macOS</span></span>

<span data-ttu-id="a3aac-109">La première étape consiste à créer une soumission.</span><span class="sxs-lookup"><span data-stu-id="a3aac-109">The first step is to create your plist.</span></span> <span data-ttu-id="a3aac-110">Vous pouvez créer le fichier plist avec n’importe quel éditeur de texte ou vous pouvez utiliser [Terminal pour créer le profil de configuration](#create-a-configuration-profile-using-terminal).</span><span class="sxs-lookup"><span data-stu-id="a3aac-110">You can create the plist file with any text editor or you can use [Terminal to create the configuration profile](#create-a-configuration-profile-using-terminal).</span></span> <span data-ttu-id="a3aac-111">Toutefois, il est plus facile de créer et de modifier un fichier plist à l’aide d’un outil qui met en forme le code XML à votre place.</span><span class="sxs-lookup"><span data-stu-id="a3aac-111">However, it's easier to create and edit a plist file using a tool that formats the XML code for you.</span></span> <span data-ttu-id="a3aac-112">*Xcode* est un environnement de développement intégré gratuit que vous pouvez obtenir de l’une des manières suivantes:</span><span class="sxs-lookup"><span data-stu-id="a3aac-112">*Xcode* is a free integrated development environment that you can get from one of the following locations:</span></span>

- [<span data-ttu-id="a3aac-113">Site web des développeurs Apple</span><span class="sxs-lookup"><span data-stu-id="a3aac-113">Apple developer website</span></span>](https://developer.apple.com/xcode/)
- [<span data-ttu-id="a3aac-114">AppStore Mac</span><span class="sxs-lookup"><span data-stu-id="a3aac-114">Mac App Store</span></span>](https://apps.apple.com/app/xcode/id497799835?mt=12)

<span data-ttu-id="a3aac-115">Pour obtenir la liste des stratégies prises en charge et leurs noms de clé de préférence, consultez [Référence sur les stratégies de navigateur MicrosoftEdge](microsoft-edge-policies.md).</span><span class="sxs-lookup"><span data-stu-id="a3aac-115">For a list of supported policies and their preference key names, see [Microsoft Edge browser policies reference](microsoft-edge-policies.md).</span></span> <span data-ttu-id="a3aac-116">Le fichier de modèles de stratégie, qui peut être téléchargé à partir de la [page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise) contient un exemple de plist (*itadminexample.plist*) dans le dossier d’**exemples**.</span><span class="sxs-lookup"><span data-stu-id="a3aac-116">In the policy templates file, which can be downloaded from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise), there's an example plist (*itadminexample.plist*) in the **examples** folder.</span></span> <span data-ttu-id="a3aac-117">L’exemple de fichier contient tous les types de données pris en charge que vous pouvez personnaliser pour définir vos paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="a3aac-117">The example file contains all supported data types that you can customize to define your policy settings.</span></span> 

<span data-ttu-id="a3aac-118">L’étape suivante, après la création du contenu de votre plist, consiste à la nommer en utilisant le domaine de préférence Microsoft Edge, *com.microsoft.Edge*.</span><span class="sxs-lookup"><span data-stu-id="a3aac-118">The next step after you create the contents of your plist, is to name it using the Microsoft Edge preference domain, *com.microsoft.Edge*.</span></span> <span data-ttu-id="a3aac-119">Le nom respecte la casse et ne doit pas contenir le canal que vous ciblez, car il s’applique à tous les canaux MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="a3aac-119">The name is case sensitive and should not include the channel you are targeting because it applies to all Microsoft Edge channels.</span></span> <span data-ttu-id="a3aac-120">Le nom du fichier plist doit être **_com.microsoft.Edge.plist_**.</span><span class="sxs-lookup"><span data-stu-id="a3aac-120">The plist file name must be **_com.microsoft.Edge.plist_**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a3aac-121">À partir de la build78.0.249.2, tous les canaux MicrosoftEdge sur macOS lisent à partir du domaine de préférence **com.microsoft.Edge**.</span><span class="sxs-lookup"><span data-stu-id="a3aac-121">Starting with build 78.0.249.2, all Microsoft Edge channels on macOS read from the **com.microsoft.Edge** preference domain.</span></span> <span data-ttu-id="a3aac-122">Toutes les versions antérieures lisent à partir d’un domaine spécifique du canal, tel que **com.microsoft.Edge.Dev** pour le canal Dev.</span><span class="sxs-lookup"><span data-stu-id="a3aac-122">All prior releases read from a channel specific domain, such as **com.microsoft.Edge.Dev** for Dev channel.</span></span>

<span data-ttu-id="a3aac-123">La dernière étape consiste à déployer votre plist sur les appareils Mac de vos utilisateurs à l’aide de votre fournisseur GPM préféré, tel que MicrosoftIntune.</span><span class="sxs-lookup"><span data-stu-id="a3aac-123">The last step is to deploy your plist to your users' Mac devices using your preferred MDM provider, such as Microsoft Intune.</span></span> <span data-ttu-id="a3aac-124">Pour obtenir des instructions, consultez [Déployer votre plist](#deploy-your-plist).</span><span class="sxs-lookup"><span data-stu-id="a3aac-124">For instructions see [Deploy your plist](#deploy-your-plist).</span></span>

### <a name="create-a-configuration-profile-using-terminal"></a><span data-ttu-id="a3aac-125">Créer un profil de configuration à l’aide de terminal</span><span class="sxs-lookup"><span data-stu-id="a3aac-125">Create a configuration profile using Terminal</span></span>

1. <span data-ttu-id="a3aac-126">Dans Terminal, utilisez la commande suivante pour créer un plist MicrosoftEdge sur votre bureau avec vos paramètres préférés:</span><span class="sxs-lookup"><span data-stu-id="a3aac-126">In Terminal, use the following command to create a plist for Microsoft Edge on your desktop with your preferred settings:</span></span>

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. <span data-ttu-id="a3aac-127">Convertissez la plist d’un format binaire en format texte brut:</span><span class="sxs-lookup"><span data-stu-id="a3aac-127">Convert the plist from binary to plain text format:</span></span>

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```

<span data-ttu-id="a3aac-128">Après avoir converti le fichier, vérifiez que vos données de stratégie sont correctes et qu’elles contiennent les paramètres de votre choix pour votre profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="a3aac-128">After converting the file verify that your policy data is correct and contains the settings you want for your configuration profile.</span></span>

> [!NOTE]
> <span data-ttu-id="a3aac-129">Seules les paires de valeurs de clé doivent figurer dans le contenu du fichier plist ou XML.</span><span class="sxs-lookup"><span data-stu-id="a3aac-129">Only key value pairs should be in the contents of the plist or xml file.</span></span> <span data-ttu-id="a3aac-130">Avant de télécharger votre fichier dans Intune, supprimez toutes les valeurs \<plist> et \<dict>, ainsi que les en-têtes XML de votre fichier.</span><span class="sxs-lookup"><span data-stu-id="a3aac-130">Prior to uploading your file into Intune remove all the \<plist> and \<dict> values, and xml headers from your file.</span></span> <span data-ttu-id="a3aac-131">Le fichier ne doit contenir que des paires clé-valeur.</span><span class="sxs-lookup"><span data-stu-id="a3aac-131">The file should only contain key value pairs.</span></span>

## <a name="deploy-your-plist"></a><span data-ttu-id="a3aac-132">Déployer votre plist</span><span class="sxs-lookup"><span data-stu-id="a3aac-132">Deploy your plist</span></span>

<span data-ttu-id="a3aac-133">Pour MicrosoftIntune créez un profil de configuration de périphérique ciblant la plateforme macOS et sélectionnez le type de profil *Fichier de préférence*.</span><span class="sxs-lookup"><span data-stu-id="a3aac-133">For Microsoft Intune create a new device configuration profile targeting the macOS platform and select the *Preference file* profile type.</span></span> <span data-ttu-id="a3aac-134">Ciblez **com.microsoft.Edge** comme nom de domaine de préférence et téléchargez votre plist.</span><span class="sxs-lookup"><span data-stu-id="a3aac-134">Target **com.microsoft.Edge** as the preference domain name and upload your plist.</span></span> <span data-ttu-id="a3aac-135">Pour plus d’informations, consultez [Ajouter un fichier de liste de propriétés à des périphériques macOS à l’aide de Microsoft Intune](/intune/configuration/preference-file-settings-macos).</span><span class="sxs-lookup"><span data-stu-id="a3aac-135">For more information see [Add a property list file to macOS devices using Microsoft Intune](/intune/configuration/preference-file-settings-macos).</span></span>

<span data-ttu-id="a3aac-136">Pour Jamf, téléchargez le fichier plist en tant que charge utile des *Paramètres personnalisés*.</span><span class="sxs-lookup"><span data-stu-id="a3aac-136">For Jamf upload the .plist file as a *Custom Settings* payload.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3aac-137">Voir également</span><span class="sxs-lookup"><span data-stu-id="a3aac-137">See also</span></span>

- [<span data-ttu-id="a3aac-138">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="a3aac-138">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="a3aac-139">Configurer pour macOS avec Jamf</span><span class="sxs-lookup"><span data-stu-id="a3aac-139">Configure for macOS with Jamf</span></span>](configure-microsoft-edge-on-mac-jamf.md)
- [<span data-ttu-id="a3aac-140">Configurer pour Windows</span><span class="sxs-lookup"><span data-stu-id="a3aac-140">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="a3aac-141">Configurer pour Windows avec Intune</span><span class="sxs-lookup"><span data-stu-id="a3aac-141">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)