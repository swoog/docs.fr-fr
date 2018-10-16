---
title: '&lt;cancelRequestedQuery&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: b690d870-02eb-4c56-8bc3-e5ca99d7097b
ms.openlocfilehash: 3943d604b586eec37a1d153f10ac049fc9bd5747
ms.sourcegitcommit: fd8d4587cc26e53f0e27e230d6e27d828ef4306b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49347565"
---
# <a name="ltcancelrequestedquerygt-of-wcf"></a><span data-ttu-id="52fa2-102">&lt;cancelRequestedQuery&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="52fa2-102">&lt;cancelRequestedQuery&gt; of WCF</span></span>

<span data-ttu-id="52fa2-103">Représente une requête qui permet d'effectuer le suivi des demande d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="52fa2-103">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="52fa2-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="52fa2-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
<span data-ttu-id="52fa2-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="52fa2-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>
  
<span data-ttu-id="52fa2-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="52fa2-106">\<system.serviceModel></span></span>  
<span data-ttu-id="52fa2-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="52fa2-107">\<tracking></span></span>  
<span data-ttu-id="52fa2-108">\<profils ></span><span class="sxs-lookup"><span data-stu-id="52fa2-108">\<profiles></span></span>  
<span data-ttu-id="52fa2-109">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="52fa2-109">\<trackingProfile></span></span>  
<span data-ttu-id="52fa2-110">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="52fa2-110">\<workflow></span></span>  
<span data-ttu-id="52fa2-111">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="52fa2-111">\<cancelRequestedQueries></span></span>  
<span data-ttu-id="52fa2-112">\<cancelRequestedQuery ></span><span class="sxs-lookup"><span data-stu-id="52fa2-112">\<cancelRequestedQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="52fa2-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52fa2-113">Syntax</span></span>  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <cancelRequestedQueries>
          <cancelRequestedQuery activityName="String"
                              childActivityName="String"/>
        </cancelRequestedQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>  
```

## <a name="attributes-and-elements"></a><span data-ttu-id="52fa2-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="52fa2-114">Attributes and elements</span></span>

<span data-ttu-id="52fa2-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="52fa2-115">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="52fa2-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="52fa2-116">Attributes</span></span>  
  
|<span data-ttu-id="52fa2-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="52fa2-117">Attribute</span></span>|<span data-ttu-id="52fa2-118">Description</span><span class="sxs-lookup"><span data-stu-id="52fa2-118">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="52fa2-119">Chaîne qui spécifie le nom de l'activité demandant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="52fa2-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|`childActivityName`|<span data-ttu-id="52fa2-120">Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="52fa2-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="52fa2-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="52fa2-121">Child elements</span></span>

<span data-ttu-id="52fa2-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="52fa2-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="52fa2-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="52fa2-123">Parent elements</span></span>
  
|<span data-ttu-id="52fa2-124">Élément</span><span class="sxs-lookup"><span data-stu-id="52fa2-124">Element</span></span>|<span data-ttu-id="52fa2-125">Description</span><span class="sxs-lookup"><span data-stu-id="52fa2-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="52fa2-126">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="52fa2-126">\<cancelRequestedQueries></span></span>](cancelrequestedqueries-of-wcf.md)|<span data-ttu-id="52fa2-127">Représente une collection de requêtes qui permettent d’effectuer le suivi des demandes d’annulation d’une activité enfant par l’activité parent.</span><span class="sxs-lookup"><span data-stu-id="52fa2-127">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="52fa2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52fa2-128">See also</span></span>  

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>
- [<span data-ttu-id="52fa2-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="52fa2-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="52fa2-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="52fa2-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
