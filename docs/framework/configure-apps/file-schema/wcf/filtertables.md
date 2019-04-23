---
title: <filterTables>
ms.date: 03/30/2017
ms.assetid: 41f1ac35-f559-473a-b2c3-8cc83a6a3831
ms.openlocfilehash: c49c7cf3a196595556c2bf1b4ed4365bfe1e4cbf
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59075728"
---
# <a name="filtertables"></a><span data-ttu-id="410d8-101">\<filterTables></span><span class="sxs-lookup"><span data-stu-id="410d8-101">\<filterTables></span></span>
<span data-ttu-id="410d8-102">Représente une section de configuration permettant de définir des tables de routage qui contiennent des mappages entre les filtres de routage et les points de terminaison cibles auxquels envoyer des messages lorsque le filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="410d8-102">Represents a configuration section for defining routing tables that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="410d8-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="410d8-103">\<system.serviceModel></span></span>  
<span data-ttu-id="410d8-104">\<routing></span><span class="sxs-lookup"><span data-stu-id="410d8-104">\<routing></span></span>  
<span data-ttu-id="410d8-105">\<routingTables></span><span class="sxs-lookup"><span data-stu-id="410d8-105">\<routingTables></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="410d8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="410d8-106">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="410d8-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="410d8-107">Attributes and Elements</span></span>  
 <span data-ttu-id="410d8-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="410d8-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="410d8-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="410d8-109">Attributes</span></span>  
 <span data-ttu-id="410d8-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="410d8-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="410d8-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="410d8-111">Child Elements</span></span>  
  
|<span data-ttu-id="410d8-112">Élément</span><span class="sxs-lookup"><span data-stu-id="410d8-112">Element</span></span>|<span data-ttu-id="410d8-113">Description</span><span class="sxs-lookup"><span data-stu-id="410d8-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="410d8-114">\<filtres></span><span class="sxs-lookup"><span data-stu-id="410d8-114">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="410d8-115">Table de routage qui contient des mappages entre les filtres de routage et les points de terminaison cibles vers lesquels envoyer des messages lorsque le filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="410d8-115">A routing table that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="410d8-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="410d8-116">Parent Elements</span></span>  
  
|<span data-ttu-id="410d8-117">Élément</span><span class="sxs-lookup"><span data-stu-id="410d8-117">Element</span></span>|<span data-ttu-id="410d8-118">Description</span><span class="sxs-lookup"><span data-stu-id="410d8-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="410d8-119">\<routing></span><span class="sxs-lookup"><span data-stu-id="410d8-119">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="410d8-120">Section de configuration qui contient des filtres de routage et des tables de routage.</span><span class="sxs-lookup"><span data-stu-id="410d8-120">A configuration section that contains routing filters and routing tables.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="410d8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="410d8-121">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableCollection?displayProperty=nameWithType>
