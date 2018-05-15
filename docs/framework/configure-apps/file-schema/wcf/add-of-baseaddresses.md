---
title: '&lt;add&gt; de &lt;baseAddress&gt;'
ms.date: 03/30/2017
ms.assetid: 1bd7426f-5f4f-43fc-b8e9-de842219aa32
ms.openlocfilehash: 3f1b7e8f1f4ab8542270d459ce5020ce4320eea9
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltaddgt-of-ltbaseaddressesgt"></a><span data-ttu-id="a1163-102">&lt;add&gt; de &lt;baseAddress&gt;</span><span class="sxs-lookup"><span data-stu-id="a1163-102">&lt;add&gt; of &lt;baseAddresses&gt;</span></span>
<span data-ttu-id="a1163-103">Représente un élément de configuration qui spécifie les adresses de base utilisées par l'hôte de service.</span><span class="sxs-lookup"><span data-stu-id="a1163-103">Represents a configuration element that specifies the base addresses used by the service host.</span></span>  
  
 <span data-ttu-id="a1163-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="a1163-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="a1163-105">\<client></span><span class="sxs-lookup"><span data-stu-id="a1163-105">\<client></span></span>  
<span data-ttu-id="a1163-106">\<point de terminaison ></span><span class="sxs-lookup"><span data-stu-id="a1163-106">\<endpoint></span></span>  
<span data-ttu-id="a1163-107">\<hôte ></span><span class="sxs-lookup"><span data-stu-id="a1163-107">\<host></span></span>  
<span data-ttu-id="a1163-108">\<baseAddresses ></span><span class="sxs-lookup"><span data-stu-id="a1163-108">\<baseAddresses></span></span>  
<span data-ttu-id="a1163-109">\<baseAddress ></span><span class="sxs-lookup"><span data-stu-id="a1163-109">\<baseAddress></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1163-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1163-110">Syntax</span></span>  
  
```xml  
<add baseAddress="string" />  
```  
  
## <a name="type"></a><span data-ttu-id="a1163-111">Type</span><span class="sxs-lookup"><span data-stu-id="a1163-111">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a1163-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a1163-112">Attributes and Elements</span></span>  
 <span data-ttu-id="a1163-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a1163-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a1163-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="a1163-114">Attributes</span></span>  
  
|<span data-ttu-id="a1163-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="a1163-115">Attribute</span></span>|<span data-ttu-id="a1163-116">Description</span><span class="sxs-lookup"><span data-stu-id="a1163-116">Description</span></span>|  
|---------------|-----------------|  
|`baseAddress`|<span data-ttu-id="a1163-117">Chaîne indiquant une adresse de base utilisée par l'hôte de service.</span><span class="sxs-lookup"><span data-stu-id="a1163-117">A string that specifies a base address used by the service host.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a1163-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a1163-118">Child Elements</span></span>  
 <span data-ttu-id="a1163-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a1163-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a1163-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a1163-120">Parent Elements</span></span>  
  
|<span data-ttu-id="a1163-121">Élément</span><span class="sxs-lookup"><span data-stu-id="a1163-121">Element</span></span>|<span data-ttu-id="a1163-122">Description</span><span class="sxs-lookup"><span data-stu-id="a1163-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a1163-123">\<baseAddresses ></span><span class="sxs-lookup"><span data-stu-id="a1163-123">\<baseAddresses></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/baseaddresses.md)|<span data-ttu-id="a1163-124">Collection d'éléments `baseAddress`.</span><span class="sxs-lookup"><span data-stu-id="a1163-124">A collection of `baseAddress` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a1163-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1163-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.HostElement>  
 <xref:System.ServiceModel.ServiceHost>  
 <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>  
 [<span data-ttu-id="a1163-126">Hébergement</span><span class="sxs-lookup"><span data-stu-id="a1163-126">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
