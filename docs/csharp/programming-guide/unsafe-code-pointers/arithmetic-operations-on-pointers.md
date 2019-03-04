---
title: Opérations arithmétiques sur les pointeurs - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], arithmetic operations
ms.assetid: d4f0b623-827e-45ce-8649-cfcebc8692aa
ms.openlocfilehash: bfa81bc926b4fe81455cecb88bc55f4dcd69268e
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56977836"
---
# <a name="arithmetic-operations-on-pointers-c-programming-guide"></a>Opérations arithmétiques sur les pointeurs (Guide de programmation C#)
Cette rubrique explique comment utiliser les opérateurs arithmétiques `+` et `-` pour manipuler les pointeurs.  
  
> [!NOTE]
>  Vous ne pouvez pas effectuer d’opérations arithmétiques sur les pointeurs void.  
  
## <a name="adding-and-subtracting-numeric-values-to-or-from-pointers"></a>Ajouter et soustraire des valeurs numériques aux pointeurs  
 Vous pouvez ajouter une valeur `n` de type [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md) ou [ulong](../../../csharp/language-reference/keywords/ulong.md) à un pointeur. Si `p` est un pointeur de type `pointer-type*`, le résultat `p+n` est le pointeur résultant de l’ajout de `n * sizeof(pointer-type)` à l’adresse de `p`. De la même façon, `p-n` est le pointeur qui résulte de la soustraction de `n * sizeof(pointer-type)` de l’adresse de `p`.  
  
## <a name="subtracting-pointers"></a>Soustraire des pointeurs  
 Vous pouvez également soustraire des pointeurs du même type. Le résultat est toujours du type `long`. Par exemple, si `p1` et `p2` sont des pointeurs du type `pointer-type*`, l’expression `p1-p2` produit le résultat suivant :  
  
 `((long)p1 - (long)p2)/sizeof(pointer-type)`  
  
 Aucune exception n’est générée si l’opération arithmétique produit un dépassement de capacité sur le domaine du pointeur, et le résultat dépend de l’implémentation.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csProgGuidePointers#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuidePointers/CS/Pointers2.cs#14)]  
  
 [!code-csharp[csProgGuidePointers#15](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuidePointers/CS/Pointers.cs#15)]  
  
## <a name="c-language-specification"></a>spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../../../csharp/programming-guide/index.md)
- [Pointeurs et code unsafe](../../../csharp/programming-guide/unsafe-code-pointers/index.md)
- [Expressions de pointeur](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
- [Manipulation de pointeurs](../../../csharp/programming-guide/unsafe-code-pointers/manipulating-pointers.md)
- [Types de pointeur](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [Types](../../../csharp/language-reference/keywords/types.md)
- [unsafe](../../../csharp/language-reference/keywords/unsafe.md)
- [fixed, instruction](../../../csharp/language-reference/keywords/fixed-statement.md)
- [stackalloc](../../../csharp/language-reference/keywords/stackalloc.md)
