---
title: <argument>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a7144d53-8023-4e90-971f-895e016fd58a
ms.openlocfilehash: e386ad261422904d3f33385bb80bdb8c1ac029b9
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57371176"
---
# <a name="argument"></a><span data-ttu-id="6e2d5-101">\<argument></span><span class="sxs-lookup"><span data-stu-id="6e2d5-101">\<argument></span></span>
<span data-ttu-id="6e2d5-102">Élément de configuration qui représente un argument associé à une requête d'état d'activité.</span><span class="sxs-lookup"><span data-stu-id="6e2d5-102">A configuration element that represents an argument associated with an activity state query.</span></span>  
  
 <span data-ttu-id="6e2d5-103">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="6e2d5-103">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="6e2d5-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="6e2d5-104">\<system.serviceModel></span></span>  
<span data-ttu-id="6e2d5-105">\<tracking></span><span class="sxs-lookup"><span data-stu-id="6e2d5-105">\<tracking></span></span>  
<span data-ttu-id="6e2d5-106">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="6e2d5-106">\<trackingProfile></span></span>  
<span data-ttu-id="6e2d5-107">\<workflow></span><span class="sxs-lookup"><span data-stu-id="6e2d5-107">\<workflow></span></span>  
<span data-ttu-id="6e2d5-108">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="6e2d5-108">\<activityStateQueries></span></span>  
<span data-ttu-id="6e2d5-109">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="6e2d5-109">\<activityStateQuery></span></span>  
<span data-ttu-id="6e2d5-110">\<arguments></span><span class="sxs-lookup"><span data-stu-id="6e2d5-110">\<arguments></span></span>  
<span data-ttu-id="6e2d5-111">\<argument></span><span class="sxs-lookup"><span data-stu-id="6e2d5-111">\<argument></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e2d5-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e2d5-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6e2d5-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6e2d5-113">Attributes and Elements</span></span>  
 <span data-ttu-id="6e2d5-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6e2d5-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6e2d5-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="6e2d5-115">Attributes</span></span>  
  
|<span data-ttu-id="6e2d5-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="6e2d5-116">Attribute</span></span>|<span data-ttu-id="6e2d5-117">Description</span><span class="sxs-lookup"><span data-stu-id="6e2d5-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6e2d5-118">name</span><span class="sxs-lookup"><span data-stu-id="6e2d5-118">name</span></span>|<span data-ttu-id="6e2d5-119">Chaîne qui spécifie le nom de l'argument.</span><span class="sxs-lookup"><span data-stu-id="6e2d5-119">A string that specifies the name of the argument.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6e2d5-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6e2d5-120">Child Elements</span></span>  
 <span data-ttu-id="6e2d5-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6e2d5-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6e2d5-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6e2d5-122">Parent Elements</span></span>  
  
|<span data-ttu-id="6e2d5-123">Élément</span><span class="sxs-lookup"><span data-stu-id="6e2d5-123">Element</span></span>|<span data-ttu-id="6e2d5-124">Description</span><span class="sxs-lookup"><span data-stu-id="6e2d5-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6e2d5-125">\<arguments></span><span class="sxs-lookup"><span data-stu-id="6e2d5-125">\<arguments></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)|<span data-ttu-id="6e2d5-126">Collection d’arguments associés à cette requête d’activité.</span><span class="sxs-lookup"><span data-stu-id="6e2d5-126">A collection of arguments associated with this activity query.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6e2d5-127">Notes</span><span class="sxs-lookup"><span data-stu-id="6e2d5-127">Remarks</span></span>  
 <span data-ttu-id="6e2d5-128">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="6e2d5-128">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="6e2d5-129">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="6e2d5-129">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="6e2d5-130">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="6e2d5-130">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="6e2d5-131">L’exemple suivant illustre une requête d’état d’activité qui extrait des variables et arguments lorsque l’enregistrement de suivi `Closed` de l’activité est émis.</span><span class="sxs-lookup"><span data-stu-id="6e2d5-131">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="6e2d5-132">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent, êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="6e2d5-132">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="6e2d5-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e2d5-133">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.ArgumentElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="6e2d5-134">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="6e2d5-134">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="6e2d5-135">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="6e2d5-135">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
