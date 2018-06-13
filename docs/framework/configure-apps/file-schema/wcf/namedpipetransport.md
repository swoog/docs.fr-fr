---
title: '&lt;namedPipeTransport&gt;'
ms.date: 03/30/2017
ms.assetid: 9fc3f42f-43e2-4ab1-8bc7-3c95a9220df1
ms.openlocfilehash: 652cb551fb318d43d4284dbee48aeb994f056692
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32746795"
---
# <a name="ltnamedpipetransportgt"></a><span data-ttu-id="70a01-102">&lt;namedPipeTransport&gt;</span><span class="sxs-lookup"><span data-stu-id="70a01-102">&lt;namedPipeTransport&gt;</span></span>
<span data-ttu-id="70a01-103">Définit un transport qui entraîne un canal à transférer des messages à l’aide de canaux nommés lorsqu’il est inclus dans une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="70a01-103">Defines a transport that causes a channel to transfer messages using named pipes when it is included in a custom binding.</span></span>  
  
<span data-ttu-id="70a01-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="70a01-104">\<system.serviceModel></span></span>  
<span data-ttu-id="70a01-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="70a01-105">\<bindings></span></span>  
<span data-ttu-id="70a01-106">\<customBinding ></span><span class="sxs-lookup"><span data-stu-id="70a01-106">\<customBinding></span></span>  
<span data-ttu-id="70a01-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="70a01-107">\<binding></span></span>  
<span data-ttu-id="70a01-108">\<namePipeTransport ></span><span class="sxs-lookup"><span data-stu-id="70a01-108">\<namePipeTransport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70a01-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70a01-109">Syntax</span></span>  
  
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
                          idleTimeout"TimeSpan"  
                          maxOutboundConnectionsPerEndpopint="Integer" />  
</namedPipeTransport>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="70a01-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="70a01-110">Attributes and Elements</span></span>  
<span data-ttu-id="70a01-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="70a01-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="70a01-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="70a01-112">Attributes</span></span>  
<span data-ttu-id="70a01-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="70a01-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="70a01-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="70a01-114">Child Elements</span></span>  
  
