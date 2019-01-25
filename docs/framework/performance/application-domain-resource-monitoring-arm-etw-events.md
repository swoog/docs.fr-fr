---
title: Événements ETW d'analyse de ressource de domaine d'application
ms.date: 03/30/2017
helpviewer_keywords:
- ETW, application domain monitoring events
- application domain monitoring events [.NET Framework]
ms.assetid: d38ff268-a2ee-434e-b504-d570880e0289
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8442b8723476984b90f740beac912688719f1791
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54689833"
---
# <a name="application-domain-resource-monitoring-arm-etw-events"></a><span data-ttu-id="45df9-102">Événements ETW d'analyse de ressource de domaine d'application</span><span class="sxs-lookup"><span data-stu-id="45df9-102">Application Domain Resource Monitoring (ARM) ETW Events</span></span>
<a name="top"></a> <span data-ttu-id="45df9-103">Ces événements fournissent des informations de diagnostic détaillées sur l'état d'un domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="45df9-103">These events provide detailed diagnostic information about the state of an application domain.</span></span> <span data-ttu-id="45df9-104">Vous pouvez utiliser ces événements ou la fonctionnalité ARM d'analyse de ressource de domaine d'application pour obtenir les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="45df9-104">You can use these events or use the application domain resource monitoring (ARM) feature to obtain the same information.</span></span>  
  
 <span data-ttu-id="45df9-105">Cette catégorie comprend les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="45df9-105">This category consists of the following events:</span></span>  
  
