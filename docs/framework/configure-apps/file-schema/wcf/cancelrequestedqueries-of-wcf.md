---
title: '&lt;cancelRequestedQueries&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: a7cc7125-9ea3-4d3f-99c0-878cdeb1258a
ms.openlocfilehash: 40fbcafd641e93be6ba21635f4f6e6428be62c12
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49373320"
---
# <a name="ltcancelrequestedqueriesgt-of-wcf"></a><span data-ttu-id="a6901-102">&lt;cancelRequestedQueries&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="a6901-102">&lt;cancelRequestedQueries&gt; of WCF</span></span>
<span data-ttu-id="a6901-103">Représente une collection de requêtes qui permettent d’effectuer le suivi des demandes d’annulation d’une activité enfant par l’activité parent.</span><span class="sxs-lookup"><span data-stu-id="a6901-103">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="a6901-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="a6901-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
<span data-ttu-id="a6901-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="a6901-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="a6901-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="a6901-106">\<system.serviceModel></span></span>  
<span data-ttu-id="a6901-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="a6901-107">\<tracking></span></span>  
<span data-ttu-id="a6901-108">\<profils > \<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="a6901-108">\<profiles> \<trackingProfile></span></span>  
<span data-ttu-id="a6901-109">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="a6901-109">\<workflow></span></span>  
<span data-ttu-id="a6901-110">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="a6901-110">\<cancelRequestedQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6901-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6901-111">Syntax</span></span>  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <cancelRequestQueries>
          <cancelRequestQuery activityName="String"
                              childActivityName="String"/>
        </cancelRequestQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>  
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a6901-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a6901-112">Attributes and elements</span></span>  

<span data-ttu-id="a6901-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a6901-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a6901-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="a6901-114">Attributes</span></span>

<span data-ttu-id="a6901-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a6901-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6901-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a6901-116">Child elements</span></span>
  
|<span data-ttu-id="a6901-117">Élément</span><span class="sxs-lookup"><span data-stu-id="a6901-117">Element</span></span>|<span data-ttu-id="a6901-118">Description</span><span class="sxs-lookup"><span data-stu-id="a6901-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a6901-119">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="a6901-119">\<cancelRequestedQuery></span></span>](cancelrequestedquery-of-wcf.md)|<span data-ttu-id="a6901-120">Requête qui permet d'effectuer le suivi des demande d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="a6901-120">A query that is used to track requests to cancel a child activity by the parent activity</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a6901-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a6901-121">Parent elements</span></span>  
  
|<span data-ttu-id="a6901-122">Élément</span><span class="sxs-lookup"><span data-stu-id="a6901-122">Element</span></span>|<span data-ttu-id="a6901-123">Description</span><span class="sxs-lookup"><span data-stu-id="a6901-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a6901-124">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="a6901-124">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="a6901-125">Élément de configuration qui contient toutes les requêtes d'un flux de travail spécifique identifié par la propriété <xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileWorkflowElement.ActivityDefinitionId>.</span><span class="sxs-lookup"><span data-stu-id="a6901-125">A configuration element that contains all queries for a specific workflow identified by the <xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileWorkflowElement.ActivityDefinitionId> property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a6901-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6901-126">See also</span></span>

- <xref:System.Activities.Tracking.CancelRequestedQuery>
- [<span data-ttu-id="a6901-127">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="a6901-127">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="a6901-128">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="a6901-128">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
