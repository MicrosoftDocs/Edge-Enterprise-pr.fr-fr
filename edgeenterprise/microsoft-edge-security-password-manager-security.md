---
title: 'Sécurité du gestionnaire des mots de passe Microsoft Edge '
ms.author: v-andreabarr
author: AndreaLBarr
manager: collw
ms.date: 05/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Sécurité du gestionnaire des mots de passe Microsoft Edge
ms.openlocfilehash: 830658dd1ff577bfb88be5512c955d556c437bcb
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618111"
---
# <a name="microsoft-edge-password-manager-security"></a>Sécurité du gestionnaire des mots de passe Microsoft Edge 

Les questions fréquemment posées dans cet article décrivent comment le gestionnaire des mots de passe intégré de Microsoft Edge offre une sécurité des mots de passe des utilisateurs.

> [!Note]
>Cet article concerne MicrosoftEdge version77 ou ultérieure.

## <a name="how-are-passwords-stored-in-microsoft-edge-and-how-safe-is-this-approach"></a>Comment les mots de passe sont-ils stockés dans MicrosoftEdge et quel est le niveau de sécurité de cette approche?

MicrosoftEdge stocke les mots de passe chiffrés sur disque. Elles sont chiffrées à l’aide d’AES256 et la clé de chiffrement est enregistrée dans une zone de stockage du système d’exploitation (SE). Cette technique est appelée chiffrement de données locales. Bien que toutes les données du navigateur ne soient pas chiffrées, les données sensibles telles que les mots de passe, les numéros de carte de crédit et les cookies sont chiffrées lorsqu’elles sont enregistrées.

Le gestionnaire des mots de passe Microsoft Edge chiffre les mots de passe afin qu’ils soient accessibles uniquement lorsqu’un utilisateur est connecté au système d’exploitation. Même si un attaquant dispose de droits d’administrateur ou d’accès hors connexion et peut accéder aux données stockées localement, le système est conçu pour empêcher l’attaquant d’obtenir les mots de passe en texte brut d’un utilisateur qui n’est pas connecté.

La façon de déchiffrer les mots de passe d’un autre utilisateur est si cet utilisateur était connecté et que l’attaquant disposait du mot de passe de l’utilisateur ou qu’il a compromis le contrôleur de domaine.

### <a name="about-the-encryption-method"></a>À propos de la méthode de chiffrement

La clé de chiffrement du profil est protégée à l’aide d’OSCrypt de Chromium et utilise les emplacements de stockage de système d’exploitation spécifiques à la plateforme suivants:

- Sur Windows, la zone de stockage est DPAPI

- Sur Mac, la zone de stockage est Keychain

- Sur Linux, la zone de stockage est Gnome Keyring ou KWallet

Toutes ces zones de stockage chiffrent la clé AES256 à l’aide d’une clé accessible à tout ou partie des processus s’exécutant en tant que l’utilisateur. Ce vecteur d’attaque est souvent présenté dans les blogs comme une «attaque» ou une «vulnérabilité» possible, ce qui constitue une mauvaise compréhension du modèle de menace du navigateur et de la posture de sécurité.

Toutefois, les attaques locales physiques et les programmes malveillants sont en dehors du modèle de menace et, dans ces conditions, les données chiffrées sont vulnérables. Si votre ordinateur est infecté par un programme malveillant, une personne malveillante peut obtenir un accès déchiffré aux zones de stockage du navigateur. Le code de l’attaquant, qui s’exécute en tant que compte d’utilisateur, peut faire tout ce que vous pouvez faire.

## <a name="why-encrypt-data-locally-why-not-store-the-encryption-key-elsewhere-or-make-it-harder-to-obtain"></a>Pourquoi chiffrer les données localement? Pourquoi ne pas stocker la clé de chiffrement ailleurs ou rendre l’obtention plus difficile?

Les navigateurs Internet (y compris MicrosoftEdge) ne sont pas équipés de défenses pour se protéger contre les menaces lorsque l’intégralité de l’appareil est compromise en raison d’un programme malveillant s’exécutant en tant que l’utilisateur sur l’ordinateur. Toutefois, les programmes, tels que les MicrosoftDefenderSmartScreen et les protections au niveau du système d’exploitation tels que WindowsDefender, sont conçus pour s’assurer, pour commencer, que l’appareil n’est pas compromis.

Malgré son incapacité à se protéger contre les programmes malveillants de confiance totale, le chiffrement de données locales est utile dans certains scénarios. Par exemple, si une personne malveillante trouve le moyen de voler des fichiers sur le disque sans pouvoir exécuter de code ou qu’elle a volé un ordinateur portable qui n’est pas protégé par le chiffrement de disque complet, le chiffrement de données local complique l’accès aux données stockées.

