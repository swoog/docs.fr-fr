---
title: '&lt;workflowInstanceQueries&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: b0852f77-16e4-4d55-8eb7-a19feb0e8fc4
ms.openlocfilehash: dfa75a7e4729244ba5887e6666c0fdfe840e9faf
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45741971"
---
# <a name="ltworkflowinstancequeriesgt-of-wcf"></a><span data-ttu-id="c911a-102">&lt;workflowInstanceQueries&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="c911a-102">&lt;workflowInstanceQueries&gt; of WCF</span></span>
<span data-ttu-id="c911a-103">Représente une collection d’éléments de configuration qui effectuent le suivi des changements dans le cycle de vie d’une instance de flux de travail, tels que le début ou la fin d’un événement.</span><span class="sxs-lookup"><span data-stu-id="c911a-103">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>  
  
 <span data-ttu-id="c911a-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="c911a-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
 <span data-ttu-id="c911a-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="c911a-105">\<system.serviceModel></span></span>  
<span data-ttu-id="c911a-106">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="c911a-106">\<tracking></span></span>  
<span data-ttu-id="c911a-107">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="c911a-107">\<trackingProfile></span></span>  
<span data-ttu-id="c911a-108">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="c911a-108">\<workflow></span></span>  
<span data-ttu-id="c911a-109">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="c911a-109">\<workflowInstanceQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c911a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c911a-110">Syntax</span></span>  
  
```xml
<tracking>   <trackingProfile name="Name">       <workflow>          <workflowInstanceQueries>             <workflowInstanceQuery>                <states>                   <state name="Name"/>                </states>            </workflowInstanceQuery>         </workflowInstanceQueries>       </workflow>   </trackingProfile></tracking>  
```
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c911a-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c911a-111">Attributes and Elements</span></span>  
 <span data-ttu-id="c911a-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c911a-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c911a-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="c911a-113">Attributes</span></span>  
 <span data-ttu-id="c911a-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c911a-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="c911a-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c911a-115">Child Elements</span></span>  
  
|<span data-ttu-id="c911a-116">Élément</span><span class="sxs-lookup"><span data-stu-id="c911a-116">Element</span></span>|<span data-ttu-id="c911a-117">Description</span><span class="sxs-lookup"><span data-stu-id="c911a-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c911a-118">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="c911a-118">\<workflowInstanceQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflowinstancequery.md)|<span data-ttu-id="c911a-119">Requête qui permet d'effectuer le suivi des changements dans le cycle de vie d'une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="c911a-119">A query that is used to track workflow instance life cycle changes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c911a-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c911a-120">Parent Elements</span></span>  
  
|<span data-ttu-id="c911a-121">Élément</span><span class="sxs-lookup"><span data-stu-id="c911a-121">Element</span></span>|<span data-ttu-id="c911a-122">Description</span><span class="sxs-lookup"><span data-stu-id="c911a-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c911a-123">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="c911a-123">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="c911a-124">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le [activityDefinitionId](https://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx) propriété.</span><span class="sxs-lookup"><span data-stu-id="c911a-124">A configuration element that contains all queries for a specific workflow identified by the [activityDefinitionId](https://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx) property.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c911a-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c911a-125">Remarks</span></span>  
 <span data-ttu-id="c911a-126">L'objet <xref:System.Activities.Tracking.WorkflowInstanceQuery> sert à s'abonner aux objets <xref:System.Activities.Tracking.TrackingRecord> suivants :</span><span class="sxs-lookup"><span data-stu-id="c911a-126">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="c911a-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="c911a-127">Example</span></span>  
 <span data-ttu-id="c911a-128">La configuration suivante permet de s'abonner aux enregistrements de suivi au niveau de l'instance de flux de travail pour l'état de l'instance `Started` à l'aide de cette requête.</span><span class="sxs-lookup"><span data-stu-id="c911a-128">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="c911a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c911a-129">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElementCollection?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="c911a-130">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="c911a-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="c911a-131">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="c911a-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
