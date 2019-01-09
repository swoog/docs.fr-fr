---
title: '&lt;activityScheduledQueries&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: e351329f-9676-4f11-9b19-f4bac82f36fc
ms.openlocfilehash: d6bc2360ccdeebe291de495e6ee5c7e22f26590a
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145573"
---
# <a name="ltactivityscheduledqueriesgt-of-wcf"></a><span data-ttu-id="8a99c-102">&lt;activityScheduledQueries&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="8a99c-102">&lt;activityScheduledQueries&gt; of WCF</span></span>
<span data-ttu-id="8a99c-103">Représente une collection de requêtes qui permettent d’effectuer le suivi d’une activité dont l’exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="8a99c-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="8a99c-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements d'une activité planifiée.</span><span class="sxs-lookup"><span data-stu-id="8a99c-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
<span data-ttu-id="8a99c-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="8a99c-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="8a99c-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="8a99c-106">\<system.serviceModel></span></span>  
<span data-ttu-id="8a99c-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="8a99c-107">\<tracking></span></span>  
<span data-ttu-id="8a99c-108">\<profils ></span><span class="sxs-lookup"><span data-stu-id="8a99c-108">\<profiles></span></span>  
<span data-ttu-id="8a99c-109">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="8a99c-109">\<trackingProfile></span></span>  
<span data-ttu-id="8a99c-110">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="8a99c-110">\<workflow></span></span>  
<span data-ttu-id="8a99c-111">\<activityScheduledQueries ></span><span class="sxs-lookup"><span data-stu-id="8a99c-111">\<activityScheduledQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a99c-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a99c-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8a99c-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="8a99c-113">Attributes and elements</span></span>  

<span data-ttu-id="8a99c-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="8a99c-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8a99c-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="8a99c-115">Attributes</span></span>  

<span data-ttu-id="8a99c-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8a99c-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="8a99c-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8a99c-117">Child elements</span></span>  
  
|<span data-ttu-id="8a99c-118">Élément</span><span class="sxs-lookup"><span data-stu-id="8a99c-118">Element</span></span>|<span data-ttu-id="8a99c-119">Description</span><span class="sxs-lookup"><span data-stu-id="8a99c-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8a99c-120">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="8a99c-120">\<activityScheduledQuery></span></span>](activityscheduledquery-of-wcf.md)|<span data-ttu-id="8a99c-121">Requête qui permet d'effectuer le suivi d'une activité dont l'exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="8a99c-121">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="8a99c-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8a99c-122">Parent elements</span></span>  
  
|<span data-ttu-id="8a99c-123">Élément</span><span class="sxs-lookup"><span data-stu-id="8a99c-123">Element</span></span>|<span data-ttu-id="8a99c-124">Description</span><span class="sxs-lookup"><span data-stu-id="8a99c-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8a99c-125">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="8a99c-125">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="8a99c-126">Élément de configuration qui contient toutes les requêtes d'un flux de travail spécifique identifié par la propriété `activityDefinitionId`.</span><span class="sxs-lookup"><span data-stu-id="8a99c-126">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8a99c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a99c-127">See also</span></span>  

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElementCollection>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [<span data-ttu-id="8a99c-128">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="8a99c-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="8a99c-129">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="8a99c-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
