---
title: '&lt;bookmarkResumptionQueries&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 8ed61a7f-4254-439c-bdd8-b474971533f7
ms.openlocfilehash: ae6a81123379ecd0e7fdc72f4e115a462f81eb90
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54555035"
---
# <a name="ltbookmarkresumptionqueriesgt"></a><span data-ttu-id="38bd9-102">&lt;bookmarkResumptionQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="38bd9-102">&lt;bookmarkResumptionQueries&gt;</span></span>
<span data-ttu-id="38bd9-103">Représente une collection de requêtes qui permettent d’effectuer le suivi de la reprise d’un signet dans une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="38bd9-103">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="38bd9-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de reprise de signet.</span><span class="sxs-lookup"><span data-stu-id="38bd9-104">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
 <span data-ttu-id="38bd9-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="38bd9-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="38bd9-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="38bd9-106">\<system.serviceModel></span></span>  
<span data-ttu-id="38bd9-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="38bd9-107">\<tracking></span></span>  
<span data-ttu-id="38bd9-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="38bd9-108">\<trackingProfile></span></span>  
<span data-ttu-id="38bd9-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="38bd9-109">\<workflow></span></span>  
<span data-ttu-id="38bd9-110">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="38bd9-110">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="38bd9-111">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="38bd9-111">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38bd9-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38bd9-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="38bd9-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="38bd9-113">Attributes and Elements</span></span>  
 <span data-ttu-id="38bd9-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="38bd9-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="38bd9-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="38bd9-115">Attributes</span></span>  
 <span data-ttu-id="38bd9-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="38bd9-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="38bd9-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="38bd9-117">Child Elements</span></span>  
  
|<span data-ttu-id="38bd9-118">Élément</span><span class="sxs-lookup"><span data-stu-id="38bd9-118">Element</span></span>|<span data-ttu-id="38bd9-119">Description</span><span class="sxs-lookup"><span data-stu-id="38bd9-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="38bd9-120">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="38bd9-120">\<bookmarkResumptionQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/bookmarkresumptionquery.md)|<span data-ttu-id="38bd9-121">Requête qui permet d'effectuer le suivi de la reprise d'un signet dans une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="38bd9-121">A query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="38bd9-122">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de reprise de signet.</span><span class="sxs-lookup"><span data-stu-id="38bd9-122">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="38bd9-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="38bd9-123">Parent Elements</span></span>  
  
|<span data-ttu-id="38bd9-124">Élément</span><span class="sxs-lookup"><span data-stu-id="38bd9-124">Element</span></span>|<span data-ttu-id="38bd9-125">Description</span><span class="sxs-lookup"><span data-stu-id="38bd9-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="38bd9-126">\<workflow></span><span class="sxs-lookup"><span data-stu-id="38bd9-126">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="38bd9-127">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le **activityDefinitionId** propriété.</span><span class="sxs-lookup"><span data-stu-id="38bd9-127">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="38bd9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38bd9-128">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="38bd9-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="38bd9-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="38bd9-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="38bd9-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
