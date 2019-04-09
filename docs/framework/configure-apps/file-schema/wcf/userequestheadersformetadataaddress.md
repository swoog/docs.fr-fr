---
title: <useRequestHeadersForMetadataAddress>
ms.date: 03/30/2017
ms.assetid: 679f0eae-f353-44d1-b42d-a9e247509774
ms.openlocfilehash: 969461d0e5bdc9f8c49b7a019a6000af5af77eec
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59121184"
---
# <a name="userequestheadersformetadataaddress"></a><span data-ttu-id="9da71-101">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="9da71-101">\<useRequestHeadersForMetadataAddress></span></span>
<span data-ttu-id="9da71-102">Active la récupération des informations d'adresse des métadonnées à partir des en-têtes de message de demande.</span><span class="sxs-lookup"><span data-stu-id="9da71-102">Enables the retrieval of metadata address information from the request message headers.</span></span>  
  
<span data-ttu-id="9da71-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="9da71-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="9da71-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="9da71-104">\<behaviors></span></span>  
<span data-ttu-id="9da71-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="9da71-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="9da71-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="9da71-106">\<behavior></span></span>  
<span data-ttu-id="9da71-107">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="9da71-107">\<useRequestHeadersForMetadataAddress></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9da71-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9da71-108">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9da71-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9da71-109">Attributes and Elements</span></span>  
 <span data-ttu-id="9da71-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9da71-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9da71-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="9da71-111">Attributes</span></span>  
 <span data-ttu-id="9da71-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9da71-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9da71-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9da71-113">Child Elements</span></span>  
  
|<span data-ttu-id="9da71-114">Élément</span><span class="sxs-lookup"><span data-stu-id="9da71-114">Element</span></span>|<span data-ttu-id="9da71-115">Description</span><span class="sxs-lookup"><span data-stu-id="9da71-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9da71-116">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="9da71-116">\<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/defaultports.md)|<span data-ttu-id="9da71-117">Collection des ports par défaut répertoriant les points de terminaison de communication par défaut écoutés par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="9da71-117">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9da71-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9da71-118">Parent Elements</span></span>  
  
|<span data-ttu-id="9da71-119">Élément</span><span class="sxs-lookup"><span data-stu-id="9da71-119">Element</span></span>|<span data-ttu-id="9da71-120">Description</span><span class="sxs-lookup"><span data-stu-id="9da71-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9da71-121">\<behavior></span><span class="sxs-lookup"><span data-stu-id="9da71-121">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="9da71-122">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="9da71-122">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9da71-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9da71-123">See also</span></span>

- <xref:System.ServiceModel.Configuration.UseRequestHeadersForMetadataAddressElement>
