---
title: AutoResetEvent
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- threading [.NET Framework], AutoResetEvent class
- AutoResetEvent class
ms.assetid: 6d39c48d-6b37-4a9b-8631-f2924cfd9c18
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 71933d0be804fdf68b0dc602902343f2d88b8c82
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="autoresetevent"></a><span data-ttu-id="aa673-102">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="aa673-102">AutoResetEvent</span></span>
<span data-ttu-id="aa673-103">La classe <xref:System.Threading.AutoResetEvent> représente un événement de handle d’attente local qui se réinitialise automatiquement quand il est signalé, après avoir libéré un thread en attente unique.</span><span class="sxs-lookup"><span data-stu-id="aa673-103">The <xref:System.Threading.AutoResetEvent> class represents a local wait handle event that resets automatically when signaled, after releasing a single waiting thread.</span></span> <span data-ttu-id="aa673-104">Cette classe représente un cas spécial de sa classe de base, <xref:System.Threading.EventWaitHandle>.</span><span class="sxs-lookup"><span data-stu-id="aa673-104">This class represents a special case of its base class, <xref:System.Threading.EventWaitHandle>.</span></span> <span data-ttu-id="aa673-105">Consultez la documentation conceptuelle de [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) relative à l’utilisation et aux fonctionnalités des événements de réinitialisation automatique.</span><span class="sxs-lookup"><span data-stu-id="aa673-105">See the [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) conceptual documentation for the use and features of automatic reset events.</span></span>  
  
 <span data-ttu-id="aa673-106">Un objet <xref:System.Threading.AutoResetEvent> est automatiquement réinitialisé à l’état non signalé par le système après la libération d’un thread en attente unique.</span><span class="sxs-lookup"><span data-stu-id="aa673-106">An <xref:System.Threading.AutoResetEvent> object is automatically reset to non-signaled by the system after a single waiting thread has been released.</span></span> <span data-ttu-id="aa673-107">Si aucun thread n’attend, l’état de l’objet d’événement reste signalé.</span><span class="sxs-lookup"><span data-stu-id="aa673-107">If no threads are waiting, the event object's state remains signaled.</span></span> <span data-ttu-id="aa673-108"><xref:System.Threading.AutoResetEvent> correspond à un appel `CreateEvent` Win32 spécifiant `false` pour l’argument `bManualReset`.</span><span class="sxs-lookup"><span data-stu-id="aa673-108"><xref:System.Threading.AutoResetEvent> corresponds to a Win32 `CreateEvent` call, specifying `false` for the `bManualReset` argument.</span></span>  
  
 <span data-ttu-id="aa673-109">Pour obtenir un exemple utilisant <xref:System.Threading.AutoResetEvent>, consultez [Monitor](http://msdn.microsoft.com/library/33fe4aef-b44b-42fd-9e72-c908e39e75db).</span><span class="sxs-lookup"><span data-stu-id="aa673-109">For an example that uses <xref:System.Threading.AutoResetEvent>, see [Monitor](http://msdn.microsoft.com/library/33fe4aef-b44b-42fd-9e72-c908e39e75db).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa673-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa673-110">See Also</span></span>  
 <xref:System.Threading.ManualResetEvent>  
 <xref:System.Threading.Monitor>  
 [<span data-ttu-id="aa673-111">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="aa673-111">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>](../../../docs/standard/threading/eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)  
 [<span data-ttu-id="aa673-112">Thread</span><span class="sxs-lookup"><span data-stu-id="aa673-112">Threading</span></span>](../../../docs/standard/threading/index.md)  
 [<span data-ttu-id="aa673-113">Fonctionnalités et objets de threading</span><span class="sxs-lookup"><span data-stu-id="aa673-113">Threading Objects and Features</span></span>](../../../docs/standard/threading/threading-objects-and-features.md)  
 [<span data-ttu-id="aa673-114">Descripteurs d’attente</span><span class="sxs-lookup"><span data-stu-id="aa673-114">Wait Handles</span></span>](http://msdn.microsoft.com/library/48d10b6f-5fd7-407c-86ab-0179aef72489)
