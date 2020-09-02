---
title: Syntaxe expression régulière2
ms.author: comanea
author: dan-wesley
manager: seanlyn
ms.date: 06/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Syntaxe expression régulière2
ms.openlocfilehash: 9654a25d2c0474601fb719b145ebb1f59241a6d9
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979748"
---
# Syntaxe expression régulière 2 (re2.h)

Les expressions régulières sont une notation permettant de décrire des jeux de chaînes de caractères. Lorsqu’une chaîne se trouve dans le groupe décrit par une expression régulière, l’expression régulière correspond souvent à la chaîne.

L’expression régulière la plus simple est un caractère littéral unique. À l’exception des métacaractères tels que *\ * +? ()|*, les caractères correspondent eux-mêmes. Pour faire correspondre un métacaractère, faites-le glisser avec une barre oblique inverse: \ + correspond à un signe plus.

Deux expressions régulières peuvent être modifiées ou concaténées pour former une nouvelle expression régulière: si *e<sub>1</sub>* correspond à _s_ et *e<sub>2</sub>* correspond à _t_, puis*e<sub>1</sub>* | *e<sub>2</sub>* correspond à _s_ ou _t_, et *e<sub>1</sub>* *e<sub>2</sub>*  correspond à _st_.

Les métacaractères _\*_ , _+_ et _?_ les opérateurs de répétition sont les suivants: *e<sub>1</sub>* _\*_ correspond à une séquence de zéro ou plusieurs chaînes (peut-être différente) qui correspondent *e<sub>1</sub>*; *e<sub>1</sub>* _+_ correspond à un ou plusieurs; *e<sub>1</sub>* _?_ correspond à zéro ou à un.

La priorité de l’opérateur, de la plus faible à la liaison la plus forte, est la première alternative, la concaténation et enfin les opérateurs de répétition. Des parenthèses explicites peuvent être utilisées pour imposer des significations différentes, comme dans les expressions arithmétiques. Voici quelques exemples: _ab|cd_ équivaut à _(ab)|(cd)_; _ab\*_ équivaut à _a(b\*)_ .

La syntaxe décrite jusqu'à présent est la plupart de la syntaxe traditionnelle d'expression régulière Unix _egrep_. Ce sous-ensemble suffit à décrire toutes les langues standard: en fait, une langue standard est un ensemble de chaînes qui peuvent être mises en correspondance en une seule passe dans le texte en utilisant uniquement une quantité fixe de mémoire. Les nouvelles fonctionnalités des expressions régulières (notamment Perl et celles qui ont été copiées) ont ajouté de nombreux opérateurs et séquences d’échappement, ce qui rend les expressions régulières plus concises, voire plus énigmatiques, mais généralement plus puissantes.

Cette page répertorie la syntaxe de l’expression régulière acceptée par RE2.

Elle répertorie également une syntaxe acceptée par PCRE, PERL et VIM.

## Tables de syntaxe

