---
title: <cancelRequestedQuery> de WCF
ms.date: 03/30/2017
ms.assetid: b690d870-02eb-4c56-8bc3-e5ca99d7097b
ms.openlocfilehash: bd6157e63761efa954744ab08ea6c66535def514
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61673349"
---
# <a name="cancelrequestedquery-of-wcf"></a><span data-ttu-id="2f696-102">\<cancelRequestedQuery > de WCF</span><span class="sxs-lookup"><span data-stu-id="2f696-102">\<cancelRequestedQuery> of WCF</span></span>

<span data-ttu-id="2f696-103">Représente une requête qui permet d'effectuer le suivi des demande d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="2f696-103">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="2f696-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="2f696-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
<span data-ttu-id="2f696-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="2f696-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>
  
<span data-ttu-id="2f696-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="2f696-106">\<system.serviceModel></span></span>  
<span data-ttu-id="2f696-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="2f696-107">\<tracking></span></span>  
<span data-ttu-id="2f696-108">\<profiles></span><span class="sxs-lookup"><span data-stu-id="2f696-108">\<profiles></span></span>  
<span data-ttu-id="2f696-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="2f696-109">\<trackingProfile></span></span>  
<span data-ttu-id="2f696-110">\<workflow></span><span class="sxs-lookup"><span data-stu-id="2f696-110">\<workflow></span></span>  
<span data-ttu-id="2f696-111">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="2f696-111">\<cancelRequestedQueries></span></span>  
<span data-ttu-id="2f696-112">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="2f696-112">\<cancelRequestedQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f696-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f696-113">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <cancelRequestedQueries>
          <cancelRequestedQuery activityName="String"
                                childActivityName="String" />
        </cancelRequestedQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2f696-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="2f696-114">Attributes and elements</span></span>

<span data-ttu-id="2f696-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="2f696-115">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="2f696-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="2f696-116">Attributes</span></span>  
  
|<span data-ttu-id="2f696-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="2f696-117">Attribute</span></span>|<span data-ttu-id="2f696-118">Description</span><span class="sxs-lookup"><span data-stu-id="2f696-118">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="2f696-119">Chaîne qui spécifie le nom de l'activité demandant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="2f696-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|`childActivityName`|<span data-ttu-id="2f696-120">Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="2f696-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2f696-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2f696-121">Child elements</span></span>

<span data-ttu-id="2f696-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2f696-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2f696-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2f696-123">Parent elements</span></span>
  
|<span data-ttu-id="2f696-124">Élément</span><span class="sxs-lookup"><span data-stu-id="2f696-124">Element</span></span>|<span data-ttu-id="2f696-125">Description</span><span class="sxs-lookup"><span data-stu-id="2f696-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2f696-126">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="2f696-126">\<cancelRequestedQueries></span></span>](cancelrequestedqueries-of-wcf.md)|<span data-ttu-id="2f696-127">Représente une collection de requêtes qui permettent d’effectuer le suivi des demandes d’annulation d’une activité enfant par l’activité parent.</span><span class="sxs-lookup"><span data-stu-id="2f696-127">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2f696-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f696-128">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>
- [<span data-ttu-id="2f696-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="2f696-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="2f696-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="2f696-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
