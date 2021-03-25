---
title: Configurations et expérimentation de Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurations et expérimentation de Microsoft Edge
ms.openlocfilehash: aef19fd9c119926a934a1ab00009a89ce2fe31fc
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447768"
---
# <a name="microsoft-edge-configurations-and-experimentation"></a><span data-ttu-id="222e4-103">Configurations et expérimentation de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="222e4-103">Microsoft Edge configurations and experimentation</span></span>

<span data-ttu-id="222e4-104">Cet article décrit l’interaction entre MicrosoftEdge et le Service d’expérimentation et de configuration (ECS).</span><span class="sxs-lookup"><span data-stu-id="222e4-104">This article describes the interaction between Microsoft Edge and the Experimentation and Configuration Service (ECS).</span></span> <span data-ttu-id="222e4-105">MicrosoftEdge communique avec ce service pour demander et recevoir différents types de charges utiles.</span><span class="sxs-lookup"><span data-stu-id="222e4-105">Microsoft Edge communicates with this service to request and receive different kinds of payloads.</span></span> <span data-ttu-id="222e4-106">Ces charges utiles sont notamment les configurations, les déploiements de fonctionnalités et les expériences.</span><span class="sxs-lookup"><span data-stu-id="222e4-106">These payloads include configurations, feature rollouts, and experiments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="222e4-107">Veuillez vous assurer que les clients peuvent accéder à `https://config.edge.skype.com` afin que les charges utiles soient reçues.</span><span class="sxs-lookup"><span data-stu-id="222e4-107">Make sure clients are able to access `https://config.edge.skype.com` so payloads can be received.</span></span>

> [!NOTE]
> <span data-ttu-id="222e4-108">Il concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="222e4-108">This applies to Microsoft Edge version 77 or later.</span></span>

## <a name="configurations"></a><span data-ttu-id="222e4-109">Configurations</span><span class="sxs-lookup"><span data-stu-id="222e4-109">Configurations</span></span>

<span data-ttu-id="222e4-110">Les configurations sont la charge utile destinée à garantir l’intégrité du produit, la sécurité et la conformité de la confidentialité. Elles sont conçues pour avoir la même valeur pour tous les utilisateurs (en fonction des plateformes et des canaux.) Il peut s’agir de l’activation d’un indicateur de fonctionnalité pour une action de domaine, qui peut également être utilisée pour désactiver un indicateur de fonctionnalité en cas de bogue.</span><span class="sxs-lookup"><span data-stu-id="222e4-110">Configurations are the payload meant to ensure product health, security, and privacy compliance, and are intended to have the same value for all the users (based on platforms and channels.) This could be to enable a feature flag for a domain action, and can also be used to disable a feature flag in the event of a bug.</span></span>

## <a name="controlled-feature-rollout"></a><span data-ttu-id="222e4-111">Déploiement de fonctionnalités contrôlé</span><span class="sxs-lookup"><span data-stu-id="222e4-111">Controlled Feature Rollout</span></span>

<span data-ttu-id="222e4-112">Le déploiement de fonctionnalités contrôlé (CFR) est une procédure qui permet d’augmenter lentement la taille du groupe d’utilisateurs qui reçoit une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="222e4-112">Controlled Feature Rollout (CFR) is a procedure for slowly increasing the size of the user group that receives a feature.</span></span> <span data-ttu-id="222e4-113">En distribuant une nouvelle fonctionnalité à un sous-ensemble de la population d’utilisateurs sélectionné de façon aléatoire, il est possible de comparer les commentaires utilisateur à un groupe de contrôle de taille égale sans la fonctionnalité, afin de mesurer l’impact de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="222e4-113">By distributing a new feature to a randomly selected subset of the user population, it’s possible to compare user feedback to an equally sized control group without the feature to measure the impact of the feature.</span></span>

## <a name="experiments"></a><span data-ttu-id="222e4-114">Expériences</span><span class="sxs-lookup"><span data-stu-id="222e4-114">Experiments</span></span>