## <a name="do-you-recommend-storing-passwords-in-microsoft-edge"></a>Est-ce que vous recommandez de stocker les mots de passe Microsoft Edge?

Les utilisateurs qui peuvent s’appuyer sur le gestionnaire de mots de passe intégré de MicrosoftEdge peuvent (et utilisent) des mots de passe plus forts et uniques, car ils n’ont pas besoin de les mémoriser tous et de les taper aussi souvent. Et comme le gestionnaire de mots de passe ne remplira que les mots de passe sur les sites auxquels ils appartiennent, les utilisateurs sont moins susceptibles d’être la cause d’une attaque par hameçonnage.

> [!Note]
>Les rapports du secteur indiquent que 80% des incidents en ligne sont liés au hameçonnage et que plus de 37% des utilisateurs non formés échouent aux tests de hameçonnage.

Le gestionnaire de mots de passe de Microsoft Edge est pratique et facilement distribué, ce qui contribue à une sécurité améliorée. Lorsqu’il est combiné avec la synchronisation, vous pouvez obtenir tous vos mots de passe sur tous vos appareils et il est facile d’utiliser un mot de passe différent pour chaque site web. Vous pouvez utiliser des mots de passe longs et complexes que vous n’avez pas à mémoriser pour chaque site et ignorer la difficulté de taper une chaîne complexe à chaque fois. La commodité du gestionnaire des mots de passe signifie qu’il existe moins de risques d’être victime d’une tentative d’hameçonnage.

Toutefois, l’utilisation d’un gestionnaire de mots de passe qui est essentiel à la session de connexion du système d’exploitation de l’utilisateur signifie également qu’une personne malveillante dans cette session peut immédiatement récupérer tous les mots de passe enregistrés par l’utilisateur. Sans gestionnaire de mots de passe auprès duquel dérober, un adversaire doit suivre les frappes de touches ou surveiller les mots de passe envoyés.

La décision d’utiliser ou non un gestionnaire de mots de passe revient à évaluer les nombreux avantages que nous avons décrits par rapport à la possibilité que la totalité de l’appareil soit compromis. Pour la plupart des modèles de menace, l’utilisation du gestionnaire de mots de passe MicrosoftEdge est l’option recommandée.

> [!Note]
>Si une entreprise est concernée par le vol d’un mot de passe spécifique ou si un site est compromis en raison d’un mot de passe volé, des précautions supplémentaires doivent être prises. Certaines solutions efficaces qui permettent d’atténuer ce type d’incident sont l'authentification unique (SSO) via ActiveDirectory, AzureActiveDirectory ou un tiers. Les autres solutions incluent 2FA (par exemple, [MS Authenticator](/azure/active-directory/user-help/user-help-auth-app-download-install)) ou [WebAuthN](https://webauthn.guide/).

## <a name="should-a-password-manager-be-enabled-by-an-organization"></a>Un gestionnaire de mots de passe doit-il être activé par une organisation?

La réponse simple et rapide est : oui, utilisez le gestionnaire de mots de passe du navigateur.

Une réponse plus complète signifie une connaissance approfondie de votre modèle de menace, car les options et les choix de sécurité varient en fonction de différents modèles de menace. Voici quelques questions pertinentes à prendre en considération lorsque vous envisagez d’activer ou non le gestionnaire de mots de passe pour votre organisation:

- Quels types d’attaquants vous préoccupent?

- Sur quels types de sites web vos utilisateurs se connectent-ils?

- Vos utilisateurs sélectionnent-ils des mots de passe forts et uniques?

- Les comptes de vos utilisateurs sont-ils protégés par 2FA?

- Quels types d’attaques sont les plus probables?

- Comment protéger vos appareils d’entreprise contre les programmes malveillants?

- Quelle est la tolérance personnelle de vos utilisateurs aux désagréments?

- Prenez en compte l’impact de la synchronisation des données.

Il est important de prendre en compte la sécurité des données utilisateur à mesure qu’elles sont synchronisées avec différents appareils utilisateur et le degré de contrôle dont dispose l’organisation sur la synchronisation des données de remplissage automatique.

Synchronisation des données MicrosoftEdge:

- La synchronisation des données peut être activée ou désactivée comme vous le souhaitez au sein de l’organisation.

- Sécurité des données en transit et au repos dans le cloud: toutes les données synchronisées sont chiffrées en transit sur HTTPS lorsqu’elles sont transférées entre le navigateur et les serveurs Microsoft. Les données synchronisées sont également stockées dans un état chiffré sur les serveurs Microsoft. Les types de données sensibles tels que les adresses et les mots de passe sont chiffrés sur l’appareil avant d’être synchronisés. Si vous utilisez un compte scolaire ou scolaire, tous les types de données sont chiffrés avant d’être synchronisés à l’aide de Microsoft Information Protection.

