---
title: <netHttpsBinding>
ms.date: 03/30/2017
ms.assetid: ff122116-6042-4792-9f21-275b4f97a105
ms.openlocfilehash: 400444c0346b47d86ad799d4f8f2e7531b74a94c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59195226"
---
# <a name="nethttpsbinding"></a><span data-ttu-id="e0d7e-101">\<netHttpsBinding></span><span class="sxs-lookup"><span data-stu-id="e0d7e-101">\<netHttpsBinding></span></span>
<span data-ttu-id="e0d7e-102">Représente une liaison qu’un service Windows Communication Foundation (WCF) peut utiliser pour configurer et exposer des points de terminaison qui sont en mesure de communiquer via le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-102">Represents a binding that a Windows Communication Foundation (WCF) service can use to configure and expose endpoints that are able to communicate over HTTPS.</span></span> <span data-ttu-id="e0d7e-103">Lorsqu'elle est utilisée avec un contrat duplex, WebSocket est utilisé, sinon HTTPS est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-103">When used with a duplex contract, Web Sockets will be used, otherwise HTTPS will be used.</span></span>  
  
 <span data-ttu-id="e0d7e-104">Élément racine</span><span class="sxs-lookup"><span data-stu-id="e0d7e-104">Root Element</span></span>  
<span data-ttu-id="e0d7e-105">Élément suivant</span><span class="sxs-lookup"><span data-stu-id="e0d7e-105">Next Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0d7e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0d7e-106">Syntax</span></span>  
  
```xml  
<netHttpsBinding>
  <binding allowCookies="Boolean"
           bypassProxyOnLocal="Boolean"
           closeTimeout="TimeSpan"
           hostNameComparisonMode="StrongWildCard/Exact/WeakWildcard"
           maxBufferPoolSize="Integer"
           maxBufferSize="Integer"
           maxReceivedMessageSize="Integer"
           messageEncoding="Binary/Text/Mtom"
           name="string"
           openTimeout="TimeSpan"
           proxyAddress="URI"
           receiveTimeout="TimeSpan"
           sendTimeout="TimeSpan"
           textEncoding="UnicodeFffeTextEncoding/Utf16TextEncoding/Utf8TextEncoding"
           transferMode="Buffered/Streamed/StreamedRequest/StreamedResponse"
           useDefaultWebProxy="Boolean">
    <security mode="None/Transport/Message/TransportWithMessageCredential/TransportCredentialOnly">
      <transport clientCredentialType="None/Basic/Digest/Ntlm/Windows/Certificate"
                 proxyCredentialType="None/Basic/Digest/Ntlm/Windows"
                 realm="string" />
      <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               clientCredentialType="UserName/Certificate" />
    </security>
    <readerQuotas maxArrayLength="Integer"
                  maxBytesPerRead="Integer"
                  maxDepth="Integer"
                  maxNameTableCharCount="Integer"
                  maxStringContentLength="Integer" />
  </binding>
</netHttpsBinding>
```  
  
## <a name="type"></a><span data-ttu-id="e0d7e-107">Type</span><span class="sxs-lookup"><span data-stu-id="e0d7e-107">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e0d7e-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e0d7e-108">Attributes and Elements</span></span>  
 <span data-ttu-id="e0d7e-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e0d7e-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="e0d7e-110">Attributes</span></span>  
  
