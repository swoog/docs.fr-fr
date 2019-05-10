---
title: Événements ETW d'analyse de ressource de domaine d'application
ms.date: 03/30/2017
helpviewer_keywords:
- ETW, application domain monitoring events
- application domain monitoring events [.NET Framework]
ms.assetid: d38ff268-a2ee-434e-b504-d570880e0289
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ac396e1a5b83f33068266553024c37ef436c150d
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64616632"
---
# <a name="application-domain-resource-monitoring-arm-etw-events"></a><span data-ttu-id="3c809-102">Événements ETW d'analyse de ressource de domaine d'application</span><span class="sxs-lookup"><span data-stu-id="3c809-102">Application Domain Resource Monitoring (ARM) ETW Events</span></span>
<a name="top"></a> <span data-ttu-id="3c809-103">Ces événements fournissent des informations de diagnostic détaillées sur l'état d'un domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="3c809-103">These events provide detailed diagnostic information about the state of an application domain.</span></span> <span data-ttu-id="3c809-104">Vous pouvez utiliser ces événements ou la fonctionnalité ARM d'analyse de ressource de domaine d'application pour obtenir les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="3c809-104">You can use these events or use the application domain resource monitoring (ARM) feature to obtain the same information.</span></span>  
  
 <span data-ttu-id="3c809-105">Cette catégorie comprend les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="3c809-105">This category consists of the following events:</span></span>  
  
