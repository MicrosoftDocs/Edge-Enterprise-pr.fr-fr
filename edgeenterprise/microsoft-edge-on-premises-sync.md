---
title: Synchronisation locale pour les utilisateurs de Active Directory (AD)
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Synchronisation locale pour les utilisateurs de Active Directory (AD)
ms.openlocfilehash: f595c863193f2b3d383a6215ab7817a53bbf5ca6
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642440"
---
# <a name="on-premises-sync-for-active-directory-ad-users"></a>Synchronisation locale pour les utilisateurs de Active Directory (AD)

Cet article explique comment les utilisateurs d’Active Directory (AD) peuvent parcourir les favoris et paramètres entre les ordinateurs sans se connecter aux services Cloud de Microsoft.

> [!NOTE]
> Cet article concerne Microsoft Edge version 85 ou ultérieure.

## <a name="introduction"></a>Introduction

La synchronisation des données d’utilisateur dans Microsoft Edge nécessite normalement un compte Microsoft ou un compte Azure Active Directory (Azure AD), ainsi qu’une connexion aux services Cloud de Microsoft. Avec la synchronisation locale, Microsoft Edge enregistre les favoris et paramètres d’un utilisateur d’Active Directory dans un fichier qui peut être transféré entre différents ordinateurs. La synchronisation locale n’interfère pas avec la synchronisation Cloud pour les profils qui l’autorisent.

## <a name="how-it-works"></a>Fonctionnement

Microsoft Edge permet aux profils d’être associés à des comptes Active Directory (AD), qui ne peuvent pas être utilisés avec la synchronisation cloud. Lorsque la synchronisation locale est activée, les données du profil AD sont enregistrées dans un fichier nommé profil.pb. Par défaut, ce fichier est stocké dans * %APPDATA%/Microsoft/Edge*. Une fois ce fichier écrit, il peut être transféré entre différents ordinateurs, et les données d’utilisateur sont lues et écrites sur chaque ordinateur. Microsoft Edge lit et écrit uniquement à partir de ce fichier ; il incombe à l’administrateur de s’assurer que le fichier est déplacé selon les besoins.

## <a name="use-on-premises-sync"></a>Utiliser la synchronisation locale

Pour utiliser la synchronisation locale, vous devez l’activer, associer un profil à un compte AD, et éventuellement, changer l’emplacement des données d’utilisateur.

### <a name="enable-on-premises-sync"></a>Activer la synchronisation locale

Pour activer la synchronisation locale dans Microsoft Edge, configurez la stratégie de [ParcourirSupportduProfilActivé](./microsoft-edge-policies.md#roamingprofilesupportenabled).

### <a name="ensure-that-a-profile-is-associated-with-an-active-directory-account"></a>Vérifier qu’un profil est associé à un compte Active Directory

La synchronisation locale fonctionne uniquement avec le profil associé à un compte Active Directory (AD). Si aucun profil de ce type n’existe, la synchronisation locale ne fonctionnera pas. Pour vous assurer que les utilisateurs se connectent à l’aide d’un compte AD, configurez la stratégie de [ConfigurerlaConnexionAutomatiqueauCompteLocale](./microsoft-edge-policies.md#configureonpremisesaccountautosignin). Pour la synchronisation sur site, Microsoft Edge s’appuie uniquement sur AD pour établir une identité pour les données utilisateur et il n’existe aucune relation directe entre la façon dont Microsoft Edge lit et écrit les données sur site sur la façon dont l’administrateur a configuré l’itinérance pour un utilisateur AD.

### <a name="change-the-location-of-the-user-data-optional"></a>Changer l’emplacement des données d’utilisateur (facultatif)

Par défaut, les données d’utilisateur sont stockées dans un fichier nommé**profil.pb** dans * %APPDATA%/Microsoft/Edge*. Pour changer l’emplacement de ce fichier, configurez la stratégie [Parcourirl’EmplacementduProfil](./microsoft-edge-policies.md#roamingprofilelocation).

## <a name="changes-in-the-user-experience-when-on-premises-sync-is-enabled"></a>Modifications apportées à l’expérience d’utilisateur lorsque la synchronisation locale est activée

Lorsque la synchronisation locale est activée, les utilisateurs ne sont pas invités à activer la synchronisation. De plus, les utilisateurs ne peuvent pas désactiver la synchronisation dans les paramètres de synchronisation et ils ne peuvent pas activer les types de synchronisation qui ne sont pas pris en charge par la synchronisation locale.

## <a name="on-premises-sync-usage-notes"></a>Notes d’utilisation de la synchronisation locale

### <a name="running-cloud-sync-and-on-premises-sync-on-the-same-computer"></a>Exécution de la synchronisation cloud et de la synchronisation locale sur le même ordinateur

La synchronisation locale n’interfère pas avec la synchronisation cloud. Si Microsoft Edge possède plusieurs comptes Microsoft ou des profils Azure Active Directory synchronisés avec le cloud, ceux-ci continuent d’être synchronisés pendant que la synchronisation locale est activée.

### <a name="running-microsoft-edge-on-more-than-one-computer-at-a-time-isnt-recommended"></a>Il n’est pas recommandé d’utiliser Microsoft Edge sur plusieurs ordinateurs à la fois

Étant donné que la synchronisation locale fonctionne en transférant un fichier de données d’utilisateur entre les ordinateurs, la synchronisation locale ne synchronise pas les modifications entre les sessions simultanées. Pour cette raison, la synchronisation locale fonctionne de manière optimale lorsqu’elle est utilisée sur un ordinateur à la fois. Lorsque des sessions simultanées locales sont exécutées, les données sur les ordinateurs peuvent être écrasées de manière inattendue par les données d’un autre ordinateur lors du prochain démarrage d’une session de navigateur.

> [!NOTE]
> Microsoft Edge verrouille le fichier **profil.pb** lorsque la synchronisation locale est activée. Si la redirection de dossiers est utilisée pour partager un fichier unique **profil.pb** entre différents ordinateurs, une seule instance de Microsoft Edge utilisant ce fichier peut être alors démarrée.

### <a name="using-other-sync-policies-with-on-premises-sync"></a>Utiliser d’autres stratégies de synchronisation avec la synchronisation locale

La stratégie [ListedeTypedeSynchronisationDésactivée](./microsoft-edge-policies.md#synctypeslistdisabled) peut être utilisée pour désactiver de façon sélective la synchronisation des favoris ou des paramètres, si vous le souhaitez. La [stratégie SyncDisabled](./microsoft-edge-policies.md#syncdisabled) n’a aucun impact sur la synchronisation sur site.

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge et Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Synchronisation de Microsoft Edge Entreprise](microsoft-edge-enterprise-sync.md)