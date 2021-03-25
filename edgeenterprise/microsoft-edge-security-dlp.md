---
title: Protection contre la perte de données dans Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 03/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Protection contre la perte de données (DLP) dans Microsoft Edge
ms.openlocfilehash: ac34386ed1b691d7b45f30c2b2ec295955d11104
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447928"
---
# <a name="data-loss-prevention-dlp-in-microsoft-edge"></a>Protection contre la perte de données (DLP) dans Microsoft Edge

La protection contre la perte de données (DLP) est un système de technologies permettant d’identifier et de protéger les données d’entreprise sensibles contre la divulgation non autorisée. Pour se conformer aux normes d’entreprise et réglementations sectorielles, les organisations doivent protéger les informations sensibles et empêcher toute divulgation non autorisée. Les informations sensibles incluent les données financières ou les informations d’identification personnelle (PII) telles que les numéros de carte de crédit, les numéros de sécurité sociale ou les dossiers médicaux, et bien plus encore.

Le travail à distance a renforcé l’importance accordée à la protection contre la perte de données. Avec l’utilisation croissante des appareils pour les activités personnelles et professionnelles, les entreprises constatent un risque plus important de partage non autorisé de leurs données hors du lieu de travail.

Ce mélange d’activités des utilisateurs s’est également étendu aux appareils. Un transfert de données a alors lieu entre les appareils personnels et les appareils d’entreprise sur plusieurs réseaux publics et privés. Cela entraîne une augmentation considérable du risque d’exposition des données sensibles.

Microsoft Edge prend en charge en mode natif deux solutions DLP différentes: Microsoft Endpoint DLP et Protection des informations Windows (WIP).

## <a name="microsoft-endpoint-data-loss-prevention-endpoint-dlp"></a>Protection de perte de données de points de terminaison Microsoft (Endpoint DLP)

Protection de perte de données de points de terminaison Microsoft est la nouvelle génération de prévention de perte de données à l’aide de concepts modernes tels que la protection orientée données. Elle est intégrée à Windows 10 et à Microsoft Edge, de sorte qu’il n’a pas besoin d’agents ou de plug-ins supplémentaires sur l’appareil.

> [!NOTE]
> Ceci concerne MicrosoftEdge version85 ou ultérieure.

Pour en savoir plus sur le point de terminaison DLP, utilisez les ressources suivantes:

- [Vidéo: Microsoft Edge et la protection contre la perte de données (DLP)](microsoft-edge-video-security-dlp.md)
- [Découvrez la protection contre la perte de données de Point de terminaison Microsoft365](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide)
- [Prise en main de la protection contre la perte de données de point de terminaison](/microsoft-365/compliance/endpoint-dlp-getting-started?preserve-view=true&view=o365-worldwide)

Microsoft Edge applique les stratégies configurées par l’administrateur pour les fichiers sensibles et enregistre les événements d’audit sur les activités non conformes.

Vous pouvez auditer et gérer les activités suivantes des utilisateurs sur les appareils exécutant Windows10:

- Chargement des fichiers:protégez les fichiers sensibles contre le chargement dans des emplacements cloud non autorisés. <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- Protection du Presse-papiers: protégez les données sensibles contre toute copie hors du fichier.
- Protection contre les impressions: protégez les fichiers sensibles contre les impressions.
- Enregistrer sur un support USB/réseau: protégez les fichiers sensibles contre tout enregistrement sur un espace de stockage USB amovible ou à des emplacements réseau non autorisés.

Si vous souhaitez en savoir plus sur les activités des utilisateurs que vous pouvez auditer et gérer, veuillez consulter la rubrique [Activités de point de terminaison que vous pouvez surveiller et sur lesquelles vous pouvez agir](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).

## <a name="windows-information-protection"></a>Protection des informations Windows

Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Support pour la Protection des informations Windows](./microsoft-edge-security-windows-information-protection.md). Cette rubrique décrit comment Microsoft Edge prend en charge la protection des informations Windows (WIP). Si vous souhaitez en savoir plus sur la configuration requise, les avantages et les fonctionnalités prises en charge, veuillez consulter les sections suivantes:

- [Configuration système](./microsoft-edge-security-windows-information-protection.md#system-requirements)
- [Avantages de la Protection des informations Windows](./microsoft-edge-security-windows-information-protection.md#windows-information-protection-benefits)
- [Fonctionnalités WIP prises en charge dans Microsoft Edge](./microsoft-edge-security-windows-information-protection.md#wip-features-supported-in-microsoft-edge)

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Vidéo: protection contre la perte de données dans Microsoft Edge](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [Vue d'ensemble de la protection contre la perte de données](/microsoft-365/compliance/data-loss-prevention-policies?preserve-view=true&view=o365-worldwide)
- [Protéger vos données d’entreprise à l’aide de la Protection des informations Windows](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)