## <a name="why-do-microsoft-security-baselines-recommend-disabling-the-password-manager"></a>Pourquoi les lignes de base de la sécurité Microsoft recommandent-elles de désactiver le gestionnaire de mots de passe?

L’équipe de sécurité Microsoft a actuellement évalué l’impact d’un ver qui compromet un réseau de PCS Enterprise (causant la perte de toutes les informations d’identification dans les gestionnaires de mots de passe de tous les appareils) comme étant plus grave que le risque (plus probable mais impact plus faible) d’attaques par hameçonnage ciblées qui compromettent les informations d’identification saisies par un seul utilisateur.

Cette évaluation est en cours de discussion et peut faire l’objet de modifications avec l’ajout de nouvelles fonctionnalités d’amélioration de la sécurité MicrosoftEdge.

## <a name="can-malicious-extensions-gain-access-to-passwords"></a>Les extensions malveillantes peuvent-elles accéder aux mots de passe?

Une extension avec l’autorisation d’interagir avec une page est intrinsèquement en mesure d’accéder à n’importe quoi dans cette page, y compris un mot de passe de rempli automatiquement. De même, une extension malveillante peut modifier le contenu des champs de formulaire et des demandes/réponses réseau pour utiliser incorrectement l’autorité du contexte de connexion de l’utilisateur actuel.

Toutefois, MicrosoftEdge fournit un ensemble étendu de stratégies qui permettent un contrôle précis sur les extensions installées. L’utilisation des stratégies du tableau suivant est nécessaire pour protéger les données d’entreprise.

