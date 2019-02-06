---
title: <workflowInstanceQueries> de WCF
ms.date: 03/30/2017
ms.assetid: b0852f77-16e4-4d55-8eb7-a19feb0e8fc4
ms.openlocfilehash: 89e122b87743a81a80ce63b382ae235c1c4863bc
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2019
ms.locfileid: "55759247"
---
# <a name="workflowinstancequeries-of-wcf"></a><span data-ttu-id="88616-102">\<workflowInstanceQueries > de WCF</span><span class="sxs-lookup"><span data-stu-id="88616-102">\<workflowInstanceQueries> of WCF</span></span>

<span data-ttu-id="88616-103">Représente une collection d’éléments de configuration qui effectuent le suivi des changements dans le cycle de vie d’une instance de flux de travail, tels que le début ou la fin d’un événement.</span><span class="sxs-lookup"><span data-stu-id="88616-103">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>  
  
<span data-ttu-id="88616-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="88616-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="88616-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="88616-105">\<system.serviceModel></span></span>  
<span data-ttu-id="88616-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="88616-106">\<tracking></span></span>  
<span data-ttu-id="88616-107">\<profiles></span><span class="sxs-lookup"><span data-stu-id="88616-107">\<profiles></span></span>  
<span data-ttu-id="88616-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="88616-108">\<trackingProfile></span></span>  
<span data-ttu-id="88616-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="88616-109">\<workflow></span></span>  
<span data-ttu-id="88616-110">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="88616-110">\<workflowInstanceQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="88616-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88616-111">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="88616-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="88616-112">Attributes and elements</span></span>

<span data-ttu-id="88616-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="88616-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="88616-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="88616-114">Attributes</span></span>  

<span data-ttu-id="88616-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="88616-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="88616-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="88616-116">Child elements</span></span>  
  
|<span data-ttu-id="88616-117">Élément</span><span class="sxs-lookup"><span data-stu-id="88616-117">Element</span></span>|<span data-ttu-id="88616-118">Description</span><span class="sxs-lookup"><span data-stu-id="88616-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="88616-119">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="88616-119">\<workflowInstanceQuery></span></span>](workflowinstancequery-of-wcf.md)|<span data-ttu-id="88616-120">Requête qui permet d'effectuer le suivi des changements dans le cycle de vie d'une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="88616-120">A query that is used to track workflow instance life cycle changes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="88616-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="88616-121">Parent elements</span></span>  
  
|<span data-ttu-id="88616-122">Élément</span><span class="sxs-lookup"><span data-stu-id="88616-122">Element</span></span>|<span data-ttu-id="88616-123">Description</span><span class="sxs-lookup"><span data-stu-id="88616-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="88616-124">\<workflow></span><span class="sxs-lookup"><span data-stu-id="88616-124">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="88616-125">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le [activityDefinitionId](xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileWorkflowElement.ActivityDefinitionId) propriété.</span><span class="sxs-lookup"><span data-stu-id="88616-125">A configuration element that contains all queries for a specific workflow identified by the [activityDefinitionId](xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileWorkflowElement.ActivityDefinitionId) property.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="88616-126">Notes</span><span class="sxs-lookup"><span data-stu-id="88616-126">Remarks</span></span>

<span data-ttu-id="88616-127">L'objet <xref:System.Activities.Tracking.WorkflowInstanceQuery> sert à s'abonner aux objets <xref:System.Activities.Tracking.TrackingRecord> suivants :</span><span class="sxs-lookup"><span data-stu-id="88616-127">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="88616-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="88616-128">Example</span></span>  

<span data-ttu-id="88616-129">La configuration suivante permet de s'abonner aux enregistrements de suivi au niveau de l'instance de flux de travail pour l'état de l'instance `Started` à l'aide de cette requête.</span><span class="sxs-lookup"><span data-stu-id="88616-129">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="88616-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88616-130">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="88616-131">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="88616-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="88616-132">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="88616-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
