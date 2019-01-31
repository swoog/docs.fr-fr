---
title: <defaultPorts>
ms.date: 03/30/2017
ms.assetid: 725d4ee5-bd46-4f0e-9c20-30ba75d6eb2c
ms.openlocfilehash: 595970a56e05c4fc1c9b2c0eb669ec3b3a120fe1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55262378"
---
# <a name="defaultports"></a><span data-ttu-id="54e1d-101">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="54e1d-101">\<defaultPorts></span></span>
<span data-ttu-id="54e1d-102">Collection des ports par défaut répertoriant les points de terminaison de communication par défaut écoutés par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="54e1d-102">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>  
  
<span data-ttu-id="54e1d-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="54e1d-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="54e1d-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="54e1d-104">\<behaviors></span></span>  
<span data-ttu-id="54e1d-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="54e1d-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="54e1d-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="54e1d-106">\<behavior></span></span>  
<span data-ttu-id="54e1d-107">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="54e1d-107">\<useRequestHeadersForMetadataAddress></span></span>  
<span data-ttu-id="54e1d-108">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="54e1d-108">\<defaultPorts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="54e1d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54e1d-109">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="54e1d-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="54e1d-110">Attributes and Elements</span></span>  
 <span data-ttu-id="54e1d-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="54e1d-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="54e1d-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="54e1d-112">Attributes</span></span>  
 <span data-ttu-id="54e1d-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="54e1d-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="54e1d-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="54e1d-114">Child Elements</span></span>  
  
|<span data-ttu-id="54e1d-115">Élément</span><span class="sxs-lookup"><span data-stu-id="54e1d-115">Element</span></span>|<span data-ttu-id="54e1d-116">Description</span><span class="sxs-lookup"><span data-stu-id="54e1d-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="54e1d-117">\<Ajouter > de \<defaultPorts ></span><span class="sxs-lookup"><span data-stu-id="54e1d-117">\<add> of \<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-defaultports.md)|<span data-ttu-id="54e1d-118">Point de terminaison de communication par défaut écouté par l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="54e1d-118">A default communications endpoint that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="54e1d-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="54e1d-119">Parent Elements</span></span>  
  
|<span data-ttu-id="54e1d-120">Élément</span><span class="sxs-lookup"><span data-stu-id="54e1d-120">Element</span></span>|<span data-ttu-id="54e1d-121">Description</span><span class="sxs-lookup"><span data-stu-id="54e1d-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="54e1d-122">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="54e1d-122">\<useRequestHeadersForMetadataAddress></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/userequestheadersformetadataaddress.md)|<span data-ttu-id="54e1d-123">Liste de ports par défaut.</span><span class="sxs-lookup"><span data-stu-id="54e1d-123">A list of default ports.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="54e1d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54e1d-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.DefaultPortElementCollection>
