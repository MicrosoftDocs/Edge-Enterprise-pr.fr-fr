---
title: Sécurité Microsoft Edge pour votre entreprise
ms.author: collw
author: seanongit
manager: chuckf
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Sécurité Microsoft Edge pour votre entreprise
ms.openlocfilehash: d16b22b63212e3f5319b0bb7df1e457e45cd6208
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642300"
---
# <a name="microsoft-edge-security-for-your-business"></a>Sécurité Microsoft Edge pour votre entreprise

Microsoft Edge s’appuie sur le projet open source de chrome (le projet qui est essentiel de Google Chrome), ce qui signifie qu’il partage la même architecture de sécurité bien conçue et bien testée que la conception de base. L’histoire de la sécurité Microsoft Edge ne s’arrête pas là. En fait, **Microsoft Edge est plus sécurisé que Google Chrome pour votre entreprise sur Windows 10**. Il offre des défenses intégrées et puissantes contre le hameçonnage et les programmes malveillants, et prend en charge l’isolation du matériel de façon native sur Windows 10. Vous n’avez pas besoin d’un logiciel supplémentaire pour atteindre cette base de référence sécurisée. Par ailleurs, en cas de prise en charge native pour les services de sécurité et de conformité Microsoft 365, Microsoft Edge offre des fonctionnalités de sécurité et des fonctionnalités de sécurité avancées qui vous permettent de vous protéger contre la perte de données. Pour plus d’informations, regardez [la vidéo : sécurité, compatibilité et gestion de Microsoft Edge](microsoft-edge-video-security-compatibility-manageability.md).

Nous allons voir les détails, à partir des **menaces externes** et examiner **les risques internes et la protection des informations**.

## <a name="external-threat-protection"></a>Protection contre les menaces externes

### <a name="highest-rated-protection-against-phishing-and-malware"></a>Protection la mieux cotée contre le hameçonnage et les programmes malveillants

