---
title: Thread.Suspend, Garbage Collection et les points sans risque
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- suspending threads
- safe points
- threading [.NET Framework], suspending
- threading [.NET Framework], garbage collection
- garbage collection, threads
ms.assetid: e8f58e17-2714-4821-802a-f8eb3b2baa62
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fc3af01167fe97b701bdb0c7bc37af02d8e8a77c
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46004177"
---
# <a name="threadsuspend-garbage-collection-and-safe-points"></a><span data-ttu-id="1b345-102">Thread.Suspend, Garbage Collection et les points sans risque</span><span class="sxs-lookup"><span data-stu-id="1b345-102">Thread.Suspend, Garbage Collection, and Safe Points</span></span>
<span data-ttu-id="1b345-103">Quand vous appelez <xref:System.Threading.Thread.Suspend%2A?displayProperty=nameWithType> sur un thread, le système indique qu’une suspension du thread a été demandée et permet au thread de s’exécuter jusqu'à ce qu’il ait atteint un point sans risque avant de suspendre réellement le thread.</span><span class="sxs-lookup"><span data-stu-id="1b345-103">When you call <xref:System.Threading.Thread.Suspend%2A?displayProperty=nameWithType> on a thread, the system notes that a thread suspension has been requested and allows the thread to execute until it has reached a safe point before actually suspending the thread.</span></span> <span data-ttu-id="1b345-104">Un point sans risque pour un thread est un point de son exécution auquel le nettoyage de la mémoire peut être exécuté.</span><span class="sxs-lookup"><span data-stu-id="1b345-104">A safe point for a thread is a point in its execution at which garbage collection can be performed.</span></span>  
  
 <span data-ttu-id="1b345-105">Une fois atteint un point sans risque, le runtime garantit que le thread suspendu ne progressera pas dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="1b345-105">Once a safe point is reached, the runtime guarantees that the suspended thread will not make any further progress in managed code.</span></span> <span data-ttu-id="1b345-106">Un thread s’exécutant en dehors du code managé est toujours sûr pour le nettoyage de la mémoire, et son exécution se poursuit jusqu'à ce qu’il tente de reprendre l’exécution du code managé.</span><span class="sxs-lookup"><span data-stu-id="1b345-106">A thread executing outside managed code is always safe for garbage collection, and its execution continues until it attempts to resume execution of managed code.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1b345-107">Pour effectuer un nettoyage de la mémoire, le runtime doit suspendre tous les threads, sauf celui qui exécute le nettoyage.</span><span class="sxs-lookup"><span data-stu-id="1b345-107">In order to perform a garbage collection, the runtime must suspend all the threads except the thread performing the collection.</span></span> <span data-ttu-id="1b345-108">Chaque thread doit être acheminé vers un point sans risque avant de pouvoir être suspendu.</span><span class="sxs-lookup"><span data-stu-id="1b345-108">Each thread must be brought to a safe point before it can be suspended.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1b345-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b345-109">See also</span></span>

- <xref:System.Threading.Thread>  
- <xref:System.GC>  
- [<span data-ttu-id="1b345-110">Thread</span><span class="sxs-lookup"><span data-stu-id="1b345-110">Threading</span></span>](../../../docs/standard/threading/index.md)  
- [<span data-ttu-id="1b345-111">Gestion automatique de la mémoire</span><span class="sxs-lookup"><span data-stu-id="1b345-111">Automatic Memory Management</span></span>](../../../docs/standard/automatic-memory-management.md)
