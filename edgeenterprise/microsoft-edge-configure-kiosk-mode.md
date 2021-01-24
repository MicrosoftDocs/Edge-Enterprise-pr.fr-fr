---
title: Configurer Microsoft Edge en mode plein écran
ms.author: aguta
author: aguta
manager: srugh
ms.date: 01/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer Microsoft Edge en mode plein écran
ms.openlocfilehash: be353a0e13e9234de40296a2e8dcc31b1b800f52
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297470"
---
# <span data-ttu-id="223f7-103">Configurer Microsoft Edge en mode plein écran</span><span class="sxs-lookup"><span data-stu-id="223f7-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="223f7-104">Cet article décrit la configuration des options Microsoft Edge en mode plein écran que vous pouvez piloter.</span><span class="sxs-lookup"><span data-stu-id="223f7-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="223f7-105">Il existe également une feuille de route des fonctionnalités que nous ciblons.</span><span class="sxs-lookup"><span data-stu-id="223f7-105">There's also a roadmap of features we're targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="223f7-106">Cet article concerne MicrosoftEdge version87 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="223f7-106">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="223f7-107">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="223f7-107">Overview</span></span>

<span data-ttu-id="223f7-108">Microsoft Edge en mode plein écran offre deux expériences de verrouillage du navigateur afin de permettre aux organisations de créer, gérer et offrir une expérience optimale pour leurs clients.</span><span class="sxs-lookup"><span data-stu-id="223f7-108">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="223f7-109">Les expériences de verrouillage suivantes sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="223f7-109">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="223f7-110">**Expérience de connexion numérique/interactive** : affiche un site spécifique en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="223f7-110">**Digital/Interactive Signage** experience - Displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="223f7-111">**Expérience de navigation publique** : exécute une version multi-onglet limitée de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="223f7-111">**Public-Browsing** experience - Runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="223f7-112">Les deux expériences exécutent une session MicrosoftEdge InPrivate qui protège les données de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="223f7-112">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="223f7-113">Configurer MicrosoftEdge en mode plein écran</span><span class="sxs-lookup"><span data-stu-id="223f7-113">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="223f7-114">Un ensemble initial de fonctionnalités du mode plein écran est disponible pour le test avec le canal stable MicrosoftEdge, version87.</span><span class="sxs-lookup"><span data-stu-id="223f7-114">An initial set of kiosk mode features is available to test with Microsoft Edge Stable Channel, version 87.</span></span> <span data-ttu-id="223f7-115">Vous pouvez télécharger la dernière version à partir [de MicrosoftEdge (canal stable officiel).](https://www.microsoft.com/edge)</span><span class="sxs-lookup"><span data-stu-id="223f7-115">You can download the latest version from [Microsoft Edge (Official Stable Channel)](https://www.microsoft.com/edge).</span></span>

### <span data-ttu-id="223f7-116">Fonctionnalités prise en charge en mode plein écran</span><span class="sxs-lookup"><span data-stu-id="223f7-116">Kiosk mode supported features</span></span>

<span data-ttu-id="223f7-117">Le tableau suivant répertorie les fonctionnalités prises en charge par le mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="223f7-117">The following table lists the features supported by kiosk mode.</span></span>

|<span data-ttu-id="223f7-118">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="223f7-118">Feature</span></span>|<span data-ttu-id="223f7-119">Connexion numérique/interactive</span><span class="sxs-lookup"><span data-stu-id="223f7-119">Digital\Interactive Signage</span></span>|<span data-ttu-id="223f7-120">Navigation publique</span><span class="sxs-lookup"><span data-stu-id="223f7-120">Public browsing</span></span>|<span data-ttu-id="223f7-121">Disponible avec la version de MicrosoftEdge (et versions supérieures)</span><span class="sxs-lookup"><span data-stu-id="223f7-121">Available with Microsoft Edge version (and higher)</span></span>|
|-|-|-|-|
|<span data-ttu-id="223f7-122">Navigation InPrivate</span><span class="sxs-lookup"><span data-stu-id="223f7-122">InPrivate Navigation</span></span>|<span data-ttu-id="223f7-123">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-123">Y</span></span>|<span data-ttu-id="223f7-124">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-124">Y</span></span>|<span data-ttu-id="223f7-125">87</span><span class="sxs-lookup"><span data-stu-id="223f7-125">87</span></span>|
|<span data-ttu-id="223f7-126">Réinitialiser en période d’inactivité</span><span class="sxs-lookup"><span data-stu-id="223f7-126">Reset on inactivity</span></span>|<span data-ttu-id="223f7-127">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-127">Y</span></span>|<span data-ttu-id="223f7-128">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-128">Y</span></span>|<span data-ttu-id="223f7-129">87</span><span class="sxs-lookup"><span data-stu-id="223f7-129">87</span></span>|
|<span data-ttu-id="223f7-130">[Barre d’adresses en lecture seule](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (stratégie)</span><span class="sxs-lookup"><span data-stu-id="223f7-130">[Read only address bar](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (policy)</span></span> |<span data-ttu-id="223f7-131">N</span><span class="sxs-lookup"><span data-stu-id="223f7-131">N</span></span>|<span data-ttu-id="223f7-132">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-132">Y</span></span> |<span data-ttu-id="223f7-133">87</span><span class="sxs-lookup"><span data-stu-id="223f7-133">87</span></span>|
|<span data-ttu-id="223f7-134">[Supprimer les téléchargements à la sortie](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (stratégie)</span><span class="sxs-lookup"><span data-stu-id="223f7-134">[Delete downloads on exit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (policy)</span></span>  | <span data-ttu-id="223f7-135">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-135">Y</span></span>|<span data-ttu-id="223f7-136">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-136">Y</span></span> |<span data-ttu-id="223f7-137">87</span><span class="sxs-lookup"><span data-stu-id="223f7-137">87</span></span>|
|<span data-ttu-id="223f7-138">F11 bloqué (entrée/sortie en plein écran)</span><span class="sxs-lookup"><span data-stu-id="223f7-138">F11 blocked (enter/exit full-screen)</span></span> | <span data-ttu-id="223f7-139">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-139">Y</span></span> | <span data-ttu-id="223f7-140">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-140">Y</span></span> | <span data-ttu-id="223f7-141">87</span><span class="sxs-lookup"><span data-stu-id="223f7-141">87</span></span> |
|<span data-ttu-id="223f7-142">F12 bloqué (lancer les outils de développement)</span><span class="sxs-lookup"><span data-stu-id="223f7-142">F12 blocked (launch Developer Tools)</span></span> | <span data-ttu-id="223f7-143">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-143">Y</span></span> | <span data-ttu-id="223f7-144">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-144">Y</span></span> | <span data-ttu-id="223f7-145">87</span><span class="sxs-lookup"><span data-stu-id="223f7-145">87</span></span> |
| <span data-ttu-id="223f7-146">Prise en charge de plusieurs onglets</span><span class="sxs-lookup"><span data-stu-id="223f7-146">Multi tab support</span></span> | <span data-ttu-id="223f7-147">N</span><span class="sxs-lookup"><span data-stu-id="223f7-147">N</span></span>| <span data-ttu-id="223f7-148">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-148">Y</span></span>| <span data-ttu-id="223f7-149">87</span><span class="sxs-lookup"><span data-stu-id="223f7-149">87</span></span>|
|<span data-ttu-id="223f7-150">Bouton Terminer la session</span><span class="sxs-lookup"><span data-stu-id="223f7-150">End session button</span></span> | <span data-ttu-id="223f7-151">N</span><span class="sxs-lookup"><span data-stu-id="223f7-151">N</span></span>| <span data-ttu-id="223f7-152">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-152">Y</span></span>| <span data-ttu-id="223f7-153">88</span><span class="sxs-lookup"><span data-stu-id="223f7-153">88</span></span>|
|<span data-ttu-id="223f7-154">Toutes les URL MicrosoftEdge internes sont bloquées, à l’exception de *edge://downloads* et *edge://print*</span><span class="sxs-lookup"><span data-stu-id="223f7-154">All internal Microsoft Edge URLs are blocked, except for *edge://downloads* and *edge://print*</span></span> |<span data-ttu-id="223f7-155">N</span><span class="sxs-lookup"><span data-stu-id="223f7-155">N</span></span>|<span data-ttu-id="223f7-156">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-156">Y</span></span>|<span data-ttu-id="223f7-157">88</span><span class="sxs-lookup"><span data-stu-id="223f7-157">88</span></span>|
| <span data-ttu-id="223f7-158">Ctrl+N bloqué (ouvrir une nouvelle fenêtre)</span><span class="sxs-lookup"><span data-stu-id="223f7-158">CTRL+N blocked (open a new window)</span></span> | <span data-ttu-id="223f7-159">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-159">Y</span></span> | <span data-ttu-id="223f7-160">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-160">Y</span></span> | <span data-ttu-id="223f7-161">89</span><span class="sxs-lookup"><span data-stu-id="223f7-161">89</span></span> |
| <span data-ttu-id="223f7-162">Ctrl+T bloqué (ouvrir un nouvel onglet)</span><span class="sxs-lookup"><span data-stu-id="223f7-162">CTRL+T blocked (open new tab)</span></span> | <span data-ttu-id="223f7-163">N</span><span class="sxs-lookup"><span data-stu-id="223f7-163">N</span></span> | <span data-ttu-id="223f7-164">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-164">Y</span></span> | <span data-ttu-id="223f7-165">89</span><span class="sxs-lookup"><span data-stu-id="223f7-165">89</span></span> |
|<span data-ttu-id="223f7-166">Paramètres et plus (...) afficheront uniquement les options requises</span><span class="sxs-lookup"><span data-stu-id="223f7-166">Settings and more (...) will display only the required options</span></span>  |<span data-ttu-id="223f7-167">N</span><span class="sxs-lookup"><span data-stu-id="223f7-167">N</span></span> |<span data-ttu-id="223f7-168">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-168">Y</span></span> |<span data-ttu-id="223f7-169">89</span><span class="sxs-lookup"><span data-stu-id="223f7-169">89</span></span> |

> [!NOTE]
> <span data-ttu-id="223f7-170">Lorsque le mode plein écran évolue, d’autres fonctionnalités sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="223f7-170">As kiosk mode evolves, more features will be available.</span></span>

## <span data-ttu-id="223f7-171">Utiliser les fonctionnalités du mode plein écran</span><span class="sxs-lookup"><span data-stu-id="223f7-171">Use kiosk mode features</span></span>

<span data-ttu-id="223f7-172">Les fonctionnalités du mode plein écran de MicrosoftEdge peuvent être invoquées avec les options de ligne de commande Windows10 suivantes:</span><span class="sxs-lookup"><span data-stu-id="223f7-172">Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="223f7-173">Connexion numérique/interactive du mode plein écran:</span><span class="sxs-lookup"><span data-stu-id="223f7-173">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="223f7-174">Navigation publique en mode plein écran:</span><span class="sxs-lookup"><span data-stu-id="223f7-174">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### <span data-ttu-id="223f7-175">Autres options de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="223f7-175">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="223f7-176">: désactivez la première expérience d’exécution de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="223f7-176">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="223f7-177">: modifiez l’heure (en minutes) de la dernière activité d’utilisateur avant la réinitialisation de la session de l’utilisateur par la version du mode plein écran de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="223f7-177">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="223f7-178">Les valeurs suivantes sont prises en charge:</span><span class="sxs-lookup"><span data-stu-id="223f7-178">The following values are supported:</span></span>

  - <span data-ttu-id="223f7-179">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="223f7-179">Default values</span></span>
    - <span data-ttu-id="223f7-180">Plein écran: désactivé</span><span class="sxs-lookup"><span data-stu-id="223f7-180">Full screen - turned off</span></span>
    - <span data-ttu-id="223f7-181">Navigation publique: 5minutes</span><span class="sxs-lookup"><span data-stu-id="223f7-181">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="223f7-182">Valeurs autorisées</span><span class="sxs-lookup"><span data-stu-id="223f7-182">Allowed values</span></span>
    - <span data-ttu-id="223f7-183">0: désactive le minuteur</span><span class="sxs-lookup"><span data-stu-id="223f7-183">0 - turns off the timer</span></span>
    - <span data-ttu-id="223f7-184">1-1440 minutes pour la réinitialisation du minuteur d’inactivité</span><span class="sxs-lookup"><span data-stu-id="223f7-184">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="223f7-185">Stratégies de support pour le mode plein écran</span><span class="sxs-lookup"><span data-stu-id="223f7-185">Support policies for kiosk mode</span></span>

<span data-ttu-id="223f7-186">Utilisez l’une des stratégies MicrosoftEdge répertoriées dans le tableau suivant pour améliorer l’expérience plein écran pour le type de mode plein écran MicrosoftEdge que vous configurez.</span><span class="sxs-lookup"><span data-stu-id="223f7-186">Use any of the Microsoft Edge policies listed in the following table to enhance the kiosk experience for the Microsoft Edge kiosk mode type you configure.</span></span> <span data-ttu-id="223f7-187">Pour en savoir plus sur ces stratégies, voir [MicrosoftEdge – Référence de stratégie de navigateur.](https://docs.microsoft.com/deployedge/microsoft-edge-policies)</span><span class="sxs-lookup"><span data-stu-id="223f7-187">To learn more about these policies, see [Microsoft Edge – Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies).</span></span>

> [!NOTE]
> <span data-ttu-id="223f7-188">La configuration des stratégies n’est pas limitée aux stratégies répertoriées dans le tableau suivant, mais des stratégies supplémentaires doivent être testées pour s’assurer que les fonctionnalités du mode plein écran ne sont pas affectées.</span><span class="sxs-lookup"><span data-stu-id="223f7-188">Policy configuration isn't limited to the policies listed in the following table, however additional policies should be tested to ensure that kiosk mode functionality isn't negatively affected.</span></span>

|<span data-ttu-id="223f7-189">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="223f7-189">Group policy</span></span>|<span data-ttu-id="223f7-190">Connexion numérique/interactive</span><span class="sxs-lookup"><span data-stu-id="223f7-190">Digital\Interactive signage</span></span>|<span data-ttu-id="223f7-191">Navigation publique à application unique</span><span class="sxs-lookup"><span data-stu-id="223f7-191">Public browsing single-app</span></span>|
|--|--|--|
|[<span data-ttu-id="223f7-192">Impression</span><span class="sxs-lookup"><span data-stu-id="223f7-192">Printing</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | <span data-ttu-id="223f7-193">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-193">Y</span></span>|<span data-ttu-id="223f7-194">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-194">Y</span></span> |
|[<span data-ttu-id="223f7-195">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="223f7-195">HomePageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |<span data-ttu-id="223f7-196">N</span><span class="sxs-lookup"><span data-stu-id="223f7-196">N</span></span> | <span data-ttu-id="223f7-197">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-197">Y</span></span>|
|[<span data-ttu-id="223f7-198">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="223f7-198">ShowHomeButton</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |<span data-ttu-id="223f7-199">N</span><span class="sxs-lookup"><span data-stu-id="223f7-199">N</span></span> | <span data-ttu-id="223f7-200">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-200">Y</span></span>|
|[<span data-ttu-id="223f7-201">NewTabPageLocation</span><span class="sxs-lookup"><span data-stu-id="223f7-201">NewTabPageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |<span data-ttu-id="223f7-202">N</span><span class="sxs-lookup"><span data-stu-id="223f7-202">N</span></span> |<span data-ttu-id="223f7-203">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-203">Y</span></span> |
|[<span data-ttu-id="223f7-204">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="223f7-204">FavoritesBarEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |<span data-ttu-id="223f7-205">N</span><span class="sxs-lookup"><span data-stu-id="223f7-205">N</span></span> |<span data-ttu-id="223f7-206">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-206">Y</span></span> |
|[<span data-ttu-id="223f7-207">URLAllowlist</span><span class="sxs-lookup"><span data-stu-id="223f7-207">URLAllowlist</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |<span data-ttu-id="223f7-208">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-208">Y</span></span> |<span data-ttu-id="223f7-209">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-209">Y</span></span> |
|[<span data-ttu-id="223f7-210">URLBlocklist</span><span class="sxs-lookup"><span data-stu-id="223f7-210">URLBlocklist</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |<span data-ttu-id="223f7-211">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-211">Y</span></span> | <span data-ttu-id="223f7-212">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-212">Y</span></span>|
|[<span data-ttu-id="223f7-213">ManagedSearchEngines</span><span class="sxs-lookup"><span data-stu-id="223f7-213">ManagedSearchEngines</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |<span data-ttu-id="223f7-214">N</span><span class="sxs-lookup"><span data-stu-id="223f7-214">N</span></span> | <span data-ttu-id="223f7-215">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-215">Y</span></span>|
|[<span data-ttu-id="223f7-216">UserFeedbackAllowed</span><span class="sxs-lookup"><span data-stu-id="223f7-216">UserFeedbackAllowed</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |<span data-ttu-id="223f7-217">N</span><span class="sxs-lookup"><span data-stu-id="223f7-217">N</span></span> | <span data-ttu-id="223f7-218">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-218">Y</span></span>|
|[<span data-ttu-id="223f7-219">VerticalTabsAllowed</span><span class="sxs-lookup"><span data-stu-id="223f7-219">VerticalTabsAllowed</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | <span data-ttu-id="223f7-220">N</span><span class="sxs-lookup"><span data-stu-id="223f7-220">N</span></span>|<span data-ttu-id="223f7-221">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-221">Y</span></span> |
|[<span data-ttu-id="223f7-222">Paramètres SmartScreen</span><span class="sxs-lookup"><span data-stu-id="223f7-222">SmartScreen settings</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |<span data-ttu-id="223f7-223">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-223">Y</span></span> |<span data-ttu-id="223f7-224">Y</span><span class="sxs-lookup"><span data-stu-id="223f7-224">Y</span></span> |

## <span data-ttu-id="223f7-225">MicrosoftEdge avec accès affecté</span><span class="sxs-lookup"><span data-stu-id="223f7-225">Microsoft Edge with assigned access</span></span>

### <span data-ttu-id="223f7-226">Borne à application unique</span><span class="sxs-lookup"><span data-stu-id="223f7-226">Single app kiosk</span></span>

<span data-ttu-id="223f7-227">MicrosoftEdge prend actuellement en charge un sous-ensemble des mêmes types de mode plein écran hérités de MicrosoftEdge pour l’accès affecté à une seule application avec les expériences de verrouillage suivantes: connexion numérique/interactive et navigation publique.</span><span class="sxs-lookup"><span data-stu-id="223f7-227">Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences: Digital/Interactive signage, and Public-browsing.</span></span>  

<span data-ttu-id="223f7-228">Le mode plein écran avec accès attribué est actuellement disponible pour le test avec la version la plus récente de la  [version d'évaluation Windows10Insider](https://insider.windows.com/), version 20215 ou ultérieure, et avec le  [canal de développement Microsoft Edge](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="223f7-228">Kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 or higher.</span></span>

**<span data-ttu-id="223f7-229">Comment puis-je obtenir l’aperçu de Windows Insider?</span><span class="sxs-lookup"><span data-stu-id="223f7-229">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="223f7-230">Si vous souhaitez en savoir plus sur l’installation d’une version d'évaluation de Windows10 Insider sur un PC, veuillez consulter les instructions de la rubrique  [Prise en main des versions d'évaluation de Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="223f7-230">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="223f7-231">Borne à plusieurs applications</span><span class="sxs-lookup"><span data-stu-id="223f7-231">Multi-app kiosk</span></span>

<span data-ttu-id="223f7-232">Vous pouvez exécuter MicrosoftEdge avec un [accès attribué à plusieurs applications](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) sous Windows10. Cela équivaut au type de mode plein écran «Navigation normale» de l’ancienne version de Microsoft Edge .</span><span class="sxs-lookup"><span data-stu-id="223f7-232">Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="223f7-233">Pour configurer MicrosoftEdge avec un accès affecté à plusieurs applications, suivez les instructions sur la configuration d’une borne [multi-application](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span><span class="sxs-lookup"><span data-stu-id="223f7-233">To configure Microsoft Edge with multi-app assigned access, follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="223f7-234">(L’AUMID du canal stable de MicrosoftEdge est **MSEdge**).</span><span class="sxs-lookup"><span data-stu-id="223f7-234">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

<span data-ttu-id="223f7-235">Lorsque vous utilisez MicrosoftEdge avec un accès affecté à plusieurs applications, vous pouvez configurer MicrosoftEdge Kiosk pour utiliser les stratégies de navigateur[Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) afin de configurer l’expérience de navigation afin de répondre à vos besoins uniques.</span><span class="sxs-lookup"><span data-stu-id="223f7-235">When using Microsoft Edge with multi-app assigned access, you can configure Microsoft Edge kiosk to use the[Microsoft Edge browser policies](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.</span></span>

### <span data-ttu-id="223f7-236">Configurer à l’aide des paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="223f7-236">Configure using Windows Settings</span></span>

<span data-ttu-id="223f7-237">Les paramètres Windows constituent le moyen le plus simple de configurer un ou deux appareils borne à une seule application.</span><span class="sxs-lookup"><span data-stu-id="223f7-237">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="223f7-238">Procédez comme suit pour configurer un ordinateur borne à une seul application.</span><span class="sxs-lookup"><span data-stu-id="223f7-238">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="223f7-239">Installez la version la plus récente de Windows10 Insider Preview, version 20215 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="223f7-239">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="223f7-240">Suivez les instructions de [Prise en main des versions d'évaluation de Windows10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="223f7-240">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="223f7-241">Installez la dernière version du canal [stable MicrosoftEdge,](https://www.microsoft.com/edge)version 87 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="223f7-241">Install the latest version of [Microsoft Edge Stable channel](https://www.microsoft.com/edge), version 87 or higher.</span></span>  <span data-ttu-id="223f7-242">Pour tester les dernières fonctionnalités, vous pouvez télécharger le dernier [canal de développement Microsoft Edge,](https://www.microsoftedgeinsider.com/download)version89 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="223f7-242">To test the latest features, you can download the latest [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), version 89 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="223f7-243">Une installation au niveau des appareils étant requise, seul un canal non-Canary est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="223f7-243">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="223f7-244">Sur l’ordinateur borne, ouvrez Paramètres Windows, puis tapez «borne» dans le champ de recherche.</span><span class="sxs-lookup"><span data-stu-id="223f7-244">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="223f7-245">Sélectionnez  **Configurer une borne (accès attribué)**, illustré dans la capture d’écran suivante pour ouvrir la boîte de dialogue de création de la borne.</span><span class="sxs-lookup"><span data-stu-id="223f7-245">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurer la borne avec l’accès attribué":::

4. <span data-ttu-id="223f7-247">Sur la page **Configurer une borne** , cliquez sur  **Prise en main**.</span><span class="sxs-lookup"><span data-stu-id="223f7-247">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Page borne: prise en main":::

5. <span data-ttu-id="223f7-249">Tapez un nom pour créer un nouveau compte borne ou sélectionnez un compte existant dans la liste déroulante rempli, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="223f7-249">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Mode plein écran: créer un compte":::

6. <span data-ttu-id="223f7-251">Dans la page **Choisir une application borne** , sélectionnez **Microsoft Edge**, puis cliquez sur  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="223f7-251">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="223f7-252">Cela s’applique uniquement aux canaux Microsoft Edge dev, Beta et stable.</span><span class="sxs-lookup"><span data-stu-id="223f7-252">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Mode plein écran: choisir une application":::

7. <span data-ttu-id="223f7-254">Sélectionnez l’une des options suivantes pour l’affichage de Microsoft Edge en mode plein écran:</span><span class="sxs-lookup"><span data-stu-id="223f7-254">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="223f7-255">Connexion numérique/interactive: affiche un site spécifique en mode plein écran, exécutant Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="223f7-255">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="223f7-256">Navigateur public: exécute une version multi-onglet limitée de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="223f7-256">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Affichage en mode plein écran: signature numérique plein écran":::

8. <span data-ttu-id="223f7-258">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="223f7-258">Select **Next**.</span></span>
9. <span data-ttu-id="223f7-259">Tapez l’URL à charger lors du lancement du kiosque.</span><span class="sxs-lookup"><span data-stu-id="223f7-259">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Mode plein écran: entrer l’URL":::

10. <span data-ttu-id="223f7-261">Acceptez la valeur par défaut de 5 minutes pour le temps d’inactivité ou indiquez la valeur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="223f7-261">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Mode plein écran: entrer la durée d’inactivité":::

11. <span data-ttu-id="223f7-263">Cliquez sur  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="223f7-263">Click **Next**.</span></span>
12. <span data-ttu-id="223f7-264">Fermez la fenêtre  **Paramètres**  pour enregistrer et appliquer vos choix.</span><span class="sxs-lookup"><span data-stu-id="223f7-264">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Mode plein écran: terminer la configuration":::

13. <span data-ttu-id="223f7-266">Déconnectez-vous à partir de l’appareil kiosque et connectez-vous avec le compte kiosque local pour valider la configuration.</span><span class="sxs-lookup"><span data-stu-id="223f7-266">Sign out from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="223f7-267">Limitations fonctionnelles</span><span class="sxs-lookup"><span data-stu-id="223f7-267">Functional limitations</span></span>

<span data-ttu-id="223f7-268">Avec la publication de cette version d’évaluation du mode plein écran, nous continuons à travailler sur l’amélioration du produit et en ajoutant de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="223f7-268">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="223f7-269">Nous vous recommandons de désactiver :</span><span class="sxs-lookup"><span data-stu-id="223f7-269">We recommend that you turn off:</span></span>

- [<span data-ttu-id="223f7-270">StartupBoostEnabled</span><span class="sxs-lookup"><span data-stu-id="223f7-270">StartupBoostEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [<span data-ttu-id="223f7-271">InternetExplorerIntegrationLevel</span><span class="sxs-lookup"><span data-stu-id="223f7-271">InternetExplorerIntegrationLevel</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [<span data-ttu-id="223f7-272">Extensions</span><span class="sxs-lookup"><span data-stu-id="223f7-272">Extensions</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)
- [<span data-ttu-id="223f7-273">BackgroundModeEnabled</span><span class="sxs-lookup"><span data-stu-id="223f7-273">BackgroundModeEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)

## <span data-ttu-id="223f7-274">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="223f7-274">Roadmap</span></span>

### <span data-ttu-id="223f7-275">Début 2021</span><span class="sxs-lookup"><span data-stu-id="223f7-275">In early 2021</span></span>

<span data-ttu-id="223f7-276">Nous allons ajouter la prise en charge et les fonctionnalités suivantes:</span><span class="sxs-lookup"><span data-stu-id="223f7-276">We'll add the following support and features:</span></span>

- <span data-ttu-id="223f7-277">Disponibilité générale du mode plein écran de MicrosoftEdge avec accès affecté à l’application unique sur Windows10 1909 et les plus élevés.</span><span class="sxs-lookup"><span data-stu-id="223f7-277">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows 10 1909 and higher.</span></span>
- <span data-ttu-id="223f7-278">Fonctionnalités supplémentaires pour la parité avec la version MicrosoftEdge hérité.</span><span class="sxs-lookup"><span data-stu-id="223f7-278">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="223f7-279">Intégration avec Intune pour configurer les appareils à l’aide d’un profil en mode plein écran UX.</span><span class="sxs-lookup"><span data-stu-id="223f7-279">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>
- <span data-ttu-id="223f7-280">Les raccourcis clavier supplémentaires seront bloqués.</span><span class="sxs-lookup"><span data-stu-id="223f7-280">Additional keyboard shortcuts will be blocked.</span></span>
- <span data-ttu-id="223f7-281">Limiter le lancement d’autres applications à partir du navigateur.</span><span class="sxs-lookup"><span data-stu-id="223f7-281">Restrict the launch of other applications from the browser.</span></span>

## <span data-ttu-id="223f7-282">Voir également</span><span class="sxs-lookup"><span data-stu-id="223f7-282">See also</span></span>

- [<span data-ttu-id="223f7-283">Configurer des bornes et enseignes numériques dans les éditions Windows de bureau</span><span class="sxs-lookup"><span data-stu-id="223f7-283">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="223f7-284">Déployer la version héritée du mode plein écran de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="223f7-284">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode)
- [<span data-ttu-id="223f7-285">Planifier votre déploiement de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="223f7-285">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="223f7-286">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="223f7-286">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
