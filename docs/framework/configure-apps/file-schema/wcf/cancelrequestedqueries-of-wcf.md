---
title: '&lt;cancelRequestedQueries&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: a7cc7125-9ea3-4d3f-99c0-878cdeb1258a
ms.openlocfilehash: 24970d0fa810db13423fa4c0fc37a4531feeb550
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32746816"
---
# <a name="ltcancelrequestedqueriesgt-of-wcf"></a><span data-ttu-id="d836b-102">&lt;cancelRequestedQueries&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="d836b-102">&lt;cancelRequestedQueries&gt; of WCF</span></span>
<span data-ttu-id="d836b-103">Représente une collection de requêtes qui permettent d’effectuer le suivi des demandes d’annulation d’une activité enfant par l’activité parent.</span><span class="sxs-lookup"><span data-stu-id="d836b-103">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="d836b-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="d836b-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="d836b-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="d836b-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
 <span data-ttu-id="d836b-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="d836b-106">\<system.serviceModel></span></span>  
<span data-ttu-id="d836b-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="d836b-107">\<tracking></span></span>  
<span data-ttu-id="d836b-108">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="d836b-108">\<trackingProfile></span></span>  
<span data-ttu-id="d836b-109">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="d836b-109">\<workflow></span></span>  
<span data-ttu-id="d836b-110">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="d836b-110">\<cancelRequestedQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d836b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d836b-111">Syntax</span></span>  
  
```xml
<tracking>   <trackingProfile name="Name">       <workflow>          <cancelRequestQueries>             <cancelRequestQuery activityName="String"                 childActivityName="String"/>          </cancelRequestQueries>       </workflow>   </trackingProfile></tracking>  
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d836b-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d836b-112">Attributes and Elements</span></span>  
 <span data-ttu-id="d836b-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d836b-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d836b-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="d836b-114">Attributes</span></span>  
 <span data-ttu-id="d836b-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d836b-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d836b-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d836b-116">Child Elements</span></span>  
  
|<span data-ttu-id="d836b-117">Élément</span><span class="sxs-lookup"><span data-stu-id="d836b-117">Element</span></span>|<span data-ttu-id="d836b-118">Description</span><span class="sxs-lookup"><span data-stu-id="d836b-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d836b-119">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="d836b-119">\<cancelRequestedQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/cancelrequestedquery.md)|<span data-ttu-id="d836b-120">Requête qui permet d'effectuer le suivi des demande d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="d836b-120">A query that is used to track requests to cancel a child activity by the parent activity</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d836b-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d836b-121">Parent Elements</span></span>  
  
|<span data-ttu-id="d836b-122">Élément</span><span class="sxs-lookup"><span data-stu-id="d836b-122">Element</span></span>|<span data-ttu-id="d836b-123">Description</span><span class="sxs-lookup"><span data-stu-id="d836b-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d836b-124">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="d836b-124">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="d836b-125">Élément de configuration qui contient toutes les requêtes d'un flux de travail spécifique identifié par la propriété `a HYPERLINK "http://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx" ctivityDefinitionId`.</span><span class="sxs-lookup"><span data-stu-id="d836b-125">A configuration element that contains all queries for a specific workflow identified by the `a HYPERLINK "http://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx" ctivityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d836b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d836b-126">See Also</span></span>  
 <xref:System.Activities.Tracking.CancelRequestedQuery>  
 [<span data-ttu-id="d836b-127">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="d836b-127">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="d836b-128">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="d836b-128">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
