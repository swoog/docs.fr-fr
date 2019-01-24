---
title: '&gt;&gt;=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '>>=_CSharpKeyword'
helpviewer_keywords:
- right shift assignment operator (>>=) [C#]
- '>>= operator (right-shift assignment) [C#]'
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
ms.openlocfilehash: 02a9559a5c4086eeed09094c15c3620366ffad8c
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333684"
---
# <a name="gtgt-operator-c-reference"></a>&gt;&gt;=, opérateur (référence C#)

Opérateur d’assignation de décalage vers la droite.

## <a name="remarks"></a>Notes

Une expression sous la forme

```csharp
x >>= y
```

est évaluée comme étant

```csharp
x = x >> y
```

sauf que `x` n’est évalué qu’une seule fois. L’[opérateur >>](right-shift-operator.md) décale `x` vers la droite de la valeur spécifiée par `y`.

L’opérateur >>= ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur >>](right-shift-operator.md) (voir [operator](../keywords/operator.md)).

## <a name="example"></a>Exemple

[!code-csharp[csRefOperators#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#11)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)