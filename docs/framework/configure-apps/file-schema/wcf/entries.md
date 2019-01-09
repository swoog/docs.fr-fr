---
title: '&lt;Entrées&gt;'
ms.date: 03/30/2017
ms.assetid: 202e430c-c1b9-4343-abe2-ac78c181a3b7
ms.openlocfilehash: 8c442990ee736c17b71b625e06d961230a8ceed2
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146431"
---
# <a name="ltentriesgt"></a><span data-ttu-id="622fc-102">&lt;Entrées&gt;</span><span class="sxs-lookup"><span data-stu-id="622fc-102">&lt;entries&gt;</span></span>
<span data-ttu-id="622fc-103">Entrée de routage qui contient des mappages entre les filtres de routage et les points de terminaison cibles vers lesquels envoyer des messages lorsque le filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="622fc-103">A routing entry that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="622fc-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="622fc-104">\<system.serviceModel></span></span>  
<span data-ttu-id="622fc-105">\<routage ></span><span class="sxs-lookup"><span data-stu-id="622fc-105">\<routing></span></span>  
<span data-ttu-id="622fc-106">\<routingTables ></span><span class="sxs-lookup"><span data-stu-id="622fc-106">\<routingTables></span></span>  
<span data-ttu-id="622fc-107">\<table ></span><span class="sxs-lookup"><span data-stu-id="622fc-107">\<table></span></span>  
<span data-ttu-id="622fc-108">\<entrées ></span><span class="sxs-lookup"><span data-stu-id="622fc-108">\<entries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="622fc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="622fc-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="622fc-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="622fc-110">Attributes and Elements</span></span>  
 <span data-ttu-id="622fc-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="622fc-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="622fc-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="622fc-112">Attributes</span></span>  
 <span data-ttu-id="622fc-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="622fc-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="622fc-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="622fc-114">Child Elements</span></span>  
  
|<span data-ttu-id="622fc-115">Élément</span><span class="sxs-lookup"><span data-stu-id="622fc-115">Element</span></span>|<span data-ttu-id="622fc-116">Description</span><span class="sxs-lookup"><span data-stu-id="622fc-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="622fc-117">\<filtres></span><span class="sxs-lookup"><span data-stu-id="622fc-117">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="622fc-118">Mappe un filtre à un point de terminaison client précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="622fc-118">Maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="622fc-119">Les messages correspondant à ce filtre sont envoyés à cette destination.</span><span class="sxs-lookup"><span data-stu-id="622fc-119">Messages matching this filter will be sent to this destination.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="622fc-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="622fc-120">Parent Elements</span></span>  
  
|<span data-ttu-id="622fc-121">Élément</span><span class="sxs-lookup"><span data-stu-id="622fc-121">Element</span></span>|<span data-ttu-id="622fc-122">Description</span><span class="sxs-lookup"><span data-stu-id="622fc-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="622fc-123">\<routage ></span><span class="sxs-lookup"><span data-stu-id="622fc-123">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="622fc-124">Section de configuration qui contient une table de routage.</span><span class="sxs-lookup"><span data-stu-id="622fc-124">A configuration section that contains a routing table.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="622fc-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="622fc-125">See Also</span></span>  
 <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>       
 <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>    
