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
ms.openlocfilehash: f25e1fa7a610645f6ca0ca10cbcfc69ae8689b7a
ms.sourcegitcommit: f14286edec59ee9183bdf38c15fc890881efd64f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "11384982"
---
# <a name="data-loss-prevention-dlp-in-microsoft-edge"></a><span data-ttu-id="f6a04-103">Protection contre la perte de données (DLP) dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f6a04-103">Data Loss Prevention (DLP) in Microsoft Edge</span></span>

<span data-ttu-id="f6a04-104">La protection contre la perte de données (DLP) est un système de technologies permettant d’identifier et de protéger les données d’entreprise sensibles contre la divulgation non autorisée.</span><span class="sxs-lookup"><span data-stu-id="f6a04-104">Data loss prevention (DLP) is a system of technologies that identify and safeguard sensitive enterprise data from unauthorized disclosure.</span></span> <span data-ttu-id="f6a04-105">Pour se conformer aux normes d’entreprise et réglementations sectorielles, les organisations doivent protéger les informations sensibles et empêcher toute divulgation non autorisée.</span><span class="sxs-lookup"><span data-stu-id="f6a04-105">To comply with business standards and industry regulations, organizations must protect sensitive information and prevent its unauthorized disclosure.</span></span> <span data-ttu-id="f6a04-106">Les informations sensibles incluent les données financières ou les informations d’identification personnelle (PII) telles que les numéros de carte de crédit, les numéros de sécurité sociale ou les dossiers médicaux, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="f6a04-106">Sensitive information includes financial data or personally identifiable information (PII) such as credit card numbers, social security numbers, or health records, among many other things.</span></span>

<span data-ttu-id="f6a04-107">Le travail à distance a renforcé l’importance accordée à la protection contre la perte de données.</span><span class="sxs-lookup"><span data-stu-id="f6a04-107">Remote work has increased the emphasis on using DLP.</span></span> <span data-ttu-id="f6a04-108">Avec l’utilisation croissante des appareils pour les activités personnelles et professionnelles, les entreprises constatent un risque plus important de partage non autorisé de leurs données hors du lieu de travail.</span><span class="sxs-lookup"><span data-stu-id="f6a04-108">With the growing use of personal and work activities on devices, enterprises are seeing an increased risk of unauthorized sharing of corporate data outside the workplace.</span></span>

<span data-ttu-id="f6a04-109">Ce mélange d’activités des utilisateurs s’est également étendu aux appareils. Un transfert de données a alors lieu entre les appareils personnels et les appareils d’entreprise sur plusieurs réseaux publics et privés.</span><span class="sxs-lookup"><span data-stu-id="f6a04-109">This blending of user activities has spread to devices as well, where data is moved between personal and corporate devices over a variety of public and private networks.</span></span> <span data-ttu-id="f6a04-110">Cela entraîne une augmentation considérable du risque d’exposition des données sensibles.</span><span class="sxs-lookup"><span data-stu-id="f6a04-110">The net result is a dramatically increased risk of exposing sensitive data.</span></span>

<span data-ttu-id="f6a04-111">Microsoft Edge prend en charge en mode natif deux solutions DLP différentes: Microsoft Endpoint DLP et Protection des informations Windows (WIP).</span><span class="sxs-lookup"><span data-stu-id="f6a04-111">Microsoft Edge natively supports two different DLP solutions, Microsoft Endpoint DLP and Windows Information Protection (WIP).</span></span>

## <a name="microsoft-endpoint-data-loss-prevention-endpoint-dlp"></a><span data-ttu-id="f6a04-112">Protection de perte de données de points de terminaison Microsoft (Endpoint DLP)</span><span class="sxs-lookup"><span data-stu-id="f6a04-112">Microsoft Endpoint data loss prevention (Endpoint DLP)</span></span>

<span data-ttu-id="f6a04-113">Protection de perte de données de points de terminaison Microsoft est la nouvelle génération de prévention de perte de données à l’aide de concepts modernes tels que la protection orientée données.</span><span class="sxs-lookup"><span data-stu-id="f6a04-113">Microsoft Endpoint DLP is the next generation of data loss prevention using modern concepts such as data-centric protection.</span></span> <span data-ttu-id="f6a04-114">Elle est intégrée à Windows 10 et à Microsoft Edge, de sorte qu’il n’a pas besoin d’agents ou de plug-ins supplémentaires sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f6a04-114">It's built-in to Windows 10 and Microsoft Edge so it doesn't need additional agents or plugins on the device.</span></span>

> [!NOTE]
> <span data-ttu-id="f6a04-115">Ceci concerne MicrosoftEdge version85 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f6a04-115">This applies to Microsoft Edge version 85 or later.</span></span>

<span data-ttu-id="f6a04-116">Pour en savoir plus sur le point de terminaison DLP, utilisez les ressources suivantes:</span><span class="sxs-lookup"><span data-stu-id="f6a04-116">To learn more about Endpoint DLP, use the following resources:</span></span>

