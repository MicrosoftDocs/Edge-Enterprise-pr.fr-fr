---
title: Paramètres de confidentialité de Microsoft Edge Enterprise
ms.author: likravit
author: dan-wesley
manager: srugh
ms.date: 05/26/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Configurer les paramètres de confidentialité de Microsoft Edge Enterprise
ms.openlocfilehash: 2b7a33087ae5110c53d18b3192486d4ae62fa540
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979818"
---
# Configurer des stratégies Microsoft Edge pour la prise en charge de la confidentialité entreprise

Microsoft s’engage à fournir aux entreprises les informations et les contrôles nécessaires pour faire des choix concernant la collecte de données dans MicrosoftEdge.

## Vue d'ensemble

Par défaut, Microsoft Edge déployé sur les plateformes non Windows n’envoie pas de données de diagnostic ou d’informations de site vers Microsoft. Lorsque Microsoft Edge est déployé sur Windows10, la valeur par défaut est d’envoyer des données de diagnostic sur la base des [paramètres des données de diagnostic Windows](https://go.microsoft.com/fwlink/?linkid=2099569) de l’utilisateur.

Vous pouvez également configurer la façon dont MicrosoftEdge gère la collecte de données pour votre organisation avec les stratégies de groupe suivantes:

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled): activer les rapports de données d’utilisation et d’incident.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices): Envoyer des informations sur les sites pour améliorer les services Microsoft.

## configurer des paramètres de stratégie,

Avant de commencer, téléchargez et utilisez le dernier modèle de stratégie MicrosoftEdge (pour plus d’informations, consultez [Configurer MicrosoftEdge](configure-microsoft-edge.md)).

### Activer les rapports de données d’utilisation et d’incident

Cette stratégie permet l’envoi à Microsoft de rapports sur l’utilisation et les incidents liés à MicrosoftEdge.

MicrosoftEdge collecte un ensemble de données obligatoires, nécessaires pour garantir la mise à jour, la sécurité et le fonctionnement corrects du produit. Ces données incluent les informations de connectivité et de configuration de périphérique de base provenant de MicrosoftEdge concernant le consentement en matière de collecte de données, la version de l’application et l’état d’installation, concernant votre installation de MicrosoftEdge.Cette collection de données peut être désactivé en désactivant la stratégie.

Activez cette stratégie pour envoyer des rapports sur l’utilisation et les incidents à Microsoft. Désactivez cette stratégie pour ne pas envoyer les données à Microsoft. Dans un cas comme dans l’autre, les utilisateurs ne peuvent pas modifier ou remplacer le paramètre.

Lorsque Microsoft Edge est exécuté sur Windows 10:

- Si cette stratégie n’est pas configurée, MicrosoftEdge est défini par défaut sur le paramètre données de diagnostic Windows.
- Si cette stratégie est activée, MicrosoftEdge envoie des données d’utilisation uniquement si le paramètre de données de Diagnostic Windows est défini sur **Avancé** ou **Complet**.
- Si cette stratégie est désactivée, MicrosoftEdge n’enverra pas de données d’utilisation. Les données liées aux incidents sont envoyées en fonction du paramètre de données de diagnostic Windows. [Si vous souhaitez en savoir plus sur les paramètres de données de diagnostic Windows, rendez-vous sur](https://go.microsoft.com/fwlink/?linkid=2099569).

Lorsque Microsoft Edge est exécuté sur Windows 7, 8 et macOS:

- Si cette stratégie n’est pas configurée, MicrosoftEdge est défini par défaut sur les préférences de l’utilisateur.

### Envoyer des informations sur les sites pour améliorer les services Microsoft

Cette stratégie permet d’envoyer à Microsoft des informations sur les sites web visités dans MicrosoftEdge afin d’améliorer les produits et services Microsoft tels que la fonctionnalité de recherche.

Activez cette stratégie pour envoyer des informations sur les sites web visités dans MicrosoftEdge à Microsoft. Désactivez cette stratégie pour ne pas envoyer à Microsoft d’informations sur les sites web visités dans MicrosoftEdge. Dans un cas comme dans l’autre, les utilisateurs ne peuvent pas modifier ou remplacer le paramètre.

Lorsque Microsoft Edge est exécuté sur Windows 10:

- Si cette stratégie n’est pas configurée, MicrosoftEdge est défini par défaut sur le paramètre données de diagnostic Windows.
- Si cette stratégie est activée, MicrosoftEdge envoie uniquement des informations concernant les sites web visités si le paramètre de données de Diagnostic Windows est défini sur **Complet**.
- Si cette stratégie est désactivée, MicrosoftEdge n’enverra pas d’informations concernant les sites web visités. Pour [en savoir plus sur les paramètres de données de diagnostic Windows](https://go.microsoft.com/fwlink/?linkid=2099569).

Lorsque Microsoft Edge est exécuté sur Windows 7, 8 et macOS:

- Si cette stratégie n’est pas configurée, MicrosoftEdge est défini par défaut sur les préférences de l’utilisateur.

## Détails de la mise en œuvre

Pour que Windows10 comprenne notre implémentation avec la dépendance du paramètre données de Diagnostic Windows, le tableau suivant décrit notre configuration si **Activer les rapports de données d’utilisation et d’incident** et **Envoyer des informations sur les sites pour améliorer les services Microsoft** n’ont pas été configurés.

| Paramètres de données de diagnostic Windows | Activer les rapports de données d’utilisation et d’incident | Envoyer des informations sur les sites pour améliorer les services Microsoft |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| Sécurité                        | Non envoyé                                      | Non envoyé                                            |
| De base                           | Non envoyé                                      | Non envoyé                                            |
| Avancé                        | Envoyé                                          | Non envoyé                                            |
| Complet                            | Envoyé                                          | Envoyé                                                |

Si vos configurations pour Windows10 ne sont pas configurés correctement conformément à le précédent tableau, nous revenons au paramètre de collecte de données moins important.

Par exemple:

- Si vous définissez la stratégie «Activer les rapports de données d’utilisation» et d’incident sur **Activé** mais que le paramètre données de diagnostic Windows est défini sur **De base**. Nous n’envoyons pas les données d’utilisation et d’incident.
- Vous définissez l’option «Envoyer des informations sur les sites pour améliorer les services Microsoft» sur **Désactivé** mais que le paramètre de données de diagnostic Windows est défini sur **Complet**. Nous n’envoyons pas d’informations sur les sites visités.

L’implémentation correcte consiste à définir les précédents paramètres sur «Activer les rapports de données d’utilisation et d’incident» sur **Activé** et définir le paramètre de données de diagnostic Windows sur **Amélioré** ou **Complet**.

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
