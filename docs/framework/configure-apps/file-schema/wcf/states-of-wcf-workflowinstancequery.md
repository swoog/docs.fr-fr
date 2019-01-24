---
title: '&lt;states&gt; de WCF, &lt;workflowInstanceQuery&gt;'
ms.date: 03/30/2017
ms.assetid: d17f7525-8035-4e9e-85a0-4cddae59f85d
ms.openlocfilehash: 56e3c6ce5c86e468c9a4dd63021264703ab75b02
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54540817"
---
# <a name="ltstatesgt-of-wcf-ltworkflowinstancequerygt"></a><span data-ttu-id="1bb70-102">&lt;states&gt; de WCF, &lt;workflowInstanceQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="1bb70-102">&lt;states&gt; of WCF, &lt;workflowInstanceQuery&gt;</span></span>

<span data-ttu-id="1bb70-103">Représente une collection d’états faisant l’objet d’un abonnement dans l’instance de flux de travail suivie lors de la création des enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="1bb70-103">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
<span data-ttu-id="1bb70-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="1bb70-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="1bb70-105">\<system.serviceModel> \<tracking></span><span class="sxs-lookup"><span data-stu-id="1bb70-105">\<system.serviceModel> \<tracking></span></span>  
<span data-ttu-id="1bb70-106">\<profiles></span><span class="sxs-lookup"><span data-stu-id="1bb70-106">\<profiles></span></span>  
<span data-ttu-id="1bb70-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="1bb70-107">\<trackingProfile></span></span>  
<span data-ttu-id="1bb70-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="1bb70-108">\<workflow></span></span>  
<span data-ttu-id="1bb70-109">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="1bb70-109">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="1bb70-110">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="1bb70-110">\<workflowInstanceQuery></span></span>  
<span data-ttu-id="1bb70-111">\<states></span><span class="sxs-lookup"><span data-stu-id="1bb70-111">\<states></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1bb70-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bb70-112">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <workflowInstanceQueries>
          <workflowInstanceQuery>
            <states>
              <state name="Name" />
            </states>
          </workflowInstanceQuery>
        </workflowInstanceQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1bb70-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1bb70-113">Attributes and elements</span></span>

<span data-ttu-id="1bb70-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1bb70-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1bb70-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="1bb70-115">Attributes</span></span>  

<span data-ttu-id="1bb70-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1bb70-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="1bb70-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1bb70-117">Child elements</span></span>
  
|<span data-ttu-id="1bb70-118">Élément</span><span class="sxs-lookup"><span data-stu-id="1bb70-118">Element</span></span>|<span data-ttu-id="1bb70-119">Description</span><span class="sxs-lookup"><span data-stu-id="1bb70-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1bb70-120">\<states></span><span class="sxs-lookup"><span data-stu-id="1bb70-120">\<states></span></span>](state-of-wcf-workflowinstancequery.md)|<span data-ttu-id="1bb70-121">État faisant l'objet d'un abonnement de l'instance de flux de travail suivie lors de la création de l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="1bb70-121">A subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1bb70-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1bb70-122">Parent elements</span></span>  
  
|<span data-ttu-id="1bb70-123">Élément</span><span class="sxs-lookup"><span data-stu-id="1bb70-123">Element</span></span>|<span data-ttu-id="1bb70-124">Description</span><span class="sxs-lookup"><span data-stu-id="1bb70-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1bb70-125">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="1bb70-125">\<workflowInstanceQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflowinstancequery.md)|<span data-ttu-id="1bb70-126">Requête qui effectue le suivi des changements dans le cycle de vie d'une instance de flux de travail, tels que le début ou la fin d'un événement.</span><span class="sxs-lookup"><span data-stu-id="1bb70-126">A query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1bb70-127">Notes</span><span class="sxs-lookup"><span data-stu-id="1bb70-127">Remarks</span></span>

<span data-ttu-id="1bb70-128">Les enregistrements retournés sont filtrés par états dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="1bb70-128">The returned records are filtered by the states in this collection.</span></span>  
  
<span data-ttu-id="1bb70-129">Les valeurs d'état possibles sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1bb70-129">Possible state values are described in the following table.</span></span>  
  
