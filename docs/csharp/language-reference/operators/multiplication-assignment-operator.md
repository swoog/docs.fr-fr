---
title: '*=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 02/26/2019
f1_keywords:
- '*=_CSharpKeyword'
helpviewer_keywords:
- '*= operator [C#]'
- binary multiplication assignment operator (*=) [C#]
ms.assetid: 2e472155-59db-4dbf-bb94-bcccfa1a794d
ms.openlocfilehash: 70461f79e714e44354fe4137e5360769fa048d3e
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56967384"
---
# <a name="-operator-c-reference"></a>\*=, opérateur (référence C#)

Opérateur d’assignation de multiplication.

Expression utilisant l’opérateur `*=`, par exemple

```csharp
x *= y
```

est équivalent à

```csharp
x = x * y
```

sauf que `x` n’est évalué qu’une seule fois.

Pour les types numériques, [l’opérateur \*](multiplication-operator.md) calcule le produit de ses opérandes.

L’exemple suivant illustre l’utilisation de l’opérateur `*=` :

[!code-csharp-interactive[multiply and assign](~/samples/snippets/csharp/language-reference/operators/MultiplicationExamples.cs#MultiplyAndAssign)]

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Si un type défini par l’utilisateur [surcharge](../keywords/operator.md) [l’opérateur de multiplication](multiplication-operator.md) `*`, l’opérateur d’assignation de multiplication `*=` est implicitement surchargé. Un type défini par l’utilisateur ne peut pas surcharger explicitement l’opérateur d’assignation de multiplication.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez la section [Assignation composée](~/_csharplang/spec/expressions.md#compound-assignment) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
