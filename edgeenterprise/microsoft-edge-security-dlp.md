---
title: Protection contre la perte de données dans Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Protection contre la perte de données (DLP) dans Microsoft Edge
ms.openlocfilehash: 8c7906f69f8d1161b47aa381bc04bcdaa70fe6cd
ms.sourcegitcommit: c290b0b0fa6b7d7f94dcdfdda91302da733326ec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314557"
---
# Protection contre la perte de données (DLP) dans Microsoft Edge

La protection contre la perte de données (DLP) est un système de technologies permettant d’identifier et de protéger les données d’entreprise sensibles contre la divulgation non autorisée. Pour se conformer aux normes d’entreprise et réglementations sectorielles, les organisations doivent protéger les informations sensibles et empêcher toute divulgation non autorisée. Les informations sensibles incluent les données financières ou les informations d’identification personnelle (PII) telles que les numéros de carte de crédit, les numéros de sécurité sociale ou les dossiers médicaux, et bien plus encore.

Le travail à distance a renforcé l’importance accordée à la protection contre la perte de données. Avec l’utilisation croissante des appareils pour les activités personnelles et professionnelles, les entreprises constatent un risque plus important de partage non autorisé de leurs données hors du lieu de travail.

Ce mélange d’activités des utilisateurs s’est également étendu aux appareils. Un transfert de données a alors lieu entre les appareils personnels et les appareils d’entreprise sur plusieurs réseaux publics et privés. Cela entraîne une augmentation considérable du risque d’exposition des données sensibles.

Microsoft Edge prend en charge en mode natif deux solutions DLP différentes : Microsoft Endpoint DLP et Protection des informations Windows (WIP).

## Protection de perte de données de points de terminaison Microsoft (Endpoint DLP)

Protection de perte de données de points de terminaison Microsoft est la nouvelle génération de prévention de perte de données à l’aide de concepts modernes tels que la protection orientée données. Elle est intégrée à Windows 10 et à Microsoft Edge, de sorte qu’il n’a pas besoin d’agents ou de plug-ins supplémentaires sur l’appareil.

> [!NOTE]
> Ceci concerne Microsoft Edge version 85 ou ultérieure.

Pour en savoir plus sur le point de terminaison DLP, utilisez les ressources suivantes :

- [Vidéo : Microsoft Edge et la protection contre la perte de données (DLP)](microsoft-edge-video-security-dlp.md)
- [Découvrez la protection contre la perte de données de Point de terminaison Microsoft 365](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide&preserve-view=true)
- [Prise en main de la protection contre la perte de données de point de terminaison](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-getting-started?view=o365-worldwide&preserve-view=true)

Microsoft Edge applique les stratégies configurées par l’administrateur pour les fichiers sensibles et enregistre les événements d’audit sur les activités non conformes.

Vous pouvez auditer et gérer les activités suivantes des utilisateurs sur les appareils exécutant Windows 10 :

- Chargement des fichiers : protégez les fichiers sensibles contre le chargement dans des emplacements cloud non autorisés. <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- Protection du Presse-papiers : protégez les données sensibles contre toute copie hors du fichier.
- Protection contre les impressions : protégez les fichiers sensibles contre les impressions.
- Enregistrer sur un support USB/réseau : protégez les fichiers sensibles contre tout enregistrement sur un espace de stockage USB amovible ou à des emplacements réseau non autorisés.

Si vous souhaitez en savoir plus sur les activités des utilisateurs que vous pouvez auditer et gérer, veuillez consulter la rubrique [Activités de point de terminaison que vous pouvez surveiller et sur lesquelles vous pouvez agir](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on&preserve-view=true).

## Protection des informations Windows

Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Support pour la Protection des informations Windows](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection). Cette rubrique décrit comment Microsoft Edge prend en charge la protection des informations Windows (WIP). Si vous souhaitez en savoir plus sur la configuration requise, les avantages et les fonctionnalités prises en charge, veuillez consulter les sections suivantes :

- [Configuration système](https://docs.microsoft.com/deployedge/:microsoft-edge-security-windows-information-protection#system-requirements)
- [Avantages de la Protection des informations Windows](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#windows-information-protection-benefits)
- [Fonctionnalités WIP prises en charge dans Microsoft Edge](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection#wip-features-supported-in-microsoft-edge)

## Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Vidéo : protection contre la perte de données dans Microsoft Edge](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [Vue d'ensemble de la protection contre la perte de données](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide&preserve-view=true)
- [Protéger vos données d’entreprise à l’aide de la Protection des informations Windows](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
