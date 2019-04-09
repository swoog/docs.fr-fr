---
title: <entries>
ms.date: 03/30/2017
ms.assetid: 202e430c-c1b9-4343-abe2-ac78c181a3b7
ms.openlocfilehash: 5561cf61cef2258ec61bd32770538add1c69f5c1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59201791"
---
# <a name="entries"></a><span data-ttu-id="6fe79-101">\<entries></span><span class="sxs-lookup"><span data-stu-id="6fe79-101">\<entries></span></span>
<span data-ttu-id="6fe79-102">Entrée de routage qui contient des mappages entre les filtres de routage et les points de terminaison cibles vers lesquels envoyer des messages lorsque le filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="6fe79-102">A routing entry that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="6fe79-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="6fe79-103">\<system.serviceModel></span></span>  
<span data-ttu-id="6fe79-104">\<routing></span><span class="sxs-lookup"><span data-stu-id="6fe79-104">\<routing></span></span>  
<span data-ttu-id="6fe79-105">\<routingTables></span><span class="sxs-lookup"><span data-stu-id="6fe79-105">\<routingTables></span></span>  
<span data-ttu-id="6fe79-106">\<table></span><span class="sxs-lookup"><span data-stu-id="6fe79-106">\<table></span></span>  
<span data-ttu-id="6fe79-107">\<entries></span><span class="sxs-lookup"><span data-stu-id="6fe79-107">\<entries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6fe79-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fe79-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6fe79-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6fe79-109">Attributes and Elements</span></span>  
 <span data-ttu-id="6fe79-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6fe79-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6fe79-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="6fe79-111">Attributes</span></span>  
 <span data-ttu-id="6fe79-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6fe79-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="6fe79-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6fe79-113">Child Elements</span></span>  
  
|<span data-ttu-id="6fe79-114">Élément</span><span class="sxs-lookup"><span data-stu-id="6fe79-114">Element</span></span>|<span data-ttu-id="6fe79-115">Description</span><span class="sxs-lookup"><span data-stu-id="6fe79-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6fe79-116">\<filters></span><span class="sxs-lookup"><span data-stu-id="6fe79-116">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="6fe79-117">Mappe un filtre à un point de terminaison client précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="6fe79-117">Maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="6fe79-118">Les messages correspondant à ce filtre sont envoyés à cette destination.</span><span class="sxs-lookup"><span data-stu-id="6fe79-118">Messages matching this filter will be sent to this destination.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6fe79-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6fe79-119">Parent Elements</span></span>  
  
|<span data-ttu-id="6fe79-120">Élément</span><span class="sxs-lookup"><span data-stu-id="6fe79-120">Element</span></span>|<span data-ttu-id="6fe79-121">Description</span><span class="sxs-lookup"><span data-stu-id="6fe79-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6fe79-122">\<routing></span><span class="sxs-lookup"><span data-stu-id="6fe79-122">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="6fe79-123">Section de configuration qui contient une table de routage.</span><span class="sxs-lookup"><span data-stu-id="6fe79-123">A configuration section that contains a routing table.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6fe79-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fe79-124">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>
