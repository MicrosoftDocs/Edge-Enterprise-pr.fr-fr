---
title: FAQ sur le mode IE
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 02/02/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Forum aux questions et résolution des problèmes pour Microsoft Edge avec le mode IE
ms.openlocfilehash: aeae79dfd1745c754fb5ab690338f87fd25c080b
ms.sourcegitcommit: ff67ccc93d07588a9128e9b1fe007d5393a9d6af
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "11312590"
---
# FAQ sur le mode IE

Cet article fournit des conseils de dépannage et un FAQ pour MicrosoftEdge version77 ou ultérieure.

> [!NOTE]
> Cet article concerne les canaux MicrosoftEdge **stable**, **Beta** et **Dev**, version77 ou ultérieures.

## Résolution des problèmes en mode InternetExplorer

Utilisez les informations contenues dans cette section pour diagnostiquer et résoudre les problèmes liés au mode InternetExplorer.

### Informations de diagnostic du mode InternetExplorer

Vous pouvez obtenir des informations de diagnostic en mode InternetExplorer sous l’onglet Compatibilité MicrosoftEdge. Pour ouvrir cet onglet, accédez à *edge://compat/iediagnostic*. Cette page peut afficher les messages de diagnostic. Cette page fournit également des informations de configuration pour les catégories suivantes:

- **Vérifier la clé de Registre**. (S’affiche uniquement si la vérification échoue.) Vérifie si l’intégration d’Internet Explorer est correctement configurée dans le registre. Si ce n’est pas le cas, l’utilisateur peut cliquer sur **Réparer** pour résoudre le problème.
- **Mode InternetExplorer**. Affiche la version de l’API utilisée, en fonction de la configuration et du système d’exploitation. En cas de problème, l’utilisateur peut être invité à installer un **Windows Update**.
- **Paramètre Mode InternetExplorer**. Indique si le mode Internet Explorer est activé et comment il est configuré.
- **Ligne de commande**. Affiche la chaîne de ligne de commande et les commutateurs utilisés pour démarrer MicrosoftEdge.
- **Paramètres de stratégie de groupe**. Indique si le mode IE est configuré à l’aide de stratégies de groupe et quelles stratégies sont appliquées.

### Message d’erreur: «Pour ouvrir cette page en mode InternetExplorer, réinstallez MicrosoftEdge avec des privilèges d’administrateur.»

