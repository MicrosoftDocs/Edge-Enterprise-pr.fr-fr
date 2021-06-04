---
title: Associer les extensions de fichier avec le mode Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Associer les extensions de fichier avec le mode Internet Explorer
ms.openlocfilehash: 63ab0bb8eafda093dedbed0c38a6763e0c054cdf
ms.sourcegitcommit: c7c326c97926764d2d614520c1c8dc2546254c98
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "11218920"
---
# Associer les extensions de fichier avec le mode Internet Explorer

Cet article explique comment associer Microsoft Edge au mode Internet Explorer avec des extensions de fichier pour applications de bureau.

> [!NOTE]
> Cet article concerne Microsoft Edge version 86 ou ultérieure.

##  <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a>Recommandations en matière d’association d’extensions de fichier avec le mode Internet Explorer

Les instructions suivantes indiquent une entrée qui associe Microsoft Edge au mode IE avec le type de fichier .mht. Pour définir une association de fichiers, procédez comme suit.

> [!NOTE]
> Vous pouvez définir des extensions de fichier spécifiques pour que ces fichiers s’ouvrent en mode Internet Explorer par défaut via la stratégie pour **Définir un fichier de configuration des associations par défaut**. Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Fournisseur de solutions Cloud de stratégie : ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

1. Définissez un nouvel identificateur ProgID avec le canal Microsoft Edge. Cet identificateur sera nécessaire pour ouvrir des fichiers en mode Internet Explorer. L’identificateur ProgID inclut le nom et l’icône de l’application, ainsi que le chemin d’accès complet au fichier msedge.exe.

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

2. Configurez les mises à jour de l’interpréteur de commandes pour transmettre la ligne de commande nécessaire à l’ouverture en mode IE.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. Enfin, associez l’extension de fichier .mht à un nouvel identificateur ProgID. Ajoutez votre identificateur ProgID en tant que nom de valeur, avec le type de valeur REG_SZ.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

Une fois que vous avez défini les clés décrites dans l’exemple précédent, une option supplémentaire s’affiche dans le menu **Ouvrir avec** de vos utilisateurs. Cette option permet d’ouvrir un fichier .mht avec Microsoft Edge \<channel\> en mode IE.

##  <a name="registry-example"></a>Exemple de registre

Vous pouvez enregistrer l’extrait de code suivant sous la forme d’un fichier .reg, puis l’importer dans le registre.

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
##  <a name="configuring-file-types-to-open-in-internet-explorer-mode"></a>Configurer l’ouverture de types de fichiers dans le mode Internet Explorer

À partir Edge 88, vous pouvez configurer des liens de types de fichiers spécifiques pour qu'ils s'ouvrent dans le mode Internet Explorer à l'aide de la stratégie [Afficher le menu contextuel pour ouvrir les liens dans le mode Internet Explorer](https://docs.microsoft.com/deployedge/microsoft-edge-policies#show-context-menu-to-open-a-link-in-internet-explorer-mode). 

Vous pouvez définir les types de fichiers auxquels cette option doit s'appliquer, en spécifiant les extensions de fichiers dans cette stratégie [Ouvrir des fichiers locaux dans le mode Internet Explorer Liste des extensions de fichiers autorisées](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist). 

##  <a name="see-also"></a>Voir également

- [À propos du mode IE](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Informations sur les sites configurables](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [Informations supplémentaires sur le mode entreprise](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Définition des associations de types de fichiers](https://docs.microsoft.com/windows/win32/shell/fa-file-types)
- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
