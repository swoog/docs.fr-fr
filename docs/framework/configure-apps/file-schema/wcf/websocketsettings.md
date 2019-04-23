---
title: <webSocketSettings>
ms.date: 03/30/2017
ms.assetid: bbf97e02-8dd1-4922-acac-3cd33397b249
ms.openlocfilehash: 1101d021f3c7436c4f45a22a48e50f6d1553f753
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59226870"
---
# <a name="websocketsettings"></a><span data-ttu-id="d428f-101">\<webSocketSettings></span><span class="sxs-lookup"><span data-stu-id="d428f-101">\<webSocketSettings></span></span>
<span data-ttu-id="d428f-102">Élément de configuration utilisé pour spécifier des paramètres WebSocket.</span><span class="sxs-lookup"><span data-stu-id="d428f-102">A configuration element used to specify Web Socket settings.</span></span>  
  
<span data-ttu-id="d428f-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="d428f-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="d428f-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="d428f-104">\<bindings></span></span>  
<span data-ttu-id="d428f-105">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="d428f-105">\<netHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d428f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d428f-106">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d428f-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d428f-107">Attributes and Elements</span></span>  
 <span data-ttu-id="d428f-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d428f-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d428f-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="d428f-109">Attributes</span></span>  
  
|<span data-ttu-id="d428f-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="d428f-110">Attribute</span></span>|<span data-ttu-id="d428f-111">Description</span><span class="sxs-lookup"><span data-stu-id="d428f-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d428f-112">createNotificationOnConnection</span><span class="sxs-lookup"><span data-stu-id="d428f-112">createNotificationOnConnection</span></span>|<span data-ttu-id="d428f-113">Spécifie si une notification est envoyée lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="d428f-113">Specifies whether a notification is sent upon connection.</span></span>|  
|<span data-ttu-id="d428f-114">disablePayloadMasking</span><span class="sxs-lookup"><span data-stu-id="d428f-114">disablePayloadMasking</span></span>|<span data-ttu-id="d428f-115">Spécifie si le masquage WebSocket est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d428f-115">Specifies whether Web Socket masking is disabled.</span></span>|  
|<span data-ttu-id="d428f-116">keepAliveInterval</span><span class="sxs-lookup"><span data-stu-id="d428f-116">keepAliveInterval</span></span>|<span data-ttu-id="d428f-117">Spécifie l'intervalle de maintien de l'activité.</span><span class="sxs-lookup"><span data-stu-id="d428f-117">Specifies the keep alive interval.</span></span>|  
|<span data-ttu-id="d428f-118">maxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="d428f-118">maxPendingConnections</span></span>|<span data-ttu-id="d428f-119">Spécifie le nombre maximal de connexions entrantes en attente de distribution sur le service.</span><span class="sxs-lookup"><span data-stu-id="d428f-119">Specifies the maximum number of connections awaiting dispatch on the service.</span></span>|  
|<span data-ttu-id="d428f-120">receiveBufferSize</span><span class="sxs-lookup"><span data-stu-id="d428f-120">receiveBufferSize</span></span>|<span data-ttu-id="d428f-121">Spécifie la taille de la mémoire tampon de réception.</span><span class="sxs-lookup"><span data-stu-id="d428f-121">Specifies the size of the receive buffer.</span></span>|  
|<span data-ttu-id="d428f-122">sendBufferSize</span><span class="sxs-lookup"><span data-stu-id="d428f-122">sendBufferSize</span></span>|<span data-ttu-id="d428f-123">Spécifie la taille de la mémoire tampon d'envoi.</span><span class="sxs-lookup"><span data-stu-id="d428f-123">Specifies the size of the send buffer.</span></span>|  
|<span data-ttu-id="d428f-124">subProtocol</span><span class="sxs-lookup"><span data-stu-id="d428f-124">subProtocol</span></span>|<span data-ttu-id="d428f-125">Spécifie le sous-protocole WebSocket.</span><span class="sxs-lookup"><span data-stu-id="d428f-125">Specifies the Web Socket subprotocol.</span></span>|  
|<span data-ttu-id="d428f-126">transportUsage</span><span class="sxs-lookup"><span data-stu-id="d428f-126">transportUsage</span></span>|<span data-ttu-id="d428f-127">Spécifie quand utiliser WebSocket.</span><span class="sxs-lookup"><span data-stu-id="d428f-127">Specifies when to use Web Sockets.</span></span>|  
  
