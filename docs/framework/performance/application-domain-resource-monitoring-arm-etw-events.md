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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61788061"
---
# <a name="application-domain-resource-monitoring-arm-etw-events"></a><span data-ttu-id="8554e-102">Événements ETW d'analyse de ressource de domaine d'application</span><span class="sxs-lookup"><span data-stu-id="8554e-102">Application Domain Resource Monitoring (ARM) ETW Events</span></span>
<a name="top"></a> <span data-ttu-id="8554e-103">Ces événements fournissent des informations de diagnostic détaillées sur l'état d'un domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="8554e-103">These events provide detailed diagnostic information about the state of an application domain.</span></span> <span data-ttu-id="8554e-104">Vous pouvez utiliser ces événements ou la fonctionnalité ARM d'analyse de ressource de domaine d'application pour obtenir les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="8554e-104">You can use these events or use the application domain resource monitoring (ARM) feature to obtain the same information.</span></span>  
  
 <span data-ttu-id="8554e-105">Cette catégorie comprend les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="8554e-105">This category consists of the following events:</span></span>  
  
- [<span data-ttu-id="8554e-106">Événement ThreadCreated</span><span class="sxs-lookup"><span data-stu-id="8554e-106">ThreadCreated Event</span></span>](#threadcreated_event)  
  
- [<span data-ttu-id="8554e-107">Événement AppDomainMemAllocated</span><span class="sxs-lookup"><span data-stu-id="8554e-107">AppDomainMemAllocated Event</span></span>](#appdomainmemallocated_event)  
  
- [<span data-ttu-id="8554e-108">Événement AppDomainMemSurvived</span><span class="sxs-lookup"><span data-stu-id="8554e-108">AppDomainMemSurvived Event</span></span>](#appdomainmemsurvived_event)  
  
- [<span data-ttu-id="8554e-109">Événement ThreadAppDomainEnter</span><span class="sxs-lookup"><span data-stu-id="8554e-109">ThreadAppDomainEnter Event</span></span>](#threadappdomainenter_event)  
  
- [<span data-ttu-id="8554e-110">Événement ThreadTerminated</span><span class="sxs-lookup"><span data-stu-id="8554e-110">ThreadTerminated Event</span></span>](#threadterminated_event)  
  
<a name="threadcreated_event"></a>   
## <a name="threadcreated-event"></a><span data-ttu-id="8554e-111">Événement ThreadCreated</span><span class="sxs-lookup"><span data-stu-id="8554e-111">ThreadCreated Event</span></span>  
 <span data-ttu-id="8554e-112">Cet événement est également déclenché sous le fournisseur d'arrêt en tant que `ThreadDC` (sous le mot clé `AppDomainResourceManagementRundownKeyword` ).</span><span class="sxs-lookup"><span data-stu-id="8554e-112">This event is also raised  under the rundown provider as `ThreadDC` (under the `AppDomainResourceManagementRundownKeyword` keyword).</span></span> <span data-ttu-id="8554e-113">Il s’agit du seul événement déclenché sous le fournisseur d'arrêt dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="8554e-113">This is the only event that is raised under the rundown provider in this category.</span></span>  
  
 <span data-ttu-id="8554e-114">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="8554e-114">The following table shows the keyword and level.</span></span> <span data-ttu-id="8554e-115">(Pour plus d'informations, consultez [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span><span class="sxs-lookup"><span data-stu-id="8554e-115">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="8554e-116">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="8554e-116">Keyword for raising the event</span></span>|<span data-ttu-id="8554e-117">Niveau</span><span class="sxs-lookup"><span data-stu-id="8554e-117">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="8554e-118">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="8554e-118">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="8554e-119">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="8554e-119">Informational(4)</span></span>|  
|<span data-ttu-id="8554e-120">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="8554e-120">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="8554e-121">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="8554e-121">Informational(4)</span></span>|  
  
 <span data-ttu-id="8554e-122">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="8554e-122">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="8554e-123">Événement</span><span class="sxs-lookup"><span data-stu-id="8554e-123">Event</span></span>|<span data-ttu-id="8554e-124">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="8554e-124">Event ID</span></span>|<span data-ttu-id="8554e-125">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="8554e-125">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ThreadCreated`|<span data-ttu-id="8554e-126">85</span><span class="sxs-lookup"><span data-stu-id="8554e-126">85</span></span>|<span data-ttu-id="8554e-127">Un thread a été créé pour le domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="8554e-127">A thread was created for the application domain.</span></span>|  
  
 <span data-ttu-id="8554e-128">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="8554e-128">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="8554e-129">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="8554e-129">Field name</span></span>|<span data-ttu-id="8554e-130">Type de données</span><span class="sxs-lookup"><span data-stu-id="8554e-130">Data type</span></span>|<span data-ttu-id="8554e-131">Description</span><span class="sxs-lookup"><span data-stu-id="8554e-131">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="8554e-132">ThreadID</span><span class="sxs-lookup"><span data-stu-id="8554e-132">ThreadID</span></span>|<span data-ttu-id="8554e-133">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="8554e-133">win:UInt64</span></span>|<span data-ttu-id="8554e-134">ID du thread qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="8554e-134">ID of the thread that was created.</span></span>|  
|<span data-ttu-id="8554e-135">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="8554e-135">AppDomainID</span></span>|<span data-ttu-id="8554e-136">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="8554e-136">win:UInt64</span></span>|<span data-ttu-id="8554e-137">Identificateur du domaine d'application pour lequel l'activité du thread est signalée.</span><span class="sxs-lookup"><span data-stu-id="8554e-137">Identifier of the application domain for which thread activity is being reported.</span></span>|  
|<span data-ttu-id="8554e-138">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="8554e-138">Flags</span></span>|<span data-ttu-id="8554e-139">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="8554e-139">win:UInt32</span></span>|<span data-ttu-id="8554e-140">Indicateurs de création de thread.</span><span class="sxs-lookup"><span data-stu-id="8554e-140">Thread creation flags.</span></span>|  
|<span data-ttu-id="8554e-141">ManagedThreadIndex</span><span class="sxs-lookup"><span data-stu-id="8554e-141">ManagedThreadIndex</span></span>|<span data-ttu-id="8554e-142">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="8554e-142">win:UInt32</span></span>|<span data-ttu-id="8554e-143">Index managé du thread qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="8554e-143">Managed index of the thread that was created.</span></span>|  
|<span data-ttu-id="8554e-144">OSThreadID</span><span class="sxs-lookup"><span data-stu-id="8554e-144">OSThreadID</span></span>|<span data-ttu-id="8554e-145">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="8554e-145">win:UInt32</span></span>|<span data-ttu-id="8554e-146">ID de système d’exploitation du thread qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="8554e-146">Operating system ID of the thread that was created.</span></span>|  
|<span data-ttu-id="8554e-147">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="8554e-147">ClrInstanceID</span></span>|<span data-ttu-id="8554e-148">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="8554e-148">win:UInt16</span></span>|<span data-ttu-id="8554e-149">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="8554e-149">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="8554e-150">Retour au début</span><span class="sxs-lookup"><span data-stu-id="8554e-150">Back to top</span></span>](#top)  
  
<a name="appdomainmemallocated_event"></a>   
## <a name="appdomainmemallocated-event"></a><span data-ttu-id="8554e-151">Événement AppDomainMemAllocated</span><span class="sxs-lookup"><span data-stu-id="8554e-151">AppDomainMemAllocated Event</span></span>  
 <span data-ttu-id="8554e-152">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="8554e-152">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="8554e-153">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="8554e-153">Keyword for raising the event</span></span>|<span data-ttu-id="8554e-154">Niveau</span><span class="sxs-lookup"><span data-stu-id="8554e-154">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="8554e-155">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="8554e-155">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="8554e-156">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="8554e-156">Informational(4)</span></span>|  
  
 <span data-ttu-id="8554e-157">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="8554e-157">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="8554e-158">Événement</span><span class="sxs-lookup"><span data-stu-id="8554e-158">Event</span></span>|<span data-ttu-id="8554e-159">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="8554e-159">Event ID</span></span>|<span data-ttu-id="8554e-160">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="8554e-160">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`AppDomainMemAllocated`|<span data-ttu-id="8554e-161">83</span><span class="sxs-lookup"><span data-stu-id="8554e-161">83</span></span>|<span data-ttu-id="8554e-162">Chaque bloc de 4 Mo de mémoire (environ) est alloué dans le domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="8554e-162">Every 4 MB of memory (approximately) is allocated in the application domain.</span></span>|  
  
 <span data-ttu-id="8554e-163">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="8554e-163">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="8554e-164">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="8554e-164">Field name</span></span>|<span data-ttu-id="8554e-165">Type de données</span><span class="sxs-lookup"><span data-stu-id="8554e-165">Data type</span></span>|<span data-ttu-id="8554e-166">Description</span><span class="sxs-lookup"><span data-stu-id="8554e-166">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="8554e-167">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="8554e-167">AppDomainID</span></span>|<span data-ttu-id="8554e-168">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="8554e-168">win:UInt64</span></span>|<span data-ttu-id="8554e-169">Identificateur du domaine d'application pour lequel l'utilisation des ressources est signalée.</span><span class="sxs-lookup"><span data-stu-id="8554e-169">Identifier of the application domain for which resource usage is being reported.</span></span>|  
|<span data-ttu-id="8554e-170">Allocated</span><span class="sxs-lookup"><span data-stu-id="8554e-170">Allocated</span></span>|<span data-ttu-id="8554e-171">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="8554e-171">win:UInt64</span></span>|<span data-ttu-id="8554e-172">Nombre total d'octets alloués dans ce domaine d'application depuis sa création (la quantité de mémoire libérée n'est pas soustraite).</span><span class="sxs-lookup"><span data-stu-id="8554e-172">The total number of bytes allocated in this application domain since the application domain was created (the amount of freed memory is not subtracted).</span></span>|  
|<span data-ttu-id="8554e-173">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="8554e-173">ClrInstanceID</span></span>|<span data-ttu-id="8554e-174">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="8554e-174">win:UInt16</span></span>|<span data-ttu-id="8554e-175">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="8554e-175">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="8554e-176">Retour au début</span><span class="sxs-lookup"><span data-stu-id="8554e-176">Back to top</span></span>](#top)  
  
<a name="appdomainmemsurvived_event"></a>   
## <a name="appdomainmemsurvived-event"></a><span data-ttu-id="8554e-177">Événement AppDomainMemSurvived</span><span class="sxs-lookup"><span data-stu-id="8554e-177">AppDomainMemSurvived Event</span></span>  
 <span data-ttu-id="8554e-178">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="8554e-178">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="8554e-179">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="8554e-179">Keyword for raising the event</span></span>|<span data-ttu-id="8554e-180">Niveau</span><span class="sxs-lookup"><span data-stu-id="8554e-180">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="8554e-181">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="8554e-181">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="8554e-182">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="8554e-182">Informational(4)</span></span>|  
  
 <span data-ttu-id="8554e-183">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="8554e-183">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="8554e-184">Événement</span><span class="sxs-lookup"><span data-stu-id="8554e-184">Event</span></span>|<span data-ttu-id="8554e-185">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="8554e-185">Event ID</span></span>|<span data-ttu-id="8554e-186">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="8554e-186">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`AppDomainMemSurvived`|<span data-ttu-id="8554e-187">84</span><span class="sxs-lookup"><span data-stu-id="8554e-187">84</span></span>|<span data-ttu-id="8554e-188">Chaque garbage collection est terminé.</span><span class="sxs-lookup"><span data-stu-id="8554e-188">Each garbage collection has ended.</span></span>|  
  
 <span data-ttu-id="8554e-189">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="8554e-189">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="8554e-190">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="8554e-190">Field name</span></span>|<span data-ttu-id="8554e-191">Type de données</span><span class="sxs-lookup"><span data-stu-id="8554e-191">Data type</span></span>|<span data-ttu-id="8554e-192">Description</span><span class="sxs-lookup"><span data-stu-id="8554e-192">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="8554e-193">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="8554e-193">AppDomainID</span></span>|<span data-ttu-id="8554e-194">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="8554e-194">win:UInt64</span></span>|<span data-ttu-id="8554e-195">Identificateur du domaine pour lequel l’utilisation des ressources est signalée.</span><span class="sxs-lookup"><span data-stu-id="8554e-195">Identifier of the domain for which resource usage is being reported.</span></span>|  
|<span data-ttu-id="8554e-196">Survived</span><span class="sxs-lookup"><span data-stu-id="8554e-196">Survived</span></span>|<span data-ttu-id="8554e-197">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="8554e-197">win:UInt64</span></span>|<span data-ttu-id="8554e-198">Nombre d'octets ayant survécu après la dernière collection et qui sont conservés par ce domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="8554e-198">The number of bytes that survived after the last collection and that are known to be held by this application domain.</span></span> <span data-ttu-id="8554e-199">Ce nombre est exact et complet après une collection complète, mais peut être incomplet après une collection éphémère.</span><span class="sxs-lookup"><span data-stu-id="8554e-199">This number is accurate and complete after a full collection, but may be incomplete after an ephemeral collection.</span></span>|  
|<span data-ttu-id="8554e-200">ProcessSurvived</span><span class="sxs-lookup"><span data-stu-id="8554e-200">ProcessSurvived</span></span>|<span data-ttu-id="8554e-201">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="8554e-201">win:UInt64</span></span>|<span data-ttu-id="8554e-202">Nombre total d'octets qui ont survécu à la dernière collection.</span><span class="sxs-lookup"><span data-stu-id="8554e-202">The total bytes that survived from the last collection.</span></span> <span data-ttu-id="8554e-203">Après une collection complète, ce nombre représente le nombre d'octets maintenus actifs dans les tas managés.</span><span class="sxs-lookup"><span data-stu-id="8554e-203">After a full collection, this number represents the number of bytes being held live in managed heaps.</span></span> <span data-ttu-id="8554e-204">Après une collection éphémère, ce nombre représente le nombre d'octets maintenus actifs dans les générations éphémères.</span><span class="sxs-lookup"><span data-stu-id="8554e-204">After an ephemeral collection, this number represents the number of bytes held live in ephemeral generations.</span></span>|  
|<span data-ttu-id="8554e-205">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="8554e-205">ClrInstanceID</span></span>|<span data-ttu-id="8554e-206">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="8554e-206">win:UInt16</span></span>|<span data-ttu-id="8554e-207">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="8554e-207">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="8554e-208">Retour au début</span><span class="sxs-lookup"><span data-stu-id="8554e-208">Back to top</span></span>](#top)  
  
<a name="threadappdomainenter_event"></a>   
## <a name="threadappdomainenter-event"></a><span data-ttu-id="8554e-209">Événement ThreadAppDomainEnter</span><span class="sxs-lookup"><span data-stu-id="8554e-209">ThreadAppDomainEnter Event</span></span>  
 <span data-ttu-id="8554e-210">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="8554e-210">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="8554e-211">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="8554e-211">Keyword for raising the event</span></span>|<span data-ttu-id="8554e-212">Niveau</span><span class="sxs-lookup"><span data-stu-id="8554e-212">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="8554e-213">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="8554e-213">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="8554e-214">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="8554e-214">Informational(4)</span></span>|  
|<span data-ttu-id="8554e-215">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="8554e-215">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="8554e-216">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="8554e-216">Informational(4)</span></span>|  
  
 <span data-ttu-id="8554e-217">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="8554e-217">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="8554e-218">Événement</span><span class="sxs-lookup"><span data-stu-id="8554e-218">Event</span></span>|<span data-ttu-id="8554e-219">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="8554e-219">Event ID</span></span>|<span data-ttu-id="8554e-220">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="8554e-220">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ThreadAppDomainEnter`|<span data-ttu-id="8554e-221">87</span><span class="sxs-lookup"><span data-stu-id="8554e-221">87</span></span>|<span data-ttu-id="8554e-222">Un thread entre dans un domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="8554e-222">A thread enters an application domain.</span></span>|  
  
 <span data-ttu-id="8554e-223">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="8554e-223">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="8554e-224">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="8554e-224">Field name</span></span>|<span data-ttu-id="8554e-225">Type de données</span><span class="sxs-lookup"><span data-stu-id="8554e-225">Data type</span></span>|<span data-ttu-id="8554e-226">Description</span><span class="sxs-lookup"><span data-stu-id="8554e-226">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="8554e-227">ThreadID</span><span class="sxs-lookup"><span data-stu-id="8554e-227">ThreadID</span></span>|<span data-ttu-id="8554e-228">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="8554e-228">win:UInt64</span></span>|<span data-ttu-id="8554e-229">Identificateur du thread.</span><span class="sxs-lookup"><span data-stu-id="8554e-229">The thread identifier.</span></span>|  
|<span data-ttu-id="8554e-230">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="8554e-230">AppDomainID</span></span>|<span data-ttu-id="8554e-231">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="8554e-231">win:UInt64</span></span>|<span data-ttu-id="8554e-232">Identificateur du domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="8554e-232">The application domain identifier.</span></span>|  
|<span data-ttu-id="8554e-233">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="8554e-233">ClrInstanceID</span></span>|<span data-ttu-id="8554e-234">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="8554e-234">win:UInt16</span></span>|<span data-ttu-id="8554e-235">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="8554e-235">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="8554e-236">Retour au début</span><span class="sxs-lookup"><span data-stu-id="8554e-236">Back to top</span></span>](#top)  
  
<a name="threadterminated_event"></a>   
## <a name="threadterminated-event"></a><span data-ttu-id="8554e-237">Événement ThreadTerminated</span><span class="sxs-lookup"><span data-stu-id="8554e-237">ThreadTerminated Event</span></span>  
 <span data-ttu-id="8554e-238">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="8554e-238">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="8554e-239">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="8554e-239">Keyword for raising the event</span></span>|<span data-ttu-id="8554e-240">Niveau</span><span class="sxs-lookup"><span data-stu-id="8554e-240">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="8554e-241">`AppDomainResourceManagementKeyword` (0x800)</span><span class="sxs-lookup"><span data-stu-id="8554e-241">`AppDomainResourceManagementKeyword` (0x800)</span></span>|<span data-ttu-id="8554e-242">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="8554e-242">Informational(4)</span></span>|  
|<span data-ttu-id="8554e-243">`ThreadingKeyword` (0x10000)</span><span class="sxs-lookup"><span data-stu-id="8554e-243">`ThreadingKeyword` (0x10000)</span></span>|<span data-ttu-id="8554e-244">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="8554e-244">Informational(4)</span></span>|  
  
 <span data-ttu-id="8554e-245">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="8554e-245">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="8554e-246">Événement</span><span class="sxs-lookup"><span data-stu-id="8554e-246">Event</span></span>|<span data-ttu-id="8554e-247">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="8554e-247">Event ID</span></span>|<span data-ttu-id="8554e-248">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="8554e-248">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ThreadTerminated`|<span data-ttu-id="8554e-249">86</span><span class="sxs-lookup"><span data-stu-id="8554e-249">86</span></span>|<span data-ttu-id="8554e-250">Un thread se termine.</span><span class="sxs-lookup"><span data-stu-id="8554e-250">A thread terminates.</span></span>|  
  
 <span data-ttu-id="8554e-251">Le tableau ci-dessous montre les données d’événements.</span><span class="sxs-lookup"><span data-stu-id="8554e-251">The following table shows the event data:</span></span>  
  
|<span data-ttu-id="8554e-252">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="8554e-252">Field name</span></span>|<span data-ttu-id="8554e-253">Type de données</span><span class="sxs-lookup"><span data-stu-id="8554e-253">Data type</span></span>|<span data-ttu-id="8554e-254">Description</span><span class="sxs-lookup"><span data-stu-id="8554e-254">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="8554e-255">ThreadID</span><span class="sxs-lookup"><span data-stu-id="8554e-255">ThreadID</span></span>|<span data-ttu-id="8554e-256">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="8554e-256">win:UInt64</span></span>|<span data-ttu-id="8554e-257">Identificateur du thread.</span><span class="sxs-lookup"><span data-stu-id="8554e-257">The thread identifier.</span></span>|  
|<span data-ttu-id="8554e-258">AppDomainID</span><span class="sxs-lookup"><span data-stu-id="8554e-258">AppDomainID</span></span>|<span data-ttu-id="8554e-259">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="8554e-259">win:UInt64</span></span>|<span data-ttu-id="8554e-260">Identificateur du domaine d'application.</span><span class="sxs-lookup"><span data-stu-id="8554e-260">The application domain identifier.</span></span>|  
|<span data-ttu-id="8554e-261">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="8554e-261">ClrInstanceID</span></span>|<span data-ttu-id="8554e-262">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="8554e-262">win:UInt16</span></span>|<span data-ttu-id="8554e-263">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="8554e-263">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8554e-264">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8554e-264">See also</span></span>

- [<span data-ttu-id="8554e-265">Événements ETW du CLR</span><span class="sxs-lookup"><span data-stu-id="8554e-265">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
