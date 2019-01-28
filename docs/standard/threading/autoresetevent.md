---
title: AutoResetEvent
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], AutoResetEvent class
- AutoResetEvent class
ms.assetid: 6d39c48d-6b37-4a9b-8631-f2924cfd9c18
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 70af739bdb90a70a1319354b4964c261e432912b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54729955"
---
# <a name="autoresetevent"></a><span data-ttu-id="b367a-102">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="b367a-102">AutoResetEvent</span></span>
<span data-ttu-id="b367a-103">La classe <xref:System.Threading.AutoResetEvent> représente un événement de handle d’attente local qui se réinitialise automatiquement quand il est signalé, après avoir libéré un thread en attente unique.</span><span class="sxs-lookup"><span data-stu-id="b367a-103">The <xref:System.Threading.AutoResetEvent> class represents a local wait handle event that resets automatically when signaled, after releasing a single waiting thread.</span></span> <span data-ttu-id="b367a-104">Cette classe représente un cas spécial de sa classe de base, <xref:System.Threading.EventWaitHandle>.</span><span class="sxs-lookup"><span data-stu-id="b367a-104">This class represents a special case of its base class, <xref:System.Threading.EventWaitHandle>.</span></span> <span data-ttu-id="b367a-105">Consultez la documentation conceptuelle de [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) relative à l’utilisation et aux fonctionnalités des événements de réinitialisation automatique.</span><span class="sxs-lookup"><span data-stu-id="b367a-105">See the [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) conceptual documentation for the use and features of automatic reset events.</span></span>  
  
 <span data-ttu-id="b367a-106">Un objet <xref:System.Threading.AutoResetEvent> est automatiquement réinitialisé à l’état non signalé par le système après la libération d’un thread en attente unique.</span><span class="sxs-lookup"><span data-stu-id="b367a-106">An <xref:System.Threading.AutoResetEvent> object is automatically reset to non-signaled by the system after a single waiting thread has been released.</span></span> <span data-ttu-id="b367a-107">Si aucun thread n’attend, l’état de l’objet d’événement reste signalé.</span><span class="sxs-lookup"><span data-stu-id="b367a-107">If no threads are waiting, the event object's state remains signaled.</span></span>
  
 <span data-ttu-id="b367a-108">Pour obtenir un exemple qui utilise <xref:System.Threading.AutoResetEvent>, consultez <xref:System.Threading.Monitor>.</span><span class="sxs-lookup"><span data-stu-id="b367a-108">For an example that uses <xref:System.Threading.AutoResetEvent>, see <xref:System.Threading.Monitor>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b367a-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b367a-109">See also</span></span>

- <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- [<span data-ttu-id="b367a-110">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="b367a-110">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)
- [<span data-ttu-id="b367a-111">Fonctionnalités et objets de threading</span><span class="sxs-lookup"><span data-stu-id="b367a-111">Threading objects and features</span></span>](threading-objects-and-features.md)
- [<span data-ttu-id="b367a-112">Thread</span><span class="sxs-lookup"><span data-stu-id="b367a-112">Threading</span></span>](index.md)
