---
title: '&lt;Entrées&gt;'
ms.date: 03/30/2017
ms.assetid: 202e430c-c1b9-4343-abe2-ac78c181a3b7
ms.openlocfilehash: 33f98cb4b138307622a14463ce5a3008058b6e31
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587058"
---
# <a name="ltentriesgt"></a><span data-ttu-id="349de-102">&lt;Entrées&gt;</span><span class="sxs-lookup"><span data-stu-id="349de-102">&lt;entries&gt;</span></span>
<span data-ttu-id="349de-103">Entrée de routage qui contient des mappages entre les filtres de routage et les points de terminaison cibles vers lesquels envoyer des messages lorsque le filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="349de-103">A routing entry that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="349de-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="349de-104">\<system.serviceModel></span></span>  
<span data-ttu-id="349de-105">\<routing></span><span class="sxs-lookup"><span data-stu-id="349de-105">\<routing></span></span>  
<span data-ttu-id="349de-106">\<routingTables></span><span class="sxs-lookup"><span data-stu-id="349de-106">\<routingTables></span></span>  
<span data-ttu-id="349de-107">\<table></span><span class="sxs-lookup"><span data-stu-id="349de-107">\<table></span></span>  
<span data-ttu-id="349de-108">\<entries></span><span class="sxs-lookup"><span data-stu-id="349de-108">\<entries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="349de-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="349de-109">Syntax</span></span>  
  
```xml  
<routing>
  <filterTables>
    <filterTable name="String">
      <entries>
        <add backupList="String"
             endpointName="String"
             filterName="String"
             priority="Integer" />
      </entries>
    </filterTable>
  </filterTables>
</routing>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="349de-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="349de-110">Attributes and Elements</span></span>  
 <span data-ttu-id="349de-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="349de-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="349de-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="349de-112">Attributes</span></span>  
 <span data-ttu-id="349de-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="349de-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="349de-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="349de-114">Child Elements</span></span>  
  
|<span data-ttu-id="349de-115">Élément</span><span class="sxs-lookup"><span data-stu-id="349de-115">Element</span></span>|<span data-ttu-id="349de-116">Description</span><span class="sxs-lookup"><span data-stu-id="349de-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="349de-117">\<filtres></span><span class="sxs-lookup"><span data-stu-id="349de-117">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="349de-118">Mappe un filtre à un point de terminaison client précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="349de-118">Maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="349de-119">Les messages correspondant à ce filtre sont envoyés à cette destination.</span><span class="sxs-lookup"><span data-stu-id="349de-119">Messages matching this filter will be sent to this destination.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="349de-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="349de-120">Parent Elements</span></span>  
  
|<span data-ttu-id="349de-121">Élément</span><span class="sxs-lookup"><span data-stu-id="349de-121">Element</span></span>|<span data-ttu-id="349de-122">Description</span><span class="sxs-lookup"><span data-stu-id="349de-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="349de-123">\<routing></span><span class="sxs-lookup"><span data-stu-id="349de-123">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="349de-124">Section de configuration qui contient une table de routage.</span><span class="sxs-lookup"><span data-stu-id="349de-124">A configuration section that contains a routing table.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="349de-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="349de-125">See also</span></span>
- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>
