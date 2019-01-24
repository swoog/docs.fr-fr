---
title: '&lt;activityStateQueries&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: bdd3c8ae-a13f-4df1-9b3c-a9d6c4bb1b5f
ms.openlocfilehash: bfd19e00e79a95eb717ca9131e92b5ff5c600d5b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54511980"
---
# <a name="ltactivitystatequeriesgt"></a><span data-ttu-id="f47e5-102">&lt;activityStateQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="f47e5-102">&lt;activityStateQueries&gt;</span></span>
<span data-ttu-id="f47e5-103">Représente une collection de requêtes qui permettent d’effectuer le suivi des changements dans le cycle de vie des activités qui composent une instance de workflow.</span><span class="sxs-lookup"><span data-stu-id="f47e5-103">Represents a collection of queries that are used to track life cycle changes of the activities that make up a workflow instance.</span></span> <span data-ttu-id="f47e5-104">Par exemple, vous souhaiterez effectuer le suivi de chaque fois que l’activité « Envoyer un message électronique » se termine dans une instance de workflow.</span><span class="sxs-lookup"><span data-stu-id="f47e5-104">For example, you may want to keep track of every time the "Send E-Mail" activity completes within a workflow instance.</span></span> <span data-ttu-id="f47e5-105">Cette requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement d'état d'activité.</span><span class="sxs-lookup"><span data-stu-id="f47e5-105">This query is necessary for a tracking participant to subscribe to activity state record objects.</span></span> <span data-ttu-id="f47e5-106">Les états disponibles auxquels s'abonner sont spécifiés dans ActivityStates.</span><span class="sxs-lookup"><span data-stu-id="f47e5-106">The available states to subscribe to are specified in ActivityStates.</span></span>  
  
 <span data-ttu-id="f47e5-107">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="f47e5-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="f47e5-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="f47e5-108">\<system.serviceModel></span></span>  
<span data-ttu-id="f47e5-109">\<tracking></span><span class="sxs-lookup"><span data-stu-id="f47e5-109">\<tracking></span></span>  
<span data-ttu-id="f47e5-110">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="f47e5-110">\<trackingProfile></span></span>  
<span data-ttu-id="f47e5-111">\<workflow></span><span class="sxs-lookup"><span data-stu-id="f47e5-111">\<workflow></span></span>  
<span data-ttu-id="f47e5-112">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="f47e5-112">\<activityStateQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f47e5-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f47e5-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f47e5-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f47e5-114">Attributes and Elements</span></span>  
 <span data-ttu-id="f47e5-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f47e5-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f47e5-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="f47e5-116">Attributes</span></span>  
 <span data-ttu-id="f47e5-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f47e5-117">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="f47e5-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f47e5-118">Child Elements</span></span>  
  
|<span data-ttu-id="f47e5-119">Élément</span><span class="sxs-lookup"><span data-stu-id="f47e5-119">Element</span></span>|<span data-ttu-id="f47e5-120">Description</span><span class="sxs-lookup"><span data-stu-id="f47e5-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f47e5-121">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="f47e5-121">\<activityStateQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)|<span data-ttu-id="f47e5-122">Requête utilisée pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="f47e5-122">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="f47e5-123">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="f47e5-123">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f47e5-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f47e5-124">Parent Elements</span></span>  
  
|<span data-ttu-id="f47e5-125">Élément</span><span class="sxs-lookup"><span data-stu-id="f47e5-125">Element</span></span>|<span data-ttu-id="f47e5-126">Description</span><span class="sxs-lookup"><span data-stu-id="f47e5-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f47e5-127">\<workflow></span><span class="sxs-lookup"><span data-stu-id="f47e5-127">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="f47e5-128">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le **activityDefinitionId** propriété.</span><span class="sxs-lookup"><span data-stu-id="f47e5-128">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f47e5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f47e5-129">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityStateQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="f47e5-130">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="f47e5-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="f47e5-131">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="f47e5-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
