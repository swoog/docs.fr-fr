---
title: Événements ETW de garbage collection
ms.date: 03/30/2017
helpviewer_keywords:
- GC events
- garbage collection events [.NET Framework]
- ETW, garbage collection events (CLR)
ms.assetid: f14b6fd7-0966-4d87-bc89-54ef3a44a94a
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7f9bf0e309ec8c77d4b1d6afbf111e7eeae629ac
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59149732"
---
# <a name="garbage-collection-etw-events"></a><span data-ttu-id="af1b2-102">Événements ETW de garbage collection</span><span class="sxs-lookup"><span data-stu-id="af1b2-102">Garbage Collection ETW Events</span></span>
<a name="top"></a> <span data-ttu-id="af1b2-103">Ces événements collectent des informations relatives au garbage collection.</span><span class="sxs-lookup"><span data-stu-id="af1b2-103">These events collect information pertaining to garbage collection.</span></span> <span data-ttu-id="af1b2-104">Ils vous aident dans le diagnostic et le débogage, y compris pour déterminer combien de fois le garbage collection a été effectué, la quantité de mémoire libérée pendant le garbage collection, etc.</span><span class="sxs-lookup"><span data-stu-id="af1b2-104">They help in diagnostics and debugging, including determining how many times garbage collection was performed, how much memory was freed during garbage collection, and so on.</span></span>  
  
 <span data-ttu-id="af1b2-105">Cette catégorie comprend les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="af1b2-105">This category consists of the following events:</span></span>  
  
