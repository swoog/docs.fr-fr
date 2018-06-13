---
title: Les classes dérivées ne peuvent pas déclencher les événements de la classe de base
ms.date: 07/20/2015
f1_keywords:
- vbc30029
- bc30029
helpviewer_keywords:
- BC30029
ms.assetid: 63afa1c6-2f93-4512-a2f0-372455979771
ms.openlocfilehash: 365ce6ece1d964d3fac2a44f7ed4c1e16f44c95d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33586397"
---
# <a name="derived-classes-cannot-raise-base-class-events"></a><span data-ttu-id="51a90-102">Les classes dérivées ne peuvent pas déclencher les événements de la classe de base</span><span class="sxs-lookup"><span data-stu-id="51a90-102">Derived classes cannot raise base class events</span></span>
<span data-ttu-id="51a90-103">Un événement peut être déclenché uniquement à partir de l’espace de déclaration dans lequel elle est déclarée.</span><span class="sxs-lookup"><span data-stu-id="51a90-103">An event can be raised only from the declaration space in which it is declared.</span></span> <span data-ttu-id="51a90-104">Par conséquent, une classe ne peut pas déclencher d’événements à partir de toute autre classe, même si celle-ci à partir de laquelle elle est dérivée.</span><span class="sxs-lookup"><span data-stu-id="51a90-104">Therefore, a class cannot raise events from any other class, even one from which it is derived.</span></span>  
  
 <span data-ttu-id="51a90-105">**ID d’erreur :** BC30029</span><span class="sxs-lookup"><span data-stu-id="51a90-105">**Error ID:** BC30029</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="51a90-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="51a90-106">To correct this error</span></span>  
  
-   <span data-ttu-id="51a90-107">Déplacer le `Event` instruction ou la `RaiseEvent` instruction afin qu’ils soient dans la même classe.</span><span class="sxs-lookup"><span data-stu-id="51a90-107">Move the `Event` statement or the `RaiseEvent` statement so they are in the same class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51a90-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51a90-108">See Also</span></span>  
 [<span data-ttu-id="51a90-109">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="51a90-109">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)  
 [<span data-ttu-id="51a90-110">RaiseEvent (instruction)</span><span class="sxs-lookup"><span data-stu-id="51a90-110">RaiseEvent Statement</span></span>](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
