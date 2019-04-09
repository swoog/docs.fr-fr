---
title: Événements ETW d'analyse de ressource de domaine d'application
ms.date: 03/30/2017
helpviewer_keywords:
- ETW, application domain monitoring events
- application domain monitoring events [.NET Framework]
ms.assetid: d38ff268-a2ee-434e-b504-d570880e0289
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2bb2b0dd95877fc6492f6d23a19c14688cd78f7c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59133820"
---
# <a name="application-domain-resource-monitoring-arm-etw-events"></a><span data-ttu-id="70118-102">Événements ETW d'analyse de ressource de domaine d'application</span><span class="sxs-lookup"><span data-stu-id="70118-102">Application Domain Resource Monitoring (ARM) ETW Events</span></span>
<a name="top"></a> <span data-ttu-id="70118-103">Ces événements fournissent des informations de diagnostic détaillées sur l'état d'un domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="70118-103">These events provide detailed diagnostic information about the state of an application domain.</span></span> <span data-ttu-id="70118-104">Vous pouvez utiliser ces événements ou la fonctionnalité ARM d'analyse de ressource de domaine d'application pour obtenir les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="70118-104">You can use these events or use the application domain resource monitoring (ARM) feature to obtain the same information.</span></span>  
  
 <span data-ttu-id="70118-105">Cette catégorie comprend les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="70118-105">This category consists of the following events:</span></span>  
  
