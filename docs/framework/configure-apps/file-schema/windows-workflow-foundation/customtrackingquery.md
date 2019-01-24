---
title: '&lt;customTrackingQuery&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 4e108e89-1132-46b7-868a-c7f5c69dc89f
ms.openlocfilehash: 9ee5a4a25d379eafb936098597df1ec61ff09f0c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54725855"
---
# <a name="ltcustomtrackingquerygt"></a><span data-ttu-id="84e3c-102">&lt;customTrackingQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="84e3c-102">&lt;customTrackingQuery&gt;</span></span>
<span data-ttu-id="84e3c-103">Représente une collection de requêtes permettant d’effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="84e3c-103">Represents a collection of queries that are used to track events that you define in your code activities.</span></span> <span data-ttu-id="84e3c-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de suivi personnalisés.</span><span class="sxs-lookup"><span data-stu-id="84e3c-104">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>  
  
 <span data-ttu-id="84e3c-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="84e3c-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="84e3c-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="84e3c-106">\<system.serviceModel></span></span>  
<span data-ttu-id="84e3c-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="84e3c-107">\<tracking></span></span>  
<span data-ttu-id="84e3c-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="84e3c-108">\<trackingProfile></span></span>  
<span data-ttu-id="84e3c-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="84e3c-109">\<workflow></span></span>  
<span data-ttu-id="84e3c-110">\<customTrackingQueries></span><span class="sxs-lookup"><span data-stu-id="84e3c-110">\<customTrackingQueries></span></span>  
<span data-ttu-id="84e3c-111">\<customTrackingQuery></span><span class="sxs-lookup"><span data-stu-id="84e3c-111">\<customTrackingQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84e3c-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84e3c-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="84e3c-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="84e3c-113">Attributes and Elements</span></span>  
 <span data-ttu-id="84e3c-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="84e3c-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="84e3c-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="84e3c-115">Attributes</span></span>  
  
|<span data-ttu-id="84e3c-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="84e3c-116">Attribute</span></span>|<span data-ttu-id="84e3c-117">Description</span><span class="sxs-lookup"><span data-stu-id="84e3c-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="84e3c-118">activityName</span><span class="sxs-lookup"><span data-stu-id="84e3c-118">activityName</span></span>|<span data-ttu-id="84e3c-119">Chaîne qui spécifie le nom de l'activité ayant généré l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="84e3c-119">A string that specifies the name of the activity that generated the tracking record.</span></span>|  
|<span data-ttu-id="84e3c-120">name</span><span class="sxs-lookup"><span data-stu-id="84e3c-120">name</span></span>|<span data-ttu-id="84e3c-121">Chaîne qui spécifie le nom de l'enregistrement de suivi personnalisé émis.</span><span class="sxs-lookup"><span data-stu-id="84e3c-121">A string that specifies the name of the custom tracking record that is emitted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="84e3c-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="84e3c-122">Child Elements</span></span>  
 <span data-ttu-id="84e3c-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="84e3c-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="84e3c-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="84e3c-124">Parent Elements</span></span>  
  
|<span data-ttu-id="84e3c-125">Élément</span><span class="sxs-lookup"><span data-stu-id="84e3c-125">Element</span></span>|<span data-ttu-id="84e3c-126">Description</span><span class="sxs-lookup"><span data-stu-id="84e3c-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="84e3c-127">\<customTrackingQuery></span><span class="sxs-lookup"><span data-stu-id="84e3c-127">\<customTrackingQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/customtrackingquery.md)|<span data-ttu-id="84e3c-128">Requête qui permet d'effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="84e3c-128">A query that is used to track events that you define in your code activities.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="84e3c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84e3c-129">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>
- [<span data-ttu-id="84e3c-130">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="84e3c-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="84e3c-131">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="84e3c-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