|<span data-ttu-id="70a01-115">Élément</span><span class="sxs-lookup"><span data-stu-id="70a01-115">Element</span></span>|<span data-ttu-id="70a01-116">Description</span><span class="sxs-lookup"><span data-stu-id="70a01-116">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="70a01-117">ChannelInitializationTimeout</span><span class="sxs-lookup"><span data-stu-id="70a01-117">ChannelInitializationTimeout</span></span>|<span data-ttu-id="70a01-118">Obtient ou définit un <xref:System.TimeSpan> qui détermine la durée maximale, un canal peut être dans l’état d’initialisation avant d’être déconnectée.</span><span class="sxs-lookup"><span data-stu-id="70a01-118">Gets or sets a <xref:System.TimeSpan> that determines the maximum time a channel can be in the initialization status before being disconnected.</span></span>|  
|<span data-ttu-id="70a01-119">ConnectionBufferSize</span><span class="sxs-lookup"><span data-stu-id="70a01-119">ConnectionBufferSize</span></span>|<span data-ttu-id="70a01-120">Obtient ou définit la taille de la mémoire tampon utilisée pour transmettre un bloc du message sérialisé sur le câble depuis le client ou le service.</span><span class="sxs-lookup"><span data-stu-id="70a01-120">Gets or sets the size of the buffer used to transmit a chunk of the serialized message on the wire from the client or service.</span></span>|  
|<span data-ttu-id="70a01-121">hostNameComparisonMode</span><span class="sxs-lookup"><span data-stu-id="70a01-121">hostNameComparisonMode</span></span>|<span data-ttu-id="70a01-122">Obtient ou définit une valeur qui indique si le nom d'hôte est utilisé pour atteindre le service lors de la correspondance avec l'URI.</span><span class="sxs-lookup"><span data-stu-id="70a01-122">Gets or sets a value that indicates whether the hostname is used to reach the service when matching on the URI.</span></span>|  
|<span data-ttu-id="70a01-123">manualAddressing</span><span class="sxs-lookup"><span data-stu-id="70a01-123">manualAddressing</span></span>|<span data-ttu-id="70a01-124">Obtient ou définit une valeur qui indique si l'adressage manuel du message est requis.</span><span class="sxs-lookup"><span data-stu-id="70a01-124">Gets or sets a value that indicates whether manual addressing of the message is required.</span></span>|  
|<span data-ttu-id="70a01-125">maxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="70a01-125">maxBufferPoolSize</span></span>|<span data-ttu-id="70a01-126">Obtient ou définit la taille maximale, en octets, de pools de mémoires tampons utilisées par le transport.</span><span class="sxs-lookup"><span data-stu-id="70a01-126">Gets or sets the maximum size, in bytes, of any buffer pools used by the transport.</span></span>|  
|<span data-ttu-id="70a01-127">maxBufferSize</span><span class="sxs-lookup"><span data-stu-id="70a01-127">maxBufferSize</span></span>|<span data-ttu-id="70a01-128">Obtient ou définit la taille maximale de la mémoire tampon à utiliser.</span><span class="sxs-lookup"><span data-stu-id="70a01-128">Gets or sets the maximum size of the buffer to use.</span></span> <span data-ttu-id="70a01-129">Pour les messages diffusés en continu, cette valeur doit être au moins égale à la taille maximale possible des en-têtes de message, qui sont lus en mode mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="70a01-129">For streamed messages, this value should be at least the maximum possible size of the message headers, which are read in buffered mode.</span></span>|  
|<span data-ttu-id="70a01-130">maxOutputDelay</span><span class="sxs-lookup"><span data-stu-id="70a01-130">maxOutputDelay</span></span>|<span data-ttu-id="70a01-131">Obtient ou définit la durée maximale pendant laquelle un bloc d'un message ou un message complet peut être conservé dans la mémoire tampon avant d'être expédié.</span><span class="sxs-lookup"><span data-stu-id="70a01-131">Gets or sets the maximum interval of time that a chunk of a message or a full message can remain buffered in memory before being sent out.</span></span>|  
|<span data-ttu-id="70a01-132">maxPendingAccepts</span><span class="sxs-lookup"><span data-stu-id="70a01-132">maxPendingAccepts</span></span>|<span data-ttu-id="70a01-133">Obtient ou définit le nombre maximal de canaux de qu'un service peut avoir en attente sur un écouteur pour le traitement des connexions entrantes vers le service.</span><span class="sxs-lookup"><span data-stu-id="70a01-133">Gets or sets the maximum number of channels a service can have waiting on a listener for processing incoming connections to the service.</span></span>|  
|<span data-ttu-id="70a01-134">maxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="70a01-134">maxPendingConnections</span></span>|<span data-ttu-id="70a01-135">Obtient ou définit le nombre maximal de connexions en attente de distribution sur le service.</span><span class="sxs-lookup"><span data-stu-id="70a01-135">Gets or sets the maximum number of connections awaiting dispatch on the service.</span></span>|  
|<span data-ttu-id="70a01-136">maxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="70a01-136">maxReceivedMessageSize</span></span>|<span data-ttu-id="70a01-137">Obtient et définit la taille de message maximale autorisée, en octets, qui peuvent être reçus.</span><span class="sxs-lookup"><span data-stu-id="70a01-137">Gets and sets the maximum allowable message size, in bytes, that can be received.</span></span>|  
|<span data-ttu-id="70a01-138">transferMode</span><span class="sxs-lookup"><span data-stu-id="70a01-138">transferMode</span></span>|<span data-ttu-id="70a01-139">Obtient ou définit une valeur qui indique si les messages sont mis en mémoire tampon ou transmis en continu par le transport orienté connexion.</span><span class="sxs-lookup"><span data-stu-id="70a01-139">Gets or sets a value that indicates whether the messages are buffered or streamed with the connection-oriented transport.</span></span>|  
|[<span data-ttu-id="70a01-140">\<connectionPoolSettings > de \<namedPipeTransport ></span><span class="sxs-lookup"><span data-stu-id="70a01-140">\<connectionPoolSettings> of \<namedPipeTransport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/connectionpoolsettings.md)|<span data-ttu-id="70a01-141">Spécifie des paramètres de pool de connexions supplémentaires pour une liaison de canal nommé.</span><span class="sxs-lookup"><span data-stu-id="70a01-141">Specifies additional connection pool settings for a Named Pipe binding.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="70a01-142">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="70a01-142">Parent Elements</span></span>  
  
