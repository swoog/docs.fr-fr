---
title: <webSocketSettings>
ms.date: 03/30/2017
ms.assetid: bbf97e02-8dd1-4922-acac-3cd33397b249
ms.openlocfilehash: 1101d021f3c7436c4f45a22a48e50f6d1553f753
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59226870"
---
# <a name="websocketsettings"></a><span data-ttu-id="86169-101">\<webSocketSettings></span><span class="sxs-lookup"><span data-stu-id="86169-101">\<webSocketSettings></span></span>
<span data-ttu-id="86169-102">Élément de configuration utilisé pour spécifier des paramètres WebSocket.</span><span class="sxs-lookup"><span data-stu-id="86169-102">A configuration element used to specify Web Socket settings.</span></span>  
  
<span data-ttu-id="86169-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="86169-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="86169-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="86169-104">\<bindings></span></span>  
<span data-ttu-id="86169-105">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="86169-105">\<netHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86169-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86169-106">Syntax</span></span>  
  
```xml  
<netHttpBinding>
  <binding>
    <webSocketSettings createNotificationOnConnection="Boolean"
                       disablePayloadMasking="Boolean"
                       keepAliveInterval="TimeSpan"
                       maxPendingConnections="Integer"
                       receiveBufferSize="Integer"
                       sendBufferSize="Integer"
                       subProtocol="String"
                       transportUsage="WhenDuplex/Always/Never" />
  </binding>
</netHttpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="86169-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="86169-107">Attributes and Elements</span></span>  
 <span data-ttu-id="86169-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="86169-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="86169-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="86169-109">Attributes</span></span>  
  
|<span data-ttu-id="86169-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="86169-110">Attribute</span></span>|<span data-ttu-id="86169-111">Description</span><span class="sxs-lookup"><span data-stu-id="86169-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="86169-112">createNotificationOnConnection</span><span class="sxs-lookup"><span data-stu-id="86169-112">createNotificationOnConnection</span></span>|<span data-ttu-id="86169-113">Spécifie si une notification est envoyée lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="86169-113">Specifies whether a notification is sent upon connection.</span></span>|  
|<span data-ttu-id="86169-114">disablePayloadMasking</span><span class="sxs-lookup"><span data-stu-id="86169-114">disablePayloadMasking</span></span>|<span data-ttu-id="86169-115">Spécifie si le masquage WebSocket est désactivé.</span><span class="sxs-lookup"><span data-stu-id="86169-115">Specifies whether Web Socket masking is disabled.</span></span>|  
|<span data-ttu-id="86169-116">keepAliveInterval</span><span class="sxs-lookup"><span data-stu-id="86169-116">keepAliveInterval</span></span>|<span data-ttu-id="86169-117">Spécifie l'intervalle de maintien de l'activité.</span><span class="sxs-lookup"><span data-stu-id="86169-117">Specifies the keep alive interval.</span></span>|  
|<span data-ttu-id="86169-118">maxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="86169-118">maxPendingConnections</span></span>|<span data-ttu-id="86169-119">Spécifie le nombre maximal de connexions entrantes en attente de distribution sur le service.</span><span class="sxs-lookup"><span data-stu-id="86169-119">Specifies the maximum number of connections awaiting dispatch on the service.</span></span>|  
|<span data-ttu-id="86169-120">receiveBufferSize</span><span class="sxs-lookup"><span data-stu-id="86169-120">receiveBufferSize</span></span>|<span data-ttu-id="86169-121">Spécifie la taille de la mémoire tampon de réception.</span><span class="sxs-lookup"><span data-stu-id="86169-121">Specifies the size of the receive buffer.</span></span>|  
|<span data-ttu-id="86169-122">sendBufferSize</span><span class="sxs-lookup"><span data-stu-id="86169-122">sendBufferSize</span></span>|<span data-ttu-id="86169-123">Spécifie la taille de la mémoire tampon d'envoi.</span><span class="sxs-lookup"><span data-stu-id="86169-123">Specifies the size of the send buffer.</span></span>|  
|<span data-ttu-id="86169-124">subProtocol</span><span class="sxs-lookup"><span data-stu-id="86169-124">subProtocol</span></span>|<span data-ttu-id="86169-125">Spécifie le sous-protocole WebSocket.</span><span class="sxs-lookup"><span data-stu-id="86169-125">Specifies the Web Socket subprotocol.</span></span>|  
|<span data-ttu-id="86169-126">transportUsage</span><span class="sxs-lookup"><span data-stu-id="86169-126">transportUsage</span></span>|<span data-ttu-id="86169-127">Spécifie quand utiliser WebSocket.</span><span class="sxs-lookup"><span data-stu-id="86169-127">Specifies when to use Web Sockets.</span></span>|  
  
## <a name="transportusage-attribute"></a><span data-ttu-id="86169-128">Attribut transportUsage</span><span class="sxs-lookup"><span data-stu-id="86169-128">transportUsage Attribute</span></span>  
  
|<span data-ttu-id="86169-129">Value</span><span class="sxs-lookup"><span data-stu-id="86169-129">Value</span></span>|<span data-ttu-id="86169-130">Description</span><span class="sxs-lookup"><span data-stu-id="86169-130">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="86169-131">WhenDuplex</span><span class="sxs-lookup"><span data-stu-id="86169-131">WhenDuplex</span></span>|<span data-ttu-id="86169-132">Utilisez le protocole WebSocket lorsque le contrat est en duplex.</span><span class="sxs-lookup"><span data-stu-id="86169-132">Use the Web Socket protocol when the contract is duplex.</span></span>|  
|<span data-ttu-id="86169-133">Always</span><span class="sxs-lookup"><span data-stu-id="86169-133">Always</span></span>|<span data-ttu-id="86169-134">Utilisez toujours le protocole WebSocket indépendamment du contrat.</span><span class="sxs-lookup"><span data-stu-id="86169-134">Always use the Web Socket protocol regardless of the contract.</span></span>|  
|<span data-ttu-id="86169-135">Never</span><span class="sxs-lookup"><span data-stu-id="86169-135">Never</span></span>|<span data-ttu-id="86169-136">N'utilisez jamais le protocole WebSocket.</span><span class="sxs-lookup"><span data-stu-id="86169-136">Never use the Web Socket protocol.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="86169-137">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="86169-137">Child Elements</span></span>  
 <span data-ttu-id="86169-138">Aucun.</span><span class="sxs-lookup"><span data-stu-id="86169-138">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="86169-139">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="86169-139">Parent Elements</span></span>  
  
|<span data-ttu-id="86169-140">Élément</span><span class="sxs-lookup"><span data-stu-id="86169-140">Element</span></span>|<span data-ttu-id="86169-141">Description</span><span class="sxs-lookup"><span data-stu-id="86169-141">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="86169-142">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="86169-142">\<netHttpBinding></span></span>|<span data-ttu-id="86169-143">Spécifie le NetHttpBinding</span><span class="sxs-lookup"><span data-stu-id="86169-143">Specifies the NetHttpBinding</span></span>|  
  
## <a name="example"></a><span data-ttu-id="86169-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="86169-144">Example</span></span>  
 <span data-ttu-id="86169-145">L’exemple suivant montre comment utiliser le \<webSocketSettings > élément.</span><span class="sxs-lookup"><span data-stu-id="86169-145">The following example shows how to use the \<webSocketSettings> element.</span></span>  
  
```xml  
<netHttpBinding>
  <binding>
    <webSocketSettings createNotificationOnConnection="true"
                       disablePayloadMasking="false"
                       keepAliveInterval="00:10:00"
                       maxPendingConnections="100"
                       receiveBufferSize="1000"
                       sendBufferSize="1000"
                       subProtocol="Soap"
                       transportUsage="WhenDuplex/Always/Never" />
  </binding>
</netHttpBinding>
```  
  
## <a name="see-also"></a><span data-ttu-id="86169-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86169-146">See also</span></span>

- <xref:System.ServiceModel.Channels.Binding>
- <xref:System.ServiceModel.Channels.BindingElement>
- <xref:System.ServiceModel.BasicHttpBinding>
- <xref:System.ServiceModel.Configuration.BasicHttpBindingElement>
- [<span data-ttu-id="86169-147">Liaisons</span><span class="sxs-lookup"><span data-stu-id="86169-147">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="86169-148">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="86169-148">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="86169-149">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="86169-149">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="86169-150">\<binding></span><span class="sxs-lookup"><span data-stu-id="86169-150">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
