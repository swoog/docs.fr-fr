---
title: <faultPropagationQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 00ff90ae-ebe0-4c85-a93f-61557288d0a3
ms.openlocfilehash: 402b938913575adfa9125b981dc2913680f07b73
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790154"
---
# <a name="faultpropagationqueries"></a><span data-ttu-id="18d1e-101">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="18d1e-101">\<faultPropagationQueries></span></span>
<span data-ttu-id="18d1e-102">Représente une collection de requêtes qui permettent d’effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="18d1e-102">Represents a collection of queries that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="18d1e-103">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="18d1e-103">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="18d1e-104">Vous devez utiliser cette requête pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="18d1e-104">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="18d1e-105">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements de propagation d'erreur.</span><span class="sxs-lookup"><span data-stu-id="18d1e-105">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
 <span data-ttu-id="18d1e-106">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="18d1e-106">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="18d1e-107">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="18d1e-107">\<system.serviceModel></span></span>  
<span data-ttu-id="18d1e-108">\<tracking></span><span class="sxs-lookup"><span data-stu-id="18d1e-108">\<tracking></span></span>  
<span data-ttu-id="18d1e-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="18d1e-109">\<trackingProfile></span></span>  
<span data-ttu-id="18d1e-110">\<workflow></span><span class="sxs-lookup"><span data-stu-id="18d1e-110">\<workflow></span></span>  
<span data-ttu-id="18d1e-111">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="18d1e-111">\<faultPropagationQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="18d1e-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18d1e-112">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <faultPropagationQueries>
        <faultPropagationQuery activityName="String" 
                               faultHandlerActivityName="String" />
      </faultPropagationQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="18d1e-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="18d1e-113">Attributes and Elements</span></span>  
 <span data-ttu-id="18d1e-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="18d1e-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="18d1e-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="18d1e-115">Attributes</span></span>  
 <span data-ttu-id="18d1e-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="18d1e-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="18d1e-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="18d1e-117">Child Elements</span></span>  
  
|<span data-ttu-id="18d1e-118">Élément</span><span class="sxs-lookup"><span data-stu-id="18d1e-118">Element</span></span>|<span data-ttu-id="18d1e-119">Description</span><span class="sxs-lookup"><span data-stu-id="18d1e-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="18d1e-120">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="18d1e-120">\<faultPropagationQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationquery.md)|<span data-ttu-id="18d1e-121">Requête utilisée pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="18d1e-121">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="18d1e-122">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="18d1e-122">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="18d1e-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="18d1e-123">Parent Elements</span></span>  
  
|<span data-ttu-id="18d1e-124">Élément</span><span class="sxs-lookup"><span data-stu-id="18d1e-124">Element</span></span>|<span data-ttu-id="18d1e-125">Description</span><span class="sxs-lookup"><span data-stu-id="18d1e-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="18d1e-126">\<workflow></span><span class="sxs-lookup"><span data-stu-id="18d1e-126">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="18d1e-127">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le **activityDefinitionId** propriété.</span><span class="sxs-lookup"><span data-stu-id="18d1e-127">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="18d1e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18d1e-128">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="18d1e-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="18d1e-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="18d1e-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="18d1e-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
