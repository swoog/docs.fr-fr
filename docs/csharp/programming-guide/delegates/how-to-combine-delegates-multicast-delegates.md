---
title: 'Procédure : Combiner des délégués (délégués multicast) - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- delegates [C#], combining
- multicast delegates [C#]
ms.assetid: 4e689450-6d0c-46de-acfd-f961018ae5dd
ms.openlocfilehash: d835f9b22fef550d6e73cbd620a283bd71e393ec
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237790"
---
# <a name="how-to-combine-delegates-multicast-delegatesc-programming-guide"></a>Procédure : Combiner des délégués (délégués multicast) (Guide de programmation C#)
Cet exemple explique comment créer des délégués multicast. Une propriété utile des objets [délégués](../../../csharp/language-reference/keywords/delegate.md) est que plusieurs objets peuvent être assignés à une instance de délégué à l’aide de l’opérateur `+`. Le délégué multicast contient une liste des délégués assignés. Quand le délégué multicast est appelé, il appelle les délégués dans la liste, dans l’ordre. Seuls des délégués de même type peuvent être combinés.  
  
 Vous pouvez utiliser l’opérateur `-` pour supprimer un délégué de composant d’un délégué multicast.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csProgGuideDelegates#11](../../../csharp/programming-guide/delegates/codesnippet/CSharp/how-to-combine-delegates-multicast-delegates_1.cs)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.MulticastDelegate>  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Événements](../../../csharp/programming-guide/events/index.md)
