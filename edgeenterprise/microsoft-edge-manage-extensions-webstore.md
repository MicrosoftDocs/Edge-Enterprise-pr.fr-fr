---
title: Extensions d’auto-hébergement Microsoft Edge
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 04/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez comment empaqueter et auto-héberger les extensions Microsoft Edge dans l’entreprise.
ms.openlocfilehash: 403b6879b15c146f40fa2564da76eae59b2abe88
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618100"
---
# <a name="self-host-microsoft-edge-extensions"></a>Extensions d’auto-hébergement Microsoft Edge

Cet article fournit des instructions de base pour empaqueter une extension à héberger sur votre propre site web. Il inclut également des instructions sur la façon de déployer des extensions sur les appareils et les utilisateurs de votre organisation.

## <a name="prerequisites"></a>Conditions préalables

Pour auto-héberger vos propres extensions, vous devrez fournir vos propres services d’hébergement web pour les extensions et leurs fichiers manifestes.

 Les étapes suivantes supposent que vous avez déjà créé votre extension, que vous avez de l’expérience avec les fichiers XML, que vous avez une connaissance approfondie de la configuration de la stratégie de groupe et que vous savez comment utiliser le Registre Windows.

## <a name="publish-an-extension"></a>Publier une extension

Avant de publier une extension, elle doit être empaquetée dans un fichier CRX (extension Chrome). Utilisez les étapes suivantes pour empaqueter une extension en tant que fichier CRX.

1. Dans la barre d'adresses de Microsoft Edge, allez à* edge://extensions* et activez **Développeur Mode**s’il n’est pas déjà activé.
2. Sous **Extensions installées**cliquez sur **Pack Extension** pour créer le fichier CRX.
3. Utilisez la boîte de dialogue **Pack Extension**pour rechercher le répertoire qui possède la source de l’extension. Sélectionnez le répertoire, puis cliquez sur **Pack Extension**.  Cela crée votre fichier CRX, ainsi qu’un fichier PEM. Enregistrez le fichier PEM, car il est nécessaire pour faire les mises à jour des versions de l’extension. La capture d’écran suivante montre la boîte de dialogue **Extension Pack**pour localiser le répertoire racine de l’extension.

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-pack-dialog.png" alt-text="Boîte de dialogue Extension Pack pour trouver le code source d’une extension.":::

   > [!IMPORTANT]
   > Stockez le fichier PEM dans un emplacement sûr, car il s’agit de la clé de l’extension et est nécessaire pour les futures mises à jour.

4. Faites glisser le fichier CRX dans la fenêtre d’extensions et assurez-vous qu’il se charge.
5. Testez l’extension et notez le champ ID (il s’agit de l’ID CRX) et le numéro de version. Vous aurez besoin de ces informations ultérieurement. La capture d’écran suivante montre une extension de test avec son ID CRX.

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-test-extension.png" alt-text="Exemple d’extension affichant l’ID CRX":::

6. Téléchargez le fichier CRX sur l’hôte et notez l’URL de l’emplacement à partir duquel il sera téléchargé. Ces informations sont nécessaires pour le fichier manifeste XML.
7. Pour créer un fichier manifeste XML avec l’ID d’application/extension, téléchargez l’URL, et la version, définissez les champs suivants:  

   - **appid**: L’ID d’extension de l’étape 5
   - **codebase**: L’emplacement du téléchargement du fichier CRX de l’étape 6
   - **version**: La version de l’application/extension, qui doit correspondre à la version spécifiée dans le manifeste de l’extension.

   L’extrait de code suivant montre un exemple de fichier manifeste XML.

   ```xml
   <?xml version='1.0' encoding='UTF-8'?> 
   <gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'> 
     <app appid='ekilpdeokbpjmminmhfcgkncmmohmfeb'> 
     <updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.0' /> 
     </app> 
   </gupdate> 
   ```

   Pour plus d’informations voir[Extensions de mise à jour automatique dans Microsoft Edge Microsoft Edge Développement](/microsoft-edge/extensions-chromium/enterprise/auto-update).

