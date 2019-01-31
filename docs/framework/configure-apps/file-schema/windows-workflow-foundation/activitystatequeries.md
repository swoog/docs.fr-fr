---
title: <activityStateQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: bdd3c8ae-a13f-4df1-9b3c-a9d6c4bb1b5f
ms.openlocfilehash: ad41c1afec0b46a404f8f24882587c1dfeb68a80
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55267805"
---
# <a name="activitystatequeries"></a><span data-ttu-id="90028-101">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="90028-101">\<activityStateQueries></span></span>
<span data-ttu-id="90028-102">Représente une collection de requêtes qui permettent d’effectuer le suivi des changements dans le cycle de vie des activités qui composent une instance de workflow.</span><span class="sxs-lookup"><span data-stu-id="90028-102">Represents a collection of queries that are used to track life cycle changes of the activities that make up a workflow instance.</span></span> <span data-ttu-id="90028-103">Par exemple, vous souhaiterez effectuer le suivi de chaque fois que l’activité « Envoyer un message électronique » se termine dans une instance de workflow.</span><span class="sxs-lookup"><span data-stu-id="90028-103">For example, you may want to keep track of every time the "Send E-Mail" activity completes within a workflow instance.</span></span> <span data-ttu-id="90028-104">Cette requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement d'état d'activité.</span><span class="sxs-lookup"><span data-stu-id="90028-104">This query is necessary for a tracking participant to subscribe to activity state record objects.</span></span> <span data-ttu-id="90028-105">Les états disponibles auxquels s'abonner sont spécifiés dans ActivityStates.</span><span class="sxs-lookup"><span data-stu-id="90028-105">The available states to subscribe to are specified in ActivityStates.</span></span>  
  
 <span data-ttu-id="90028-106">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="90028-106">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="90028-107">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="90028-107">\<system.serviceModel></span></span>  
<span data-ttu-id="90028-108">\<tracking></span><span class="sxs-lookup"><span data-stu-id="90028-108">\<tracking></span></span>  
<span data-ttu-id="90028-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="90028-109">\<trackingProfile></span></span>  
<span data-ttu-id="90028-110">\<workflow></span><span class="sxs-lookup"><span data-stu-id="90028-110">\<workflow></span></span>  
<span data-ttu-id="90028-111">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="90028-111">\<activityStateQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="90028-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90028-112">Syntax</span></span>  
  
```xml
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <arguments>
          <argument name="String" />
        </arguments>
        <states>
          <state name="String" />
        </states>
        <variables>
         <variable name="String" />
        </variables>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="90028-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="90028-113">Attributes and Elements</span></span>  
 <span data-ttu-id="90028-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="90028-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="90028-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="90028-115">Attributes</span></span>  
 <span data-ttu-id="90028-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="90028-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="90028-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="90028-117">Child Elements</span></span>  
  
|<span data-ttu-id="90028-118">Élément</span><span class="sxs-lookup"><span data-stu-id="90028-118">Element</span></span>|<span data-ttu-id="90028-119">Description</span><span class="sxs-lookup"><span data-stu-id="90028-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="90028-120">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="90028-120">\<activityStateQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)|<span data-ttu-id="90028-121">Requête utilisée pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="90028-121">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="90028-122">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="90028-122">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="90028-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="90028-123">Parent Elements</span></span>  
  
|<span data-ttu-id="90028-124">Élément</span><span class="sxs-lookup"><span data-stu-id="90028-124">Element</span></span>|<span data-ttu-id="90028-125">Description</span><span class="sxs-lookup"><span data-stu-id="90028-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="90028-126">\<workflow></span><span class="sxs-lookup"><span data-stu-id="90028-126">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="90028-127">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le **activityDefinitionId** propriété.</span><span class="sxs-lookup"><span data-stu-id="90028-127">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="90028-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90028-128">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityStateQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="90028-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="90028-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="90028-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="90028-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
