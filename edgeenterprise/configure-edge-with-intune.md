---
title: Configurer les paramètres de stratégie MicrosoftEdge pour Windows avec MicrosoftIntune
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/18/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer les paramètres de stratégie MicrosoftEdge pour Windows avec MicrosoftIntune.
ms.openlocfilehash: 0189a3fc2f9dc115563e7cf6dca1df960680bf22
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447558"
---
# <a name="configure-microsoft-edge-policy-settings-with-microsoft-intune"></a>Configurer les paramètres de stratégie MicrosoftEdge avec MicrosoftIntune

Cet article explique comment configurer les paramètres de stratégie MicrosoftEdge pour Windows10 à l’aide de MicrosoftIntune.

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

Vous pouvez configurer les stratégies et paramètres MicrosoftEdge en ajoutant un profil de configuration de périphérique à MicrosoftIntune. L’utilisation de Intune pour gérer et appliquer des méthodes revient à utiliser la méthode de groupe ActiveDirectory ou à configurer les paramètres du Group Policy Object (GPO) local sur les périphériques des utilisateurs.

Pour plus d’informations sur la gestion des stratégies de MicrosoftEdge avec MicrosoftIntune, vous pouvez consulter [Gérer l’accès au web à l’aide de MicrosoftEdge avec MicrosoftIntune](/intune/manage-microsoft-edge). Gardez néanmoins à l’esprit que l’article associé est spécifique à MicrosoftEdge version45 et versions antérieures et que, par conséquent, il peut contenir des informations et des références qui ne concernent pas MicrosoftEdge Enterprise version77 et ultérieures.

> [!TIP]
> Pour plus d’informations sur la configuration de MicrosoftEdge sur macOS à l’aide de MicrosoftIntune, consultez [Configurer pour macOS](configure-microsoft-edge-on-mac.md).

## <a name="create-a-profile-to-manage-settings-in-microsoft-edge-for-windows-10"></a>Créer un profil pour gérer les paramètres dans MicrosoftEdge pour Windows10

Grâce aux modèles d’administration dans MicrosoftIntune, vous pouvez gérer les stratégies de groupe MicrosoftEdge sur vos appareils Windows10 en utilisant le cloud. Cette section vous aidera à créer un modèle pour configurer les paramètres d’application spécifiques de MicrosoftEdge. Lorsque vous créez le modèle, il crée un profil de configuration de périphérique. Vous pouvez ensuite attribuer ou déployer ce profil sur les appareils Windows10 de votre organisation.

### <a name="prerequisites"></a>Prérequis

