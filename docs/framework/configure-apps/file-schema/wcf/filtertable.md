---
title: '&lt;filterTable&gt;'
ms.date: 03/30/2017
ms.assetid: e9f05441-3ad1-49b9-a267-71724aa094b4
ms.openlocfilehash: 83339eebef9a4f1b7f69e0bd1dd16b8278a68258
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54534603"
---
# <a name="ltfiltertablegt"></a><span data-ttu-id="5db06-102">&lt;filterTable&gt;</span><span class="sxs-lookup"><span data-stu-id="5db06-102">&lt;filterTable&gt;</span></span>
<span data-ttu-id="5db06-103">Représente une table de routage qui contient une liste de filtres pour évaluer des messages et router les messages vers le point de terminaison client si le filtre a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="5db06-103">Represents a routing table that contains a list of filters to evaluate messages against and the client endpoint to route messages to if the filter evaluates to true.</span></span>  
  
 <span data-ttu-id="5db06-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="5db06-104">\<system.serviceModel></span></span>  
<span data-ttu-id="5db06-105">\<routing></span><span class="sxs-lookup"><span data-stu-id="5db06-105">\<routing></span></span>  
<span data-ttu-id="5db06-106">\<routingTables></span><span class="sxs-lookup"><span data-stu-id="5db06-106">\<routingTables></span></span>  
<span data-ttu-id="5db06-107">\<table></span><span class="sxs-lookup"><span data-stu-id="5db06-107">\<table></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5db06-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5db06-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5db06-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5db06-109">Attributes and Elements</span></span>  
 <span data-ttu-id="5db06-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5db06-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5db06-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="5db06-111">Attributes</span></span>  
  
|<span data-ttu-id="5db06-112">Élément</span><span class="sxs-lookup"><span data-stu-id="5db06-112">Element</span></span>|<span data-ttu-id="5db06-113">Description</span><span class="sxs-lookup"><span data-stu-id="5db06-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="5db06-114">name</span><span class="sxs-lookup"><span data-stu-id="5db06-114">name</span></span>|<span data-ttu-id="5db06-115">Chaîne qui contient le nom unique de cet élément de configuration.</span><span class="sxs-lookup"><span data-stu-id="5db06-115">A string that contains the unique name of this configuration element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5db06-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5db06-116">Child Elements</span></span>  
  
|<span data-ttu-id="5db06-117">Élément</span><span class="sxs-lookup"><span data-stu-id="5db06-117">Element</span></span>|<span data-ttu-id="5db06-118">Description</span><span class="sxs-lookup"><span data-stu-id="5db06-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5db06-119">\<filtres></span><span class="sxs-lookup"><span data-stu-id="5db06-119">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="5db06-120">Mappages entre les filtres de routage et les points de terminaison cibles auxquels envoyer des messages lorsque le filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="5db06-120">Mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5db06-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5db06-121">Parent Elements</span></span>  
  
|<span data-ttu-id="5db06-122">Élément</span><span class="sxs-lookup"><span data-stu-id="5db06-122">Element</span></span>|<span data-ttu-id="5db06-123">Description</span><span class="sxs-lookup"><span data-stu-id="5db06-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5db06-124">\<routing></span><span class="sxs-lookup"><span data-stu-id="5db06-124">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="5db06-125">Section de configuration qui contient des tables de routage.</span><span class="sxs-lookup"><span data-stu-id="5db06-125">A configuration section that contains routing tables.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5db06-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5db06-126">See also</span></span>
- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
