---
title: EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent
ms.date: 09/14/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- wait handles
- threading [.NET Framework], EventWaitHandle class
- event wait handles [.NET Framework]
ms.assetid: cd94fc34-ac15-427f-b723-a1240a4fab7d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: be9c858d7c76fdcc1b3e02485eb0b459f4e7555c
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48583150"
---
# <a name="eventwaithandle-autoresetevent-countdownevent-manualresetevent"></a><span data-ttu-id="9406d-102">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="9406d-102">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>

<span data-ttu-id="9406d-103">Les handles d’attente d’événements permettent aux threads de synchroniser les activités en se signalant et en attendant les signaux des uns et des autres.</span><span class="sxs-lookup"><span data-stu-id="9406d-103">Event wait handles allow threads to synchronize activities by signaling each other and by waiting on each other's signals.</span></span> <span data-ttu-id="9406d-104">Ces événements de synchronisation s’appuient sur des handles d’attente de système d’exploitation et se divisent en deux types : ceux qui se réinitialisent automatiquement et ceux qui sont réinitialisés manuellement.</span><span class="sxs-lookup"><span data-stu-id="9406d-104">These synchronization events are based on operating system wait handles and can be divided into two types: those that reset automatically when signaled and those that are reset manually.</span></span>  
  
<span data-ttu-id="9406d-105">Les handles d’attente d’événements sont utiles dans la majorité des scénarios de synchronisation de la classe <xref:System.Threading.Monitor>.</span><span class="sxs-lookup"><span data-stu-id="9406d-105">Event wait handles are useful in many of the same synchronization scenarios as the <xref:System.Threading.Monitor> class.</span></span> <span data-ttu-id="9406d-106">Les handles d’attente d’événement sont souvent plus faciles à utiliser que les méthodes <xref:System.Threading.Monitor.Wait%2A?displayProperty=nameWithType> et <xref:System.Threading.Monitor.Pulse%2A?displayProperty=nameWithType>, et ils offrent un meilleur contrôle du signalement.</span><span class="sxs-lookup"><span data-stu-id="9406d-106">Event wait handles are often easier to use than the <xref:System.Threading.Monitor.Wait%2A?displayProperty=nameWithType> and <xref:System.Threading.Monitor.Pulse%2A?displayProperty=nameWithType> methods, and they offer more control over signaling.</span></span> <span data-ttu-id="9406d-107">Les handles d’attente d’événements nommés peuvent également servir à synchroniser les activités entre les différents processus et domaines d’application, tandis que les moniteurs sont liés localement à un domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="9406d-107">Named event wait handles can also be used to synchronize activities across application domains and processes, whereas monitors are local to an application domain.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="9406d-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9406d-108">In this section</span></span>

 [<span data-ttu-id="9406d-109">EventWaitHandle</span><span class="sxs-lookup"><span data-stu-id="9406d-109">EventWaitHandle</span></span>](eventwaithandle.md)  
 <span data-ttu-id="9406d-110">La classe <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType> peut représenter des événements à réinitialisation automatique ou manuelle et des événements locaux ou des événements système nommés.</span><span class="sxs-lookup"><span data-stu-id="9406d-110">The <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType> class can represent either automatic or manual reset events and either local events or named system events.</span></span>  
  
 [<span data-ttu-id="9406d-111">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="9406d-111">AutoResetEvent</span></span>](autoresetevent.md)  
 <span data-ttu-id="9406d-112">La classe <xref:System.Threading.AutoResetEvent?displayProperty=nameWithType> dérive de la classe <xref:System.Threading.EventWaitHandle> et représente un événement local qui se réinitialise automatiquement.</span><span class="sxs-lookup"><span data-stu-id="9406d-112">The <xref:System.Threading.AutoResetEvent?displayProperty=nameWithType> class derives from <xref:System.Threading.EventWaitHandle> and represents a local event that resets automatically.</span></span>  
  
 [<span data-ttu-id="9406d-113">ManualResetEvent and ManualResetEventSlim</span><span class="sxs-lookup"><span data-stu-id="9406d-113">ManualResetEvent and ManualResetEventSlim</span></span>](manualresetevent-and-manualreseteventslim.md)  
 <span data-ttu-id="9406d-114">La classe <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> dérive de la classe <xref:System.Threading.EventWaitHandle> et représente un événement local qui doit être réinitialisé manuellement.</span><span class="sxs-lookup"><span data-stu-id="9406d-114">The <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> class derives from <xref:System.Threading.EventWaitHandle> and represents a local event that must be reset manually.</span></span> <span data-ttu-id="9406d-115">La classe <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> est une version légère et plus rapide qui peut être utilisée pour les événements dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="9406d-115">The <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> class is a lightweight, faster version that can be used for events within the same process.</span></span>  
  
 [<span data-ttu-id="9406d-116">CountdownEvent</span><span class="sxs-lookup"><span data-stu-id="9406d-116">CountdownEvent</span></span>](countdownevent.md)  
 <span data-ttu-id="9406d-117">La classe <xref:System.Threading.CountdownEvent?displayProperty=nameWithType> représente un moyen simple d’implémenter des modèles de parallélisme de type duplication/jointure dans un code qui utilise des handles d’attente.</span><span class="sxs-lookup"><span data-stu-id="9406d-117">The <xref:System.Threading.CountdownEvent?displayProperty=nameWithType> class provides a simplified way to implement fork/join parallelism patterns in code that uses wait handles.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9406d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9406d-118">See also</span></span>

- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.Threading.Barrier?displayProperty=nameWithType>
- [<span data-ttu-id="9406d-119">Fonctionnalités et objets de threading</span><span class="sxs-lookup"><span data-stu-id="9406d-119">Threading objects and features</span></span>](threading-objects-and-features.md)
- [<span data-ttu-id="9406d-120">Éléments fondamentaux du threading managé</span><span class="sxs-lookup"><span data-stu-id="9406d-120">Managed threading basics</span></span>](managed-threading-basics.md)
