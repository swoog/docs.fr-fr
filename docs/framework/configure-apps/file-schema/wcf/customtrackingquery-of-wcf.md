---
title: <customTrackingQuery> de WCF
ms.date: 03/30/2017
ms.assetid: 164446ae-8440-4b67-b217-6786cfae1e01
ms.openlocfilehash: 0a5e7c034ce1ef12a8d7d5b1753e2e441e48e293
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55279485"
---
# <a name="customtrackingquery-of-wcf"></a><span data-ttu-id="3ff18-102">\<customTrackingQuery> of WCF</span><span class="sxs-lookup"><span data-stu-id="3ff18-102">\<customTrackingQuery> of WCF</span></span>

<span data-ttu-id="3ff18-103">Représente une requête qui est utilisée pour effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="3ff18-103">Represents a query that is used to track events that you define in your code activities.</span></span> <span data-ttu-id="3ff18-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de suivi personnalisés.</span><span class="sxs-lookup"><span data-stu-id="3ff18-104">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>

<span data-ttu-id="3ff18-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="3ff18-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="3ff18-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="3ff18-106">\<system.serviceModel></span></span>  
<span data-ttu-id="3ff18-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="3ff18-107">\<tracking></span></span>  
<span data-ttu-id="3ff18-108">\<profiles></span><span class="sxs-lookup"><span data-stu-id="3ff18-108">\<profiles></span></span>  
<span data-ttu-id="3ff18-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="3ff18-109">\<trackingProfile></span></span>  
<span data-ttu-id="3ff18-110">\<workflow></span><span class="sxs-lookup"><span data-stu-id="3ff18-110">\<workflow></span></span>  
<span data-ttu-id="3ff18-111">\<customTrackingQueries></span><span class="sxs-lookup"><span data-stu-id="3ff18-111">\<customTrackingQueries></span></span>  
<span data-ttu-id="3ff18-112">\<customTrackingQuery></span><span class="sxs-lookup"><span data-stu-id="3ff18-112">\<customTrackingQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3ff18-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ff18-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3ff18-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3ff18-114">Attributes and elements</span></span>  

<span data-ttu-id="3ff18-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3ff18-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3ff18-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ff18-116">Attributes</span></span>  
  
|<span data-ttu-id="3ff18-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="3ff18-117">Attribute</span></span>|<span data-ttu-id="3ff18-118">Description</span><span class="sxs-lookup"><span data-stu-id="3ff18-118">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="3ff18-119">Chaîne qui spécifie le nom de l'activité ayant généré l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="3ff18-119">A string that specifies the name of the activity that generated the tracking record.</span></span>|  
|`name`|<span data-ttu-id="3ff18-120">Chaîne qui spécifie le nom de l'enregistrement de suivi personnalisé émis.</span><span class="sxs-lookup"><span data-stu-id="3ff18-120">A string that specifies the name of the custom tracking record that is emitted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3ff18-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3ff18-121">Child elements</span></span>

<span data-ttu-id="3ff18-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3ff18-122">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="3ff18-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3ff18-123">Parent elements</span></span>

|<span data-ttu-id="3ff18-124">Élément</span><span class="sxs-lookup"><span data-stu-id="3ff18-124">Element</span></span>|<span data-ttu-id="3ff18-125">Description</span><span class="sxs-lookup"><span data-stu-id="3ff18-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3ff18-126">\<customTrackingQueries></span><span class="sxs-lookup"><span data-stu-id="3ff18-126">\<customTrackingQueries></span></span>](customtrackingqueries-of-wcf.md)|<span data-ttu-id="3ff18-127">Représente une collection de requêtes permettant d’effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="3ff18-127">Represents a collection of queries that are used to track events that you define in your code activities.</span></span>|
  
## <a name="see-also"></a><span data-ttu-id="3ff18-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ff18-128">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>
- [<span data-ttu-id="3ff18-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="3ff18-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="3ff18-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="3ff18-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
