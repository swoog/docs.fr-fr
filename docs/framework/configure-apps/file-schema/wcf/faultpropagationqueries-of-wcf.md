---
title: <faultPropagationQueries> de WCF
ms.date: 03/30/2017
ms.assetid: d85f66a7-e7b0-4dbb-83cc-89fa06fc9161
ms.openlocfilehash: bc016827c5bb243bc83dbb53c1eda7eec1bfd8c4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704009"
---
# <a name="faultpropagationqueries-of-wcf"></a><span data-ttu-id="ef6da-102">\<faultPropagationQueries > de WCF</span><span class="sxs-lookup"><span data-stu-id="ef6da-102">\<faultPropagationQueries> of WCF</span></span>

<span data-ttu-id="ef6da-103">Représente une collection de requêtes qui permettent d’effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="ef6da-103">Represents a collection of queries that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="ef6da-104">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="ef6da-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="ef6da-105">Vous devez utiliser cette requête pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="ef6da-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="ef6da-106">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements de propagation d'erreur.</span><span class="sxs-lookup"><span data-stu-id="ef6da-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
<span data-ttu-id="ef6da-107">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="ef6da-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="ef6da-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="ef6da-108">\<system.serviceModel></span></span>  
<span data-ttu-id="ef6da-109">\<tracking></span><span class="sxs-lookup"><span data-stu-id="ef6da-109">\<tracking></span></span>  
<span data-ttu-id="ef6da-110">\<profiles></span><span class="sxs-lookup"><span data-stu-id="ef6da-110">\<profiles></span></span>  
<span data-ttu-id="ef6da-111">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="ef6da-111">\<trackingProfile></span></span>  
<span data-ttu-id="ef6da-112">\<workflow></span><span class="sxs-lookup"><span data-stu-id="ef6da-112">\<workflow></span></span>  
<span data-ttu-id="ef6da-113">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="ef6da-113">\<faultPropagationQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ef6da-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef6da-114">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <faultPropagationQueries>
          <faultPropagationQuery faultSourceActivityName="String"
                                 faultHandlerActivityName="String"/>
        </faultPropagationQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ef6da-115">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ef6da-115">Attributes and elements</span></span>

<span data-ttu-id="ef6da-116">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ef6da-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef6da-117">Attributs</span><span class="sxs-lookup"><span data-stu-id="ef6da-117">Attributes</span></span>

<span data-ttu-id="ef6da-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ef6da-118">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef6da-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ef6da-119">Child elements</span></span>

|<span data-ttu-id="ef6da-120">Élément</span><span class="sxs-lookup"><span data-stu-id="ef6da-120">Element</span></span>|<span data-ttu-id="ef6da-121">Description</span><span class="sxs-lookup"><span data-stu-id="ef6da-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ef6da-122">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="ef6da-122">\<faultPropagationQuery></span></span>](faultpropagationquery-of-wcf.md)|<span data-ttu-id="ef6da-123">Requête utilisée pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="ef6da-123">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="ef6da-124">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="ef6da-124">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ef6da-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ef6da-125">Parent elements</span></span>  
  
|<span data-ttu-id="ef6da-126">Élément</span><span class="sxs-lookup"><span data-stu-id="ef6da-126">Element</span></span>|<span data-ttu-id="ef6da-127">Description</span><span class="sxs-lookup"><span data-stu-id="ef6da-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ef6da-128">\<workflow></span><span class="sxs-lookup"><span data-stu-id="ef6da-128">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="ef6da-129">Élément de configuration qui contient toutes les requêtes d'un flux de travail spécifique identifié par la propriété `activityDefinitionId`.</span><span class="sxs-lookup"><span data-stu-id="ef6da-129">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ef6da-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef6da-130">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="ef6da-131">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="ef6da-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="ef6da-132">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="ef6da-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
