---
title: Configurer Microsoft Edge en mode plein écran
ms.author: aguta
author: aguta
manager: srugh
ms.date: 10/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer Microsoft Edge en mode plein écran
ms.openlocfilehash: 799b3dd4b7fc96f0b8e5cb718bca98fd4f38ec15
ms.sourcegitcommit: 78905f66f4a6590a57c8f2bf808af92106b62996
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/05/2020
ms.locfileid: "11094861"
---
# <span data-ttu-id="153d5-103">Configurer Microsoft Edge en mode plein écran</span><span class="sxs-lookup"><span data-stu-id="153d5-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="153d5-104">Cet article décrit la configuration des options Microsoft Edge en mode plein écran que vous pouvez piloter.</span><span class="sxs-lookup"><span data-stu-id="153d5-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="153d5-105">Il existe également une feuille de route des fonctionnalités que nous mettons en cible.</span><span class="sxs-lookup"><span data-stu-id="153d5-105">There's also a roadmap of features we are targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="153d5-106">Cet article concerne MicrosoftEdge version87 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="153d5-106">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="153d5-107">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="153d5-107">Overview</span></span>

<span data-ttu-id="153d5-108">Microsoft Edge en mode plein écran offre deux expériences de verrouillage du navigateur afin de permettre aux organisations de créer, gérer et offrir une expérience optimale pour leurs clients.</span><span class="sxs-lookup"><span data-stu-id="153d5-108">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="153d5-109">Les expériences de verrouillage suivantes sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="153d5-109">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="153d5-110">L’expérience de signalement numérique/interactif affiche un site spécifique en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="153d5-110">The Digital/Interactive signage experience displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="153d5-111">L’expérience de navigation publique exécute une version multi-onglet limitée de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="153d5-111">The public-browsing experience runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="153d5-112">Les deux expériences exécutent une session Microsoft Edge InPrivate qui protège les données de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="153d5-112">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="153d5-113">Configurer Microsoft Edge en mode plein écran</span><span class="sxs-lookup"><span data-stu-id="153d5-113">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="153d5-114">Un groupe initial de fonctionnalités du mode plein écran est désormais disponible pour tester avec le canal Microsoft Edge Canary (version87).</span><span class="sxs-lookup"><span data-stu-id="153d5-114">An initial set of kiosk mode features are now available to test with Microsoft Edge Canary Channel, version 87.</span></span> <span data-ttu-id="153d5-115">Vous pouvez télécharger Microsoft Edge Canary à partir de la page [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) .</span><span class="sxs-lookup"><span data-stu-id="153d5-115">You can download Microsoft Edge Canary from the [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) page.</span></span>

### <span data-ttu-id="153d5-116">Fonctionnalités du mode plein écran</span><span class="sxs-lookup"><span data-stu-id="153d5-116">Kiosk mode features</span></span>

<span data-ttu-id="153d5-117">Les composants suivants sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="153d5-117">The following features are available:</span></span>

- <span data-ttu-id="153d5-118">La navigation InPrivate protège les données des utilisateurs en supprimant les données du navigateur et les téléchargements à la fin de la session.</span><span class="sxs-lookup"><span data-stu-id="153d5-118">InPrivate navigation protects user data by deleting browser data and downloads when the session ends.</span></span>
- <span data-ttu-id="153d5-119">Stratégie permettant de configurer la fonctionnalité Supprimer les téléchargements à la fermeture.</span><span class="sxs-lookup"><span data-stu-id="153d5-119">A policy to configure Delete downloads on exit.</span></span>
- <span data-ttu-id="153d5-120">Option permettant de réinitialiser une session utilisateur après une certaine période d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="153d5-120">The option to reset a user session after a certain period of inactivity.</span></span>
- <span data-ttu-id="153d5-121">Ensemble initial de fonctionnalités de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="153d5-121">An initial set of lockdown functionality.</span></span> <span data-ttu-id="153d5-122">Les fonctions suivantes sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="153d5-122">The following functions are available:</span></span>

  - <span data-ttu-id="153d5-123">Menu contextuel de la souris</span><span class="sxs-lookup"><span data-stu-id="153d5-123">Mouse context menu</span></span>
  - <span data-ttu-id="153d5-124">F12: outils de développement</span><span class="sxs-lookup"><span data-stu-id="153d5-124">F12 Developer Tools</span></span>
  - <span data-ttu-id="153d5-125">F11: quitter le mode plein écran (en mode plein écran)</span><span class="sxs-lookup"><span data-stu-id="153d5-125">F11 Exit full screen (while in full screen mode)</span></span>
  - <span data-ttu-id="153d5-126">Blocage du groupe initial des pages *Edge://*</span><span class="sxs-lookup"><span data-stu-id="153d5-126">Blocking of the initial set of *Edge://* pages</span></span>

