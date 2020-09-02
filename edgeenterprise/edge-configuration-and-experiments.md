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
ms.openlocfilehash: f66da4075c33c1f375dfb593c1a1bd2b4a139833
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979720"
---
# <span data-ttu-id="64f93-103">Configurations et expérimentation de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="64f93-103">Microsoft Edge configurations and experimentation</span></span>

<span data-ttu-id="64f93-104">Cet article décrit l’interaction entre MicrosoftEdge et le Service d’expérimentation et de configuration (ECS).</span><span class="sxs-lookup"><span data-stu-id="64f93-104">This article describes the interaction between Microsoft Edge and the Experimentation and Configuration Service (ECS).</span></span> <span data-ttu-id="64f93-105">MicrosoftEdge communique avec ce service pour demander et recevoir différents types de charges utiles.</span><span class="sxs-lookup"><span data-stu-id="64f93-105">Microsoft Edge communicates with this service to request and receive different kinds of payloads.</span></span> <span data-ttu-id="64f93-106">Ces charges utiles sont notamment les configurations, les déploiements de fonctionnalités et les expériences.</span><span class="sxs-lookup"><span data-stu-id="64f93-106">These payloads include configurations, feature rollouts, and experiments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64f93-107">Veuillez vous assurer que les clients peuvent accéder à `https://config.edge.skype.com` afin que les charges utiles soient reçues.</span><span class="sxs-lookup"><span data-stu-id="64f93-107">Make sure clients are able to access `https://config.edge.skype.com` so payloads can be received.</span></span>

> [!NOTE]
> <span data-ttu-id="64f93-108">Il concerne MicrosoftEdge version77 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="64f93-108">This applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="64f93-109">Configurations</span><span class="sxs-lookup"><span data-stu-id="64f93-109">Configurations</span></span>

<span data-ttu-id="64f93-110">Les configurations sont la charge utile destinée à garantir l’intégrité du produit, la sécurité et la conformité de la confidentialité. Elles sont conçues pour avoir la même valeur pour tous les utilisateurs (en fonction des plateformes et des canaux.) Il peut s’agir de l’activation d’un indicateur de fonctionnalité pour une action de domaine, qui peut également être utilisée pour désactiver un indicateur de fonctionnalité en cas de bogue.</span><span class="sxs-lookup"><span data-stu-id="64f93-110">Configurations are the payload meant to ensure product health, security, and privacy compliance, and are intended to have the same value for all the users (based on platforms and channels.) This could be to enable a feature flag for a domain action, and can also be used to disable a feature flag in the event of a bug.</span></span>

## <span data-ttu-id="64f93-111">Déploiement de fonctionnalités contrôlé</span><span class="sxs-lookup"><span data-stu-id="64f93-111">Controlled Feature Rollout</span></span>

<span data-ttu-id="64f93-112">Le déploiement de fonctionnalités contrôlé (CFR) est une procédure qui permet d’augmenter lentement la taille du groupe d’utilisateurs qui reçoit une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="64f93-112">Controlled Feature Rollout (CFR) is a procedure for slowly increasing the size of the user group that receives a feature.</span></span> <span data-ttu-id="64f93-113">En distribuant une nouvelle fonctionnalité à un sous-ensemble de la population d’utilisateurs sélectionné de façon aléatoire, il est possible de comparer les commentaires utilisateur à un groupe de contrôle de taille égale sans la fonctionnalité, afin de mesurer l’impact de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="64f93-113">By distributing a new feature to a randomly selected subset of the user population, it’s possible to compare user feedback to an equally sized control group without the feature to measure the impact of the feature.</span></span>

## <span data-ttu-id="64f93-114">Expériences</span><span class="sxs-lookup"><span data-stu-id="64f93-114">Experiments</span></span>

<span data-ttu-id="64f93-115">Les builds MicrosoftEdge ont des fonctionnalités et fonctions qui sont toujours en développement ou qui sont expérimentales.</span><span class="sxs-lookup"><span data-stu-id="64f93-115">Microsoft Edge builds have features and functionality that are still in development or are experimental.</span></span> <span data-ttu-id="64f93-116">Les expériences sont comme les CFR, mais la taille du groupe d’utilisateurs est plus petite pour tester le nouveau concept.</span><span class="sxs-lookup"><span data-stu-id="64f93-116">Experiments are like CFR, but the size of the user group is much smaller for testing the new concept.</span></span> <span data-ttu-id="64f93-117">Ces fonctionnalités sont masquées par défaut jusqu’à ce que la fonctionnalité déployée ou que l’expérience soit terminée.</span><span class="sxs-lookup"><span data-stu-id="64f93-117">These features are hidden by default until the feature's rolled out or the experiment's finished.</span></span> <span data-ttu-id="64f93-118">Les indicateurs d’expérience sont utilisés pour activer et désactiver ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="64f93-118">Experiment flags are used to enable and disable these features.</span></span>

## <span data-ttu-id="64f93-119">À propos de l’ECS</span><span class="sxs-lookup"><span data-stu-id="64f93-119">About the ECS</span></span>

<span data-ttu-id="64f93-120">Dans tous les scénarios précédents, le service fournit les valeurs d’indicateur de fonctionnalité au client de navigateur afin qu’elles puissent être appliquées.</span><span class="sxs-lookup"><span data-stu-id="64f93-120">In all the preceding scenarios, the service delivers the feature flag values to the browser client so they can be applied.</span></span> <span data-ttu-id="64f93-121">En fonction de la mise à jour, les configurations sont appliquées immédiatement ou lorsque l’utilisateur redémarre le navigateur.</span><span class="sxs-lookup"><span data-stu-id="64f93-121">Depending on the update, configurations are applied immediately or when the user restarts the browser.</span></span>

<span data-ttu-id="64f93-122">L’interaction de MicrosoftEdge avec ce service est contrôlée par les paramètres de la stratégie [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol).</span><span class="sxs-lookup"><span data-stu-id="64f93-122">Microsoft Edge's interaction with this service is controlled by settings in the [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) policy.</span></span> <span data-ttu-id="64f93-123">Vous pouvez configurer les paramètres de la stratégie de configuration de sorte à:</span><span class="sxs-lookup"><span data-stu-id="64f93-123">You can configure policy settings to:</span></span>

- <span data-ttu-id="64f93-124">Récupérer les configurations uniquement</span><span class="sxs-lookup"><span data-stu-id="64f93-124">Retrieve configurations only</span></span>
- <span data-ttu-id="64f93-125">Récupérer les configurations et les expérimentations</span><span class="sxs-lookup"><span data-stu-id="64f93-125">Retrieve configurations and experiments</span></span>
- <span data-ttu-id="64f93-126">Désactiver la communication avec le service</span><span class="sxs-lookup"><span data-stu-id="64f93-126">Disable communication with the service</span></span>

  > [!CAUTION]
  > <span data-ttu-id="64f93-127">Si vous désactivez les communications avec le service, cela affectera la capacité de Microsoft à répondre à un bogue grave en temps et en heure.</span><span class="sxs-lookup"><span data-stu-id="64f93-127">If you disable communications with the service, this will affect Microsoft’s ability to respond to a severe bug in a timely manner.</span></span>

## <span data-ttu-id="64f93-128">Articles associés</span><span class="sxs-lookup"><span data-stu-id="64f93-128">See also</span></span>

- [<span data-ttu-id="64f93-129">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="64f93-129">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="64f93-130">Page d’accueil de la documentation MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="64f93-130">Microsoft Edge documentation landing page</span></span>](https://docs.microsoft.com/DeployEdge/)
