---
title: '&lt;customTrackingQueries&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: 14cfe47e-9935-4120-84f1-8f38de8ca4c1
ms.openlocfilehash: 11ad4281d2925a48508c6a3e8258b0b1cd49a326
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32749684"
---
# <a name="ltcustomtrackingqueriesgt-of-wcf"></a><span data-ttu-id="3b958-102">&lt;customTrackingQueries&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="3b958-102">&lt;customTrackingQueries&gt; of WCF</span></span>
<span data-ttu-id="3b958-103">Représente une collection de requêtes permettant d’effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="3b958-103">Represents a collection of queries that are used to track events that you define in your code activities.</span></span> <span data-ttu-id="3b958-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de suivi personnalisés.</span><span class="sxs-lookup"><span data-stu-id="3b958-104">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>  
  
 <span data-ttu-id="3b958-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="3b958-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
 <span data-ttu-id="3b958-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="3b958-106">\<system.serviceModel></span></span>  
<span data-ttu-id="3b958-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="3b958-107">\<tracking></span></span>  
<span data-ttu-id="3b958-108">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="3b958-108">\<trackingProfile></span></span>  
<span data-ttu-id="3b958-109">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="3b958-109">\<workflow></span></span>  
<span data-ttu-id="3b958-110">\<customTrackingQueries ></span><span class="sxs-lookup"><span data-stu-id="3b958-110">\<customTrackingQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b958-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b958-111">Syntax</span></span>  
  
```xml
<tracking>   <trackingProfile name="Name">       <workflow>          <customTrackingQueries>             <customTrackingQuery activityName="String"                 name="String"/>          </customTrackingQueries>       </workflow>   </trackingProfile></tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3b958-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3b958-112">Attributes and Elements</span></span>  
 <span data-ttu-id="3b958-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3b958-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3b958-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="3b958-114">Attributes</span></span>  
 <span data-ttu-id="3b958-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3b958-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="3b958-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3b958-116">Child Elements</span></span>  
  
|<span data-ttu-id="3b958-117">Élément</span><span class="sxs-lookup"><span data-stu-id="3b958-117">Element</span></span>|<span data-ttu-id="3b958-118">Description</span><span class="sxs-lookup"><span data-stu-id="3b958-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3b958-119">\<customTrackingQuery ></span><span class="sxs-lookup"><span data-stu-id="3b958-119">\<customTrackingQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/customtrackingquery.md)|<span data-ttu-id="3b958-120">Requête qui permet d'effectuer le suivi des événements que vous définissez dans vos activités de code.</span><span class="sxs-lookup"><span data-stu-id="3b958-120">A query that is used to track events that you define in your code activities.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="3b958-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3b958-121">Parent Elements</span></span>  
  
|<span data-ttu-id="3b958-122">Élément</span><span class="sxs-lookup"><span data-stu-id="3b958-122">Element</span></span>|<span data-ttu-id="3b958-123">Description</span><span class="sxs-lookup"><span data-stu-id="3b958-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3b958-124">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="3b958-124">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="3b958-125">Élément de configuration qui contient toutes les requêtes d'un flux de travail spécifique identifié par la propriété `activityDefinitionId`.</span><span class="sxs-lookup"><span data-stu-id="3b958-125">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3b958-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b958-126">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="3b958-127">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="3b958-127">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="3b958-128">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="3b958-128">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
