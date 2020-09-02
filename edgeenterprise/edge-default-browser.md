---
title: Définir MicrosoftEdge comme navigateur par défaut sur Windows et macOS
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 1/15/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez comment définir MicrosoftEdge comme navigateur par défaut
ms.openlocfilehash: c8cc45e0fe42dcbbd828dd81ae568f141cda2985
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979712"
---
# Définir MicrosoftEdge comme navigateur par défaut

Cet article explique comment vous pouvez définir MicrosoftEdge comme navigateur par défaut sur Windows et macOS.

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure sur Windows8 et Windows10. Pour Windows7 et macOS, consultez la stratégie [Définir MicrosoftEdge comme navigateur par défaut](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled).

## Introduction

Vous pouvez utiliser la stratégie de groupe **Définir un fichier de configuration des associations par défaut** ou le paramètre de Gestion des appareils mobiles [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) pour définir MicrosoftEdge comme navigateur par défaut pour votre organisation.

Pour définir MicrosoftEdge Stable comme navigateur par défaut pour les fichiers html et les liens http/https et les fichiers PDF, utilisez l’exemple de fichier d’association d’application suivant:

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
> Pour définir MicrosoftEdge Beta en tant que navigateur par défaut, définissez **ApplicationName** sur «MicrosoftEdge Dev» et **ProgId** sur «MSEdgeBHTML». Pour définir MicrosoftEdge Dev en tant que navigateur par défaut, définissez **ApplicationName** sur «MicrosoftEdge Dev» et **ProgId** sur «MSEdgeDHTML».


> [!NOTE]
> Les associations de fichiers par défaut ne sont pas appliquées si MicrosoftEdge n’est pas installé sur le périphérique cible. Dans ce scénario, les utilisateurs sont invités à sélectionner leur application par défaut lorsqu’ils ouvrent un lien ou un fichier htm/html.

## Définir MicrosoftEdge comme navigateur par défaut

Vous pouvez définir Microsoft Edge comme navigateur par défaut sur les périphériques joints par domaine en configurant la stratégie de groupe **Définir un fichier de configuration des associations par défaut**. Si vous activez ce paramètre, vous devez également créer et stocker un fichier de configuration des associations par défaut, en local ou sur un partage réseau. Ce fichier est stocké localement ou sur un partage réseau. Pour en savoir plus sur la création de ce fichier, consultez [Exporter ou importer des associations d’applications par défaut](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).

### Pour configurer la stratégie de groupe pour un type de fichier par défaut et un fichier de configuration d’associations de protocoles:

1. Ouvrez l’éditeur de stratégie de groupe et accédez à **Configuration de l’ordinateur\Modèles d’administration\Composants Windows\Explorateur de fichiers**.
2. Sélectionnez **Définir un fichier de configuration des associations par défaut**.
3. Cliquez sur **Paramètre de stratégie**, puis sur **Activé**.
4. Cliquez sur **Activé** puis, dans la zone Options, saisissez l’emplacement dans votre fichier de configuration des associations par défaut.
5. Cliquez sur **OK** pour enregistrer le paramètre.

L’exemple de la capture d’écran suivante montre un fichier d’associations nommé *appassoc.xml* sur un partage réseau qui est accessible à partir du périphérique cible.

   ![Activer l’association de fichiers dans la stratégie de groupe](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > Si ce paramètre est activé et que le périphérique de l’utilisateur est joint au domaine, le fichier de configuration des associations est traité la fois suivante où l’utilisateur se connecte.

## Définir MicrosoftEdge comme navigateur par défaut sur les périphériques Azure Active Directory joints

Pour définir MicrosoftEdge comme navigateur par défaut sur les périphériques Azure ActiveDirectory joints, suivez la procédure présentée dans le paramètre [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) de Gestion des appareils mobiles en utilisant l’exemple de fichier d’association d’application suivant.

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
> Pour définir MicrosoftEdge Beta en tant que navigateur par défaut, définissez **ApplicationName** sur «MicrosoftEdge Dev» et **ProgId** sur «MSEdgeBHTML». Pour définir MicrosoftEdge Dev en tant que navigateur par défaut, définissez **ApplicationName** sur «MicrosoftEdge Dev» et **ProgId** sur «MSEdgeDHTML».

## Définir MicrosoftEdge comme navigateur par défaut sur macOS

Si vous tentez de définir par programmation le navigateur par défaut sur macOS, une invite s’affiche pour l’utilisateur final. Cette invite est une fonctionnalité de sécurité macOS qui ne peut être automatisée qu’à l’aide d’un AppleScript.

En raison de cette limitation, il existe deux méthodes principales pour définir MicrosoftEdge comme navigateur par défaut sur un macOS. La première option consiste à flasher l’appareil avec une image de macOS où MicrosoftEdge a déjà été défini comme navigateur par défaut. L’autre option consiste à utiliser la stratégie  [Définir MicrosoftEdge comme navigateur par défaut](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled) , qui invite l’utilisateur à définir MicrosoftEdge comme navigateur par défaut.

Lorsque vous utilisez l’une de ces méthodes, il est toujours possible pour un utilisateur de modifier le navigateur par défaut. Cela est dû au fait que, pour des raisons de sécurité, la préférence de navigateur par défaut ne peut pas être bloquée par programmation. Pour cette raison, nous vous recommandons de déployer la stratégie **Définir MicrosoftEdge comme navigateur par défaut** , même si vous créez une image avec MicrosoftEdge comme navigateur par défaut. Si la stratégie est définie et qu’un utilisateur change le navigateur par défaut la prochaine fois qu’il ouvrira MicrosoftEdge, il sera invité à le définir comme valeur par défaut.

## Articles associés

- [Planifier votre déploiement de MicrosoftEdge](https://docs.microsoft.com/DeployEdge/deploy-edge-plan-deployment)
- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Définir MicrosoftEdge comme navigateur par défaut (Windows7 et macOS)](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled)
- [Windows10: comment configurer des associations de fichiers pour les professionnels de l’informatique?](https://docs.microsoft.com/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [Pour en savoir plus sur la création de ce fichier, voir Exporter ou importer des associations d’applications par défaut.](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [Vue d’ensemble du module de plateforme sécurisée (DISM)](https://docs.microsoft.com/windows-hardware/manufacture/desktop/what-is-dism)
  - [DISM (Deployment Image Servicing and Management) - Gestion et maintenance des images de déploiement](https://docs.microsoft.com/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)
