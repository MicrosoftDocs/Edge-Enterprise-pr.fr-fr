---
title: Mises à jour Windows pour MicrosoftEdge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Mises à jour Windows pour MicrosoftEdge.
ms.openlocfilehash: ab5832dc878495a0f0a0880676fb7c3e34b69d4d
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979790"
---
# Mises à jour Windows pour prendre en charge la prochaine version de MicrosoftEdge

Cet article décrit comment Windows sera mis à jour pour prendre en charge la prochaine version de MicrosoftEdge.

> [!NOTE]
> Cet article concerne le canal MicrosoftEdge Stable.

## MicrosoftEdge et le cycle de publication Windows

La prochaine version de MicrosoftEdge offre des fonctionnalités des mise à jour plus fréquentes et flexibles. Les versions de navigateur n’étant pas liées aux versions majeures de Windows, des modifications seront apportées au système d’exploitation pour garantir que la prochaine version de MicrosoftEdge s’adapte de façon transparente à Windows. Par conséquent, les mises à jour des fonctionnalités seront publiées sur un cycle de 6semaines (approximativement). Les mises à jour de sécurité et de compatibilité seront fournies en fonction des besoins.

## Mises à jour et expérience utilisateur

Les mises à jour ne modifieront pas l’expérience utilisateur tant que le canal Stable de la version suivante de MicrosoftEdge ne sera pas installé. L’installation de MicrosoftEdge Beta, Dev ou Canary ne déclenche pas de modifications dans Windows. Ces versions du navigateur seront installées à côté des navigateurs existants.

Lorsque toutes les mises à jour sont appliquées ET que le canal Stable de la version suivante de MicrosoftEdge est installé au niveau du système, les modifications suivantes prennent effet sur le système:

- Tous les codes confidentiels du menu démarrer, les vignettes et les raccourcis de la version actuelle de MicrosoftEdge sont migrés vers la version suivante de MicrosoftEdge.
- Tous les codes confidentiels et raccourcis de la barre des tâches pour la version actuelle de MicrosoftEdge sont migrés vers la version suivante de MicrosoftEdge.
- La prochaine version de MicrosoftEdge sera épinglée à la barre des tâches. Si la version actuelle de MicrosoftEdge est déjà épinglée, elle sera remplacée.
- La prochaine version de MicrosoftEdge ajoutera un raccourci sur le Bureau. Si la version actuelle de MicrosoftEdge possède déjà un raccourci, celui-ci sera remplacé.
- La plupart des protocoles que MicrosoftEdge gère par défaut seront migrés vers la version suivante de MicrosoftEdge.
- La version actuelle de MicrosoftEdge sera masquée sur toutes les surfaces d’expérience utilisateur du système d’exploitation, y compris les paramètres, toutes les applications et les boîtes de dialogue de prise en charge de fichiers ou de protocoles.
- Toutes les tentatives de lancement de la version actuelle de MicrosoftEdge seront redirigées vers la version suivante de MicrosoftEdge.

  > [!NOTE]
  > Les installations de niveau utilisateur ne déclencheront pas ces comportements.

Avec les modifications précédentes, des modifications seront apportées, que le canal Stable de la version suivante de MicrosoftEdge soit installé ou non.

- MicrosoftEdge annulera l’inscription aux livres et protocoles XML que la version suivante de MicrosoftEdge ne prend pas en charge. Les utilisateurs qui essaient d’ouvrir ces protocoles verront s’afficher une boîte de dialogue les invitant à choisir une application par défaut. Pour en savoir plus sur les modifications de la prise en charge des livres, consultez [Téléchargez une application ePub pour continuer à lire des livres électroniques](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsupport.microsoft.com%2Fhelp%2F4517840&data=02%7C01%7Cv-danwes%40microsoft.com%7Cc9f8571b880549c30fcf08d72be5eaf9%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637026138803983526&sdata=qtb3DvVZQ6H%2FFXnBievkl%2B%2BngAQXwl340PcH8kRc3y4%3D&reserved=0).

## Chronologie

Les modifications nécessaires à la prise en charge de l’expérience décrite seront fournies avec trois mises à jour pour différentes versions de Windows.

### Windows versions 1903 et 1909

- Premier ensemble de modifications dans la mise à jour facultative de juillet2019, compris dans la mise à jour de sécurité d’août2019.
- Deuxième ensemble de modifications dans la mise à jour facultative d’août2019, compris dans la mise à jour de sécurité de septembre2019.

  > [!NOTE]
  > Il s’agit de la mise à jour dans laquelle MicrosoftEdge annule l’inscription du protocole XML.

- Troisième ensemble de modifications dans la mise à jour facultative de septembre2019, compris dans la mise à jour de sécurité d’octobre2019.

  > [!NOTE]
  > Il s’agit de la mise à jour dans laquelle MicrosoftEdge ne prend plus en charge les e-books.

### Windows versions1709, 1803 et 1809

- Premier ensemble de modifications dans une mise à jour facultative d’août2019, compris dans la mise à jour de sécurité de septembre2019.
- Deuxième ensemble de modifications dans une mise à jour facultative de septembre2019, compris dans la mise à jour de sécurité d’octobre2019.

  > [!NOTE]
  > Il s’agit de la mise à jour dans laquelle MicrosoftEdge annule l’inscription du protocole XML.

- Troisième ensemble de modifications dans une mise à jour facultative d’octobre2019, compris dans la mise à jour de sécurité de novembre2019.

  > [!NOTE]
  > Il s’agit de la mise à jour dans laquelle MicrosoftEdge ne prend plus en charge les e-books.

Le tableau suivant fournit des détails sur les mises à jour spécifiques de chaque ensemble de modifications.

| Windows10 | Plus d’informations | Téléchargement requis |
|--|--|--|
| Version1709 | [KB4525241](https://support.microsoft.com/help/4525241/windows-10-update-kb4525241) | [Mise à jour de sécurité cumulative pour Windows 10, version1709](https://www.catalog.update.microsoft.com/Search.aspx?q=4525241) |
| Version1803  | [KB4525237](https://support.microsoft.com/help/4525237/windows-10-update-kb4525237) | [Mise à jour de sécurité cumulative pour Windows 10, version1803](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4525237) |
| Version 1809  | [KB4523205](https://support.microsoft.com/help/4523205/windows-10-update-kb4523205) | [Mise à jour de sécurité cumulative pour Windows 10, version1809](https://www.catalog.update.microsoft.com/Search.aspx?q=4523205) |
| Version 1903 et 1909 |[KB4517389](https://support.microsoft.com/help/4517389/windows-10-update-kb4517389)  | [Mise à jour de sécurité cumulative pour Windows 10, version1903 et 1909](https://www.catalog.update.microsoft.com/Search.aspx?q=4517389) |

## Articles associés

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Documentation MicrosoftEdge](https://docs.microsoft.com/DeployEdge/)
