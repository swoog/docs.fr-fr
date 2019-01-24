---
title: '* opérateur - Référence C#'
ms.custom: seodec18
ms.date: 04/04/2018
f1_keywords:
- '*_CSharpKeyword'
helpviewer_keywords:
- multiplication operator (*) [C#]
- '* operator [C#]'
ms.assetid: abd9a5f0-9b24-431e-971a-09ee1c45c50e
ms.openlocfilehash: f4490c4632d9344eb879ea55c20787b838781d91
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333731"
---
# <a name="-operator-c-reference"></a>*, opérateur (référence C#)

L’opérateur de multiplication (`*`) calcule le produit de ses opérandes. Tous les types numériques ont des opérateurs de multiplication prédéfinis.

Par ailleurs, `*` sert d’opérateur de déréférencement qui permet de lire un pointeur et d’écrire sur celui-ci.

## <a name="remarks"></a>Notes

L’opérateur `*` est aussi utilisé pour déclarer des types pointeur et déréférencer des pointeurs. Cet opérateur ne peut être utilisé que dans des contextes unsafe signalés par l’utilisation du mot clé [unsafe](../keywords/unsafe.md). Il nécessite l’option de compilateur [/unsafe](../compiler-options/unsafe-compiler-option.md).  L’opérateur de déréférencement est également appelé opérateur d’indirection.

Les types définis par l’utilisateur peuvent surcharger l’opérateur `*` binaire (voir [operator](../keywords/operator.md)). Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.

## <a name="example"></a>Exemple

[!code-csharp-interactive[csRefOperators#50](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#50)]

## <a name="example"></a>Exemple

[!code-csharp[csRefOperators#51](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#51)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Pointeurs et code unsafe](../../programming-guide/unsafe-code-pointers/index.md)
- [Opérateurs C#](index.md)