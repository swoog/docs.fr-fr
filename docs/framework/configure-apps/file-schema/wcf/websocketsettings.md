---
title: '&lt;webSocketSettings&gt;'
ms.date: 03/30/2017
ms.assetid: bbf97e02-8dd1-4922-acac-3cd33397b249
ms.openlocfilehash: 134a233a337c40d21f7547fe385ec788cef2165b
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150056"
---
# <a name="ltwebsocketsettingsgt"></a><span data-ttu-id="fbe75-102">&lt;webSocketSettings&gt;</span><span class="sxs-lookup"><span data-stu-id="fbe75-102">&lt;webSocketSettings&gt;</span></span>
<span data-ttu-id="fbe75-103">Élément de configuration utilisé pour spécifier des paramètres WebSocket.</span><span class="sxs-lookup"><span data-stu-id="fbe75-103">A configuration element used to specify Web Socket settings.</span></span>  
  
<span data-ttu-id="fbe75-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="fbe75-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="fbe75-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="fbe75-105">\<bindings></span></span>  
<span data-ttu-id="fbe75-106">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="fbe75-106">\<netHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fbe75-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbe75-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fbe75-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="fbe75-108">Attributes and Elements</span></span>  
 <span data-ttu-id="fbe75-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="fbe75-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fbe75-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="fbe75-110">Attributes</span></span>  
  
|<span data-ttu-id="fbe75-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="fbe75-111">Attribute</span></span>|<span data-ttu-id="fbe75-112">Description</span><span class="sxs-lookup"><span data-stu-id="fbe75-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="fbe75-113">createNotificationOnConnection</span><span class="sxs-lookup"><span data-stu-id="fbe75-113">createNotificationOnConnection</span></span>|<span data-ttu-id="fbe75-114">Spécifie si une notification est envoyée lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="fbe75-114">Specifies whether a notification is sent upon connection.</span></span>|  
|<span data-ttu-id="fbe75-115">disablePayloadMasking</span><span class="sxs-lookup"><span data-stu-id="fbe75-115">disablePayloadMasking</span></span>|<span data-ttu-id="fbe75-116">Spécifie si le masquage WebSocket est désactivé.</span><span class="sxs-lookup"><span data-stu-id="fbe75-116">Specifies whether Web Socket masking is disabled.</span></span>|  
|<span data-ttu-id="fbe75-117">keepAliveInterval</span><span class="sxs-lookup"><span data-stu-id="fbe75-117">keepAliveInterval</span></span>|<span data-ttu-id="fbe75-118">Spécifie l'intervalle de maintien de l'activité.</span><span class="sxs-lookup"><span data-stu-id="fbe75-118">Specifies the keep alive interval.</span></span>|  
|<span data-ttu-id="fbe75-119">maxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="fbe75-119">maxPendingConnections</span></span>|<span data-ttu-id="fbe75-120">Spécifie le nombre maximal de connexions entrantes en attente de distribution sur le service.</span><span class="sxs-lookup"><span data-stu-id="fbe75-120">Specifies the maximum number of connections awaiting dispatch on the service.</span></span>|  
|<span data-ttu-id="fbe75-121">receiveBufferSize</span><span class="sxs-lookup"><span data-stu-id="fbe75-121">receiveBufferSize</span></span>|<span data-ttu-id="fbe75-122">Spécifie la taille de la mémoire tampon de réception.</span><span class="sxs-lookup"><span data-stu-id="fbe75-122">Specifies the size of the receive buffer.</span></span>|  
|<span data-ttu-id="fbe75-123">sendBufferSize</span><span class="sxs-lookup"><span data-stu-id="fbe75-123">sendBufferSize</span></span>|<span data-ttu-id="fbe75-124">Spécifie la taille de la mémoire tampon d'envoi.</span><span class="sxs-lookup"><span data-stu-id="fbe75-124">Specifies the size of the send buffer.</span></span>|  
|<span data-ttu-id="fbe75-125">subProtocol</span><span class="sxs-lookup"><span data-stu-id="fbe75-125">subProtocol</span></span>|<span data-ttu-id="fbe75-126">Spécifie le sous-protocole WebSocket.</span><span class="sxs-lookup"><span data-stu-id="fbe75-126">Specifies the Web Socket subprotocol.</span></span>|  
|<span data-ttu-id="fbe75-127">transportUsage</span><span class="sxs-lookup"><span data-stu-id="fbe75-127">transportUsage</span></span>|<span data-ttu-id="fbe75-128">Spécifie quand utiliser WebSocket.</span><span class="sxs-lookup"><span data-stu-id="fbe75-128">Specifies when to use Web Sockets.</span></span>|  
  
