---
title: '&lt;faultPropagationQueries&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: d85f66a7-e7b0-4dbb-83cc-89fa06fc9161
ms.openlocfilehash: 1db99a8d80fad5c0eca93777d87047b43371d048
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50044409"
---
# <a name="ltfaultpropagationqueriesgt-of-wcf"></a><span data-ttu-id="d46e5-102">&lt;faultPropagationQueries&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="d46e5-102">&lt;faultPropagationQueries&gt; of WCF</span></span>

<span data-ttu-id="d46e5-103">Représente une collection de requêtes qui permettent d’effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="d46e5-103">Represents a collection of queries that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="d46e5-104">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="d46e5-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="d46e5-105">Vous devez utiliser cette requête pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="d46e5-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="d46e5-106">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements de propagation d'erreur.</span><span class="sxs-lookup"><span data-stu-id="d46e5-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
<span data-ttu-id="d46e5-107">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="d46e5-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="d46e5-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="d46e5-108">\<system.serviceModel></span></span>  
<span data-ttu-id="d46e5-109">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="d46e5-109">\<tracking></span></span>  
<span data-ttu-id="d46e5-110">\<profils ></span><span class="sxs-lookup"><span data-stu-id="d46e5-110">\<profiles></span></span>  
<span data-ttu-id="d46e5-111">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="d46e5-111">\<trackingProfile></span></span>  
<span data-ttu-id="d46e5-112">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="d46e5-112">\<workflow></span></span>  
<span data-ttu-id="d46e5-113">\<faultPropagationQueries ></span><span class="sxs-lookup"><span data-stu-id="d46e5-113">\<faultPropagationQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d46e5-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d46e5-114">Syntax</span></span>  
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="d46e5-115">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d46e5-115">Attributes and elements</span></span>

<span data-ttu-id="d46e5-116">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d46e5-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d46e5-117">Attributs</span><span class="sxs-lookup"><span data-stu-id="d46e5-117">Attributes</span></span>

<span data-ttu-id="d46e5-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d46e5-118">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d46e5-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d46e5-119">Child elements</span></span>

|<span data-ttu-id="d46e5-120">Élément</span><span class="sxs-lookup"><span data-stu-id="d46e5-120">Element</span></span>|<span data-ttu-id="d46e5-121">Description</span><span class="sxs-lookup"><span data-stu-id="d46e5-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d46e5-122">\<faultPropagationQuery ></span><span class="sxs-lookup"><span data-stu-id="d46e5-122">\<faultPropagationQuery></span></span>](faultpropagationquery-of-wcf.md)|<span data-ttu-id="d46e5-123">Requête utilisée pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="d46e5-123">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="d46e5-124">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="d46e5-124">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d46e5-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d46e5-125">Parent elements</span></span>  
  
|<span data-ttu-id="d46e5-126">Élément</span><span class="sxs-lookup"><span data-stu-id="d46e5-126">Element</span></span>|<span data-ttu-id="d46e5-127">Description</span><span class="sxs-lookup"><span data-stu-id="d46e5-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d46e5-128">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="d46e5-128">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="d46e5-129">Élément de configuration qui contient toutes les requêtes d'un flux de travail spécifique identifié par la propriété `activityDefinitionId`.</span><span class="sxs-lookup"><span data-stu-id="d46e5-129">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d46e5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d46e5-130">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="d46e5-131">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="d46e5-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="d46e5-132">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="d46e5-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
