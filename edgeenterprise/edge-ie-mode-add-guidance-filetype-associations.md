---
title: Associer les extensions de fichier avec le mode Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Associer les extensions de fichier avec le mode Internet Explorer
ms.openlocfilehash: 9f39a3319c3e45001090dd9f0cffb3e7ce2648fb
ms.sourcegitcommit: 306582403d4272831bcac390154c7cc7041a9b7e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/21/2020
ms.locfileid: "11238191"
---
# <span data-ttu-id="0df60-103">Associer les extensions de fichier avec le mode Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="0df60-103">Associate file extensions with Internet Explorer mode</span></span>

<span data-ttu-id="0df60-104">Cet article explique comment associer Microsoft Edge au mode Internet Explorer avec des extensions de fichier pour applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="0df60-104">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="0df60-105">Cet article concerne MicrosoftEdge version86 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0df60-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="0df60-106">Recommandations en matière d’association d’extensions de fichier avec le mode Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="0df60-106">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="0df60-107">Les instructions suivantes indiquent une entrée qui associe Microsoft Edge au mode IE avec le type de fichier .mht.</span><span class="sxs-lookup"><span data-stu-id="0df60-107">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="0df60-108">Pour définir une association de fichiers, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="0df60-108">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="0df60-109">Vous pouvez définir des extensions de fichier spécifiques pour que ces fichiers s’ouvrent en mode Internet Explorer par défaut via la stratégie pour **Définir un fichier de configuration des associations par défaut**.</span><span class="sxs-lookup"><span data-stu-id="0df60-109">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="0df60-110">Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Fournisseur de solutions Cloud de stratégie: ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="0df60-110">For more information, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="0df60-111">Définissez un nouvel identificateur ProgID avec le canal Microsoft Edge. Cet identificateur sera nécessaire pour ouvrir des fichiers en mode Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0df60-111">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="0df60-112">L’identificateur ProgID inclut le nom et l’icône de l’application, ainsi que le chemin d’accès complet au fichier msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="0df60-112">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""
```

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"
```

2. <span data-ttu-id="0df60-113">Configurez les mises à jour de l’interpréteur de commandes pour transmettre la ligne de commande nécessaire à l’ouverture en mode IE.</span><span class="sxs-lookup"><span data-stu-id="0df60-113">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="0df60-114">Enfin, associez l’extension de fichier .mht à un nouvel identificateur ProgID.</span><span class="sxs-lookup"><span data-stu-id="0df60-114">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="0df60-115">Ajoutez votre identificateur ProgID en tant que nom de valeur, avec le type de valeur REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="0df60-115">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="0df60-116">Une fois que vous avez défini les clés décrites dans l’exemple précédent, une option supplémentaire s’affiche dans le menu **Ouvrir avec** de vos utilisateurs. Cette option permet d’ouvrir un fichier .mht avec Microsoft Edge \<channel\> en mode IE.</span><span class="sxs-lookup"><span data-stu-id="0df60-116">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <span data-ttu-id="0df60-117">Exemple de registre</span><span class="sxs-lookup"><span data-stu-id="0df60-117">Registry Example</span></span>

<span data-ttu-id="0df60-118">Vous pouvez enregistrer l’extrait de code suivant sous la forme d’un fichier .reg, puis l’importer dans le registre.</span><span class="sxs-lookup"><span data-stu-id="0df60-118">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

```markdown
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""

```
## <span data-ttu-id="0df60-119">Configurer l’ouverture de types de fichiers dans le mode Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="0df60-119">Configuring file types to open in Internet Explorer mode</span></span>

<span data-ttu-id="0df60-120">À partir Edge 88, vous pouvez configurer des liens de types de fichiers spécifiques pour qu'ils s'ouvrent dans le mode Internet Explorer à l'aide de la stratégie [Afficher le menu contextuel pour ouvrir les liens dans le mode Internet Explorer](https://docs.microsoft.com/deployedge/microsoft-edge-policies#show-context-menu-to-open-a-link-in-internet-explorer-mode).</span><span class="sxs-lookup"><span data-stu-id="0df60-120">Starting Edge 88, you can configure specific file type links to open in Internet Explorer mode using the policy [Show context menu to open links in Internet Explorer mode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#show-context-menu-to-open-a-link-in-internet-explorer-mode).</span></span> 

<span data-ttu-id="0df60-121">Vous pouvez définir les types de fichiers auxquels cette option doit s'appliquer, en spécifiant les extensions de fichiers dans cette stratégie [Ouvrir des fichiers locaux dans le mode Internet Explorer Liste des extensions de fichiers autorisées](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist).</span><span class="sxs-lookup"><span data-stu-id="0df60-121">You can define file types this option should apply to, by specifying file extensions in this policy [Open local files in Internet Explorer mode file extension allow list](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist).</span></span> 

## <span data-ttu-id="0df60-122">Voir également</span><span class="sxs-lookup"><span data-stu-id="0df60-122">See also</span></span>

- [<span data-ttu-id="0df60-123">À propos du mode IE</span><span class="sxs-lookup"><span data-stu-id="0df60-123">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="0df60-124">Informations sur les sites configurables</span><span class="sxs-lookup"><span data-stu-id="0df60-124">Configurable sites information</span></span>](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [<span data-ttu-id="0df60-125">Informations supplémentaires sur le mode entreprise</span><span class="sxs-lookup"><span data-stu-id="0df60-125">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="0df60-126">Définition des associations de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="0df60-126">Setting file type associations</span></span>](https://docs.microsoft.com/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="0df60-127">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="0df60-127">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
