---
title: '>>=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- '>>=_CSharpKeyword'
helpviewer_keywords:
- right shift assignment operator (>>=) [C#]
- '>>= operator (right-shift assignment) [C#]'
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
ms.openlocfilehash: 51914bb5e9ebffd5d868528b5a8d3072a956cea6
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56220911"
---
# <a name="-operator-c-reference"></a>>>=, opérateur (référence C#)

Opérateur d’assignation de décalage vers la droite.

Expression utilisant l’opérateur `>>=`, par exemple

```csharp
x >>= y
```

est équivalent à

```csharp
x = x >> y
```

sauf que `x` n’est évalué qu’une seule fois.

L’opérateur [`>>` ](right-shift-operator.md) décale son premier opérande vers la droite du nombre de bits spécifié par son deuxième opérande.

L’exemple suivant illustre l’utilisation de l’opérateur `>>=` :

[!code-csharp-interactive[right shift assignment](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShiftAssignment)]

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Si un type défini par l’utilisateur [surcharge ](../keywords/operator.md) l’[`>>`opérateur](right-shift-operator.md), l’opérateur d’assignation de décalage vers la droite `>>=` est implicitement surchargé. Un type défini par l’utilisateur ne peut pas surcharger explicitement l’opérateur d’assignation de décalage vers la droite.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez la section [Assignation composée](~/_csharplang/spec/expressions.md#compound-assignment) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)