## <a name="transportusage-attribute"></a><span data-ttu-id="d428f-128">Attribut transportUsage</span><span class="sxs-lookup"><span data-stu-id="d428f-128">transportUsage Attribute</span></span>  
  
|<span data-ttu-id="d428f-129">Value</span><span class="sxs-lookup"><span data-stu-id="d428f-129">Value</span></span>|<span data-ttu-id="d428f-130">Description</span><span class="sxs-lookup"><span data-stu-id="d428f-130">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="d428f-131">WhenDuplex</span><span class="sxs-lookup"><span data-stu-id="d428f-131">WhenDuplex</span></span>|<span data-ttu-id="d428f-132">Utilisez le protocole WebSocket lorsque le contrat est en duplex.</span><span class="sxs-lookup"><span data-stu-id="d428f-132">Use the Web Socket protocol when the contract is duplex.</span></span>|  
|<span data-ttu-id="d428f-133">Always</span><span class="sxs-lookup"><span data-stu-id="d428f-133">Always</span></span>|<span data-ttu-id="d428f-134">Utilisez toujours le protocole WebSocket indépendamment du contrat.</span><span class="sxs-lookup"><span data-stu-id="d428f-134">Always use the Web Socket protocol regardless of the contract.</span></span>|  
|<span data-ttu-id="d428f-135">Never</span><span class="sxs-lookup"><span data-stu-id="d428f-135">Never</span></span>|<span data-ttu-id="d428f-136">N'utilisez jamais le protocole WebSocket.</span><span class="sxs-lookup"><span data-stu-id="d428f-136">Never use the Web Socket protocol.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d428f-137">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d428f-137">Child Elements</span></span>  
 <span data-ttu-id="d428f-138">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d428f-138">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d428f-139">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d428f-139">Parent Elements</span></span>  
  
|<span data-ttu-id="d428f-140">Élément</span><span class="sxs-lookup"><span data-stu-id="d428f-140">Element</span></span>|<span data-ttu-id="d428f-141">Description</span><span class="sxs-lookup"><span data-stu-id="d428f-141">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d428f-142">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="d428f-142">\<netHttpBinding></span></span>|<span data-ttu-id="d428f-143">Spécifie le NetHttpBinding</span><span class="sxs-lookup"><span data-stu-id="d428f-143">Specifies the NetHttpBinding</span></span>|  
  
## <a name="example"></a><span data-ttu-id="d428f-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="d428f-144">Example</span></span>  
 <span data-ttu-id="d428f-145">L’exemple suivant montre comment utiliser le \<webSocketSettings > élément.</span><span class="sxs-lookup"><span data-stu-id="d428f-145">The following example shows how to use the \<webSocketSettings> element.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="d428f-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d428f-146">See also</span></span>

- <xref:System.ServiceModel.Channels.Binding>
- <xref:System.ServiceModel.Channels.BindingElement>
- <xref:System.ServiceModel.BasicHttpBinding>
- <xref:System.ServiceModel.Configuration.BasicHttpBindingElement>
- [<span data-ttu-id="d428f-147">Liaisons</span><span class="sxs-lookup"><span data-stu-id="d428f-147">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="d428f-148">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="d428f-148">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="d428f-149">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="d428f-149">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="d428f-150">\<binding></span><span class="sxs-lookup"><span data-stu-id="d428f-150">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
