---
title: <activityScheduledQueries> de WCF
ms.date: 03/30/2017
ms.assetid: e351329f-9676-4f11-9b19-f4bac82f36fc
ms.openlocfilehash: 1c9c292080016d7a2d0014ed07be371c0e247621
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61701123"
---
# <a name="activityscheduledqueries-of-wcf"></a><span data-ttu-id="70fc0-102">\<activityScheduledQueries > de WCF</span><span class="sxs-lookup"><span data-stu-id="70fc0-102">\<activityScheduledQueries> of WCF</span></span>
<span data-ttu-id="70fc0-103">Représente une collection de requêtes qui permettent d'effectuer le suivi d'une activité dont l'exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="70fc0-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="70fc0-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements d'une activité planifiée.</span><span class="sxs-lookup"><span data-stu-id="70fc0-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
<span data-ttu-id="70fc0-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="70fc0-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="70fc0-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="70fc0-106">\<system.serviceModel></span></span>  
<span data-ttu-id="70fc0-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="70fc0-107">\<tracking></span></span>  
<span data-ttu-id="70fc0-108">\<profiles></span><span class="sxs-lookup"><span data-stu-id="70fc0-108">\<profiles></span></span>  
<span data-ttu-id="70fc0-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="70fc0-109">\<trackingProfile></span></span>  
<span data-ttu-id="70fc0-110">\<workflow></span><span class="sxs-lookup"><span data-stu-id="70fc0-110">\<workflow></span></span>  
<span data-ttu-id="70fc0-111">\<activityScheduledQueries></span><span class="sxs-lookup"><span data-stu-id="70fc0-111">\<activityScheduledQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70fc0-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70fc0-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="70fc0-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="70fc0-113">Attributes and elements</span></span>  

<span data-ttu-id="70fc0-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="70fc0-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="70fc0-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="70fc0-115">Attributes</span></span>  

<span data-ttu-id="70fc0-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="70fc0-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="70fc0-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="70fc0-117">Child elements</span></span>  
  
|<span data-ttu-id="70fc0-118">Élément</span><span class="sxs-lookup"><span data-stu-id="70fc0-118">Element</span></span>|<span data-ttu-id="70fc0-119">Description</span><span class="sxs-lookup"><span data-stu-id="70fc0-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="70fc0-120">\<activityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="70fc0-120">\<activityScheduledQuery></span></span>](activityscheduledquery-of-wcf.md)|<span data-ttu-id="70fc0-121">Requête qui permet d'effectuer le suivi d'une activité dont l'exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="70fc0-121">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="70fc0-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="70fc0-122">Parent elements</span></span>  
  
|<span data-ttu-id="70fc0-123">Élément</span><span class="sxs-lookup"><span data-stu-id="70fc0-123">Element</span></span>|<span data-ttu-id="70fc0-124">Description</span><span class="sxs-lookup"><span data-stu-id="70fc0-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="70fc0-125">\<workflow></span><span class="sxs-lookup"><span data-stu-id="70fc0-125">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="70fc0-126">Élément de configuration qui contient toutes les requêtes d'un flux de travail spécifique identifié par la propriété `activityDefinitionId`.</span><span class="sxs-lookup"><span data-stu-id="70fc0-126">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="70fc0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70fc0-127">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElementCollection>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [<span data-ttu-id="70fc0-128">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="70fc0-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="70fc0-129">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="70fc0-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
