---
title: +=, opérateur (référence C#)
ms.date: 10/29/2018
f1_keywords:
- +=_CSharpKeyword
helpviewer_keywords:
- += operator [C#]
- addition assignment operator (+=) [C#]
- event subscription [C#]
ms.assetid: 9cdf97e6-331d-492b-85e1-3ec3171484e9
ms.openlocfilehash: ac9330e283cb58ae4e0ee7b644aa2c22bdf64c46
ms.sourcegitcommit: 3b1cb8467bd73dee854b604e306c0e7e3882d91a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "50192029"
---
# <a name="-operator-c-reference"></a>+=, opérateur (référence C#)

Opérateur d’assignation d’addition.

Expression utilisant l’opérateur `+=`, par exemple

```csharp
x += y
```

est équivalent à

```csharp
x = x + y
```

sauf que `x` n’est évalué qu’une seule fois.
  
Pour les types numériques, [l’opérateur d’addition](addition-operator.md) `+` calcule la somme de ses opérandes. Quand les deux opérandes ou l’un d’entre eux sont de type [chaîne](../keywords/string.md), il concatène les représentations sous forme de chaîne des opérandes. Pour les types délégués, l’opérateur `+` retourne une nouvelle instance de délégué qui est la combinaison de ses opérandes.

Vous utilisez également l’opérateur `+=` pour spécifier une méthode de gestionnaire d’événements lorsque vous vous abonnez à un [événement](../keywords/event.md). Pour plus d’informations, consultez [Guide pratique pour s’abonner et annuler l’abonnement à des événements](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).

L’exemple suivant illustre l’utilisation de l’opérateur `+=` :

[!code-csharp-interactive[+= examples](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddAndAssign)]

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Si un type défini par l’utilisateur [surcharge](../keywords/operator.md) [l’opérateur d’addition](addition-operator.md) `+`, l’opérateur d’assignation d’addition `+=` est implicitement surchargé. Un type défini par l’utilisateur ne peut pas surcharger explicitement l’opérateur d’assignation d’addition.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez les sections [Assignation composée](~/_csharplang/spec/expressions.md#compound-assignment) et [Assignation d’événement](~/_csharplang/spec/expressions.md#event-assignment) de la [spécification du langage C#](../language-specification/index.md).
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [Événements](../../programming-guide/events/index.md)
- [Délégués](../../programming-guide/delegates/index.md)
