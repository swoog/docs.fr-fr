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
ms.openlocfilehash: 58e5fd72a3748e7af0894093fc461c4efb543608
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2018
ms.locfileid: "42925538"
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

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
