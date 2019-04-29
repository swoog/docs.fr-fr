---
title: <states>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: ebea5e7c-ad58-43c5-8f2d-cca25ae1b721
ms.openlocfilehash: 30cb2efa4c00c8b292a8ace6a03306d6ac76a7f4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61797798"
---
# <a name="states"></a><span data-ttu-id="2fed8-101">\<states></span><span class="sxs-lookup"><span data-stu-id="2fed8-101">\<states></span></span>
<span data-ttu-id="2fed8-102">Représente une collection d’états faisant l’objet d’un abonnement dans l’instance de flux de travail suivie lors de la création des enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="2fed8-102">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
 <span data-ttu-id="2fed8-103">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="2fed8-103">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="2fed8-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="2fed8-104">\<system.serviceModel></span></span>  
<span data-ttu-id="2fed8-105">\<tracking></span><span class="sxs-lookup"><span data-stu-id="2fed8-105">\<tracking></span></span>  
<span data-ttu-id="2fed8-106">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="2fed8-106">\<trackingProfile></span></span>  
<span data-ttu-id="2fed8-107">\<workflow></span><span class="sxs-lookup"><span data-stu-id="2fed8-107">\<workflow></span></span>  
<span data-ttu-id="2fed8-108">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="2fed8-108">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="2fed8-109">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="2fed8-109">\<workflowInstanceQuery></span></span>  
<span data-ttu-id="2fed8-110">\<states></span><span class="sxs-lookup"><span data-stu-id="2fed8-110">\<states></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2fed8-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fed8-111">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2fed8-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="2fed8-112">Attributes and Elements</span></span>  
 <span data-ttu-id="2fed8-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="2fed8-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2fed8-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="2fed8-114">Attributes</span></span>  
 <span data-ttu-id="2fed8-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2fed8-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="2fed8-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2fed8-116">Child Elements</span></span>  
  
|<span data-ttu-id="2fed8-117">Élément</span><span class="sxs-lookup"><span data-stu-id="2fed8-117">Element</span></span>|<span data-ttu-id="2fed8-118">Description</span><span class="sxs-lookup"><span data-stu-id="2fed8-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2fed8-119">\<state></span><span class="sxs-lookup"><span data-stu-id="2fed8-119">\<state></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)|<span data-ttu-id="2fed8-120">État faisant l'objet d'un abonnement de l'instance de flux de travail suivie lors de la création de l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="2fed8-120">A subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2fed8-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2fed8-121">Parent Elements</span></span>  
  
|<span data-ttu-id="2fed8-122">Élément</span><span class="sxs-lookup"><span data-stu-id="2fed8-122">Element</span></span>|<span data-ttu-id="2fed8-123">Description</span><span class="sxs-lookup"><span data-stu-id="2fed8-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2fed8-124">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="2fed8-124">\<workflowInstanceQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflowinstancequery.md)|<span data-ttu-id="2fed8-125">Requête qui effectue le suivi des changements dans le cycle de vie d'une instance de flux de travail, tels que le début ou la fin d'un événement.</span><span class="sxs-lookup"><span data-stu-id="2fed8-125">A query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2fed8-126">Notes</span><span class="sxs-lookup"><span data-stu-id="2fed8-126">Remarks</span></span>  
 <span data-ttu-id="2fed8-127">Les enregistrements retournés sont filtrés par états dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="2fed8-127">The returned records are filtered by the states in this collection.</span></span>  
  
 <span data-ttu-id="2fed8-128">Les valeurs d'état possibles sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2fed8-128">Possible state values are described in the following table.</span></span>  
  
