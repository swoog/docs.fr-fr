---
title: +=, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- +=_CSharpKeyword
helpviewer_keywords:
- += operator [C#]
- addition assignment operator (+=) [C#]
ms.assetid: 9cdf97e6-331d-492b-85e1-3ec3171484e9
ms.openlocfilehash: bcd56acad8e2b08585e5ae60f1c3cf8183b5664a
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
ms.locfileid: "34171877"
---
# <a name="-operator-c-reference"></a>+=, opérateur (référence C#)
Opérateur d’assignation d’addition.  
  
## <a name="remarks"></a>Notes  
 Une expression qui utilise l’opérateur d’assignation `+=`, telle que  
  
```csharp  
x += y  
```  
  
 est équivalent à  
  
```csharp  
x = x + y  
```  
  
 sauf que `x` n’est évalué qu’une seule fois. La signification de l’[opérateur +](../../../csharp/language-reference/operators/addition-operator.md) dépend des types de `x` et `y` (addition pour les opérandes numériques, concaténation pour les opérandes de type chaîne, etc.).  
  
 L’opérateur `+=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur -](../../../csharp/language-reference/operators/addition-operator.md) (consultez [operator](../../../csharp/language-reference/keywords/operator.md)).  
  
 L’opérateur `+=` est également utilisé pour spécifier une méthode qui sera appelée en réponse à un événement ; ces méthodes sont appelées « gestionnaires d’événements ». L’utilisation de l’opérateur `+=` dans ce contexte est appelée *abonnement à un événement*. Pour plus d’informations, consultez [Guide pratique pour s’abonner et annuler l’abonnement à des événements](../../../csharp/programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md) et [Délégués](../../../csharp/programming-guide/delegates/index.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#35](../../../csharp/language-reference/operators/codesnippet/CSharp/addition-assignment-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
