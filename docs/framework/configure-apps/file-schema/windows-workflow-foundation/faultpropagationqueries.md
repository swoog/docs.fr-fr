---
title: '&lt;faultPropagationQueries&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 00ff90ae-ebe0-4c85-a93f-61557288d0a3
ms.openlocfilehash: 5fd6ffc9560247089c7fbb60b0e5a7d3a417ea6f
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32755147"
---
# <a name="ltfaultpropagationqueriesgt"></a><span data-ttu-id="20308-102">&lt;faultPropagationQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="20308-102">&lt;faultPropagationQueries&gt;</span></span>
<span data-ttu-id="20308-103">Représente une collection de requêtes qui permettent d’effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="20308-103">Represents a collection of queries that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="20308-104">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="20308-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="20308-105">Vous devez utiliser cette requête pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="20308-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="20308-106">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements de propagation d'erreur.</span><span class="sxs-lookup"><span data-stu-id="20308-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
 <span data-ttu-id="20308-107">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="20308-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="20308-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="20308-108">\<system.serviceModel></span></span>  
<span data-ttu-id="20308-109">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="20308-109">\<tracking></span></span>  
<span data-ttu-id="20308-110">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="20308-110">\<trackingProfile></span></span>  
<span data-ttu-id="20308-111">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="20308-111">\<workflow></span></span>  
<span data-ttu-id="20308-112">\<faultPropagationQueries ></span><span class="sxs-lookup"><span data-stu-id="20308-112">\<faultPropagationQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20308-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20308-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="20308-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="20308-114">Attributes and Elements</span></span>  
 <span data-ttu-id="20308-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="20308-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="20308-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="20308-116">Attributes</span></span>  
 <span data-ttu-id="20308-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="20308-117">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="20308-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="20308-118">Child Elements</span></span>  
  
|<span data-ttu-id="20308-119">Élément</span><span class="sxs-lookup"><span data-stu-id="20308-119">Element</span></span>|<span data-ttu-id="20308-120">Description</span><span class="sxs-lookup"><span data-stu-id="20308-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="20308-121">\<faultPropagationQuery ></span><span class="sxs-lookup"><span data-stu-id="20308-121">\<faultPropagationQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationquery.md)|<span data-ttu-id="20308-122">Requête utilisée pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="20308-122">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="20308-123">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="20308-123">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="20308-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="20308-124">Parent Elements</span></span>  
  
|<span data-ttu-id="20308-125">Élément</span><span class="sxs-lookup"><span data-stu-id="20308-125">Element</span></span>|<span data-ttu-id="20308-126">Description</span><span class="sxs-lookup"><span data-stu-id="20308-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="20308-127">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="20308-127">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="20308-128">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le **activityDefinitionId** propriété.</span><span class="sxs-lookup"><span data-stu-id="20308-128">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="20308-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20308-129">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElementCollection?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="20308-130">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="20308-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="20308-131">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="20308-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