|<span data-ttu-id="2fed8-129">État</span><span class="sxs-lookup"><span data-stu-id="2fed8-129">State</span></span>|<span data-ttu-id="2fed8-130">Description</span><span class="sxs-lookup"><span data-stu-id="2fed8-130">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="2fed8-131">Abandonné</span><span class="sxs-lookup"><span data-stu-id="2fed8-131">Aborted</span></span>|<span data-ttu-id="2fed8-132">L'instance de flux de travail est abandonnée.</span><span class="sxs-lookup"><span data-stu-id="2fed8-132">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="2fed8-133">Terminé</span><span class="sxs-lookup"><span data-stu-id="2fed8-133">Completed</span></span>|<span data-ttu-id="2fed8-134">L'instance de flux de travail est terminée.</span><span class="sxs-lookup"><span data-stu-id="2fed8-134">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="2fed8-135">Supprimé</span><span class="sxs-lookup"><span data-stu-id="2fed8-135">Deleted</span></span>|<span data-ttu-id="2fed8-136">L'instance de flux de travail est supprimée.</span><span class="sxs-lookup"><span data-stu-id="2fed8-136">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="2fed8-137">Inactif</span><span class="sxs-lookup"><span data-stu-id="2fed8-137">Idle</span></span>|<span data-ttu-id="2fed8-138">L'instance de workflow est inactive.</span><span class="sxs-lookup"><span data-stu-id="2fed8-138">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="2fed8-139">Persistant</span><span class="sxs-lookup"><span data-stu-id="2fed8-139">Persisted</span></span>|<span data-ttu-id="2fed8-140">L'instance de flux de travail est persistante.</span><span class="sxs-lookup"><span data-stu-id="2fed8-140">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="2fed8-141">Repris</span><span class="sxs-lookup"><span data-stu-id="2fed8-141">Resumed</span></span>|<span data-ttu-id="2fed8-142">L'instance de flux de travail est reprise.</span><span class="sxs-lookup"><span data-stu-id="2fed8-142">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="2fed8-143">Démarré</span><span class="sxs-lookup"><span data-stu-id="2fed8-143">Started</span></span>|<span data-ttu-id="2fed8-144">L'instance de flux de travail est démarrée.</span><span class="sxs-lookup"><span data-stu-id="2fed8-144">The workflow instance is started.</span></span>|  
|<span data-ttu-id="2fed8-145">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="2fed8-145">UnhandledException</span></span>|<span data-ttu-id="2fed8-146">L'instance de flux de travail a rencontré une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="2fed8-146">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="2fed8-147">Non chargé</span><span class="sxs-lookup"><span data-stu-id="2fed8-147">Unloaded</span></span>|<span data-ttu-id="2fed8-148">L'instance de flux de travail est déchargée.</span><span class="sxs-lookup"><span data-stu-id="2fed8-148">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="2fed8-149">Canceled</span><span class="sxs-lookup"><span data-stu-id="2fed8-149">Canceled</span></span>|<span data-ttu-id="2fed8-150">L'instance de flux de travail est annulée.</span><span class="sxs-lookup"><span data-stu-id="2fed8-150">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="2fed8-151">Suspendu</span><span class="sxs-lookup"><span data-stu-id="2fed8-151">Suspended</span></span>|<span data-ttu-id="2fed8-152">L'instance de workflow est interrompue.</span><span class="sxs-lookup"><span data-stu-id="2fed8-152">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="2fed8-153">Arrêté</span><span class="sxs-lookup"><span data-stu-id="2fed8-153">Terminated</span></span>|<span data-ttu-id="2fed8-154">L'instance de flux de travail est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="2fed8-154">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="2fed8-155">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="2fed8-155">Unsuspended</span></span>|<span data-ttu-id="2fed8-156">L'instance de flux de travail est non interrompue.</span><span class="sxs-lookup"><span data-stu-id="2fed8-156">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="2fed8-157">Exemple</span><span class="sxs-lookup"><span data-stu-id="2fed8-157">Example</span></span>  
 <span data-ttu-id="2fed8-158">La configuration suivante permet de s'abonner aux enregistrements de suivi au niveau de l'instance de flux de travail pour l'état de l'instance `Started` à l'aide de cette requête.</span><span class="sxs-lookup"><span data-stu-id="2fed8-158">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="2fed8-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fed8-159">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="2fed8-160">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="2fed8-160">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="2fed8-161">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="2fed8-161">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
