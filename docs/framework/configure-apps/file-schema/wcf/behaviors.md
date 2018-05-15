---
title: '&lt;Comportements&gt;'
ms.date: 03/30/2017
ms.assetid: 0e5da4e6-1aa5-466c-924e-f10efee57f0b
ms.openlocfilehash: ca9cf5daa6590c14d4b5fd15c502d67af1f93b52
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltbehaviorsgt"></a><span data-ttu-id="4223b-102">&lt;Comportements&gt;</span><span class="sxs-lookup"><span data-stu-id="4223b-102">&lt;behaviors&gt;</span></span>
<span data-ttu-id="4223b-103">Cet élément définit deux collections enfants nommées `endpointBehaviors` et `serviceBehaviors`.</span><span class="sxs-lookup"><span data-stu-id="4223b-103">This element defines two child collections named `endpointBehaviors` and `serviceBehaviors`.</span></span>  <span data-ttu-id="4223b-104">Chaque collection définit des éléments de comportement consommés respectivement par les points de terminaison et les services.</span><span class="sxs-lookup"><span data-stu-id="4223b-104">Each collection defines behavior elements consumed by endpoints and services respectively.</span></span> <span data-ttu-id="4223b-105">Chaque élément de comportement est identifié par son attribut `name` unique.</span><span class="sxs-lookup"><span data-stu-id="4223b-105">Each behavior element is identified by its unique `name` attribute.</span></span> <span data-ttu-id="4223b-106">Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d'avoir un nom.</span><span class="sxs-lookup"><span data-stu-id="4223b-106">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="4223b-107">Pour plus d’informations sur la configuration par défaut et nommées liaisons et comportements, consultez [Configuration simplifiée](../../../../../docs/framework/wcf/simplified-configuration.md) et [simplifié la Configuration des Services WCF](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="4223b-107">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>  
  
 <span data-ttu-id="4223b-108">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="4223b-108">\<system.ServiceModel></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4223b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4223b-109">Syntax</span></span>  
  
```xml  
<behaviors>  
   <serviceBehaviors>  
   </serviceBehaviors>  
   <endpointBehaviors>  
   </endpointBehaviors>  
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4223b-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4223b-110">Attributes and Elements</span></span>  
 <span data-ttu-id="4223b-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4223b-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4223b-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="4223b-112">Attributes</span></span>  
 <span data-ttu-id="4223b-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="4223b-113">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4223b-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4223b-114">Child Elements</span></span>  
  
|<span data-ttu-id="4223b-115">Élément</span><span class="sxs-lookup"><span data-stu-id="4223b-115">Element</span></span>|<span data-ttu-id="4223b-116">Description</span><span class="sxs-lookup"><span data-stu-id="4223b-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4223b-117">\<endpointBehaviors ></span><span class="sxs-lookup"><span data-stu-id="4223b-117">\<endpointBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpointbehaviors.md)|<span data-ttu-id="4223b-118">Cette section de configuration représente tous les comportements définis pour un point de terminaison spécifique.</span><span class="sxs-lookup"><span data-stu-id="4223b-118">This configuration section represents all the behaviors defined for a specific endpoint.</span></span>|  
|[<span data-ttu-id="4223b-119">\<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="4223b-119">\<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicebehaviors.md)|<span data-ttu-id="4223b-120">Cette section de configuration représente tous les comportements définis pour un service spécifique.</span><span class="sxs-lookup"><span data-stu-id="4223b-120">This configuration section represents all the behaviors defined for a specific service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4223b-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4223b-121">Parent Elements</span></span>  
  
|<span data-ttu-id="4223b-122">Élément</span><span class="sxs-lookup"><span data-stu-id="4223b-122">Element</span></span>|<span data-ttu-id="4223b-123">Description</span><span class="sxs-lookup"><span data-stu-id="4223b-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4223b-124">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="4223b-124">\<system.serviceModel></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)|<span data-ttu-id="4223b-125">Élément racine de tous les éléments de configuration Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="4223b-125">The root element of all Windows Communication Foundation (WCF) configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4223b-126">Notes</span><span class="sxs-lookup"><span data-stu-id="4223b-126">Remarks</span></span>  
 <span data-ttu-id="4223b-127">Vous pouvez utiliser l'élément `<remove>` pour supprimer un comportement particulier de la collection.</span><span class="sxs-lookup"><span data-stu-id="4223b-127">You can use the `<remove>` element to remove a particular behavior from the collection.</span></span> <span data-ttu-id="4223b-128">Pour cela, fournissez le nom du comportement à supprimer dans l'attribut `name` de l'élément `<remove>`.</span><span class="sxs-lookup"><span data-stu-id="4223b-128">To do so, simply supply the name of the behavior to remove in the `name` attribute of the `<remove>` element.</span></span>  <span data-ttu-id="4223b-129">Vous pouvez également utiliser l'élément `<clear>` pour vous assurer qu'une collection de comportements est vide au démarrage en supprimant tout le contenu de la collection.</span><span class="sxs-lookup"><span data-stu-id="4223b-129">You can also use the `<clear>` element to insure that a behavior collection starts empty by clearing out all the content of the collection.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4223b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4223b-130">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.BehaviorsSection>  
 <xref:System.ServiceModel.Configuration.EndpointBehaviorElementCollection>  
 <xref:System.ServiceModel.Configuration.EndpointBehaviorElement>  
 <xref:System.ServiceModel.Configuration.ServiceBehaviorElementCollection>  
 <xref:System.ServiceModel.Configuration.ServiceBehaviorElement>  
 [<span data-ttu-id="4223b-131">Configuration et extension de l’exécution à l’aide de comportements</span><span class="sxs-lookup"><span data-stu-id="4223b-131">Configuring and Extending the Runtime with Behaviors</span></span>](../../../../../docs/framework/wcf/extending/configuring-and-extending-the-runtime-with-behaviors.md)  
 [<span data-ttu-id="4223b-132">Configuration des comportements clients</span><span class="sxs-lookup"><span data-stu-id="4223b-132">Configuring Client Behaviors</span></span>](../../../../../docs/framework/wcf/configuring-client-behaviors.md)  
 [<span data-ttu-id="4223b-133">Spécification du comportement du client au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="4223b-133">Specifying Client Run-Time Behavior</span></span>](../../../../../docs/framework/wcf/specifying-client-run-time-behavior.md)  
 [<span data-ttu-id="4223b-134">Spécification du comportement du service au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="4223b-134">Specifying Service Run-Time Behavior</span></span>](../../../../../docs/framework/wcf/specifying-service-run-time-behavior.md)  
 [<span data-ttu-id="4223b-135">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="4223b-135">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
