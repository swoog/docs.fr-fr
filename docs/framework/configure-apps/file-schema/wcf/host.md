---
title: '&lt;Ordinateur hôte&gt;'
ms.date: 03/30/2017
ms.assetid: be566d55-9d50-4b2e-985d-52a5cc26cbbb
ms.openlocfilehash: ec53568e9d1df9ebb04bc299f491e80674950c63
ms.sourcegitcommit: 22c3c8f74eaa138dbbbb02eb7d720fce87fc30a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2018
---
# <a name="lthostgt"></a><span data-ttu-id="80003-102">&lt;Ordinateur hôte&gt;</span><span class="sxs-lookup"><span data-stu-id="80003-102">&lt;host&gt;</span></span>
<span data-ttu-id="80003-103">Spécifie les paramètres d'un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="80003-103">Specifies settings for a service host.</span></span>  
  
 <span data-ttu-id="80003-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="80003-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="80003-105">\<services></span><span class="sxs-lookup"><span data-stu-id="80003-105">\<services></span></span>  
<span data-ttu-id="80003-106">\<service ></span><span class="sxs-lookup"><span data-stu-id="80003-106">\<service></span></span>  
<span data-ttu-id="80003-107">\<hôte ></span><span class="sxs-lookup"><span data-stu-id="80003-107">\<host></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80003-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80003-108">Syntax</span></span>  
  
```xml  
<host>
    <baseAddresses>  
        <add baseAddress="string" />  
    </baseAddresses>  
    <timeOuts closeTimeout="TimeSpan" openTimeout="TimeSpan">  
</host>  
```  
  
## <a name="type"></a><span data-ttu-id="80003-109">Type</span><span class="sxs-lookup"><span data-stu-id="80003-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="80003-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="80003-110">Attributes and Elements</span></span>  
 <span data-ttu-id="80003-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="80003-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="80003-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="80003-112">Attributes</span></span>  
 <span data-ttu-id="80003-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="80003-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="80003-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="80003-114">Child Elements</span></span>  
  
|<span data-ttu-id="80003-115">Élément</span><span class="sxs-lookup"><span data-stu-id="80003-115">Element</span></span>|<span data-ttu-id="80003-116">Description</span><span class="sxs-lookup"><span data-stu-id="80003-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="80003-117">\<baseAddresses ></span><span class="sxs-lookup"><span data-stu-id="80003-117">\<baseAddresses></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/baseaddresses.md)|<span data-ttu-id="80003-118">Collection d'éléments `baseAddress` qui spécifie les adresses de base utilisées par l'hôte de service.</span><span class="sxs-lookup"><span data-stu-id="80003-118">A collection of `baseAddress` elements that specifies the base addresses used by the service host.</span></span>|  
|[<span data-ttu-id="80003-119">\<délais d’attente ></span><span class="sxs-lookup"><span data-stu-id="80003-119">\<timeOuts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/timeouts.md)|<span data-ttu-id="80003-120">Élément de configuration qui spécifie la durée d'ouverture ou de fermeture autorisée de l'hôte de service.</span><span class="sxs-lookup"><span data-stu-id="80003-120">A configuration element that specifies the interval of time allowed for the service host to open or close.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="80003-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="80003-121">Parent Elements</span></span>  
  
|<span data-ttu-id="80003-122">Élément</span><span class="sxs-lookup"><span data-stu-id="80003-122">Element</span></span>|<span data-ttu-id="80003-123">Description</span><span class="sxs-lookup"><span data-stu-id="80003-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="80003-124">\<service></span><span class="sxs-lookup"><span data-stu-id="80003-124">\<service></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/service.md)|<span data-ttu-id="80003-125">Spécifie les paramètres pour un service Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="80003-125">Specifies the settings for a Windows Communication Foundation (WCF) service.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="80003-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80003-126">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.HostElement>  
 <xref:System.ServiceModel.ServiceHost>  
 [<span data-ttu-id="80003-127">Hébergement</span><span class="sxs-lookup"><span data-stu-id="80003-127">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
