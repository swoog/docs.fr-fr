---
title: '&lt;udpAnnoucementEndpoint&gt;'
ms.date: 03/30/2017
ms.assetid: 5b3fa9c5-f372-4df9-a9d6-1e426063b721
ms.openlocfilehash: a6dbec19beb3800603bd745bacbd6cbcbcdaa739
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltudpannoucementendpointgt"></a><span data-ttu-id="13ac5-102">&lt;udpAnnoucementEndpoint&gt;</span><span class="sxs-lookup"><span data-stu-id="13ac5-102">&lt;udpAnnoucementEndpoint&gt;</span></span>
<span data-ttu-id="13ac5-103">Cet élément de configuration définit un point de terminaison standard utilisé par les services pour envoyer des messages d’annonce via une liaison UDP.</span><span class="sxs-lookup"><span data-stu-id="13ac5-103">This configuration element defines a standard endpoint that is used by services to send announcement messages over a UDP binding.</span></span> <span data-ttu-id="13ac5-104">Il a un contrat fixe et prend en charge deux versions de découverte.</span><span class="sxs-lookup"><span data-stu-id="13ac5-104">It has a fixed contract and supports two discovery versions.</span></span> <span data-ttu-id="13ac5-105">De plus, il possède une liaison UDP fixe et une valeur d'adresse par défaut indiquée dans les spécifications WS-Discovery (WS-Discovery Avril 2005 ou WS-Discovery version 1.1).</span><span class="sxs-lookup"><span data-stu-id="13ac5-105">In addition it has a fixed UDP binding and a default address value as specified in the WS-Discovery specifications (WS-Discovery April 2005 or WS-Discovery version 1.1).</span></span> <span data-ttu-id="13ac5-106">Vous pouvez spécifier l'adresse de multidiffusion à utiliser pour l'envoi et la réception de messages d'annonce.</span><span class="sxs-lookup"><span data-stu-id="13ac5-106">You can specify the multicast address to use for sending and receiving the announcement messages.</span></span>  
  
<span data-ttu-id="13ac5-107">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="13ac5-107">\<system.ServiceModel></span></span>  
<span data-ttu-id="13ac5-108">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="13ac5-108">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="13ac5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13ac5-109">Syntax</span></span>  
  