- Windows10, avec la configuration minimale requise suivante:
  - Windows10 version1909
  - Windows10, version1903 avec la mise à jour [KB4512941](https://support.microsoft.com/kb/4512941) installée
  - Windows10, version1809 avec la mise à jour [KB4512534](https://support.microsoft.com/kb/4512534) installée
  - Windows10, version1803 avec la mise à jour [KB4512509](https://support.microsoft.com/kb/4512509) installée
  - Windows10, version1709 avec la mise à jour [KB4516071](https://support.microsoft.com/kb/4516071) installée

### <a name="use-administrative-templates-to-create-a-policy-for-microsoft-edge"></a>Utiliser les modèles d’administration pour créer méthode pour Microsoft Edge

Cette procédure s’inspire des modèles d’administration (que vous avez peut-être utilisés dans la méthode de groupe) intégrés à Intune. Vous pouvez utiliser ces modèles pour créer une méthode pour Microsoft Edge en sélectionnant les paramètres dans une liste préconfigurée.

1. Connectez-vous au portail [Microsoft Endpoint Manager](https://endpoint.microsoft.com/).
2. Sélectionnez **Appareils** dans le volet gauche de navigation.
3. De ** Appareils ** | **Vue d’ensemble**, sélectionner ** Profil de Configuration** (sous l’en-tête Méthode).
4. Dans la barre de commandes supérieure, sélectionnez **Créer profil**.
5. Dans la liste déroulante ci-dessous **Plateforme**,sélectionner **Windows 10 et ultérieure**.
6. Dans la liste déroulante ci-dessous**Profil**,sélectionner **Modèles d’Administration** puis cliquer sur le ** bouton **.Créer. La capture d’écran suivante montre les listes déroulantes permettant de sélectionner la plateforme et le type de profil.

    ![Sélectionner une plateforme et un type de profil](./media/configure-edge-with-intune/create-profile-platform.png)

7. Sous l’onglet Notions de Base, entrer un**Nom descriptif **, tel que Méthode Microsoft Edge. Si vous le souhaitez, saisissez une **Description**pour la méthode.
La capture d’écran suivante montre le formulaire de l’onglet **Notions de Base** et la barre de menus affiche les étapes suivantes (sous la forme d’onglets grisés) pour créer le profil.

   ![Entrer Nom et Description](./media/configure-edge-with-intune/create-profile-basics-tab.png)

8. Sélectionnez **Suivant**.
9. Sous l’onglet **Paramètres de configuration**, sélectionnez le dossier Microsoft Edge dans l’un des emplacements suivants:

   - ci-dessous le dossier Configuration Ordinateur
   - ci-dessous le dossier Configuration Utilisateur.

   Les paramètres disponibles pour Microsoft Edge s’affichent dans le volet droit. Par exemple, *Configuration Ordinateur/Microsoft Edge/Autoriser les restrictions de téléchargement* présenté dans la capture d’écran suivante.

   ![Onglet Paramètres de configuration](./media/configure-edge-with-intune/create-profile-configuration-settings-tab.png)

   > [!NOTE]
   > Consulter [MICROSOFT– Méthodes](./microsoft-edge-policies.md) et [Microsoft Edge– Méthodes de Mises à jour](./microsoft-edge-update-policies.md) pour la liste la plus complète et récente de tous les paramètres disponibles pour Microsoft Edge.

10. Utiliser le champ de recherche («Rechercher pour filtrer les éléments...») pour trouver un paramètre spécifique que vous voulez configurer. Dans cet exemple, la chaîne de recherche est «page d’accueil». La capture d’écran suivante montre les résultats de la recherche.

    ![Résultats de la recherche](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-search.png)

11. Une fois que vous avez trouvé le paramètre que vous voulez configurer, sélectionnez le pour afficher les valeurs que vous pouvez définir. Dans la capture d’écran suivante, nous avons sélectionné «Configurer l’URL de la page d’accueil» à titre d’exemple.

    ![Configurer la méthode URL de la page d’accueil](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-edit-pol.png)

12. Activer la méthode et entrez une valeur pour l’URL de la Page d’accueil URL, comme présenté dans la capture d’écran précédente.

13. Cliquez sur **OK**. La colonne des paramètres «État» doit apparaître comme «activé», comme illustré dans la capture d’écran suivante.

    ![L’état du paramètre est activé](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-set-enabled.png)

14. Cliquez sur le bouton **Suivant**.

15. Sur l’onglet Indicateurs d’étendue, ajoutez une balise d’étendue si vous le souhaitez, sinon cliquez sur le**bouton ** suivant.

16. Sous l’onglet **Assignations**, cliquez sur + sélectionner des groupes à inclure  pour assigner cette méthode au groupe Azure Active Directory (Azure AD) qui contient les appareils ou les utilisateurs auxquels vous voulez assigner ce paramètre de méthode. Consultez [Assigner les profils d’utilisateur et de périphérique dans MicrosoftIntune](/intune/device-profile-assign) pour les informations sur comment assigner le profil à vos groupes d’utilisateurs ou à périphériques Azure AD.

    ![Sélectionner les groupes à inclure](./media/configure-edge-with-intune/create-profile-assignments-tab.png)

17. Cliquez sur le bouton **Suivant**.

18. Sous l’onglet **Révision + créer**, réviser le résumé de vos modifications pour vous assurer qu’il est correct, puis cliquez sur le**bouton**Créer.

19. La méthode récemment créée (Méthode Microsoft Edge) est présentée dans la capture d’écran suivante.

    ![Sélectionner les groupes à inclure](./media/configure-edge-with-intune/create-profile-new-policy-finished.png)

Pour plus d’informations sur les profils Windows10, consultez [Utiliser des modèles Windows10 pour configurer les paramètres de stratégie de groupe dans MicrosoftIntune](/intune/administrative-templates-windows).

## <a name="see-also"></a>Articles associés

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Gérer l’accès web à l’aide de MicrosoftEdge avec MicrosoftIntune](/intune/manage-microsoft-edge)
- [Utilisez les modèles Windows10 pour configurer les paramètres de stratégie de groupe dans MicrosoftIntune](/intune/administrative-templates-windows)
- [Déployer MicrosoftEdge à l’aide de MicrosoftIntune](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)