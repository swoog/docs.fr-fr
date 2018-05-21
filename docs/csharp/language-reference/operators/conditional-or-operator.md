---
title: '||, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- '||_CSharpKeyword'
helpviewer_keywords:
- logical OR operator [C#]
- conditional-OR operator (||) [C#]
- '|| operator [C#]'
ms.assetid: 7d442d8e-400d-421f-b4d2-034bf82bcbdc
ms.openlocfilehash: d22e57d097edb0fe52b604e9c6431e167c410f0b
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
---
# <a name="-operator-c-reference"></a>||, opérateur (référence C#)
L’opérateur conditionnel OR (`||`) effectue une opération OR logique de ses opérandes `bool`. Si le premier opérande prend la valeur `true`, le deuxième opérande n’est pas évalué. Si le premier opérande prend la valeur `false`, le deuxième opérateur détermine si l’expression OR dans son ensemble prend la valeur `true` ou `false`.  
  
## <a name="remarks"></a>Notes  
 L’opération  
  
```csharp  
x || y  
```  
  
 correspond à l’opération  
  
```csharp  
x | y  
```  
  
 sauf si `x` a la valeur `true`, auquel cas `y` n’est pas évalué, car l’opération OR a la valeur `true`, indépendamment de la valeur d’`y`. Ce concept est connu sous le nom d’évaluation de « court-circuit ».  
  
 L’opérateur OR conditionnel ne peut pas être surchargé, mais les surcharges des opérateurs logiques normaux et des opérateurs [true](../../../csharp/language-reference/keywords/true.md) et [false](../../../csharp/language-reference/keywords/false.md) sont, avec certaines restrictions, également considérées comme des surcharges des opérateurs logiques conditionnels.  
  
## <a name="example"></a>Exemple  
 Dans les exemples suivants, l’expression qui utilise `||` évalue seulement le premier opérande. L’expression qui utilise `|` évalue les deux opérandes. Dans le deuxième exemple, une exception runtime se produit si les deux opérandes sont évalués.  
  
 [!code-csharp[csRefOperators#52](../../../csharp/language-reference/operators/codesnippet/CSharp/conditional-or-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
