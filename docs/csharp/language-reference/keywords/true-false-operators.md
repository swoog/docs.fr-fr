---
title: Opérateurs true et false - Référence C#
ms.custom: seodec18
ms.date: 12/10/2018
helpviewer_keywords:
- false operator [C#]
- true operator [C#]
ms.assetid: 81a888fd-011e-4589-b242-6c261fea505e
ms.openlocfilehash: 869eeab6515340b2f1884ab7206979e83654a10b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59328242"
---
# <a name="true-and-false-operators-c-reference"></a>Opérateurs true et false (Référence C#)

L’opérateur `true` retourne la valeur [bool](bool.md) `true` pour indiquer qu’un opérande est true. L’opérateur `false` retourne la valeur `bool` `true` pour indiquer qu’un opérande est false. Les opérateurs `true` et `false` ne sont pas forcément complémentaires. Autrement dit, les opérateurs `true` et `false` peuvent retourner la valeur `bool` `false` pour le même opérande. Si un type définit un des deux opérateurs, il doit aussi définir un autre opérateur.

Si un type avec les opérateurs `true` et `false` définis [surcharge](operator.md) [l’opérateur OR logique](../operators/boolean-logical-operators.md#logical-or-operator-) `|` ou [l’opérateur AND logique](../operators/boolean-logical-operators.md#logical-and-operator-) `&` d’une façon, [l’opérateur OR logique conditionnel](../operators/boolean-logical-operators.md#conditional-logical-or-operator-) `||` ou [l’opérateur AND logique conditionnel](../operators/boolean-logical-operators.md#conditional-logical-and-operator-) `&&`, respectivement, peut être évalué pour les opérandes de ce type. Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels définis par l’utilisateur](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) de la [spécification du langage C#](../language-specification/index.md).

Un type avec l’opérateur `true` défini peut être le type de résultat d’une expression conditionnelle de contrôle dans les instructions [if](if-else.md), [do](do.md), [while](while.md) et [for](for.md) et dans [l’opérateur conditionnel `?:`](../operators/conditional-operator.md). Pour plus d’informations, voir la section [Expressions booléennes](~/_csharplang/spec/expressions.md#boolean-expressions) de la [spécification du langage C#](../language-specification/index.md).

> [!TIP]
> Utilisez le type `bool?` si vous voulez suivre une logique à trois valeurs, par exemple pour travailler avec des bases de données qui acceptent un type booléen à trois valeurs. C# fournit les opérateurs `&` et `|` qui prennent en charge la logique à trois valeurs avec les opérandes `bool?`. Pour plus d’informations, voir la section [Opérateurs logiques booléens Nullable](../operators/boolean-logical-operators.md#nullable-boolean-logical-operators) de l’article [Opérateurs logiques booléens](../operators/boolean-logical-operators.md).

L’exemple suivant présente le type qui définit les opérateurs `true` et `false`. Par ailleurs, il surcharge l’opérateur AND logique `&` de sorte que l’opérateur `&&` peut aussi être évalué pour les opérandes de ce type.

[!code-csharp-interactive[true and false operators example](~/samples/snippets/csharp/keywords/TrueFalseOperatorsExample.cs)]

Remarquez le comportement de court-circuit de l’opérateur `&&`. Lorsque la méthode `GetFuelLaunchStatus` retourne `LaunchStatus.Red`, le second opérande de l’opérateur `&&` n’est pas évalué. En effet, `LaunchStatus.Red` est false. Le résultat du AND logique ne dépend donc pas la valeur du second opérande. Voici la sortie de l’exemple :

```console
Getting fuel launch status...
Wait!
```

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Mots clés C#](index.md)
- [Opérateurs C#](../operators/index.md)
- [`true`, littéral](true-literal.md)
- [`false`, littéral](false-literal.md)