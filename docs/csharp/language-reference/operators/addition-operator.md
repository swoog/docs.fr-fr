---
title: + Opérateur - Référence C#
ms.custom: seodec18
ms.date: 10/22/2018
f1_keywords:
- +_CSharpKeyword
helpviewer_keywords:
- + operator [C#]
- concatenation operator [C#]
- addition operator [C#]
ms.assetid: 93e56486-bb42-43c1-bd43-60af11e64e67
ms.openlocfilehash: 92e20dad8ae6358f71137e955bb80e3641a66a54
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237751"
---
# <a name="-operator-c-reference"></a>+, opérateur (référence C#)

L’opérateur `+` est pris en charge sous deux formes : un opérateur plus unaire plus ou un opérateur d’addition binaire.

## <a name="unary-plus-operator"></a>Opérateur plus unaire

L’opérateur unaire `+` retourne la valeur de son opérande. Il est pris en charge par tous les types numériques.

## <a name="numeric-addition"></a>Addition numérique

Pour les types numériques, l’opérateur `+` calcule la somme de ses opérandes :

[!code-csharp-interactive[numeric addition](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddNumerics)]

## <a name="string-concatenation"></a>Concaténation de chaînes

Quand les deux opérandes ou l’un d’entre eux sont de [type chaîne](../keywords/string.md), l’opérateur `+` concatène les représentations sous forme de chaîne de ses opérandes :

[!code-csharp-interactive[string concatenation](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddStrings)]

À partir de C# 6, l’[interpolation de chaîne](../tokens/interpolated.md) fournit un moyen plus pratique de mettre en format les chaînes :

[!code-csharp-interactive[string interpolation](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#UseStringInterpolation)]

## <a name="delegate-combination"></a>Combinaison de délégués

Pour les types [délégué](../keywords/delegate.md), l’opérateur `+` retourne une nouvelle instance de délégué qui, lorsqu’elle est appelée, appelle le premier opérande puis appelle le second opérande. Si un des opérandes est `null`, l’opérateur `+` retourne la valeur de l’autre opérande (qui peut également être `null`). L’exemple suivant montre comment les délégués peuvent être combinés avec l’opérateur `+` :

[!code-csharp-interactive[delegate combination](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddDelegates)]

Pour plus d'informations sur les types de délégués, consultez [Délégués](../../programming-guide/delegates/index.md).

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) les opérateurs unaires et binaires `+`. Quand un opérateur binaire `+` est surchargé, l’[opérateur d’assignation d’addition](addition-assignment-operator.md) `+=` est aussi implicitement surchargé.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez les sections [Opérateur unaire plus](~/_csharplang/spec/expressions.md#unary-plus-operator) et [Opérateur d’addition](~/_csharplang/spec/expressions.md#addition-operator) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [Interpolation de chaîne](../tokens/interpolated.md)
- [Guide pratique pour concaténer plusieurs chaînes](../../how-to/concatenate-multiple-strings.md)
- [Délégués](../../programming-guide/delegates/index.md)
- [Checked et unchecked](../keywords/checked-and-unchecked.md)
