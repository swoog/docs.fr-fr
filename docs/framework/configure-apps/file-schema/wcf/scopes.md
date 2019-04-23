---
title: <scopes>
ms.date: 03/30/2017
ms.assetid: 9a0dd3ce-e383-4ac3-b7be-7d604388304a
ms.openlocfilehash: 8bc720238ca3039106345783381cd26134fc46b5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59213075"
---
# <a name="scopes"></a><span data-ttu-id="00f10-101">\<scopes></span><span class="sxs-lookup"><span data-stu-id="00f10-101">\<scopes></span></span>
<span data-ttu-id="00f10-102">Contient une collection d’éléments de configuration qui spécifient des URI de portée personnalisés à utiliser pour filtrer des points de terminaison de service pendant la requête.</span><span class="sxs-lookup"><span data-stu-id="00f10-102">Contains a collection of configuration elements that specify custom scope Uris that can be used to filter service endpoints during query.</span></span>  
  
<span data-ttu-id="00f10-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="00f10-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="00f10-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="00f10-104">\<behaviors></span></span>  
<span data-ttu-id="00f10-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="00f10-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="00f10-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="00f10-106">\<behavior></span></span>  
<span data-ttu-id="00f10-107">\<endpointDiscovery></span><span class="sxs-lookup"><span data-stu-id="00f10-107">\<endpointDiscovery></span></span>  
<span data-ttu-id="00f10-108">\<scopes></span><span class="sxs-lookup"><span data-stu-id="00f10-108">\<scopes></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00f10-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00f10-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="String">
      <endpointDiscovery enable="Boolean">
        <scopes>
          <add scope="URI" />
        </scopes>
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="00f10-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="00f10-110">Attributes and Elements</span></span>  
 <span data-ttu-id="00f10-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="00f10-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="00f10-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="00f10-112">Attributes</span></span>  
 <span data-ttu-id="00f10-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="00f10-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="00f10-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="00f10-114">Child Elements</span></span>  
  
|<span data-ttu-id="00f10-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="00f10-115">Attribute</span></span>|<span data-ttu-id="00f10-116">Description</span><span class="sxs-lookup"><span data-stu-id="00f10-116">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="00f10-117">\<add></span><span class="sxs-lookup"><span data-stu-id="00f10-117">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-scopes.md)|<span data-ttu-id="00f10-118">Ajoute les informations de portée du point de terminaison à utiliser lors de la mise en correspondance des critères de recherche des services.</span><span class="sxs-lookup"><span data-stu-id="00f10-118">Adds the scope information for the endpoint that can be used in matching criteria for finding services.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="00f10-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="00f10-119">Parent Elements</span></span>  
  
|<span data-ttu-id="00f10-120">Élément</span><span class="sxs-lookup"><span data-stu-id="00f10-120">Element</span></span>|<span data-ttu-id="00f10-121">Description</span><span class="sxs-lookup"><span data-stu-id="00f10-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="00f10-122">\<endpointDiscovery></span><span class="sxs-lookup"><span data-stu-id="00f10-122">\<endpointDiscovery></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpointdiscovery.md)|<span data-ttu-id="00f10-123">Spécifie les différents paramètres de découverte d’un point de terminaison, tels que la fonctionnalité de découverte, les portées et toutes les extensions personnalisées de ses métadonnées.</span><span class="sxs-lookup"><span data-stu-id="00f10-123">Specifies the various discovery settings for an endpoint, such as its discoverability, scopes, and any custom extensions to its metadata.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="00f10-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00f10-124">See also</span></span>

- <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
