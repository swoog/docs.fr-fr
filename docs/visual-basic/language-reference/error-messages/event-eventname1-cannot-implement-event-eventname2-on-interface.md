---
title: L'événement '<eventname1>' ne peut pas implémenter l'événement '<eventname2>' pour l'interface '<interface>', car leurs types délégués '<delegate1>' et '<delegate2> ne correspondent pas
ms.date: 07/20/2015
f1_keywords:
- vbc31423
- bc31423
helpviewer_keywords:
- BC31423
ms.assetid: 2e754b66-5836-48ff-9697-b9c0d7085f18
ms.openlocfilehash: 3ec3e7bb2f28bf8c4dd38bc71e11193456860021
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57379755"
---
# <a name="event-eventname1-cannot-implement-event-eventname2-on-interface-interface-because-their-delegate-types-delegate1-and-delegate2-do-not-match"></a><span data-ttu-id="54625-102">Événement '\<nom_événement1 >' ne peut pas implémenter l’événement '\<nom_événement2 >' sur l’interface '\<interface >', car leurs types' délégués\<delegate1 >' et '\<delegate2 >' ne correspondent pas</span><span class="sxs-lookup"><span data-stu-id="54625-102">Event '\<eventname1>' cannot implement event '\<eventname2>' on interface '\<interface>' because their delegate types '\<delegate1>' and '\<delegate2>' do not match</span></span>
<span data-ttu-id="54625-103">Visual Basic ne peut pas implémenter un événement, car le type de délégué de l’événement ne correspond pas au type de délégué de l’événement dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="54625-103">Visual Basic cannot implement an event because the delegate type of the event does not match the delegate type of the event in the interface.</span></span> <span data-ttu-id="54625-104">Cette erreur peut se produire quand vous définissez plusieurs événements dans une interface et essayez ensuite de les implémenter ensemble avec le même événement.</span><span class="sxs-lookup"><span data-stu-id="54625-104">This error can occur when you define multiple events in an interface and then attempt to implement them together with the same event.</span></span> <span data-ttu-id="54625-105">Un événement peut implémenter deux événements ou plus seulement si tous les événements implémentés sont déclarés à l’aide de la syntaxe `As` et s’ils spécifient le même type délégué.</span><span class="sxs-lookup"><span data-stu-id="54625-105">An event can implement two or more events only if all implemented events are declared using the `As` syntax and specify the same delegate type.</span></span>  
  
 <span data-ttu-id="54625-106">**ID d’erreur :** BC31423</span><span class="sxs-lookup"><span data-stu-id="54625-106">**Error ID:** BC31423</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="54625-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="54625-107">To correct this error</span></span>  
  
-   <span data-ttu-id="54625-108">Implémentez les événements séparément.</span><span class="sxs-lookup"><span data-stu-id="54625-108">Implement the events separately.</span></span>  
  
     <span data-ttu-id="54625-109">- ou -</span><span class="sxs-lookup"><span data-stu-id="54625-109">—or—</span></span>  
  
-   <span data-ttu-id="54625-110">Définissez les événements dans l’interface à l’aide de la `As` syntaxe et spécifient le même type délégué.</span><span class="sxs-lookup"><span data-stu-id="54625-110">Define the events in the interface using the `As` syntax and specify the same delegate type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="54625-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54625-111">See also</span></span>
- [<span data-ttu-id="54625-112">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="54625-112">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)
- [<span data-ttu-id="54625-113">Delegate (instruction)</span><span class="sxs-lookup"><span data-stu-id="54625-113">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)
- [<span data-ttu-id="54625-114">Événements</span><span class="sxs-lookup"><span data-stu-id="54625-114">Events</span></span>](../../../visual-basic/programming-guide/language-features/events/index.md)
