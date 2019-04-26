---
title: '&amp;, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 10/29/2018
f1_keywords:
- '&_CSharpKeyword'
helpviewer_keywords:
- bitwise AND operator [C#]
- ampersand operator (&) [C#]
- '& operator [C#]'
- AND operator (&) [C#]
ms.assetid: afa346d5-90ec-4b1f-a2c8-3881f018741d
ms.openlocfilehash: 67d60709e1c6c76071ecfb7aac74c83dec6f372a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59310042"
---
# <a name="amp-operator-c-reference"></a>&amp;, opérateur (référence C#)

L’opérateur `&` est pris en charge sous deux formes : un opérateur address-of unaire ou un opérateur logique binaire.

## <a name="unary-address-of-operator"></a>address-of, opérateur unaire

L’opérateur unaire `&` retourne l’adresse de son opérande. Pour plus d’informations, consultez [Guide pratique pour obtenir l’adresse d’une variable](../../programming-guide/unsafe-code-pointers/how-to-obtain-the-address-of-a-variable.md)

L’opérateur address-of `&` nécessite un contexte [unsafe](../keywords/unsafe.md).

## <a name="integer-logical-bitwise-and-operator"></a>Opérateur logique AND au niveau du bit pour les types entier

Pour les types entier, l’opérateur `&` calcule l’opération logique AND au niveau du bit de ses opérandes :

[!code-csharp-interactive[integer logical bitwise AND](~/samples/snippets/csharp/language-reference/operators/AndOperatorExamples.cs#IntegerOperands)]

> [!NOTE]
> L’exemple précédent utilise les littéraux binaires [introduits dans C# 7.0](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements) et [améliorés dans C# 7.2](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals).

Étant donné que les opérations sur les types entier sont généralement autorisées sur les types énumération, l’opérateur `&` prend également en charge les opérandes [enum](../keywords/enum.md).

## <a name="boolean-logical-and-operator"></a>Opérateur logique booléen AND

Pour les opérandes [bool](../keywords/bool.md), l’opérateur `&` calcule l’opération logique AND de ses opérandes. Le résultat de `x & y` est `true` si `x` et `y` sont `true`. Sinon, le résultat est `false`.

L’opérateur `&` évalue les deux opérandes, même si le premier opérande prend la valeur `false`. Le résultat est donc `false` quelle que soit la valeur du deuxième opérande. L’exemple suivant illustre ce comportement :

[!code-csharp-interactive[bool logical AND](~/samples/snippets/csharp/language-reference/operators/AndOperatorExamples.cs#BooleanOperands)]

[L’opérateur conditionnel AND](boolean-logical-operators.md#conditional-logical-and-operator-) `&&` calcule également l’opération logique AND de ses opérandes, mais n’évalue pas le deuxième opérande si le premier donne `false`.

Pour les opérandes bool nullables, le comportement de l’opérateur `&` est cohérent avec la logique ternaire de SQL. Pour plus d’informations, voir la section [Opérateurs logiques booléens Nullable](boolean-logical-operators.md#nullable-boolean-logical-operators) de l’article [Opérateurs logiques booléens](boolean-logical-operators.md).

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur binaire `&`. Quand un opérateur binaire `&` est surchargé, [l’opérateur d’assignation AND](and-assignment-operator.md) `&=` est aussi implicitement surchargé.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez les sections [Opérateur address-of](~/_csharplang/spec/unsafe-code.md#the-address-of-operator) et [Opérateurs logiques](~/_csharplang/spec/expressions.md#logical-operators) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [Opérateurs logiques booléens](boolean-logical-operators.md)
- [Types de pointeur](../../programming-guide/unsafe-code-pointers/pointer-types.md)
- [|, opérateur](or-operator.md)
- [^, opérateur](xor-operator.md)
- [~, opérateur](bitwise-complement-operator.md)
