---
title: Microsoft Edge et les téléchargements de contenu mixte
ms.author: kele
author: dan-wesley
manager: srugh
ms.date: 04/30/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge et les téléchargements de contenu mixte
ms.openlocfilehash: 13cc9d935dfe415039078b2ca794945b4fa2d1a3
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447268"
---
# <a name="learn-about-microsoft-edge-and-mixed-content-downloads"></a><span data-ttu-id="bd160-103">Découvrez Microsoft Edge et les téléchargements de contenu mixte</span><span class="sxs-lookup"><span data-stu-id="bd160-103">Learn about Microsoft Edge and mixed content downloads</span></span>

<span data-ttu-id="bd160-104">Cet article décrit les téléchargements de contenu mixte et leur traitement par Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bd160-104">This article explains mixed content downloads and how Microsoft Edge handles them.</span></span>

>[!NOTE]
><span data-ttu-id="bd160-105">Cet article concerne MicrosoftEdge version85 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bd160-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <a name="what-are-mixed-content-downloads"></a><span data-ttu-id="bd160-106">Quels sont les téléchargements de contenu mixte?</span><span class="sxs-lookup"><span data-stu-id="bd160-106">What are mixed content downloads?</span></span>

<span data-ttu-id="bd160-107">Un téléchargement de contenu mixte se produit lorsque vous démarrez un téléchargement à partir d’une page HTML qui a été chargée sur une connexion HTTPS sécurisée, mais que l’une des conditions suivantes existe:</span><span class="sxs-lookup"><span data-stu-id="bd160-107">A mixed content download happens when you start a download from an HTML page that was loaded over a secure HTTPS connection, but one of the following conditions exists:</span></span>

- <span data-ttu-id="bd160-108">Au moins une des redirections de l’emplacement de téléchargement a été chargée via une connexion HTTP non sécurisée.</span><span class="sxs-lookup"><span data-stu-id="bd160-108">One or more of the download location's redirects was loaded over an insecure HTTP connection.</span></span>
- <span data-ttu-id="bd160-109">L’emplacement final de téléchargement a été chargé via une connexion HTTP non sécurisée.</span><span class="sxs-lookup"><span data-stu-id="bd160-109">The final download location was loaded over an insecure HTTP connection.</span></span>

<span data-ttu-id="bd160-110">Les deux scénarios sont un contenu mixte, car la demande a été effectuée à l’aide d'une connexion HTTPS sécurisée et que les contenus HTTP et HTTPS sont impliqués dans l'accession à la destination finale du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="bd160-110">Either scenario is a mixed content because the request was made using secure HTTPS and both HTTP and HTTPS content are involved in reaching the final download destination.</span></span> <span data-ttu-id="bd160-111">Les navigateurs modernes affichent des avertissements sur ce type de contenu pour indiquer à l’utilisateur que ce téléchargement ne peut pas être transféré de manière non sécurisée, même si la page d’origine consultée était sécurisée.</span><span class="sxs-lookup"><span data-stu-id="bd160-111">Modern browsers display warnings about this type of content to indicate to the user that this download may be transferred insecurely even though the original page accessed was secure.</span></span>

## <a name="download-warnings-and-user-options"></a><span data-ttu-id="bd160-112">Télécharger des avertissements et options de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="bd160-112">Download warnings and user options</span></span>

<span data-ttu-id="bd160-113">L’avertissement de téléchargement permet aux utilisateurs de savoir que le fichier qu’ils téléchargent peut être lu par des pirates sur leur réseau.</span><span class="sxs-lookup"><span data-stu-id="bd160-113">The download warning ensures that users know that the file they're downloading could be read by malicious attackers on their network.</span></span> <span data-ttu-id="bd160-114">Cet avertissement permet à un utilisateur de prendre une décision éclairée sur le téléchargement ou non du fichier.</span><span class="sxs-lookup"><span data-stu-id="bd160-114">This warning lets a user make an informed decision on whether to download the file.</span></span>

