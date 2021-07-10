---
title: Partage de cookies de Microsoft Edge vers Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 'Mode de partage de cookies de Microsoft Edge vers Internet Explorer '
ms.openlocfilehash: 8f1a38106e49f71aa9d27f32cfecbd0df44eaf9f
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641840"
---
# <a name="cookie-sharing-from-microsoft-edge-to-internet-explorer"></a>Partage de cookies de Microsoft Edge vers Internet Explorer

>[!Note]
> L’application de bureau Internet Explorer 11 sera retirée et ne sera plus prise en charge le 15 juin 2022 (pour obtenir la liste des éléments concernés, [consultez le FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Les mêmes applications et sites Internet Explorer 11 que vous utilisez aujourd’hui peuvent s’ouvrir Microsoft Edge le mode Internet Explorer. [Apprenez-en plus ici](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

Cet article décrit la configuration du partage de cookies de session d’un processus Microsoft Edge vers un processus Internet Explorer, en utilisant le mode Internet Explorer.

> [!NOTE]
> Cet article concerne Microsoft Edge version 87 ou ultérieure.

## <a name="prerequisites"></a>Conditions préalables

- Mises à jour Windows

  - Windows 10 version 2004, Windows Server version 2004-KB4571744 ou version ultérieure
  - Windows 10 version 1909, Windows Server version 1909 – KB4566116 ou version ultérieure
  - Windows 10 version 1903, Windows Server version 1903 – KB4566116 ou version ultérieure
  - Windows 10 version 1809, Windows Server version 1809 et Windows Server 2019 – KB4571748 ou plus
  - Windows 10 version 1803 : KB4577032 ou plus

- Microsoft Edge version 87 ou ultérieure
- [Mode Internet Explorer](./edge-ie-mode.md)  configuré avec la liste des sites en mode Entreprise

## <a name="overview"></a>Vue d'ensemble

Une configuration courante dans les grandes organisations consiste à lier une application qui fonctionne sur un navigateur moderne à une autre application, configurable pour s’ouvrir en mode Internet Explorer avec l’authentification unique (SSO) activée dans le flux de travail.

Par défaut, les processus Microsoft Edge et Internet Explorer ne partagent pas de cookies de session, ce qui peut s’avérer gênant dans certains cas. Par exemple, lorsqu’un utilisateur doit s’authentifier de nouveau en mode Internet Explorer ou lorsque la déconnexion d’une session Microsoft Edge n’entraîne pas celle de la session en mode Internet Explorer. Dans ces scénarios, vous pouvez configurer des cookies spécifiques définis par l’authentification unique pour qu’ils soient envoyés à partir de Microsoft Edge vers Internet Explorer pour que l’expérience d’authentification devienne plus transparente en éliminant la nécessité de s’authentifier à nouveau.

> [!NOTE]
> Vous pouvez partager des cookies de session uniquement de Microsoft Edge vers Internet Explorer. Vous ne pouvez pas partager de cookies de session dans le sens inverse (d’Internet Explorer vers Microsoft Edge).

## <a name="how-cookie-sharing-works"></a>Fonctionnement du partage de cookies

Nous avons étendu le fichier XML de liste de sites en mode entreprise pour autoriser des éléments supplémentaires à spécifier des cookies à partager depuis une session Microsoft Edge avec Internet Explorer.  

Lors de la première création d’un onglet de mode Internet Explorer dans une session Microsoft Edge, le partage de tous les cookies correspondants s’effectue vers la session Internet Explorer. Par la suite, chaque fois à chaque ajout, suppression ou modification d’un cookie qui correspond à une règle, l’application envoie ce cookie sous forme de mise à jour à la session Internet Explorer. L’ensemble de cookies partagés fait également l’objet d’une réévaluation lors de la mise à jour de la liste de sites.

### <a name="updated-schema-elements"></a>Éléments de schéma mis à jour

Le tableau suivant décrit l’élément \<shared-cookie\> ajouté pour la prise en charge de la fonctionnalité de partage de cookies.

| Élément| Description |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>OU<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |**(obligatoire)** Un élément \<shared-cookie\> nécessite au minimum un attribut de *domaine* (pour les cookies de domaine) ou un attribut d’*hôte* (pour les cookies hôtes uniquement) et un attribut de *nom*.<br>Il doit s’agir de correspondances exactes avec le domaine et le nom du cookie, respectivement. **Notez** que les sous-domaines ne correspondent pas.<br><br>Nous utilisons l’attribut de *domaine* pour les cookies de domaine (et nous autorisons un point de début, cependant facultatif).<br>Nous utilisons l’attribut d’*hôte* pour les cookies hôtes uniquement (et un point de début correspond à une erreur). Le fait de ne spécifier aucun de ces attributs ou les deux attributs génère une erreur.<br>* Un cookie est un cookie de domaine si la chaîne de cookie comprend un domaine spécifié (par le biais de l’en-tête de réponse HTTP Set-Cookie ou de l’API document.cookie JS). Un cookie de domaine s’applique au domaine spécifié et à tous les sous-domaines. Si la chaîne de cookie ne comprend aucun domaine spécifié, le cookie est un cookie d’hôte uniquement qui s’applique uniquement à l’hôte spécifique pour lequel il a été défini. Notez que certaines classes d’URL telles que les noms d’hôte en un seul mot (par exemple, http://intranetsite) et les adresses IP (par exemple, http://10.0.0.1) ne peuvent définir que des cookies d’hôte uniquement.    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | ** (facultatif)** Vous pouvez spécifier un attribut de *chemin d’accès*. Si vous ne spécifiez aucun attribut de chemin d'accès (ou si cet attribut est vide), les cookies qui correspondent à un domaine/hôte et à un nom correspondent à la stratégie, quel que soit le chemin d’accès (règle de caractère générique).<br><br>Si vous spécifiez un chemin d’accès, celui-ci doit être une correspondance exacte.<br>Les cookie correspondant à une règle avec un chemin d’accès ont priorité sur les règles sans chemin d’accès. |

#### <a name="sharing-example"></a>Exemple de partage

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## <a name="see-also"></a>Voir également

- [À propos du mode IE](./edge-ie-mode.md)
- [Informations sur les sites configurables](./edge-learnmore-configurable-sites-ie-mode.md)
- [Informations supplémentaires sur le mode entreprise](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)