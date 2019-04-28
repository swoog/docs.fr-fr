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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61722937"
---
# <a name="garbage-collection-etw-events"></a><span data-ttu-id="11458-102">Événements ETW de garbage collection</span><span class="sxs-lookup"><span data-stu-id="11458-102">Garbage Collection ETW Events</span></span>
<a name="top"></a> <span data-ttu-id="11458-103">Ces événements collectent des informations relatives au garbage collection.</span><span class="sxs-lookup"><span data-stu-id="11458-103">These events collect information pertaining to garbage collection.</span></span> <span data-ttu-id="11458-104">Ils vous aident dans le diagnostic et le débogage, y compris pour déterminer combien de fois le garbage collection a été effectué, la quantité de mémoire libérée pendant le garbage collection, etc.</span><span class="sxs-lookup"><span data-stu-id="11458-104">They help in diagnostics and debugging, including determining how many times garbage collection was performed, how much memory was freed during garbage collection, and so on.</span></span>  
  
 <span data-ttu-id="11458-105">Cette catégorie comprend les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="11458-105">This category consists of the following events:</span></span>  
  
- [<span data-ttu-id="11458-106">Événement GCStart_V1</span><span class="sxs-lookup"><span data-stu-id="11458-106">GCStart_V1 Event</span></span>](#gcstart_v1_event)  
  
- [<span data-ttu-id="11458-107">Événement GCEnd_V1</span><span class="sxs-lookup"><span data-stu-id="11458-107">GCEnd_V1 Event</span></span>](#gcend_v1_event)  
  
- [<span data-ttu-id="11458-108">Événement GCHeapStats_V1</span><span class="sxs-lookup"><span data-stu-id="11458-108">GCHeapStats_V1 Event</span></span>](#gcheapstats_v1_event)  
  
- [<span data-ttu-id="11458-109">Événement GCCreateSegment_V1</span><span class="sxs-lookup"><span data-stu-id="11458-109">GCCreateSegment_V1 Event</span></span>](#gccreatesegment_v1_event)  
  
- [<span data-ttu-id="11458-110">Événement GCFreeSegment_V1</span><span class="sxs-lookup"><span data-stu-id="11458-110">GCFreeSegment_V1 Event</span></span>](#gcfreesegment_v1_event)  
  
- [<span data-ttu-id="11458-111">Événement GCRestartEEBegin_V1</span><span class="sxs-lookup"><span data-stu-id="11458-111">GCRestartEEBegin_V1 Event</span></span>](#gcrestarteebegin_v1_event)  
  
- [<span data-ttu-id="11458-112">Événement GCRestartEEEnd_V1</span><span class="sxs-lookup"><span data-stu-id="11458-112">GCRestartEEEnd_V1 Event</span></span>](#gcrestarteeend_v1_event)  
  
- [<span data-ttu-id="11458-113">Événement GCSuspendEE_V1</span><span class="sxs-lookup"><span data-stu-id="11458-113">GCSuspendEE_V1 Event</span></span>](#gcsuspendee_v1_event)  
  
- [<span data-ttu-id="11458-114">Événement GCSuspendEEEnd_V1</span><span class="sxs-lookup"><span data-stu-id="11458-114">GCSuspendEEEnd_V1 Event</span></span>](#gcsuspendeeend_v1_event)  
  
- [<span data-ttu-id="11458-115">Événement GCAllocationTick_V2</span><span class="sxs-lookup"><span data-stu-id="11458-115">GCAllocationTick_V2 Event</span></span>](#gcallocationtick_v2_event)  
  
- [<span data-ttu-id="11458-116">Événement GCFinalizersBegin_V1</span><span class="sxs-lookup"><span data-stu-id="11458-116">GCFinalizersBegin_V1 Event</span></span>](#gcfinalizersbegin_v1_event)  
  
- [<span data-ttu-id="11458-117">Événement GCFinalizersEnd_V1</span><span class="sxs-lookup"><span data-stu-id="11458-117">GCFinalizersEnd_V1 Event</span></span>](#gcfinalizersend_v1_event)  
  
- [<span data-ttu-id="11458-118">Événement GCCreateConcurrentThread_V1</span><span class="sxs-lookup"><span data-stu-id="11458-118">GCCreateConcurrentThread_V1 Event</span></span>](#gccreateconcurrentthread_v1_event)  
  
- [<span data-ttu-id="11458-119">Événement GCTerminateConcurrentThread_V1</span><span class="sxs-lookup"><span data-stu-id="11458-119">GCTerminateConcurrentThread_V1 Event</span></span>](#gcterminateconcurrentthread_v1_event)  
  
<a name="gcstart_v1_event"></a>   
## <a name="gcstartv1-event"></a><span data-ttu-id="11458-120">Événement GCStart_V1</span><span class="sxs-lookup"><span data-stu-id="11458-120">GCStart_V1 Event</span></span>  
 <span data-ttu-id="11458-121">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-121">The following table shows the keyword and level.</span></span> <span data-ttu-id="11458-122">(Pour plus d'informations, consultez [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span><span class="sxs-lookup"><span data-stu-id="11458-122">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="11458-123">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-123">Keyword for raising the event</span></span>|<span data-ttu-id="11458-124">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-124">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-125">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-125">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-126">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-126">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-127">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-127">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="11458-128">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-128">Event</span></span>|<span data-ttu-id="11458-129">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-129">Event ID</span></span>|<span data-ttu-id="11458-130">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="11458-130">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCStart_V1`|<span data-ttu-id="11458-131">1</span><span class="sxs-lookup"><span data-stu-id="11458-131">1</span></span>|<span data-ttu-id="11458-132">Un garbage collection a démarré.</span><span class="sxs-lookup"><span data-stu-id="11458-132">A garbage collection has started.</span></span>|  
  
 <span data-ttu-id="11458-133">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-133">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="11458-134">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="11458-134">Field name</span></span>|<span data-ttu-id="11458-135">Type de données</span><span class="sxs-lookup"><span data-stu-id="11458-135">Data type</span></span>|<span data-ttu-id="11458-136">Description</span><span class="sxs-lookup"><span data-stu-id="11458-136">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="11458-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="11458-137">Count</span></span>|<span data-ttu-id="11458-138">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-138">win:UInt32</span></span>|<span data-ttu-id="11458-139">Le *n*ième garbage collection.</span><span class="sxs-lookup"><span data-stu-id="11458-139">The *n*th garbage collection.</span></span>|  
|<span data-ttu-id="11458-140">Profondeur</span><span class="sxs-lookup"><span data-stu-id="11458-140">Depth</span></span>|<span data-ttu-id="11458-141">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-141">win:UInt32</span></span>|<span data-ttu-id="11458-142">La génération est collectée.</span><span class="sxs-lookup"><span data-stu-id="11458-142">The generation that is being collected.</span></span>|  
|<span data-ttu-id="11458-143">Raison</span><span class="sxs-lookup"><span data-stu-id="11458-143">Reason</span></span>|<span data-ttu-id="11458-144">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-144">win:UInt32</span></span>|<span data-ttu-id="11458-145">Pourquoi le garbage collection a été déclenché :</span><span class="sxs-lookup"><span data-stu-id="11458-145">Why the garbage collection was triggered:</span></span><br /><br /> <span data-ttu-id="11458-146">0x0 – Allocation de tas de petits objets.</span><span class="sxs-lookup"><span data-stu-id="11458-146">0x0 - Small object heap allocation.</span></span><br /><br /> <span data-ttu-id="11458-147">0x1 – Induit.</span><span class="sxs-lookup"><span data-stu-id="11458-147">0x1 - Induced.</span></span><br /><br /> <span data-ttu-id="11458-148">0x2 – Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="11458-148">0x2 - Low memory.</span></span><br /><br /> <span data-ttu-id="11458-149">0x3 – Vide.</span><span class="sxs-lookup"><span data-stu-id="11458-149">0x3 - Empty.</span></span><br /><br /> <span data-ttu-id="11458-150">0x4 – Allocation de tas d'objets volumineux.</span><span class="sxs-lookup"><span data-stu-id="11458-150">0x4 - Large object heap allocation.</span></span><br /><br /> <span data-ttu-id="11458-151">0x5 – Espace insuffisant (pour un tas de petits objets)</span><span class="sxs-lookup"><span data-stu-id="11458-151">0x5 - Out of space (for small object heap).</span></span><br /><br /> <span data-ttu-id="11458-152">0x6 – Espace insuffisant (pour un tas d'objets volumineux)</span><span class="sxs-lookup"><span data-stu-id="11458-152">0x6 - Out of space (for large object heap).</span></span><br /><br /> <span data-ttu-id="11458-153">0x7 – Induit mais non forcé comme blocage</span><span class="sxs-lookup"><span data-stu-id="11458-153">0x7 - Induced but not forced as blocking.</span></span>|  
|<span data-ttu-id="11458-154">Type</span><span class="sxs-lookup"><span data-stu-id="11458-154">Type</span></span>|<span data-ttu-id="11458-155">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-155">win:UInt32</span></span>|<span data-ttu-id="11458-156">0x0 – Un blocage de garbage collection s'est produit en dehors du garbage collection d'arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="11458-156">0x0 - Blocking garbage collection occurred outside background garbage collection.</span></span><br /><br /> <span data-ttu-id="11458-157">0x1 – Garbage collection d'arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="11458-157">0x1 - Background garbage collection.</span></span><br /><br /> <span data-ttu-id="11458-158">0x2 – Un blocage de garbage collection s'est produit pendant le garbage collection d'arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="11458-158">0x2 - Blocking garbage collection occurred during background garbage collection.</span></span>|  
|<span data-ttu-id="11458-159">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="11458-159">ClrInstanceID</span></span>|<span data-ttu-id="11458-160">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="11458-160">win:UInt16</span></span>|<span data-ttu-id="11458-161">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="11458-161">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="11458-162">Retour au début</span><span class="sxs-lookup"><span data-stu-id="11458-162">Back to top</span></span>](#top)  
  
<a name="gcend_v1_event"></a>   
## <a name="gcendv1-event"></a><span data-ttu-id="11458-163">Événement GCEnd_V1</span><span class="sxs-lookup"><span data-stu-id="11458-163">GCEnd_V1 Event</span></span>  
 <span data-ttu-id="11458-164">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-164">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="11458-165">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-165">Keyword for raising the event</span></span>|<span data-ttu-id="11458-166">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-166">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-167">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-167">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-168">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-168">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-169">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-169">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="11458-170">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-170">Event</span></span>|<span data-ttu-id="11458-171">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-171">Event ID</span></span>|<span data-ttu-id="11458-172">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="11458-172">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCEnd_V1`|<span data-ttu-id="11458-173">2</span><span class="sxs-lookup"><span data-stu-id="11458-173">2</span></span>|<span data-ttu-id="11458-174">Un garbage collection s'est terminé.</span><span class="sxs-lookup"><span data-stu-id="11458-174">The garbage collection has ended.</span></span>|  
  
 <span data-ttu-id="11458-175">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-175">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="11458-176">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="11458-176">Field name</span></span>|<span data-ttu-id="11458-177">Type de données</span><span class="sxs-lookup"><span data-stu-id="11458-177">Data type</span></span>|<span data-ttu-id="11458-178">Description</span><span class="sxs-lookup"><span data-stu-id="11458-178">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="11458-179">Nombre</span><span class="sxs-lookup"><span data-stu-id="11458-179">Count</span></span>|<span data-ttu-id="11458-180">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-180">win:UInt32</span></span>|<span data-ttu-id="11458-181">Le *n*ième garbage collection.</span><span class="sxs-lookup"><span data-stu-id="11458-181">The *n*th garbage collection.</span></span>|  
|<span data-ttu-id="11458-182">Profondeur</span><span class="sxs-lookup"><span data-stu-id="11458-182">Depth</span></span>|<span data-ttu-id="11458-183">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-183">win:UInt32</span></span>|<span data-ttu-id="11458-184">Génération ayant été collectée.</span><span class="sxs-lookup"><span data-stu-id="11458-184">The generation that was collected.</span></span>|  
|<span data-ttu-id="11458-185">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="11458-185">ClrInstanceID</span></span>|<span data-ttu-id="11458-186">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="11458-186">win:UInt16</span></span>|<span data-ttu-id="11458-187">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="11458-187">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="11458-188">Retour au début</span><span class="sxs-lookup"><span data-stu-id="11458-188">Back to top</span></span>](#top)  
  
<a name="gcheapstats_v1_event"></a>   
## <a name="gcheapstatsv1-event"></a><span data-ttu-id="11458-189">Événement GCHeapStats_V1</span><span class="sxs-lookup"><span data-stu-id="11458-189">GCHeapStats_V1 Event</span></span>  
 <span data-ttu-id="11458-190">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-190">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="11458-191">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-191">Keyword for raising the event</span></span>|<span data-ttu-id="11458-192">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-192">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-193">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-193">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-194">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-194">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-195">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-195">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="11458-196">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-196">Event</span></span>|<span data-ttu-id="11458-197">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-197">Event ID</span></span>|<span data-ttu-id="11458-198">Description</span><span class="sxs-lookup"><span data-stu-id="11458-198">Description</span></span>|  
|-----------|--------------|-----------------|  
|`GCHeapStats_V1`|<span data-ttu-id="11458-199">4</span><span class="sxs-lookup"><span data-stu-id="11458-199">4</span></span>|<span data-ttu-id="11458-200">Affiche les statistiques relatives aux tas à la fin de chaque garbage collection.</span><span class="sxs-lookup"><span data-stu-id="11458-200">Shows the heap statistics at the end of each garbage collection.</span></span>|  
  
 <span data-ttu-id="11458-201">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-201">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="11458-202">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="11458-202">Field name</span></span>|<span data-ttu-id="11458-203">Type de données</span><span class="sxs-lookup"><span data-stu-id="11458-203">Data type</span></span>|<span data-ttu-id="11458-204">Description</span><span class="sxs-lookup"><span data-stu-id="11458-204">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="11458-205">GenerationSize0</span><span class="sxs-lookup"><span data-stu-id="11458-205">GenerationSize0</span></span>|<span data-ttu-id="11458-206">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-206">win:UInt64</span></span>|<span data-ttu-id="11458-207">Taille, en octets, de la mémoire de génération 0.</span><span class="sxs-lookup"><span data-stu-id="11458-207">The size, in bytes, of generation 0 memory.</span></span>|  
|<span data-ttu-id="11458-208">TotalPromotedSize0</span><span class="sxs-lookup"><span data-stu-id="11458-208">TotalPromotedSize0</span></span>|<span data-ttu-id="11458-209">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-209">win:UInt64</span></span>|<span data-ttu-id="11458-210">Nombre d'octets promus de la génération 0 à la génération 1.</span><span class="sxs-lookup"><span data-stu-id="11458-210">The number of bytes that are promoted from generation 0 to generation 1.</span></span>|  
|<span data-ttu-id="11458-211">GenerationSize1</span><span class="sxs-lookup"><span data-stu-id="11458-211">GenerationSize1</span></span>|<span data-ttu-id="11458-212">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-212">win:UInt64</span></span>|<span data-ttu-id="11458-213">Taille, en octets, de la mémoire de génération 1.</span><span class="sxs-lookup"><span data-stu-id="11458-213">The size, in bytes, of generation 1 memory.</span></span>|  
|<span data-ttu-id="11458-214">TotalPromotedSize1</span><span class="sxs-lookup"><span data-stu-id="11458-214">TotalPromotedSize1</span></span>|<span data-ttu-id="11458-215">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-215">win:UInt64</span></span>|<span data-ttu-id="11458-216">Nombre d'octets promus de la génération 1 à la génération 2.</span><span class="sxs-lookup"><span data-stu-id="11458-216">The number of bytes that are promoted from generation 1 to generation 2.</span></span>|  
|<span data-ttu-id="11458-217">GenerationSize2</span><span class="sxs-lookup"><span data-stu-id="11458-217">GenerationSize2</span></span>|<span data-ttu-id="11458-218">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-218">win:UInt64</span></span>|<span data-ttu-id="11458-219">Taille, en octets, de la mémoire de génération 2.</span><span class="sxs-lookup"><span data-stu-id="11458-219">The size, in bytes, of generation 2 memory.</span></span>|  
|<span data-ttu-id="11458-220">TotalPromotedSize2</span><span class="sxs-lookup"><span data-stu-id="11458-220">TotalPromotedSize2</span></span>|<span data-ttu-id="11458-221">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-221">win:UInt64</span></span>|<span data-ttu-id="11458-222">Nombre d'octets ayant survécu dans la génération 2 après la dernière collection.</span><span class="sxs-lookup"><span data-stu-id="11458-222">The number of bytes that survived in generation 2 after the last collection.</span></span>|  
|<span data-ttu-id="11458-223">GenerationSize3</span><span class="sxs-lookup"><span data-stu-id="11458-223">GenerationSize3</span></span>|<span data-ttu-id="11458-224">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-224">win:UInt64</span></span>|<span data-ttu-id="11458-225">Taille, en octets, du tas des objets volumineux.</span><span class="sxs-lookup"><span data-stu-id="11458-225">The size, in bytes, of the large object heap.</span></span>|  
|<span data-ttu-id="11458-226">TotalPromotedSize3</span><span class="sxs-lookup"><span data-stu-id="11458-226">TotalPromotedSize3</span></span>|<span data-ttu-id="11458-227">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-227">win:UInt64</span></span>|<span data-ttu-id="11458-228">Nombre d'octets ayant survécu dans le tas d'objets volumineux après la dernière collection.</span><span class="sxs-lookup"><span data-stu-id="11458-228">The number of bytes that survived in the large object heap after the last collection.</span></span>|  
|<span data-ttu-id="11458-229">FinalizationPromotedSize</span><span class="sxs-lookup"><span data-stu-id="11458-229">FinalizationPromotedSize</span></span>|<span data-ttu-id="11458-230">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-230">win:UInt64</span></span>|<span data-ttu-id="11458-231">Taille totale, en octets, des objets qui sont prêts pour la finalisation.</span><span class="sxs-lookup"><span data-stu-id="11458-231">The total size, in bytes, of the objects that are ready for finalization.</span></span>|  
|<span data-ttu-id="11458-232">FinalizationPromotedSize</span><span class="sxs-lookup"><span data-stu-id="11458-232">FinalizationPromotedCount</span></span>|<span data-ttu-id="11458-233">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-233">win:UInt64</span></span>|<span data-ttu-id="11458-234">Nombre d'objets qui sont prêts pour la finalisation.</span><span class="sxs-lookup"><span data-stu-id="11458-234">The number of objects that are ready for finalization.</span></span>|  
|<span data-ttu-id="11458-235">PinnedObjectCount</span><span class="sxs-lookup"><span data-stu-id="11458-235">PinnedObjectCount</span></span>|<span data-ttu-id="11458-236">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-236">win:UInt32</span></span>|<span data-ttu-id="11458-237">Nombre d'objets (non déplaçables) épinglés.</span><span class="sxs-lookup"><span data-stu-id="11458-237">The number of pinned (unmovable) objects.</span></span>|  
|<span data-ttu-id="11458-238">SinkBlockCount</span><span class="sxs-lookup"><span data-stu-id="11458-238">SinkBlockCount</span></span>|<span data-ttu-id="11458-239">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-239">win:UInt32</span></span>|<span data-ttu-id="11458-240">Nombre de blocs de synchronisation en cours d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="11458-240">The number of synchronization blocks in use.</span></span>|  
|<span data-ttu-id="11458-241">GCHandleCount</span><span class="sxs-lookup"><span data-stu-id="11458-241">GCHandleCount</span></span>|<span data-ttu-id="11458-242">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-242">win:UInt32</span></span>|<span data-ttu-id="11458-243">Nombre de handles de garbage collection en cours d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="11458-243">The number of garbage collection handles in use.</span></span>|  
|<span data-ttu-id="11458-244">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="11458-244">ClrInstanceID</span></span>|<span data-ttu-id="11458-245">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="11458-245">win:UInt16</span></span>|<span data-ttu-id="11458-246">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="11458-246">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="11458-247">Retour au début</span><span class="sxs-lookup"><span data-stu-id="11458-247">Back to top</span></span>](#top)  
  
<a name="gccreatesegment_v1_event"></a>   
## <a name="gccreatesegmentv1-event"></a><span data-ttu-id="11458-248">Événement GCCreateSegment_V1</span><span class="sxs-lookup"><span data-stu-id="11458-248">GCCreateSegment_V1 Event</span></span>  
 <span data-ttu-id="11458-249">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-249">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="11458-250">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-250">Keyword for raising the event</span></span>|<span data-ttu-id="11458-251">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-251">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-252">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-252">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-253">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-253">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-254">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-254">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="11458-255">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-255">Event</span></span>|<span data-ttu-id="11458-256">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-256">Event ID</span></span>|<span data-ttu-id="11458-257">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="11458-257">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCCreateSegment_V1`|<span data-ttu-id="11458-258">5</span><span class="sxs-lookup"><span data-stu-id="11458-258">5</span></span>|<span data-ttu-id="11458-259">Un nouveau segment de garbage collection a été créé.</span><span class="sxs-lookup"><span data-stu-id="11458-259">A new garbage collection segment has been created.</span></span> <span data-ttu-id="11458-260">En outre, quand le suivi est activé sur un processus en cours d'exécution, cet événement est déclenché pour chaque segment existant.</span><span class="sxs-lookup"><span data-stu-id="11458-260">In addition, when tracing is enabled on a process that is already running, this event is raised for each existing segment.</span></span>|  
  
 <span data-ttu-id="11458-261">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-261">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="11458-262">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="11458-262">Field name</span></span>|<span data-ttu-id="11458-263">Type de données</span><span class="sxs-lookup"><span data-stu-id="11458-263">Data type</span></span>|<span data-ttu-id="11458-264">Description</span><span class="sxs-lookup"><span data-stu-id="11458-264">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="11458-265">Adresse</span><span class="sxs-lookup"><span data-stu-id="11458-265">Address</span></span>|<span data-ttu-id="11458-266">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-266">win:UInt64</span></span>|<span data-ttu-id="11458-267">Adresse du segment.</span><span class="sxs-lookup"><span data-stu-id="11458-267">The address of the segment.</span></span>|  
|<span data-ttu-id="11458-268">Taille</span><span class="sxs-lookup"><span data-stu-id="11458-268">Size</span></span>|<span data-ttu-id="11458-269">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-269">win:UInt64</span></span>|<span data-ttu-id="11458-270">Taille du segment.</span><span class="sxs-lookup"><span data-stu-id="11458-270">The size of the segment.</span></span>|  
|<span data-ttu-id="11458-271">Type</span><span class="sxs-lookup"><span data-stu-id="11458-271">Type</span></span>|<span data-ttu-id="11458-272">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-272">win:UInt32</span></span>|<span data-ttu-id="11458-273">0x0 – Tas de petits objets.</span><span class="sxs-lookup"><span data-stu-id="11458-273">0x0 - Small object heap.</span></span><br /><br /> <span data-ttu-id="11458-274">0x1 – Tas d'objets volumineux.</span><span class="sxs-lookup"><span data-stu-id="11458-274">0x1 - Large object heap.</span></span><br /><br /> <span data-ttu-id="11458-275">0x2 – Tas en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="11458-275">0x2 - Read-only heap.</span></span>|  
|<span data-ttu-id="11458-276">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="11458-276">ClrInstanceID</span></span>|<span data-ttu-id="11458-277">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="11458-277">win:UInt16</span></span>|<span data-ttu-id="11458-278">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="11458-278">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 <span data-ttu-id="11458-279">Notez que la taille des segments alloués par le garbage collector est spécifique à l'implémentation et susceptible de changer à tout moment, y compris lors des mises à jour périodiques.</span><span class="sxs-lookup"><span data-stu-id="11458-279">Note that the size of segments allocated by the garbage collector is implementation-specific and is subject to change at any time, including in periodic updates.</span></span> <span data-ttu-id="11458-280">Votre application ne doit jamais faire d'hypothèses concernant une taille de segment particulière, ni dépendre de celle-ci. Elle ne doit pas non plus tenter de configurer la quantité de mémoire disponible pour les allocations de segments.</span><span class="sxs-lookup"><span data-stu-id="11458-280">Your app should never make assumptions about or depend on a particular segment size, nor should it attempt to configure the amount of memory available for segment allocations.</span></span>  
  
 [<span data-ttu-id="11458-281">Retour au début</span><span class="sxs-lookup"><span data-stu-id="11458-281">Back to top</span></span>](#top)  
  
<a name="gcfreesegment_v1_event"></a>   
## <a name="gcfreesegmentv1-event"></a><span data-ttu-id="11458-282">Événement GCFreeSegment_V1</span><span class="sxs-lookup"><span data-stu-id="11458-282">GCFreeSegment_V1 Event</span></span>  
 <span data-ttu-id="11458-283">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-283">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="11458-284">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-284">Keyword for raising the event</span></span>|<span data-ttu-id="11458-285">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-285">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-286">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-286">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-287">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-287">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-288">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-288">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="11458-289">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-289">Event</span></span>|<span data-ttu-id="11458-290">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-290">Event ID</span></span>|<span data-ttu-id="11458-291">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="11458-291">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCFreeSegment_V1`|<span data-ttu-id="11458-292">6</span><span class="sxs-lookup"><span data-stu-id="11458-292">6</span></span>|<span data-ttu-id="11458-293">Un nouveau segment de garbage collection a été libéré.</span><span class="sxs-lookup"><span data-stu-id="11458-293">A garbage collection segment has been released.</span></span>|  
  
 <span data-ttu-id="11458-294">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-294">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="11458-295">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="11458-295">Field name</span></span>|<span data-ttu-id="11458-296">Type de données</span><span class="sxs-lookup"><span data-stu-id="11458-296">Data type</span></span>|<span data-ttu-id="11458-297">Description</span><span class="sxs-lookup"><span data-stu-id="11458-297">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="11458-298">Adresse</span><span class="sxs-lookup"><span data-stu-id="11458-298">Address</span></span>|<span data-ttu-id="11458-299">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-299">win:UInt64</span></span>|<span data-ttu-id="11458-300">Adresse du segment.</span><span class="sxs-lookup"><span data-stu-id="11458-300">The address of the segment.</span></span>|  
|<span data-ttu-id="11458-301">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="11458-301">ClrInstanceID</span></span>|<span data-ttu-id="11458-302">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="11458-302">win:UInt16</span></span>|<span data-ttu-id="11458-303">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="11458-303">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="11458-304">Retour au début</span><span class="sxs-lookup"><span data-stu-id="11458-304">Back to top</span></span>](#top)  
  
<a name="gcrestarteebegin_v1_event"></a>   
## <a name="gcrestarteebeginv1-event"></a><span data-ttu-id="11458-305">Événement GCRestartEEBegin_V1</span><span class="sxs-lookup"><span data-stu-id="11458-305">GCRestartEEBegin_V1 Event</span></span>  
 <span data-ttu-id="11458-306">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-306">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="11458-307">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-307">Keyword for raising the event</span></span>|<span data-ttu-id="11458-308">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-308">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-309">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-309">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-310">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-310">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-311">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-311">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="11458-312">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-312">Event</span></span>|<span data-ttu-id="11458-313">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-313">Event ID</span></span>|<span data-ttu-id="11458-314">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="11458-314">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCRestartEEBegin_V1`|<span data-ttu-id="11458-315">7</span><span class="sxs-lookup"><span data-stu-id="11458-315">7</span></span>|<span data-ttu-id="11458-316">La reprise du common language runtime après sa suspension a commencé.</span><span class="sxs-lookup"><span data-stu-id="11458-316">Resumption from common language runtime suspension has begun.</span></span>|  
  
 <span data-ttu-id="11458-317">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="11458-317">No event data.</span></span>  
  
 [<span data-ttu-id="11458-318">Retour au début</span><span class="sxs-lookup"><span data-stu-id="11458-318">Back to top</span></span>](#top)  
  
<a name="gcrestarteeend_v1_event"></a>   
## <a name="gcrestarteeendv1-event"></a><span data-ttu-id="11458-319">Événement GCRestartEEEnd_V1</span><span class="sxs-lookup"><span data-stu-id="11458-319">GCRestartEEEnd_V1 Event</span></span>  
 <span data-ttu-id="11458-320">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-320">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="11458-321">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-321">Keyword for raising the event</span></span>|<span data-ttu-id="11458-322">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-322">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-323">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-323">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-324">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-324">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-325">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-325">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="11458-326">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-326">Event</span></span>|<span data-ttu-id="11458-327">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-327">Event Id</span></span>|<span data-ttu-id="11458-328">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="11458-328">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCRestartEEEnd_V1`|<span data-ttu-id="11458-329">3</span><span class="sxs-lookup"><span data-stu-id="11458-329">3</span></span>|<span data-ttu-id="11458-330">La reprise du common language runtime après sa suspension s'est terminée.</span><span class="sxs-lookup"><span data-stu-id="11458-330">Resumption from common language runtime suspension has ended.</span></span>|  
  
 <span data-ttu-id="11458-331">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="11458-331">No event data.</span></span>  
  
 [<span data-ttu-id="11458-332">Retour au début</span><span class="sxs-lookup"><span data-stu-id="11458-332">Back to top</span></span>](#top)  
  
<a name="gcsuspendee_v1_event"></a>   
## <a name="gcsuspendeev1-event"></a><span data-ttu-id="11458-333">Événement GCSuspendEE_V1</span><span class="sxs-lookup"><span data-stu-id="11458-333">GCSuspendEE_V1 Event</span></span>  
 <span data-ttu-id="11458-334">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-334">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="11458-335">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-335">Keyword for raising the event</span></span>|<span data-ttu-id="11458-336">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-336">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-337">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-337">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-338">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-338">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-339">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-339">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="11458-340">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-340">Event</span></span>|<span data-ttu-id="11458-341">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-341">Event ID</span></span>|<span data-ttu-id="11458-342">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="11458-342">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCSuspendEE_V1`|<span data-ttu-id="11458-343">9</span><span class="sxs-lookup"><span data-stu-id="11458-343">9</span></span>|<span data-ttu-id="11458-344">Début de la suspension du moteur d'exécution pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="11458-344">Start of suspension of the execution engine for garbage collection.</span></span>|  
  
 <span data-ttu-id="11458-345">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-345">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="11458-346">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="11458-346">Field name</span></span>|<span data-ttu-id="11458-347">Type de données</span><span class="sxs-lookup"><span data-stu-id="11458-347">Data type</span></span>|<span data-ttu-id="11458-348">Description</span><span class="sxs-lookup"><span data-stu-id="11458-348">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="11458-349">Raison</span><span class="sxs-lookup"><span data-stu-id="11458-349">Reason</span></span>|<span data-ttu-id="11458-350">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="11458-350">win:UInt16</span></span>|<span data-ttu-id="11458-351">0x0 – Autre.</span><span class="sxs-lookup"><span data-stu-id="11458-351">0x0 - Other.</span></span><br /><br /> <span data-ttu-id="11458-352">0x1 – Garbage collection.</span><span class="sxs-lookup"><span data-stu-id="11458-352">0x1 - Garbage collection.</span></span><br /><br /> <span data-ttu-id="11458-353">0x2 – Fermeture du domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="11458-353">0x2 - Application domain shutdown.</span></span><br /><br /> <span data-ttu-id="11458-354">0x3 – Pitching de code.</span><span class="sxs-lookup"><span data-stu-id="11458-354">0x3 - Code pitching.</span></span><br /><br /> <span data-ttu-id="11458-355">0x4 – Arrêt.</span><span class="sxs-lookup"><span data-stu-id="11458-355">0x4 - Shutdown.</span></span><br /><br /> <span data-ttu-id="11458-356">0x5 – Débogueur.</span><span class="sxs-lookup"><span data-stu-id="11458-356">0x5 - Debugger.</span></span><br /><br /> <span data-ttu-id="11458-357">0x6 – Préparation pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="11458-357">0x6 - Preparation for garbage collection.</span></span>|  
|<span data-ttu-id="11458-358">Nombre</span><span class="sxs-lookup"><span data-stu-id="11458-358">Count</span></span>|<span data-ttu-id="11458-359">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-359">win:UInt32</span></span>|<span data-ttu-id="11458-360">Nombre GC à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="11458-360">The GC count at the time.</span></span> <span data-ttu-id="11458-361">En règle générale, vous verrez un événement de démarrage de GC par la suite et son nombre doit être égal à ce nombre + 1 à mesure que nous augmentons l’index GC pendant un garbage collection.</span><span class="sxs-lookup"><span data-stu-id="11458-361">Usually, you would see a subsequent GC Start event after this, and its Count would be this Count + 1 as we increase the GC index during a garbage collection.</span></span>|  
|<span data-ttu-id="11458-362">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="11458-362">ClrInstanceID</span></span>|<span data-ttu-id="11458-363">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="11458-363">win:UInt16</span></span>|<span data-ttu-id="11458-364">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="11458-364">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="11458-365">Retour au début</span><span class="sxs-lookup"><span data-stu-id="11458-365">Back to top</span></span>](#top)  
  
<a name="gcsuspendeeend_v1_event"></a>   
## <a name="gcsuspendeeendv1-event"></a><span data-ttu-id="11458-366">Événement GCSuspendEEEnd_V1</span><span class="sxs-lookup"><span data-stu-id="11458-366">GCSuspendEEEnd_V1 Event</span></span>  
 <span data-ttu-id="11458-367">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-367">The following table shows the keyword and level:</span></span>  
  
|<span data-ttu-id="11458-368">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-368">Keyword for raising the event</span></span>|<span data-ttu-id="11458-369">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-369">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-370">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-370">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-371">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-371">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-372">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-372">The following table shows the event information:</span></span>  
  
|<span data-ttu-id="11458-373">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-373">Event</span></span>|<span data-ttu-id="11458-374">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-374">Event ID</span></span>|<span data-ttu-id="11458-375">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="11458-375">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCSuspendEEEnd_V1`|<span data-ttu-id="11458-376">8</span><span class="sxs-lookup"><span data-stu-id="11458-376">8</span></span>|<span data-ttu-id="11458-377">Fin de la suspension du moteur d'exécution pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="11458-377">End of suspension of the execution engine for garbage collection.</span></span>|  
  
 <span data-ttu-id="11458-378">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="11458-378">No event data.</span></span>  
  
 [<span data-ttu-id="11458-379">Retour au début</span><span class="sxs-lookup"><span data-stu-id="11458-379">Back to top</span></span>](#top)  
  
<a name="gcallocationtick_v2_event"></a>   
## <a name="gcallocationtickv2-event"></a><span data-ttu-id="11458-380">Événement GCAllocationTick_V2</span><span class="sxs-lookup"><span data-stu-id="11458-380">GCAllocationTick_V2 Event</span></span>  
 <span data-ttu-id="11458-381">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-381">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="11458-382">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-382">Keyword for raising the event</span></span>|<span data-ttu-id="11458-383">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-383">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-384">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-384">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-385">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-385">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-386">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-386">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="11458-387">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-387">Event</span></span>|<span data-ttu-id="11458-388">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-388">Event ID</span></span>|<span data-ttu-id="11458-389">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="11458-389">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCAllocationTick_V2`|<span data-ttu-id="11458-390">10</span><span class="sxs-lookup"><span data-stu-id="11458-390">10</span></span>|<span data-ttu-id="11458-391">Chaque fois qu'environ 100 Ko sont alloués.</span><span class="sxs-lookup"><span data-stu-id="11458-391">Each time approximately 100 KB is allocated.</span></span>|  
  
 <span data-ttu-id="11458-392">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-392">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="11458-393">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="11458-393">Field name</span></span>|<span data-ttu-id="11458-394">Type de données</span><span class="sxs-lookup"><span data-stu-id="11458-394">Data type</span></span>|<span data-ttu-id="11458-395">Description</span><span class="sxs-lookup"><span data-stu-id="11458-395">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="11458-396">AllocationAmount</span><span class="sxs-lookup"><span data-stu-id="11458-396">AllocationAmount</span></span>|<span data-ttu-id="11458-397">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-397">win:UInt32</span></span>|<span data-ttu-id="11458-398">Taille de l'allocation, en octets.</span><span class="sxs-lookup"><span data-stu-id="11458-398">The allocation size, in bytes.</span></span> <span data-ttu-id="11458-399">Cette valeur est correcte pour les allocations inférieures à la longueur d'un ULONG (4 294 967 295 octets).</span><span class="sxs-lookup"><span data-stu-id="11458-399">This value is accurate for allocations that are less than the length of a ULONG (4,294,967,295 bytes).</span></span> <span data-ttu-id="11458-400">Si l'allocation est supérieure, ce champ contient une valeur tronquée.</span><span class="sxs-lookup"><span data-stu-id="11458-400">If the allocation is greater, this field contains a truncated value.</span></span> <span data-ttu-id="11458-401">Utilisez `AllocationAmount64` pour les allocations très volumineuses.</span><span class="sxs-lookup"><span data-stu-id="11458-401">Use `AllocationAmount64` for very large allocations.</span></span>|  
|<span data-ttu-id="11458-402">AllocationKind</span><span class="sxs-lookup"><span data-stu-id="11458-402">AllocationKind</span></span>|<span data-ttu-id="11458-403">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-403">win:UInt32</span></span>|<span data-ttu-id="11458-404">0x0 – Allocation de petits objets (l'allocation se fait dans le tas de petits objets).</span><span class="sxs-lookup"><span data-stu-id="11458-404">0x0 - Small object allocation (allocation is in small object heap).</span></span><br /><br /> <span data-ttu-id="11458-405">0x1 – Allocation d'objets volumineux (l'allocation se fait dans le tas des objets volumineux).</span><span class="sxs-lookup"><span data-stu-id="11458-405">0x1 - Large object allocation (allocation is in large object heap).</span></span>|  
|<span data-ttu-id="11458-406">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="11458-406">ClrInstanceID</span></span>|<span data-ttu-id="11458-407">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="11458-407">win:UInt16</span></span>|<span data-ttu-id="11458-408">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="11458-408">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
|<span data-ttu-id="11458-409">AllocationAmount64</span><span class="sxs-lookup"><span data-stu-id="11458-409">AllocationAmount64</span></span>|<span data-ttu-id="11458-410">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="11458-410">win:UInt64</span></span>|<span data-ttu-id="11458-411">Taille de l'allocation, en octets.</span><span class="sxs-lookup"><span data-stu-id="11458-411">The allocation size, in bytes.</span></span> <span data-ttu-id="11458-412">Cette valeur est correcte pour les allocations très volumineuses.</span><span class="sxs-lookup"><span data-stu-id="11458-412">This value is accurate for very large allocations.</span></span>|  
|<span data-ttu-id="11458-413">TypeId</span><span class="sxs-lookup"><span data-stu-id="11458-413">TypeId</span></span>|<span data-ttu-id="11458-414">win:Pointer</span><span class="sxs-lookup"><span data-stu-id="11458-414">win:Pointer</span></span>|<span data-ttu-id="11458-415">Adresse de MethodTable.</span><span class="sxs-lookup"><span data-stu-id="11458-415">The address of the MethodTable.</span></span> <span data-ttu-id="11458-416">Quand plusieurs types d'objets ont été alloués au cours de cet événement, il s'agit de l'adresse de MethodTable qui correspond au dernier objet alloué (l'objet qui a provoqué le dépassement du seuil de 100 Ko).</span><span class="sxs-lookup"><span data-stu-id="11458-416">When there are several types of objects that were allocated during this event, this is the address of the MethodTable that corresponds to the last object allocated (the object that caused the 100 KB threshold to be exceeded).</span></span>|  
|<span data-ttu-id="11458-417">TypeName</span><span class="sxs-lookup"><span data-stu-id="11458-417">TypeName</span></span>|<span data-ttu-id="11458-418">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="11458-418">win:UnicodeString</span></span>|<span data-ttu-id="11458-419">Nom du type ayant été alloué.</span><span class="sxs-lookup"><span data-stu-id="11458-419">The name of the type that was allocated.</span></span> <span data-ttu-id="11458-420">Quand plusieurs types d'objets ont été alloués au cours de cet événement, il s'agit du type du dernier objet alloué (l'objet qui a provoqué le dépassement du seuil de 100 Ko).</span><span class="sxs-lookup"><span data-stu-id="11458-420">When there are several types of objects that were allocated during this event, this is the type of the last object allocated (the object that caused the 100 KB threshold to be exceeded).</span></span>|  
|<span data-ttu-id="11458-421">HeapIndex</span><span class="sxs-lookup"><span data-stu-id="11458-421">HeapIndex</span></span>|<span data-ttu-id="11458-422">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-422">win:UInt32</span></span>|<span data-ttu-id="11458-423">Segment de mémoire où l'objet a été alloué.</span><span class="sxs-lookup"><span data-stu-id="11458-423">The heap where the object was allocated.</span></span> <span data-ttu-id="11458-424">Cette valeur est de 0 (zéro) lors d'une exécution avec le garbage collection pour station de travail.</span><span class="sxs-lookup"><span data-stu-id="11458-424">This value is 0 (zero) when running with workstation garbage collection.</span></span>|  
  
 [<span data-ttu-id="11458-425">Retour au début</span><span class="sxs-lookup"><span data-stu-id="11458-425">Back to top</span></span>](#top)  
  
<a name="gcfinalizersbegin_v1_event"></a>   
## <a name="gcfinalizersbeginv1-event"></a><span data-ttu-id="11458-426">Événement GCFinalizersBegin_V1</span><span class="sxs-lookup"><span data-stu-id="11458-426">GCFinalizersBegin_V1 Event</span></span>  
 <span data-ttu-id="11458-427">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-427">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="11458-428">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-428">Keyword for raising the event</span></span>|<span data-ttu-id="11458-429">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-429">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-430">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-430">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-431">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-431">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-432">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-432">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="11458-433">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-433">Event</span></span>|<span data-ttu-id="11458-434">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-434">Event ID</span></span>|<span data-ttu-id="11458-435">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="11458-435">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCFinalizersBegin_V1`|<span data-ttu-id="11458-436">14</span><span class="sxs-lookup"><span data-stu-id="11458-436">14</span></span>|<span data-ttu-id="11458-437">Début de l'exécution des finaliseurs.</span><span class="sxs-lookup"><span data-stu-id="11458-437">The start of running finalizers.</span></span>|  
  
 <span data-ttu-id="11458-438">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="11458-438">No event data.</span></span>  
  
 [<span data-ttu-id="11458-439">Retour au début</span><span class="sxs-lookup"><span data-stu-id="11458-439">Back to top</span></span>](#top)  
  
<a name="gcfinalizersend_v1_event"></a>   
## <a name="gcfinalizersendv1-event"></a><span data-ttu-id="11458-440">Événement GCFinalizersEnd_V1</span><span class="sxs-lookup"><span data-stu-id="11458-440">GCFinalizersEnd_V1 Event</span></span>  
 <span data-ttu-id="11458-441">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-441">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="11458-442">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-442">Keyword for raising the event</span></span>|<span data-ttu-id="11458-443">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-443">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-444">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-444">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-445">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-445">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-446">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-446">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="11458-447">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-447">Event</span></span>|<span data-ttu-id="11458-448">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-448">Event ID</span></span>|<span data-ttu-id="11458-449">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="11458-449">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCFinalizersEnd_V1`|<span data-ttu-id="11458-450">13</span><span class="sxs-lookup"><span data-stu-id="11458-450">13</span></span>|<span data-ttu-id="11458-451">Fin de l'exécution des finaliseurs.</span><span class="sxs-lookup"><span data-stu-id="11458-451">The end of running finalizers.</span></span>|  
  
 <span data-ttu-id="11458-452">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-452">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="11458-453">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="11458-453">Field name</span></span>|<span data-ttu-id="11458-454">Type de données</span><span class="sxs-lookup"><span data-stu-id="11458-454">Data type</span></span>|<span data-ttu-id="11458-455">Description</span><span class="sxs-lookup"><span data-stu-id="11458-455">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="11458-456">Nombre</span><span class="sxs-lookup"><span data-stu-id="11458-456">Count</span></span>|<span data-ttu-id="11458-457">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="11458-457">win:UInt32</span></span>|<span data-ttu-id="11458-458">Nombre de finaliseurs exécutés.</span><span class="sxs-lookup"><span data-stu-id="11458-458">The number of finalizers that were run.</span></span>|  
|<span data-ttu-id="11458-459">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="11458-459">ClrInstanceID</span></span>|<span data-ttu-id="11458-460">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="11458-460">win:UInt16</span></span>|<span data-ttu-id="11458-461">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="11458-461">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="11458-462">Retour au début</span><span class="sxs-lookup"><span data-stu-id="11458-462">Back to top</span></span>](#top)  
  
<a name="gccreateconcurrentthread_v1_event"></a>   
## <a name="gccreateconcurrentthreadv1-event"></a><span data-ttu-id="11458-463">Événement GCCreateConcurrentThread_V1</span><span class="sxs-lookup"><span data-stu-id="11458-463">GCCreateConcurrentThread_V1 Event</span></span>  
 <span data-ttu-id="11458-464">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-464">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="11458-465">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-465">Keyword for raising the event</span></span>|<span data-ttu-id="11458-466">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-466">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-467">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-467">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-468">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-468">Informational (4)</span></span>|  
|<span data-ttu-id="11458-469">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="11458-469">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="11458-470">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-470">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-471">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-471">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="11458-472">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-472">Event</span></span>|<span data-ttu-id="11458-473">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-473">Event ID</span></span>|<span data-ttu-id="11458-474">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="11458-474">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCCreateConcurrentThread_V1`|<span data-ttu-id="11458-475">11</span><span class="sxs-lookup"><span data-stu-id="11458-475">11</span></span>|<span data-ttu-id="11458-476">Un thread de garbage collection simultané a été créé.</span><span class="sxs-lookup"><span data-stu-id="11458-476">Concurrent garbage collection thread was created.</span></span>|  
  
 <span data-ttu-id="11458-477">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="11458-477">No event data.</span></span>  
  
 [<span data-ttu-id="11458-478">Retour au début</span><span class="sxs-lookup"><span data-stu-id="11458-478">Back to top</span></span>](#top)  
  
<a name="gcterminateconcurrentthread_v1_event"></a>   
## <a name="gcterminateconcurrentthreadv1-event"></a><span data-ttu-id="11458-479">Événement GCTerminateConcurrentThread_V1</span><span class="sxs-lookup"><span data-stu-id="11458-479">GCTerminateConcurrentThread_V1 Event</span></span>  
 <span data-ttu-id="11458-480">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="11458-480">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="11458-481">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="11458-481">Keyword for raising the event</span></span>|<span data-ttu-id="11458-482">Niveau</span><span class="sxs-lookup"><span data-stu-id="11458-482">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="11458-483">`GCKeyword` (0x1)</span><span class="sxs-lookup"><span data-stu-id="11458-483">`GCKeyword` (0x1)</span></span>|<span data-ttu-id="11458-484">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-484">Informational (4)</span></span>|  
|<span data-ttu-id="11458-485">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="11458-485">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="11458-486">Informatif (4)</span><span class="sxs-lookup"><span data-stu-id="11458-486">Informational (4)</span></span>|  
  
 <span data-ttu-id="11458-487">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="11458-487">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="11458-488">Événement</span><span class="sxs-lookup"><span data-stu-id="11458-488">Event</span></span>|<span data-ttu-id="11458-489">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="11458-489">Event ID</span></span>|<span data-ttu-id="11458-490">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="11458-490">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`GCTerminateConcurrentThread_V1`|<span data-ttu-id="11458-491">12</span><span class="sxs-lookup"><span data-stu-id="11458-491">12</span></span>|<span data-ttu-id="11458-492">Un thread de garbage collection simultané s'est terminé.</span><span class="sxs-lookup"><span data-stu-id="11458-492">Concurrent garbage collection thread was terminated.</span></span>|  
  
 <span data-ttu-id="11458-493">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="11458-493">No event data.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="11458-494">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11458-494">See also</span></span>

- [<span data-ttu-id="11458-495">Événements ETW du CLR</span><span class="sxs-lookup"><span data-stu-id="11458-495">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
