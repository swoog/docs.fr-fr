---
title: "Procédure : Implémenter de manière explicite des membres d'interface - Guide de programmation C#"
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- interfaces [C#], explicitly implementing
ms.assetid: 514cde76-f981-474e-8b40-9493619f899c
ms.openlocfilehash: 8cef6c840bf6afff8ccbf7d02012990e11d47991
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64595369"
---
# <a name="how-to-explicitly-implement-interface-members-c-programming-guide"></a>Procédure : Implémenter de manière explicite des membres d'interface (Guide de programmation C#)
Cet exemple déclare une [interface](../../../csharp/language-reference/keywords/interface.md), `IDimensions` et une classe `Box`, qui implémente de manière explicite les membres d’interface `getLength` et `getWidth`. Les membres sont accessibles via l’instance d’interface `dimensions`.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csProgGuideInheritance#8](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideInheritance/CS/Inheritance.cs#8)]  
  
## <a name="robust-programming"></a>Programmation fiable  
  
- Notez que les lignes suivantes de la méthode `Main` sont commentées car elles produiraient des erreurs de compilation. Un membre d’interface qui est implémenté de façon explicite n’est pas accessible à partir d’une instance de [classe](../../../csharp/language-reference/keywords/class.md) :  
  
     [!code-csharp[csProgGuideInheritance#45](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideInheritance/CS/Inheritance.cs#45)]  
  
- Notez également que les lignes suivantes de la méthode `Main` impriment correctement les dimensions de la zone, car les méthodes sont appelées à partir d’une instance de l’interface :  
  
     [!code-csharp[csProgGuideInheritance#46](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideInheritance/CS/Inheritance.cs#46)]  
  
## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../../../csharp/programming-guide/index.md)
- [Classes et structs](../../../csharp/programming-guide/classes-and-structs/index.md)
- [Interfaces](../../../csharp/programming-guide/interfaces/index.md)
- [Guide pratique pour implémenter de manière explicite des membres de deux interfaces](../../../csharp/programming-guide/interfaces/how-to-explicitly-implement-members-of-two-interfaces.md)
