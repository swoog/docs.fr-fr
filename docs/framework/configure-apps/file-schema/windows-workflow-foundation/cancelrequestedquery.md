---
title: <cancelRequestedQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 8da9b1c4-338a-4f23-9830-6d257772d340
ms.openlocfilehash: 5f2e46d5e4cdd64c37219476790b9ff92c606b6b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59215311"
---
# <a name="cancelrequestedquery"></a><span data-ttu-id="bd373-101">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="bd373-101">\<cancelRequestedQuery></span></span>
<span data-ttu-id="bd373-102">Représente une requête qui permet d'effectuer le suivi des demande d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="bd373-102">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="bd373-103">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="bd373-103">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="bd373-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="bd373-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="bd373-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="bd373-105">\<system.serviceModel></span></span>  
<span data-ttu-id="bd373-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="bd373-106">\<tracking></span></span>  
<span data-ttu-id="bd373-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="bd373-107">\<trackingProfile></span></span>  
<span data-ttu-id="bd373-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="bd373-108">\<workflow></span></span>  
<span data-ttu-id="bd373-109">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="bd373-109">\<cancelRequestedQueries></span></span>  
<span data-ttu-id="bd373-110">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="bd373-110">\<cancelRequestedQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd373-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd373-111">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bd373-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="bd373-112">Attributes and Elements</span></span>  
 <span data-ttu-id="bd373-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="bd373-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bd373-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="bd373-114">Attributes</span></span>  
  
|<span data-ttu-id="bd373-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="bd373-115">Attribute</span></span>|<span data-ttu-id="bd373-116">Description</span><span class="sxs-lookup"><span data-stu-id="bd373-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="bd373-117">activityName</span><span class="sxs-lookup"><span data-stu-id="bd373-117">activityName</span></span>|<span data-ttu-id="bd373-118">Chaîne qui spécifie le nom de l'activité demandant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="bd373-118">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="bd373-119">childActivityName</span><span class="sxs-lookup"><span data-stu-id="bd373-119">childActivityName</span></span>|<span data-ttu-id="bd373-120">Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="bd373-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bd373-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bd373-121">Child Elements</span></span>  
 <span data-ttu-id="bd373-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bd373-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="bd373-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bd373-123">Parent Elements</span></span>  
  
|<span data-ttu-id="bd373-124">Élément</span><span class="sxs-lookup"><span data-stu-id="bd373-124">Element</span></span>|<span data-ttu-id="bd373-125">Description</span><span class="sxs-lookup"><span data-stu-id="bd373-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bd373-126">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="bd373-126">\<faultPropagationQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationquery.md)|<span data-ttu-id="bd373-127">Représente une liste d'éléments de configuration qui permettent d'effectuer le suivi des demandes d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="bd373-127">Represents a list of configuration elements that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="bd373-128">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="bd373-128">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="bd373-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd373-129">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>
- [<span data-ttu-id="bd373-130">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="bd373-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="bd373-131">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="bd373-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
