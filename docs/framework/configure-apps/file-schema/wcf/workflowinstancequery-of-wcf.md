---
title: '&lt;workflowInstanceQuery&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: 35c73f9d-474e-42eb-874d-ddc04b1987f3
ms.openlocfilehash: 01867171941db82260d28b0825bdf3453e46e66c
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148173"
---
# <a name="ltworkflowinstancequerygt-of-wcf"></a><span data-ttu-id="692a7-102">&lt;workflowInstanceQuery&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="692a7-102">&lt;workflowInstanceQuery&gt; of WCF</span></span>

<span data-ttu-id="692a7-103">Représente une requête qui effectue le suivi des changements dans le cycle de vie d'une instance de flux de travail, tels que le début et la fin d'un événement.</span><span class="sxs-lookup"><span data-stu-id="692a7-103">Represents a query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>  
  
<span data-ttu-id="692a7-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="692a7-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="692a7-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="692a7-105">\<system.serviceModel></span></span>  
<span data-ttu-id="692a7-106">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="692a7-106">\<tracking></span></span>  
<span data-ttu-id="692a7-107">\<profils ></span><span class="sxs-lookup"><span data-stu-id="692a7-107">\<profiles></span></span>  
<span data-ttu-id="692a7-108">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="692a7-108">\<trackingProfile></span></span>  
<span data-ttu-id="692a7-109">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="692a7-109">\<workflow></span></span>  
<span data-ttu-id="692a7-110">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="692a7-110">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="692a7-111">\<workflowInstanceQuery ></span><span class="sxs-lookup"><span data-stu-id="692a7-111">\<workflowInstanceQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="692a7-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="692a7-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="692a7-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="692a7-113">Attributes and elements</span></span>  

<span data-ttu-id="692a7-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="692a7-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="692a7-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="692a7-115">Attributes</span></span>  

<span data-ttu-id="692a7-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="692a7-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="692a7-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="692a7-117">Child elements</span></span>  
  
|<span data-ttu-id="692a7-118">Élément</span><span class="sxs-lookup"><span data-stu-id="692a7-118">Element</span></span>|<span data-ttu-id="692a7-119">Description</span><span class="sxs-lookup"><span data-stu-id="692a7-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="692a7-120">\<États ></span><span class="sxs-lookup"><span data-stu-id="692a7-120">\<states></span></span>](states-of-wcf-workflowinstancequery.md)|<span data-ttu-id="692a7-121">Collection d’états faisant l’objet d’un abonnement dans l’instance de flux de travail suivie lors de la création des enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="692a7-121">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="692a7-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="692a7-122">Parent elements</span></span>  
  
|<span data-ttu-id="692a7-123">Élément</span><span class="sxs-lookup"><span data-stu-id="692a7-123">Element</span></span>|<span data-ttu-id="692a7-124">Description</span><span class="sxs-lookup"><span data-stu-id="692a7-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="692a7-125">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="692a7-125">\<workflowInstanceQueries></span></span>](workflowinstancequeries-of-wcf.md)|<span data-ttu-id="692a7-126">Représente une collection d’éléments de configuration qui effectuent le suivi des changements dans le cycle de vie d’une instance de flux de travail, tels que le début ou la fin d’un événement.</span><span class="sxs-lookup"><span data-stu-id="692a7-126">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="692a7-127">Notes</span><span class="sxs-lookup"><span data-stu-id="692a7-127">Remarks</span></span>  

<span data-ttu-id="692a7-128">L'objet <xref:System.Activities.Tracking.WorkflowInstanceQuery> sert à s'abonner aux objets <xref:System.Activities.Tracking.TrackingRecord> suivants :</span><span class="sxs-lookup"><span data-stu-id="692a7-128">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="692a7-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="692a7-129">Example</span></span>  

<span data-ttu-id="692a7-130">La configuration suivante permet de s'abonner aux enregistrements de suivi au niveau de l'instance de flux de travail pour l'état de l'instance `Started` à l'aide de cette requête.</span><span class="sxs-lookup"><span data-stu-id="692a7-130">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="692a7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="692a7-131">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="692a7-132">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="692a7-132">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="692a7-133">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="692a7-133">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
