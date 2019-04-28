---
title: <activityScheduledQuery> de WCF
ms.date: 03/30/2017
ms.assetid: 25f6eee1-3d98-4c39-b517-c0813f03f106
ms.openlocfilehash: 5087d56092296f8c68b719ec0945993adeb3de0a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704712"
---
# <a name="activityscheduledquery-of-wcf"></a><span data-ttu-id="31652-102">\<activityScheduledQuery > de WCF</span><span class="sxs-lookup"><span data-stu-id="31652-102">\<activityScheduledQuery> of WCF</span></span>

<span data-ttu-id="31652-103">Représente une collection de requêtes qui permettent d'effectuer le suivi d'une activité dont l'exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="31652-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="31652-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements d'une activité planifiée.</span><span class="sxs-lookup"><span data-stu-id="31652-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
<span data-ttu-id="31652-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="31652-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="31652-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="31652-106">\<system.serviceModel></span></span>  
<span data-ttu-id="31652-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="31652-107">\<tracking></span></span>  
<span data-ttu-id="31652-108">\<profiles></span><span class="sxs-lookup"><span data-stu-id="31652-108">\<profiles></span></span>  
<span data-ttu-id="31652-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="31652-109">\<trackingProfile></span></span>  
<span data-ttu-id="31652-110">\<workflow></span><span class="sxs-lookup"><span data-stu-id="31652-110">\<workflow></span></span>  
<span data-ttu-id="31652-111">\<activityScheduledQueries></span><span class="sxs-lookup"><span data-stu-id="31652-111">\<activityScheduledQueries></span></span>  
<span data-ttu-id="31652-112">\<activityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="31652-112">\<activityScheduledQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="31652-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31652-113">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityScheduledQueries>
          <activityScheduledQuery activityName="String"
                                  childActivityName="String" />
        </activityScheduledQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="31652-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="31652-114">Attributes and elements</span></span>  

<span data-ttu-id="31652-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="31652-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="31652-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="31652-116">Attributes</span></span>  
  
|<span data-ttu-id="31652-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="31652-117">Attribute</span></span>|<span data-ttu-id="31652-118">Description</span><span class="sxs-lookup"><span data-stu-id="31652-118">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="31652-119">Chaîne qui spécifie le nom de l'activité demandant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="31652-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|`childActivityName`|<span data-ttu-id="31652-120">Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="31652-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="31652-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="31652-121">Child elements</span></span>

<span data-ttu-id="31652-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="31652-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="31652-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="31652-123">Parent elements</span></span>  
  
|<span data-ttu-id="31652-124">Élément</span><span class="sxs-lookup"><span data-stu-id="31652-124">Element</span></span>|<span data-ttu-id="31652-125">Description</span><span class="sxs-lookup"><span data-stu-id="31652-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="31652-126">\<activityScheduledQueries></span><span class="sxs-lookup"><span data-stu-id="31652-126">\<activityScheduledQueries></span></span>](activityscheduledqueries-of-wcf.md)|<span data-ttu-id="31652-127">Une collection de requêtes qui sont utilisés pour suivre une activité planifiée pour l’exécution d’une activité parente.</span><span class="sxs-lookup"><span data-stu-id="31652-127">A collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="31652-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31652-128">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElement>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [<span data-ttu-id="31652-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="31652-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="31652-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="31652-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