|<span data-ttu-id="e0d7e-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="e0d7e-111">Attribute</span></span>|<span data-ttu-id="e0d7e-112">Description</span><span class="sxs-lookup"><span data-stu-id="e0d7e-112">Description</span></span>|  
|---------------|-----------------|  
|`allowCookies`|<span data-ttu-id="e0d7e-113">Valeur booléenne qui indique si le client accepte les cookies et les propage dans de futures demandes.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-113">A Boolean value that indicates whether the client accepts cookies and propagates them on future requests.</span></span> <span data-ttu-id="e0d7e-114">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-114">The default is `false`.</span></span><br /><br /> <span data-ttu-id="e0d7e-115">Vous pouvez utiliser cette propriété lorsque vous interagissez avec les services Web ASMX qui utilisent des cookies.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-115">You can use this property when you interact with ASMX Web services that use cookies.</span></span> <span data-ttu-id="e0d7e-116">De cette manière, vous avez la certitude que les cookies retournés par le serveur sont automatiquement copiés dans toutes les futures demandes du client pour ce service.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-116">In this way, you can be sure that the cookies returned from the server are automatically copied to all future client requests for that service.</span></span>|  
|`bypassProxyOnLocal`|<span data-ttu-id="e0d7e-117">Valeur booléenne qui indique s'il faut ignorer le serveur proxy pour les adresses locales.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-117">A Boolean value that indicates whether to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="e0d7e-118">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-118">The default is `false`.</span></span><br /><br /> <span data-ttu-id="e0d7e-119">Une ressource Internet est locale si elle dispose d'une adresse locale.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-119">An Internet resource is local if it has a local address.</span></span> <span data-ttu-id="e0d7e-120">Une adresse locale est celui qui se trouve sur le même ordinateur, le réseau local ou l’intranet local et est identifiée, syntaxiquement, par l’absence de point (.) comme dans l’URI « http://webserver/« et » http://localhost/».</span><span class="sxs-lookup"><span data-stu-id="e0d7e-120">A local address is one that is on same computer, the local LAN or intranet and is identified, syntactically, by the lack of a period (.) as in the URIs "http://webserver/" and "http://localhost/".</span></span><br /><br /> <span data-ttu-id="e0d7e-121">La définition de cet attribut détermine si les points de terminaison configurés avec le BasicHttpBinding utilisent le serveur proxy lors de l'accès aux ressources locales.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-121">Setting this attribute determines whether endpoints configured with the BasicHttpBinding use the proxy server when accessing local resources.</span></span> <span data-ttu-id="e0d7e-122">Si cet attribut est `true`, les demandes adressées à des ressources Internet locales n'utilisent pas le serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-122">If this attribute is `true`, requests to local Internet resources do not use the proxy server.</span></span> <span data-ttu-id="e0d7e-123">Utilisez le nom d'hôte (plutôt que localhost) si vous souhaitez que les clients traversent un proxy lorsqu'ils parlent aux services sur le même ordinateur et que cet attribut a la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-123">Use the host name (rather than localhost) if you want clients to go through a proxy when talking to services on the same machine when this attribute is set to `true`.</span></span><br /><br /> <span data-ttu-id="e0d7e-124">Si cet attribut est `false`, toutes les demandes Internet sont exécutées par le serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-124">When this attribute is `false`, all Internet requests are made through the proxy server.</span></span>|  
|`closeTimeout`|<span data-ttu-id="e0d7e-125"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de fermeture.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-125">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="e0d7e-126">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-126">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="e0d7e-127">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-127">The default is 00:01:00.</span></span>|  
|`hostNameComparisonMode`|<span data-ttu-id="e0d7e-128">Spécifie le mode de comparaison du nom d'hôte HTTP utilisé pour analyser des URI.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-128">Specifies the HTTP hostname comparison mode used to parse URIs.</span></span> <span data-ttu-id="e0d7e-129">Cet attribut est de type <xref:System.ServiceModel.HostNameComparisonMode>, ce qui indique si le nom d'hôte est utilisé pour atteindre le service en cas de correspondance sur l'URI.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-129">This attribute is of type <xref:System.ServiceModel.HostNameComparisonMode>, which indicates whether the hostname is used to reach the service when matching on the URI.</span></span> <span data-ttu-id="e0d7e-130">La valeur par défaut est <xref:System.ServiceModel.HostNameComparisonMode.StrongWildcard>, qui ignore le nom d'hôte dans la correspondance.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-130">The default value is <xref:System.ServiceModel.HostNameComparisonMode.StrongWildcard>, which ignores the hostname in the match.</span></span>|  
|`maxBufferPoolSize`|<span data-ttu-id="e0d7e-131">Entier qui spécifie la quantité de mémoire maximale allouée pour une utilisation par le gestionnaire de tampons des messages qui reçoivent des messages du canal.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-131">An integer value that specifies the maximum amount of memory that is allocated for use by the manager of the message buffers that receive messages from the channel.</span></span> <span data-ttu-id="e0d7e-132">La valeur par défaut est de 524 288 (0x80000) octets.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-132">The default value is 524288 (0x80000) bytes.</span></span><br /><br /> <span data-ttu-id="e0d7e-133">Le gestionnaire de tampons réduit le coût d'utilisation des mémoires tampons à l'aide d'un pool de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-133">The Buffer Manager minimizes the cost of using buffers by using a buffer pool.</span></span> <span data-ttu-id="e0d7e-134">Les mémoires tampons sont requises par le service pour traiter des messages lorsqu'ils sortent du canal.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-134">Buffers are required to process messages by the service when they come out of the channel.</span></span> <span data-ttu-id="e0d7e-135">S’il n’y a pas mémoire suffisante dans le pool de mémoires tampons pour traiter la charge de message, le gestionnaire de mémoires tampons doit allouer de la mémoire additionnelle dans le segment de mémoire CLR, ce qui augmente le traitement du garbage collection.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-135">If there is not sufficient memory in the buffer pool to process the message load, the Buffer Manager must allocate additional memory from the CLR heap, which increases the garbage collection overhead.</span></span> <span data-ttu-id="e0d7e-136">Une allocation importante de mémoire issue du tas de garbage CLR indique que la taille du pool de mémoires tampons est insuffisante et qu'il est possible d'améliorer les performances en augmentant la limite spécifiée par cet attribut.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-136">Extensive allocation from the CLR garbage heap is an indication that the buffer pool size is too small and that performance can be improved with a larger allocation by increasing the limit specified by this attribute.</span></span>|  
|`maxBufferSize`|<span data-ttu-id="e0d7e-137">Entier qui spécifie la taille maximale, en octets, d’une mémoire tampon qui stocke des messages pendant qu’ils sont traités pour un point de terminaison configuré avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-137">An integer value that specifies the maximum size, in bytes, of a buffer that stores messages while they are processed for an endpoint configured with this binding.</span></span> <span data-ttu-id="e0d7e-138">La valeur par défaut est de 65 536 octets.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-138">The default value is 65,536 bytes.</span></span>|  
|`maxReceivedMessageSize`|<span data-ttu-id="e0d7e-139">Entier positif qui définit la taille maximale du message, en octets, y compris les en-têtes d’un message pouvant être reçu sur un canal configuré avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-139">A positive integer that defines the maximum message size, in bytes, including headers, for a message that can be received on a channel configured with this binding.</span></span> <span data-ttu-id="e0d7e-140">L'expéditeur reçoit une erreur SOAP si le message est trop grand pour le récepteur.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-140">The sender receives a SOAP fault if the message is too large for the receiver.</span></span> <span data-ttu-id="e0d7e-141">Ce dernier dépose le message et crée une entrée d’événement dans le journal de suivi.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-141">The receiver drops the message and creates an entry of the event in the trace log.</span></span> <span data-ttu-id="e0d7e-142">La valeur par défaut est 65 536 octets.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-142">The default is 65,536 bytes.</span></span>|  
|`messageEncoding`|<span data-ttu-id="e0d7e-143">Définit l'encodeur utilisé pour encoder le message SOAP.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-143">Defines the encoder used to encode the SOAP message.</span></span> <span data-ttu-id="e0d7e-144">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e0d7e-144">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="e0d7e-145">-Texte : Utiliser un encodeur de message texte.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-145">-   Text: Use a text message encoder.</span></span><br /><span data-ttu-id="e0d7e-146">-   Mtom: Utiliser un encodeur Message Transmission Organization Mechanism 1.0 (MTOM).</span><span class="sxs-lookup"><span data-stu-id="e0d7e-146">-   Mtom: Use a Message Transmission Organization Mechanism 1.0 (MTOM) encoder.</span></span><br /><br /> <span data-ttu-id="e0d7e-147">La valeur par défaut est Text.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-147">The default is Text.</span></span> <span data-ttu-id="e0d7e-148">Cet attribut est de type <xref:System.ServiceModel.WSMessageEncoding>.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-148">This attribute is of type <xref:System.ServiceModel.WSMessageEncoding>.</span></span>|  
|`name`|<span data-ttu-id="e0d7e-149">Chaîne qui contient le nom de configuration de la liaison.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-149">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="e0d7e-150">Cette valeur doit être unique car elle permet d'identifier la liaison.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-150">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="e0d7e-151">Chaque liaison porte un `name` et a un attribut `namespace` qui l’identifient de façon unique dans les métadonnées du service.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-151">Each binding has a `name` and `namespace` attribute that together uniquely identify it in the metadata of the service.</span></span> <span data-ttu-id="e0d7e-152">De plus, ce nom est unique parmi les liaisons du même type.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-152">In addition, this name is unique among bindings of the same type.</span></span> <span data-ttu-id="e0d7e-153">Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d’avoir un nom.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-153">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="e0d7e-154">Pour plus d’informations sur la configuration par défaut et les liaisons sans nom et les comportements, consultez [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="e0d7e-154">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|`namespace`|<span data-ttu-id="e0d7e-155">Spécifie l'espace de noms XML de la liaison.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-155">Specifies the XML namespace of the binding.</span></span> <span data-ttu-id="e0d7e-156">La valeur par défaut est « http://tempuri.org/Bindings ».</span><span class="sxs-lookup"><span data-stu-id="e0d7e-156">The default value is "http://tempuri.org/Bindings".</span></span> <span data-ttu-id="e0d7e-157">Chaque liaison porte un `name` et a un attribut `namespace` qui l’identifient de façon unique dans les métadonnées du service.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-157">Each binding has a `name` and `namespace` attribute that together uniquely identify it in the metadata of the service.</span></span>|  
|`openTimeout`|<span data-ttu-id="e0d7e-158"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'ouverture.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-158">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="e0d7e-159">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-159">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="e0d7e-160">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-160">The default is 00:01:00.</span></span>|  
|`proxyAddress`|<span data-ttu-id="e0d7e-161">URI qui contient l'adresse du proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-161">A URI that contains the address of the HTTP proxy.</span></span> <span data-ttu-id="e0d7e-162">Si `useSystemWebProxy` a la valeur `true` ce paramètre doit avoir la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-162">If `useSystemWebProxy` is set to `true`, this setting must be `null`.</span></span> <span data-ttu-id="e0d7e-163">La valeur par défaut est `null`.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-163">The default is `null`.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="e0d7e-164"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de réception.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-164">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="e0d7e-165">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-165">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="e0d7e-166">La valeur par défaut est 00:10:00.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-166">The default is 00:10:00.</span></span>|  
|`sendTimeout`|<span data-ttu-id="e0d7e-167"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'envoi.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-167">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="e0d7e-168">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-168">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="e0d7e-169">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-169">The default is 00:01:00.</span></span>|  
|`textEncoding`|<span data-ttu-id="e0d7e-170">Définit l'encodage de jeu de caractères à utiliser pour l'émission de messages sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-170">Sets the character set encoding to be used for emitting messages on the binding.</span></span> <span data-ttu-id="e0d7e-171">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e0d7e-171">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="e0d7e-172">-   BigEndianUnicode: Codage Unicode BigEndian.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-172">-   BigEndianUnicode: Unicode BigEndian encoding.</span></span><br /><span data-ttu-id="e0d7e-173">-Unicode : encodage 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-173">-   Unicode: 16-bit encoding.</span></span><br /><span data-ttu-id="e0d7e-174">-UTF-8 : codage 8 bits</span><span class="sxs-lookup"><span data-stu-id="e0d7e-174">-   UTF8: 8-bit encoding</span></span><br /><br /> <span data-ttu-id="e0d7e-175">La valeur par défaut est UTF8.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-175">The default is UTF8.</span></span> <span data-ttu-id="e0d7e-176">Cet attribut est de type <xref:System.Text.Encoding>.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-176">This attribute is of type <xref:System.Text.Encoding>.</span></span>|  
|`transferMode`|<span data-ttu-id="e0d7e-177">Valeur <xref:System.ServiceModel.TransferMode> valide qui spécifie si les messages sont mis en mémoire tampon ou transmis en continu dans une demande ou une réponse.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-177">A valid <xref:System.ServiceModel.TransferMode> value that specifies whether messages are buffered or streamed on a request or response.</span></span>|  
|`useDefaultWebProxy`|<span data-ttu-id="e0d7e-178">Valeur booléenne qui spécifie si le proxy HTTP du système, configuré automatiquement, doit être utilisé, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-178">A Boolean value that specifies whether the auto-configured HTTP proxy of the system should be used, if available.</span></span> <span data-ttu-id="e0d7e-179">La valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-179">The default is `true`.</span></span>|  
|||  
  
