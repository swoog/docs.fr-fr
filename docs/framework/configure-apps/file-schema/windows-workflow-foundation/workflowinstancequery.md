---
title: <workflowInstanceQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 9096e812-626a-409a-9eda-c31a60b84c55
ms.openlocfilehash: 7541ddcf4df8135d82b1f7f5ae2c02f031090e17
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55275062"
---
# <a name="workflowinstancequery"></a><span data-ttu-id="0f999-101">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="0f999-101">\<workflowInstanceQuery></span></span>
<span data-ttu-id="0f999-102">Représente une requête qui effectue le suivi des changements dans le cycle de vie d'une instance de flux de travail, tels que le début et la fin d'un événement.</span><span class="sxs-lookup"><span data-stu-id="0f999-102">Represents a query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>  
  
 <span data-ttu-id="0f999-103">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="0f999-103">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="0f999-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="0f999-104">\<system.serviceModel></span></span>  
<span data-ttu-id="0f999-105">\<tracking></span><span class="sxs-lookup"><span data-stu-id="0f999-105">\<tracking></span></span>  
<span data-ttu-id="0f999-106">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="0f999-106">\<trackingProfile></span></span>  
<span data-ttu-id="0f999-107">\<workflow></span><span class="sxs-lookup"><span data-stu-id="0f999-107">\<workflow></span></span>  
<span data-ttu-id="0f999-108">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="0f999-108">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="0f999-109">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="0f999-109">\<workflowInstanceQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f999-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f999-110">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0f999-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0f999-111">Attributes and Elements</span></span>  
 <span data-ttu-id="0f999-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0f999-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0f999-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="0f999-113">Attributes</span></span>  
 <span data-ttu-id="0f999-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0f999-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0f999-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0f999-115">Child Elements</span></span>  
  
|<span data-ttu-id="0f999-116">Élément</span><span class="sxs-lookup"><span data-stu-id="0f999-116">Element</span></span>|<span data-ttu-id="0f999-117">Description</span><span class="sxs-lookup"><span data-stu-id="0f999-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0f999-118">\<states></span><span class="sxs-lookup"><span data-stu-id="0f999-118">\<states></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)|<span data-ttu-id="0f999-119">Collection d’états faisant l’objet d’un abonnement dans l’instance de flux de travail suivie lors de la création des enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="0f999-119">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0f999-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0f999-120">Parent Elements</span></span>  
  
|<span data-ttu-id="0f999-121">Élément</span><span class="sxs-lookup"><span data-stu-id="0f999-121">Element</span></span>|<span data-ttu-id="0f999-122">Description</span><span class="sxs-lookup"><span data-stu-id="0f999-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0f999-123">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="0f999-123">\<workflowInstanceQueries></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflowinstancequeries.md)|<span data-ttu-id="0f999-124">Représente une collection d’éléments de configuration qui effectuent le suivi des changements dans le cycle de vie d’une instance de flux de travail, tels que le début ou la fin d’un événement.</span><span class="sxs-lookup"><span data-stu-id="0f999-124">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0f999-125">Notes</span><span class="sxs-lookup"><span data-stu-id="0f999-125">Remarks</span></span>  
 <span data-ttu-id="0f999-126">L'objet <xref:System.Activities.Tracking.WorkflowInstanceQuery> sert à s'abonner aux objets <xref:System.Activities.Tracking.TrackingRecord> suivants :</span><span class="sxs-lookup"><span data-stu-id="0f999-126">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="0f999-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="0f999-127">Example</span></span>  
 <span data-ttu-id="0f999-128">La configuration suivante permet de s'abonner aux enregistrements de suivi au niveau de l'instance de flux de travail pour l'état de l'instance `Started` à l'aide de cette requête.</span><span class="sxs-lookup"><span data-stu-id="0f999-128">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0f999-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f999-129">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="0f999-130">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="0f999-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="0f999-131">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="0f999-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
