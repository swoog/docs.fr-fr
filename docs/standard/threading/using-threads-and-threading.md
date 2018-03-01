---
title: Utilisation des threads et du threading
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- threading [.NET Framework], about threading
- managed threading
ms.assetid: 9b5ec2cd-121b-4d49-b075-222cf26f2344
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 5bed13950a29cfa787ef8c9eb2608c6d74dfd49f
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="using-threads-and-threading"></a><span data-ttu-id="c4e10-102">Utilisation des threads et du threading</span><span class="sxs-lookup"><span data-stu-id="c4e10-102">Using Threads and Threading</span></span>
<span data-ttu-id="c4e10-103">Les rubriques de cette section décrivent la création et la gestion de threads managés. Elles expliquent également comment passer des données à des threads managés et obtenir des résultats en retour, et comment détruire des threads et gérer une exception <xref:System.Threading.ThreadAbortException>.</span><span class="sxs-lookup"><span data-stu-id="c4e10-103">The topics in this section discuss the creation and management of managed threads, how to pass data to managed threads and get results back, and how to destroy threads and handle a <xref:System.Threading.ThreadAbortException>.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c4e10-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="c4e10-104">In This Section</span></span>  
 [<span data-ttu-id="c4e10-105">Création de threads et passage de données au démarrage</span><span class="sxs-lookup"><span data-stu-id="c4e10-105">Creating Threads and Passing Data at Start Time</span></span>](../../../docs/standard/threading/creating-threads-and-passing-data-at-start-time.md)  
 <span data-ttu-id="c4e10-106">Décrit et illustre la création de threads managés, y compris la façon de passer des données à de nouveaux threads et d’obtenir des données en retour.</span><span class="sxs-lookup"><span data-stu-id="c4e10-106">Discusses and demonstrates the creation of managed threads, including how to pass data to new threads and how to get data back.</span></span>  
  
 [<span data-ttu-id="c4e10-107">Suspension et reprise des threads</span><span class="sxs-lookup"><span data-stu-id="c4e10-107">Pausing and Resuming Threads</span></span>](../../../docs/standard/threading/pausing-and-resuming-threads.md)  
 <span data-ttu-id="c4e10-108">Décrit les conséquences de la suspension et de la reprise de threads managés.</span><span class="sxs-lookup"><span data-stu-id="c4e10-108">Discusses the ramifications of pausing and resuming managed threads.</span></span>  
  
 [<span data-ttu-id="c4e10-109">Détruire de threads</span><span class="sxs-lookup"><span data-stu-id="c4e10-109">Destroying Threads</span></span>](../../../docs/standard/threading/destroying-threads.md)  
 <span data-ttu-id="c4e10-110">Décrit les conséquences de la destruction de threads managés et explique comment gérer une exception <xref:System.Threading.ThreadAbortException>.</span><span class="sxs-lookup"><span data-stu-id="c4e10-110">Discusses the ramifications of destroying managed threads, and how to handle a <xref:System.Threading.ThreadAbortException>.</span></span>  
  
 [<span data-ttu-id="c4e10-111">Planification de threads</span><span class="sxs-lookup"><span data-stu-id="c4e10-111">Scheduling Threads</span></span>](../../../docs/standard/threading/scheduling-threads.md)  
 <span data-ttu-id="c4e10-112">Décrit les priorités des threads et explique comment ils affectent la planification de threads.</span><span class="sxs-lookup"><span data-stu-id="c4e10-112">Discusses thread priorities and how they affect thread scheduling.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="c4e10-113">Référence</span><span class="sxs-lookup"><span data-stu-id="c4e10-113">Reference</span></span>  
 <xref:System.Threading.Thread>  
 <span data-ttu-id="c4e10-114">Fournit la documentation de référence pour la classe <xref:System.Threading.Thread> qui représente un thread managé, qu'elle provienne de code non managé ou qu'elle ait été créée dans une application managée.</span><span class="sxs-lookup"><span data-stu-id="c4e10-114">Provides reference documentation for the <xref:System.Threading.Thread> class, which represents a managed thread, whether it came from unmanaged code or was created in a managed application.</span></span>  
  
 <xref:System.Threading.ThreadStart>  
 <span data-ttu-id="c4e10-115">Fournit la documentation de référence pour le délégué <xref:System.Threading.ThreadStart> qui représente les procédures de thread sans paramètres.</span><span class="sxs-lookup"><span data-stu-id="c4e10-115">Provides reference documentation for the <xref:System.Threading.ThreadStart> delegate that represents parameterless thread procedures.</span></span>  
  
 <xref:System.Threading.ParameterizedThreadStart>  
 <span data-ttu-id="c4e10-116">Fournit un moyen simple de passer des données à une procédure de thread, même sans typage fort.</span><span class="sxs-lookup"><span data-stu-id="c4e10-116">Provides an easy way to pass data to a thread procedure, although without strong typing.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="c4e10-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4e10-117">Related Sections</span></span>  
 [<span data-ttu-id="c4e10-118">Threads et threading</span><span class="sxs-lookup"><span data-stu-id="c4e10-118">Threads and Threading</span></span>](../../../docs/standard/threading/threads-and-threading.md)  
 <span data-ttu-id="c4e10-119">Offre une introduction au threading managé.</span><span class="sxs-lookup"><span data-stu-id="c4e10-119">Provides an introduction to managed threading.</span></span>
