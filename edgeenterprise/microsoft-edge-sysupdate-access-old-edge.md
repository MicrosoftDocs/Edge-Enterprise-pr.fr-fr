---
title: Accéder à l’ancienne version de MicrosoftEdge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 08/17/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez comment accéder à la version héritée de MicrosoftEdge.
ms.openlocfilehash: e5a97a487dc6b3a45504a721e460a69103b0174e
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979793"
---
# Accéder à la version héritée de MicrosoftEdge après avoir installé la nouvelle version de MicrosoftEdge

Découvrez comment accéder à la version héritée de MicrosoftEdge après avoir installé la nouvelle version de MicrosoftEdge.

> [!NOTE]
> Cet article concerne le [canal stable](microsoft-edge-channels.md) de MicrosoftEdge.

Bien que la plupart des organisations souhaiteront remplacer l’héritage Microsoft Edge par la nouvelle version, il existe certaines situations dans lesquelles les utilisateurs auront besoin d’accéder à ces deux versions. Par exemple:

- Support technique et techniciens du support qui interagissent avec les utilisateurs qui utilisent la version de Microsoft Edge, ou les deux.
- Développeurs prenant en charge des clients qui utilisent la version de Microsoft Edge, ou les deux.

> [!IMPORTANT]
> Il n’est pas recommandé d’utiliser l’application Microsoft Edge Legacy côte à côte avec la nouvelle version de Microsoft Edge en production. Cette configuration ne doit être utilisée que dans les cas spécifiques où des tests avec les deux versions du navigateur sont requis.
>
> L’ Assistance pour l’application de bureau de Microsoft Edge arrivera à terme le 9 mars 2021 en faveur de la nouvelle application Microsoft Edge. Cela signifie que Microsoft Edge Legacy ne recevra pas de mises à jour de sécurité après cette date. Ce changement est applicable à toutes les options qui sont exécutées dans l’application de bureau de Microsoft Edge Legacy. [En savoir plus](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).

## Avant de commencer

Les procédures présentées dans cet article s’appliquent aux systèmes qui ont été mis à jour avec les dernières mises à jour de sécurité. Lorsque la nouvelle version de MicrosoftEdge est installée, l’ancienne version (MicrosoftEdge héritée) est masquée. Par défaut, toutes les tentatives de lancement de l’ancienne version de MicrosoftEdge redirigent l’utilisateur vers la nouvelle version de MicrosoftEdge installée. Cet article décrit la manière dont vous pouvez continuer à utiliser le langage hérité Microsoft Edge après l’installation de Microsoft Edge.

## Démarrage rapide: Option côte à côte avec la Chaine Beta de Microsoft Edge et Microsoft Edge Legacy

Avant d’utiliser les instructions détaillées de cet article, prenez en compte les deux étapes suivantes pour permettre à vos utilisateurs d’exécuter Microsoft Edge Legacy et la chaine Beta de [ Microsoft Edge](microsoft-edge-channels.md) cote à cote.

