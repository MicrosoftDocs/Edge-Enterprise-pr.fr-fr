---
title: Paramètres de confidentialité de Microsoft Edge Enterprise
ms.author: likravit
author: dan-wesley
manager: srugh
ms.date: 09/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer les paramètres de confidentialité de Microsoft Edge Enterprise
ms.openlocfilehash: 25b475206734634df9995f568a6d4e8c52e9f9de
ms.sourcegitcommit: 16984537c8f5c9c60e92f41f0f869231fb79ccd0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "11005492"
---
# Configurer des stratégies Microsoft Edge pour la prise en charge de la confidentialité entreprise

Microsoft s’engage à fournir aux entreprises les informations et les contrôles nécessaires pour faire des choix concernant la collecte de données dans MicrosoftEdge.

## Vue d'ensemble

Lorsque Microsoft Edge est déployé sur Windows10, la valeur par défaut est d’envoyer des données de diagnostic sur la base des [paramètres des données de diagnostic Windows](https://go.microsoft.com/fwlink/?linkid=2099569) de l’utilisateur.

Lorsque Microsoft Edge est déployé sur des plateformes non Windows, les données de diagnostic sont collectées conformément aux paramètres des stratégies de groupe suivantes:

- (DÉCONSEILLÉE) [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled): activer les rapports de données d’utilisation et d’incident. Cette stratégie sera obsolète dans la version89 de Microsoft Edge.
- (DÉCONSEILLÉE) [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices): Envoyer des informations sur les sites pour améliorer les services Microsoft. Cette stratégie sera obsolète dans la version89 de Microsoft Edge.

Ces stratégies déconseillées ci-dessus sont remplacées par [Autoriser la télémétrie](https://go.microsoft.com/fwlink/?linkid=2099569) sur Windows10, et la stratégie [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) pour toutes les autres plateformes.  

## configurer des paramètres de stratégie,

Avant de commencer, téléchargez et utilisez le dernier modèle de stratégie MicrosoftEdge (pour plus d’informations, consultez [Configurer MicrosoftEdge](configure-microsoft-edge.md)).

### Envoyer les données de diagnostic requises et facultatives relatives à l’utilisation du navigateur

Si la stratégie [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) est configurée, elle a priorité sur [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) et [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices).

#### Données de diagnostic requises et facultatives

Les données de diagnostic requises sont collectées pour garantir le niveau attendu de sécurité, de mise à jour et de performance de MicrosoftEdge.

Les données de diagnostic facultatives incluent des données sur l’utilisation du navigateur, des sites web que vous visitez et des rapports de blocage pour renforcer la sécurité, la mise à jour et l’exécution de Microsoft Edge, et permet d’améliorer les produits et services Microsoft Edge et les autres produits et services Microsoft pour tous les utilisateurs.

> [!NOTE]
> Cette stratégie n’est pas prise en charge sur les appareils Windows10. Pour contrôler la collecte de données sur Windows10, les administrateurs informatiques doivent utiliser la stratégie de groupe de données de diagnostic de Windows. Selon la version de Windows, cette stratégie est soit **Autoriser la télémétrie**, soit **Autoriser les données de diagnostic**. Si vous souhaitez en savoir plus sur la [collecte de données de diagnostic Windows10](https://docs.microsoft.com/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

Utilisez l’un des paramètres suivants pour configurer **DiagnosticData**:

- «Désactivé» (non recommandé) (0) désactive la collecte de données de diagnostic requises et facultatives. 
- Données requises (1) envoie les données de diagnostic requises, mais désactive la collecte de données de diagnostic facultatives. MicrosoftEdge envoie les données de diagnostic requises pour garantir le niveau attendu de sécurité, de mise à jour et de performance de MicrosoftEdge. 
- Les données facultatives (2) envoient des données de diagnostic facultatives qui incluent des données sur l’utilisation des navigateurs, des sites web visités, des rapports d’incident envoyés à Microsoft pour renforcer la sécurité, la mise à jour et l’exécution de Microsoft Edge comme prévu. il est utilisé pour améliorer Microsoft Edge et d’autres produits et services Microsoft pour tous les utilisateurs.

Sur Windows7, Windows8/8.1 et macOS, cette stratégie contrôle l’envoi à Microsoft de données de diagnostic requises et facultatives.

Si vous ne configurez pas cette stratégie ou si vous la désactivez, MicrosoftEdge est défini par défaut sur les préférences de l’utilisateur.

### (DÉCONSEILLÉE) Activer les rapports de données d’utilisation et d’incident

Cette stratégie **MetricsReportingEnabled** permet l’envoi à Microsoft de rapports sur l’utilisation et les incidents liés à MicrosoftEdge.

MicrosoftEdge collecte un ensemble de données obligatoires, nécessaires pour garantir la mise à jour, la sécurité et le fonctionnement du produit. Ces données incluent les informations de connectivité et de configuration de périphérique de base provenant de MicrosoftEdge concernant le consentement en matière de collecte de données, la version de l’application et l’état d’installation, concernant votre installation de MicrosoftEdge.Cette collection de données peut être désactivé en désactivant la stratégie.

Activez cette stratégie pour envoyer des rapports sur l’utilisation et les incidents à Microsoft. Désactivez cette stratégie pour ne pas envoyer les données à Microsoft. Dans un cas comme dans l’autre, les utilisateurs ne peuvent pas modifier ou remplacer le paramètre.

Lorsque Microsoft Edge est exécuté sur Windows 10:

- Si cette stratégie n’est pas configurée, MicrosoftEdge est défini par défaut sur le paramètre données de diagnostic Windows.
- Si cette stratégie est activée, MicrosoftEdge envoie des données d’utilisation uniquement si le paramètre de données de Diagnostic Windows est défini sur **Avancé** ou **Complet**.
  - Si cette stratégie est activée, Microsoft Edge enverra uniquement les données d’utilisation si [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) est également activée.
- Si cette stratégie est désactivée, MicrosoftEdge n’enverra pas de données d’utilisation. Les données liées aux incidents sont envoyées en fonction du paramètre de données de diagnostic Windows. [Si vous souhaitez en savoir plus sur les paramètres de données de diagnostic Windows, rendez-vous sur](https://go.microsoft.com/fwlink/?linkid=2099569).

Lorsque Microsoft Edge est exécuté sur Windows 7, 8 et macOS:

- Si cette stratégie n’est pas configurée, MicrosoftEdge est défini par défaut sur les préférences de l’utilisateur.
-  Si cette stratégie est activée, Microsoft Edge enverra uniquement les données d’utilisation si [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) est également activée.

### (DÉCONSEILLÉ) Envoyer des informations sur les sites pour améliorer les services Microsoft

La stratégie **SendSiteInformationToImproveServices** permet d’envoyer à Microsoft des informations sur les sites web visités dans MicrosoftEdge afin d’améliorer les produits et services Microsoft tels que la fonctionnalité de recherche.

Activez cette stratégie pour envoyer des informations sur les sites web visités dans MicrosoftEdge à Microsoft. Désactivez cette stratégie pour ne pas envoyer à Microsoft d’informations sur les sites web visités dans MicrosoftEdge. Dans un cas comme dans l’autre, les utilisateurs ne peuvent pas modifier ou remplacer le paramètre.

Lorsque Microsoft Edge est exécuté sur Windows 10:

- Si cette stratégie n’est pas configurée, MicrosoftEdge est défini par défaut sur le paramètre données de diagnostic Windows.
- Si cette stratégie est activée, MicrosoftEdge envoie uniquement des informations concernant les sites web visités si le paramètre de données de Diagnostic Windows est défini sur **Complet**.
  - Si cette stratégie est activée, Microsoft Edge enverra uniquement les données d’utilisation si [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) est également activée. 
- Si cette stratégie est désactivée, MicrosoftEdge n’enverra pas d’informations concernant les sites web visités. Pour [en savoir plus sur les paramètres de données de diagnostic Windows](https://go.microsoft.com/fwlink/?linkid=2099569).

Lorsque Microsoft Edge est exécuté sur Windows 7, 8 et macOS:

- Si cette stratégie est activée, Microsoft Edge enverra uniquement les données d’utilisation si [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) est également activée.
- Si cette stratégie n’est pas configurée, MicrosoftEdge est défini par défaut sur les préférences de l’utilisateur.

## Détails de la mise en œuvre

Pour les appareils autres que Windows 10: 
- Si la stratégie [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) est configurée, elle a priorité sur [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) et [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices). 
- Si la stratégie [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) n’est pas configurée, Microsoft Edge écoute [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) et [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices).  

Pour que Windows10 comprenne notre implémentation avec la dépendance vis-à-vis du paramètre de données de diagnostic Windows, le tableau suivant indique si **Obligatoire** et **Facultatif** les données de diagnostic sont envoyées à Microsoft.

| Paramètres de données de diagnostic Windows | Données de diagnostic requises  | Données de diagnostic optionnelles |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| Sécurité                        | Non envoyé                                      | Non envoyé                                            |
| De base                           | Envoyé                                      | Non envoyé                                            |
| Avancé                        | Envoyé                                          | Non envoyé                                            |
| Complet                            | Envoyé                                          | Envoyé                                                |

> [!IMPORTANT]
> Microsoft Edge prend en charge **MetricsReportingEnabled** et **SendSiteInfoToImproveServices** pour Microsoft Edge versions86 – 88 incluse. Dans Microsoft Edge version89, **MetricsReportingEnabled** et **SendSiteInfoToImproveServices** ne sera plus prise en charge et prendra par défaut **DiagnosticData** sur les plateformes non Windows10 ou la stratégie **autoriser la télémétrie** pour Windows10.

## Options de stratégie de confidentialité supplémentaires

Vous pouvez envisager les stratégies de groupe suivantes liées à la confidentialité des données:

- Bloquer les cookies sur des sites spécifiques
- Bloquer les cookies tiers
- Configurer Ne pas me suivre
- Désactiver le mode InPrivate

## Articles associés

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Stratégies Microsoft Edge](microsoft-edge-policies.md)
- [Livre blanc sur la confidentialité MicrosoftEdge](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper)
