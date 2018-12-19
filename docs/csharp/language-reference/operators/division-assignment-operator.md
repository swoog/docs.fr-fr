---
title: /=, opérateur - Référence C#
ms.custom: seodec18
ms.date: 12/13/2018
f1_keywords:
- /=_CSharpKeyword
helpviewer_keywords:
- division assignment operator (/=) [C#]
- /= (division assignment operator) [C#]
ms.assetid: 50fc02b0-ee9c-4c3e-b58d-d591282caf1c
ms.openlocfilehash: ed4dd6c0c944b77543aae4de8d51534b4df4f4ef
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286518"
---
# <a name="-operator-c-reference"></a>/=, opérateur (référence C#)

Opérateur d’assignation de division.

Expression utilisant l’opérateur `/=`, par exemple

```csharp
x /= y
```

est équivalent à

```csharp
x = x / y
```

sauf que `x` n’est évalué qu’une seule fois.

[L’opérateur de division](division-operator.md) `/` divise son premier opérande par son deuxième opérande. Il est pris en charge par tous les types numériques.

L’exemple suivant illustre l’utilisation de l’opérateur `/=` :

[!code-csharp-interactive[divide and assign](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#DivisionAssignment)]

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Si un type défini par l’utilisateur [surcharge](../keywords/operator.md) [l’opérateur de division](division-operator.md) `/`, l’opérateur d’assignation de division `/=` est implicitement surchargé. Un type défini par l’utilisateur ne peut pas surcharger explicitement l’opérateur d’assignation de division.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez la section [Assignation composée](~/_csharplang/spec/expressions.md#compound-assignment) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
