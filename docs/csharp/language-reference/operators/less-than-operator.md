---
title: '&lt;, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- <_CSharpKeyword
helpviewer_keywords:
- less than operator (<) [C#]
- < operator [C#]
ms.assetid: 38cb91e6-79a6-48ec-9c1e-7b71fd8d2b41
ms.openlocfilehash: eceb6214e4e625aa71e12788d5dd5e8324c75443
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="lt-operator-c-reference"></a>&lt;, opérateur (référence C#)
Tous les types numériques et d’énumération définissent un opérateur relationnel « inférieur à » (`<`) qui retourne `true` si le premier opérande est inférieur au deuxième et `false` dans le cas contraire.  
  
## <a name="remarks"></a>Notes  
 Les types définis par l’utilisateur peuvent surcharger l’opérateur `<` (voir [operator](../../../csharp/language-reference/keywords/operator.md)). Si `<` est surchargé, [>](../../../csharp/language-reference/operators/greater-than-operator.md) doit aussi l’être. Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#24](../../../csharp/language-reference/operators/codesnippet/CSharp/less-than-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
