---
title: '&lt;state&gt; de WCF, &lt;workflowInstanceQuery&gt;'
ms.date: 03/30/2017
ms.assetid: 40f21055-766c-4be9-86c4-d1d899007098
ms.openlocfilehash: 168a6980e955f602ee60bff26461f06cb16c836a
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145924"
---
# <a name="ltstategt-of-wcf-ltworkflowinstancequerygt"></a><span data-ttu-id="b4a60-102">&lt;state&gt; de WCF, &lt;workflowInstanceQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="b4a60-102">&lt;state&gt; of WCF, &lt;workflowInstanceQuery&gt;</span></span>
<span data-ttu-id="b4a60-103">Représente une collection d’états faisant l’objet d’un abonnement dans l’instance de flux de travail suivie lors de la création des enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="b4a60-103">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
 <span data-ttu-id="b4a60-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="b4a60-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="b4a60-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="b4a60-105">\<system.serviceModel></span></span>  
<span data-ttu-id="b4a60-106">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="b4a60-106">\<tracking></span></span>  
<span data-ttu-id="b4a60-107">\<profils ></span><span class="sxs-lookup"><span data-stu-id="b4a60-107">\<profiles></span></span>  
<span data-ttu-id="b4a60-108">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="b4a60-108">\<trackingProfile></span></span>  
<span data-ttu-id="b4a60-109">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="b4a60-109">\<workflow></span></span>  
<span data-ttu-id="b4a60-110">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="b4a60-110">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="b4a60-111">\<workflowInstanceQuery ></span><span class="sxs-lookup"><span data-stu-id="b4a60-111">\<workflowInstanceQuery></span></span>  
<span data-ttu-id="b4a60-112">\<États ></span><span class="sxs-lookup"><span data-stu-id="b4a60-112">\<states></span></span>  
<span data-ttu-id="b4a60-113">\<état ></span><span class="sxs-lookup"><span data-stu-id="b4a60-113">\<state></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b4a60-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4a60-114">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b4a60-115">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b4a60-115">Attributes and elements</span></span>

<span data-ttu-id="b4a60-116">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b4a60-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4a60-117">Attributs</span><span class="sxs-lookup"><span data-stu-id="b4a60-117">Attributes</span></span>

|<span data-ttu-id="b4a60-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="b4a60-118">Attribute</span></span>|<span data-ttu-id="b4a60-119">Description</span><span class="sxs-lookup"><span data-stu-id="b4a60-119">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="b4a60-120">Chaîne qui spécifie un état faisant l'objet d'un abonnement dans l'instance de flux de travail suivie lors de la création de l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="b4a60-120">A string that specifies a subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b4a60-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b4a60-121">Child elements</span></span>

<span data-ttu-id="b4a60-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b4a60-122">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="b4a60-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b4a60-123">Parent elements</span></span>

|<span data-ttu-id="b4a60-124">Élément</span><span class="sxs-lookup"><span data-stu-id="b4a60-124">Element</span></span>|<span data-ttu-id="b4a60-125">Description</span><span class="sxs-lookup"><span data-stu-id="b4a60-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b4a60-126">\<États ></span><span class="sxs-lookup"><span data-stu-id="b4a60-126">\<states></span></span>](states-of-wcf-workflowinstancequery.md)|<span data-ttu-id="b4a60-127">Collection d’états faisant l’objet d’un abonnement dans l’instance de flux de travail suivie lors de la création des enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="b4a60-127">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b4a60-128">Notes</span><span class="sxs-lookup"><span data-stu-id="b4a60-128">Remarks</span></span>  

<span data-ttu-id="b4a60-129">Les enregistrements retournés sont filtrés par états dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="b4a60-129">The returned records are filtered by the states in this collection.</span></span>  
  
<span data-ttu-id="b4a60-130">Valeurs d’état possibles sont décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="b4a60-130">Possible state values are described in the following table:</span></span>
  
