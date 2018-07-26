---
title: Événements (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- classes [C#], events
- C# language, events
- events [C#]
ms.assetid: a8e51b22-d294-44fb-9539-0072f06c4cb3
ms.openlocfilehash: 5b844b20ac62b4cbc2a73931eecab95f22b4b1de
ms.sourcegitcommit: 2d8b7488d94101b534ca3e9780b1c1e840233405
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2018
ms.locfileid: "39199441"
---
# <a name="events-c-programming-guide"></a><span data-ttu-id="56688-102">Événements (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="56688-102">Events (C# Programming Guide)</span></span>
<span data-ttu-id="56688-103">Les événements permettent à une [classe](../../../csharp/language-reference/keywords/class.md) ou à un objet de notifier d’autres classes ou objets quand quelque chose de significatif se produit.</span><span class="sxs-lookup"><span data-stu-id="56688-103">Events enable a [class](../../../csharp/language-reference/keywords/class.md) or object to notify other classes or objects when something of interest occurs.</span></span> <span data-ttu-id="56688-104">La classe qui envoie (ou *déclenche*) l’événement est appelée *publieur* et les classes qui reçoivent (ou *gèrent*) l’événement sont appelées *abonnés*.</span><span class="sxs-lookup"><span data-stu-id="56688-104">The class that sends (or *raises*) the event is called the *publisher* and the classes that receive (or *handle*) the event are called *subscribers*.</span></span>  
  
 <span data-ttu-id="56688-105">Dans une application C# Windows Forms ou web classique, vous vous abonnez à des événements déclenchés par des contrôles, comme des boutons et des zones de liste.</span><span class="sxs-lookup"><span data-stu-id="56688-105">In a typical C# Windows Forms or Web application, you subscribe to events raised by controls such as buttons and list boxes.</span></span> <span data-ttu-id="56688-106">Vous pouvez utiliser l’IDE Visual C# pour parcourir les événements publiés par un contrôle et sélectionner ceux que vous voulez gérer.</span><span class="sxs-lookup"><span data-stu-id="56688-106">You can use the Visual C# integrated development environment (IDE) to browse the events that a control publishes and select the ones that you want to handle.</span></span> <span data-ttu-id="56688-107">L’IDE ajoute automatiquement une méthode de gestionnaire d’événements vide et le code pour vous abonner à l’événement.</span><span class="sxs-lookup"><span data-stu-id="56688-107">The IDE automatically adds an empty event handler method and the code to subscribe to the event.</span></span> <span data-ttu-id="56688-108">Pour plus d’informations, consultez [Guide pratique pour s’abonner et annuler l’abonnement à des événements](../../../csharp/programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span><span class="sxs-lookup"><span data-stu-id="56688-108">For more information, see [How to: Subscribe to and Unsubscribe from Events](../../../csharp/programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span></span>  
  
## <a name="events-overview"></a><span data-ttu-id="56688-109">Vue d'ensemble des événements</span><span class="sxs-lookup"><span data-stu-id="56688-109">Events Overview</span></span>  
 <span data-ttu-id="56688-110">Les événements ont les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="56688-110">Events have the following properties:</span></span>  
  
-   <span data-ttu-id="56688-111">Le publieur détermine quand un événement est déclenché ; les abonnés déterminent l’action entreprise en réponse à l’événement.</span><span class="sxs-lookup"><span data-stu-id="56688-111">The publisher determines when an event is raised; the subscribers determine what action is taken in response to the event.</span></span>  
  
-   <span data-ttu-id="56688-112">Un événement peut avoir plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="56688-112">An event can have multiple subscribers.</span></span> <span data-ttu-id="56688-113">Un abonné peut gérer plusieurs événements provenant de plusieurs publieurs.</span><span class="sxs-lookup"><span data-stu-id="56688-113">A subscriber can handle multiple events from multiple publishers.</span></span>  
  
-   <span data-ttu-id="56688-114">Les événements qui n’ont aucun abonné ne sont jamais déclenchés.</span><span class="sxs-lookup"><span data-stu-id="56688-114">Events that have no subscribers are never raised.</span></span>  
  
-   <span data-ttu-id="56688-115">Les événements sont généralement utilisés pour signaler des actions de l’utilisateur, comme les clics de bouton ou les sélections de menu dans les interfaces utilisateur graphiques.</span><span class="sxs-lookup"><span data-stu-id="56688-115">Events are typically used to signal user actions such as button clicks or menu selections in graphical user interfaces.</span></span>  
  
-   <span data-ttu-id="56688-116">Quand un événement a plusieurs abonnés, les gestionnaires d’événements sont appelées de façon synchrone quand un événement est déclenché.</span><span class="sxs-lookup"><span data-stu-id="56688-116">When an event has multiple subscribers, the event handlers are invoked synchronously when an event is raised.</span></span> <span data-ttu-id="56688-117">Pour appeler des événements de façon asynchrone, consultez [Calling Synchronous Methods Asynchronously](../../../../docs/standard/asynchronous-programming-patterns/calling-synchronous-methods-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="56688-117">To invoke events asynchronously, see [Calling Synchronous Methods Asynchronously](../../../../docs/standard/asynchronous-programming-patterns/calling-synchronous-methods-asynchronously.md).</span></span>  
  
-   <span data-ttu-id="56688-118">Dans la bibliothèque de classes [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] , les événements sont basés sur le délégué <xref:System.EventHandler> et la classe de base <xref:System.EventArgs> .</span><span class="sxs-lookup"><span data-stu-id="56688-118">In the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] class library, events are based on the <xref:System.EventHandler> delegate and the <xref:System.EventArgs> base class.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="56688-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56688-119">Related Sections</span></span>  
 <span data-ttu-id="56688-120">Pour plus d'informations, voir :</span><span class="sxs-lookup"><span data-stu-id="56688-120">For more information, see:</span></span>  
  
-   [<span data-ttu-id="56688-121">Guide pratique pour s’abonner et se désabonner d’événements</span><span class="sxs-lookup"><span data-stu-id="56688-121">How to: Subscribe to and Unsubscribe from Events</span></span>](../../../csharp/programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md)  
  
-   [<span data-ttu-id="56688-122">Comment : publier des événements conformes aux indications du .NET Framework</span><span class="sxs-lookup"><span data-stu-id="56688-122">How to: Publish Events that Conform to .NET Framework Guidelines</span></span>](../../../csharp/programming-guide/events/how-to-publish-events-that-conform-to-net-framework-guidelines.md)  
  
-   [<span data-ttu-id="56688-123">Comment : déclencher les événements de la classe de base dans les classes dérivées</span><span class="sxs-lookup"><span data-stu-id="56688-123">How to: Raise Base Class Events in Derived Classes</span></span>](../../../csharp/programming-guide/events/how-to-raise-base-class-events-in-derived-classes.md)  
  
-   [<span data-ttu-id="56688-124">Guide pratique d’implémentation d’événements d’interface</span><span class="sxs-lookup"><span data-stu-id="56688-124">How to:  Implement Interface Events</span></span>](../../../csharp/programming-guide/events/how-to-implement-interface-events.md)  
  
-   [<span data-ttu-id="56688-125">Synchronisation des threads</span><span class="sxs-lookup"><span data-stu-id="56688-125">Thread Synchronization</span></span>](../../../csharp/programming-guide/concepts/threading/thread-synchronization.md)  
  
-   [<span data-ttu-id="56688-126">Comment : utiliser un dictionnaire pour stocker des instances d’événements</span><span class="sxs-lookup"><span data-stu-id="56688-126">How to: Use a Dictionary to Store Event Instances</span></span>](../../../csharp/programming-guide/events/how-to-use-a-dictionary-to-store-event-instances.md)  
  
-   [<span data-ttu-id="56688-127">Comment : implémenter des accesseurs d’événement personnalisés</span><span class="sxs-lookup"><span data-stu-id="56688-127">How to: Implement Custom Event Accessors</span></span>](../../../csharp/programming-guide/events/how-to-implement-custom-event-accessors.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="56688-128">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="56688-128">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="featured-book-chapters"></a><span data-ttu-id="56688-129">Chapitres proposés</span><span class="sxs-lookup"><span data-stu-id="56688-129">Featured Book Chapters</span></span>  
 <span data-ttu-id="56688-130">[Delegates, Events, and Lambda Expressions](https://msdn.microsoft.com/library/orm-9780596516109-03-09.aspx) (Délégués, événements et expressions lambda) dans [C# 3.0 Cookbook, Third Edition: More than 250 solutions for C# 3.0 programmers](https://msdn.microsoft.com/library/orm-9780596516109-03.aspx)</span><span class="sxs-lookup"><span data-stu-id="56688-130">[Delegates, Events, and Lambda Expressions](https://msdn.microsoft.com/library/orm-9780596516109-03-09.aspx) in [C# 3.0 Cookbook, Third Edition: More than 250 solutions for C# 3.0 programmers](https://msdn.microsoft.com/library/orm-9780596516109-03.aspx)</span></span>  
  
 <span data-ttu-id="56688-131">[Delegates and Events](https://msdn.microsoft.com/library/orm-9780596521066-01-17.aspx) dans [Learning C# 3.0: Master the fundamentals of C# 3.0](https://msdn.microsoft.com/library/orm-9780596521066-01.aspx)</span><span class="sxs-lookup"><span data-stu-id="56688-131">[Delegates and Events](https://msdn.microsoft.com/library/orm-9780596521066-01-17.aspx) in [Learning C# 3.0: Master the fundamentals of C# 3.0](https://msdn.microsoft.com/library/orm-9780596521066-01.aspx)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="56688-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56688-132">See Also</span></span>  
 <xref:System.EventHandler>  
 [<span data-ttu-id="56688-133">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="56688-133">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="56688-134">Délégués</span><span class="sxs-lookup"><span data-stu-id="56688-134">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)  
 [<span data-ttu-id="56688-135">Création de gestionnaires d’événements dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="56688-135">Creating Event Handlers in Windows Forms</span></span>](../../../../docs/framework/winforms/creating-event-handlers-in-windows-forms.md)  
 [<span data-ttu-id="56688-136">Programmation multithread avec le modèle asynchrone basé sur les événements</span><span class="sxs-lookup"><span data-stu-id="56688-136">Multithreaded Programming with the Event-based Asynchronous Pattern</span></span>](../../../../docs/standard/asynchronous-programming-patterns/multithreaded-programming-with-the-event-based-asynchronous-pattern.md)
