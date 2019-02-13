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
ms.openlocfilehash: f25609bc3c4dd829c66a1a4514b7f1121f9c0909
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2019
ms.locfileid: "55759026"
---
# <a name="threading-objects-and-features"></a><span data-ttu-id="aca71-102">Fonctionnalités et objets de threading</span><span class="sxs-lookup"><span data-stu-id="aca71-102">Threading objects and features</span></span>

<span data-ttu-id="aca71-103">En plus de la classe <xref:System.Threading.Thread?displayProperty=nameWithType>, .NET fournit plusieurs classes qui facilitent le développement des applications multithread.</span><span class="sxs-lookup"><span data-stu-id="aca71-103">Along with the <xref:System.Threading.Thread?displayProperty=nameWithType> class, .NET provides a number of classes that help you develop multithreaded applications.</span></span> <span data-ttu-id="aca71-104">Les articles suivants présentent ces différentes classes :</span><span class="sxs-lookup"><span data-stu-id="aca71-104">The following articles provide overview of those classes:</span></span>

|<span data-ttu-id="aca71-105">Titre</span><span class="sxs-lookup"><span data-stu-id="aca71-105">Title</span></span>|<span data-ttu-id="aca71-106">Description</span><span class="sxs-lookup"><span data-stu-id="aca71-106">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="aca71-107">Pool de threads managés</span><span class="sxs-lookup"><span data-stu-id="aca71-107">The managed thread pool</span></span>](the-managed-thread-pool.md)|<span data-ttu-id="aca71-108">Décrit la classe <xref:System.Threading.ThreadPool?displayProperty=nameWithType>, qui fournit un pool de threads de travail managés par .NET.</span><span class="sxs-lookup"><span data-stu-id="aca71-108">Describes the <xref:System.Threading.ThreadPool?displayProperty=nameWithType> class, which provides a pool of worker threads that are managed by .NET.</span></span>|  
|[<span data-ttu-id="aca71-109">Minuteries</span><span class="sxs-lookup"><span data-stu-id="aca71-109">Timers</span></span>](timers.md)|<span data-ttu-id="aca71-110">Décrit les minuteurs .NET qui peuvent être utilisés dans un environnement multithread.</span><span class="sxs-lookup"><span data-stu-id="aca71-110">Describes .NET timers that can be used in a multithreaded environment.</span></span>|
|[<span data-ttu-id="aca71-111">Vue d’ensemble des primitives de synchronisation</span><span class="sxs-lookup"><span data-stu-id="aca71-111">Overview of synchronization primitives</span></span>](overview-of-synchronization-primitives.md)|<span data-ttu-id="aca71-112">Décrit les types qui peuvent être utilisés pour synchroniser l’accès à une ressource partagée ou contrôler les interactions de threads.</span><span class="sxs-lookup"><span data-stu-id="aca71-112">Describes types that can be used to synchronize access to a shared resource or control thread interaction.</span></span>|
|[<span data-ttu-id="aca71-113">EventWaitHandle</span><span class="sxs-lookup"><span data-stu-id="aca71-113">EventWaitHandle</span></span>](eventwaithandle.md)|<span data-ttu-id="aca71-114">Décrit la classe <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType>, qui représente un événement de synchronisation de threads.</span><span class="sxs-lookup"><span data-stu-id="aca71-114">Describes the <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType> class, which represents a thread synchronization event.</span></span>|
|[<span data-ttu-id="aca71-115">CountdownEvent</span><span class="sxs-lookup"><span data-stu-id="aca71-115">CountdownEvent</span></span>](countdownevent.md)|<span data-ttu-id="aca71-116">Décrit la classe <xref:System.Threading.CountdownEvent?displayProperty=nameWithType>, qui représente un événement de synchronisation de threads défini quand son nombre est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="aca71-116">Describes the <xref:System.Threading.CountdownEvent?displayProperty=nameWithType> class, which represents a thread synchronization event that becomes set when its count is zero.</span></span>|
|[<span data-ttu-id="aca71-117">Mutex</span><span class="sxs-lookup"><span data-stu-id="aca71-117">Mutexes</span></span>](mutexes.md)|<span data-ttu-id="aca71-118">Décrit la classe <xref:System.Threading.Mutex?displayProperty=nameWithType>, qui accorde un accès exclusif à une ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="aca71-118">Describes the <xref:System.Threading.Mutex?displayProperty=nameWithType> class, which grants exclusive access to a shared resource.</span></span>|
|[<span data-ttu-id="aca71-119">Semaphore et SemaphoreSlim</span><span class="sxs-lookup"><span data-stu-id="aca71-119">Semaphore and SemaphoreSlim</span></span>](semaphore-and-semaphoreslim.md)|<span data-ttu-id="aca71-120">Décrit la classe <xref:System.Threading.Semaphore?displayProperty=nameWithType>, qui limite le nombre de threads qui peuvent accéder simultanément à une ressource partagée ou à un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="aca71-120">Describes the <xref:System.Threading.Semaphore?displayProperty=nameWithType> class, which limits number of threads that can access a shared resource or a pool of resources concurrently.</span></span>|
|[<span data-ttu-id="aca71-121">Barrier</span><span class="sxs-lookup"><span data-stu-id="aca71-121">Barrier</span></span>](barrier.md)|<span data-ttu-id="aca71-122">Décrit la classe <xref:System.Threading.Barrier?displayProperty=nameWithType>, qui implémente le modèle de cloisonnement pour la coordination des threads dans les opérations planifiées.</span><span class="sxs-lookup"><span data-stu-id="aca71-122">Describes the <xref:System.Threading.Barrier?displayProperty=nameWithType> class, which implements the barrier pattern for coordination of threads in phased operations.</span></span>|
|[<span data-ttu-id="aca71-123">SpinLock</span><span class="sxs-lookup"><span data-stu-id="aca71-123">SpinLock</span></span>](spinlock.md)|<span data-ttu-id="aca71-124">Décrit la structure <xref:System.Threading.SpinLock?displayProperty=nameWithType>, une alternative légère à la classe <xref:System.Threading.Monitor?displayProperty=nameWithType> pour certains scénarios de verrouillage de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="aca71-124">Describes the <xref:System.Threading.SpinLock?displayProperty=nameWithType> structure, which is a lightweight alternative to the <xref:System.Threading.Monitor?displayProperty=nameWithType> class for certain low-level locking scenarios.</span></span>|
|[<span data-ttu-id="aca71-125">SpinWait</span><span class="sxs-lookup"><span data-stu-id="aca71-125">SpinWait</span></span>](spinwait.md)|<span data-ttu-id="aca71-126">Décrit la structure <xref:System.Threading.SpinWait?displayProperty=nameWithType>, qui fournit la prise en charge pour l’attente basée sur les spins.</span><span class="sxs-lookup"><span data-stu-id="aca71-126">Describes the <xref:System.Threading.SpinWait?displayProperty=nameWithType> structure, which provides support for spin-based waiting.</span></span>|

## <a name="see-also"></a><span data-ttu-id="aca71-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aca71-127">See also</span></span>

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Task?displayProperty=nameWithType>
- [<span data-ttu-id="aca71-128">Utilisation des threads et du threading</span><span class="sxs-lookup"><span data-stu-id="aca71-128">Using threads and threading</span></span>](using-threads-and-threading.md)
- [<span data-ttu-id="aca71-129">Asynchronous File I/O</span><span class="sxs-lookup"><span data-stu-id="aca71-129">Asynchronous File I/O</span></span>](../io/asynchronous-file-i-o.md)
- [<span data-ttu-id="aca71-130">Programmation parallèle</span><span class="sxs-lookup"><span data-stu-id="aca71-130">Parallel Programming</span></span>](../parallel-programming/index.md)
- [<span data-ttu-id="aca71-131">La bibliothèque parallèle de tâches</span><span class="sxs-lookup"><span data-stu-id="aca71-131">Task Parallel Library (TPL)</span></span>](../parallel-programming/task-parallel-library-tpl.md)
