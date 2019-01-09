---
title: '&lt;bookmarkResumptionQuery&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: 755a34f0-87c9-4a1e-ae4d-0fb8a6fbdc0e
ms.openlocfilehash: 6463404e17edff8eb1efe3f96e44b5b9997ffca3
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147809"
---
# <a name="ltbookmarkresumptionquerygt-of-wcf"></a><span data-ttu-id="af78a-102">&lt;bookmarkResumptionQuery&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="af78a-102">&lt;bookmarkResumptionQuery&gt; of WCF</span></span>

<span data-ttu-id="af78a-103">Représente une requête qui permet d'effectuer le suivi de la reprise d'un signet dans une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="af78a-103">Represents a query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="af78a-104">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de reprise de signet.</span><span class="sxs-lookup"><span data-stu-id="af78a-104">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
<span data-ttu-id="af78a-105">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="af78a-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>
  
<span data-ttu-id="af78a-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="af78a-106">\<system.serviceModel></span></span>  
<span data-ttu-id="af78a-107">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="af78a-107">\<tracking></span></span>  
<span data-ttu-id="af78a-108">\<profils ></span><span class="sxs-lookup"><span data-stu-id="af78a-108">\<profiles></span></span>  
<span data-ttu-id="af78a-109">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="af78a-109">\<trackingProfile></span></span>  
<span data-ttu-id="af78a-110">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="af78a-110">\<workflow></span></span>  
<span data-ttu-id="af78a-111">\<bookmarkResumptionQueries ></span><span class="sxs-lookup"><span data-stu-id="af78a-111">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="af78a-112">\<bookmarkResumptionQuery ></span><span class="sxs-lookup"><span data-stu-id="af78a-112">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="af78a-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af78a-113">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <bookmarkResumptionQueries>
          <bookmarkResumptionQuery name="String" />
        </bookmarkResumptionQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="af78a-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="af78a-114">Attributes and elements</span></span>

<span data-ttu-id="af78a-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="af78a-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="af78a-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="af78a-116">Attributes</span></span>  
  
|<span data-ttu-id="af78a-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="af78a-117">Attribute</span></span>|<span data-ttu-id="af78a-118">Description</span><span class="sxs-lookup"><span data-stu-id="af78a-118">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="af78a-119">Chaîne qui spécifie le nom de l'enregistrement de signet auquel s'abonner.</span><span class="sxs-lookup"><span data-stu-id="af78a-119">A string that specifies the name of the bookmark record to subscribe to.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="af78a-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="af78a-120">Child elements</span></span>

<span data-ttu-id="af78a-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="af78a-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="af78a-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="af78a-122">Parent elements</span></span>  
  
|<span data-ttu-id="af78a-123">Élément</span><span class="sxs-lookup"><span data-stu-id="af78a-123">Element</span></span>|<span data-ttu-id="af78a-124">Description</span><span class="sxs-lookup"><span data-stu-id="af78a-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="af78a-125">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="af78a-125">\<bookmarkResumptionQueries></span></span>](bookmarkresumptionqueries-of-wcf.md)|<span data-ttu-id="af78a-126">Représente une collection de requêtes qui permettent d’effectuer le suivi de la reprise d’un signet dans une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="af78a-126">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="af78a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af78a-127">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="af78a-128">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="af78a-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="af78a-129">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="af78a-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