|<span data-ttu-id="1bb70-130">État</span><span class="sxs-lookup"><span data-stu-id="1bb70-130">State</span></span>|<span data-ttu-id="1bb70-131">Description</span><span class="sxs-lookup"><span data-stu-id="1bb70-131">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="1bb70-132">Abandonné</span><span class="sxs-lookup"><span data-stu-id="1bb70-132">Aborted</span></span>|<span data-ttu-id="1bb70-133">L'instance de flux de travail est abandonnée.</span><span class="sxs-lookup"><span data-stu-id="1bb70-133">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="1bb70-134">Terminé</span><span class="sxs-lookup"><span data-stu-id="1bb70-134">Completed</span></span>|<span data-ttu-id="1bb70-135">L'instance de flux de travail est terminée.</span><span class="sxs-lookup"><span data-stu-id="1bb70-135">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="1bb70-136">Supprimé</span><span class="sxs-lookup"><span data-stu-id="1bb70-136">Deleted</span></span>|<span data-ttu-id="1bb70-137">L'instance de flux de travail est supprimée.</span><span class="sxs-lookup"><span data-stu-id="1bb70-137">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="1bb70-138">Inactif</span><span class="sxs-lookup"><span data-stu-id="1bb70-138">Idle</span></span>|<span data-ttu-id="1bb70-139">L'instance de workflow est inactive.</span><span class="sxs-lookup"><span data-stu-id="1bb70-139">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="1bb70-140">Persistant</span><span class="sxs-lookup"><span data-stu-id="1bb70-140">Persisted</span></span>|<span data-ttu-id="1bb70-141">L'instance de flux de travail est persistante.</span><span class="sxs-lookup"><span data-stu-id="1bb70-141">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="1bb70-142">Repris</span><span class="sxs-lookup"><span data-stu-id="1bb70-142">Resumed</span></span>|<span data-ttu-id="1bb70-143">L'instance de flux de travail est reprise.</span><span class="sxs-lookup"><span data-stu-id="1bb70-143">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="1bb70-144">Démarré</span><span class="sxs-lookup"><span data-stu-id="1bb70-144">Started</span></span>|<span data-ttu-id="1bb70-145">L'instance de flux de travail est démarrée.</span><span class="sxs-lookup"><span data-stu-id="1bb70-145">The workflow instance is started.</span></span>|  
|<span data-ttu-id="1bb70-146">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="1bb70-146">UnhandledException</span></span>|<span data-ttu-id="1bb70-147">L'instance de flux de travail a rencontré une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="1bb70-147">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="1bb70-148">Unloaded</span><span class="sxs-lookup"><span data-stu-id="1bb70-148">Unloaded</span></span>|<span data-ttu-id="1bb70-149">L'instance de flux de travail est déchargée.</span><span class="sxs-lookup"><span data-stu-id="1bb70-149">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="1bb70-150">Canceled</span><span class="sxs-lookup"><span data-stu-id="1bb70-150">Canceled</span></span>|<span data-ttu-id="1bb70-151">L'instance de flux de travail est annulée.</span><span class="sxs-lookup"><span data-stu-id="1bb70-151">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="1bb70-152">Interrompu</span><span class="sxs-lookup"><span data-stu-id="1bb70-152">Suspended</span></span>|<span data-ttu-id="1bb70-153">L'instance de workflow est interrompue.</span><span class="sxs-lookup"><span data-stu-id="1bb70-153">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="1bb70-154">Arrêté</span><span class="sxs-lookup"><span data-stu-id="1bb70-154">Terminated</span></span>|<span data-ttu-id="1bb70-155">L'instance de flux de travail est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="1bb70-155">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="1bb70-156">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="1bb70-156">Unsuspended</span></span>|<span data-ttu-id="1bb70-157">L'instance de flux de travail est non interrompue.</span><span class="sxs-lookup"><span data-stu-id="1bb70-157">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="1bb70-158">Exemple</span><span class="sxs-lookup"><span data-stu-id="1bb70-158">Example</span></span>

<span data-ttu-id="1bb70-159">La configuration suivante permet de s'abonner aux enregistrements de suivi au niveau de l'instance de flux de travail pour l'état de l'instance `Started` à l'aide de cette requête.</span><span class="sxs-lookup"><span data-stu-id="1bb70-159">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="1bb70-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bb70-160">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="1bb70-161">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="1bb70-161">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="1bb70-162">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="1bb70-162">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
