---
title: <cancelRequestedQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 8da9b1c4-338a-4f23-9830-6d257772d340
ms.openlocfilehash: 049ca79355f13fd4ffacedbb7501d760361f0a81
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55282020"
---
# <a name="cancelrequestedquery"></a><span data-ttu-id="cf385-101">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="cf385-101">\<cancelRequestedQuery></span></span>
<span data-ttu-id="cf385-102">Représente une requête qui permet d'effectuer le suivi des demande d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="cf385-102">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="cf385-103">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="cf385-103">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="cf385-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="cf385-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="cf385-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="cf385-105">\<system.serviceModel></span></span>  
<span data-ttu-id="cf385-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="cf385-106">\<tracking></span></span>  
<span data-ttu-id="cf385-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="cf385-107">\<trackingProfile></span></span>  
<span data-ttu-id="cf385-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="cf385-108">\<workflow></span></span>  
<span data-ttu-id="cf385-109">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="cf385-109">\<cancelRequestedQueries></span></span>  
<span data-ttu-id="cf385-110">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="cf385-110">\<cancelRequestedQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cf385-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf385-111">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cf385-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="cf385-112">Attributes and Elements</span></span>  
 <span data-ttu-id="cf385-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="cf385-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cf385-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="cf385-114">Attributes</span></span>  
  
|<span data-ttu-id="cf385-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="cf385-115">Attribute</span></span>|<span data-ttu-id="cf385-116">Description</span><span class="sxs-lookup"><span data-stu-id="cf385-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="cf385-117">activityName</span><span class="sxs-lookup"><span data-stu-id="cf385-117">activityName</span></span>|<span data-ttu-id="cf385-118">Chaîne qui spécifie le nom de l'activité demandant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="cf385-118">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="cf385-119">childActivityName</span><span class="sxs-lookup"><span data-stu-id="cf385-119">childActivityName</span></span>|<span data-ttu-id="cf385-120">Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="cf385-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cf385-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cf385-121">Child Elements</span></span>  
 <span data-ttu-id="cf385-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cf385-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="cf385-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="cf385-123">Parent Elements</span></span>  
  
|<span data-ttu-id="cf385-124">Élément</span><span class="sxs-lookup"><span data-stu-id="cf385-124">Element</span></span>|<span data-ttu-id="cf385-125">Description</span><span class="sxs-lookup"><span data-stu-id="cf385-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cf385-126">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="cf385-126">\<faultPropagationQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationquery.md)|<span data-ttu-id="cf385-127">Représente une liste d'éléments de configuration qui permettent d'effectuer le suivi des demandes d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="cf385-127">Represents a list of configuration elements that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="cf385-128">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="cf385-128">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="cf385-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf385-129">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>
- [<span data-ttu-id="cf385-130">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="cf385-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="cf385-131">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="cf385-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
