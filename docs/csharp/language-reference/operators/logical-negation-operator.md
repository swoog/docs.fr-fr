---
title: '! opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '!_CSharpKeyword'
helpviewer_keywords:
- '! operator [C#]'
- logical negation operator (!) [C#]
- NOT operator [C#]
ms.assetid: f5ae133f-8f64-4560-b34f-cd9cd5eed4ad
ms.openlocfilehash: 6b6d1796032f536aac0be49d4f101c1380b4e98f
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333224"
---
# <a name="-operator-c-reference"></a>! operator (référence C#)

L’opérateur de négation logique (`!`) est un opérateur unaire qui nie son opérande. Il est défini pour `bool` et retourne `true` si et seulement si son opérande a la valeur `false`.

## <a name="remarks"></a>Notes

Les types définis par l’utilisateur peuvent surcharger l’opérateur `!` (voir [operator](../keywords/operator.md)).

## <a name="example"></a>Exemple

[!code-csharp[csRefOperators#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#7)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)