### <a name="child-elements"></a><span data-ttu-id="e0d7e-180">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e0d7e-180">Child Elements</span></span>  
  
|<span data-ttu-id="e0d7e-181">Élément</span><span class="sxs-lookup"><span data-stu-id="e0d7e-181">Element</span></span>|<span data-ttu-id="e0d7e-182">Description</span><span class="sxs-lookup"><span data-stu-id="e0d7e-182">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e0d7e-183">\<security></span><span class="sxs-lookup"><span data-stu-id="e0d7e-183">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-nethttpbinding.md)|<span data-ttu-id="e0d7e-184">Définit les paramètres de sécurité de la liaison.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-184">Defines the security settings for the binding.</span></span> <span data-ttu-id="e0d7e-185">Cet élément est de type <xref:System.ServiceModel.Configuration.BasicHttpsSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-185">This element is of type <xref:System.ServiceModel.Configuration.BasicHttpsSecurityElement>.</span></span> |  
|[<span data-ttu-id="e0d7e-186">\<readerQuotas></span><span class="sxs-lookup"><span data-stu-id="e0d7e-186">\<readerQuotas></span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))|<span data-ttu-id="e0d7e-187">Définit les contraintes sur la complexité des messages SOAP pouvant être traités par les points de terminaison configurés avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-187">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="e0d7e-188">Cet élément est de type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-188">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e0d7e-189">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e0d7e-189">Parent Elements</span></span>  
  
