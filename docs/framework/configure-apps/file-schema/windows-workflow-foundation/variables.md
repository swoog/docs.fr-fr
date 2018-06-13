---
title: '&lt;variables&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: da0fd144-dda9-4613-b650-fe6325076513
ms.openlocfilehash: d0dc83951bdf894d0061971ae4b79854a7c8bcd8
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32756577"
---
# <a name="ltvariablesgt"></a><span data-ttu-id="9b3ae-102">&lt;variables&gt;</span><span class="sxs-lookup"><span data-stu-id="9b3ae-102">&lt;variables&gt;</span></span>
<span data-ttu-id="9b3ae-103">Représente une collection de variables associées à cette requête d'activité.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-103">Represents a collection of variables associated with this activity query.</span></span>  
  
 <span data-ttu-id="9b3ae-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="9b3ae-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="9b3ae-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="9b3ae-105">\<system.serviceModel></span></span>  
<span data-ttu-id="9b3ae-106">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="9b3ae-106">\<tracking></span></span>  
<span data-ttu-id="9b3ae-107">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="9b3ae-107">\<trackingProfile></span></span>  
<span data-ttu-id="9b3ae-108">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="9b3ae-108">\<workflow></span></span>  
<span data-ttu-id="9b3ae-109">\<activityStateQueries ></span><span class="sxs-lookup"><span data-stu-id="9b3ae-109">\<activityStateQueries></span></span>  
<span data-ttu-id="9b3ae-110">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="9b3ae-110">\<activityStateQuery></span></span>  
<span data-ttu-id="9b3ae-111">\<variables ></span><span class="sxs-lookup"><span data-stu-id="9b3ae-111">\<variables></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9b3ae-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b3ae-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9b3ae-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9b3ae-113">Attributes and Elements</span></span>  
 <span data-ttu-id="9b3ae-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9b3ae-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="9b3ae-115">Attributes</span></span>  
 <span data-ttu-id="9b3ae-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9b3ae-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9b3ae-117">Child Elements</span></span>  
  
|<span data-ttu-id="9b3ae-118">Élément</span><span class="sxs-lookup"><span data-stu-id="9b3ae-118">Element</span></span>|<span data-ttu-id="9b3ae-119">Description</span><span class="sxs-lookup"><span data-stu-id="9b3ae-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9b3ae-120">\<variable ></span><span class="sxs-lookup"><span data-stu-id="9b3ae-120">\<variable></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/variable.md)|<span data-ttu-id="9b3ae-121">Variable associée à une requête d'état d'activité.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-121">A variable associated with an activity state query.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9b3ae-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9b3ae-122">Parent Elements</span></span>  
  
|<span data-ttu-id="9b3ae-123">Élément</span><span class="sxs-lookup"><span data-stu-id="9b3ae-123">Element</span></span>|<span data-ttu-id="9b3ae-124">Description</span><span class="sxs-lookup"><span data-stu-id="9b3ae-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9b3ae-125">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="9b3ae-125">\<activityStateQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)|<span data-ttu-id="9b3ae-126">Représente un élément de configuration qui permet d'effectuer le suivi des demandes d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-126">Represents a configuration element that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="9b3ae-127">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-127">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9b3ae-128">Notes</span><span class="sxs-lookup"><span data-stu-id="9b3ae-128">Remarks</span></span>  
 <span data-ttu-id="9b3ae-129">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-129">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="9b3ae-130">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-130">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="9b3ae-131">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail. L’exemple suivant montre une requête d’état d’activité qui extrait des variables et arguments lorsque l’activité `Closed` enregistrement de suivi est émis.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-131">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="9b3ae-132">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="9b3ae-132">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="9b3ae-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b3ae-133">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.VariableElementCollection?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="9b3ae-134">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="9b3ae-134">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="9b3ae-135">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="9b3ae-135">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
