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
# <a name="how-to-declare-custom-events-to-conserve-memory-visual-basic"></a><span data-ttu-id="51639-102">Procédure : Déclarer des événements personnalisés pour économiser la mémoire (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="51639-102">How to: Declare Custom Events To Conserve Memory (Visual Basic)</span></span>
<span data-ttu-id="51639-103">Il existe plusieurs circonstances quand il est important qu’une application limiter son utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="51639-103">There are several circumstances when it is important that an application keep its memory usage low.</span></span> <span data-ttu-id="51639-104">Événements personnalisés permettent à l’application pour utiliser la mémoire uniquement pour les événements qu’il gère.</span><span class="sxs-lookup"><span data-stu-id="51639-104">Custom events allow the application to use memory only for the events that it handles.</span></span>  
  
 <span data-ttu-id="51639-105">Par défaut, lorsqu’une classe déclare un événement, le compilateur alloue la mémoire pour un champ stocker les informations d’événement.</span><span class="sxs-lookup"><span data-stu-id="51639-105">By default, when a class declares an event, the compiler allocates memory for a field to store the event information.</span></span> <span data-ttu-id="51639-106">Si une classe comporte plusieurs événements inutilisés, ils mémoire inutilement.</span><span class="sxs-lookup"><span data-stu-id="51639-106">If a class has many unused events, they needlessly take up memory.</span></span>  
  
 <span data-ttu-id="51639-107">Au lieu d’utiliser l’implémentation par défaut d’événements Visual Basic, vous pouvez utiliser des événements personnalisés pour gérer l’utilisation de la mémoire plus attentivement.</span><span class="sxs-lookup"><span data-stu-id="51639-107">Instead of using the default implementation of events that Visual Basic provides, you can use custom events to manage the memory usage more carefully.</span></span>  
  
## <a name="example"></a><span data-ttu-id="51639-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="51639-108">Example</span></span>  
 <span data-ttu-id="51639-109">Dans cet exemple, la classe utilise une instance de la <xref:System.ComponentModel.EventHandlerList> (classe), stockée dans le `Events` champ pour stocker des informations sur les événements en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="51639-109">In this example, the class uses one instance of the <xref:System.ComponentModel.EventHandlerList> class, stored in the `Events` field, to store information about the events in use.</span></span> <span data-ttu-id="51639-110">Le <xref:System.ComponentModel.EventHandlerList> est une classe de liste optimisée conçue pour contenir des délégués.</span><span class="sxs-lookup"><span data-stu-id="51639-110">The <xref:System.ComponentModel.EventHandlerList> class is an optimized list class designed to hold delegates.</span></span>  
  
 <span data-ttu-id="51639-111">Tous les événements de la classe utilisent le `Events` afin de suivre les méthodes qui gèrent chaque événement.</span><span class="sxs-lookup"><span data-stu-id="51639-111">All events in the class use the `Events` field to keep track of what methods are handling each event.</span></span>  
  
 [!code-vb[VbVbalrEvents#22](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-declare-custom-events-to-conserve-memory_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="51639-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51639-112">See also</span></span>
- <xref:System.ComponentModel.EventHandlerList>
- [<span data-ttu-id="51639-113">Événements</span><span class="sxs-lookup"><span data-stu-id="51639-113">Events</span></span>](../../../../visual-basic/programming-guide/language-features/events/index.md)
- [<span data-ttu-id="51639-114">Guide pratique pour Déclarer des événements personnalisés pour éviter les blocages</span><span class="sxs-lookup"><span data-stu-id="51639-114">How to: Declare Custom Events To Avoid Blocking</span></span>](../../../../visual-basic/programming-guide/language-features/events/how-to-declare-custom-events-to-avoid-blocking.md)
