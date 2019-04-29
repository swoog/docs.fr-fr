---
title: <variables>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: da0fd144-dda9-4613-b650-fe6325076513
ms.openlocfilehash: 61a786efc67f4e9afa585864e1f62b966b5cdff8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61613405"
---
# <a name="variables"></a><span data-ttu-id="1af2f-101">\<variables></span><span class="sxs-lookup"><span data-stu-id="1af2f-101">\<variables></span></span>
<span data-ttu-id="1af2f-102">Représente une collection de variables associées à cette requête d'activité.</span><span class="sxs-lookup"><span data-stu-id="1af2f-102">Represents a collection of variables associated with this activity query.</span></span>  
  
 <span data-ttu-id="1af2f-103">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="1af2f-103">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="1af2f-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="1af2f-104">\<system.serviceModel></span></span>  
<span data-ttu-id="1af2f-105">\<tracking></span><span class="sxs-lookup"><span data-stu-id="1af2f-105">\<tracking></span></span>  
<span data-ttu-id="1af2f-106">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="1af2f-106">\<trackingProfile></span></span>  
<span data-ttu-id="1af2f-107">\<workflow></span><span class="sxs-lookup"><span data-stu-id="1af2f-107">\<workflow></span></span>  
<span data-ttu-id="1af2f-108">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="1af2f-108">\<activityStateQueries></span></span>  
<span data-ttu-id="1af2f-109">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="1af2f-109">\<activityStateQuery></span></span>  
<span data-ttu-id="1af2f-110">\<variables></span><span class="sxs-lookup"><span data-stu-id="1af2f-110">\<variables></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1af2f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1af2f-111">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1af2f-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1af2f-112">Attributes and Elements</span></span>  
 <span data-ttu-id="1af2f-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1af2f-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1af2f-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="1af2f-114">Attributes</span></span>  
 <span data-ttu-id="1af2f-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1af2f-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="1af2f-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1af2f-116">Child Elements</span></span>  
  
|<span data-ttu-id="1af2f-117">Élément</span><span class="sxs-lookup"><span data-stu-id="1af2f-117">Element</span></span>|<span data-ttu-id="1af2f-118">Description</span><span class="sxs-lookup"><span data-stu-id="1af2f-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1af2f-119">\<variable></span><span class="sxs-lookup"><span data-stu-id="1af2f-119">\<variable></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/variable.md)|<span data-ttu-id="1af2f-120">Variable associée à une requête d'état d'activité.</span><span class="sxs-lookup"><span data-stu-id="1af2f-120">A variable associated with an activity state query.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1af2f-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1af2f-121">Parent Elements</span></span>  
  
|<span data-ttu-id="1af2f-122">Élément</span><span class="sxs-lookup"><span data-stu-id="1af2f-122">Element</span></span>|<span data-ttu-id="1af2f-123">Description</span><span class="sxs-lookup"><span data-stu-id="1af2f-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1af2f-124">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="1af2f-124">\<activityStateQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)|<span data-ttu-id="1af2f-125">Représente un élément de configuration qui permet d'effectuer le suivi des demandes d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="1af2f-125">Represents a configuration element that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="1af2f-126">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="1af2f-126">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1af2f-127">Notes</span><span class="sxs-lookup"><span data-stu-id="1af2f-127">Remarks</span></span>  
 <span data-ttu-id="1af2f-128">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="1af2f-128">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="1af2f-129">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="1af2f-129">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="1af2f-130">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="1af2f-130">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="1af2f-131">L’exemple suivant illustre une requête d’état d’activité qui extrait des variables et arguments lorsque l’enregistrement de suivi `Closed` de l’activité est émis.</span><span class="sxs-lookup"><span data-stu-id="1af2f-131">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="1af2f-132">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent, êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="1af2f-132">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="1af2f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1af2f-133">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.VariableElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="1af2f-134">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="1af2f-134">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="1af2f-135">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="1af2f-135">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
