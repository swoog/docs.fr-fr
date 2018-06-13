---
title: '&lt;activityScheduledQuery&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a8bcd6d4-b389-4daf-86bf-1ade85fec114
ms.openlocfilehash: 0822d0ce7dd82ff396596a0ed2431a5f2084ad8f
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32755368"
---
# <a name="ltactivityscheduledquerygt"></a><span data-ttu-id="9e3ac-102">&lt;activityScheduledQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="9e3ac-102">&lt;activityScheduledQuery&gt;</span></span>
<span data-ttu-id="9e3ac-103">Représente une collection de requêtes qui permettent d’effectuer le suivi d’une activité dont l’exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="9e3ac-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="9e3ac-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements d'une activité planifiée.</span><span class="sxs-lookup"><span data-stu-id="9e3ac-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
 <span data-ttu-id="9e3ac-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="9e3ac-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="9e3ac-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="9e3ac-106">\<system.serviceModel></span></span>  
<span data-ttu-id="9e3ac-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="9e3ac-107">\<tracking></span></span>  
<span data-ttu-id="9e3ac-108">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="9e3ac-108">\<trackingProfile></span></span>  
<span data-ttu-id="9e3ac-109">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="9e3ac-109">\<workflow></span></span>  
<span data-ttu-id="9e3ac-110">\<activityScheduledQueries ></span><span class="sxs-lookup"><span data-stu-id="9e3ac-110">\<activityScheduledQueries></span></span>  
<span data-ttu-id="9e3ac-111">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="9e3ac-111">\<activityScheduledQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9e3ac-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e3ac-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9e3ac-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9e3ac-113">Attributes and Elements</span></span>  
 <span data-ttu-id="9e3ac-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9e3ac-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9e3ac-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="9e3ac-115">Attributes</span></span>  
  
|<span data-ttu-id="9e3ac-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="9e3ac-116">Attribute</span></span>|<span data-ttu-id="9e3ac-117">Description</span><span class="sxs-lookup"><span data-stu-id="9e3ac-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9e3ac-118">activityName</span><span class="sxs-lookup"><span data-stu-id="9e3ac-118">activityName</span></span>|<span data-ttu-id="9e3ac-119">Chaîne qui spécifie le nom de l'activité demandant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="9e3ac-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="9e3ac-120">childActivityName</span><span class="sxs-lookup"><span data-stu-id="9e3ac-120">childActivityName</span></span>|<span data-ttu-id="9e3ac-121">Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="9e3ac-121">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9e3ac-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9e3ac-122">Child Elements</span></span>  
 <span data-ttu-id="9e3ac-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9e3ac-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9e3ac-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9e3ac-124">Parent Elements</span></span>  
  
|<span data-ttu-id="9e3ac-125">Élément</span><span class="sxs-lookup"><span data-stu-id="9e3ac-125">Element</span></span>|<span data-ttu-id="9e3ac-126">Description</span><span class="sxs-lookup"><span data-stu-id="9e3ac-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9e3ac-127">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="9e3ac-127">\<activityScheduledQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activityscheduledquery.md)|<span data-ttu-id="9e3ac-128">Requête qui permet d'effectuer le suivi d'une activité dont l'exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="9e3ac-128">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9e3ac-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e3ac-129">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElement?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.ActivityScheduledQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="9e3ac-130">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="9e3ac-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="9e3ac-131">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="9e3ac-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
