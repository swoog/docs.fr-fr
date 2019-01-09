---
title: '&lt;wsHttpBinding&gt;'
ms.date: 03/30/2017
helpviewer_keywords:
- wsHttpBinding Element
ms.assetid: 0eee8ced-ad68-427d-b95a-97260e98deed
ms.openlocfilehash: 05eb8d43e137c8dfc78dc3d7c0b145ce7a4e95ef
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150940"
---
# <a name="ltwshttpbindinggt"></a><span data-ttu-id="2a812-102">&lt;wsHttpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="2a812-102">&lt;wsHttpBinding&gt;</span></span>
<span data-ttu-id="2a812-103">Définit une liaison sécurisée, fiable, interopérable adaptée aux contrats de service non duplex.</span><span class="sxs-lookup"><span data-stu-id="2a812-103">Defines a secure, reliable, interoperable binding suitable for non-duplex service contracts.</span></span> <span data-ttu-id="2a812-104">La liaison implémente les spécifications suivantes : WS-Reliable Messaging pour la fiabilité et WS-Security pour l’authentification et de sécurité de message.</span><span class="sxs-lookup"><span data-stu-id="2a812-104">The binding implements the following specifications: WS-Reliable Messaging for reliability, and WS-Security for message security and authentication.</span></span> <span data-ttu-id="2a812-105">Le protocole de transport est HTTP et l'encodage de message est Text/XML.</span><span class="sxs-lookup"><span data-stu-id="2a812-105">The transport is HTTP, and message encoding is Text/XML encoding.</span></span>  
  
 <span data-ttu-id="2a812-106">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="2a812-106">\<system.ServiceModel></span></span>  
<span data-ttu-id="2a812-107">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="2a812-107">\<bindings></span></span>  
<span data-ttu-id="2a812-108">\<wsHttpBinding></span><span class="sxs-lookup"><span data-stu-id="2a812-108">\<wsHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a812-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a812-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2a812-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="2a812-110">Attributes and Elements</span></span>  
 <span data-ttu-id="2a812-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="2a812-111">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2a812-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="2a812-112">Attributes</span></span>  
  
