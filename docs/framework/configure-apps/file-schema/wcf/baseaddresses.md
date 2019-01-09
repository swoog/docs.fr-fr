---
title: '&lt;Adresses de base&gt;'
ms.date: 03/30/2017
ms.assetid: 78918102-2898-46e0-9ea8-6b8afe65603e
ms.openlocfilehash: 0af5dee41c6adf560c90874e6e9a44b62c5decc6
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147346"
---
# <a name="ltbaseaddressesgt"></a><span data-ttu-id="f1806-102">&lt;Adresses de base&gt;</span><span class="sxs-lookup"><span data-stu-id="f1806-102">&lt;baseAddresses&gt;</span></span>
<span data-ttu-id="f1806-103">Représente une collection d’éléments `baseAddress`, qui sont les adresses de base d’un hôte de service dans un environnement auto-hébergé.</span><span class="sxs-lookup"><span data-stu-id="f1806-103">Represents a collection of `baseAddress` elements, which are base addresses for a service host in a self-hosted environment.</span></span> <span data-ttu-id="f1806-104">Si une adresse de base est présente, les points de terminaison peuvent être configurés avec des adresses relatives à l'adresse de base.</span><span class="sxs-lookup"><span data-stu-id="f1806-104">If a base address is present, endpoints can be configured with addresses relative to the base address.</span></span>  
  
 <span data-ttu-id="f1806-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="f1806-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="f1806-106">\<client></span><span class="sxs-lookup"><span data-stu-id="f1806-106">\<client></span></span>  
<span data-ttu-id="f1806-107">\<point de terminaison ></span><span class="sxs-lookup"><span data-stu-id="f1806-107">\<endpoint></span></span>  
<span data-ttu-id="f1806-108">\<hôte ></span><span class="sxs-lookup"><span data-stu-id="f1806-108">\<host></span></span>  
<span data-ttu-id="f1806-109">\<BaseAddress ></span><span class="sxs-lookup"><span data-stu-id="f1806-109">\<baseAddresses></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f1806-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1806-110">Syntax</span></span>  
  
```xml  
<baseAddresses>
  <add baseAddress="string" />
</baseAddresses>
```  
  
## <a name="type"></a><span data-ttu-id="f1806-111">Type</span><span class="sxs-lookup"><span data-stu-id="f1806-111">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f1806-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f1806-112">Attributes and Elements</span></span>  
 <span data-ttu-id="f1806-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f1806-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f1806-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="f1806-114">Attributes</span></span>  
 <span data-ttu-id="f1806-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f1806-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="f1806-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f1806-116">Child Elements</span></span>  
  
|<span data-ttu-id="f1806-117">Élément</span><span class="sxs-lookup"><span data-stu-id="f1806-117">Element</span></span>|<span data-ttu-id="f1806-118">Description</span><span class="sxs-lookup"><span data-stu-id="f1806-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f1806-119">\<add></span><span class="sxs-lookup"><span data-stu-id="f1806-119">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-baseaddresses.md)|<span data-ttu-id="f1806-120">Élément de configuration qui spécifie les adresses de base utilisées par l'hôte de service.</span><span class="sxs-lookup"><span data-stu-id="f1806-120">A configuration element that specifies the base addresses used by the service host.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f1806-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f1806-121">Parent Elements</span></span>  
  
|<span data-ttu-id="f1806-122">Élément</span><span class="sxs-lookup"><span data-stu-id="f1806-122">Element</span></span>|<span data-ttu-id="f1806-123">Description</span><span class="sxs-lookup"><span data-stu-id="f1806-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f1806-124">\<hôte ></span><span class="sxs-lookup"><span data-stu-id="f1806-124">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="f1806-125">Élément de configuration qui spécifie des paramètres pour un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="f1806-125">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f1806-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1806-126">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.HostElement>  
 <xref:System.ServiceModel.ServiceHost>  
 <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>  
 [<span data-ttu-id="f1806-127">Hébergement</span><span class="sxs-lookup"><span data-stu-id="f1806-127">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