<span data-ttu-id="bd160-115">Dans Microsoft Edge, les téléchargements de contenu mixte sont bloqués, mais les utilisateurs peuvent passer outre et télécharger le fichier s’ils le souhaitent.</span><span class="sxs-lookup"><span data-stu-id="bd160-115">In Microsoft Edge, mixed content downloads will be blocked but users can override and download the file if they want to.</span></span> <span data-ttu-id="bd160-116">Microsoft Edge prévoit de commencer à bloquer les téléchargements de fichiers exécutables de contenu mixte à partir de Microsoft Edge version85 et bloquera différents types de fichiers dans les prochaines versions.</span><span class="sxs-lookup"><span data-stu-id="bd160-116">Microsoft Edge plans on starting to block mixed content executable file downloads starting with Microsoft Edge version 85 and will block different filetypes in future releases.</span></span>

> [!NOTE]
> <span data-ttu-id="bd160-117">Le déploiement de cette fonctionnalité peut faire l’objet de modifications en fonction du calendrier des publications et des commentaires des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bd160-117">Deployment of this feature is subject to change based on release schedule and user feedback.</span></span>

<!-- The schedule of the block for different filetypes is to be determined and may be impacted by usage data and user feedback. -->

<span data-ttu-id="bd160-118">Dans l’étagère de téléchargement, le message d’avertissement du blocage se présente comme l’exemple de la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="bd160-118">In the download shelf, the block warning message looks like the example in the next screenshot.</span></span>

 ![Avertissement de contenu mixte dans le plateau de téléchargement](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-tray-warning.png)

<span data-ttu-id="bd160-120">Sur la page de téléchargement, l’avertissement de blocage se présente comme dans la capture d’écran suivante:</span><span class="sxs-lookup"><span data-stu-id="bd160-120">On the download page, the block warning looks like the following screenshot example:</span></span>

 ![Invite d'ignorer le contenu mixte](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-page-warning.png)

<span data-ttu-id="bd160-122">Si un utilisateur décide de conserver le téléchargement, il est invité à confirmer son action.</span><span class="sxs-lookup"><span data-stu-id="bd160-122">If a user decides to keep the download, they are prompted to confirm their action.</span></span> <span data-ttu-id="bd160-123">La capture d’écran suivante présente un exemple de cette invite de confirmation.</span><span class="sxs-lookup"><span data-stu-id="bd160-123">The next screenshot shows an example of this confirmation prompt.</span></span>

 ![Choisissez Mode InternetExplorer](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-override.png)

## <a name="supporting-policies"></a><span data-ttu-id="bd160-125">Stratégies d'appui</span><span class="sxs-lookup"><span data-stu-id="bd160-125">Supporting policies</span></span>

<span data-ttu-id="bd160-126">Les entreprises souhaitant exclure le blocage de contenu mixte de certains sites web peuvent utiliser la stratégie [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) pour le faire.</span><span class="sxs-lookup"><span data-stu-id="bd160-126">Enterprises that want to exclude mixed content blocking from specific websites can use the [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) policy to do so.</span></span>

## <a name="content-license"></a><span data-ttu-id="bd160-127">Licence de contenu</span><span class="sxs-lookup"><span data-stu-id="bd160-127">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="bd160-128">Certaines parties de cette page sont des modifications basées sur le travail créé et partagé par Chromium.org et utilisé conformément aux conditions décrites dans la [Licence internationale Creative Commons Attribution4.0](http://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="bd160-128">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="bd160-129">La page d’origine est disponible [ici](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).</span><span class="sxs-lookup"><span data-stu-id="bd160-129">The original page can be found [here](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="bd160-130">Ce travail est concédé sous une <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licence internationale Creative Commons Attribution4.0</a>.</span><span class="sxs-lookup"><span data-stu-id="bd160-130">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd160-131">Voir également</span><span class="sxs-lookup"><span data-stu-id="bd160-131">See also</span></span>

- [<span data-ttu-id="bd160-132">Page d’accueil MicrosoftEdge Entreprise</span><span class="sxs-lookup"><span data-stu-id="bd160-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)