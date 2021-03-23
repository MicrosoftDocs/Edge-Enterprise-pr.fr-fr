---
title: Documentation relative aux stratégies WebView2 Microsoft Edge
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 03/18/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Documentation relative à toutes les stratégies prises en charge par le navigateur MicrosoftEdge pour Windows et Mac
ms.openlocfilehash: 38aac0e4ffd932583ad48a2dd13cf8e93df79e29
ms.sourcegitcommit: 6a3787dead062e4a0860adbc570229974dcaee07
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "11442374"
---
# <a name="microsoft-edge-webview2---policies"></a>Microsoft Edge WebView2 - Politiques

La dernière version de Microsoft Edge WebView2 comprend les politiques suivantes. Vous pouvez utiliser ces politiques pour configurer le fonctionnement de Microsoft Edge WebView2 dans votre organisation.

Pour plus d'informations sur un ensemble supplémentaire de politiques utilisées pour contrôler quand et comment Microsoft Edge WebView2 est mis à jour, consultez la [référence des politiques de mise à jour de Microsoft Edge](microsoft-edge-update-policies.md).

> [!NOTE]
> Cet article concerne MicrosoftEdge version87 ou ultérieure.

## <a name="available-policies"></a>Stratégies disponibles

Ces tableaux répertorient toutes les politiques de groupe disponibles dans cette version de Microsoft Edge WebView2. Utilisez les liens dans le tableau pour obtenir plus de détails sur des stratégies données.

- [Paramètres d'annulation du chargeur](#loader-override-settings)


### [*<a name="loader-override-settings"></a>Paramètres d'annulation du chargeur*](#loader-override-settings-policies)

|Nom de la stratégie|Caption|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Configurer l'emplacement du dossier de l'exécutable du navigateur|
|[ReleaseChannelPreference](#releasechannelpreference)|Définir la préférence de l'ordre de recherche du canal de diffusion|




  ## <a name="loader-override-settings-policies"></a>Politiques d'annulation des paramètres du chargeur

  [Retour au début](#microsoft-edge-webview2---policies)

  ### <a name="browserexecutablefolder"></a>BrowserExecutableFolder

  #### <a name="configure-the-location-of-the-browser-executable-folder"></a>Configurer l'emplacement du dossier de l'exécutable du navigateur

  
  
  #### <a name="supported-versions"></a>Versions prises en charge:

  - Sur Windows depuis la version87 ou versions ultérieures

  #### <a name="description"></a>Description

  Cette politique configure les applications WebView2 pour qu'elles utilisent le runtime WebView2 dans le chemin spécifié. Le dossier doit contenir les fichiers suivants : msedgewebview2.exe, msedge.dll, etc.

Pour définir la valeur du chemin d'accès au dossier, fournissez un nom de valeur et une paire de valeurs. Définissez le nom de la valeur à l'ID du modèle d'utilisateur de l'application ou au nom du fichier exécutable. Vous pouvez utiliser le «*» joker comme nom de valeur à appliquer à toutes les applications.

  #### <a name="supported-features"></a>Fonctionnalités prises en charge:

  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### <a name="data-type"></a>Type de données:

  - Liste composée de chaînes

  #### <a name="windows-information-and-settings"></a>Informations et paramètres Windows

  ##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)

  - Nom unique de GP: BrowserExecutableFolder
  - Nom du GP : Configurer l'emplacement du dossier de l'exécutable du navigateur
  - Parcours GP (Obligatoire) : Modèles d'administration/Microsoft Edge WebView2/Loader Paramètres de remplacement
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier GP ADMX : MSEdgeWebView2.admx

  ##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows

  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur : liste des REG_SZ
  - Type de valeur: liste composée de REG_SZ

  ##### <a name="example-value"></a>Exemple de valeur:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [Retour au début](#microsoft-edge-webview2---policies)

  ### <a name="releasechannelpreference"></a>ReleaseChannelPreference

  #### <a name="set-the-release-channel-search-order-preference"></a>Définir la préférence de l'ordre de recherche du canal de diffusion

  
  
  #### <a name="supported-versions"></a>Versions prises en charge:

  - Sur Windows depuis la version87 ou versions ultérieures

  #### <a name="description"></a>Description

  L'ordre de recherche des chaînes par défaut est le suivant : WebView2 Runtime, Beta, Dev et Canary.

Pour inverser l'ordre de recherche par défaut, réglez cette politique sur 1.

Pour définir la valeur de la préférence de canal de diffusion, fournissez un nom de valeur et une paire de valeurs. Définissez le nom de la valeur à l'ID du modèle d'utilisateur de l'application ou au nom du fichier exécutable. Vous pouvez utiliser le «*» joker comme nom de valeur à appliquer à toutes les applications.

  #### <a name="supported-features"></a>Fonctionnalités prises en charge:

  - Peut être obligatoire: Oui
  - Peut être recommandée: Non
  - Actualisation dynamique de la stratégie: Oui

  #### <a name="data-type"></a>Type de données:

  - Liste composée de chaînes

  #### <a name="windows-information-and-settings"></a>Informations et paramètres Windows

  ##### <a name="group-policy-admx-info"></a>Informations relatives à la stratégie de groupe (ADMX)

  - Nom unique de GP: ReleaseChannelPreference
  - Nom du GP : Définir la préférence de l'ordre de recherche du canal de diffusion
  - Parcours GP (Obligatoire) : Modèles d'administration/Microsoft Edge WebView2/Loader Paramètres de remplacement
  - Chemin d’accès de la stratégie de groupe (recommandé): N/A
  - Nom du fichier GP ADMX : MSEdgeWebView2.admx

  ##### <a name="windows-registry-settings"></a>Paramètres du Registre Windows

  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference
  - Chemin d’accès (recommandé): N/A
  - Nom de la valeur : liste des REG_SZ
  - Type de valeur: liste composée de REG_SZ

  ##### <a name="example-value"></a>Exemple de valeur:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [Retour au début](#microsoft-edge-webview2---policies)


## <a name="see-also"></a>Voir également

- [Configuration de MicrosoftEdge](configure-microsoft-edge.md)
- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Blog sur les bases de la sécurité Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)