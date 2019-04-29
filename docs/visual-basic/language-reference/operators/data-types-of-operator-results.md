---
title: Types de données des résultats d'opérateur (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- data types [Visual Basic], operator result data types
- result data types [Visual Basic]
- operator result data types [Visual Basic]
- operators [Visual Basic], data types
- data types [Visual Basic], ranges
- operators [Visual Basic], result data types
ms.assetid: 9d524533-e1a1-4aa8-b1b8-622068173d06
ms.openlocfilehash: 45dcc80ee791da1c2731ba32f0ebd34564faf806
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61778558"
---
# <a name="data-types-of-operator-results-visual-basic"></a>Types de données des résultats d'opérateur (Visual Basic)
Visual Basic détermine le type de données de résultat d’une opération basée sur les types de données des opérandes. Dans certains cas, cela peut être un type de données avec une plage supérieure à celle de des opérandes.  
  
## <a name="data-type-ranges"></a>plages de types de données  
 Les plages des types de données pertinentes, dans l’ordre du plus petit au plus grand, sont les suivantes :  
  
- [Boolean](../../../visual-basic/language-reference/data-types/boolean-data-type.md) — deux valeurs possibles  
  
- [SByte](../../../visual-basic/language-reference/data-types/sbyte-data-type.md), [octets](../../../visual-basic/language-reference/data-types/byte-data-type.md) — 256 valeurs intégrales possibles  
  
- [Court](../../../visual-basic/language-reference/data-types/short-data-type.md), [UShort](../../../visual-basic/language-reference/data-types/ushort-data-type.md) : 65 536 (6.5... E + 4) des valeurs intégrales possibles  
  
- [Entier](../../../visual-basic/language-reference/data-types/integer-data-type.md), [UInteger](../../../visual-basic/language-reference/data-types/uinteger-data-type.md) : 4 294 967 296 (4.2... E + 9) des valeurs intégrales possibles  
  
- [Long](../../../visual-basic/language-reference/data-types/long-data-type.md), [ULong](../../../visual-basic/language-reference/data-types/ulong-data-type.md) — 18,446,744,073,709,551,615 (1.8... E + 19) des valeurs intégrales possibles  
  
- [Décimal](../../../visual-basic/language-reference/data-types/decimal-data-type.md) — 1.5... E + 29 possible de valeurs intégrales, nombre maximales de plage 7.9... E + 28 (valeur absolue)  
  
- [Seul](../../../visual-basic/language-reference/data-types/single-data-type.md) : plage maximale 3.4... E + 38 (valeur absolue)  
  
- [Double](../../../visual-basic/language-reference/data-types/double-data-type.md) : plage maximale 1.7... E + 308 (valeur absolue)  
  
 Pour plus d’informations sur les types de données Visual Basic, consultez [Types de données](../../../visual-basic/language-reference/data-types/index.md).  
  
 Si un opérande a la valeur [rien](../../../visual-basic/language-reference/nothing.md), les opérateurs arithmétiques Visual Basic peut le traiter en tant que zéro.  
  
## <a name="decimal-arithmetic"></a>Opération arithmétique décimale  
 Notez que le [décimal](../../../visual-basic/language-reference/data-types/decimal-data-type.md) type de données n’est ni à virgule flottante ni entier.  
  
 Si des opérandes d’un `+`, `–`, `*`, `/`, ou `Mod` opération est `Decimal` et l’autre n’est pas `Single` ou `Double`, Visual Basic étend l’autre opérande à `Decimal`. Il effectue l’opération dans `Decimal`, et le type de données de résultat est `Decimal`.  
  
## <a name="floating-point-arithmetic"></a>Arithmétique à virgule flottante  
 Visual Basic effectue la plupart des arithmétique à virgule flottante dans [Double](../../../visual-basic/language-reference/data-types/double-data-type.md), qui est les plus efficace des données de type pour ces opérations. Toutefois, si un opérande est [unique](../../../visual-basic/language-reference/data-types/single-data-type.md) et l’autre n’est pas `Double`, Visual Basic effectue l’opération dans `Single`. Il élargit chaque opérande correctement pour le type de données approprié avant l’opération, et le résultat est du même type de données.  
  
