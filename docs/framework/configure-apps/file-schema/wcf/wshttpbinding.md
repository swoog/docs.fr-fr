---
title: <wsHttpBinding>
ms.date: 03/30/2017
helpviewer_keywords:
- wsHttpBinding Element
ms.assetid: 0eee8ced-ad68-427d-b95a-97260e98deed
ms.openlocfilehash: d22065abcb04209ebd1ad51b41bfc9167af6d4c9
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2019
ms.locfileid: "55758974"
---
# <a name="wshttpbinding"></a><span data-ttu-id="1a270-101">\<wsHttpBinding></span><span class="sxs-lookup"><span data-stu-id="1a270-101">\<wsHttpBinding></span></span>
<span data-ttu-id="1a270-102">Définit une liaison sécurisée, fiable, interopérable adaptée aux contrats de service non duplex.</span><span class="sxs-lookup"><span data-stu-id="1a270-102">Defines a secure, reliable, interoperable binding suitable for non-duplex service contracts.</span></span> <span data-ttu-id="1a270-103">La liaison implémente les spécifications suivantes : WS-Reliable Messaging pour la fiabilité et WS-Security pour l’authentification et de sécurité de message.</span><span class="sxs-lookup"><span data-stu-id="1a270-103">The binding implements the following specifications: WS-Reliable Messaging for reliability, and WS-Security for message security and authentication.</span></span> <span data-ttu-id="1a270-104">Le protocole de transport est HTTP et l'encodage de message est Text/XML.</span><span class="sxs-lookup"><span data-stu-id="1a270-104">The transport is HTTP, and message encoding is Text/XML encoding.</span></span>  
  
 <span data-ttu-id="1a270-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="1a270-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="1a270-106">\<bindings></span><span class="sxs-lookup"><span data-stu-id="1a270-106">\<bindings></span></span>  
<span data-ttu-id="1a270-107">\<wsHttpBinding></span><span class="sxs-lookup"><span data-stu-id="1a270-107">\<wsHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1a270-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a270-108">Syntax</span></span>  
  
