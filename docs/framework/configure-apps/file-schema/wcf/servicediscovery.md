---
title: <serviceDiscovery>
ms.date: 03/30/2017
ms.assetid: a3c68a4a-fc95-43c5-aacb-785936c0cf39
ms.openlocfilehash: 564410fdc4085cc3ed14c394006551cddb028910
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57373749"
---
# <a name="servicediscovery"></a><span data-ttu-id="247d8-101">\<serviceDiscovery></span><span class="sxs-lookup"><span data-stu-id="247d8-101">\<serviceDiscovery></span></span>
<span data-ttu-id="247d8-102">Spécifie la fonctionnalité de découverte des points de terminaison de service.</span><span class="sxs-lookup"><span data-stu-id="247d8-102">Specifies the discoverability of service endpoints.</span></span>  
  
 <span data-ttu-id="247d8-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="247d8-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="247d8-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="247d8-104">\<behaviors></span></span>  
<span data-ttu-id="247d8-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="247d8-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="247d8-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="247d8-106">\<behavior></span></span>  
<span data-ttu-id="247d8-107">\<serviceDiscovery></span><span class="sxs-lookup"><span data-stu-id="247d8-107">\<serviceDiscovery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="247d8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="247d8-108">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <serviceDiscovery>
        <announcementEndpoints>
          <endpoint name="String"
                    kind="Type" />
        </announcementEndpoints>
        <discoveryEndpoints>
          <endpoint name="String"
                    kind="Type" />
        </discoveryEndpoints>
      </serviceDiscovery>
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="247d8-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="247d8-109">Attributes and Elements</span></span>  
 <span data-ttu-id="247d8-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="247d8-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="247d8-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="247d8-111">Attributes</span></span>  
 <span data-ttu-id="247d8-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="247d8-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="247d8-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="247d8-113">Child Elements</span></span>  
  
|<span data-ttu-id="247d8-114">Élément</span><span class="sxs-lookup"><span data-stu-id="247d8-114">Element</span></span>|<span data-ttu-id="247d8-115">Description</span><span class="sxs-lookup"><span data-stu-id="247d8-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="247d8-116">\<announcementEndpoint></span><span class="sxs-lookup"><span data-stu-id="247d8-116">\<announcementEndpoint></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md)|<span data-ttu-id="247d8-117">Collection de points de terminaison d’annonce.</span><span class="sxs-lookup"><span data-stu-id="247d8-117">A collection of announcement endpoints.</span></span> <span data-ttu-id="247d8-118">Cette section permet de spécifier les points de terminaison à utiliser pour l'envoi de messages d'annonce.</span><span class="sxs-lookup"><span data-stu-id="247d8-118">Use this section to specify the endpoints to use for sending announcement messages.</span></span>|  
|[<span data-ttu-id="247d8-119">\<discoveryEndpoint></span><span class="sxs-lookup"><span data-stu-id="247d8-119">\<discoveryEndpoint></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md)|<span data-ttu-id="247d8-120">Collection de points de terminaison de découverte.</span><span class="sxs-lookup"><span data-stu-id="247d8-120">A collection of discovery endpoints.</span></span> <span data-ttu-id="247d8-121">Cette section permet de spécifier les points de terminaison sur lesquels écouter les messages de découverte.</span><span class="sxs-lookup"><span data-stu-id="247d8-121">Use this section to specify the endpoints on which to listen for the discovery messages.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="247d8-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="247d8-122">Parent Elements</span></span>  
  
|<span data-ttu-id="247d8-123">Élément</span><span class="sxs-lookup"><span data-stu-id="247d8-123">Element</span></span>|<span data-ttu-id="247d8-124">Description</span><span class="sxs-lookup"><span data-stu-id="247d8-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="247d8-125">\<behavior></span><span class="sxs-lookup"><span data-stu-id="247d8-125">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="247d8-126">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="247d8-126">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="247d8-127">Notes</span><span class="sxs-lookup"><span data-stu-id="247d8-127">Remarks</span></span>  
 <span data-ttu-id="247d8-128">Lorsqu'il est ajouté à la configuration de comportement du service, cet élément de configuration rend tous les points de terminaison de ce service détectables.</span><span class="sxs-lookup"><span data-stu-id="247d8-128">When added to the service’s behavior configuration, this configuration element makes all of the endpoints of that service discoverable.</span></span> <span data-ttu-id="247d8-129">Vous pouvez configurer davantage de fonctionnalités de découverte de tels points de terminaison à l’aide de la [ \<discoveryEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) ou [ \<announcementEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="247d8-129">You can further configure the discovery features of such endpoints by using the [\<discoveryEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) or [\<announcementEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) child elements.</span></span> <span data-ttu-id="247d8-130">Utiliser le [ \<announcementEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) section pour configurer les annonces en spécifiant la configuration de point de terminaison à utiliser pour envoyer des annonces de service (en ligne/Hello et hors connexion/Bye).</span><span class="sxs-lookup"><span data-stu-id="247d8-130">Use the [\<announcementEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) section to configure the announcements by specifying the endpoint configuration to be use to send service announcements (online/Hello and offline/Bye).</span></span> <span data-ttu-id="247d8-131">Utilisez le [ \<discoveryEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) section pour spécifier manuellement le point de terminaison d’écoute pour les messages de découverte.</span><span class="sxs-lookup"><span data-stu-id="247d8-131">Use the [\<discoveryEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) section to manually specify the endpoint on which to listen for the discovery messages.</span></span>  
  
## <a name="example"></a><span data-ttu-id="247d8-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="247d8-132">Example</span></span>  
 <span data-ttu-id="247d8-133">L'exemple de configuration suivant spécifie que CalculatorService doit être détectable et indique éventuellement le point de terminaison d'annonce à utiliser.</span><span class="sxs-lookup"><span data-stu-id="247d8-133">The following configuration example specifies that the CalculatorService to be discoverable, and optionally specifies the announcement endpoint to be used.</span></span>  
  
```xml  
<services>
  <service name="CalculatorService"
           behaviorConfiguration="CalculatorServiceBehavior">
    ...
  </service>
</services>
<behaviors>
  <serviceBehaviors>
    <behavior name="CalculatorServiceBehavior">
      <serviceDiscovery>
        <announcementEndpoints>
          <endpoint name="udpEndpoint"
                    kind="udpAnnouncementEndpoint" />
        </announcementEndpoints>
      </serviceDiscovery>
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="247d8-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="247d8-134">See also</span></span>
- <xref:System.ServiceModel.Discovery.ServiceDiscoveryBehavior>
