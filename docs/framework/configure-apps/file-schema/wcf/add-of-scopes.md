---
title: '&lt;add&gt; de &lt;scopes&gt;'
ms.date: 03/30/2017
ms.assetid: 0563a7d8-fc84-4c85-9066-af32665857c2
ms.openlocfilehash: a889100da4723a1f5e8f84ca88ea426ccaa2e77f
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32745797"
---
# <a name="ltaddgt-of-ltscopesgt"></a><span data-ttu-id="1ec89-102">&lt;add&gt; de &lt;scopes&gt;</span><span class="sxs-lookup"><span data-stu-id="1ec89-102">&lt;add&gt; of &lt;scopes&gt;</span></span>
<span data-ttu-id="1ec89-103">Ajoute un URI de portée personnalisé qui permet de filtrer les points de terminaison de service pendant la requête.</span><span class="sxs-lookup"><span data-stu-id="1ec89-103">Adds a custom scope Uri that can be used to filter service endpoints during query.</span></span>  
  
<span data-ttu-id="1ec89-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="1ec89-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="1ec89-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="1ec89-105">\<behaviors></span></span>  
<span data-ttu-id="1ec89-106">\<endpointBehaviors ></span><span class="sxs-lookup"><span data-stu-id="1ec89-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="1ec89-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="1ec89-107">\<behavior></span></span>  
<span data-ttu-id="1ec89-108">\<endpointDiscovery ></span><span class="sxs-lookup"><span data-stu-id="1ec89-108">\<endpointDiscovery></span></span>  
<span data-ttu-id="1ec89-109">\<étendues ></span><span class="sxs-lookup"><span data-stu-id="1ec89-109">\<scopes></span></span>  
<span data-ttu-id="1ec89-110">\<add></span><span class="sxs-lookup"><span data-stu-id="1ec89-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ec89-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ec89-111">Syntax</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="String">
      <endpointDiscovery enable="Boolean">
        <scopes>
          <add scope="URI"/>
        </scopes>
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1ec89-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1ec89-112">Attributes and Elements</span></span>  
 <span data-ttu-id="1ec89-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1ec89-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1ec89-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="1ec89-114">Attributes</span></span>  
  
|<span data-ttu-id="1ec89-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="1ec89-115">Attribute</span></span>|<span data-ttu-id="1ec89-116">Description</span><span class="sxs-lookup"><span data-stu-id="1ec89-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="1ec89-117">portée</span><span class="sxs-lookup"><span data-stu-id="1ec89-117">scope</span></span>|<span data-ttu-id="1ec89-118">URI qui contient les informations de portée du point de terminaison à utiliser lors de la mise en correspondance des critères de recherche des services.</span><span class="sxs-lookup"><span data-stu-id="1ec89-118">A URI that contains scope information for the endpoint that can be used in matching criteria for finding services.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1ec89-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1ec89-119">Child Elements</span></span>  
 <span data-ttu-id="1ec89-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1ec89-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1ec89-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1ec89-121">Parent Elements</span></span>  
  
|<span data-ttu-id="1ec89-122">Élément</span><span class="sxs-lookup"><span data-stu-id="1ec89-122">Element</span></span>|<span data-ttu-id="1ec89-123">Description</span><span class="sxs-lookup"><span data-stu-id="1ec89-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1ec89-124">\<étendues ></span><span class="sxs-lookup"><span data-stu-id="1ec89-124">\<scopes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)|<span data-ttu-id="1ec89-125">Contient une collection d’éléments de configuration qui spécifient des URI de portée personnalisés à utiliser pour filtrer des points de terminaison de service pendant la requête.</span><span class="sxs-lookup"><span data-stu-id="1ec89-125">Contains a collection of configuration elements that specify custom scope Uris that can be used to filter service endpoints during query.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1ec89-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ec89-126">See Also</span></span>  
 <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
