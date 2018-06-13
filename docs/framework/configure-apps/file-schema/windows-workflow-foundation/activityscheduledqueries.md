---
title: '&lt;activityScheduledQueries&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: ca6e82f1-54f2-48d6-899c-9873065b5547
ms.openlocfilehash: 6192fea9a520a3f453593e5efac964a5d32a492f
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32756291"
---
# <a name="ltactivityscheduledqueriesgt"></a><span data-ttu-id="9947b-102">&lt;activityScheduledQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="9947b-102">&lt;activityScheduledQueries&gt;</span></span>
<span data-ttu-id="9947b-103">Représente une collection de requêtes qui permettent d’effectuer le suivi d’une activité dont l’exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="9947b-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="9947b-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements d'une activité planifiée.</span><span class="sxs-lookup"><span data-stu-id="9947b-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
 <span data-ttu-id="9947b-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="9947b-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="9947b-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="9947b-106">\<system.serviceModel></span></span>  
<span data-ttu-id="9947b-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="9947b-107">\<tracking></span></span>  
<span data-ttu-id="9947b-108">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="9947b-108">\<trackingProfile></span></span>  
<span data-ttu-id="9947b-109">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="9947b-109">\<workflow></span></span>  
<span data-ttu-id="9947b-110">\<activityScheduledQueries ></span><span class="sxs-lookup"><span data-stu-id="9947b-110">\<activityScheduledQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9947b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9947b-111">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityScheduledQueries>
        <activityScheduledQuery activityName="String" 
                                childActivityName="String" />
      </activityScheduledQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9947b-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9947b-112">Attributes and Elements</span></span>  
 <span data-ttu-id="9947b-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9947b-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9947b-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="9947b-114">Attributes</span></span>  
 <span data-ttu-id="9947b-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9947b-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9947b-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9947b-116">Child Elements</span></span>  
  
|<span data-ttu-id="9947b-117">Élément</span><span class="sxs-lookup"><span data-stu-id="9947b-117">Element</span></span>|<span data-ttu-id="9947b-118">Description</span><span class="sxs-lookup"><span data-stu-id="9947b-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9947b-119">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="9947b-119">\<activityScheduledQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activityscheduledquery.md)|<span data-ttu-id="9947b-120">Requête qui permet d'effectuer le suivi d'une activité dont l'exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="9947b-120">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9947b-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9947b-121">Parent Elements</span></span>  
  
|<span data-ttu-id="9947b-122">Élément</span><span class="sxs-lookup"><span data-stu-id="9947b-122">Element</span></span>|<span data-ttu-id="9947b-123">Description</span><span class="sxs-lookup"><span data-stu-id="9947b-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9947b-124">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="9947b-124">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="9947b-125">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le **activityDefinitionId** propriété.</span><span class="sxs-lookup"><span data-stu-id="9947b-125">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9947b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9947b-126">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElementCollection?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.ActivityScheduledQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="9947b-127">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="9947b-127">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="9947b-128">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="9947b-128">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
