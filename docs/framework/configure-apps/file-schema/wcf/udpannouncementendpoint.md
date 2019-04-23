---
title: <udpAnnouncementEndpoint>
ms.date: 03/30/2017
ms.assetid: 5b3fa9c5-f372-4df9-a9d6-1e426063b721
ms.openlocfilehash: 04f5fb27a0da7e553ff3c0308f7fb2e2df2e0b20
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59210007"
---
# <a name="udpannouncementendpoint"></a><span data-ttu-id="73e8d-101">\<udpAnnouncementEndpoint></span><span class="sxs-lookup"><span data-stu-id="73e8d-101">\<udpAnnouncementEndpoint></span></span>
<span data-ttu-id="73e8d-102">Cet élément de configuration définit un point de terminaison standard utilisé par les services pour envoyer des messages d'annonce via une liaison UDP.</span><span class="sxs-lookup"><span data-stu-id="73e8d-102">This configuration element defines a standard endpoint that is used by services to send announcement messages over a UDP binding.</span></span> <span data-ttu-id="73e8d-103">Il a un contrat fixe et prend en charge deux versions de découverte.</span><span class="sxs-lookup"><span data-stu-id="73e8d-103">It has a fixed contract and supports two discovery versions.</span></span> <span data-ttu-id="73e8d-104">De plus, il possède une liaison UDP fixe et une valeur d'adresse par défaut indiquée dans les spécifications WS-Discovery (WS-Discovery Avril 2005 ou WS-Discovery version 1.1).</span><span class="sxs-lookup"><span data-stu-id="73e8d-104">In addition it has a fixed UDP binding and a default address value as specified in the WS-Discovery specifications (WS-Discovery April 2005 or WS-Discovery version 1.1).</span></span> <span data-ttu-id="73e8d-105">Vous pouvez spécifier l'adresse de multidiffusion à utiliser pour l'envoi et la réception de messages d'annonce.</span><span class="sxs-lookup"><span data-stu-id="73e8d-105">You can specify the multicast address to use for sending and receiving the announcement messages.</span></span>  
  
<span data-ttu-id="73e8d-106">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="73e8d-106">\<system.ServiceModel></span></span>  
<span data-ttu-id="73e8d-107">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="73e8d-107">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="73e8d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73e8d-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="73e8d-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="73e8d-109">Attributes and Elements</span></span>  
 <span data-ttu-id="73e8d-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="73e8d-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="73e8d-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="73e8d-111">Attributes</span></span>  
  
