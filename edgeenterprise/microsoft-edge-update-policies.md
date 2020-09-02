---
title: Documentation relative aux stratégies Microsoft Edge Update
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 06/10/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentation relative à toutes les stratégies prises en charge par le programme de mise à jour MicrosoftEdge
ms.openlocfilehash: d772d8dd6f60b89e9bd12a77b740e5fad699756a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979782"
---
# Microsoft Edge - Stratégies de mise à jour
La dernière version de MicrosoftEdge comprend les stratégies suivantes que vous pouvez utiliser pour contrôler comment et quand MicrosoftEdge est mis à jour.

           
Pour plus d’informations sur les autres stratégies disponibles dans MicrosoftEdge, consultez la [Référence de stratégies du navigateur MicrosoftEdge](microsoft-edge-policies.md)
> [!NOTE]
> Cet article concerne MicrosoftEdge version77 ou ultérieure.

## Stratégies disponibles
Ces tableaux répertorient toutes les stratégies de groupe relatives aux mises à jour disponibles dans cette version de MicrosoftEdge. Utilisez les liens dans le tableau pour obtenir plus de détails sur des stratégies données.

|||
|-|-|
|[Applications](#applications)|[Préférences](#preferences)|
|[Serveur proxy](#proxy-server)||

### [Applications](#applications-policies)
|Nom de la stratégie|Caption|
|-|-|
|[InstallDefault](#installdefault)|Autoriser l’installation par défaut|
|[UpdateDefault](#updatedefault)|Remplacer la stratégie de mise à jour par défaut|
|[Installer](#install)|Autoriser l’installation (par canal)|
|[Update](#update)|Remplacer la stratégie de mise à jour (par canal)|
|[Allowsxs](#allowsxs)|Autoriser l’expérience de navigateur côte à côte MicrosoftEdge|
|[CreateDesktopShortcutDefault](#createdesktopshortcutdefault)|Empêcher la création du Raccourci Bureau lors de l’installation par défaut|
|[CreateDesktopShortcut](#createdesktopshortcut)|Empêcher la création du Raccourci Bureau lors de l’installation (par canal)|
|[TargetVersionPrefix](#targetversionprefix)|Remplacement de la version cible (par canal)|

### [Préférences](#preferences-policies)
|Nom de la stratégie|Caption|
|-|-|
|[AutoUpdateCheckPeriodMinutes](#autoupdatecheckperiodminutes)|Remplacement de la période de vérification de mise à jour automatique|
|[UpdatesSuppressed](#updatessuppressed)|Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique|

### [Serveur proxy](#proxy-server-policies)
|Nom de la stratégie|Légende|
|-|-|
|[ProxyMode](#proxymode)|Choisir comment spécifier les paramètres du serveur proxy|
|[ProxyPacUrl](#proxypacurl)|URL d’un fichier proxy. pac|
|[ProxyServer](#proxyserver)|Adresse ou URL du serveur proxy|

                 
      
  
             
            
                  

## Stratégies d’applications

[Retour au début](#microsoft-edge---update-policies)
### InstallDefault
#### Autoriser l’installation par défaut
>MicrosoftEdge Update1.2.145.5 et versions ultérieures

#### Description
Vous pouvez spécifier le comportement par défaut de tous les canaux pour autoriser ou bloquer les mises à jour Microsoft Edge lorsque Microsoft Edge Update est utilisé.

Vous pouvez remplacer cette stratégie pour des canaux individuels en spécifiant la stratégie «[Autoriser l’installation](#install)» pour des canaux spécifiques.

Si vous désactivez cette stratégie, l’installation de MicrosoftEdge via MicrosoftEdge Update est bloquée. Ceci affecte l’installation du logiciel MicrosoftEdge uniquement lorsque les utilisateurs exécutent MicrosoftEdge Update et s’ils n’ont pas configuré la stratégie «[Autoriser l’installation](#install)».

Cette stratégie n’empêche pas MicrosoftEdge Update de s’exécuter, ni les utilisateurs d’installer le logiciel MicrosoftEdge en utilisant d’autres méthodes.
#### Informations et paramètres Windows
##### Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe: InstallDefault
- Nom de la stratégie de groupe: Autoriser l’installation par défaut
- Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Applications
- Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx
##### Paramètres du Registre Windows
- Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur: InstallDefault
- Type de valeur: REG_DWORD
##### Exemple de valeur:
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


### UpdateDefault
#### Remplacer la stratégie de mise à jour par défaut
>MicrosoftEdge Update1.2.145.5 et versions ultérieures

#### Description
Permet de spécifier le comportement par défaut de tous les canaux concernant la façon dont MicrosoftEdge Update gère les mises à jour disponibles pour MicrosoftEdge. Peut être remplacé pour des canaux individuels en spécifiant la stratégie «[Remplacer la stratégie de mise à jour](#update)» pour ces canaux spécifiques.

  Si vous activez cette stratégie, MicrosoftEdge Update gère les mises à jour de MicrosoftEdge en fonction de la façon dont vous configurez les options suivantes:
   - Toujours autoriser les mises à jour: les mises à jour sont toujours appliquées lorsqu’elles sont trouvées, soit par une recherche de mise à jour périodique, soit par une recherche de mise à jour manuelle.
   - Mises à jour automatiques en mode silencieux uniquement: les mises à jour sont appliquées uniquement lorsqu’elles sont trouvées par la recherche de mise à jour périodique.
   - Mises à jour manuelles uniquement: les mises à jour sont appliquées uniquement lorsque l’utilisateur exécute une recherche de mise à jour manuelle.
   - Mises à jour désactivées: les mises à jour ne sont jamais appliquées.

  Si vous sélectionnez les mises à jour manuelles, vérifiez régulièrement si des mises à jour sont disponibles à l’aide du mécanisme de mise à jour manuelle de l’application, le cas échéant. Si vous désactivez les mises à jour, recherchez régulièrement les mises à jour et distribuez-les aux utilisateurs.

  Si vous n’activez pas et ne configurez pas cette stratégie, MicrosoftEdge Update gère les mises à jour disponibles, comme spécifié par la stratégie «[Remplacer la stratégie de mise à jour](#update)».
#### Informations et paramètres Windows
##### Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe: UpdateDefault
- Nom de la stratégie de groupe: Remplacer la stratégie de mise à jour par défaut
- Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Applications
- Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx
##### Paramètres du Registre Windows
- Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur: UpdateDefault
- Type de valeur: REG_DWORD
##### Exemple de valeur:
```
0x00000003
```
[Retour au début](#microsoft-edge---update-policies)


### Install
#### Autoriser l’installation
>MicrosoftEdge Update1.2.145.5 et versions ultérieures

#### Description
Spécifie si un canal de MicrosoftEdge peut être installé à l’aide de MicrosoftEdge Update.

  Si vous activez cette stratégie pour un canal, les utilisateurs peuvent installer ce canal de MicrosoftEdge via MicrosoftEdge Update.

  Si vous désactivez cette stratégie pour un canal, les utilisateurs ne peuvent pas installer ce canal de MicrosoftEdge via MicrosoftEdge Update.

  Si vous ne configurez pas cette stratégie pour un canal, la configuration de la stratégie «[Autoriser l’installation par défaut](#installdefault)» détermine si les utilisateurs peuvent installer ce canal de MicrosoftEdge via MicrosoftEdge Update.
#### Informations et paramètres Windows
##### Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe: Install
- Nom de la stratégie de groupe: Autoriser l’installation
- Chemin de la stratégie de groupe: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx
##### Paramètres du Registre Windows
- Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur: 
  - (Stable): install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Type de valeur: REG_DWORD
##### Exemple de valeur:
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


### Update
#### Remplacer la stratégie de mise à jour
>MicrosoftEdge Update1.2.145.5 et versions ultérieures

#### Description
Spécifie comment MicrosoftEdge Update gère les mises à jour disponibles à partir de MicrosoftEdge.

  Si vous activez cette stratégie, MicrosoftEdge Update gère les mises à jour de MicrosoftEdge en fonction de la façon dont vous configurez les options suivantes:
   - Toujours autoriser les mises à jour: les mises à jour sont toujours appliquées lorsqu’elles sont trouvées, soit par une recherche de mise à jour périodique, soit par une recherche de mise à jour manuelle.
   - Mises à jour automatiques en mode silencieux uniquement: les mises à jour sont appliquées uniquement lorsqu’elles sont trouvées par la recherche de mise à jour périodique.
   - Mises à jour manuelles uniquement: les mises à jour sont appliquées uniquement lorsque l’utilisateur exécute une recherche de mise à jour manuelle. (Toutes les applications n’offrent pas une interface pour cette option.)
   - Mises à jour désactivées: les mises à jour ne sont jamais appliquées.

  Si vous sélectionnez les mises à jour manuelles, vérifiez régulièrement si des mises à jour sont disponibles à l’aide du mécanisme de mise à jour manuelle de l’application, le cas échéant. Si vous désactivez les mises à jour, recherchez régulièrement les mises à jour et distribuez-les aux utilisateurs.

  Si vous n’activez pas et ne configurez pas cette stratégie, MicrosoftEdge Update gère les mises à jour disponibles, comme spécifié par la stratégie «[Remplacer la stratégie de mise à jour par défaut](#updatedefault)».
#### Informations et paramètres Windows
##### Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe: Update
- Nom de la stratégie de groupe: Remplacer la stratégie de mise à jour
- Chemin de la stratégie de groupe: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx
##### Paramètres du Registre Windows
- Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur: 
  - (Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Type de valeur: REG_DWORD
##### Exemple de valeur:
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


### Allowsxs
#### Autoriser l’expérience de navigateur côte à côte MicrosoftEdge
>MicrosoftEdge Update1.2.145.5 et versions ultérieures

#### Description
Cette stratégie permet à un utilisateur d’exécuter MicrosoftEdge (HTML Edge) et MicrosoftEdge (basé sur Chromium) côte à côte.

Si cette stratégie est définie sur «Non configuré», MicrosoftEdge (basée sur Chromium) remplace MicrosoftEdge (Edge HTML) après installation du canal stable MicrosoftEdge (basé sur Chromium) et des mises à jour de sécurité de novembre2019.  C’est le même comportement que le paramètre «Désactivé».

Le paramètre «Désactivé» bloque une expérience côte-à-côte et MicrosoftEdge (basée sur Chromium) remplace MicrosoftEdge (Edge HTML) après installation du canal stable MicrosoftEdge (basé sur Chromium) et des mises à jour de sécurité de novembre2019.  C’est le même comportement que le paramètre «Non configuré».

Lorsque cette stratégie est «Activée», MicrosoftEdge (basé sur Chromium) et MicrosoftEdge (Edge HTML) peuvent s’exécuter côte à côte après l’installation de MicrosoftEdge (basé sur Chromium).

Pour que cette stratégie de groupe prenne effet, elle doit être configurée avant l’installation automatique de MicrosoftEdge (basé sur Chromium) par Windows Update. Remarque: un utilisateur peut bloquer la mise à jour automatique de MicrosoftEdge (basé sur Chromium) à l’aide du kit de ressources de bloqueur MicrosoftEdge (basé sur Chromium).
#### Informations et paramètres Windows
##### Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe: Allowsxs
- Nom de la stratégie de groupe: Autoriser l’expérience de navigateur côte à côte MicrosoftEdge
- Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Applications
- Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx
##### Paramètres du Registre Windows
- Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur: Allowsxs
- Type de valeur: REG_DWORD
##### Exemple de valeur:
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


### CreateDesktopShortcutDefault
#### Empêcher la création du Raccourci Bureau lors de l’installation par défaut
>MicrosoftEdge Update1.3.128.0 et versions ultérieures

#### Description
Vous permet de spécifier le comportement par défaut de tous les canaux pour créer un raccourci bureau lorsque Microsoft Edge est installé.

  Si vous activez cette stratégie, un raccourci bureau est créé lors de l’installation de Microsoft Edge.
Si vous désactivez cette stratégie, aucun raccourci bureau n’est créé lors de l’installation de Microsoft Edge.
Si vous ne configurez pas cette stratégie, un raccourci bureau vers Microsoft Edge est créé pendant l’installation.
Si Microsoft Edge est déjà installé, cette stratégie n’a aucun effet.
#### Informations et paramètres Windows
##### Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de stratégie de groupe: CreateDesktopShortcutDefault
- Nom de stratégie de groupe: empêcher la création du Raccourci Bureau lors de l’installation par défaut
- Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Applications
- Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx
##### Paramètres du Registre Windows
- Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de valeur: CreateDesktopShortcutDefault
- Type de valeur: REG_DWORD
##### Exemple de valeur:
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


### CreateDesktopShortcut
#### Empêcher la création du Raccourci Bureau lors de l’installation
>MicrosoftEdge Update1.3.128.0 et versions ultérieures

#### Description
Si vous activez cette stratégie, un raccourci bureau est créé lors de l’installation de Microsoft Edge.
Si vous désactivez cette stratégie, aucun raccourci bureau n’est créé lors de l’installation de Microsoft Edge.
Si vous ne configurez pas cette stratégie, un raccourci bureau vers Microsoft Edge est créé pendant l’installation.
Si Microsoft Edge est déjà installé, cette stratégie n’a aucun effet.

  Si vous ne configurez pas cette stratégie pour un canal, la configuration de stratégie «[Empêcher la création de raccourcis clavier lors de l’installation de la configuration de stratégie par défaut](#createdesktopshortcutdefault)» définit la création d’un raccourci lors de l’installation de Microsoft Edge.
#### Informations et paramètres Windows
##### Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de stratégie de groupe: CreateDesktopShortcut
- Nom de stratégie de groupe: empêcher la création du Raccourci Bureau lors de l’installation
- Chemin de la stratégie de groupe: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx
##### Paramètres du Registre Windows
- Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de valeur: 
  - (Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Bêta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): CreateDesktopShortcut {65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Type de valeur: REG_DWORD
##### Exemple de valeur:
```
0x00000001
```
[Retour au début](#microsoft-edge---update-policies)


### TargetVersionPrefix
#### Remplacement de la version cible
>MicrosoftEdge Update1.3.119.43 et versions ultérieures

#### Description
Lorsque cette stratégie est activée et que la mise à jour automatique est activée, Microsoft Edge est mis à jour vers la version spécifiée par cette valeur de stratégie.

La valeur de la stratégie doit être une version spécifique de Microsoft Edge, par exemple, 83.0.499.12.

Si la version de Microsoft Edge d’un appareil est plus récente que la valeur spécifiée, Microsoft Edge reste sur la version la plus récente et n’est pas rétrogradé vers la version spécifiée.

Si la version spécifiée n’existe pas ou n’est pas mise en forme de manière correcte, Microsoft Edge reste sur sa version actuelle et ne sera pas mise à jour automatiquement vers les versions ultérieures.
#### Informations et paramètres Windows
##### Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de stratégie de groupe: TargetVersionPrefix
- Nom de stratégie de groupe: Remplacement de la version cible
- Chemin de la stratégie de groupe: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx
##### Paramètres du Registre Windows
- Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de valeur: 
  - (Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Type de valeur: REG_SZ
##### Exemple de valeur:
```
83.0.499.12
```
[Retour au début](#microsoft-edge---update-policies)


## Stratégies de préférences

[Retour au début](#microsoft-edge---update-policies)
### AutoUpdateCheckPeriodMinutes
#### Remplacement de la période de vérification de mise à jour automatique
>MicrosoftEdge Update1.2.145.5 et versions ultérieures

#### Description
Si elle est activée, cette stratégie vous permet de définir une valeur pour le nombre minimal de minutes entre les recherches automatiques de mises à jour. Dans le cas contraire, par défaut, la mise à jour automatique recherche les mises à jour toutes les 10heures.

  Si vous souhaitez désactiver toutes les vérifications de mise à jour automatique, définissez la valeur sur 0 (non recommandé).
#### Informations et paramètres Windows
##### Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe: AutoUpdateCheckPeriodMinutes
- Nom de la stratégie de groupe: Remplacement de la période de vérification de mise à jour automatique
- Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Preferences
- Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx
##### Paramètres du Registre Windows
- Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur: AutoUpdateCheckPeriodMinutes
- Type de valeur: REG_DWORD
##### Exemple de valeur:
```
0x00000578
```
[Retour au début](#microsoft-edge---update-policies)


### UpdatesSuppressed
#### Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique
>MicrosoftEdge Update1.3.33.5 et versions ultérieures

#### Description
Si vous activez cette stratégie, les vérifications de mise à jour sont supprimées chaque jour à partir de Heure:Minute pendant une Durée (en minutes). La durée n’est pas affectée par l’heure d’été. Par exemple, si l’heure de début est 22:00 et que la durée est 480minutes, les mises à jour seront supprimées pendant exactement 8heures, même si l’heure d’été commence ou se termine pendant cette période.

  Si vous désactivez ou que vous ne configurez pas cette stratégie, les vérifications de mise à jour ne sont pas supprimées pendant une période spécifique.
#### Informations et paramètres Windows
##### Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe: UpdatesSuppressed
- Nom de la stratégie de groupe: Période quotidienne pendant laquelle supprimer la vérification de mise à jour automatique
  - Options { Hour, Minute, Duration }
- Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Preferences
- Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx
##### Paramètres du Registre Windows
- Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur: 
  - UpdatesSuppressedDurationMin
  - UpdatesSuppressedStartHour
  - UpdatesSuppressedStartMin
- Type de valeur: REG_DWORD
##### Exemple de valeur:
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[Retour au début](#microsoft-edge---update-policies)


## Stratégies de serveur proxy
  
  

[Retour au début](#microsoft-edge---update-policies)
### ProxyMode
#### Choisir comment spécifier les paramètres du serveur proxy
>MicrosoftEdge Update1.3.21.81 et versions ultérieures

#### Description
Permet de spécifier les paramètres de serveur proxy qui sont utilisés par MicrosoftEdge Update.

  Si vous activez cette stratégie, vous pouvez choisir l’une des options de serveur proxy suivantes:
   - Si vous choisissez de ne jamais utiliser un serveur proxy et de toujours vous connecter directement, toutes les autres options sont ignorées.
   - Si vous choisissez d’utiliser les paramètres de proxy système ou de détection automatique du serveur proxy, toutes les autres options sont ignorées.
   - Si vous choisissez le mode de serveur proxy fixe, vous pouvez spécifier d’autres options dans la stratégie [«Adresse ou URL du serveur proxy»](#proxyserver).
   - Si vous choisissez d’utiliser un script de proxy .pac, vous devez spécifier l’URL du script dans la stratégie [«URL d’un fichier proxy. pac»](#proxypacurl).

  Si vous activez cette stratégie, les utilisateurs de votre organisation ne peuvent pas modifier les paramètres du proxy dans MicrosoftEdge Update.

  Si vous désactivez ou que vous ne configurez pas cette stratégie, aucun paramètre de serveur proxy n’est configuré, mais les utilisateurs de votre organisation peuvent choisir leurs propres paramètres de proxy pour MicrosoftEdge Update.
#### Informations et paramètres Windows
##### Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe: ProxyMode
- Nom de la stratégie de groupe: Choisir comment spécifier les paramètres du serveur proxy
- Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Proxy Server
- Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx
##### Paramètres du Registre Windows
- Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur: ProxyMode
- Type de valeur: REG_SZ
##### Exemple de valeur:
```
fixed_servers
```
[Retour au début](#microsoft-edge---update-policies)


### ProxyPacUrl
#### URL d’un fichier proxy. pac
>MicrosoftEdge Update1.3.21.81 et versions ultérieures

#### Description
Permet de spécifier une URL pour un fichier de configuration automatique de proxy (PAC).

  Si vous activez cette stratégie, vous pouvez spécifier une URL pour un fichier PAC pour automatiser la façon dont MicrosoftEdge Update sélectionne le serveur proxy approprié pour l’extraction d’un site web particulier.

  Cette stratégie est appliquée uniquement si vous avez spécifié des paramètres de proxy manuels dans la stratégie «[Choisir comment spécifier les paramètres du serveur proxy](#proxymode)».

  Ne configurez pas cette stratégie si vous avez sélectionné un paramètre de proxy autre que manuel dans la stratégie «[Choisir comment spécifier les paramètres du serveur proxy](#proxymode)».
#### Informations et paramètres Windows
##### Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe: ProxyPacUrl
- Nom de la stratégie de groupe: URL d’un fichier proxy. pac
- Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Proxy Server
- Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx
##### Paramètres du Registre Windows
- Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur: ProxyPacUrl
- Type de valeur: REG_SZ
##### Exemple de valeur:
```
https://www.microsoft.com
```
[Retour au début](#microsoft-edge---update-policies)


### ProxyServer
#### Adresse ou URL du serveur proxy
>MicrosoftEdge Update1.3.21.81 et versions ultérieures

#### Description
Permet de spécifier l’URL du serveur proxy que MicrosoftEdge Update doit utiliser.

  Si vous activez cette stratégie, vous pouvez définir l’URL de serveur proxy utilisée par MicrosoftEdge Update dans votre organisation.

  Cette stratégie est appliquée uniquement si vous avez sélectionné plusieurs paramètres de proxy manuels dans la stratégie «[Choisir comment spécifier les paramètres du serveur proxy](#proxymode)».

  Ne configurez pas cette stratégie si vous avez sélectionné un paramètre de proxy autre que manuel dans la stratégie «[Choisir comment spécifier les paramètres du serveur proxy](#proxymode)».
#### Informations et paramètres Windows
##### Informations relatives à la stratégie de groupe (ADMX)
- Nom unique de la stratégie de groupe: ProxyServer
- Nom de la stratégie de groupe: Adresse ou URL du serveur proxy
- Chemin de la stratégie de groupe: Administrative Templates/Microsoft Edge Update/Proxy Server
- Nom du fichier ADMX de la stratégie de groupe: edgeupdate.admx
##### Paramètres du Registre Windows
- Chemin d’accès: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Nom de la valeur: ProxyServer
- Type de valeur: REG_SZ
##### Exemple de valeur:
```
https://www.microsoft.com
```
[Retour au début](#microsoft-edge---update-policies)


## Voir également
  - [Configuration de MicrosoftEdge](configure-microsoft-edge.md)
  - [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
