---
title: <host>
ms.date: 03/30/2017
ms.assetid: be566d55-9d50-4b2e-985d-52a5cc26cbbb
ms.openlocfilehash: 3d1f7774f61060880a5c3b0327bdd6c2cc4dd74e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61746715"
---
# <a name="host"></a><span data-ttu-id="43ecb-101">\<host></span><span class="sxs-lookup"><span data-stu-id="43ecb-101">\<host></span></span>
<span data-ttu-id="43ecb-102">Spécifie les paramètres d'un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="43ecb-102">Specifies settings for a service host.</span></span>  
  
 <span data-ttu-id="43ecb-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="43ecb-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="43ecb-104">\<services></span><span class="sxs-lookup"><span data-stu-id="43ecb-104">\<services></span></span>  
<span data-ttu-id="43ecb-105">\<service></span><span class="sxs-lookup"><span data-stu-id="43ecb-105">\<service></span></span>  
<span data-ttu-id="43ecb-106">\<host></span><span class="sxs-lookup"><span data-stu-id="43ecb-106">\<host></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="43ecb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43ecb-107">Syntax</span></span>  
  
```xml  
<host>
  <baseAddresses>
    <add baseAddress="string" />
  </baseAddresses>
  <timeOuts closeTimeout="TimeSpan"
            openTimeout="TimeSpan" />
</host>
```  
  
## <a name="type"></a><span data-ttu-id="43ecb-108">Type</span><span class="sxs-lookup"><span data-stu-id="43ecb-108">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="43ecb-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="43ecb-109">Attributes and Elements</span></span>  
 <span data-ttu-id="43ecb-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="43ecb-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="43ecb-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="43ecb-111">Attributes</span></span>  
 <span data-ttu-id="43ecb-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="43ecb-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="43ecb-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="43ecb-113">Child Elements</span></span>  
  
|<span data-ttu-id="43ecb-114">Élément</span><span class="sxs-lookup"><span data-stu-id="43ecb-114">Element</span></span>|<span data-ttu-id="43ecb-115">Description</span><span class="sxs-lookup"><span data-stu-id="43ecb-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="43ecb-116">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="43ecb-116">\<baseAddresses></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/baseaddresses.md)|<span data-ttu-id="43ecb-117">Collection d’éléments `baseAddress` qui spécifie les adresses de base utilisées par l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="43ecb-117">A collection of `baseAddress` elements that specifies the base addresses used by the service host.</span></span>|  
|[<span data-ttu-id="43ecb-118">\<timeOuts></span><span class="sxs-lookup"><span data-stu-id="43ecb-118">\<timeOuts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/timeouts.md)|<span data-ttu-id="43ecb-119">Élément de configuration qui spécifie la durée d'ouverture ou de fermeture autorisée de l'hôte de service.</span><span class="sxs-lookup"><span data-stu-id="43ecb-119">A configuration element that specifies the interval of time allowed for the service host to open or close.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="43ecb-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="43ecb-120">Parent Elements</span></span>  
  
|<span data-ttu-id="43ecb-121">Élément</span><span class="sxs-lookup"><span data-stu-id="43ecb-121">Element</span></span>|<span data-ttu-id="43ecb-122">Description</span><span class="sxs-lookup"><span data-stu-id="43ecb-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="43ecb-123">\<service></span><span class="sxs-lookup"><span data-stu-id="43ecb-123">\<service></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/service.md)|<span data-ttu-id="43ecb-124">Spécifie les paramètres pour un service Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="43ecb-124">Specifies the settings for a Windows Communication Foundation (WCF) service.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="43ecb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43ecb-125">See also</span></span>

- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- [<span data-ttu-id="43ecb-126">Hébergement</span><span class="sxs-lookup"><span data-stu-id="43ecb-126">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
