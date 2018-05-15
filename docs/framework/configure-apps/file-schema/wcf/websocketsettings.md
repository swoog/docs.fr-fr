---
title: '&lt;webSocketSettings&gt;'
ms.date: 03/30/2017
ms.assetid: bbf97e02-8dd1-4922-acac-3cd33397b249
ms.openlocfilehash: 84aee31b6c15beb32732f89eae7c3d176f57971d
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltwebsocketsettingsgt"></a><span data-ttu-id="9c528-102">&lt;webSocketSettings&gt;</span><span class="sxs-lookup"><span data-stu-id="9c528-102">&lt;webSocketSettings&gt;</span></span>
<span data-ttu-id="9c528-103">Élément de configuration utilisé pour spécifier des paramètres WebSocket.</span><span class="sxs-lookup"><span data-stu-id="9c528-103">A configuration element used to specify Web Socket settings.</span></span>  
  
<span data-ttu-id="9c528-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="9c528-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="9c528-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="9c528-105">\<bindings></span></span>  
<span data-ttu-id="9c528-106">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="9c528-106">\<netHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c528-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c528-107">Syntax</span></span>  
  
```xml  
<netHttpBinding>  
  <binding>   
    <webSocketSettings createNotificationOnConnection="boolean" 
                       disablePayloadMasking="boolean" 
                       keepAliveInterval="TimeSpan" 
                       maxPendingConnections="Integer" 
                       receiveBufferSize="Integer" 
                       sendBufferSize="Integer" 
                       subProtocol="String" 
                       transportUsage="WhenDuplex/Always/Never"/>
  </binding>  
</netHttpBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9c528-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9c528-108">Attributes and Elements</span></span>  
 <span data-ttu-id="9c528-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9c528-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9c528-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="9c528-110">Attributes</span></span>  
  
|<span data-ttu-id="9c528-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="9c528-111">Attribute</span></span>|<span data-ttu-id="9c528-112">Description</span><span class="sxs-lookup"><span data-stu-id="9c528-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9c528-113">createNotificationOnConnection</span><span class="sxs-lookup"><span data-stu-id="9c528-113">createNotificationOnConnection</span></span>|<span data-ttu-id="9c528-114">Spécifie si une notification est envoyée lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="9c528-114">Specifies whether a notification is sent upon connection.</span></span>|  
|<span data-ttu-id="9c528-115">disablePayloadMasking</span><span class="sxs-lookup"><span data-stu-id="9c528-115">disablePayloadMasking</span></span>|<span data-ttu-id="9c528-116">Spécifie si le masquage WebSocket est désactivé.</span><span class="sxs-lookup"><span data-stu-id="9c528-116">Specifies whether Web Socket masking is disabled.</span></span>|  
|<span data-ttu-id="9c528-117">keepAliveInterval</span><span class="sxs-lookup"><span data-stu-id="9c528-117">keepAliveInterval</span></span>|<span data-ttu-id="9c528-118">Spécifie l'intervalle de maintien de l'activité.</span><span class="sxs-lookup"><span data-stu-id="9c528-118">Specifies the keep alive interval.</span></span>|  
|<span data-ttu-id="9c528-119">maxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="9c528-119">maxPendingConnections</span></span>|<span data-ttu-id="9c528-120">Spécifie le nombre maximal de connexions entrantes en attente de distribution sur le service.</span><span class="sxs-lookup"><span data-stu-id="9c528-120">Specifies the maximum number of connections awaiting dispatch on the service.</span></span>|  
|<span data-ttu-id="9c528-121">receiveBufferSize</span><span class="sxs-lookup"><span data-stu-id="9c528-121">receiveBufferSize</span></span>|<span data-ttu-id="9c528-122">Spécifie la taille de la mémoire tampon de réception.</span><span class="sxs-lookup"><span data-stu-id="9c528-122">Specifies the size of the receive buffer.</span></span>|  
|<span data-ttu-id="9c528-123">sendBufferSize</span><span class="sxs-lookup"><span data-stu-id="9c528-123">sendBufferSize</span></span>|<span data-ttu-id="9c528-124">Spécifie la taille de la mémoire tampon d'envoi.</span><span class="sxs-lookup"><span data-stu-id="9c528-124">Specifies the size of the send buffer.</span></span>|  
|<span data-ttu-id="9c528-125">subProtocol</span><span class="sxs-lookup"><span data-stu-id="9c528-125">subProtocol</span></span>|<span data-ttu-id="9c528-126">Spécifie le sous-protocole WebSocket.</span><span class="sxs-lookup"><span data-stu-id="9c528-126">Specifies the Web Socket subprotocol.</span></span>|  
|<span data-ttu-id="9c528-127">transportUsage</span><span class="sxs-lookup"><span data-stu-id="9c528-127">transportUsage</span></span>|<span data-ttu-id="9c528-128">Spécifie quand utiliser WebSocket.</span><span class="sxs-lookup"><span data-stu-id="9c528-128">Specifies when to use Web Sockets.</span></span>|  
  
## <a name="transportusage-attribute"></a><span data-ttu-id="9c528-129">Attribut transportUsage</span><span class="sxs-lookup"><span data-stu-id="9c528-129">transportUsage Attribute</span></span>  
  
|<span data-ttu-id="9c528-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c528-130">Value</span></span>|<span data-ttu-id="9c528-131">Description</span><span class="sxs-lookup"><span data-stu-id="9c528-131">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="9c528-132">WhenDuplex</span><span class="sxs-lookup"><span data-stu-id="9c528-132">WhenDuplex</span></span>|<span data-ttu-id="9c528-133">Utilisez le protocole WebSocket lorsque le contrat est en duplex.</span><span class="sxs-lookup"><span data-stu-id="9c528-133">Use the Web Socket protocol when the contract is duplex.</span></span>|  
|<span data-ttu-id="9c528-134">Always</span><span class="sxs-lookup"><span data-stu-id="9c528-134">Always</span></span>|<span data-ttu-id="9c528-135">Utilisez toujours le protocole WebSocket indépendamment du contrat.</span><span class="sxs-lookup"><span data-stu-id="9c528-135">Always use the Web Socket protocol regardless of the contract.</span></span>|  
|<span data-ttu-id="9c528-136">Never</span><span class="sxs-lookup"><span data-stu-id="9c528-136">Never</span></span>|<span data-ttu-id="9c528-137">N'utilisez jamais le protocole WebSocket.</span><span class="sxs-lookup"><span data-stu-id="9c528-137">Never use the Web Socket protocol.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9c528-138">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9c528-138">Child Elements</span></span>  
 <span data-ttu-id="9c528-139">Aucun</span><span class="sxs-lookup"><span data-stu-id="9c528-139">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9c528-140">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9c528-140">Parent Elements</span></span>  
  
|<span data-ttu-id="9c528-141">Élément</span><span class="sxs-lookup"><span data-stu-id="9c528-141">Element</span></span>|<span data-ttu-id="9c528-142">Description</span><span class="sxs-lookup"><span data-stu-id="9c528-142">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9c528-143">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="9c528-143">\<netHttpBinding></span></span>|<span data-ttu-id="9c528-144">Spécifie le NetHttpBinding</span><span class="sxs-lookup"><span data-stu-id="9c528-144">Specifies the NetHttpBinding</span></span>|  
  
## <a name="example"></a><span data-ttu-id="9c528-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="9c528-145">Example</span></span>  
 <span data-ttu-id="9c528-146">L’exemple suivant montre comment utiliser le \<webSocketSettings > élément.</span><span class="sxs-lookup"><span data-stu-id="9c528-146">The following example shows how to use the \<webSocketSettings> element.</span></span>  
  
```xml  
<netHttpBinding>  
        <binding>  
          <webSocketSettings createNotificationOnConnection="true"  
                              disablePayloadMasking="false  
                              keepAliveInterval="00:10:00"  
                              maxPendingConnections="100"  
                              receiveBufferSize="1000"  
                              sendBufferSize="1000"  
                              subProtocol="Soap"  
                              transportUsage="WhenDuplex/Always/Never"/>  
  
        </binding>  
      </netHttpBinding>  
```  
  
## <a name="see-also"></a><span data-ttu-id="9c528-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c528-147">See Also</span></span>  
 <xref:System.ServiceModel.Channels.Binding>  
 <xref:System.ServiceModel.Channels.BindingElement>  
 <xref:System.ServiceModel.BasicHttpBinding>  
 <xref:System.ServiceModel.Configuration.BasicHttpBindingElement>  
 [<span data-ttu-id="9c528-148">Liaisons</span><span class="sxs-lookup"><span data-stu-id="9c528-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="9c528-149">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="9c528-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="9c528-150">Utilisation de liaisons pour configurer les Clients et les Services Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="9c528-150">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](http://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="9c528-151">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="9c528-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
