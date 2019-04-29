---
title: <activityScheduledQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a8bcd6d4-b389-4daf-86bf-1ade85fec114
ms.openlocfilehash: d49c6d933a09dce5d657746358f1a5f716ab639b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790414"
---
# <a name="activityscheduledquery"></a><span data-ttu-id="e6162-101">\<activityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="e6162-101">\<activityScheduledQuery></span></span>
<span data-ttu-id="e6162-102">Représente une collection de requêtes qui permettent d'effectuer le suivi d'une activité dont l'exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="e6162-102">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="e6162-103">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements d'une activité planifiée.</span><span class="sxs-lookup"><span data-stu-id="e6162-103">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
 <span data-ttu-id="e6162-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="e6162-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="e6162-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="e6162-105">\<system.serviceModel></span></span>  
<span data-ttu-id="e6162-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="e6162-106">\<tracking></span></span>  
<span data-ttu-id="e6162-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="e6162-107">\<trackingProfile></span></span>  
<span data-ttu-id="e6162-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="e6162-108">\<workflow></span></span>  
<span data-ttu-id="e6162-109">\<activityScheduledQueries></span><span class="sxs-lookup"><span data-stu-id="e6162-109">\<activityScheduledQueries></span></span>  
<span data-ttu-id="e6162-110">\<activityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="e6162-110">\<activityScheduledQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6162-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6162-111">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e6162-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e6162-112">Attributes and Elements</span></span>  
 <span data-ttu-id="e6162-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e6162-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e6162-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="e6162-114">Attributes</span></span>  
  
|<span data-ttu-id="e6162-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="e6162-115">Attribute</span></span>|<span data-ttu-id="e6162-116">Description</span><span class="sxs-lookup"><span data-stu-id="e6162-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e6162-117">activityName</span><span class="sxs-lookup"><span data-stu-id="e6162-117">activityName</span></span>|<span data-ttu-id="e6162-118">Chaîne qui spécifie le nom de l'activité demandant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="e6162-118">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="e6162-119">childActivityName</span><span class="sxs-lookup"><span data-stu-id="e6162-119">childActivityName</span></span>|<span data-ttu-id="e6162-120">Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="e6162-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e6162-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e6162-121">Child Elements</span></span>  
 <span data-ttu-id="e6162-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e6162-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e6162-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e6162-123">Parent Elements</span></span>  
  
|<span data-ttu-id="e6162-124">Élément</span><span class="sxs-lookup"><span data-stu-id="e6162-124">Element</span></span>|<span data-ttu-id="e6162-125">Description</span><span class="sxs-lookup"><span data-stu-id="e6162-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e6162-126">\<activityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="e6162-126">\<activityScheduledQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activityscheduledquery.md)|<span data-ttu-id="e6162-127">Requête qui permet d'effectuer le suivi d'une activité dont l'exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="e6162-127">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e6162-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6162-128">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityScheduledQuery?displayProperty=nameWithType>
- [<span data-ttu-id="e6162-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="e6162-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="e6162-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="e6162-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
