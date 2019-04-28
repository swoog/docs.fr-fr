---
title: <baseAddresses>
ms.date: 03/30/2017
ms.assetid: 78918102-2898-46e0-9ea8-6b8afe65603e
ms.openlocfilehash: 7d0afd638e9a311b69ff47b6789d5fde093945ba
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61673522"
---
# <a name="baseaddresses"></a><span data-ttu-id="fa1ef-101">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="fa1ef-101">\<baseAddresses></span></span>
<span data-ttu-id="fa1ef-102">Représente une collection d’éléments `baseAddress`, qui sont les adresses de base d’un hôte de service dans un environnement auto-hébergé.</span><span class="sxs-lookup"><span data-stu-id="fa1ef-102">Represents a collection of `baseAddress` elements, which are base addresses for a service host in a self-hosted environment.</span></span> <span data-ttu-id="fa1ef-103">Si une adresse de base est présente, les points de terminaison peuvent être configurés avec des adresses relatives à l'adresse de base.</span><span class="sxs-lookup"><span data-stu-id="fa1ef-103">If a base address is present, endpoints can be configured with addresses relative to the base address.</span></span>  
  
 <span data-ttu-id="fa1ef-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="fa1ef-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="fa1ef-105">\<client></span><span class="sxs-lookup"><span data-stu-id="fa1ef-105">\<client></span></span>  
<span data-ttu-id="fa1ef-106">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="fa1ef-106">\<endpoint></span></span>  
<span data-ttu-id="fa1ef-107">\<host></span><span class="sxs-lookup"><span data-stu-id="fa1ef-107">\<host></span></span>  
<span data-ttu-id="fa1ef-108">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="fa1ef-108">\<baseAddresses></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa1ef-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa1ef-109">Syntax</span></span>  
  
```xml  
<baseAddresses>
  <add baseAddress="string" />
</baseAddresses>
```  
  
## <a name="type"></a><span data-ttu-id="fa1ef-110">Type</span><span class="sxs-lookup"><span data-stu-id="fa1ef-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fa1ef-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="fa1ef-111">Attributes and Elements</span></span>  
 <span data-ttu-id="fa1ef-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="fa1ef-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fa1ef-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="fa1ef-113">Attributes</span></span>  
 <span data-ttu-id="fa1ef-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fa1ef-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="fa1ef-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fa1ef-115">Child Elements</span></span>  
  
|<span data-ttu-id="fa1ef-116">Élément</span><span class="sxs-lookup"><span data-stu-id="fa1ef-116">Element</span></span>|<span data-ttu-id="fa1ef-117">Description</span><span class="sxs-lookup"><span data-stu-id="fa1ef-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fa1ef-118">\<add></span><span class="sxs-lookup"><span data-stu-id="fa1ef-118">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-baseaddresses.md)|<span data-ttu-id="fa1ef-119">Élément de configuration qui spécifie les adresses de base utilisées par l'hôte de service.</span><span class="sxs-lookup"><span data-stu-id="fa1ef-119">A configuration element that specifies the base addresses used by the service host.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="fa1ef-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fa1ef-120">Parent Elements</span></span>  
  
|<span data-ttu-id="fa1ef-121">Élément</span><span class="sxs-lookup"><span data-stu-id="fa1ef-121">Element</span></span>|<span data-ttu-id="fa1ef-122">Description</span><span class="sxs-lookup"><span data-stu-id="fa1ef-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fa1ef-123">\<host></span><span class="sxs-lookup"><span data-stu-id="fa1ef-123">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="fa1ef-124">Élément de configuration qui spécifie des paramètres pour un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="fa1ef-124">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="fa1ef-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa1ef-125">See also</span></span>

- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>
- [<span data-ttu-id="fa1ef-126">Hébergement</span><span class="sxs-lookup"><span data-stu-id="fa1ef-126">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
