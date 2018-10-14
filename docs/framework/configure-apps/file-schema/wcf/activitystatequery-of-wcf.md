---
title: '&lt;activityStateQuery&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: d6cdc04b-6f3a-4097-a623-ee4a1be3b5c4
ms.openlocfilehash: a0dae6b90659bd3f53386459513abf92f25b005b
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2018
ms.locfileid: "49308311"
---
# <a name="ltactivitystatequerygt-of-wcf"></a><span data-ttu-id="a343b-102">&lt;activityStateQuery&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="a343b-102">&lt;activityStateQuery&gt; of WCF</span></span>

<span data-ttu-id="a343b-103">Représente une requête qui permet d'effectuer le suivi des changements dans le cycle de vie des activités qui composent une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="a343b-103">Represents a query that is used to track life cycle changes of the activities that make up a workflow instance.</span></span> <span data-ttu-id="a343b-104">Par exemple, vous souhaiterez effectuer le suivi de chaque fois que l’activité « Envoyer un message électronique » se termine dans une instance de workflow.</span><span class="sxs-lookup"><span data-stu-id="a343b-104">For example, you may want to keep track of every time the "Send E-Mail" activity completes within a workflow instance.</span></span> <span data-ttu-id="a343b-105">Cette requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement d'état d'activité.</span><span class="sxs-lookup"><span data-stu-id="a343b-105">This query is necessary for a tracking participant to subscribe to activity state record objects.</span></span> <span data-ttu-id="a343b-106">Les états disponibles auxquels s'abonner sont spécifiés dans ActivityStates.</span><span class="sxs-lookup"><span data-stu-id="a343b-106">The available states to subscribe to are specified in ActivityStates.</span></span>  
  
<span data-ttu-id="a343b-107">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="a343b-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>

<span data-ttu-id="a343b-108">\<system.serviceModel > \<suivi ></span><span class="sxs-lookup"><span data-stu-id="a343b-108">\<system.serviceModel> \<tracking></span></span>  
<span data-ttu-id="a343b-109">\<profils > \<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="a343b-109">\<profiles> \<trackingProfile></span></span>  
<span data-ttu-id="a343b-110">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="a343b-110">\<workflow></span></span>  
<span data-ttu-id="a343b-111">\<activityStateQueries ></span><span class="sxs-lookup"><span data-stu-id="a343b-111">\<activityStateQueries></span></span>  
<span data-ttu-id="a343b-112">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="a343b-112">\<activityStateQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a343b-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a343b-113">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityStateQueries>
          <activityStateQuery activityName="String">
            <arguments>
              <argument name="String"/>
            </arguments>
            <states>
              <state name="String"/>
            </states>
            <variables>
              <variable name="String"/>
            </variables>
          </activityStateQuery>
        </activityStateQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a343b-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a343b-114">Attributes and elements</span></span>  

<span data-ttu-id="a343b-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a343b-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a343b-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="a343b-116">Attributes</span></span>  
  
|<span data-ttu-id="a343b-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="a343b-117">Attribute</span></span>|<span data-ttu-id="a343b-118">Description</span><span class="sxs-lookup"><span data-stu-id="a343b-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a343b-119">activityName</span><span class="sxs-lookup"><span data-stu-id="a343b-119">activityName</span></span>|<span data-ttu-id="a343b-120">Chaîne qui spécifie le nom de l'activité sur lequel filtrer des instances <xref:System.Activities.Tracking.ActivityStateRecord>.</span><span class="sxs-lookup"><span data-stu-id="a343b-120">A string that specifies the name of the activity to filter <xref:System.Activities.Tracking.ActivityStateRecord> instances on.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a343b-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a343b-121">Child elements</span></span>  
  
|<span data-ttu-id="a343b-122">Élément</span><span class="sxs-lookup"><span data-stu-id="a343b-122">Element</span></span>|<span data-ttu-id="a343b-123">Description</span><span class="sxs-lookup"><span data-stu-id="a343b-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a343b-124">\<arguments ></span><span class="sxs-lookup"><span data-stu-id="a343b-124">\<arguments></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)|<span data-ttu-id="a343b-125">Collection d’arguments associés à cette requête d’activité.</span><span class="sxs-lookup"><span data-stu-id="a343b-125">A collection of arguments associated with this activity query.</span></span>|  
|[<span data-ttu-id="a343b-126">\<États ></span><span class="sxs-lookup"><span data-stu-id="a343b-126">\<states></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)|<span data-ttu-id="a343b-127">Collection d’éléments de configuration qui contiennent les états de l’activité faisant l’objet d’un abonnement pour laquelle un enregistrement de suivi doit être émis.</span><span class="sxs-lookup"><span data-stu-id="a343b-127">A collection of configuration elements that contain the states of the subscribed activity for which a tracking record should be emitted.</span></span>|  
|[<span data-ttu-id="a343b-128">\<États ></span><span class="sxs-lookup"><span data-stu-id="a343b-128">\<states></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)|<span data-ttu-id="a343b-129">Collection de variables associées à cette requête d’activité.</span><span class="sxs-lookup"><span data-stu-id="a343b-129">A collection of variables associated with this activity query.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a343b-130">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a343b-130">Parent elements</span></span>  
  
|<span data-ttu-id="a343b-131">Élément</span><span class="sxs-lookup"><span data-stu-id="a343b-131">Element</span></span>|<span data-ttu-id="a343b-132">Description</span><span class="sxs-lookup"><span data-stu-id="a343b-132">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a343b-133">\<faultPropagationQuery ></span><span class="sxs-lookup"><span data-stu-id="a343b-133">\<faultPropagationQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationquery.md)|<span data-ttu-id="a343b-134">Représente une liste d'éléments de configuration qui permettent d'effectuer le suivi des demandes d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="a343b-134">Represents a list of configuration elements that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="a343b-135">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="a343b-135">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a343b-136">Notes</span><span class="sxs-lookup"><span data-stu-id="a343b-136">Remarks</span></span>

<span data-ttu-id="a343b-137">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="a343b-137">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="a343b-138">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="a343b-138">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="a343b-139">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail. L’exemple suivant montre une requête d’état d’activité qui extrait des variables et des arguments lors de l’activité `Closed` enregistrement de suivi est émis.</span><span class="sxs-lookup"><span data-stu-id="a343b-139">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="a343b-140">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent, êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="a343b-140">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="a343b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a343b-141">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityStateQueryElement>
- <xref:System.Activities.Tracking.ActivityStateQuery>
- [<span data-ttu-id="a343b-142">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="a343b-142">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="a343b-143">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="a343b-143">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
