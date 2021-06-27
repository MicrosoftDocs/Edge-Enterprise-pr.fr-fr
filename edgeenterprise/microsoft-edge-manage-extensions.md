---
title: Gérer les extensions MicrosoftEdge dans l’entreprise
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 04/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Gérer les extensions MicrosoftEdge dans l’entreprise
ms.openlocfilehash: c123deaed638004b380308fd0d29b40b132dbfd5
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618096"
---
# <a name="manage-microsoft-edge-extensions-in-the-enterprise"></a>Gérer les extensions MicrosoftEdge dans l’entreprise

Cet article fournit des conseils sur les meilleures pratiques pour les administrateurs qui gèrent les extensions MicrosoftEdge dans leur organisation. Vous pouvez utiliser les informations de cet article pour développer une stratégie de gestion des extensions au sein de votre organisation.

> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

## <a name="introduction"></a>Introduction

Les organisations souhaitent protéger les données d’entreprise et d’utilisateur et évaluer les extensions de navigateur pour s’assurer qu’elles sont sécurisées et pertinentes pour leur entreprise. Les administrateurs souhaitent:

- Empêchez l’installation de mauvaises applications et extensions.
- Conservez les extensions dont les utilisateurs ont besoin pour faire leur travail.
- Gérez l’accès aux données utilisateur et d’entreprise.  

Cet article est le premier d’une série qui aide les administrateurs à gérer les extensions afin de fournir une expérience sécurisée et productive à leurs utilisateurs. Cette série vous permet de choisir la meilleure méthode de gestion des extensions. La série comprend les articles suivants:

- [Gérez les extensions MicrosoftEdge dans l’entreprise](microsoft-edge-manage-extensions.md). Créez une stratégie pour gérer les extensions et configurer les modèles d’administration requis pour la gestion du navigateur.
- [Utilisez des stratégies de groupe pour gérer les extensions MicrosoftEdge](microsoft-edge-manage-extensions-policies.md). Options utilisant des stratégies de groupe pour gérer les extensions.
- [Créez un magasin web pour héberger les extensions MicrosoftEdge](microsoft-edge-manage-extensions-webstore.md). Créez et hébergez des extensions.
- [FAQ sur les extensions Microsoft Edge](microsoft-edge-manage-extensions-faq.md). Questions fréquemment posées.

## <a name="things-to-consider-when-managing-extensions"></a>Éléments à prendre en compte lors de la gestion des extensions

Vos utilisateurs ont besoin d’accéder à certaines applications, sites et extensions pour faire leur travail tout en protégeant les utilisateurs et les données de l’entreprise. Une stratégie de sécurité efficace implique de poser les bonnes questions pour votre entreprise et de savoir comment les extensions peuvent répondre aux besoins de votre entreprise. Voici quelques-unes des questions clés à poser:

- Quelles réglementations et mesures de conformité dois-je respecter?
- Certaines extensions demandent-elles des autorisations trop larges, ce qui pourrait aller à l’encontre des stratégies de sécurité des données de mon entreprise?
- Quelle quantité de données utilisateur ou d’entreprise sont stockées sur les appareils de mes utilisateurs?

Lorsque vous répondez à ces questions, vous pouvez utiliser les stratégies granulaires que Microsoft Edge fournit pour:

- Bloquez ou autorisez les extensions sur les ordinateurs des utilisateurs en fonction de vos stratégies de protection des données.
- Forcez l’installation des extensions sur les appareils de vos utilisateurs afin qu’ils disposent des outils dont ils ont besoin pour être productifs.
- Les extensions de liste verte ou de liste rouge permettent à vos utilisateurs d’avoir les droits les plus faibles nécessaires pour effectuer leur travail.

Le modèle traditionnel de gestion des extensions utilise l’approche de liste verte et de liste rouge pour des extensions spécifiques. Toutefois, MicrosoftEdge vous permet également de gérer les autorisations exigées par les extensions. À l’aide de ce modèle, vous pouvez choisir les droits et autorisations souhaitées pour autoriser les extensions à utiliser sur vos ordinateurs et appareils, puis implémenter une stratégie globale qui autorise ou bloque les extensions en fonction de vos besoins.  

