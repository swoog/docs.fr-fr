---
title: <workflowInstanceQueries> de WCF
ms.date: 03/30/2017
ms.assetid: b0852f77-16e4-4d55-8eb7-a19feb0e8fc4
ms.openlocfilehash: 544ca868485a409554ece9d9b000beb1a472d344
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255300"
---
# <a name="workflowinstancequeries-of-wcf"></a><span data-ttu-id="811d9-102">\<workflowInstanceQueries > de WCF</span><span class="sxs-lookup"><span data-stu-id="811d9-102">\<workflowInstanceQueries> of WCF</span></span>

<span data-ttu-id="811d9-103">Représente une collection d’éléments de configuration qui effectuent le suivi des changements dans le cycle de vie d’une instance de flux de travail, tels que le début ou la fin d’un événement.</span><span class="sxs-lookup"><span data-stu-id="811d9-103">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>  
  
<span data-ttu-id="811d9-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="811d9-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="811d9-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="811d9-105">\<system.serviceModel></span></span>  
<span data-ttu-id="811d9-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="811d9-106">\<tracking></span></span>  
<span data-ttu-id="811d9-107">\<profiles></span><span class="sxs-lookup"><span data-stu-id="811d9-107">\<profiles></span></span>  
<span data-ttu-id="811d9-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="811d9-108">\<trackingProfile></span></span>  
<span data-ttu-id="811d9-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="811d9-109">\<workflow></span></span>  
<span data-ttu-id="811d9-110">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="811d9-110">\<workflowInstanceQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="811d9-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="811d9-111">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="811d9-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="811d9-112">Attributes and elements</span></span>

<span data-ttu-id="811d9-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="811d9-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="811d9-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="811d9-114">Attributes</span></span>  

<span data-ttu-id="811d9-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="811d9-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="811d9-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="811d9-116">Child elements</span></span>  
  
|<span data-ttu-id="811d9-117">Élément</span><span class="sxs-lookup"><span data-stu-id="811d9-117">Element</span></span>|<span data-ttu-id="811d9-118">Description</span><span class="sxs-lookup"><span data-stu-id="811d9-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="811d9-119">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="811d9-119">\<workflowInstanceQuery></span></span>](workflowinstancequery-of-wcf.md)|<span data-ttu-id="811d9-120">Requête qui permet d'effectuer le suivi des changements dans le cycle de vie d'une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="811d9-120">A query that is used to track workflow instance life cycle changes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="811d9-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="811d9-121">Parent elements</span></span>  
  
|<span data-ttu-id="811d9-122">Élément</span><span class="sxs-lookup"><span data-stu-id="811d9-122">Element</span></span>|<span data-ttu-id="811d9-123">Description</span><span class="sxs-lookup"><span data-stu-id="811d9-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="811d9-124">\<workflow></span><span class="sxs-lookup"><span data-stu-id="811d9-124">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="811d9-125">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le [activityDefinitionId](https://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx) propriété.</span><span class="sxs-lookup"><span data-stu-id="811d9-125">A configuration element that contains all queries for a specific workflow identified by the [activityDefinitionId](https://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx) property.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="811d9-126">Notes</span><span class="sxs-lookup"><span data-stu-id="811d9-126">Remarks</span></span>

<span data-ttu-id="811d9-127">L'objet <xref:System.Activities.Tracking.WorkflowInstanceQuery> sert à s'abonner aux objets <xref:System.Activities.Tracking.TrackingRecord> suivants :</span><span class="sxs-lookup"><span data-stu-id="811d9-127">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="811d9-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="811d9-128">Example</span></span>  

<span data-ttu-id="811d9-129">La configuration suivante permet de s'abonner aux enregistrements de suivi au niveau de l'instance de flux de travail pour l'état de l'instance `Started` à l'aide de cette requête.</span><span class="sxs-lookup"><span data-stu-id="811d9-129">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="811d9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="811d9-130">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="811d9-131">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="811d9-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="811d9-132">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="811d9-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
