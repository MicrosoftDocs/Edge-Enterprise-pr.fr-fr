---
title: Microsoft Edge et les téléchargements de contenu mixte
ms.author: kele
author: dan-wesley
manager: srugh
ms.date: 04/30/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge et les téléchargements de contenu mixte
ms.openlocfilehash: 57da17a8684b97aad88e7837ff9d070f6862357b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979751"
---
# Découvrez Microsoft Edge et les téléchargements de contenu mixte

Cet article décrit les téléchargements de contenu mixte et leur traitement par Microsoft Edge.

>[!NOTE]
>Cet article concerne MicrosoftEdge version85 ou ultérieure.

## Quels sont les téléchargements de contenu mixte?

Un téléchargement de contenu mixte se produit lorsque vous démarrez un téléchargement à partir d’une page HTML qui a été chargée sur une connexion HTTPS sécurisée, mais que l’une des conditions suivantes existe:

- Au moins une des redirections de l’emplacement de téléchargement a été chargée via une connexion HTTP non sécurisée.
- L’emplacement final de téléchargement a été chargé via une connexion HTTP non sécurisée.

Les deux scénarios sont un contenu mixte, car la demande a été effectuée à l’aide d'une connexion HTTPS sécurisée et que les contenus HTTP et HTTPS sont impliqués dans l'accession à la destination finale du téléchargement. Les navigateurs modernes affichent des avertissements sur ce type de contenu pour indiquer à l’utilisateur que ce téléchargement ne peut pas être transféré de manière non sécurisée, même si la page d’origine consultée était sécurisée.

## Télécharger des avertissements et options de l'utilisateur

L’avertissement de téléchargement permet aux utilisateurs de savoir que le fichier qu’ils téléchargent peut être lu par des pirates sur leur réseau. Cet avertissement permet à un utilisateur de prendre une décision éclairée sur le téléchargement ou non du fichier.

Dans Microsoft Edge, les téléchargements de contenu mixte sont bloqués, mais les utilisateurs peuvent passer outre et télécharger le fichier s’ils le souhaitent. Microsoft Edge prévoit de commencer à bloquer les téléchargements de fichiers exécutables de contenu mixte à partir de Microsoft Edge version85 et bloquera différents types de fichiers dans les prochaines versions.

> [!NOTE]
> Le déploiement de cette fonctionnalité peut faire l’objet de modifications en fonction du calendrier des publications et des commentaires des utilisateurs.

<!-- The schedule of the block for different filetypes is to be determined and may be impacted by usage data and user feedback. -->

Dans l’étagère de téléchargement, le message d’avertissement du blocage se présente comme l’exemple de la capture d’écran suivante.

 ![Avertissement de contenu mixte dans le plateau de téléchargement](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-tray-warning.png)

Sur la page de téléchargement, l’avertissement de blocage se présente comme dans la capture d’écran suivante:

 ![Invite d'ignorer le contenu mixte](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-page-warning.png)

Si un utilisateur décide de conserver le téléchargement, il est invité à confirmer son action. La capture d’écran suivante présente un exemple de cette invite de confirmation.

 ![Choisissez Mode InternetExplorer](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-override.png)

## Stratégies d'appui

Les entreprises souhaitant exclure le blocage de contenu mixte de certains sites web peuvent utiliser la stratégie [InsecureContentAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#insecurecontentallowedforurls) pour le faire.

## Licence de contenu

> [!NOTE]
> Certaines parties de cette page sont des modifications basées sur le travail créé et partagé par Chromium.org et utilisé conformément aux conditions décrites dans la [Licence internationale Creative Commons Attribution4.0](http://creativecommons.org/licenses/by/4.0/). La page d’origine est disponible [ici](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Ce travail est concédé sous une <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licence internationale Creative Commons Attribution4.0</a>.

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