- [<span data-ttu-id="3c809-106">Événement ThreadCreated</span><span class="sxs-lookup"><span data-stu-id="3c809-106">ThreadCreated Event</span></span>](#threadcreated_event)  
  
- [<span data-ttu-id="3c809-107">Événement AppDomainMemAllocated</span><span class="sxs-lookup"><span data-stu-id="3c809-107">AppDomainMemAllocated Event</span></span>](#appdomainmemallocated_event)  
  
- [<span data-ttu-id="3c809-108">Événement AppDomainMemSurvived</span><span class="sxs-lookup"><span data-stu-id="3c809-108">AppDomainMemSurvived Event</span></span>](#appdomainmemsurvived_event)  
  
- [<span data-ttu-id="3c809-109">Événement ThreadAppDomainEnter</span><span class="sxs-lookup"><span data-stu-id="3c809-109">ThreadAppDomainEnter Event</span></span>](#threadappdomainenter_event)  
  
- [<span data-ttu-id="3c809-110">Événement ThreadTerminated</span><span class="sxs-lookup"><span data-stu-id="3c809-110">ThreadTerminated Event</span></span>](#threadterminated_event)  
  
<a name="threadcreated_event"></a>   
## <a name="threadcreated-event"></a><span data-ttu-id="3c809-111">Événement ThreadCreated</span><span class="sxs-lookup"><span data-stu-id="3c809-111">ThreadCreated Event</span></span>  
 <span data-ttu-id="3c809-112">Cet événement est également déclenché sous le fournisseur d'arrêt en tant que `ThreadDC` (sous le mot clé `AppDomainResourceManagementRundownKeyword` ).</span><span class="sxs-lookup"><span data-stu-id="3c809-112">This event is also raised  under the rundown provider as `ThreadDC` (under the `AppDomainResourceManagementRundownKeyword` keyword).</span></span> <span data-ttu-id="3c809-113">Il s’agit du seul événement déclenché sous le fournisseur d'arrêt dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="3c809-113">This is the only event that is raised under the rundown provider in this category.</span></span>  
  
 <span data-ttu-id="3c809-114">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="3c809-114">The following table shows the keyword and level.</span></span> <span data-ttu-id="3c809-115">(Pour plus d'informations, consultez [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span><span class="sxs-lookup"><span data-stu-id="3c809-115">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="3c809-116">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="3c809-116">Keyword for raising the event</span></span>|<span data-ttu-id="3c809-117">Niveau</span><span class="sxs-lookup"><span data-stu-id="3c809-117">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="3c809-118">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="3c809-118">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="3c809-119">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="3c809-119">Informational(4)</span></span>|  
|<span data-ttu-id="3c809-120">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="3c809-120">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="3c809-121">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="3c809-121">Informational(4)</span></span>|  
  
 <span data-ttu-id="3c809-122">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="3c809-122">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="3c809-123">Événement</span><span class="sxs-lookup"><span data-stu-id="3c809-123">Event</span></span>|<span data-ttu-id="3c809-124">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="3c809-124">Event ID</span></span>|<span data-ttu-id="3c809-125">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="3c809-125">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ThreadCreated`|<span data-ttu-id="3c809-126">85</span><span class="sxs-lookup"><span data-stu-id="3c809-126">85</span></span>|<span data-ttu-id="3c809-127">Un thread a été créé pour le domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="3c809-127">A thread was created for the application domain.</span></span>|  
  
 <span data-ttu-id="3c809-128">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="3c809-128">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="3c809-129">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="3c809-129">Field name</span></span>|<span data-ttu-id="3c809-130">Type de données</span><span class="sxs-lookup"><span data-stu-id="3c809-130">Data type</span></span>|<span data-ttu-id="3c809-131">Description</span><span class="sxs-lookup"><span data-stu-id="3c809-131">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="3c809-132">ThreadID</span><span class="sxs-lookup"><span data-stu-id="3c809-132">ThreadID</span></span>|<span data-ttu-id="3c809-133">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="3c809-133">win:UInt64</span></span>|<span data-ttu-id="3c809-134">ID du thread qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="3c809-134">ID of the thread that was created.</span></span>|  
|<span data-ttu-id="3c809-135">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="3c809-135">AppDomainID</span></span>|<span data-ttu-id="3c809-136">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="3c809-136">win:UInt64</span></span>|<span data-ttu-id="3c809-137">Identificateur du domaine d'application pour lequel l'activité du thread est signalée.</span><span class="sxs-lookup"><span data-stu-id="3c809-137">Identifier of the application domain for which thread activity is being reported.</span></span>|  
|<span data-ttu-id="3c809-138">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="3c809-138">Flags</span></span>|<span data-ttu-id="3c809-139">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="3c809-139">win:UInt32</span></span>|<span data-ttu-id="3c809-140">Indicateurs de création de thread.</span><span class="sxs-lookup"><span data-stu-id="3c809-140">Thread creation flags.</span></span>|  
|<span data-ttu-id="3c809-141">ManagedThreadIndex</span><span class="sxs-lookup"><span data-stu-id="3c809-141">ManagedThreadIndex</span></span>|<span data-ttu-id="3c809-142">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="3c809-142">win:UInt32</span></span>|<span data-ttu-id="3c809-143">Index managé du thread qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="3c809-143">Managed index of the thread that was created.</span></span>|  
|<span data-ttu-id="3c809-144">OSThreadID</span><span class="sxs-lookup"><span data-stu-id="3c809-144">OSThreadID</span></span>|<span data-ttu-id="3c809-145">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="3c809-145">win:UInt32</span></span>|<span data-ttu-id="3c809-146">ID de système d’exploitation du thread qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="3c809-146">Operating system ID of the thread that was created.</span></span>|  
|<span data-ttu-id="3c809-147">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="3c809-147">ClrInstanceID</span></span>|<span data-ttu-id="3c809-148">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="3c809-148">win:UInt16</span></span>|<span data-ttu-id="3c809-149">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="3c809-149">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="3c809-150">Retour au début</span><span class="sxs-lookup"><span data-stu-id="3c809-150">Back to top</span></span>](#top)  
  
<a name="appdomainmemallocated_event"></a>   
## <a name="appdomainmemallocated-event"></a><span data-ttu-id="3c809-151">Événement AppDomainMemAllocated</span><span class="sxs-lookup"><span data-stu-id="3c809-151">AppDomainMemAllocated Event</span></span>  
 <span data-ttu-id="3c809-152">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="3c809-152">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="3c809-153">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="3c809-153">Keyword for raising the event</span></span>|<span data-ttu-id="3c809-154">Niveau</span><span class="sxs-lookup"><span data-stu-id="3c809-154">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="3c809-155">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="3c809-155">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="3c809-156">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="3c809-156">Informational(4)</span></span>|  
  
 <span data-ttu-id="3c809-157">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="3c809-157">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="3c809-158">Événement</span><span class="sxs-lookup"><span data-stu-id="3c809-158">Event</span></span>|<span data-ttu-id="3c809-159">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="3c809-159">Event ID</span></span>|<span data-ttu-id="3c809-160">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="3c809-160">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`AppDomainMemAllocated`|<span data-ttu-id="3c809-161">83</span><span class="sxs-lookup"><span data-stu-id="3c809-161">83</span></span>|<span data-ttu-id="3c809-162">Chaque bloc de 4 Mo de mémoire (environ) est alloué dans le domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="3c809-162">Every 4 MB of memory (approximately) is allocated in the application domain.</span></span>|  
  
 <span data-ttu-id="3c809-163">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="3c809-163">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="3c809-164">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="3c809-164">Field name</span></span>|<span data-ttu-id="3c809-165">Type de données</span><span class="sxs-lookup"><span data-stu-id="3c809-165">Data type</span></span>|<span data-ttu-id="3c809-166">Description</span><span class="sxs-lookup"><span data-stu-id="3c809-166">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="3c809-167">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="3c809-167">AppDomainID</span></span>|<span data-ttu-id="3c809-168">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="3c809-168">win:UInt64</span></span>|<span data-ttu-id="3c809-169">Identificateur du domaine d'application pour lequel l'utilisation des ressources est signalée.</span><span class="sxs-lookup"><span data-stu-id="3c809-169">Identifier of the application domain for which resource usage is being reported.</span></span>|  
|<span data-ttu-id="3c809-170">Allocated</span><span class="sxs-lookup"><span data-stu-id="3c809-170">Allocated</span></span>|<span data-ttu-id="3c809-171">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="3c809-171">win:UInt64</span></span>|<span data-ttu-id="3c809-172">Nombre total d'octets alloués dans ce domaine d'application depuis sa création (la quantité de mémoire libérée n'est pas soustraite).</span><span class="sxs-lookup"><span data-stu-id="3c809-172">The total number of bytes allocated in this application domain since the application domain was created (the amount of freed memory is not subtracted).</span></span>|  
|<span data-ttu-id="3c809-173">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="3c809-173">ClrInstanceID</span></span>|<span data-ttu-id="3c809-174">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="3c809-174">win:UInt16</span></span>|<span data-ttu-id="3c809-175">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="3c809-175">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="3c809-176">Retour au début</span><span class="sxs-lookup"><span data-stu-id="3c809-176">Back to top</span></span>](#top)  
  
<a name="appdomainmemsurvived_event"></a>   
## <a name="appdomainmemsurvived-event"></a><span data-ttu-id="3c809-177">Événement AppDomainMemSurvived</span><span class="sxs-lookup"><span data-stu-id="3c809-177">AppDomainMemSurvived Event</span></span>  
 <span data-ttu-id="3c809-178">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="3c809-178">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="3c809-179">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="3c809-179">Keyword for raising the event</span></span>|<span data-ttu-id="3c809-180">Niveau</span><span class="sxs-lookup"><span data-stu-id="3c809-180">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="3c809-181">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="3c809-181">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="3c809-182">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="3c809-182">Informational(4)</span></span>|  
  
 <span data-ttu-id="3c809-183">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="3c809-183">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="3c809-184">Événement</span><span class="sxs-lookup"><span data-stu-id="3c809-184">Event</span></span>|<span data-ttu-id="3c809-185">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="3c809-185">Event ID</span></span>|<span data-ttu-id="3c809-186">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="3c809-186">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`AppDomainMemSurvived`|<span data-ttu-id="3c809-187">84</span><span class="sxs-lookup"><span data-stu-id="3c809-187">84</span></span>|<span data-ttu-id="3c809-188">Chaque garbage collection est terminé.</span><span class="sxs-lookup"><span data-stu-id="3c809-188">Each garbage collection has ended.</span></span>|  
  
 <span data-ttu-id="3c809-189">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="3c809-189">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="3c809-190">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="3c809-190">Field name</span></span>|<span data-ttu-id="3c809-191">Type de données</span><span class="sxs-lookup"><span data-stu-id="3c809-191">Data type</span></span>|<span data-ttu-id="3c809-192">Description</span><span class="sxs-lookup"><span data-stu-id="3c809-192">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="3c809-193">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="3c809-193">AppDomainID</span></span>|<span data-ttu-id="3c809-194">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="3c809-194">win:UInt64</span></span>|<span data-ttu-id="3c809-195">Identificateur du domaine pour lequel l’utilisation des ressources est signalée.</span><span class="sxs-lookup"><span data-stu-id="3c809-195">Identifier of the domain for which resource usage is being reported.</span></span>|  
|<span data-ttu-id="3c809-196">Survived</span><span class="sxs-lookup"><span data-stu-id="3c809-196">Survived</span></span>|<span data-ttu-id="3c809-197">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="3c809-197">win:UInt64</span></span>|<span data-ttu-id="3c809-198">Nombre d'octets ayant survécu après la dernière collection et qui sont conservés par ce domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="3c809-198">The number of bytes that survived after the last collection and that are known to be held by this application domain.</span></span> <span data-ttu-id="3c809-199">Ce nombre est exact et complet après une collection complète, mais peut être incomplet après une collection éphémère.</span><span class="sxs-lookup"><span data-stu-id="3c809-199">This number is accurate and complete after a full collection, but may be incomplete after an ephemeral collection.</span></span>|  
|<span data-ttu-id="3c809-200">ProcessSurvived</span><span class="sxs-lookup"><span data-stu-id="3c809-200">ProcessSurvived</span></span>|<span data-ttu-id="3c809-201">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="3c809-201">win:UInt64</span></span>|<span data-ttu-id="3c809-202">Nombre total d'octets qui ont survécu à la dernière collection.</span><span class="sxs-lookup"><span data-stu-id="3c809-202">The total bytes that survived from the last collection.</span></span> <span data-ttu-id="3c809-203">Après une collection complète, ce nombre représente le nombre d'octets maintenus actifs dans les tas managés.</span><span class="sxs-lookup"><span data-stu-id="3c809-203">After a full collection, this number represents the number of bytes being held live in managed heaps.</span></span> <span data-ttu-id="3c809-204">Après une collection éphémère, ce nombre représente le nombre d'octets maintenus actifs dans les générations éphémères.</span><span class="sxs-lookup"><span data-stu-id="3c809-204">After an ephemeral collection, this number represents the number of bytes held live in ephemeral generations.</span></span>|  
|<span data-ttu-id="3c809-205">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="3c809-205">ClrInstanceID</span></span>|<span data-ttu-id="3c809-206">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="3c809-206">win:UInt16</span></span>|<span data-ttu-id="3c809-207">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="3c809-207">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="3c809-208">Retour au début</span><span class="sxs-lookup"><span data-stu-id="3c809-208">Back to top</span></span>](#top)  
  
<a name="threadappdomainenter_event"></a>   
## <a name="threadappdomainenter-event"></a><span data-ttu-id="3c809-209">Événement ThreadAppDomainEnter</span><span class="sxs-lookup"><span data-stu-id="3c809-209">ThreadAppDomainEnter Event</span></span>  
 <span data-ttu-id="3c809-210">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="3c809-210">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="3c809-211">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="3c809-211">Keyword for raising the event</span></span>|<span data-ttu-id="3c809-212">Niveau</span><span class="sxs-lookup"><span data-stu-id="3c809-212">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="3c809-213">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="3c809-213">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="3c809-214">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="3c809-214">Informational(4)</span></span>|  
|<span data-ttu-id="3c809-215">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="3c809-215">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="3c809-216">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="3c809-216">Informational(4)</span></span>|  
  
 <span data-ttu-id="3c809-217">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="3c809-217">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="3c809-218">Événement</span><span class="sxs-lookup"><span data-stu-id="3c809-218">Event</span></span>|<span data-ttu-id="3c809-219">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="3c809-219">Event ID</span></span>|<span data-ttu-id="3c809-220">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="3c809-220">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ThreadAppDomainEnter`|<span data-ttu-id="3c809-221">87</span><span class="sxs-lookup"><span data-stu-id="3c809-221">87</span></span>|<span data-ttu-id="3c809-222">Un thread entre dans un domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="3c809-222">A thread enters an application domain.</span></span>|  
  
 <span data-ttu-id="3c809-223">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="3c809-223">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="3c809-224">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="3c809-224">Field name</span></span>|<span data-ttu-id="3c809-225">Type de données</span><span class="sxs-lookup"><span data-stu-id="3c809-225">Data type</span></span>|<span data-ttu-id="3c809-226">Description</span><span class="sxs-lookup"><span data-stu-id="3c809-226">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="3c809-227">ThreadID</span><span class="sxs-lookup"><span data-stu-id="3c809-227">ThreadID</span></span>|<span data-ttu-id="3c809-228">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="3c809-228">win:UInt64</span></span>|<span data-ttu-id="3c809-229">Identificateur du thread.</span><span class="sxs-lookup"><span data-stu-id="3c809-229">The thread identifier.</span></span>|  
|<span data-ttu-id="3c809-230">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="3c809-230">AppDomainID</span></span>|<span data-ttu-id="3c809-231">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="3c809-231">win:UInt64</span></span>|<span data-ttu-id="3c809-232">Identificateur du domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="3c809-232">The application domain identifier.</span></span>|  
|<span data-ttu-id="3c809-233">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="3c809-233">ClrInstanceID</span></span>|<span data-ttu-id="3c809-234">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="3c809-234">win:UInt16</span></span>|<span data-ttu-id="3c809-235">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="3c809-235">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="3c809-236">Retour au début</span><span class="sxs-lookup"><span data-stu-id="3c809-236">Back to top</span></span>](#top)  
  
<a name="threadterminated_event"></a>   
## <a name="threadterminated-event"></a><span data-ttu-id="3c809-237">Événement ThreadTerminated</span><span class="sxs-lookup"><span data-stu-id="3c809-237">ThreadTerminated Event</span></span>  
 <span data-ttu-id="3c809-238">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="3c809-238">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="3c809-239">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="3c809-239">Keyword for raising the event</span></span>|<span data-ttu-id="3c809-240">Niveau</span><span class="sxs-lookup"><span data-stu-id="3c809-240">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="3c809-241">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="3c809-241">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="3c809-242">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="3c809-242">Informational(4)</span></span>|  
|<span data-ttu-id="3c809-243">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="3c809-243">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="3c809-244">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="3c809-244">Informational(4)</span></span>|  
  
 <span data-ttu-id="3c809-245">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="3c809-245">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="3c809-246">Événement</span><span class="sxs-lookup"><span data-stu-id="3c809-246">Event</span></span>|<span data-ttu-id="3c809-247">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="3c809-247">Event ID</span></span>|<span data-ttu-id="3c809-248">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="3c809-248">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ThreadTerminated`|<span data-ttu-id="3c809-249">86</span><span class="sxs-lookup"><span data-stu-id="3c809-249">86</span></span>|<span data-ttu-id="3c809-250">Un thread se termine.</span><span class="sxs-lookup"><span data-stu-id="3c809-250">A thread terminates.</span></span>|  
  
 <span data-ttu-id="3c809-251">Le tableau ci-dessous montre les données d’événements.</span><span class="sxs-lookup"><span data-stu-id="3c809-251">The following table shows the event data:</span></span>  
  
|<span data-ttu-id="3c809-252">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="3c809-252">Field name</span></span>|<span data-ttu-id="3c809-253">Type de données</span><span class="sxs-lookup"><span data-stu-id="3c809-253">Data type</span></span>|<span data-ttu-id="3c809-254">Description</span><span class="sxs-lookup"><span data-stu-id="3c809-254">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="3c809-255">ThreadID</span><span class="sxs-lookup"><span data-stu-id="3c809-255">ThreadID</span></span>|<span data-ttu-id="3c809-256">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="3c809-256">win:UInt64</span></span>|<span data-ttu-id="3c809-257">Identificateur du thread.</span><span class="sxs-lookup"><span data-stu-id="3c809-257">The thread identifier.</span></span>|  
|<span data-ttu-id="3c809-258">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="3c809-258">AppDomainID</span></span>|<span data-ttu-id="3c809-259">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="3c809-259">win:UInt64</span></span>|<span data-ttu-id="3c809-260">Identificateur du domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="3c809-260">The application domain identifier.</span></span>|  
|<span data-ttu-id="3c809-261">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="3c809-261">ClrInstanceID</span></span>|<span data-ttu-id="3c809-262">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="3c809-262">win:UInt16</span></span>|<span data-ttu-id="3c809-263">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="3c809-263">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3c809-264">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c809-264">See also</span></span>

- [<span data-ttu-id="3c809-265">Événements ETW du CLR</span><span class="sxs-lookup"><span data-stu-id="3c809-265">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
