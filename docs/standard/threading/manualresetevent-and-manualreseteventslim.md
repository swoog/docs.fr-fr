---
title: ManualResetEvent et ManualResetEventSlim
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], ManualResetEvent class
- ManualResetEvent class, about ManualResetEvent class
ms.assetid: 465fdcf9-ba24-4d8d-a43f-d983b7cb0cc6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c85d0c5c291743c6daac549e15d479fcf332235c
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452821"
---
# <a name="manualresetevent-and-manualreseteventslim"></a><span data-ttu-id="e939d-102">ManualResetEvent et ManualResetEventSlim</span><span class="sxs-lookup"><span data-stu-id="e939d-102">ManualResetEvent and ManualResetEventSlim</span></span>
<span data-ttu-id="e939d-103">La classe <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> représente un événement de descripteur d’attente local qui doit être réinitialisé manuellement après avoir été signalé.</span><span class="sxs-lookup"><span data-stu-id="e939d-103">The <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> class represents a local wait handle event that must be reset manually after it is signaled.</span></span> <span data-ttu-id="e939d-104">Cette classe représente un cas spécial de sa classe de base, <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="e939d-104">This class represents a special case of its base class, <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType>.</span></span> <span data-ttu-id="e939d-105">Consultez la documentation conceptuelle de [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) relative à l’utilisation et aux fonctionnalités des événements de réinitialisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="e939d-105">See the [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) conceptual documentation for the use and features of manual reset events.</span></span>  
  
 <span data-ttu-id="e939d-106">Un <xref:System.Threading.ManualResetEvent> objet reste signalé jusqu'à ce que sa méthode <xref:System.Threading.EventWaitHandle.Reset%2A?displayProperty=nameWithType> soit appelée.</span><span class="sxs-lookup"><span data-stu-id="e939d-106">A <xref:System.Threading.ManualResetEvent> object remains signaled until its <xref:System.Threading.EventWaitHandle.Reset%2A?displayProperty=nameWithType> method is called.</span></span> <span data-ttu-id="e939d-107">Lorsque l’état de l’objet est signalé, un nombre indéterminé de threads en attente, ou de threads attendant l’événement une fois celui-ci signalé, peuvent être libérés.</span><span class="sxs-lookup"><span data-stu-id="e939d-107">Any number of waiting threads, or threads that wait on the event after it has been signaled, can be released while the object's state is signaled.</span></span>
  
 <span data-ttu-id="e939d-108">Dans [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], vous pouvez utiliser la classe <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> pour améliorer les performances lorsque les temps d’attente prévus sont très courts et lorsque l’événement ne franchit aucune limite de processus.</span><span class="sxs-lookup"><span data-stu-id="e939d-108">In the [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], you can use the <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> class for better performance when wait times are expected to be very short, and when the event does not cross a process boundary.</span></span> <span data-ttu-id="e939d-109"><xref:System.Threading.ManualResetEventSlim> utilise la rotation intensive pendant une courte période, tout en attendant la signalisation de l’événement.</span><span class="sxs-lookup"><span data-stu-id="e939d-109"><xref:System.Threading.ManualResetEventSlim> uses busy spinning for a short time while it waits for the event to become signaled.</span></span> <span data-ttu-id="e939d-110">Lorsque les temps d’attente sont courts, la rotation peut s’avérer beaucoup moins coûteuse que les descripteurs d’attente.</span><span class="sxs-lookup"><span data-stu-id="e939d-110">When wait times are short, spinning can be much less expensive than waiting by using wait handles.</span></span> <span data-ttu-id="e939d-111">Toutefois, si l’événement n’est pas signalé pendant une période définie, <xref:System.Threading.ManualResetEventSlim> recourt à une attente de descripteur d’événement classique.</span><span class="sxs-lookup"><span data-stu-id="e939d-111">However, if the event does not become signaled within a certain period of time, <xref:System.Threading.ManualResetEventSlim> resorts to a regular event handle wait.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e939d-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e939d-112">See also</span></span>

- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- [<span data-ttu-id="e939d-113">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="e939d-113">AutoResetEvent</span></span>](autoresetevent.md)  
- [<span data-ttu-id="e939d-114">SpinWait</span><span class="sxs-lookup"><span data-stu-id="e939d-114">SpinWait</span></span>](spinwait.md)  
- [<span data-ttu-id="e939d-115">Semaphore et SemaphoreSlim</span><span class="sxs-lookup"><span data-stu-id="e939d-115">Semaphore and SemaphoreSlim</span></span>](semaphore-and-semaphoreslim.md)
- [<span data-ttu-id="e939d-116">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="e939d-116">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)  
- [<span data-ttu-id="e939d-117">Fonctionnalités et objets de threading</span><span class="sxs-lookup"><span data-stu-id="e939d-117">Threading objects and features</span></span>](threading-objects-and-features.md)  
- [<span data-ttu-id="e939d-118">Thread</span><span class="sxs-lookup"><span data-stu-id="e939d-118">Threading</span></span>](index.md)  
