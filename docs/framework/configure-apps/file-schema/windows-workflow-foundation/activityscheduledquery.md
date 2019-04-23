---
title: <activityScheduledQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a8bcd6d4-b389-4daf-86bf-1ade85fec114
ms.openlocfilehash: d49c6d933a09dce5d657746358f1a5f716ab639b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59143362"
---
# <a name="activityscheduledquery"></a><span data-ttu-id="93031-101">\<activityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="93031-101">\<activityScheduledQuery></span></span>
<span data-ttu-id="93031-102">Représente une collection de requêtes qui permettent d'effectuer le suivi d'une activité dont l'exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="93031-102">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="93031-103">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements d'une activité planifiée.</span><span class="sxs-lookup"><span data-stu-id="93031-103">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
 <span data-ttu-id="93031-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="93031-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="93031-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="93031-105">\<system.serviceModel></span></span>  
<span data-ttu-id="93031-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="93031-106">\<tracking></span></span>  
<span data-ttu-id="93031-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="93031-107">\<trackingProfile></span></span>  
<span data-ttu-id="93031-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="93031-108">\<workflow></span></span>  
<span data-ttu-id="93031-109">\<activityScheduledQueries></span><span class="sxs-lookup"><span data-stu-id="93031-109">\<activityScheduledQueries></span></span>  
<span data-ttu-id="93031-110">\<activityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="93031-110">\<activityScheduledQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93031-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93031-111">Syntax</span></span>  
  
```xml 
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityScheduledQueries>
        <activityScheduledQuery activityName="String" 
                                childActivityName="String"/>
      </activityScheduledQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="93031-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="93031-112">Attributes and Elements</span></span>  
 <span data-ttu-id="93031-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="93031-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="93031-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="93031-114">Attributes</span></span>  
  
|<span data-ttu-id="93031-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="93031-115">Attribute</span></span>|<span data-ttu-id="93031-116">Description</span><span class="sxs-lookup"><span data-stu-id="93031-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="93031-117">activityName</span><span class="sxs-lookup"><span data-stu-id="93031-117">activityName</span></span>|<span data-ttu-id="93031-118">Chaîne qui spécifie le nom de l'activité demandant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="93031-118">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="93031-119">childActivityName</span><span class="sxs-lookup"><span data-stu-id="93031-119">childActivityName</span></span>|<span data-ttu-id="93031-120">Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="93031-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="93031-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="93031-121">Child Elements</span></span>  
 <span data-ttu-id="93031-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="93031-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="93031-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="93031-123">Parent Elements</span></span>  
  
|<span data-ttu-id="93031-124">Élément</span><span class="sxs-lookup"><span data-stu-id="93031-124">Element</span></span>|<span data-ttu-id="93031-125">Description</span><span class="sxs-lookup"><span data-stu-id="93031-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="93031-126">\<activityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="93031-126">\<activityScheduledQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activityscheduledquery.md)|<span data-ttu-id="93031-127">Requête qui permet d'effectuer le suivi d'une activité dont l'exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="93031-127">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="93031-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93031-128">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityScheduledQuery?displayProperty=nameWithType>
- [<span data-ttu-id="93031-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="93031-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="93031-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="93031-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
