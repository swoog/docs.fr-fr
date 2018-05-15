---
title: '&lt;Entrées&gt;'
ms.date: 03/30/2017
ms.assetid: 202e430c-c1b9-4343-abe2-ac78c181a3b7
ms.openlocfilehash: b9cc7f7736ffefaca68a0f197bd064a99c4dca9a
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltentriesgt"></a><span data-ttu-id="a1eff-102">&lt;Entrées&gt;</span><span class="sxs-lookup"><span data-stu-id="a1eff-102">&lt;entries&gt;</span></span>
<span data-ttu-id="a1eff-103">Entrée de routage qui contient des mappages entre les filtres de routage et les points de terminaison cibles vers lesquels envoyer des messages lorsque le filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="a1eff-103">A routing entry that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="a1eff-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="a1eff-104">\<system.serviceModel></span></span>  
<span data-ttu-id="a1eff-105">\<routage ></span><span class="sxs-lookup"><span data-stu-id="a1eff-105">\<routing></span></span>  
<span data-ttu-id="a1eff-106">\<routingTables ></span><span class="sxs-lookup"><span data-stu-id="a1eff-106">\<routingTables></span></span>  
<span data-ttu-id="a1eff-107">\<table ></span><span class="sxs-lookup"><span data-stu-id="a1eff-107">\<table></span></span>  
<span data-ttu-id="a1eff-108">\<entrées ></span><span class="sxs-lookup"><span data-stu-id="a1eff-108">\<entries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1eff-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1eff-109">Syntax</span></span>  
  
```xml
   <routing>      <filterTables>        <filterTable name="String">          <entries>            <add backupList="String"                 endpointName="String"                  filterName="String"                  priority="Integer" />          </entries>        </table>      </routingTables></routing>  
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a1eff-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a1eff-110">Attributes and Elements</span></span>  
 <span data-ttu-id="a1eff-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a1eff-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a1eff-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="a1eff-112">Attributes</span></span>  
 <span data-ttu-id="a1eff-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a1eff-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="a1eff-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a1eff-114">Child Elements</span></span>  
  
|<span data-ttu-id="a1eff-115">Élément</span><span class="sxs-lookup"><span data-stu-id="a1eff-115">Element</span></span>|<span data-ttu-id="a1eff-116">Description</span><span class="sxs-lookup"><span data-stu-id="a1eff-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a1eff-117">\<filtres ></span><span class="sxs-lookup"><span data-stu-id="a1eff-117">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="a1eff-118">Mappe un filtre à un point de terminaison client précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="a1eff-118">Maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="a1eff-119">Les messages correspondant à ce filtre sont envoyés à cette destination.</span><span class="sxs-lookup"><span data-stu-id="a1eff-119">Messages matching this filter will be sent to this destination.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a1eff-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a1eff-120">Parent Elements</span></span>  
  
|<span data-ttu-id="a1eff-121">Élément</span><span class="sxs-lookup"><span data-stu-id="a1eff-121">Element</span></span>|<span data-ttu-id="a1eff-122">Description</span><span class="sxs-lookup"><span data-stu-id="a1eff-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a1eff-123">\<routage ></span><span class="sxs-lookup"><span data-stu-id="a1eff-123">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="a1eff-124">Section de configuration qui contient une table de routage.</span><span class="sxs-lookup"><span data-stu-id="a1eff-124">A configuration section that contains a routing table.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a1eff-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1eff-125">See Also</span></span>  
 <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>       
 <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>    
