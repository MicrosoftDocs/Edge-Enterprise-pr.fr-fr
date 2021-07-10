---
title: Guide détaillé de la stratégie ExtensionSettings
ms.author: aspoddar
author: dan-wesley
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Guide de référence détaillé pour la configuration des extensions Microsoft Edge à l’aide de la stratégie ExtensionSettings.
ms.openlocfilehash: 3acd798be6b2b56761991d8adaf014ae614a3fd4
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641320"
---
# <a name="detailed-guide-to-the-extensionsettings-policy"></a>Guide détaillé de la stratégie ExtensionSettings

Microsoft Edge offre plusieurs façons de gérer les extensions. Une manière courante consiste à définir plusieurs stratégies à un seul endroit avec une chaîne JSON dans l’Éditeur de stratégie de groupe Windows ou dans le Registre Windows à l’aide de la stratégie [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings).

> [!NOTE]
> Cet article concerne Microsoft Edge version 77 ou ultérieure.

## <a name="before-you-begin"></a>Avant de commencer

Vous décidez si vous souhaitez définir tous les paramètres de gestion des extensions ici ou définir ces contrôles par le biais d’autres stratégies.
  
La stratégie ExtensionSettings peut avoir la place d’autres stratégies que vous avez définies ailleurs dans la stratégie de groupe, notamment les stratégies suivantes :

