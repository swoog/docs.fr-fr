---
title: <state> de <states>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: ab483c7f-a091-4933-ba6b-708d96846d38
ms.openlocfilehash: 657814eb120878cdc71cd7603d0499ff65ca50e8
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57367087"
---
# <a name="state-of-states"></a><span data-ttu-id="cb1ea-102">\<état > de \<États ></span><span class="sxs-lookup"><span data-stu-id="cb1ea-102">\<state> of \<states></span></span>
<span data-ttu-id="cb1ea-103">Élément de configuration qui contient l'état de l'activité faisant l'objet d'un abonnement pour laquelle un enregistrement de suivi doit être émis.</span><span class="sxs-lookup"><span data-stu-id="cb1ea-103">A configuration element that contains the state of the subscribed activity for which a tracking record should be emitted.</span></span>  
  
 <span data-ttu-id="cb1ea-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="cb1ea-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="cb1ea-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="cb1ea-105">\<system.serviceModel></span></span>  
<span data-ttu-id="cb1ea-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="cb1ea-106">\<tracking></span></span>  
<span data-ttu-id="cb1ea-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="cb1ea-107">\<trackingProfile></span></span>  
<span data-ttu-id="cb1ea-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="cb1ea-108">\<workflow></span></span>  
<span data-ttu-id="cb1ea-109">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="cb1ea-109">\<activityStateQueries></span></span>  
<span data-ttu-id="cb1ea-110">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="cb1ea-110">\<activityStateQuery></span></span>  
<span data-ttu-id="cb1ea-111">\<states></span><span class="sxs-lookup"><span data-stu-id="cb1ea-111">\<states></span></span>  
<span data-ttu-id="cb1ea-112">\<state></span><span class="sxs-lookup"><span data-stu-id="cb1ea-112">\<state></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cb1ea-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb1ea-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cb1ea-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="cb1ea-114">Attributes and Elements</span></span>  
 <span data-ttu-id="cb1ea-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="cb1ea-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cb1ea-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="cb1ea-116">Attributes</span></span>  
  
|<span data-ttu-id="cb1ea-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="cb1ea-117">Attribute</span></span>|<span data-ttu-id="cb1ea-118">Description</span><span class="sxs-lookup"><span data-stu-id="cb1ea-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="cb1ea-119">name</span><span class="sxs-lookup"><span data-stu-id="cb1ea-119">name</span></span>|<span data-ttu-id="cb1ea-120">Chaîne qui spécifie l'état de l'activité faisant l'objet d'un abonnement pour laquelle un enregistrement de suivi doit être émis.</span><span class="sxs-lookup"><span data-stu-id="cb1ea-120">A string that specifies the state of the subscribed activity for which a tracking record should be emitted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cb1ea-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cb1ea-121">Child Elements</span></span>  
 <span data-ttu-id="cb1ea-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cb1ea-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="cb1ea-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="cb1ea-123">Parent Elements</span></span>  
  
|<span data-ttu-id="cb1ea-124">Élément</span><span class="sxs-lookup"><span data-stu-id="cb1ea-124">Element</span></span>|<span data-ttu-id="cb1ea-125">Description</span><span class="sxs-lookup"><span data-stu-id="cb1ea-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cb1ea-126">\<states></span><span class="sxs-lookup"><span data-stu-id="cb1ea-126">\<states></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states-of-activitystatequery.md)|<span data-ttu-id="cb1ea-127">Collection d’éléments de configuration qui contiennent les états de l’activité faisant l’objet d’un abonnement pour laquelle un enregistrement de suivi doit être émis.</span><span class="sxs-lookup"><span data-stu-id="cb1ea-127">A collection of configuration elements that contain the states of the subscribed activity for which a tracking record should be emitted.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cb1ea-128">Notes</span><span class="sxs-lookup"><span data-stu-id="cb1ea-128">Remarks</span></span>  
 <span data-ttu-id="cb1ea-129">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="cb1ea-129">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="cb1ea-130">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="cb1ea-130">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="cb1ea-131">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="cb1ea-131">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="cb1ea-132">L’exemple suivant illustre une requête d’état d’activité qui extrait des variables et arguments lorsque l’enregistrement de suivi `Closed` de l’activité est émis.</span><span class="sxs-lookup"><span data-stu-id="cb1ea-132">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="cb1ea-133">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent, êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="cb1ea-133">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="cb1ea-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb1ea-134">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="cb1ea-135">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="cb1ea-135">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="cb1ea-136">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="cb1ea-136">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
