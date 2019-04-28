---
title: <entries>
ms.date: 03/30/2017
ms.assetid: 202e430c-c1b9-4343-abe2-ac78c181a3b7
ms.openlocfilehash: 5561cf61cef2258ec61bd32770538add1c69f5c1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704204"
---
# <a name="entries"></a><span data-ttu-id="9c7b2-101">\<entries></span><span class="sxs-lookup"><span data-stu-id="9c7b2-101">\<entries></span></span>
<span data-ttu-id="9c7b2-102">Entrée de routage qui contient des mappages entre les filtres de routage et les points de terminaison cibles vers lesquels envoyer des messages lorsque le filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="9c7b2-102">A routing entry that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="9c7b2-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="9c7b2-103">\<system.serviceModel></span></span>  
<span data-ttu-id="9c7b2-104">\<routing></span><span class="sxs-lookup"><span data-stu-id="9c7b2-104">\<routing></span></span>  
<span data-ttu-id="9c7b2-105">\<routingTables></span><span class="sxs-lookup"><span data-stu-id="9c7b2-105">\<routingTables></span></span>  
<span data-ttu-id="9c7b2-106">\<table></span><span class="sxs-lookup"><span data-stu-id="9c7b2-106">\<table></span></span>  
<span data-ttu-id="9c7b2-107">\<entries></span><span class="sxs-lookup"><span data-stu-id="9c7b2-107">\<entries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c7b2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c7b2-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9c7b2-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9c7b2-109">Attributes and Elements</span></span>  
 <span data-ttu-id="9c7b2-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9c7b2-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9c7b2-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="9c7b2-111">Attributes</span></span>  
 <span data-ttu-id="9c7b2-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9c7b2-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9c7b2-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9c7b2-113">Child Elements</span></span>  
  
|<span data-ttu-id="9c7b2-114">Élément</span><span class="sxs-lookup"><span data-stu-id="9c7b2-114">Element</span></span>|<span data-ttu-id="9c7b2-115">Description</span><span class="sxs-lookup"><span data-stu-id="9c7b2-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9c7b2-116">\<filtres></span><span class="sxs-lookup"><span data-stu-id="9c7b2-116">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="9c7b2-117">Mappe un filtre à un point de terminaison client précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="9c7b2-117">Maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="9c7b2-118">Les messages correspondant à ce filtre sont envoyés à cette destination.</span><span class="sxs-lookup"><span data-stu-id="9c7b2-118">Messages matching this filter will be sent to this destination.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9c7b2-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9c7b2-119">Parent Elements</span></span>  
  
|<span data-ttu-id="9c7b2-120">Élément</span><span class="sxs-lookup"><span data-stu-id="9c7b2-120">Element</span></span>|<span data-ttu-id="9c7b2-121">Description</span><span class="sxs-lookup"><span data-stu-id="9c7b2-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9c7b2-122">\<routing></span><span class="sxs-lookup"><span data-stu-id="9c7b2-122">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="9c7b2-123">Section de configuration qui contient une table de routage.</span><span class="sxs-lookup"><span data-stu-id="9c7b2-123">A configuration section that contains a routing table.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9c7b2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c7b2-124">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>
