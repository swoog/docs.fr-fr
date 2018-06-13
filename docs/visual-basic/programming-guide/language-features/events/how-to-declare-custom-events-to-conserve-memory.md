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
# <a name="how-to-declare-custom-events-to-conserve-memory-visual-basic"></a><span data-ttu-id="792d7-102">Comment : déclarer des événements personnalisés pour économiser la mémoire (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="792d7-102">How to: Declare Custom Events To Conserve Memory (Visual Basic)</span></span>
<span data-ttu-id="792d7-103">Il existe plusieurs circonstances lorsqu’il est important qu’une application conserve son utilisation de la mémoire basse.</span><span class="sxs-lookup"><span data-stu-id="792d7-103">There are several circumstances when it is important that an application keep its memory usage low.</span></span> <span data-ttu-id="792d7-104">Événements personnalisés permettent à l’application d’utiliser la mémoire uniquement pour les événements qu’il gère.</span><span class="sxs-lookup"><span data-stu-id="792d7-104">Custom events allow the application to use memory only for the events that it handles.</span></span>  
  
 <span data-ttu-id="792d7-105">Par défaut, lorsqu’une classe déclare un événement, le compilateur alloue la mémoire pour un champ stocker les informations d’événement.</span><span class="sxs-lookup"><span data-stu-id="792d7-105">By default, when a class declares an event, the compiler allocates memory for a field to store the event information.</span></span> <span data-ttu-id="792d7-106">Si une classe comporte plusieurs événements inutilisés, leur mémoire inutilement.</span><span class="sxs-lookup"><span data-stu-id="792d7-106">If a class has many unused events, they needlessly take up memory.</span></span>  
  
 <span data-ttu-id="792d7-107">Au lieu d’utiliser l’implémentation par défaut d’événements Visual Basic, vous pouvez utiliser des événements personnalisés pour gérer l’utilisation de la mémoire plus attentivement.</span><span class="sxs-lookup"><span data-stu-id="792d7-107">Instead of using the default implementation of events that Visual Basic provides, you can use custom events to manage the memory usage more carefully.</span></span>  
  
## <a name="example"></a><span data-ttu-id="792d7-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="792d7-108">Example</span></span>  
 <span data-ttu-id="792d7-109">Dans cet exemple, la classe utilise une instance de la <xref:System.ComponentModel.EventHandlerList> (classe), stockée dans le `Events` champ pour stocker des informations sur les événements en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="792d7-109">In this example, the class uses one instance of the <xref:System.ComponentModel.EventHandlerList> class, stored in the `Events` field, to store information about the events in use.</span></span> <span data-ttu-id="792d7-110">Le <xref:System.ComponentModel.EventHandlerList> est une classe de liste optimisée conçue pour contenir des délégués.</span><span class="sxs-lookup"><span data-stu-id="792d7-110">The <xref:System.ComponentModel.EventHandlerList> class is an optimized list class designed to hold delegates.</span></span>  
  
 <span data-ttu-id="792d7-111">Tous les événements de la classe utilisent la `Events` champ pour effectuer le suivi des méthodes qui gèrent chaque événement.</span><span class="sxs-lookup"><span data-stu-id="792d7-111">All events in the class use the `Events` field to keep track of what methods are handling each event.</span></span>  
  
 [!code-vb[VbVbalrEvents#22](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-declare-custom-events-to-conserve-memory_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="792d7-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="792d7-112">See Also</span></span>  
 <xref:System.ComponentModel.EventHandlerList>  
 [<span data-ttu-id="792d7-113">Événements</span><span class="sxs-lookup"><span data-stu-id="792d7-113">Events</span></span>](../../../../visual-basic/programming-guide/language-features/events/index.md)  
 [<span data-ttu-id="792d7-114">Guide pratique : déclarer des événements personnalisés pour éviter les blocages</span><span class="sxs-lookup"><span data-stu-id="792d7-114">How to: Declare Custom Events To Avoid Blocking</span></span>](../../../../visual-basic/programming-guide/language-features/events/how-to-declare-custom-events-to-avoid-blocking.md)
