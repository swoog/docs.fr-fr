---
title: '&lt;serviceDiscovery&gt;'
ms.date: 03/30/2017
ms.assetid: a3c68a4a-fc95-43c5-aacb-785936c0cf39
ms.openlocfilehash: 2b3061274ef670ccd672c3155ca7285d567834bd
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146899"
---
# <a name="ltservicediscoverygt"></a><span data-ttu-id="46b95-102">&lt;serviceDiscovery&gt;</span><span class="sxs-lookup"><span data-stu-id="46b95-102">&lt;serviceDiscovery&gt;</span></span>
<span data-ttu-id="46b95-103">Spécifie la fonctionnalité de découverte des points de terminaison de service.</span><span class="sxs-lookup"><span data-stu-id="46b95-103">Specifies the discoverability of service endpoints.</span></span>  
  
 <span data-ttu-id="46b95-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="46b95-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="46b95-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="46b95-105">\<behaviors></span></span>  
<span data-ttu-id="46b95-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="46b95-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="46b95-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="46b95-107">\<behavior></span></span>  
<span data-ttu-id="46b95-108">\<serviceDiscovery ></span><span class="sxs-lookup"><span data-stu-id="46b95-108">\<serviceDiscovery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46b95-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46b95-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="46b95-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="46b95-110">Attributes and Elements</span></span>  
 <span data-ttu-id="46b95-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="46b95-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="46b95-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="46b95-112">Attributes</span></span>  
 <span data-ttu-id="46b95-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="46b95-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="46b95-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="46b95-114">Child Elements</span></span>  
  
|<span data-ttu-id="46b95-115">Élément</span><span class="sxs-lookup"><span data-stu-id="46b95-115">Element</span></span>|<span data-ttu-id="46b95-116">Description</span><span class="sxs-lookup"><span data-stu-id="46b95-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="46b95-117">\<announcementEndpoint ></span><span class="sxs-lookup"><span data-stu-id="46b95-117">\<announcementEndpoint></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md)|<span data-ttu-id="46b95-118">Collection de points de terminaison d’annonce.</span><span class="sxs-lookup"><span data-stu-id="46b95-118">A collection of announcement endpoints.</span></span> <span data-ttu-id="46b95-119">Cette section permet de spécifier les points de terminaison à utiliser pour l'envoi de messages d'annonce.</span><span class="sxs-lookup"><span data-stu-id="46b95-119">Use this section to specify the endpoints to use for sending announcement messages.</span></span>|  
|[<span data-ttu-id="46b95-120">\<discoveryEndpoint ></span><span class="sxs-lookup"><span data-stu-id="46b95-120">\<discoveryEndpoint></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md)|<span data-ttu-id="46b95-121">Collection de points de terminaison de découverte.</span><span class="sxs-lookup"><span data-stu-id="46b95-121">A collection of discovery endpoints.</span></span> <span data-ttu-id="46b95-122">Cette section permet de spécifier les points de terminaison sur lesquels écouter les messages de découverte.</span><span class="sxs-lookup"><span data-stu-id="46b95-122">Use this section to specify the endpoints on which to listen for the discovery messages.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="46b95-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="46b95-123">Parent Elements</span></span>  
  
|<span data-ttu-id="46b95-124">Élément</span><span class="sxs-lookup"><span data-stu-id="46b95-124">Element</span></span>|<span data-ttu-id="46b95-125">Description</span><span class="sxs-lookup"><span data-stu-id="46b95-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="46b95-126">\<behavior></span><span class="sxs-lookup"><span data-stu-id="46b95-126">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="46b95-127">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="46b95-127">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="46b95-128">Notes</span><span class="sxs-lookup"><span data-stu-id="46b95-128">Remarks</span></span>  
 <span data-ttu-id="46b95-129">Lorsqu'il est ajouté à la configuration de comportement du service, cet élément de configuration rend tous les points de terminaison de ce service détectables.</span><span class="sxs-lookup"><span data-stu-id="46b95-129">When added to the service’s behavior configuration, this configuration element makes all of the endpoints of that service discoverable.</span></span> <span data-ttu-id="46b95-130">Vous pouvez configurer davantage de fonctionnalités de découverte de tels points de terminaison à l’aide de la [ \<discoveryEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) ou [ \<announcementEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="46b95-130">You can further configure the discovery features of such endpoints by using the [\<discoveryEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) or [\<announcementEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) child elements.</span></span> <span data-ttu-id="46b95-131">Utiliser le [ \<announcementEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) section pour configurer les annonces en spécifiant la configuration de point de terminaison à utiliser pour envoyer des annonces de service (en ligne/Hello et hors connexion/Bye).</span><span class="sxs-lookup"><span data-stu-id="46b95-131">Use the [\<announcementEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) section to configure the announcements by specifying the endpoint configuration to be use to send service announcements (online/Hello and offline/Bye).</span></span> <span data-ttu-id="46b95-132">Utilisez le [ \<discoveryEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) section pour spécifier manuellement le point de terminaison d’écoute pour les messages de découverte.</span><span class="sxs-lookup"><span data-stu-id="46b95-132">Use the [\<discoveryEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) section to manually specify the endpoint on which to listen for the discovery messages.</span></span>  
  
## <a name="example"></a><span data-ttu-id="46b95-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="46b95-133">Example</span></span>  
 <span data-ttu-id="46b95-134">L'exemple de configuration suivant spécifie que CalculatorService doit être détectable et indique éventuellement le point de terminaison d'annonce à utiliser.</span><span class="sxs-lookup"><span data-stu-id="46b95-134">The following configuration example specifies that the CalculatorService to be discoverable, and optionally specifies the announcement endpoint to be used.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="46b95-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46b95-135">See Also</span></span>  
 <xref:System.ServiceModel.Discovery.ServiceDiscoveryBehavior>
