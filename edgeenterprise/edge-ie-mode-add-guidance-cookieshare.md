---
title: Partage de cookies de Microsoft Edge vers Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Mode de partage de cookies de Microsoft Edge vers Internet Explorer '
ms.openlocfilehash: ddd9d34b5e2b0ee49093734da82e4a4fa7aa6a69
ms.sourcegitcommit: 306582403d4272831bcac390154c7cc7041a9b7e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/21/2020
ms.locfileid: "11238181"
---
# Partage de cookies de Microsoft Edge vers Internet Explorer

Cet article décrit la configuration du partage de cookies de session d’un processus Microsoft Edge vers un processus Internet Explorer, en utilisant le mode Internet Explorer.

> [!NOTE]
> Cet article concerne MicrosoftEdge version87 ou ultérieure.

## Conditions préalables

- Mises à jour Windows

  - Windows 10 version 2004, Windows Server version 2004-KB4571744 ou version ultérieure
  - Windows 10 version 1909, Windows Server version 1909 – KB4566116 ou version ultérieure
  - Windows 10 version 1903, Windows Server version 1903 – KB4566116 ou version ultérieure
  - Windows10 version1809, Windows Server version1809 et Windows Server2019 – KB4571748 ou plus
  - Windows10 version1803: KB4577032 ou plus

- Microsoft Edge version87 ou ultérieure
- [Mode Internet Explorer](https://aka.ms/iemodeonedge)  configuré avec la liste des sites en mode Entreprise

## Vue d'ensemble

Une configuration courante dans les grandes organisations consiste à lier une application qui fonctionne sur un navigateur moderne à une autre application, configurable pour s’ouvrir en mode Internet Explorer avec l’authentification unique (SSO) activée dans le flux de travail.

Par défaut, les processus Microsoft Edge et Internet Explorer ne partagent pas de cookies de session, ce qui peut s’avérer gênant dans certains cas. Par exemple, lorsqu’un utilisateur doit s’authentifier de nouveau en mode Internet Explorer ou lorsque la déconnexion d’une session Microsoft Edge n’entraîne pas celle de la session en mode Internet Explorer. Dans ces scénarios, vous pouvez configurer des cookies spécifiques définis par l’authentification unique pour qu’ils soient envoyés à partir de Microsoft Edge vers Internet Explorer pour que l’expérience d’authentification devienne plus transparente en éliminant la nécessité de s’authentifier à nouveau.

> [!NOTE]
> Vous pouvez partager des cookies de session uniquement de Microsoft Edge vers Internet Explorer. Vous ne pouvez pas partager de cookies de session dans le sens inverse (d’Internet Explorer vers Microsoft Edge).

## Fonctionnement du partage de cookies

Nous avons étendu le fichier XML de liste de sites en mode entreprise pour autoriser des éléments supplémentaires à spécifier des cookies à partager depuis une session Microsoft Edge avec Internet Explorer.  

Lors de la première création d’un onglet de mode Internet Explorer dans une session Microsoft Edge, le partage de tous les cookies correspondants s’effectue vers la session Internet Explorer. Par la suite, chaque fois à chaque ajout, suppression ou modification d’un cookie qui correspond à une règle, l’application envoie ce cookie sous forme de mise à jour à la session Internet Explorer. L’ensemble de cookies partagés fait également l’objet d’une réévaluation lors de la mise à jour de la liste de sites.

### Éléments de schéma mis à jour

Le tableau suivant décrit l’élément \<shared-cookie\> ajouté pour la prise en charge de la fonctionnalité de partage de cookies.

| Élément| Description |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>OU<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |**(obligatoire)** Un élément \<shared-cookie\> nécessite au minimum un attribut de *domaine* (pour les cookies de domaine) ou un attribut d’*hôte* (pour les cookies hôtes uniquement) et un attribut de *nom*.<br>Il doit s’agir de correspondances exactes avec le domaine et le nom du cookie, respectivement. **Notez** que les sous-domaines ne correspondent pas.<br><br>Nous utilisons l’attribut de *domaine* pour les cookies de domaine (et nous autorisons un point de début, cependant facultatif).<br>Nous utilisons l’attribut d’*hôte* pour les cookies hôtes uniquement (et un point de début correspond à une erreur). Le fait de ne spécifier aucun de ces attributs ou les deux attributs génère une erreur.<br>* Un cookie est un cookie de domaine si la chaîne de cookie comprend un domaine spécifié (par le biais de l’en-tête de réponse HTTP Set-Cookie ou de l’API document.cookie JS). Un cookie de domaine s’applique au domaine spécifié et à tous les sous-domaines. Si la chaîne de cookie ne comprend aucun domaine spécifié, le cookie est un cookie d’hôte uniquement qui s’applique uniquement à l’hôte spécifique pour lequel il a été défini. Notez que certaines classes d’URL telles que les noms d’hôte en un seul mot (par exemple, http://intranetsite) et les adresses IP (par exemple, http://10.0.0.1) ne peuvent définir que des cookies d’hôte uniquement.    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | ** (facultatif)** Vous pouvez spécifier un attribut de *chemin d’accès*. Si vous ne spécifiez aucun attribut de chemin d'accès (ou si cet attribut est vide), les cookies qui correspondent à un domaine/hôte et à un nom correspondent à la stratégie, quel que soit le chemin d’accès (règle de caractère générique).<br><br>Si vous spécifiez un chemin d’accès, celui-ci doit être une correspondance exacte.<br>Les cookie correspondant à une règle avec un chemin d’accès ont priorité sur les règles sans chemin d’accès. |

#### Exemple de partage

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## Voir également

- [À propos du mode IE](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Informations sur les sites configurables](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [Informations supplémentaires sur le mode entreprise](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
