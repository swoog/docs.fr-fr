---
title: <workflowInstanceQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 4fe7ce85-cf9a-4dbf-a8f7-bc9b1fc2fe35
ms.openlocfilehash: e54f98c980f60d02377e38d53d9d0eb48581eec0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59132481"
---
# <a name="workflowinstancequeries"></a><span data-ttu-id="01797-101">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="01797-101">\<workflowInstanceQueries></span></span>
<span data-ttu-id="01797-102">Représente une collection d'éléments de configuration qui effectuent le suivi des changements dans le cycle de vie d'une instance de flux de travail, tels que le début ou la fin d'un événement.</span><span class="sxs-lookup"><span data-stu-id="01797-102">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>  
  
 <span data-ttu-id="01797-103">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="01797-103">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="01797-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="01797-104">\<system.serviceModel></span></span>  
<span data-ttu-id="01797-105">\<tracking></span><span class="sxs-lookup"><span data-stu-id="01797-105">\<tracking></span></span>  
<span data-ttu-id="01797-106">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="01797-106">\<trackingProfile></span></span>  
<span data-ttu-id="01797-107">\<workflow></span><span class="sxs-lookup"><span data-stu-id="01797-107">\<workflow></span></span>  
<span data-ttu-id="01797-108">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="01797-108">\<workflowInstanceQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="01797-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01797-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="01797-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="01797-110">Attributes and Elements</span></span>  
 <span data-ttu-id="01797-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="01797-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="01797-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="01797-112">Attributes</span></span>  
 <span data-ttu-id="01797-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="01797-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="01797-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="01797-114">Child Elements</span></span>  
  
|<span data-ttu-id="01797-115">Élément</span><span class="sxs-lookup"><span data-stu-id="01797-115">Element</span></span>|<span data-ttu-id="01797-116">Description</span><span class="sxs-lookup"><span data-stu-id="01797-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="01797-117">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="01797-117">\<workflowInstanceQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflowinstancequery.md)|<span data-ttu-id="01797-118">Requête qui permet d'effectuer le suivi des changements dans le cycle de vie d'une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="01797-118">A query that is used to track workflow instance life cycle changes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="01797-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="01797-119">Parent Elements</span></span>  
  
|<span data-ttu-id="01797-120">Élément</span><span class="sxs-lookup"><span data-stu-id="01797-120">Element</span></span>|<span data-ttu-id="01797-121">Description</span><span class="sxs-lookup"><span data-stu-id="01797-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="01797-122">\<workflow></span><span class="sxs-lookup"><span data-stu-id="01797-122">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="01797-123">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le **activityDefinitionId** propriété.</span><span class="sxs-lookup"><span data-stu-id="01797-123">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="01797-124">Notes</span><span class="sxs-lookup"><span data-stu-id="01797-124">Remarks</span></span>  
 <span data-ttu-id="01797-125">L'objet <xref:System.Activities.Tracking.WorkflowInstanceQuery> sert à s'abonner aux objets <xref:System.Activities.Tracking.TrackingRecord> suivants :</span><span class="sxs-lookup"><span data-stu-id="01797-125">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="01797-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="01797-126">Example</span></span>  
 <span data-ttu-id="01797-127">La configuration suivante permet de s'abonner aux enregistrements de suivi au niveau de l'instance de flux de travail pour l'état de l'instance `Started` à l'aide de cette requête.</span><span class="sxs-lookup"><span data-stu-id="01797-127">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="01797-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01797-128">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="01797-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="01797-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="01797-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="01797-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
