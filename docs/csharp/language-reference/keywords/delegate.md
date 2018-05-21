---
title: delegate (référence C#)
ms.date: 07/20/2015
f1_keywords:
- delegate_CSharpKeyword
- delegate
- CS0123
helpviewer_keywords:
- delegate keyword [C#]
- function pointers [C#]
ms.assetid: 0bb8cb6d-2f87-47c7-9d1f-d65c1cd01e9f
ms.openlocfilehash: 4eafd0ffb6da191db80fd69f1980a167dbfc742b
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
---
# <a name="delegate-c-reference"></a>delegate (référence C#)
La déclaration d’un type délégué est semblable à une signature de méthode. Elle a une valeur de retour et un nombre quelconque de paramètres de type quelconque :  
  
```csharp  
public delegate void TestDelegate(string message);  
public delegate int TestDelegate(MyType m, long num);  
```  
  
 Un `delegate` est un type référence qui peut être utilisé pour encapsuler une méthode anonyme ou nommée. Les délégués sont comparables aux pointeurs fonction en C++, mais ils offrent l’avantage d’être sûrs et de type sécurisé. Pour les applications de délégués, consultez [Délégués](../../../csharp/programming-guide/delegates/index.md) et [Délégués génériques](../../../csharp/programming-guide/generics/generic-delegates.md).  
  
## <a name="remarks"></a>Notes  
 Les délégués sont la base des [événements](../../../csharp/programming-guide/events/index.md).  
  
 Un délégué peut être instancié en l’associant à une méthode nommée ou anonyme. Pour plus d’informations, consultez [Méthodes nommées](../../../csharp/programming-guide/delegates/delegates-with-named-vs-anonymous-methods.md) et [Méthodes anonymes](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md).  
  
 Le délégué doit être instancié avec une méthode ou une expression lambda qui a un type de retour compatible et des paramètres d’entrée. Pour plus d’informations sur le degré de variance autorisé dans la signature de méthode, consultez [Variance dans les délégués](../../programming-guide/concepts/covariance-contravariance/using-variance-in-delegates.md). Pour une utilisation avec des méthodes anonymes, le délégué et le code à lui associer sont déclarés ensemble. Les deux façons d’instancier un délégué sont décrites dans cette section.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csrefKeywordsTypes#8](../../../csharp/language-reference/keywords/codesnippet/CSharp/delegate_1.cs)]  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
 [Types référence](../../../csharp/language-reference/keywords/reference-types.md)  
 [Délégués](../../../csharp/programming-guide/delegates/index.md)  
 [Événements](../../../csharp/programming-guide/events/index.md)  
 [Délégués avec méthodes nommées et méthodes anonymes](../../../csharp/programming-guide/delegates/delegates-with-named-vs-anonymous-methods.md)  
 [Méthodes anonymes](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md)
