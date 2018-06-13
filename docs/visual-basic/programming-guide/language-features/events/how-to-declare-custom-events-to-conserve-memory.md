---
title: 'Comment : déclarer des événements personnalisés pour économiser la mémoire (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- declaring events [Visual Basic], custom
- events [Visual Basic], custom
- custom events [Visual Basic]
ms.assetid: 87ebee87-260c-462f-979c-407874debd19
ms.openlocfilehash: d19c91d66e458ca2317dc049d517b92fa7406ef6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33647177"
---
# <a name="how-to-declare-custom-events-to-conserve-memory-visual-basic"></a>Comment : déclarer des événements personnalisés pour économiser la mémoire (Visual Basic)
Il existe plusieurs circonstances lorsqu’il est important qu’une application conserve son utilisation de la mémoire basse. Événements personnalisés permettent à l’application d’utiliser la mémoire uniquement pour les événements qu’il gère.  
  
 Par défaut, lorsqu’une classe déclare un événement, le compilateur alloue la mémoire pour un champ stocker les informations d’événement. Si une classe comporte plusieurs événements inutilisés, leur mémoire inutilement.  
  
 Au lieu d’utiliser l’implémentation par défaut d’événements Visual Basic, vous pouvez utiliser des événements personnalisés pour gérer l’utilisation de la mémoire plus attentivement.  
  
## <a name="example"></a>Exemple  
 Dans cet exemple, la classe utilise une instance de la <xref:System.ComponentModel.EventHandlerList> (classe), stockée dans le `Events` champ pour stocker des informations sur les événements en cours d’utilisation. Le <xref:System.ComponentModel.EventHandlerList> est une classe de liste optimisée conçue pour contenir des délégués.  
  
 Tous les événements de la classe utilisent la `Events` champ pour effectuer le suivi des méthodes qui gèrent chaque événement.  
  
 [!code-vb[VbVbalrEvents#22](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-declare-custom-events-to-conserve-memory_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ComponentModel.EventHandlerList>  
 [Événements](../../../../visual-basic/programming-guide/language-features/events/index.md)  
 [Guide pratique : déclarer des événements personnalisés pour éviter les blocages](../../../../visual-basic/programming-guide/language-features/events/how-to-declare-custom-events-to-avoid-blocking.md)
