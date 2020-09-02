---
title: Conserver la navigation dans la page en mode Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Conserver la navigation dans la page en mode Internet Explorer
ms.openlocfilehash: 0acca9e05a0d09b02fa61d5ddd7de3f7c6cabb92
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979762"
---
# <span data-ttu-id="76f6a-103">Conserver la navigation dans la page en mode Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="76f6a-103">Keep in-page navigation in Internet Explorer mode</span></span>

<span data-ttu-id="76f6a-104">Vous pouvez utiliser cette stratégie comme solution temporaire pour forcer toute navigation dans la page des sites en mode Internet Explorer (mode IE) à conserver ce mode.</span><span class="sxs-lookup"><span data-stu-id="76f6a-104">You can use this policy as a temporary solution to force all in-page navigation from Internet Explorer mode (IE mode) sites to stay in IE mode.</span></span>

<span data-ttu-id="76f6a-105">Une navigation dans la page est lancée à partir d'un lien, d'un script ou d'un formulaire de la page en cours.</span><span class="sxs-lookup"><span data-stu-id="76f6a-105">An in-page navigation is started from a link, a script, or a form on the current page.</span></span> <span data-ttu-id="76f6a-106">Il peut également s'agir d'une redirection côté serveur d'une précédente tentative de navigation dans la page.</span><span class="sxs-lookup"><span data-stu-id="76f6a-106">It can also be a server-side redirect of a previous in-page navigation attempt.</span></span> <span data-ttu-id="76f6a-107">À l’inverse, un utilisateur peut démarrer une navigation qui n’est pas «dans la page» et qui est indépendante de la page active de plusieurs façons en utilisant les contrôles du navigateur.</span><span class="sxs-lookup"><span data-stu-id="76f6a-107">Conversely, a user can start a navigation that isn't in-page that's independent of the current page in several ways by using the browser controls.</span></span> <span data-ttu-id="76f6a-108">Par exemple, à l’aide de la barre d’adresses, du bouton précédent ou d’un lien favori.</span><span class="sxs-lookup"><span data-stu-id="76f6a-108">For example, using the address bar, the back button, or a favorite link.</span></span>

>[!NOTE]
><span data-ttu-id="76f6a-109">Cet article concerne MicrosoftEdge version81 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="76f6a-109">This article applies to Microsoft Edge version 81 or later.</span></span>

## <span data-ttu-id="76f6a-110">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="76f6a-110">Prerequisites</span></span>

<span data-ttu-id="76f6a-111">Les mises à jour Windows suivantes sont nécessaires pour cette stratégie:</span><span class="sxs-lookup"><span data-stu-id="76f6a-111">The following Windows updates are required for this policy:</span></span>

