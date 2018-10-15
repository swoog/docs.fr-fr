---
title: '&lt;customTrackingQuery&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: 164446ae-8440-4b67-b217-6786cfae1e01
ms.openlocfilehash: e13064afbd9f5dbc8d7216eb384001e1e005785c
ms.sourcegitcommit: d88024e6d6d8b242feae5f4007a709379355aa24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2018
ms.locfileid: "49316231"
---
# <a name="ltcustomtrackingquerygt-of-wcf"></a><span data-ttu-id="00ddb-102">&lt;customTrackingQuery&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="00ddb-102">&lt;customTrackingQuery&gt; of WCF</span></span>

<span data-ttu-id="00ddb-103">Représente une requête qui est utilisée pour effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="00ddb-103">Represents a query that is used to track events that you define in your code activities.</span></span> <span data-ttu-id="00ddb-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de suivi personnalisés.</span><span class="sxs-lookup"><span data-stu-id="00ddb-104">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>

<span data-ttu-id="00ddb-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="00ddb-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="00ddb-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="00ddb-106">\<system.serviceModel></span></span>  
<span data-ttu-id="00ddb-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="00ddb-107">\<tracking></span></span>  
<span data-ttu-id="00ddb-108">\<profils ></span><span class="sxs-lookup"><span data-stu-id="00ddb-108">\<profiles></span></span>  
<span data-ttu-id="00ddb-109">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="00ddb-109">\<trackingProfile></span></span>  
<span data-ttu-id="00ddb-110">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="00ddb-110">\<workflow></span></span>  
<span data-ttu-id="00ddb-111">\<customTrackingQueries ></span><span class="sxs-lookup"><span data-stu-id="00ddb-111">\<customTrackingQueries></span></span>  
<span data-ttu-id="00ddb-112">\<customTrackingQuery ></span><span class="sxs-lookup"><span data-stu-id="00ddb-112">\<customTrackingQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00ddb-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00ddb-113">Syntax</span></span>  
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="00ddb-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="00ddb-114">Attributes and elements</span></span>  

<span data-ttu-id="00ddb-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="00ddb-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="00ddb-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="00ddb-116">Attributes</span></span>  
  
|<span data-ttu-id="00ddb-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="00ddb-117">Attribute</span></span>|<span data-ttu-id="00ddb-118">Description</span><span class="sxs-lookup"><span data-stu-id="00ddb-118">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="00ddb-119">Chaîne qui spécifie le nom de l'activité ayant généré l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="00ddb-119">A string that specifies the name of the activity that generated the tracking record.</span></span>|  
|`name`|<span data-ttu-id="00ddb-120">Chaîne qui spécifie le nom de l'enregistrement de suivi personnalisé émis.</span><span class="sxs-lookup"><span data-stu-id="00ddb-120">A string that specifies the name of the custom tracking record that is emitted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="00ddb-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="00ddb-121">Child elements</span></span>

<span data-ttu-id="00ddb-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="00ddb-122">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="00ddb-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="00ddb-123">Parent elements</span></span>

|<span data-ttu-id="00ddb-124">Élément</span><span class="sxs-lookup"><span data-stu-id="00ddb-124">Element</span></span>|<span data-ttu-id="00ddb-125">Description</span><span class="sxs-lookup"><span data-stu-id="00ddb-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="00ddb-126">\<customTrackingQueries></span><span class="sxs-lookup"><span data-stu-id="00ddb-126">\<customTrackingQueries></span></span>](customtrackingqueries-of-wcf.md)|<span data-ttu-id="00ddb-127">Représente une collection de requêtes permettant d’effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="00ddb-127">Represents a collection of queries that are used to track events that you define in your code activities.</span></span>|
  
## <a name="see-also"></a><span data-ttu-id="00ddb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00ddb-128">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>
- [<span data-ttu-id="00ddb-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="00ddb-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="00ddb-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="00ddb-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