|<span data-ttu-id="73e8d-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="73e8d-112">Attribute</span></span>|<span data-ttu-id="73e8d-113">Description</span><span class="sxs-lookup"><span data-stu-id="73e8d-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="73e8d-114">discoveryVersion</span><span class="sxs-lookup"><span data-stu-id="73e8d-114">discoveryVersion</span></span>|<span data-ttu-id="73e8d-115">Chaîne qui spécifie l'une des deux versions du protocole WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="73e8d-115">A string that specifies one of the two versions of WS-Discovery protocol.</span></span> <span data-ttu-id="73e8d-116">Les valeurs valides sont WSDiscovery11 et WSDiscoveryApril2005.</span><span class="sxs-lookup"><span data-stu-id="73e8d-116">Valid values are WSDiscovery11 and WSDiscoveryApril2005.</span></span> <span data-ttu-id="73e8d-117">Cette valeur est de type <xref:System.ServiceModel.Discovery.Configuration.AnnouncementEndpointElement.DiscoveryVersion>.</span><span class="sxs-lookup"><span data-stu-id="73e8d-117">This value is of type <xref:System.ServiceModel.Discovery.Configuration.AnnouncementEndpointElement.DiscoveryVersion>.</span></span>|  
|<span data-ttu-id="73e8d-118">maxAnnouncementDelay</span><span class="sxs-lookup"><span data-stu-id="73e8d-118">maxAnnouncementDelay</span></span>|<span data-ttu-id="73e8d-119">Valeur Timespan qui spécifie le délai d'attente maximal du protocole de découverte avant l'envoi d'un message de type Hello.</span><span class="sxs-lookup"><span data-stu-id="73e8d-119">A Timespan value that specifies the maximum value for the delay the Discovery protocol will wait before sending a Hello message.</span></span> <span data-ttu-id="73e8d-120">Les messages attendent pendant un délai aléatoire compris entre 0 et la valeur de cet attribut avant d'être envoyés.</span><span class="sxs-lookup"><span data-stu-id="73e8d-120">The messages will wait for a random time value between 0 and the value of this attribute before being sent.</span></span> <span data-ttu-id="73e8d-121">Cet attribut permet de définir un délai court et aléatoire pour empêcher toute tempête de réseau lorsqu'un réseau est en panne et que tous les services reviennent en ligne en même temps.</span><span class="sxs-lookup"><span data-stu-id="73e8d-121">This attribute is used to set a small, random delay to prevent network storms when a network goes out and all services come back online at the same time.</span></span>|  
|<span data-ttu-id="73e8d-122">multicastAddress</span><span class="sxs-lookup"><span data-stu-id="73e8d-122">multicastAddress</span></span>|<span data-ttu-id="73e8d-123">URI qui spécifie une adresse de multidiffusion à utiliser pour l'envoi et la réception des messages de découverte.</span><span class="sxs-lookup"><span data-stu-id="73e8d-123">A URI that specifies a multicast address to use for sending and receiving the discovery messages.</span></span> <span data-ttu-id="73e8d-124">La valeur par défaut est représentée par l'adresse de multidiffusion conforme à la spécification du protocole.</span><span class="sxs-lookup"><span data-stu-id="73e8d-124">The default value is the multicast address as conformant to the protocol specification.</span></span>|  
|<span data-ttu-id="73e8d-125">name</span><span class="sxs-lookup"><span data-stu-id="73e8d-125">name</span></span>|<span data-ttu-id="73e8d-126">Chaîne qui spécifie le nom de la configuration du point de terminaison standard.</span><span class="sxs-lookup"><span data-stu-id="73e8d-126">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="73e8d-127">Le nom est utilisé dans l'attribut `endpointConfiguration` du point de terminaison de service pour lier un point de terminaison standard à sa configuration.</span><span class="sxs-lookup"><span data-stu-id="73e8d-127">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="73e8d-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="73e8d-128">Child Elements</span></span>  
  
|<span data-ttu-id="73e8d-129">Élément</span><span class="sxs-lookup"><span data-stu-id="73e8d-129">Element</span></span>|<span data-ttu-id="73e8d-130">Description</span><span class="sxs-lookup"><span data-stu-id="73e8d-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="73e8d-131">\<udpTransportSettings></span><span class="sxs-lookup"><span data-stu-id="73e8d-131">\<udpTransportSettings></span></span>](udptransportsettings.md)|<span data-ttu-id="73e8d-132">Collection de paramètres qui vous permettent de configurer le transport UDP pour le point de terminaison UDP.</span><span class="sxs-lookup"><span data-stu-id="73e8d-132">A collection of settings that allow you to configure UDP transport for the UDP endpoint.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="73e8d-133">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="73e8d-133">Parent Elements</span></span>  
  
|<span data-ttu-id="73e8d-134">Élément</span><span class="sxs-lookup"><span data-stu-id="73e8d-134">Element</span></span>|<span data-ttu-id="73e8d-135">Description</span><span class="sxs-lookup"><span data-stu-id="73e8d-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="73e8d-136">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="73e8d-136">\<standardEndpoints></span></span>](standardendpoints.md)|<span data-ttu-id="73e8d-137">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="73e8d-137">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="73e8d-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="73e8d-138">Example</span></span>  
 <span data-ttu-id="73e8d-139">L'exemple suivant montre un client à l'écoute d'une annonce sur un transport de multidiffusion UDP avec adresse de multidiffusion par défaut, et sur un transport de multidiffusion UDP avec l'adresse de multidiffusion spécifiée.</span><span class="sxs-lookup"><span data-stu-id="73e8d-139">The following example demonstrates a client listening for announcement over a UDP multicast transport with default multicast address, and UDP multicast transport with specified multicast address.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="73e8d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73e8d-140">See also</span></span>

- <xref:System.ServiceModel.Discovery.UdpAnnouncementEndpoint>
