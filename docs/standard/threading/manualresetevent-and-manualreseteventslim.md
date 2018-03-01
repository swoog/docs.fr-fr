---
title: ManualResetEvent et ManualResetEventSlim
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- threading [.NET Framework], ManualResetEvent class
- ManualResetEvent class, about ManualResetEvent class
ms.assetid: 465fdcf9-ba24-4d8d-a43f-d983b7cb0cc6
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: b90a84cf87c6c64d48d89840e2213d83b2e39d44
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="manualresetevent-and-manualreseteventslim"></a><span data-ttu-id="5d6e0-102">ManualResetEvent et ManualResetEventSlim</span><span class="sxs-lookup"><span data-stu-id="5d6e0-102">ManualResetEvent and ManualResetEventSlim</span></span>
<span data-ttu-id="5d6e0-103">La classe <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> représente un événement de descripteur d’attente local qui doit être réinitialisé manuellement après avoir été signalé.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-103">The <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> class represents a local wait handle event that must be reset manually after it is signaled.</span></span> <span data-ttu-id="5d6e0-104">Cette classe représente un cas spécial de sa classe de base, <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-104">This class represents a special case of its base class, <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType>.</span></span> <span data-ttu-id="5d6e0-105">Consultez la documentation conceptuelle de [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) relative à l’utilisation et aux fonctionnalités des événements de réinitialisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-105">See the [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) conceptual documentation for the use and features of manual reset events.</span></span>  
  
 <span data-ttu-id="5d6e0-106">Un <xref:System.Threading.ManualResetEvent> objet reste signalé jusqu'à ce que sa méthode <xref:System.Threading.EventWaitHandle.Reset%2A?displayProperty=nameWithType> soit appelée.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-106">A <xref:System.Threading.ManualResetEvent> object remains signaled until its <xref:System.Threading.EventWaitHandle.Reset%2A?displayProperty=nameWithType> method is called.</span></span> <span data-ttu-id="5d6e0-107">Lorsque l’état de l’objet est signalé, un nombre indéterminé de threads en attente, ou de threads attendant l’événement une fois celui-ci signalé, peuvent être libérés.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-107">Any number of waiting threads, or threads that wait on the event after it has been signaled, can be released while the object's state is signaled.</span></span> <span data-ttu-id="5d6e0-108"><xref:System.Threading.ManualResetEvent> correspond à un appel Win32 `CreateEvent` spécifiant `true` pour l’argument `bManualReset`.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-108"><xref:System.Threading.ManualResetEvent> corresponds to a Win32 `CreateEvent` call, specifying `true` for the `bManualReset` argument.</span></span>  
  
 <span data-ttu-id="5d6e0-109">Dans [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], vous pouvez utiliser la classe <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> pour améliorer les performances lorsque les temps d’attente prévus sont très courts et lorsque l’événement ne franchit aucune limite de processus.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-109">In the [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], you can use the <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> class for better performance when wait times are expected to be very short, and when the event does not cross a process boundary.</span></span> <span data-ttu-id="5d6e0-110"><xref:System.Threading.ManualResetEventSlim> utilise la rotation intensive pendant une courte période, tout en attendant la signalisation de l’événement.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-110"><xref:System.Threading.ManualResetEventSlim> uses busy spinning for a short time while it waits for the event to become signaled.</span></span> <span data-ttu-id="5d6e0-111">Lorsque les temps d’attente sont courts, la rotation peut s’avérer beaucoup moins coûteuse que les descripteurs d’attente.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-111">When wait times are short, spinning can be much less expensive than waiting by using wait handles.</span></span> <span data-ttu-id="5d6e0-112">Toutefois, si l’événement n’est pas signalé pendant une période définie, <xref:System.Threading.ManualResetEventSlim> recourt à une attente de descripteur d’événement classique.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-112">However, if the event does not become signaled within a certain period of time, <xref:System.Threading.ManualResetEventSlim> resorts to a regular event handle wait.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5d6e0-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d6e0-113">See Also</span></span>  
 [<span data-ttu-id="5d6e0-114">Thread</span><span class="sxs-lookup"><span data-stu-id="5d6e0-114">Threading</span></span>](../../../docs/standard/threading/index.md)  
 [<span data-ttu-id="5d6e0-115">Fonctionnalités et objets de threading</span><span class="sxs-lookup"><span data-stu-id="5d6e0-115">Threading Objects and Features</span></span>](../../../docs/standard/threading/threading-objects-and-features.md)  
 [<span data-ttu-id="5d6e0-116">Descripteurs d’attente</span><span class="sxs-lookup"><span data-stu-id="5d6e0-116">Wait Handles</span></span>](http://msdn.microsoft.com/library/48d10b6f-5fd7-407c-86ab-0179aef72489)  
 [<span data-ttu-id="5d6e0-117">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="5d6e0-117">AutoResetEvent</span></span>](../../../docs/standard/threading/autoresetevent.md)  
 [<span data-ttu-id="5d6e0-118">SpinWait</span><span class="sxs-lookup"><span data-stu-id="5d6e0-118">SpinWait</span></span>](../../../docs/standard/threading/spinwait.md)  
 [<span data-ttu-id="5d6e0-119">Semaphore et SemaphoreSlim</span><span class="sxs-lookup"><span data-stu-id="5d6e0-119">Semaphore and SemaphoreSlim</span></span>](../../../docs/standard/threading/semaphore-and-semaphoreslim.md)