|<span data-ttu-id="2a812-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="2a812-113">Attribute</span></span>|<span data-ttu-id="2a812-114">Description</span><span class="sxs-lookup"><span data-stu-id="2a812-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2a812-115">allowCookies</span><span class="sxs-lookup"><span data-stu-id="2a812-115">allowCookies</span></span>|<span data-ttu-id="2a812-116">Valeur booléenne qui indique si le client accepte les cookies et les propage dans de futures demandes.</span><span class="sxs-lookup"><span data-stu-id="2a812-116">A Boolean value that indicates whether the client accepts cookies and propagates them on future requests.</span></span> <span data-ttu-id="2a812-117">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="2a812-117">The default is false.</span></span><br /><br /> <span data-ttu-id="2a812-118">Vous pouvez utiliser cette propriété lorsque vous interagissez avec les services Web ASMX qui utilisent des cookies.</span><span class="sxs-lookup"><span data-stu-id="2a812-118">You can use this property when you interact with ASMX Web services that use cookies.</span></span> <span data-ttu-id="2a812-119">De cette manière, vous avez la certitude que les cookies retournés par le serveur sont automatiquement copiés dans toutes les futures demandes du client pour ce service.</span><span class="sxs-lookup"><span data-stu-id="2a812-119">In this way, you can be sure that the cookies returned from the server are automatically copied to all future client requests for that service.</span></span>|  
|<span data-ttu-id="2a812-120">bypassProxyOnLocal</span><span class="sxs-lookup"><span data-stu-id="2a812-120">bypassProxyOnLocal</span></span>|<span data-ttu-id="2a812-121">Valeur booléenne qui indique s'il faut ignorer le serveur proxy pour les adresses locales.</span><span class="sxs-lookup"><span data-stu-id="2a812-121">A Boolean value that indicates whether to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="2a812-122">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="2a812-122">The default is `false`.</span></span>|  
|<span data-ttu-id="2a812-123">closeTimeout</span><span class="sxs-lookup"><span data-stu-id="2a812-123">closeTimeout</span></span>|<span data-ttu-id="2a812-124"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de fermeture.</span><span class="sxs-lookup"><span data-stu-id="2a812-124">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="2a812-125">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="2a812-125">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="2a812-126">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="2a812-126">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="2a812-127">hostnameComparisonMode</span><span class="sxs-lookup"><span data-stu-id="2a812-127">hostnameComparisonMode</span></span>|<span data-ttu-id="2a812-128">Spécifie le mode de comparaison du nom d'hôte HTTP utilisé pour analyser des URI.</span><span class="sxs-lookup"><span data-stu-id="2a812-128">Specifies the HTTP hostname comparison mode used to parse URIs.</span></span> <span data-ttu-id="2a812-129">Cet attribut est de type <xref:System.ServiceModel.HostNameComparisonMode>, ce qui indique si le nom d'hôte est utilisé pour atteindre le service en cas de correspondance sur l'URI.</span><span class="sxs-lookup"><span data-stu-id="2a812-129">This attribute is of type <xref:System.ServiceModel.HostNameComparisonMode>, which indicates whether the hostname is used to reach the service when matching on the URI.</span></span> <span data-ttu-id="2a812-130">La valeur par défaut est <xref:System.ServiceModel.HostNameComparisonMode.StrongWildcard>, qui ignore le nom d'hôte dans la correspondance.</span><span class="sxs-lookup"><span data-stu-id="2a812-130">The default value is <xref:System.ServiceModel.HostNameComparisonMode.StrongWildcard>, which ignores the hostname in the match.</span></span>|  
|<span data-ttu-id="2a812-131">maxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="2a812-131">maxBufferPoolSize</span></span>|<span data-ttu-id="2a812-132">Entier qui spécifie la taille maximale du pool de mémoires tampons pour cette liaison.</span><span class="sxs-lookup"><span data-stu-id="2a812-132">An integer that specifies the maximum buffer pool size for this binding.</span></span> <span data-ttu-id="2a812-133">La valeur par défaut est 524 288 octets (512 x 1024).</span><span class="sxs-lookup"><span data-stu-id="2a812-133">The default is 524,288 bytes (512 \* 1024).</span></span> <span data-ttu-id="2a812-134">De nombreuses parties de Windows Communication Foundation (WCF) utilisent des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="2a812-134">Many parts of Windows Communication Foundation (WCF) use buffers.</span></span> <span data-ttu-id="2a812-135">La création et la destruction des mémoires tampons à chaque utilisation sont chères, tout comme leur nettoyage.</span><span class="sxs-lookup"><span data-stu-id="2a812-135">Creating and destroying buffers each time they are used is expensive, and garbage collection for buffers is also expensive.</span></span> <span data-ttu-id="2a812-136">Avec les pools de mémoires tampons, vous pouvez prendre une mémoire tampon du pool, l'utiliser et la retourner au pool une fois que vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="2a812-136">With buffer pools, you can take a buffer from the pool, use it, and return it to the pool once you are done.</span></span> <span data-ttu-id="2a812-137">Ainsi, la surcharge de la création et de la destruction des mémoires tampons est évitée.</span><span class="sxs-lookup"><span data-stu-id="2a812-137">Thus the overhead in creating and destroying buffers is avoided.</span></span>|  
|<span data-ttu-id="2a812-138">maxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="2a812-138">maxReceivedMessageSize</span></span>|<span data-ttu-id="2a812-139">Entier positif qui spécifie la taille maximale du message, en octets, y compris les en-têtes, pouvant être reçu sur un canal configuré avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="2a812-139">A positive integer that specifies the maximum message size, in bytes, including headers, that can be received on a channel configured with this binding.</span></span> <span data-ttu-id="2a812-140">L'expéditeur d'un message qui dépasse cette limite se verra notifier une erreur SOAP.</span><span class="sxs-lookup"><span data-stu-id="2a812-140">The sender of a message exceeding this limit will receive a SOAP fault.</span></span> <span data-ttu-id="2a812-141">Ce dernier abandonne le message et crée une entrée d'événement dans le journal de suivi.</span><span class="sxs-lookup"><span data-stu-id="2a812-141">The receiver drops the message and creates an entry of the event in the trace log.</span></span> <span data-ttu-id="2a812-142">La valeur par défaut est 65536.</span><span class="sxs-lookup"><span data-stu-id="2a812-142">The default is 65536.</span></span>|  
|<span data-ttu-id="2a812-143">messageEncoding</span><span class="sxs-lookup"><span data-stu-id="2a812-143">messageEncoding</span></span>|<span data-ttu-id="2a812-144">Définit l'encodeur utilisé pour encoder le message.</span><span class="sxs-lookup"><span data-stu-id="2a812-144">Defines the encoder used to encode the message.</span></span> <span data-ttu-id="2a812-145">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a812-145">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="2a812-146">-Texte : Utiliser un encodeur de message texte.</span><span class="sxs-lookup"><span data-stu-id="2a812-146">-   Text: Use a text message encoder.</span></span><br /><span data-ttu-id="2a812-147">-Mtom : Utiliser un encodeur Message Transmission Organization Mechanism 1.0 (MTOM).</span><span class="sxs-lookup"><span data-stu-id="2a812-147">-   Mtom: Use a Message Transmission Organization Mechanism 1.0 (MTOM) encoder.</span></span><br /><span data-ttu-id="2a812-148">-La valeur par défaut est texte.</span><span class="sxs-lookup"><span data-stu-id="2a812-148">-   The default is Text.</span></span><br /><br /> <span data-ttu-id="2a812-149">Cet attribut est de type <xref:System.ServiceModel.WSMessageEncoding>.</span><span class="sxs-lookup"><span data-stu-id="2a812-149">This attribute is of type <xref:System.ServiceModel.WSMessageEncoding>.</span></span>|  
|<span data-ttu-id="2a812-150">name</span><span class="sxs-lookup"><span data-stu-id="2a812-150">name</span></span>|<span data-ttu-id="2a812-151">Chaîne qui contient le nom de configuration de la liaison.</span><span class="sxs-lookup"><span data-stu-id="2a812-151">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="2a812-152">Cette valeur doit être unique car elle permet d'identifier la liaison.</span><span class="sxs-lookup"><span data-stu-id="2a812-152">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="2a812-153">Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d’avoir un nom.</span><span class="sxs-lookup"><span data-stu-id="2a812-153">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="2a812-154">Pour plus d’informations sur la configuration par défaut et les liaisons sans nom et les comportements, consultez [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="2a812-154">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|<span data-ttu-id="2a812-155">openTimeout</span><span class="sxs-lookup"><span data-stu-id="2a812-155">openTimeout</span></span>|<span data-ttu-id="2a812-156"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'ouverture.</span><span class="sxs-lookup"><span data-stu-id="2a812-156">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="2a812-157">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="2a812-157">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="2a812-158">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="2a812-158">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="2a812-159">proxyAddress</span><span class="sxs-lookup"><span data-stu-id="2a812-159">proxyAddress</span></span>|<span data-ttu-id="2a812-160">URI qui spécifie l'adresse du proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="2a812-160">A URI that specifies the address of the HTTP proxy.</span></span> <span data-ttu-id="2a812-161">Si `useSystemWebProxy` est `true`, ce paramètre doit avoir la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="2a812-161">If `useSystemWebProxy` is `true`, this setting must be `null`.</span></span> <span data-ttu-id="2a812-162">La valeur par défaut est `null`.</span><span class="sxs-lookup"><span data-stu-id="2a812-162">The default is `null`.</span></span>|  
|<span data-ttu-id="2a812-163">receiveTimeout</span><span class="sxs-lookup"><span data-stu-id="2a812-163">receiveTimeout</span></span>|<span data-ttu-id="2a812-164"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de réception.</span><span class="sxs-lookup"><span data-stu-id="2a812-164">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="2a812-165">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="2a812-165">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="2a812-166">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="2a812-166">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="2a812-167">sendTimeout</span><span class="sxs-lookup"><span data-stu-id="2a812-167">sendTimeout</span></span>|<span data-ttu-id="2a812-168"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'envoi.</span><span class="sxs-lookup"><span data-stu-id="2a812-168">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="2a812-169">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="2a812-169">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="2a812-170">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="2a812-170">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="2a812-171">textEncoding</span><span class="sxs-lookup"><span data-stu-id="2a812-171">textEncoding</span></span>|<span data-ttu-id="2a812-172">Spécifie l'encodage de jeu de caractères à utiliser pour l'émission de messages sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="2a812-172">Specifies the character set encoding to be used for emitting messages on the binding.</span></span> <span data-ttu-id="2a812-173">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a812-173">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="2a812-174">-UnicodeFffeTextEncoding : Codage Unicode BigEndian.</span><span class="sxs-lookup"><span data-stu-id="2a812-174">-   UnicodeFffeTextEncoding: Unicode BigEndian encoding.</span></span><br /><span data-ttu-id="2a812-175">-Utf16TextEncoding : encodage 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2a812-175">-   Utf16TextEncoding: 16-bit encoding.</span></span><br /><span data-ttu-id="2a812-176">-Utf8TextEncoding : encodage 8 bits.</span><span class="sxs-lookup"><span data-stu-id="2a812-176">-   Utf8TextEncoding: 8-bit encoding.</span></span><br /><br /> <span data-ttu-id="2a812-177">La valeur par défaut est Utf8TextEncoding.</span><span class="sxs-lookup"><span data-stu-id="2a812-177">The default is Utf8TextEncoding.</span></span><br /><br /> <span data-ttu-id="2a812-178">Cet attribut est de type <xref:System.Text.Encoding>.</span><span class="sxs-lookup"><span data-stu-id="2a812-178">This attribute is of type <xref:System.Text.Encoding>.</span></span>|  
|<span data-ttu-id="2a812-179">transactionFlow</span><span class="sxs-lookup"><span data-stu-id="2a812-179">transactionFlow</span></span>|<span data-ttu-id="2a812-180">Valeur booléenne qui spécifie si la liaison prend en charge le flux WS-Transactions.</span><span class="sxs-lookup"><span data-stu-id="2a812-180">A Boolean value that specifies whether the binding supports flowing WS-Transactions.</span></span> <span data-ttu-id="2a812-181">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="2a812-181">The default is `false`.</span></span>|  
|<span data-ttu-id="2a812-182">useDefaultWebProxy</span><span class="sxs-lookup"><span data-stu-id="2a812-182">useDefaultWebProxy</span></span>|<span data-ttu-id="2a812-183">Valeur booléenne qui spécifie si le proxy HTTP du système configuré automatiquement est utilisé.</span><span class="sxs-lookup"><span data-stu-id="2a812-183">A Boolean value that specifies whether the system’s auto-configured HTTP proxy is used.</span></span> <span data-ttu-id="2a812-184">La valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="2a812-184">The default is `true`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2a812-185">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2a812-185">Child Elements</span></span>  
  
