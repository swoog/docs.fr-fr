---
title: <connectionPoolSettings> de <tcpTransport>
ms.date: 03/30/2017
ms.assetid: 2fbc3aa7-fcc9-4193-99a3-85d31d60d3f7
ms.openlocfilehash: 93363c5ff1753ff02956404da7697780078c9839
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61673236"
---
# <a name="connectionpoolsettings-of-tcptransport"></a><span data-ttu-id="8a8ea-102">\<connectionPoolSettings> of \<tcpTransport></span><span class="sxs-lookup"><span data-stu-id="8a8ea-102">\<connectionPoolSettings> of \<tcpTransport></span></span>
<span data-ttu-id="8a8ea-103">Spécifie des paramètres de pool de connexions supplémentaires pour un transport TCP.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-103">Specifies additional connection pool settings for a TCP transport.</span></span>  
  
 <span data-ttu-id="8a8ea-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="8a8ea-104">\<system.serviceModel></span></span>  
<span data-ttu-id="8a8ea-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="8a8ea-105">\<bindings></span></span>  
<span data-ttu-id="8a8ea-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="8a8ea-106">\<customBinding></span></span>  
<span data-ttu-id="8a8ea-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="8a8ea-107">\<binding></span></span>  
<span data-ttu-id="8a8ea-108">\<tcpTransport></span><span class="sxs-lookup"><span data-stu-id="8a8ea-108">\<tcpTransport></span></span>  
<span data-ttu-id="8a8ea-109">\<connectionPoolSettings></span><span class="sxs-lookup"><span data-stu-id="8a8ea-109">\<connectionPoolSettings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a8ea-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a8ea-110">Syntax</span></span>  
  