| Stratégie | Sous-titre |
|-|-|
|[BlockExternalExtensions](/deployedge/microsoft-edge-policies#blockexternalextensions)|Empêche l’installation d’extensions externes|
|[ExtensionAllowedTypes](/deployedge/microsoft-edge-policies#extensionallowedtypes)|Configurer les types d’extension autorisés|
|[ExtensionInstallAllowlist](/deployedge/microsoft-edge-policies#extensioninstallallowlist)|Autoriser l’installation d’extensions spécifiques|
|[ExtensionInstallBlocklist](/deployedge/microsoft-edge-policies#extensioninstallblocklist)|Déterminer les extensions ne pouvant pas être installées|
|[ExtensionInstallForcelist](/deployedge/microsoft-edge-policies#extensioninstallforcelist)|Contrôler l’installation silencieuse de certaines extensions|
|[ExtensionInstallSources](/deployedge/microsoft-edge-policies#extensioninstallsources)|Configurer les sources d’installation des extensions et des scripts d’utilisateur|
| [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) |Configurer les paramètres de gestion des extensions |

## <a name="how-does-the-microsoft-edge-password-manager-compare-with-a-third-party-product"></a>Comment le gestionnaire de mots de passe MicrosoftEdge est-il comparé à un produit tiers?

Le tableau suivant montre comment le gestionnaire de mots de passe MicrosoftEdge est comparé aux gestionnaires de mots de passe tiers.

| Gestionnaire de mots de passe tiers | Gestionnaire de mots de passe Microsoft Edge|
|-|-|
| *Synchronisation du serveur*. Certains produits stockent les mots de passe dans le cloud pour synchroniser tous vos appareils. Cette fonctionnalité est utile, mais elle présente un risque si le service cloud est compromis et que vos données sont exposées. **Remarques:** Le risque est atténué en faisant en sorte que les mots de passe soient chiffrés dans le cloud et en stockant la clé de chiffrement sur votre(vos) appareil(s) afin que des personnes malveillantes ne puissent pas obtenir la clé et vos mots de passe.| Il existe un risque d’exposition au cloud, car les mots de passe sont synchronisés sur les appareils Windows sur lesquels MicrosoftEdge est installé. **Remarques:** Ce risque est atténué par les étapes de sécurité des données couvertes dans cet article.|
| *Approbation*. Il est nécessaire d’être sûr que le tiers ne fait rien de malveillant, par exemple l’envoi de vos mots de passe à une autre partie. **Remarques:**   Ce risque peut être atténué en réviser le code source (dans le cas des produits open source) ou en estimant que le fournisseur se soucie de sa réputation et de ses revenus. | **Remarques:** Microsoft est un fournisseur connu et approuvé qui fournit depuis des années une sécurité et une productivité de niveau entreprise, avec des ressources conçues pour protéger vos mots de passe dans le monde entier. |
| *Sécurité de la chaîne logistique*. Il est difficile de vérifier que le fournisseur dispose de processus sécurisés de chaîne logistique/de build/publication pour le code source. |**Remarques:** Microsoft dispose de processus internes robustes pour garantir un risque minimal pour le code source. |
| *Client ou compte compromis*.Si un appareil client ou un compte utilisateur est compromis, une personne malveillante peut obtenir les mots de passe. **Remarques:** Ce risque est atténué pour certains gestionnaires de mots de passe qui exigent que l’utilisateur entre un mot de passe principal qui n’est pas stocké localement pour déchiffrer les mots de passe.Un mot de passe principal n’est qu’une atténuation partielle, car un attaquant peut lire les frappes et obtenir le mot de passe principal lorsqu’il est tapé ou lu à partir de la mémoire du processus lors du remplissage d’un champ de formulaire. | **Remarques:** Microsoft offre des protections au niveau du système d’exploitation, telles que WindowsDefender, conçues pour s’assurer que l’appareil n’est pas compromis au départ. Toutefois, si un appareil client est compromis, un attaquant peut être en mesure de déchiffrer les mots de passe. |

> [!Note]
> Les produits tiers peuvent fournir une protection contre les modèles de menaces supplémentaires, mais cela s’effectue au détriment de la complexité ou de la facilité d’utilisation. Le gestionnaire de mots de passe MicrosoftEdge est conçu pour fournir une gestion pratique et facile à utiliser des mots de passe qui peut être entièrement contrôlée par les administrateurs informatiques à l’aide de la stratégie de groupe et ne nécessite pas l’approbation d’un tiers.

## <a name="why-doesnt-microsoft-offer-a-master-password-to-protect-the-data"></a>Pourquoi Microsoft ne propose-t-il pas de mot de passe principal pour protéger les données?

Lorsque les mots de passe du navigateur sont chiffrés sur disque, la clé de chiffrement est disponible pour tout processus sur votre appareil, y compris les programmes malveillants s’exécutant localement. Même si les mots de passe sont chiffrés dans un «coffre» par une clé principale, ils sont déchiffrés lors du chargement dans l’espace mémoire du navigateur et peuvent être supprimés après le déverrouillage du coffre.

Une fonctionnalité mot de passe principal (qui authentifie l’utilisateur avant de remplir automatiquement ses données) offre un compromis de commodité pour une atténuation plus étendue des menaces. Plus précisément, il permet de réduire la fenêtre d’exposition des données contre les programmes malveillants latents ou les personnes malveillantes locales. Toutefois, un mot de passe principal n’est pas une panacée et les attaquants locaux et les programmes malveillants dédiés ont différentes stratégies pour contourner la protection d’un mot de passe principal.

> [!Note]
> Microsoft reconnaît la valeur de l’authentification des utilisateurs avant le remplissage automatique et cette fonctionnalité sera ajoutée à MicrosoftEdge dans une prochaine version.

## <a name="can-using-a-password-manager-impact-my-privacy"></a>L’utilisation d’un gestionnaire de mots de passe peut-elle avoir un impact sur ma confidentialité?

Non, pas si des mesures sont prises pour protéger l’accès à vos mots de passe enregistrés.

Il existe une exploitation connue que certains annonceurs utilisent, qui utilise des mots de passe stockés pour identifier et suivre les utilisateurs de manière unique. Pour plus d’informations, voir  [Les ciblages publicitaires qui extraient des données à partir du gestionnaire de mots de passe de votre navigateur](https://www.theverge.com/2017/12/30/16829804/browser-password-manager-adthink-princeton-research). Les navigateurs ont pris des mesures pour atténuer ce [problème de confidentialité](https://bugs.chromium.org/p/chromium/issues/detail?id=798492).La classe PasswordValueGatekeeper peut être utilisée pour limiter l’accès aux données de champ de mot de passe, même lorsque le navigateur est configuré pour le remplissage automatique lors du chargement.

Cette menace de collecte d’informations utilisateur peut être facilement atténuée en activant la fonctionnalité edge://flags/#fill-on-account-select facultative. Cette fonctionnalité permet uniquement d’ajouter des mots de passe à un champ de formulaire une fois que l’utilisateur a choisi explicitement des informations d’identification, ce qui garantit que les utilisateurs restent informés de la personne qui reçoit leur mot de passe.

## <a name="see-also"></a>Voir également

[Page d’accueil MicrosoftEdgeEntreprise](https://www.microsoft.com/edge/business/download)

[Comment MicrosoftEdge est plus sécurisé que Chrome pour les entreprises sur Windows10](/DeployEdge/ms-edge-security-for-business)