1. Empêchez l’installation automatique du canal stable MicrosoftEdge par [Windows Update.](https://support.microsoft.com/help/12373/windows-update-faq)

   > [!TIP]
   > Utilisez [Blocker Toolkit](microsoft-edge-blocker-toolkit.md) pour désactiver la distribution automatique de MicrosoftEdge.

2. Installez le [canal bêta](https://www.microsoft.com/edge/business/download) de la nouvelle version de Microsoft Edge.

   > [!NOTE]
   > Lisez [informations supplémentaires](#additional-information) pour plus d’informations sur les paramètres de clé de registre.

Cette solution côte à côte est moins complexe et nécessite moins de gestion que la solution détaillée décrite dans cet article. Toutefois, cette solution signifie que vous exécutez la Chaine Beta, plutôt que la Chaine Stable.

## L’option côte à côte avec la Chaine Stable de Microsoft Edge et Microsoft Edge Legacy

L’installation du canal stable de la nouvelle version de Microsoft Edge au niveau système entraînera le masquage de la version actuelle (le contrôle de l’ancienne version de Microsoft Edge). Si vous voulez permettre aux utilisateurs de voir les deux versions de Microsoft Edge côte à côte dans Windows, vous pouvez activer cette option en définissant l’option **autoriser le navigateur Microsoft Edge côte** à côte sur **activé**.

Cette stratégie de groupe est documentée [ici](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)

### Pour configurer la stratégie d’interface de navigateur côte à côte:

1. Installez les définitions de stratégie à partir de [Microsoft Edge pour les entreprises](https://www.microsoft.com/edge/business/download).

   - Choisissez le canal/la construction et la plateforme que vous voulez utiliser, puis cliquez sur obtenir des fichiers de stratégie.
   - Extrayez les fichiers zip.
   - Copiez msedge.admx et msedgeupdate.admx dans le répertoire `C:\Windows\PolicyDefinitions`.
   - Copiez msedge. adml et msedgeupdate. adml (à partir du répertoire Language/locale approprié) vers `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` le répertoire.

2. Ouvrez l’éditeur de stratégies de groupe (gpedit.msc).
3. Sous **Configuration de l’ordinateur**, accédez à *Modèles d’administration > Microsoft Edge Update > Applications*.

    > [!NOTE]
    > Si vous ne voyez pas le dossier *Microsoft Edge Update* , vérifiez que l’étape 1 s’est correctement effectuée.

4. Sous **Applications**, double-cliquez sur «Autoriser l’expérience de navigateur côte à côte MicrosoftEdge». Consultez notre [guide des bonnes pratiques](#best-practice-guidance) avant de passer à l’étape suivante.

    > [!NOTE]
    > Par défaut, cette stratégie de groupe est définie sur «Non configurée», ce qui entraîne le masquage de la version héritée de MicrosoftEdge lors de l’installation de la nouvelle version de MicrosoftEdge.

5. Sélectionnez **Activé**, puis cliquez sur **OK**.  

La définition de cette stratégie définira la clé de Registre suivante sur «00000001»:

- Clé: `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- Nom de la valeur: `Allowsxs`
- Type de la valeur: `'REG_DWORD'`

#### Guide des bonnes pratiques

Pour une expérience optimale, la stratégie **Autoriser l’expérience de navigateur côte à côte MicrosoftEdge** doit être activée avant le déploiement de la nouvelle version de MicrosoftEdge sur les appareils de vos utilisateurs.

Si elle est activée après le déploiement de MicrosoftEdge, les effets secondaires suivants se produisent et les actions suivantes sont requises:

1. **Autoriser l’expérience de navigateur côte à côte MicrosoftEdge** ne prend effet que lorsque le programme d’installation de la nouvelle version de MicrosoftEdge est exécuté à nouveau.

   > [!NOTE]
   > Le programme d’installation peut être exécuté directement ou automatiquement lorsque la nouvelle version de MicrosoftEdge est mise à jour.

2. La version héritée de MicrosoftEdge doit être épinglée à nouveau à l’écran de démarrage ou à la barre des tâches, car l’épinglage est migré lors du déploiement de la nouvelle version de MicrosoftEdge.
3. Les sites qui étaient épinglés à l’écran de démarrage ou à la barre des tâches pour la version héritée de MicrosoftEdge seront migrés vers la nouvelle version de MicrosoftEdge.

## Informations complémentaires

Une fois que les systèmes sont entièrement mis à jour et que le canal stable de la version suivante de MicrosoftEdge est installé, la clé de Registre et la valeur de Registre suivantes sont définies:

- Clé: `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- Valeur de clé: `BrowserReplacement`

  > [!IMPORTANT]
  > Cette clé est écrasée chaque fois que le canal stable MicrosoftEdge est mis à jour. Il est recommandé de NE PAS supprimer cette clé, afin de permettre aux utilisateurs d’accéder aux deux versions de MicrosoftEdge.

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Mises à jour Windows pour prendre en charge MicrosoftEdge](microsoft-edge-sysupdate-windows-updates.md)
