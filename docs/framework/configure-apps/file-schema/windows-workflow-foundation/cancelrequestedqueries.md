---
title: '&lt;cancelRequestedQueries&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: eab5af7e-76fa-434d-9d36-873e995cee05
ms.openlocfilehash: 5bc2e3ffeb93bdfcd45638d6b50e218c03706f42
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520683"
---
# <a name="ltcancelrequestedqueriesgt"></a><span data-ttu-id="85547-102">&lt;cancelRequestedQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="85547-102">&lt;cancelRequestedQueries&gt;</span></span>
<span data-ttu-id="85547-103">Représente une collection de requêtes qui permettent d’effectuer le suivi des demandes d’annulation d’une activité enfant par l’activité parent.</span><span class="sxs-lookup"><span data-stu-id="85547-103">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="85547-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="85547-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="85547-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="85547-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="85547-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="85547-106">\<system.serviceModel></span></span>  
<span data-ttu-id="85547-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="85547-107">\<tracking></span></span>  
<span data-ttu-id="85547-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="85547-108">\<trackingProfile></span></span>  
<span data-ttu-id="85547-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="85547-109">\<workflow></span></span>  
<span data-ttu-id="85547-110">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="85547-110">\<cancelRequestedQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="85547-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85547-111">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <cancelRequestQueries>
        <cancelRequestQuery activityName="String" 
                            childActivityName="String"/>
      </cancelRequestQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="85547-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="85547-112">Attributes and Elements</span></span>  
 <span data-ttu-id="85547-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="85547-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="85547-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="85547-114">Attributes</span></span>  
 <span data-ttu-id="85547-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="85547-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="85547-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="85547-116">Child Elements</span></span>  
  
|<span data-ttu-id="85547-117">Élément</span><span class="sxs-lookup"><span data-stu-id="85547-117">Element</span></span>|<span data-ttu-id="85547-118">Description</span><span class="sxs-lookup"><span data-stu-id="85547-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="85547-119">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="85547-119">\<cancelRequestedQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/cancelrequestedquery.md)|<span data-ttu-id="85547-120">Requête qui permet d'effectuer le suivi des demande d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="85547-120">A query that is used to track requests to cancel a child activity by the parent activity</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="85547-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="85547-121">Parent Elements</span></span>  
  
|<span data-ttu-id="85547-122">Élément</span><span class="sxs-lookup"><span data-stu-id="85547-122">Element</span></span>|<span data-ttu-id="85547-123">Description</span><span class="sxs-lookup"><span data-stu-id="85547-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="85547-124">\<workflow></span><span class="sxs-lookup"><span data-stu-id="85547-124">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="85547-125">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le **activityDefinitionId** propriété.</span><span class="sxs-lookup"><span data-stu-id="85547-125">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="85547-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85547-126">See also</span></span>
- [<span data-ttu-id="85547-127">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="85547-127">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="85547-128">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="85547-128">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
