---
title: '&lt;activityScheduledQuery&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: 25f6eee1-3d98-4c39-b517-c0813f03f106
ms.openlocfilehash: 9a53d72316dad0178f24e05656a4fb4531b88aec
ms.sourcegitcommit: 2eb5ca4956231c1a0efd34b6a9cab6153a5438af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49087763"
---
# <a name="ltactivityscheduledquerygt-of-wcf"></a><span data-ttu-id="363a4-102">&lt;activityScheduledQuery&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="363a4-102">&lt;activityScheduledQuery&gt; of WCF</span></span>
<span data-ttu-id="363a4-103">Représente une collection de requêtes qui permettent d’effectuer le suivi d’une activité dont l’exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="363a4-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="363a4-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements d'une activité planifiée.</span><span class="sxs-lookup"><span data-stu-id="363a4-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
 <span data-ttu-id="363a4-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="363a4-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
 <span data-ttu-id="363a4-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="363a4-106">\<system.serviceModel></span></span>  
<span data-ttu-id="363a4-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="363a4-107">\<tracking></span></span>  
<span data-ttu-id="363a4-108">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="363a4-108">\<trackingProfile></span></span>  
<span data-ttu-id="363a4-109">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="363a4-109">\<workflow></span></span>  
<span data-ttu-id="363a4-110">\<activityScheduledQueries ></span><span class="sxs-lookup"><span data-stu-id="363a4-110">\<activityScheduledQueries></span></span>  
<span data-ttu-id="363a4-111">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="363a4-111">\<activityScheduledQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="363a4-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="363a4-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="363a4-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="363a4-113">Attributes and Elements</span></span>  
 <span data-ttu-id="363a4-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="363a4-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="363a4-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="363a4-115">Attributes</span></span>  
  
|<span data-ttu-id="363a4-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="363a4-116">Attribute</span></span>|<span data-ttu-id="363a4-117">Description</span><span class="sxs-lookup"><span data-stu-id="363a4-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="363a4-118">activityName</span><span class="sxs-lookup"><span data-stu-id="363a4-118">activityName</span></span>|<span data-ttu-id="363a4-119">Chaîne qui spécifie le nom de l'activité demandant l'annulation.</span><span class="sxs-lookup"><span data-stu-id="363a4-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="363a4-120">childActivityName</span><span class="sxs-lookup"><span data-stu-id="363a4-120">childActivityName</span></span>|<span data-ttu-id="363a4-121">Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="363a4-121">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="363a4-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="363a4-122">Child Elements</span></span>  
 <span data-ttu-id="363a4-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="363a4-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="363a4-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="363a4-124">Parent Elements</span></span>  
  
|<span data-ttu-id="363a4-125">Élément</span><span class="sxs-lookup"><span data-stu-id="363a4-125">Element</span></span>|<span data-ttu-id="363a4-126">Description</span><span class="sxs-lookup"><span data-stu-id="363a4-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="363a4-127">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="363a4-127">\<activityScheduledQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activityscheduledquery.md)|<span data-ttu-id="363a4-128">Requête qui permet d'effectuer le suivi d'une activité dont l'exécution par une activité parent est planifiée.</span><span class="sxs-lookup"><span data-stu-id="363a4-128">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="363a4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="363a4-129">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElement>     
 <xref:System.Activities.Tracking.ActivityScheduledQuery>     
 [<span data-ttu-id="363a4-130">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="363a4-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="363a4-131">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="363a4-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