|<span data-ttu-id="e0d7e-190">Élément</span><span class="sxs-lookup"><span data-stu-id="e0d7e-190">Element</span></span>|<span data-ttu-id="e0d7e-191">Description</span><span class="sxs-lookup"><span data-stu-id="e0d7e-191">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e0d7e-192">\<bindings></span><span class="sxs-lookup"><span data-stu-id="e0d7e-192">\<bindings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|<span data-ttu-id="e0d7e-193">Cet élément conserve une collection de liaisons standard et personnalisées.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-193">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e0d7e-194">Notes</span><span class="sxs-lookup"><span data-stu-id="e0d7e-194">Remarks</span></span>  
 <span data-ttu-id="e0d7e-195">Le NetHttpsBinding utilise HTTPS en guise de transport pour envoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-195">The NetHttpsBinding uses HTTPS as the transport for sending messages.</span></span> <span data-ttu-id="e0d7e-196">Lorsqu'elle est utilisée avec un contrat duplex, WebSocket est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-196">When used with a duplex contract, Web Sockets will be used.</span></span>  <span data-ttu-id="e0d7e-197">Lorsqu'elle est utilisée avec un contrat de demande-réponse, NetHttpsBinding se comporte comme un BasicHttpsBinding avec un encodeur binaire.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-197">When used with a request-reply contract NetHttpsBinding will behave like a BasicHttpsBinding with a binary encoder.</span></span>  
  
 <span data-ttu-id="e0d7e-198">Sécurité est désactivée par défaut, mais peut être ajoutée en affectant l’attribut mode de le [ \<sécurité >](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-basichttpbinding.md) élément enfant à une valeur autre que `None`.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-198">Security is turned off by default, but can be added setting the mode attribute of the [\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-basichttpbinding.md) child element to a value other than `None`.</span></span> <span data-ttu-id="e0d7e-199">Par défaut, il utilise un encodage de message "Texte" et un encodage texte UTF-8.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-199">It uses a "Text" message encoding and UTF-8 text encoding by default.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e0d7e-200">Exemple</span><span class="sxs-lookup"><span data-stu-id="e0d7e-200">Example</span></span>  
 <span data-ttu-id="e0d7e-201">L'exemple suivant montre l'utilisation de <xref:System.ServiceModel.NetHttpBinding> qui fournit la communication HTTPS et l'interopérabilité maximale avec les services Web de première et seconde génération.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-201">The following example demonstrates the use of <xref:System.ServiceModel.NetHttpBinding> that provides HTTPS communication and maximum interoperability with first- and second-generation Web services.</span></span> <span data-ttu-id="e0d7e-202">La liaison est spécifiée dans les fichiers de configuration pour le client et le service.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-202">The binding is specified in the configuration files for the client and service.</span></span> <span data-ttu-id="e0d7e-203">Le type de liaison est spécifié à l’aide de l’attribut `binding` de l’élément `<endpoint>`.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-203">The binding type is specified using the `binding` attribute of the `<endpoint>` element.</span></span> <span data-ttu-id="e0d7e-204">Si vous souhaitez configurer la liaison de base et modifier certains de ses paramètres, vous devez définir une configuration de liaison.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-204">If you want to configure the basic binding and change some of its settings, it is necessary to define a binding configuration.</span></span> <span data-ttu-id="e0d7e-205">Le point de terminaison doit référencer la configuration de liaison par nom en utilisant l’attribut `bindingConfiguration` de l’élément `<endpoint>`, comme présenté dans le code de configuration suivant pour le service.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-205">The endpoint must reference the binding configuration by name by using the `bindingConfiguration` attribute of the `<endpoint>` element, as shown in the following configuration code for the service.</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service type="Microsoft.ServiceModel.Samples.CalculatorService"
             behaviorConfiguration="CalculatorServiceBehavior">
      <endpoint address=""
                binding="netHttpsBinding"
                bindingConfiguration="Binding1"
                contract="Microsoft.ServiceModel.Samples.ICalculator" />
    </service>
  </services>
  <bindings>
    <netHttpsBinding>
      <binding name="Binding1"
               hostNameComparisonMode="StrongWildcard"
               receiveTimeout="00:10:00"
               sendTimeout="00:10:00"
               openTimeout="00:10:00"
               closeTimeout="00:10:00"
               maxReceivedMessageSize="65536"
               maxBufferSize="65536"
               maxBufferPoolSize="524288"
               transferMode="Buffered"
               messageEncoding="Binary"
               textEncoding="utf-8"
               bypassProxyOnLocal="false"
               useDefaultWebProxy="true">
        <security mode="None" />
      </binding>
    </netHttpsBinding>
  </bindings>
