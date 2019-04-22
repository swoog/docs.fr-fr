---
title: Les classes dérivées ne peuvent pas déclencher les événements de la classe de base
ms.date: 07/20/2015
f1_keywords:
- vbc30029
- bc30029
helpviewer_keywords:
- BC30029
ms.assetid: 63afa1c6-2f93-4512-a2f0-372455979771
ms.openlocfilehash: 0e9acf4b3e71295655c15ae9b1c80852c9aca8df
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58835139"
---
# <a name="derived-classes-cannot-raise-base-class-events"></a>Les classes dérivées ne peuvent pas déclencher les événements de la classe de base
Un événement peut être déclenché uniquement à partir de l’espace de déclaration dans laquelle elle est déclarée. Par conséquent, une classe ne peut pas déclencher d’événements à partir d’une autre classe, même si celle-ci à partir de laquelle elle est dérivée.  
  
 **ID d’erreur :** BC30029  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Déplacer le `Event` instruction ou la `RaiseEvent` instruction afin qu’ils soient dans la même classe.  
  
## <a name="see-also"></a>Voir aussi

- [Event (instruction)](../../../visual-basic/language-reference/statements/event-statement.md)
- [RaiseEvent (instruction)](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
