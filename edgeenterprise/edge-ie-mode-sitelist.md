---
title: Configurer des Sites dans la Liste des Sites en Mode Entreprise
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 05/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer la Liste des Sites d’Entreprise
ms.openlocfilehash: 969a4f6001dbe08a51c26ecf35812b101d315a59
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979809"
---
# Configurer des Sites dans la Liste des Sites en Mode Entreprise

Cet article décrit les modifications apportées à la Liste des Sites en Mode Entreprise qui prennent en charge la configuration du mode IE pour Microsoft Edge version 77 et ultérieures.

Pour plus d’informations sur le schéma du fichier XML de Liste des Sites en Mode Entreprise, voir [Guide de schéma Mode Enterprise v.2](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

> [!NOTE]
> Cet article concerne les canaux MicrosoftEdge **stable**, **Beta** et **Dev**, version77 ou ultérieures.

## Éléments de schéma mis à jour

Le tableau suivant décrit l’élément \<open-in app\> ajouté au schéma de mode entreprisev.2:

| **Élément** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | Un élément enfant qui contrôle quel navigateur est utilisé pour les sites. Cet élément est requis pour les sites qui doivent s’**ouvrir dans Internet Explorer11**.|

**Exemple:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

Le tableau suivant présente les valeurs possibles de l’élément \<open-in\>:

| **Valeur** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Ouvre le site en mode IE ou une fenêtre IE11 complète. Pour activer le mode IE, voir [Configurer les stratégies de mode IE](https://docs.microsoft.com/deployedge/edge-ie-mode-policies)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Ouvre le site dans une fenêtre IE11 complète |
| **\<open-in\>MSEdge\</open-in\>** | Ouvre le site dans Microsoft Edge |
| **\<open-in\>Aucun ou non spécifié\</open-in\>** | Ouvre le site dans le navigateur par défaut ou dans le navigateur où la navigation a été initialisée par l’utilisateur. |
|**\<open-in\>Configurable\</open-in\>** | Permet au site de participer à la détermination du moteur du mode IE. Pour plus d’informations, consultez[En savoir plus sur les sites configurables en mode Internet Explorer](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> L’attribut app=**"true"** est reconnu uniquement lorsqu’il est associé à _’open-in’ IE11_. Le fait de l’ajouter aux autres éléments «open-in» ne modifie pas le comportement du navigateur.   

## Configuration de sites neutres

Afin que le mode IE fonctionne correctement, l’authentification/les Serveurs à connexion unique doivent être expressément configurés en tant que sites neutres. Dans le cas contraire, les pages du mode IE tenteront d’effectuer une redirection vers Microsoft Edge, et l’authentification échouera.

Un site neutre utilise le navigateur dans lequel la navigation a commencé, soit Microsoft Edge, soit le mode IE. La configuration de sites neutres garantit que toutes les applications utilisant ces serveurs d’authentification, modernes et héritées, continuent de fonctionner.

Vous pouvez configurer des sites neutres en paramétrant le menu déroulant *Ouvrir dans* sur «Note»dans l’outil Gestionnaire de liste de sites en mode entreprise ou en mettant directement à jour le fichier XML de liste de sites:

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

Pour identifier les serveurs d’authentification, examinez le trafic réseau d’une application à l’aide des outils de développement IE11. Si vous avez besoin de davantage de temps pour identifier vos serveurs d’authentification, vous pouvez configurer une stratégie pour conserver toute la navigation dans la page en mode IE. Pour réduire l’utilisation du mode IE, désactivez ce paramètre une fois que vous avez identifié et ajouté vos serveurs d’authentification à la liste des sites. Pour plus d’informations, voir [Configurer la navigation dans des pages pour qu'elles restent en mode IE](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationsiteredirect).

>[!NOTE]
   >Le schéma du mode entreprisev.1 n’est pas pris en charge pour l’intégration du mode IE. Si vous utilisez actuellement le schémav.1 avec Internet Explorer11, vous devez effectuer la mise à niveau vers le schémav.2. Pour plus d’informations, consultez [Recommandations sur le schéma du mode Entreprisev.2](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [À propos du mode IE](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Informations supplémentaires sur le mode entreprise](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)