Vous pouvez rencontrer cette erreur si vous n’avez pas toutes les mises à jour Windows requises. Consultez les conditions requises listées dans [À propos du mode IE](https://docs.microsoft.com/deployedge/edge-ie-mode) pour connaître les versions requises de Windows et MicrosoftEdge.

Si vous avez déjà installé toutes les mises à jour Windows requises, vous pouvez rencontrer cette erreur dans les cas suivants:

- Vous utilisez le canal Canari, qui est installé par défaut au niveau de l’utilisateur.
- Vous utilisez le canal Stable, Bêta ou Dev, mais lorsque vous êtes invité à une élévation lors de l’installation, l’élévation est annulée. Lorsque vous annulez l’invite d’élévation, l’installation se poursuit au niveau de l’utilisateur.
- InternetExplorer11 a été désactivé dans les fonctionnalités Windows.

Solutions possibles:

- Exécutez le programme d’installation de n’importe quel canal au niveau du système: `installer.exe --system-level`.
- Activer Internet Explorer11 dans les fonctionnalités de Windows.

Pour vérifier si MicrosoftEdge est installé au niveau du système, tapez «edge://version» dans la barre d’adresse MicrosoftEdge. Le chemin d’accès de l’Exécutable montre un chemin qui commence par *C:\Program Files*, qui indique une installation du système. Si le chemin d’accès de l’Exécutable commence par *C:\Users\*, désinstallez, puis réinstallez MicrosoftEdge avec des privilèges d’administrateur.

### Message d’erreur: «Pour ouvrir cette page en mode InternetExplorer, essayez de redémarrer MicrosoftEdge».

Cette erreur peut apparaître en cas d’erreur inattendue dans Internet Explorer. Le redémarrage de Microsoft Edge résout généralement ce problème.

### Message d’erreur: «Désactiver le débogage à distance pour ouvrir ce site en mode InternetExplorer, sinon il risque de ne pas fonctionner comme prévu».

Vous pouvez rencontrer cette erreur si vous procédez au débogage distant et accédez à une page Web configurée pour s’exécuter en mode IE. Vous pouvez continuer, mais la page sera affichée à l’aide de Microsoft Edge.

### Message d’erreur: «Erreur: La liste des sites EMIE n’a pas pu être récupérée.»

Vous pouvez voir cette erreur sur la page *edge://compat/enterprise* indiquant que le téléchargement de la liste des sites a échoué. À partir de La version87 de MicrosoftEdge, lorsque les cookies sont bloqués pour les demandes tierces à l’aide de la stratégie [BlockThirdPartyCookies,](https://docs.microsoft.com/deployedge/microsoft-edge-policies#blockthirdpartycookies) l’authentification HTTP est également interdite. Vous pouvez autoriser les cookies pour le domaine spécifique hébergeant votre liste des sites en mode Entreprise à l’aide de la stratégie [CookiesAllowedForURLs](https://docs.microsoft.com/deployedge/microsoft-edge-policies#cookiesallowedforurls) pour vous assurer que les téléchargements de listes de sites sont réussis.

## Forum Aux Questions

### Le mode IE remplace-t-il Internet Explorer11?

Nous nous engageons à ce qu’Internet Explorer reste un navigateur pris en charge, fiable et sécurisé. Internet Explorer reste un composant de Windows et suit le cycle de vie du support du système d’exploitation sur lequel il est installé. Pour plus de détails, consultez [FAQ sur le cycle de vie: Internet Explorer](https://support.microsoft.com/help/17454/). Bien que Microsoft continue à prendre en charge et à mettre à jour Internet Explorer, les fonctionnalités et mises à jour de plateforme les plus récentes seront disponibles uniquement dans MicrosoftEdge.

### Puis-je utiliser «Ouvrir avec l’Explorateur» ou «Afficher dans l’Explorateur de fichiers» dans SharePoint avec le mode IE?

Oui, si cela fonctionne dans Internet Explorer11 autonome, cela fonctionnera en mode IE. Cependant, plutôt que d’utiliser l’option Ouvrir avec Explorer, l’approche recommandée de gestion des fichiers et des dossiers en dehors de SharePoint est de [synchroniser vos fichiers SharePoint](https://support.office.com/en-us/article/sync-sharepoint-files-with-the-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88) ou de [déplacer ou copier des fichiers dans SharePoint](https://support.office.com/en-us/article/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc).

### Le mode IE sur Microsoft Edge prend-il en charge l’option *NoMerge* prise en charge dans Internet Explorer 11?

Il n’existe pas de ligne de commande explicite dans Microsoft Edge pour mettre en miroir l’option *nomerge*, mais il existe quelques solutions de remplacement recommandées pour offrir ces fonctionnalités.

1. Utiliser les profils dans Microsoft Edge: chaque profil est mappé à une session IE différente pour les pages du mode IE, de sorte qu’il se comporte de la même façon que l’option *NoMerge*.
2. Utilisez la ligne de commande `--user-data-dir=<path>`, mais avec un chemin d’accès différent pour chaque session. Si nécessaire, vous pouvez créer un utilitaire permettant à l’utilisateur d’exécuter et de lancer Microsoft Edge et de modifier le chemin d’accès de la session.

Si aucune des options ci-dessus ne fonctionne pour votre scénario, contactez l’un de nos canaux de commentaires: support Microsoft, [Forum TechCommunity](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise)ou [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/forums/928825-enterprise).

### Est-il possible d’enregistrer les liens sous forme de pages web en mode Internet Explorer?
 
Oui, vous pouvez activer l’option Enregistrer la cible sous dans le menu contextuel du mode InternetExplorer dans MicrosoftEdge. Pour ce faire, configurez la stratégie de groupe *«Autoriser Enregistrer la cible sous dans le mode InternetExplorer»* située sur *Configuration de l'ordinateur > Modèles d’administration > Composants Windows > Internet Explorer*.
Le mécanisme d’enregistrement fonctionne de la même façon que dans InternetExplorer et si la cible est enregistrée sous forme de fichier HTML, la réouverture du fichier entraîne le rendu de la page dans MicrosoftEdge.
 
Notez que cette fonctionnalité nécessite les mises à jour de système d’exploitation minimales suivantes:
- Windows10, version2004, Windows Server version2004, Windows10, version20H2: [KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)
- Windows10, version1903, Windows10, version1909, Windows Server version1903: [KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386)
- Windows10, version1809, Windows Server version1809, Windows Server2019: [KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390)
- Windows10, version1803: [KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)
- Windows10, version1607: [KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)
- Windows10, version1507: [KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)


## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [À propos du mode IE](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Informations supplémentaires sur le mode entreprise](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