```xml  
<connectionPoolSettings groupName="String"
                        idleTimeout="TimeSpan"
                        leaseTimeout="TimeSpan"
                        maxOutboundConnectionsPerEndpopint="Integer" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8a8ea-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="8a8ea-111">Attributes and Elements</span></span>  
 <span data-ttu-id="8a8ea-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8a8ea-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="8a8ea-113">Attributes</span></span>  
  
|<span data-ttu-id="8a8ea-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="8a8ea-114">Attribute</span></span>|<span data-ttu-id="8a8ea-115">Description</span><span class="sxs-lookup"><span data-stu-id="8a8ea-115">Description</span></span>|  
|---------------|-----------------|  
|`groupName`|<span data-ttu-id="8a8ea-116">Chaîne qui définit le nom du pool de connexions utilisé pour les canaux sortants.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-116">A string that defines the name of the connection pool used for outgoing channels.</span></span> <span data-ttu-id="8a8ea-117">En mode de transmission continu, les connexions ne sont pas partagées, ce qui signifie que la mise en pool des connexions est désactivée.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-117">In streamed mode, connections are not shared, meaning that connection pooling is disabled.</span></span> <span data-ttu-id="8a8ea-118">La valeur par défaut est une chaîne par défaut.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-118">The default is a "default" string.</span></span> <span data-ttu-id="8a8ea-119">Vous pouvez modifier cette valeur pour isoler les connexions d'un client particulier dans des groupes séparés.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-119">You can modify this value to isolate the connections for a particular client into separate groups.</span></span>|  
|`idleTimeout`|<span data-ttu-id="8a8ea-120"><xref:System.TimeSpan> positif qui spécifie la période maximale d'inactivité de la connexion au terme de laquelle la connexion est coupée.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-120">A positive <xref:System.TimeSpan> that specifies the maximum time the connection can be idle before being disconnected.</span></span> <span data-ttu-id="8a8ea-121">La valeur par défaut est 00:02:00.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-121">The default is 00:02:00.</span></span>|  
|`leaseTimeout`|<span data-ttu-id="8a8ea-122"><xref:System.TimeSpan> qui spécifie le délai après lequel une connexion active est fermée.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-122">A <xref:System.TimeSpan> that specifies the time after which an active connection is closed.</span></span> <span data-ttu-id="8a8ea-123">La valeur par défaut est 00:05:00.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-123">The default is 00:05:00.</span></span><br /><br /> <span data-ttu-id="8a8ea-124">Une connexion est fermée après qu'elle ait été retournée au cache de connexions et non pendant la transmission active.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-124">A connection is closed after it has been returned to the connection cache and not during active transmission.</span></span> <span data-ttu-id="8a8ea-125">Le cache de connexions utilisé par le transport TCP crée les connexions requises pour chaque point de terminaison jusqu'à la limite de cache définie par `maxOutboundConnectionsPerEndpoint.`</span><span class="sxs-lookup"><span data-stu-id="8a8ea-125">The connection cache used by the TCP transport creates new connections as required for each endpoint, up to the cache limit that is set by `maxOutboundConnectionsPerEndpoint.`</span></span>|  
|`maxOutboundConnectionsPerEndpoint`|<span data-ttu-id="8a8ea-126">Entier positif qui spécifie le nombre maximal de connexions à un point de terminaison distant initié par le service.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-126">A positive integer that specifies the maximum number of connections to a remote endpoint initiated by the service.</span></span> <span data-ttu-id="8a8ea-127">Toute connexion dépassant cette limite est mise en file d'attente jusqu'à ce qu'une place se libère.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-127">Connections in excess of the limit are queued until a space below the limit becomes available.</span></span> <span data-ttu-id="8a8ea-128">`idleTimeout` limite la durée pendant laquelle les connexions restent dans la file d'attente avant qu'une exception soit levée.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-128">The `idleTimeout` limits the duration in which connections remain queued before an exception is thrown.</span></span> <span data-ttu-id="8a8ea-129">La valeur par défaut est 10.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-129">The default is 10.</span></span><br /><br /> <span data-ttu-id="8a8ea-130">Cet attribut limite le nombre de connexions actives simultanées entre le client et un point de terminaison de service particulier.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-130">This attribute limits the number of simultaneous active connections from the client to a particular service endpoint.</span></span> <span data-ttu-id="8a8ea-131">Si cette valeur est dépassée, il est possible que le service ne semble pas répondre au client.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-131">If this value is exceeded by having more active client connections, the service may appear unresponsive to the client.</span></span> <span data-ttu-id="8a8ea-132">Dans ce cas, cette valeur doit être ajustée de façon à être supérieure au nombre maximal de connexions simultanées prévues à un point de terminaison spécifique.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-132">In this case, this value should be adjusted to exceed the maximum number of expected simultaneous client connections to a specific endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8a8ea-133">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8a8ea-133">Child Elements</span></span>  
 <span data-ttu-id="8a8ea-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-134">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8a8ea-135">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8a8ea-135">Parent Elements</span></span>  
  
|<span data-ttu-id="8a8ea-136">Élément</span><span class="sxs-lookup"><span data-stu-id="8a8ea-136">Element</span></span>|<span data-ttu-id="8a8ea-137">Description</span><span class="sxs-lookup"><span data-stu-id="8a8ea-137">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8a8ea-138">\<namedPipeTransport></span><span class="sxs-lookup"><span data-stu-id="8a8ea-138">\<namedPipeTransport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/namedpipetransport.md)|<span data-ttu-id="8a8ea-139">Définit un transport qui entraîne un canal à transférer des messages à l'aide de canaux nommés.</span><span class="sxs-lookup"><span data-stu-id="8a8ea-139">Defines a transport that causes a channel to transfer messages using named pipes.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8a8ea-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a8ea-140">See also</span></span>

- <xref:System.ServiceModel.Configuration.TcpConnectionPoolSettingsElement>
- <xref:System.ServiceModel.Channels.TcpTransportBindingElement.ConnectionPoolSettings%2A>
- <xref:System.ServiceModel.Channels.TcpConnectionPoolSettings>
- <xref:System.ServiceModel.Channels.TransportBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="8a8ea-141">Transports</span><span class="sxs-lookup"><span data-stu-id="8a8ea-141">Transports</span></span>](../../../../../docs/framework/wcf/feature-details/transports.md)
- [<span data-ttu-id="8a8ea-142">Choix d’un transport</span><span class="sxs-lookup"><span data-stu-id="8a8ea-142">Choosing a Transport</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)
- [<span data-ttu-id="8a8ea-143">Liaisons</span><span class="sxs-lookup"><span data-stu-id="8a8ea-143">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="8a8ea-144">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="8a8ea-144">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="8a8ea-145">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="8a8ea-145">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="8a8ea-146">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="8a8ea-146">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
