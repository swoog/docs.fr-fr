---
title: <namedPipeTransport>
ms.date: 03/30/2017
ms.assetid: 9fc3f42f-43e2-4ab1-8bc7-3c95a9220df1
ms.openlocfilehash: e30fcd5952fadc3b6cf30cb352a3bb51c86cc117
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55285903"
---
# <a name="namedpipetransport"></a><span data-ttu-id="4de99-101">\<namedPipeTransport></span><span class="sxs-lookup"><span data-stu-id="4de99-101">\<namedPipeTransport></span></span>
<span data-ttu-id="4de99-102">Définit un transport qui entraîne un canal à transférer des messages à l’aide de canaux nommés lorsqu’il est inclus dans une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4de99-102">Defines a transport that causes a channel to transfer messages using named pipes when it is included in a custom binding.</span></span>  
  
<span data-ttu-id="4de99-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="4de99-103">\<system.serviceModel></span></span>  
<span data-ttu-id="4de99-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="4de99-104">\<bindings></span></span>  
<span data-ttu-id="4de99-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="4de99-105">\<customBinding></span></span>  
<span data-ttu-id="4de99-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="4de99-106">\<binding></span></span>  
<span data-ttu-id="4de99-107">\<namePipeTransport></span><span class="sxs-lookup"><span data-stu-id="4de99-107">\<namePipeTransport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4de99-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4de99-108">Syntax</span></span>  
  
