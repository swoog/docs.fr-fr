---
title: <add> de <scopes>
ms.date: 03/30/2017
ms.assetid: 0563a7d8-fc84-4c85-9066-af32665857c2
ms.openlocfilehash: c29e47f688118e34fbdb4deb396c930d478f0582
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59187082"
---
# <a name="add-of-scopes"></a><span data-ttu-id="4ccf4-102">\<Ajouter > de \<étendues ></span><span class="sxs-lookup"><span data-stu-id="4ccf4-102">\<add> of \<scopes></span></span>
<span data-ttu-id="4ccf4-103">Ajoute un URI de portée personnalisé qui permet de filtrer les points de terminaison de service pendant la requête.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-103">Adds a custom scope Uri that can be used to filter service endpoints during query.</span></span>  
  
<span data-ttu-id="4ccf4-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="4ccf4-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="4ccf4-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="4ccf4-105">\<behaviors></span></span>  
<span data-ttu-id="4ccf4-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="4ccf4-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="4ccf4-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="4ccf4-107">\<behavior></span></span>  
<span data-ttu-id="4ccf4-108">\<endpointDiscovery></span><span class="sxs-lookup"><span data-stu-id="4ccf4-108">\<endpointDiscovery></span></span>  
<span data-ttu-id="4ccf4-109">\<scopes></span><span class="sxs-lookup"><span data-stu-id="4ccf4-109">\<scopes></span></span>  
<span data-ttu-id="4ccf4-110">\<add></span><span class="sxs-lookup"><span data-stu-id="4ccf4-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ccf4-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ccf4-111">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4ccf4-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4ccf4-112">Attributes and Elements</span></span>  
 <span data-ttu-id="4ccf4-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4ccf4-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="4ccf4-114">Attributes</span></span>  
  
|<span data-ttu-id="4ccf4-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="4ccf4-115">Attribute</span></span>|<span data-ttu-id="4ccf4-116">Description</span><span class="sxs-lookup"><span data-stu-id="4ccf4-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4ccf4-117">portée</span><span class="sxs-lookup"><span data-stu-id="4ccf4-117">scope</span></span>|<span data-ttu-id="4ccf4-118">URI qui contient les informations de portée du point de terminaison à utiliser lors de la mise en correspondance des critères de recherche des services.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-118">A URI that contains scope information for the endpoint that can be used in matching criteria for finding services.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4ccf4-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4ccf4-119">Child Elements</span></span>  
 <span data-ttu-id="4ccf4-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4ccf4-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4ccf4-121">Parent Elements</span></span>  
  
|<span data-ttu-id="4ccf4-122">Élément</span><span class="sxs-lookup"><span data-stu-id="4ccf4-122">Element</span></span>|<span data-ttu-id="4ccf4-123">Description</span><span class="sxs-lookup"><span data-stu-id="4ccf4-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4ccf4-124">\<scopes></span><span class="sxs-lookup"><span data-stu-id="4ccf4-124">\<scopes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)|<span data-ttu-id="4ccf4-125">Contient une collection d’éléments de configuration qui spécifient des URI de portée personnalisés à utiliser pour filtrer des points de terminaison de service pendant la requête.</span><span class="sxs-lookup"><span data-stu-id="4ccf4-125">Contains a collection of configuration elements that specify custom scope Uris that can be used to filter service endpoints during query.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4ccf4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ccf4-126">See also</span></span>

- <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