## <a name="understand-extension-permissions"></a>Comprendre les autorisations d’extension

Les extensions peuvent exiger des droits pour apporter des modifications à un appareil ou à une page web pour s’exécuter correctement. Ces droits sont appelés autorisations. Les développeurs doivent répertorier les droits, puis accéder à leurs extensions. Il existe deux principales catégories pour les autorisations et de nombreuses extensions ont besoin des deux autorisations suivantes:

- Les autorisations d’hôte nécessitent l’extension pour lister les pages web qu’il peut afficher ou modifier.
- Les autorisations d’appareil sont les droits requis par une extension sur l’appareil sur lequel elle est en cours d’exécution.

Voici quelques exemples de ces autorisations : l’accès à un port USB, un écran de stockage ou d’affichage et la communication avec des programmes natifs.  

## <a name="get-ready-to-manage-extensions"></a>Se préparer à gérer les extensions

## <a name="before-you-begin"></a>Avant de commencer

Les options d’extensions supposent que vous avez déjà MicrosoftEdge géré pour vos utilisateurs. Pour plus d’informations sur la configuration de modèles d’administration pour les stratégies Microsoft Edge, voir:

-   [Configurer les paramètres de stratégie MicrosoftEdge sur Windows](/DeployEdge/configure-microsoft-edge)
-   [Configuration pour Windows avec Intune](/mem/intune/configuration/administrative-templates-configure-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)
-   [Configurer pour Windows avec la gestion des périphériques mobiles](/deployedge/configure-edge-with-mdm)
-   [Configurer pour macOS à l'aide d'un fichier .plist](/deployedge/configure-microsoft-edge-on-mac)
-   [Configuration pour macOS avec Jamf](/deployedge/configure-microsoft-edge-on-mac-jamf)

Les étapes de configuration de cet article sont Windows. Pour l’implémentation correspondante dans MAC/Linux, voir la référence de stratégie de navigateur MicrosoftEdge.

## <a name="decide-which-extensions-to-allow"></a>Déterminer les extensions à autoriser

La plupart des organisations doivent gérer les extensions par leurs autorisations et les sites web auxquels elles ont accès. Cette méthode est plus sécurisée, plus facile à gérer et évolutive pour les grandes organisations.  

- Autorisations bloquées/autorisées: vous permet de contrôler les extensions selon les autorisations dont elles ont besoin.
- Hôtes de blocage runtime: vous permet de contrôler les sites web accessibles par ces extensions.

Cette approche permet de gagner du temps, car vous n’avez besoin de les définir qu’une seule fois. Avec la stratégie d’hôtes à l’exécution, vos sites les plus importants seront protégés. Il existe d’autres options telles que:

-   Forcer les extensions d’installation: vous permet d’installer les extensions en mode silencieux.
-   Liste verte/liste rouge (si nécessaire) : déterminez les extensions autorisées à être installées.

Utilisez les étapes suivantes comme guide pour déterminer les extensions à autoriser dans votre organisation.

1. Créez une liste des extensions dont les employés ont besoin sur leurs ordinateurs. Testez les extensions dans un environnement de test pour diagnostiquer les problèmes de compatibilité avec les applications internes.
2. Choisissez les sites qui doivent être plus sécurisés.

   - Découvrez les sites web ou domaines internes sensibles sur lesquels vous devez empêcher les extensions d’apporter des modifications ou de lire des données.  
   - Empêchez l’accès à ces sites en bloquant les appels d’API lors de l’exécution de l’extension. Cela inclut le blocage des demandes web, la lecture des cookies, l’injection JavaScript, XHR, etc.

