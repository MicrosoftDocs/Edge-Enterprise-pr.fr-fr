---
title: Résolution des problèmes du mode IE et FORUM aux questions
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/15/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Résolution des problèmes et forum aux questions pour le mode Microsoft Edge Internet Explorer
ms.openlocfilehash: 77b31362bd7d28598ead7f0a3b33a69f2f4cb264
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470202"
---
# <a name="ie-mode-troubleshooting-and-faq"></a>Résolution des problèmes du mode IE et FORUM aux questions

Cet article fournit des conseils de dépannage et un FAQ pour Microsoft Edge version 77 ou ultérieure.

> [!NOTE]
> Cet article concerne Microsoft Edge version 77 ou ultérieure.


## <a name="troubleshoot-ie-mode"></a>Résolution des problèmes en mode Internet Explorer

Utilisez les informations contenues dans cette section pour diagnostiquer et résoudre les problèmes liés au mode Internet Explorer.

### <a name="internet-explorer-mode-diagnostic-information"></a>Informations de diagnostic du mode Internet Explorer

Vous pouvez obtenir des informations de diagnostic en mode Internet Explorer sous l’onglet Compatibilité Microsoft Edge. Pour ouvrir cet onglet, accédez à *edge://compat/iediagnostic*. Cette page peut afficher les messages de diagnostic. Cette page fournit également des informations de configuration pour les catégories suivantes :

- **Vérifier la clé de Registre**. (S’affiche uniquement si la vérification échoue.) Vérifie si l’intégration d’Internet Explorer est correctement configurée dans le registre. Si ce n’est pas le cas, l’utilisateur peut cliquer sur **Réparer** pour résoudre le problème.
- **Mode Internet Explorer**. Affiche la version de l’API utilisée, en fonction de la configuration et du système d’exploitation. En cas de problème, l’utilisateur peut être invité à installer un **Windows Update**.
- **Paramètre Mode Internet Explorer**. Indique si le mode Internet Explorer est activé et comment il est configuré.
- **Ligne de commande**. Affiche la chaîne de ligne de commande et les commutateurs utilisés pour démarrer Microsoft Edge.
- **Paramètres de stratégie de groupe**. Indique si le mode IE est configuré à l’aide de stratégies de groupe et quelles stratégies sont appliquées.

### <a name="error-message-to-open-this-page-in-internet-explorer-mode-reinstall-microsoft-edge-with-administrator-privileges"></a>Message d’erreur : « Pour ouvrir cette page en mode Internet Explorer, réinstallez Microsoft Edge avec des privilèges d’administrateur. »

Vous pouvez rencontrer cette erreur si vous n’avez pas toutes les mises à jour Windows requises. Consultez les conditions requises listées dans [À propos du mode IE](./edge-ie-mode.md) pour connaître les versions requises de Windows et Microsoft Edge.

Si vous avez déjà installé toutes les mises à jour Windows requises, vous pouvez rencontrer cette erreur dans les cas suivants :

- Vous utilisez le canal Canari, qui est installé par défaut au niveau de l’utilisateur.
- Vous utilisez le canal Stable, Bêta ou Dev, mais lorsque vous êtes invité à une élévation lors de l’installation, l’élévation est annulée. Lorsque vous annulez l’invite d’élévation, l’installation se poursuit au niveau de l’utilisateur.
- Internet Explorer 11 a été désactivé dans les fonctionnalités Windows.

Solutions possibles :

- Exécutez le programme d’installation de n’importe quel canal au niveau du système : `installer.exe --system-level`.
- Activer Internet Explorer 11 dans les fonctionnalités de Windows.

Pour vérifier si Microsoft Edge est installé au niveau du système, tapez « edge://version » dans la barre d’adresse Microsoft Edge. Le chemin d’accès de l’Exécutable montre un chemin qui commence par *C:\Program Files*, qui indique une installation du système. Si le chemin d’accès de l’Exécutable commence par *C:\Users\*, désinstallez, puis réinstallez Microsoft Edge avec des privilèges d’administrateur.

### <a name="error-message-to-open-this-page-in-ie-mode-try-restarting-microsoft-edge"></a>Message d’erreur : « Pour ouvrir cette page en mode Internet Explorer, essayez de redémarrer Microsoft Edge ».

Cette erreur peut apparaître en cas d’erreur inattendue dans Internet Explorer. Le redémarrage de Microsoft Edge résout généralement ce problème.

### <a name="error-message-turn-off-remote-debugging-to-open-this-site-in-ie-mode-otherwise-it-might-not-work-as-expected"></a>Message d’erreur : « Désactiver le débogage à distance pour ouvrir ce site en mode Internet Explorer, sinon il risque de ne pas fonctionner comme prévu ».

Vous pouvez rencontrer cette erreur si vous procédez au débogage distant et accédez à une page Web configurée pour s’exécuter en mode IE. Vous pouvez continuer, mais la page sera affichée à l’aide de Microsoft Edge.

