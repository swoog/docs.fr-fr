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
ms.openlocfilehash: c1785ce223f0dcd4da7ea6ef9fa3a3e897a39dca
ms.sourcegitcommit: dc02d7d95f1e3efcc7166eaf431b0ec0dc9d8dca
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2018
ms.locfileid: "37143516"
---
# <a name="autoresetevent"></a><span data-ttu-id="3d51d-102">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="3d51d-102">AutoResetEvent</span></span>
<span data-ttu-id="3d51d-103">La classe <xref:System.Threading.AutoResetEvent> représente un événement de handle d’attente local qui se réinitialise automatiquement quand il est signalé, après avoir libéré un thread en attente unique.</span><span class="sxs-lookup"><span data-stu-id="3d51d-103">The <xref:System.Threading.AutoResetEvent> class represents a local wait handle event that resets automatically when signaled, after releasing a single waiting thread.</span></span> <span data-ttu-id="3d51d-104">Cette classe représente un cas spécial de sa classe de base, <xref:System.Threading.EventWaitHandle>.</span><span class="sxs-lookup"><span data-stu-id="3d51d-104">This class represents a special case of its base class, <xref:System.Threading.EventWaitHandle>.</span></span> <span data-ttu-id="3d51d-105">Consultez la documentation conceptuelle de [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) relative à l’utilisation et aux fonctionnalités des événements de réinitialisation automatique.</span><span class="sxs-lookup"><span data-stu-id="3d51d-105">See the [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) conceptual documentation for the use and features of automatic reset events.</span></span>  
  
 <span data-ttu-id="3d51d-106">Un objet <xref:System.Threading.AutoResetEvent> est automatiquement réinitialisé à l’état non signalé par le système après la libération d’un thread en attente unique.</span><span class="sxs-lookup"><span data-stu-id="3d51d-106">An <xref:System.Threading.AutoResetEvent> object is automatically reset to non-signaled by the system after a single waiting thread has been released.</span></span> <span data-ttu-id="3d51d-107">Si aucun thread n’attend, l’état de l’objet d’événement reste signalé.</span><span class="sxs-lookup"><span data-stu-id="3d51d-107">If no threads are waiting, the event object's state remains signaled.</span></span> <span data-ttu-id="3d51d-108"><xref:System.Threading.AutoResetEvent> correspond à un appel `CreateEvent` Win32 spécifiant `false` pour l’argument `bManualReset`.</span><span class="sxs-lookup"><span data-stu-id="3d51d-108"><xref:System.Threading.AutoResetEvent> corresponds to a Win32 `CreateEvent` call, specifying `false` for the `bManualReset` argument.</span></span>  
  
 <span data-ttu-id="3d51d-109">Pour obtenir un exemple qui utilise <xref:System.Threading.AutoResetEvent>, consultez <xref:System.Threading.Monitor>.</span><span class="sxs-lookup"><span data-stu-id="3d51d-109">For an example that uses <xref:System.Threading.AutoResetEvent>, see <xref:System.Threading.Monitor>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3d51d-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d51d-110">See Also</span></span>  
 <xref:System.Threading.ManualResetEvent>  
 <xref:System.Threading.Monitor>  
 [<span data-ttu-id="3d51d-111">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="3d51d-111">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>](../../../docs/standard/threading/eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)  
 [<span data-ttu-id="3d51d-112">Thread</span><span class="sxs-lookup"><span data-stu-id="3d51d-112">Threading</span></span>](../../../docs/standard/threading/index.md)  
 [<span data-ttu-id="3d51d-113">Fonctionnalités et objets de threading</span><span class="sxs-lookup"><span data-stu-id="3d51d-113">Threading Objects and Features</span></span>](../../../docs/standard/threading/threading-objects-and-features.md)  
 [<span data-ttu-id="3d51d-114">Descripteurs d’attente</span><span class="sxs-lookup"><span data-stu-id="3d51d-114">Wait Handles</span></span>](http://msdn.microsoft.com/library/48d10b6f-5fd7-407c-86ab-0179aef72489)
