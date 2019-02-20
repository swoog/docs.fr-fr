---
title: '>> opérateur - Référence C#'
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- '>>_CSharpKeyword'
helpviewer_keywords:
- '>> operator [C#]'
- right shift operator (>>) [C#]
ms.assetid: a07f8679-d318-4ef8-b38b-65903efb8056
ms.openlocfilehash: 809cd2cab29d3378892ea224cf846e9d0909b073
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219722"
---
# <a name="-operator-c-reference"></a>>>, opérateur (référence C#)

L’opérateur de décalage vers la droite `>>` décale son premier opérande vers la droite du nombre de bits défini par son deuxième opérande. Tous les types d’entiers acceptent l’opérateur `>>`. Cependant, le deuxième opérande doit être de type [int](../keywords/int.md) ou d’un type pour lequel une [conversion numérique implicite](../keywords/implicit-numeric-conversions-table.md) vers `int` est prédéfinie.

L’opération de décalage vers la droite ignore les bits d’ordre inférieur. Les positions de bits vides d’ordre supérieur sont définies en fonction du type du premier opérande comme suit :

- si le premier opérande est de type [int](../keywords/int.md) ou [long](../keywords/long.md), l’opérateur de décalage vers la droite effectue un décalage **arithmétique** : la valeur du bit le plus significatif (le bit de signe) du premier opérande est propagée vers les positions des bits vides d’ordre supérieur. Autrement dit, les positions de bits vides d’ordre supérieur sont définies sur zéro si le premier opérande n’est pas négatif et sur un s’il est négatif.

- Si le premier opérande est de type [uint](../keywords/uint.md) ou [ulong](../keywords/ulong.md), l’opérateur de décalage vers la droite effectue un décalage **logique** : les positions des bits vides d’ordre supérieur sont toujours définies sur zéro.

L’exemple suivant illustre ce comportement :

[!code-csharp-interactive[right shift example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShift)]

## <a name="shift-count"></a>Valeur du décalage

Pour l’expression `x >> count`, la valeur réelle du décalage varie selon le type de `x` comme suit :

- si le type `x` est [int ](../keywords/int.md) ou [uint](../keywords/uint.md), la valeur du décalage est donnée par les *cinq* bits d’ordre inférieur du deuxième opérande. La valeur de décalage est donc calculée à partir de `count & 0x1F` (ou de `count & 0b_1_1111`).

- Si le type `x` est [long ](../keywords/long.md) ou [ulong](../keywords/ulong.md), la valeur du décalage est donnée par les *six* bits d’ordre inférieur du deuxième opérande. La valeur de décalage est donc calculée à partir de `count & 0x3F` (ou de `count & 0b_11_1111`).

L’exemple suivant illustre ce comportement :

[!code-csharp-interactive[shift count example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShiftByLargeCount)]

## <a name="remarks"></a>Remarques

Les opérations de décalage ne provoquent jamais de dépassements de capacité et donnent les mêmes résultats dans des contextes [checked and unchecked](../keywords/checked-and-unchecked.md).

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `>>`. Si un type `T` défini par l’utilisateur surcharge l’opérateur `>>`, le premier opérande doit être de type `T` et le deuxième de type `int`. Quand l’opérateur `>>` est surchargé, [l’opérateur d’assignation de décalage vers la droite](right-shift-assignment-operator.md) `>>=` est aussi implicitement surchargé.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, voir la section [Opérateurs de décalage](~/_csharplang/spec/expressions.md#shift-operators) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [<< opérateur](left-shift-operator.md)