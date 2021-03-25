---
title: Utilisation de Microsoft Edge pour se protéger contre des applications potentiellement indésirables
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 03/04/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Utilisation de Microsoft Edge pour se protéger contre des applications potentiellement indésirables
ms.openlocfilehash: 4e9d513c4d1144d4109064d7aa42e4ef31a59b88
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448028"
---
# <a name="protect-against-potentially-unwanted-applications-puas"></a>Protection contre des applications potentiellement indésirables (PUA)

Cet article vous explique la façon de vous protéger contre des applications potentiellement indésirables (PUA) à l’aide de Microsoft Edge ou de l’Antivirus Windows Defender.

> [!NOTE]
> Cet article concerne MicrosoftEdge version80 ou ultérieure.

## <a name="overview"></a>Vue d'ensemble

Les applications potentiellement indésirables ne sont pas désignées comme des virus ou des programmes malveillants, mais elles peuvent effectuer des actions sur les points de terminaison qui ont un impact négatif sur les performances ou l’utilisation des points de terminaison. Par exemple, le *logiciel Evasion* essaie activement d’éviter sa détection par des produits de sécurité. Ce type de logiciel peut augmenter le risque d’infection de votre réseau par de véritables programmes malveillants. Le terme PUA peut aussi désigner des applications ayant mauvaise réputation.

Pour obtenir une description des critères utilisés pour classifier le logiciel en tant que PUA, voir les [Applications potentiellement indésirables](/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).

## <a name="protect-against-pua-with-microsoft-edge"></a>Se protéger contre les PUA à l'aide de Microsoft Edge

Microsoft Edge (version 80.0.361.50 ou ultérieure) bloque les téléchargements PUA ainsi que les URL de ressources associées.

Vous pouvez configurer la protection en activant la fonctionnalité **Bloquer les applications potentiellement indésirables** dans Microsoft Edge.

> [!NOTE]
> La [publication du billet de l’équipe Microsoft Edge](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) décrit cette nouvelle fonctionnalité et explique comment gérer une application mal étiquetée un étiquetage ou signaler une application comme indésirable.

### <a name="to-enable-pua-protection"></a>Pour activer la protection PUA:

1. Ouvrez les **Paramètres** dans le navigateur.
2. Sélectionnez **Confidentialité et services**.
3. Dans la section **Services**, vérifiez que **Microsoft Defender SmartScreen** est activé. Dans le cas contraire, activez Microsoft Defender SmartScreen. L’exemple de la capture d’écran ci-après indique que le navigateur est géré par l’organisation et que Microsoft Defender SmartScreen est activé.

   ![Activer Microsoft Edge PUA dans les Paramètres](./media/microsoft-edge-potentially-unwanted-apps/security-pua-setup.png)

4. Dans la section **Services**, utilisez le bouton bascule présenté dans la capture d’écran précédente pour activer **Bloquer les applications potentiellement indésirables**.

   > [!TIP]
   > Vous pouvez en toute sécurité explorer la fonctionnalité de blocage d’URL de la protection PUA en la testant sur l’un de nos pages de démonstration de [Windows Defender SmartScreen](https://demo.smartscreen.msft.net/).

Si Microsoft Edge détecte une PUA, un message semblable à celui de la capture d’écran suivante s’affiche.

   ![Message d’avertissement de Microsoft Edge PUA](./media/microsoft-edge-potentially-unwanted-apps/security-pua-msg.png)

### <a name="to-block-against-pua-associated-urls"></a>Pour empêcher les URL associées à la protection PUA

Après avoir activé la protection PUA dans Microsoft Edge, Windows Defender SmartScreen vous protège des URL associées à PUA.

Les administrateurs peuvent configurer le fonctionnement conjoint de Microsoft Edge et Windows Defender SmartScreen pour protéger les utilisateurs contre des URL associées à PUA. Pour plus d’informations, voir:

- [Configurer les paramètres de stratégie MicrosoftEdge sur Windows](./configure-microsoft-edge.md)
- [Paramètres SmartScreen](./microsoft-edge-policies.md#smartscreen-settings)
- [Stratégie SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled)
- [Configurer Windows Defender SmartScreen](/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen)

Les administrateurs peuvent également personnaliser la liste de blocage de la Microsoft Defender Protection avancée contre les menaces (Microsoft Defender ATP). Ils peuvent utiliser le portail Microsoft Defender Protection avancée contre les menaces pour [créer et gérer des indicateurs pour les adresses IP et les URL](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).

## <a name="protect-against-pua-with-windows-defender-antivirus"></a>Protégez-vous contre PUA à l’aide de l’Antivirus Windows Defender

L'article sur la [Détection et le blocage des applications potentiellement indésirables](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) explique également comment configurer l’antivirus Windows Defender pour activer la protection PUA. Vous pouvez configurer la protection en utilisant l’une des options suivantes:

- [MicrosoftIntune](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-intune-to-configure-pua-protection)
- [Microsoft Endpoint Configuration Manager](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-configuration-manager-to-configure-pua-protection)
- [Stratégie de groupe](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-group-policy-to-configure-pua-protection)
- [Applets de commande PowerShell](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)

Lorsque Windows Defender détecte un fichier PUA sur un point de terminaison, il met le fichier en quarantaine et avertit l’utilisateur ([sauf si les notifications sont désactivées](/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)) dans le même format que celui de la détection de menace normale (précédée de «PUA:»). Les menaces détectées apparaissent également dans la [liste de mise en quarantaine dans l'application Sécurité Windows](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history).

### <a name="pua-notifications-and-events"></a>Évènements et notifications PUA

Un administrateur peut accéder aux événements PUA de plusieurs manières:

- Dans l’observateur d’événements Windows, mais pas dans le Gestionnaire de configuration de point de terminaison Microsoft ou Intune.
- Dans un e-mail si la notification par courrier électronique est activée pour les détections PUA.
- Dans les journaux d'évènements de [Antivirus Windows Defender](/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus), où un événement PUA est enregistré sous l’ID d’événement1116 avec le message: «La plateforme anti-programme malveillant a détecté des programmes malveillants ou d’autres logiciels potentiellement indésirables».

> [!NOTE]
> L’utilisateur pourra voir «*.exe a été bloqué en tant qu'application potentiellement indésirable par Microsoft Defender SmartScreen».

### <a name="allow-list-an-app"></a>Autoriser une application sur une liste verte

Tout comme Microsoft Edge, l’Antivirus Windows Defender offre un moyen d’autoriser les fichiers bloqués par erreur ou nécessaires à l’exécution d’une tâche. Si cela se produit, vous pouvez autoriser le fichier sur une liste verte. Pour plus d’informations, voir la [Configuration de la protection des points de terminaison dans Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders) pour découvrir comment exclure des fichiers ou des dossiers spécifiques.

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Protection contre les menaces](/windows/security/threat-protection/index)
- [Configurer la protection en temps réel, heuristique et comportementale](/windows/security/threat-protection/windows-defender-antivirus/configure-protection-features-windows-defender-antivirus)
- [Protection de nouvelle génération](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-antivirus-in-windows-10)
- [Base de sécurité pour Microsoft Edge basé sur Chromium, version79](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/security-baseline-final-for-chromium-based-microsoft-edge/ba-p/1111863)