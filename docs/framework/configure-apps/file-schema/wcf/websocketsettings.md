---
title: '&lt;webSocketSettings&gt;'
ms.date: 03/30/2017
ms.assetid: bbf97e02-8dd1-4922-acac-3cd33397b249
ms.openlocfilehash: 94a5883c37221a8d637a188fe42aad220a332575
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48582396"
---
# <a name="ltwebsocketsettingsgt"></a><span data-ttu-id="ad1fd-102">&lt;webSocketSettings&gt;</span><span class="sxs-lookup"><span data-stu-id="ad1fd-102">&lt;webSocketSettings&gt;</span></span>
<span data-ttu-id="ad1fd-103">Élément de configuration utilisé pour spécifier des paramètres WebSocket.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-103">A configuration element used to specify Web Socket settings.</span></span>  
  
<span data-ttu-id="ad1fd-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="ad1fd-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="ad1fd-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="ad1fd-105">\<bindings></span></span>  
<span data-ttu-id="ad1fd-106">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="ad1fd-106">\<netHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad1fd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad1fd-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ad1fd-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ad1fd-108">Attributes and Elements</span></span>  
 <span data-ttu-id="ad1fd-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ad1fd-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="ad1fd-110">Attributes</span></span>  
  
|<span data-ttu-id="ad1fd-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="ad1fd-111">Attribute</span></span>|<span data-ttu-id="ad1fd-112">Description</span><span class="sxs-lookup"><span data-stu-id="ad1fd-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ad1fd-113">createNotificationOnConnection</span><span class="sxs-lookup"><span data-stu-id="ad1fd-113">createNotificationOnConnection</span></span>|<span data-ttu-id="ad1fd-114">Spécifie si une notification est envoyée lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-114">Specifies whether a notification is sent upon connection.</span></span>|  
|<span data-ttu-id="ad1fd-115">disablePayloadMasking</span><span class="sxs-lookup"><span data-stu-id="ad1fd-115">disablePayloadMasking</span></span>|<span data-ttu-id="ad1fd-116">Spécifie si le masquage WebSocket est désactivé.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-116">Specifies whether Web Socket masking is disabled.</span></span>|  
|<span data-ttu-id="ad1fd-117">keepAliveInterval</span><span class="sxs-lookup"><span data-stu-id="ad1fd-117">keepAliveInterval</span></span>|<span data-ttu-id="ad1fd-118">Spécifie l'intervalle de maintien de l'activité.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-118">Specifies the keep alive interval.</span></span>|  
|<span data-ttu-id="ad1fd-119">maxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="ad1fd-119">maxPendingConnections</span></span>|<span data-ttu-id="ad1fd-120">Spécifie le nombre maximal de connexions entrantes en attente de distribution sur le service.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-120">Specifies the maximum number of connections awaiting dispatch on the service.</span></span>|  
|<span data-ttu-id="ad1fd-121">receiveBufferSize</span><span class="sxs-lookup"><span data-stu-id="ad1fd-121">receiveBufferSize</span></span>|<span data-ttu-id="ad1fd-122">Spécifie la taille de la mémoire tampon de réception.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-122">Specifies the size of the receive buffer.</span></span>|  
|<span data-ttu-id="ad1fd-123">sendBufferSize</span><span class="sxs-lookup"><span data-stu-id="ad1fd-123">sendBufferSize</span></span>|<span data-ttu-id="ad1fd-124">Spécifie la taille de la mémoire tampon d'envoi.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-124">Specifies the size of the send buffer.</span></span>|  
|<span data-ttu-id="ad1fd-125">subProtocol</span><span class="sxs-lookup"><span data-stu-id="ad1fd-125">subProtocol</span></span>|<span data-ttu-id="ad1fd-126">Spécifie le sous-protocole WebSocket.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-126">Specifies the Web Socket subprotocol.</span></span>|  
|<span data-ttu-id="ad1fd-127">transportUsage</span><span class="sxs-lookup"><span data-stu-id="ad1fd-127">transportUsage</span></span>|<span data-ttu-id="ad1fd-128">Spécifie quand utiliser WebSocket.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-128">Specifies when to use Web Sockets.</span></span>|  
  
## <a name="transportusage-attribute"></a><span data-ttu-id="ad1fd-129">Attribut transportUsage</span><span class="sxs-lookup"><span data-stu-id="ad1fd-129">transportUsage Attribute</span></span>  
  
|<span data-ttu-id="ad1fd-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad1fd-130">Value</span></span>|<span data-ttu-id="ad1fd-131">Description</span><span class="sxs-lookup"><span data-stu-id="ad1fd-131">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="ad1fd-132">WhenDuplex</span><span class="sxs-lookup"><span data-stu-id="ad1fd-132">WhenDuplex</span></span>|<span data-ttu-id="ad1fd-133">Utilisez le protocole WebSocket lorsque le contrat est en duplex.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-133">Use the Web Socket protocol when the contract is duplex.</span></span>|  
|<span data-ttu-id="ad1fd-134">Always</span><span class="sxs-lookup"><span data-stu-id="ad1fd-134">Always</span></span>|<span data-ttu-id="ad1fd-135">Utilisez toujours le protocole WebSocket indépendamment du contrat.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-135">Always use the Web Socket protocol regardless of the contract.</span></span>|  
|<span data-ttu-id="ad1fd-136">Never</span><span class="sxs-lookup"><span data-stu-id="ad1fd-136">Never</span></span>|<span data-ttu-id="ad1fd-137">N'utilisez jamais le protocole WebSocket.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-137">Never use the Web Socket protocol.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ad1fd-138">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ad1fd-138">Child Elements</span></span>  
 <span data-ttu-id="ad1fd-139">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-139">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ad1fd-140">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ad1fd-140">Parent Elements</span></span>  
  
|<span data-ttu-id="ad1fd-141">Élément</span><span class="sxs-lookup"><span data-stu-id="ad1fd-141">Element</span></span>|<span data-ttu-id="ad1fd-142">Description</span><span class="sxs-lookup"><span data-stu-id="ad1fd-142">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ad1fd-143">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="ad1fd-143">\<netHttpBinding></span></span>|<span data-ttu-id="ad1fd-144">Spécifie le NetHttpBinding</span><span class="sxs-lookup"><span data-stu-id="ad1fd-144">Specifies the NetHttpBinding</span></span>|  
  
## <a name="example"></a><span data-ttu-id="ad1fd-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="ad1fd-145">Example</span></span>  
 <span data-ttu-id="ad1fd-146">L’exemple suivant montre comment utiliser le \<webSocketSettings > élément.</span><span class="sxs-lookup"><span data-stu-id="ad1fd-146">The following example shows how to use the \<webSocketSettings> element.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="ad1fd-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad1fd-147">See Also</span></span>  
 <xref:System.ServiceModel.Channels.Binding>  
 <xref:System.ServiceModel.Channels.BindingElement>  
 <xref:System.ServiceModel.BasicHttpBinding>  
 <xref:System.ServiceModel.Configuration.BasicHttpBindingElement>  
 [<span data-ttu-id="ad1fd-148">Liaisons</span><span class="sxs-lookup"><span data-stu-id="ad1fd-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="ad1fd-149">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="ad1fd-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="ad1fd-150">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="ad1fd-150">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="ad1fd-151">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="ad1fd-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
