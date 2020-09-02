---
title: Blocker Toolkit pour désactiver la distribution automatique de MicrosoftEdge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Blocker Toolkit pour désactiver la distribution automatique de MicrosoftEdge
ms.openlocfilehash: 7563d2c94cf91a8434328699e46c75dbcfb77561
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979825"
---
# Blocker Toolkit pour désactiver la distribution automatique de MicrosoftEdge (basé sur Chromium)

Cet article décrit le Blocker Toolkit qui permet de désactiver la distribution et l’installation automatiques de MicrosoftEdge. Nous avons mis à jour cet article le **09/01/2020** avec des informations sur les appareils susceptibles d’exiger l’utilisation de Blocker Toolkit, le **28/02/2020** pour supprimer «géré par GPM» des critères des appareils à exclure de cette mise à jour automatique, puis le **30/06/2020** pour intégrer le fait que cette mise à jour concerne tous les appareils connectés à Windows Update (en vigueur au plus tôt le 30/07/2020).

> [!NOTE]
> Cet article concerne le canal Stable de MicrosoftEdge.

## Présentation

Pour aider nos clients à rester à jour et à assurer leur sécurité, Microsoft distribuera MicrosoftEdge (basé sur Chromium) sur tous les appareils connectés à Windows Update et exécutant Windows10 versions1803 et ultérieures. Ce processus démarrera après le 15janvier2020, et des informations supplémentaires seront disponibles à cette date.

Blocker Toolkit est destiné aux organisations qui souhaitent bloquer la distribution automatique de MicrosoftEdge (basée sur Chromium) sur les appareils connectés à Windows Update et exécutant Windows10 versions1803 et ultérieures.
Cette mise à jour automatique ne concernera pas les appareils gérés par Windows Server Update Services (WSUS) ou Windows Update pour Entreprise.

**Il est important de noter que:**

- Blocker Toolkit n’empêche pas les utilisateurs d’installer manuellement MicrosoftEdge (basé sur Chromium) à partir d’un téléchargement Internet ou à partir d’un support externe.
- Les organisations dont les mises à jour sont gérées via Windows Update pour Entreprise (WUfB) ne recevront pas automatiquement cette mise à jour et n’ont pas besoin de déployer Blocker Toolkit.
- Les entreprises dotées d’environnements gérés avec une solution de gestion des mises à jour telle que WindowsServerUpdateServices (WSUS) ou SystemCenter ConfigurationManager (SCCM) n’ont pas besoin de déployer Blocker Toolkit. Elles peuvent utiliser ces produits pour gérer entièrement le déploiement des mises à jour publiées via Windows Update et Microsoft Update, notamment MicrosoftEdge (basé sur Chromium), au sein de leur environnement.
- Cette mise à jour est une mise à jour autonome (qui ne fait pas partie de la mise à jour cumulative mensuelle) pour offrir aux clients d’entreprise une flexibilité et un contrôle maximal sur le déploiement de cette mise à jour.
- Le nouveau Microsoft Edge (basé sur Chromium) fera partie de la mise à jour des fonctionnalités de Windows10 version20H2 au second semestre 2020. Blocker Toolkit n’a aucun impact sur les comportements ou le déploiement de 20H2. Si vous souhaitez en savoir plus d’informations sur Windows10 version20H2, veuillez cliquer [ici](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).

Vous pouvez télécharger le fichier exécutable de Blocker Toolkit à partir de [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).

### Composants de Blocker Toolkit

Ce kit de ressources comprend les composants suivants:

- Script de bloqueur exécutable (.CMD)
- Modèle d’administration de la stratégie de groupe (.ADMX et .ADML)

### Systèmes d’exploitation pris en charge

Windows10, version1803 et ultérieures.

## Script de bloqueur

Le script crée une clé de registre et définit la valeur associée à bloquer ou débloquer (selon l’option de ligne de commande utilisée) de la distribution automatique de MicrosoftEdge (basé sur Chromium) sur l’ordinateur local ou sur un ordinateur cible distant.

**Clé de Registre:** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**Nom de la valeur de clé:** `DoNotUpdateToEdgeWithChromium`

| Valeur                | Résultat                         |
|----------------------|--------------------------------|
| *La clé n’est pas définie* | La distribution n’est *pas* bloquée. |
| 0                    | La distribution n’est *pas* bloquée. |
| 1                    | La distribution est bloquée.       |

Le script possède la syntaxe de ligne de commande suivante:<br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### Nom de l’ordinateur

Le paramètre `<machine name>` est facultatif. Si ce paramètre n’est pas spécifié, l’action est effectuée sur l’ordinateur local. Dans le cas contraire, l’ordinateur distant est accessible par le biais des fonctionnalités de Registre distant de la commande `REG`. Si le Registre distant est inaccessible en raison d’autorisations de sécurité ou si l’ordinateur distant est introuvable, un message d’erreur est renvoyé par la commande `REG`.

### Commutateurs

Les commutateurs utilisés par le script s’excluent mutuellement et seul le premier commutateur valide d’une commande donnée est traité. Le script peut être exécuté plusieurs fois sur le même ordinateur.

| Commutateur       | Description                              |
|--------------|------------------------------------------|
| `/B`         | Bloque la distribution                      |
| `/U`         | Débloque la distribution                    |
| `/H` ou `/?` | Affiche l’aide récapitulative suivante:<br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## Modèle d’administration de la stratégie de groupe (fichiers .ADMX et .ADML)

Le modèle d’administration de la stratégie de groupe (fichiers .ADMX et.ADML) permet aux administrateurs d’importer les nouveaux paramètres de stratégie de groupe pour bloquer ou débloquer la distribution automatique de MicrosoftEdge (basé sur Chromium) dans leur environnement de stratégie de groupe, et d’utiliser une stratégie de groupe pour exécuter l’action de manière centralisée sur les différents systèmes au sein de leur environnement.

Les utilisateurs qui exécutent Windows10RS3Entreprise/EDU et RS4 et versions ultérieures verront la stratégie sous le chemin d’accès suivant:

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

Ce paramètre est disponible uniquement en tant que paramètre d’ordinateur; il n’existe aucun paramètre par utilisateur.

> [!IMPORTANT]
> Ce paramètre de Registre n’est pas stocké dans une clé de stratégies, il est considéré comme une *préférence*. Par conséquent, si l’objet de stratégie de groupe qui implémente le paramètre est supprimé ou si la stratégie est définie sur **non configurée**, le paramètre est conservé. Pour débloquer la distribution de MicrosoftEdge (basé sur Chromium) à l’aide d’une stratégie de groupe, définissez la stratégie sur **désactivé**.

## Articles associés

- [Page d’accueil MicrosoftEdge Entreprise](https://www.microsoftedgeinsider.com/enterprise)
- [Mises à jour Windows pour prendre en charge MicrosoftEdge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [Comment accéder à l’ancienne version de MicrosoftEdge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
