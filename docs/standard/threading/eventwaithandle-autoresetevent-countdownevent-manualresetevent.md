---
title: EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- wait handles
- threading [.NET Framework], EventWaitHandle class
- event wait handles [.NET Framework]
ms.assetid: cd94fc34-ac15-427f-b723-a1240a4fab7d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2f61e614696e731a85a030e34aa4356137d9000d
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44260147"
---
# <a name="eventwaithandle-autoresetevent-countdownevent-manualresetevent"></a><span data-ttu-id="84c78-102">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="84c78-102">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>
<span data-ttu-id="84c78-103">Les handles d’attente d’événements permettent aux threads de synchroniser les activités en se signalant et en attendant les signaux des uns et des autres.</span><span class="sxs-lookup"><span data-stu-id="84c78-103">Event wait handles allow threads to synchronize activities by signaling each other and by waiting on each other's signals.</span></span> <span data-ttu-id="84c78-104">Ces événements de synchronisation s’appuient sur des handles d’attente Win32 et se divisent en deux types : ceux qui se réinitialisent automatiquement et ceux qui sont réinitialisés manuellement.</span><span class="sxs-lookup"><span data-stu-id="84c78-104">These synchronization events are based on Win32 wait handles and can be divided into two types: those that reset automatically when signaled and those that are reset manually.</span></span>  
  
 <span data-ttu-id="84c78-105">Les handles d’attente d’événements sont utiles dans la majorité des scénarios de synchronisation de la classe <xref:System.Threading.Monitor>.</span><span class="sxs-lookup"><span data-stu-id="84c78-105">Event wait handles are useful in many of the same synchronization scenarios as the <xref:System.Threading.Monitor> class.</span></span> <span data-ttu-id="84c78-106">Les handles d’attente d’événement sont souvent plus faciles à utiliser que les méthodes <xref:System.Threading.Monitor.Wait%2A?displayProperty=nameWithType> et <xref:System.Threading.Monitor.Pulse%2A?displayProperty=nameWithType>, et ils offrent un meilleur contrôle du signalement.</span><span class="sxs-lookup"><span data-stu-id="84c78-106">Event wait handles are often easier to use than the <xref:System.Threading.Monitor.Wait%2A?displayProperty=nameWithType> and <xref:System.Threading.Monitor.Pulse%2A?displayProperty=nameWithType> methods, and they offer more control over signaling.</span></span> <span data-ttu-id="84c78-107">Les handles d’attente d’événements nommés peuvent également servir à synchroniser les activités entre les différents processus et domaines d’application, tandis que les moniteurs sont liés localement à un domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="84c78-107">Named event wait handles can also be used to synchronize activities across application domains and processes, whereas monitors are local to an application domain.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="84c78-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="84c78-108">In This Section</span></span>  
 [<span data-ttu-id="84c78-109">EventWaitHandle</span><span class="sxs-lookup"><span data-stu-id="84c78-109">EventWaitHandle</span></span>](../../../docs/standard/threading/eventwaithandle.md)  
 <span data-ttu-id="84c78-110">La classe <xref:System.Threading.EventWaitHandle> peut représenter des événements à réinitialisation automatique ou manuelle et des événements locaux ou des événements système nommés.</span><span class="sxs-lookup"><span data-stu-id="84c78-110">The <xref:System.Threading.EventWaitHandle> class can represent either automatic or manual reset events and either local events or named system events.</span></span>  
  
 [<span data-ttu-id="84c78-111">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="84c78-111">AutoResetEvent</span></span>](../../../docs/standard/threading/autoresetevent.md)  
 <span data-ttu-id="84c78-112">La classe <xref:System.Threading.AutoResetEvent> dérive de la classe <xref:System.Threading.EventWaitHandle> et représente un événement local qui se réinitialise automatiquement.</span><span class="sxs-lookup"><span data-stu-id="84c78-112">The <xref:System.Threading.AutoResetEvent> class derives from <xref:System.Threading.EventWaitHandle> and represents a local event that resets automatically.</span></span>  
  
 [<span data-ttu-id="84c78-113">ManualResetEvent and ManualResetEventSlim</span><span class="sxs-lookup"><span data-stu-id="84c78-113">ManualResetEvent and ManualResetEventSlim</span></span>](../../../docs/standard/threading/manualresetevent-and-manualreseteventslim.md)  
 <span data-ttu-id="84c78-114">La classe <xref:System.Threading.ManualResetEvent> dérive de la classe <xref:System.Threading.EventWaitHandle> et représente un événement local qui doit être réinitialisé manuellement.</span><span class="sxs-lookup"><span data-stu-id="84c78-114">The <xref:System.Threading.ManualResetEvent> class derives from <xref:System.Threading.EventWaitHandle> and represents a local event that must be reset manually.</span></span> <span data-ttu-id="84c78-115">La classe <xref:System.Threading.ManualResetEventSlim> est une version légère et plus rapide qui peut être utilisée pour les événements dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="84c78-115">The <xref:System.Threading.ManualResetEventSlim> class is a lightweight, faster version that can be used for events within the same process.</span></span>  
  
 [<span data-ttu-id="84c78-116">CountdownEvent</span><span class="sxs-lookup"><span data-stu-id="84c78-116">CountdownEvent</span></span>](../../../docs/standard/threading/countdownevent.md)  
 <span data-ttu-id="84c78-117">La classe <xref:System.Threading.CountdownEvent> représente un moyen simple d’implémenter des modèles de parallélisme de type duplication/jointure dans un code qui utilise des handles d’attente.</span><span class="sxs-lookup"><span data-stu-id="84c78-117">The <xref:System.Threading.CountdownEvent> class provides a simplified way to implement fork/join parallelism patterns in code that uses wait handles.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="84c78-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="84c78-118">Related Sections</span></span>  
 [<span data-ttu-id="84c78-119">Descripteurs d’attente</span><span class="sxs-lookup"><span data-stu-id="84c78-119">Wait Handles</span></span>](https://msdn.microsoft.com/library/48d10b6f-5fd7-407c-86ab-0179aef72489)  
 <span data-ttu-id="84c78-120">La classe <xref:System.Threading.WaitHandle> est la classe de base des classes <xref:System.Threading.EventWaitHandle>, <xref:System.Threading.Semaphore> et <xref:System.Threading.Mutex>.</span><span class="sxs-lookup"><span data-stu-id="84c78-120">The <xref:System.Threading.WaitHandle> class is the base class for the <xref:System.Threading.EventWaitHandle>, <xref:System.Threading.Semaphore>, and <xref:System.Threading.Mutex> classes.</span></span> <span data-ttu-id="84c78-121">Elle contient des méthodes statiques telles que <xref:System.Threading.WaitHandle.SignalAndWait%2A> et <xref:System.Threading.WaitHandle.WaitAll%2A> qui sont utiles quand vous travaillez avec tous les types de handles d’attente.</span><span class="sxs-lookup"><span data-stu-id="84c78-121">It contains static methods such as <xref:System.Threading.WaitHandle.SignalAndWait%2A> and <xref:System.Threading.WaitHandle.WaitAll%2A> that are useful when working with all types of wait handles.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84c78-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84c78-122">See also</span></span>

- <xref:System.Threading.EventWaitHandle>  
- <xref:System.Threading.WaitHandle>  
- <xref:System.Threading.AutoResetEvent>  
- <xref:System.Threading.ManualResetEvent>  
- [<span data-ttu-id="84c78-123">Fonctionnalités et objets de threading</span><span class="sxs-lookup"><span data-stu-id="84c78-123">Threading Objects and Features</span></span>](../../../docs/standard/threading/threading-objects-and-features.md)  
- [<span data-ttu-id="84c78-124">Éléments fondamentaux du threading managé</span><span class="sxs-lookup"><span data-stu-id="84c78-124">Managed Threading Basics</span></span>](../../../docs/standard/threading/managed-threading-basics.md)
