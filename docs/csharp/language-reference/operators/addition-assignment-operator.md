---
title: +=, opérateur (référence C#)
ms.date: 10/22/2018
f1_keywords:
- +=_CSharpKeyword
helpviewer_keywords:
- += operator [C#]
- addition assignment operator (+=) [C#]
- event subscription [C#]
ms.assetid: 9cdf97e6-331d-492b-85e1-3ec3171484e9
ms.openlocfilehash: ee335e3e2e7d352d4e26b802bad2b08a05c666ab
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
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

Si un type défini par l’utilisateur [surcharge](../keywords/operator.md) [l’opérateur d’addition](addition-operator.md) `+`, l’opérateur d’assignation d’addition `+=` est implicitement surchargé.

Vous utilisez également l’opérateur `+=` pour spécifier une méthode de gestionnaire d’événements lorsque vous vous abonnez à un [événement](../keywords/event.md). Pour plus d’informations, consultez [Guide pratique pour s’abonner et annuler l’abonnement à des événements](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).

L’exemple suivant illustre l’utilisation de l’opérateur `+=` :

[!code-csharp-interactive[+= examples](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddAndAssign)]
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [Événements](../../programming-guide/events/index.md)
- [Délégués](../../programming-guide/delegates/index.md)
