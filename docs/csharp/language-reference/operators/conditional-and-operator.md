---
title: '&amp;&amp;, opérateur (Informations de référence sur C#)'
ms.date: 07/20/2015
f1_keywords:
- '&&_CSharpKeyword'
helpviewer_keywords:
- '&& operator [C#]'
- logical AND operator [C#]
ms.assetid: 2e4f0a1c-92a3-40f8-8e3b-17b607f20c31
ms.openlocfilehash: 86508c6eeb2998c6f202608f9204b72b60786e4a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="ampamp-operator-c-reference"></a>&amp;&amp;, opérateur (Informations de référence sur C#)
L’opérateur AND conditionnel (`&&`) effectue une opération AND logique sur ses opérandes de type `bool`, mais évalue uniquement le second opérande, si nécessaire.  
  
## <a name="remarks"></a>Notes  
 L’opération  
  
```  
x && y  
```  
  
 correspond à l’opération  
  
```  
x & y  
```  
  
 sauf si `x` a la valeur `false`, auquel cas `y` n’est pas évalué, car le résultat de l’opération AND est `false` quelle que soit la valeur de `y`. Ce procédé est connu sous le nom d’évaluation "de court-circuit".  
  
 L’opérateur AND conditionnel ne peut pas être surchargé, mais les surcharges des opérateurs logiques normaux et des opérateurs [true](../../../csharp/language-reference/keywords/true.md) et [false](../../../csharp/language-reference/keywords/false.md) sont, avec certaines restrictions, également considérées comme des surcharges des opérateurs logiques conditionnels.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple suivant, l’expression conditionnelle dans la deuxième instruction `if` évalue seulement le premier opérande, car ce dernier retourne `false`.  
  
 [!code-csharp[csRefOperators#48](../../../csharp/language-reference/operators/codesnippet/CSharp/conditional-and-operator_1.cs)]  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