```xml  
<wsHttpBinding>
  <binding allowCookies="Boolean"
           bypassProxyOnLocal="Boolean"
           closeTimeout="TimeSpan"
           hostNameComparisonMode="StrongWildCard/Exact/WeakWildcard"
           maxBufferPoolSize="integer"
           maxReceivedMessageSize="Integer"
           messageEncoding="Text/Mtom"
           name="string"
           openTimeout="TimeSpan"
           proxyAddress="URI"
           receiveTimeout="TimeSpan"
           sendTimeout="TimeSpan"
           textEncoding="UnicodeFffeTextEncoding/Utf16TextEncoding/Utf8TextEncoding"
           transactionFlow="Boolean"
           useDefaultWebProxy="Boolean">
    <reliableSession ordered="Boolean"
                     inactivityTimeout="TimeSpan"
                     enabled="Boolean" />
    <security mode="Message/None/Transport/TransportWithCredential">
      <transport clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"
                 proxyCredentialType="Basic/Digest/None/Ntlm/Windows"
                 realm="string" />
      <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               clientCredentialType="Certificate/IssuedToken/None/UserName/Windows"
               establishSecurityContext="Boolean"
               negotiateServiceCredential="Boolean" />
    </security>
    <readerQuotas maxArrayLength="Integer"
                  maxBytesPerRead="Integer"
                  maxDepth="Integer"
                  maxNameTableCharCount="Integer"
                  maxStringContentLength="Integer" />
  </binding>
</wsHttpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1a270-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1a270-109">Attributes and Elements</span></span>  
 <span data-ttu-id="1a270-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1a270-110">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1a270-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="1a270-111">Attributes</span></span>  
  
|<span data-ttu-id="1a270-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="1a270-112">Attribute</span></span>|<span data-ttu-id="1a270-113">Description</span><span class="sxs-lookup"><span data-stu-id="1a270-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="1a270-114">allowCookies</span><span class="sxs-lookup"><span data-stu-id="1a270-114">allowCookies</span></span>|<span data-ttu-id="1a270-115">Valeur booléenne qui indique si le client accepte les cookies et les propage dans de futures demandes.</span><span class="sxs-lookup"><span data-stu-id="1a270-115">A Boolean value that indicates whether the client accepts cookies and propagates them on future requests.</span></span> <span data-ttu-id="1a270-116">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="1a270-116">The default is false.</span></span><br /><br /> <span data-ttu-id="1a270-117">Vous pouvez utiliser cette propriété lorsque vous interagissez avec les services Web ASMX qui utilisent des cookies.</span><span class="sxs-lookup"><span data-stu-id="1a270-117">You can use this property when you interact with ASMX Web services that use cookies.</span></span> <span data-ttu-id="1a270-118">De cette manière, vous avez la certitude que les cookies retournés par le serveur sont automatiquement copiés dans toutes les futures demandes du client pour ce service.</span><span class="sxs-lookup"><span data-stu-id="1a270-118">In this way, you can be sure that the cookies returned from the server are automatically copied to all future client requests for that service.</span></span>|  
|<span data-ttu-id="1a270-119">bypassProxyOnLocal</span><span class="sxs-lookup"><span data-stu-id="1a270-119">bypassProxyOnLocal</span></span>|<span data-ttu-id="1a270-120">Valeur booléenne qui indique s'il faut ignorer le serveur proxy pour les adresses locales.</span><span class="sxs-lookup"><span data-stu-id="1a270-120">A Boolean value that indicates whether to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="1a270-121">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="1a270-121">The default is `false`.</span></span>|  
|<span data-ttu-id="1a270-122">closeTimeout</span><span class="sxs-lookup"><span data-stu-id="1a270-122">closeTimeout</span></span>|<span data-ttu-id="1a270-123"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de fermeture.</span><span class="sxs-lookup"><span data-stu-id="1a270-123">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="1a270-124">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="1a270-124">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="1a270-125">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="1a270-125">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="1a270-126">hostnameComparisonMode</span><span class="sxs-lookup"><span data-stu-id="1a270-126">hostnameComparisonMode</span></span>|<span data-ttu-id="1a270-127">Spécifie le mode de comparaison du nom d'hôte HTTP utilisé pour analyser des URI.</span><span class="sxs-lookup"><span data-stu-id="1a270-127">Specifies the HTTP hostname comparison mode used to parse URIs.</span></span> <span data-ttu-id="1a270-128">Cet attribut est de type <xref:System.ServiceModel.HostNameComparisonMode>, ce qui indique si le nom d'hôte est utilisé pour atteindre le service en cas de correspondance sur l'URI.</span><span class="sxs-lookup"><span data-stu-id="1a270-128">This attribute is of type <xref:System.ServiceModel.HostNameComparisonMode>, which indicates whether the hostname is used to reach the service when matching on the URI.</span></span> <span data-ttu-id="1a270-129">La valeur par défaut est <xref:System.ServiceModel.HostNameComparisonMode.StrongWildcard>, qui ignore le nom d'hôte dans la correspondance.</span><span class="sxs-lookup"><span data-stu-id="1a270-129">The default value is <xref:System.ServiceModel.HostNameComparisonMode.StrongWildcard>, which ignores the hostname in the match.</span></span>|  
|<span data-ttu-id="1a270-130">maxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="1a270-130">maxBufferPoolSize</span></span>|<span data-ttu-id="1a270-131">Entier qui spécifie la taille maximale du pool de mémoires tampons pour cette liaison.</span><span class="sxs-lookup"><span data-stu-id="1a270-131">An integer that specifies the maximum buffer pool size for this binding.</span></span> <span data-ttu-id="1a270-132">La valeur par défaut est 524 288 octets (512 x 1024).</span><span class="sxs-lookup"><span data-stu-id="1a270-132">The default is 524,288 bytes (512 \* 1024).</span></span> <span data-ttu-id="1a270-133">De nombreuses parties de Windows Communication Foundation (WCF) utilisent des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="1a270-133">Many parts of Windows Communication Foundation (WCF) use buffers.</span></span> <span data-ttu-id="1a270-134">La création et la destruction des mémoires tampons à chaque utilisation sont chères, tout comme leur nettoyage.</span><span class="sxs-lookup"><span data-stu-id="1a270-134">Creating and destroying buffers each time they are used is expensive, and garbage collection for buffers is also expensive.</span></span> <span data-ttu-id="1a270-135">Avec les pools de mémoires tampons, vous pouvez prendre une mémoire tampon du pool, l'utiliser et la retourner au pool une fois que vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="1a270-135">With buffer pools, you can take a buffer from the pool, use it, and return it to the pool once you are done.</span></span> <span data-ttu-id="1a270-136">Ainsi, la surcharge de la création et de la destruction des mémoires tampons est évitée.</span><span class="sxs-lookup"><span data-stu-id="1a270-136">Thus the overhead in creating and destroying buffers is avoided.</span></span>|  
|<span data-ttu-id="1a270-137">maxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="1a270-137">maxReceivedMessageSize</span></span>|<span data-ttu-id="1a270-138">Entier positif qui spécifie la taille maximale du message, en octets, y compris les en-têtes, pouvant être reçu sur un canal configuré avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="1a270-138">A positive integer that specifies the maximum message size, in bytes, including headers, that can be received on a channel configured with this binding.</span></span> <span data-ttu-id="1a270-139">L'expéditeur d'un message qui dépasse cette limite se verra notifier une erreur SOAP.</span><span class="sxs-lookup"><span data-stu-id="1a270-139">The sender of a message exceeding this limit will receive a SOAP fault.</span></span> <span data-ttu-id="1a270-140">Ce dernier abandonne le message et crée une entrée d'événement dans le journal de suivi.</span><span class="sxs-lookup"><span data-stu-id="1a270-140">The receiver drops the message and creates an entry of the event in the trace log.</span></span> <span data-ttu-id="1a270-141">La valeur par défaut est 65536.</span><span class="sxs-lookup"><span data-stu-id="1a270-141">The default is 65536.</span></span>|  
|<span data-ttu-id="1a270-142">messageEncoding</span><span class="sxs-lookup"><span data-stu-id="1a270-142">messageEncoding</span></span>|<span data-ttu-id="1a270-143">Définit l'encodeur utilisé pour encoder le message.</span><span class="sxs-lookup"><span data-stu-id="1a270-143">Defines the encoder used to encode the message.</span></span> <span data-ttu-id="1a270-144">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a270-144">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="1a270-145">-Texte : Utiliser un encodeur de message texte.</span><span class="sxs-lookup"><span data-stu-id="1a270-145">-   Text: Use a text message encoder.</span></span><br /><span data-ttu-id="1a270-146">-   Mtom: Utiliser un encodeur Message Transmission Organization Mechanism 1.0 (MTOM).</span><span class="sxs-lookup"><span data-stu-id="1a270-146">-   Mtom: Use a Message Transmission Organization Mechanism 1.0 (MTOM) encoder.</span></span><br /><span data-ttu-id="1a270-147">-La valeur par défaut est texte.</span><span class="sxs-lookup"><span data-stu-id="1a270-147">-   The default is Text.</span></span><br /><br /> <span data-ttu-id="1a270-148">Cet attribut est de type <xref:System.ServiceModel.WSMessageEncoding>.</span><span class="sxs-lookup"><span data-stu-id="1a270-148">This attribute is of type <xref:System.ServiceModel.WSMessageEncoding>.</span></span>|  
|<span data-ttu-id="1a270-149">name</span><span class="sxs-lookup"><span data-stu-id="1a270-149">name</span></span>|<span data-ttu-id="1a270-150">Chaîne qui contient le nom de configuration de la liaison.</span><span class="sxs-lookup"><span data-stu-id="1a270-150">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="1a270-151">Cette valeur doit être unique car elle permet d'identifier la liaison.</span><span class="sxs-lookup"><span data-stu-id="1a270-151">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="1a270-152">Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d’avoir un nom.</span><span class="sxs-lookup"><span data-stu-id="1a270-152">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="1a270-153">Pour plus d’informations sur la configuration par défaut et les liaisons sans nom et les comportements, consultez [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="1a270-153">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|<span data-ttu-id="1a270-154">openTimeout</span><span class="sxs-lookup"><span data-stu-id="1a270-154">openTimeout</span></span>|<span data-ttu-id="1a270-155"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'ouverture.</span><span class="sxs-lookup"><span data-stu-id="1a270-155">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="1a270-156">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="1a270-156">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="1a270-157">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="1a270-157">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="1a270-158">proxyAddress</span><span class="sxs-lookup"><span data-stu-id="1a270-158">proxyAddress</span></span>|<span data-ttu-id="1a270-159">URI qui spécifie l'adresse du proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="1a270-159">A URI that specifies the address of the HTTP proxy.</span></span> <span data-ttu-id="1a270-160">Si `useSystemWebProxy` est `true`, ce paramètre doit avoir la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="1a270-160">If `useSystemWebProxy` is `true`, this setting must be `null`.</span></span> <span data-ttu-id="1a270-161">La valeur par défaut est `null`.</span><span class="sxs-lookup"><span data-stu-id="1a270-161">The default is `null`.</span></span>|  
|<span data-ttu-id="1a270-162">receiveTimeout</span><span class="sxs-lookup"><span data-stu-id="1a270-162">receiveTimeout</span></span>|<span data-ttu-id="1a270-163"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de réception.</span><span class="sxs-lookup"><span data-stu-id="1a270-163">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="1a270-164">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="1a270-164">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="1a270-165">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="1a270-165">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="1a270-166">sendTimeout</span><span class="sxs-lookup"><span data-stu-id="1a270-166">sendTimeout</span></span>|<span data-ttu-id="1a270-167"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'envoi.</span><span class="sxs-lookup"><span data-stu-id="1a270-167">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="1a270-168">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="1a270-168">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="1a270-169">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="1a270-169">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="1a270-170">textEncoding</span><span class="sxs-lookup"><span data-stu-id="1a270-170">textEncoding</span></span>|<span data-ttu-id="1a270-171">Spécifie l'encodage de jeu de caractères à utiliser pour l'émission de messages sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="1a270-171">Specifies the character set encoding to be used for emitting messages on the binding.</span></span> <span data-ttu-id="1a270-172">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a270-172">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="1a270-173">-   UnicodeFffeTextEncoding: Codage Unicode BigEndian.</span><span class="sxs-lookup"><span data-stu-id="1a270-173">-   UnicodeFffeTextEncoding: Unicode BigEndian encoding.</span></span><br /><span data-ttu-id="1a270-174">-   Utf16TextEncoding: encodage 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1a270-174">-   Utf16TextEncoding: 16-bit encoding.</span></span><br /><span data-ttu-id="1a270-175">-   Utf8TextEncoding: encodage 8 bits.</span><span class="sxs-lookup"><span data-stu-id="1a270-175">-   Utf8TextEncoding: 8-bit encoding.</span></span><br /><br /> <span data-ttu-id="1a270-176">La valeur par défaut est Utf8TextEncoding.</span><span class="sxs-lookup"><span data-stu-id="1a270-176">The default is Utf8TextEncoding.</span></span><br /><br /> <span data-ttu-id="1a270-177">Cet attribut est de type <xref:System.Text.Encoding>.</span><span class="sxs-lookup"><span data-stu-id="1a270-177">This attribute is of type <xref:System.Text.Encoding>.</span></span>|  
|<span data-ttu-id="1a270-178">transactionFlow</span><span class="sxs-lookup"><span data-stu-id="1a270-178">transactionFlow</span></span>|<span data-ttu-id="1a270-179">Valeur booléenne qui spécifie si la liaison prend en charge le flux WS-Transactions.</span><span class="sxs-lookup"><span data-stu-id="1a270-179">A Boolean value that specifies whether the binding supports flowing WS-Transactions.</span></span> <span data-ttu-id="1a270-180">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="1a270-180">The default is `false`.</span></span>|  
|<span data-ttu-id="1a270-181">useDefaultWebProxy</span><span class="sxs-lookup"><span data-stu-id="1a270-181">useDefaultWebProxy</span></span>|<span data-ttu-id="1a270-182">Valeur booléenne qui spécifie si le proxy HTTP du système configuré automatiquement est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1a270-182">A Boolean value that specifies whether the system’s auto-configured HTTP proxy is used.</span></span> <span data-ttu-id="1a270-183">La valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="1a270-183">The default is `true`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1a270-184">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1a270-184">Child Elements</span></span>  
  
|<span data-ttu-id="1a270-185">Élément</span><span class="sxs-lookup"><span data-stu-id="1a270-185">Element</span></span>|<span data-ttu-id="1a270-186">Description</span><span class="sxs-lookup"><span data-stu-id="1a270-186">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1a270-187">\<security></span><span class="sxs-lookup"><span data-stu-id="1a270-187">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-wshttpbinding.md)|<span data-ttu-id="1a270-188">Définit les paramètres de sécurité de la liaison.</span><span class="sxs-lookup"><span data-stu-id="1a270-188">Defines the security settings for the binding.</span></span> <span data-ttu-id="1a270-189">Cet élément est de type <xref:System.ServiceModel.Configuration.WSHttpSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="1a270-189">This element is of type <xref:System.ServiceModel.Configuration.WSHttpSecurityElement>.</span></span>|  
|<span data-ttu-id="1a270-190">[\<readerQuotas>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1a270-190">[\<readerQuotas>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))</span></span>|<span data-ttu-id="1a270-191">Définit les contraintes sur la complexité des messages SOAP pouvant être traités par les points de terminaison configurés avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="1a270-191">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="1a270-192">Cet élément est de type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span><span class="sxs-lookup"><span data-stu-id="1a270-192">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
|<span data-ttu-id="1a270-193">[\<reliableSession>](https://docs.microsoft.com/previous-versions/ms731375(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="1a270-193">[\<reliableSession>](https://docs.microsoft.com/previous-versions/ms731375(v=vs.90))</span></span>|<span data-ttu-id="1a270-194">Spécifie si des sessions fiables sont établies entre les points de terminaison du canal.</span><span class="sxs-lookup"><span data-stu-id="1a270-194">Specifies if reliable sessions are established between channel endpoints.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1a270-195">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1a270-195">Parent Elements</span></span>  
  
|<span data-ttu-id="1a270-196">Élément</span><span class="sxs-lookup"><span data-stu-id="1a270-196">Element</span></span>|<span data-ttu-id="1a270-197">Description</span><span class="sxs-lookup"><span data-stu-id="1a270-197">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1a270-198">\<bindings></span><span class="sxs-lookup"><span data-stu-id="1a270-198">\<bindings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|<span data-ttu-id="1a270-199">Cet élément conserve une collection de liaisons standard et personnalisées.</span><span class="sxs-lookup"><span data-stu-id="1a270-199">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1a270-200">Notes</span><span class="sxs-lookup"><span data-stu-id="1a270-200">Remarks</span></span>  
 <span data-ttu-id="1a270-201">`WSHttpBinding` est semblable à `BasicHttpBinding` mais fournit plus de fonctionnalités de service Web.</span><span class="sxs-lookup"><span data-stu-id="1a270-201">The `WSHttpBinding` is similar to the `BasicHttpBinding` but provides more Web service features.</span></span> <span data-ttu-id="1a270-202">Il utilise le transport HTTP et assure la sécurité des messages, comme BasicHttpBinding, mais il fournit également des transactions, une messagerie fiable et WS-Addressing, qu’il soit actif par défaut ou disponible par l’intermédiaire d’un paramètre de contrôle unique.</span><span class="sxs-lookup"><span data-stu-id="1a270-202">It uses the HTTP transport and provides message security, as does BasicHttpBinding, but it also provides transactions, reliable messaging, and WS-Addressing, either enabled by default or available through a single control setting.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1a270-203">Exemple</span><span class="sxs-lookup"><span data-stu-id="1a270-203">Example</span></span>  
  
```xml  
<configuration>
  <system.ServiceModel>
    <bindings>
      <wsHttpBinding>
        <binding closeTimeout="00:00:10"
                 openTimeout="00:00:20"
                 receiveTimeout="00:00:30"
                 sendTimeout="00:00:40"
                 bypassProxyOnLocal="false"
                 transactionFlow="false"
                 hostNameComparisonMode="WeakWildcard"
                 maxReceivedMessageSize="1000"
                 messageEncoding="Mtom"
                 proxyAddress="http://foo/bar"
                 textEncoding="utf-16"
                 useDefaultWebProxy="false">
          <reliableSession ordered="false"
                           inactivityTimeout="00:02:00"
                           enabled="true" />
          <security mode="Transport">
            <transport clientCredentialType="Digest"
                       proxyCredentialType="None"
                       realm="someRealm" />
            <message clientCredentialType="Windows"
                     negotiateServiceCredential="false"
                     algorithmSuite="Aes128"
                     defaultProtectionLevel="None" />
          </security>
        </binding>
      </wsHttpBinding>
    </bindings>
  </system.ServiceModel>
</configuration>
```  
  
## <a name="see-also"></a><span data-ttu-id="1a270-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a270-204">See also</span></span>
- <xref:System.ServiceModel.WSHttpBinding>
- <xref:System.ServiceModel.Configuration.WSHttpBindingElement>
- [<span data-ttu-id="1a270-205">Liaisons</span><span class="sxs-lookup"><span data-stu-id="1a270-205">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="1a270-206">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="1a270-206">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="1a270-207">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="1a270-207">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="1a270-208">\<binding></span><span class="sxs-lookup"><span data-stu-id="1a270-208">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
