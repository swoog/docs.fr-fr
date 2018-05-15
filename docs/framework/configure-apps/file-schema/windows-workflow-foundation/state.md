---
title: '&lt;state&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 619414f2-61c2-4427-9977-d05009e343db
ms.openlocfilehash: 327a5e98a9ecf6ba23eaf47c3d6d73bfb7852ee7
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltstategt"></a><span data-ttu-id="b9859-102">&lt;state&gt;</span><span class="sxs-lookup"><span data-stu-id="b9859-102">&lt;state&gt;</span></span>
<span data-ttu-id="b9859-103">Représente une collection d’états faisant l’objet d’un abonnement dans l’instance de flux de travail suivie lors de la création des enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="b9859-103">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
 <span data-ttu-id="b9859-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="b9859-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="b9859-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="b9859-105">\<system.serviceModel></span></span>  
<span data-ttu-id="b9859-106">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="b9859-106">\<tracking></span></span>  
<span data-ttu-id="b9859-107">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="b9859-107">\<trackingProfile></span></span>  
<span data-ttu-id="b9859-108">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="b9859-108">\<workflow></span></span>  
<span data-ttu-id="b9859-109">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="b9859-109">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="b9859-110">\<workflowInstanceQuery ></span><span class="sxs-lookup"><span data-stu-id="b9859-110">\<workflowInstanceQuery></span></span>  
<span data-ttu-id="b9859-111">\<États ></span><span class="sxs-lookup"><span data-stu-id="b9859-111">\<states></span></span>  
<span data-ttu-id="b9859-112">\<état ></span><span class="sxs-lookup"><span data-stu-id="b9859-112">\<state></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9859-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9859-113">Syntax</span></span>  
  