|<span data-ttu-id="2a812-186">Élément</span><span class="sxs-lookup"><span data-stu-id="2a812-186">Element</span></span>|<span data-ttu-id="2a812-187">Description</span><span class="sxs-lookup"><span data-stu-id="2a812-187">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2a812-188">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="2a812-188">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-wshttpbinding.md)|<span data-ttu-id="2a812-189">Définit les paramètres de sécurité de la liaison.</span><span class="sxs-lookup"><span data-stu-id="2a812-189">Defines the security settings for the binding.</span></span> <span data-ttu-id="2a812-190">Cet élément est de type <xref:System.ServiceModel.Configuration.WSHttpSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="2a812-190">This element is of type <xref:System.ServiceModel.Configuration.WSHttpSecurityElement>.</span></span>|  
|[<span data-ttu-id="2a812-191">\<readerQuotas></span><span class="sxs-lookup"><span data-stu-id="2a812-191">\<readerQuotas></span></span>](https://msdn.microsoft.com/library/3e5e42ff-cef8-478f-bf14-034449239bfd)|<span data-ttu-id="2a812-192">Définit les contraintes sur la complexité des messages SOAP pouvant être traités par les points de terminaison configurés avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="2a812-192">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="2a812-193">Cet élément est de type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span><span class="sxs-lookup"><span data-stu-id="2a812-193">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
|[<span data-ttu-id="2a812-194">reliableSession</span><span class="sxs-lookup"><span data-stu-id="2a812-194">reliableSession</span></span>](https://msdn.microsoft.com/library/9c93818a-7dfa-43d5-b3a1-1aafccf3a00b)|<span data-ttu-id="2a812-195">Spécifie si des sessions fiables sont établies entre les points de terminaison du canal.</span><span class="sxs-lookup"><span data-stu-id="2a812-195">Specifies if reliable sessions are established between channel endpoints.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2a812-196">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2a812-196">Parent Elements</span></span>  
  
|<span data-ttu-id="2a812-197">Élément</span><span class="sxs-lookup"><span data-stu-id="2a812-197">Element</span></span>|<span data-ttu-id="2a812-198">Description</span><span class="sxs-lookup"><span data-stu-id="2a812-198">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2a812-199">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="2a812-199">\<bindings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|<span data-ttu-id="2a812-200">Cet élément conserve une collection de liaisons standard et personnalisées.</span><span class="sxs-lookup"><span data-stu-id="2a812-200">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2a812-201">Notes</span><span class="sxs-lookup"><span data-stu-id="2a812-201">Remarks</span></span>  
 <span data-ttu-id="2a812-202">`WSHttpBinding` est semblable à `BasicHttpBinding` mais fournit plus de fonctionnalités de service Web.</span><span class="sxs-lookup"><span data-stu-id="2a812-202">The `WSHttpBinding` is similar to the `BasicHttpBinding` but provides more Web service features.</span></span> <span data-ttu-id="2a812-203">Il utilise le transport HTTP et assure la sécurité des messages, comme BasicHttpBinding, mais il fournit également des transactions, une messagerie fiable et WS-Addressing, qu’il soit actif par défaut ou disponible par l’intermédiaire d’un paramètre de contrôle unique.</span><span class="sxs-lookup"><span data-stu-id="2a812-203">It uses the HTTP transport and provides message security, as does BasicHttpBinding, but it also provides transactions, reliable messaging, and WS-Addressing, either enabled by default or available through a single control setting.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2a812-204">Exemple</span><span class="sxs-lookup"><span data-stu-id="2a812-204">Example</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="2a812-205">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a812-205">See Also</span></span>  
 <xref:System.ServiceModel.WSHttpBinding>  
 <xref:System.ServiceModel.Configuration.WSHttpBindingElement>  
 [<span data-ttu-id="2a812-206">Liaisons</span><span class="sxs-lookup"><span data-stu-id="2a812-206">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="2a812-207">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="2a812-207">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="2a812-208">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="2a812-208">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="2a812-209">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="2a812-209">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
