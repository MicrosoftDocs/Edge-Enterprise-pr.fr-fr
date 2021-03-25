---
title: ClickOnce et DirectInvoke dans MicrosoftEdge
ms.author: kele
author: dan-wesley
manager: srugh
ms.date: 09/10/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez ClickOnce et DirectInvoke dans MicrosoftEdge.
ms.openlocfilehash: 1103c4f5c071b0d04c347a7c7c9fbc5556c4c0fb
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447668"
---
# <a name="understand-the-clickonce-and-directinvoke-features-in-microsoft-edge"></a>Découvrez les fonctionnalités ClickOnce et DirectInvoke dans MicrosoftEdge

ClickOnce et DirectInvoke sont des fonctionnalités disponibles dans Internet Explorer et MicrosoftEdge (version45 et antérieures), qui permettent d’utiliser un gestionnaire de fichiers pour télécharger des fichiers à partir d’un site web. Bien que leur finalité soit différente, les deux fonctionnalités permettent aux sites web de spécifier qu’un fichier demandé pour le téléchargement doit être transmis à un gestionnaire de fichiers sur le périphérique de l’utilisateur. Les demandes ClickOnce sont gérées par le gestionnaire de fichiers natif dans Windows. Les demandes DirectInvoke sont gérées par un gestionnaire de fichiers inscrit spécifié par le site web qui héberge le fichier.

Pour plus d’informations sur ces méthodes, voir les articles suivants:

