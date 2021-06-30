---
title: Associer les extensions de fichier avec le mode Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Associer les extensions de fichier avec le mode Internet Explorer
ms.openlocfilehash: c027b11e426cd665cb9e6cc25b4c9f66a0c6762a
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617454"
---
# <a name="associate-file-extensions-with-internet-explorer-mode"></a><span data-ttu-id="36c95-103">Associer les extensions de fichier avec le mode InternetExplorer</span><span class="sxs-lookup"><span data-stu-id="36c95-103">Associate file extensions with Internet Explorer mode</span></span>

>[!Note]
> <span data-ttu-id="36c95-104">L’application de bureau Internet Explorer 11 sera retirée et ne sera plus prise en charge le 15 juin 2022 (pour obtenir la liste des éléments concernés, [consultez le FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span><span class="sxs-lookup"><span data-stu-id="36c95-104">The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span></span> <span data-ttu-id="36c95-105">Les mêmes applications et sites IE11 que vous utilisez aujourd’hui peuvent s’ouvrir dans Microsoft Edge avec le mode Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="36c95-105">The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode.</span></span> <span data-ttu-id="36c95-106">[Apprenez-en plus ici](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span><span class="sxs-lookup"><span data-stu-id="36c95-106">[Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span></span>

<span data-ttu-id="36c95-107">Cet article explique comment associer Microsoft Edge au mode Internet Explorer avec des extensions de fichier pour applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="36c95-107">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="36c95-108">Cet article concerne Microsoft Edge version 86 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="36c95-108">This article applies to Microsoft Edge version 86 or later.</span></span>

## <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a><span data-ttu-id="36c95-109">Recommandations en matière d’association d’extensions de fichier avec le mode Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="36c95-109">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="36c95-110">Les instructions suivantes indiquent une entrée qui associe Microsoft Edge au mode IE avec le type de fichier .mht.</span><span class="sxs-lookup"><span data-stu-id="36c95-110">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="36c95-111">Pour définir une association de fichiers, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="36c95-111">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="36c95-112">Vous pouvez définir des extensions de fichier spécifiques pour que ces fichiers s’ouvrent en mode Internet Explorer par défaut via la stratégie pour **Définir un fichier de configuration des associations par défaut**.</span><span class="sxs-lookup"><span data-stu-id="36c95-112">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="36c95-113">Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Fournisseur de solutions Cloud de stratégie : ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="36c95-113">For more information, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="36c95-114">Définissez un nouvel identificateur ProgID avec le canal Microsoft Edge. Cet identificateur sera nécessaire pour ouvrir des fichiers en mode Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="36c95-114">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="36c95-115">L’identificateur ProgID inclut le nom et l’icône de l’application, ainsi que le chemin d’accès complet au fichier msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="36c95-115">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="36c95-116">Configurez les mises à jour de l’interpréteur de commandes pour transmettre la ligne de commande nécessaire à l’ouverture en mode IE.</span><span class="sxs-lookup"><span data-stu-id="36c95-116">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="36c95-117">Enfin, associez l’extension de fichier .mht à un nouvel identificateur ProgID.</span><span class="sxs-lookup"><span data-stu-id="36c95-117">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="36c95-118">Ajoutez votre identificateur ProgID en tant que nom de valeur, avec le type de valeur REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="36c95-118">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="36c95-119">Une fois que vous avez défini les clés décrites dans l’exemple précédent, une option supplémentaire s’affiche dans le menu **Ouvrir avec** de vos utilisateurs. Cette option permet d’ouvrir un fichier .mht avec Microsoft Edge \<channel\> en mode IE.</span><span class="sxs-lookup"><span data-stu-id="36c95-119">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <a name="registry-example"></a><span data-ttu-id="36c95-120">Exemple de registre</span><span class="sxs-lookup"><span data-stu-id="36c95-120">Registry Example</span></span>

<span data-ttu-id="36c95-121">Vous pouvez enregistrer l’extrait de code suivant sous la forme d’un fichier .reg, puis l’importer dans le registre.</span><span class="sxs-lookup"><span data-stu-id="36c95-121">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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

## <a name="configuring-file-types-to-open-in-internet-explorer-mode"></a><span data-ttu-id="36c95-122">Configurer l’ouverture de types de fichiers dans le mode Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="36c95-122">Configuring file types to open in Internet Explorer mode</span></span>

<span data-ttu-id="36c95-123">À partir Edge 88, vous pouvez configurer des liens de types de fichiers spécifiques pour qu'ils s'ouvrent dans le mode Internet Explorer à l'aide de la stratégie [Afficher le menu contextuel pour ouvrir les liens dans le mode Internet Explorer](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed).</span><span class="sxs-lookup"><span data-stu-id="36c95-123">Starting Edge 88, you can configure specific file type links to open in Internet Explorer mode using the policy [Show context menu to open links in Internet Explorer mode](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed).</span></span>

<span data-ttu-id="36c95-124">Vous pouvez définir les types de fichiers auxquels cette option doit s'appliquer, en spécifiant les extensions de fichiers dans cette stratégie [Ouvrir des fichiers locaux dans le mode Internet Explorer Liste des extensions de fichiers autorisées](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span><span class="sxs-lookup"><span data-stu-id="36c95-124">You can define file types this option should apply to, by specifying file extensions in this policy [Open local files in Internet Explorer mode file extension allow list](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span></span> 

## <a name="see-also"></a><span data-ttu-id="36c95-125">Voir également</span><span class="sxs-lookup"><span data-stu-id="36c95-125">See also</span></span>

- [<span data-ttu-id="36c95-126">À propos du mode IE</span><span class="sxs-lookup"><span data-stu-id="36c95-126">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="36c95-127">Informations sur les sites configurables</span><span class="sxs-lookup"><span data-stu-id="36c95-127">Configurable sites information</span></span>](./edge-learnmore-configurable-sites-ie-mode.md)
- [<span data-ttu-id="36c95-128">Informations supplémentaires sur le mode entreprise</span><span class="sxs-lookup"><span data-stu-id="36c95-128">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="36c95-129">Définition des associations de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="36c95-129">Setting file type associations</span></span>](/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="36c95-130">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="36c95-130">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)