- [ExtensionAllowedTypes](/DeployEdge/microsoft-edge-policies#extensionallowedtypes)
- [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist)
- [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ExtensionInstallSources](/DeployEdge/microsoft-edge-policies#extensioninstallsources)
- [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallsources)

## <a name="extensionsettings-policy-fields"></a>Champs de stratégie ExtensionSettings

Cette stratégie peut contrôler les paramètres tels que l’URL de mise à jour, l’emplacement à partir duquel l’extension sera téléchargée pour l’installation initiale et les autorisations bloquées, ou les autorisations qui ne sont pas autorisées à s’exécuter. Les champs de stratégie disponibles sont décrits dans le tableau suivant.

| &nbsp; | Description |
|--|--|
| **allowed_types** | Peut uniquement être utilisé pour configurer la configuration par défaut, *. Spécifie les types d’application ou d’extension que les utilisateurs sont autorisés à installer sur Microsoft Edge. La valeur est une liste de chaînes, chacune devant être l’un des types suivants : « extension », « thème », « user_script » et « hosted_app »   |
| **blocked_install_message**| Si vous bloquez l’installation de certaines extensions par les utilisateurs, vous pouvez spécifier un message personnalisé à afficher dans le navigateur si les utilisateurs tentent de les installer.<br>Ajoutez du texte au message d’erreur générique qui s’affiche sur le site web des modules complémentaires Microsoft Edge. Par exemple, vous pouvez indiquer aux utilisateurs comment contacter le service informatique ou pourquoi une extension particulière n’est pas disponible. Le message peut contenir jusqu’à 1 000 caractères.   |
|**blocked_permissions**  | Empêche les utilisateurs d’installer et d’exécuter des extensions qui demandent certaines autorisations d’API que votre organisation n’autorise pas. Par exemple, vous pouvez bloquer les extensions qui accèdent aux cookies. Si une extension nécessite une autorisation que vous avez bloquée, l’utilisateur ne peut pas l’installer. Si les utilisateurs ont précédemment installé l’extension, elle ne se charge plus. Si une extension contient une autorisation bloquée en tant que condition facultative, elle s’installe comme d’habitude. Ensuite, pendant l’exécution de l’extension, les autorisations bloquées sont automatiquement refusées.<br>Pour obtenir la liste des autorisations disponibles, voir [déclarer des autorisations](/microsoft-edge/extensions-chromium/enterprise/declare-permissions).   |
| **installation_mode**| Contrôle si et comment les extensions que vous spécifiez sont ajoutées à Microsoft Edge. Vous pouvez définir le mode d’installation sur l’une des options suivantes :<br>- autorisé : les utilisateurs peuvent installer l’extension. Si aucun mode d’installation n’est défini, ce paramètre est défini par défaut.<br>- bloqué : les utilisateurs ne peuvent pas installer l’extension.<br>- force_installed : installer automatiquement l’extension sans interaction de l’utilisateur. Les utilisateurs ne peuvent pas le supprimer. Vous devez également définir l’emplacement de téléchargement de l’extension à l’aide update_url. **Remarque** : vous ne pouvez pas utiliser ce paramètre avec * car Microsoft Edge ne sait pas quelle extension installer automatiquement.<br>- normal_installed : installer automatiquement l’extension sans interaction de l’utilisateur. Les utilisateurs peuvent la désactiver. Vous devez également définir l’emplacement de téléchargement de l’extension à l’aide update_url. **Remarque** : vous ne pouvez pas utiliser ce paramètre avec * car Microsoft Edge ne sait pas quelle extension installer automatiquement.<br>- supprimé : les utilisateurs ne peuvent pas installer l’extension. Si les utilisateurs ont précédemment installé l’extension, Microsoft Edge la supprime. |  |
| **install_sources** | Peut être utilisé uniquement pour configurer la configuration par défaut, *. Spécifie les URL autorisées à installer les extensions. L’emplacement du fichier *.crx et la page à partir de laquelle le téléchargement est démarré (le référent) doivent être autorisés par ces modèles. Pour obtenir des exemples de modèle d’URL, voir [les modèles de correspondance](/microsoft-edge/extensions-chromium/enterprise/match-patterns).  |
| **minimum_version_required** |Microsoft Edge désactive les extensions, y compris les extensions installées avec force, avec une version antérieure à la version minimale spécifiée.<br>Le format de la chaîne de version est identique à celui utilisé dans le manifeste d’extension.     |
| **update_url** | S’applique uniquement aux force_installed et normal_installed. Spécifie l’emplacement à partir duquel Microsoft Edge doit télécharger une extension. Si l’extension est hébergée sur le site web des modules complémentaires Microsoft Edge, utilisez cet emplacement : `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.<br>Microsoft Edge utilise l’URL que vous spécifiez pour l’installation initiale de l’extension. Pour les mises à jour d’extension ultérieures, Microsoft Edge utilise l’URL dans le manifeste de l’extension.   |
| **runtime_allowed_hosts**| Permet aux extensions d’interagir avec des sites web spécifiés, même si elles sont également définies dans runtime_blocked_hosts. Vous pouvez spécifier jusqu’à 100 entrées. Les entrées supplémentaires sont ignorées.<br>Le format de modèle hôte est similaire aux [modèles de correspondance](/microsoft-edge/extensions-chromium/enterprise/match-patterns) , sauf que vous ne pouvez pas définir le chemin d’accès. Exemple :<br>- *://*.example.com<br>- *://exemple.*—Les caractères génériques eTLD sont pris en charge     |
| **runtime_blocked_hosts**| Empêcher les extensions d’interagir ou de modifier des sites web que vous spécifiez. Les modifications incluent le blocage de l’injection JavaScript, l’accès aux cookies et les modifications de demande web.<br>Vous pouvez spécifier jusqu’à 100 entrées. Les entrées supplémentaires sont ignorées.<br>Le format de modèle hôte est similaire aux modèles de correspondance, sauf que vous ne pouvez pas définir le chemin d’accès. Exemple :<br>- *://*.example.com<br>- *://exemple.*—Les caractères génériques eTLD sont pris en charge   |


## <a name="configure-using-a-json-string-in-windows-group-policy-editor"></a>Configurer à l’aide d’une chaîne JSON dans l’Éditeur de stratégie de groupe Windows

Les étapes d’utilisation de la stratégie de paramètres d’extension à l’aide de l’outil de stratégie de groupe supposent que vous avez déjà importé ADM/ADMX pour les stratégies Microsoft Edge.

1. Ouvrez l’Éditeur de stratégie de groupe, puis accédez à **Microsoft Edge > Extensions > Configurer une stratégie de paramètres de gestion des extensions**.
2. Activez la stratégie et entrez ses données JSON (JavaScript Object Notation) compactes dans la zone de texte sous la forme d’une seule ligne sans interruption de ligne.
3. Pour valider la stratégie et la compacter en une seule ligne, utilisez un outil de compression JSON.

### <a name="properly-format-json-for-the-extension-settings-policy"></a>Mettre correctement en forme JSON pour la stratégie de paramètres d’extension

Vous devez comprendre les deux parties de cette stratégie : l’étendue par défaut et l’étendue individuelle. L’étendue par défaut est un « fourre-tout » pour les extensions sans leur propre étendue. L’étendue individuelle est appliquée à cette extension uniquement.  

L’étendue par défaut est identifiée par l’astérisque (*). L’exemple suivant définit une étendue par défaut et une étendue d’extension individuelle.

```json
{ 
   “*”: {}, 
   “nckgahadagoaajjgafhacjanaoiihapd”: {} 
} 
```

Une extension ne peut obtenir ses paramètres qu’à partir d’une étendue. S’il existe une étendue d’extension individuelle pour cette extension, il s’agit des paramètres qui s’appliquent à cette extension. Si aucune étendue d’extension individuelle n’existe, l’extension utilisera l’étendue par défaut.  

L’exemple JSON suivant bloque l’exécution d’une extension sur `.example.com` et bloque toute extension nécessitant l’autorisation « USB ».

```json
{ 
  "*": { 
    "runtime_blocked_hosts": ["*://*.example.com"], 
    "blocked_permissions": ["usb"] 
  } 
} 
```

**JSON compact**

```json
{"*":{"runtime_blocked_hosts":["*://*.example.com"],"blocked_permissions":["usb"]}} 
```

### <a name="a-few-more-json-examples-for-extension-settings"></a>Quelques exemples JSON pour les paramètres d’extension

#### <a name="using-installation_mode-property-to-allow-and-block-extensions"></a>Utilisation installation_mode propriété pour autoriser et bloquer les extensions

- L’utilisateur peut installer toutes les extensions : il s’agit du paramètre par défaut 

  `{ "*": {"installation_mode": "allowed" }}`
- L’utilisateur ne peut installer aucune extension.  

  `{ "*": {"installation_mode": "blocked" }}`

- Spécifiez un message personnalisé à afficher lorsque l’installation est bloquée.

   `{"*": {"blocked_install_message": ["Call IT(408 - 555 - 1234) for an exception"]}}`

#### <a name="using-installation_mode-property-to-force-install-extensions"></a>Utilisation de installation_mode propriété pour forcer l’installation des extensions

Lorsque vous utilisez installation_mode comme « force_installed », l’extension est installée automatiquement sans intervention de l’utilisateur. Un utilisateur ne peut pas désactiver ou supprimer l’extension. Si une extension est installée « normal » ou « forcer », le champ **update_url** doit également être défini. Ce champ pointe vers l’emplacement à partir duquel l’extension peut être installée. Utilisez les emplacements suivants pour le champ **le update_url** :

- Si l’extension que vous téléchargez est hébergée sur le magasin de modules complémentaires Microsoft Edge, utilisez [https://edge.microsoft.com/extensionwebstorebase/v1/crx](https://edge.microsoft.com/extensionwebstorebase/v1/crx).
- Si l’extension que vous téléchargez est hébergée sur le Chrome Web Store, utilisez [https://clients2.google.com/service/update2/crx](https://clients2.google.com/service/update2/crx).
- Si vous hébergez l’extension sur votre propre serveur, utilisez l’URL Microsoft Edge pouvez télécharger l’extension placée dans un package (fichier.crx). Exemple JSON :

   `{"nckgahadagoaajjgafhacjanaoiihapd": {"installation_mode": "force_installed","update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"}}`
  
Dans l’exemple ci-dessus, au lieu de « force_installed », si vous utilisez « normal_installed », l’extension est installée automatiquement sans interaction de l’utilisateur, mais elle peut désactiver l’extension.  

   > [!TIP]
   > La mise en forme correcte d’une chaîne JSON peut être difficile. Utilisez un outil de vérification JSON avant d’implémenter la stratégie. Ou essayez la version antérieure de [l’Outil générateur des paramètres de l’extension](https://microsoft.github.io/edge-extension-settings-generator/minimal)

## <a name="configure-using-the-windows-registry"></a>Configurer à l’aide du Registre Windows

La stratégie ExtensionSettings doit être écrite dans le Registre sous cette clé :

`HKLM\Software\Policies\Microsoft\Edge\`

> [!NOTE]
> Il est possible d’utiliser HKCU au lieu de HKLM. Le chemin d’accès équivalent peut être configuré avec l’objet de stratégie de groupe (GPO).  

Pour Microsoft Edge, tous les paramètres démarrent sous cette clé :

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\`

La clé suivante que vous allez créer est soit l’ID d’extension de l’étendue individuelle, soit un astérisque (*) pour l’étendue par défaut. Par exemple, vous devez utiliser l’emplacement suivant pour les paramètres qui s’appliquent à Google Hangouts :

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\nckgahadagoaajjgafhacjanaoiihapd`

Pour les paramètres qui s’appliquent à l’étendue par défaut, utilisez cet emplacement :

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\*`

Différents paramètres nécessitent différents formats, selon qu’il s’agit d’une chaîne ou d’un tableau de chaînes. Les valeurs de tableau requièrent [ " value " ]. Les valeurs de chaîne peuvent être entrées telles qu’elle sont. La liste suivante indique les paramètres qui sont des tableaux ou des chaînes :

- Installation_mode = Chaîne
- update_url = Chaîne
- blocked_permissions = Tableau de chaînes
- allowed_permissions = Tableau de chaînes
- minimum_version_required = Chaîne
- runtime_blocked_hosts = Tableau de chaînes
- runtime_allowed_hosts = Tableau de chaînes
- blocked_install_message = Chaîne


## <a name="see-also"></a>Voir également

- [Gérer les extensions Microsoft Edge dans l’entreprise](microsoft-edge-manage-extensions.md)
- [Utiliser des stratégies de groupe pour gérer les extensions Microsoft Edge](microsoft-edge-manage-extensions-policies.md)
- [FAQ sur les extensions Microsoft Edge](microsoft-edge-manage-extensions-faq.md)
- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
