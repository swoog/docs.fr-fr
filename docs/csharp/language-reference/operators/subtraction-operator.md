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
ms.openlocfilehash: 920981addd5c779c9ad1c666ef45e1de5cd23408
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65633000"
---
# <a name="--operator-c-reference"></a>-, opérateur (référence C#)

L’opérateur `-` peut être utilisé comme opérateur unaire ou opérateur binaire.

## <a name="remarks"></a>Remarques

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