8. Chargez le fichier XML terminé à un emplacement à partir de lequel il peut être téléchargé, en notant l’URL. Cette URL sera nécessaire lorsque vous installerez l’extension à l’aide d’une stratégie de groupe. Consultez [Distribuer une extension hébergée en privé](#distribute-a-privately-hosted-extension).

   > [!IMPORTANT]
   > L’emplacement d’hébergement de l’extension n’a pas besoin d’authentification. Il doit être accessible par les appareils des utilisateurs où qu’ils soient.

## <a name="publish-updates-to-an-extension"></a>Publiez les mises à jour sur une extension

Après avoir changé et testé l’extension mise à jour, vous pouvez la publier. Utilisez les étapes suivantes comme guide pour publier une mise à jour.

1. Modifiez le numéro de version dans le manifeste de votre extension. Le fichier JSON à un nombre supérieur à l’aide de la syntaxe suivante:`"version":"versionString"`. Si la « version »:« 1.0 », vous pouvez mettre à jour vers « version »:« 1.1 » ou tout nombre supérieur à « 1.0 ».
2. Mettez à jour la « version » de `<updatecheck>`dans le fichier XML pour correspondre au numéro que vous avez placé dans le fichier manifeste à l’étape précédente. Exemple:<br>`<updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.1' />`
3. Créez un fichier CRX qui inclut les nouvelles modifications. Accédez à *edge://extensions* et activez **Mode Developeur**.
4. Cliquez sur**Extension Pack** et allez dans le répertoire de la source de l’extension.

   > [!IMPORTANT]
   > Utilisez le même fichier PEM qui a été généré et enregistré la première fois que le fichier CRX a été créé. Si vous n’utilisez pas le même fichier PEM, l’ID d’application de l’extension change et la mise à jour est traitée comme une nouvelle extension.

5. Faites glisser et déposez le fichier CRX dans la fenêtre d’extensions et vérifiez qu’il se charge.
6. Testez l’extension mise à jour.
7. Remplacez l’ancien fichier CRX et le fichier XML par les nouveaux fichiers pour l’extension mise à jour.

Les modifications de l’extension seront récupérées pendant le prochain cycle de synchronisation de stratégie. Pour plus d’informations sur la mise à jour des extensions, consultez: [Mise à jour de l’URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) et[Mise à jour de manifeste](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).

## <a name="distribute-a-privately-hosted-extension"></a>Distribuez une extension hébergée en privé

Vous pouvez partager le lien de l’emplacement où le fichier CRX est hébergé, et dès que les utilisateurs entrent l’URL dans leur navigateur, l’extension est téléchargée et installée. Les utilisateurs peuvent activer l’extension à partir de edge://extensions page. Pour permettre aux utilisateurs d’installer des extensions auto-hébergées, ajoutez les IDs CRX d’extension à la stratégie [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist).

Vous pouvez également utiliser la stratégie de groupe [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) pour forcer l’installation d’une extension sur les appareils de vos utilisateurs.

Vous pouvez appliquer ces stratégies à vos utilisateurs, appareils sélectionnés ou les deux. N’oubliez pas que les mises à jour de stratégie ne sont pas instantanées et qu’il faudra du temps aux paramètres de stratégie pour prendre effet.

## <a name="see-also"></a>Voir également

- [Gérer les extensions Microsoft Edge dans l’entreprise](microsoft-edge-manage-extensions.md)
- [Utiliser des stratégies de groupe pour gérer les extensions Microsoft Edge](microsoft-edge-manage-extensions-policies.md)
- [Guide détaillé de la stratégie ExtensionSettings](microsoft-edge-manage-extensions-ref-guide.md)
- [FAQ sur les extensions Microsoft Edge](microsoft-edge-manage-extensions-faq.md)
- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
