---
title: Support Microsoft Edge pour la Protection des informations Windows
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2029
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Support Microsoft Edge pour la Protection des informations Windows
ms.openlocfilehash: 53564d6089e84969501ac4802cf96dbdb1b24361
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642240"
---
# <a name="microsoft-edge-support-for-windows-information-protection-wip"></a>Support Microsoft Edge pour la Protection des informations Windows (WIP)

Cet article explique comment Microsoft Edge prend en charge la Protection des informations Windows (WIP).

> [!NOTE]
> Ceci concerne MicrosoftEdge version81 ou ultérieure.

## <a name="overview"></a>Vue d'ensemble

La fonctionnalité de Protection des informations Windows (WIP) est une fonctionnalité de Windows 10 qui vous permet de protéger les données d’entreprise contre toute divulgation non autorisée ou accidentelle. Avec l’augmentation du travail à distance, il y a un risque accru de partager des données organisationnelles à l’extérieur du milieu de travail. Ce risque augmente lorsque des activités personnelles et des activités professionnelles se produisent sur les appareils d’entreprise.

Microsoft Edge prend en charge les travaux en cours pour protéger le contenu dans un environnement Web dans lequel les utilisateurs partagent et distribuent souvent du contenu.

### <a name="system-requirements"></a>Configuration requise

Les conditions requises s’appliquent aux appareils utilisant le travail en cours au sein de l’entreprise:

