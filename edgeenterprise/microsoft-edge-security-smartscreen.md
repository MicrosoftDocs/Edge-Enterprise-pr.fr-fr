---
title: Prise en charge de Microsoft Edge pour Microsoft Defender SmartScreen
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Prise en charge de Microsoft Edge pour Microsoft Defender SmartScreen
ms.openlocfilehash: 363605200c61807ca526818ab417301273d64f91
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642630"
---
# <a name="microsoft-edge-support-for-microsoft-defender-smartscreen"></a>Prise en charge de Microsoft Edge pour Microsoft Defender SmartScreen

Cet article présente les avantages liés à l’utilisation de Microsoft Defender SmartScreen, explique son fonctionnement et décrit comment configurer cette fonctionnalité de Microsoft Edge.

> [!NOTE]
> Cet article concerne Microsoft Edge version 77 ou ultérieure.

Microsoft Defender SmartScreen est un service utilisé par Microsoft Edge pour préserver votre sécurité lorsque vous naviguez sur le web. Microsoft Defender SmartScreen offre un système d’alerte anticipée à l’encontre des sites web susceptibles de lancer des attaques par hameçonnage ou de tenter de distribuer des logiciels malveillants via une attaque ciblée. Pour plus d’informations, regardez [la vidéo : Sécuriser la navigation sur Microsoft Edge](microsoft-edge-video-security-smartscreen.md).

> [!NOTE]
> Avant la version 1703 de Windows 10, cette fonctionnalité était appelée filtre SmartScreen lorsqu’elle était utilisée dans le navigateur et Microsoft SmartScreen dans le cas d’une utilisation en dehors du navigateur.

## <a name="the-benefits-of-microsoft-defender-smartscreen"></a>Avantages de Microsoft Defender SmartScreen

