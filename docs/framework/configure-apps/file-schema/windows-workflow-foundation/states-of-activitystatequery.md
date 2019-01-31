---
title: <states> de <activityStateQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a7cc2018-2b79-44f1-825a-bb7ca08690a3
ms.openlocfilehash: 97664518f7c7c0078cef1c81035724a02c9857c0
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55257731"
---
# <a name="states-of-activitystatequery"></a><span data-ttu-id="08635-102">\<États > de \<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="08635-102">\<states> of \<activityStateQuery></span></span>
<span data-ttu-id="08635-103">Collection d’éléments de configuration qui contiennent les états de l’activité faisant l’objet d’un abonnement pour laquelle un enregistrement de suivi doit être émis.</span><span class="sxs-lookup"><span data-stu-id="08635-103">A collection of configuration elements that contain the states of the subscribed activity for which a tracking record should be emitted.</span></span>  
  
 <span data-ttu-id="08635-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="08635-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="08635-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="08635-105">\<system.serviceModel></span></span>  
<span data-ttu-id="08635-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="08635-106">\<tracking></span></span>  
<span data-ttu-id="08635-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="08635-107">\<trackingProfile></span></span>  
<span data-ttu-id="08635-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="08635-108">\<workflow></span></span>  
<span data-ttu-id="08635-109">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="08635-109">\<activityStateQueries></span></span>  
<span data-ttu-id="08635-110">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="08635-110">\<activityStateQuery></span></span>  
<span data-ttu-id="08635-111">\<states></span><span class="sxs-lookup"><span data-stu-id="08635-111">\<states></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08635-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08635-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="08635-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="08635-113">Attributes and Elements</span></span>  
 <span data-ttu-id="08635-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="08635-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="08635-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="08635-115">Attributes</span></span>  
 <span data-ttu-id="08635-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="08635-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="08635-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="08635-117">Child Elements</span></span>  
  
|<span data-ttu-id="08635-118">Élément</span><span class="sxs-lookup"><span data-stu-id="08635-118">Element</span></span>|<span data-ttu-id="08635-119">Description</span><span class="sxs-lookup"><span data-stu-id="08635-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="08635-120">\<state></span><span class="sxs-lookup"><span data-stu-id="08635-120">\<state></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/state-of-states.md)|<span data-ttu-id="08635-121">Élément de configuration qui contient les états de l'activité faisant l'objet d'un abonnement pour laquelle un enregistrement de suivi doit être émis.</span><span class="sxs-lookup"><span data-stu-id="08635-121">A configuration element that contains the states of the subscribed activity for which a tracking record should be emitted.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="08635-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="08635-122">Parent Elements</span></span>  
  
|<span data-ttu-id="08635-123">Élément</span><span class="sxs-lookup"><span data-stu-id="08635-123">Element</span></span>|<span data-ttu-id="08635-124">Description</span><span class="sxs-lookup"><span data-stu-id="08635-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="08635-125">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="08635-125">\<activityStateQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)|<span data-ttu-id="08635-126">Représente un élément de configuration qui permet d'effectuer le suivi des demandes d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="08635-126">Represents a configuration element that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="08635-127">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="08635-127">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="08635-128">Notes</span><span class="sxs-lookup"><span data-stu-id="08635-128">Remarks</span></span>  
 <span data-ttu-id="08635-129">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="08635-129">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="08635-130">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="08635-130">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="08635-131">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="08635-131">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="08635-132">L’exemple suivant illustre une requête d’état d’activité qui extrait des variables et arguments lorsque l’enregistrement de suivi `Closed` de l’activité est émis.</span><span class="sxs-lookup"><span data-stu-id="08635-132">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="08635-133">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent, êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="08635-133">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="08635-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08635-134">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="08635-135">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="08635-135">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="08635-136">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="08635-136">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
