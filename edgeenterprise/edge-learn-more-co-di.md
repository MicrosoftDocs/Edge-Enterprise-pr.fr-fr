---
title: ClickOnce et DirectInvoke dans MicrosoftEdge
ms.author: kele
author: dan-wesley
manager: srugh
ms.date: 04/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez ClickOnce et DirectInvoke dans MicrosoftEdge.
ms.openlocfilehash: 8290c34bd29ca72678e3fa68f74b689d0cf797e3
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979765"
---
# <span data-ttu-id="bb441-103">Découvrez les fonctionnalités ClickOnce et DirectInvoke dans MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="bb441-103">Understand the ClickOnce and DirectInvoke features in Microsoft Edge</span></span>

<span data-ttu-id="bb441-104">ClickOnce et DirectInvoke sont des fonctionnalités disponibles dans Internet Explorer et MicrosoftEdge (version45 et antérieures), qui permettent d’utiliser un gestionnaire de fichiers pour télécharger des fichiers à partir d’un site web.</span><span class="sxs-lookup"><span data-stu-id="bb441-104">ClickOnce and DirectInvoke are features available in IE and Microsoft Edge (version 45 and earlier) that support the use of a file handler to download files from a website.</span></span> <span data-ttu-id="bb441-105">Bien que leur finalité soit différente, les deux fonctionnalités permettent aux sites web de spécifier qu’un fichier demandé pour le téléchargement doit être transmis à un gestionnaire de fichiers sur le périphérique de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bb441-105">Although they serve different purposes, both features let websites specify that a file requested for download is passed to a file handler on the user's device.</span></span> <span data-ttu-id="bb441-106">Les demandes ClickOnce sont gérées par le gestionnaire de fichiers natif dans Windows.</span><span class="sxs-lookup"><span data-stu-id="bb441-106">ClickOnce requests are handled by the native file handler in Windows.</span></span> <span data-ttu-id="bb441-107">Les demandes DirectInvoke sont gérées par un gestionnaire de fichiers inscrit spécifié par le site web qui héberge le fichier.</span><span class="sxs-lookup"><span data-stu-id="bb441-107">DirectInvoke requests are handled by a registered file handler specified by the website hosting the file.</span></span>

<span data-ttu-id="bb441-108">Pour plus d’informations sur ces méthodes, voir les articles suivants:</span><span class="sxs-lookup"><span data-stu-id="bb441-108">For more information about these features, see:</span></span>

