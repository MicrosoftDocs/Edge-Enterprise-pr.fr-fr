---
title: Qu'est-ce que le mode Internet Explorer?
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 02/26/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Découvrez comment le mode Internet Explorer dans Microsoft Edge permet d’accéder aux sites qui ont besoin d’Internet Explorer 11 et d’accéder aux sites modernes.
ms.openlocfilehash: 5ca14c4d448b573dc7de6781ce86ee62281a48a4
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470222"
---
# <a name="what-is-internet-explorer-ie-mode"></a>Qu’est-ce qu’Internet Explorer ?

Nous avons créé le mode Internet Explorer (IE) dans Microsoft Edge pour les organisations qui ont encore besoin d’Internet Explorer 11 pour la compatibilité vers l’arrière avec des sites web existants, mais qui ont également besoin d’un navigateur moderne. Cette fonctionnalité permet aux organisations d’utiliser un seul navigateur, pour les applications web héritées ou pour une application web/moderne. Cet article vous propose une introduction à l’utilisation de Microsoft Edge avec le mode IE.

> [!NOTE]
> Cet article concerne Microsoft Edge version 77 ou ultérieure.

## <a name="what-is-ie-mode"></a>Qu’est-ce que le mode IE ?

Le mode IE sur Microsoft Edge simplifie l’utilisation de tous les sites nécessaires à votre organisation dans un seul navigateur. Il utilise le moteur Chromium intégré pour les sites modernes et utilise le moteur Trident MSHTML d’Internet Explorer 11 (IE11) pour les sites hérités.

Lorsqu’un site se charge en mode IE, l’indicateur du logo Internet Explorer s’affiche sur le côté gauche de la barre de navigation. Vous pouvez cliquer sur l’indicateur du logo Internet Explorer pour afficher des informations supplémentaires, comme illustré ci-après :

  ![Indicateur du logo Internet Explorer](./media/ie-mode/ie-logo-indicator1.png)

Seuls les sites configurés spécifiquement (via une stratégie) utiliseront le mode IE, tous les autres sites seront affichés sous forme de sites web modernes. Pour qu’un site utilise le mode Internet Explorer, vous devez :

- Répertorier le site dans l'élément XML de la liste des sites en Mode entreprise défini dans l’une de ces stratégies :
  - Microsoft Edge 78 ou version ultérieure, « Configurer la liste des sites en mode Entreprise »
  - Internet Explorer, « Utiliser la liste des sites Web en mode Entreprise d’Internet Explorer »
  > [!NOTE]
  > Nous ne traitons qu’une seule liste de sites en Mode entreprise. La stratégie de liste de sites Microsoft Edge est prioritaire sur la stratégie de liste de sites Internet Explorer.
- Tous les sites intranet dont la stratégie de groupe **Envoyer tous les sites intranet vers Internet Explorer** est activée (Microsoft Edge 77 ou version ultérieure).

### <a name="ie-mode-supports-the-following-internet-explorer-functionality"></a>Le mode IE prend en charge les fonctionnalités Internet Explorer suivantes

- Tous les modes document et les modes entreprise
- Contrôles ActiveX (par exemple, Java ou Silverlight)
- Objets application d’assistance du navigateur 
- Les paramètres et stratégies de groupe Internet Explorer qui affectent les paramètres de zone de sécurité et le mode protégé
- Les outils de développement F12 pour IE lorsqu'ils sont lancés avec [IEChooser](/office/dev/add-ins/testing/debug-add-ins-using-f12-developer-tools-on-windows-10)
- Les extensions Microsoft Edge (extensions qui interagissent directement avec le contenu de la page IE ne sont pas prises en charge.)

### <a name="ie-mode-doesnt-support-the-following-internet-explorer-functionality"></a>Le mode IE ne prend pas en charge les fonctionnalités Internet Explorer suivantes

- Barres d’outils Internet Explorer
- Paramètres et stratégies de groupe Internet Explorer qui affectent le menu de navigation (par exemple, moteurs de recherche et pages d’accueil).
- Outils de développement IE11 ou Microsoft Edge F12

## <a name="prerequisites"></a>Conditions préalables

Les prérequis suivants concernent l’utilisation de Microsoft Edge avec le mode IE.

