---
title: '&lt;bookmarkResumptionQuery&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 226de75d-d25c-48d5-b069-4b7d80a6852b
ms.openlocfilehash: a5eb00d1e094484e3ec01e0db18719ec50e4b953
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515065"
---
# <a name="ltbookmarkresumptionquerygt"></a><span data-ttu-id="dbaa2-102">&lt;bookmarkResumptionQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="dbaa2-102">&lt;bookmarkResumptionQuery&gt;</span></span>
<span data-ttu-id="dbaa2-103">Représente une requête qui permet d'effectuer le suivi de la reprise d'un signet dans une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="dbaa2-103">Represents a query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="dbaa2-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de reprise de signet.</span><span class="sxs-lookup"><span data-stu-id="dbaa2-104">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
 <span data-ttu-id="dbaa2-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="dbaa2-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="dbaa2-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="dbaa2-106">\<system.serviceModel></span></span>  
<span data-ttu-id="dbaa2-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="dbaa2-107">\<tracking></span></span>  
<span data-ttu-id="dbaa2-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="dbaa2-108">\<trackingProfile></span></span>  
<span data-ttu-id="dbaa2-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="dbaa2-109">\<workflow></span></span>  
<span data-ttu-id="dbaa2-110">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="dbaa2-110">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="dbaa2-111">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="dbaa2-111">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dbaa2-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbaa2-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dbaa2-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="dbaa2-113">Attributes and Elements</span></span>  
 <span data-ttu-id="dbaa2-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="dbaa2-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dbaa2-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="dbaa2-115">Attributes</span></span>  
  
|<span data-ttu-id="dbaa2-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="dbaa2-116">Attribute</span></span>|<span data-ttu-id="dbaa2-117">Description</span><span class="sxs-lookup"><span data-stu-id="dbaa2-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="dbaa2-118">name</span><span class="sxs-lookup"><span data-stu-id="dbaa2-118">name</span></span>|<span data-ttu-id="dbaa2-119">Chaîne qui spécifie le nom de l'enregistrement de signet auquel s'abonner.</span><span class="sxs-lookup"><span data-stu-id="dbaa2-119">A string that specifies the name of the bookmark record to subscribe to.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dbaa2-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dbaa2-120">Child Elements</span></span>  
 <span data-ttu-id="dbaa2-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dbaa2-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dbaa2-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="dbaa2-122">Parent Elements</span></span>  
  
|<span data-ttu-id="dbaa2-123">Élément</span><span class="sxs-lookup"><span data-stu-id="dbaa2-123">Element</span></span>|<span data-ttu-id="dbaa2-124">Description</span><span class="sxs-lookup"><span data-stu-id="dbaa2-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dbaa2-125">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="dbaa2-125">\<bookmarkResumptionQueries></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/bookmarkresumptionqueries.md)|<span data-ttu-id="dbaa2-126">Représente une collection de requêtes qui permettent d’effectuer le suivi de la reprise d’un signet dans une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="dbaa2-126">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="dbaa2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbaa2-127">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="dbaa2-128">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="dbaa2-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="dbaa2-129">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="dbaa2-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
