---
title: 'Enterprise Site List Manager dans Microsoft Edge '
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 02/02/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Activer et utiliser Enterprise Site List Manager dans Microsoft Edge '
ms.openlocfilehash: 9700c2b78bba514525c4d80d211ef744dd175d2f
ms.sourcegitcommit: ff67ccc93d07588a9128e9b1fe007d5393a9d6af
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "11312580"
---
# Enterprise Site List Manager dans Microsoft Edge

Cet article explique comment activer l’accès à Enterprise Site List Manager dans Microsoft Edge et l’utiliser pour créer, modifier et exporter votre liste des sites en mode Entreprise pour le mode Internet Explorer.

> [!NOTE]
> Cet article s’applique à Microsoft Edge version 89 ou ultérieure. 

## Vue d’ensemble

Enterprise Site List Manager est une version dans le navigateur de [l’outil autonome Enterprise Mode Site List Manager](https://www.microsoft.com/download/details.aspx?id=49974) qui vous permet de créer, modifier et exporter la liste des sites de votre organisation.

De futures améliorations de l’outil pour le mode Internet Explorer seront disponibles via Enterprise Site List Manager dans Microsoft Edge. L’outil autonome reste disponible dans le Centre de téléchargement, mais ne reçoit aucune mise à jour des fonctionnalités.

## Activation de l’accès à Enterprise Site List Manager

Vous pouvez configurer l’accès à l’outil à l’aide de la stratégie de groupe [EnterpriseModeSiteListManagerAllowed.](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed)

S’il est activé, vos utilisateurs voient une option nommée Enterprise Site List Manager dans le volet de navigation gauche dans *edge://compat*. Si elle est désactivée, les utilisateurs ne verront pas le point d'entrée du gestionnaire de liste de sites d'entreprise dans le volet de navigation de gauche. Il s’agit du comportement par défaut.

## Utilisation de l’outil Enterprise Site List Manager

L’outil Enterprise Site List Manager utilise la version v.2 du schéma. Si vous importez un schéma de version v.1 dans Enterprise Site List Manager (schéma v.2), le XML est enregistré dans la version v.2 du schéma. Voir [Guide du schéma du mode entreprise v.2](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

### Ajouter des sites uniques à votre liste de sites  

Utilisez les étapes suivantes pour ajouter des sites individuels à votre liste des sites.

> [!NOTE]
> Vous pouvez uniquement ajouter des URL spécifiques, et non des zones Internet ou Intranet.

1. Dans Enterprise Site List Manager, cliquez sur  **Ajouter un site**.
2. Tapez l’URL du site web que vous souhaitez ajouter, par exemple :  <domain>.com ou <domain>.com/<path>  dans la zone URL.
3. Sélectionnez l’une des options suivantes dans la liste **Ouvrir dans**  :

   - **IE11**. Ouvre le site dans l’application IE11.
   - **Mode IE**. Ouvre le site en mode Internet Explorer sur Microsoft Edge s’il est activé et dans l’application Internet Explorer 11 dans le cas contraire. Consultez le  [mode Internet Explorer sur Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode).
   - **MSEdge**. Ouvre le site dans Microsoft Edge.
   - **Configurable**. Permet au site de participer à la détermination du moteur du mode IE. Voir [sites configurables en mode IE](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
   - **Aucun**. S’ouvre dans n’importe quel navigateur choisi par l’utilisateur.  

4. Sous  **Mode de compatibilité**, choisissez l’une des options suivantes :

   - **IE8Enterprise**. Charge le site en mode Entreprise IE8.
   - **IE7Enterprise**. Charge le site en mode Entreprise IE7.
   - **IE[x]**. Où [x] est le numéro du mode document et le site se charge dans le mode de document spécifié.
   - **Mode par défaut**. Charge le site à l’aide du mode de compatibilité par défaut pour la page.

   Le chemin d’accès au sein d’un domaine peut nécessiter un mode de compatibilité différent de celui du domaine lui-même. Par exemple, le domaine peut apparaître correctement dans le navigateur IE11 par défaut, mais le chemin d’accès peut rencontrer des problèmes et nécessiter l’utilisation du mode Entreprise. Si vous avez précédemment ajouté le domaine, votre choix de compatibilité d’origine est toujours sélectionné. Toutefois, si le domaine est nouveau, le  **mode Entreprise iE8**  est automatiquement sélectionné.

   Le mode Entreprise est prioritaire sur les modes document, afin que les sites qui figurent déjà dans la liste des sites en mode Entreprise ne soient pas affectés par cette mise à jour et continuent à se charger dans ce mode, comme d’habitude. Pour plus d’informations sur l’utilisation des modes document, voir Résoudre les problèmes de compatibilité web à l’aide des modes document et de la liste des sites en  [mode Entreprise](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/fix-compat-issues-with-doc-modes-and-enterprise-mode-site-list).

5. La case à cocher **Autoriser la redirection** s’applique au traitement des redirections côté serveur. Si vous cochez cette case, les redirections côté serveur s’ouvrent dans le navigateur spécifié par la balise d’ouverture. Pour plus d’informations, voir [ici](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-attributes).
6. Tapez des commentaires sur le site web dans la zone  **Commentaires**. Les administrateurs peuvent uniquement voir les commentaires lorsqu’ils sont dans cet outil et ces commentaires sont conservés dans le xml de liste des sites.
7. Cliquez sur  **Ajouter** pour ajouter le site à votre liste des sites.

### Exporter la liste des sites au XML

Après avoir créé votre liste des sites dans Enterprise Site List Manager, vous pouvez exporter le contenu vers un mode Entreprise (.EMIE) ou un fichier XML. 

> [!NOTE]
> Ce fichier inclut toutes vos URL, y compris vos sélections en matière de mode de compatibilité ; il doit être stocké dans un endroit sûr.

Pour exporter la liste des sites, suivez les étapes suivantes :

1. Dans Enterprise Site List Manager, cliquez sur **Exporter au XML**.
2. Entrez un **numéro de version** et un nom de **fichier**.
3. Cliquez sur **Exporter**.

Vous pouvez enregistrer le fichier en local ou sur un partage réseau. Toutefois, vous devez vérifier qu’il est déployé à l’emplacement indiqué dans votre clé de Registre. Pour plus d’informations, voir  [Activer le mode Internet Explorer et utiliser une liste des sites](https://docs.microsoft.com/deployedge/edge-ie-mode-policies).

### Importer plusieurs sites dans votre liste des sites

Après avoir créé votre fichier .xml, vous pouvez ajouter en bloc des sites à l’éditeur à l’aide de **Importer à partir de XML**.

Si vous souhaitez remplacer tout le contenu de l’éditeur, cliquez sur les ellipses (...) et choisissez **Effacer la liste**. Après avoir effacer l’éditeur, utilisez les étapes suivantes pour importer le site.

1. Dans Enterprise Site List Manager, cliquez sur **Importer à partir du XML**. 
2. Cliquez sur **Choisir un fichier** pour sélectionner votre liste des sites afin d’ajouter les sites inclus à l’outil. Sélectionnez la liste des sites à ajouter, puis cliquez sur  **Ouvrir**. Les formats pris en charge pour l’importation sont .xml, .emie ou .txt contenant le schéma v.2 de la liste des sites en mode Entreprise. Voir [Conseils sur le schéma du mode Entreprise v.2](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).
3. Cliquez sur  **Charger**  pour ajouter les sites à partir du fichier tp de l’éditeur.

Vous pouvez enregistrer le fichier en local ou sur un partage réseau. Toutefois, vous devez vérifier qu’il est déployé à l’emplacement indiqué dans votre clé de Registre. Pour plus d’informations, voir  [Activer le mode Internet Explorer et utiliser une liste des sites](https://docs.microsoft.com/deployedge/edge-ie-mode-policies).

### Modifier des sites dans votre liste des sites

 Vous pouvez modifier les attributs des entrées de site existantes dans Enterprise Site List Manager. Vous pouvez également ajouter, retirer ou supprimer des commentaires associés.

1. Dans Enterprise Site List Manager, cliquez sur les ellipses (...) et choisissez **Modifier le site** pour l’URL que vous souhaitez modifier.
2. Vous pouvez modifier n’importe quel attribut de l’entrée de site à l’exception de l’URL. Cliquez sur **Enregistrer** après avoir terminé la modification.

   > [!NOTE]
   > Si vous souhaitez supprimer une entrée de site, choisissez **Supprimer le site** à l’étape 1.

3. Cliquez sur **Exporter au XML**, puis enregistrez le fichier mis à jour.

Vous pouvez enregistrer le fichier en local ou sur un partage réseau. Toutefois, vous devez vérifier qu’il est déployé à l’emplacement indiqué dans votre clé de Registre. Pour plus d’informations, voir  [Activer le mode Internet Explorer et utiliser une liste des sites](https://docs.microsoft.com/deployedge/edge-ie-mode-policies).

### Afficher un aperçu de votre liste des sites au format XML

Vous pouvez afficher un aperçu des sites dans l’éditeur au format XML avant d’exporter et d’enregistrer dans votre emplacement de liste des sites. Cliquez sur **Aperçu XML** pour ouvrir le fichier dans un nouvel onglet.

### Recherche dans Enterprise Site List Manager

Vous pouvez rechercher si un site spécifique apparaît déjà dans votre liste des sites afin de ne pas essayer de l’ajouter à nouveau.

Pour effectuer une recherche, tapez une partie de l’URL dans la zone de recherche  **Filtrer les sites par URL** dans le coin supérieur droit de l’éditeur.

## Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [À propos du mode Internet Explorer](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Guide du schéma du mode entreprise v.2](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)
- [Informations supplémentaires sur le mode entreprise](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