- [ClickOnce](/visualstudio/deployment/clickonce-security-and-deployment?view=vs-2019)
- [DirectInvoke]( https://technet.microsoft.com/learning/jj215788(v=vs.94).aspx)

> [!NOTE]
> Actuellement, Chromium n’offre pas de prise en charge native pour ClickOnce ou DirectInvoke.

## <a name="overview-prerequisites-and-process"></a>Vue d’ensemble: conditions préalables et processus

Pour que ClickOnce et DirectInvoke fonctionnent comme prévu et que le gestionnaire de fichiers soit correctement demandé, ce dernier doit être inscrit auprès du système d’exploitation comme prenant en charge ClickOnce ou DirectInvoke. Cette inscription survient généralement lorsque le système d’exploitation d’origine est installé ou lorsqu’un nouveau programme installé demande la possibilité d’utiliser DirectInvoke pour les mises à jour.

Lorsqu’un site web reçoit une demande de téléchargement qui nécessite ClickOnce ou DirectInvoke, les actions suivantes se produisent:

- Le site web demande au navigateur d’utiliser un gestionnaire de fichiers spécifié.
- Le navigateur vérifie le Registre du système d’exploitation pour voir si le gestionnaire de fichiers est inscrit pour le type de fichier demandé.
- Si le gestionnaire de fichiers est inscrit, le navigateur appelle le gestionnaire de fichiers et transmet l’URL en tant qu’argument au gestionnaire de fichiers.
- Le gestionnaire de fichiers traite l’URL et télécharge le fichier.

  > [!NOTE]
  > L’URL permet de déterminer la source du fichier, ainsi que les paramètres à utiliser lors de l’accès au fichier.  Par exemple: points de terminaison, manifeste ou métadonnées.

## <a name="use-cases"></a>Cas d’utilisation

Les cas d’utilisation suivants sont représentatifs.

Vous pouvez utiliser ClickOnce pour déployer et mettre à jour facilement des logiciels sur des appareils avec une interaction utilisateur minimale. Les utilisateurs peuvent installer et exécuter une application Windows en cliquant sur un lien dans une page web. Si elle est correctement configurée, l’application ClickOnce peut installer des programmes sans que les utilisateurs ne définissent des configurations pour le programme d’installation. Par exemple, les emplacements de fichiers, les options à installer, etc.

Les cas d’utilisation de DirectInvoke dépendent de l’intention du site web demandant DirectInvoke. Par exemple, la fonctionnalité de modification de fichiers collaborative de MicrosoftWord. Au lieu de cliquer sur un lien et de télécharger la copie complète d’un document sur lequel vous travaillez avec vos collègues, DirectInvoke vous permet de télécharger les parties du document qui ont été modifiées. Cette stratégie réduit la quantité de données transférées et peut réduire le temps nécessaire à l’ouverture du document.  

## <a name="current-support-for-clickonce-and-directinvoke-in-microsoft-edge"></a>Prise en charge actuelle de ClickOnce et de DirectInvoke dans MicrosoftEdge

Prise en charge de ClickOnce et de DirectInvoke:

- DirectInvoke et ClickOnce sont prises en charge pour tous les utilisateurs de Windows.

  > [!NOTE]
  > Les utilisateurs souhaitant désactiver le support ClickOnce peuvent accéder à *edge://flags/#edge-click-once* et sélectionnent **Désactivé** dans la liste déroulante. Vous devez ensuite **Redémarrer** le navigateur.

- ClickOnce et DirectInvoke ne sont pas pris en charge sur les plateformes autres que Windows.

## <a name="clickonce-and-directinvoke-file-handling-security"></a>Sécurité de gestion des fichiers ClickOnce et DirectInvoke

ClickOnce et DirectInvoke sont protégés par le service d’analyse de la réputation des URL de Microsoft Defender SmartScreen.

Si une demande ClickOnce ou DirectInvoke est marquée par le service de réputation des URL de Microsoft Defender SmartScreen comme étant dangereuse, les utilisateurs pour lesquels ClickOnce ou DirectInvoke est activé voient deux fenêtres contextuelles.

La première fenêtre contextuelle demande à l’utilisateur s’il souhaite ouvrir le fichier. Cette fenêtre contextuelle s’affiche, que le fichier soit marqué comme sûr ou dangereux. L’utilisateur peut **Signaler le fichier comme dangereux**, **Annuler** la demande ou cliquer sur **Ouvrir** pour continuer.

   ![Invite d’ouverture du fichier](./media/edge-learn-more-co-di/edge-clickonce-modal-1.png)

Si l’utilisateur tente d’ouvrir le fichier et que le fichier a été marqué comme dangereux, une deuxième fenêtre contextuelle s’affiche.  Cette fenêtre contextuelle avertit l’utilisateur que le fichier a été marqué comme dangereux et lui demande s’il souhaite le télécharger.

La deuxième fenêtre contextuelle s’affiche uniquement si:

- le fichier est un fichier ClickOnce ou DirectInvoke;
- ClickOnce ou DirectInvoke est activé;
- le fichier est marqué comme dangereux.

 ![Invite d’ouverture d’un fichier dangereux](./media/edge-learn-more-co-di/edge-clickonce-modal-2.png)

> [!NOTE]
> Si ClickOnce ou DirectInvoke est désactivé, les fichiers demandés sont traités comme des téléchargements ordinaires et, s’ils sont signalés comme étant dangereux, ils sont marqués comme dangereux. Cette procédure est cohérente avec le traitement des autres téléchargements dangereux.

## <a name="clickonce-and-directinvoke-policies"></a>Stratégies ClickOnce et DirectInvoke

Il existe deux stratégies de groupe que vous pouvez utiliser pour activer ou désactiver ClickOnce et DirectInvoke pour les utilisateurs d’entreprise. Ces deux stratégies sont [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled) et [DirectInvokeEnabled](./microsoft-edge-policies.md#directinvokeenabled). Ces deux stratégies sont étiquetées dans l’éditeur de stratégie de groupe en tant que «Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole ClickOnce» et «Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole DirectInvoke», respectivement.

## <a name="clickonce-and-directinvoke-behavior"></a>Comportement de ClickOnce et DirectInvoke

Les exemples suivants illustrent la gestion des fichiers lorsque ClickOnce et DirectInvoke sont activés ou désactivés.

### <a name="clickonce-enabled"></a>ClickOnce activé

1. Un utilisateur ouvre un lien vers une page qui demande la prise en charge de ClickOnce et reçoit l’invite présentée dans la capture d’écran suivante.

   ![Invite d’ouverture d’un fichier dangereux](./media/edge-learn-more-co-di/edge-clickonce-enabled-1.png)

2. Lorsque l’utilisateur clique sur **Ouvrir**, ClickOnce tente de lancer l’application.

   ![ClickOnce tente de lancer l’application](./media/edge-learn-more-co-di/edge-clickonce-enabled-launch-app.png)

3. Lorsque l’utilisateur clique sur **Ouvrir**, le navigateur affiche une fenêtre contextuelle qui demande à l’utilisateur s’il souhaite installer l’application.

   ![Invite d’ouverture du fichier](./media/edge-learn-more-co-di/edge-clickonce-enabled-2.png)

   > [!NOTE]
   > L’interface, la messagerie et les options affichées par le gestionnaire de fichiers ClickOnce varient en fonction du type et de la configuration du fichier auquel vous accédez.

### <a name="clickonce-disabled"></a>ClickOnce désactivé

1. Lorsqu’un utilisateur ouvre un lien vers une page qui demande la prise en charge de ClickOnce, un message s’affiche dans la barre d’état de téléchargement, semblable à celui de la capture d’écran suivante.

   ![Invite de téléchargement de fichier](./media/edge-learn-more-co-di/edge-clickonce-disabled-1.png)

### <a name="directinvoke-enabled"></a>DirectInvoke activé

1. Un utilisateur ouvre un lien vers une page qui demande la prise en charge de DirectInvoke et reçoit l’invite présentée dans la capture d’écran suivante.

   ![Invite d’ouverture du fichier](./media/edge-learn-more-co-di/edge-directinvoke-open-link-1.png)

2. Lorsque l’utilisateur clique sur **Ouvrir**, le gestionnaire de fichiers demandé s’ouvre. Dans cet exemple, MicrosoftWord est utilisé pour ouvrir le document affiché dans la capture d’écran précédente.

   > [!NOTE]
   > L’interface, la messagerie et les options affichées par le gestionnaire de fichiers DirectInvoke varient en fonction du type et de la configuration du fichier auquel vous accédez.

### <a name="directinvoke-disabled"></a>DirectInvoke désactivé

1. Lorsqu’un utilisateur ouvre un lien vers une page qui demande une prise en charge de DirectInvoke, DirectInvoke se comporte de la même manière que lorsque ClickOnce est désactivé. Un message semblable à celui de la capture d’écran suivante s’affiche dans barre d’état de téléchargement.

   ![Invite d’ouverture du fichier](./media/edge-learn-more-co-di/edge-directinvoke-open-link-2.png)

## <a name="see-also"></a>Articles associés

- [Sécurité et déploiement de ClickOnce](/visualstudio/deployment/clickonce-security-and-deployment)
- [DirectInvoke dans Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/jj215788(v=vs.85))
- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)