---
title: '- opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- -_CSharpKeyword
helpviewer_keywords:
- '- operator [C#]'
- subtraction operator (-) [C#]
ms.assetid: 4de7a4fa-c69d-48e6-aff1-3130af970b2d
ms.openlocfilehash: 8cf6e8871a88e2b37b9531ecbd616289523473c7
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333757"
---
# <a name="--operator-c-reference"></a>-, opérateur (référence C#)

L’opérateur `-` peut être utilisé comme opérateur unaire ou opérateur binaire.

## <a name="remarks"></a>Notes

Les opérateurs `-` sont prédéfinis pour tous les types numériques. Le résultat d’une opération `-` unaire sur un type numérique correspond à la négation numérique de l’opérande.

Les opérateurs `-` binaires sont prédéfinis pour tous les types numériques et d’énumérations pour soustraire le second opérande au premier.

Les types délégués fournissent également un opérateur `-` binaire, qui effectue une suppression de délégué.

Les types définis par l’utilisateur peuvent surcharger les opérateurs `-` unaires et `-` binaires. Pour plus d’informations, consultez [operator, mot clé](../keywords/operator.md).

## <a name="example"></a>Exemple

[!code-csharp[csRefOperators#40](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#40)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)