</system.serviceModel>
```  
  
## <a name="example"></a><span data-ttu-id="e0d7e-206">Exemple</span><span class="sxs-lookup"><span data-stu-id="e0d7e-206">Example</span></span>  
 <span data-ttu-id="e0d7e-207">Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d’avoir un nom.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-207">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="e0d7e-208">La fonctionnalité de l’exemple précédent est possible en supprimant le bindingConfiguration de l’adresse de point de terminaison et le nom de la liaison.</span><span class="sxs-lookup"><span data-stu-id="e0d7e-208">The functionality from the previous example can be accomplished by removing the bindingConfiguration from the endpoint address and the name from the binding.</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service type="Microsoft.ServiceModel.Samples.CalculatorService"
             behaviorConfiguration="CalculatorServiceBehavior">
      <endpoint address=""
                binding="netHttpsBinding"
                contract="Microsoft.ServiceModel.Samples.ICalculator" />
    </service>
  </services>
  <bindings>
    <netHttpsBinding>
      <binding hostNameComparisonMode="StrongWildcard"
               receiveTimeout="00:10:00"
               sendTimeout="00:10:00"
               openTimeout="00:10:00"
               closeTimeout="00:10:00"
               maxReceivedMessageSize="65536"
               maxBufferSize="65536"
               maxBufferPoolSize="524288"
               transferMode="Buffered"
               messageEncoding="Binary"
               textEncoding="utf-8"
               bypassProxyOnLocal="false"
               useDefaultWebProxy="true">
        <security mode="None" />
      </binding>
    </netHttpsBinding>
  </bindings>
</system.serviceModel>
```  
  
 <span data-ttu-id="e0d7e-209">Pour plus d’informations sur la configuration par défaut et les liaisons sans nom et les comportements, consultez [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="e0d7e-209">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0d7e-210">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0d7e-210">See also</span></span>

- <xref:System.ServiceModel.Channels.Binding>
- <xref:System.ServiceModel.Channels.BindingElement>
- <xref:System.ServiceModel.BasicHttpBinding>
- <xref:System.ServiceModel.Configuration.BasicHttpBindingElement>
- [<span data-ttu-id="e0d7e-211">Liaisons</span><span class="sxs-lookup"><span data-stu-id="e0d7e-211">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="e0d7e-212">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="e0d7e-212">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="e0d7e-213">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="e0d7e-213">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="e0d7e-214">\<binding></span><span class="sxs-lookup"><span data-stu-id="e0d7e-214">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