```xml  
<tracking>
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
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b9859-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b9859-114">Attributes and Elements</span></span>  
 <span data-ttu-id="b9859-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b9859-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b9859-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="b9859-116">Attributes</span></span>  
  
|<span data-ttu-id="b9859-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="b9859-117">Attribute</span></span>|<span data-ttu-id="b9859-118">Description</span><span class="sxs-lookup"><span data-stu-id="b9859-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b9859-119">name</span><span class="sxs-lookup"><span data-stu-id="b9859-119">name</span></span>|<span data-ttu-id="b9859-120">Chaîne qui spécifie un état faisant l'objet d'un abonnement dans l'instance de flux de travail suivie lors de la création de l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="b9859-120">A string that specifies a subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b9859-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b9859-121">Child Elements</span></span>  
 <span data-ttu-id="b9859-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b9859-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b9859-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b9859-123">Parent Elements</span></span>  
  
|<span data-ttu-id="b9859-124">Élément</span><span class="sxs-lookup"><span data-stu-id="b9859-124">Element</span></span>|<span data-ttu-id="b9859-125">Description</span><span class="sxs-lookup"><span data-stu-id="b9859-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b9859-126">\<États ></span><span class="sxs-lookup"><span data-stu-id="b9859-126">\<states></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)|<span data-ttu-id="b9859-127">Collection d’états faisant l’objet d’un abonnement dans l’instance de flux de travail suivie lors de la création des enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="b9859-127">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b9859-128">Notes</span><span class="sxs-lookup"><span data-stu-id="b9859-128">Remarks</span></span>  
 <span data-ttu-id="b9859-129">Les enregistrements retournés sont filtrés par états dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="b9859-129">The returned records are filtered by the states in this collection.</span></span>  
  
 <span data-ttu-id="b9859-130">Les valeurs d'état possibles sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b9859-130">Possible state values are described in the following table.</span></span>  
  
|<span data-ttu-id="b9859-131">État</span><span class="sxs-lookup"><span data-stu-id="b9859-131">State</span></span>|<span data-ttu-id="b9859-132">Description</span><span class="sxs-lookup"><span data-stu-id="b9859-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="b9859-133">Abandonné</span><span class="sxs-lookup"><span data-stu-id="b9859-133">Aborted</span></span>|<span data-ttu-id="b9859-134">L'instance de flux de travail est abandonnée.</span><span class="sxs-lookup"><span data-stu-id="b9859-134">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="b9859-135">Terminé</span><span class="sxs-lookup"><span data-stu-id="b9859-135">Completed</span></span>|<span data-ttu-id="b9859-136">L'instance de flux de travail est terminée.</span><span class="sxs-lookup"><span data-stu-id="b9859-136">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="b9859-137">Supprimé</span><span class="sxs-lookup"><span data-stu-id="b9859-137">Deleted</span></span>|<span data-ttu-id="b9859-138">L'instance de flux de travail est supprimée.</span><span class="sxs-lookup"><span data-stu-id="b9859-138">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="b9859-139">Inactif</span><span class="sxs-lookup"><span data-stu-id="b9859-139">Idle</span></span>|<span data-ttu-id="b9859-140">L'instance de workflow est inactive.</span><span class="sxs-lookup"><span data-stu-id="b9859-140">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="b9859-141">Persistant</span><span class="sxs-lookup"><span data-stu-id="b9859-141">Persisted</span></span>|<span data-ttu-id="b9859-142">L'instance de flux de travail est persistante.</span><span class="sxs-lookup"><span data-stu-id="b9859-142">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="b9859-143">Repris</span><span class="sxs-lookup"><span data-stu-id="b9859-143">Resumed</span></span>|<span data-ttu-id="b9859-144">L'instance de flux de travail est reprise.</span><span class="sxs-lookup"><span data-stu-id="b9859-144">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="b9859-145">Démarré</span><span class="sxs-lookup"><span data-stu-id="b9859-145">Started</span></span>|<span data-ttu-id="b9859-146">L'instance de flux de travail est démarrée.</span><span class="sxs-lookup"><span data-stu-id="b9859-146">The workflow instance is started.</span></span>|  
|<span data-ttu-id="b9859-147">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="b9859-147">UnhandledException</span></span>|<span data-ttu-id="b9859-148">L'instance de flux de travail a rencontré une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="b9859-148">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="b9859-149">Unloaded</span><span class="sxs-lookup"><span data-stu-id="b9859-149">Unloaded</span></span>|<span data-ttu-id="b9859-150">L'instance de flux de travail est déchargée.</span><span class="sxs-lookup"><span data-stu-id="b9859-150">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="b9859-151">Canceled</span><span class="sxs-lookup"><span data-stu-id="b9859-151">Canceled</span></span>|<span data-ttu-id="b9859-152">L'instance de flux de travail est annulée.</span><span class="sxs-lookup"><span data-stu-id="b9859-152">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="b9859-153">Interrompu</span><span class="sxs-lookup"><span data-stu-id="b9859-153">Suspended</span></span>|<span data-ttu-id="b9859-154">L'instance de workflow est interrompue.</span><span class="sxs-lookup"><span data-stu-id="b9859-154">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="b9859-155">Arrêté</span><span class="sxs-lookup"><span data-stu-id="b9859-155">Terminated</span></span>|<span data-ttu-id="b9859-156">L'instance de flux de travail est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="b9859-156">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="b9859-157">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="b9859-157">Unsuspended</span></span>|<span data-ttu-id="b9859-158">L'instance de flux de travail est non interrompue.</span><span class="sxs-lookup"><span data-stu-id="b9859-158">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="b9859-159">Exemple</span><span class="sxs-lookup"><span data-stu-id="b9859-159">Example</span></span>  
 <span data-ttu-id="b9859-160">La configuration suivante permet de s'abonner aux enregistrements de suivi au niveau de l'instance de flux de travail pour l'état de l'instance `Started` à l'aide de cette requête.</span><span class="sxs-lookup"><span data-stu-id="b9859-160">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="b9859-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9859-161">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>       
 <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>      
 [<span data-ttu-id="b9859-162">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="b9859-162">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="b9859-163">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="b9859-163">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
