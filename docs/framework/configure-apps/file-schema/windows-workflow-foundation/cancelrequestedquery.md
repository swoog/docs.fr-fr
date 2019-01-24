---
title: '&lt;cancelRequestedQuery&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 8da9b1c4-338a-4f23-9830-6d257772d340
ms.openlocfilehash: a3d24536589288ce9585901f3d955075bc856c97
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520306"
---
# <a name="ltcancelrequestedquerygt"></a><span data-ttu-id="1679e-102">&lt;cancelRequestedQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="1679e-102">&lt;cancelRequestedQuery&gt;</span></span>
<span data-ttu-id="1679e-103">Représente une requête qui permet d'effectuer le suivi des demande d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="1679e-103">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="1679e-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="1679e-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="1679e-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="1679e-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="1679e-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="1679e-106">\<system.serviceModel></span></span>  
<span data-ttu-id="1679e-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="1679e-107">\<tracking></span></span>  
<span data-ttu-id="1679e-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="1679e-108">\<trackingProfile></span></span>  
<span data-ttu-id="1679e-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="1679e-109">\<workflow></span></span>  
<span data-ttu-id="1679e-110">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="1679e-110">\<cancelRequestedQueries></span></span>  
<span data-ttu-id="1679e-111">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="1679e-111">\<cancelRequestedQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1679e-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1679e-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1679e-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1679e-113">Attributes and Elements</span></span>  
 <span data-ttu-id="1679e-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1679e-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1679e-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="1679e-115">Attributes</span></span>  
  
|<span data-ttu-id="1679e-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="1679e-116">Attribute</span></span>|<span data-ttu-id="1679e-117">Description</span><span class="sxs-lookup"><span data-stu-id="1679e-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="1679e-118">activityName</span><span class="sxs-lookup"><span data-stu-id="1679e-118">activityName</span></span>|<span data-ttu-id="1679e-119">Chaîne qui spécifie le nom de l'activité demandant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="1679e-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="1679e-120">childActivityName</span><span class="sxs-lookup"><span data-stu-id="1679e-120">childActivityName</span></span>|<span data-ttu-id="1679e-121">Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="1679e-121">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1679e-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1679e-122">Child Elements</span></span>  
 <span data-ttu-id="1679e-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1679e-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1679e-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1679e-124">Parent Elements</span></span>  
  
|<span data-ttu-id="1679e-125">Élément</span><span class="sxs-lookup"><span data-stu-id="1679e-125">Element</span></span>|<span data-ttu-id="1679e-126">Description</span><span class="sxs-lookup"><span data-stu-id="1679e-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1679e-127">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="1679e-127">\<faultPropagationQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationquery.md)|<span data-ttu-id="1679e-128">Représente une liste d'éléments de configuration qui permettent d'effectuer le suivi des demandes d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="1679e-128">Represents a list of configuration elements that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="1679e-129">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="1679e-129">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1679e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1679e-130">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>
- [<span data-ttu-id="1679e-131">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="1679e-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="1679e-132">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="1679e-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
