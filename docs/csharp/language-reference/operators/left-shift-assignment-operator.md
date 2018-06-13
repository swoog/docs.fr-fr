---
title: '&lt;&lt;=, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: e5f3886670baa34b0360501ee15280b93fac36bc
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
ms.locfileid: "34171791"
---
# <a name="ltlt-operator-c-reference"></a>&lt;&lt;=, opérateur (référence C#)
Opérateur d’assignation de décalage vers la gauche.  
  
## <a name="remarks"></a>Notes  
 Une expression sous la forme  
  
```csharp  
x <<= y  
```  
  
 est évaluée comme étant  
  
```csharp  
x = x << y  
```  
  
 sauf que `x` n’est évalué qu’une seule fois. L’[opérateur << ](../../../csharp/language-reference/operators/left-shift-operator.md) déplace `x` vers la gauche du nombre de bits spécifié par `y`.  
  
 L’opérateur `<<=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur <<](../../../csharp/language-reference/operators/left-shift-operator.md) (consultez [operator](../../../csharp/language-reference/keywords/operator.md)).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#12](../../../csharp/language-reference/operators/codesnippet/CSharp/left-shift-assignment-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