## <a name="transportusage-attribute"></a><span data-ttu-id="fbe75-129">Attribut transportUsage</span><span class="sxs-lookup"><span data-stu-id="fbe75-129">transportUsage Attribute</span></span>  
  
|<span data-ttu-id="fbe75-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbe75-130">Value</span></span>|<span data-ttu-id="fbe75-131">Description</span><span class="sxs-lookup"><span data-stu-id="fbe75-131">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="fbe75-132">WhenDuplex</span><span class="sxs-lookup"><span data-stu-id="fbe75-132">WhenDuplex</span></span>|<span data-ttu-id="fbe75-133">Utilisez le protocole WebSocket lorsque le contrat est en duplex.</span><span class="sxs-lookup"><span data-stu-id="fbe75-133">Use the Web Socket protocol when the contract is duplex.</span></span>|  
|<span data-ttu-id="fbe75-134">Always</span><span class="sxs-lookup"><span data-stu-id="fbe75-134">Always</span></span>|<span data-ttu-id="fbe75-135">Utilisez toujours le protocole WebSocket indépendamment du contrat.</span><span class="sxs-lookup"><span data-stu-id="fbe75-135">Always use the Web Socket protocol regardless of the contract.</span></span>|  
|<span data-ttu-id="fbe75-136">Never</span><span class="sxs-lookup"><span data-stu-id="fbe75-136">Never</span></span>|<span data-ttu-id="fbe75-137">N'utilisez jamais le protocole WebSocket.</span><span class="sxs-lookup"><span data-stu-id="fbe75-137">Never use the Web Socket protocol.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="fbe75-138">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fbe75-138">Child Elements</span></span>  
 <span data-ttu-id="fbe75-139">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fbe75-139">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="fbe75-140">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fbe75-140">Parent Elements</span></span>  
  
|<span data-ttu-id="fbe75-141">Élément</span><span class="sxs-lookup"><span data-stu-id="fbe75-141">Element</span></span>|<span data-ttu-id="fbe75-142">Description</span><span class="sxs-lookup"><span data-stu-id="fbe75-142">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fbe75-143">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="fbe75-143">\<netHttpBinding></span></span>|<span data-ttu-id="fbe75-144">Spécifie le NetHttpBinding</span><span class="sxs-lookup"><span data-stu-id="fbe75-144">Specifies the NetHttpBinding</span></span>|  
  
## <a name="example"></a><span data-ttu-id="fbe75-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="fbe75-145">Example</span></span>  
 <span data-ttu-id="fbe75-146">L’exemple suivant montre comment utiliser le \<webSocketSettings > élément.</span><span class="sxs-lookup"><span data-stu-id="fbe75-146">The following example shows how to use the \<webSocketSettings> element.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="fbe75-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbe75-147">See Also</span></span>  
 <xref:System.ServiceModel.Channels.Binding>  
 <xref:System.ServiceModel.Channels.BindingElement>  
 <xref:System.ServiceModel.BasicHttpBinding>  
 <xref:System.ServiceModel.Configuration.BasicHttpBindingElement>  
 [<span data-ttu-id="fbe75-148">Liaisons</span><span class="sxs-lookup"><span data-stu-id="fbe75-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="fbe75-149">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="fbe75-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="fbe75-150">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="fbe75-150">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="fbe75-151">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="fbe75-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
