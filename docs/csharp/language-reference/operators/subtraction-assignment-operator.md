---
title: -=, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- -=_CSharpKeyword
helpviewer_keywords:
- subtraction assignment operator (-=) [C#]
- -= operator (subtraction assignment ) [C#]
ms.assetid: 05c7d68a-423f-4de8-891b-cf24e8fb6ed7
ms.openlocfilehash: 2f37bfa303fb523840b15e896ee3b4a967eb5b2b
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
---
# <a name="--operator-c-reference"></a>-=, opérateur (référence C#)
Opérateur d’assignation de soustraction.  
  
## <a name="remarks"></a>Notes  
 Une expression qui utilise l’opérateur d’assignation `-=`, telle que  
  
```csharp  
x -= y  
```  
  
 est équivalent à  
  
```csharp  
x = x - y  
```  
  
 sauf que `x` n’est évalué qu’une seule fois. La signification de l’[opérateur -](../../../csharp/language-reference/operators/subtraction-operator.md) dépend des types de `x` et `y` (soustraction pour les opérandes numériques, suppression de délégués pour les opérandes délégués, etc.).  
  
 L’opérateur `-=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur -](../../../csharp/language-reference/operators/subtraction-operator.md) (voir [opérateur](../../../csharp/language-reference/keywords/operator.md)).  
  
 L’opérateur -= est également utilisé en C# pour annuler l’abonnement à un événement. Pour plus d’informations, consultez [Guide pratique pour s’abonner et annuler l’abonnement à des événements](../../../csharp/programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#6](codesnippet/CSharp/subtraction-assignment-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