|<span data-ttu-id="b4a60-131">État</span><span class="sxs-lookup"><span data-stu-id="b4a60-131">State</span></span>|<span data-ttu-id="b4a60-132">Description</span><span class="sxs-lookup"><span data-stu-id="b4a60-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="b4a60-133">Abandonné</span><span class="sxs-lookup"><span data-stu-id="b4a60-133">Aborted</span></span>|<span data-ttu-id="b4a60-134">L'instance de flux de travail est abandonnée.</span><span class="sxs-lookup"><span data-stu-id="b4a60-134">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="b4a60-135">Terminé</span><span class="sxs-lookup"><span data-stu-id="b4a60-135">Completed</span></span>|<span data-ttu-id="b4a60-136">L'instance de flux de travail est terminée.</span><span class="sxs-lookup"><span data-stu-id="b4a60-136">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="b4a60-137">Supprimé</span><span class="sxs-lookup"><span data-stu-id="b4a60-137">Deleted</span></span>|<span data-ttu-id="b4a60-138">L'instance de flux de travail est supprimée.</span><span class="sxs-lookup"><span data-stu-id="b4a60-138">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="b4a60-139">Inactif</span><span class="sxs-lookup"><span data-stu-id="b4a60-139">Idle</span></span>|<span data-ttu-id="b4a60-140">L'instance de workflow est inactive.</span><span class="sxs-lookup"><span data-stu-id="b4a60-140">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="b4a60-141">Persistant</span><span class="sxs-lookup"><span data-stu-id="b4a60-141">Persisted</span></span>|<span data-ttu-id="b4a60-142">L'instance de flux de travail est persistante.</span><span class="sxs-lookup"><span data-stu-id="b4a60-142">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="b4a60-143">Repris</span><span class="sxs-lookup"><span data-stu-id="b4a60-143">Resumed</span></span>|<span data-ttu-id="b4a60-144">L'instance de flux de travail est reprise.</span><span class="sxs-lookup"><span data-stu-id="b4a60-144">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="b4a60-145">Démarré</span><span class="sxs-lookup"><span data-stu-id="b4a60-145">Started</span></span>|<span data-ttu-id="b4a60-146">L'instance de flux de travail est démarrée.</span><span class="sxs-lookup"><span data-stu-id="b4a60-146">The workflow instance is started.</span></span>|  
|<span data-ttu-id="b4a60-147">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="b4a60-147">UnhandledException</span></span>|<span data-ttu-id="b4a60-148">L'instance de flux de travail a rencontré une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="b4a60-148">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="b4a60-149">Unloaded</span><span class="sxs-lookup"><span data-stu-id="b4a60-149">Unloaded</span></span>|<span data-ttu-id="b4a60-150">L'instance de flux de travail est déchargée.</span><span class="sxs-lookup"><span data-stu-id="b4a60-150">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="b4a60-151">Canceled</span><span class="sxs-lookup"><span data-stu-id="b4a60-151">Canceled</span></span>|<span data-ttu-id="b4a60-152">L'instance de flux de travail est annulée.</span><span class="sxs-lookup"><span data-stu-id="b4a60-152">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="b4a60-153">Interrompu</span><span class="sxs-lookup"><span data-stu-id="b4a60-153">Suspended</span></span>|<span data-ttu-id="b4a60-154">L'instance de workflow est interrompue.</span><span class="sxs-lookup"><span data-stu-id="b4a60-154">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="b4a60-155">Arrêté</span><span class="sxs-lookup"><span data-stu-id="b4a60-155">Terminated</span></span>|<span data-ttu-id="b4a60-156">L'instance de flux de travail est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="b4a60-156">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="b4a60-157">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="b4a60-157">Unsuspended</span></span>|<span data-ttu-id="b4a60-158">L'instance de flux de travail est non interrompue.</span><span class="sxs-lookup"><span data-stu-id="b4a60-158">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="b4a60-159">Exemple</span><span class="sxs-lookup"><span data-stu-id="b4a60-159">Example</span></span>

<span data-ttu-id="b4a60-160">La configuration suivante permet de s'abonner aux enregistrements de suivi au niveau de l'instance de flux de travail pour l'état de l'instance `Started` à l'aide de cette requête.</span><span class="sxs-lookup"><span data-stu-id="b4a60-160">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="b4a60-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4a60-161">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="b4a60-162">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="b4a60-162">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="b4a60-163">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="b4a60-163">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