> [!NOTE]
> <span data-ttu-id="153d5-127">Lorsque le mode plein écran évolue, d’autres fonctionnalités sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="153d5-127">As kiosk mode evolves, more features will be available.</span></span>

## <span data-ttu-id="153d5-128">Utiliser les fonctionnalités du mode plein écran</span><span class="sxs-lookup"><span data-stu-id="153d5-128">Use kiosk mode features</span></span>

<span data-ttu-id="153d5-129">Vous pouvez appeler les fonctionnalités de Microsoft Edge en mode plein écran grâce aux options de ligne de commande suivantes de Windows10 :</span><span class="sxs-lookup"><span data-stu-id="153d5-129">You can invoke Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="153d5-130">Signalisation numérique/interactive du mode plein écran</span><span class="sxs-lookup"><span data-stu-id="153d5-130">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="153d5-131">Navigation publique en mode plein écran:</span><span class="sxs-lookup"><span data-stu-id="153d5-131">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### <span data-ttu-id="153d5-132">Autres options de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="153d5-132">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="153d5-133">: désactivez la première expérience d’exécution de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="153d5-133">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="153d5-134">: modifiez l’heure (en minutes) de la dernière activité d’utilisateur avant la réinitialisation de la session de l’utilisateur par la version du mode plein écran de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="153d5-134">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="153d5-135">Les valeurs suivantes sont prises en charge:</span><span class="sxs-lookup"><span data-stu-id="153d5-135">The following values are supported:</span></span>

  - <span data-ttu-id="153d5-136">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="153d5-136">Default values</span></span>
    - <span data-ttu-id="153d5-137">Plein écran: désactivé</span><span class="sxs-lookup"><span data-stu-id="153d5-137">Full screen - turned off</span></span>
    - <span data-ttu-id="153d5-138">Navigation publique: 5minutes</span><span class="sxs-lookup"><span data-stu-id="153d5-138">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="153d5-139">Valeurs autorisées</span><span class="sxs-lookup"><span data-stu-id="153d5-139">Allowed values</span></span>
    - <span data-ttu-id="153d5-140">0: désactive le minuteur</span><span class="sxs-lookup"><span data-stu-id="153d5-140">0 - turns off the timer</span></span>
    - <span data-ttu-id="153d5-141">1-1440 minutes pour la réinitialisation du minuteur d’inactivité</span><span class="sxs-lookup"><span data-stu-id="153d5-141">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="153d5-142">MicrosoftEdge avec accès affecté</span><span class="sxs-lookup"><span data-stu-id="153d5-142">Microsoft Edge with assigned access</span></span>

### <span data-ttu-id="153d5-143">Borne à application unique</span><span class="sxs-lookup"><span data-stu-id="153d5-143">Single app kiosk</span></span>

<span data-ttu-id="153d5-144">Microsoft Edge prend actuellement en charge un sous-ensemble des mêmes types de mode plein écran de l’ancienne version de Microsoft Edge pour un accès attribué à une application unique avec les expériences de verrouillage, la signalisation numérique/interactive et la navigation publique ci-après.</span><span class="sxs-lookup"><span data-stu-id="153d5-144">Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences, Digital/Interactive signage and Public-browsing.</span></span>  

