---
title: '&lt;defaultPorts&gt;'
ms.date: 03/30/2017
ms.assetid: 725d4ee5-bd46-4f0e-9c20-30ba75d6eb2c
ms.openlocfilehash: 2f7de066a1b91e9fa22fbe0213e221c6f4bbe617
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltdefaultportsgt"></a><span data-ttu-id="fce59-102">&lt;defaultPorts&gt;</span><span class="sxs-lookup"><span data-stu-id="fce59-102">&lt;defaultPorts&gt;</span></span>
<span data-ttu-id="fce59-103">Collection des ports par défaut répertoriant les points de terminaison de communication par défaut écoutés par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="fce59-103">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>  
  
<span data-ttu-id="fce59-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="fce59-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="fce59-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="fce59-105">\<behaviors></span></span>  
<span data-ttu-id="fce59-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="fce59-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="fce59-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="fce59-107">\<behavior></span></span>  
<span data-ttu-id="fce59-108">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="fce59-108">\<useRequestHeadersForMetadataAddress></span></span>  
<span data-ttu-id="fce59-109">\<defaultPorts ></span><span class="sxs-lookup"><span data-stu-id="fce59-109">\<defaultPorts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fce59-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fce59-110">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http" port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fce59-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="fce59-111">Attributes and Elements</span></span>  
 <span data-ttu-id="fce59-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="fce59-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fce59-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="fce59-113">Attributes</span></span>  
 <span data-ttu-id="fce59-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fce59-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="fce59-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fce59-115">Child Elements</span></span>  
  
|<span data-ttu-id="fce59-116">Élément</span><span class="sxs-lookup"><span data-stu-id="fce59-116">Element</span></span>|<span data-ttu-id="fce59-117">Description</span><span class="sxs-lookup"><span data-stu-id="fce59-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fce59-118">\<Ajouter > de \<defaultPorts ></span><span class="sxs-lookup"><span data-stu-id="fce59-118">\<add> of \<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-defaultports.md)|<span data-ttu-id="fce59-119">Point de terminaison de communication par défaut écouté par l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="fce59-119">A default communications endpoint that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="fce59-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fce59-120">Parent Elements</span></span>  
  
|<span data-ttu-id="fce59-121">Élément</span><span class="sxs-lookup"><span data-stu-id="fce59-121">Element</span></span>|<span data-ttu-id="fce59-122">Description</span><span class="sxs-lookup"><span data-stu-id="fce59-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fce59-123">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="fce59-123">\<useRequestHeadersForMetadataAddress></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/userequestheadersformetadataaddress.md)|<span data-ttu-id="fce59-124">Liste de ports par défaut.</span><span class="sxs-lookup"><span data-stu-id="fce59-124">A list of default ports.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="fce59-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fce59-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.DefaultPortElementCollection>
