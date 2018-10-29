---
title: '&lt;customTrackingQueries&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: 14cfe47e-9935-4120-84f1-8f38de8ca4c1
ms.openlocfilehash: 060e2b5c8efd51f6245a39bd9562a69f0111fd41
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50202222"
---
# <a name="ltcustomtrackingqueriesgt-of-wcf"></a><span data-ttu-id="67ac3-102">&lt;customTrackingQueries&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="67ac3-102">&lt;customTrackingQueries&gt; of WCF</span></span>

<span data-ttu-id="67ac3-103">Représente une collection de requêtes permettant d’effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="67ac3-103">Represents a collection of queries that are used to track events that you define in your code activities.</span></span> <span data-ttu-id="67ac3-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de suivi personnalisés.</span><span class="sxs-lookup"><span data-stu-id="67ac3-104">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>  
  
 <span data-ttu-id="67ac3-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="67ac3-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>
  
<span data-ttu-id="67ac3-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="67ac3-106">\<system.serviceModel></span></span>  
<span data-ttu-id="67ac3-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="67ac3-107">\<tracking></span></span>  
<span data-ttu-id="67ac3-108">\<profils ></span><span class="sxs-lookup"><span data-stu-id="67ac3-108">\<profiles></span></span>  
<span data-ttu-id="67ac3-109">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="67ac3-109">\<trackingProfile></span></span>  
<span data-ttu-id="67ac3-110">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="67ac3-110">\<workflow></span></span>  
<span data-ttu-id="67ac3-111">\<customTrackingQueries ></span><span class="sxs-lookup"><span data-stu-id="67ac3-111">\<customTrackingQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="67ac3-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67ac3-112">Syntax</span></span>  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <customTrackingQueries>
          <customTrackingQuery activityName="String"
                               name="String"/>
        </customTrackingQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="67ac3-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="67ac3-113">Attributes and elements</span></span>

<span data-ttu-id="67ac3-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="67ac3-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="67ac3-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="67ac3-115">Attributes</span></span>

<span data-ttu-id="67ac3-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="67ac3-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="67ac3-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="67ac3-117">Child elements</span></span>
  
|<span data-ttu-id="67ac3-118">Élément</span><span class="sxs-lookup"><span data-stu-id="67ac3-118">Element</span></span>|<span data-ttu-id="67ac3-119">Description</span><span class="sxs-lookup"><span data-stu-id="67ac3-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="67ac3-120">\<customTrackingQuery ></span><span class="sxs-lookup"><span data-stu-id="67ac3-120">\<customTrackingQuery></span></span>](customtrackingquery-of-wcf.md)|<span data-ttu-id="67ac3-121">Requête qui permet d'effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="67ac3-121">A query that is used to track events that you define in your code activities.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="67ac3-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="67ac3-122">Parent elements</span></span>  
  
|<span data-ttu-id="67ac3-123">Élément</span><span class="sxs-lookup"><span data-stu-id="67ac3-123">Element</span></span>|<span data-ttu-id="67ac3-124">Description</span><span class="sxs-lookup"><span data-stu-id="67ac3-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="67ac3-125">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="67ac3-125">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="67ac3-126">Élément de configuration qui contient toutes les requêtes d'un flux de travail spécifique identifié par la propriété `activityDefinitionId`.</span><span class="sxs-lookup"><span data-stu-id="67ac3-126">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="67ac3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67ac3-127">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>       
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>       
- [<span data-ttu-id="67ac3-128">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="67ac3-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
- [<span data-ttu-id="67ac3-129">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="67ac3-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
