---
title: <host>
ms.date: 03/30/2017
ms.assetid: be566d55-9d50-4b2e-985d-52a5cc26cbbb
ms.openlocfilehash: 8a8f9db96281d8d775ff5c2923018228b3a9c1e5
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55269027"
---
# <a name="host"></a><span data-ttu-id="6db89-101">\<host></span><span class="sxs-lookup"><span data-stu-id="6db89-101">\<host></span></span>
<span data-ttu-id="6db89-102">Spécifie les paramètres d'un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="6db89-102">Specifies settings for a service host.</span></span>  
  
 <span data-ttu-id="6db89-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="6db89-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="6db89-104">\<services></span><span class="sxs-lookup"><span data-stu-id="6db89-104">\<services></span></span>  
<span data-ttu-id="6db89-105">\<service></span><span class="sxs-lookup"><span data-stu-id="6db89-105">\<service></span></span>  
<span data-ttu-id="6db89-106">\<host></span><span class="sxs-lookup"><span data-stu-id="6db89-106">\<host></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6db89-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6db89-107">Syntax</span></span>  
  
```xml  
<host>
  <baseAddresses>
    <add baseAddress="string" />
  </baseAddresses>
  <timeOuts closeTimeout="TimeSpan"
            openTimeout="TimeSpan" />
</host>
```  
  
## <a name="type"></a><span data-ttu-id="6db89-108">Type</span><span class="sxs-lookup"><span data-stu-id="6db89-108">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6db89-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6db89-109">Attributes and Elements</span></span>  
 <span data-ttu-id="6db89-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6db89-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6db89-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="6db89-111">Attributes</span></span>  
 <span data-ttu-id="6db89-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6db89-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="6db89-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6db89-113">Child Elements</span></span>  
  
|<span data-ttu-id="6db89-114">Élément</span><span class="sxs-lookup"><span data-stu-id="6db89-114">Element</span></span>|<span data-ttu-id="6db89-115">Description</span><span class="sxs-lookup"><span data-stu-id="6db89-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6db89-116">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="6db89-116">\<baseAddresses></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/baseaddresses.md)|<span data-ttu-id="6db89-117">Collection d’éléments `baseAddress` qui spécifie les adresses de base utilisées par l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="6db89-117">A collection of `baseAddress` elements that specifies the base addresses used by the service host.</span></span>|  
|[<span data-ttu-id="6db89-118">\<timeOuts></span><span class="sxs-lookup"><span data-stu-id="6db89-118">\<timeOuts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/timeouts.md)|<span data-ttu-id="6db89-119">Élément de configuration qui spécifie la durée d'ouverture ou de fermeture autorisée de l'hôte de service.</span><span class="sxs-lookup"><span data-stu-id="6db89-119">A configuration element that specifies the interval of time allowed for the service host to open or close.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6db89-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6db89-120">Parent Elements</span></span>  
  
|<span data-ttu-id="6db89-121">Élément</span><span class="sxs-lookup"><span data-stu-id="6db89-121">Element</span></span>|<span data-ttu-id="6db89-122">Description</span><span class="sxs-lookup"><span data-stu-id="6db89-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6db89-123">\<service></span><span class="sxs-lookup"><span data-stu-id="6db89-123">\<service></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/service.md)|<span data-ttu-id="6db89-124">Spécifie les paramètres pour un service Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="6db89-124">Specifies the settings for a Windows Communication Foundation (WCF) service.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6db89-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6db89-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- [<span data-ttu-id="6db89-126">Hébergement</span><span class="sxs-lookup"><span data-stu-id="6db89-126">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
