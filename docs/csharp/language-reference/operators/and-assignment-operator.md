---
title: '&amp;=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 10/29/2018
f1_keywords:
- '&=_CSharpKeyword'
helpviewer_keywords:
- AND assignment operator (&=) [C#]
- '&= operator [C#]'
ms.assetid: e8d58f3f-72dd-4b5a-b995-452fcce7e6bb
ms.openlocfilehash: 223d2f30ee77457e1f9d5304ec299517932499d0
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237023"
---
# <a name="amp-operator-c-reference"></a>&amp;=, opérateur (référence C#)

Opérateur d’assignation AND.

Expression utilisant l’opérateur `&=`, par exemple

```csharp
x &= y
```

est équivalent à

```csharp
x = x & y
```

sauf que `x` n’est évalué qu’une seule fois.

Pour les opérandes entiers, [l’opérateur `&`](and-operator.md) calcule l’opération logique AND au niveau du bit de ses opérandes ; pour les opérandes [bool](../keywords/bool.md), il calcule l’opération logique AND de ses opérandes.

L’exemple suivant illustre l’utilisation de l’opérateur `&=` :

[!code-csharp-interactive[AND assignment example](~/samples/snippets/csharp/language-reference/operators/AndOperatorExamples.cs#AndAssignmentExample)]

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Si un type défini par l’utilisateur [surcharge](../keywords/operator.md) [l’opérateur `&` ](and-operator.md), l’opérateur d’assignation AND `&=` est implicitement surchargé. Un type défini par l’utilisateur ne peut pas surcharger explicitement l’opérateur d’assignation AND.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez la section [Assignation composée](~/_csharplang/spec/expressions.md#compound-assignment) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
