---
title: <<=, opérateur - Référence C#
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: d2105fbee4ddfe1b2cb3325d82b0f2f8c5559297
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219447"
---
# <a name="-operator-c-reference"></a>\<\<=, opérateur (référence C#)

Opérateur d’assignation de décalage vers la gauche.

Expression utilisant l’opérateur `<<=`, par exemple

```csharp
x <<= y
```

est équivalent à

```csharp
x = x << y
```

sauf que `x` n’est évalué qu’une seule fois.

L’[`<<`opérateur](left-shift-operator.md) décale son premier opérande vers la gauche du nombre de bits spécifié par son deuxième opérande.

L’exemple suivant illustre l’utilisation de l’opérateur `<<=` :

[!code-csharp-interactive[left shift assignment](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#LeftShiftAssignment)]

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Si un type défini par l’utilisateur [surcharge ](../keywords/operator.md) l’[`<<`opérateur](left-shift-operator.md), l’opérateur d’assignation de décalage vers la gauche `<<=` est implicitement surchargé. Un type défini par l’utilisateur ne peut pas surcharger explicitement l’opérateur d’assignation de décalage vers la gauche.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez la section [Assignation composée](~/_csharplang/spec/expressions.md#compound-assignment) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