<span data-ttu-id="153d5-145">Le mode plein écran avec accès attribué est actuellement disponible pour le test avec la version la plus récente de la  [version d'évaluation Windows10Insider](https://insider.windows.com/), version 20215 ou ultérieure, et avec le  [canal de développement Microsoft Edge](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="153d5-145">Kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 or higher.</span></span>

**<span data-ttu-id="153d5-146">Comment puis-je obtenir l’aperçu de Windows Insider?</span><span class="sxs-lookup"><span data-stu-id="153d5-146">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="153d5-147">Si vous souhaitez en savoir plus sur l’installation d’une version d'évaluation de Windows10 Insider sur un PC, veuillez consulter les instructions de la rubrique  [Prise en main des versions d'évaluation de Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="153d5-147">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="153d5-148">Borne à plusieurs applications</span><span class="sxs-lookup"><span data-stu-id="153d5-148">Multi-app kiosk</span></span>

<span data-ttu-id="153d5-149">Vous pouvez exécuter MicrosoftEdge avec un [accès attribué à plusieurs applications](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) sous Windows10. Cela équivaut au type de mode plein écran «Navigation normale» de l’ancienne version de Microsoft Edge .</span><span class="sxs-lookup"><span data-stu-id="153d5-149">Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="153d5-150">Pour configurer MicrosoftEdge avec accès affecté à plusieurs applications, suivez les instructions sur la façon de [Configurer une borne à plusieurs applications](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span><span class="sxs-lookup"><span data-stu-id="153d5-150">To configure Microsoft Edge with multi-app assigned access follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="153d5-151">(L’AUMID du canal stable de MicrosoftEdge est **MSEdge**).</span><span class="sxs-lookup"><span data-stu-id="153d5-151">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

<span data-ttu-id="153d5-152">Configurer le mode plein écran de Microsoft Edge
Lorsque vous utilisez MicrosoftEdge avec accès attribué à plusieurs applications, vous pouvez utiliser les [stratégies de navigateur MicrosoftEdge](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) pour configurer l’expérience de navigation en fonction de vos besoins spécifiques.</span><span class="sxs-lookup"><span data-stu-id="153d5-152">Configure Microsoft Edge kiosk mode When using Microsoft Edge with multi-app assigned access you can use the [Microsoft Edge browser policies](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.</span></span>

### <span data-ttu-id="153d5-153">Configurer à l’aide des paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="153d5-153">Configure using Windows Settings</span></span>

<span data-ttu-id="153d5-154">Les paramètres Windows constituent le moyen le plus simple de configurer un ou deux appareils borne à une seule application.</span><span class="sxs-lookup"><span data-stu-id="153d5-154">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="153d5-155">Procédez comme suit pour configurer un ordinateur borne à une seul application.</span><span class="sxs-lookup"><span data-stu-id="153d5-155">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="153d5-156">Installez la version la plus récente de Windows10 Insider Preview, version 20215 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="153d5-156">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="153d5-157">Suivez les instructions de [Prise en main des versions d'évaluation de Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="153d5-157">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="153d5-158">Installez la dernière version du [canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), 87.0.644.4 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="153d5-158">Install the latest version of [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), 87.0.644.4 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="153d5-159">Une installation au niveau des appareils étant requise, seul un canal non-Canary est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="153d5-159">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="153d5-160">Sur l’ordinateur borne, ouvrez Paramètres Windows, puis tapez «borne» dans le champ de recherche.</span><span class="sxs-lookup"><span data-stu-id="153d5-160">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="153d5-161">Sélectionnez  **Configurer une borne (accès attribué)**, illustré dans la capture d’écran suivante pour ouvrir la boîte de dialogue de création de la borne.</span><span class="sxs-lookup"><span data-stu-id="153d5-161">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurer la borne avec l’accès attribué":::

4. <span data-ttu-id="153d5-163">Sur la page **Configurer une borne** , cliquez sur  **Prise en main**.</span><span class="sxs-lookup"><span data-stu-id="153d5-163">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Configurer la borne avec l’accès attribué":::

5. <span data-ttu-id="153d5-165">Tapez un nom pour créer un nouveau compte borne ou sélectionnez un compte existant dans la liste déroulante rempli, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="153d5-165">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Configurer la borne avec l’accès attribué":::

6. <span data-ttu-id="153d5-167">Dans la page **Choisir une application borne** , sélectionnez **Microsoft Edge**, puis cliquez sur  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="153d5-167">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="153d5-168">Cela s’applique uniquement aux canaux Microsoft Edge dev, Beta et stable.</span><span class="sxs-lookup"><span data-stu-id="153d5-168">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Configurer la borne avec l’accès attribué":::

7. <span data-ttu-id="153d5-170">Sélectionnez l’une des options suivantes pour l’affichage de Microsoft Edge en mode plein écran:</span><span class="sxs-lookup"><span data-stu-id="153d5-170">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="153d5-171">Connexion numérique/interactive: affiche un site spécifique en mode plein écran, exécutant Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="153d5-171">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="153d5-172">Navigateur public: exécute une version multi-onglet limitée de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="153d5-172">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Configurer la borne avec l’accès attribué":::

8. <span data-ttu-id="153d5-174">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="153d5-174">Select **Next**.</span></span>
9. <span data-ttu-id="153d5-175">Tapez l’URL à charger lors du lancement du kiosque.</span><span class="sxs-lookup"><span data-stu-id="153d5-175">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Configurer la borne avec l’accès attribué":::

10. <span data-ttu-id="153d5-177">Acceptez la valeur par défaut de 5 minutes pour le temps d’inactivité ou indiquez la valeur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="153d5-177">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Configurer la borne avec l’accès attribué":::

11. <span data-ttu-id="153d5-179">Cliquez sur  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="153d5-179">Click **Next**.</span></span>
12. <span data-ttu-id="153d5-180">Fermez la fenêtre  **Paramètres**  pour enregistrer et appliquer vos choix.</span><span class="sxs-lookup"><span data-stu-id="153d5-180">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Configurer la borne avec l’accès attribué":::

13. <span data-ttu-id="153d5-182">Redémarrez l’appareil borne et connectez-vous avec le compte borne local pour valider la configuration.</span><span class="sxs-lookup"><span data-stu-id="153d5-182">Sign off from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="153d5-183">Limitations fonctionnelles</span><span class="sxs-lookup"><span data-stu-id="153d5-183">Functional limitations</span></span>

<span data-ttu-id="153d5-184">Avec la publication de cette version d’évaluation du mode plein écran, nous continuons à travailler sur l’amélioration du produit et en ajoutant de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="153d5-184">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="153d5-185">Bien que le mode plein écran ne prenne pas en charge les fonctionnalités suivantes, le travail est actuellement en cours sur les fonctionnalités suivantes:</span><span class="sxs-lookup"><span data-stu-id="153d5-185">Although kiosk mode doesn't currently support the following functionality, work is underway on the following features:</span></span>

- <span data-ttu-id="153d5-186">Regroupements</span><span class="sxs-lookup"><span data-stu-id="153d5-186">Collections</span></span>
- <span data-ttu-id="153d5-187">Extensions</span><span class="sxs-lookup"><span data-stu-id="153d5-187">Extensions</span></span>
- <span data-ttu-id="153d5-188">Mode InternetExplorer</span><span class="sxs-lookup"><span data-stu-id="153d5-188">Internet Explorer mode</span></span>
- <span data-ttu-id="153d5-189">WindowsDefenderApplicationGuard (WDAG)</span><span class="sxs-lookup"><span data-stu-id="153d5-189">Windows Defender Application Guard (WDAG)</span></span>

## <span data-ttu-id="153d5-190">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="153d5-190">Roadmap</span></span>

### <span data-ttu-id="153d5-191">Plus tard cette année (2020)</span><span class="sxs-lookup"><span data-stu-id="153d5-191">Later this year (2020)</span></span>

<span data-ttu-id="153d5-192">Nous allons ajouter les fonctionnalités suivantes:</span><span class="sxs-lookup"><span data-stu-id="153d5-192">We'll add the following features:</span></span>

- <span data-ttu-id="153d5-193">Bouton terminer la session</span><span class="sxs-lookup"><span data-stu-id="153d5-193">End session button</span></span>
- <span data-ttu-id="153d5-194">Barre d’adresse en lecture seule</span><span class="sxs-lookup"><span data-stu-id="153d5-194">Read only address bar</span></span>  
  - <span data-ttu-id="153d5-195">Configurable avec une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="153d5-195">Configurable with group policy</span></span>
  - <span data-ttu-id="153d5-196">Lorsque cette option est activée, les utilisateurs ne peuvent pas modifier la barre d’adresse, ni accéder à une autre page.</span><span class="sxs-lookup"><span data-stu-id="153d5-196">When enabled, users will be prevented from editing the address bar and navigating to another page.</span></span>

- <span data-ttu-id="153d5-197">Autres fonctions de verrouillage:</span><span class="sxs-lookup"><span data-stu-id="153d5-197">More lockdown functions:</span></span>

  - <span data-ttu-id="153d5-198">Les accélérateurs supplémentaires sont bloqués (par exemple, CTRL + N).</span><span class="sxs-lookup"><span data-stu-id="153d5-198">Additional accelerators will be blocked (for example, CTRL+N)</span></span>
  - <span data-ttu-id="153d5-199">Le menu paramètres «...» permet d’activer uniquement les options requises (par exemple, imprimer, aide, commentaires et lire à haute voix)</span><span class="sxs-lookup"><span data-stu-id="153d5-199">The "…" settings menu will enable only required options (for example, Print, Help,  Feedback, and Read aloud)</span></span>
  - <span data-ttu-id="153d5-200">Verrouillage des pages supplémentaires *edge://* (par exemple, *edge://settings*)</span><span class="sxs-lookup"><span data-stu-id="153d5-200">Additional *edge://* pages lockdown (for example, *edge://settings*)</span></span>
  - <span data-ttu-id="153d5-201">Configurer l’interface utilisateur des options d’impression</span><span class="sxs-lookup"><span data-stu-id="153d5-201">Configure print options UI</span></span>
  - <span data-ttu-id="153d5-202">Limiter l’Explorateur de fichiers au dossier de téléchargement uniquement.</span><span class="sxs-lookup"><span data-stu-id="153d5-202">Limiting file explorer to the download folder only.</span></span>

### <span data-ttu-id="153d5-203">Début 2021</span><span class="sxs-lookup"><span data-stu-id="153d5-203">In early 2021</span></span>

<span data-ttu-id="153d5-204">Nous allons ajouter la prise en charge et les fonctionnalités suivantes:</span><span class="sxs-lookup"><span data-stu-id="153d5-204">We'll add the following support and features:</span></span>

- <span data-ttu-id="153d5-205">Disponibilité générale de Microsoft Edge en mode plein écran avec accès affecté à une seule application sur Windows.</span><span class="sxs-lookup"><span data-stu-id="153d5-205">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows.</span></span>
- <span data-ttu-id="153d5-206">Fonctionnalités supplémentaires pour la parité avec l’Ancienne version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="153d5-206">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="153d5-207">Intégration avec Intune pour configurer les appareils à l’aide d’un profil en mode plein écran UX.</span><span class="sxs-lookup"><span data-stu-id="153d5-207">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>

## <span data-ttu-id="153d5-208">Voir également</span><span class="sxs-lookup"><span data-stu-id="153d5-208">See also</span></span>

- [<span data-ttu-id="153d5-209">Configurer des bornes et enseignes numériques dans les éditions Windows de bureau</span><span class="sxs-lookup"><span data-stu-id="153d5-209">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="153d5-210">Déployer la version héritée du mode plein écran de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="153d5-210">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode)
- [<span data-ttu-id="153d5-211">Planifier votre déploiement de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="153d5-211">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="153d5-212">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="153d5-212">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
