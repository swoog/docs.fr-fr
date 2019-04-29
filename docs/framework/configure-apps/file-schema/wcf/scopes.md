---
title: <scopes>
ms.date: 03/30/2017
ms.assetid: 9a0dd3ce-e383-4ac3-b7be-7d604388304a
ms.openlocfilehash: 8bc720238ca3039106345783381cd26134fc46b5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61670623"
---
# <a name="scopes"></a><span data-ttu-id="fa1bc-101">\<scopes></span><span class="sxs-lookup"><span data-stu-id="fa1bc-101">\<scopes></span></span>
<span data-ttu-id="fa1bc-102">Contient une collection d’éléments de configuration qui spécifient des URI de portée personnalisés à utiliser pour filtrer des points de terminaison de service pendant la requête.</span><span class="sxs-lookup"><span data-stu-id="fa1bc-102">Contains a collection of configuration elements that specify custom scope Uris that can be used to filter service endpoints during query.</span></span>  
  
<span data-ttu-id="fa1bc-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="fa1bc-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="fa1bc-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="fa1bc-104">\<behaviors></span></span>  
<span data-ttu-id="fa1bc-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="fa1bc-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="fa1bc-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="fa1bc-106">\<behavior></span></span>  
<span data-ttu-id="fa1bc-107">\<endpointDiscovery></span><span class="sxs-lookup"><span data-stu-id="fa1bc-107">\<endpointDiscovery></span></span>  
<span data-ttu-id="fa1bc-108">\<scopes></span><span class="sxs-lookup"><span data-stu-id="fa1bc-108">\<scopes></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa1bc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa1bc-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fa1bc-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="fa1bc-110">Attributes and Elements</span></span>  
 <span data-ttu-id="fa1bc-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="fa1bc-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fa1bc-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="fa1bc-112">Attributes</span></span>  
 <span data-ttu-id="fa1bc-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fa1bc-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="fa1bc-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fa1bc-114">Child Elements</span></span>  
  
|<span data-ttu-id="fa1bc-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="fa1bc-115">Attribute</span></span>|<span data-ttu-id="fa1bc-116">Description</span><span class="sxs-lookup"><span data-stu-id="fa1bc-116">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="fa1bc-117">\<add></span><span class="sxs-lookup"><span data-stu-id="fa1bc-117">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-scopes.md)|<span data-ttu-id="fa1bc-118">Ajoute les informations de portée du point de terminaison à utiliser lors de la mise en correspondance des critères de recherche des services.</span><span class="sxs-lookup"><span data-stu-id="fa1bc-118">Adds the scope information for the endpoint that can be used in matching criteria for finding services.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="fa1bc-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fa1bc-119">Parent Elements</span></span>  
  
|<span data-ttu-id="fa1bc-120">Élément</span><span class="sxs-lookup"><span data-stu-id="fa1bc-120">Element</span></span>|<span data-ttu-id="fa1bc-121">Description</span><span class="sxs-lookup"><span data-stu-id="fa1bc-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fa1bc-122">\<endpointDiscovery></span><span class="sxs-lookup"><span data-stu-id="fa1bc-122">\<endpointDiscovery></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpointdiscovery.md)|<span data-ttu-id="fa1bc-123">Spécifie les différents paramètres de découverte d’un point de terminaison, tels que la fonctionnalité de découverte, les portées et toutes les extensions personnalisées de ses métadonnées.</span><span class="sxs-lookup"><span data-stu-id="fa1bc-123">Specifies the various discovery settings for an endpoint, such as its discoverability, scopes, and any custom extensions to its metadata.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="fa1bc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa1bc-124">See also</span></span>

- <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
