---
title: Fonctionnalités et objets de threading
ms.date: 08/16/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], features
- managed threading
ms.assetid: 239b2e8d-581b-4ca3-992b-0e8525b9321c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2d56d962279120a03a6e4b89154ac1429ea5479e
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "44039327"
---
# <a name="threading-objects-and-features"></a>Fonctionnalités et objets de threading

En plus de la classe <xref:System.Threading.Thread?displayProperty=nameWithType>, .NET fournit plusieurs classes qui facilitent le développement des applications multithread. Les articles suivants présentent ces différentes classes :

|Titre|Description|  
|-----------|-----------------|  
|[Pool de threads managés](the-managed-thread-pool.md)|Décrit la classe <xref:System.Threading.ThreadPool?displayProperty=nameWithType>, qui fournit un pool de threads de travail managés par .NET.|  
|[Minuteries](timers.md)|Décrit les minuteurs qui peuvent être utilisés dans un environnement multithread.|
|[Vue d’ensemble des primitives de synchronisation](overview-of-synchronization-primitives.md)|Décrit les classes qui peuvent être utilisées pour synchroniser l’accès aux données ou contrôler les interactions de threads.|
|[EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)|Décrit les handles d’attente d’événements managés qui sont utilisés pour synchroniser les activités de thread en signalant et en attendant des signaux.|
|[Mutex](mutexes.md)|Décrit comment utiliser un <xref:System.Threading.Mutex?displayProperty=nameWithType> pour synchroniser l’accès à un objet ou créer vos propres mécanismes de synchronisation.|
|[Opérations verrouillées](interlocked-operations.md)|Décrit la classe <xref:System.Threading.Interlocked?displayProperty=nameWithType>, qui fournit des opérations atomiques pour les variables partagées par plusieurs threads.|
|[Verrous de lecteur-writer](reader-writer-locks.md)|Décrit la classe <xref:System.Threading.ReaderWriterLockSlim?displayProperty=nameWithType>, qui fournit une sémantique writer unique/lecteurs multiples.|
|[Semaphore et SemaphoreSlim](semaphore-and-semaphoreslim.md)|Décrit la classe <xref:System.Threading.Semaphore?displayProperty=nameWithType> et explique comment l’utiliser pour contrôler l’accès aux ressources limitées.|
|[Barrier](barrier.md)|Décrit la classe <xref:System.Threading.Barrier?displayProperty=nameWithType> qui implémentent le modèle de cloisonnement pour la coordination des threads dans les opérations planifiées.|
|[SpinLock](spinlock.md)|Décrit la classe <xref:System.Threading.SpinLock?displayProperty=nameWithType>, une alternative légère à la classe <xref:System.Threading.Monitor?displayProperty=nameWithType> pour certains scénarios de bas niveau.|
|[SpinWait](spinwait.md)|Décrit la classe <xref:System.Threading.SpinWait?displayProperty=nameWithType>, une primitive de synchronisation de bas niveau qui exécute une attente active avant d’initialiser une attente basée sur le noyau.|

## <a name="see-also"></a>Voir aussi

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Task?displayProperty=nameWithType>
- [Utilisation des threads et du threading](using-threads-and-threading.md)
- [E/S sur fichier asynchrones](../io/asynchronous-file-i-o.md)
- [Programmation parallèle](../parallel-programming/index.md)
- [La bibliothèque parallèle de tâches](../parallel-programming/task-parallel-library-tpl.md)
