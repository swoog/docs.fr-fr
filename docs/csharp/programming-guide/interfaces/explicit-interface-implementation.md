---
title: Implémentation d’interface explicite - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- explicit interfaces [C#]
- interfaces [C#], explicit
ms.assetid: 181c901f-0d4c-4f29-97fc-895079617bf2
ms.openlocfilehash: c57ba732c5139d7ead85372323f9433bd3137622
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54570211"
---
# <a name="explicit-interface-implementation-c-programming-guide"></a>Implémentation d’interface explicite (Guide de programmation C#)
Si une [classe](../../../csharp/language-reference/keywords/class.md) implémente deux interfaces qui contiennent un membre avec la même signature, l’implémentation de ce membre sur la classe a pour conséquence que les deux interfaces utilisent ce membre comme leur implémentation. Dans l’exemple suivant, tous les appels à `Paint` appellent la même méthode.  
  
 [!code-csharp[csProgGuideInheritance#39](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/explicit-interface-implementation_1.cs)]  
  
 Toutefois, si les deux membres d’[interface](../../../csharp/language-reference/keywords/interface.md) n’exécutent pas la même fonction, cela peut engendrer une implémentation incorrecte d’une interface ou des deux. Il est possible d’implémenter un membre d’interface explicitement, en créant un membre de classe qui n’est appelé que via l’interface et qui est spécifique à cette interface. Pour ce faire, vous devez nommer le membre de classe avec le nom de l’interface et un point. Par exemple :  
  
 [!code-csharp[csProgGuideInheritance#40](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/explicit-interface-implementation_2.cs)]  
  
 Le membre de classe `IControl.Paint` est disponible uniquement via l’interface `IControl` et `ISurface.Paint` est disponible uniquement via `ISurface`. Les deux implémentations de méthode sont distinctes, et aucune n’est directement disponible sur la classe. Par exemple :  
  
 [!code-csharp[csProgGuideInheritance#41](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/explicit-interface-implementation_3.cs)]  
  
 L’implémentation explicite est également utilisée pour résoudre les cas où deux interfaces déclarent chacune des membres différents du même nom, comme une propriété et une méthode :  
  
 [!code-csharp[csProgGuideInheritance#42](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/explicit-interface-implementation_4.cs)]  
  
 Pour implémenter les deux interfaces, une classe doit utiliser l’implémentation explicite pour la propriété P, la méthode P, ou les deux, pour éviter une erreur du compilateur. Par exemple :  
  
 [!code-csharp[csProgGuideInheritance#43](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/explicit-interface-implementation_5.cs)]  
  
## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../../../csharp/programming-guide/index.md)
- [Classes et structs](../../../csharp/programming-guide/classes-and-structs/index.md)
- [Interfaces](../../../csharp/programming-guide/interfaces/index.md)
- [Héritage](../../../csharp/programming-guide/classes-and-structs/inheritance.md)
