---
title: ~, opérateur (référence C#)
ms.date: 11/05/2018
f1_keywords:
- ~_CSharpKeyword
helpviewer_keywords:
- tilde (~) one's complement operator [C#]
- ~ operator [C#]
- ~ [C#], bitwise complement operator
- bitwise complement operator [C#]
ms.assetid: 11bc078a-50e2-4d7e-9896-67ef669dc602
ms.openlocfilehash: 1bcb07c5639a098e3a8c566e92083ca0d48efb81
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53153213"
---
# <a name="-operator-c-reference"></a>~, opérateur (référence C#)

L’opérateur de complément au niveau du bit `~` est un opérateur unaire qui produit un complément au niveau du bit de son opérande en inversant chaque bit. Tous les types d’entiers acceptent l’opérateur `~`.

> [!NOTE]
> Le symbole `~` est également utilisé pour déclarer des finaliseurs. Pour plus d’informations, consultez [Finaliseurs](../../programming-guide/classes-and-structs/destructors.md).

L’exemple suivant illustre l’utilisation de l’opérateur `~` :

[!code-csharp-interactive[bitwise NOT](~/samples/snippets/csharp/language-reference/operators/BitwiseComplementExamples.cs#Example)]

> [!NOTE]
> L’exemple précédent utilise les littéraux binaires [introduits dans C# 7.0](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements) et [améliorés dans C# 7.2](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals).

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `~`.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, voir la section [Opérateur de complément au niveau du bit](~/_csharplang/spec/expressions.md#bitwise-complement-operator) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [Finaliseurs](../../programming-guide/classes-and-structs/destructors.md)
- [&, opérateur](and-operator.md)
- [|, opérateur](or-operator.md)
- [^, opérateur](xor-operator.md)
