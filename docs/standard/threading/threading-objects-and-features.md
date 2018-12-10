---
title: Fonctionnalités et objets de threading
ms.date: 10/01/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], features
- managed threading
ms.assetid: 239b2e8d-581b-4ca3-992b-0e8525b9321c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9a355c2e996ddb00dad804dfeb22987923d91aa6
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53144518"
---
# <a name="threading-objects-and-features"></a>Fonctionnalités et objets de threading

En plus de la classe <xref:System.Threading.Thread?displayProperty=nameWithType>, .NET fournit plusieurs classes qui facilitent le développement des applications multithread. Les articles suivants présentent ces différentes classes :

|Titre|Description|  
|-----------|-----------------|  
|[Pool de threads managés](the-managed-thread-pool.md)|Décrit la classe <xref:System.Threading.ThreadPool?displayProperty=nameWithType>, qui fournit un pool de threads de travail managés par .NET.|  
|[Minuteries](timers.md)|Décrit les minuteurs .NET qui peuvent être utilisés dans un environnement multithread.|
|[Vue d’ensemble des primitives de synchronisation](overview-of-synchronization-primitives.md)|Décrit les types qui peuvent être utilisés pour synchroniser l’accès à une ressource partagée ou contrôler les interactions de threads.|
|[EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)|Décrit les handles d’attente d’événements managés qui sont utilisés pour synchroniser les activités de thread en signalant et en attendant des signaux.|
|[Mutex](mutexes.md)|Décrit <xref:System.Threading.Mutex?displayProperty=nameWithType>, qui accorde un accès exclusif à une ressource partagée.|
|[Semaphore et SemaphoreSlim](semaphore-and-semaphoreslim.md)|Décrit la classe <xref:System.Threading.Semaphore?displayProperty=nameWithType>, qui limite le nombre de threads qui peuvent accéder simultanément à une ressource partagée ou à un pool de ressources.|
|[Barrier](barrier.md)|Décrit la classe <xref:System.Threading.Barrier?displayProperty=nameWithType> qui implémentent le modèle de cloisonnement pour la coordination des threads dans les opérations planifiées.|
|[SpinLock](spinlock.md)|Décrit la structure <xref:System.Threading.SpinLock?displayProperty=nameWithType>, une alternative légère à la classe <xref:System.Threading.Monitor?displayProperty=nameWithType> pour certains scénarios de verrouillage de bas niveau.|
|[SpinWait](spinwait.md)|Décrit la structure <xref:System.Threading.SpinWait?displayProperty=nameWithType>, qui fournit la prise en charge pour l’attente basée sur les spins.|

## <a name="see-also"></a>Voir aussi

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Task?displayProperty=nameWithType>
- [Utilisation des threads et du threading](using-threads-and-threading.md)
- [Asynchronous File I/O](../io/asynchronous-file-i-o.md)
- [Programmation parallèle](../parallel-programming/index.md)
- [La bibliothèque parallèle de tâches](../parallel-programming/task-parallel-library-tpl.md)
