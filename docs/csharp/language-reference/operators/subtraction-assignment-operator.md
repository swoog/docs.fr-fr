---
title: -=, opérateur - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- -=_CSharpKeyword
helpviewer_keywords:
- subtraction assignment operator (-=) [C#]
- -= operator (subtraction assignment ) [C#]
ms.assetid: 05c7d68a-423f-4de8-891b-cf24e8fb6ed7
ms.openlocfilehash: 3b6890be4460a599a5d2f5f5f6ee1627be933f0b
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333328"
---
# <a name="--operator-c-reference"></a>-=, opérateur (référence C#)

Opérateur d’assignation de soustraction.

## <a name="remarks"></a>Notes

Une expression qui utilise l’opérateur d’assignation `-=`, telle que

```csharp
x -= y
```

 est équivalent à

```csharp
x = x - y
```

sauf que `x` n’est évalué qu’une seule fois. La signification de l’[opérateur -](subtraction-operator.md) dépend des types de `x` et `y` (soustraction pour les opérandes numériques, suppression de délégués pour les opérandes délégués, etc.).

L’opérateur `-=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur -](subtraction-operator.md) (voir [opérateur](../keywords/operator.md)).

L’opérateur -= est également utilisé en C# pour annuler l’abonnement à un événement. Pour plus d'informations, voir [Procédure : s’abonner et se désabonner d’événements](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).

## <a name="example"></a>Exemple

[!code-csharp[csRefOperators#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#6)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
