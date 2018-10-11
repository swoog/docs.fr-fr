---
title: '&lt;bookmarkResumptionQuery&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: 755a34f0-87c9-4a1e-ae4d-0fb8a6fbdc0e
ms.openlocfilehash: 07215347da19a05d5915296668d990853fdae646
ms.sourcegitcommit: 2eb5ca4956231c1a0efd34b6a9cab6153a5438af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49087789"
---
# <a name="ltbookmarkresumptionquerygt-of-wcf"></a><span data-ttu-id="dac96-102">&lt;bookmarkResumptionQuery&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="dac96-102">&lt;bookmarkResumptionQuery&gt; of WCF</span></span>
<span data-ttu-id="dac96-103">Représente une requête qui permet d'effectuer le suivi de la reprise d'un signet dans une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="dac96-103">Represents a query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="dac96-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de reprise de signet.</span><span class="sxs-lookup"><span data-stu-id="dac96-104">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
 <span data-ttu-id="dac96-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="dac96-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
 <span data-ttu-id="dac96-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="dac96-106">\<system.serviceModel></span></span>  
<span data-ttu-id="dac96-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="dac96-107">\<tracking></span></span>  
<span data-ttu-id="dac96-108">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="dac96-108">\<trackingProfile></span></span>  
<span data-ttu-id="dac96-109">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="dac96-109">\<workflow></span></span>  
<span data-ttu-id="dac96-110">\<bookmarkResumptionQueries ></span><span class="sxs-lookup"><span data-stu-id="dac96-110">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="dac96-111">\<bookmarkResumptionQuery ></span><span class="sxs-lookup"><span data-stu-id="dac96-111">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dac96-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dac96-112">Syntax</span></span>  
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="dac96-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="dac96-113">Attributes and Elements</span></span>  
 <span data-ttu-id="dac96-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="dac96-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dac96-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="dac96-115">Attributes</span></span>  
  
|<span data-ttu-id="dac96-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="dac96-116">Attribute</span></span>|<span data-ttu-id="dac96-117">Description</span><span class="sxs-lookup"><span data-stu-id="dac96-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="dac96-118">name</span><span class="sxs-lookup"><span data-stu-id="dac96-118">name</span></span>|<span data-ttu-id="dac96-119">Chaîne qui spécifie le nom de l'enregistrement de signet auquel s'abonner.</span><span class="sxs-lookup"><span data-stu-id="dac96-119">A string that specifies the name of the bookmark record to subscribe to.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dac96-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dac96-120">Child Elements</span></span>  
 <span data-ttu-id="dac96-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dac96-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dac96-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="dac96-122">Parent Elements</span></span>  
  
|<span data-ttu-id="dac96-123">Élément</span><span class="sxs-lookup"><span data-stu-id="dac96-123">Element</span></span>|<span data-ttu-id="dac96-124">Description</span><span class="sxs-lookup"><span data-stu-id="dac96-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dac96-125">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="dac96-125">\<bookmarkResumptionQueries></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/bookmarkresumptionqueries.md)|<span data-ttu-id="dac96-126">Représente une collection de requêtes qui permettent d’effectuer le suivi de la reprise d’un signet dans une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="dac96-126">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="dac96-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dac96-127">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="dac96-128">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="dac96-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="dac96-129">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="dac96-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
