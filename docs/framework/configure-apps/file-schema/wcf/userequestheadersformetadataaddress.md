---
title: <useRequestHeadersForMetadataAddress>
ms.date: 03/30/2017
ms.assetid: 679f0eae-f353-44d1-b42d-a9e247509774
ms.openlocfilehash: 842f989ab1f2f0b9e8fe08e8fd729f983e846ffc
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261566"
---
# <a name="userequestheadersformetadataaddress"></a><span data-ttu-id="d258e-101">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="d258e-101">\<useRequestHeadersForMetadataAddress></span></span>
<span data-ttu-id="d258e-102">Active la récupération des informations d'adresse des métadonnées à partir des en-têtes de message de demande.</span><span class="sxs-lookup"><span data-stu-id="d258e-102">Enables the retrieval of metadata address information from the request message headers.</span></span>  
  
<span data-ttu-id="d258e-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="d258e-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="d258e-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="d258e-104">\<behaviors></span></span>  
<span data-ttu-id="d258e-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="d258e-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="d258e-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="d258e-106">\<behavior></span></span>  
<span data-ttu-id="d258e-107">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="d258e-107">\<useRequestHeadersForMetadataAddress></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d258e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d258e-108">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d258e-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d258e-109">Attributes and Elements</span></span>  
 <span data-ttu-id="d258e-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d258e-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d258e-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="d258e-111">Attributes</span></span>  
 <span data-ttu-id="d258e-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d258e-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d258e-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d258e-113">Child Elements</span></span>  
  
|<span data-ttu-id="d258e-114">Élément</span><span class="sxs-lookup"><span data-stu-id="d258e-114">Element</span></span>|<span data-ttu-id="d258e-115">Description</span><span class="sxs-lookup"><span data-stu-id="d258e-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d258e-116">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="d258e-116">\<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/defaultports.md)|<span data-ttu-id="d258e-117">Collection des ports par défaut répertoriant les points de terminaison de communication par défaut écoutés par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="d258e-117">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d258e-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d258e-118">Parent Elements</span></span>  
  
|<span data-ttu-id="d258e-119">Élément</span><span class="sxs-lookup"><span data-stu-id="d258e-119">Element</span></span>|<span data-ttu-id="d258e-120">Description</span><span class="sxs-lookup"><span data-stu-id="d258e-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d258e-121">\<behavior></span><span class="sxs-lookup"><span data-stu-id="d258e-121">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="d258e-122">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="d258e-122">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d258e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d258e-123">See also</span></span>
- <xref:System.ServiceModel.Configuration.UseRequestHeadersForMetadataAddressElement>