Intégré à Microsoft Edge, SmartScreen bloque davantage de tentatives de [hameçonnage](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWASN1) et de [programmes malveillants](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWANMW) que Google Chrome, en fonction d’une étude indépendante de NSS Labs. SmartScreen fournit des vérifications de réputation en temps réel sur les sites et les téléchargements au fur et à mesure que les utilisateurs travaillent en ligne. Il fait partie de la [Sécurité intelligente Microsoft Graph](https://www.microsoft.com/microsoft-365/windows/intelligent-security), qui permet de dessiner des signaux et des informations générés par le réseau de grande envergure de biens généraux, de chercheurs et de partenaires de Microsoft. En exécutant des vérifications sur des listes dynamiques de sites et de téléchargements dangereux, Microsoft Edge permet de détecter et de bloquer même les menaces éphémères qui disparaissent rapidement.  

[Microsoft Edge SmartScreen](//DeployEdge/microsoft-edge-security-smartscreen)a bloqué 95,5% des tentatives d’hameçonnage pendant le test de[Protection contre l’hameçonnage de NSS Labs](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWASN1)et 98,5% des tentatives de programme malveillants pendant le test de [Protection des programmes malveillants de NSS Labs](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWANMW)par rapport aux taux de navigation sécurisée de Chrome de 86,9% et 86,0% respectivement.

### <a name="the-only-browser-on-windows-10-that-natively-supports-hardware-isolation"></a>Le seul navigateur sur Windows 10 qui prend en charge l’isolation du matériel en mode natif

Microsoft Edge est le seul navigateur sur Windows 10 qui prend en charge les fonctionnalités d’isolation de matériel en mode natif. Dans le cadre de Windows 10 Professionnel ou Entreprise, Microsoft Defender Application Guard (Application Guard) exécute les sites non approuvés dans un noyau isolé de l’appareil local et des réseaux internes. Les sites non dignes de confiance sont exécutés dans un « conteneur », de sorte qu’en cas d’attaque, celui-ci est mis en sandbox à partir du reste du réseau d’entreprise. Pour plus d’informations, consultez [Microsoft Edge support pour Application Guard](./microsoft-edge-security-windows-defender-application-guard.md).

Pour Chrome, une extension est disponible pour tirer parti de l’isolation du matériel Windows 10, l’extension MDAG. Cette extension lance ensuite Microsoft Edge afin de tirer parti de l’isolation de niveau noyau de l’Application Guard. De plus, pour obtenir une isolation de niveau noyau similaire pour une solution de chrome uniquement, un logiciel d’isolation tiers est nécessaire.

> [!NOTE]
> Application Guard est disponible sur Windows 10, 1809 et version ultérieure. Application Guard n’est pas disponible dans les éditions Windows 10 Famille.

## <a name="internal-risks-and-information-protection"></a>Risques internes et protection des informations

### <a name="native-support-for-microsoft-365-security-without-additional-software"></a>Prise en charge native de la sécurité Microsoft 365 sans logiciel supplémentaire

Outre la protection contre les menaces externes, les administrateurs informatiques doivent également se prémunir contre les risques internes. La protection des données d’entreprise sensibles (à l’échelle) est une priorité essentielle pour les administrateurs informatiques, notamment lorsque les effectifs ont été décentralisés. Microsoft Edge est le seul navigateur avec une prise en charge native de l’accès conditionnel Azure AD, la Protection des informations Windows et la nouvelle protection contre la perte de données (DLP) Microsoft Endpoint sans nécessiter de logiciel supplémentaire.

**Microsoft Edge est le seul navigateur à prendre en charge en mode natif l’accès conditionnel**. [La prise en charge de Microsoft Edge pour l’accès conditionnel](ms-edge-security-conditional-access.md) permet aux organisations d’utiliser les signaux d’identité dans le cadre de leurs décisions de contrôle d’accès. [L’accès conditionnel](/azure/active-directory/conditional-access/overview) est l’outil utilisé par Azure Active Directory pour rassembler les signaux, prendre des décisions et appliquer des stratégies d’organisation. L’accès conditionnel est au cœur du nouveau plan de contrôle orienté identité. Pour obtenir une prise en charge de l’accès conditionnel sur chrome, un plug-in supplémentaire est nécessaire.

> [!NOTE]
> Microsoft 365 E3 ou une version ultérieure requise pour l’accès conditionnel Azure AD.

**Microsoft Edge est le seul navigateur à prendre en charge en mode natif la Protection des informations Windows (WIP)**, qui assurent la protection des données d’entreprise afin d’éviter les fuites accidentelles d’utilisateurs sur les appareils Windows 10. [Prise en charge de Microsoft Edge pour les travaux en cours](./microsoft-edge-security-windows-information-protection.md) pouvez être configuré pour autoriser uniquement les applications autorisées à accéder aux données d’entreprise. Il fournit également des contrôles de fuite (tels que la protection du presse-papiers, le chiffrement des fichiers au téléchargement et l’interdiction de téléchargement de fichiers sur des partages réseau non autorisés ou sur un emplacement cloud), avec une expérience utilisateur transparente. Le travail en cours utilise une configuration de périmètre dans laquelle les administrateurs informatiques définissent la limite d’entreprise et toutes les données à l’intérieur de cette limite sont considérées comme professionnelles. Chrome n’est pas adapté pour les travaux en cours avec contrôles de fuite.

> [!NOTE]
> La configuration de la Protection des informations Windows (WIP) requiert des licences Microsoft Intune ou Microsoft Endpoint Configuration Manager, ou à l’aide d’une solution de gestion des appareils mobiles tierces, susceptible d’avoir des exigences en matière de licences supplémentaires.

**Microsoft Endpoint Protection contre la perte de données (Endpoint DLP) est uniquement pris en charge en mode natif dans Microsoft Edge**. Microsoft Endpoint Protection contre la perte de données est intégré au centre de sécurité Microsoft et étend la protection des informations à Microsoft Edge pour alerter les utilisateurs et empêcher la perte de données à mesure que les utilisateurs travaillent en ligne. Ce système découvre et libelle les données sensibles à l’intérieur de l’entreprise qui correspondent à des critères définis par l’administrateur, tels que des fichiers contenant des numéros de carte bancaire ou des ID gouvernementaux (par exemple, des numéros de sécurité sociale), des informations financières, et bien plus encore. Vous pouvez déployer des stratégies de protection des informations Microsoft vers Microsoft Endpoint DLP sans reconfiguration supplémentaire, y compris les identificateurs de contenu sensible et les stratégies que les administrateurs informatiques ont déjà personnalisés. Il s’agit d’un déploiement transparent de la protection des informations pour les administrateurs informatiques.

Pour en savoir plus sur les conditions préalables de Microsoft Endpoint Protection contre la perte de données et sur la manière de le configurer, consultez [Prise en main de la protection contre la perte de données de point de terminaison](/microsoft-365/compliance/endpoint-dlp-getting-started?preserve-view=true&view=o365-worldwide).

> [!NOTE]
> Microsoft 365 E5 ou l’abonnement de conformité Microsoft 365 E5 est requis pour Protection contre la perte de données Microsoft Endpoint.

## <a name="see-also"></a>Voir également

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Vidéo : Sécurité, compatibilité et facilité de gestion de Microsoft Edge](microsoft-edge-video-security-compatibility-manageability.md)