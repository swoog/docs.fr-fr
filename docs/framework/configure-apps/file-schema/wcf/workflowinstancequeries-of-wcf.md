---
title: '&lt;workflowInstanceQueries&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: b0852f77-16e4-4d55-8eb7-a19feb0e8fc4
ms.openlocfilehash: dfa75a7e4729244ba5887e6666c0fdfe840e9faf
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45508354"
---
# <a name="ltworkflowinstancequeriesgt-of-wcf"></a><span data-ttu-id="46e42-102">&lt;workflowInstanceQueries&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="46e42-102">&lt;workflowInstanceQueries&gt; of WCF</span></span>
<span data-ttu-id="46e42-103">Représente une collection d’éléments de configuration qui effectuent le suivi des changements dans le cycle de vie d’une instance de flux de travail, tels que le début ou la fin d’un événement.</span><span class="sxs-lookup"><span data-stu-id="46e42-103">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>  
  
 <span data-ttu-id="46e42-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="46e42-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
 <span data-ttu-id="46e42-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="46e42-105">\<system.serviceModel></span></span>  
<span data-ttu-id="46e42-106">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="46e42-106">\<tracking></span></span>  
<span data-ttu-id="46e42-107">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="46e42-107">\<trackingProfile></span></span>  
<span data-ttu-id="46e42-108">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="46e42-108">\<workflow></span></span>  
<span data-ttu-id="46e42-109">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="46e42-109">\<workflowInstanceQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46e42-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46e42-110">Syntax</span></span>  
  
```xml
<tracking>   <trackingProfile name="Name">       <workflow>          <workflowInstanceQueries>             <workflowInstanceQuery>                <states>                   <state name="Name"/>                </states>            </workflowInstanceQuery>         </workflowInstanceQueries>       </workflow>   </trackingProfile></tracking>  
```
  
## <a name="attributes-and-elements"></a><span data-ttu-id="46e42-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="46e42-111">Attributes and Elements</span></span>  
 <span data-ttu-id="46e42-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="46e42-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="46e42-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="46e42-113">Attributes</span></span>  
 <span data-ttu-id="46e42-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="46e42-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="46e42-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="46e42-115">Child Elements</span></span>  
  
|<span data-ttu-id="46e42-116">Élément</span><span class="sxs-lookup"><span data-stu-id="46e42-116">Element</span></span>|<span data-ttu-id="46e42-117">Description</span><span class="sxs-lookup"><span data-stu-id="46e42-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="46e42-118">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="46e42-118">\<workflowInstanceQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflowinstancequery.md)|<span data-ttu-id="46e42-119">Requête qui permet d'effectuer le suivi des changements dans le cycle de vie d'une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="46e42-119">A query that is used to track workflow instance life cycle changes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="46e42-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="46e42-120">Parent Elements</span></span>  
  
|<span data-ttu-id="46e42-121">Élément</span><span class="sxs-lookup"><span data-stu-id="46e42-121">Element</span></span>|<span data-ttu-id="46e42-122">Description</span><span class="sxs-lookup"><span data-stu-id="46e42-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="46e42-123">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="46e42-123">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="46e42-124">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le [activityDefinitionId](https://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx) propriété.</span><span class="sxs-lookup"><span data-stu-id="46e42-124">A configuration element that contains all queries for a specific workflow identified by the [activityDefinitionId](https://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx) property.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="46e42-125">Notes</span><span class="sxs-lookup"><span data-stu-id="46e42-125">Remarks</span></span>  
 <span data-ttu-id="46e42-126">L'objet <xref:System.Activities.Tracking.WorkflowInstanceQuery> sert à s'abonner aux objets <xref:System.Activities.Tracking.TrackingRecord> suivants :</span><span class="sxs-lookup"><span data-stu-id="46e42-126">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="46e42-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="46e42-127">Example</span></span>  
 <span data-ttu-id="46e42-128">La configuration suivante permet de s'abonner aux enregistrements de suivi au niveau de l'instance de flux de travail pour l'état de l'instance `Started` à l'aide de cette requête.</span><span class="sxs-lookup"><span data-stu-id="46e42-128">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="46e42-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46e42-129">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElementCollection?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="46e42-130">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="46e42-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="46e42-131">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="46e42-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
