---
title: <bookmarkResumptionQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 226de75d-d25c-48d5-b069-4b7d80a6852b
ms.openlocfilehash: e43ba66e2c3ccfbb723b1eea8ef6774ad3f9f2aa
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59140034"
---
# <a name="bookmarkresumptionquery"></a><span data-ttu-id="4e9e9-101">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="4e9e9-101">\<bookmarkResumptionQuery></span></span>
<span data-ttu-id="4e9e9-102">Représente une requête qui permet d'effectuer le suivi de la reprise d'un signet dans une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="4e9e9-102">Represents a query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="4e9e9-103">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de reprise de signet.</span><span class="sxs-lookup"><span data-stu-id="4e9e9-103">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
 <span data-ttu-id="4e9e9-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="4e9e9-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="4e9e9-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="4e9e9-105">\<system.serviceModel></span></span>  
<span data-ttu-id="4e9e9-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="4e9e9-106">\<tracking></span></span>  
<span data-ttu-id="4e9e9-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="4e9e9-107">\<trackingProfile></span></span>  
<span data-ttu-id="4e9e9-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="4e9e9-108">\<workflow></span></span>  
<span data-ttu-id="4e9e9-109">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="4e9e9-109">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="4e9e9-110">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="4e9e9-110">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e9e9-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e9e9-111">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <bookmarkResumptionQueries>
        <bookmarkResumptionQuery name="String" />
      </bookmarkResumptionQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4e9e9-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4e9e9-112">Attributes and Elements</span></span>  
 <span data-ttu-id="4e9e9-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4e9e9-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4e9e9-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="4e9e9-114">Attributes</span></span>  
  
|<span data-ttu-id="4e9e9-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="4e9e9-115">Attribute</span></span>|<span data-ttu-id="4e9e9-116">Description</span><span class="sxs-lookup"><span data-stu-id="4e9e9-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4e9e9-117">name</span><span class="sxs-lookup"><span data-stu-id="4e9e9-117">name</span></span>|<span data-ttu-id="4e9e9-118">Chaîne qui spécifie le nom de l'enregistrement de signet auquel s'abonner.</span><span class="sxs-lookup"><span data-stu-id="4e9e9-118">A string that specifies the name of the bookmark record to subscribe to.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4e9e9-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4e9e9-119">Child Elements</span></span>  
 <span data-ttu-id="4e9e9-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4e9e9-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4e9e9-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4e9e9-121">Parent Elements</span></span>  
  
|<span data-ttu-id="4e9e9-122">Élément</span><span class="sxs-lookup"><span data-stu-id="4e9e9-122">Element</span></span>|<span data-ttu-id="4e9e9-123">Description</span><span class="sxs-lookup"><span data-stu-id="4e9e9-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4e9e9-124">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="4e9e9-124">\<bookmarkResumptionQueries></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/bookmarkresumptionqueries.md)|<span data-ttu-id="4e9e9-125">Représente une collection de requêtes qui permettent d’effectuer le suivi de la reprise d’un signet dans une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="4e9e9-125">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4e9e9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e9e9-126">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="4e9e9-127">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="4e9e9-127">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="4e9e9-128">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="4e9e9-128">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
