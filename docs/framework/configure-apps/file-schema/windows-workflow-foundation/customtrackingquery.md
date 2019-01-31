---
title: <customTrackingQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 4e108e89-1132-46b7-868a-c7f5c69dc89f
ms.openlocfilehash: 4e525bc4c77649a6c6d70ddb2408b6ecce4a0f09
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55263761"
---
# <a name="customtrackingquery"></a><span data-ttu-id="714dd-101">\<customTrackingQuery></span><span class="sxs-lookup"><span data-stu-id="714dd-101">\<customTrackingQuery></span></span>
<span data-ttu-id="714dd-102">Représente une collection de requêtes permettant d’effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="714dd-102">Represents a collection of queries that are used to track events that you define in your code activities.</span></span> <span data-ttu-id="714dd-103">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de suivi personnalisés.</span><span class="sxs-lookup"><span data-stu-id="714dd-103">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>  
  
 <span data-ttu-id="714dd-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="714dd-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="714dd-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="714dd-105">\<system.serviceModel></span></span>  
<span data-ttu-id="714dd-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="714dd-106">\<tracking></span></span>  
<span data-ttu-id="714dd-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="714dd-107">\<trackingProfile></span></span>  
<span data-ttu-id="714dd-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="714dd-108">\<workflow></span></span>  
<span data-ttu-id="714dd-109">\<customTrackingQueries></span><span class="sxs-lookup"><span data-stu-id="714dd-109">\<customTrackingQueries></span></span>  
<span data-ttu-id="714dd-110">\<customTrackingQuery></span><span class="sxs-lookup"><span data-stu-id="714dd-110">\<customTrackingQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="714dd-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="714dd-111">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="714dd-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="714dd-112">Attributes and Elements</span></span>  
 <span data-ttu-id="714dd-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="714dd-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="714dd-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="714dd-114">Attributes</span></span>  
  
|<span data-ttu-id="714dd-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="714dd-115">Attribute</span></span>|<span data-ttu-id="714dd-116">Description</span><span class="sxs-lookup"><span data-stu-id="714dd-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="714dd-117">activityName</span><span class="sxs-lookup"><span data-stu-id="714dd-117">activityName</span></span>|<span data-ttu-id="714dd-118">Chaîne qui spécifie le nom de l'activité ayant généré l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="714dd-118">A string that specifies the name of the activity that generated the tracking record.</span></span>|  
|<span data-ttu-id="714dd-119">name</span><span class="sxs-lookup"><span data-stu-id="714dd-119">name</span></span>|<span data-ttu-id="714dd-120">Chaîne qui spécifie le nom de l'enregistrement de suivi personnalisé émis.</span><span class="sxs-lookup"><span data-stu-id="714dd-120">A string that specifies the name of the custom tracking record that is emitted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="714dd-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="714dd-121">Child Elements</span></span>  
 <span data-ttu-id="714dd-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="714dd-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="714dd-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="714dd-123">Parent Elements</span></span>  
  
|<span data-ttu-id="714dd-124">Élément</span><span class="sxs-lookup"><span data-stu-id="714dd-124">Element</span></span>|<span data-ttu-id="714dd-125">Description</span><span class="sxs-lookup"><span data-stu-id="714dd-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="714dd-126">\<customTrackingQuery></span><span class="sxs-lookup"><span data-stu-id="714dd-126">\<customTrackingQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/customtrackingquery.md)|<span data-ttu-id="714dd-127">Requête qui permet d'effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="714dd-127">A query that is used to track events that you define in your code activities.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="714dd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="714dd-128">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>
- [<span data-ttu-id="714dd-129">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="714dd-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="714dd-130">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="714dd-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
