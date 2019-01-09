---
title: '&lt;activityScheduledQuery&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: 25f6eee1-3d98-4c39-b517-c0813f03f106
ms.openlocfilehash: fd7830bc178de0693f0632cea3b390d792408ec1
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147874"
---
# <a name="ltactivityscheduledquerygt-of-wcf"></a><span data-ttu-id="a56a1-102">&lt;activityScheduledQuery&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="a56a1-102">&lt;activityScheduledQuery&gt; of WCF</span></span>

<span data-ttu-id="a56a1-103">Représente une collection de requêtes qui permettent d’effectuer le suivi d’une activité dont l’exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="a56a1-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="a56a1-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements d'une activité planifiée.</span><span class="sxs-lookup"><span data-stu-id="a56a1-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
<span data-ttu-id="a56a1-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="a56a1-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="a56a1-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="a56a1-106">\<system.serviceModel></span></span>  
<span data-ttu-id="a56a1-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="a56a1-107">\<tracking></span></span>  
<span data-ttu-id="a56a1-108">\<profils ></span><span class="sxs-lookup"><span data-stu-id="a56a1-108">\<profiles></span></span>  
<span data-ttu-id="a56a1-109">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="a56a1-109">\<trackingProfile></span></span>  
<span data-ttu-id="a56a1-110">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="a56a1-110">\<workflow></span></span>  
<span data-ttu-id="a56a1-111">\<activityScheduledQueries ></span><span class="sxs-lookup"><span data-stu-id="a56a1-111">\<activityScheduledQueries></span></span>  
<span data-ttu-id="a56a1-112">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="a56a1-112">\<activityScheduledQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a56a1-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a56a1-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a56a1-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a56a1-114">Attributes and elements</span></span>  

<span data-ttu-id="a56a1-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a56a1-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a56a1-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="a56a1-116">Attributes</span></span>  
  
|<span data-ttu-id="a56a1-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="a56a1-117">Attribute</span></span>|<span data-ttu-id="a56a1-118">Description</span><span class="sxs-lookup"><span data-stu-id="a56a1-118">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="a56a1-119">Chaîne qui spécifie le nom de l'activité demandant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="a56a1-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|`childActivityName`|<span data-ttu-id="a56a1-120">Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="a56a1-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a56a1-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a56a1-121">Child elements</span></span>

<span data-ttu-id="a56a1-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a56a1-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a56a1-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a56a1-123">Parent elements</span></span>  
  
|<span data-ttu-id="a56a1-124">Élément</span><span class="sxs-lookup"><span data-stu-id="a56a1-124">Element</span></span>|<span data-ttu-id="a56a1-125">Description</span><span class="sxs-lookup"><span data-stu-id="a56a1-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a56a1-126">\<activityScheduledQueries></span><span class="sxs-lookup"><span data-stu-id="a56a1-126">\<activityScheduledQueries></span></span>](activityscheduledqueries-of-wcf.md)|<span data-ttu-id="a56a1-127">Une collection de requêtes qui sont utilisés pour suivre une activité planifiée pour l’exécution d’une activité parente.</span><span class="sxs-lookup"><span data-stu-id="a56a1-127">A collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a56a1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a56a1-128">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElement>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [<span data-ttu-id="a56a1-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="a56a1-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="a56a1-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="a56a1-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
