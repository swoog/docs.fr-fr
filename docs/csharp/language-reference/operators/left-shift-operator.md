---
title: <<, opérateur - Référence C#
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- <<_CSharpKeyword
helpviewer_keywords:
- left shift operator (<<) [C#]
- << operator [C#]
ms.assetid: a654eb56-1ff7-4bf3-9064-b631be0cdccc
ms.openlocfilehash: deea2d0f720ba7f096e65c67378586bc88f24673
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219435"
---
# <a name="-operator-c-reference"></a>\<\<, opérateur (référence C#)

L’opérateur de décalage vers la gauche `<<` décale son premier opérande vers la gauche du nombre de bits défini par son deuxième opérande. Tous les types d’entiers acceptent l’opérateur `<<`. Cependant, le deuxième opérande doit être de type [int](../keywords/int.md) ou d’un type pour lequel une [conversion numérique implicite](../keywords/implicit-numeric-conversions-table.md) vers `int` est prédéfinie.

Les bits d’ordre supérieur qui sont en dehors de la plage du type de résultat sont ignorés, et les positions de bits vides d’ordre inférieur sont définies sur zéro, comme le montre l’exemple suivant :

[!code-csharp-interactive[left shift example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#LeftShift)]

## <a name="shift-count"></a>Valeur du décalage

Pour l’expression `x << count`, la valeur réelle du décalage varie selon le type de `x` comme suit :

- si le type `x` est [int ](../keywords/int.md) ou [uint](../keywords/uint.md), la valeur du décalage est donnée par les *cinq* bits d’ordre inférieur du deuxième opérande. La valeur de décalage est donc calculée à partir de `count & 0x1F` (ou de `count & 0b_1_1111`).

- si le type `x` est [long ](../keywords/long.md) ou [ulong](../keywords/ulong.md), la valeur du décalage est donnée par les *six* bits d’ordre inférieur du deuxième opérande. La valeur de décalage est donc calculée à partir de `count & 0x3F` (ou de `count & 0b_11_1111`).

L’exemple suivant illustre ce comportement :

[!code-csharp-interactive[shift count example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#LeftShiftByLargeCount)]

## <a name="remarks"></a>Remarques

Les opérations de décalage ne provoquent jamais de dépassements de capacité et donnent les mêmes résultats dans des contextes [checked and unchecked](../keywords/checked-and-unchecked.md).

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `<<`. Si un type `T` défini par l’utilisateur surcharge l’opérateur `<<`, le premier opérande doit être de type `T` et le deuxième de type `int`. Quand l’opérateur `<<` est surchargé, [l’opérateur d’assignation de décalage vers la gauche](left-shift-assignment-operator.md) `<<=` est aussi implicitement surchargé.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, voir la section [Opérateurs de décalage](~/_csharplang/spec/expressions.md#shift-operators) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [>> opérateur](right-shift-operator.md)
