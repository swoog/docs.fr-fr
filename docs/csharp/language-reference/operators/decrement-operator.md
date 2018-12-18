---
title: --, opérateur - Référence C#
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- --_CSharpKeyword
helpviewer_keywords:
- -- operator [C#]
- decrement operator (--) [C#]
ms.assetid: 6b9cfe86-63c7-421f-9379-c9690fea8720
ms.openlocfilehash: 4fba014e8dabc13cd874e17f23515dc29d93f24b
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236919"
---
# <a name="---operator-c-reference"></a>--, opérateur (référence C#)

L’opérateur de décrémentation unaire `--` décrémente son opérande de 1. Il est pris en charge sous deux formes : l’opérateur de décrémentation suffixé, `x--`, et l’opérateur de décrémentation préfixé, `--x`.

## <a name="postfix-decrement-operator"></a>Opérateur de décrémentation suffixé

Le résultat de `x--` est la valeur de `x` *avant* l’opération, comme le montre l’exemple suivant :

[!code-csharp-interactive[postfix decrement](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PostfixDecrement)]

## <a name="prefix-decrement-operator"></a>Opérateur de décrémentation préfixé

Le résultat de `--x` est la valeur de `x` *après* l’opération, comme le montre l’exemple suivant :

[!code-csharp-interactive[prefix decrement](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PrefixDecrement)]

## <a name="remarks"></a>Notes

L’opérateur de décrémentation est prédéfini pour toutes les [types intégraux](../keywords/integral-types-table.md) (y compris le type [char](../keywords/char.md)), les [types à virgule flottante](../keywords/floating-point-types-table.md) et n’importe quel type [enum](../keywords/enum.md).

Un opérande de l’opérateur de décrémentation doit être une variable, un accès [propriété](../../programming-guide/classes-and-structs/properties.md) ou un accès [indexeur](../../../csharp/programming-guide/indexers/index.md).

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `--`.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, voir les sections [Opérateurs d’incrémentation et de décrémentation](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators) et [Opérateurs d’incrémentation et de décrémentation préfixés](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [++, opérateur](increment-operator.md)
- [Guide pratique : Incrémenter et décrémenter des pointeurs](../../programming-guide/unsafe-code-pointers/how-to-increment-and-decrement-pointers.md)