- [<span data-ttu-id="bb441-109">ClickOnce</span><span class="sxs-lookup"><span data-stu-id="bb441-109">ClickOnce</span></span>](https://docs.microsoft.com/visualstudio/deployment/clickonce-security-and-deployment?view=vs-2019)
- [<span data-ttu-id="bb441-110">DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="bb441-110">DirectInvoke</span></span>]( https://technet.microsoft.com/learning/jj215788(v=vs.94).aspx)

> [!NOTE]
> <span data-ttu-id="bb441-111">Actuellement, Chromium n’offre pas de prise en charge native pour ClickOnce ou DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="bb441-111">Currently, Chromium doesn't provide native support for ClickOnce or DirectInvoke.</span></span>

## <span data-ttu-id="bb441-112">Vue d’ensemble: conditions préalables et processus</span><span class="sxs-lookup"><span data-stu-id="bb441-112">Overview: prerequisites and process</span></span>

<span data-ttu-id="bb441-113">Pour que ClickOnce et DirectInvoke fonctionnent comme prévu et que le gestionnaire de fichiers soit correctement demandé, ce dernier doit être inscrit auprès du système d’exploitation comme prenant en charge ClickOnce ou DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="bb441-113">For ClickOnce and DirectInvoke to work as designed and for the file handler to be successfully requested, the file handler must be registered to the operating system as supporting ClickOnce or DirectInvoke.</span></span> <span data-ttu-id="bb441-114">Cette inscription survient généralement lorsque le système d’exploitation d’origine est installé ou lorsqu’un nouveau programme installé demande la possibilité d’utiliser DirectInvoke pour les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="bb441-114">This registration typically happens when the original operating system is installed or when a new program that's installed requests the ability to use DirectInvoke for updates.</span></span>

<span data-ttu-id="bb441-115">Lorsqu’un site web reçoit une demande de téléchargement qui nécessite ClickOnce ou DirectInvoke, les actions suivantes se produisent:</span><span class="sxs-lookup"><span data-stu-id="bb441-115">When a website receives a download request that requires ClickOnce or DirectInvoke, the following actions happen:</span></span>

- <span data-ttu-id="bb441-116">Le site web demande au navigateur d’utiliser un gestionnaire de fichiers spécifié.</span><span class="sxs-lookup"><span data-stu-id="bb441-116">The website requests that the browser use a specified file handler.</span></span>
- <span data-ttu-id="bb441-117">Le navigateur vérifie le Registre du système d’exploitation pour voir si le gestionnaire de fichiers est inscrit pour le type de fichier demandé.</span><span class="sxs-lookup"><span data-stu-id="bb441-117">The browser checks the operating system registry to see if the file handler is registered for the requested file type.</span></span>
- <span data-ttu-id="bb441-118">Si le gestionnaire de fichiers est inscrit, le navigateur appelle le gestionnaire de fichiers et transmet l’URL en tant qu’argument au gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="bb441-118">If the file handler is registered, the browser calls the file handler and passes the URL as an argument to the file handler.</span></span>
- <span data-ttu-id="bb441-119">Le gestionnaire de fichiers traite l’URL et télécharge le fichier.</span><span class="sxs-lookup"><span data-stu-id="bb441-119">The file handler processes the URL and downloads the file.</span></span>

  > [!NOTE]
  > <span data-ttu-id="bb441-120">L’URL permet de déterminer la source du fichier, ainsi que les paramètres à utiliser lors de l’accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="bb441-120">The URL is used to determine the source of the file, as well as any parameters to use when accessing the file.</span></span>  <span data-ttu-id="bb441-121">Par exemple: points de terminaison, manifeste ou métadonnées.</span><span class="sxs-lookup"><span data-stu-id="bb441-121">For example: endpoints, a manifest, or metadata.</span></span>

## <span data-ttu-id="bb441-122">Cas d’utilisation</span><span class="sxs-lookup"><span data-stu-id="bb441-122">Use cases</span></span>

<span data-ttu-id="bb441-123">Les cas d’utilisation suivants sont représentatifs.</span><span class="sxs-lookup"><span data-stu-id="bb441-123">The following use cases are representative.</span></span>

<span data-ttu-id="bb441-124">Vous pouvez utiliser ClickOnce pour déployer et mettre à jour facilement des logiciels sur des appareils avec une interaction utilisateur minimale.</span><span class="sxs-lookup"><span data-stu-id="bb441-124">You can use ClickOnce to easily deploy and update software on devices with minimal user interaction.</span></span> <span data-ttu-id="bb441-125">Les utilisateurs peuvent installer et exécuter une application Windows en cliquant sur un lien dans une page web.</span><span class="sxs-lookup"><span data-stu-id="bb441-125">Users can install and run a Windows application by clicking a link in a web page.</span></span> <span data-ttu-id="bb441-126">Si elle est correctement configurée, l’application ClickOnce peut installer des programmes sans que les utilisateurs ne définissent des configurations pour le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="bb441-126">If configured correctly, the ClickOnce application can install programs without having users set configurations for the installer.</span></span> <span data-ttu-id="bb441-127">Par exemple, les emplacements de fichiers, les options à installer, etc.</span><span class="sxs-lookup"><span data-stu-id="bb441-127">For example, file locations, what options to install, and so on.</span></span>

<span data-ttu-id="bb441-128">Les cas d’utilisation de DirectInvoke dépendent de l’intention du site web demandant DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="bb441-128">DirectInvoke use cases depend on the intent of the website requesting DirectInvoke.</span></span> <span data-ttu-id="bb441-129">Par exemple, la fonctionnalité de modification de fichiers collaborative de MicrosoftWord.</span><span class="sxs-lookup"><span data-stu-id="bb441-129">For example, the collaborative file-editing feature of Microsoft Word.</span></span> <span data-ttu-id="bb441-130">Au lieu de cliquer sur un lien et de télécharger la copie complète d’un document sur lequel vous travaillez avec vos collègues, DirectInvoke vous permet de télécharger les parties du document qui ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="bb441-130">Instead of clicking a link and downloading the entire copy of a document you're working on with your colleagues, DirectInvoke lets you download the parts of the document that have been changed.</span></span> <span data-ttu-id="bb441-131">Cette stratégie réduit la quantité de données transférées et peut réduire le temps nécessaire à l’ouverture du document.</span><span class="sxs-lookup"><span data-stu-id="bb441-131">This strategy reduces the amount of data transferred and can reduce the time needed to open the document.</span></span>  

## <span data-ttu-id="bb441-132">Prise en charge actuelle de ClickOnce et de DirectInvoke dans MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="bb441-132">Current support for ClickOnce and DirectInvoke in Microsoft Edge</span></span>

<span data-ttu-id="bb441-133">Prise en charge de ClickOnce et de DirectInvoke:</span><span class="sxs-lookup"><span data-stu-id="bb441-133">Support for ClickOnce and DirectInvoke:</span></span>

- <span data-ttu-id="bb441-134">DirectInvoke est pris en charge directement par tous les utilisateurs de Windows, mais ClickOnce est désactivé pour tous les utilisateurs de Windows.</span><span class="sxs-lookup"><span data-stu-id="bb441-134">DirectInvoke is supported out of the box for all Windows users but ClickOnce is disabled for all Windows users.</span></span>

  > [!NOTE]
  > <span data-ttu-id="bb441-135">Les utilisateurs qui ont besoin d’une prise en charge ClickOnce peuvent accéder à edge://flags/#edge-click-once et sélectionner **Activer** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="bb441-135">Users that need ClickOnce support can go to edge://flags/#edge-click-once and select **Enable** from the dropdown list.</span></span> <span data-ttu-id="bb441-136">Vous devez ensuite **Redémarrer** le navigateur.</span><span class="sxs-lookup"><span data-stu-id="bb441-136">You'll have to **Restart** the browser.</span></span>

- <span data-ttu-id="bb441-137">ClickOnce et DirectInvoke ne sont pas pris en charge sur les plateformes autres que Windows.</span><span class="sxs-lookup"><span data-stu-id="bb441-137">ClickOnce and DirectInvoke aren't supported on any platforms other than Windows.</span></span>
- <span data-ttu-id="bb441-138">Dans la mesure où ClickOnce est une fonctionnalité axée sur l’entreprise qui est utilisée par un groupe spécifique d’utilisateurs chevronnés et qu’elle n’est pas destinée à une utilisation générale, ClickOnce est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="bb441-138">Because ClickOnce is an enterprise-focused feature that's used by a specific group of power users and not intended for general use, ClickOnce is disabled by default.</span></span>

## <span data-ttu-id="bb441-139">Sécurité de gestion des fichiers ClickOnce et DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="bb441-139">ClickOnce and DirectInvoke file handling security</span></span>

<span data-ttu-id="bb441-140">ClickOnce et DirectInvoke sont protégés par le service d’analyse de la réputation des URL de Microsoft Defender SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="bb441-140">ClickOnce and DirectInvoke are protected by Microsoft Defender SmartScreen's URL reputation scanning service.</span></span>

<span data-ttu-id="bb441-141">Si une demande ClickOnce ou DirectInvoke est marquée par le service de réputation des URL de Microsoft Defender SmartScreen comme étant dangereuse, les utilisateurs pour lesquels ClickOnce ou DirectInvoke est activé voient deux fenêtres contextuelles.</span><span class="sxs-lookup"><span data-stu-id="bb441-141">If a ClickOnce or a DirectInvoke request is flagged by the Microsoft Defender SmartScreen URL reputation service as unsafe, users with ClickOnce or DirectInvoke enabled will see two popups.</span></span>

<span data-ttu-id="bb441-142">La première fenêtre contextuelle demande à l’utilisateur s’il souhaite ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="bb441-142">The first popup asks the user if they want to open the file.</span></span> <span data-ttu-id="bb441-143">Cette fenêtre contextuelle s’affiche, que le fichier soit marqué comme sûr ou dangereux.</span><span class="sxs-lookup"><span data-stu-id="bb441-143">This popup is displayed regardless of whether the file was flagged as safe or unsafe.</span></span> <span data-ttu-id="bb441-144">L’utilisateur peut **Signaler le fichier comme dangereux**, **Annuler** la demande ou cliquer sur **Ouvrir** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="bb441-144">The user can **Report the file as unsafe**, **Cancel** the request, or click **Open** to continue.</span></span>

   ![Invite d’ouverture du fichier](./media/edge-learn-more-co-di/edge-clickonce-modal-1.png)

<span data-ttu-id="bb441-146">Si l’utilisateur tente d’ouvrir le fichier et que le fichier a été marqué comme dangereux, une deuxième fenêtre contextuelle s’affiche.</span><span class="sxs-lookup"><span data-stu-id="bb441-146">If the user tries to open the file, and the file was flagged as unsafe, a second popup is displayed.</span></span>  <span data-ttu-id="bb441-147">Cette fenêtre contextuelle avertit l’utilisateur que le fichier a été marqué comme dangereux et lui demande s’il souhaite le télécharger.</span><span class="sxs-lookup"><span data-stu-id="bb441-147">This popup warns the user that the file was flagged as unsafe, and asks them if they're sure they want to download the file.</span></span>

<span data-ttu-id="bb441-148">La deuxième fenêtre contextuelle s’affiche uniquement si:</span><span class="sxs-lookup"><span data-stu-id="bb441-148">The second popup only shows up if:</span></span>

- <span data-ttu-id="bb441-149">le fichier est un fichier ClickOnce ou DirectInvoke;</span><span class="sxs-lookup"><span data-stu-id="bb441-149">the file is a ClickOnce or DirectInvoke file</span></span>
- <span data-ttu-id="bb441-150">ClickOnce ou DirectInvoke est activé;</span><span class="sxs-lookup"><span data-stu-id="bb441-150">ClickOnce or DirectInvoke are enabled</span></span>
- <span data-ttu-id="bb441-151">le fichier est marqué comme dangereux.</span><span class="sxs-lookup"><span data-stu-id="bb441-151">the file is flagged as unsafe</span></span>

 ![Invite d’ouverture d’un fichier dangereux](./media/edge-learn-more-co-di/edge-clickonce-modal-2.png)

> [!NOTE]
> <span data-ttu-id="bb441-153">Si ClickOnce ou DirectInvoke est désactivé, les fichiers demandés sont traités comme des téléchargements ordinaires et, s’ils sont signalés comme étant dangereux, ils sont marqués comme dangereux.</span><span class="sxs-lookup"><span data-stu-id="bb441-153">If ClickOnce or DirectInvoke are disabled, requested files are treated as regular downloads and if flagged as unsafe, will be marked as unsafe.</span></span> <span data-ttu-id="bb441-154">Cette procédure est cohérente avec le traitement des autres téléchargements dangereux.</span><span class="sxs-lookup"><span data-stu-id="bb441-154">This is consistent with the treatment of other unsafe downloads.</span></span>

## <span data-ttu-id="bb441-155">Stratégies ClickOnce et DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="bb441-155">ClickOnce and DirectInvoke policies</span></span>

<span data-ttu-id="bb441-156">Il existe deux stratégies de groupe que vous pouvez utiliser pour activer ou désactiver ClickOnce et DirectInvoke pour les utilisateurs d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="bb441-156">There are two group policies that you can use to enable or disable ClickOnce and DirectInvoke for enterprise users.</span></span> <span data-ttu-id="bb441-157">Ces deux stratégies sont [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled) et [DirectInvokeEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#directinvokeenabled).</span><span class="sxs-lookup"><span data-stu-id="bb441-157">These two policies are [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled) and [DirectInvokeEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#directinvokeenabled).</span></span> <span data-ttu-id="bb441-158">Ces deux stratégies sont étiquetées dans l’éditeur de stratégie de groupe en tant que «Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole ClickOnce» et «Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole DirectInvoke», respectivement.</span><span class="sxs-lookup"><span data-stu-id="bb441-158">These two policies are labeled in the Group Policy Editor as "Allow users to open files using the ClickOnce protocol" and "Allow users to open files using the DirectInvoke protocol" respectively.</span></span>

## <span data-ttu-id="bb441-159">Comportement de ClickOnce et DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="bb441-159">ClickOnce and DirectInvoke behavior</span></span>

<span data-ttu-id="bb441-160">Les exemples suivants illustrent la gestion des fichiers lorsque ClickOnce et DirectInvoke sont activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="bb441-160">The following examples show file handling when ClickOnce and DirectInvoke are enabled or disabled.</span></span>

### <span data-ttu-id="bb441-161">ClickOnce activé</span><span class="sxs-lookup"><span data-stu-id="bb441-161">ClickOnce enabled</span></span>

1. <span data-ttu-id="bb441-162">Un utilisateur ouvre un lien vers une page qui demande la prise en charge de ClickOnce et reçoit l’invite présentée dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="bb441-162">A user opens a link to a page that requests ClickOnce support and gets the prompt in the next screenshot.</span></span>

   ![Invite d’ouverture d’un fichier dangereux](./media/edge-learn-more-co-di/edge-clickonce-enabled-1.png)

2. <span data-ttu-id="bb441-164">Lorsque l’utilisateur clique sur **Ouvrir**, ClickOnce tente de lancer l’application.</span><span class="sxs-lookup"><span data-stu-id="bb441-164">After the user clicks **Open**, ClickOnce attempts to launch the application.</span></span>

   ![ClickOnce tente de lancer l’application](./media/edge-learn-more-co-di/edge-clickonce-enabled-launch-app.png)

3. <span data-ttu-id="bb441-166">Lorsque l’utilisateur clique sur **Ouvrir**, le navigateur affiche une fenêtre contextuelle qui demande à l’utilisateur s’il souhaite installer l’application.</span><span class="sxs-lookup"><span data-stu-id="bb441-166">After the user clicks **Open**, the browser shows a popup that asks the user if they're sure they want to install the application.</span></span>

   ![Invite d’ouverture du fichier](./media/edge-learn-more-co-di/edge-clickonce-enabled-2.png)

   > [!NOTE]
   > <span data-ttu-id="bb441-168">L’interface, la messagerie et les options affichées par le gestionnaire de fichiers ClickOnce varient en fonction du type et de la configuration du fichier auquel vous accédez.</span><span class="sxs-lookup"><span data-stu-id="bb441-168">The interface, messaging, and options shown by the ClickOnce file handler will vary depending on the type and configuration of the file that's accessed.</span></span>

### <span data-ttu-id="bb441-169">ClickOnce désactivé</span><span class="sxs-lookup"><span data-stu-id="bb441-169">ClickOnce disabled</span></span>

1. <span data-ttu-id="bb441-170">Lorsqu’un utilisateur ouvre un lien vers une page qui demande la prise en charge de ClickOnce, un message s’affiche dans la barre d’état de téléchargement, semblable à celui de la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="bb441-170">When a user opens a link to a page that requests ClickOnce support, they will see a message in the download tray that is similar to the one in the next screenshot.</span></span>

   ![Invite de téléchargement de fichier](./media/edge-learn-more-co-di/edge-clickonce-disabled-1.png)

### <span data-ttu-id="bb441-172">DirectInvoke activé</span><span class="sxs-lookup"><span data-stu-id="bb441-172">DirectInvoke enabled</span></span>

1. <span data-ttu-id="bb441-173">Un utilisateur ouvre un lien vers une page qui demande la prise en charge de DirectInvoke et reçoit l’invite présentée dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="bb441-173">A user opens a link to a page that requests DirectInvoke support and gets the prompt in the next screenshot.</span></span>

   ![Invite d’ouverture du fichier](./media/edge-learn-more-co-di/edge-directinvoke-open-link-1.png)

2. <span data-ttu-id="bb441-175">Lorsque l’utilisateur clique sur **Ouvrir**, le gestionnaire de fichiers demandé s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="bb441-175">When the user clicks **Open**, the requested file handler is opened.</span></span> <span data-ttu-id="bb441-176">Dans cet exemple, MicrosoftWord est utilisé pour ouvrir le document affiché dans la capture d’écran précédente.</span><span class="sxs-lookup"><span data-stu-id="bb441-176">In this example, Microsoft Word is used to open the document that's shown in the previous screenshot.</span></span>

   > [!NOTE]
   > <span data-ttu-id="bb441-177">L’interface, la messagerie et les options affichées par le gestionnaire de fichiers DirectInvoke varient en fonction du type et de la configuration du fichier auquel vous accédez.</span><span class="sxs-lookup"><span data-stu-id="bb441-177">The interface, messaging, and options shown by the DirectInvoke file handler will vary depending on the type and configuration of the file that's accessed.</span></span>

### <span data-ttu-id="bb441-178">DirectInvoke désactivé</span><span class="sxs-lookup"><span data-stu-id="bb441-178">DirectInvoke disabled</span></span>

1. <span data-ttu-id="bb441-179">Lorsqu’un utilisateur ouvre un lien vers une page qui demande une prise en charge de DirectInvoke, DirectInvoke se comporte de la même manière que lorsque ClickOnce est désactivé.</span><span class="sxs-lookup"><span data-stu-id="bb441-179">When a user opens a link to a page that requests DirectInvoke support, DirectInvoke behaves the same as when ClickOnce is disabled.</span></span> <span data-ttu-id="bb441-180">Un message semblable à celui de la capture d’écran suivante s’affiche dans barre d’état de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="bb441-180">They will see a message in the download tray that's similar to the one in the next screenshot.</span></span>

   ![Invite d’ouverture du fichier](./media/edge-learn-more-co-di/edge-directinvoke-open-link-2.png)

## <span data-ttu-id="bb441-182">Articles associés</span><span class="sxs-lookup"><span data-stu-id="bb441-182">See also</span></span>

- [<span data-ttu-id="bb441-183">Sécurité et déploiement de ClickOnce</span><span class="sxs-lookup"><span data-stu-id="bb441-183">ClickOnce security and deployment</span></span>](https://go.microsoft.com/fwlink/?linkid=2099880)
- [<span data-ttu-id="bb441-184">DirectInvoke dans Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="bb441-184">DirectInvoke in Internet Explorer</span></span>](https://go.microsoft.com/fwlink/?linkid=2099871)
- [<span data-ttu-id="bb441-185">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="bb441-185">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
