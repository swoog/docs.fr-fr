---
title: <argument>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a7144d53-8023-4e90-971f-895e016fd58a
ms.openlocfilehash: a920d60d703fe262bee96d75c420c526d54f88ab
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59210644"
---
# <a name="argument"></a><span data-ttu-id="a23a0-101">\<argument></span><span class="sxs-lookup"><span data-stu-id="a23a0-101">\<argument></span></span>
<span data-ttu-id="a23a0-102">Élément de configuration qui représente un argument associé à une requête d'état d'activité.</span><span class="sxs-lookup"><span data-stu-id="a23a0-102">A configuration element that represents an argument associated with an activity state query.</span></span>  
  
 <span data-ttu-id="a23a0-103">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="a23a0-103">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="a23a0-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="a23a0-104">\<system.serviceModel></span></span>  
<span data-ttu-id="a23a0-105">\<tracking></span><span class="sxs-lookup"><span data-stu-id="a23a0-105">\<tracking></span></span>  
<span data-ttu-id="a23a0-106">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="a23a0-106">\<trackingProfile></span></span>  
<span data-ttu-id="a23a0-107">\<workflow></span><span class="sxs-lookup"><span data-stu-id="a23a0-107">\<workflow></span></span>  
<span data-ttu-id="a23a0-108">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="a23a0-108">\<activityStateQueries></span></span>  
<span data-ttu-id="a23a0-109">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="a23a0-109">\<activityStateQuery></span></span>  
<span data-ttu-id="a23a0-110">\<arguments></span><span class="sxs-lookup"><span data-stu-id="a23a0-110">\<arguments></span></span>  
<span data-ttu-id="a23a0-111">\<argument></span><span class="sxs-lookup"><span data-stu-id="a23a0-111">\<argument></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a23a0-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a23a0-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a23a0-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a23a0-113">Attributes and Elements</span></span>  
 <span data-ttu-id="a23a0-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a23a0-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a23a0-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="a23a0-115">Attributes</span></span>  
  
|<span data-ttu-id="a23a0-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="a23a0-116">Attribute</span></span>|<span data-ttu-id="a23a0-117">Description</span><span class="sxs-lookup"><span data-stu-id="a23a0-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a23a0-118">name</span><span class="sxs-lookup"><span data-stu-id="a23a0-118">name</span></span>|<span data-ttu-id="a23a0-119">Chaîne qui spécifie le nom de l'argument.</span><span class="sxs-lookup"><span data-stu-id="a23a0-119">A string that specifies the name of the argument.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a23a0-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a23a0-120">Child Elements</span></span>  
 <span data-ttu-id="a23a0-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a23a0-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a23a0-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a23a0-122">Parent Elements</span></span>  
  
|<span data-ttu-id="a23a0-123">Élément</span><span class="sxs-lookup"><span data-stu-id="a23a0-123">Element</span></span>|<span data-ttu-id="a23a0-124">Description</span><span class="sxs-lookup"><span data-stu-id="a23a0-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a23a0-125">\<arguments></span><span class="sxs-lookup"><span data-stu-id="a23a0-125">\<arguments></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)|<span data-ttu-id="a23a0-126">Collection d’arguments associés à cette requête d’activité.</span><span class="sxs-lookup"><span data-stu-id="a23a0-126">A collection of arguments associated with this activity query.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a23a0-127">Notes</span><span class="sxs-lookup"><span data-stu-id="a23a0-127">Remarks</span></span>  
 <span data-ttu-id="a23a0-128">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="a23a0-128">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="a23a0-129">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="a23a0-129">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="a23a0-130">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="a23a0-130">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="a23a0-131">L’exemple suivant illustre une requête d’état d’activité qui extrait des variables et arguments lorsque l’enregistrement de suivi `Closed` de l’activité est émis.</span><span class="sxs-lookup"><span data-stu-id="a23a0-131">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="a23a0-132">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent, êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="a23a0-132">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="a23a0-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a23a0-133">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ArgumentElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="a23a0-134">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="a23a0-134">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="a23a0-135">Modèles de suivi</span><span class="sxs-lookup"><span data-stu-id="a23a0-135">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
