---
title: <defaultPorts>
ms.date: 03/30/2017
ms.assetid: 725d4ee5-bd46-4f0e-9c20-30ba75d6eb2c
ms.openlocfilehash: 4d7fdfb1cccb14f03d11864f1939cb578c79880a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704113"
---
# <a name="defaultports"></a><span data-ttu-id="1f1b4-101">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="1f1b4-101">\<defaultPorts></span></span>
<span data-ttu-id="1f1b4-102">Collection des ports par défaut répertoriant les points de terminaison de communication par défaut écoutés par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="1f1b4-102">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>  
  
<span data-ttu-id="1f1b4-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="1f1b4-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="1f1b4-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="1f1b4-104">\<behaviors></span></span>  
<span data-ttu-id="1f1b4-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="1f1b4-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="1f1b4-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="1f1b4-106">\<behavior></span></span>  
<span data-ttu-id="1f1b4-107">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="1f1b4-107">\<useRequestHeadersForMetadataAddress></span></span>  
<span data-ttu-id="1f1b4-108">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="1f1b4-108">\<defaultPorts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1f1b4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f1b4-109">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1f1b4-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1f1b4-110">Attributes and Elements</span></span>  
 <span data-ttu-id="1f1b4-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1f1b4-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1f1b4-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="1f1b4-112">Attributes</span></span>  
 <span data-ttu-id="1f1b4-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1f1b4-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="1f1b4-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1f1b4-114">Child Elements</span></span>  
  
|<span data-ttu-id="1f1b4-115">Élément</span><span class="sxs-lookup"><span data-stu-id="1f1b4-115">Element</span></span>|<span data-ttu-id="1f1b4-116">Description</span><span class="sxs-lookup"><span data-stu-id="1f1b4-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1f1b4-117">\<Ajouter > de \<defaultPorts ></span><span class="sxs-lookup"><span data-stu-id="1f1b4-117">\<add> of \<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-defaultports.md)|<span data-ttu-id="1f1b4-118">Point de terminaison de communication par défaut écouté par l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="1f1b4-118">A default communications endpoint that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1f1b4-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1f1b4-119">Parent Elements</span></span>  
  
|<span data-ttu-id="1f1b4-120">Élément</span><span class="sxs-lookup"><span data-stu-id="1f1b4-120">Element</span></span>|<span data-ttu-id="1f1b4-121">Description</span><span class="sxs-lookup"><span data-stu-id="1f1b4-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1f1b4-122">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="1f1b4-122">\<useRequestHeadersForMetadataAddress></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/userequestheadersformetadataaddress.md)|<span data-ttu-id="1f1b4-123">Liste de ports par défaut.</span><span class="sxs-lookup"><span data-stu-id="1f1b4-123">A list of default ports.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1f1b4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f1b4-124">See also</span></span>

- <xref:System.ServiceModel.Configuration.DefaultPortElementCollection>