```xml  
<namedPipeTransport channelInitializationTimeout="TimeSpan"
                    connectionBufferSize="Integer"
                    hostNameComparisonMode="StrongWildcard/Exact/WeakWildcard"
                    manualAddressing="Boolean"
                    maxBufferPoolSize="Integer"
                    maxBufferSize="Integer"
                    maxOutputDelay="TimeSpan"
                    maxPendingAccepts="Integer"
                    maxPendingConnections="Integer"
                    maxReceivedMessageSize="Integer"
                    transferMode="Buffered/Streamed/StreamedRequest/StreamedResponse">
  <connectionPoolSettings groupName="String"
                          idleTimeout="TimeSpan"
                          maxOutboundConnectionsPerEndpopint="Integer" />
</namedPipeTransport>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4de99-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4de99-109">Attributes and Elements</span></span>  
<span data-ttu-id="4de99-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4de99-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4de99-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="4de99-111">Attributes</span></span>  
<span data-ttu-id="4de99-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4de99-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4de99-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4de99-113">Child Elements</span></span>  
  
|<span data-ttu-id="4de99-114">Élément</span><span class="sxs-lookup"><span data-stu-id="4de99-114">Element</span></span>|<span data-ttu-id="4de99-115">Description</span><span class="sxs-lookup"><span data-stu-id="4de99-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="4de99-116">ChannelInitializationTimeout</span><span class="sxs-lookup"><span data-stu-id="4de99-116">ChannelInitializationTimeout</span></span>|<span data-ttu-id="4de99-117">Obtient ou définit un <xref:System.TimeSpan> qui détermine la durée maximale, un canal peut être dans l’état d’initialisation avant d’être déconnectée.</span><span class="sxs-lookup"><span data-stu-id="4de99-117">Gets or sets a <xref:System.TimeSpan> that determines the maximum time a channel can be in the initialization status before being disconnected.</span></span>|  
|<span data-ttu-id="4de99-118">ConnectionBufferSize</span><span class="sxs-lookup"><span data-stu-id="4de99-118">ConnectionBufferSize</span></span>|<span data-ttu-id="4de99-119">Obtient ou définit la taille de la mémoire tampon utilisée pour transmettre un bloc du message sérialisé sur le câble depuis le client ou le service.</span><span class="sxs-lookup"><span data-stu-id="4de99-119">Gets or sets the size of the buffer used to transmit a chunk of the serialized message on the wire from the client or service.</span></span>|  
|<span data-ttu-id="4de99-120">hostNameComparisonMode</span><span class="sxs-lookup"><span data-stu-id="4de99-120">hostNameComparisonMode</span></span>|<span data-ttu-id="4de99-121">Obtient ou définit une valeur qui indique si le nom d'hôte est utilisé pour atteindre le service lors de la correspondance avec l'URI.</span><span class="sxs-lookup"><span data-stu-id="4de99-121">Gets or sets a value that indicates whether the hostname is used to reach the service when matching on the URI.</span></span>|  
|<span data-ttu-id="4de99-122">manualAddressing</span><span class="sxs-lookup"><span data-stu-id="4de99-122">manualAddressing</span></span>|<span data-ttu-id="4de99-123">Obtient ou définit une valeur qui indique si l'adressage manuel du message est requis.</span><span class="sxs-lookup"><span data-stu-id="4de99-123">Gets or sets a value that indicates whether manual addressing of the message is required.</span></span>|  
|<span data-ttu-id="4de99-124">maxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="4de99-124">maxBufferPoolSize</span></span>|<span data-ttu-id="4de99-125">Obtient ou définit la taille maximale, en octets, de pools de mémoires tampons utilisés par le transport.</span><span class="sxs-lookup"><span data-stu-id="4de99-125">Gets or sets the maximum size, in bytes, of any buffer pools used by the transport.</span></span>|  
|<span data-ttu-id="4de99-126">maxBufferSize</span><span class="sxs-lookup"><span data-stu-id="4de99-126">maxBufferSize</span></span>|<span data-ttu-id="4de99-127">Obtient ou définit la taille maximale de la mémoire tampon à utiliser.</span><span class="sxs-lookup"><span data-stu-id="4de99-127">Gets or sets the maximum size of the buffer to use.</span></span> <span data-ttu-id="4de99-128">Pour les messages diffusés en continu, cette valeur doit être au moins égale à la taille maximale possible des en-têtes de message, qui sont lus en mode mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4de99-128">For streamed messages, this value should be at least the maximum possible size of the message headers, which are read in buffered mode.</span></span>|  
|<span data-ttu-id="4de99-129">maxOutputDelay</span><span class="sxs-lookup"><span data-stu-id="4de99-129">maxOutputDelay</span></span>|<span data-ttu-id="4de99-130">Obtient ou définit la durée maximale pendant laquelle un bloc d'un message ou un message complet peut être conservé dans la mémoire tampon avant d'être expédié.</span><span class="sxs-lookup"><span data-stu-id="4de99-130">Gets or sets the maximum interval of time that a chunk of a message or a full message can remain buffered in memory before being sent out.</span></span>|  
|<span data-ttu-id="4de99-131">maxPendingAccepts</span><span class="sxs-lookup"><span data-stu-id="4de99-131">maxPendingAccepts</span></span>|<span data-ttu-id="4de99-132">Obtient ou définit le nombre maximal de canaux de qu'un service peut avoir en attente sur un écouteur pour traiter les connexions entrantes au service.</span><span class="sxs-lookup"><span data-stu-id="4de99-132">Gets or sets the maximum number of channels a service can have waiting on a listener for processing incoming connections to the service.</span></span>|  
|<span data-ttu-id="4de99-133">maxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="4de99-133">maxPendingConnections</span></span>|<span data-ttu-id="4de99-134">Obtient ou définit le nombre maximal de connexions en attente de distribution sur le service.</span><span class="sxs-lookup"><span data-stu-id="4de99-134">Gets or sets the maximum number of connections awaiting dispatch on the service.</span></span>|  
|<span data-ttu-id="4de99-135">maxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="4de99-135">maxReceivedMessageSize</span></span>|<span data-ttu-id="4de99-136">Obtient et définit la taille de message maximale autorisée, en octets, qui peut être reçue.</span><span class="sxs-lookup"><span data-stu-id="4de99-136">Gets and sets the maximum allowable message size, in bytes, that can be received.</span></span>|  
|<span data-ttu-id="4de99-137">transferMode</span><span class="sxs-lookup"><span data-stu-id="4de99-137">transferMode</span></span>|<span data-ttu-id="4de99-138">Obtient ou définit une valeur qui indique si les messages sont mis en mémoire tampon ou transmis en continu par le transport orienté connexion.</span><span class="sxs-lookup"><span data-stu-id="4de99-138">Gets or sets a value that indicates whether the messages are buffered or streamed with the connection-oriented transport.</span></span>|  
|[<span data-ttu-id="4de99-139">\<connectionPoolSettings> of \<namedPipeTransport></span><span class="sxs-lookup"><span data-stu-id="4de99-139">\<connectionPoolSettings> of \<namedPipeTransport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/connectionpoolsettings.md)|<span data-ttu-id="4de99-140">Spécifie des paramètres de pool de connexions supplémentaires pour une liaison de canal nommé.</span><span class="sxs-lookup"><span data-stu-id="4de99-140">Specifies additional connection pool settings for a Named Pipe binding.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4de99-141">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4de99-141">Parent Elements</span></span>  
  
|<span data-ttu-id="4de99-142">Élément</span><span class="sxs-lookup"><span data-stu-id="4de99-142">Element</span></span>|<span data-ttu-id="4de99-143">Description</span><span class="sxs-lookup"><span data-stu-id="4de99-143">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4de99-144">\<binding></span><span class="sxs-lookup"><span data-stu-id="4de99-144">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="4de99-145">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4de99-145">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4de99-146">Notes</span><span class="sxs-lookup"><span data-stu-id="4de99-146">Remarks</span></span>  
<span data-ttu-id="4de99-147">Ce transport utilise des URI au format "net.pipe://nom_hôte/chemin".</span><span class="sxs-lookup"><span data-stu-id="4de99-147">This transport uses URIs of the form "net.pipe://hostname/path".</span></span> <span data-ttu-id="4de99-148">Les autres composants URI sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="4de99-148">Other URI components are optional.</span></span>  
  
<span data-ttu-id="4de99-149">L'élément `namedPipeTransport` constitue le point de départ pour créer une liaison personnalisée qui implémente le protocole de transport des canaux nommés.</span><span class="sxs-lookup"><span data-stu-id="4de99-149">The `namedPipeTransport` element is the starting point for creating a custom binding that implements the named pipes transport protocol.</span></span> <span data-ttu-id="4de99-150">Ce transport est utilisé pour la communication entre WCF (Windows Communication Foundation) et WCF sur des ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="4de99-150">This transport is used for on-machine Windows Communication Foundation (WCF)-to-WCF communication.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4de99-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4de99-151">See also</span></span>
- <xref:System.ServiceModel.Configuration.NamedPipeTransportElement>
- <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement>
- <xref:System.ServiceModel.Channels.TransportBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="4de99-152">Transports</span><span class="sxs-lookup"><span data-stu-id="4de99-152">Transports</span></span>](../../../../../docs/framework/wcf/feature-details/transports.md)
- [<span data-ttu-id="4de99-153">Choix d’un transport</span><span class="sxs-lookup"><span data-stu-id="4de99-153">Choosing a Transport</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)
- [<span data-ttu-id="4de99-154">Liaisons</span><span class="sxs-lookup"><span data-stu-id="4de99-154">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="4de99-155">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="4de99-155">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="4de99-156">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="4de99-156">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="4de99-157">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="4de99-157">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
