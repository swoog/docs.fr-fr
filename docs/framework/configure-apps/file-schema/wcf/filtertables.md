---
title: <filterTables>
ms.date: 03/30/2017
ms.assetid: 41f1ac35-f559-473a-b2c3-8cc83a6a3831
ms.openlocfilehash: c49c7cf3a196595556c2bf1b4ed4365bfe1e4cbf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704243"
---
# <a name="filtertables"></a><span data-ttu-id="7c245-101">\<filterTables></span><span class="sxs-lookup"><span data-stu-id="7c245-101">\<filterTables></span></span>
<span data-ttu-id="7c245-102">Représente une section de configuration permettant de définir des tables de routage qui contiennent des mappages entre les filtres de routage et les points de terminaison cibles auxquels envoyer des messages lorsque le filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="7c245-102">Represents a configuration section for defining routing tables that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="7c245-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="7c245-103">\<system.serviceModel></span></span>  
<span data-ttu-id="7c245-104">\<routing></span><span class="sxs-lookup"><span data-stu-id="7c245-104">\<routing></span></span>  
<span data-ttu-id="7c245-105">\<routingTables></span><span class="sxs-lookup"><span data-stu-id="7c245-105">\<routingTables></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7c245-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c245-106">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7c245-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7c245-107">Attributes and Elements</span></span>  
 <span data-ttu-id="7c245-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7c245-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7c245-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="7c245-109">Attributes</span></span>  
 <span data-ttu-id="7c245-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7c245-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="7c245-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7c245-111">Child Elements</span></span>  
  
|<span data-ttu-id="7c245-112">Élément</span><span class="sxs-lookup"><span data-stu-id="7c245-112">Element</span></span>|<span data-ttu-id="7c245-113">Description</span><span class="sxs-lookup"><span data-stu-id="7c245-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7c245-114">\<filtres></span><span class="sxs-lookup"><span data-stu-id="7c245-114">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="7c245-115">Table de routage qui contient des mappages entre les filtres de routage et les points de terminaison cibles vers lesquels envoyer des messages lorsque le filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="7c245-115">A routing table that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="7c245-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7c245-116">Parent Elements</span></span>  
  
|<span data-ttu-id="7c245-117">Élément</span><span class="sxs-lookup"><span data-stu-id="7c245-117">Element</span></span>|<span data-ttu-id="7c245-118">Description</span><span class="sxs-lookup"><span data-stu-id="7c245-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7c245-119">\<routing></span><span class="sxs-lookup"><span data-stu-id="7c245-119">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="7c245-120">Section de configuration qui contient des filtres de routage et des tables de routage.</span><span class="sxs-lookup"><span data-stu-id="7c245-120">A configuration section that contains routing filters and routing tables.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7c245-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c245-121">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableCollection?displayProperty=nameWithType>
