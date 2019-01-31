---
title: <behaviors>
ms.date: 03/30/2017
ms.assetid: 0e5da4e6-1aa5-466c-924e-f10efee57f0b
ms.openlocfilehash: b9d30d7e1c9d211cd57982a0f03fe855a6b53c12
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55257916"
---
# <a name="behaviors"></a><span data-ttu-id="d8b18-101">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="d8b18-101">\<behaviors></span></span>
<span data-ttu-id="d8b18-102">Cet élément définit deux collections enfants nommées `endpointBehaviors` et `serviceBehaviors`.</span><span class="sxs-lookup"><span data-stu-id="d8b18-102">This element defines two child collections named `endpointBehaviors` and `serviceBehaviors`.</span></span>  <span data-ttu-id="d8b18-103">Chaque collection définit des éléments de comportement consommés respectivement par les points de terminaison et les services.</span><span class="sxs-lookup"><span data-stu-id="d8b18-103">Each collection defines behavior elements consumed by endpoints and services respectively.</span></span> <span data-ttu-id="d8b18-104">Chaque élément de comportement est identifié par son attribut `name` unique.</span><span class="sxs-lookup"><span data-stu-id="d8b18-104">Each behavior element is identified by its unique `name` attribute.</span></span> <span data-ttu-id="d8b18-105">Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d’avoir un nom.</span><span class="sxs-lookup"><span data-stu-id="d8b18-105">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="d8b18-106">Pour plus d’informations sur la configuration par défaut et les liaisons sans nom et les comportements, consultez [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="d8b18-106">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>  
  
 <span data-ttu-id="d8b18-107">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="d8b18-107">\<system.ServiceModel></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d8b18-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8b18-108">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
  </serviceBehaviors>
  <endpointBehaviors>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d8b18-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d8b18-109">Attributes and Elements</span></span>  
 <span data-ttu-id="d8b18-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d8b18-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d8b18-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="d8b18-111">Attributes</span></span>  
 <span data-ttu-id="d8b18-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d8b18-112">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d8b18-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d8b18-113">Child Elements</span></span>  
  
|<span data-ttu-id="d8b18-114">Élément</span><span class="sxs-lookup"><span data-stu-id="d8b18-114">Element</span></span>|<span data-ttu-id="d8b18-115">Description</span><span class="sxs-lookup"><span data-stu-id="d8b18-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d8b18-116">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="d8b18-116">\<endpointBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpointbehaviors.md)|<span data-ttu-id="d8b18-117">Cette section de configuration représente tous les comportements définis pour un point de terminaison spécifique.</span><span class="sxs-lookup"><span data-stu-id="d8b18-117">This configuration section represents all the behaviors defined for a specific endpoint.</span></span>|  
|[<span data-ttu-id="d8b18-118">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="d8b18-118">\<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicebehaviors.md)|<span data-ttu-id="d8b18-119">Cette section de configuration représente tous les comportements définis pour un service spécifique.</span><span class="sxs-lookup"><span data-stu-id="d8b18-119">This configuration section represents all the behaviors defined for a specific service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d8b18-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d8b18-120">Parent Elements</span></span>  
  
|<span data-ttu-id="d8b18-121">Élément</span><span class="sxs-lookup"><span data-stu-id="d8b18-121">Element</span></span>|<span data-ttu-id="d8b18-122">Description</span><span class="sxs-lookup"><span data-stu-id="d8b18-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d8b18-123">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="d8b18-123">\<system.serviceModel></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)|<span data-ttu-id="d8b18-124">Élément racine de tous les éléments de configuration Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="d8b18-124">The root element of all Windows Communication Foundation (WCF) configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d8b18-125">Notes</span><span class="sxs-lookup"><span data-stu-id="d8b18-125">Remarks</span></span>  
 <span data-ttu-id="d8b18-126">Vous pouvez utiliser l’élément `<remove>` pour supprimer un comportement particulier de la collection.</span><span class="sxs-lookup"><span data-stu-id="d8b18-126">You can use the `<remove>` element to remove a particular behavior from the collection.</span></span> <span data-ttu-id="d8b18-127">Pour cela, fournissez le nom du comportement à supprimer dans l'attribut `name` de l'élément `<remove>`.</span><span class="sxs-lookup"><span data-stu-id="d8b18-127">To do so, simply supply the name of the behavior to remove in the `name` attribute of the `<remove>` element.</span></span>  <span data-ttu-id="d8b18-128">Vous pouvez également utiliser l’élément `<clear>` pour vous assurer qu’une collection de comportements est vide au démarrage en supprimant tout le contenu de la collection.</span><span class="sxs-lookup"><span data-stu-id="d8b18-128">You can also use the `<clear>` element to insure that a behavior collection starts empty by clearing out all the content of the collection.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8b18-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8b18-129">See also</span></span>
- <xref:System.ServiceModel.Configuration.BehaviorsSection>
- <xref:System.ServiceModel.Configuration.EndpointBehaviorElementCollection>
- <xref:System.ServiceModel.Configuration.EndpointBehaviorElement>
- <xref:System.ServiceModel.Configuration.ServiceBehaviorElementCollection>
- <xref:System.ServiceModel.Configuration.ServiceBehaviorElement>
- [<span data-ttu-id="d8b18-130">Configuration et extension de l’exécution à l’aide de comportements</span><span class="sxs-lookup"><span data-stu-id="d8b18-130">Configuring and Extending the Runtime with Behaviors</span></span>](../../../../../docs/framework/wcf/extending/configuring-and-extending-the-runtime-with-behaviors.md)
- [<span data-ttu-id="d8b18-131">Configuration des comportements clients</span><span class="sxs-lookup"><span data-stu-id="d8b18-131">Configuring Client Behaviors</span></span>](../../../../../docs/framework/wcf/configuring-client-behaviors.md)
- [<span data-ttu-id="d8b18-132">Spécification du comportement du client au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="d8b18-132">Specifying Client Run-Time Behavior</span></span>](../../../../../docs/framework/wcf/specifying-client-run-time-behavior.md)
- [<span data-ttu-id="d8b18-133">Spécification du comportement du service au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="d8b18-133">Specifying Service Run-Time Behavior</span></span>](../../../../../docs/framework/wcf/specifying-service-run-time-behavior.md)
- [<span data-ttu-id="d8b18-134">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="d8b18-134">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
