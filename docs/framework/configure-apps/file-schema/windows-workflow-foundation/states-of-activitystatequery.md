---
title: '&lt;states&gt; de &lt;activityStateQuery&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a7cc2018-2b79-44f1-825a-bb7ca08690a3
ms.openlocfilehash: d26687e9d0f2bee672f6b0c6c38b87fadf6e7888
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltstatesgt-of-ltactivitystatequerygt"></a><span data-ttu-id="fd0d9-102">&lt;states&gt; de &lt;activityStateQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="fd0d9-102">&lt;states&gt; of &lt;activityStateQuery&gt;</span></span>
<span data-ttu-id="fd0d9-103">Collection d’éléments de configuration qui contiennent les états de l’activité faisant l’objet d’un abonnement pour laquelle un enregistrement de suivi doit être émis.</span><span class="sxs-lookup"><span data-stu-id="fd0d9-103">A collection of configuration elements that contain the states of the subscribed activity for which a tracking record should be emitted.</span></span>  
  
 <span data-ttu-id="fd0d9-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="fd0d9-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="fd0d9-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="fd0d9-105">\<system.serviceModel></span></span>  
<span data-ttu-id="fd0d9-106">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="fd0d9-106">\<tracking></span></span>  
<span data-ttu-id="fd0d9-107">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="fd0d9-107">\<trackingProfile></span></span>  
<span data-ttu-id="fd0d9-108">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="fd0d9-108">\<workflow></span></span>  
<span data-ttu-id="fd0d9-109">\<activityStateQueries ></span><span class="sxs-lookup"><span data-stu-id="fd0d9-109">\<activityStateQueries></span></span>  
<span data-ttu-id="fd0d9-110">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="fd0d9-110">\<activityStateQuery></span></span>  
<span data-ttu-id="fd0d9-111">\<États ></span><span class="sxs-lookup"><span data-stu-id="fd0d9-111">\<states></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd0d9-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd0d9-112">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <states>
          <state name="String" />
        </states>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fd0d9-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="fd0d9-113">Attributes and Elements</span></span>  
 <span data-ttu-id="fd0d9-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="fd0d9-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fd0d9-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="fd0d9-115">Attributes</span></span>  
 <span data-ttu-id="fd0d9-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fd0d9-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="fd0d9-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fd0d9-117">Child Elements</span></span>  
  
|<span data-ttu-id="fd0d9-118">Élément</span><span class="sxs-lookup"><span data-stu-id="fd0d9-118">Element</span></span>|<span data-ttu-id="fd0d9-119">Description</span><span class="sxs-lookup"><span data-stu-id="fd0d9-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fd0d9-120">\<état ></span><span class="sxs-lookup"><span data-stu-id="fd0d9-120">\<state></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/state-of-states.md)|<span data-ttu-id="fd0d9-121">Élément de configuration qui contient les états de l'activité faisant l'objet d'un abonnement pour laquelle un enregistrement de suivi doit être émis.</span><span class="sxs-lookup"><span data-stu-id="fd0d9-121">A configuration element that contains the states of the subscribed activity for which a tracking record should be emitted.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="fd0d9-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fd0d9-122">Parent Elements</span></span>  
  
|<span data-ttu-id="fd0d9-123">Élément</span><span class="sxs-lookup"><span data-stu-id="fd0d9-123">Element</span></span>|<span data-ttu-id="fd0d9-124">Description</span><span class="sxs-lookup"><span data-stu-id="fd0d9-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fd0d9-125">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="fd0d9-125">\<activityStateQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)|<span data-ttu-id="fd0d9-126">Représente un élément de configuration qui permet d'effectuer le suivi des demandes d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="fd0d9-126">Represents a configuration element that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="fd0d9-127">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="fd0d9-127">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fd0d9-128">Notes</span><span class="sxs-lookup"><span data-stu-id="fd0d9-128">Remarks</span></span>  
 <span data-ttu-id="fd0d9-129">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="fd0d9-129">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="fd0d9-130">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="fd0d9-130">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="fd0d9-131">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail. L’exemple suivant montre une requête d’état d’activité qui extrait des variables et arguments lorsque l’activité `Closed` enregistrement de suivi est émis.</span><span class="sxs-lookup"><span data-stu-id="fd0d9-131">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="fd0d9-132">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="fd0d9-132">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
```xml  
<activityStateQuery activityName="SendEmailActivity">  
  <states>  
    <state name="Closed"/>  
  </states>  
  <variables>  
    <variable name="FromAddress"/>  
  </variables>  
  <arguments>  
    <argument name="Result"/>  
  </arguments>  
</activityStateQuery>  
```  
  
## <a name="see-also"></a><span data-ttu-id="fd0d9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd0d9-133">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElementCollection?displayProperty=nameWithType>      
 <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="fd0d9-134">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="fd0d9-134">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="fd0d9-135">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="fd0d9-135">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