```xml  
<system.serviceModel>  
  <standardEndpoints>
    <announcementEndpoint>
      <standardEndpoint discoveryVersion="WSDiscovery11/WSDiscoveryApril2005" 
                        maxAnnouncementDelay="Timespan"
                        multicastAddress="Uri"
                        name="String" />
    </announcementEndpoint>
  </standardEndpoints>  
</system.serviceModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="13ac5-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="13ac5-110">Attributes and Elements</span></span>  
 <span data-ttu-id="13ac5-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="13ac5-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="13ac5-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="13ac5-112">Attributes</span></span>  
  
|<span data-ttu-id="13ac5-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="13ac5-113">Attribute</span></span>|<span data-ttu-id="13ac5-114">Description</span><span class="sxs-lookup"><span data-stu-id="13ac5-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="13ac5-115">discoveryVersion</span><span class="sxs-lookup"><span data-stu-id="13ac5-115">discoveryVersion</span></span>|<span data-ttu-id="13ac5-116">Chaîne qui spécifie l'une des deux versions du protocole WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="13ac5-116">A string that specifies one of the two versions of WS-Discovery protocol.</span></span> <span data-ttu-id="13ac5-117">Les valeurs valides sont WSDiscovery11 et WSDiscoveryApril2005.</span><span class="sxs-lookup"><span data-stu-id="13ac5-117">Valid values are WSDiscovery11 and WSDiscoveryApril2005.</span></span> <span data-ttu-id="13ac5-118">Cette valeur est de type <xref:System.ServiceModel.Discovery.Configuration.AnnouncementEndpointElement.DiscoveryVersion>.</span><span class="sxs-lookup"><span data-stu-id="13ac5-118">This value is of type <xref:System.ServiceModel.Discovery.Configuration.AnnouncementEndpointElement.DiscoveryVersion>.</span></span>|  
|<span data-ttu-id="13ac5-119">maxAnnouncementDelay</span><span class="sxs-lookup"><span data-stu-id="13ac5-119">maxAnnouncementDelay</span></span>|<span data-ttu-id="13ac5-120">Valeur Timespan qui spécifie le délai d'attente maximal du protocole de découverte avant l'envoi d'un message de type Hello.</span><span class="sxs-lookup"><span data-stu-id="13ac5-120">A Timespan value that specifies the maximum value for the delay the Discovery protocol will wait before sending a Hello message.</span></span> <span data-ttu-id="13ac5-121">Les messages attendent pendant un délai aléatoire compris entre 0 et la valeur de cet attribut avant d'être envoyés.</span><span class="sxs-lookup"><span data-stu-id="13ac5-121">The messages will wait for a random time value between 0 and the value of this attribute before being sent.</span></span> <span data-ttu-id="13ac5-122">Cet attribut permet de définir un délai court et aléatoire pour empêcher toute tempête de réseau lorsqu'un réseau est en panne et que tous les services reviennent en ligne en même temps.</span><span class="sxs-lookup"><span data-stu-id="13ac5-122">This attribute is used to set a small, random delay to prevent network storms when a network goes out and all services come back online at the same time.</span></span>|  
|<span data-ttu-id="13ac5-123">multicastAddress</span><span class="sxs-lookup"><span data-stu-id="13ac5-123">multicastAddress</span></span>|<span data-ttu-id="13ac5-124">URI qui spécifie une adresse de multidiffusion à utiliser pour l'envoi et la réception des messages de découverte.</span><span class="sxs-lookup"><span data-stu-id="13ac5-124">A URI that specifies a multicast address to use for sending and receiving the discovery messages.</span></span> <span data-ttu-id="13ac5-125">La valeur par défaut est représentée par l'adresse de multidiffusion conforme à la spécification du protocole.</span><span class="sxs-lookup"><span data-stu-id="13ac5-125">The default value is the multicast address as conformant to the protocol specification.</span></span>|  
|<span data-ttu-id="13ac5-126">name</span><span class="sxs-lookup"><span data-stu-id="13ac5-126">name</span></span>|<span data-ttu-id="13ac5-127">Chaîne qui spécifie le nom de la configuration du point de terminaison standard.</span><span class="sxs-lookup"><span data-stu-id="13ac5-127">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="13ac5-128">Le nom est utilisé dans l'attribut `endpointConfiguration` du point de terminaison de service pour lier un point de terminaison standard à sa configuration.</span><span class="sxs-lookup"><span data-stu-id="13ac5-128">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="13ac5-129">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="13ac5-129">Child Elements</span></span>  
  
|<span data-ttu-id="13ac5-130">Élément</span><span class="sxs-lookup"><span data-stu-id="13ac5-130">Element</span></span>|<span data-ttu-id="13ac5-131">Description</span><span class="sxs-lookup"><span data-stu-id="13ac5-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="13ac5-132">\<udpTransportSettings ></span><span class="sxs-lookup"><span data-stu-id="13ac5-132">\<udpTransportSettings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/udptransportsettings.md)|<span data-ttu-id="13ac5-133">Collection de paramètres qui vous permettent de configurer le transport UDP pour le point de terminaison UDP.</span><span class="sxs-lookup"><span data-stu-id="13ac5-133">A collection of settings that allow you to configure UDP transport for the UDP endpoint.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="13ac5-134">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="13ac5-134">Parent Elements</span></span>  
  
|<span data-ttu-id="13ac5-135">Élément</span><span class="sxs-lookup"><span data-stu-id="13ac5-135">Element</span></span>|<span data-ttu-id="13ac5-136">Description</span><span class="sxs-lookup"><span data-stu-id="13ac5-136">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="13ac5-137">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="13ac5-137">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="13ac5-138">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="13ac5-138">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="13ac5-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="13ac5-139">Example</span></span>  
 <span data-ttu-id="13ac5-140">L'exemple suivant montre un client à l'écoute d'une annonce sur un transport de multidiffusion UDP avec adresse de multidiffusion par défaut, et sur un transport de multidiffusion UDP avec l'adresse de multidiffusion spécifiée.</span><span class="sxs-lookup"><span data-stu-id="13ac5-140">The following example demonstrates a client listening for announcement over a UDP multicast transport with default multicast address, and UDP multicast transport with specified multicast address.</span></span>  
  
```xml  
<services>  
  <service name="ServiceAnnouncementListener">  
      <endpoint name="udpAnnouncementEndpointStandard"  
                kind="udpAnnouncementEndpoint"  
                bindingConfiguration="..." />  
      <endpoint name="udpAnnouncementEndpoint2"  
                kind="udpAnnouncementEndpoint"  
                endpointConfiguration="AnnouncementConfiguration3702"  
                bindingConfiguration="..." />  
...  
  </service>  
</services>  
<standardEndpoints>  
  <udpAnnouncementEndpoint>  
     <standardEndpoint name="AnnouncementConfiguration2"   
          version="WSDiscoveryApril2005"   
          multicastAddress="soap.udp://239.255.255.250:3703"/>          
  </udpAnnouncementEndpoint>  
</standardEndpoints>  
```  
  
## <a name="see-also"></a><span data-ttu-id="13ac5-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13ac5-141">See Also</span></span>  
 <xref:System.ServiceModel.Discovery.UdpAnnouncementEndpoint>
