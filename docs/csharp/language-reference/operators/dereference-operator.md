---
title: -&gt;, opérateur (Informations de référence sur C#)
ms.date: 07/20/2015
f1_keywords:
- ->_CSharpKeyword
helpviewer_keywords:
- member access operator (->) [C#]
- -> operator [C#]
ms.assetid: e39ccdc1-f1ff-4a92-bf1d-ac2c8c11316a
ms.openlocfilehash: 09d67b8386da371f7d98a8171f60298b316091ea
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="-gt-operator-c-reference"></a>-&gt;, opérateur (Informations de référence sur C#)
L’opérateur `->` allie l’annulation de la référence d’un pointeur et l’accès au membre.  
  
## <a name="remarks"></a>Notes  
 Une expression de forme  
  
```  
x->y  
```  
  
 (où `x` est un pointeur de type `T*` et `y` un membre de `T`) est équivalente à  
  
```  
(*x).y  
```  
  
 L’opérateur `->` peut être utilisé uniquement dans du code marqué comme [unsafe](../../../csharp/language-reference/keywords/unsafe.md).  
  
 L’opérateur `->` ne peut pas être surchargé.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#15](../../../csharp/language-reference/operators/codesnippet/CSharp/dereference-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
