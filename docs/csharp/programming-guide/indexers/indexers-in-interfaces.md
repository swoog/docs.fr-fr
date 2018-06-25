---
title: Indexeurs dans les interfaces (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- indexers [C#], in interfaces
- accessors [C#], indexers
ms.assetid: e16b54bd-4a83-4f52-bd75-65819fca79e8
ms.openlocfilehash: 120b6e72a6ab906437c593d6eb33024d1df8f52b
ms.sourcegitcommit: 6bc4efca63e526ce6f2d257fa870f01f8c459ae4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36207897"
---
# <a name="indexers-in-interfaces-c-programming-guide"></a>Indexeurs dans les interfaces (Guide de programmation C#)
Des indexeurs peuvent être déclarés dans une [interface](../../../csharp/language-reference/keywords/interface.md). Les accesseurs d’indexeurs d’interface se distinguent sur plusieurs plans des accesseurs d’indexeurs de [classe](../../../csharp/language-reference/keywords/class.md), à savoir :  
  
-   Les accesseurs d’interface n’utilisent pas de modificateurs.  
  
-   Un accesseur d’interface n’a pas de corps.  
  
 Par conséquent, un accesseur vise à indiquer si l’indexeur est en lecture-écriture, en lecture seule ou en écriture seule.  
  
 L’exemple ci-dessous porte sur un accesseur d’indexeur d’interface :  
  
 [!code-csharp[csProgGuideIndexers#3](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/indexers-in-interfaces_1.cs)]  
  
 La signature d’un indexeur doit se distinguer de tous les autres indexeurs déclarés dans la même interface.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment implémenter des indexeurs d’interface.  
  
 [!code-csharp[csProgGuideIndexers#4](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/indexers-in-interfaces_2.cs)]  
  
 Dans l’exemple précédent, vous pouvez utiliser l’implémentation de membre d’interface explicite en utilisant le nom qualifié complet du membre d’interface. Exemple :  
  
```  
string ISomeInterface.this[int index]   
{   
}   
```  
  
 Cependant, le nom qualifié complet est seulement nécessaire pour éviter toute ambiguïté quand la classe implémente plusieurs interfaces avec la même signature d’indexeur. Par exemple, si une classe `Employee` implémente deux interfaces, `ICitizen` et `IEmployee`, et que les deux interfaces ont la même signature d’indexeur, l’implémentation de membre d’interface explicite est nécessaire. Autrement dit, la déclaration d’indexeur suivante :  
  
```  
string IEmployee.this[int index]   
{   
}   
```  
  
 implémente l’indexeur dans l’interface `IEmployee`, alors que la déclaration suivante :  
  
```  
string ICitizen.this[int index]
{   
}   
```  
  
 implémente l’interface dans l’interface `ICitizen`.  
  
## <a name="see-also"></a>Voir aussi  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Indexeurs](../../../csharp/programming-guide/indexers/index.md)  
 [Propriétés](../../../csharp/programming-guide/classes-and-structs/properties.md)  
 [Interfaces](../../../csharp/programming-guide/interfaces/index.md)
