---
title: '&lt;useRequestHeadersForMetadataAddress&gt;'
ms.date: 03/30/2017
ms.assetid: 679f0eae-f353-44d1-b42d-a9e247509774
ms.openlocfilehash: bcbf1c633e0796c6056759dfbb55014838e0e293
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151408"
---
# <a name="ltuserequestheadersformetadataaddressgt"></a><span data-ttu-id="edf2c-102">&lt;useRequestHeadersForMetadataAddress&gt;</span><span class="sxs-lookup"><span data-stu-id="edf2c-102">&lt;useRequestHeadersForMetadataAddress&gt;</span></span>
<span data-ttu-id="edf2c-103">Active la récupération des informations d'adresse des métadonnées à partir des en-têtes de message de demande.</span><span class="sxs-lookup"><span data-stu-id="edf2c-103">Enables the retrieval of metadata address information from the request message headers.</span></span>  
  
<span data-ttu-id="edf2c-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="edf2c-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="edf2c-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="edf2c-105">\<behaviors></span></span>  
<span data-ttu-id="edf2c-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="edf2c-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="edf2c-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="edf2c-107">\<behavior></span></span>  
<span data-ttu-id="edf2c-108">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="edf2c-108">\<useRequestHeadersForMetadataAddress></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="edf2c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edf2c-109">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="edf2c-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="edf2c-110">Attributes and Elements</span></span>  
 <span data-ttu-id="edf2c-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="edf2c-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="edf2c-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="edf2c-112">Attributes</span></span>  
 <span data-ttu-id="edf2c-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="edf2c-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="edf2c-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="edf2c-114">Child Elements</span></span>  
  
|<span data-ttu-id="edf2c-115">Élément</span><span class="sxs-lookup"><span data-stu-id="edf2c-115">Element</span></span>|<span data-ttu-id="edf2c-116">Description</span><span class="sxs-lookup"><span data-stu-id="edf2c-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="edf2c-117">\<defaultPorts ></span><span class="sxs-lookup"><span data-stu-id="edf2c-117">\<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/defaultports.md)|<span data-ttu-id="edf2c-118">Collection des ports par défaut répertoriant les points de terminaison de communication par défaut écoutés par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="edf2c-118">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="edf2c-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="edf2c-119">Parent Elements</span></span>  
  
|<span data-ttu-id="edf2c-120">Élément</span><span class="sxs-lookup"><span data-stu-id="edf2c-120">Element</span></span>|<span data-ttu-id="edf2c-121">Description</span><span class="sxs-lookup"><span data-stu-id="edf2c-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="edf2c-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="edf2c-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="edf2c-123">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="edf2c-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="edf2c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edf2c-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.UseRequestHeadersForMetadataAddressElement>
