---
title: Configurer Microsoft Edge à l’aide de Gestion des périphériques mobiles
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 10/25/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer Microsoft Edge à l’aide de Gestion des périphériques mobiles.
ms.openlocfilehash: dda35199f653b3dfb8f20b33b068c59621222b36
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979687"
---
# Configurer Microsoft Edge à l’aide de Gestion des périphériques mobiles

Cet article explique comment configurer Microsoft Edge sur Windows 10 à l’aide de [Gestion des périphériques mobiles (GPM)](https://docs.microsoft.com/windows/client-management/mdm/) au moyen de l’[Ingestion ADMX](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration). Cet article présente également :

- Procédure de [création d’un identifiant OMA-URI (Open Mobile Alliance Uniform Resource Identifier) pour les stratégies Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).
- Procédure de [configuration de Microsoft Edge dans Intune à l’aide de l’ingestion ADMX et d’un OMA-URI personnalisé](#configure-microsoft-edge-in-intune-using-admx-ingestion).

> [!NOTE]
> Cet article concerne Microsoft Edge version 77 ou ultérieure.

## Éléments prérequis

Windows 10, avec la configuration minimale requise suivante :

- Windows 10, version 1903 avec les mises à jour [KB4512941](https://support.microsoft.com/help/4512941/) et [KB4517211](https://support.microsoft.com/help/4517211/) installées
- Windows 10, version 1809 avec les mises à jour [KB4512534](https://support.microsoft.com/help/4512534/) et [KB4520062](https://support.microsoft.com/help/4520062/) installées
- Windows 10, version 1803 avec les mises à jour [KB4512509](https://support.microsoft.com/help/4512509/) et [KB4519978](https://support.microsoft.com/help/4519978) installées
- Windows 10, version 1709 avec les mises à jour [KB4516071](https://support.microsoft.com/help/4516071/) et [KB4520006](https://support.microsoft.com/help/4520006) installées

## Présentation

Vous pouvez configurer Microsoft Edge sur Windows 10 à l’aide de GPM avec votre fournisseur préféré de Gestion de la mobilité d’entreprise ou GPM qui prend en charge l’[Ingestion ADMX](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).

La configuration de Microsoft Edge avec GPM est un processus en deux parties :

1. Intégration du fichier ADMX Microsoft Edge dans votre fournisseur EMM ou GPM. Pour obtenir des instructions sur l’ingestion d’un fichier ADMX, consultez votre fournisseur.

   > [!NOTE]
   > Pour Microsoft Intune, consultez [Configurer Microsoft Edge dans Intune à l’aide de l’ingestion ADMX](#configure-microsoft-edge-in-intune-using-admx-ingestion).

2. [Création d’un OMA-URI pour une stratégie Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).

## Créer un OMA-URI pour les stratégies Microsoft Edge

Les sections suivantes décrivent la procédure de création du chemin d’accès OMA-URI et la procédure de recherche et de définition de la valeur au format XML pour les stratégies de navigateur obligatoires et recommandées.

Avant de commencer, téléchargez le fichier de modèles de stratégie Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) à partir de [la page d’accueil de Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise) et extrayez le contenu.

Il existe trois étapes pour définir l’OMA-URI :

1. [Créer le chemin d’accès OMA-URI](#create-the-oma-uri-path)
2. [Spécifier le type de données OMA-URI](#specify-the-data-type)
3. [Définir la valeur OMA-URI](#set-the-value-for-a-browser-policy)

### Créer le chemin d’accès OMA-URI

Utilisez la formule suivante comme guide pour la création des chemins d’accès OMA-URI. <br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`* <br/><br/>

| Paramètre         | Description                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| \<ADMXIngestName> | Utilisez « Edge » ou ce que vous avez défini lors de l’ingestion du modèle d’administration. Par exemple, si vous avez utilisé « ./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx », utilisez « MicrosoftEdge ».<br/><br/> Le `<ADMXIngestionName>` doit correspondre à celui utilisé lors de l’ingestion du fichier ADMX. |
| \<ADMXNamespace>  | « microsoft_edge » ou « microsoft_edge_recommended », selon que vous définissez une stratégie obligatoire ou recommandée. |
| \<ADMXCategory>   | La catégorie « parentCategory » de la stratégie est définie dans le fichier ADMX. Omettez `<ADMXCategory>` si la stratégie n’est pas groupée (aucune « parentCategory » définie). |
| \<PolicyName>     | Le nom de la stratégie est indiqué dans l’article [Référence de la stratégie du navigateur](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies). |

#### Exemple de chemin d’URI :

Pour cet exemple, supposons que le nœud `<ADMXIngestName>` est nommé « Edge » et que vous définissez une stratégie obligatoire. Le chemin d’URI serait :<br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~<ADMXCategory>/<PolicyName>`*

Si la stratégie n’est pas dans un groupe (par exemple, DiskCacheSize), supprimez « `~<ADMXCategory>` ». Remplacez `<PolicyName>` par le nom de la stratégie, DiskCacheSize. Le chemin d’URI serait :<br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`*

Si la stratégie se trouve dans un groupe, procédez comme suit :

1. Ouvrez **msedge.admx** avec n’importe quel éditeur xml.
2. Recherchez le nom de la stratégie que vous souhaitez définir. Par exemple, « ExtensionInstallForceList ».
3. Utilisez la valeur de l’attribut *ref* de l’élément *parentCategory*. Par exemple, « Extensions » de \<parentCategory ref=" Extensions"/>.
4. Remplacez `<ADMXCategory>` par la valeur *ref* de l’attribut pour construire le chemin d’accès de l’URI. Le chemin d’URI serait :<br/><br/>
*`/Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`*

### Spécifier le type de données

Le type de données OMA-URI est toujours « chaîne ».

### Définir la valeur d’une stratégie de navigateur

Cette section décrit comment définir la valeur, au format XML, pour chaque type de données. Accédez à la [Référence de stratégie du navigateur](https://docs.microsoft.com/deployedge/microsoft-edge-policies) pour rechercher le type de données de la stratégie.

> [!NOTE]
> Pour les données de type non booléen, la valeur commence toujours par `<enabled/>`.

#### Données de type booléen

Pour les stratégies qui sont des types booléens, utilisez `<enabled/>` ou `<disabled/>`.

#### Données de type entier

La valeur doit toujours commencer par l’élément `<enabled/>` suivi de `<data id="[valueName]" value="[decimal value]"/>`.

Pour rechercher le nom de la valeur et la valeur décimale d’une nouvelle page d’onglets, procédez comme suit :

1. Ouvrez **msedge.admx** avec n’importe quel éditeur xml.
2. Recherchez l’élément `<policy>` dans lequel l’attribut Name correspond au nom de la stratégie que vous souhaitez définir. Pour « RestoreOnStartup », recherchez `name="RestoreOnStartup"`.
3. Dans le nœud `<elements>`, recherchez la valeur que vous souhaitez définir.
4. Utilisez la valeur de l’attribut « valueName » dans le nœud `<elements>`. Pour « RestoreOnStartup », « valueName » est « RestoreOnStartup ».
5. Utilisez la valeur de l’attribut « value » dans le nœud `<decimal>`. Pour « RestoreOnStartup » pour ouvrir la page de nouvel onglet, la valeur est « 5 ».

Pour ouvrir la page de nouvel onglet au démarrage, utilisez :<br>
`<enabled/> <data id="RestoreOnStartup" value="5"/>`

#### Données de type liste de chaînes

La valeur doit toujours commencer par l’élément `<enabled/>` suivi de `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.

> [!NOTE]
> Le nom d’attribut « id » n’est pas le nom de la stratégie, même si, dans la plupart des cas, il correspond au nom de la stratégie. Il s’agit de la valeur de l’attribut de nœud \<list>, qui se trouve dans le fichier ADMX.

Pour rechercher le listID et définir la valeur pour bloquer une URL, procédez comme suit :

1. Ouvrez **msedge.admx** avec n’importe quel éditeur xml.
2. Recherchez l’élément `<policy>` dans lequel l’attribut Name correspond au nom de la stratégie que vous souhaitez définir. Pour « URLBlocklist », recherchez `name="URLBlocklist"`.
3. Utilisez la valeur de l’attribut « id » du nœud `<list> node for [listID]`.
4. La « valeur » est une liste d’URL séparées par un point-virgule (;)

Par exemple, pour bloquer l’accès à `contoso.com` et à `https://ssl.server.com` :<br>
`<enabled/> <data id=" URLBlocklistDesc" value="contoso.com;https://ssl.server.com"/>`

#### Type de données dictionnaire ou chaîne

La valeur doit toujours commencer par l’élément `<enabled/>` suivi de `<data id="[textID]" value="[string]"/>`.

Pour rechercher le textID et définir la valeur définie par les paramètres régionaux, procédez comme suit :

1. Ouvrez **msedge.admx** avec n’importe quel éditeur xml.
2. Recherchez l’élément `<policy>` dans lequel l’attribut Name correspond au nom de la stratégie que vous souhaitez définir. Pour « ApplicationLocaleValue », recherchez `name="ApplicationLocaleValue"`.
3. Utilisez la valeur de l’attribut « id » du nœud `<text>` pour `[textID]`.
4. Définissez la « valeur » sur le code de culture.

Pour définir les paramètres régionaux sur « es-US » avec la stratégie « ApplicationLocaleValue » :<br>
`<enabled/> <data id="ApplicationLocaleValue" value="es-US"/>`

### Créer l’OMA-URI pour une stratégie recommandée

La définition du chemin d’URI pour les stratégies recommandées dépend de la stratégie que vous souhaitez configurer.

#### Pour définir le chemin d’URI d’une stratégie recommandée

Utilisez la formule de chemin d’URI (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) et les étapes suivantes pour définir le chemin d’accès de l’URI :

1. Ouvrez **msedge.admx** avec n’importe quel éditeur xml.
2. Si la stratégie que vous souhaitez configurer ne figure pas dans un groupe, passez à l’étape 4 et supprimez `~<ADMXCategory>` du chemin d’accès.
3. Si la stratégie que vous souhaitez configurer se trouve dans un groupe :

   - Pour consulter la catégorie `<ADMXCategory>`, recherchez la stratégie que vous souhaitez définir. Lors de la recherche, ajoutez « _recommended » au nom de la stratégie. Par exemple, une recherche de « RegisteredProtocolHandlers_recommended » a le résultat suivant :

        ```xml
         <policy class="Both" displayName="$(string.RegisteredProtocolHandlers)" explainText="$(string.RegisteredProtocolHandlers_Explain)" key="Software\Policies\Microsoft\Edge\Recommended" name="RegisteredProtocolHandlers_recommended" presentation="$(presentation.RegisteredProtocolHandlers)">
           <parentCategory ref="ContentSettings_recommended"/>
           <supportedOn ref="SUPPORTED_WIN7_V77"/>
           <elements>
             <text id="RegisteredProtocolHandlers" maxLength="1000000" valueName="RegisteredProtocolHandlers"/>
           </elements>
         </policy>
        ```

   - Copiez la valeur de l’attribut *ref* de l’élément `<parentCategory>`. Pour « ContentSettings », copiez « ContentSettings_recommended » à partir de `<parentCategory ref=" ContentSettings_recommended"/>`.
   - Remplacez `<ADMXCategory>` par la valeur de l’attribut *ref* pour construire le chemin d’accès de l’URI dans la formule de chemin d’URI.

4. `<PolicyName>` est le nom de la stratégie, auquel est ajouté « _recommended ».

#### Exemples de chemin d’accès OMA-URI pour les stratégies recommandées

Le tableau suivant présente des exemples de chemins d’accès OMA-URI pour les stratégies recommandées.

|              Stratégie               |             OMA-URI                      |
|-----------------------------------|------------------------------------------|
| [RegisteredProtocolHandlers](https://docs.microsoft.com/deployedge/microsoft-edge-policies#registeredprotocolhandlers)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~ContentSettings_recommended/RegisteredProtocolHandlers_recommended`                        |
| [PasswordManagerEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordmanagerenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~PasswordManager_recommended/PasswordManagerEnabled_recommended`                        |
| [PrintHeaderFooter](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printheaderfooter)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Printing_recommended/PrintHeaderFooter_recommended`                        |
| [SmartScreenEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreenenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~SmartScreen_recommended/SmartScreenEnabled_recommended`                        |
| [HomePageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/HomepageLocation_recommended`                        |
| [ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/ShowHomeButton_recommended`                        |
| [FavoritesBarEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~/FavoritesBarEnabled_recommended`                        |

### Exemples d’OMA-URI

Exemples d’OMA-URI avec leur chemin d’URI, le type et un exemple de valeur.

#### Exemples de données de type booléen

*[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ShowHomeButton):*

| Champ   | Valeur                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nom    | Microsoft Edge: ShowHomeButton                                                       |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton` |
| type    | Chaîne                                                                               |
| Valeur   | `<enabled/>`                                                                          |

*[DefaultSearchProviderEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultSearchProviderEnabled) :*

| Champ   | Valeur                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nom    | Microsoft Edge: DefaultSearchProviderEnabled                                         |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~DefaultSearchProvider/DefaultSearchProviderEnabled`    |
| type    | Chaîne                                                                               |
| Valeur   | `<disable/>`                                                                          |

### Exemples de données de type entier

*[AutoImportAtFirstRun](https://docs.microsoft.com/deployedge/microsoft-edge-policies#AutoImportAtFirstRun) :*

| Champ   | Valeur                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nom    | Microsoft Edge: AutoImportAtFirstRun                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/AutoImportAtFirstRun`   |
| type    | Chaîne                                                                               |
| Valeur   | `<enabled/><data id="AutoImportAtFirstRun" value="1"/>`                             |

*[DefaultImagesSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultImagesSetting) :*

| Champ   | Valeur                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nom    | Microsoft Edge: DefaultImagesSetting                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/DefaultImagesSetting`    |
| type    | Chaîne                                                                               |
| Valeur   | `<enabled/><data id="DefaultImagesSetting" value="2"/>`                             |

*[DiskCacheSize](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DiskCacheSize) :*

| Champ   | Valeur                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nom    | Microsoft Edge: DiskCacheSize                                                        |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`        |
| type    | Chaîne                                                                               |
| Valeur   | `<enabled/><data id="DiskCacheSize" value="1000000"/>`                               |

#### Exemples de données de type liste de chaînes
<!--
*[NotificationsAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#NotificationsAllowedForUrls):*

| Field   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: NotificationsAllowedForUrls                                          |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/NotificationsAllowedForUrls`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com"/>`<br>For multiple list items: `<data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com;[*.]contoso.edu"/>`                               |
-->
*[RestoreOnStartupURLS](https://docs.microsoft.com/deployedge/microsoft-edge-policies#RestoreOnStartupURLS) :*

| Champ   | Valeur                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nom    | Microsoft Edge: RestoreOnStartupURLS                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/RestoreOnStartupURLs`    |
| Type    | Chaîne                                                                               |
| Valeur   | `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com"/>`<br>Pour les éléments de listes multiples : `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com&#xF000;2&#xF000;http://www.microsoft.com"/>`  |

*[ExtensionInstallForcelist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ExtensionInstallForcelist) :*

| Champ   | Valeur                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nom    | Microsoft Edge: ExtensionInstallForcelist                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`    |
| Type    | Chaîne                                                                               |
| Valeur   | `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000;gbchcmhmhahfdphkhkmpfmihenigjmpp;https://extensionwebstorebase.edgesv.net/v1/crx"/>`                               |

#### Exemple de données de type dictionnaire et chaîne

*[ProxyMode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ProxyMode) :*

| Champ   | Valeur                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Nom    | Microsoft Edge: ProxyMode                                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ProxyMode/ProxyMode`  |
| Type    | Chaîne                                                                               |
| Valeur   | `<enabled/><data id="ProxyMode" value="auto_detect"/>`                               |

## Configurer Microsoft Edge dans Intune à l’aide de l’ingestion ADMX

La méthode recommandée pour configurer Microsoft Edge avec Microsoft Intune consiste à utiliser le profil de modèles d’administration comme décrit dans [Configurer les paramètres de stratégie Microsoft Edge avec Microsoft Intune](https://docs.microsoft.com/deployedge/configure-edge-with-intune). Si vous souhaitez évaluer une stratégie qui n’est actuellement pas disponible dans les modèles d’administration Microsoft Edge dans Intune, vous pouvez configurer Microsoft Edge avec des [paramètres personnalisés pour les appareils Windows 10 dans Intune](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10).

Cette section décrit comment fournir des ressources de multiplexage aux pilotes clients.

1. [Ingérer le fichier ADMX Microsoft Edge dans Intune](#ingest-the-microsoft-edge-admx-file-into-intune)
2. [Définir une stratégie à l’aide d’un OMA-URI personnalisé dans Intune](#set-a-policy-using-custom-oma-uri-in-intune)

> [!IMPORTANT]
> Il est recommandé d’utiliser un profil OMA-URI personnalisé et un profil de modèles d’administration pour configurer le même paramètre Microsoft Edge dans Intune. Si vous déployez la même stratégie à l’aide d’un OMA-URI personnalisé et d’un profil de modèle d’administration, mais avec des valeurs différentes, les utilisateurs obtiendront des résultats imprévisibles. Nous vous recommandons vivement de supprimer votre profil OMA-URI avant d’utiliser un profil de modèles d’administration.

### Ingérer le fichier ADMX Microsoft Edge dans Intune

Cette section décrit la procédure d’ingestion du modèle d’administration Microsoft Edge (**fichier msedge.admx**) dans Intune.

> [!WARNING]
> Ne modifiez pas le fichier ADMX avant d’ingérer le fichier.

Pour ingérer le fichier ADMX, procédez comme suit :

1. Téléchargez le fichier de modèles de stratégie Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) à partir de [la page d’accueil de Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise) et extrayez le contenu. Le fichier que vous souhaitez ingérer est **msedge.admx**.
2. Connectez-vous au [portail Microsoft Azure](https://portal.azure.com).
3. Sélectionnez **Intune** dans _Tous les services_ ou recherchez Intune dans la zone de recherche du portail.
4. Dans _Microsoft Intune - Vue d’ensemble_, sélectionnez **Configuration du périphérique** | **Profils**.
5. Dans la barre de commandes supérieure, sélectionnez **+ Créer profil**.

   ![Créer un profil d’appareil](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile.png)

6. Fournissez les informations de profil suivantes :

   - **Nom** : entrez un nom descriptif. Pour cet exemple, « Configuration ingérée Microsoft Edge ».
   - **Description** : entrez une description facultative du profil.
   - **Plateforme** : sélectionnez « Windows 10 et versions ultérieures »
   - **Type de profil** : sélectionnez « Personnalisé »

7. Sur **Paramètres OMA-URI personnalisés**, cliquez sur **Ajouter** pour ajouter une ingestion ADMX.

   ![Ajouter l’ingestion pour OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-add-omauri.png)

8. Sur **Ajouter une ligne**, indiquez les informations suivantes :

   - **Nom** : entrez un nom descriptif. Pour cet exemple, utilisez « Ingestion ADMX Microsoft Edge ».
   - **Description** : entrez une description facultative du paramètre.
   - **OMA-URI** : entrez « *./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx* »
   - **Type de données** : sélectionnez « chaîne ».
   - **Valeur** : cette zone d’entrée s’affiche une fois que vous avez sélectionné le **Type de données**. Ouvrez le fichier msedge.admx à partir du fichier de modèles de stratégie Microsoft Edge que vous avez extrait à l’étape 1. Copiez **TOUT le texte** du fichier msedge.admx et collez-le dans la zone de texte **Valeur** illustrée dans la capture d’écran suivante.

        ![Ajouter une ingestion ADMX](./media/edge-cfg-with-mdm/configure-edge-intune-mdm-omauri-addrow-ingest.png)

   - Cliquez sur **OK**.

9. Sous **Paramètres OMA-URI personnalisés**, cliquez sur **OK**.
10. Sur **Créer un profil**, cliquez sur **Créer**. La capture d’écran suivante présente des informations sur le profil nouvellement créé.

    ![Informations sur le nouveau profil de périphérique ](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-done.png)

<!--
> [!NOTE]
> You can use the preceding steps to ingest the msedgeupate.admx policy template file.
-->
### Définir une stratégie à l’aide d’un OMA-URI personnalisé dans Intune

> [!NOTE]
> Avant d’utiliser les étapes de cette section, vous devez appliquer les étapes présentées dans [Ingérer le fichier ADMX Microsoft Edge dans Intune](#ingest-the-microsoft-edge-admx-file-into-intune).

1. Connectez-vous au [portail Microsoft Azure](https://portal.azure.com).
2. Sélectionnez **Intune** dans _Tous les services_ ou recherchez Intune dans la zone de recherche du portail.
3. Accédez à **Intune**>**Configuration du périphérique**>**Profils**.
4. Sélectionnez le profil « Configuration ingérée de Microsoft Edge ADMX » ou le nom que vous avez utilisé pour le profil.
5. Pour ajouter des paramètres de stratégie Microsoft Edge, vous devez ouvrir **Paramètres OMA-URI personnalisés**. Sous **Gérer**, cliquez sur **Propriétés**, puis sur **Paramètres**.

    ![Configurer les paramètres de profil](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings.png)

6. Sur **Paramètres OMA-URI personnalisés**, cliquez sur **Ajouter**.

    ![Ajouter une ligne aux paramètres OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings-add-row.png)

7. Sur **Ajouter une ligne**, indiquez les informations suivantes :

   - **Nom** : entrez un nom descriptif. Nous vous suggérons d’utiliser le nom de stratégie que vous souhaitez configurer. Pour cet exemple, utilisez « ShowHomeButton ».
   - **Description** (facultatif) : entrez une description du paramètre.
   - **OMA-URI** : entrez l’OMA-URI pour la stratégie. En prenant la stratégie « ShowHomeButton » comme exemple, utilisez la chaîne suivante : « *./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton* »
   - **Type de données** : sélectionnez le type de données des paramètres de stratégie. Pour la stratégie « ShowHomeButton », utilisez « chaîne ».
   - **Valeur** : entrez le paramètre que vous souhaitez configurer pour la stratégie. Pour l’exemple « ShowHomeButton », entrez « \<enabled/> ». La capture d’écran suivante présente les paramètres de configuration d’une stratégie.

        ![Ajouter une ligne, Paramètres OMA-URI personnalisés](./media/edge-cfg-with-mdm/configure-edge-mdm-custom-omauri-setting.png)

   - Cliquez sur **OK**.

8. Sous **Paramètres OMA-URI personnalisés**, cliquez sur **OK**.
9. Dans le profil « **Configuration ingérée de Microsoft Edge ADMX - Propriétés** » (ou le nom que vous avez utilisé), cliquez sur **Enregistrer**.

Une fois le profil créé et les propriétés définies, vous devez [attribuer le profil dans Microsoft Intune](https://docs.microsoft.com/intune/configuration/device-profile-assign).

#### Vérifiez que la stratégie a été créée.

Procédez comme suit pour confirmer que la stratégie Microsoft Edge utilise le profil que vous avez créé. (Laissez à Microsoft Intune le temps de propager la stratégie sur un périphérique que vous avez attribué dans l’exemple de profil « Configuration ingérée de Microsoft Edge ADMX ».)

1. Ouvrez Microsoft Edge et accédez à *edge://policy*.
2. Sur la page **Stratégies**, vérifiez si la stratégie que vous avez définie dans le profil est répertoriée.
3. Si ce n’est pas le cas, consultez [Diagnostiquer les échecs GPM dans Windows 10](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) ou [Résoudre les problèmes liés à un paramètre de stratégie](#troubleshoot-a-policy-setting).

#### Résoudre les problèmes liés à un paramètre de stratégie

Si une stratégie Microsoft Edge ne prend pas effet, procédez comme suit :

Ouvrez la page *edge://policy* sur le périphérique cible (un périphérique auquel vous avez affecté le profil dans Microsoft Intune) et recherchez la stratégie. Si la stratégie ne figure pas sur la page *edge://policy*, essayez ce qui suit :

- Vérifiez que la stratégie est bien dans le registre et qu’elle est correcte. Sur le périphérique cible, ouvrez l’Éditeur du Registre Windows 10 (**touche Windows +r**, entrez « *regedit* », puis appuyez sur **Entrée**.) Vérifiez que la stratégie est correctement définie dans le chemin d’accès *\Software\Policies\ Microsoft\Edge*. Si vous ne trouvez pas la stratégie dans le chemin d’accès attendu, cela signifie qu’elle n’a pas été envoyée correctement au périphérique.
- Vérifiez que le chemin d’accès OMA-URI est correct et que la valeur est une chaîne XML valide. Si l’une de ces conditions est incorrecte, la stratégie ne sera pas envoyée vers l’appareil cible.

Pour plus de conseils sur la résolution de problèmes, consultez [Installer Microsoft Intune](https://docs.microsoft.com/intune/fundamentals/setup-steps) et [Synchroniser les périphériques](https://docs.microsoft.com/intune/remote-actions/device-sync).

## Articles associés

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Configurer les paramètres de stratégie Microsoft Edge avec Microsoft Intune](configure-edge-with-intune.md)
- [Gestion des périphériques mobiles](https://docs.microsoft.com/windows/client-management/mdm/)
- [Utiliser les paramètres personnalisés pour les appareils Windows 10 dans Intune](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10)
- [Configuration de stratégie d’applications Win32 et Pont du bureau](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)
- [Fonctionnement des stratégies ADMX](https://docs.microsoft.com/windows/client-management/mdm/understanding-admx-backed-policies)
