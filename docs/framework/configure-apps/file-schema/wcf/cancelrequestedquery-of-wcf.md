---
title: '&lt;cancelRequestedQuery&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: b690d870-02eb-4c56-8bc3-e5ca99d7097b
ms.openlocfilehash: 6b41721dcc0c489377c59bfccdd0b1a617f551b0
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149070"
---
# <a name="ltcancelrequestedquerygt-of-wcf"></a><span data-ttu-id="c490c-102">&lt;cancelRequestedQuery&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="c490c-102">&lt;cancelRequestedQuery&gt; of WCF</span></span>

<span data-ttu-id="c490c-103">Représente une requête qui permet d'effectuer le suivi des demande d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="c490c-103">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="c490c-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="c490c-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
<span data-ttu-id="c490c-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="c490c-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>
  
<span data-ttu-id="c490c-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="c490c-106">\<system.serviceModel></span></span>  
<span data-ttu-id="c490c-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="c490c-107">\<tracking></span></span>  
<span data-ttu-id="c490c-108">\<profils ></span><span class="sxs-lookup"><span data-stu-id="c490c-108">\<profiles></span></span>  
<span data-ttu-id="c490c-109">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="c490c-109">\<trackingProfile></span></span>  
<span data-ttu-id="c490c-110">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="c490c-110">\<workflow></span></span>  
<span data-ttu-id="c490c-111">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="c490c-111">\<cancelRequestedQueries></span></span>  
<span data-ttu-id="c490c-112">\<cancelRequestedQuery ></span><span class="sxs-lookup"><span data-stu-id="c490c-112">\<cancelRequestedQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c490c-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c490c-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c490c-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c490c-114">Attributes and elements</span></span>

<span data-ttu-id="c490c-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c490c-115">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="c490c-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="c490c-116">Attributes</span></span>  
  
|<span data-ttu-id="c490c-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="c490c-117">Attribute</span></span>|<span data-ttu-id="c490c-118">Description</span><span class="sxs-lookup"><span data-stu-id="c490c-118">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="c490c-119">Chaîne qui spécifie le nom de l'activité demandant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="c490c-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|`childActivityName`|<span data-ttu-id="c490c-120">Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="c490c-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c490c-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c490c-121">Child elements</span></span>

<span data-ttu-id="c490c-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c490c-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c490c-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c490c-123">Parent elements</span></span>
  
|<span data-ttu-id="c490c-124">Élément</span><span class="sxs-lookup"><span data-stu-id="c490c-124">Element</span></span>|<span data-ttu-id="c490c-125">Description</span><span class="sxs-lookup"><span data-stu-id="c490c-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c490c-126">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="c490c-126">\<cancelRequestedQueries></span></span>](cancelrequestedqueries-of-wcf.md)|<span data-ttu-id="c490c-127">Représente une collection de requêtes qui permettent d’effectuer le suivi des demandes d’annulation d’une activité enfant par l’activité parent.</span><span class="sxs-lookup"><span data-stu-id="c490c-127">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c490c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c490c-128">See also</span></span>  

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>
- [<span data-ttu-id="c490c-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="c490c-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="c490c-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="c490c-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
