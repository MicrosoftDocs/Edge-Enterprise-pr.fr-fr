---
title: Configurer Microsoft Edge en mode plein écran
ms.author: aguta
author: aguta
manager: srugh
ms.date: 09/24/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer Microsoft Edge en mode plein écran
ms.openlocfilehash: 17852cc7c7e4921a0fbef7d09a3f1c3d3cccf49f
ms.sourcegitcommit: b1285b7745eb41b241d706b401f8ce78fa33b227
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2020
ms.locfileid: "11078664"
---
# <span data-ttu-id="76aea-103">Configurer Microsoft Edge en mode plein écran</span><span class="sxs-lookup"><span data-stu-id="76aea-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="76aea-104">Cet article décrit la configuration des options Microsoft Edge en mode plein écran que vous pouvez piloter.</span><span class="sxs-lookup"><span data-stu-id="76aea-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="76aea-105">Il existe également une feuille de route des fonctionnalités que nous mettons en cible.</span><span class="sxs-lookup"><span data-stu-id="76aea-105">There's also a roadmap of features we are targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="76aea-106">Cet article concerne MicrosoftEdge version87 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="76aea-106">This article applies to Microsoft Edge version 87 or later.</span></span>

<span data-ttu-id="76aea-107">Pour plus d’informations sur la version héritée du mode plein écran de MicrosoftEdge (version45 et antérieure , consultez [Déployer Microsoft Edge en mode plein écran](https://aka.ms/edgekioskmode).</span><span class="sxs-lookup"><span data-stu-id="76aea-107">For information about Microsoft Edge Legacy kiosk mode (version 45 and earlier) see [Deploy Microsoft Edge kiosk mode](https://aka.ms/edgekioskmode).</span></span>

## <span data-ttu-id="76aea-108">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="76aea-108">Overview</span></span>

<span data-ttu-id="76aea-109">Microsoft Edge en mode plein écran offre deux expériences de verrouillage du navigateur afin de permettre aux organisations de créer, gérer et offrir une expérience optimale pour leurs clients.</span><span class="sxs-lookup"><span data-stu-id="76aea-109">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="76aea-110">Les expériences de verrouillage suivantes sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="76aea-110">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="76aea-111">L’expérience de signalement numérique/interactif affiche un site spécifique en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="76aea-111">The Digital/Interactive signage experience displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="76aea-112">L’expérience de navigation publique exécute une version multi-onglet limitée de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76aea-112">The public-browsing experience runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="76aea-113">Les deux expériences exécutent une session Microsoft Edge InPrivate qui protège les données de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="76aea-113">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="76aea-114">Configurer Microsoft Edge en mode plein écran</span><span class="sxs-lookup"><span data-stu-id="76aea-114">Set up Microsoft Edge kiosk mode</span></span>  

<span data-ttu-id="76aea-115">Un groupe initial de fonctionnalités du mode plein écran est désormais disponible pour tester avec le canal Microsoft Edge Canary (version87).</span><span class="sxs-lookup"><span data-stu-id="76aea-115">An initial set of kiosk mode features are now available to test with Microsoft Edge Canary Channel, version 87.</span></span> <span data-ttu-id="76aea-116">Vous pouvez télécharger Microsoft Edge Canary à partir de la page [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) .</span><span class="sxs-lookup"><span data-stu-id="76aea-116">You can download Microsoft Edge Canary from the [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) page.</span></span>

### <span data-ttu-id="76aea-117">Fonctionnalités du mode plein écran</span><span class="sxs-lookup"><span data-stu-id="76aea-117">Kiosk mode features</span></span>

<span data-ttu-id="76aea-118">Les composants suivants sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="76aea-118">The following features are available:</span></span>

- <span data-ttu-id="76aea-119">Navigation InPrivate.</span><span class="sxs-lookup"><span data-stu-id="76aea-119">InPrivate navigation.</span></span> <span data-ttu-id="76aea-120">Protège les données des utilisateurs en supprimant les données du navigateur et les téléchargements lorsque la session se termine.</span><span class="sxs-lookup"><span data-stu-id="76aea-120">Protects user data by deleting browser data and downloads when the session ends.</span></span>
- <span data-ttu-id="76aea-121">Stratégie permettant de configurer les téléchargements supprimés à la fermeture.</span><span class="sxs-lookup"><span data-stu-id="76aea-121">Policy to configure Delete downloads on exit.</span></span>
- <span data-ttu-id="76aea-122">Réinitialiser la session utilisateur après une certaine période d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="76aea-122">Reset user session after a certain period of inactivity.</span></span>
- <span data-ttu-id="76aea-123">Première série de fonctionnalités de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="76aea-123">Initial set of lockdown functionality.</span></span> <span data-ttu-id="76aea-124">Les fonctions suivantes sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="76aea-124">The following functions are available:</span></span>

  - <span data-ttu-id="76aea-125">Menu contextuel de la souris</span><span class="sxs-lookup"><span data-stu-id="76aea-125">Mouse context menu</span></span>
  - <span data-ttu-id="76aea-126">F12: outils de développement</span><span class="sxs-lookup"><span data-stu-id="76aea-126">F12 Developer Tools</span></span>
  - <span data-ttu-id="76aea-127">F11: quitter le mode plein écran (en mode plein écran)</span><span class="sxs-lookup"><span data-stu-id="76aea-127">F11 Exit full screen (while in full screen mode)</span></span>
  - <span data-ttu-id="76aea-128">Blocage du groupe initial des pages *Edge://*</span><span class="sxs-lookup"><span data-stu-id="76aea-128">Blocking of the initial set of *Edge://* pages</span></span>

> [!NOTE]
> <span data-ttu-id="76aea-129">Lorsque le mode plein écran évolue, d’autres fonctionnalités sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="76aea-129">As kiosk mode evolves, more features will be available.</span></span>

### <span data-ttu-id="76aea-130">Utiliser les fonctionnalités du mode plein écran</span><span class="sxs-lookup"><span data-stu-id="76aea-130">Use kiosk mode features</span></span>

<span data-ttu-id="76aea-131">Vous pouvez appeler les fonctionnalités de Microsoft Edge en mode plein écran grâce aux options de ligne de commande suivantes de Windows10 :</span><span class="sxs-lookup"><span data-stu-id="76aea-131">You can invoke Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="76aea-132">Signalisation numérique/interactive du mode plein écran</span><span class="sxs-lookup"><span data-stu-id="76aea-132">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="76aea-133">Navigation publique en mode plein écran:</span><span class="sxs-lookup"><span data-stu-id="76aea-133">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

#### <span data-ttu-id="76aea-134">Autres options de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="76aea-134">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="76aea-135">: désactivez la première expérience d’exécution de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76aea-135">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="76aea-136">: modifiez l’heure (en minutes) de la dernière activité d’utilisateur avant la réinitialisation de la session de l’utilisateur par la version du mode plein écran de MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="76aea-136">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="76aea-137">Les valeurs suivantes sont prises en charge:</span><span class="sxs-lookup"><span data-stu-id="76aea-137">The following values are supported:</span></span>

  - <span data-ttu-id="76aea-138">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="76aea-138">Default values</span></span>
    - <span data-ttu-id="76aea-139">Plein écran: désactivé</span><span class="sxs-lookup"><span data-stu-id="76aea-139">Full screen - turned off</span></span>
    - <span data-ttu-id="76aea-140">Navigation publique: 5minutes</span><span class="sxs-lookup"><span data-stu-id="76aea-140">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="76aea-141">Valeurs autorisées</span><span class="sxs-lookup"><span data-stu-id="76aea-141">Allowed values</span></span>
    - <span data-ttu-id="76aea-142">0: désactive le minuteur</span><span class="sxs-lookup"><span data-stu-id="76aea-142">0 - turns off the timer</span></span>
    - <span data-ttu-id="76aea-143">1-1440 minutes pour la réinitialisation du minuteur d’inactivité</span><span class="sxs-lookup"><span data-stu-id="76aea-143">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="76aea-144">Configurer le mode plein écran avec l’accès attribué</span><span class="sxs-lookup"><span data-stu-id="76aea-144">Set up kiosk mode with assigned access</span></span>

<span data-ttu-id="76aea-145">Microsoft Edge en mode plein écran avec accès attribué est actuellement disponible pour le test avec la version la plus récente de la [version d'évaluation Windows10Insider](https://insider.windows.com/), version 20215 ou ultérieure, et avec le [canal de développement Microsoft Edge](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="76aea-145">Microsoft Edge kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4  or higher.</span></span>

**<span data-ttu-id="76aea-146">Comment puis-je obtenir l’aperçu de Windows Insider?</span><span class="sxs-lookup"><span data-stu-id="76aea-146">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="76aea-147">Pour installer une version d'évaluation de Windows10 Insider sur un PC, suivez les instructions de [Prise en main des versions d'évaluation de Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="76aea-147">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="76aea-148">Configurer à l’aide des paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="76aea-148">Configure using Windows Settings</span></span>

<span data-ttu-id="76aea-149">Les paramètres Windows constituent le moyen le plus simple de configurer un ou deux appareils borne à une seule application.</span><span class="sxs-lookup"><span data-stu-id="76aea-149">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="76aea-150">Procédez comme suit pour configurer un ordinateur borne à une seul application.</span><span class="sxs-lookup"><span data-stu-id="76aea-150">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="76aea-151">Installez la version la plus récente de Windows10 Insider Preview, version 20215 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="76aea-151">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="76aea-152">Suivez les instructions de [Prise en main des versions d'évaluation de Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="76aea-152">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="76aea-153">Installez la dernière version du [canal Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), 87.0.644.4 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="76aea-153">Install the latest version of [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), 87.0.644.4 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="76aea-154">Une installation au niveau des appareils étant requise, seul un canal non-Canary est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="76aea-154">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="76aea-155">Sur l’ordinateur borne, ouvrez Paramètres Windows, puis tapez «borne» dans le champ de recherche.</span><span class="sxs-lookup"><span data-stu-id="76aea-155">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="76aea-156">Sélectionnez  **Configurer une borne (accès attribué)**, illustré dans la capture d’écran suivante pour ouvrir la boîte de dialogue de création de la borne.</span><span class="sxs-lookup"><span data-stu-id="76aea-156">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Configurer la borne avec l’accès attribué":::

4. <span data-ttu-id="76aea-158">Sur la page **Configurer une borne** , cliquez sur  **Prise en main**.</span><span class="sxs-lookup"><span data-stu-id="76aea-158">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Configurer la borne avec l’accès attribué":::

5. <span data-ttu-id="76aea-160">Tapez un nom pour créer un nouveau compte borne ou sélectionnez un compte existant dans la liste déroulante rempli, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="76aea-160">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Configurer la borne avec l’accès attribué":::

6. <span data-ttu-id="76aea-162">Dans la page **Choisir une application borne** , sélectionnez **Microsoft Edge**, puis cliquez sur  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="76aea-162">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="76aea-163">Cela s’applique uniquement aux canaux Microsoft Edge dev, Beta et stable.</span><span class="sxs-lookup"><span data-stu-id="76aea-163">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Configurer la borne avec l’accès attribué":::

7. <span data-ttu-id="76aea-165">Sélectionnez l’une des options suivantes pour l’affichage de Microsoft Edge en mode plein écran:</span><span class="sxs-lookup"><span data-stu-id="76aea-165">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="76aea-166">Connexion numérique/interactive: affiche un site spécifique en mode plein écran, exécutant Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76aea-166">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="76aea-167">Navigateur public: exécute une version multi-onglet limitée de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76aea-167">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Configurer la borne avec l’accès attribué":::

8. <span data-ttu-id="76aea-169">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="76aea-169">Select **Next**.</span></span>
9. <span data-ttu-id="76aea-170">Tapez l’URL à charger lors du lancement du kiosque.</span><span class="sxs-lookup"><span data-stu-id="76aea-170">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Configurer la borne avec l’accès attribué":::

10. <span data-ttu-id="76aea-172">Acceptez la valeur par défaut de 5 minutes pour le temps d’inactivité ou indiquez la valeur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="76aea-172">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Configurer la borne avec l’accès attribué":::

11. <span data-ttu-id="76aea-174">Cliquez sur  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="76aea-174">Click **Next**.</span></span>
12. <span data-ttu-id="76aea-175">Fermez la fenêtre  **Paramètres**  pour enregistrer et appliquer vos choix.</span><span class="sxs-lookup"><span data-stu-id="76aea-175">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Configurer la borne avec l’accès attribué":::

13. <span data-ttu-id="76aea-177">Redémarrez l’appareil borne et connectez-vous avec le compte borne local pour valider la configuration.</span><span class="sxs-lookup"><span data-stu-id="76aea-177">Sign off from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="76aea-178">Limitations fonctionnelles</span><span class="sxs-lookup"><span data-stu-id="76aea-178">Functional limitations</span></span>

<span data-ttu-id="76aea-179">Avec la publication de cette version d’évaluation du mode plein écran, nous continuons à travailler sur l’amélioration du produit et en ajoutant de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="76aea-179">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="76aea-180">Bien que le mode plein écran ne prenne pas en charge les fonctionnalités suivantes, le travail est actuellement en cours sur les fonctionnalités suivantes:</span><span class="sxs-lookup"><span data-stu-id="76aea-180">Although kiosk mode doesn't currently support the following functionality, work is underway on the following features:</span></span>

- <span data-ttu-id="76aea-181">Regroupements</span><span class="sxs-lookup"><span data-stu-id="76aea-181">Collections</span></span>
- <span data-ttu-id="76aea-182">Extensions</span><span class="sxs-lookup"><span data-stu-id="76aea-182">Extensions</span></span>
- <span data-ttu-id="76aea-183">Mode InternetExplorer</span><span class="sxs-lookup"><span data-stu-id="76aea-183">Internet Explorer mode</span></span>
- <span data-ttu-id="76aea-184">WindowsDefenderApplicationGuard (WDAG)</span><span class="sxs-lookup"><span data-stu-id="76aea-184">Windows Defender Application Guard (WDAG)</span></span>

## <span data-ttu-id="76aea-185">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="76aea-185">Roadmap</span></span>

### <span data-ttu-id="76aea-186">Plus tard cette année (2020)</span><span class="sxs-lookup"><span data-stu-id="76aea-186">Later this year (2020)</span></span>

<span data-ttu-id="76aea-187">Nous allons ajouter les fonctionnalités suivantes:</span><span class="sxs-lookup"><span data-stu-id="76aea-187">We'll add the following features:</span></span>

- <span data-ttu-id="76aea-188">Bouton terminer la session</span><span class="sxs-lookup"><span data-stu-id="76aea-188">End session button</span></span>
- <span data-ttu-id="76aea-189">Barre d’adresse URL en lecture seule</span><span class="sxs-lookup"><span data-stu-id="76aea-189">Read only URL address bar</span></span>  
  - <span data-ttu-id="76aea-190">Configurable avec une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="76aea-190">Configurable with group policy</span></span>
  - <span data-ttu-id="76aea-191">Lorsque cette option est activée, les utilisateurs ne peuvent pas modifier l’URL de la barre d’adresses pour essayer d’accéder à une autre page.</span><span class="sxs-lookup"><span data-stu-id="76aea-191">When enabled, users will be prevented from editing the address bar URL to try navigating away to another page.</span></span>

- <span data-ttu-id="76aea-192">Autres fonctions de verrouillage:</span><span class="sxs-lookup"><span data-stu-id="76aea-192">More lockdown functions:</span></span>

  - <span data-ttu-id="76aea-193">Les accélérateurs supplémentaires sont bloqués (par exemple, CTRL + N).</span><span class="sxs-lookup"><span data-stu-id="76aea-193">Additional accelerators will be blocked (for example, CTRL+N)</span></span>
  - <span data-ttu-id="76aea-194">Le menu paramètres «...» permet d’activer uniquement les options requises (par exemple, imprimer, aide, commentaires et lire à haute voix)</span><span class="sxs-lookup"><span data-stu-id="76aea-194">The "…" settings menu will enable only required options (for example, Print, Help,  Feedback, and Read aloud)</span></span>
  - <span data-ttu-id="76aea-195">Verrouillage des pages supplémentaires *edge://* (par exemple, *edge://settings*)</span><span class="sxs-lookup"><span data-stu-id="76aea-195">Additional *edge://* pages lockdown (for example, *edge://settings*)</span></span>
  - <span data-ttu-id="76aea-196">Configurer l’interface utilisateur des options d’impression</span><span class="sxs-lookup"><span data-stu-id="76aea-196">Configure print options UI</span></span>
  - <span data-ttu-id="76aea-197">Limiter l’Explorateur de fichiers au dossier de téléchargement uniquement.</span><span class="sxs-lookup"><span data-stu-id="76aea-197">Limiting file explorer to the download folder only.</span></span>

### <span data-ttu-id="76aea-198">Début 2021</span><span class="sxs-lookup"><span data-stu-id="76aea-198">In early 2021</span></span>

<span data-ttu-id="76aea-199">Nous allons ajouter la prise en charge et les fonctionnalités suivantes:</span><span class="sxs-lookup"><span data-stu-id="76aea-199">We'll add the following support and features:</span></span>

- <span data-ttu-id="76aea-200">Disponibilité générale de Microsoft Edge en mode plein écran avec accès affecté à une seule application sur Windows.</span><span class="sxs-lookup"><span data-stu-id="76aea-200">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows.</span></span>
- <span data-ttu-id="76aea-201">Fonctionnalités supplémentaires pour la parité avec l’Ancienne version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76aea-201">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="76aea-202">Intégration avec Intune pour configurer les appareils à l’aide d’un profil en mode plein écran UX.</span><span class="sxs-lookup"><span data-stu-id="76aea-202">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>

## <span data-ttu-id="76aea-203">Voir également</span><span class="sxs-lookup"><span data-stu-id="76aea-203">See also</span></span>

- [<span data-ttu-id="76aea-204">Configurer des bornes et enseignes numériques dans les éditions Windows de bureau</span><span class="sxs-lookup"><span data-stu-id="76aea-204">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="76aea-205">Déployer la version héritée du mode plein écran de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="76aea-205">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode)
- [<span data-ttu-id="76aea-206">Planifier votre déploiement de MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="76aea-206">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="76aea-207">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="76aea-207">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)