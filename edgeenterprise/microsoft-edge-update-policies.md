---
title: Documentation relative aux stratégies Microsoft Edge Update
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 11/12/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentation relative à toutes les stratégies prises en charge par le programme de mise à jour Microsoft Edge
ms.openlocfilehash: 921a95c0a5e80ba08fa745748ffa8b0da714ea7d
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617884"
---
# <a name="microsoft-edge---update-policies"></a>Microsoft Edge - Stratégies de mise à jour

La dernière version de Microsoft Edge comprend les stratégies suivantes que vous pouvez utiliser pour contrôler comment et quand Microsoft Edge est mis à jour.

Pour plus d’informations sur les autres stratégies disponibles dans Microsoft Edge, consultez la [Référence de stratégies du navigateur Microsoft Edge](microsoft-edge-policies.md)
> [!NOTE]
> Cet article concerne Microsoft Edge version 77 ou ultérieure.
## <a name="available-policies"></a>Stratégies disponibles
Ces tableaux répertorient toutes les stratégies de groupe relatives aux mises à jour disponibles dans cette version de Microsoft Edge. Utilisez les liens dans le tableau pour obtenir plus de détails sur des stratégies données.

|&nbsp;|&nbsp;| |**-**|-| |[](#preferences)| |**[Appications](#applications)**|[Préférences](#preferences)| |**[Serveur proxy](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|
### [<a name="applications"></a>Applications](#applications-policies)
|Nom de la stratégie|Caption|
|-|-|
|[InstallDefault](#installdefault)|Autoriser l’installation par défaut|
|[UpdateDefault](#updatedefault)|Remplacer la stratégie de mise à jour par défaut|
|[Install](#install)|Autoriser l’installation (par canal)|
|[Update](#update)|Remplacer la stratégie de mise à jour (par canal)|
|[Allowsxs](#allowsxs)|Autoriser l’expérience de navigateur côte à côte Microsoft Edge|
|[CreateDesktopShortcutDefault](#createdesktopshortcutdefault)|Empêcher la création du Raccourci Bureau lors de l’installation par défaut|
|[CreateDesktopShortcut](#createdesktopshortcut)|Empêcher la création du Raccourci Bureau lors de l’installation (par canal)|
|[RollbackToTargetVersion](#rollbacktotargetversion)|Restaurez la version Cible (par canal)|
|[TargetVersionPrefix](#targetversionprefix)|Remplacement de la version cible (par canal)|

### [<a name="preferences"></a>Préférences](#preferences-policies)
|Nom de la stratégie|Caption|
|-|-|
|[AutoUpdateCheckPeriodMinutes](#autoupdatecheckperiodminutes)|Remplacement de la période de vérification de mise à jour automatique|
|[UpdatesSuppressed](#updatessuppressed)|Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique|

### [<a name="proxy-server"></a>Serveur proxy](#proxy-server-policies)
|Nom de la stratégie|Légende|
|-|-|
|[ProxyMode](#proxymode)|Choisir comment spécifier les paramètres du serveur proxy|
|[ProxyPacUrl](#proxypacurl)|URL d’un fichier proxy. pac|
|[ProxyServer](#proxyserver)|Adresse ou URL du serveur proxy|

### [<a name="microsoft-edge-webview"></a>Affichage web Microsoft Edge](#microsoft-edge-webview-policies)
|Nom de la stratégie|Caption|
|-|-|
|[Installer](#install-webview)|Autoriser l’installation|
|[Mettre à jour/Mise à jour](#update-webview)|Remplacer la stratégie de mise à jour|

## <a name="applications-policies"></a>Stratégies d’applications

[Retour au début](#microsoft-edge---update-policies)
### <a name="installdefault"></a>InstallDefault
#### <a name="allow-installation-default"></a>Autoriser l’installation par défaut
>Microsoft Edge Update 1.2.145.5 et versions ultérieures

#### <a name="description"></a>Description
Vous pouvez spécifier le comportement par défaut de tous les canaux pour autoriser ou bloquer Microsoft Edge sur les appareils liés à un domaine.

Vous pouvez remplacer cette stratégie pour des canaux individuels en spécifiant la stratégie « [Autoriser l’installation](#install) » pour des canaux spécifiques.

Si vous désactivez cette stratégie, l’installation de Microsoft Edge est bloquée. Cela affecte uniquement l’installation du logiciel Microsoft Edge lorsque la stratégie «[Autoriser l’installation](#install)» est définie Non Configurée.

Cette stratégie n’empêche pas Microsoft Edge Update de s’exécuter, ni les utilisateurs d’installer le logiciel Microsoft Edge en utilisant d’autres méthodes.

Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe : InstallDefault
- Nom de la stratégie de groupe : Autoriser l’installation par défaut
- Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Applications
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur : InstallDefault
- Type de valeur : REG_DWORD
##### <a name="example-value"></a>Exemple de valeur :
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


### <a name="updatedefault"></a>UpdateDefault
#### <a name="update-policy-override-default"></a>Remplacer la stratégie de mise à jour par défaut
>Microsoft Edge Update 1.2.145.5 et versions ultérieures

#### <a name="description"></a>Description
Permet de spécifier le comportement par défaut de tous les canaux concernant la façon dont Microsoft Edge Update gère les mises à jour disponibles pour Microsoft Edge. Peut être remplacé pour des canaux individuels en spécifiant la stratégie « [Remplacer la stratégie de mise à jour](#update) » pour ces canaux spécifiques.

  Si vous activez cette stratégie, Microsoft Edge Update gère les mises à jour de Microsoft Edge en fonction de la façon dont vous configurez les options suivantes :
   - Toujours autoriser les mises à jour : les mises à jour sont toujours appliquées lorsqu’elles sont trouvées, soit par une recherche de mise à jour périodique, soit par une recherche de mise à jour manuelle.
   - Mises à jour automatiques en mode silencieux uniquement : les mises à jour sont appliquées uniquement lorsqu’elles sont trouvées par la recherche de mise à jour périodique.
   - Mises à jour manuelles uniquement : les mises à jour sont appliquées uniquement lorsque l’utilisateur exécute une recherche de mise à jour manuelle.
   - Mises à jour désactivées : les mises à jour ne sont jamais appliquées.

  Si vous sélectionnez les mises à jour manuelles, vérifiez régulièrement si des mises à jour sont disponibles à l’aide du mécanisme de mise à jour manuelle de l’application, le cas échéant. Si vous désactivez les mises à jour, recherchez régulièrement les mises à jour et distribuez-les aux utilisateurs.

  Si vous n’activez pas et ne configurez pas cette stratégie, Microsoft Edge Update gère les mises à jour disponibles, comme spécifié par la stratégie « [Remplacer la stratégie de mise à jour](#update) ».

  Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe : UpdateDefault
- Nom de la stratégie de groupe : Remplacer la stratégie de mise à jour par défaut
- Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Applications
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur : UpdateDefault
- Type de valeur : REG_DWORD
##### <a name="example-value"></a>Exemple de valeur :
```
0x00000003
```
[Retour au début](#microsoft-edge---update-policies)


### <a name="install"></a>Install
#### <a name="allow-installation"></a>Autoriser l’installation
>Microsoft Edge Update 1.2.145.5 et versions ultérieures

#### <a name="description"></a>Description
Spécifie si un canal de Microsoft Edge peut être installé sur des appareils liés à un domaine.

  Si vous activez cette stratégie pour un canal, l’installation de Microsoft Edge ne sera pas bloquée.

  Si vous désactivez cette stratégie pour un canal, l’installation de Microsoft Edge sera bloquée.

  Si vous ne configurez pas cette stratégie pour un canal, la configuration de la stratégie «[Autoriser l’installation par défaut](#installdefault)» détermine si les utilisateurs peuvent installer ce canal de Microsoft Edge.

  Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe : Install
- Nom de la stratégie de groupe : Autoriser l’installation
- Chemin de la stratégie de groupe : 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur : 
  - (Stable) : install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta) : install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary) : Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev) : Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Type de valeur : REG_DWORD
##### <a name="example-value"></a>Exemple de valeur :
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


### <a name="update"></a>Update
#### <a name="update-policy-override"></a>Remplacer la stratégie de mise à jour
>Microsoft Edge Update 1.2.145.5 et versions ultérieures

#### <a name="description"></a>Description
Spécifie comment Microsoft Edge Update gère les mises à jour disponibles à partir de Microsoft Edge.

Si vous activez cette stratégie, Microsoft Edge Update gère les mises à jour de Microsoft Edge en fonction de la façon dont vous configurez les options suivantes :
  - Toujours autoriser les mises à jour : les mises à jour sont toujours appliquées lorsqu’elles sont trouvées, soit par une recherche de mise à jour périodique, soit par une recherche de mise à jour manuelle.
  - Mises à jour automatiques en mode silencieux uniquement : les mises à jour sont appliquées uniquement lorsqu’elles sont trouvées par la recherche de mise à jour périodique.
  - Mises à jour manuelles uniquement : les mises à jour sont appliquées uniquement lorsque l’utilisateur exécute une recherche de mise à jour manuelle. (Toutes les applications n’offrent pas une interface pour cette option.)
  - Mises à jour désactivées : les mises à jour ne sont jamais appliquées.

Si vous sélectionnez les mises à jour manuelles, vérifiez régulièrement si des mises à jour sont disponibles à l’aide du mécanisme de mise à jour manuelle de l’application, le cas échéant. Si vous désactivez les mises à jour, recherchez régulièrement les mises à jour et distribuez-les aux utilisateurs.

Si vous n’activez pas et ne configurez pas cette stratégie, Microsoft Edge Update gère les mises à jour disponibles, comme spécifié par la stratégie « [Remplacer la stratégie de mise à jour par défaut](#updatedefault) ».

Si vous souhaitez en savoir plus, consultez [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406).

Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe : Update
- Nom de la stratégie de groupe : Remplacer la stratégie de mise à jour
- Chemin de la stratégie de groupe : 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur : 
  - (Stable) : Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta) : Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary) : Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev) : Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Type de valeur : REG_DWORD
##### <a name="example-value"></a>Exemple de valeur :
```
always allow updates 0x00000001
Automatic silent updates only 0x00000003
manual updates only 0x00000002
updates disabled 0x00000000
```
[Retour au début](#microsoft-edge---update-policies)


### <a name="allowsxs"></a>Allowsxs
#### <a name="allow-microsoft-edge-side-by-side-browser-experience"></a>Autoriser l’expérience de navigateur côte à côte Microsoft Edge
>Microsoft Edge Update 1.2.145.5 et versions ultérieures

#### <a name="description"></a>Description
Cette stratégie permet à un utilisateur d’exécuter Microsoft Edge (HTML Edge) et Microsoft Edge (basé sur Chromium) côte à côte.

Si cette stratégie est définie sur « Non configuré », Microsoft Edge (basée sur Chromium) remplace Microsoft Edge (Edge HTML) après installation du canal stable Microsoft Edge (basé sur Chromium) et des mises à jour de sécurité de novembre 2019.  C’est le même comportement que le paramètre « Désactivé ».

Le paramètre « Désactivé » bloque une expérience côte-à-côte et Microsoft Edge (basée sur Chromium) remplace Microsoft Edge (Edge HTML) après installation du canal stable Microsoft Edge (basé sur Chromium) et des mises à jour de sécurité de novembre 2019.  C’est le même comportement que le paramètre « Non configuré ».

Lorsque cette stratégie est « Activée », Microsoft Edge (basé sur Chromium) et Microsoft Edge (Edge HTML) peuvent s’exécuter côte à côte après l’installation de Microsoft Edge (basé sur Chromium).

Pour que cette stratégie de groupe prenne effet, elle doit être configurée avant l’installation automatique de Microsoft Edge (basé sur Chromium) par Windows Update. Remarque : un utilisateur peut bloquer la mise à jour automatique de Microsoft Edge (basé sur Chromium) à l’aide du kit de ressources de bloqueur Microsoft Edge (basé sur Chromium).
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe : Allowsxs
- Nom de la stratégie de groupe : Autoriser l’expérience de navigateur côte à côte Microsoft Edge
- Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Applications
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur : Allowsxs
- Type de valeur : REG_DWORD
##### <a name="example-value"></a>Exemple de valeur :
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


### <a name="createdesktopshortcutdefault"></a>CreateDesktopShortcutDefault
#### <a name="prevent-desktop-shortcut-creation-upon-install-default"></a>Empêcher la création du Raccourci Bureau lors de l’installation par défaut
>Microsoft Edge Update 1.3.128.0 et versions ultérieures

#### <a name="description"></a>Description
Vous permet de spécifier le comportement par défaut de tous les canaux pour créer un raccourci bureau lorsque Microsoft Edge est installé.

  Si vous activez cette stratégie, un raccourci bureau est créé lors de l’installation de Microsoft Edge.
Si vous désactivez cette stratégie, aucun raccourci bureau n’est créé lors de l’installation de Microsoft Edge.
Si vous ne configurez pas cette stratégie, un raccourci bureau vers Microsoft Edge est créé pendant l’installation.
Si Microsoft Edge est déjà installé, cette stratégie n’a aucun effet.
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de stratégie de groupe : CreateDesktopShortcutDefault
- Nom de stratégie de groupe : empêcher la création du Raccourci Bureau lors de l’installation par défaut
- Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Applications
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de valeur : CreateDesktopShortcutDefault
- Type de valeur : REG_DWORD
##### <a name="example-value"></a>Exemple de valeur :
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


### <a name="createdesktopshortcut"></a>CreateDesktopShortcut
#### <a name="prevent-desktop-shortcut-creation-upon-install"></a>Empêcher la création du Raccourci Bureau lors de l’installation
>Microsoft Edge Update 1.3.128.0 et versions ultérieures

#### <a name="description"></a>Description
Si vous activez cette stratégie, un raccourci bureau est créé lors de l’installation de Microsoft Edge.
Si vous désactivez cette stratégie, aucun raccourci bureau n’est créé lors de l’installation de Microsoft Edge.
Si vous ne configurez pas cette stratégie, un raccourci bureau vers Microsoft Edge est créé pendant l’installation.
Si Microsoft Edge est déjà installé, cette stratégie n’a aucun effet.

  Si vous ne configurez pas cette stratégie pour un canal, la configuration de stratégie « [Empêcher la création de raccourcis clavier lors de l’installation de la configuration de stratégie par défaut](#createdesktopshortcutdefault) » définit la création d’un raccourci lors de l’installation de Microsoft Edge.
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de stratégie de groupe : CreateDesktopShortcut
- Nom de stratégie de groupe : empêcher la création du Raccourci Bureau lors de l’installation
- Chemin de la stratégie de groupe : 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de valeur : 
  - (Stable) : CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Bêta) : CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary) : CreateDesktopShortcut {65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev) : CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Type de valeur : REG_DWORD
##### <a name="example-value"></a>Exemple de valeur :
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


### <a name="rollbacktotargetversion"></a>RollbackToTargetVersion
#### <a name="rollback-to-target-version"></a>Restaurez la version Cible
>Microsoft Edge Update 1.3.133.3 et versions ultérieures

#### <a name="description"></a>Description
Spécifie que Microsoft Edge Update doit restaurer les installations de Microsoft Edge à la version indiquée dans «[Remplacement de la version cible](#targetversionprefix)».

Cette stratégie n’a aucun effet, sauf si «[Remplacement de la version cible](#targetversionprefix)» est défini et «[Remplacement de la stratégie de mise à jour](#update)» est défini à l’un des états d’activation (Toujours autoriser les mises à jour, Mises à jour automatiques silencieuses uniquement, Mises à jour manuelles uniquement).

Si vous désactivez cette stratégie ou si vous ne la configurez pas, les installations dont la version est supérieure à celle spécifiée par «[Remplacement de la version cible](#targetversionprefix)» sont conservées.

Si vous activez cette stratégie, les installations qui ont une version actuelle supérieure à celle spécifiée par «[Remplacement de la version cible](#targetversionprefix)» sont rétrogradées à la version cible.

Nous recommandons aux utilisateurs d’installer la dernière version du navigateur Microsoft Edge afin de profiter de la protection offerte par les dernières mises à jour de sécurité. La restauration à une version antérieure présente des risques d’exposition aux problèmes de sécurité connus. Cette stratégie est destinée à être utilisée comme correctif temporaire pour résoudre les problèmes de mise à jour du navigateur Microsoft Edge.

Avant de restaurer temporairement la version de votre navigateur, nous vous recommandons d’activer la Synchronisation ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) pour tous les utilisateurs de votre organisation. Si vous n’activez pas la Synchronisation, vous risquez de perdre définitivement les données de navigation. L’ utilisation de cette stratégie comporte des risques.

Remarque : Vous pouvez afficher toutes les versions disponibles pour la restauration ici [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).

Cette stratégie s’applique à Microsoft Edge version 86 ou ultérieure.

Si vous souhaitez en savoir plus, consultez [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918).

Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique GP : RollbackToTargetVersion
- Nom GP: Restaurez la version Cible
- Chemin de la stratégie de groupe : 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de valeur : 
  - (Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Type de valeur : REG_DWORD
##### <a name="example-value"></a>Exemple de valeur :
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


### <a name="targetversionprefix"></a>TargetVersionPrefix
#### <a name="target-version-override"></a>Remplacement de la version cible
>Microsoft Edge Update 1.3.119.43 et versions ultérieures

#### <a name="description"></a>Description
Lorsque cette stratégie est activée et que la mise à jour automatique est activée, Microsoft Edge est mis à jour vers la version spécifiée par cette valeur de stratégie.

La valeur de la stratégie doit être une version spécifique de Microsoft Edge, par exemple, 83.0.499.12.

Si la version de Microsoft Edge d’un appareil est plus récente que la valeur spécifiée, Microsoft Edge reste sur la version la plus récente et n’est pas rétrogradé vers la version spécifiée.

Si la version spécifiée n’existe pas ou n’est pas mise en forme de manière correcte, Microsoft Edge reste sur sa version actuelle et ne sera pas mise à jour automatiquement vers les versions ultérieures.

Si vous souhaitez en savoir plus, consultez [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707).

Cette stratégie est disponible uniquement sur les instances Windows qui sont liées au domaine Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de stratégie de groupe : TargetVersionPrefix
- Nom de stratégie de groupe : Remplacement de la version cible
- Chemin de la stratégie de groupe : 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de valeur : 
  - (Stable) : TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta) : TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary) : TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev) : TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Type de valeur : REG_SZ
##### <a name="example-value"></a>Exemple de valeur :
```
83.0.499.12
```
[Retour au début](#microsoft-edge---update-policies)


## <a name="preferences-policies"></a>Stratégies de préférences

[Retour au début](#microsoft-edge---update-policies)
### <a name="autoupdatecheckperiodminutes"></a>AutoUpdateCheckPeriodMinutes
#### <a name="auto-update-check-period-override"></a>Remplacement de la période de vérification de mise à jour automatique
>Microsoft Edge Update 1.2.145.5 et versions ultérieures

#### <a name="description"></a>Description
Si elle est activée, cette stratégie vous permet de définir une valeur pour le nombre minimal de minutes entre les recherches automatiques de mises à jour. Dans le cas contraire, par défaut, la mise à jour automatique recherche les mises à jour toutes les 10 heures.

  Si vous souhaitez désactiver toutes les vérifications de mise à jour automatique, définissez la valeur sur 0 (non recommandé).
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe : AutoUpdateCheckPeriodMinutes
- Nom de la stratégie de groupe : Remplacement de la période de vérification de mise à jour automatique
- Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Preferences
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur : AutoUpdateCheckPeriodMinutes
- Type de valeur : REG_DWORD
##### <a name="example-value"></a>Exemple de valeur :
```
0x00000578
```
[Retour au début](#microsoft-edge---update-policies)


### <a name="updatessuppressed"></a>UpdatesSuppressed
#### <a name="time-period-in-each-day-to-suppress-auto-update-check"></a>Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique
>Microsoft Edge Update 1.3.33.5 et versions ultérieures

#### <a name="description"></a>Description
Si vous activez cette stratégie, les vérifications de mise à jour sont supprimées chaque jour à partir de Heure:Minute pendant une Durée (en minutes). La durée n’est pas affectée par l’heure d’été. Par exemple, si l’heure de début est 22:00 et que la durée est 480 minutes, les mises à jour seront supprimées pendant exactement 8 heures, même si l’heure d’été commence ou se termine pendant cette période.

  Si vous désactivez ou que vous ne configurez pas cette stratégie, les vérifications de mise à jour ne sont pas supprimées pendant une période spécifique.
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe : UpdatesSuppressed
- Nom de la stratégie de groupe : Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique
  - Options { Hour, Minute, Duration }
- Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Preferences
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur : 
  - UpdatesSuppressedDurationMin
  - UpdatesSuppressedStartHour
  - UpdatesSuppressedStartMin
- Type de valeur : REG_DWORD
##### <a name="example-value"></a>Exemple de valeur :
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[Retour au début](#microsoft-edge---update-policies)


## <a name="proxy-server-policies"></a>Stratégies de serveur proxy

[Retour au début](#microsoft-edge---update-policies)
### <a name="proxymode"></a>ProxyMode
#### <a name="choose-how-to-specify-proxy-server-settings"></a>Choisir comment spécifier les paramètres du serveur proxy
>Microsoft Edge Update 1.3.21.81 et versions ultérieures

#### <a name="description"></a>Description
Permet de spécifier les paramètres de serveur proxy qui sont utilisés par Microsoft Edge Update.

  Si vous activez cette stratégie, vous pouvez choisir l’une des options de serveur proxy suivantes :
   - Si vous choisissez de ne jamais utiliser un serveur proxy et de toujours vous connecter directement, toutes les autres options sont ignorées.
   - Si vous choisissez d’utiliser les paramètres de proxy système ou de détection automatique du serveur proxy, toutes les autres options sont ignorées.
   - Si vous choisissez le mode de serveur proxy fixe, vous pouvez spécifier d’autres options dans la stratégie [« Adresse ou URL du serveur proxy »](#proxyserver).
   - Si vous choisissez d’utiliser un script de proxy .pac, vous devez spécifier l’URL du script dans la stratégie [« URL d’un fichier proxy. pac »](#proxypacurl).

  Si vous activez cette stratégie, les utilisateurs de votre organisation ne peuvent pas modifier les paramètres du proxy dans Microsoft Edge Update.

  Si vous désactivez ou que vous ne configurez pas cette stratégie, aucun paramètre de serveur proxy n’est configuré, mais les utilisateurs de votre organisation peuvent choisir leurs propres paramètres de proxy pour Microsoft Edge Update.
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe : ProxyMode
- Nom de la stratégie de groupe : Choisir comment spécifier les paramètres du serveur proxy
- Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Proxy Server
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur : ProxyMode
- Type de valeur : REG_SZ
##### <a name="example-value"></a>Exemple de valeur :
```
fixed_servers
```
[Retour au début](#microsoft-edge---update-policies)


### <a name="proxypacurl"></a>ProxyPacUrl
#### <a name="url-to-a-proxy-pac-file"></a>URL d’un fichier proxy. pac
>Microsoft Edge Update 1.3.21.81 et versions ultérieures

#### <a name="description"></a>Description
Permet de spécifier une URL pour un fichier de configuration automatique de proxy (PAC).

  Si vous activez cette stratégie, vous pouvez spécifier une URL pour un fichier PAC pour automatiser la façon dont Microsoft Edge Update sélectionne le serveur proxy approprié pour l’extraction d’un site web particulier.

  Cette stratégie est appliquée uniquement si vous avez spécifié des paramètres de proxy manuels dans la stratégie « [Choisir comment spécifier les paramètres du serveur proxy](#proxymode) ».

  Ne configurez pas cette stratégie si vous avez sélectionné un paramètre de proxy autre que manuel dans la stratégie « [Choisir comment spécifier les paramètres du serveur proxy](#proxymode) ».
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe : ProxyPacUrl
- Nom de la stratégie de groupe : URL d’un fichier proxy. pac
- Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Proxy Server
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur : ProxyPacUrl
- Type de valeur : REG_SZ
##### <a name="example-value"></a>Exemple de valeur :
```
https://www.microsoft.com
```
[Retour au début](#microsoft-edge---update-policies)


### <a name="proxyserver"></a>ProxyServer
#### <a name="address-or-url-of-proxy-server"></a>Adresse ou URL du serveur proxy
>Microsoft Edge Update 1.3.21.81 et versions ultérieures

#### <a name="description"></a>Description
Permet de spécifier l’URL du serveur proxy que Microsoft Edge Update doit utiliser.

  Si vous activez cette stratégie, vous pouvez définir l’URL de serveur proxy utilisée par Microsoft Edge Update dans votre organisation.

  Cette stratégie est appliquée uniquement si vous avez sélectionné plusieurs paramètres de proxy manuels dans la stratégie « [Choisir comment spécifier les paramètres du serveur proxy](#proxymode) ».

  Ne configurez pas cette stratégie si vous avez sélectionné un paramètre de proxy autre que manuel dans la stratégie « [Choisir comment spécifier les paramètres du serveur proxy](#proxymode) ».
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe : ProxyServer
- Nom de la stratégie de groupe : Adresse ou URL du serveur proxy
- Chemin de la stratégie de groupe : Administrative Templates/Microsoft Edge Update/Proxy Server
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur : ProxyServer
- Type de valeur : REG_SZ
##### <a name="example-value"></a>Exemple de valeur :
```
https://www.microsoft.com
```
[Retour au début](#microsoft-edge---update-policies)


## <a name="microsoft-edge-webview-policies"></a>Stratégies d’affichage web Microsoft Edge

[Retour au début](#microsoft-edge---update-policies)
### <a name="install-webview"></a>Installation (Affichage web)
#### <a name="allow-installation"></a>Autoriser l’installation
>Microsoft Edge Update 1.3.127.1 et versions ultérieures

#### <a name="description"></a>Description
Vous permet de spécifier si un affichage web de Microsoft Edge peut être installé à l’aide de Microsoft Edge Update.

  - Si vous activez cette stratégie, les utilisateurs peuvent installer l’affichage web de Microsoft Edge via Microsoft Edge Update.
  - Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas installer l’affichage web de Microsoft Edge via Microsoft Edge Update.
  - Si vous ne configurez pas cette stratégie, la configuration de la stratégie «[Autoriser l’installation par défaut](#installdefault)» détermine si les utilisateurs peuvent installer l’Affichage web Microsoft Edge via Microsoft Edge Update.
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe : Install
- Nom de la stratégie de groupe : Autoriser l’installation
- Chemin d’accès de la stratégie de groupe : Modèles administratifs/Microsoft Edge Update/Applications/Affichage web Microsoft Edge
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de valeur : 
  - Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
- Type de valeur : REG_DWORD
##### <a name="example-value"></a>Exemple de valeur :
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


### <a name="update-webview"></a>Mise à jour (Affichage web)
#### <a name="update-policy-override"></a>Remplacer la stratégie de mise à jour
>Microsoft Edge Update 1.3.127.1 et versions ultérieures

#### <a name="description"></a>Description
Vous permet de spécifier si les mises à jour automatiques sont activées pour l’affichage web de Microsoft Edge. L’affichage web de Microsoft Edge est un composant utilisé par les applications pour afficher du contenu web.
Les mises à jour automatiques sont activées par défaut. La désactivation des mises à jour automatiques pour l’affichage web de Microsoft Edge peut entraîner des problèmes de compatibilité avec les applications qui dépendent de ce composant.

  Si vous activez cette stratégie, Microsoft Edge Update gère les mises à jour de l’affichage web de Microsoft Edge en fonction de la façon dont vous configurez les options suivantes :
  - Toujours autoriser les mises à jour : les mises à jour sont téléchargées et appliquées automatiquement
  - Mises à jour désactivées : les mises à jour ne sont jamais téléchargées ou appliquées.

  Si vous n’activez pas cette stratégie, les mises à jour sont automatiquement téléchargées et appliquées.
#### <a name="windows-information-and-settings"></a>Informations et paramètres Windows
##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe : Update
- Nom de la stratégie de groupe : Remplacer la stratégie de mise à jour
- Chemin d’accès de la stratégie de groupe : Modèles administratifs/Microsoft Edge Update/Applications/Affichage web Microsoft Edge
- Nom du fichier GP ADMX: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows
- Chemin d’accès : HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de valeur : 
  - Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
- Type de valeur : REG_DWORD
##### <a name="example-value"></a>Exemple de valeur :
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


## <a name="see-also"></a>Voir également
  - [Configuration de Microsoft Edge](configure-microsoft-edge.md)
  - [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
