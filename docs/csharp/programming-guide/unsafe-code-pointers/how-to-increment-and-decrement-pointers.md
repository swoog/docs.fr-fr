---
title: 'Guide pratique : Incrémenter et décrémenter des pointeurs (Guide de programmation C#)'
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], increment and decrement
- pointer expressions [C#], increment and decrement
ms.assetid: 1b8b9281-44ee-485a-9045-3db38a4b4b89
ms.openlocfilehash: c75432d88a1e96742573a6e69a4e035066a387c4
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53128334"
---
# <a name="how-to-increment-and-decrement-pointers-c-programming-guide"></a>Guide pratique : Incrémenter et décrémenter des pointeurs (Guide de programmation C#)

Utilisez les opérateurs d’incrémentation et de décrémentation, `++` et `--`, pour changer l’emplacement du pointeur de `sizeof(pointer-type)` pour un pointeur de type `pointer-type*`. Les expressions d’incrémentation et de décrémentation prennent la forme suivante :  
  
```csharp
++p;  
p++;  
--p;  
p--;  
```  
  
 Les opérateurs d’incrémentation et de décrémentation peuvent être appliqués aux pointeurs de tout type à l’exception du type `void*`.  
  
 L’application de l’opérateur d’incrémentation à un pointeur de type `pointer-type*` a pour effet d’ajouter `sizeof(pointer-type)` à l’adresse contenue dans la variable pointeur.  
  
 L’application de l’opérateur de décrémentation à un pointeur de type `pointer-type*` a pour effet de soustraire `sizeof(pointer-type)` à l’adresse contenue dans la variable pointeur.  
  
 Aucune exception n’est générée si l’opération produit un dépassement de capacité sur le domaine du pointeur, et le résultat dépend de l’implémentation.  
  
## <a name="example"></a>Exemple  
 Dans cet exemple, vous parcourez un tableau en incrémentant le pointeur de la taille de `int`. À chaque étape, vous affichez l’adresse et le contenu de l’élément de tableau.  
  
 [!code-csharp[csProgGuidePointers#3](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-increment-and-decrement-pointers_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#13](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-increment-and-decrement-pointers_2.cs)]  
  
**Value:0 @ Address:12860272**
**Value:1 @ Address:12860276**
**Value:2 @ Address:12860280**
**Value:3 @ Address:12860284**
**Value:4 @ Address:12860288**

## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Expressions de pointeur](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)  
- [Manipulation de pointeurs](../../../csharp/programming-guide/unsafe-code-pointers/manipulating-pointers.md)  
- [Types de pointeur](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)  
- [Types](../../../csharp/language-reference/keywords/types.md)  
- [unsafe](../../../csharp/language-reference/keywords/unsafe.md)  
- [fixed, instruction](../../../csharp/language-reference/keywords/fixed-statement.md)  
- [stackalloc](../../../csharp/language-reference/keywords/stackalloc.md)
- [sizeof](../../../csharp/language-reference/keywords/sizeof.md)
