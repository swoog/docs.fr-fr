---
title: <customTrackingQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 4e9e732d-911d-45a3-a569-4b5e9cd1ffbe
ms.openlocfilehash: a4689e55962cd32d738682129aaa0612a4684384
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55264635"
---
# <a name="customtrackingqueries"></a><span data-ttu-id="4ae5b-101">\<customTrackingQueries></span><span class="sxs-lookup"><span data-stu-id="4ae5b-101">\<customTrackingQueries></span></span>
<span data-ttu-id="4ae5b-102">Représente une collection de requêtes permettant d’effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="4ae5b-102">Represents a collection of queries that are used to track events that you define in your code activities.</span></span> <span data-ttu-id="4ae5b-103">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de suivi personnalisés.</span><span class="sxs-lookup"><span data-stu-id="4ae5b-103">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>  
  
 <span data-ttu-id="4ae5b-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="4ae5b-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="4ae5b-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="4ae5b-105">\<system.serviceModel></span></span>  
<span data-ttu-id="4ae5b-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="4ae5b-106">\<tracking></span></span>  
<span data-ttu-id="4ae5b-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="4ae5b-107">\<trackingProfile></span></span>  
<span data-ttu-id="4ae5b-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="4ae5b-108">\<workflow></span></span>  
<span data-ttu-id="4ae5b-109">\<customTrackingQueries></span><span class="sxs-lookup"><span data-stu-id="4ae5b-109">\<customTrackingQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ae5b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ae5b-110">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <customTrackingQueries>
        <customTrackingQuery activityName="String" 
                             name="String" />
      </customTrackingQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4ae5b-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4ae5b-111">Attributes and Elements</span></span>  
 <span data-ttu-id="4ae5b-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4ae5b-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4ae5b-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="4ae5b-113">Attributes</span></span>  
 <span data-ttu-id="4ae5b-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4ae5b-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4ae5b-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4ae5b-115">Child Elements</span></span>  
  
|<span data-ttu-id="4ae5b-116">Élément</span><span class="sxs-lookup"><span data-stu-id="4ae5b-116">Element</span></span>|<span data-ttu-id="4ae5b-117">Description</span><span class="sxs-lookup"><span data-stu-id="4ae5b-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4ae5b-118">\<customTrackingQuery></span><span class="sxs-lookup"><span data-stu-id="4ae5b-118">\<customTrackingQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/customtrackingquery.md)|<span data-ttu-id="4ae5b-119">Requête qui permet d'effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="4ae5b-119">A query that is used to track events that you define in your code activities.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4ae5b-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4ae5b-120">Parent Elements</span></span>  
  
|<span data-ttu-id="4ae5b-121">Élément</span><span class="sxs-lookup"><span data-stu-id="4ae5b-121">Element</span></span>|<span data-ttu-id="4ae5b-122">Description</span><span class="sxs-lookup"><span data-stu-id="4ae5b-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4ae5b-123">\<workflow></span><span class="sxs-lookup"><span data-stu-id="4ae5b-123">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="4ae5b-124">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le **activityDefinitionId** propriété.</span><span class="sxs-lookup"><span data-stu-id="4ae5b-124">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4ae5b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ae5b-125">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>
- [<span data-ttu-id="4ae5b-126">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="4ae5b-126">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="4ae5b-127">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="4ae5b-127">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
