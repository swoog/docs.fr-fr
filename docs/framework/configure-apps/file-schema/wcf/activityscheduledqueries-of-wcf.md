---
title: '&lt;activityScheduledQueries&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: e351329f-9676-4f11-9b19-f4bac82f36fc
ms.openlocfilehash: 35bcb0dc0c33d30eee566869579edb32f131f495
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452694"
---
# <a name="ltactivityscheduledqueriesgt-of-wcf"></a><span data-ttu-id="f81ba-102">&lt;activityScheduledQueries&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="f81ba-102">&lt;activityScheduledQueries&gt; of WCF</span></span>
<span data-ttu-id="f81ba-103">Représente une collection de requêtes qui permettent d’effectuer le suivi d’une activité dont l’exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="f81ba-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="f81ba-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements d'une activité planifiée.</span><span class="sxs-lookup"><span data-stu-id="f81ba-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
<span data-ttu-id="f81ba-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="f81ba-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="f81ba-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="f81ba-106">\<system.serviceModel></span></span>  
<span data-ttu-id="f81ba-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="f81ba-107">\<tracking></span></span>  
<span data-ttu-id="f81ba-108">\<profils ></span><span class="sxs-lookup"><span data-stu-id="f81ba-108">\<profiles></span></span>  
<span data-ttu-id="f81ba-109">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="f81ba-109">\<trackingProfile></span></span>  
<span data-ttu-id="f81ba-110">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="f81ba-110">\<workflow></span></span>  
<span data-ttu-id="f81ba-111">\<activityScheduledQueries ></span><span class="sxs-lookup"><span data-stu-id="f81ba-111">\<activityScheduledQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f81ba-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f81ba-112">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityScheduledQueries>
          <activityScheduledQuery activityName="String"   
                                  childActivityName="String"/>
        </activityScheduledQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f81ba-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f81ba-113">Attributes and elements</span></span>  

<span data-ttu-id="f81ba-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f81ba-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f81ba-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="f81ba-115">Attributes</span></span>  

<span data-ttu-id="f81ba-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f81ba-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="f81ba-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f81ba-117">Child elements</span></span>  
  
|<span data-ttu-id="f81ba-118">Élément</span><span class="sxs-lookup"><span data-stu-id="f81ba-118">Element</span></span>|<span data-ttu-id="f81ba-119">Description</span><span class="sxs-lookup"><span data-stu-id="f81ba-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f81ba-120">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="f81ba-120">\<activityScheduledQuery></span></span>](activityscheduledquery-of-wcf.md)|<span data-ttu-id="f81ba-121">Requête qui permet d'effectuer le suivi d'une activité dont l'exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="f81ba-121">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f81ba-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f81ba-122">Parent elements</span></span>  
  
|<span data-ttu-id="f81ba-123">Élément</span><span class="sxs-lookup"><span data-stu-id="f81ba-123">Element</span></span>|<span data-ttu-id="f81ba-124">Description</span><span class="sxs-lookup"><span data-stu-id="f81ba-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f81ba-125">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="f81ba-125">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="f81ba-126">Élément de configuration qui contient toutes les requêtes d'un flux de travail spécifique identifié par la propriété `activityDefinitionId`.</span><span class="sxs-lookup"><span data-stu-id="f81ba-126">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f81ba-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f81ba-127">See also</span></span>  

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElementCollection>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [<span data-ttu-id="f81ba-128">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="f81ba-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="f81ba-129">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="f81ba-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