3. Déterminez les autorisations requises pour que ces extensions s’exécutent. Identifiez les autorisations qui présentent des risques potentiels pour vos utilisateurs.

   - Auditez les extensions installées par vos utilisateurs et voyez les autorisations qui leur sont nécessaires. Vous pouvez examiner le fichier manifeste JSON de l’application web dans le code de l’extension. Pour voir les droits dont l’extension a besoin, prenez les mesures suivantes:

     - Installez l’extension à partir du site web des [modules complémentaires MicrosoftEdge](https://microsoftedge.microsoft.com/addons/) ou de [Chrome Web Store](https://chrome.google.com/webstore).
     - Testez l’extension et comprenez son fonctionnement dans votre organisation.
     - Examinez les autorisations dont l’extension a besoin en naviguant vers *edge://extensions*. Par exemple, l’extension MicrosoftOffice affichée dans la capture d’écran suivante demande les autorisations «Lire votre historique de navigation» et «Afficher les notifications». Mettez en balance l’utilité de cette extension par rapport au niveau d’autorisations qu’elle demande. Après avoir approuvé une extension pour votre organisation, gérez-la à l’aide des outils suivants.
   :::image type="content" source="media/microsoft-edge-manage-extensions/manage-extesions-office-extension.png" alt-text="Extension MicrosoftOffice avec des autorisations.":::

   - Vous pouvez également valider les extensions demandées par les utilisateurs de votre organisation avant de les approuver dans l’organisation. Certaines des autorisations que les extensions utilisent peuvent être vagues. Pour les applications critiques de l’entreprise, vous pouvez entrer directement en contact avec le développeur ou le fournisseur d’applications pour obtenir plus d’informations sur l’extension ou examiner le code source. Ils doivent être en mesure de détailler les modifications que l’extension peut apporter sur les appareils et les sites web.
   - Examinez la liste Déclarer les autorisations, qui répertorie toutes les autorisations qu’une extension peut utiliser. Dans cette liste, vous pouvez choisir les autorisations que vous souhaitez autoriser dans votre organisation.

4. Créez une liste principale à partir des données que vous avez collectées. Cette liste inclut les informations suivantes:

   - **Extensions requises**. Cette liste peut être organisée par service, emplacement du bureau ou autres informations pertinentes.
   - **Liste verte des extensions**. Extensions requises avec des autorisations qui peuvent être bloquées mais qui seront autorisées à s’exécuter. Ces extensions sont requises par vos utilisateurs ou sont déterminées comme n’étant pas un risque via des conversations avec le fournisseur.
   - **Liste rouge des extensions**. Extensions dont l’installation est bloquée. Les extensions de cette liste ont des autorisations qui ne sont pas autorisées à s’exécuter. Incluez également les principaux sites et domaines à conserver sécurisés et non autorisés à accéder aux extensions. Vous pourrez ensuite comparer cette liste rouge à d’autres que vous avez déjà en place. Il se peut que vous trouviez que vous pouvez relâcher vos stratégies de liste rouge actuelles.

5. Présentez votre liste à vos parties prenantes et à l’équipe informatique pour qu’ils puissent en bénéficier.
6. Testez la nouvelle stratégie dans votre laboratoire ou avec un petit pilote dans votre organisation.
7. Déployer ces nouveaux ensembles de stratégies aux employés par phases. Pour plus d’informations, voir [Utiliser des stratégies de groupe pour gérer les extension Microsoft Edge](microsoft-edge-manage-extensions-policies.md).
8. Examinez les commentaires de vos utilisateurs.
9. Répétez et affinez le processus tous les mois, tous les trimestres ou chaque année.

Avec la ligne de base des autorisations autorisées appliquées et des sites d’entreprise sensibles protégés, vous pouvez fournir à votre entreprise une plus grande sécurité tout en offrant une meilleure expérience aux utilisateurs. Le personnel peut installer des extensions qu’il n’a pas pu faire auparavant, mais il ne peut pas les exécuter sur des sites d’entreprise sensibles.  

## <a name="see-also"></a>Voir également

- [Utiliser des stratégies de groupe pour gérer les extensions MicrosoftEdge](microsoft-edge-manage-extensions-policies.md)
- [Créer un magasin web pour héberger les extensions Microsoft Edge](microsoft-edge-manage-extensions-webstore.md)
- [Guide de référence pour la stratégie ExtensionSettings](microsoft-edge-manage-extensions-ref-guide.md)
- [FAQ sur les extensions Microsoft Edge](microsoft-edge-manage-extensions-faq.md)
- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)