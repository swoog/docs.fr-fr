---
title: <peerTransport>
ms.date: 03/30/2017
ms.assetid: c1a5013a-9dd4-4a27-b114-795b8b323177
ms.openlocfilehash: 6765259f290047a4199a422b4ad0cced2ffee9ae
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61783349"
---
# <a name="peertransport"></a><span data-ttu-id="09dcf-101">\<peerTransport></span><span class="sxs-lookup"><span data-stu-id="09dcf-101">\<peerTransport></span></span>
<span data-ttu-id="09dcf-102">Définit un transport d’homologue pour une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="09dcf-102">Defines a peer transport for a custom binding.</span></span>  
  
 <span data-ttu-id="09dcf-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="09dcf-103">\<system.serviceModel></span></span>  
<span data-ttu-id="09dcf-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="09dcf-104">\<bindings></span></span>  
<span data-ttu-id="09dcf-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="09dcf-105">\<customBinding></span></span>  
<span data-ttu-id="09dcf-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="09dcf-106">\<binding></span></span>  
<span data-ttu-id="09dcf-107">\<peerTransport></span><span class="sxs-lookup"><span data-stu-id="09dcf-107">\<peerTransport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="09dcf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09dcf-108">Syntax</span></span>  
  
```xml  
<peerTransport listenIpAddress="String"
               maxBufferPoolSize="Integer"
               maxReceivedMessageSize="Integer"
               port="Integer">
  <security>
  </security>
</peerTransport>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="09dcf-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="09dcf-109">Attributes and Elements</span></span>  
 <span data-ttu-id="09dcf-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="09dcf-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="09dcf-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="09dcf-111">Attributes</span></span>  
  
|<span data-ttu-id="09dcf-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="09dcf-112">Attribute</span></span>|<span data-ttu-id="09dcf-113">Description</span><span class="sxs-lookup"><span data-stu-id="09dcf-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="09dcf-114">listenIpAddress</span><span class="sxs-lookup"><span data-stu-id="09dcf-114">listenIpAddress</span></span>|<span data-ttu-id="09dcf-115">Chaîne indiquant une adresse IP utilisée par le nœud homologue pour écouter les messages TCP.</span><span class="sxs-lookup"><span data-stu-id="09dcf-115">A string that specifies an IP address on which the peer node will listen for TCP messages.</span></span> <span data-ttu-id="09dcf-116">La valeur par défaut est `null`.</span><span class="sxs-lookup"><span data-stu-id="09dcf-116">The default is `null`.</span></span>|  
|<span data-ttu-id="09dcf-117">maxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="09dcf-117">maxBufferPoolSize</span></span>|<span data-ttu-id="09dcf-118">Entier positif indiquant la taille maximale du pool de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="09dcf-118">A positive integer that specifies the maximum size of the buffer pool.</span></span> <span data-ttu-id="09dcf-119">La valeur par défaut est 524288.</span><span class="sxs-lookup"><span data-stu-id="09dcf-119">The default is 524288.</span></span><br /><br /> <span data-ttu-id="09dcf-120">De nombreux éléments de WCF utilisent des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="09dcf-120">Many parts of WCF use buffers.</span></span> <span data-ttu-id="09dcf-121">La création et la destruction des mémoires tampons à chaque utilisation sont chères, tout comme leur nettoyage.</span><span class="sxs-lookup"><span data-stu-id="09dcf-121">Creating and destroying buffers each time they are used is expensive, and garbage collection for buffers is also expensive.</span></span> <span data-ttu-id="09dcf-122">Avec les pools de mémoires tampons, vous pouvez prendre une mémoire tampon du pool, l'utiliser et la retourner au pool une fois que vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="09dcf-122">With buffer pools, you can take a buffer from the pool, use it, and return it to the pool once you are done.</span></span> <span data-ttu-id="09dcf-123">Ainsi, la surcharge de la création et de la destruction des mémoires tampons est évitée.</span><span class="sxs-lookup"><span data-stu-id="09dcf-123">Thus the overhead in creating and destroying buffers is avoided.</span></span>|  
|<span data-ttu-id="09dcf-124">maxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="09dcf-124">maxReceivedMessageSize</span></span>|<span data-ttu-id="09dcf-125">Entier positif définissant la taille maximale du message (en octets, en-têtes compris).</span><span class="sxs-lookup"><span data-stu-id="09dcf-125">A positive integer that defines the maximum message size in bytes including headers.</span></span> <span data-ttu-id="09dcf-126">L'expéditeur d'un message reçoit une erreur SOAP si ce message est trop volumineux pour le récepteur.</span><span class="sxs-lookup"><span data-stu-id="09dcf-126">The sender of a message receives a SOAP fault when the message is too large for the receiver.</span></span> <span data-ttu-id="09dcf-127">Ce dernier dépose le message et crée une entrée d’événement dans le journal de suivi.</span><span class="sxs-lookup"><span data-stu-id="09dcf-127">The receiver drops the message and creates an entry of the event in the trace log.</span></span> <span data-ttu-id="09dcf-128">La valeur par défaut est 65536.</span><span class="sxs-lookup"><span data-stu-id="09dcf-128">The default is 65536.</span></span>|  
|<span data-ttu-id="09dcf-129">port</span><span class="sxs-lookup"><span data-stu-id="09dcf-129">port</span></span>|<span data-ttu-id="09dcf-130">Entier indiquant le port d’interface réseau utilisé par cette liaison pour traiter les messages TCP du canal homologue.</span><span class="sxs-lookup"><span data-stu-id="09dcf-130">An integer that specifies the network interface port on which this binding will process peer channel TCP messages.</span></span> <span data-ttu-id="09dcf-131">Cette valeur doit être comprise entre <xref:System.Net.IPEndPoint.MinPort> et <xref:System.Net.IPEndPoint.MaxPort>.</span><span class="sxs-lookup"><span data-stu-id="09dcf-131">This value must be between <xref:System.Net.IPEndPoint.MinPort> and <xref:System.Net.IPEndPoint.MaxPort>.</span></span> <span data-ttu-id="09dcf-132">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="09dcf-132">The default is 0.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="09dcf-133">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="09dcf-133">Child Elements</span></span>  
  
|<span data-ttu-id="09dcf-134">Élément</span><span class="sxs-lookup"><span data-stu-id="09dcf-134">Element</span></span>|<span data-ttu-id="09dcf-135">Description</span><span class="sxs-lookup"><span data-stu-id="09dcf-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="09dcf-136">\<security></span><span class="sxs-lookup"><span data-stu-id="09dcf-136">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-peertransport.md)|<span data-ttu-id="09dcf-137">Définit les paramètres de sécurité correspondant à ce transport.</span><span class="sxs-lookup"><span data-stu-id="09dcf-137">Defines the security settings for this transport.</span></span> <span data-ttu-id="09dcf-138">Cet élément est de type <xref:System.ServiceModel.Configuration.PeerSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="09dcf-138">This element is of type <xref:System.ServiceModel.Configuration.PeerSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="09dcf-139">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="09dcf-139">Parent Elements</span></span>  
  
|<span data-ttu-id="09dcf-140">Élément</span><span class="sxs-lookup"><span data-stu-id="09dcf-140">Element</span></span>|<span data-ttu-id="09dcf-141">Description</span><span class="sxs-lookup"><span data-stu-id="09dcf-141">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="09dcf-142">\<binding></span><span class="sxs-lookup"><span data-stu-id="09dcf-142">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="09dcf-143">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="09dcf-143">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="09dcf-144">Notes</span><span class="sxs-lookup"><span data-stu-id="09dcf-144">Remarks</span></span>  
 <span data-ttu-id="09dcf-145">Ce transport ne peut pas être utilisé avec les contrats comportant des opérations de demande/réponse.</span><span class="sxs-lookup"><span data-stu-id="09dcf-145">This transport cannot be used with contracts that have request/reply operations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09dcf-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09dcf-146">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerTransportElement>
- <xref:System.ServiceModel.Channels.PeerTransportBindingElement>
- <xref:System.ServiceModel.Channels.TransportBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="09dcf-147">Transports</span><span class="sxs-lookup"><span data-stu-id="09dcf-147">Transports</span></span>](../../../../../docs/framework/wcf/feature-details/transports.md)
- [<span data-ttu-id="09dcf-148">Choix d’un transport</span><span class="sxs-lookup"><span data-stu-id="09dcf-148">Choosing a Transport</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)
- [<span data-ttu-id="09dcf-149">Liaisons</span><span class="sxs-lookup"><span data-stu-id="09dcf-149">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="09dcf-150">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="09dcf-150">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="09dcf-151">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="09dcf-151">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="09dcf-152">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="09dcf-152">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
