---
title: '&lt;Variable&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 46cc8cbc-10ec-4625-8813-3f5cd6c6afde
ms.openlocfilehash: c65b377d85783f29ca2a8223e97eb10b073cee0a
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53155234"
---
# <a name="ltvariablegt"></a><span data-ttu-id="6db8d-102">&lt;Variable&gt;</span><span class="sxs-lookup"><span data-stu-id="6db8d-102">&lt;variable&gt;</span></span>
<span data-ttu-id="6db8d-103">Représente une collection de variables associées à cette requête d'activité.</span><span class="sxs-lookup"><span data-stu-id="6db8d-103">Represents a collection of variables associated with this activity query.</span></span>  
  
 <span data-ttu-id="6db8d-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="6db8d-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="6db8d-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="6db8d-105">\<system.serviceModel></span></span>  
<span data-ttu-id="6db8d-106">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="6db8d-106">\<tracking></span></span>  
<span data-ttu-id="6db8d-107">\<profils ></span><span class="sxs-lookup"><span data-stu-id="6db8d-107">\<profiles></span></span>  
<span data-ttu-id="6db8d-108">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="6db8d-108">\<trackingProfile></span></span>  
<span data-ttu-id="6db8d-109">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="6db8d-109">\<workflow></span></span>  
<span data-ttu-id="6db8d-110">\<activityStateQueries ></span><span class="sxs-lookup"><span data-stu-id="6db8d-110">\<activityStateQueries></span></span>  
<span data-ttu-id="6db8d-111">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="6db8d-111">\<activityStateQuery></span></span>  
<span data-ttu-id="6db8d-112">\<variables ></span><span class="sxs-lookup"><span data-stu-id="6db8d-112">\<variables></span></span>  
<span data-ttu-id="6db8d-113">\<variable ></span><span class="sxs-lookup"><span data-stu-id="6db8d-113">\<variable></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6db8d-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6db8d-114">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6db8d-115">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6db8d-115">Attributes and Elements</span></span>  
 <span data-ttu-id="6db8d-116">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6db8d-116">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6db8d-117">Attributs</span><span class="sxs-lookup"><span data-stu-id="6db8d-117">Attributes</span></span>  
  
|<span data-ttu-id="6db8d-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="6db8d-118">Attribute</span></span>|<span data-ttu-id="6db8d-119">Description</span><span class="sxs-lookup"><span data-stu-id="6db8d-119">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6db8d-120">name</span><span class="sxs-lookup"><span data-stu-id="6db8d-120">name</span></span>|<span data-ttu-id="6db8d-121">Chaîne qui spécifie le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="6db8d-121">A string that specifies the name of the variable.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6db8d-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6db8d-122">Child Elements</span></span>  
 <span data-ttu-id="6db8d-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6db8d-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6db8d-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6db8d-124">Parent Elements</span></span>  
  
|<span data-ttu-id="6db8d-125">Élément</span><span class="sxs-lookup"><span data-stu-id="6db8d-125">Element</span></span>|<span data-ttu-id="6db8d-126">Description</span><span class="sxs-lookup"><span data-stu-id="6db8d-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6db8d-127">\<variable ></span><span class="sxs-lookup"><span data-stu-id="6db8d-127">\<variable></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/variable.md)|<span data-ttu-id="6db8d-128">Variable associée à une requête d'état d'activité.</span><span class="sxs-lookup"><span data-stu-id="6db8d-128">A variable associated with an activity state query.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6db8d-129">Notes</span><span class="sxs-lookup"><span data-stu-id="6db8d-129">Remarks</span></span>  
 <span data-ttu-id="6db8d-130">Une fonctionnalité propre à ActivityStateQuery est la possibilité d’extraire des données lors du suivi de l’exécution d’un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="6db8d-130">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="6db8d-131">Vous disposez ainsi d'un contexte supplémentaire lors de l'accès à une post-exécution d'enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="6db8d-131">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="6db8d-132">Vous pouvez utiliser la [ \<arguments >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) et [ \<États >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) éléments à extraire une variable ou un argument à partir de toutes les activités dans un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="6db8d-132">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="6db8d-133">L’exemple suivant illustre une requête d’état d’activité qui extrait des variables et arguments lorsque l’enregistrement de suivi `Closed` de l’activité est émis.</span><span class="sxs-lookup"><span data-stu-id="6db8d-133">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="6db8d-134">Variables et arguments peuvent être extraits uniquement avec un objet ActivityStateRecord et par conséquent, êtes abonnés au sein d’un suivi à l’aide du profil [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span><span class="sxs-lookup"><span data-stu-id="6db8d-134">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="6db8d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6db8d-135">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.VariableElement?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="6db8d-136">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="6db8d-136">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="6db8d-137">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="6db8d-137">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
