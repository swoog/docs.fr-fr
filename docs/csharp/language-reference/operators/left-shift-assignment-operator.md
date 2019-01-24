---
title: '&lt;&lt;=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: 4513c4b78dea3e8102c72a43249b4a44ffa2421d
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333250"
---
# <a name="ltlt-operator-c-reference"></a>&lt;&lt;=, opérateur (référence C#)

Opérateur d’assignation de décalage vers la gauche.

## <a name="remarks"></a>Notes

Une expression sous la forme

```csharp
x <<= y
```

est évaluée comme étant

```csharp
x = x << y
```

sauf que `x` n’est évalué qu’une seule fois. L’[opérateur << ](left-shift-operator.md) déplace `x` vers la gauche du nombre de bits spécifié par `y`.

L’opérateur `<<=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur <<](left-shift-operator.md) (consultez [operator](../keywords/operator.md)).

## <a name="example"></a>Exemple

[!code-csharp[csRefOperators#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#12)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
