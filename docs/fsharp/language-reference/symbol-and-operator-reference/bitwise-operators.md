---
title: Opérateurs au niveau du bit (F#)
description: 'Obtenir des informations sur les opérateurs de bits qui sont disponibles dans le langage de programmation F #.'
ms.date: 05/16/2016
ms.openlocfilehash: bc653ae7ff6dd6bc2c269aaba344f073df1fb708
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="bitwise-operators"></a>Opérateurs au niveau du bit

Cette rubrique décrit les opérateurs de bits qui sont disponibles dans le langage F #.

## <a name="summary-of-bitwise-operators"></a>Résumé des opérateurs de bits
Le tableau suivant décrit les opérateurs au niveau du bit qui sont pris en charge pour les types intégraux unboxed dans le langage F #.

|Opérateur|Notes|
|--------|-----|
|`&&&`|Opérateur de bits AND. Dans le résultat ont la valeur 1 si et seulement si les bits correspondants dans les deux opérandes source sont 1.|
|<code>&#124;&#124;&#124;</code>|Opérateur de bits OR. Dans le résultat ont la valeur 1 si des bits correspondants dans la source d’opérandes sont de 1.|
|`^^^`|Au niveau du bit opérateur OR exclusif. Dans le résultat ont la valeur 1 si et seulement si les bits dans les opérandes source ont des valeurs différentes.|
|`~~~`|Opérateur de négation au niveau du bit. Ceci est un opérateur unaire et produit un résultat dans lequel tous les bits 0 dans l’opérande source sont convertis en bits 1 et tous les bits 1 sont convertis en bits 0.|
|`<<<`|Au niveau du bit opérateur de décalage vers la gauche. Le résultat est le premier opérande avec bits décalée vers la gauche du nombre de bits dans le second opérande. Les bits décalés à la position la plus significative n’a pas lieu dans la position la moins significative. Les bits les moins significatifs sont complétées avec des zéros. Le type du deuxième argument est `int32`.|
|`>>>`|Au niveau du bit opérateur de décalage vers la droite. Le résultat est le premier opérande avec bits décalée vers la droite du nombre de bits dans le second opérande. Les bits décalés à la position la moins significative n’a pas lieu vers la position la plus significative. Pour les types non signés, les bits les plus significatifs sont remplis avec des zéros. Pour les types signés, les bits les plus significatifs sont complétées par d’autres. Le type du deuxième argument est `int32`.|

Les types suivants peuvent être utilisés avec des opérateurs au niveau du bit : `byte`, `sbyte`, `int16`, `uint16`, `int32 (int)`, `uint32`, `int64`, `uint64`, `nativeint`, et `unativeint`.

## <a name="see-also"></a>Voir aussi
[Informations de référence des symboles et opérateurs](index.md)

[Opérateurs arithmétiques](arithmetic-operators.md)

[Opérateurs booléens](boolean-operators.md)