### <a name="-and--operators"></a>/ et ^ opérateurs  
 Le `/` opérateur est défini uniquement pour le [décimal](../../../visual-basic/language-reference/data-types/decimal-data-type.md), [unique](../../../visual-basic/language-reference/data-types/single-data-type.md), et [Double](../../../visual-basic/language-reference/data-types/double-data-type.md) types de données. Visual Basic élargit chaque opérande correctement pour le type de données approprié avant l’opération, et le résultat est du même type de données.  
  
 Le tableau suivant montre le résultat de types de données pour le `/` opérateur. Notez que cette table est symétrique ; pour une combinaison donnée de types de données d’opérande, le type de données de résultat est le même quel que soit l’ordre des opérandes.  
  
||||||  
|---|---|---|---|---|  
||`Decimal`|`Single`|`Double`|N’importe quel type entier|  
|`Decimal`|Decimal|Single|Double|Decimal|  
|`Single`|Single|Single|Double|Single|  
|`Double`|Double|Double|Double|Double|  
|N’importe quel type entier|Decimal|Single|Double|Double|  
  
 Le `^` opérateur est défini uniquement pour le `Double` type de données. Visual Basic élargit chaque opérande correctement à `Double` avant l’opération et le résultat de type de données est toujours `Double`.  
  
## <a name="integer-arithmetic"></a>Arithmétique sur les entiers  
 Le type de données de résultat d’une opération entière varie selon les types de données des opérandes. En général, Visual Basic utilise les stratégies suivantes pour déterminer le type de données de résultat :  
  
- Si les deux opérandes d’un opérateur binaire ont le même type de données, le résultat a ce type de données. Une exception est `Boolean`, qui est obligé de `Short`.  
  
- Si un opérande non signé fait partie avec un opérande signé, le résultat a un type signé au moins aussi grande une plage en tant que des opérandes.  
  
- Sinon, le résultat est généralement le plus grand de deux types de données d’opérande.  
  
 Notez que le type de données de résultat ne peut pas être identique à un type de données d’opérande.  
  
> [!NOTE]
>  Le type de données de résultat n’est pas toujours suffisamment grand pour contenir toutes les valeurs possibles résultant de l’opération. Un <xref:System.OverflowException> exception peut se produire si la valeur est trop grande pour le type de données de résultat.  
  
### <a name="unary--and--operators"></a>Unaires + et -les opérateurs  
 Le tableau suivant montre le résultat de types de données pour les deux opérateurs unaires, `+` et `–`.  
  
|||||||||||  
|---|---|---|---|---|---|---|---|---|---|  
||`Boolean`|`SByte`|`Byte`|`Short`|`UShort`|`Integer`|`UInteger`|`Long`|`ULong`|  
|Unaire `+`|Courte|SByte|Byte|Courte|UShort|Entier|UInteger|Longue|ULong|  
|Unaire `–`|Courte|SByte|Courte|Courte|Entier|Entier|Longue|Longue|Decimal|  
  
### <a name="-and--operators"></a><\< et >> opérateurs  
 Le tableau suivant montre le résultat de types de données pour les deux opérateurs de décalage de bits, `<<` et `>>`. Visual Basic traite chaque opérateur de décalage de bits comme un opérateur unaire sur son opérande gauche (modèle binaire à décaler).  
  
|||||||||||  
|---|---|---|---|---|---|---|---|---|---|  
||`Boolean`|`SByte`|`Byte`|`Short`|`UShort`|`Integer`|`UInteger`|`Long`|`ULong`|  
|`<<`, `>>`|Courte|SByte|Byte|Courte|UShort|Entier|UInteger|Longue|ULong|  
  
 Si l’opérande gauche est `Decimal`, `Single`, `Double`, ou `String`, Visual Basic essaie de convertir en `Long` avant l’opération et le résultat est de type de données `Long`. L’opérande droit (le nombre de positions de bits à décaler) doit être `Integer` ou un type qui s’étend à `Integer`.  
  
### <a name="binary----and-mod-operators"></a>Binaire +, -, * et les opérateurs Mod  
 Le tableau suivant présente le résultat des types de données pour le fichier binaire `+` et `–` opérateurs et le `*` et `Mod` opérateurs. Notez que cette table est symétrique ; pour une combinaison donnée de types de données d’opérande, le type de données de résultat est le même quel que soit l’ordre des opérandes.  
  