> [!IMPORTANT]
> Pour vous garantir le succès, installez les dernières mises à jour pour Windows et Microsoft Edge. Si ce n’est pas le cas, le mode Internet Explorer risque d'échouer.

1. Les mises à jour système minimales pour les systèmes d’exploitation sont indiqués dans le tableau suivant.

 | Système d’exploitation | Version       | Mises à jour |
 |------------------|---------------|---------|
 | Windows 10       | 1909 ou version ultérieure |         |
 | Windows 10       | 1903          | [KB4501375](https://support.microsoft.com/help/4501375/windows-10-update-kb4501375) ou version ultérieure |
 | Windows Server   | 1903          | [KB4501375](https://support.microsoft.com/help/4501375/windows-10-update-kb4501375) ou version ultérieure |
 | Windows 10       | 1809          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) ou version ultérieure |
 | Windows Server   | 1809          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) ou version ultérieure |
 | Windows Server   | 2019          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) ou version ultérieure |
 | Windows 10       | 1803          | [KB4512509](https://support.microsoft.com/help/4512509/windows-10-update-kb4512509) ou version ultérieure |
 | Windows 10       | 1709          | [KB4512494](https://support.microsoft.com/help/4512494/windows-10-update-kb4512494) ou version ultérieure |
 | Windows 10       | 1607          | [KB4516061](https://support.microsoft.com/help/4516061/windows-10-update-kb4516061) ou version ultérieure |
 | Windows Server   | 2016          | [KB4516061](https://support.microsoft.com/help/4516061/windows-10-update-kb4516061) ou version ultérieure |
 | Windows 10       | version initiale, juillet 2015 | [KB4520011](https://support.microsoft.com/help/4520011/windows-10-update-kb4520011) ou version ultérieure |
 | Windows 8       | 8.1              | [KB4507463](https://support.microsoft.com/help/4507463/july-16-2019-kb4507463-os-build-preview-of-monthly-rollup) ou version ultérieure ; ou [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) ou version ultérieure |
 | Windows Server   | 2012 R2       | [KB4507463](https://support.microsoft.com/help/4507463/july-16-2019-kb4507463-os-build-preview-of-monthly-rollup) ou version ultérieure ; ou [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) ou version ultérieure |
 | Windows 8  | Incorporé            | Installez [KB4492872](https://support.microsoft.com/help/4492872/update-for-internet-explorer-april-16-2019) pour mettre à jour vers Internet Explorer 11, puis installez [KB4507447](https://support.microsoft.com/help/4507447/windows-server-2012-update-kb4507447) ou version ultérieure ou [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) ou version ultérieure |
 | Windows Server   | 2012           | Installez [KB4492872](https://support.microsoft.com/help/4492872/update-for-internet-explorer-april-16-2019) pour mettre à jour vers Internet Explorer 11, puis installez [KB4507447](https://support.microsoft.com/help/4507447/windows-server-2012-update-kb4507447) ou version ultérieure ou [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) ou version ultérieure |
 | Windows 7        |  SP1**        | [KB4507437](https://support.microsoft.com/help/4507437/windows-7-update-kb4507437) ou version ultérieure ; ou [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) ou version ultérieure |
 | Windows Server   |  2008 R2**    | [KB4507437](https://support.microsoft.com/help/4507437/windows-7-update-kb4507437) ou version ultérieure ; ou [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) ou version ultérieure |
  > [!IMPORTANT]
  > ** Windows 7 et Windows Server 2008 R2 seront pris en charge par Microsoft Edge même après la fin du support de ces systèmes d’exploitation. Pour que le mode IE soit pris en charge sur ces systèmes d’exploitation, les appareils doivent disposer des [Mises à jour de sécurité étendues pour Windows 7](https://support.microsoft.com/help/4527878/faq-about-extended-security-updates-for-windows-7). Nous vous recommandons d’effectuer une mise à jour vers un système d’exploitation pris en charge dès que possible afin de maintenir la sécurité. La prise en charge de Microsoft Edge avec les mises à jour de sécurité étendues doit être considérée comme un pont temporaire pour obtenir un état de système d’exploitation pris en charge.

2. Modèle d’administration Microsoft Edge. Pour plus d’informations, voir [Configurer Microsoft Edge](./configure-microsoft-edge.md).
3. Internet Explorer 11 activé dans les fonctionnalités de Windows.

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Informations supplémentaires sur le mode entreprise](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)