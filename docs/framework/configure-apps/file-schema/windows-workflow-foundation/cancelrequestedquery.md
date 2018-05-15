---
title: '&lt;cancelRequestedQuery&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 8da9b1c4-338a-4f23-9830-6d257772d340
ms.openlocfilehash: 3e532ea482108c9a5cabe13a99afddca10f8341d
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltcancelrequestedquerygt"></a><span data-ttu-id="5978f-102">&lt;cancelRequestedQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="5978f-102">&lt;cancelRequestedQuery&gt;</span></span>
<span data-ttu-id="5978f-103">Représente une requête qui permet d'effectuer le suivi des demande d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="5978f-103">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="5978f-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="5978f-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="5978f-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="5978f-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="5978f-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="5978f-106">\<system.serviceModel></span></span>  
<span data-ttu-id="5978f-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="5978f-107">\<tracking></span></span>  
<span data-ttu-id="5978f-108">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="5978f-108">\<trackingProfile></span></span>  
<span data-ttu-id="5978f-109">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="5978f-109">\<workflow></span></span>  
<span data-ttu-id="5978f-110">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="5978f-110">\<cancelRequestedQueries></span></span>  
<span data-ttu-id="5978f-111">\<cancelRequestedQuery ></span><span class="sxs-lookup"><span data-stu-id="5978f-111">\<cancelRequestedQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5978f-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5978f-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5978f-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5978f-113">Attributes and Elements</span></span>  
 <span data-ttu-id="5978f-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5978f-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5978f-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="5978f-115">Attributes</span></span>  
  
|<span data-ttu-id="5978f-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="5978f-116">Attribute</span></span>|<span data-ttu-id="5978f-117">Description</span><span class="sxs-lookup"><span data-stu-id="5978f-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5978f-118">activityName</span><span class="sxs-lookup"><span data-stu-id="5978f-118">activityName</span></span>|<span data-ttu-id="5978f-119">Chaîne qui spécifie le nom de l'activité demandant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="5978f-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="5978f-120">childActivityName</span><span class="sxs-lookup"><span data-stu-id="5978f-120">childActivityName</span></span>|<span data-ttu-id="5978f-121">Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="5978f-121">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5978f-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5978f-122">Child Elements</span></span>  
 <span data-ttu-id="5978f-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5978f-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5978f-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5978f-124">Parent Elements</span></span>  
  
|<span data-ttu-id="5978f-125">Élément</span><span class="sxs-lookup"><span data-stu-id="5978f-125">Element</span></span>|<span data-ttu-id="5978f-126">Description</span><span class="sxs-lookup"><span data-stu-id="5978f-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5978f-127">\<faultPropagationQuery ></span><span class="sxs-lookup"><span data-stu-id="5978f-127">\<faultPropagationQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationquery.md)|<span data-ttu-id="5978f-128">Représente une liste d'éléments de configuration qui permettent d'effectuer le suivi des demandes d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="5978f-128">Represents a list of configuration elements that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="5978f-129">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="5978f-129">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5978f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5978f-130">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="5978f-131">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="5978f-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="5978f-132">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="5978f-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
