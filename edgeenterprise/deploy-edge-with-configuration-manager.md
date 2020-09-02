---
title: Déployer Microsoft Edge à l’aide de SystemCenter ConfigurationManager
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 09/30/2019
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez comment déployer Microsoft Edge avec SystemCenter ConfigurationManager (SCCM).
ms.openlocfilehash: be14f2db3b28b7585bfad1706b9f82209235df0a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979727"
---
# Déployer Microsoft Edge à l’aide de SystemCenter ConfigurationManager

Cet article explique comment automatiser un déploiement de MicrosoftEdge à l’aide de SystemCenter ConfigurationManager (SCCM).

>[!NOTE]
>Cet article concerne MicrosoftEdge version77 ou ultérieure.

## Avant de commencer

Consultez les informations dans [Présentation de la gestion d’applications dans Configuration Manager](https://docs.microsoft.com/sccm/apps/understand/introduction-to-application-management). Cet article relatif à la gestion des applications vous aidera à mieux appréhender la terminologie utilisée dans cet article. Il vous aidera également à préparer votre site à l’installation d’applications.

Téléchargez les fichiers d’installation de MicrosoftEdge (**MicrosoftEdgeDevEnterpriseX64.msi** et/ou **MicrosoftEdgeDevEnterpriseX86.msi**) sur la [page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise).

Enregistrez les fichiers d’installation de MicrosoftEdge dans un emplacement réseau accessible.

## Créez la liste des langues de l’application.

Vous allez créer l’application à l’aide d’un Assistant Gestionnaire de configuration.

### Démarrer l’Assistant Création d’une application et créer l’application  

1. Dans la console Configuration Manager, cliquez sur **Bibliothèque de logiciels** > **Gestion des applications** > **Applications**.  

2. Dans l’onglet **Accueil**, dans le groupe **Créer**, cliquez sur **Créer une application**. Vous pouvez également cliquer avec le bouton droit sur **Applications** dans la barre de navigation, puis cliquer sur **Créer une application**.

    ![Créer votre première application](./media/edge-ent-deployment-sccm/edge-ent-create-app-1.png)

3. Dans la page **Général** de l’**Assistant Création d’une application**, cochez la case **Détecter automatiquement les informations de cette application à partir des fichiers d’installation**. Ces informations sont pré-renseignées dans l’Assistant avec les données extraites du fichier d’installation. msi. Indiquez les informations suivantes:  

   - **Type**: choisissez **Windows Installer (fichier \*.msi)**.  

   - **Emplacement**: tapez l’emplacement (ou cliquez sur **Parcourir** pour sélectionner l’emplacement) du fichier d’installation **MicrosoftEdgeDevEnterpriseX64.msi** ou **MicrosoftEdgeDevEnterpriseX86.msi**. Notez que l’emplacement doit être spécifié sous la forme *\\\Serveur\Partage\Fichier* pour que Configuration Manager localise les fichiers d’installation.  

   La page **Spécifier les paramètres de cette application** ressemblera à l’exemple suivant:  

    ![Spécifier les paramètres de cette application](./media/edge-ent-deployment-sccm/edge-ent-create-app-2.png)

4. Cliquez sur **Suivant**. Sous **Détails** sur la page **Informations importées**, vous verrez des informations concernant l’application et tous les fichiers associés qui ont été importés. Cliquez sur **Suivant** pour poursuivre l’Assistant.  

    ![Afficher les informations importées](./media/edge-ent-deployment-sccm/edge-ent-create-app-3.png)

5. Sur la page **Informations générales**, vous pouvez ajouter des informations supplémentaires sur l’application. Par exemple, version du logiciel, commentaires de l’administrateur et éditeur. Vous pouvez utiliser ces informations pour vous aider à trier et à rechercher l’application dans la console Configuration Manager.

   Vous pouvez également utiliser le champ **Programme d’installation** pour spécifier la ligne de commande complète qui sera utilisée pour installer l’application sur les PC. Vous pouvez la modifier pour ajouter vos propres propriétés (par exemple, **/q** pour une installation sans assistance).

   La capture d’écran suivante présente un exemple d’utilisation des champs **Spécifier des informations sur cette application**.

   ![Spécifier les métadonnées de l’application](./media/edge-ent-deployment-sccm/edge-ent-create-app-5.png)

6. Cliquez sur **Suivant**.
7. Sur la page **Résumé**, vous pouvez confirmer vos paramètres d’application sous **Détails**, puis terminer à l’aide de l’Assistant. Cliquez sur **Suivant**.  

    ![Détails des paramètres d’application](./media/edge-ent-deployment-sccm/edge-ent-create-app-6.png)

8. Sur la page **Fin**, cliquez sur **Fermer**.

    ![Boîte de dialogue Réussite](./media/edge-ent-deployment-sccm/edge-ent-create-app-7.png)

Vous avez terminé de créer l’application. Utilisez la procédure suivante pour la voir dans Configuration Manager:

- sélectionnez l’espace de travail **Bibliothèque de logiciels**
- développez **Gestion des applications**
- cliquez sur **Applications**.

La capture d’écran suivante illustre l’exemple utilisé pour cet article.  

![Applications](./media/edge-ent-deployment-sccm/edge-ent-create-app-8.png)

## Modifier les propriétés de l’application et les paramètres de déploiement

Après avoir créé une application, vous pouvez affiner les paramètres d’application, le cas échéant. Pour consulter les propriétés de l’application:

- sélectionnez l’application
- dans **Accueil**>**Propriétés**, cliquez sur **Propriétés**.  

   ![Configurer les propriétés de l’application](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-1.png)

 Dans la boîte de dialogue **Propriétés de l’application <nom de l’application\>**, vous verrez une vue avec onglets des éléments que vous pouvez configurer pour modifier le comportement de l’application. Pour plus d’informations sur les paramètres que vous pouvez configurer, consultez [Créer des applications](https://docs.microsoft.com/sccm/apps/deploy-use/create-applications).

Pour cet exemple, vous allez modifier certaines propriétés du type de déploiement de l’application. Pour modifier les propriétés de déploiement:

1. Cliquez sur l’onglet **Types de déploiement**.
2. Sous **Types de déploiement**:, sélectionnez le **Nom** de l’application
3. Cliquez sur **Modifier**.

   ![Modifier le type de déploiement](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-2.png)

### Ajouter une condition requise au type de déploiement

 Les conditions requises spécifient les critères à remplir pour qu’une application soit installée sur un périphérique. Vous pouvez choisir parmi les conditions requises intégrées ou vous pouvez créer votre propre configuration. Par exemple, vous pouvez ajouter une condition stipulant que l’application sera installée uniquement sur les PC exécutant Windows10 **x86** ou **x64**, en fonction de l’architecture du processeur cible du fichier d’installation. Dans cet exemple, vous allez spécifier Windows10 **x86**.

1. Dans la page Propriétés du type de déploiement que vous venez d’ouvrir, cliquez sur l’onglet **Conditions requises**.

2. Cliquez sur **Ajouter** pour ouvrir la boîte de dialogue **Créer une spécification**.

    ![Créer une spécification](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-3.png)

3. Dans la boîte de dialogue **Créer une spécification**, spécifiez les informations suivantes:

    - **Catégorie**: **Périphérique**  

    - **Condition**: **Système d’exploitation**  

    - **Type de règle**: **Valeur**  

    - **Opérateur**: **Un de**  

    - Dans la liste systèmes d’exploitation, sélectionnez **Windows10** > **Tous les Windows10 (32bits)**.  

    Lorsque vous avez terminé, la boîte de dialogue ressemble à la capture d’écran suivante:

    ![Ajouter une condition requise](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-4.png)

4. Cliquez sur **OK** pour fermer chaque page de propriétés ouverte et revenir à la liste **Applications** dans la console Configuration Manager.  

## Ajouter le contenu de l’application à un point de distribution  

Pour déployer l’application mise à jour sur des PC, assurez-vous que le contenu de l’application est copié sur un point de distribution. Les PC accèdent au point de distribution pour installer l’application.  

>[!TIP]
>Pour en savoir plus sur les points de distribution et la gestion de contenu dans Configuration Manager, consultez [Déployer et gérer le contenu pour SystemCenter ConfigurationManager](https://docs.microsoft.com/sccm/core/servers/deploy/configure/deploy-and-manage-content).  

1. Dans la console Configuration Manager, cliquez sur **Bibliothèque de logiciels**.  

2. Dans l’espace de travail **Bibliothèque de logiciels**, développez **Applications**. Sélectionnez l’application que vous avez créée dans la liste des applications.

3. Sous l’onglet **Accueil** du groupe **Déploiement**, cliquez sur **Distribuer du contenu**.  

4. Sur la page **Général** de l’**Assistant de distribution de contenu**, vérifiez que le nom de l’application est correct, puis cliquez sur **Suivant**.  

5. Sur la page **Contenu**, vérifiez les informations qui seront copiées dans le point de distribution, puis cliquez sur **Suivant**.  

6. Sur la page **Destination du contenu**, cliquez sur **Ajouter** pour sélectionner un ou plusieurs regroupements, points de distribution ou groupes de points de destination où vous souhaitez installer le contenu de l’application.

7. Terminez l’Assistant.

Vous pouvez vérifier que le contenu de l’application a été copié correctement dans le point de distribution à partir de l’espace de travail **Surveillance**, sous **État de la distribution** > **État du contenu**.  

## Déployer l’application  

Ensuite, déployez l’application sur un regroupement de périphériques dans votre hiérarchie. Dans cet exemple, vous déployez l’application sur le regroupement de périphériques **Tous les systèmes**.  

>[!TIP]
>N’oubliez pas que seuls les ordinateurs Windows10 de l’architecture de processeur spécifiée installent l’application, en raison des conditions requises que vous avez sélectionnées précédemment.  

1. Dans la console Configuration Manager, cliquez sur **Bibliothèque de logiciels** > **Gestion des applications** > **Applications**.

2. Dans la liste des applications, sélectionnez l’application que vous avez créée. Puis, sous l’onglet **Accueil** du groupe **Déploiement**, cliquez sur **Déployer** ou cliquez avec le bouton droit sur l’application et sélectionnez **Déployer**.

    ![Déployer l’application](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-1.png)

3. Sur la page **Général** de l’**Assistant de déploiement de logiciel**, cliquez sur **Parcourir** pour sélectionner le regroupement de périphériques sur lequel vous souhaitez déployer l’application.

    ![Accéder au fichier d’installation](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-2.png)

4. Sur la page **Contenu**, vérifiez que le point de distribution à partir duquel vous souhaitez que les PC installent l’application est sélectionné.

    ![Spécifier un point de distribution](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-6.png)

5. Sur la page **Paramètres de déploiement**, vérifiez que l’action de déploiement est définie sur **Installer** et que l’objet du déploiement est défini sur **Obligatoire**.

    ![Configurer les paramètres de déploiement](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-8.png)

    >[!TIP]
    >En définissant l’objet du déploiement sur **Obligatoire**, vous vous assurez que l’application est installée sur les PC qui répondent aux conditions que vous avez définies. Si vous définissez cette valeur sur **Disponible**, les utilisateurs peuvent installer l’application à la demande à partir du Centre logiciel.  

6. Sur la page **Planification**, vous pouvez configurer le moment où l’application sera installée. Pour cet exemple, sélectionnez **Dès que possible après le temps disponible**.

    ![Planifier le déploiement](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-9.png)

7. Sur la page **Expérience utilisateur**, sélectionnez les valeurs de votre choix et cliquez sur **Suivant**.

    ![Spécifier l’expérience utilisateur](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-10.png)

8. Définissez les options d’alerte de votre choix, puis cliquez sur **Suivant**.

    ![Spécifier des paramètres d’alerte](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-11.png)

9. Terminez l’Assistant.

Utilisez les informations de la section **Surveiller l’application** suivante pour afficher l’état du déploiement de votre application.  

## Surveiller l’application

 Dans cette section, vous allez consulter rapidement l’état du déploiement de l’application que vous venez de déployer.  

### Pour consulter l’état du déploiement  

1. Dans la console Configuration Manager, cliquez sur **Surveillance** > **Déploiements**.  

2. Dans la liste des déploiements, sélectionnez l’application.

    ![Surveiller le déploiement](./media/edge-ent-deployment-sccm/edge-ent-monitor-deployment.png)

3. Dans l’onglet **Accueil** du groupe **Déploiement**, cliquez sur **Afficher l’état**.  

4. Sélectionnez l’un des onglets suivants pour afficher plus de mises à jour d’état concernant le déploiement d’applications:  

    - **Réussite**: l’application a été installée correctement sur les PC indiqués.  

    - **En cours**: l’installation de l’application n’est pas encore terminée.  

    - **Erreur**: une erreur s’est produite lors de l’installation de l’application sur les PC indiqués. Des informations supplémentaires sur l’erreur s’affichent également.  

    - **Conditions non remplies**: aucune tentative d’installation n’a été effectuée sur les appareils indiqués, car ils ne répondent pas aux critères que vous avez configurés (dans cet exemple, parce qu’ils ne fonctionnent pas sur Windows10.)

    - **Inconnu**: ConfigurationManager n’a pas pu signaler l’état du déploiement. Vérifiez à nouveau ultérieurement.  

    >[!TIP]
    >Il existe plusieurs façons de surveiller le déploiements des applications. Pour plus d’informations, consultez [Surveiller les applications avec la console SystemCenterConfigurationManager](https://docs.microsoft.com/sccm/apps/deploy-use/monitor-applications-from-the-console).  

## Expérience pour l’utilisateur final  

Les utilisateurs qui disposent de PC gérés par ConfigurationManager et qui exécutent Windows10 de l’architecture de processeur spécifiée verront un message leur indiquant qu’ils doivent installer l’application MicrosoftEdge Dev. Lorsqu’ils acceptent cette option d’installation, l’application est installée.  

## Articles associés

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Pour plus d’informations sur le déploiement de packages MSI, voir Créer et déployer une application avec System Center Configuration Manager.](https://docs.microsoft.com/sccm/apps/get-started/create-and-deploy-an-application)
