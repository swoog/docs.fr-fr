---
title: '&lt;Argument&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a7144d53-8023-4e90-971f-895e016fd58a
ms.openlocfilehash: bfcb98085e0b2292d46acfd0a57096219afff606
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltargumentgt"></a><span data-ttu-id="13516-102">&lt;Argument&gt;</span><span class="sxs-lookup"><span data-stu-id="13516-102">&lt;argument&gt;</span></span>
<span data-ttu-id="13516-103">Élément de configuration qui représente un argument associé à une requête d'état d'activité.</span><span class="sxs-lookup"><span data-stu-id="13516-103">A configuration element that represents an argument associated with an activity state query.</span></span>  
  
 <span data-ttu-id="13516-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="13516-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="13516-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="13516-105">\<system.serviceModel></span></span>  
<span data-ttu-id="13516-106">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="13516-106">\<tracking></span></span>  
<span data-ttu-id="13516-107">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="13516-107">\<trackingProfile></span></span>  
<span data-ttu-id="13516-108">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="13516-108">\<workflow></span></span>  
<span data-ttu-id="13516-109">\<activityStateQueries ></span><span class="sxs-lookup"><span data-stu-id="13516-109">\<activityStateQueries></span></span>  
<span data-ttu-id="13516-110">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="13516-110">\<activityStateQuery></span></span>  
<span data-ttu-id="13516-111">\<arguments ></span><span class="sxs-lookup"><span data-stu-id="13516-111">\<arguments></span></span>  
<span data-ttu-id="13516-112">\<argument ></span><span class="sxs-lookup"><span data-stu-id="13516-112">\<argument></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="13516-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13516-113">Syntax</span></span>  
  
```xml
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <arguments>
          <argument name="String"/>
        </arguments>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="13516-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="13516-114">Attributes and Elements</span></span>  
 <span data-ttu-id="13516-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="13516-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="13516-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="13516-116">Attributes</span></span>  
  
|<span data-ttu-id="13516-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="13516-117">Attribute</span></span>|<span data-ttu-id="13516-118">Description</span><span class="sxs-lookup"><span data-stu-id="13516-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="13516-119">name</span><span class="sxs-lookup"><span data-stu-id="13516-119">name</span></span>|<span data-ttu-id="13516-120">Chaîne qui spécifie le nom de l'argument.</span><span class="sxs-lookup"><span data-stu-id="13516-120">A string that specifies the name of the argument.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="13516-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="13516-121">Child Elements</span></span>  
 <span data-ttu-id="13516-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="13516-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="13516-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="13516-123">Parent Elements</span></span>  
  
|<span data-ttu-id="13516-124">Élément</span><span class="sxs-lookup"><span data-stu-id="13516-124">Element</span></span>|<span data-ttu-id="13516-125">Description</span><span class="sxs-lookup"><span data-stu-id="13516-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="13516-126">\<arguments ></span><span class="sxs-lookup"><span data-stu-id="13516-126">\<arguments></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)|<span data-ttu-id="13516-127">Collection d’arguments associés à cette requête d’activité.</span><span class="sxs-lookup"><span data-stu-id="13516-127">A collection of arguments associated with this activity query.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="13516-128">Notes</span><span class="sxs-lookup"><span data-stu-id="13516-128">Remarks</span></span>  
 <span data-ttu-id="13516-129">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="13516-129">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="13516-130">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="13516-130">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="13516-131">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail. L’exemple suivant montre une requête d’état d’activité qui extrait des variables et arguments lorsque l’activité `Closed` enregistrement de suivi est émis.</span><span class="sxs-lookup"><span data-stu-id="13516-131">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="13516-132">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="13516-132">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="13516-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13516-133">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.ArgumentElement?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="13516-134">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="13516-134">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="13516-135">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="13516-135">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
