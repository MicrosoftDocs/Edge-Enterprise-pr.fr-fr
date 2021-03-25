---
title: Automatiser MicrosoftEdge pour le déploiement sur macOS avec Jamf
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 11/30/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Procédure d’automatisation de MicrosoftEdge pour le déploiement sur macOS avec Jamf.
ms.openlocfilehash: f02b9efde872082cf2301a4cf66b0a3f3782e39b
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447488"
---
# <a name="deploy-to-macos-with-jamf"></a>Déployer sur macOS avec Jamf

Cet article décrit comment déployer MicrosoftEdge pour macOS à l’aide de Jamf.

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

## <a name="prerequisites"></a>Prérequis

Avant de déployer Microsot Edge, assurez-vous que les conditions préalables suivantes sont réunies:

- Le fichier d’installation de MicrosoftEdge, **MicrosoftEdgeDev-\\<version\>.pkg**, se trouve dans un emplacement accessible sur votre réseau. Vous pouvez téléchargez les fichiers d’installation de Microsoft Edge Entreprise sur la [page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise).
- Vous disposez d’un compte Cloud Jamf avec le niveau d’accès et de privilèges nécessaires pour créer et déployer des fichiers d’installation sur des ordinateurs.

## <a name="to-deploy-microsoft-edge-using-jamf"></a>Pour déployer MicrosoftEdge à l’aide de Jamf:

1. Connectez-vous à Jamf et accédez à **Tous les paramètres**.

    ![Ouvrez Tous les paramètres](./media/mac-deploy/jamf-dash-main-open-settings.png)

2. Sous **Tous les paramètres**, cliquez sur **Gestion de l’ordinateur**.

    ![Sélectionnez Gestion de l’ordinateur](./media/mac-deploy/jamf-all-settings-computer-mgmt.png)

3. Sous **Gestion de l’ordinateur**, cliquez sur **Packages**.

    ![Sélectionnez Packages](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkgs.png)

4. Sur la page **Packages**, cliquez sur **+ Nouveau** pour ajouter un nouveau package.

    ![Sélectionnez Nouveau pour ajouter un nouveau package](./media/mac-deploy/jamf-all-settings-computer-mgmt-new-pkg.png)

5. Sur la page **Nouveau package**, entrez les détails du package, puis cliquez sur **Enregistrer**. (Par exemple, NOM D’AFFICHAGE, INFO ou NOTES.)

    ![Sélectionnez Enregistrer pour enregistrer les informations relatives au package](./media/mac-deploy/jamf-all-settings-computer-mgmt-save-pkg-info.png)

6. Sélectionnez **Ordinateurs** dans la barre de menus, puis **Stratégies** dans la barre de navigation.

7. Sélectionnez **+ Nouveau** pour afficher le volet **Nouvelle stratégie**.

    ![Sélectionnez Nouveau pour créer une nouvelle stratégie](./media/mac-deploy/jamf-all-settings-computer-new-policy.png)

8. Sous l’onglet **Options**, sélectionnez **Général**.

    - Sous **NOM D’AFFICHAGE**, entrez le nom d’affichage de la stratégie.
    - Sous **Déclencheur**, sélectionnez l’événement qui déclenchera la stratégie. Dans l’exemple suivant, l’événement est Démarrage.

    ![Entrez les informations relatives au déploiement](./media/mac-deploy/jamf-all-settings-computer-cfg-policy.png)

9. Sous l’onglet **Options**, cliquez sur **Packages**.

10. Dans la fenêtre contextuelle **Configurer des packages**, cliquez sur **Configurer**.

    ![Configurer un package d’application](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-configure.png)

11. Le package que vous avez ajouté apparaît dans le volet **Packages**. Cliquez sur **Ajouter**. Pour cet exemple, le package est «MicrosoftEdgeBeta» dans la capture d’écran suivant.

    ![Ajouter un package](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-add-beta.png)

12. Sur la page **Nouvelle stratégie**, utilisez les listes déroulantes pour sélectionner le **POINT DE DISTRIBUTION** et l’**ACTION** à effectuer pout la stratégie. Cliquez sur **Enregistrer**. La capture d’écran suivante utilise par exemple «Le point de distribution par défaut de chaque ordinateur» et «Installer».

    ![Sélectionner un point de distribution de une action](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkg-cfg-distro.png)

13. Sur la page **Nouvelle stratégie**, sélectionnez l’onglet **Étendue**. Vous pouvez gérer l’étendue du déploiement en fonction des ordinateurs ou des utilisateurs. Pour cet exemple, sélectionnez **Tous les ordinateurs **dans la liste déroulante **ORDINATEURS CIBLES**, puis cliquez sur **Enregistrer**.

    ![Sélectionnez l’étendue du déploiement](./media/mac-deploy/jamf-all-settings-computer-mgmt-add-target.png)

14. À ce stade, vous pouvez passer en revue la stratégie de déploiement de MicrosoftEdge. Si les options de déploiement répondent à vos besoins cliquez sur **Terminé**.

    ![Cliquez sur Terminé.](./media/mac-deploy/jamf-all-settings-computer-mgmt-finish-add-deployment.png)

    > [!NOTE]
    > Vous pouvez revenir à une stratégie de déploiement à tout moment pour modifier les paramètres.

Félicitations! Vous venez de terminer la configuration de Jamf pour déployer MicrosoftEdge pour macOS. Lorsque la condition de déclencheur que vous avez définie sera true, le package sera déployé sur les ordinateurs que vous avez désignés.

## <a name="see-also"></a>Articles associés

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Jamf.com](https://www.jamf.com/)
- [Intégrer Jamf à Microsoft Intune](/intune/conditional-access-integrate-jamf)