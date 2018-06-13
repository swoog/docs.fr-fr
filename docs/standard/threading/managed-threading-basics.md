---
title: Éléments fondamentaux du threading managé
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- multiple threads
- threading [.NET Framework], multiple threads
- threading [.NET Framework], about threading
- managed threading
ms.assetid: b2944911-0e8f-427d-a8bb-077550618935
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5fa91bb22de6492815f79bfd50e1fefc800c6047
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33586511"
---
# <a name="managed-threading-basics"></a><span data-ttu-id="aa76c-102">Éléments fondamentaux du threading managé</span><span class="sxs-lookup"><span data-stu-id="aa76c-102">Managed Threading Basics</span></span>
<span data-ttu-id="aa76c-103">Les cinq premières rubriques de cette section sont conçues pour vous aider à déterminer quand utiliser le threading managé et pour expliquer des fonctionnalités de base.</span><span class="sxs-lookup"><span data-stu-id="aa76c-103">The first five topics of this section are designed to help you determine when to use managed threading, and to explain some basic features.</span></span> <span data-ttu-id="aa76c-104">Pour plus d’informations sur les classes qui fournissent des fonctionnalités supplémentaires, consultez [Fonctionnalités et objets de Threading](../../../docs/standard/threading/threading-objects-and-features.md) et [Vue d’ensemble des Primitives de synchronisation](../../../docs/standard/threading/overview-of-synchronization-primitives.md).</span><span class="sxs-lookup"><span data-stu-id="aa76c-104">For information on classes that provide additional features, see [Threading Objects and Features](../../../docs/standard/threading/threading-objects-and-features.md) and [Overview of Synchronization Primitives](../../../docs/standard/threading/overview-of-synchronization-primitives.md).</span></span>  
  
 <span data-ttu-id="aa76c-105">Le reste des rubriques de cette section traitent des sujets avancés, y compris l’interaction du threading managé avec le système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="aa76c-105">The rest of the topics in this section cover advanced topics, including the interaction of managed threading with the Windows operating system.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="aa76c-106">Dans [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], la bibliothèque parallèle de tâches et PLINQ fournissent des API pour le parallélisme des tâches et des données dans les programmes multithreads.</span><span class="sxs-lookup"><span data-stu-id="aa76c-106">In the [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], the Task Parallel Library and PLINQ provide APIs for task and data parallelism in multi-threaded programs.</span></span> <span data-ttu-id="aa76c-107">Pour plus d’informations, consultez la page [Programmation parallèle](../../../docs/standard/parallel-programming/index.md).</span><span class="sxs-lookup"><span data-stu-id="aa76c-107">For more information, see [Parallel Programming](../../../docs/standard/parallel-programming/index.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="aa76c-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="aa76c-108">In This Section</span></span>  
 [<span data-ttu-id="aa76c-109">Threads et threading</span><span class="sxs-lookup"><span data-stu-id="aa76c-109">Threads and Threading</span></span>](../../../docs/standard/threading/threads-and-threading.md)  
 <span data-ttu-id="aa76c-110">Explique les avantages et les inconvénients de plusieurs threads et présente les scénarios dans lesquels vous pouvez créer des threads ou utiliser des threads du pool de threads.</span><span class="sxs-lookup"><span data-stu-id="aa76c-110">Discusses the advantages and drawbacks of multiple threads, and outlines the scenarios in which you might create threads or use thread pool threads.</span></span>  
  
 [<span data-ttu-id="aa76c-111">Exceptions dans les threads managés</span><span class="sxs-lookup"><span data-stu-id="aa76c-111">Exceptions in Managed Threads</span></span>](../../../docs/standard/threading/exceptions-in-managed-threads.md)  
 <span data-ttu-id="aa76c-112">Décrit le comportement des exceptions non prises en charge dans les threads pour différentes versions de .NET Framework, notamment lorsqu’elles entraînent l’arrêt de l’application.</span><span class="sxs-lookup"><span data-stu-id="aa76c-112">Describes the behavior of unhandled exceptions in threads for different versions of the .NET Framework, in particular the situations in which they result in termination of the application.</span></span>  
  
 [<span data-ttu-id="aa76c-113">Synchronisation des données pour le multithreading</span><span class="sxs-lookup"><span data-stu-id="aa76c-113">Synchronizing Data for Multithreading</span></span>](../../../docs/standard/threading/synchronizing-data-for-multithreading.md)  
 <span data-ttu-id="aa76c-114">Décrit les stratégies de synchronisation des données dans des classes qui seront utilisées avec plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="aa76c-114">Describes strategies for synchronizing data in classes that will be used with multiple threads.</span></span>  
  
 [<span data-ttu-id="aa76c-115">États des threads managés</span><span class="sxs-lookup"><span data-stu-id="aa76c-115">Managed Thread States</span></span>](../../../docs/standard/threading/managed-thread-states.md)  
 <span data-ttu-id="aa76c-116">Décrit les états de thread de base et explique comment détecter si un thread est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="aa76c-116">Describes the basic thread states, and explains how to detect whether a thread is running.</span></span>  
  
 [<span data-ttu-id="aa76c-117">Threads de premier plan et d'arrière-plan</span><span class="sxs-lookup"><span data-stu-id="aa76c-117">Foreground and Background Threads</span></span>](../../../docs/standard/threading/foreground-and-background-threads.md)  
 <span data-ttu-id="aa76c-118">Explique les différences entre les threads de premier plan et d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="aa76c-118">Explains the differences between foreground and background threads.</span></span>  
  
 [<span data-ttu-id="aa76c-119">Threading managé et non managé dans Windows</span><span class="sxs-lookup"><span data-stu-id="aa76c-119">Managed and Unmanaged Threading in Windows</span></span>](../../../docs/standard/threading/managed-and-unmanaged-threading-in-windows.md)  
 <span data-ttu-id="aa76c-120">Décrit la relation entre le threading managé et non managé, répertorie les équivalents managés de l’API de threading Windows et explique l’interaction des cloisonnements COM et des threads managés.</span><span class="sxs-lookup"><span data-stu-id="aa76c-120">Discusses the relationship between managed and unmanaged threading, lists managed equivalents for Windows threading APIs, and discusses the interaction of COM apartments and managed threads.</span></span>  
  
 [<span data-ttu-id="aa76c-121">Thread.Suspend, Garbage Collection et les points sans risque</span><span class="sxs-lookup"><span data-stu-id="aa76c-121">Thread.Suspend, Garbage Collection, and Safe Points</span></span>](../../../docs/standard/threading/thread-suspend-garbage-collection-and-safe-points.md)  
 <span data-ttu-id="aa76c-122">Décrit la suspension du thread et le nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="aa76c-122">Describes thread suspension and garbage collection.</span></span>  
  
 [<span data-ttu-id="aa76c-123">Stockage local des threads : champs statiques et emplacements de données relatifs à un thread</span><span class="sxs-lookup"><span data-stu-id="aa76c-123">Thread Local Storage: Thread-Relative Static Fields and Data Slots</span></span>](../../../docs/standard/threading/thread-local-storage-thread-relative-static-fields-and-data-slots.md)  
 <span data-ttu-id="aa76c-124">Décrit les mécanismes de stockage relatifs aux threads.</span><span class="sxs-lookup"><span data-stu-id="aa76c-124">Describes thread-relative storage mechanisms.</span></span>  
  
 [<span data-ttu-id="aa76c-125">Annulation dans les threads managés</span><span class="sxs-lookup"><span data-stu-id="aa76c-125">Cancellation in Managed Threads</span></span>](../../../docs/standard/threading/cancellation-in-managed-threads.md)  
 <span data-ttu-id="aa76c-126">Décrit comment des opérations asynchrones ou des opérations synchrones à long terme peuvent être annulées à l’aide d’un jeton d’annulation.</span><span class="sxs-lookup"><span data-stu-id="aa76c-126">Describes how asynchronous or long-running synchronous operations can be canceled by using a cancellation token.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="aa76c-127">Référence</span><span class="sxs-lookup"><span data-stu-id="aa76c-127">Reference</span></span>  
 <xref:System.Threading.Thread>  
 <span data-ttu-id="aa76c-128">Fournit la documentation de référence pour la classe **Thread** qui représente un thread managé, qu’elle provienne de code non managé ou qu’elle ait été créée dans une application managée.</span><span class="sxs-lookup"><span data-stu-id="aa76c-128">Provides reference documentation for the **Thread** class, which represents a managed thread, whether it came from unmanaged code or was created in a managed application.</span></span>  
  
 <xref:System.ComponentModel.BackgroundWorker>  
 <span data-ttu-id="aa76c-129">Fournit un moyen sûr d’implémenter le multithreading conjointement avec des objets d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aa76c-129">Provides a safe way to implement multithreading in conjunction with user-interface objects.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="aa76c-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa76c-130">Related Sections</span></span>  
 [<span data-ttu-id="aa76c-131">Vue d’ensemble des primitives de synchronisation</span><span class="sxs-lookup"><span data-stu-id="aa76c-131">Overview of Synchronization Primitives</span></span>](../../../docs/standard/threading/overview-of-synchronization-primitives.md)  
 <span data-ttu-id="aa76c-132">Décrit les classes managées utilisées pour synchroniser les activités de plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="aa76c-132">Describes the managed classes used to synchronize the activities of multiple threads.</span></span>  
  
 [<span data-ttu-id="aa76c-133">Bonnes pratiques de threading géré</span><span class="sxs-lookup"><span data-stu-id="aa76c-133">Managed Threading Best Practices</span></span>](../../../docs/standard/threading/managed-threading-best-practices.md)  
 <span data-ttu-id="aa76c-134">Décrit les problèmes courants avec le multithreading et les stratégies pour les éviter.</span><span class="sxs-lookup"><span data-stu-id="aa76c-134">Describes common problems with multithreading and strategies for avoiding problems.</span></span>  
  
 [<span data-ttu-id="aa76c-135">Programmation parallèle</span><span class="sxs-lookup"><span data-stu-id="aa76c-135">Parallel Programming</span></span>](../../../docs/standard/parallel-programming/index.md)  
 <span data-ttu-id="aa76c-136">Décrit la bibliothèque parallèle de tâches et PLINQ, qui simplifient considérablement le travail de création d’applications .NET Framework asynchrones et multithreads.</span><span class="sxs-lookup"><span data-stu-id="aa76c-136">Describes the Task Parallel Library and PLINQ, which greatly simplify the work of creating asynchronous and multi-threaded .NET Framework applications.</span></span>
