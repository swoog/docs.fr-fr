---
title: '&amp;=, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- '&=_CSharpKeyword'
helpviewer_keywords:
- AND assignment operator (&=) [C#]
- '&= operator [C#]'
ms.assetid: e8d58f3f-72dd-4b5a-b995-452fcce7e6bb
ms.openlocfilehash: f3a6fe20ca89a90b5a64118d73fb39e9a364d1e9
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43406733"
---
# <a name="amp-operator-c-reference"></a>&amp;=, opérateur (référence C#)
Opérateur d’assignation AND.  
  
## <a name="remarks"></a>Notes  
 Une expression qui utilise l’opérateur d’assignation `&=`, telle que  
  
```csharp  
x &= y  
```  
  
 est équivalent à  
  
```csharp  
x = x & y  
```  
  
 sauf que `x` n’est évalué qu’une seule fois. L’[opérateur &](../../../csharp/language-reference/operators/and-operator.md) effectue une opération AND logique au niveau du bit sur les opérandes de type intégral et une opération AND logique sur les opérandes de type `bool`.  
  
 L’opérateur `&=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur &](../../../csharp/language-reference/operators/and-operator.md) binaire (voir [operator](../../../csharp/language-reference/keywords/operator.md)).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#34](../../../csharp/language-reference/operators/codesnippet/CSharp/and-assignment-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