Microsoft Defender SmartScreen offre plusieurs avantages synthétisés dans la liste suivante. Ces avantages sont décrits en détail dans la [Documentation de Microsoft Defender SmartScreen](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview#benefits-of-windows-defender-smartscreen). Les avantages sont les suivants :

- Prise en charge de l’anti-hameçonnage et de l’anti-programme malveillant
- URL et protection de l’application basées sur la réputation
- Intégration du système d’exploitation
- Méthode heuristique et données de diagnostic améliorées
- Gestion par le biais de la stratégie de groupe et Microsoft Intune
- Blocage des URL associées à des applications potentiellement indésirables

## <a name="understand-how-microsoft-defender-smartscreen-works"></a>Comprendre le fonctionnement de Microsoft Defender SmartScreen

Plusieurs entrées contribuent aux avertissements Microsoft Defender SmartScreen. Les données sont reçues de nombreuses sources, notamment les commentaires des utilisateurs, les fournisseurs de données et les modèles d’intelligence. Ces données sont utilisées pour vous aider à identifier le contenu potentiellement malveillant. Microsoft Defender SmartScreen vérifie également si les programmes d’installation des applications ou les programmes téléchargés sont malveillants. Dans les deux cas, Microsoft Defender SmartScreen avertit les utilisateurs sur un contenu suspect de façon appropriée.

### <a name="site-analysis"></a>Analyse de site

Microsoft Defender SmartScreen détermine si un site est potentiellement dangereux par :

- Analyse des pages web visitées pour des signes indiquant un comportement suspect.
- Comparaison des sites visités à un enregistrement dynamique de signalement des sites d’hameçonnage.

Si Microsoft Defender SmartScreen établit qu’une page est malveillante, une page d’avertissement s’affiche pour aviser l’utilisateur que ce site est considéré comme non sécurisé. La capture d’écran suivante présente l’exemple d’une page d’avertissement Microsoft Defender SmartScreen lorsqu’un utilisateur tente d’ouvrir un site web malveillant.

![Page de blocage de Microsoft Defender SmartScreen relative à un lien vers un site externe](media/microsoft-edge-security-smartscreen/microsoft-edge-smartscreen-warning.png)

Les utilisateurs ont la possibilité de signaler un site comme fiable ou non sécurisé dans le message d’avertissement. Pour plus d'informations, consultez [Comment signaler un site](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device#how-users-can-report-websites-as-safe-or-unsafe).

### <a name="file-analysis"></a>Analyse de fichier

Microsoft Defender SmartScreen détermine si une application téléchargée ou un programme d’installation d’application est potentiellement malveillant en fonction de nombreux critères, tels que le trafic de téléchargement, l’historique de téléchargement, les résultats précédents d’un antivirus et la réputation de l’URL.

- Les fichiers présentant une réputation sûre connue sont téléchargés sans notification.  
- Les fichiers présentant une réputation malveillante connue affichent un avertissement indiquant à l’utilisateur que le fichier est non sécurisé et qu’il a été signalé comme malveillant. La capture d’écran suivante présente un exemple d’avertissement pour un fichier malveillant.

  ![Notification de blocage de Microsoft Defender SmartScreen pour un fichier avec une réputation malveillante](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-known-malicious.png)

- Les fichiers inconnus affichent un avertissement indiquant à l’utilisateur que le téléchargement ne possède pas d’empreinte connue et conseille la prudence. La capture d’écran suivante présente un exemple d’avertissement pour un fichier inconnu.

  ![Notification de blocage de Microsoft Defender SmartScreen pour un fichier dont la réputation est inconnue](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious.png)

Tous les programmes inconnus ne sont pas malveillants et l’avertissement d’un élément inconnu entend fournir un contexte et des instructions aux utilisateurs qui en ont besoin, en particulier si l’avertissement est inattendu.

  ![Conserver le fichier avec une réputation malveillante](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious-keep.png)

Toutefois, les utilisateurs peuvent continuer à télécharger et exécuter l’application en cliquant sur **... Conserver | Afficher plus | Conserver quand même**.

> [!TIP]
> **Note d’information aux clients de l’entreprise.** Par défaut, Microsoft Defender SmartScreen permet aux utilisateurs d’ignorer les avertissements. L’interaction de l’utilisateur étant potentiellement risquée, nous vous recommandons de passer en revue ces [paramètres recommandés de stratégie de groupe](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-available-settings#recommended-group-policy-and-mdm-settings-for-your-organization).

Vous voyez la façon dont Microsoft Defender SmartScreen répond à différents scénarios à l’aide de notre [site de démonstration](https://demo.smartscreen.msft.net/).

## <a name="microsoft-defender-smartscreen-and-user-privacy"></a>Microsoft Defender SmartScreen et la confidentialité de l’utilisateur

Microsoft Defender SmartScreen protège les utilisateurs lorsqu’ils naviguent sur Internet à l’aide d’un système de vérification de la réputation. Microsoft Edge transmet les informations pertinentes sur l’URL ou le fichier au service Microsoft Defender SmartScreen pour commencer la vérification de réputation. La vérification compare le site web ou le fichier à des listes dynamiques de sites et de fichiers connus comme étant dangereux. Toutes les demandes adressées au service Microsoft Defender SmartScreen sont effectuées avec le chiffrement TLS. Le service renvoie les résultats de la vérification de réputation, ce qui peut entraîner l’affichage par Microsoft Edge d’un avertissement pour le site ou le fichier. Ces résultats sont stockés localement sur l’appareil.

Le service Microsoft Defender SmartScreen stocke les données sur les vérifications de réputation. Au fur et à mesure de l’identification de nouveaux sites, le service ajoute une base de données dynamique d’URL et de fichiers malveillants connus. Ces données sont stockées sur des serveurs Microsoft sécurisés et sont uniquement utilisées pour les services de sécurité Microsoft. Ces données ne sont jamais utilisées pour identifier les utilisateurs ou les cibler d’une façon ou d’une autre. Le vidage du cache de navigation efface localement toutes les données de l’URL de Microsoft Defender SmartScreen stockées. La suppression de l’historique de téléchargement supprime toutes les données SmartScreen stockées localement relatives aux téléchargements de fichiers.

Pour plus d’informations sur Microsoft Defender SmartScreen et la confidentialité sur Microsoft Edge, consultez le [Livre blanc sur la confidentialité Microsoft Edge](/microsoft-edge/privacy-whitepaper#smartscreen).

## <a name="microsoft-defender-smartscreen-setup-for-admins"></a>Configuration de Microsoft Defender SmartScreen pour les administrateurs

Les administrateurs peuvent configurer Microsoft Defender SmartScreen en utilisation les paramètres de stratégie de groupe, de Microsoft Intune ou de Gestion des périphériques mobiles (MDM). Selon la manière dont vous configurez Microsoft Defender SmartScreen, vous pouvez afficher une page d’avertissement à destination de vos employés et leur permettre de poursuivre la consultation du site, ou vous pouvez bloquer ce dernier.

### <a name="microsoft-defender-smartscreen-set-up-using-group-policy"></a>Microsoft Defender SmartScreen est configuré à l’aide d’une stratégie de groupe

Pour obtenir la liste complète des stratégies SmartScreen, voir les [paramètres de Microsoft Defender SmartScreen](./microsoft-edge-policies.md#smartscreen-settings)

### <a name="microsoft-defender-smartscreen-set-up-using-mdm"></a>Configuration de Microsoft Defender SmartScreen à l’aide de la Gestion des périphériques mobiles (MDM)

Pour plus d’informations, voir :

- [Paramètres de Windows Intune pour Microsoft Defender SmartScreen](/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)
- [Paramètres de stratégie de Gestion des périphériques mobiles (MDM)](/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)

## <a name="microsoft-defender-smartscreen-setup-for-users"></a>Configuration de Microsoft Defender SmartScreen pour les utilisateurs

Microsoft Edge pour Microsoft Defender SmartScreen est activé par défaut pour Microsoft Edge. Pour désactiver Microsoft Defender SmartScreen, accédez à *edge://settings/privacy > Services > Microsoft Defender SmartScreen*. Ce paramètre est identique pour tous les profils associés à l’installation de Microsoft Edge sur un appareil. Ce paramètre n’est pas synchronisé sur tous vos appareils. Le paramètre s’applique à la navigation InPrivate et au mode Invité. Si un appareil est géré à l’aide de stratégies de groupe définies par une organisation, cette configuration est reflétée dans *edge://settings/privacy*.

> [!NOTE]
> Les utilisateurs peuvent configurer Microsoft Defender SmartScreen pour un appareil individuel, sauf si la stratégie de groupe ou le service de Gestion des périphériques mobiles (MDM) est configuré pour l’empêcher. Pour plus d’informations, voir [configurer et utiliser Microsoft Defender SmartScreen sur des appareils individuels](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device).

## <a name="frequently-asked-questions"></a>Forum Aux Questions

### <a name="how-does-the-reputation-check-system-work"></a>Fonctionnement du système de vérification de la réputation

Lorsque vous naviguez sur le web, Microsoft Defender SmartScreen classe les sites web et les téléchargements en tant que trafic principal, dangereux ou inconnu. Le trafic principal concerne les sites populaires que Microsoft Defender SmartScreen a déterminés comme étant fiables. Si vous accédez à un site marqué comme dangereux, Microsoft Defender SmartScreen vous empêche immédiatement d’accéder au site. Lorsque vous accédez à un site inconnu, Microsoft DefenderSmartScreen vérifie sa réputation afin de déterminer si vous pouvez accéder au site.

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Vidéo : Sécuriser la navigation sur Microsoft Edge](microsoft-edge-video-security-smartscreen.md)
- [Présentation de Microsoft Defender SmartScreen](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview)
- [Protection contre les menaces](/windows/security/threat-protection/index)
- [Protection contre des applications potentiellement indésirables (PUA)](./microsoft-edge-potentially-unwanted-apps.md)