-   [<span data-ttu-id="45df9-106">Événement ThreadCreated</span><span class="sxs-lookup"><span data-stu-id="45df9-106">ThreadCreated Event</span></span>](#threadcreated_event)  
  
-   [<span data-ttu-id="45df9-107">Événement AppDomainMemAllocated</span><span class="sxs-lookup"><span data-stu-id="45df9-107">AppDomainMemAllocated Event</span></span>](#appdomainmemallocated_event)  
  
-   [<span data-ttu-id="45df9-108">Événement AppDomainMemSurvived</span><span class="sxs-lookup"><span data-stu-id="45df9-108">AppDomainMemSurvived Event</span></span>](#appdomainmemsurvived_event)  
  
-   [<span data-ttu-id="45df9-109">Événement ThreadAppDomainEnter</span><span class="sxs-lookup"><span data-stu-id="45df9-109">ThreadAppDomainEnter Event</span></span>](#threadappdomainenter_event)  
  
-   [<span data-ttu-id="45df9-110">Événement ThreadTerminated</span><span class="sxs-lookup"><span data-stu-id="45df9-110">ThreadTerminated Event</span></span>](#threadterminated_event)  
  
<a name="threadcreated_event"></a>   
## <a name="threadcreated-event"></a><span data-ttu-id="45df9-111">Événement ThreadCreated</span><span class="sxs-lookup"><span data-stu-id="45df9-111">ThreadCreated Event</span></span>  
 <span data-ttu-id="45df9-112">Cet événement est également déclenché sous le fournisseur d'arrêt en tant que `ThreadDC` (sous le mot clé `AppDomainResourceManagementRundownKeyword` ).</span><span class="sxs-lookup"><span data-stu-id="45df9-112">This event is also raised  under the rundown provider as `ThreadDC` (under the `AppDomainResourceManagementRundownKeyword` keyword).</span></span> <span data-ttu-id="45df9-113">Il s’agit du seul événement déclenché sous le fournisseur d'arrêt dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="45df9-113">This is the only event that is raised under the rundown provider in this category.</span></span>  
  
 <span data-ttu-id="45df9-114">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="45df9-114">The following table shows the keyword and level.</span></span> <span data-ttu-id="45df9-115">(Pour plus d'informations, consultez [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span><span class="sxs-lookup"><span data-stu-id="45df9-115">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="45df9-116">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="45df9-116">Keyword for raising the event</span></span>|<span data-ttu-id="45df9-117">Niveau</span><span class="sxs-lookup"><span data-stu-id="45df9-117">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="45df9-118">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="45df9-118">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="45df9-119">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="45df9-119">Informational(4)</span></span>|  
|<span data-ttu-id="45df9-120">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="45df9-120">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="45df9-121">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="45df9-121">Informational(4)</span></span>|  
  
 <span data-ttu-id="45df9-122">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="45df9-122">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="45df9-123">Événement</span><span class="sxs-lookup"><span data-stu-id="45df9-123">Event</span></span>|<span data-ttu-id="45df9-124">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="45df9-124">Event ID</span></span>|<span data-ttu-id="45df9-125">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="45df9-125">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ThreadCreated`|<span data-ttu-id="45df9-126">85</span><span class="sxs-lookup"><span data-stu-id="45df9-126">85</span></span>|<span data-ttu-id="45df9-127">Un thread a été créé pour le domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="45df9-127">A thread was created for the application domain.</span></span>|  
  
 <span data-ttu-id="45df9-128">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="45df9-128">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="45df9-129">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="45df9-129">Field name</span></span>|<span data-ttu-id="45df9-130">Type de données</span><span class="sxs-lookup"><span data-stu-id="45df9-130">Data type</span></span>|<span data-ttu-id="45df9-131">Description</span><span class="sxs-lookup"><span data-stu-id="45df9-131">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="45df9-132">ThreadID</span><span class="sxs-lookup"><span data-stu-id="45df9-132">ThreadID</span></span>|<span data-ttu-id="45df9-133">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="45df9-133">win:UInt64</span></span>|<span data-ttu-id="45df9-134">ID du thread qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="45df9-134">ID of the thread that was created.</span></span>|  
|<span data-ttu-id="45df9-135">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="45df9-135">AppDomainID</span></span>|<span data-ttu-id="45df9-136">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="45df9-136">win:UInt64</span></span>|<span data-ttu-id="45df9-137">Identificateur du domaine d'application pour lequel l'activité du thread est signalée.</span><span class="sxs-lookup"><span data-stu-id="45df9-137">Identifier of the application domain for which thread activity is being reported.</span></span>|  
|<span data-ttu-id="45df9-138">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="45df9-138">Flags</span></span>|<span data-ttu-id="45df9-139">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="45df9-139">win:UInt32</span></span>|<span data-ttu-id="45df9-140">Indicateurs de création de thread.</span><span class="sxs-lookup"><span data-stu-id="45df9-140">Thread creation flags.</span></span>|  
|<span data-ttu-id="45df9-141">ManagedThreadIndex</span><span class="sxs-lookup"><span data-stu-id="45df9-141">ManagedThreadIndex</span></span>|<span data-ttu-id="45df9-142">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="45df9-142">win:UInt32</span></span>|<span data-ttu-id="45df9-143">Index managé du thread qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="45df9-143">Managed index of the thread that was created.</span></span>|  
|<span data-ttu-id="45df9-144">OSThreadID</span><span class="sxs-lookup"><span data-stu-id="45df9-144">OSThreadID</span></span>|<span data-ttu-id="45df9-145">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="45df9-145">win:UInt32</span></span>|<span data-ttu-id="45df9-146">ID de système d’exploitation du thread qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="45df9-146">Operating system ID of the thread that was created.</span></span>|  
|<span data-ttu-id="45df9-147">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="45df9-147">ClrInstanceID</span></span>|<span data-ttu-id="45df9-148">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="45df9-148">win:UInt16</span></span>|<span data-ttu-id="45df9-149">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="45df9-149">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="45df9-150">Retour au début</span><span class="sxs-lookup"><span data-stu-id="45df9-150">Back to top</span></span>](#top)  
  
<a name="appdomainmemallocated_event"></a>   
## <a name="appdomainmemallocated-event"></a><span data-ttu-id="45df9-151">Événement AppDomainMemAllocated</span><span class="sxs-lookup"><span data-stu-id="45df9-151">AppDomainMemAllocated Event</span></span>  
 <span data-ttu-id="45df9-152">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="45df9-152">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="45df9-153">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="45df9-153">Keyword for raising the event</span></span>|<span data-ttu-id="45df9-154">Niveau</span><span class="sxs-lookup"><span data-stu-id="45df9-154">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="45df9-155">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="45df9-155">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="45df9-156">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="45df9-156">Informational(4)</span></span>|  
  
 <span data-ttu-id="45df9-157">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="45df9-157">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="45df9-158">Événement</span><span class="sxs-lookup"><span data-stu-id="45df9-158">Event</span></span>|<span data-ttu-id="45df9-159">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="45df9-159">Event ID</span></span>|<span data-ttu-id="45df9-160">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="45df9-160">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`AppDomainMemAllocated`|<span data-ttu-id="45df9-161">83</span><span class="sxs-lookup"><span data-stu-id="45df9-161">83</span></span>|<span data-ttu-id="45df9-162">Chaque bloc de 4 Mo de mémoire (environ) est alloué dans le domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="45df9-162">Every 4 MB of memory (approximately) is allocated in the application domain.</span></span>|  
  
 <span data-ttu-id="45df9-163">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="45df9-163">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="45df9-164">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="45df9-164">Field name</span></span>|<span data-ttu-id="45df9-165">Type de données</span><span class="sxs-lookup"><span data-stu-id="45df9-165">Data type</span></span>|<span data-ttu-id="45df9-166">Description</span><span class="sxs-lookup"><span data-stu-id="45df9-166">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="45df9-167">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="45df9-167">AppDomainID</span></span>|<span data-ttu-id="45df9-168">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="45df9-168">win:UInt64</span></span>|<span data-ttu-id="45df9-169">Identificateur du domaine d'application pour lequel l'utilisation des ressources est signalée.</span><span class="sxs-lookup"><span data-stu-id="45df9-169">Identifier of the application domain for which resource usage is being reported.</span></span>|  
|<span data-ttu-id="45df9-170">Allocated</span><span class="sxs-lookup"><span data-stu-id="45df9-170">Allocated</span></span>|<span data-ttu-id="45df9-171">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="45df9-171">win:UInt64</span></span>|<span data-ttu-id="45df9-172">Nombre total d'octets alloués dans ce domaine d'application depuis sa création (la quantité de mémoire libérée n'est pas soustraite).</span><span class="sxs-lookup"><span data-stu-id="45df9-172">The total number of bytes allocated in this application domain since the application domain was created (the amount of freed memory is not subtracted).</span></span>|  
|<span data-ttu-id="45df9-173">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="45df9-173">ClrInstanceID</span></span>|<span data-ttu-id="45df9-174">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="45df9-174">win:UInt16</span></span>|<span data-ttu-id="45df9-175">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="45df9-175">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="45df9-176">Retour au début</span><span class="sxs-lookup"><span data-stu-id="45df9-176">Back to top</span></span>](#top)  
  
<a name="appdomainmemsurvived_event"></a>   
## <a name="appdomainmemsurvived-event"></a><span data-ttu-id="45df9-177">Événement AppDomainMemSurvived</span><span class="sxs-lookup"><span data-stu-id="45df9-177">AppDomainMemSurvived Event</span></span>  
 <span data-ttu-id="45df9-178">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="45df9-178">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="45df9-179">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="45df9-179">Keyword for raising the event</span></span>|<span data-ttu-id="45df9-180">Niveau</span><span class="sxs-lookup"><span data-stu-id="45df9-180">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="45df9-181">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="45df9-181">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="45df9-182">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="45df9-182">Informational(4)</span></span>|  
  
 <span data-ttu-id="45df9-183">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="45df9-183">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="45df9-184">Événement</span><span class="sxs-lookup"><span data-stu-id="45df9-184">Event</span></span>|<span data-ttu-id="45df9-185">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="45df9-185">Event ID</span></span>|<span data-ttu-id="45df9-186">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="45df9-186">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`AppDomainMemSurvived`|<span data-ttu-id="45df9-187">84</span><span class="sxs-lookup"><span data-stu-id="45df9-187">84</span></span>|<span data-ttu-id="45df9-188">Chaque garbage collection est terminé.</span><span class="sxs-lookup"><span data-stu-id="45df9-188">Each garbage collection has ended.</span></span>|  
  
 <span data-ttu-id="45df9-189">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="45df9-189">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="45df9-190">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="45df9-190">Field name</span></span>|<span data-ttu-id="45df9-191">Type de données</span><span class="sxs-lookup"><span data-stu-id="45df9-191">Data type</span></span>|<span data-ttu-id="45df9-192">Description</span><span class="sxs-lookup"><span data-stu-id="45df9-192">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="45df9-193">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="45df9-193">AppDomainID</span></span>|<span data-ttu-id="45df9-194">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="45df9-194">win:UInt64</span></span>|<span data-ttu-id="45df9-195">Identificateur du domaine pour lequel l’utilisation des ressources est signalée.</span><span class="sxs-lookup"><span data-stu-id="45df9-195">Identifier of the domain for which resource usage is being reported.</span></span>|  
|<span data-ttu-id="45df9-196">Survived</span><span class="sxs-lookup"><span data-stu-id="45df9-196">Survived</span></span>|<span data-ttu-id="45df9-197">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="45df9-197">win:UInt64</span></span>|<span data-ttu-id="45df9-198">Nombre d'octets ayant survécu après la dernière collection et qui sont conservés par ce domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="45df9-198">The number of bytes that survived after the last collection and that are known to be held by this application domain.</span></span> <span data-ttu-id="45df9-199">Ce nombre est exact et complet après une collection complète, mais peut être incomplet après une collection éphémère.</span><span class="sxs-lookup"><span data-stu-id="45df9-199">This number is accurate and complete after a full collection, but may be incomplete after an ephemeral collection.</span></span>|  
|<span data-ttu-id="45df9-200">ProcessSurvived</span><span class="sxs-lookup"><span data-stu-id="45df9-200">ProcessSurvived</span></span>|<span data-ttu-id="45df9-201">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="45df9-201">win:UInt64</span></span>|<span data-ttu-id="45df9-202">Nombre total d'octets qui ont survécu à la dernière collection.</span><span class="sxs-lookup"><span data-stu-id="45df9-202">The total bytes that survived from the last collection.</span></span> <span data-ttu-id="45df9-203">Après une collection complète, ce nombre représente le nombre d'octets maintenus actifs dans les tas managés.</span><span class="sxs-lookup"><span data-stu-id="45df9-203">After a full collection, this number represents the number of bytes being held live in managed heaps.</span></span> <span data-ttu-id="45df9-204">Après une collection éphémère, ce nombre représente le nombre d'octets maintenus actifs dans les générations éphémères.</span><span class="sxs-lookup"><span data-stu-id="45df9-204">After an ephemeral collection, this number represents the number of bytes held live in ephemeral generations.</span></span>|  
|<span data-ttu-id="45df9-205">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="45df9-205">ClrInstanceID</span></span>|<span data-ttu-id="45df9-206">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="45df9-206">win:UInt16</span></span>|<span data-ttu-id="45df9-207">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="45df9-207">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="45df9-208">Retour au début</span><span class="sxs-lookup"><span data-stu-id="45df9-208">Back to top</span></span>](#top)  
  
<a name="threadappdomainenter_event"></a>   
## <a name="threadappdomainenter-event"></a><span data-ttu-id="45df9-209">Événement ThreadAppDomainEnter</span><span class="sxs-lookup"><span data-stu-id="45df9-209">ThreadAppDomainEnter Event</span></span>  
 <span data-ttu-id="45df9-210">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="45df9-210">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="45df9-211">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="45df9-211">Keyword for raising the event</span></span>|<span data-ttu-id="45df9-212">Niveau</span><span class="sxs-lookup"><span data-stu-id="45df9-212">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="45df9-213">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="45df9-213">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="45df9-214">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="45df9-214">Informational(4)</span></span>|  
|<span data-ttu-id="45df9-215">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="45df9-215">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="45df9-216">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="45df9-216">Informational(4)</span></span>|  
  
 <span data-ttu-id="45df9-217">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="45df9-217">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="45df9-218">Événement</span><span class="sxs-lookup"><span data-stu-id="45df9-218">Event</span></span>|<span data-ttu-id="45df9-219">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="45df9-219">Event ID</span></span>|<span data-ttu-id="45df9-220">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="45df9-220">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ThreadAppDomainEnter`|<span data-ttu-id="45df9-221">87</span><span class="sxs-lookup"><span data-stu-id="45df9-221">87</span></span>|<span data-ttu-id="45df9-222">Un thread entre dans un domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="45df9-222">A thread enters an application domain.</span></span>|  
  
 <span data-ttu-id="45df9-223">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="45df9-223">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="45df9-224">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="45df9-224">Field name</span></span>|<span data-ttu-id="45df9-225">Type de données</span><span class="sxs-lookup"><span data-stu-id="45df9-225">Data type</span></span>|<span data-ttu-id="45df9-226">Description</span><span class="sxs-lookup"><span data-stu-id="45df9-226">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="45df9-227">ThreadID</span><span class="sxs-lookup"><span data-stu-id="45df9-227">ThreadID</span></span>|<span data-ttu-id="45df9-228">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="45df9-228">win:UInt64</span></span>|<span data-ttu-id="45df9-229">Identificateur du thread.</span><span class="sxs-lookup"><span data-stu-id="45df9-229">The thread identifier.</span></span>|  
|<span data-ttu-id="45df9-230">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="45df9-230">AppDomainID</span></span>|<span data-ttu-id="45df9-231">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="45df9-231">win:UInt64</span></span>|<span data-ttu-id="45df9-232">Identificateur du domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="45df9-232">The application domain identifier.</span></span>|  
|<span data-ttu-id="45df9-233">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="45df9-233">ClrInstanceID</span></span>|<span data-ttu-id="45df9-234">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="45df9-234">win:UInt16</span></span>|<span data-ttu-id="45df9-235">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="45df9-235">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="45df9-236">Retour au début</span><span class="sxs-lookup"><span data-stu-id="45df9-236">Back to top</span></span>](#top)  
  
<a name="threadterminated_event"></a>   
## <a name="threadterminated-event"></a><span data-ttu-id="45df9-237">Événement ThreadTerminated</span><span class="sxs-lookup"><span data-stu-id="45df9-237">ThreadTerminated Event</span></span>  
 <span data-ttu-id="45df9-238">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="45df9-238">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="45df9-239">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="45df9-239">Keyword for raising the event</span></span>|<span data-ttu-id="45df9-240">Niveau</span><span class="sxs-lookup"><span data-stu-id="45df9-240">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="45df9-241">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="45df9-241">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="45df9-242">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="45df9-242">Informational(4)</span></span>|  
|<span data-ttu-id="45df9-243">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="45df9-243">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="45df9-244">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="45df9-244">Informational(4)</span></span>|  
  
 <span data-ttu-id="45df9-245">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="45df9-245">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="45df9-246">Événement</span><span class="sxs-lookup"><span data-stu-id="45df9-246">Event</span></span>|<span data-ttu-id="45df9-247">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="45df9-247">Event ID</span></span>|<span data-ttu-id="45df9-248">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="45df9-248">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ThreadTerminated`|<span data-ttu-id="45df9-249">86</span><span class="sxs-lookup"><span data-stu-id="45df9-249">86</span></span>|<span data-ttu-id="45df9-250">Un thread se termine.</span><span class="sxs-lookup"><span data-stu-id="45df9-250">A thread terminates.</span></span>|  
  
 <span data-ttu-id="45df9-251">Le tableau ci-dessous montre les données d’événements.</span><span class="sxs-lookup"><span data-stu-id="45df9-251">The following table shows the event data:</span></span>  
  
|<span data-ttu-id="45df9-252">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="45df9-252">Field name</span></span>|<span data-ttu-id="45df9-253">Type de données</span><span class="sxs-lookup"><span data-stu-id="45df9-253">Data type</span></span>|<span data-ttu-id="45df9-254">Description</span><span class="sxs-lookup"><span data-stu-id="45df9-254">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="45df9-255">ThreadID</span><span class="sxs-lookup"><span data-stu-id="45df9-255">ThreadID</span></span>|<span data-ttu-id="45df9-256">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="45df9-256">win:UInt64</span></span>|<span data-ttu-id="45df9-257">Identificateur du thread.</span><span class="sxs-lookup"><span data-stu-id="45df9-257">The thread identifier.</span></span>|  
|<span data-ttu-id="45df9-258">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="45df9-258">AppDomainID</span></span>|<span data-ttu-id="45df9-259">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="45df9-259">win:UInt64</span></span>|<span data-ttu-id="45df9-260">Identificateur du domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="45df9-260">The application domain identifier.</span></span>|  
|<span data-ttu-id="45df9-261">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="45df9-261">ClrInstanceID</span></span>|<span data-ttu-id="45df9-262">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="45df9-262">win:UInt16</span></span>|<span data-ttu-id="45df9-263">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="45df9-263">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="45df9-264">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45df9-264">See also</span></span>
- [<span data-ttu-id="45df9-265">Événements ETW du CLR</span><span class="sxs-lookup"><span data-stu-id="45df9-265">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
