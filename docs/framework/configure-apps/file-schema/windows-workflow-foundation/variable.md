---
title: <variable>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 46cc8cbc-10ec-4625-8813-3f5cd6c6afde
ms.openlocfilehash: c85f3c57739c48566c97c8b1debfb7f2c3912bdf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61613519"
---
# <a name="variable"></a><span data-ttu-id="1f61c-101">\<variable></span><span class="sxs-lookup"><span data-stu-id="1f61c-101">\<variable></span></span>
<span data-ttu-id="1f61c-102">Représente une collection de variables associées à cette requête d'activité.</span><span class="sxs-lookup"><span data-stu-id="1f61c-102">Represents a collection of variables associated with this activity query.</span></span>  
  
 <span data-ttu-id="1f61c-103">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="1f61c-103">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="1f61c-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="1f61c-104">\<system.serviceModel></span></span>  
<span data-ttu-id="1f61c-105">\<tracking></span><span class="sxs-lookup"><span data-stu-id="1f61c-105">\<tracking></span></span>  
<span data-ttu-id="1f61c-106">\<profiles></span><span class="sxs-lookup"><span data-stu-id="1f61c-106">\<profiles></span></span>  
<span data-ttu-id="1f61c-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="1f61c-107">\<trackingProfile></span></span>  
<span data-ttu-id="1f61c-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="1f61c-108">\<workflow></span></span>  
<span data-ttu-id="1f61c-109">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="1f61c-109">\<activityStateQueries></span></span>  
<span data-ttu-id="1f61c-110">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="1f61c-110">\<activityStateQuery></span></span>  
<span data-ttu-id="1f61c-111">\<variables></span><span class="sxs-lookup"><span data-stu-id="1f61c-111">\<variables></span></span>  
<span data-ttu-id="1f61c-112">\<variable></span><span class="sxs-lookup"><span data-stu-id="1f61c-112">\<variable></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1f61c-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f61c-113">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <variables>
          <variable name="String" />
        </variables>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1f61c-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1f61c-114">Attributes and Elements</span></span>  
 <span data-ttu-id="1f61c-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1f61c-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1f61c-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="1f61c-116">Attributes</span></span>  
  
|<span data-ttu-id="1f61c-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="1f61c-117">Attribute</span></span>|<span data-ttu-id="1f61c-118">Description</span><span class="sxs-lookup"><span data-stu-id="1f61c-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="1f61c-119">name</span><span class="sxs-lookup"><span data-stu-id="1f61c-119">name</span></span>|<span data-ttu-id="1f61c-120">Chaîne qui spécifie le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="1f61c-120">A string that specifies the name of the variable.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1f61c-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1f61c-121">Child Elements</span></span>  
 <span data-ttu-id="1f61c-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1f61c-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1f61c-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1f61c-123">Parent Elements</span></span>  
  
|<span data-ttu-id="1f61c-124">Élément</span><span class="sxs-lookup"><span data-stu-id="1f61c-124">Element</span></span>|<span data-ttu-id="1f61c-125">Description</span><span class="sxs-lookup"><span data-stu-id="1f61c-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1f61c-126">\<variable></span><span class="sxs-lookup"><span data-stu-id="1f61c-126">\<variable></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/variable.md)|<span data-ttu-id="1f61c-127">Variable associée à une requête d'état d'activité.</span><span class="sxs-lookup"><span data-stu-id="1f61c-127">A variable associated with an activity state query.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1f61c-128">Notes</span><span class="sxs-lookup"><span data-stu-id="1f61c-128">Remarks</span></span>  
 <span data-ttu-id="1f61c-129">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="1f61c-129">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="1f61c-130">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="1f61c-130">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="1f61c-131">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="1f61c-131">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="1f61c-132">L’exemple suivant illustre une requête d’état d’activité qui extrait des variables et arguments lorsque l’enregistrement de suivi `Closed` de l’activité est émis.</span><span class="sxs-lookup"><span data-stu-id="1f61c-132">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="1f61c-133">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent, êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="1f61c-133">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="1f61c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f61c-134">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.VariableElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="1f61c-135">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="1f61c-135">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="1f61c-136">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="1f61c-136">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