|<span data-ttu-id="70a01-143">Élément</span><span class="sxs-lookup"><span data-stu-id="70a01-143">Element</span></span>|<span data-ttu-id="70a01-144">Description</span><span class="sxs-lookup"><span data-stu-id="70a01-144">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="70a01-145">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="70a01-145">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="70a01-146">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="70a01-146">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="70a01-147">Notes</span><span class="sxs-lookup"><span data-stu-id="70a01-147">Remarks</span></span>  
<span data-ttu-id="70a01-148">Ce transport utilise des URI au format "net.pipe://nom_hôte/chemin".</span><span class="sxs-lookup"><span data-stu-id="70a01-148">This transport uses URIs of the form "net.pipe://hostname/path".</span></span> <span data-ttu-id="70a01-149">Les autres composants URI sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="70a01-149">Other URI components are optional.</span></span>  
  
<span data-ttu-id="70a01-150">L'élément `namedPipeTransport` constitue le point de départ pour créer une liaison personnalisée qui implémente le protocole de transport des canaux nommés.</span><span class="sxs-lookup"><span data-stu-id="70a01-150">The `namedPipeTransport` element is the starting point for creating a custom binding that implements the named pipes transport protocol.</span></span> <span data-ttu-id="70a01-151">Ce transport est utilisé pour la communication entre WCF (Windows Communication Foundation) et WCF sur des ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="70a01-151">This transport is used for on-machine Windows Communication Foundation (WCF)-to-WCF communication.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="70a01-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70a01-152">See Also</span></span>  
<xref:System.ServiceModel.Configuration.NamedPipeTransportElement>   
<xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement>   
<xref:System.ServiceModel.Channels.TransportBindingElement>   
<xref:System.ServiceModel.Channels.CustomBinding>   
<span data-ttu-id="70a01-153">[Transports](../../../../../docs/framework/wcf/feature-details/transports.md) </span><span class="sxs-lookup"><span data-stu-id="70a01-153">[Transports](../../../../../docs/framework/wcf/feature-details/transports.md) </span></span>  
<span data-ttu-id="70a01-154">[Choix d’un Transport](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md) </span><span class="sxs-lookup"><span data-stu-id="70a01-154">[Choosing a Transport](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md) </span></span>  
<span data-ttu-id="70a01-155">[Liaisons](../../../../../docs/framework/wcf/bindings.md) </span><span class="sxs-lookup"><span data-stu-id="70a01-155">[Bindings](../../../../../docs/framework/wcf/bindings.md) </span></span>  
<span data-ttu-id="70a01-156">[Extension de liaisons](../../../../../docs/framework/wcf/extending/extending-bindings.md) </span><span class="sxs-lookup"><span data-stu-id="70a01-156">[Extending Bindings](../../../../../docs/framework/wcf/extending/extending-bindings.md) </span></span>  
<span data-ttu-id="70a01-157">[Liaisons personnalisées](../../../../../docs/framework/wcf/extending/custom-bindings.md) </span><span class="sxs-lookup"><span data-stu-id="70a01-157">[Custom Bindings](../../../../../docs/framework/wcf/extending/custom-bindings.md) </span></span>  
[<span data-ttu-id="70a01-158">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="70a01-158">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