### <a name="error-message-error-could-not-retrieve-emie-site-list"></a>Message d’erreur : « Erreur : La liste des sites EMIE n’a pas pu être récupérée. »

Vous pouvez voir cette erreur sur la page *edge://compat/enterprise* indiquant que le téléchargement de la liste des sites a échoué. À partir de La version 87 de Microsoft Edge, lorsque les cookies sont bloqués pour les demandes tierces à l’aide de la stratégie [BlockThirdPartyCookies,](./microsoft-edge-policies.md#blockthirdpartycookies) l’authentification HTTP est également interdite. Vous pouvez autoriser les cookies pour le domaine spécifique hébergeant votre liste des sites en mode Entreprise à l’aide de la stratégie [CookiesAllowedForURLs](./microsoft-edge-policies.md#cookiesallowedforurls) pour vous assurer que les téléchargements de listes de sites sont réussis.

## <a name="frequently-asked-questions"></a>Forum Aux Questions

### <a name="will-ie-mode-replace-internet-explorer-11"></a>Le mode IE remplace-t-il Internet Explorer 11 ?

Nous nous engageons à ce qu’Internet Explorer reste un navigateur pris en charge, fiable et sécurisé. Internet Explorer reste un composant de Windows et suit le cycle de vie du support du système d’exploitation sur lequel il est installé. Pour plus de détails, consultez [FAQ sur le cycle de vie : Internet Explorer](https://support.microsoft.com/help/17454/). Bien que Microsoft continue à prendre en charge et à mettre à jour Internet Explorer, les fonctionnalités et mises à jour de plateforme les plus récentes seront disponibles uniquement dans Microsoft Edge.

### <a name="can-i-use-open-with-explorer-or-view-in-file-explorer-in-sharepoint-with-ie-mode"></a>Puis-je utiliser « Ouvrir avec l’Explorateur » ou « Afficher dans l’Explorateur de fichiers » dans SharePoint avec le mode IE ?

Oui, si cela fonctionne dans Internet Explorer 11 autonome, cela fonctionnera en mode IE. Cependant, plutôt que d’utiliser l’option Ouvrir avec Explorer, l’approche recommandée de gestion des fichiers et des dossiers en dehors de SharePoint est de [synchroniser vos fichiers SharePoint](https://support.office.com/en-us/article/sync-sharepoint-files-with-the-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88) ou de [déplacer ou copier des fichiers dans SharePoint](https://support.office.com/en-us/article/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc).

### <a name="does-ie-mode-on-microsoft-edge-support-the-nomerge-option-that-was-supported-in-internet-explorer-11"></a>Le mode IE sur Microsoft Edge prend-il en charge l’option *NoMerge* prise en charge dans Internet Explorer 11 ?

Il n’existe pas de ligne de commande explicite dans Microsoft Edge pour mettre en miroir l’option *nomerge*, mais il existe quelques solutions de remplacement recommandées pour offrir ces fonctionnalités.

1. Utiliser les profils dans Microsoft Edge : chaque profil est mappé à une session IE différente pour les pages du mode IE, de sorte qu’il se comporte de la même façon que l’option *NoMerge*.
2. Utilisez la ligne de commande `--user-data-dir=<path>`, mais avec un chemin d’accès différent pour chaque session. Si nécessaire, vous pouvez créer un utilitaire permettant à l’utilisateur d’exécuter et de lancer Microsoft Edge et de modifier le chemin d’accès de la session.

Si aucune des options ci-dessus ne fonctionne pour votre scénario, contactez l’un de nos canaux de commentaires : support Microsoft ou [Forum TechCommunity](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise).

### <a name="can-i-save-links-as-webpages-in-internet-explorer-mode"></a>Est-il possible d’enregistrer les liens sous forme de pages web en mode Internet Explorer ?

Oui, vous pouvez activer l’option Enregistrer la cible sous dans le menu contextuel du mode Internet Explorer dans Microsoft Edge. Pour ce faire, configurez la stratégie de groupe *« Autoriser Enregistrer la cible sous dans le mode Internet Explorer »* située sur *Configuration de l'ordinateur > Modèles d’administration > Composants Windows > Internet Explorer*.
Le mécanisme d’enregistrement fonctionne de la même façon que dans Internet Explorer et si la cible est enregistrée sous forme de fichier HTML, la réouverture du fichier entraîne le rendu de la page dans Microsoft Edge.
 
Notez que cette fonctionnalité nécessite les mises à jour de système d’exploitation minimales suivantes :
- Windows 10, version 2004, Windows Server version 2004, Windows 10, version 20H2 : [KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)
- Windows 10, version 1903, Windows 10, version 1909, Windows Server version 1903 : [KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386)
- Windows 10, version 1809, Windows Server version 1809, Windows Server 2019 : [KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390)
- Windows 10, version 1803 : [KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)
- Windows 10, version 1607 : [KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)
- Windows 10, version 1507 : [KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)


## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [À propos du mode Internet Explorer](./edge-ie-mode.md)
- [Informations supplémentaires sur le mode entreprise](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)