<span data-ttu-id="222e4-115">Les builds MicrosoftEdge ont des fonctionnalités et fonctions qui sont toujours en développement ou qui sont expérimentales.</span><span class="sxs-lookup"><span data-stu-id="222e4-115">Microsoft Edge builds have features and functionality that are still in development or are experimental.</span></span> <span data-ttu-id="222e4-116">Les expériences sont comme les CFR, mais la taille du groupe d’utilisateurs est plus petite pour tester le nouveau concept.</span><span class="sxs-lookup"><span data-stu-id="222e4-116">Experiments are like CFR, but the size of the user group is much smaller for testing the new concept.</span></span> <span data-ttu-id="222e4-117">Ces fonctionnalités sont masquées par défaut jusqu’à ce que la fonctionnalité déployée ou que l’expérience soit terminée.</span><span class="sxs-lookup"><span data-stu-id="222e4-117">These features are hidden by default until the feature's rolled out or the experiment's finished.</span></span> <span data-ttu-id="222e4-118">Les indicateurs d’expérience sont utilisés pour activer et désactiver ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="222e4-118">Experiment flags are used to enable and disable these features.</span></span>

## <a name="about-the-ecs"></a><span data-ttu-id="222e4-119">À propos de l’ECS</span><span class="sxs-lookup"><span data-stu-id="222e4-119">About the ECS</span></span>

<span data-ttu-id="222e4-120">Dans tous les scénarios précédents, le service fournit les valeurs d’indicateur de fonctionnalité au client de navigateur afin qu’elles puissent être appliquées.</span><span class="sxs-lookup"><span data-stu-id="222e4-120">In all the preceding scenarios, the service delivers the feature flag values to the browser client so they can be applied.</span></span> <span data-ttu-id="222e4-121">En fonction de la mise à jour, les configurations sont appliquées immédiatement ou lorsque l’utilisateur redémarre le navigateur.</span><span class="sxs-lookup"><span data-stu-id="222e4-121">Depending on the update, configurations are applied immediately or when the user restarts the browser.</span></span>

<span data-ttu-id="222e4-122">L’interaction de MicrosoftEdge avec ce service est contrôlée par les paramètres de la stratégie [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol).</span><span class="sxs-lookup"><span data-stu-id="222e4-122">Microsoft Edge's interaction with this service is controlled by settings in the [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) policy.</span></span> <span data-ttu-id="222e4-123">Vous pouvez configurer les paramètres de la stratégie de configuration de sorte à:</span><span class="sxs-lookup"><span data-stu-id="222e4-123">You can configure policy settings to:</span></span>

- <span data-ttu-id="222e4-124">Récupérer les configurations uniquement</span><span class="sxs-lookup"><span data-stu-id="222e4-124">Retrieve configurations only</span></span>
- <span data-ttu-id="222e4-125">Récupérer les configurations et les expérimentations</span><span class="sxs-lookup"><span data-stu-id="222e4-125">Retrieve configurations and experiments</span></span>
- <span data-ttu-id="222e4-126">Désactiver la communication avec le service</span><span class="sxs-lookup"><span data-stu-id="222e4-126">Disable communication with the service</span></span>

  > [!CAUTION]
  > <span data-ttu-id="222e4-127">Si vous désactivez les communications avec le service, cela affectera la capacité de Microsoft à répondre à un bogue grave en temps et en heure.</span><span class="sxs-lookup"><span data-stu-id="222e4-127">If you disable communications with the service, this will affect Microsoft’s ability to respond to a severe bug in a timely manner.</span></span>

## <a name="see-also"></a><span data-ttu-id="222e4-128">Articles associés</span><span class="sxs-lookup"><span data-stu-id="222e4-128">See also</span></span>

- [<span data-ttu-id="222e4-129">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="222e4-129">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="222e4-130">Page d’accueil de la documentation MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="222e4-130">Microsoft Edge documentation landing page</span></span>](./index.yml)