- Windows10, version1607 ou ultérieure
- Uniquement les références SKU client Windows
- Une des solutions de gestion décrites dans la section conditions préalables [travaux en cours](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#prerequisites)

### <a name="windows-information-protection-benefits"></a>Avantages de la Protection des informations Windows

WIP présente les avantages suivants:

- Séparation évidente entre les données personnelles et les données d’entreprise, sans que les employés aient besoin de basculer entre les environnements ou les applications.
- Protection des données supplémentaire pour les applications métiers existantes, sans mise à jour nécessaire des applications.
- La possibilité de réinitialiser à distance les données d’entreprise à partir d’appareils mobiles sur la Gestion des périphériques mobiles (GPM) Intune tout en laissant les données personnelles non affectées. 
- Rapports d’audit pour le suivi des problèmes et pour les actions de réparation telles que la formation de conformité pour les utilisateurs.
- Intégration à votre système de gestion existant pour configurer, déployer et gérer le travail en cours. Certains exemples sont Microsoft Intune, Microsoft Endpoint Configuration Manager ou votre système de Gestion des périphériques mobiles actuel (GPM).

## <a name="wip-policy-and-protection-modes"></a>Stratégie WIP et modes de protection

À l’aide de stratégies, vous pouvez configurer les quatre modes de protection décrits dans le tableau suivant. Pour plus d’informations, voir [modes de protection des travaux WIP](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#wip-protection-modes).

| Mode | Description |
|------|-------------|
| Bloquer | La fonctionnalitéWIP recherche les pratiques de partage inapproprié des données et empêche l’employé de terminer son action. Cette recherche peut inclure le partage de données d’entreprise sur des applications non protégées par l’entreprise en plus du partage de données d’entreprise entre des applications ou du partage en dehors du réseau de votre organisation. |
| Autoriser l’utilisateur à ignorer les avertissements | La fonctionnalitéWIP recherche les partages de données inappropriés et avertit les employés s’ils effectuent des opérations potentiellement dangereuses. Toutefois, ce mode de gestion permet à l’employé de remplacer la stratégie et de partager les données, en consignant l’action dans le journal d’audit. |
| Silencieux | La fonctionnalité WIP s’exécute en mode silencieux. Elle consigne les partages inappropriés de données, sans bloquer les invites qui auraient impliqué des interactions avec les employés en mode Autoriser les remplacements. Les actions non autorisées, comme des applications tentant d’accéder de manière inappropriée à une ressource réseau ou à des données protégées par WIP, sont toujours bloquées. |
| Désactivé | La fonctionnalitéWIP est désactivée et ne permet pas de protéger ou d’auditer vos données. Une fois que vous avez désactivé la fonctionnalitéWIP, une tentative de déchiffrement des fichiers balisésWIP sur les disques connectés localement est effectuée. Vos précédentes informations de stratégie et de déchiffrement ne sont pas automatiquement appliquées à nouveau si vous réactivez la protectionWIP.
 |

## <a name="wip-features-supported-in-microsoft-edge"></a>Fonctionnalités WIP prises en charge dans Microsoft Edge

À partir de la version81 de Microsoft Edge, les fonctions suivantes sont prises en charge:

- Les sites de travail sont indiqués par une icône de porte-documents dans la barre d’adresses.  
- Les fichiers téléchargés à partir d’un emplacement de travail sont automatiquement chiffrés.
- Application de silencieusement/bloquage/remplacement pour les chargements de fichier de travail vers des emplacements non professionnels.  
- Application de silencieusement/bloquage/remplacement pour les actions de déplacement de fichier & déplacer.
- Application de silencieusement/bloquage/remplacement pour les actions du Presse-papiers.
- La recherche d’emplacements de travail à partir de profils non professionnels redirige automatiquement vers le profil de travail (associé à l’identité Azure AD).
- Le mode IE prend en charge les fonctionnalités WIP complètes.

## <a name="working-with-wip-in-microsoft-edge"></a>Utilisation de WIP dans Microsoft Edge

Une fois que le support WIP est activé pour Microsoft Edge, les utilisateurs voient quand les informations relatives au travail sont accessibles. La capture d’écran suivante montre l’icône du porte-documents dans la barre d’adresses, indiquant que les informations professionnelles sont accessibles via le navigateur.

 ![Indicateur de barre d’adresses pour les sites marqués comme «travail»](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-notify.png)

Microsoft Edge permet aux utilisateurs de partager du contenu protégé dans un site Web non approuvé. La capture d’écran suivante montre l’invite Microsoft Edge qui permet à un utilisateur d’utiliser du contenu protégé dans un site Web non approuvé.

 ![Demander le remplacement du contenu protégé](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-override.png)

## <a name="configure-policies-to-support-wip"></a>Configurer des stratégies pour la prise en charge de WIP

L’utilisation de la fonction travail en cours avec Microsoft Edge nécessite la présence d’un profil de travail.

### <a name="ensure-the-presence-of-a-work-profile"></a>Vérifier la présence d’un profil de travail

Sur les ordinateurs joints hybrides, Microsoft Edge se connecter automatiquement avec le compte Azure Active Directory (Azure AD). Pour vous assurer que les utilisateurs ne suppriment pas ce profil, lequel est nécessaire pour le travail en cours, configurez la stratégie suivante:

- [NonRemovableProfileEnabled](./microsoft-edge-policies.md#nonremovableprofileenabled)

> [!NOTE]
> Si votre environnement n’est pas joint hybride, vous pouvez participer à une jointure hybride à l’aide des instructions suivantes: [Planifier votre implémentation de jointure Azure Active Directory hybride](/azure/active-directory/devices/hybrid-azuread-join-plan).

Si la jointure hybride n’est pas une option, vous pouvez utiliser les comptes Active Directory sur local pour permettre à Microsoft Edge de créer automatiquement un profil de travail spécial avec les comptes de domaine de l’utilisateur. Notez qu’il est possible que les comptes locaux ne reçoivent pas toutes les fonctionnalités d’Azure AD, telles que la synchronisation dans le Cloud, Office NTP, etc.)

#### <a name="active-directory-ad-accounts"></a>Comptes ActiveDirectory (AD)

Pour les comptes AD, vous devez configurer la stratégie suivante de façon à ce que Microsoft Edge crée automatiquement un profil de travail spécial.

- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin)

### <a name="windows-policies-for-wip"></a>Stratégies de WIP Windows

Vous pouvez configurer le WIP à l’aide des stratégies Windows. Pour plus d’informations, voir [Créer et déployer des stratégies WIP à l’aide de Microsoft Intune](/windows/security/information-protection/windows-information-protection/overview-create-wip-policy)

## <a name="frequently-asked-questions"></a>Forum Aux Questions

### <a name="how-do-i-resolve-error-code--2147024540"></a>Comment résoudre le code d’erreur -2147024540?

Ce code d’erreur correspond à l’erreur Protection des informations Windows suivante: *ERROR_EDP_POLICY_DENIES_OPERATION: l’opération demandée a été bloquée par la stratégie Protection des informations Windows. Pour plus d’informations, contactez votre administrateur système*

MicrosoftEdge affiche cette erreur lorsque l’organisation a activé la Protection des informations Windows pour permettre uniquement aux utilisateurs disposant d’applications approuvées d’accéder aux ressources d’entreprise. Dans ce cas, étant donné que MicrosoftEdge ne figure pas dans la liste des applications approuvées, l’administrateur devra mettre à jour les stratégies de Protection des informations Windows pour accorder l’accès à MicrosoftEdge.

La capture d’écran suivante montre comment Microsoft Intune est utilisé pour ajouter Microsoft Edge en tant qu’application autorisée pour les travaux en cours.

 ![Boîte de dialogue Intune pour ajouter Microsoft Edge en tant qu’application pour les travaux en cours](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-exemption.png)

Si vous n’utilisez pas Microsoft Intune, téléchargez et appliquez la mise à jour de la stratégie dans le fichier [stratégie d’AppLocker d’entreprise de Protection des informations Windows](https://download.microsoft.com/download/8/9/9/8995d820-065c-4ab1-aa2a-9d6dc0cd7ffa/MsEdge%20-%20WIP%20Enterprise%20AppLocker%20Policy%20Files.zip).

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise) 
- [Protéger les données d’entreprise à l’aide de la Protection des informations Windows](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)