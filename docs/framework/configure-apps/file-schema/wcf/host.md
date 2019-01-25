---
title: '&lt;host&gt;'
ms.date: 03/30/2017
ms.assetid: be566d55-9d50-4b2e-985d-52a5cc26cbbb
ms.openlocfilehash: 1fb35058d407d0fbae78092bb4ccd45b0aaa40e6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702026"
---
# <a name="lthostgt"></a><span data-ttu-id="b3514-102">&lt;host&gt;</span><span class="sxs-lookup"><span data-stu-id="b3514-102">&lt;host&gt;</span></span>
<span data-ttu-id="b3514-103">Spécifie les paramètres d'un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="b3514-103">Specifies settings for a service host.</span></span>  
  
 <span data-ttu-id="b3514-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="b3514-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="b3514-105">\<services></span><span class="sxs-lookup"><span data-stu-id="b3514-105">\<services></span></span>  
<span data-ttu-id="b3514-106">\<service></span><span class="sxs-lookup"><span data-stu-id="b3514-106">\<service></span></span>  
<span data-ttu-id="b3514-107">\<host></span><span class="sxs-lookup"><span data-stu-id="b3514-107">\<host></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b3514-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3514-108">Syntax</span></span>  
  
```xml  
<host>
  <baseAddresses>
    <add baseAddress="string" />
  </baseAddresses>
  <timeOuts closeTimeout="TimeSpan"
            openTimeout="TimeSpan" />
</host>
```  
  
## <a name="type"></a><span data-ttu-id="b3514-109">Type</span><span class="sxs-lookup"><span data-stu-id="b3514-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b3514-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b3514-110">Attributes and Elements</span></span>  
 <span data-ttu-id="b3514-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b3514-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b3514-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="b3514-112">Attributes</span></span>  
 <span data-ttu-id="b3514-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b3514-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b3514-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b3514-114">Child Elements</span></span>  
  
|<span data-ttu-id="b3514-115">Élément</span><span class="sxs-lookup"><span data-stu-id="b3514-115">Element</span></span>|<span data-ttu-id="b3514-116">Description</span><span class="sxs-lookup"><span data-stu-id="b3514-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b3514-117">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="b3514-117">\<baseAddresses></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/baseaddresses.md)|<span data-ttu-id="b3514-118">Collection d’éléments `baseAddress` qui spécifie les adresses de base utilisées par l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="b3514-118">A collection of `baseAddress` elements that specifies the base addresses used by the service host.</span></span>|  
|[<span data-ttu-id="b3514-119">\<timeOuts></span><span class="sxs-lookup"><span data-stu-id="b3514-119">\<timeOuts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/timeouts.md)|<span data-ttu-id="b3514-120">Élément de configuration qui spécifie la durée d'ouverture ou de fermeture autorisée de l'hôte de service.</span><span class="sxs-lookup"><span data-stu-id="b3514-120">A configuration element that specifies the interval of time allowed for the service host to open or close.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b3514-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b3514-121">Parent Elements</span></span>  
  
|<span data-ttu-id="b3514-122">Élément</span><span class="sxs-lookup"><span data-stu-id="b3514-122">Element</span></span>|<span data-ttu-id="b3514-123">Description</span><span class="sxs-lookup"><span data-stu-id="b3514-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b3514-124">\<service></span><span class="sxs-lookup"><span data-stu-id="b3514-124">\<service></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/service.md)|<span data-ttu-id="b3514-125">Spécifie les paramètres pour un service Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="b3514-125">Specifies the settings for a Windows Communication Foundation (WCF) service.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b3514-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3514-126">See also</span></span>
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- [<span data-ttu-id="b3514-127">Hébergement</span><span class="sxs-lookup"><span data-stu-id="b3514-127">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
