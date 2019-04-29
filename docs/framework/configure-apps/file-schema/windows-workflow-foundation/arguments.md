---
title: <arguments>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 0f327196-f468-4be3-b6c4-68ba981a1bd6
ms.openlocfilehash: 2b0d982997ab590ce7f0fc4c482b1ddfa6bc758f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790362"
---
# <a name="arguments"></a><span data-ttu-id="20235-101">\<arguments></span><span class="sxs-lookup"><span data-stu-id="20235-101">\<arguments></span></span>
<span data-ttu-id="20235-102">Représente une collection d'arguments associés à une requête d'état d'activité.</span><span class="sxs-lookup"><span data-stu-id="20235-102">Represents a collection of arguments associated with an activity state query.</span></span>  
  
 <span data-ttu-id="20235-103">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="20235-103">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="20235-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="20235-104">\<system.serviceModel></span></span>  
<span data-ttu-id="20235-105">\<tracking></span><span class="sxs-lookup"><span data-stu-id="20235-105">\<tracking></span></span>  
<span data-ttu-id="20235-106">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="20235-106">\<trackingProfile></span></span>  
<span data-ttu-id="20235-107">\<workflow></span><span class="sxs-lookup"><span data-stu-id="20235-107">\<workflow></span></span>  
<span data-ttu-id="20235-108">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="20235-108">\<activityStateQueries></span></span>  
<span data-ttu-id="20235-109">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="20235-109">\<activityStateQuery></span></span>  
<span data-ttu-id="20235-110">\<arguments></span><span class="sxs-lookup"><span data-stu-id="20235-110">\<arguments></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20235-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20235-111">Syntax</span></span>  
  
```xml
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <arguments>
          <argument name="String" />
        </arguments>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="20235-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="20235-112">Attributes and Elements</span></span>  
 <span data-ttu-id="20235-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="20235-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="20235-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="20235-114">Attributes</span></span>  
 <span data-ttu-id="20235-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="20235-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="20235-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="20235-116">Child Elements</span></span>  
  
|<span data-ttu-id="20235-117">Élément</span><span class="sxs-lookup"><span data-stu-id="20235-117">Element</span></span>|<span data-ttu-id="20235-118">Description</span><span class="sxs-lookup"><span data-stu-id="20235-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="20235-119">\<argument></span><span class="sxs-lookup"><span data-stu-id="20235-119">\<argument></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/argument.md)|<span data-ttu-id="20235-120">Argument associé à une requête d'état d'activité.</span><span class="sxs-lookup"><span data-stu-id="20235-120">An argument associated with an activity state query.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="20235-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="20235-121">Parent Elements</span></span>  
  
|<span data-ttu-id="20235-122">Élément</span><span class="sxs-lookup"><span data-stu-id="20235-122">Element</span></span>|<span data-ttu-id="20235-123">Description</span><span class="sxs-lookup"><span data-stu-id="20235-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="20235-124">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="20235-124">\<activityStateQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)|<span data-ttu-id="20235-125">Représente un élément de configuration qui permet d'effectuer le suivi des demandes d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="20235-125">Represents a configuration element that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="20235-126">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="20235-126">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="20235-127">Notes</span><span class="sxs-lookup"><span data-stu-id="20235-127">Remarks</span></span>  
 <span data-ttu-id="20235-128">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="20235-128">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="20235-129">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="20235-129">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="20235-130">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="20235-130">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="20235-131">L’exemple suivant illustre une requête d’état d’activité qui extrait des variables et arguments lorsque l’enregistrement de suivi `Closed` de l’activité est émis.</span><span class="sxs-lookup"><span data-stu-id="20235-131">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="20235-132">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent, êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="20235-132">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="20235-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20235-133">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ArgumentElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="20235-134">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="20235-134">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="20235-135">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="20235-135">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
