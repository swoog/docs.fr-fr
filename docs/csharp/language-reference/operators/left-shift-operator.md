---
title: '&lt;&lt;, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <<_CSharpKeyword
helpviewer_keywords:
- left shift operator (<<) [C#]
- << operator [C#]
ms.assetid: a654eb56-1ff7-4bf3-9064-b631be0cdccc
ms.openlocfilehash: 79a48d88e2c83b5ad78804367ee3c07f78622c08
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333523"
---
# <a name="ltlt-operator-c-reference"></a>&lt;&lt;, opérateur (référence C#)

L’opérateur de décalage vers la gauche (`<<`) décale son premier opérande vers la gauche du nombre de bits spécifié par son deuxième opérande. Le deuxième opérande doit être de type [int](../keywords/int.md) ou d’un type pour lequel une conversion numérique implicite vers `int` est prédéfinie.

## <a name="remarks"></a>Notes

Si le premier opérande est de type [int](../keywords/int.md) ou [uint](../keywords/uint.md) (quantité de 32 bits), la valeur du décalage est donnée par les cinq bits de poids faible du second opérande. Autrement dit, la valeur réelle du décalage est comprise entre 0 et 31 bits.

Si le premier opérande est de type [long](../keywords/long.md) ou [ulong](../keywords/ulong.md) (quantité de 64 bits), la valeur du décalage est donnée par les six bits de poids faible du second opérande. Autrement dit, la valeur réelle du décalage est comprise entre 0 et 63 bits.

Les bits de poids fort qui ne se trouvent pas dans la plage du type du premier opérande après le décalage sont ignorés, et les bits vides de poids faible sont remplis de zéros. Les opérations de décalage ne provoquent jamais de dépassements de capacité.

Les types définis par l’utilisateur peuvent surcharger l’opérateur `<<` (consultez [operator](../keywords/operator.md)) ; le type du premier opérande doit être le type défini par l’utilisateur, et le type du second opérande doit être `int`. Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.

## <a name="example"></a>Exemple

[!code-csharp[csRefOperators#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#14)]

## <a name="comments"></a>Commentaires

Notez que `i<<1` et `i<<33` donnent le même résultat, car 1 et 33 possèdent les cinq mêmes bits de poids faible.

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
