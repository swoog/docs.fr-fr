---
title: '%, opérateur (référence C#)'
ms.date: 09/04/2018
f1_keywords:
- '%_CSharpKeyword'
helpviewer_keywords:
- remainder operator [C#]
- '% operator [C#]'
ms.assetid: 3b74f4f9-fd9c-45e7-84fa-c8d71a0dfad7
ms.openlocfilehash: cd6d49b69d40f3b45aae060d46b58632dc8448f8
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50041256"
---
# <a name="-operator-c-reference"></a>%, opérateur (référence C#)

L’opérateur de reste `%` calcule le reste après avoir divisé son premier opérande par son second opérande.

Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `%`. Quand `%` est surchargé, l’[opérateur d’assignation de reste](remainder-assignment-operator.md) `%=` est également surchargé implicitement.

Tous les types numériques prennent en charge l’opérateur de reste.

## <a name="integer-remainder"></a>Reste entier
  
Pour les opérandes entiers, le résultat de `a % b` est la valeur produite par `a - (a / b) * b`. Le signe du reste non nul est le même que celui du premier opérande, comme le montre l’exemple suivant :

[!code-csharp-interactive[integer remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#1)]

## <a name="floating-point-remainder"></a>Reste à virgule flottante

En ce qui concerne les opérandes [float](../keywords/float.md) et [double](../keywords/double.md), le résultat de `x % y` pour le `x` et le `y` finis est la valeur `z` afin que

- Le signe de `z`, s’il est différent de zéro, soit identique au signe de `x`
- La valeur absolue de `z` soit la valeur produite par `|x| - n * |y|`, où `n` représente le plus grand entier possible inférieur ou égal à `|x| / |y|`, et où `|x|` et `|y|` sont les valeurs absolues de `x` et `y`, respectivement

Pour plus d’informations sur le comportement de l’opérateur `%` avec des opérandes non finis, consultez la section [Opérateur de reste](~/_csharplang/spec/expressions.md#remainder-operator) dans la [Spécification du langage C#](../language-specification/index.md).

> [!NOTE]
> Cette méthode de calcul du reste est analogue à celle utilisée pour les opérandes entiers. Toutefois, elle ne suit pas la norme IEEE 754. Si l’opération de reste doit être conforme à la norme IEEE 754, utilisez la méthode <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType>.

L’exemple suivant illustre le comportement de l’opérateur de reste pour les opérandes `float` et `double` :

[!code-csharp-interactive[float and double remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#2)]

Notez les erreurs d’arrondi qui peuvent être associées aux types à virgule flottante.

Pour les opérandes [decimal](../keywords/decimal.md), l’opérateur de reste `%` équivaut à l’[opérateur de reste](<xref:System.Decimal.op_Modulus(System.Decimal,System.Decimal)>) de type <xref:System.Decimal?displayProperty=nameWithType>.

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType>
- <xref:System.Math.DivRem%2A?displayProperty=nameWithType>
