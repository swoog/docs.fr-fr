---
title: <entries>
ms.date: 03/30/2017
ms.assetid: 202e430c-c1b9-4343-abe2-ac78c181a3b7
ms.openlocfilehash: 9c4c7fa4f778642d549deebce6e7476f4da13a0d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55283684"
---
# <a name="entries"></a><span data-ttu-id="851b8-101">\<entries></span><span class="sxs-lookup"><span data-stu-id="851b8-101">\<entries></span></span>
<span data-ttu-id="851b8-102">Entrée de routage qui contient des mappages entre les filtres de routage et les points de terminaison cibles vers lesquels envoyer des messages lorsque le filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="851b8-102">A routing entry that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="851b8-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="851b8-103">\<system.serviceModel></span></span>  
<span data-ttu-id="851b8-104">\<routing></span><span class="sxs-lookup"><span data-stu-id="851b8-104">\<routing></span></span>  
<span data-ttu-id="851b8-105">\<routingTables></span><span class="sxs-lookup"><span data-stu-id="851b8-105">\<routingTables></span></span>  
<span data-ttu-id="851b8-106">\<table></span><span class="sxs-lookup"><span data-stu-id="851b8-106">\<table></span></span>  
<span data-ttu-id="851b8-107">\<entries></span><span class="sxs-lookup"><span data-stu-id="851b8-107">\<entries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="851b8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="851b8-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="851b8-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="851b8-109">Attributes and Elements</span></span>  
 <span data-ttu-id="851b8-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="851b8-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="851b8-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="851b8-111">Attributes</span></span>  
 <span data-ttu-id="851b8-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="851b8-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="851b8-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="851b8-113">Child Elements</span></span>  
  
|<span data-ttu-id="851b8-114">Élément</span><span class="sxs-lookup"><span data-stu-id="851b8-114">Element</span></span>|<span data-ttu-id="851b8-115">Description</span><span class="sxs-lookup"><span data-stu-id="851b8-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="851b8-116">\<filtres></span><span class="sxs-lookup"><span data-stu-id="851b8-116">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="851b8-117">Mappe un filtre à un point de terminaison client précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="851b8-117">Maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="851b8-118">Les messages correspondant à ce filtre sont envoyés à cette destination.</span><span class="sxs-lookup"><span data-stu-id="851b8-118">Messages matching this filter will be sent to this destination.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="851b8-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="851b8-119">Parent Elements</span></span>  
  
|<span data-ttu-id="851b8-120">Élément</span><span class="sxs-lookup"><span data-stu-id="851b8-120">Element</span></span>|<span data-ttu-id="851b8-121">Description</span><span class="sxs-lookup"><span data-stu-id="851b8-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="851b8-122">\<routing></span><span class="sxs-lookup"><span data-stu-id="851b8-122">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="851b8-123">Section de configuration qui contient une table de routage.</span><span class="sxs-lookup"><span data-stu-id="851b8-123">A configuration section that contains a routing table.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="851b8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="851b8-124">See also</span></span>
- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>
