---
title: Compatibilité descendante pour la page Nouvel onglet de l’Entreprise
ms.author: ruchir
author: dan-wesley
manager: vwehren
ms.date: 10/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Compatibilité descendante pour la page Nouvel onglet de l’Entreprise
ms.openlocfilehash: 5721db16c634250b3a586f6bd1b6b531a07815a5
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447258"
---
# <a name="backwards-compatibility-for-the-enterprise-new-tab-page"></a>Compatibilité descendante pour la page Nouvel onglet de l’Entreprise

Cet article décrit la modification apportée à la page Nouvel onglet et la manière dont les utilisateurs peuvent être rétrocompatibles avec les versions MicrosoftEdge version87 et antérieures.

> [!NOTE]
> Cet article concerne MicrosoftEdge version87 ou ultérieure.

## <a name="information-feeds-from-single-endpoint"></a>Flux d’informations à partir d’un point de terminaison unique

La nouvelle version de la page Nouvel onglet de l’Entreprise associe le contenu conforme à Microsoft365 à des flux d’informations pertinents et conformes au secteur qui sont traités via le point de terminaison MSN.com.

> [!NOTE]
> Le contenu Office365 était à l’origine traité en utilisant le domaine [Office.com](https://www.office.com).

Si l’accès au domaine MSN.com est limité pour votre organisation, nous vous recommandons vivement d’autoriser les utilisateurs à accéder à cette [URL](https://ntp.msn.com).

Si vous avez besoin de davantage de temps pour autoriser l’accès au domaine MSN, nous vous recommandons d’utiliser [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) qui vous permet de choisir entre l’expérience de flux Microsoft News ou Office365 pour la nouvelle page d’onglets.

### <a name="keep-using-officecom"></a>Continuer à utiliser Office.com

 Vous pouvez configurer la stratégie **NewTabPageSetFeedType** pour continuer à utiliser le domaine Office.com déconseillé.

> [!IMPORTANT]
> La stratégie **NewTabPageSetFeedType** et le domaine Office.com qui traitent le contenu Office365 cesseront de fonctionner lorsque la version90 de MicrosoftEdge est publiée.

Les paramètres de stratégie suivants forcent la page Nouvel onglet de l’Entreprise à afficher le contenu d’un document Office à partir du domaine Office.com.

- Configurez la stratégie comme **Obligatoire**.
- Définissez la valeur du mappage de stratégie sur **Office (1) = expérience de flux Office365**.

Si le passage à Office.com n’est pas possible, n’hésitez pas à nous envoyer vos commentaires. Une autre option consiste à configurer [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) pour qu’elle pointe vers une URL de point de terminaison autorisée par votre organisation.

> [!NOTE]
> La stratégie **NewTabPageLocation** a priorité si la stratégie **NewTabPageSetFeedType** est également configurée.

## <a name="enterprise-users-will-now-get-microsoft-news-content-via-my-feed"></a>Les utilisateurs Entreprise reçoivent désormais du contenu Microsoft News via Mon flux

La page Nouvel onglet de l’Entreprise propose des informations pertinentes de **Mon flux** et le contenu Office365 dans un affichage unique pour les utilisateurs connectés avec leur compte Azure Active Directory (Azure AD). Pour les utilisateurs connectés avec leur compte Azure Active Directory (Azure AD) ayant sélectionné l’option Microsoft News dans le paramètres du menu volant, leur nouvel affichage de page d’onglet est remplacé par le contenu **Mon flux**. Lorsqu’ils ouvrent une page nouvel onglet dans le navigateur, celle-ci se présente comme dans l’exemple de la capture d’écran suivante.

![Page nouvel onglet affichant le contenu de Mon flux.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-myfeed-view.png)

> [!NOTE]
> Les utilisateurs qui ne se sont pas connectés avec Azure AD continueront à voir le flux Actualités MSN lorsqu’ils ouvrent un nouvel onglet.

## <a name="page-layout"></a>Mise en page

Avec les modifications apportées à la page nouvel onglet, la mise en page ne doit plus contrôler deux types de contenu spécifiques (Office 365 et Microsoft News), de sorte que le bouton bascule de contenu n’est pas disponible. La capture d’écran suivante montre le menu volant pour la mise en page.

![Affichage de la mise en page pour la page Nouvel onglet.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-page-layout.png)

Si vous voulez continuer à accéder au contenu de Microsoft News qui n’est pas lié à votre organisation, vous devez utiliser un autre profil de navigateur. Accédez à *edge://settings/profiles* et déconnectez-vous de votre profil Azure AD. Cette action ouvre l’affichage standard pour la page Nouvel onglet de l’Entreprise. 

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [ModeEntreprise d’InternetExplorer11](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)