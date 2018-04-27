---
title: Événement &#39; &lt;nom_événement1&gt; &#39; ne peut pas implémenter l’événement &#39; &lt;nom_événement2&gt; &#39; sur l’interface &#39; &lt;interface&gt; &#39; , car leurs types délégués &#39; &lt;delegate1&gt; &#39; et &#39; &lt;delegate2&gt; &#39; ne correspondent pas
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc31423
- bc31423
helpviewer_keywords:
- BC31423
ms.assetid: 2e754b66-5836-48ff-9697-b9c0d7085f18
caps.latest.revision: 6
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 41f5984458eb17db04f20b292a0d80783093dcb4
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="event-39lteventname1gt39-cannot-implement-event-39lteventname2gt39-on-interface-39ltinterfacegt39-because-their-delegate-types-39ltdelegate1gt39-and-39ltdelegate2gt39-do-not-match"></a><span data-ttu-id="ab584-102">Événement &#39; &lt;nom_événement1&gt; &#39; ne peut pas implémenter l’événement &#39; &lt;nom_événement2&gt; &#39; sur l’interface &#39; &lt;interface&gt; &#39; , car leurs types délégués &#39; &lt;delegate1&gt; &#39; et &#39; &lt;delegate2&gt; &#39; ne correspondent pas</span><span class="sxs-lookup"><span data-stu-id="ab584-102">Event &#39;&lt;eventname1&gt;&#39; cannot implement event &#39;&lt;eventname2&gt;&#39; on interface &#39;&lt;interface&gt;&#39; because their delegate types &#39;&lt;delegate1&gt;&#39; and &#39;&lt;delegate2&gt;&#39; do not match</span></span>
<span data-ttu-id="ab584-103">Visual Basic ne peut pas implémenter un événement car le type délégué de l’événement ne correspond pas le type délégué de l’événement dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="ab584-103">Visual Basic cannot implement an event because the delegate type of the event does not match the delegate type of the event in the interface.</span></span> <span data-ttu-id="ab584-104">Cette erreur peut se produire quand vous définissez plusieurs événements dans une interface et essayez ensuite de les implémenter ensemble avec le même événement.</span><span class="sxs-lookup"><span data-stu-id="ab584-104">This error can occur when you define multiple events in an interface and then attempt to implement them together with the same event.</span></span> <span data-ttu-id="ab584-105">Un événement peut implémenter deux événements ou plus seulement si tous les événements implémentés sont déclarés à l’aide de la syntaxe `As` et s’ils spécifient le même type délégué.</span><span class="sxs-lookup"><span data-stu-id="ab584-105">An event can implement two or more events only if all implemented events are declared using the `As` syntax and specify the same delegate type.</span></span>  
  
 <span data-ttu-id="ab584-106">**ID d’erreur :** BC31423</span><span class="sxs-lookup"><span data-stu-id="ab584-106">**Error ID:** BC31423</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ab584-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="ab584-107">To correct this error</span></span>  
  
-   <span data-ttu-id="ab584-108">Implémentez les événements séparément.</span><span class="sxs-lookup"><span data-stu-id="ab584-108">Implement the events separately.</span></span>  
  
     <span data-ttu-id="ab584-109">- ou -</span><span class="sxs-lookup"><span data-stu-id="ab584-109">—or—</span></span>  
  
-   <span data-ttu-id="ab584-110">Définissez les événements dans l’interface à l’aide de la `As` syntaxe et spécifient le même type délégué.</span><span class="sxs-lookup"><span data-stu-id="ab584-110">Define the events in the interface using the `As` syntax and specify the same delegate type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab584-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab584-111">See Also</span></span>  
 [<span data-ttu-id="ab584-112">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="ab584-112">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)  
 [<span data-ttu-id="ab584-113">Delegate (instruction)</span><span class="sxs-lookup"><span data-stu-id="ab584-113">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)  
 [<span data-ttu-id="ab584-114">Événements</span><span class="sxs-lookup"><span data-stu-id="ab584-114">Events</span></span>](../../../visual-basic/programming-guide/language-features/events/index.md)