-   [<span data-ttu-id="70118-106">Événement ThreadCreated</span><span class="sxs-lookup"><span data-stu-id="70118-106">ThreadCreated Event</span></span>](#threadcreated_event)  
  
-   [<span data-ttu-id="70118-107">Événement AppDomainMemAllocated</span><span class="sxs-lookup"><span data-stu-id="70118-107">AppDomainMemAllocated Event</span></span>](#appdomainmemallocated_event)  
  
-   [<span data-ttu-id="70118-108">Événement AppDomainMemSurvived</span><span class="sxs-lookup"><span data-stu-id="70118-108">AppDomainMemSurvived Event</span></span>](#appdomainmemsurvived_event)  
  
-   [<span data-ttu-id="70118-109">Événement ThreadAppDomainEnter</span><span class="sxs-lookup"><span data-stu-id="70118-109">ThreadAppDomainEnter Event</span></span>](#threadappdomainenter_event)  
  
-   [<span data-ttu-id="70118-110">Événement ThreadTerminated</span><span class="sxs-lookup"><span data-stu-id="70118-110">ThreadTerminated Event</span></span>](#threadterminated_event)  
  
<a name="threadcreated_event"></a>   
## <a name="threadcreated-event"></a><span data-ttu-id="70118-111">Événement ThreadCreated</span><span class="sxs-lookup"><span data-stu-id="70118-111">ThreadCreated Event</span></span>  
 <span data-ttu-id="70118-112">Cet événement est également déclenché sous le fournisseur d'arrêt en tant que `ThreadDC` (sous le mot clé `AppDomainResourceManagementRundownKeyword` ).</span><span class="sxs-lookup"><span data-stu-id="70118-112">This event is also raised  under the rundown provider as `ThreadDC` (under the `AppDomainResourceManagementRundownKeyword` keyword).</span></span> <span data-ttu-id="70118-113">Il s’agit du seul événement déclenché sous le fournisseur d'arrêt dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="70118-113">This is the only event that is raised under the rundown provider in this category.</span></span>  
  
 <span data-ttu-id="70118-114">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="70118-114">The following table shows the keyword and level.</span></span> <span data-ttu-id="70118-115">(Pour plus d'informations, consultez [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span><span class="sxs-lookup"><span data-stu-id="70118-115">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="70118-116">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="70118-116">Keyword for raising the event</span></span>|<span data-ttu-id="70118-117">Niveau</span><span class="sxs-lookup"><span data-stu-id="70118-117">Level</span></span>|  
|-----------------------------------|-----------|  
|`AppDomainResourceManagementKeyword` <span data-ttu-id="70118-118">(0 x 800)</span><span class="sxs-lookup"><span data-stu-id="70118-118">(0x800)</span></span>|<span data-ttu-id="70118-119">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="70118-119">Informational(4)</span></span>|  
|`ThreadingKeyword` <span data-ttu-id="70118-120">(0 x 10000)</span><span class="sxs-lookup"><span data-stu-id="70118-120">(0x10000)</span></span>|<span data-ttu-id="70118-121">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="70118-121">Informational(4)</span></span>|  
  
 <span data-ttu-id="70118-122">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="70118-122">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="70118-123">Événement</span><span class="sxs-lookup"><span data-stu-id="70118-123">Event</span></span>|<span data-ttu-id="70118-124">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="70118-124">Event ID</span></span>|<span data-ttu-id="70118-125">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="70118-125">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ThreadCreated`|<span data-ttu-id="70118-126">85</span><span class="sxs-lookup"><span data-stu-id="70118-126">85</span></span>|<span data-ttu-id="70118-127">Un thread a été créé pour le domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="70118-127">A thread was created for the application domain.</span></span>|  
  
 <span data-ttu-id="70118-128">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="70118-128">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="70118-129">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="70118-129">Field name</span></span>|<span data-ttu-id="70118-130">Type de données</span><span class="sxs-lookup"><span data-stu-id="70118-130">Data type</span></span>|<span data-ttu-id="70118-131">Description</span><span class="sxs-lookup"><span data-stu-id="70118-131">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="70118-132">ThreadID</span><span class="sxs-lookup"><span data-stu-id="70118-132">ThreadID</span></span>|<span data-ttu-id="70118-133">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="70118-133">win:UInt64</span></span>|<span data-ttu-id="70118-134">ID du thread qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="70118-134">ID of the thread that was created.</span></span>|  
|<span data-ttu-id="70118-135">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="70118-135">AppDomainID</span></span>|<span data-ttu-id="70118-136">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="70118-136">win:UInt64</span></span>|<span data-ttu-id="70118-137">Identificateur du domaine d'application pour lequel l'activité du thread est signalée.</span><span class="sxs-lookup"><span data-stu-id="70118-137">Identifier of the application domain for which thread activity is being reported.</span></span>|  
|<span data-ttu-id="70118-138">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="70118-138">Flags</span></span>|<span data-ttu-id="70118-139">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="70118-139">win:UInt32</span></span>|<span data-ttu-id="70118-140">Indicateurs de création de thread.</span><span class="sxs-lookup"><span data-stu-id="70118-140">Thread creation flags.</span></span>|  
|<span data-ttu-id="70118-141">ManagedThreadIndex</span><span class="sxs-lookup"><span data-stu-id="70118-141">ManagedThreadIndex</span></span>|<span data-ttu-id="70118-142">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="70118-142">win:UInt32</span></span>|<span data-ttu-id="70118-143">Index managé du thread qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="70118-143">Managed index of the thread that was created.</span></span>|  
|<span data-ttu-id="70118-144">OSThreadID</span><span class="sxs-lookup"><span data-stu-id="70118-144">OSThreadID</span></span>|<span data-ttu-id="70118-145">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="70118-145">win:UInt32</span></span>|<span data-ttu-id="70118-146">ID de système d’exploitation du thread qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="70118-146">Operating system ID of the thread that was created.</span></span>|  
|<span data-ttu-id="70118-147">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="70118-147">ClrInstanceID</span></span>|<span data-ttu-id="70118-148">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="70118-148">win:UInt16</span></span>|<span data-ttu-id="70118-149">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="70118-149">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="70118-150">Retour au début</span><span class="sxs-lookup"><span data-stu-id="70118-150">Back to top</span></span>](#top)  
  
<a name="appdomainmemallocated_event"></a>   
## <a name="appdomainmemallocated-event"></a><span data-ttu-id="70118-151">Événement AppDomainMemAllocated</span><span class="sxs-lookup"><span data-stu-id="70118-151">AppDomainMemAllocated Event</span></span>  
 <span data-ttu-id="70118-152">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="70118-152">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="70118-153">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="70118-153">Keyword for raising the event</span></span>|<span data-ttu-id="70118-154">Niveau</span><span class="sxs-lookup"><span data-stu-id="70118-154">Level</span></span>|  
|-----------------------------------|-----------|  
|`AppDomainResourceManagementKeyword` <span data-ttu-id="70118-155">(0 x 800)</span><span class="sxs-lookup"><span data-stu-id="70118-155">(0x800)</span></span>|<span data-ttu-id="70118-156">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="70118-156">Informational(4)</span></span>|  
  
 <span data-ttu-id="70118-157">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="70118-157">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="70118-158">Événement</span><span class="sxs-lookup"><span data-stu-id="70118-158">Event</span></span>|<span data-ttu-id="70118-159">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="70118-159">Event ID</span></span>|<span data-ttu-id="70118-160">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="70118-160">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`AppDomainMemAllocated`|<span data-ttu-id="70118-161">83</span><span class="sxs-lookup"><span data-stu-id="70118-161">83</span></span>|<span data-ttu-id="70118-162">Chaque bloc de 4 Mo de mémoire (environ) est alloué dans le domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="70118-162">Every 4 MB of memory (approximately) is allocated in the application domain.</span></span>|  
  
 <span data-ttu-id="70118-163">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="70118-163">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="70118-164">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="70118-164">Field name</span></span>|<span data-ttu-id="70118-165">Type de données</span><span class="sxs-lookup"><span data-stu-id="70118-165">Data type</span></span>|<span data-ttu-id="70118-166">Description</span><span class="sxs-lookup"><span data-stu-id="70118-166">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="70118-167">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="70118-167">AppDomainID</span></span>|<span data-ttu-id="70118-168">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="70118-168">win:UInt64</span></span>|<span data-ttu-id="70118-169">Identificateur du domaine d'application pour lequel l'utilisation des ressources est signalée.</span><span class="sxs-lookup"><span data-stu-id="70118-169">Identifier of the application domain for which resource usage is being reported.</span></span>|  
|<span data-ttu-id="70118-170">Allocated</span><span class="sxs-lookup"><span data-stu-id="70118-170">Allocated</span></span>|<span data-ttu-id="70118-171">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="70118-171">win:UInt64</span></span>|<span data-ttu-id="70118-172">Nombre total d'octets alloués dans ce domaine d'application depuis sa création (la quantité de mémoire libérée n'est pas soustraite).</span><span class="sxs-lookup"><span data-stu-id="70118-172">The total number of bytes allocated in this application domain since the application domain was created (the amount of freed memory is not subtracted).</span></span>|  
|<span data-ttu-id="70118-173">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="70118-173">ClrInstanceID</span></span>|<span data-ttu-id="70118-174">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="70118-174">win:UInt16</span></span>|<span data-ttu-id="70118-175">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="70118-175">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="70118-176">Retour au début</span><span class="sxs-lookup"><span data-stu-id="70118-176">Back to top</span></span>](#top)  
  
<a name="appdomainmemsurvived_event"></a>   
## <a name="appdomainmemsurvived-event"></a><span data-ttu-id="70118-177">Événement AppDomainMemSurvived</span><span class="sxs-lookup"><span data-stu-id="70118-177">AppDomainMemSurvived Event</span></span>  
 <span data-ttu-id="70118-178">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="70118-178">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="70118-179">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="70118-179">Keyword for raising the event</span></span>|<span data-ttu-id="70118-180">Niveau</span><span class="sxs-lookup"><span data-stu-id="70118-180">Level</span></span>|  
|-----------------------------------|-----------|  
|`AppDomainResourceManagementKeyword` <span data-ttu-id="70118-181">(0 x 800)</span><span class="sxs-lookup"><span data-stu-id="70118-181">(0x800)</span></span>|<span data-ttu-id="70118-182">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="70118-182">Informational(4)</span></span>|  
  
 <span data-ttu-id="70118-183">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="70118-183">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="70118-184">Événement</span><span class="sxs-lookup"><span data-stu-id="70118-184">Event</span></span>|<span data-ttu-id="70118-185">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="70118-185">Event ID</span></span>|<span data-ttu-id="70118-186">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="70118-186">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`AppDomainMemSurvived`|<span data-ttu-id="70118-187">84</span><span class="sxs-lookup"><span data-stu-id="70118-187">84</span></span>|<span data-ttu-id="70118-188">Chaque garbage collection est terminé.</span><span class="sxs-lookup"><span data-stu-id="70118-188">Each garbage collection has ended.</span></span>|  
  
 <span data-ttu-id="70118-189">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="70118-189">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="70118-190">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="70118-190">Field name</span></span>|<span data-ttu-id="70118-191">Type de données</span><span class="sxs-lookup"><span data-stu-id="70118-191">Data type</span></span>|<span data-ttu-id="70118-192">Description</span><span class="sxs-lookup"><span data-stu-id="70118-192">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="70118-193">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="70118-193">AppDomainID</span></span>|<span data-ttu-id="70118-194">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="70118-194">win:UInt64</span></span>|<span data-ttu-id="70118-195">Identificateur du domaine pour lequel l’utilisation des ressources est signalée.</span><span class="sxs-lookup"><span data-stu-id="70118-195">Identifier of the domain for which resource usage is being reported.</span></span>|  
|<span data-ttu-id="70118-196">Survived</span><span class="sxs-lookup"><span data-stu-id="70118-196">Survived</span></span>|<span data-ttu-id="70118-197">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="70118-197">win:UInt64</span></span>|<span data-ttu-id="70118-198">Nombre d'octets ayant survécu après la dernière collection et qui sont conservés par ce domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="70118-198">The number of bytes that survived after the last collection and that are known to be held by this application domain.</span></span> <span data-ttu-id="70118-199">Ce nombre est exact et complet après une collection complète, mais peut être incomplet après une collection éphémère.</span><span class="sxs-lookup"><span data-stu-id="70118-199">This number is accurate and complete after a full collection, but may be incomplete after an ephemeral collection.</span></span>|  
|<span data-ttu-id="70118-200">ProcessSurvived</span><span class="sxs-lookup"><span data-stu-id="70118-200">ProcessSurvived</span></span>|<span data-ttu-id="70118-201">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="70118-201">win:UInt64</span></span>|<span data-ttu-id="70118-202">Nombre total d'octets qui ont survécu à la dernière collection.</span><span class="sxs-lookup"><span data-stu-id="70118-202">The total bytes that survived from the last collection.</span></span> <span data-ttu-id="70118-203">Après une collection complète, ce nombre représente le nombre d'octets maintenus actifs dans les tas managés.</span><span class="sxs-lookup"><span data-stu-id="70118-203">After a full collection, this number represents the number of bytes being held live in managed heaps.</span></span> <span data-ttu-id="70118-204">Après une collection éphémère, ce nombre représente le nombre d'octets maintenus actifs dans les générations éphémères.</span><span class="sxs-lookup"><span data-stu-id="70118-204">After an ephemeral collection, this number represents the number of bytes held live in ephemeral generations.</span></span>|  
|<span data-ttu-id="70118-205">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="70118-205">ClrInstanceID</span></span>|<span data-ttu-id="70118-206">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="70118-206">win:UInt16</span></span>|<span data-ttu-id="70118-207">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="70118-207">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="70118-208">Retour au début</span><span class="sxs-lookup"><span data-stu-id="70118-208">Back to top</span></span>](#top)  
  
<a name="threadappdomainenter_event"></a>   
## <a name="threadappdomainenter-event"></a><span data-ttu-id="70118-209">Événement ThreadAppDomainEnter</span><span class="sxs-lookup"><span data-stu-id="70118-209">ThreadAppDomainEnter Event</span></span>  
 <span data-ttu-id="70118-210">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="70118-210">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="70118-211">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="70118-211">Keyword for raising the event</span></span>|<span data-ttu-id="70118-212">Niveau</span><span class="sxs-lookup"><span data-stu-id="70118-212">Level</span></span>|  
|-----------------------------------|-----------|  
|`AppDomainResourceManagementKeyword` <span data-ttu-id="70118-213">(0 x 800)</span><span class="sxs-lookup"><span data-stu-id="70118-213">(0x800)</span></span>|<span data-ttu-id="70118-214">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="70118-214">Informational(4)</span></span>|  
|`ThreadingKeyword` <span data-ttu-id="70118-215">(0 x 10000)</span><span class="sxs-lookup"><span data-stu-id="70118-215">(0x10000)</span></span>|<span data-ttu-id="70118-216">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="70118-216">Informational(4)</span></span>|  
  
 <span data-ttu-id="70118-217">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="70118-217">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="70118-218">Événement</span><span class="sxs-lookup"><span data-stu-id="70118-218">Event</span></span>|<span data-ttu-id="70118-219">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="70118-219">Event ID</span></span>|<span data-ttu-id="70118-220">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="70118-220">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ThreadAppDomainEnter`|<span data-ttu-id="70118-221">87</span><span class="sxs-lookup"><span data-stu-id="70118-221">87</span></span>|<span data-ttu-id="70118-222">Un thread entre dans un domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="70118-222">A thread enters an application domain.</span></span>|  
  
 <span data-ttu-id="70118-223">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="70118-223">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="70118-224">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="70118-224">Field name</span></span>|<span data-ttu-id="70118-225">Type de données</span><span class="sxs-lookup"><span data-stu-id="70118-225">Data type</span></span>|<span data-ttu-id="70118-226">Description</span><span class="sxs-lookup"><span data-stu-id="70118-226">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="70118-227">ThreadID</span><span class="sxs-lookup"><span data-stu-id="70118-227">ThreadID</span></span>|<span data-ttu-id="70118-228">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="70118-228">win:UInt64</span></span>|<span data-ttu-id="70118-229">Identificateur du thread.</span><span class="sxs-lookup"><span data-stu-id="70118-229">The thread identifier.</span></span>|  
|<span data-ttu-id="70118-230">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="70118-230">AppDomainID</span></span>|<span data-ttu-id="70118-231">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="70118-231">win:UInt64</span></span>|<span data-ttu-id="70118-232">Identificateur du domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="70118-232">The application domain identifier.</span></span>|  
|<span data-ttu-id="70118-233">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="70118-233">ClrInstanceID</span></span>|<span data-ttu-id="70118-234">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="70118-234">win:UInt16</span></span>|<span data-ttu-id="70118-235">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="70118-235">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="70118-236">Retour au début</span><span class="sxs-lookup"><span data-stu-id="70118-236">Back to top</span></span>](#top)  
  
<a name="threadterminated_event"></a>   
## <a name="threadterminated-event"></a><span data-ttu-id="70118-237">Événement ThreadTerminated</span><span class="sxs-lookup"><span data-stu-id="70118-237">ThreadTerminated Event</span></span>  
 <span data-ttu-id="70118-238">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="70118-238">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="70118-239">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="70118-239">Keyword for raising the event</span></span>|<span data-ttu-id="70118-240">Niveau</span><span class="sxs-lookup"><span data-stu-id="70118-240">Level</span></span>|  
|-----------------------------------|-----------|  
|`AppDomainResourceManagementKeyword` <span data-ttu-id="70118-241">(0 x 800)</span><span class="sxs-lookup"><span data-stu-id="70118-241">(0x800)</span></span>|<span data-ttu-id="70118-242">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="70118-242">Informational(4)</span></span>|  
|`ThreadingKeyword` <span data-ttu-id="70118-243">(0 x 10000)</span><span class="sxs-lookup"><span data-stu-id="70118-243">(0x10000)</span></span>|<span data-ttu-id="70118-244">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="70118-244">Informational(4)</span></span>|  
  
 <span data-ttu-id="70118-245">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="70118-245">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="70118-246">Événement</span><span class="sxs-lookup"><span data-stu-id="70118-246">Event</span></span>|<span data-ttu-id="70118-247">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="70118-247">Event ID</span></span>|<span data-ttu-id="70118-248">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="70118-248">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ThreadTerminated`|<span data-ttu-id="70118-249">86</span><span class="sxs-lookup"><span data-stu-id="70118-249">86</span></span>|<span data-ttu-id="70118-250">Un thread se termine.</span><span class="sxs-lookup"><span data-stu-id="70118-250">A thread terminates.</span></span>|  
  
 <span data-ttu-id="70118-251">Le tableau ci-dessous montre les données d’événements.</span><span class="sxs-lookup"><span data-stu-id="70118-251">The following table shows the event data:</span></span>  
  
|<span data-ttu-id="70118-252">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="70118-252">Field name</span></span>|<span data-ttu-id="70118-253">Type de données</span><span class="sxs-lookup"><span data-stu-id="70118-253">Data type</span></span>|<span data-ttu-id="70118-254">Description</span><span class="sxs-lookup"><span data-stu-id="70118-254">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="70118-255">ThreadID</span><span class="sxs-lookup"><span data-stu-id="70118-255">ThreadID</span></span>|<span data-ttu-id="70118-256">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="70118-256">win:UInt64</span></span>|<span data-ttu-id="70118-257">Identificateur du thread.</span><span class="sxs-lookup"><span data-stu-id="70118-257">The thread identifier.</span></span>|  
|<span data-ttu-id="70118-258">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="70118-258">AppDomainID</span></span>|<span data-ttu-id="70118-259">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="70118-259">win:UInt64</span></span>|<span data-ttu-id="70118-260">Identificateur du domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="70118-260">The application domain identifier.</span></span>|  
|<span data-ttu-id="70118-261">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="70118-261">ClrInstanceID</span></span>|<span data-ttu-id="70118-262">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="70118-262">win:UInt16</span></span>|<span data-ttu-id="70118-263">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="70118-263">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="70118-264">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70118-264">See also</span></span>

- [<span data-ttu-id="70118-265">Événements ETW du CLR</span><span class="sxs-lookup"><span data-stu-id="70118-265">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