-   [<span data-ttu-id="af1b2-106">Événement GCStart_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-106">GCStart_V1 Event</span></span>](#gcstart_v1_event)  
  
-   [<span data-ttu-id="af1b2-107">Événement GCEnd_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-107">GCEnd_V1 Event</span></span>](#gcend_v1_event)  
  
-   [<span data-ttu-id="af1b2-108">Événement GCHeapStats_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-108">GCHeapStats_V1 Event</span></span>](#gcheapstats_v1_event)  
  
-   [<span data-ttu-id="af1b2-109">Événement GCCreateSegment_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-109">GCCreateSegment_V1 Event</span></span>](#gccreatesegment_v1_event)  
  
-   [<span data-ttu-id="af1b2-110">Événement GCFreeSegment_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-110">GCFreeSegment_V1 Event</span></span>](#gcfreesegment_v1_event)  
  
-   [<span data-ttu-id="af1b2-111">Événement GCRestartEEBegin_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-111">GCRestartEEBegin_V1 Event</span></span>](#gcrestarteebegin_v1_event)  
  
-   [<span data-ttu-id="af1b2-112">Événement GCRestartEEEnd_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-112">GCRestartEEEnd_V1 Event</span></span>](#gcrestarteeend_v1_event)  
  
-   [<span data-ttu-id="af1b2-113">Événement GCSuspendEE_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-113">GCSuspendEE_V1 Event</span></span>](#gcsuspendee_v1_event)  
  
-   [<span data-ttu-id="af1b2-114">Événement GCSuspendEEEnd_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-114">GCSuspendEEEnd_V1 Event</span></span>](#gcsuspendeeend_v1_event)  
  
-   [<span data-ttu-id="af1b2-115">Événement GCAllocationTick_V2</span><span class="sxs-lookup"><span data-stu-id="af1b2-115">GCAllocationTick_V2 Event</span></span>](#gcallocationtick_v2_event)  
  
-   [<span data-ttu-id="af1b2-116">Événement GCFinalizersBegin_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-116">GCFinalizersBegin_V1 Event</span></span>](#gcfinalizersbegin_v1_event)  
  
-   [<span data-ttu-id="af1b2-117">Événement GCFinalizersEnd_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-117">GCFinalizersEnd_V1 Event</span></span>](#gcfinalizersend_v1_event)  
  
-   [<span data-ttu-id="af1b2-118">Événement GCCreateConcurrentThread_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-118">GCCreateConcurrentThread_V1 Event</span></span>](#gccreateconcurrentthread_v1_event)  
  
-   [<span data-ttu-id="af1b2-119">Événement GCTerminateConcurrentThread_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-119">GCTerminateConcurrentThread_V1 Event</span></span>](#gcterminateconcurrentthread_v1_event)  
  
<a name="gcstart_v1_event"></a>   
## <a name="gcstartv1-event"></a><span data-ttu-id="af1b2-120">Événement GCStart_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-120">GCStart_V1 Event</span></span>  
 <span data-ttu-id="af1b2-121">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-121">The following table shows the keyword and level.</span></span> <span data-ttu-id="af1b2-122">(Pour plus d'informations, consultez [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span><span class="sxs-lookup"><span data-stu-id="af1b2-122">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="af1b2-123">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-123">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-124">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-124">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-125">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-125">(0x1)</span></span>|<span data-ttu-id="af1b2-126">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-126">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-127">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-127">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="af1b2-128">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-128">Event</span></span>|<span data-ttu-id="af1b2-129">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-129">Event ID</span></span>|<span data-ttu-id="af1b2-130">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="af1b2-130">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCStart_V1`|<span data-ttu-id="af1b2-131">1</span><span class="sxs-lookup"><span data-stu-id="af1b2-131">1</span></span>|<span data-ttu-id="af1b2-132">Un garbage collection a démarré.</span><span class="sxs-lookup"><span data-stu-id="af1b2-132">A garbage collection has started.</span></span>|  
  
 <span data-ttu-id="af1b2-133">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-133">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="af1b2-134">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="af1b2-134">Field name</span></span>|<span data-ttu-id="af1b2-135">Type de données</span><span class="sxs-lookup"><span data-stu-id="af1b2-135">Data type</span></span>|<span data-ttu-id="af1b2-136">Description</span><span class="sxs-lookup"><span data-stu-id="af1b2-136">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="af1b2-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="af1b2-137">Count</span></span>|<span data-ttu-id="af1b2-138">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-138">win:UInt32</span></span>|<span data-ttu-id="af1b2-139">Le *n*ième garbage collection.</span><span class="sxs-lookup"><span data-stu-id="af1b2-139">The *n*th garbage collection.</span></span>|  
|<span data-ttu-id="af1b2-140">Profondeur</span><span class="sxs-lookup"><span data-stu-id="af1b2-140">Depth</span></span>|<span data-ttu-id="af1b2-141">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-141">win:UInt32</span></span>|<span data-ttu-id="af1b2-142">La génération est collectée.</span><span class="sxs-lookup"><span data-stu-id="af1b2-142">The generation that is being collected.</span></span>|  
|<span data-ttu-id="af1b2-143">Raison</span><span class="sxs-lookup"><span data-stu-id="af1b2-143">Reason</span></span>|<span data-ttu-id="af1b2-144">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-144">win:UInt32</span></span>|<span data-ttu-id="af1b2-145">Pourquoi le garbage collection a été déclenché :</span><span class="sxs-lookup"><span data-stu-id="af1b2-145">Why the garbage collection was triggered:</span></span><br /><br /> <span data-ttu-id="af1b2-146">0x0 – Allocation de tas de petits objets.</span><span class="sxs-lookup"><span data-stu-id="af1b2-146">0x0 - Small object heap allocation.</span></span><br /><br /> <span data-ttu-id="af1b2-147">0x1 – Induit.</span><span class="sxs-lookup"><span data-stu-id="af1b2-147">0x1 - Induced.</span></span><br /><br /> <span data-ttu-id="af1b2-148">0x2 – Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="af1b2-148">0x2 - Low memory.</span></span><br /><br /> <span data-ttu-id="af1b2-149">0x3 – Vide.</span><span class="sxs-lookup"><span data-stu-id="af1b2-149">0x3 - Empty.</span></span><br /><br /> <span data-ttu-id="af1b2-150">0x4 – Allocation de tas d'objets volumineux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-150">0x4 - Large object heap allocation.</span></span><br /><br /> <span data-ttu-id="af1b2-151">0x5 – Espace insuffisant (pour un tas de petits objets)</span><span class="sxs-lookup"><span data-stu-id="af1b2-151">0x5 - Out of space (for small object heap).</span></span><br /><br /> <span data-ttu-id="af1b2-152">0x6 – Espace insuffisant (pour un tas d'objets volumineux)</span><span class="sxs-lookup"><span data-stu-id="af1b2-152">0x6 - Out of space (for large object heap).</span></span><br /><br /> <span data-ttu-id="af1b2-153">0x7 – Induit mais non forcé comme blocage</span><span class="sxs-lookup"><span data-stu-id="af1b2-153">0x7 - Induced but not forced as blocking.</span></span>|  
|<span data-ttu-id="af1b2-154">Type</span><span class="sxs-lookup"><span data-stu-id="af1b2-154">Type</span></span>|<span data-ttu-id="af1b2-155">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-155">win:UInt32</span></span>|<span data-ttu-id="af1b2-156">0x0 – Un blocage de garbage collection s'est produit en dehors du garbage collection d'arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="af1b2-156">0x0 - Blocking garbage collection occurred outside background garbage collection.</span></span><br /><br /> <span data-ttu-id="af1b2-157">0x1 – Garbage collection d'arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="af1b2-157">0x1 - Background garbage collection.</span></span><br /><br /> <span data-ttu-id="af1b2-158">0x2 – Un blocage de garbage collection s'est produit pendant le garbage collection d'arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="af1b2-158">0x2 - Blocking garbage collection occurred during background garbage collection.</span></span>|  
|<span data-ttu-id="af1b2-159">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="af1b2-159">ClrInstanceID</span></span>|<span data-ttu-id="af1b2-160">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="af1b2-160">win:UInt16</span></span>|<span data-ttu-id="af1b2-161">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="af1b2-161">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="af1b2-162">Retour au début</span><span class="sxs-lookup"><span data-stu-id="af1b2-162">Back to top</span></span>](#top)  
  
<a name="gcend_v1_event"></a>   
## <a name="gcendv1-event"></a><span data-ttu-id="af1b2-163">Événement GCEnd_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-163">GCEnd_V1 Event</span></span>  
 <span data-ttu-id="af1b2-164">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-164">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="af1b2-165">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-165">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-166">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-166">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-167">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-167">(0x1)</span></span>|<span data-ttu-id="af1b2-168">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-168">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-169">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-169">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="af1b2-170">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-170">Event</span></span>|<span data-ttu-id="af1b2-171">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-171">Event ID</span></span>|<span data-ttu-id="af1b2-172">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="af1b2-172">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCEnd_V1`|<span data-ttu-id="af1b2-173">2</span><span class="sxs-lookup"><span data-stu-id="af1b2-173">2</span></span>|<span data-ttu-id="af1b2-174">Un garbage collection s'est terminé.</span><span class="sxs-lookup"><span data-stu-id="af1b2-174">The garbage collection has ended.</span></span>|  
  
 <span data-ttu-id="af1b2-175">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-175">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="af1b2-176">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="af1b2-176">Field name</span></span>|<span data-ttu-id="af1b2-177">Type de données</span><span class="sxs-lookup"><span data-stu-id="af1b2-177">Data type</span></span>|<span data-ttu-id="af1b2-178">Description</span><span class="sxs-lookup"><span data-stu-id="af1b2-178">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="af1b2-179">Nombre</span><span class="sxs-lookup"><span data-stu-id="af1b2-179">Count</span></span>|<span data-ttu-id="af1b2-180">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-180">win:UInt32</span></span>|<span data-ttu-id="af1b2-181">Le *n*ième garbage collection.</span><span class="sxs-lookup"><span data-stu-id="af1b2-181">The *n*th garbage collection.</span></span>|  
|<span data-ttu-id="af1b2-182">Profondeur</span><span class="sxs-lookup"><span data-stu-id="af1b2-182">Depth</span></span>|<span data-ttu-id="af1b2-183">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-183">win:UInt32</span></span>|<span data-ttu-id="af1b2-184">Génération ayant été collectée.</span><span class="sxs-lookup"><span data-stu-id="af1b2-184">The generation that was collected.</span></span>|  
|<span data-ttu-id="af1b2-185">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="af1b2-185">ClrInstanceID</span></span>|<span data-ttu-id="af1b2-186">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="af1b2-186">win:UInt16</span></span>|<span data-ttu-id="af1b2-187">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="af1b2-187">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="af1b2-188">Retour au début</span><span class="sxs-lookup"><span data-stu-id="af1b2-188">Back to top</span></span>](#top)  
  
<a name="gcheapstats_v1_event"></a>   
## <a name="gcheapstatsv1-event"></a><span data-ttu-id="af1b2-189">Événement GCHeapStats_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-189">GCHeapStats_V1 Event</span></span>  
 <span data-ttu-id="af1b2-190">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-190">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="af1b2-191">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-191">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-192">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-192">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-193">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-193">(0x1)</span></span>|<span data-ttu-id="af1b2-194">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-194">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-195">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-195">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="af1b2-196">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-196">Event</span></span>|<span data-ttu-id="af1b2-197">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-197">Event ID</span></span>|<span data-ttu-id="af1b2-198">Description</span><span class="sxs-lookup"><span data-stu-id="af1b2-198">Description</span></span>|  
|-----------|--------------|-----------------|  
|`GCHeapStats_V1`|<span data-ttu-id="af1b2-199">4</span><span class="sxs-lookup"><span data-stu-id="af1b2-199">4</span></span>|<span data-ttu-id="af1b2-200">Affiche les statistiques relatives aux tas à la fin de chaque garbage collection.</span><span class="sxs-lookup"><span data-stu-id="af1b2-200">Shows the heap statistics at the end of each garbage collection.</span></span>|  
  
 <span data-ttu-id="af1b2-201">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-201">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="af1b2-202">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="af1b2-202">Field name</span></span>|<span data-ttu-id="af1b2-203">Type de données</span><span class="sxs-lookup"><span data-stu-id="af1b2-203">Data type</span></span>|<span data-ttu-id="af1b2-204">Description</span><span class="sxs-lookup"><span data-stu-id="af1b2-204">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="af1b2-205">GenerationSize0</span><span class="sxs-lookup"><span data-stu-id="af1b2-205">GenerationSize0</span></span>|<span data-ttu-id="af1b2-206">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-206">win:UInt64</span></span>|<span data-ttu-id="af1b2-207">Taille, en octets, de la mémoire de génération 0.</span><span class="sxs-lookup"><span data-stu-id="af1b2-207">The size, in bytes, of generation 0 memory.</span></span>|  
|<span data-ttu-id="af1b2-208">TotalPromotedSize0</span><span class="sxs-lookup"><span data-stu-id="af1b2-208">TotalPromotedSize0</span></span>|<span data-ttu-id="af1b2-209">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-209">win:UInt64</span></span>|<span data-ttu-id="af1b2-210">Nombre d'octets promus de la génération 0 à la génération 1.</span><span class="sxs-lookup"><span data-stu-id="af1b2-210">The number of bytes that are promoted from generation 0 to generation 1.</span></span>|  
|<span data-ttu-id="af1b2-211">GenerationSize1</span><span class="sxs-lookup"><span data-stu-id="af1b2-211">GenerationSize1</span></span>|<span data-ttu-id="af1b2-212">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-212">win:UInt64</span></span>|<span data-ttu-id="af1b2-213">Taille, en octets, de la mémoire de génération 1.</span><span class="sxs-lookup"><span data-stu-id="af1b2-213">The size, in bytes, of generation 1 memory.</span></span>|  
|<span data-ttu-id="af1b2-214">TotalPromotedSize1</span><span class="sxs-lookup"><span data-stu-id="af1b2-214">TotalPromotedSize1</span></span>|<span data-ttu-id="af1b2-215">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-215">win:UInt64</span></span>|<span data-ttu-id="af1b2-216">Nombre d'octets promus de la génération 1 à la génération 2.</span><span class="sxs-lookup"><span data-stu-id="af1b2-216">The number of bytes that are promoted from generation 1 to generation 2.</span></span>|  
|<span data-ttu-id="af1b2-217">GenerationSize2</span><span class="sxs-lookup"><span data-stu-id="af1b2-217">GenerationSize2</span></span>|<span data-ttu-id="af1b2-218">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-218">win:UInt64</span></span>|<span data-ttu-id="af1b2-219">Taille, en octets, de la mémoire de génération 2.</span><span class="sxs-lookup"><span data-stu-id="af1b2-219">The size, in bytes, of generation 2 memory.</span></span>|  
|<span data-ttu-id="af1b2-220">TotalPromotedSize2</span><span class="sxs-lookup"><span data-stu-id="af1b2-220">TotalPromotedSize2</span></span>|<span data-ttu-id="af1b2-221">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-221">win:UInt64</span></span>|<span data-ttu-id="af1b2-222">Nombre d'octets ayant survécu dans la génération 2 après la dernière collection.</span><span class="sxs-lookup"><span data-stu-id="af1b2-222">The number of bytes that survived in generation 2 after the last collection.</span></span>|  
|<span data-ttu-id="af1b2-223">GenerationSize3</span><span class="sxs-lookup"><span data-stu-id="af1b2-223">GenerationSize3</span></span>|<span data-ttu-id="af1b2-224">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-224">win:UInt64</span></span>|<span data-ttu-id="af1b2-225">Taille, en octets, du tas des objets volumineux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-225">The size, in bytes, of the large object heap.</span></span>|  
|<span data-ttu-id="af1b2-226">TotalPromotedSize3</span><span class="sxs-lookup"><span data-stu-id="af1b2-226">TotalPromotedSize3</span></span>|<span data-ttu-id="af1b2-227">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-227">win:UInt64</span></span>|<span data-ttu-id="af1b2-228">Nombre d'octets ayant survécu dans le tas d'objets volumineux après la dernière collection.</span><span class="sxs-lookup"><span data-stu-id="af1b2-228">The number of bytes that survived in the large object heap after the last collection.</span></span>|  
|<span data-ttu-id="af1b2-229">FinalizationPromotedSize</span><span class="sxs-lookup"><span data-stu-id="af1b2-229">FinalizationPromotedSize</span></span>|<span data-ttu-id="af1b2-230">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-230">win:UInt64</span></span>|<span data-ttu-id="af1b2-231">Taille totale, en octets, des objets qui sont prêts pour la finalisation.</span><span class="sxs-lookup"><span data-stu-id="af1b2-231">The total size, in bytes, of the objects that are ready for finalization.</span></span>|  
|<span data-ttu-id="af1b2-232">FinalizationPromotedSize</span><span class="sxs-lookup"><span data-stu-id="af1b2-232">FinalizationPromotedCount</span></span>|<span data-ttu-id="af1b2-233">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-233">win:UInt64</span></span>|<span data-ttu-id="af1b2-234">Nombre d'objets qui sont prêts pour la finalisation.</span><span class="sxs-lookup"><span data-stu-id="af1b2-234">The number of objects that are ready for finalization.</span></span>|  
|<span data-ttu-id="af1b2-235">PinnedObjectCount</span><span class="sxs-lookup"><span data-stu-id="af1b2-235">PinnedObjectCount</span></span>|<span data-ttu-id="af1b2-236">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-236">win:UInt32</span></span>|<span data-ttu-id="af1b2-237">Nombre d'objets (non déplaçables) épinglés.</span><span class="sxs-lookup"><span data-stu-id="af1b2-237">The number of pinned (unmovable) objects.</span></span>|  
|<span data-ttu-id="af1b2-238">SinkBlockCount</span><span class="sxs-lookup"><span data-stu-id="af1b2-238">SinkBlockCount</span></span>|<span data-ttu-id="af1b2-239">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-239">win:UInt32</span></span>|<span data-ttu-id="af1b2-240">Nombre de blocs de synchronisation en cours d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="af1b2-240">The number of synchronization blocks in use.</span></span>|  
|<span data-ttu-id="af1b2-241">GCHandleCount</span><span class="sxs-lookup"><span data-stu-id="af1b2-241">GCHandleCount</span></span>|<span data-ttu-id="af1b2-242">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-242">win:UInt32</span></span>|<span data-ttu-id="af1b2-243">Nombre de handles de garbage collection en cours d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="af1b2-243">The number of garbage collection handles in use.</span></span>|  
|<span data-ttu-id="af1b2-244">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="af1b2-244">ClrInstanceID</span></span>|<span data-ttu-id="af1b2-245">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="af1b2-245">win:UInt16</span></span>|<span data-ttu-id="af1b2-246">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="af1b2-246">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="af1b2-247">Retour au début</span><span class="sxs-lookup"><span data-stu-id="af1b2-247">Back to top</span></span>](#top)  
  
<a name="gccreatesegment_v1_event"></a>   
## <a name="gccreatesegmentv1-event"></a><span data-ttu-id="af1b2-248">Événement GCCreateSegment_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-248">GCCreateSegment_V1 Event</span></span>  
 <span data-ttu-id="af1b2-249">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-249">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="af1b2-250">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-250">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-251">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-251">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-252">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-252">(0x1)</span></span>|<span data-ttu-id="af1b2-253">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-253">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-254">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-254">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="af1b2-255">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-255">Event</span></span>|<span data-ttu-id="af1b2-256">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-256">Event ID</span></span>|<span data-ttu-id="af1b2-257">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="af1b2-257">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCCreateSegment_V1`|<span data-ttu-id="af1b2-258">5</span><span class="sxs-lookup"><span data-stu-id="af1b2-258">5</span></span>|<span data-ttu-id="af1b2-259">Un nouveau segment de garbage collection a été créé.</span><span class="sxs-lookup"><span data-stu-id="af1b2-259">A new garbage collection segment has been created.</span></span> <span data-ttu-id="af1b2-260">En outre, quand le suivi est activé sur un processus en cours d'exécution, cet événement est déclenché pour chaque segment existant.</span><span class="sxs-lookup"><span data-stu-id="af1b2-260">In addition, when tracing is enabled on a process that is already running, this event is raised for each existing segment.</span></span>|  
  
 <span data-ttu-id="af1b2-261">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-261">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="af1b2-262">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="af1b2-262">Field name</span></span>|<span data-ttu-id="af1b2-263">Type de données</span><span class="sxs-lookup"><span data-stu-id="af1b2-263">Data type</span></span>|<span data-ttu-id="af1b2-264">Description</span><span class="sxs-lookup"><span data-stu-id="af1b2-264">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="af1b2-265">Adresse</span><span class="sxs-lookup"><span data-stu-id="af1b2-265">Address</span></span>|<span data-ttu-id="af1b2-266">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-266">win:UInt64</span></span>|<span data-ttu-id="af1b2-267">Adresse du segment.</span><span class="sxs-lookup"><span data-stu-id="af1b2-267">The address of the segment.</span></span>|  
|<span data-ttu-id="af1b2-268">Taille</span><span class="sxs-lookup"><span data-stu-id="af1b2-268">Size</span></span>|<span data-ttu-id="af1b2-269">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-269">win:UInt64</span></span>|<span data-ttu-id="af1b2-270">Taille du segment.</span><span class="sxs-lookup"><span data-stu-id="af1b2-270">The size of the segment.</span></span>|  
|<span data-ttu-id="af1b2-271">Type</span><span class="sxs-lookup"><span data-stu-id="af1b2-271">Type</span></span>|<span data-ttu-id="af1b2-272">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-272">win:UInt32</span></span>|<span data-ttu-id="af1b2-273">0x0 – Tas de petits objets.</span><span class="sxs-lookup"><span data-stu-id="af1b2-273">0x0 - Small object heap.</span></span><br /><br /> <span data-ttu-id="af1b2-274">0x1 – Tas d'objets volumineux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-274">0x1 - Large object heap.</span></span><br /><br /> <span data-ttu-id="af1b2-275">0x2 – Tas en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="af1b2-275">0x2 - Read-only heap.</span></span>|  
|<span data-ttu-id="af1b2-276">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="af1b2-276">ClrInstanceID</span></span>|<span data-ttu-id="af1b2-277">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="af1b2-277">win:UInt16</span></span>|<span data-ttu-id="af1b2-278">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="af1b2-278">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 <span data-ttu-id="af1b2-279">Notez que la taille des segments alloués par le garbage collector est spécifique à l'implémentation et susceptible de changer à tout moment, y compris lors des mises à jour périodiques.</span><span class="sxs-lookup"><span data-stu-id="af1b2-279">Note that the size of segments allocated by the garbage collector is implementation-specific and is subject to change at any time, including in periodic updates.</span></span> <span data-ttu-id="af1b2-280">Votre application ne doit jamais faire d'hypothèses concernant une taille de segment particulière, ni dépendre de celle-ci. Elle ne doit pas non plus tenter de configurer la quantité de mémoire disponible pour les allocations de segments.</span><span class="sxs-lookup"><span data-stu-id="af1b2-280">Your app should never make assumptions about or depend on a particular segment size, nor should it attempt to configure the amount of memory available for segment allocations.</span></span>  
  
 [<span data-ttu-id="af1b2-281">Retour au début</span><span class="sxs-lookup"><span data-stu-id="af1b2-281">Back to top</span></span>](#top)  
  
<a name="gcfreesegment_v1_event"></a>   
## <a name="gcfreesegmentv1-event"></a><span data-ttu-id="af1b2-282">Événement GCFreeSegment_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-282">GCFreeSegment_V1 Event</span></span>  
 <span data-ttu-id="af1b2-283">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-283">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="af1b2-284">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-284">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-285">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-285">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-286">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-286">(0x1)</span></span>|<span data-ttu-id="af1b2-287">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-287">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-288">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-288">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="af1b2-289">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-289">Event</span></span>|<span data-ttu-id="af1b2-290">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-290">Event ID</span></span>|<span data-ttu-id="af1b2-291">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="af1b2-291">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCFreeSegment_V1`|<span data-ttu-id="af1b2-292">6</span><span class="sxs-lookup"><span data-stu-id="af1b2-292">6</span></span>|<span data-ttu-id="af1b2-293">Un nouveau segment de garbage collection a été libéré.</span><span class="sxs-lookup"><span data-stu-id="af1b2-293">A garbage collection segment has been released.</span></span>|  
  
 <span data-ttu-id="af1b2-294">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-294">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="af1b2-295">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="af1b2-295">Field name</span></span>|<span data-ttu-id="af1b2-296">Type de données</span><span class="sxs-lookup"><span data-stu-id="af1b2-296">Data type</span></span>|<span data-ttu-id="af1b2-297">Description</span><span class="sxs-lookup"><span data-stu-id="af1b2-297">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="af1b2-298">Adresse</span><span class="sxs-lookup"><span data-stu-id="af1b2-298">Address</span></span>|<span data-ttu-id="af1b2-299">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-299">win:UInt64</span></span>|<span data-ttu-id="af1b2-300">Adresse du segment.</span><span class="sxs-lookup"><span data-stu-id="af1b2-300">The address of the segment.</span></span>|  
|<span data-ttu-id="af1b2-301">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="af1b2-301">ClrInstanceID</span></span>|<span data-ttu-id="af1b2-302">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="af1b2-302">win:UInt16</span></span>|<span data-ttu-id="af1b2-303">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="af1b2-303">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="af1b2-304">Retour au début</span><span class="sxs-lookup"><span data-stu-id="af1b2-304">Back to top</span></span>](#top)  
  
<a name="gcrestarteebegin_v1_event"></a>   
## <a name="gcrestarteebeginv1-event"></a><span data-ttu-id="af1b2-305">Événement GCRestartEEBegin_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-305">GCRestartEEBegin_V1 Event</span></span>  
 <span data-ttu-id="af1b2-306">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-306">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="af1b2-307">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-307">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-308">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-308">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-309">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-309">(0x1)</span></span>|<span data-ttu-id="af1b2-310">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-310">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-311">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-311">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="af1b2-312">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-312">Event</span></span>|<span data-ttu-id="af1b2-313">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-313">Event ID</span></span>|<span data-ttu-id="af1b2-314">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="af1b2-314">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCRestartEEBegin_V1`|<span data-ttu-id="af1b2-315">7</span><span class="sxs-lookup"><span data-stu-id="af1b2-315">7</span></span>|<span data-ttu-id="af1b2-316">La reprise du common language runtime après sa suspension a commencé.</span><span class="sxs-lookup"><span data-stu-id="af1b2-316">Resumption from common language runtime suspension has begun.</span></span>|  
  
 <span data-ttu-id="af1b2-317">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="af1b2-317">No event data.</span></span>  
  
 [<span data-ttu-id="af1b2-318">Retour au début</span><span class="sxs-lookup"><span data-stu-id="af1b2-318">Back to top</span></span>](#top)  
  
<a name="gcrestarteeend_v1_event"></a>   
## <a name="gcrestarteeendv1-event"></a><span data-ttu-id="af1b2-319">Événement GCRestartEEEnd_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-319">GCRestartEEEnd_V1 Event</span></span>  
 <span data-ttu-id="af1b2-320">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-320">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="af1b2-321">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-321">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-322">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-322">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-323">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-323">(0x1)</span></span>|<span data-ttu-id="af1b2-324">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-324">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-325">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-325">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="af1b2-326">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-326">Event</span></span>|<span data-ttu-id="af1b2-327">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-327">Event Id</span></span>|<span data-ttu-id="af1b2-328">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="af1b2-328">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCRestartEEEnd_V1`|<span data-ttu-id="af1b2-329">3</span><span class="sxs-lookup"><span data-stu-id="af1b2-329">3</span></span>|<span data-ttu-id="af1b2-330">La reprise du common language runtime après sa suspension s'est terminée.</span><span class="sxs-lookup"><span data-stu-id="af1b2-330">Resumption from common language runtime suspension has ended.</span></span>|  
  
 <span data-ttu-id="af1b2-331">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="af1b2-331">No event data.</span></span>  
  
 [<span data-ttu-id="af1b2-332">Retour au début</span><span class="sxs-lookup"><span data-stu-id="af1b2-332">Back to top</span></span>](#top)  
  
<a name="gcsuspendee_v1_event"></a>   
## <a name="gcsuspendeev1-event"></a><span data-ttu-id="af1b2-333">Événement GCSuspendEE_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-333">GCSuspendEE_V1 Event</span></span>  
 <span data-ttu-id="af1b2-334">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-334">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="af1b2-335">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-335">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-336">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-336">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-337">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-337">(0x1)</span></span>|<span data-ttu-id="af1b2-338">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-338">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-339">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-339">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="af1b2-340">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-340">Event</span></span>|<span data-ttu-id="af1b2-341">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-341">Event ID</span></span>|<span data-ttu-id="af1b2-342">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="af1b2-342">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCSuspendEE_V1`|<span data-ttu-id="af1b2-343">9</span><span class="sxs-lookup"><span data-stu-id="af1b2-343">9</span></span>|<span data-ttu-id="af1b2-344">Début de la suspension du moteur d'exécution pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="af1b2-344">Start of suspension of the execution engine for garbage collection.</span></span>|  
  
 <span data-ttu-id="af1b2-345">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-345">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="af1b2-346">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="af1b2-346">Field name</span></span>|<span data-ttu-id="af1b2-347">Type de données</span><span class="sxs-lookup"><span data-stu-id="af1b2-347">Data type</span></span>|<span data-ttu-id="af1b2-348">Description</span><span class="sxs-lookup"><span data-stu-id="af1b2-348">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="af1b2-349">Raison</span><span class="sxs-lookup"><span data-stu-id="af1b2-349">Reason</span></span>|<span data-ttu-id="af1b2-350">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="af1b2-350">win:UInt16</span></span>|<span data-ttu-id="af1b2-351">0x0 – Autre.</span><span class="sxs-lookup"><span data-stu-id="af1b2-351">0x0 - Other.</span></span><br /><br /> <span data-ttu-id="af1b2-352">0x1 – Garbage collection.</span><span class="sxs-lookup"><span data-stu-id="af1b2-352">0x1 - Garbage collection.</span></span><br /><br /> <span data-ttu-id="af1b2-353">0x2 – Fermeture du domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="af1b2-353">0x2 - Application domain shutdown.</span></span><br /><br /> <span data-ttu-id="af1b2-354">0x3 – Pitching de code.</span><span class="sxs-lookup"><span data-stu-id="af1b2-354">0x3 - Code pitching.</span></span><br /><br /> <span data-ttu-id="af1b2-355">0x4 – Arrêt.</span><span class="sxs-lookup"><span data-stu-id="af1b2-355">0x4 - Shutdown.</span></span><br /><br /> <span data-ttu-id="af1b2-356">0x5 – Débogueur.</span><span class="sxs-lookup"><span data-stu-id="af1b2-356">0x5 - Debugger.</span></span><br /><br /> <span data-ttu-id="af1b2-357">0x6 – Préparation pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="af1b2-357">0x6 - Preparation for garbage collection.</span></span>|  
|<span data-ttu-id="af1b2-358">Nombre</span><span class="sxs-lookup"><span data-stu-id="af1b2-358">Count</span></span>|<span data-ttu-id="af1b2-359">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-359">win:UInt32</span></span>|<span data-ttu-id="af1b2-360">Nombre GC à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="af1b2-360">The GC count at the time.</span></span> <span data-ttu-id="af1b2-361">En règle générale, vous verrez un événement de démarrage de GC par la suite et son nombre doit être égal à ce nombre + 1 à mesure que nous augmentons l’index GC pendant un garbage collection.</span><span class="sxs-lookup"><span data-stu-id="af1b2-361">Usually, you would see a subsequent GC Start event after this, and its Count would be this Count + 1 as we increase the GC index during a garbage collection.</span></span>|  
|<span data-ttu-id="af1b2-362">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="af1b2-362">ClrInstanceID</span></span>|<span data-ttu-id="af1b2-363">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="af1b2-363">win:UInt16</span></span>|<span data-ttu-id="af1b2-364">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="af1b2-364">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="af1b2-365">Retour au début</span><span class="sxs-lookup"><span data-stu-id="af1b2-365">Back to top</span></span>](#top)  
  
<a name="gcsuspendeeend_v1_event"></a>   
## <a name="gcsuspendeeendv1-event"></a><span data-ttu-id="af1b2-366">Événement GCSuspendEEEnd_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-366">GCSuspendEEEnd_V1 Event</span></span>  
 <span data-ttu-id="af1b2-367">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-367">The following table shows the keyword and level:</span></span>  
  
|<span data-ttu-id="af1b2-368">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-368">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-369">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-369">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-370">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-370">(0x1)</span></span>|<span data-ttu-id="af1b2-371">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-371">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-372">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-372">The following table shows the event information:</span></span>  
  
|<span data-ttu-id="af1b2-373">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-373">Event</span></span>|<span data-ttu-id="af1b2-374">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-374">Event ID</span></span>|<span data-ttu-id="af1b2-375">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="af1b2-375">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCSuspendEEEnd_V1`|<span data-ttu-id="af1b2-376">8</span><span class="sxs-lookup"><span data-stu-id="af1b2-376">8</span></span>|<span data-ttu-id="af1b2-377">Fin de la suspension du moteur d'exécution pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="af1b2-377">End of suspension of the execution engine for garbage collection.</span></span>|  
  
 <span data-ttu-id="af1b2-378">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="af1b2-378">No event data.</span></span>  
  
 [<span data-ttu-id="af1b2-379">Retour au début</span><span class="sxs-lookup"><span data-stu-id="af1b2-379">Back to top</span></span>](#top)  
  
<a name="gcallocationtick_v2_event"></a>   
## <a name="gcallocationtickv2-event"></a><span data-ttu-id="af1b2-380">Événement GCAllocationTick_V2</span><span class="sxs-lookup"><span data-stu-id="af1b2-380">GCAllocationTick_V2 Event</span></span>  
 <span data-ttu-id="af1b2-381">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-381">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="af1b2-382">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-382">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-383">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-383">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-384">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-384">(0x1)</span></span>|<span data-ttu-id="af1b2-385">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-385">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-386">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-386">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="af1b2-387">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-387">Event</span></span>|<span data-ttu-id="af1b2-388">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-388">Event ID</span></span>|<span data-ttu-id="af1b2-389">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="af1b2-389">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCAllocationTick_V2`|<span data-ttu-id="af1b2-390">10</span><span class="sxs-lookup"><span data-stu-id="af1b2-390">10</span></span>|<span data-ttu-id="af1b2-391">Chaque fois qu'environ 100 Ko sont alloués.</span><span class="sxs-lookup"><span data-stu-id="af1b2-391">Each time approximately 100 KB is allocated.</span></span>|  
  
 <span data-ttu-id="af1b2-392">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-392">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="af1b2-393">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="af1b2-393">Field name</span></span>|<span data-ttu-id="af1b2-394">Type de données</span><span class="sxs-lookup"><span data-stu-id="af1b2-394">Data type</span></span>|<span data-ttu-id="af1b2-395">Description</span><span class="sxs-lookup"><span data-stu-id="af1b2-395">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="af1b2-396">AllocationAmount</span><span class="sxs-lookup"><span data-stu-id="af1b2-396">AllocationAmount</span></span>|<span data-ttu-id="af1b2-397">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-397">win:UInt32</span></span>|<span data-ttu-id="af1b2-398">Taille de l'allocation, en octets.</span><span class="sxs-lookup"><span data-stu-id="af1b2-398">The allocation size, in bytes.</span></span> <span data-ttu-id="af1b2-399">Cette valeur est correcte pour les allocations inférieures à la longueur d'un ULONG (4 294 967 295 octets).</span><span class="sxs-lookup"><span data-stu-id="af1b2-399">This value is accurate for allocations that are less than the length of a ULONG (4,294,967,295 bytes).</span></span> <span data-ttu-id="af1b2-400">Si l'allocation est supérieure, ce champ contient une valeur tronquée.</span><span class="sxs-lookup"><span data-stu-id="af1b2-400">If the allocation is greater, this field contains a truncated value.</span></span> <span data-ttu-id="af1b2-401">Utilisez `AllocationAmount64` pour les allocations très volumineuses.</span><span class="sxs-lookup"><span data-stu-id="af1b2-401">Use `AllocationAmount64` for very large allocations.</span></span>|  
|<span data-ttu-id="af1b2-402">AllocationKind</span><span class="sxs-lookup"><span data-stu-id="af1b2-402">AllocationKind</span></span>|<span data-ttu-id="af1b2-403">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-403">win:UInt32</span></span>|<span data-ttu-id="af1b2-404">0x0 – Allocation de petits objets (l'allocation se fait dans le tas de petits objets).</span><span class="sxs-lookup"><span data-stu-id="af1b2-404">0x0 - Small object allocation (allocation is in small object heap).</span></span><br /><br /> <span data-ttu-id="af1b2-405">0x1 – Allocation d'objets volumineux (l'allocation se fait dans le tas des objets volumineux).</span><span class="sxs-lookup"><span data-stu-id="af1b2-405">0x1 - Large object allocation (allocation is in large object heap).</span></span>|  
|<span data-ttu-id="af1b2-406">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="af1b2-406">ClrInstanceID</span></span>|<span data-ttu-id="af1b2-407">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="af1b2-407">win:UInt16</span></span>|<span data-ttu-id="af1b2-408">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="af1b2-408">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
|<span data-ttu-id="af1b2-409">AllocationAmount64</span><span class="sxs-lookup"><span data-stu-id="af1b2-409">AllocationAmount64</span></span>|<span data-ttu-id="af1b2-410">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="af1b2-410">win:UInt64</span></span>|<span data-ttu-id="af1b2-411">Taille de l'allocation, en octets.</span><span class="sxs-lookup"><span data-stu-id="af1b2-411">The allocation size, in bytes.</span></span> <span data-ttu-id="af1b2-412">Cette valeur est correcte pour les allocations très volumineuses.</span><span class="sxs-lookup"><span data-stu-id="af1b2-412">This value is accurate for very large allocations.</span></span>|  
|<span data-ttu-id="af1b2-413">TypeId</span><span class="sxs-lookup"><span data-stu-id="af1b2-413">TypeId</span></span>|<span data-ttu-id="af1b2-414">win:Pointer</span><span class="sxs-lookup"><span data-stu-id="af1b2-414">win:Pointer</span></span>|<span data-ttu-id="af1b2-415">Adresse de MethodTable.</span><span class="sxs-lookup"><span data-stu-id="af1b2-415">The address of the MethodTable.</span></span> <span data-ttu-id="af1b2-416">Quand plusieurs types d'objets ont été alloués au cours de cet événement, il s'agit de l'adresse de MethodTable qui correspond au dernier objet alloué (l'objet qui a provoqué le dépassement du seuil de 100 Ko).</span><span class="sxs-lookup"><span data-stu-id="af1b2-416">When there are several types of objects that were allocated during this event, this is the address of the MethodTable that corresponds to the last object allocated (the object that caused the 100 KB threshold to be exceeded).</span></span>|  
|<span data-ttu-id="af1b2-417">TypeName</span><span class="sxs-lookup"><span data-stu-id="af1b2-417">TypeName</span></span>|<span data-ttu-id="af1b2-418">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="af1b2-418">win:UnicodeString</span></span>|<span data-ttu-id="af1b2-419">Nom du type ayant été alloué.</span><span class="sxs-lookup"><span data-stu-id="af1b2-419">The name of the type that was allocated.</span></span> <span data-ttu-id="af1b2-420">Quand plusieurs types d'objets ont été alloués au cours de cet événement, il s'agit du type du dernier objet alloué (l'objet qui a provoqué le dépassement du seuil de 100 Ko).</span><span class="sxs-lookup"><span data-stu-id="af1b2-420">When there are several types of objects that were allocated during this event, this is the type of the last object allocated (the object that caused the 100 KB threshold to be exceeded).</span></span>|  
|<span data-ttu-id="af1b2-421">HeapIndex</span><span class="sxs-lookup"><span data-stu-id="af1b2-421">HeapIndex</span></span>|<span data-ttu-id="af1b2-422">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-422">win:UInt32</span></span>|<span data-ttu-id="af1b2-423">Segment de mémoire où l'objet a été alloué.</span><span class="sxs-lookup"><span data-stu-id="af1b2-423">The heap where the object was allocated.</span></span> <span data-ttu-id="af1b2-424">Cette valeur est de 0 (zéro) lors d'une exécution avec le garbage collection pour station de travail.</span><span class="sxs-lookup"><span data-stu-id="af1b2-424">This value is 0 (zero) when running with workstation garbage collection.</span></span>|  
  
 [<span data-ttu-id="af1b2-425">Retour au début</span><span class="sxs-lookup"><span data-stu-id="af1b2-425">Back to top</span></span>](#top)  
  
<a name="gcfinalizersbegin_v1_event"></a>   
## <a name="gcfinalizersbeginv1-event"></a><span data-ttu-id="af1b2-426">Événement GCFinalizersBegin_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-426">GCFinalizersBegin_V1 Event</span></span>  
 <span data-ttu-id="af1b2-427">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-427">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="af1b2-428">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-428">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-429">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-429">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-430">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-430">(0x1)</span></span>|<span data-ttu-id="af1b2-431">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-431">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-432">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-432">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="af1b2-433">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-433">Event</span></span>|<span data-ttu-id="af1b2-434">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-434">Event ID</span></span>|<span data-ttu-id="af1b2-435">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="af1b2-435">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCFinalizersBegin_V1`|<span data-ttu-id="af1b2-436">14</span><span class="sxs-lookup"><span data-stu-id="af1b2-436">14</span></span>|<span data-ttu-id="af1b2-437">Début de l'exécution des finaliseurs.</span><span class="sxs-lookup"><span data-stu-id="af1b2-437">The start of running finalizers.</span></span>|  
  
 <span data-ttu-id="af1b2-438">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="af1b2-438">No event data.</span></span>  
  
 [<span data-ttu-id="af1b2-439">Retour au début</span><span class="sxs-lookup"><span data-stu-id="af1b2-439">Back to top</span></span>](#top)  
  
<a name="gcfinalizersend_v1_event"></a>   
## <a name="gcfinalizersendv1-event"></a><span data-ttu-id="af1b2-440">Événement GCFinalizersEnd_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-440">GCFinalizersEnd_V1 Event</span></span>  
 <span data-ttu-id="af1b2-441">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-441">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="af1b2-442">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-442">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-443">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-443">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-444">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-444">(0x1)</span></span>|<span data-ttu-id="af1b2-445">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-445">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-446">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-446">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="af1b2-447">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-447">Event</span></span>|<span data-ttu-id="af1b2-448">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-448">Event ID</span></span>|<span data-ttu-id="af1b2-449">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="af1b2-449">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCFinalizersEnd_V1`|<span data-ttu-id="af1b2-450">13</span><span class="sxs-lookup"><span data-stu-id="af1b2-450">13</span></span>|<span data-ttu-id="af1b2-451">Fin de l'exécution des finaliseurs.</span><span class="sxs-lookup"><span data-stu-id="af1b2-451">The end of running finalizers.</span></span>|  
  
 <span data-ttu-id="af1b2-452">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-452">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="af1b2-453">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="af1b2-453">Field name</span></span>|<span data-ttu-id="af1b2-454">Type de données</span><span class="sxs-lookup"><span data-stu-id="af1b2-454">Data type</span></span>|<span data-ttu-id="af1b2-455">Description</span><span class="sxs-lookup"><span data-stu-id="af1b2-455">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="af1b2-456">Nombre</span><span class="sxs-lookup"><span data-stu-id="af1b2-456">Count</span></span>|<span data-ttu-id="af1b2-457">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="af1b2-457">win:UInt32</span></span>|<span data-ttu-id="af1b2-458">Nombre de finaliseurs exécutés.</span><span class="sxs-lookup"><span data-stu-id="af1b2-458">The number of finalizers that were run.</span></span>|  
|<span data-ttu-id="af1b2-459">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="af1b2-459">ClrInstanceID</span></span>|<span data-ttu-id="af1b2-460">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="af1b2-460">win:UInt16</span></span>|<span data-ttu-id="af1b2-461">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="af1b2-461">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="af1b2-462">Retour au début</span><span class="sxs-lookup"><span data-stu-id="af1b2-462">Back to top</span></span>](#top)  
  
<a name="gccreateconcurrentthread_v1_event"></a>   
## <a name="gccreateconcurrentthreadv1-event"></a><span data-ttu-id="af1b2-463">Événement GCCreateConcurrentThread_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-463">GCCreateConcurrentThread_V1 Event</span></span>  
 <span data-ttu-id="af1b2-464">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-464">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="af1b2-465">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-465">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-466">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-466">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-467">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-467">(0x1)</span></span>|<span data-ttu-id="af1b2-468">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-468">Informational (4)</span></span>|  
|`ThreadingKeyword` <span data-ttu-id="af1b2-469">(0 x 10000)</span><span class="sxs-lookup"><span data-stu-id="af1b2-469">(0x10000)</span></span>|<span data-ttu-id="af1b2-470">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-470">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-471">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-471">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="af1b2-472">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-472">Event</span></span>|<span data-ttu-id="af1b2-473">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-473">Event ID</span></span>|<span data-ttu-id="af1b2-474">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="af1b2-474">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCCreateConcurrentThread_V1`|<span data-ttu-id="af1b2-475">11</span><span class="sxs-lookup"><span data-stu-id="af1b2-475">11</span></span>|<span data-ttu-id="af1b2-476">Un thread de garbage collection simultané a été créé.</span><span class="sxs-lookup"><span data-stu-id="af1b2-476">Concurrent garbage collection thread was created.</span></span>|  
  
 <span data-ttu-id="af1b2-477">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="af1b2-477">No event data.</span></span>  
  
 [<span data-ttu-id="af1b2-478">Retour au début</span><span class="sxs-lookup"><span data-stu-id="af1b2-478">Back to top</span></span>](#top)  
  
<a name="gcterminateconcurrentthread_v1_event"></a>   
## <a name="gcterminateconcurrentthreadv1-event"></a><span data-ttu-id="af1b2-479">Événement GCTerminateConcurrentThread_V1</span><span class="sxs-lookup"><span data-stu-id="af1b2-479">GCTerminateConcurrentThread_V1 Event</span></span>  
 <span data-ttu-id="af1b2-480">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="af1b2-480">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="af1b2-481">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-481">Keyword for raising the event</span></span>|<span data-ttu-id="af1b2-482">Niveau</span><span class="sxs-lookup"><span data-stu-id="af1b2-482">Level</span></span>|  
|-----------------------------------|-----------|  
|`GCKeyword` <span data-ttu-id="af1b2-483">(0x1)</span><span class="sxs-lookup"><span data-stu-id="af1b2-483">(0x1)</span></span>|<span data-ttu-id="af1b2-484">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-484">Informational (4)</span></span>|  
|`ThreadingKeyword` <span data-ttu-id="af1b2-485">(0 x 10000)</span><span class="sxs-lookup"><span data-stu-id="af1b2-485">(0x10000)</span></span>|<span data-ttu-id="af1b2-486">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="af1b2-486">Informational (4)</span></span>|  
  
 <span data-ttu-id="af1b2-487">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="af1b2-487">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="af1b2-488">Événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-488">Event</span></span>|<span data-ttu-id="af1b2-489">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="af1b2-489">Event ID</span></span>|<span data-ttu-id="af1b2-490">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="af1b2-490">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCTerminateConcurrentThread_V1`|<span data-ttu-id="af1b2-491">12</span><span class="sxs-lookup"><span data-stu-id="af1b2-491">12</span></span>|<span data-ttu-id="af1b2-492">Un thread de garbage collection simultané s'est terminé.</span><span class="sxs-lookup"><span data-stu-id="af1b2-492">Concurrent garbage collection thread was terminated.</span></span>|  
  
 <span data-ttu-id="af1b2-493">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="af1b2-493">No event data.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="af1b2-494">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af1b2-494">See also</span></span>

- [<span data-ttu-id="af1b2-495">Événements ETW du CLR</span><span class="sxs-lookup"><span data-stu-id="af1b2-495">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
