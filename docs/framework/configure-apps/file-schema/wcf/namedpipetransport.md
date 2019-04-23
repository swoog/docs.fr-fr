---
title: <namedPipeTransport>
ms.date: 03/30/2017
ms.assetid: 9fc3f42f-43e2-4ab1-8bc7-3c95a9220df1
ms.openlocfilehash: fd7dc38e229b6135f91fc159596ed1669d43701a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59228235"
---
# <a name="namedpipetransport"></a><span data-ttu-id="ffa70-101">\<namedPipeTransport></span><span class="sxs-lookup"><span data-stu-id="ffa70-101">\<namedPipeTransport></span></span>
<span data-ttu-id="ffa70-102">Définit un transport qui entraîne un canal à transférer des messages à l’aide de canaux nommés lorsqu’il est inclus dans une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="ffa70-102">Defines a transport that causes a channel to transfer messages using named pipes when it is included in a custom binding.</span></span>  
  
<span data-ttu-id="ffa70-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="ffa70-103">\<system.serviceModel></span></span>  
<span data-ttu-id="ffa70-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="ffa70-104">\<bindings></span></span>  
<span data-ttu-id="ffa70-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="ffa70-105">\<customBinding></span></span>  
<span data-ttu-id="ffa70-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="ffa70-106">\<binding></span></span>  
<span data-ttu-id="ffa70-107">\<namePipeTransport></span><span class="sxs-lookup"><span data-stu-id="ffa70-107">\<namePipeTransport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ffa70-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffa70-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ffa70-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ffa70-109">Attributes and Elements</span></span>  
<span data-ttu-id="ffa70-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ffa70-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ffa70-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="ffa70-111">Attributes</span></span>  
<span data-ttu-id="ffa70-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ffa70-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="ffa70-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ffa70-113">Child Elements</span></span>  
  
|<span data-ttu-id="ffa70-114">Élément</span><span class="sxs-lookup"><span data-stu-id="ffa70-114">Element</span></span>|<span data-ttu-id="ffa70-115">Description</span><span class="sxs-lookup"><span data-stu-id="ffa70-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ffa70-116">ChannelInitializationTimeout</span><span class="sxs-lookup"><span data-stu-id="ffa70-116">ChannelInitializationTimeout</span></span>|<span data-ttu-id="ffa70-117">Obtient ou définit un <xref:System.TimeSpan> qui détermine la durée maximale, un canal peut être dans l’état d’initialisation avant d’être déconnectée.</span><span class="sxs-lookup"><span data-stu-id="ffa70-117">Gets or sets a <xref:System.TimeSpan> that determines the maximum time a channel can be in the initialization status before being disconnected.</span></span>|  
|<span data-ttu-id="ffa70-118">ConnectionBufferSize</span><span class="sxs-lookup"><span data-stu-id="ffa70-118">ConnectionBufferSize</span></span>|<span data-ttu-id="ffa70-119">Obtient ou définit la taille de la mémoire tampon utilisée pour transmettre un bloc du message sérialisé sur le câble depuis le client ou le service.</span><span class="sxs-lookup"><span data-stu-id="ffa70-119">Gets or sets the size of the buffer used to transmit a chunk of the serialized message on the wire from the client or service.</span></span>|  
|<span data-ttu-id="ffa70-120">hostNameComparisonMode</span><span class="sxs-lookup"><span data-stu-id="ffa70-120">hostNameComparisonMode</span></span>|<span data-ttu-id="ffa70-121">Obtient ou définit une valeur qui indique si le nom d'hôte est utilisé pour atteindre le service lors de la correspondance avec l'URI.</span><span class="sxs-lookup"><span data-stu-id="ffa70-121">Gets or sets a value that indicates whether the hostname is used to reach the service when matching on the URI.</span></span>|  
|<span data-ttu-id="ffa70-122">manualAddressing</span><span class="sxs-lookup"><span data-stu-id="ffa70-122">manualAddressing</span></span>|<span data-ttu-id="ffa70-123">Obtient ou définit une valeur qui indique si l'adressage manuel du message est requis.</span><span class="sxs-lookup"><span data-stu-id="ffa70-123">Gets or sets a value that indicates whether manual addressing of the message is required.</span></span>|  
|<span data-ttu-id="ffa70-124">maxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="ffa70-124">maxBufferPoolSize</span></span>|<span data-ttu-id="ffa70-125">Obtient ou définit la taille maximale, en octets, de pools de mémoires tampons utilisés par le transport.</span><span class="sxs-lookup"><span data-stu-id="ffa70-125">Gets or sets the maximum size, in bytes, of any buffer pools used by the transport.</span></span>|  
|<span data-ttu-id="ffa70-126">maxBufferSize</span><span class="sxs-lookup"><span data-stu-id="ffa70-126">maxBufferSize</span></span>|<span data-ttu-id="ffa70-127">Obtient ou définit la taille maximale de la mémoire tampon à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ffa70-127">Gets or sets the maximum size of the buffer to use.</span></span> <span data-ttu-id="ffa70-128">Pour les messages diffusés en continu, cette valeur doit être au moins égale à la taille maximale possible des en-têtes de message, qui sont lus en mode mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ffa70-128">For streamed messages, this value should be at least the maximum possible size of the message headers, which are read in buffered mode.</span></span>|  
|<span data-ttu-id="ffa70-129">maxOutputDelay</span><span class="sxs-lookup"><span data-stu-id="ffa70-129">maxOutputDelay</span></span>|<span data-ttu-id="ffa70-130">Obtient ou définit la durée maximale pendant laquelle un bloc d'un message ou un message complet peut être conservé dans la mémoire tampon avant d'être expédié.</span><span class="sxs-lookup"><span data-stu-id="ffa70-130">Gets or sets the maximum interval of time that a chunk of a message or a full message can remain buffered in memory before being sent out.</span></span>|  
|<span data-ttu-id="ffa70-131">maxPendingAccepts</span><span class="sxs-lookup"><span data-stu-id="ffa70-131">maxPendingAccepts</span></span>|<span data-ttu-id="ffa70-132">Obtient ou définit le nombre maximal de canaux de qu'un service peut avoir en attente sur un écouteur pour traiter les connexions entrantes au service.</span><span class="sxs-lookup"><span data-stu-id="ffa70-132">Gets or sets the maximum number of channels a service can have waiting on a listener for processing incoming connections to the service.</span></span>|  
|<span data-ttu-id="ffa70-133">maxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="ffa70-133">maxPendingConnections</span></span>|<span data-ttu-id="ffa70-134">Obtient ou définit le nombre maximal de connexions en attente de distribution sur le service.</span><span class="sxs-lookup"><span data-stu-id="ffa70-134">Gets or sets the maximum number of connections awaiting dispatch on the service.</span></span>|  
|<span data-ttu-id="ffa70-135">maxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="ffa70-135">maxReceivedMessageSize</span></span>|<span data-ttu-id="ffa70-136">Obtient et définit la taille de message maximale autorisée, en octets, qui peut être reçue.</span><span class="sxs-lookup"><span data-stu-id="ffa70-136">Gets and sets the maximum allowable message size, in bytes, that can be received.</span></span>|  
|<span data-ttu-id="ffa70-137">transferMode</span><span class="sxs-lookup"><span data-stu-id="ffa70-137">transferMode</span></span>|<span data-ttu-id="ffa70-138">Obtient ou définit une valeur qui indique si les messages sont mis en mémoire tampon ou transmis en continu par le transport orienté connexion.</span><span class="sxs-lookup"><span data-stu-id="ffa70-138">Gets or sets a value that indicates whether the messages are buffered or streamed with the connection-oriented transport.</span></span>|  
|[<span data-ttu-id="ffa70-139">\<connectionPoolSettings> of \<namedPipeTransport></span><span class="sxs-lookup"><span data-stu-id="ffa70-139">\<connectionPoolSettings> of \<namedPipeTransport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/connectionpoolsettings.md)|<span data-ttu-id="ffa70-140">Spécifie des paramètres de pool de connexions supplémentaires pour une liaison de canal nommé.</span><span class="sxs-lookup"><span data-stu-id="ffa70-140">Specifies additional connection pool settings for a Named Pipe binding.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ffa70-141">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ffa70-141">Parent Elements</span></span>  
  