- <span data-ttu-id="76f6a-112">Windows 10 version 1909 et 1903, Windows Server version 1909 et 1903  ([KB4532695](https://support.microsoft.com/help/4532695))</span><span class="sxs-lookup"><span data-stu-id="76f6a-112">Windows 10 version 1909 & 1903, Windows Server version 1909 & 1903  ([KB4532695](https://support.microsoft.com/help/4532695))</span></span>
- <span data-ttu-id="76f6a-113">Windows 10 version 1809, Windows Server version 1809, Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span><span class="sxs-lookup"><span data-stu-id="76f6a-113">Windows 10 version 1809, Windows Server version 1809, Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span></span>
- <span data-ttu-id="76f6a-114">Windows 10 version 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span><span class="sxs-lookup"><span data-stu-id="76f6a-114">Windows 10 version 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span></span>
- <span data-ttu-id="76f6a-115">Windows 10 version 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span><span class="sxs-lookup"><span data-stu-id="76f6a-115">Windows 10 version 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span></span>


## <span data-ttu-id="76f6a-116">À propos de cette stratégie</span><span class="sxs-lookup"><span data-stu-id="76f6a-116">About this policy</span></span>

<span data-ttu-id="76f6a-117">Cette stratégie vous indique le temps d’identification et de configuration de tous les serveurs d’authentification utilisés par vos sites de mode IE.</span><span class="sxs-lookup"><span data-stu-id="76f6a-117">This policy gives you time to identify and configure all of the authentication servers used by your IE mode sites.</span></span> <span data-ttu-id="76f6a-118">Toutefois, cette stratégie peut se traduire par une expérience de navigation incohérente dans laquelle certains sites sont affichés en mode IE et à d’autres moments affichés en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76f6a-118">However, this policy can result in an inconsistent browsing experience, where some sites are rendered in IE mode and at other times rendered in Microsoft Edge mode.</span></span> <span data-ttu-id="76f6a-119">Cette expérience dépend selon que la navigation vers le site à partir a commencé ou non dans une page en mode IE.</span><span class="sxs-lookup"><span data-stu-id="76f6a-119">This experience depends on whether the navigation to the site began from an IE mode page.</span></span> <span data-ttu-id="76f6a-120">Les sites qui ne sont pas explicitement configurés pour s’ouvrir dans un moteur de rendu spécifique sont soumis à cette incohérence.</span><span class="sxs-lookup"><span data-stu-id="76f6a-120">Any site that isn't explicitly configured to open in a specific rendering engine will be subject to this inconsistency.</span></span>

<span data-ttu-id="76f6a-121">Si vous activez cette stratégie, nous vous recommandons de la désactiver une fois que vous avez identifié tous les serveurs d’authentification et que vous les avez ajoutés à la liste des sites comme étant neutres.</span><span class="sxs-lookup"><span data-stu-id="76f6a-121">If you enable this policy, we recommend that you disable it after you've identified all the authentication servers and added them to the site list as neutral.</span></span> <span data-ttu-id="76f6a-122">Cette action garantit que vos sites modernes ne s’affichent jamais en mode IE par inadvertance.</span><span class="sxs-lookup"><span data-stu-id="76f6a-122">This action ensures that your modern sites never inadvertently render in IE mode.</span></span>

## <span data-ttu-id="76f6a-123">Conserver la navigation dans la page en mode InternetExplorer</span><span class="sxs-lookup"><span data-stu-id="76f6a-123">Keep in-page navigation in IE mode</span></span>

<span data-ttu-id="76f6a-124">Pour conserver la navigation automatique ou dans toutes les navigations dans la page en mode Internet Explorer, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="76f6a-124">To keep automatic or all in-page navigation in Internet Explorer mode, follow these steps:</span></span>

1. <span data-ttu-id="76f6a-125">Ouvrez l'Éditeur d'objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="76f6a-125">Open Local Group Policy Editor.</span></span>
2. <span data-ttu-id="76f6a-126">Cliquez sur **Configuration ordinateur** > **Modèles d’administration** > **MicrosoftEdge**.</span><span class="sxs-lookup"><span data-stu-id="76f6a-126">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
3. <span data-ttu-id="76f6a-127">Sous **Paramètre**, double-cliquez sur **Spécifier la manière dont les navigations «dans la page» vers les sites non configurés se comportent lorsque vous lancez à partir des pages du mode Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="76f6a-127">Under **Setting**, double-click **Specify how "in-page" navigations to unconfigured sites behave when started from Internet Explorer mode pages**.</span></span>

   ![Paramètre de la stratégie dans la page](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-settings.png)

4. <span data-ttu-id="76f6a-129">Sélectionnez **Activé**</span><span class="sxs-lookup"><span data-stu-id="76f6a-129">Select **Enabled**</span></span> 

   ![Activer la stratégie dans la page](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-enable.png)

5. <span data-ttu-id="76f6a-131">Choisissez l'une des options suivantes dans la liste déroulante:</span><span class="sxs-lookup"><span data-stu-id="76f6a-131">Choose one of the following options from the dropdown list:</span></span>

   - <span data-ttu-id="76f6a-132">**Par défaut** : sites uniquement configurés pour s’ouvrir en mode Internet Explorer s’ouvrent dans ce mode.</span><span class="sxs-lookup"><span data-stu-id="76f6a-132">**Default** - Only sites configured to open in Internet Explorer mode will open in that mode.</span></span> <span data-ttu-id="76f6a-133">Tout site non configuré pour s’ouvrir en mode Internet Explorer est redirigé vers Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76f6a-133">Any site not configured to open in Internet Explorer mode will be redirected back to Microsoft Edge.</span></span>
   - <span data-ttu-id="76f6a-134">**Garder uniquement les navigations automatiques en mode Internet Explorer** : utilisez cette option si vous souhaitez utiliser l’expérience par défaut, sauf que toutes les navigations automatiques (telles que les redirections 302) vers des sites non configurés continuent en mode Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="76f6a-134">**Keep only automatic navigations in Internet Explorer mode** - Use this option if you want the default experience except that all automatic navigations (such as 302 redirects) to unconfigured sites will be kept in Internet Explorer mode.</span></span>
   - <span data-ttu-id="76f6a-135">**Conserver toutes les navigations à l’intérieur des pages en mode Internet Explorer** ***(option la moins recommandée)*** : toutes les navigations à partir de pages chargées en mode IE vers des sites non configurés continuent en mode Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="76f6a-135">**Keep all in-page navigation in Internet Explorer mode** ***(Least Recommended)*** - All navigations from pages loaded in IE mode to unconfigured sites are kept in Internet Explorer mode.</span></span>

6. <span data-ttu-id="76f6a-136">Cliquez sur **OK** ou sur **Appliquer** pour enregistrer les paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="76f6a-136">Click **OK** or **Apply** to save the policy settings.</span></span>

## <span data-ttu-id="76f6a-137">Voir également</span><span class="sxs-lookup"><span data-stu-id="76f6a-137">See also</span></span>

- [<span data-ttu-id="76f6a-138">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="76f6a-138">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
