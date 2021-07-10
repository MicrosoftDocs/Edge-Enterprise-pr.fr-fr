---
title: Interruption des téléchargements de fichiers potentiellement dangereux
ms.author: kvice
author: AndreaLBarr
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Interruption des téléchargements de fichiers potentiellement dangereux
ms.openlocfilehash: 527b98b54cf03f6c116624296c63803b57a7f0c4
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642670"
---
# <a name="interrupting-downloads-of-potentially-dangerous-files"></a>Interruption des téléchargements de fichiers potentiellement dangereux

Le composant stratégies de type de fichier de Microsoft Edge permet de classer les fichiers selon leur niveau de «dangerosité», de sorte que les fichiers sans danger (par exemple, `.txt`fichiers) peuvent être téléchargés librement, et que les fichiers potentiellement dangereux (par exemple,`.dll`fichiers) sont soumis à un niveau de contrôle plus élevé et à une expérience utilisateur plus sensible à la sécurité.

## <a name="determining-the-danger-level-of-a-file-type"></a>Détermination du niveau de danger d’un type de fichier

Microsoft Edge hérite ses stratégies de type de fichier du navigateur Chromium en amont; affichez le contenu actuel de la liste[ici](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb). Dans la liste, vous verrez que chaque type possède une danger_level, qui est l’une des trois valeurs:`DANGEROUS`, `NOT_DANGEROUS`, ou `ALLOW_ON_USER_GESTURE`.

Les deux premières sont simples: ** NOT_DANGEROUS** signifie que le fichier peut être téléchargé en toute sécurité, même si le téléchargement a été accidentel. **DANGEREUX** signifie que le navigateur doit toujours avertir l’utilisateur que le téléchargement peut endommager son appareil.

Le troisième paramètre **ALLOW_ON_USER_GESTURE** est plus discret. Ces fichiers sont potentiellement dangereux, mais très probablement inoffensifs si l’utilisateur a demandé le téléchargement. Microsoft Edge autorisera des téléchargements automatiquement si deux conditions sont remplies:

1. Il y a un [mouvement de l’utilisateur](https://textslashplain.com/2020/05/18/browser-basics-user-gestures/) associé à la demande réseau qui a initié le téléchargement (par exemple, l’utilisateur a cliqué sur un lien de téléchargement).
2. Il existe une visite préalable enregistrée à l’origine de la référence (la page reliée au téléchargement) avant le plus récent minuit (c’est-à-dire, hier ou antérieurement). Ça implique que l’utilisateur a un historique de la visite du site.

Le téléchargement va aussi se poursuivre automatiquement si l’utilisateur l’a lancé explicitement à l’aide du lien ** Enregistrer en tant que** commande de menu contextuel, a entré l’URL du téléchargement directement dans la barre d’adresses du navigateur, ou si Microsoft Defender SmartScreen a indiqué que le fichier est sécurisé.

**Mise à jour:** À partir de la version 91, Microsoft Edge interrompra les téléchargements qui n’ont pas le mouvement requis.

## <a name="user-experience-for-downloads-lacking-gestures"></a>Expérience utilisateur pour les téléchargements de mouvements d’accès

Si un téléchargement pour un type potentiellement dangereux démarre sans le mouvement requis, Microsoft Edge indique que le téléchargement «a été bloqué ». Les commandes nommées `Keep` et `Delete` sont disponibles à partir de... menu sur l’élément de téléchargement pour permettre à l’utilisateur de continuer ou d’annuler le téléchargement.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/Dowload-was-blocked.png" alt-text="Le téléchargement a été bloqué":::

Sur la `edge://downloads`, page, l’utilisateur verra les mêmes options: 

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/msg-keep-delete-option.png" alt-text="Option conserver la suppression MSG":::

## <a name="enterprise-controls"></a>Entreprise de contrôles 

Bien que les utilisateurs soient peu susceptibles de rencontrer des interruptions de téléchargement pour les sites qu’ils utilisent quotidiennement, ils peuvent les rencontrer pour des téléchargements légitimes sur des sites qu’ils utilisent rarement. Pour simplifier l’expérience utilisateur pour les entreprises, une stratégie de groupe est disponible.

Les entreprises peuvent utiliser [exemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) pour spécifier les types de fichiers autorisés à télécharger à partir de sites spécifiques sans interruption. Par exemple, la stratégie suivante autorise le téléchargement de fichiers XML de se télécharger à partir de contoso.com et woodgrovebank.com sans interruption, et les fichiers MSG à télécharger à partir de n’importe quel site.

`[{"file_extension":"xml","domains":["contoso.com", "woodgrovebank.com"]},
{"file_extension":"msg", "domains": ["*"]}]`

## <a name="file-types-requiring-a-gesture"></a>Types de fichiers nécessitant un mouvement

Les dernières [stratégies de types de fichiers](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb) sont publiées dans le code source Chromium. Depuis mai 2021, les types de fichiers avec un `danger_level` et `ALLOW_ON_USER_GESTURE`sur au moins une plateforme de système d'exploitation sont les suivants:
`crx, pl, py, pyc, pyo, pyw, rb, efi, oxt, msi, msp, mst, ade, adp, mad, maf, mag, mam, maq, mar, mas, mat, mav, maw, mda, mdb, mde, mdt, mdw, mdz, accdb, accde, accdr, accda, ocx, ops, paf, pcd, pif, plg, prf, prg, pst, cpi, partial, xrm-ms, rels, svg, xml, xsl, xsd, ps1, ps1xml, ps2, ps2xml, psc1, psc2, js, jse, vb, vbe, vbs, vbscript, ws, wsc, wsf, wsh, msh, msh1, msh2, mshxml, msh1xml, msh2xml, ad, app, application, appref-ms, asp, asx, bas, bat, chi, chm, cmd, com, cpl, crt, cer, der, eml, exe, fon, fxp, hlp, htt, inf, ins, inx, isu, isp, job, lnk, mau, mht, mhtml, mmc, msc, msg, reg, rgs, scr, sct, search-ms, settingcontent-ms, shb, shs, slk, u3p, vdx, vsx, vtx, vsdx, vssx, vstx, vsdm, vssm, vstm, vsd, vsmacros, vss, vst, vsw, xnk, cdr, dart, dc42, diskcopy42, dmg, dmgpart, dvdr, dylib, img, imgpart, ndif, service, smi, sparsebundle, sparseimage, toast, udif, action, definition, wflow, caction, as, cpgz, command, mpkg, pax, workflow, xip, mobileconfig, configprofile, internetconnect, networkconnect, pkg, deb, pet, pup, rpm, slp, out, run, bash, csh, ksh, sh, shar, tcsh, desktop, dex,apk`

## <a name="danger-level-may-vary-by-operating-system"></a>Le niveau de danger peut varier selon système d’exploitation

Les paramètres de type de fichier varient parfois en fonction de la plateforme de système d’exploitation client. Par exemple, un `.exe` n’est pas dangereux sur un Mac, tandis qu’un `.applescript`n’est pas dangereux sur Windows.
