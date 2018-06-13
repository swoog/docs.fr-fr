---
title: '&lt;Étendues&gt;'
ms.date: 03/30/2017
ms.assetid: 9a0dd3ce-e383-4ac3-b7be-7d604388304a
ms.openlocfilehash: 7e2dda0d0def4d1f90bf1b4dbf54f18983355222
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32749619"
---
# <a name="ltscopesgt"></a><span data-ttu-id="376c8-102">&lt;Étendues&gt;</span><span class="sxs-lookup"><span data-stu-id="376c8-102">&lt;scopes&gt;</span></span>
<span data-ttu-id="376c8-103">Contient une collection d’éléments de configuration qui spécifient des URI de portée personnalisés à utiliser pour filtrer des points de terminaison de service pendant la requête.</span><span class="sxs-lookup"><span data-stu-id="376c8-103">Contains a collection of configuration elements that specify custom scope Uris that can be used to filter service endpoints during query.</span></span>  
  
<span data-ttu-id="376c8-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="376c8-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="376c8-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="376c8-105">\<behaviors></span></span>  
<span data-ttu-id="376c8-106">\<endpointBehaviors ></span><span class="sxs-lookup"><span data-stu-id="376c8-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="376c8-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="376c8-107">\<behavior></span></span>  
<span data-ttu-id="376c8-108">\<endpointDiscovery ></span><span class="sxs-lookup"><span data-stu-id="376c8-108">\<endpointDiscovery></span></span>  
<span data-ttu-id="376c8-109">\<étendues ></span><span class="sxs-lookup"><span data-stu-id="376c8-109">\<scopes></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="376c8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="376c8-110">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="376c8-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="376c8-111">Attributes and Elements</span></span>  
 <span data-ttu-id="376c8-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="376c8-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="376c8-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="376c8-113">Attributes</span></span>  
 <span data-ttu-id="376c8-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="376c8-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="376c8-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="376c8-115">Child Elements</span></span>  
  
|<span data-ttu-id="376c8-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="376c8-116">Attribute</span></span>|<span data-ttu-id="376c8-117">Description</span><span class="sxs-lookup"><span data-stu-id="376c8-117">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="376c8-118">\<add></span><span class="sxs-lookup"><span data-stu-id="376c8-118">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-scopes.md)|<span data-ttu-id="376c8-119">Ajoute les informations de portée du point de terminaison à utiliser lors de la mise en correspondance des critères de recherche des services.</span><span class="sxs-lookup"><span data-stu-id="376c8-119">Adds the scope information for the endpoint that can be used in matching criteria for finding services.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="376c8-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="376c8-120">Parent Elements</span></span>  
  
|<span data-ttu-id="376c8-121">Élément</span><span class="sxs-lookup"><span data-stu-id="376c8-121">Element</span></span>|<span data-ttu-id="376c8-122">Description</span><span class="sxs-lookup"><span data-stu-id="376c8-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="376c8-123">\<endpointDiscovery ></span><span class="sxs-lookup"><span data-stu-id="376c8-123">\<endpointDiscovery></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpointdiscovery.md)|<span data-ttu-id="376c8-124">Spécifie les différents paramètres de découverte d’un point de terminaison, tels que la fonctionnalité de découverte, les portées et toutes les extensions personnalisées de ses métadonnées.</span><span class="sxs-lookup"><span data-stu-id="376c8-124">Specifies the various discovery settings for an endpoint, such as its discoverability, scopes, and any custom extensions to its metadata.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="376c8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="376c8-125">See Also</span></span>  
 <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
