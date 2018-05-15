---
title: '&lt;useRequestHeadersForMetadataAddress&gt;'
ms.date: 03/30/2017
ms.assetid: 679f0eae-f353-44d1-b42d-a9e247509774
ms.openlocfilehash: 7e661570f8b94b979595a615b3f6819d41ed5e35
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltuserequestheadersformetadataaddressgt"></a><span data-ttu-id="22ef1-102">&lt;useRequestHeadersForMetadataAddress&gt;</span><span class="sxs-lookup"><span data-stu-id="22ef1-102">&lt;useRequestHeadersForMetadataAddress&gt;</span></span>
<span data-ttu-id="22ef1-103">Active la récupération des informations d'adresse des métadonnées à partir des en-têtes de message de demande.</span><span class="sxs-lookup"><span data-stu-id="22ef1-103">Enables the retrieval of metadata address information from the request message headers.</span></span>  
  
<span data-ttu-id="22ef1-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="22ef1-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="22ef1-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="22ef1-105">\<behaviors></span></span>  
<span data-ttu-id="22ef1-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="22ef1-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="22ef1-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="22ef1-107">\<behavior></span></span>  
<span data-ttu-id="22ef1-108">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="22ef1-108">\<useRequestHeadersForMetadataAddress></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22ef1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22ef1-109">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http" port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="22ef1-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="22ef1-110">Attributes and Elements</span></span>  
 <span data-ttu-id="22ef1-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="22ef1-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="22ef1-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="22ef1-112">Attributes</span></span>  
 <span data-ttu-id="22ef1-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="22ef1-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="22ef1-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="22ef1-114">Child Elements</span></span>  
  
|<span data-ttu-id="22ef1-115">Élément</span><span class="sxs-lookup"><span data-stu-id="22ef1-115">Element</span></span>|<span data-ttu-id="22ef1-116">Description</span><span class="sxs-lookup"><span data-stu-id="22ef1-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="22ef1-117">\<defaultPorts ></span><span class="sxs-lookup"><span data-stu-id="22ef1-117">\<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/defaultports.md)|<span data-ttu-id="22ef1-118">Collection des ports par défaut répertoriant les points de terminaison de communication par défaut écoutés par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="22ef1-118">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="22ef1-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="22ef1-119">Parent Elements</span></span>  
  
|<span data-ttu-id="22ef1-120">Élément</span><span class="sxs-lookup"><span data-stu-id="22ef1-120">Element</span></span>|<span data-ttu-id="22ef1-121">Description</span><span class="sxs-lookup"><span data-stu-id="22ef1-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="22ef1-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="22ef1-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="22ef1-123">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="22ef1-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="22ef1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22ef1-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.UseRequestHeadersForMetadataAddressElement>
