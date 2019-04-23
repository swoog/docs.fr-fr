---
title: <states>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: ebea5e7c-ad58-43c5-8f2d-cca25ae1b721
ms.openlocfilehash: 30cb2efa4c00c8b292a8ace6a03306d6ac76a7f4
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59073120"
---
# <a name="states"></a><span data-ttu-id="2e0f5-101">\<states></span><span class="sxs-lookup"><span data-stu-id="2e0f5-101">\<states></span></span>
<span data-ttu-id="2e0f5-102">Représente une collection d’états faisant l’objet d’un abonnement dans l’instance de flux de travail suivie lors de la création des enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-102">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
 <span data-ttu-id="2e0f5-103">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="2e0f5-103">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="2e0f5-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="2e0f5-104">\<system.serviceModel></span></span>  
<span data-ttu-id="2e0f5-105">\<tracking></span><span class="sxs-lookup"><span data-stu-id="2e0f5-105">\<tracking></span></span>  
<span data-ttu-id="2e0f5-106">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="2e0f5-106">\<trackingProfile></span></span>  
<span data-ttu-id="2e0f5-107">\<workflow></span><span class="sxs-lookup"><span data-stu-id="2e0f5-107">\<workflow></span></span>  
<span data-ttu-id="2e0f5-108">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="2e0f5-108">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="2e0f5-109">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="2e0f5-109">\<workflowInstanceQuery></span></span>  
<span data-ttu-id="2e0f5-110">\<states></span><span class="sxs-lookup"><span data-stu-id="2e0f5-110">\<states></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2e0f5-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e0f5-111">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <workflowInstanceQueries>
        <workflowInstanceQuery>
          <states>
            <state name="Name"/>
          </states>
        </workflowInstanceQuery>
      </workflowInstanceQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2e0f5-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="2e0f5-112">Attributes and Elements</span></span>  
 <span data-ttu-id="2e0f5-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2e0f5-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="2e0f5-114">Attributes</span></span>  
 <span data-ttu-id="2e0f5-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="2e0f5-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2e0f5-116">Child Elements</span></span>  
  
|<span data-ttu-id="2e0f5-117">Élément</span><span class="sxs-lookup"><span data-stu-id="2e0f5-117">Element</span></span>|<span data-ttu-id="2e0f5-118">Description</span><span class="sxs-lookup"><span data-stu-id="2e0f5-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2e0f5-119">\<state></span><span class="sxs-lookup"><span data-stu-id="2e0f5-119">\<state></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)|<span data-ttu-id="2e0f5-120">État faisant l'objet d'un abonnement de l'instance de flux de travail suivie lors de la création de l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-120">A subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2e0f5-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2e0f5-121">Parent Elements</span></span>  
  
|<span data-ttu-id="2e0f5-122">Élément</span><span class="sxs-lookup"><span data-stu-id="2e0f5-122">Element</span></span>|<span data-ttu-id="2e0f5-123">Description</span><span class="sxs-lookup"><span data-stu-id="2e0f5-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2e0f5-124">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="2e0f5-124">\<workflowInstanceQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflowinstancequery.md)|<span data-ttu-id="2e0f5-125">Requête qui effectue le suivi des changements dans le cycle de vie d'une instance de flux de travail, tels que le début ou la fin d'un événement.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-125">A query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2e0f5-126">Notes</span><span class="sxs-lookup"><span data-stu-id="2e0f5-126">Remarks</span></span>  
 <span data-ttu-id="2e0f5-127">Les enregistrements retournés sont filtrés par états dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-127">The returned records are filtered by the states in this collection.</span></span>  
  
 <span data-ttu-id="2e0f5-128">Les valeurs d'état possibles sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-128">Possible state values are described in the following table.</span></span>  
  
|<span data-ttu-id="2e0f5-129">État</span><span class="sxs-lookup"><span data-stu-id="2e0f5-129">State</span></span>|<span data-ttu-id="2e0f5-130">Description</span><span class="sxs-lookup"><span data-stu-id="2e0f5-130">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="2e0f5-131">Abandonné</span><span class="sxs-lookup"><span data-stu-id="2e0f5-131">Aborted</span></span>|<span data-ttu-id="2e0f5-132">L'instance de flux de travail est abandonnée.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-132">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="2e0f5-133">Terminé</span><span class="sxs-lookup"><span data-stu-id="2e0f5-133">Completed</span></span>|<span data-ttu-id="2e0f5-134">L'instance de flux de travail est terminée.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-134">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="2e0f5-135">Supprimé</span><span class="sxs-lookup"><span data-stu-id="2e0f5-135">Deleted</span></span>|<span data-ttu-id="2e0f5-136">L'instance de flux de travail est supprimée.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-136">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="2e0f5-137">Inactif</span><span class="sxs-lookup"><span data-stu-id="2e0f5-137">Idle</span></span>|<span data-ttu-id="2e0f5-138">L'instance de workflow est inactive.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-138">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="2e0f5-139">Persistant</span><span class="sxs-lookup"><span data-stu-id="2e0f5-139">Persisted</span></span>|<span data-ttu-id="2e0f5-140">L'instance de flux de travail est persistante.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-140">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="2e0f5-141">Repris</span><span class="sxs-lookup"><span data-stu-id="2e0f5-141">Resumed</span></span>|<span data-ttu-id="2e0f5-142">L'instance de flux de travail est reprise.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-142">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="2e0f5-143">Démarré</span><span class="sxs-lookup"><span data-stu-id="2e0f5-143">Started</span></span>|<span data-ttu-id="2e0f5-144">L'instance de flux de travail est démarrée.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-144">The workflow instance is started.</span></span>|  
|<span data-ttu-id="2e0f5-145">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="2e0f5-145">UnhandledException</span></span>|<span data-ttu-id="2e0f5-146">L'instance de flux de travail a rencontré une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-146">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="2e0f5-147">Non chargé</span><span class="sxs-lookup"><span data-stu-id="2e0f5-147">Unloaded</span></span>|<span data-ttu-id="2e0f5-148">L'instance de flux de travail est déchargée.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-148">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="2e0f5-149">Canceled</span><span class="sxs-lookup"><span data-stu-id="2e0f5-149">Canceled</span></span>|<span data-ttu-id="2e0f5-150">L'instance de flux de travail est annulée.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-150">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="2e0f5-151">Suspendu</span><span class="sxs-lookup"><span data-stu-id="2e0f5-151">Suspended</span></span>|<span data-ttu-id="2e0f5-152">L'instance de workflow est interrompue.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-152">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="2e0f5-153">Arrêté</span><span class="sxs-lookup"><span data-stu-id="2e0f5-153">Terminated</span></span>|<span data-ttu-id="2e0f5-154">L'instance de flux de travail est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-154">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="2e0f5-155">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="2e0f5-155">Unsuspended</span></span>|<span data-ttu-id="2e0f5-156">L'instance de flux de travail est non interrompue.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-156">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="2e0f5-157">Exemple</span><span class="sxs-lookup"><span data-stu-id="2e0f5-157">Example</span></span>  
 <span data-ttu-id="2e0f5-158">La configuration suivante permet de s'abonner aux enregistrements de suivi au niveau de l'instance de flux de travail pour l'état de l'instance `Started` à l'aide de cette requête.</span><span class="sxs-lookup"><span data-stu-id="2e0f5-158">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="2e0f5-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e0f5-159">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="2e0f5-160">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="2e0f5-160">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="2e0f5-161">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="2e0f5-161">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