- [<span data-ttu-id="f6a04-117">Vidéo: Microsoft Edge et la protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="f6a04-117">Video: Microsoft Edge and Data loss prevention (DLP)</span></span>](microsoft-edge-video-security-dlp.md)
- [<span data-ttu-id="f6a04-118">Découvrez la protection contre la perte de données de Point de terminaison Microsoft365</span><span class="sxs-lookup"><span data-stu-id="f6a04-118">Learn about Microsoft 365 Endpoint data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide&preserve-view=true)
- [<span data-ttu-id="f6a04-119">Prise en main de la protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f6a04-119">Get started with Endpoint data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-getting-started?view=o365-worldwide&preserve-view=true)

<span data-ttu-id="f6a04-120">Microsoft Edge applique les stratégies configurées par l’administrateur pour les fichiers sensibles et enregistre les événements d’audit sur les activités non conformes.</span><span class="sxs-lookup"><span data-stu-id="f6a04-120">Microsoft Edge enforces admin configured policies for sensitive files and records audit events for non-compliant activities.</span></span>

<span data-ttu-id="f6a04-121">Vous pouvez auditer et gérer les activités suivantes des utilisateurs sur les appareils exécutant Windows10:</span><span class="sxs-lookup"><span data-stu-id="f6a04-121">Some of the user activities that you can audit and manage on devices running Windows 10 include the following activities:</span></span>

- <span data-ttu-id="f6a04-122">Chargement des fichiers:protégez les fichiers sensibles contre le chargement dans des emplacements cloud non autorisés.</span><span class="sxs-lookup"><span data-stu-id="f6a04-122">File Upload: Protect sensitive file upload to unauthorized cloud locations.</span></span> <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- <span data-ttu-id="f6a04-123">Protection du Presse-papiers: protégez les données sensibles contre toute copie hors du fichier.</span><span class="sxs-lookup"><span data-stu-id="f6a04-123">Clipboard Protection: Protect sensitive data from being copied out of the file.</span></span>
- <span data-ttu-id="f6a04-124">Protection contre les impressions: protégez les fichiers sensibles contre les impressions.</span><span class="sxs-lookup"><span data-stu-id="f6a04-124">Print Protection: Protect sensitive file from being printed.</span></span>
- <span data-ttu-id="f6a04-125">Enregistrer sur un support USB/réseau: protégez les fichiers sensibles contre tout enregistrement sur un espace de stockage USB amovible ou à des emplacements réseau non autorisés.</span><span class="sxs-lookup"><span data-stu-id="f6a04-125">Save to USB/Network: Protect sensitive file from being saved to removable USB storage or unauthorized network locations.</span></span>

<span data-ttu-id="f6a04-126">Si vous souhaitez en savoir plus sur les activités des utilisateurs que vous pouvez auditer et gérer, veuillez consulter la rubrique [Activités de point de terminaison que vous pouvez surveiller et sur lesquelles vous pouvez agir](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="f6a04-126">For more detailed information about user activities you can audit and manage, see [Endpoint activities you can monitor and take action on](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on&preserve-view=true).</span></span>

## <a name="windows-information-protection"></a><span data-ttu-id="f6a04-127">Protection des informations Windows</span><span class="sxs-lookup"><span data-stu-id="f6a04-127">Windows Information Protection</span></span>

<span data-ttu-id="f6a04-128">Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Support pour la Protection des informations Windows](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection). Cette rubrique décrit comment Microsoft Edge prend en charge la protection des informations Windows (WIP).</span><span class="sxs-lookup"><span data-stu-id="f6a04-128">Check out [Support for Windows Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection), which describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span> <span data-ttu-id="f6a04-129">Si vous souhaitez en savoir plus sur la configuration requise, les avantages et les fonctionnalités prises en charge, veuillez consulter les sections suivantes:</span><span class="sxs-lookup"><span data-stu-id="f6a04-129">You can learn moe about system requirements, benefits, and supported features in the following sections:</span></span>

- [<span data-ttu-id="f6a04-130">Configuration système</span><span class="sxs-lookup"><span data-stu-id="f6a04-130">System Requirements</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#system-requirements)
- [<span data-ttu-id="f6a04-131">Avantages de la Protection des informations Windows</span><span class="sxs-lookup"><span data-stu-id="f6a04-131">Windows Information Protection Benefits</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#windows-information-protection-benefits)
- [<span data-ttu-id="f6a04-132">Fonctionnalités WIP prises en charge dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f6a04-132">WIP features supported in Microsoft Edge</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection#wip-features-supported-in-microsoft-edge)

## <a name="see-also"></a><span data-ttu-id="f6a04-133">Voir également</span><span class="sxs-lookup"><span data-stu-id="f6a04-133">See also</span></span>

- [<span data-ttu-id="f6a04-134">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="f6a04-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f6a04-135">Vidéo: protection contre la perte de données dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f6a04-135">Video: Data loss prevention - Microsoft Edge</span></span>](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [<span data-ttu-id="f6a04-136">Vue d'ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="f6a04-136">Overview of data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide&preserve-view=true)
- [<span data-ttu-id="f6a04-137">Protéger vos données d’entreprise à l’aide de la Protection des informations Windows</span><span class="sxs-lookup"><span data-stu-id="f6a04-137">Protect your enterprise data using Windows Information Protection</span></span>](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