| Types d’expressions à un seul caractère | Exemples |
| --- | --- |
| tout caractère, éventuellement avec une nouvelle ligne (s=true) | . |
| classe de caractères | [xyz] |
| classe de caractères inversée | [^xyz] |
| Classe de caractères perl ([lien](#user-content-perl)) | \d |
| classe de caractères perl inversée | \D |
| Classe de caractères ASCII ([lien](#user-content-ascii)) | [[:alpha:]] |
| classe de caractères ASCII inversée | [[:^alpha:]] |
| Classe de caractères Unicode (nom à une lettre) | \pN |
| Classe de caractères Unicode | \p{Greek} |
| classe de caractères Unicode inversée (nom à une lettre) | \PN |
| classe de caractères Unicode inversée | \P{Greek} |

| | Composites |
| --- | --- |
| xy | x suivi par y |
| x\|y | x ou y (de préférence x) |

| | Répétitions |
| --- | --- |
| x\* | zéro ou plus x, préférer plus |
| x+ | zéro ou plus x, préférer plus |
| x? | zéro ou un x, préférer un |
| x{n,m} | n ou n + 1 ou... ou m x, préférer plus |
| x{n,} | zéro ou plus x, préférer plus |
| x{n} | exactement n x |
| x\*? | zéro ou plus x, préférer moins |
| x+? | un ou plus x, préférer moins |
| x?? | zéro ou un x, préférer zéro |
| x{n,m}? | n ou n + 1 ou... ou m x, préférer moins |
| x{n,}? | n ou plus x, préférer moins |
| x{n,}? | exactement n x |
| x{} | (≡ x\*) (NON PRIS EN CHARGE) VIM |
| x{-} | (≡ x\*?) (NON PRIS EN CHARGE) VIM |
| x{-n} | (≡ x{n}?) (NON PRIS EN CHARGE) VIM |
| x= | (≡ x?) (NON PRIS EN CHARGE) VIM |

Restriction d’implémentation: les formulaires de comptage x {n, m}, x {n,} et x {n} refusent les formulaires qui créent un nombre de répétitions minimum ou maximum au-dessus de 1000. Les répétitions illimitées ne sont pas sujettes à cette restriction.

| | Répétitions de possession |
| --- | --- |
| x\*+ | zéro ou plus x, possession (NON PRIS EN CHARGE) |
| x++ | un ou plus x, possession (NON PRIS EN CHARGE) |
| x?+ | zéro ou un x, possession (NON PRIS EN CHARGE) |
| x{n,m}+ | n ou ... ou m x, possession (NON PRIS EN CHARGE) |
| x{n,}+ | n ou plus x, possession (NON PRIS EN CHARGE) |
| x{n}+ | exactement n x, possession (NON PRIS EN CHARGE) |

| | Regroupement |
| --- | --- |
| (re) | Groupe de capture numéroté (sous-correspondance) |
| (?P&lt;nom&gt;re) | nommé &amp; groupe de capture numéroté (sous-correspondance) |
| (?&lt;nom&gt;re) | nommé &amp; groupe de capture numéroté (sous-correspondance) (NON PRIS EN CHARGE) |
| (?&#39;name&#39;re) | nommé &amp; groupe de capture numéroté (sous-correspondance) (NON PRIS EN CHARGE) |
| (?:re) | groupe non capturé |
| (?flags) | activer les indicateurs dans le groupe actuel; non capture |
| (?flags:re) | définir des indicateurs pendant un re; non capture |
| (?#text) | Commentaire (NON PRIS EN CHARGE) |
| (?\|x\|y\|z) | réinitialisation de la numérotation des branches (NON PRIS EN CHARGE) |
| (?&gt;re) | correspondance de possession de re (NON PRIS EN CHARGE) |
| re@&gt; | correspondance de possession de re (NON PRIS EN CHARGE) VIM |
| %(re) | groupe de non capture (NON PRIS EN CHARGE) VIM |

| | Flags |
| --- | --- |
| i | non respect de la casse (valeur par défaut faux) |
| m | mode multilignes: ^ et $ correspondent ligne début/fin en plus du texte début/fin (valeur par défaut faux) |
| s | let . correspondre à \n (valeur par défaut faux) |
| U | ingratitude : échange de sens de x\* et x\*?, x+ et x+?, etc (valeur par défaut faux) |

La syntaxe de l’indicateur est xyz (ensemble) ou -xyz (clear) ou xy-z (ensemble xy, clear z).

|  | Chaînes vides |
| --- | --- |
| ^ | au début d’un texte ou d’une ligne (m = vrai) |
| $ | à la fin du texte (comme \z non \z) ou ligne (m = vrai) |
| \A | au début du texte |
| \b | à la limite de mot ASCII (\w d’un côté et \W, \A ou \Z de l’autre) |
| \B | non au niveau de la limite de mot ASCII |
| \g | au début du sous-texte recherché (NON PRIS EN CHARGE) PCRE |
| \G | à la fin de la dernière correspondance (NON PRIS EN CHARGE) PERL |
| \Z | à la fin du texte ou avant le saut de ligne à la fin du texte (NON PRIS EN CHARGE) |
| \z | à la fin du texte |
| (?=re) | avant la correspondance de texte re (NON PRIS EN CHARGE) |
| (?!re) | avant le texte ne correspondant pas re (NON PRIS EN CHARGE) |
| (?&lt;=re) | après la correspondance de texte re (NON PRIS EN CHARGE) |
| (?&lt;!re) | après le texte ne correspondant pas re (NON PRIS EN CHARGE) |
| re&amp; | avant la correspondance de texte re (NON PRIS EN CHARGE) VIM |
| re@= | avant la correspondance de texte re (NON PRIS EN CHARGE) VIM |
| re@! | avant le texte ne correspondant pas re (NON PRIS EN CHARGE) VIM |
| re@&lt;= | après la correspondance de texte re (NON PRIS EN CHARGE) VIM |
| re@&lt;! | après le texte ne correspondant pas re (NON PRIS EN CHARGE) VIM |
| \zs | définit le début de la correspondance (= \K) (NON PRIS EN CHARGE) VIM |
| \ze | définit la fin de la correspondance (NON PRIS EN CHARGE) VIM |
| \%^ | le début d’un fichier (NON PRIS EN CHARGE) VIM |
| \%$ | la fin d’un fichier (NON PRIS EN CHARGE) VIM |
| \%V | à l’écran (NON PRIS EN CHARGE) VIM |
| \%# | position du curseur (NON PRIS EN CHARGE) VIM |
| \%&#39;m | position de la marque m (NON PRIS EN CHARGE) VIM |
| \%23l | à la ligne 23 (NON PRIS EN CHARGE) VIM |
| \%23c | dans la colonne 23 (NON PRIS EN CHARGE) VIM |
| \%23v | dans la colonne virtuelle 23 (NON PRIS EN CHARGE) VIM |

|  | Séquences d’échappement |
| --- | --- |
| \a | bell (≡ \007) |
| \f | flux de formulaire (≡ \014) |
| \t | onglet horizontale (≡ \011) |
| \n | nouvelle ligne (≡ \012) |
| \r | retour chariot (≡ \015) |
| \v | caractère d’onglet verticale (≡ \013) |
| \* | littéral \*, pour tout signe de ponctuation \* |
| \123 | code de caractère octal (quatre chiffres au maximum) |
| \x7F | code de caractère hex (exactement deux chiffres) |
| \x{10FFFF} | code de caractère hex |
| \C | correspondre un seul octet même en mode UTF-8 |
| \Q...\E | texte littéral ... même si ... avec ponctuation |
| \1 | rétro-référence (NON PRIS EN CHARGE) |
| \b | retour arrière (NON PRIS EN CHARGE) (utiliser \010) |
| \cK | caractère de contrôle ^ K (NON PRIS EN CHARGE) (utiliser \001 etc) |
| \e | échap (NON PRIS EN CHARGE) (utiliser \033) |
| \g1 | rétro-référence (NON PRIS EN CHARGE) |
| \g{1} | rétro-référence (NON PRIS EN CHARGE) |
| \g{+1} | rétro-référence (NON PRIS EN CHARGE) |
| \g{-1} | rétro-référence (NON PRIS EN CHARGE) |
| \g{name} | rétro-référence nommé (NON PRIS EN CHARGE) |
| \g&lt;name&gt; | appel de sous-routine (NON PRIS EN CHARGE) |
| \g&#39;name&#39; | appel de sous-routine (NON PRIS EN CHARGE) |
| \k&lt;name&gt; | rétro-référence nommé (NON PRIS EN CHARGE) |
| \k&#39;name&#39; | rétro-référence nommé (NON PRIS EN CHARGE) |
| \lX | X minuscule (NON PRIS EN CHARGE) |
| \ux | X majuscule (NON PRIS EN CHARGE) |
| \L...\E | texte en minuscules... (NON PRIS EN CHARGE) |
| \K | réinitialiser le début de $0 (NON PRIS EN CHARGE) |
| \N{name} | caractère Unicode nommé (NON PRIS EN CHARGE) |
| \R | saut de ligne (NON PRIS EN CHARGE) |
| \U...\E | texte en minuscules ... (NON PRIS EN CHARGE) |
| \X | séquence Unicode étendue (NON PRIS EN CHARGE) |
| \%d123 | caractère décimal 123 (NON PRIS EN CHARGE) VIM |
| \%xFF | caractère hexadécimale FF (NON PRIS EN CHARGE) VIM |
| \%o123 | caractère octal 123 (NON PRIS EN CHARGE) VIM |
| \%u1234 | caractère Unicode 0x1234 (NON PRIS EN CHARGE) VIM |
| \%U12345678 | caractère Unicode 0x12345678 (NON PRIS EN CHARGE) VIM |

|  | Éléments de classe de caractères |
| --- | --- |
| x | caractère unique |
| A-Z | plage de caractères (incluse) |
| \d | Classe de caractères perl |
| [:foo:] | Classe de caractères ASCII foo |
| \p{Foo} | Classe de caractères Unicode Foo |
| \pF | Classe de caractères Unicode F (nom à une lettre) |

|  | Classes de caractères nommés comme éléments de classe de caractères |
| --- | --- |
| [\d] | chiffres (≡ \d) |
| [^\d] | pas de chiffres (≡ \d) |
| [\D] | pas de chiffres (≡ \d) |
| [^\D] | non pas de chiffres (≡ \d) |
| [[:name:]] | classe ASCII nommée à l’intérieur d’une classe de caractères (≡ [:name:]) |
| [^ [: nom:]] | classe ASCII nommée à l’intérieur d’une classe de caractères inversée (≡ [:name:]) |
| [\p{Name}] | propriété Unicode nommée dans la classe de caractères (≡ \p{Name}) |
| [^\p{Name}] | propriété Unicode nommée dans la classe de caractères inversée (≡ \P{Name}) |

| <a name="user-content-perl"></a> | Classes de caractères perl (tout ASCII uniquement) |
| --- | --- |
| \d | chiffres (≡ [0-9]) |
| \D | pas de chiffres (≡ [^0-9]) |
| \s | espace blanc (≡ [\t\n\f\r]) |
| \S | pas d’espace blanc (≡ [\t\n\f\r]) |
| \w | caractères de mot (≡ [0-9A-Za-z\_]) |
| \W | pas de caractères de mot (≡ [^0-9A-Za-z\_]) |
| \h | espace horizontal (NON PRIS EN CHARGE) |
| \H | pas d’espace horizontal (NON PRIS EN CHARGE) |
| \v | espace vertical (NON PRIS EN CHARGE) |
| \V | pas d’espace vertical (NON PRIS EN CHARGE) |

|<a name="user-content-ascii"></a>  | classes de caractères ASCII |
| --- | --- |
| [[:alnum:]] | alphanumérique (≡ [0-9A-za-z]) |
| [[:alpha:]] | alphabétique (≡ [A-Za-z]) |
| [[:ascii:]] | ASCII (≡ [\x00-\x7F]) |
| [[:blank:]] | vide (≡ [\t]) |
| [[:cntrl:]] | control (≡ [\x00-\x1F\x7F]) |
| [[:digit:]] | chiffres (≡ [0-9]) |
| [[:graph:]] | graphique (≡ `[!-~]` ≡ `[A-Za-z0-9!&quot;#$%&amp;&#39;()\*+,\-./:;&lt;=&gt;?@[\\\]^_`\` `{\|}~]`) |
| [[:lower:]] | minuscule (≡ [a-z]) |
| [[:print:]] | imprimable (≡ [-~] ≡ [[:graph:]]) |
| [[:punct:]] | ponctuation (≡ [!-/:-@[-`{-~]) |
| [[:space:]] | espace blanc (≡ [\t\n\v\f\r]) |
| [[:upper:]] | majuscule (≡ [A-Z]) |
| [[:word:]] | caractères de mot (≡ [0-9A-Za-z\_]) |
| [[:xdigit:]] | chiffre hexadécimal (≡ [0-9A-Fa-f]) |

| | Noms de classe de caractères Unicode--catégorie général |
| --- | --- |
| C | Autre |
| Cc | control |
| Cf | Format |
| Cn | points de codes non assignés (NON PRIS EN CHARGE) |
| Co | usage privé |
| Cs | suppléant |
| L | lettre |
| LC | lettre en majuscules (NON PRIS EN CHARGE) |
| L&amp; | lettre en majuscules (NON PRIS EN CHARGE) |
| Ll | lettres minuscules |
| Lm | lettre modificative |
| Lo | autre lettre |
| Lt | lettre de titre |
| Lu | lettres majuscules |
| M | marque |
| Mc | marque d'espacement |
| Me | marque englobante |
| Mn | marque de non-espacement |
| N | nombre |
| Nd | nombre décimal |
| Nl | numéro de lettre |
| Non | autre nombre |
| P | ponctuation |
| Pc | ponctuation de connecteur |
| Pd | ponctuation de tirets |
| Pe | ponctuation rapprochée |
| Pf | ponctuation finale |
| Pi | ponctuation initiale |
| Po | autre ponctuation |
| Ps | ponctuation ouverte |
| S | symbol |
| Sc | symbole de devise |
| Sk | symbole modificateur |
| Sm | symbole mathématique |
| So | autre symbole |
| Z | séparateur |
| Zl | séparateur de ligne |
| Zp | séparateur de paragraphe |
| Zs | séparateur d’espace |

| Noms de classe de caractères Unicode--scripts |
| --- |
| Adlam |
| Ahom |
| Anatolian\_Hieroglyphs |
| Arabe |
| Arménien |
| Avestan |
| Balinais |
| Bamoum |
| Bassa\_Vah |
| Batik |
| Bengali |
| Bhaiksuki |
| Bopomofo |
| Brahma |
| Braille |
| Bugi |
| Bouhid |
| Canadian\_Aboriginal |
| Carien |
| Caucasian\_Albanian |
| Chakma |
| Cham |
| Cherokee |
| Chorasmian |
| Commun |
| Copte |
| Cunéiforme |
| Cypriot |
| Cyrillic |
| Déseret |
| Dévanâgarî |
| Dives\_Akuru |
| Dogra |
| Duployan |
| Égyptien\_Hiéroglyphes |
| Elbasan |
| Elymaic |
| Éthiopien |
| Géorgien |
| Glagolitique |
| Gothique |
| Grantha |
| Grec |
| Goudjarati |
| Gunjala\_Gondi |
| Gurmukhi |
| Han |
| Hangul |
| Hanifi\_Rohingya |
| Hanounóo |
| Hatran |
| Hébreu |
| Hiragana |
| Impérial\_Aramaic |
| Hérité |
| Inscriptional\_Pahlavi |
| Inscriptional\_Parthian |
| Javanais |
| Kaithi |
| Kannada |
| Katakana |
| Kayah\_Li |
| Kharoshthi |
| Khitan\_Small\_Script |
| Khmer |
| Khojki |
| Khudawadi |
| Lao |
| Latin |
| Lepcha |
| Limbu |
| Linear\_A |
| Linear\_B |
| Lisu |
| Lycien |
| Lydien |
| Mahajani |
| Makasar |
| Malayalam |
| Mandéen |
| Manichéen |
| Marchen |
| Masaram\_Gondi |
| Medefaidrin |
| Meetei\_Mayek |
| Mende\_Kikakui |
| Meroitic\_Cursive |
| Meroitic\_Hieroglyphs |
| Miao |
| Modi |
| Mongole |
| Mro |
| Multani |
| Myanmar |
| Nabataean |
| Nandinagari |
| New\_Tai\_Lue |
| Newa |
| Nko |
| Nushu |
| Nyiakeng\_Puachue\_Hmong |
| Ogham |
| Ol\_Chiki |
| Old\_Hungarian |
| Old\_Italic |
| Old\_North\_Arabian |
| Old\_Permic |
| Old\_Persian |
| Old\_Sogdian |
| Old\_South\_Arabian |
| Old\_Turkic |
| Oriya |
| Osage |
| Osmanya |
| Pahawh\_Hmong |
| Palmyrene |
| Pau\_Cin\_Hau |
| Phags\_Pa |
| Phénicien |
| Psalter\_Pahlavi |
| Redjang |
| Runic |
| Samaritain |
| Saurashatra |
| Sharada |
| Shavien |
| Siddham |
| SignÉcriture |
| Sinhala |
| Sogdian |
| Sora\_Sompeng |
| Soyombo |
| Sundanais |
| Syloti\_Nagri |
| Syriaque |
| Tagalog |
| Tagbanoua |
| Tai\_Le |
| Tai\_Tham |
| Tai\_Viet |
| Takri |
| Tamoul |
| Tangut |
| Telugu |
| Thaana |
| Thaï |
| Tibétain |
| Tifinagh |
| Tirhuta |
| Ugaritic |
| Vaï |
| Wancho |
| Warang\_Citi |
| Yezidi |
| Yi |
| Zanabazar\_Square |

|  | classes de caractères Vim |
| --- | --- |
| \i | caractère d’identificateur (NON PRIS EN CHARGE) VIM |
| \I | \i sauf chiffres (NON PRIS EN CHARGE) VIM |
| \k | caractère de mot clé (NON PRIS EN CHARGE) VIM |
| \K | \k sauf chiffres (NON PRIS EN CHARGE) VIM |
| \f | caractère de nom de fichier (NON PRIS EN CHARGE) VIM |
| \F | \f sauf chiffres (NON PRIS EN CHARGE) VIM |
| \p | caractère imprimable (NON PRIS EN CHARGE) VIM |
| \P | \p sauf chiffres (NON PRIS EN CHARGE) VIM |
| \s | caractère d’espacement (≡ [\t]) (NON PRIS EN CHARGE) VIM |
| \S | caractère d’espacenon blanc (≡ [^ \t]) (NON PRIS EN CHARGE) VIM |
| \d | chiffres (≡ [0-9]) VIM |
| \D | pas de \d VIM |
| \x | chiffres hexadécimaux (≡ [0-9A-FA-f]) (NON PRIS EN CHARGE) VIM |
| \X | pas de \x (NON PRIS EN CHARGE) VIM |
| \o | chiffre octal (≡ [0-7]) (NON PRIS EN CHARGE) VIM |
| \O | pas de \o (NON PRIS EN CHARGE) VIM |
| \w | caractère de mot VIM |
| \W | pas de \w VIM |
| \h | caractère de début de mot (NON PRIS EN CHARGE) VIM |
| \H | pas de \h (NON PRIS EN CHARGE) VIM |
| \a | alphabétique (NON PRIS EN CHARGE) VIM |
| \A | pas de \a (NON PRIS EN CHARGE) VIM |
| \l | minuscule (NON PRIS EN CHARGE) VIM |
| \L | pas de minuscule (NON PRIS EN CHARGE) VIM |
| \u | majuscule (NON PRIS EN CHARGE) VIM |
| \U | pas de majuscule (NON PRIS EN CHARGE) VIM |
| \_x | \x plus nouvelle ligne, pour n’importe quel x (NON PRIS EN CHARGE) VIM |
| \c | ignorer le cas (NON PRIS EN CHARGE) VIM |
| \C | cas de correspondance (NON PRIS EN CHARGE) VIM |
| \m | magic (NON PRIS EN CHARGE) VIM |
| \M | nomagic (NON PRIS EN CHARGE) VIM |
| \v | verymagic (NON PRIS EN CHARGE) VIM |
| \V | verynomagic (NON PRIS EN CHARGE) VIM |
| \Z | ignorer les différences entre les caractères de combinaison Unicode (NON PRIS EN CHARGE) VIM |

|  | Magic |
| --- | --- |
| (?{code}) | code perl arbitraire (NON PRIS EN CHARGE) PERL |
| (??{code}) | code perl arbitraire différé (NON PRIS EN CHARGE) PERL |
| (?n) | appel récurrent au groupe de capture regexp n (NON PRIS EN CHARGE) |
| (?+n) | appel récurrent au groupe relatif +n (NON PRIS EN CHARGE) |
| (?-n) | appel récurrent au groupe relatif -n (NON PRIS EN CHARGE) |
| (?C) | Appel du PCRE (NON PRIS EN CHARGE) PCRE |
| (?R) | appel récurrent à l’ensemble de regexp (≡ (?0)) (NON PRIS EN CHARGE) |
| (?&amp;name) | appel récurrent au groupe nommé (NON PRIS EN CHARGE) |
| (?P=name) | rétro-référence nommé (NON PRIS EN CHARGE) |
| (?P&gt;name) | appel récurrent au groupe nommé (NON PRIS EN CHARGE) |
| (?(cond)true|false) | branche conditionnelle (NON PRIS EN CHARGE) |
| (?(cond)true) | branche conditionnelle (NON PRIS EN CHARGE) |
| (\*ACCEPT) | rendre les regexps plus similaires au Prologue (NON PRIS EN CHARGE) |
| (\*COMMIT) | (NON PRIS EN CHARGE) |
| (\*F) | (NON PRIS EN CHARGE) |
| (\*FAIL) | (NON PRIS EN CHARGE) |
| (\ MARQUE) | (NON PRIS EN CHARGE) |
| (\*PRUNE) | (NON PRIS EN CHARGE) |
| (\*SKIP) | (NON PRIS EN CHARGE) |
| (\*THEN) | (NON PRIS EN CHARGE) |
| (\*ANY) | définition de la convention de nouvelle ligne (NON PRIS EN CHARGE) |
| (\*ANYCRLF) | (NON PRIS EN CHARGE) |
| (\*CR) | (NON PRIS EN CHARGE) |
| (\*CRLF) | (NON PRIS EN CHARGE) |
| (\*LF) | (NON PRIS EN CHARGE) |
| (\*BSR\_ANYCRLF) | définition de la convention (NON PRIS EN CHARGE) PCRE |
| (\*BSR\_UNICODE) | (NON PRIS EN CHARGE) PCRE |

## Licence de contenu

> [!NOTE]
> Certaines parties de cette page sont des modifications basées sur le travail créé et partagé par Chromium.org et utilisé conformément aux conditions décrites dans la [Licence internationale Creative Commons Attribution4.0](http://creativecommons.org/licenses/by/4.0/). La page d’origine est disponible [ici](https://github.com/google/re2/wiki/Syntax).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Ce travail est concédé sous une <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Licence internationale Creative Commons Attribution4.0</a>.

## Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)