---
title: Paramètres de confidentialité de Microsoft Edge Enterprise
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Configurer les paramètres de confidentialité de Microsoft Edge Enterprise
ms.openlocfilehash: b5b07353af558e3832cb7a08c647fa111a14a404
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642270"
---
# <a name="configure-microsoft-edge-policies-to-support-enterprise-privacy"></a>Configurer des stratégies Microsoft Edge pour la prise en charge de la confidentialité entreprise

Microsoft s’engage à fournir aux entreprises les informations et les contrôles nécessaires pour faire des choix concernant la collecte de données dans Microsoft Edge.

## <a name="overview"></a>Vue d'ensemble

Lorsque Microsoft Edge est déployé sur Windows 10, la valeur par défaut est d’envoyer des données de diagnostic sur la base des [paramètres des données de diagnostic Windows](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) de l’utilisateur.

Lorsque Microsoft Edge est déployé sur des plateformes non Windows, les données de diagnostic sont collectées conformément aux paramètres des stratégies de groupe suivantes :

- (DÉCONSEILLÉE) [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) : activer les rapports de données d’utilisation et d’incident. Cette stratégie sera obsolète dans la version 89 de Microsoft Edge.
- (DÉCONSEILLÉE) [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) : Envoyer des informations sur les sites pour améliorer les services Microsoft. Cette stratégie sera obsolète dans la version 89 de Microsoft Edge.

Ces stratégies déconseillées ci-dessus sont remplacées par [Autoriser la télémétrie](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) sur Windows 10, et la stratégie [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) pour toutes les autres plateformes.  

## <a name="configure-policy-settings"></a>configurer des paramètres de stratégie,

Avant de commencer, téléchargez et utilisez le dernier modèle de stratégie Microsoft Edge (pour plus d’informations, consultez [Configurer Microsoft Edge](configure-microsoft-edge.md)).

### <a name="send-required-and-optional-diagnostic-data-about-browser-usage"></a>Envoyer les données de diagnostic requises et facultatives relatives à l’utilisation du navigateur

Si la stratégie [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) est configurée, elle a priorité sur [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) et [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).

#### <a name="required-and-optional-diagnostic-data"></a>Données de diagnostic requises et facultatives

Les données de diagnostic requises sont collectées pour garantir le niveau attendu de sécurité, de mise à jour et de performance de Microsoft Edge.

Les données de diagnostic facultatives incluent des données sur l’utilisation du navigateur, des sites web que vous visitez et des rapports de blocage pour renforcer la sécurité, la mise à jour et l’exécution de Microsoft Edge, et permet d’améliorer les produits et services Microsoft Edge et les autres produits et services Microsoft pour tous les utilisateurs.

