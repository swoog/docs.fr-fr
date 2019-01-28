---
title: ^, opérateur - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ^_CSharpKeyword
helpviewer_keywords:
- ^ operator [C#]
- bitwise exclusive OR operator [C#]
ms.assetid: b09bc815-570f-4db6-a637-5b4ed99d014a
ms.openlocfilehash: 16419342fec9d6c9845e19e434787c5e4f5a5b12
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54632246"
---
# <a name="-operator-c-reference"></a>^, opérateur (référence C#)

Les opérateurs `^` binaires sont prédéfinis pour les types intégraux et `bool`. Pour les types intégraux, `^` effectue l’opération de bits OR exclusif sur les opérandes. Pour les opérandes `bool`, `^` effectue l’opération OR exclusif logique sur ses opérandes. En conséquence, le résultat est `true` si et seulement si un seul des opérandes correspond à `true`.

## <a name="remarks"></a>Notes

Les types définis par l’utilisateur peuvent surcharger l’opérateur `^` (voir [operator](../keywords/operator.md)). Les opérations sur les types intégraux sont en général autorisées sur l’énumération.

## <a name="example"></a>Exemple

[!code-csharp[csRefOperators#30](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#30)]

Le calcul de `0xf8 ^ 0x3f` dans l’exemple précédent effectue une opération de bits OR exclusif des deux valeurs binaires suivantes, qui correspondent aux valeurs hexadécimales F8 et 3F :

`1111 1000`

`0011 1111`

Le résultat de l’opération OR exclusif est `1100 0111`, qui correspond à C7 en hexadécimal.

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
