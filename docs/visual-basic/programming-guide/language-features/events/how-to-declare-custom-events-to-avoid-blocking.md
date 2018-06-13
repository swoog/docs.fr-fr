---
title: 'Comment : déclarer des événements personnalisés pour éviter les blocages (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- declaring events [Visual Basic], custom
- events [Visual Basic], custom
- custom events [Visual Basic]
ms.assetid: 998b6a90-67c5-4d2c-8b11-366d3e355505
ms.openlocfilehash: 3cb66aed71195d2fd2335fbd59cc499b3dbf808e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33646924"
---
# <a name="how-to-declare-custom-events-to-avoid-blocking-visual-basic"></a><span data-ttu-id="9c44b-102">Comment : déclarer des événements personnalisés pour éviter les blocages (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9c44b-102">How to: Declare Custom Events To Avoid Blocking (Visual Basic)</span></span>
<span data-ttu-id="9c44b-103">Il existe plusieurs cas où il est important qu’un gestionnaire d’événements ne bloque pas les gestionnaires d’événements suivants.</span><span class="sxs-lookup"><span data-stu-id="9c44b-103">There are several circumstances when it is important that one event handler not block subsequent event handlers.</span></span> <span data-ttu-id="9c44b-104">Événements personnalisés permettent à l’événement à appeler ses gestionnaires d’événements de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="9c44b-104">Custom events allow the event to call its event handlers asynchronously.</span></span>  
  
 <span data-ttu-id="9c44b-105">Par défaut, le champ du magasin de stockage pour une déclaration d’événement est un délégué multicast qui associe en série tous les gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="9c44b-105">By default, the backing-store field for an event declaration is a multicast delegate that serially combines all the event handlers.</span></span> <span data-ttu-id="9c44b-106">Cela signifie que si un gestionnaire met un certain temps, il empêche les autres gestionnaires jusqu'à son achèvement.</span><span class="sxs-lookup"><span data-stu-id="9c44b-106">This means that if one handler takes a long time to complete, it blocks the other handlers until it completes.</span></span> <span data-ttu-id="9c44b-107">(Gestionnaires d’événements valides doivent jamais exécuter les opérations longues ou potentiellement bloquantes).</span><span class="sxs-lookup"><span data-stu-id="9c44b-107">(Well-behaved event handlers should never perform lengthy or potentially blocking operations.)</span></span>  
  
 <span data-ttu-id="9c44b-108">Au lieu d’utiliser l’implémentation par défaut d’événements Visual Basic, vous pouvez utiliser un événement personnalisé à exécuter de façon asynchrone les gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="9c44b-108">Instead of using the default implementation of events that Visual Basic provides, you can use a custom event to execute the event handlers asynchronously.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9c44b-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="9c44b-109">Example</span></span>  
 <span data-ttu-id="9c44b-110">Dans cet exemple, le `AddHandler` accesseur ajoute le délégué pour chaque gestionnaire de la `Click` événement à un <xref:System.Collections.ArrayList> stockés dans le `EventHandlerList` champ.</span><span class="sxs-lookup"><span data-stu-id="9c44b-110">In this example, the `AddHandler` accessor adds the delegate for each handler of the `Click` event to an <xref:System.Collections.ArrayList> stored in the `EventHandlerList` field.</span></span>  
  
 <span data-ttu-id="9c44b-111">Lorsque le code déclenche le `Click` événement, le `RaiseEvent` accesseur appelle tous les délégués de gestionnaires d’événements de façon asynchrone à l’aide de la <xref:System.Web.Services.Protocols.LogicalMethodInfo.BeginInvoke%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="9c44b-111">When code raises the `Click` event, the `RaiseEvent` accessor invokes all the event handler delegates asynchronously using the <xref:System.Web.Services.Protocols.LogicalMethodInfo.BeginInvoke%2A> method.</span></span> <span data-ttu-id="9c44b-112">Cette méthode appelle chaque gestionnaire sur un thread de travail et retourne immédiatement, afin de gestionnaires ne peut pas se bloquer mutuellement.</span><span class="sxs-lookup"><span data-stu-id="9c44b-112">That method invokes each handler on a worker thread and returns immediately, so handlers cannot block one another.</span></span>  
  
 [!code-vb[VbVbalrEvents#27](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-declare-custom-events-to-avoid-blocking_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="9c44b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c44b-113">See Also</span></span>  
 <xref:System.Collections.ArrayList>  
 <xref:System.Web.Services.Protocols.LogicalMethodInfo.BeginInvoke%2A>  
 [<span data-ttu-id="9c44b-114">Événements</span><span class="sxs-lookup"><span data-stu-id="9c44b-114">Events</span></span>](../../../../visual-basic/programming-guide/language-features/events/index.md)  
 [<span data-ttu-id="9c44b-115">Guide pratique : déclarer des événements personnalisés pour économiser la mémoire</span><span class="sxs-lookup"><span data-stu-id="9c44b-115">How to: Declare Custom Events To Conserve Memory</span></span>](../../../../visual-basic/programming-guide/language-features/events/how-to-declare-custom-events-to-conserve-memory.md)