> [!NOTE]
> Cette stratégie n’est pas prise en charge sur les appareils Windows 10. Pour contrôler la collecte de données sur Windows 10, les administrateurs informatiques doivent utiliser la stratégie de groupe de données de diagnostic de Windows. Selon la version de Windows, cette stratégie est soit **Autoriser la télémétrie**, soit **Autoriser les données de diagnostic**. Si vous souhaitez en savoir plus sur la [collecte de données de diagnostic Windows 10](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

Utilisez l’un des paramètres suivants pour configurer **DiagnosticData** :

- « Désactivé » (non recommandé) (0) désactive la collecte de données de diagnostic requises et facultatives. 
- Données requises (1) envoie les données de diagnostic requises, mais désactive la collecte de données de diagnostic facultatives. Microsoft Edge envoie les données de diagnostic requises pour garantir le niveau attendu de sécurité, de mise à jour et de performance de Microsoft Edge. 
- Les données facultatives (2) envoient des données de diagnostic facultatives qui incluent des données sur l’utilisation des navigateurs, des sites web visités, des rapports d’incident envoyés à Microsoft pour renforcer la sécurité, la mise à jour et l’exécution de Microsoft Edge comme prévu. il est utilisé pour améliorer Microsoft Edge et d’autres produits et services Microsoft pour tous les utilisateurs.

Sur Windows 7, Windows 8/8.1 et macOS, cette stratégie contrôle l’envoi à Microsoft de données de diagnostic requises et facultatives.

Si vous ne configurez pas cette stratégie ou si vous la désactivez, Microsoft Edge est défini par défaut sur les préférences de l’utilisateur.

### <a name="deprecated-enable-usage-and-crash-related-data-reporting"></a>(DÉCONSEILLÉE) Activer les rapports de données d’utilisation et d’incident

Cette stratégie **MetricsReportingEnabled** permet l’envoi à Microsoft de rapports sur l’utilisation et les incidents liés à Microsoft Edge.

Microsoft Edge collecte un ensemble de données obligatoires, nécessaires pour garantir la mise à jour, la sécurité et le fonctionnement du produit. Ces données incluent les informations de connectivité et de configuration de périphérique de base provenant de Microsoft Edge concernant le consentement en matière de collecte de données, la version de l’application et l’état d’installation, concernant votre installation de Microsoft Edge.Cette collection de données peut être désactivé en désactivant la stratégie.

Activez cette stratégie pour envoyer des rapports sur l’utilisation et les incidents à Microsoft. Désactivez cette stratégie pour ne pas envoyer les données à Microsoft. Dans un cas comme dans l’autre, les utilisateurs ne peuvent pas modifier ou remplacer le paramètre.

Lorsque Microsoft Edge est exécuté sur Windows 10 :

- Si cette stratégie n’est pas configurée, Microsoft Edge est défini par défaut sur le paramètre données de diagnostic Windows.
- Si cette stratégie est activée, Microsoft Edge envoie des données d’utilisation uniquement si le paramètre de données de Diagnostic Windows est défini sur **Avancé** ou **Complet**.
  - Si cette stratégie est activée, Microsoft Edge enverra uniquement les données d’utilisation si [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) est également activée.
- Si cette stratégie est désactivée, Microsoft Edge n’enverra pas de données d’utilisation. Les données liées aux incidents sont envoyées en fonction du paramètre de données de diagnostic Windows. [Si vous souhaitez en savoir plus sur les paramètres de données de diagnostic Windows, rendez-vous sur](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

Lorsque Microsoft Edge est exécuté sur Windows 7, 8 et macOS :

- Si cette stratégie n’est pas configurée, Microsoft Edge est défini par défaut sur les préférences de l’utilisateur.
-  Si cette stratégie est activée, Microsoft Edge enverra uniquement les données d’utilisation si [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) est également activée.

### <a name="deprecated-send-site-information-to-improve-microsoft-services"></a>(DÉCONSEILLÉ) Envoyer des informations sur les sites pour améliorer les services Microsoft

La stratégie **SendSiteInformationToImproveServices** permet d’envoyer à Microsoft des informations sur les sites web visités dans Microsoft Edge afin d’améliorer les produits et services Microsoft tels que la fonctionnalité de recherche.

Activez cette stratégie pour envoyer des informations sur les sites web visités dans Microsoft Edge à Microsoft. Désactivez cette stratégie pour ne pas envoyer à Microsoft d’informations sur les sites web visités dans Microsoft Edge. Dans un cas comme dans l’autre, les utilisateurs ne peuvent pas modifier ou remplacer le paramètre.

Lorsque Microsoft Edge est exécuté sur Windows 10 :

- Si cette stratégie n’est pas configurée, Microsoft Edge est défini par défaut sur le paramètre données de diagnostic Windows.
- Si cette stratégie est activée, Microsoft Edge envoie uniquement des informations concernant les sites web visités si le paramètre de données de Diagnostic Windows est défini sur **Complet**.
  - Si cette stratégie est activée, Microsoft Edge enverra uniquement les données d’utilisation si [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) est également activée. 
- Si cette stratégie est désactivée, Microsoft Edge n’enverra pas d’informations concernant les sites web visités. Pour [en savoir plus sur les paramètres de données de diagnostic Windows](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

Lorsque Microsoft Edge est exécuté sur Windows 7, 8 et macOS :

- Si cette stratégie est activée, Microsoft Edge enverra uniquement les données d’utilisation si [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) est également activée.
- Si cette stratégie n’est pas configurée, Microsoft Edge est défini par défaut sur les préférences de l’utilisateur.

## <a name="implementation-details"></a>Détails de la mise en œuvre

Pour les appareils autres que Windows 10 : 
- Si la stratégie [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) est configurée, elle a priorité sur [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) et [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices). 
- Si la stratégie [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) n’est pas configurée, Microsoft Edge écoute [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) et [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).  

Pour que Windows 10 comprenne notre implémentation avec la dépendance vis-à-vis du paramètre de données de diagnostic Windows, le tableau suivant indique si **Obligatoire** et **Facultatif** les données de diagnostic sont envoyées à Microsoft.

| Paramètres de données de diagnostic Windows | Données de diagnostic requises  | Données de diagnostic optionnelles |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| Sécurité                        | Non envoyé                                      | Non envoyé                                            |
| De base                           | Envoyé                                      | Non envoyé                                            |
| Avancé                        | Envoyé                                          | Non envoyé                                            |
| Complet                            | Envoyé                                          | Envoyé                                                |

> [!IMPORTANT]
> Microsoft Edge prend en charge **MetricsReportingEnabled** et **SendSiteInfoToImproveServices** pour Microsoft Edge versions 86 – 88 incluse. Dans Microsoft Edge version 89, **MetricsReportingEnabled** et **SendSiteInfoToImproveServices** ne sera plus prise en charge et prendra par défaut **DiagnosticData** sur les plateformes non Windows 10 ou la stratégie **autoriser la télémétrie** pour Windows 10.

## <a name="additional-privacy-policy-options"></a>Options de stratégie de confidentialité supplémentaires

Vous pouvez envisager les stratégies de groupe suivantes liées à la confidentialité des données :

- Bloquer les cookies sur des sites spécifiques
- Bloquer les cookies tiers
- Configurer Ne pas me suivre
- Désactiver le mode InPrivate

## <a name="see-also"></a>Articles associés

- [Page d’accueil Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Stratégies Microsoft Edge](microsoft-edge-policies.md)
- [Livre blanc sur la confidentialité Microsoft Edge](/microsoft-edge/privacy-whitepaper)