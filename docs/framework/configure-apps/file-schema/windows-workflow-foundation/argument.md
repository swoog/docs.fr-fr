---
title: '&lt;argument&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a7144d53-8023-4e90-971f-895e016fd58a
ms.openlocfilehash: 3744781f844d4a1728ba1e9846b2b8c56c0ad8fd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54554598"
---
# <a name="ltargumentgt"></a><span data-ttu-id="d90df-102">&lt;argument&gt;</span><span class="sxs-lookup"><span data-stu-id="d90df-102">&lt;argument&gt;</span></span>
<span data-ttu-id="d90df-103">Élément de configuration qui représente un argument associé à une requête d'état d'activité.</span><span class="sxs-lookup"><span data-stu-id="d90df-103">A configuration element that represents an argument associated with an activity state query.</span></span>  
  
 <span data-ttu-id="d90df-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="d90df-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="d90df-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="d90df-105">\<system.serviceModel></span></span>  
<span data-ttu-id="d90df-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="d90df-106">\<tracking></span></span>  
<span data-ttu-id="d90df-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="d90df-107">\<trackingProfile></span></span>  
<span data-ttu-id="d90df-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="d90df-108">\<workflow></span></span>  
<span data-ttu-id="d90df-109">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="d90df-109">\<activityStateQueries></span></span>  
<span data-ttu-id="d90df-110">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="d90df-110">\<activityStateQuery></span></span>  
<span data-ttu-id="d90df-111">\<arguments></span><span class="sxs-lookup"><span data-stu-id="d90df-111">\<arguments></span></span>  
<span data-ttu-id="d90df-112">\<argument></span><span class="sxs-lookup"><span data-stu-id="d90df-112">\<argument></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d90df-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d90df-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d90df-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d90df-114">Attributes and Elements</span></span>  
 <span data-ttu-id="d90df-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d90df-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d90df-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="d90df-116">Attributes</span></span>  
  
|<span data-ttu-id="d90df-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="d90df-117">Attribute</span></span>|<span data-ttu-id="d90df-118">Description</span><span class="sxs-lookup"><span data-stu-id="d90df-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d90df-119">name</span><span class="sxs-lookup"><span data-stu-id="d90df-119">name</span></span>|<span data-ttu-id="d90df-120">Chaîne qui spécifie le nom de l'argument.</span><span class="sxs-lookup"><span data-stu-id="d90df-120">A string that specifies the name of the argument.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d90df-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d90df-121">Child Elements</span></span>  
 <span data-ttu-id="d90df-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d90df-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d90df-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d90df-123">Parent Elements</span></span>  
  
|<span data-ttu-id="d90df-124">Élément</span><span class="sxs-lookup"><span data-stu-id="d90df-124">Element</span></span>|<span data-ttu-id="d90df-125">Description</span><span class="sxs-lookup"><span data-stu-id="d90df-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d90df-126">\<arguments></span><span class="sxs-lookup"><span data-stu-id="d90df-126">\<arguments></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)|<span data-ttu-id="d90df-127">Collection d’arguments associés à cette requête d’activité.</span><span class="sxs-lookup"><span data-stu-id="d90df-127">A collection of arguments associated with this activity query.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d90df-128">Notes</span><span class="sxs-lookup"><span data-stu-id="d90df-128">Remarks</span></span>  
 <span data-ttu-id="d90df-129">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="d90df-129">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="d90df-130">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="d90df-130">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="d90df-131">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="d90df-131">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="d90df-132">L’exemple suivant illustre une requête d’état d’activité qui extrait des variables et arguments lorsque l’enregistrement de suivi `Closed` de l’activité est émis.</span><span class="sxs-lookup"><span data-stu-id="d90df-132">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="d90df-133">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent, êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="d90df-133">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="d90df-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d90df-134">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.ArgumentElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="d90df-135">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="d90df-135">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="d90df-136">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="d90df-136">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
