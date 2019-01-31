---
title: <bookmarkResumptionQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 8ed61a7f-4254-439c-bdd8-b474971533f7
ms.openlocfilehash: 4277df5b4c36fa2f3571ba8441a7eb8aaf6d106a
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261544"
---
# <a name="bookmarkresumptionqueries"></a><span data-ttu-id="96109-101">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="96109-101">\<bookmarkResumptionQueries></span></span>
<span data-ttu-id="96109-102">Représente une collection de requêtes qui permettent d’effectuer le suivi de la reprise d’un signet dans une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="96109-102">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="96109-103">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de reprise de signet.</span><span class="sxs-lookup"><span data-stu-id="96109-103">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
 <span data-ttu-id="96109-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="96109-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="96109-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="96109-105">\<system.serviceModel></span></span>  
<span data-ttu-id="96109-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="96109-106">\<tracking></span></span>  
<span data-ttu-id="96109-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="96109-107">\<trackingProfile></span></span>  
<span data-ttu-id="96109-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="96109-108">\<workflow></span></span>  
<span data-ttu-id="96109-109">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="96109-109">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="96109-110">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="96109-110">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96109-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96109-111">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <bookmarkResumptionQueries>
        <bookmarkResumptionQuery name="String" />
      </bookmarkResumptionQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="96109-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="96109-112">Attributes and Elements</span></span>  
 <span data-ttu-id="96109-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="96109-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="96109-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="96109-114">Attributes</span></span>  
 <span data-ttu-id="96109-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="96109-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="96109-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="96109-116">Child Elements</span></span>  
  
|<span data-ttu-id="96109-117">Élément</span><span class="sxs-lookup"><span data-stu-id="96109-117">Element</span></span>|<span data-ttu-id="96109-118">Description</span><span class="sxs-lookup"><span data-stu-id="96109-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="96109-119">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="96109-119">\<bookmarkResumptionQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/bookmarkresumptionquery.md)|<span data-ttu-id="96109-120">Requête qui permet d'effectuer le suivi de la reprise d'un signet dans une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="96109-120">A query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="96109-121">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de reprise de signet.</span><span class="sxs-lookup"><span data-stu-id="96109-121">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="96109-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="96109-122">Parent Elements</span></span>  
  
|<span data-ttu-id="96109-123">Élément</span><span class="sxs-lookup"><span data-stu-id="96109-123">Element</span></span>|<span data-ttu-id="96109-124">Description</span><span class="sxs-lookup"><span data-stu-id="96109-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="96109-125">\<workflow></span><span class="sxs-lookup"><span data-stu-id="96109-125">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="96109-126">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le **activityDefinitionId** propriété.</span><span class="sxs-lookup"><span data-stu-id="96109-126">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="96109-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96109-127">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="96109-128">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="96109-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="96109-129">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="96109-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
