---
title: '*=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '*=_CSharpKeyword'
helpviewer_keywords:
- '*= operator [C#]'
- binary multiplication assignment operator (*=) [C#]
ms.assetid: 2e472155-59db-4dbf-bb94-bcccfa1a794d
ms.openlocfilehash: 2038f3b55d46f3503496275b3d25b17663b8c1db
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333432"
---
# <a name="-operator-c-reference"></a>\*=, opérateur (référence C#)

Opérateur d’assignation de multiplication binaire.

## <a name="remarks"></a>Notes

Une expression qui utilise l’opérateur d’assignation `*=`, telle que

```csharp
x *= y
```

est équivalent à

```csharp
x = x * y
```

sauf que `x` n’est évalué qu’une seule fois. L’[opérateur \*](multiplication-operator.md) est prédéfini pour les types numériques de façon à effectuer une multiplication.

L’opérateur `*=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur \*](multiplication-operator.md) (voir [operator](../keywords/operator.md)).

## <a name="example"></a>Exemple

[!code-csharp[csRefOperators#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#13)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
