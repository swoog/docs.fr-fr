---
title: <state> de <states>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: ab483c7f-a091-4933-ba6b-708d96846d38
ms.openlocfilehash: ff75895949c50cd369e4297ea77dc21106994067
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59073934"
---
# <a name="state-of-states"></a><span data-ttu-id="0340a-102">\<état > de \<États ></span><span class="sxs-lookup"><span data-stu-id="0340a-102">\<state> of \<states></span></span>
<span data-ttu-id="0340a-103">Élément de configuration qui contient l'état de l'activité faisant l'objet d'un abonnement pour laquelle un enregistrement de suivi doit être émis.</span><span class="sxs-lookup"><span data-stu-id="0340a-103">A configuration element that contains the state of the subscribed activity for which a tracking record should be emitted.</span></span>  
  
 <span data-ttu-id="0340a-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="0340a-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="0340a-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="0340a-105">\<system.serviceModel></span></span>  
<span data-ttu-id="0340a-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="0340a-106">\<tracking></span></span>  
<span data-ttu-id="0340a-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="0340a-107">\<trackingProfile></span></span>  
<span data-ttu-id="0340a-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="0340a-108">\<workflow></span></span>  
<span data-ttu-id="0340a-109">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="0340a-109">\<activityStateQueries></span></span>  
<span data-ttu-id="0340a-110">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="0340a-110">\<activityStateQuery></span></span>  
<span data-ttu-id="0340a-111">\<states></span><span class="sxs-lookup"><span data-stu-id="0340a-111">\<states></span></span>  
<span data-ttu-id="0340a-112">\<state></span><span class="sxs-lookup"><span data-stu-id="0340a-112">\<state></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0340a-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0340a-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0340a-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0340a-114">Attributes and Elements</span></span>  
 <span data-ttu-id="0340a-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0340a-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0340a-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="0340a-116">Attributes</span></span>  
  
|<span data-ttu-id="0340a-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="0340a-117">Attribute</span></span>|<span data-ttu-id="0340a-118">Description</span><span class="sxs-lookup"><span data-stu-id="0340a-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0340a-119">name</span><span class="sxs-lookup"><span data-stu-id="0340a-119">name</span></span>|<span data-ttu-id="0340a-120">Chaîne qui spécifie l'état de l'activité faisant l'objet d'un abonnement pour laquelle un enregistrement de suivi doit être émis.</span><span class="sxs-lookup"><span data-stu-id="0340a-120">A string that specifies the state of the subscribed activity for which a tracking record should be emitted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0340a-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0340a-121">Child Elements</span></span>  
 <span data-ttu-id="0340a-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0340a-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0340a-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0340a-123">Parent Elements</span></span>  
  
|<span data-ttu-id="0340a-124">Élément</span><span class="sxs-lookup"><span data-stu-id="0340a-124">Element</span></span>|<span data-ttu-id="0340a-125">Description</span><span class="sxs-lookup"><span data-stu-id="0340a-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0340a-126">\<states></span><span class="sxs-lookup"><span data-stu-id="0340a-126">\<states></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states-of-activitystatequery.md)|<span data-ttu-id="0340a-127">Collection d’éléments de configuration qui contiennent les états de l’activité faisant l’objet d’un abonnement pour laquelle un enregistrement de suivi doit être émis.</span><span class="sxs-lookup"><span data-stu-id="0340a-127">A collection of configuration elements that contain the states of the subscribed activity for which a tracking record should be emitted.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0340a-128">Notes</span><span class="sxs-lookup"><span data-stu-id="0340a-128">Remarks</span></span>  
 <span data-ttu-id="0340a-129">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="0340a-129">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="0340a-130">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="0340a-130">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="0340a-131">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="0340a-131">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="0340a-132">L’exemple suivant illustre une requête d’état d’activité qui extrait des variables et arguments lorsque l’enregistrement de suivi `Closed` de l’activité est émis.</span><span class="sxs-lookup"><span data-stu-id="0340a-132">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="0340a-133">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent, êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="0340a-133">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="0340a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0340a-134">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="0340a-135">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="0340a-135">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="0340a-136">Modèles de suivi</span><span class="sxs-lookup"><span data-stu-id="0340a-136">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