|||||||||||  
|---|---|---|---|---|---|---|---|---|---|  
||`Boolean`|`SByte`|`Byte`|`Short`|`UShort`|`Integer`|`UInteger`|`Long`|`ULong`|  
|`Boolean`|Courte|SByte|Courte|Courte|Entier|Entier|Longue|Longue|Decimal|  
|`SByte`|SByte|SByte|Courte|Courte|Entier|Entier|Longue|Longue|Decimal|  
|`Byte`|Courte|Courte|Byte|Courte|UShort|Entier|UInteger|Longue|ULong|  
|`Short`|Courte|Courte|Courte|Courte|Entier|Entier|Longue|Longue|Decimal|  
|`UShort`|Entier|Entier|UShort|Entier|UShort|Entier|UInteger|Longue|ULong|  
|`Integer`|Entier|Entier|Entier|Entier|Entier|Entier|Longue|Longue|Decimal|  
|`UInteger`|Longue|Longue|UInteger|Longue|UInteger|Longue|UInteger|Longue|ULong|  
|`Long`|Longue|Longue|Longue|Longue|Longue|Longue|Longue|Longue|Decimal|  
|`ULong`|Decimal|Decimal|ULong|Decimal|ULong|Decimal|ULong|Decimal|ULong|  
  
### <a name="-operator"></a>\, opérateur  
 Le tableau suivant montre le résultat de types de données pour le `\` opérateur. Notez que cette table est symétrique ; pour une combinaison donnée de types de données d’opérande, le type de données de résultat est le même quel que soit l’ordre des opérandes.  
  
|||||||||||  
|---|---|---|---|---|---|---|---|---|---|  
||`Boolean`|`SByte`|`Byte`|`Short`|`UShort`|`Integer`|`UInteger`|`Long`|`ULong`|  
|`Boolean`|Courte|SByte|Courte|Courte|Entier|Entier|Longue|Longue|Longue|  
|`SByte`|SByte|SByte|Courte|Courte|Entier|Entier|Longue|Longue|Longue|  
|`Byte`|Courte|Courte|Byte|Courte|UShort|Entier|UInteger|Longue|ULong|  
|`Short`|Courte|Courte|Courte|Courte|Entier|Entier|Longue|Longue|Longue|  
|`UShort`|Entier|Entier|UShort|Entier|UShort|Entier|UInteger|Longue|ULong|  
|`Integer`|Entier|Entier|Entier|Entier|Entier|Entier|Longue|Longue|Longue|  
|`UInteger`|Longue|Longue|UInteger|Longue|UInteger|Longue|UInteger|Longue|ULong|  
|`Long`|Longue|Longue|Longue|Longue|Longue|Longue|Longue|Longue|Longue|  
|`ULong`|Longue|Longue|ULong|Longue|ULong|Longue|ULong|Longue|ULong|  
  
 Si des opérandes de le `\` opérateur est [décimal](../../../visual-basic/language-reference/data-types/decimal-data-type.md), [unique](../../../visual-basic/language-reference/data-types/single-data-type.md), ou [Double](../../../visual-basic/language-reference/data-types/double-data-type.md), Visual Basic essaie de convertir en [Long](../../../visual-basic/language-reference/data-types/long-data-type.md)avant l’opération et le résultat est de type de données `Long`.  
  
## <a name="relational-and-bitwise-comparisons"></a>Comparaisons relationnelles et au niveau du bit  
 Le type de données de résultat d’une opération relationnelle (`=`, `<>`, `<`, `>`, `<=`, `>=`) est toujours `Boolean` [Type de données booléen](../../../visual-basic/language-reference/data-types/boolean-data-type.md). Vaut également pour les opérations logiques (`And`, `AndAlso`, `Not`, `Or`, `OrElse`, `Xor`) sur `Boolean` opérandes.  
  
 Le type de données de résultat d’une opération logique au niveau du bit dépend des types de données des opérandes. Notez que `AndAlso` et `OrElse` sont définies uniquement pour `Boolean`, et Visual Basic convertit chaque opérande si nécessaire en `Boolean` avant d’effectuer l’opération.  
  
### <a name="-----and--operators"></a>=, <>, \<, >, \<=, et > = opérateurs  
 Si les deux opérandes sont `Boolean`, Visual Basic considère `True` soit inférieure à `False`. Si un type numérique est comparé à un `String`, Visual Basic tente de convertir le `String` à `Double` avant l’opération. Un `Char` ou `Date` opérande peut être comparé uniquement avec un autre opérande du même type de données. Le type de données de résultat est toujours `Boolean`.  
  
### <a name="bitwise-not-operator"></a>Au niveau du bit pas d’opérateur  
 Le tableau suivant montre le résultat de types de données pour l’opérateur de bits `Not` opérateur.  
  
|||||||||||  
|---|---|---|---|---|---|---|---|---|---|  
||`Boolean`|`SByte`|`Byte`|`Short`|`UShort`|`Integer`|`UInteger`|`Long`|`ULong`|  
|`Not`|Booléen|SByte|Byte|Courte|UShort|Entier|UInteger|Longue|ULong|  
  
 Si l’opérande est `Decimal`, `Single`, `Double`, ou `String`, Visual Basic essaie de convertir en `Long` avant l’opération et le résultat est de type de données `Long`.  
  
### <a name="bitwise-and-or-and-xor-operators"></a>Au niveau du bit et, ou et les opérateurs de bits Xor  
 Le tableau suivant montre le résultat de types de données pour l’opérateur de bits `And`, `Or`, et `Xor` opérateurs. Notez que cette table est symétrique ; pour une combinaison donnée de types de données d’opérande, le type de données de résultat est le même quel que soit l’ordre des opérandes.  
  
|||||||||||  
|---|---|---|---|---|---|---|---|---|---|  
||`Boolean`|`SByte`|`Byte`|`Short`|`UShort`|`Integer`|`UInteger`|`Long`|`ULong`|  
|`Boolean`|Booléen|SByte|Courte|Courte|Entier|Entier|Longue|Longue|Longue|  
|`SByte`|SByte|SByte|Courte|Courte|Entier|Entier|Longue|Longue|Longue|  
|`Byte`|Courte|Courte|Byte|Courte|UShort|Entier|UInteger|Longue|ULong|  
|`Short`|Courte|Courte|Courte|Courte|Entier|Entier|Longue|Longue|Longue|  
|`UShort`|Entier|Entier|UShort|Entier|UShort|Entier|UInteger|Longue|ULong|  
|`Integer`|Entier|Entier|Entier|Entier|Entier|Entier|Longue|Longue|Longue|  
|`UInteger`|Longue|Longue|UInteger|Longue|UInteger|Longue|UInteger|Longue|ULong|  
|`Long`|Longue|Longue|Longue|Longue|Longue|Longue|Longue|Longue|Longue|  
|`ULong`|Longue|Longue|ULong|Longue|ULong|Longue|ULong|Longue|ULong|  
  
 Si un opérande est `Decimal`, `Single`, `Double`, ou `String`, Visual Basic essaie de convertir en `Long` avant l’opération et les données de résultat type est le même que si cet opérande a déjà été `Long`.  
  
## <a name="miscellaneous-operators"></a>Opérateurs divers  
 Le `&` opérateur est défini uniquement pour la concaténation de `String` opérandes. Visual Basic convertit chaque opérande si nécessaire en `String` avant l’opération et le résultat de type de données est toujours `String`. Dans le cadre de la `&` opérateur, toutes les conversions en `String` sont considérées comme des étendues, même si `Option Strict` est `On`.  
  
 Le `Is` et `IsNot` opérateurs requièrent les deux opérandes soient de type référence. Le `TypeOf`... `Is` expression requiert que le premier opérande soit d’un type référence et le second opérande par le nom d’un type de données. Dans tous les cas les données de résultat est type `Boolean`.  
  
 Le `Like` opérateur est défini uniquement pour les critères spéciaux de `String` opérandes. Visual Basic essaie de convertir chaque opérande si nécessaire en `String` avant l’opération. Le type de données de résultat est toujours `Boolean`.  
  
## <a name="see-also"></a>Voir aussi

- [Types de données](../../../visual-basic/language-reference/data-types/index.md)
- [Opérateurs et expressions](../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)
- [Opérateurs arithmétiques en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
- [Opérateurs de comparaison en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)
- [Opérateurs](../../../visual-basic/language-reference/operators/index.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Opérateurs arithmétiques](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [Opérateurs de comparaison](../../../visual-basic/language-reference/operators/comparison-operators.md)
- [Option Strict (instruction)](../../../visual-basic/language-reference/statements/option-strict-statement.md)
