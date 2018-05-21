---
title: ^=, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- ^=_CSharpKeyword
helpviewer_keywords:
- ^= operator [C#]
ms.assetid: 3658ff9a-61cd-467e-ad6b-8fbf1cfbaae4
ms.openlocfilehash: b868f2cdbfa8a80f89a12e6194a30154481f0b07
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
---
# <a name="-operator-c-reference"></a>^=, opérateur (référence C#)
Opérateur d’assignation OR exclusif.  
  
## <a name="remarks"></a>Notes  
 Une expression sous la forme  
  
```csharp  
x ^= y  
```  
  
 est évaluée comme étant  
  
```csharp  
x = x ^ y  
```  
  
 sauf que `x` n’est évalué qu’une seule fois. L’[opérateur ^](../../../csharp/language-reference/operators/xor-operator.md) effectue une opération de bits OR exclusif sur les opérandes de type intégral et une opération OR exclusif logique sur les opérandes de type [bool](../../../csharp/language-reference/keywords/bool.md).  
  
 L’opérateur ^= ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur ^](../../../csharp/language-reference/operators/xor-operator.md) (voir [operator](../../../csharp/language-reference/keywords/operator.md)).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#23](../../../csharp/language-reference/operators/codesnippet/CSharp/xor-assignment-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
