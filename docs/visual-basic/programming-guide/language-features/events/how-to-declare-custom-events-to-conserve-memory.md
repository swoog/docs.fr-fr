---
title: 'Procédure : Déclarer des événements personnalisés pour économiser la mémoire (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- declaring events [Visual Basic], custom
- events [Visual Basic], custom
- custom events [Visual Basic]
ms.assetid: 87ebee87-260c-462f-979c-407874debd19
ms.openlocfilehash: bf22c2029671588ab0ebaefd2554fcb2a5a1131c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54719519"
---
# <a name="how-to-declare-custom-events-to-conserve-memory-visual-basic"></a>Procédure : Déclarer des événements personnalisés pour économiser la mémoire (Visual Basic)
Il existe plusieurs circonstances quand il est important qu’une application limiter son utilisation de la mémoire. Événements personnalisés permettent à l’application pour utiliser la mémoire uniquement pour les événements qu’il gère.  
  
 Par défaut, lorsqu’une classe déclare un événement, le compilateur alloue la mémoire pour un champ stocker les informations d’événement. Si une classe comporte plusieurs événements inutilisés, ils mémoire inutilement.  
  
 Au lieu d’utiliser l’implémentation par défaut d’événements Visual Basic, vous pouvez utiliser des événements personnalisés pour gérer l’utilisation de la mémoire plus attentivement.  
  
## <a name="example"></a>Exemple  
 Dans cet exemple, la classe utilise une instance de la <xref:System.ComponentModel.EventHandlerList> (classe), stockée dans le `Events` champ pour stocker des informations sur les événements en cours d’utilisation. Le <xref:System.ComponentModel.EventHandlerList> est une classe de liste optimisée conçue pour contenir des délégués.  
  
 Tous les événements de la classe utilisent le `Events` afin de suivre les méthodes qui gèrent chaque événement.  
  
 [!code-vb[VbVbalrEvents#22](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-declare-custom-events-to-conserve-memory_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ComponentModel.EventHandlerList>
- [Événements](../../../../visual-basic/programming-guide/language-features/events/index.md)
- [Guide pratique pour Déclarer des événements personnalisés pour éviter les blocages](../../../../visual-basic/programming-guide/language-features/events/how-to-declare-custom-events-to-avoid-blocking.md)
