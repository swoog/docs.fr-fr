---
title: <baseAddresses>
ms.date: 03/30/2017
ms.assetid: 78918102-2898-46e0-9ea8-6b8afe65603e
ms.openlocfilehash: dc4b31e729f9037da101bdf3e6cde28e91b1a070
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55277015"
---
# <a name="baseaddresses"></a><span data-ttu-id="a33ae-101">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="a33ae-101">\<baseAddresses></span></span>
<span data-ttu-id="a33ae-102">Représente une collection d’éléments `baseAddress`, qui sont les adresses de base d’un hôte de service dans un environnement auto-hébergé.</span><span class="sxs-lookup"><span data-stu-id="a33ae-102">Represents a collection of `baseAddress` elements, which are base addresses for a service host in a self-hosted environment.</span></span> <span data-ttu-id="a33ae-103">Si une adresse de base est présente, les points de terminaison peuvent être configurés avec des adresses relatives à l'adresse de base.</span><span class="sxs-lookup"><span data-stu-id="a33ae-103">If a base address is present, endpoints can be configured with addresses relative to the base address.</span></span>  
  
 <span data-ttu-id="a33ae-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="a33ae-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="a33ae-105">\<client></span><span class="sxs-lookup"><span data-stu-id="a33ae-105">\<client></span></span>  
<span data-ttu-id="a33ae-106">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="a33ae-106">\<endpoint></span></span>  
<span data-ttu-id="a33ae-107">\<host></span><span class="sxs-lookup"><span data-stu-id="a33ae-107">\<host></span></span>  
<span data-ttu-id="a33ae-108">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="a33ae-108">\<baseAddresses></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a33ae-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a33ae-109">Syntax</span></span>  
  
```xml  
<baseAddresses>
  <add baseAddress="string" />
</baseAddresses>
```  
  
## <a name="type"></a><span data-ttu-id="a33ae-110">Type</span><span class="sxs-lookup"><span data-stu-id="a33ae-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a33ae-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a33ae-111">Attributes and Elements</span></span>  
 <span data-ttu-id="a33ae-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a33ae-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a33ae-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="a33ae-113">Attributes</span></span>  
 <span data-ttu-id="a33ae-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a33ae-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="a33ae-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a33ae-115">Child Elements</span></span>  
  
|<span data-ttu-id="a33ae-116">Élément</span><span class="sxs-lookup"><span data-stu-id="a33ae-116">Element</span></span>|<span data-ttu-id="a33ae-117">Description</span><span class="sxs-lookup"><span data-stu-id="a33ae-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a33ae-118">\<add></span><span class="sxs-lookup"><span data-stu-id="a33ae-118">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-baseaddresses.md)|<span data-ttu-id="a33ae-119">Élément de configuration qui spécifie les adresses de base utilisées par l'hôte de service.</span><span class="sxs-lookup"><span data-stu-id="a33ae-119">A configuration element that specifies the base addresses used by the service host.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a33ae-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a33ae-120">Parent Elements</span></span>  
  
|<span data-ttu-id="a33ae-121">Élément</span><span class="sxs-lookup"><span data-stu-id="a33ae-121">Element</span></span>|<span data-ttu-id="a33ae-122">Description</span><span class="sxs-lookup"><span data-stu-id="a33ae-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a33ae-123">\<host></span><span class="sxs-lookup"><span data-stu-id="a33ae-123">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="a33ae-124">Élément de configuration qui spécifie des paramètres pour un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="a33ae-124">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a33ae-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a33ae-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>
- [<span data-ttu-id="a33ae-126">Hébergement</span><span class="sxs-lookup"><span data-stu-id="a33ae-126">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