|<span data-ttu-id="ffa70-142">Élément</span><span class="sxs-lookup"><span data-stu-id="ffa70-142">Element</span></span>|<span data-ttu-id="ffa70-143">Description</span><span class="sxs-lookup"><span data-stu-id="ffa70-143">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ffa70-144">\<binding></span><span class="sxs-lookup"><span data-stu-id="ffa70-144">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="ffa70-145">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="ffa70-145">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ffa70-146">Notes</span><span class="sxs-lookup"><span data-stu-id="ffa70-146">Remarks</span></span>  
<span data-ttu-id="ffa70-147">Ce transport utilise des URI au format "net.pipe://nom_hôte/chemin".</span><span class="sxs-lookup"><span data-stu-id="ffa70-147">This transport uses URIs of the form "net.pipe://hostname/path".</span></span> <span data-ttu-id="ffa70-148">Les autres composants URI sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="ffa70-148">Other URI components are optional.</span></span>  
  
<span data-ttu-id="ffa70-149">L’élément `namedPipeTransport` constitue le point de départ pour créer une liaison personnalisée qui implémente le protocole de transport des canaux nommés.</span><span class="sxs-lookup"><span data-stu-id="ffa70-149">The `namedPipeTransport` element is the starting point for creating a custom binding that implements the named pipes transport protocol.</span></span> <span data-ttu-id="ffa70-150">Ce transport est utilisé pour la communication entre WCF (Windows Communication Foundation) et WCF sur des ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="ffa70-150">This transport is used for on-machine Windows Communication Foundation (WCF)-to-WCF communication.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ffa70-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffa70-151">See also</span></span>

- <xref:System.ServiceModel.Configuration.NamedPipeTransportElement>
- <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement>
- <xref:System.ServiceModel.Channels.TransportBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="ffa70-152">Transports</span><span class="sxs-lookup"><span data-stu-id="ffa70-152">Transports</span></span>](../../../../../docs/framework/wcf/feature-details/transports.md)
- [<span data-ttu-id="ffa70-153">Choix d’un transport</span><span class="sxs-lookup"><span data-stu-id="ffa70-153">Choosing a Transport</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)
- [<span data-ttu-id="ffa70-154">Liaisons</span><span class="sxs-lookup"><span data-stu-id="ffa70-154">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="ffa70-155">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="ffa70-155">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="ffa70-156">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="ffa70-156">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="ffa70-157">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="ffa70-157">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
