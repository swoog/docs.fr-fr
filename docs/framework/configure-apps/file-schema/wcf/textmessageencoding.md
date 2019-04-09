---
title: <textMessageEncoding>
ms.date: 03/30/2017
ms.assetid: e6d834d0-356e-45eb-b530-bbefbb9ec3f0
ms.openlocfilehash: e9942ce3ccbec949160ee70dd103d3c1799bd44d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59186301"
---
# <a name="textmessageencoding"></a><span data-ttu-id="38d72-101">\<textMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="38d72-101">\<textMessageEncoding></span></span>
<span data-ttu-id="38d72-102">Spécifie l'encodage de caractères et le suivi des versions de message utilisés pour les messages XML textuels.</span><span class="sxs-lookup"><span data-stu-id="38d72-102">Specifies the character encoding and message versioning used for text-based XML messages.</span></span>  
  
 <span data-ttu-id="38d72-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="38d72-103">\<system.serviceModel></span></span>  
<span data-ttu-id="38d72-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="38d72-104">\<bindings></span></span>  
<span data-ttu-id="38d72-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="38d72-105">\<customBinding></span></span>  
<span data-ttu-id="38d72-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="38d72-106">\<binding></span></span>  
<span data-ttu-id="38d72-107">\<textMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="38d72-107">\<textMessageEncoding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38d72-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38d72-108">Syntax</span></span>  
  
```xml  
<textMessageEncoding maxReadPoolSize="Integer"
                     maxWritePoolSize="Integer"
                     messageVersion="Soap11Addressing10/Soap12Addressing10"
                     writeEncoding="UnicodeFffeTextEncoding/Utf16TextEncoding/Utf8TextEncoding" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="38d72-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="38d72-109">Attributes and Elements</span></span>  
 <span data-ttu-id="38d72-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="38d72-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="38d72-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="38d72-111">Attributes</span></span>  
  
|<span data-ttu-id="38d72-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="38d72-112">Attribute</span></span>|<span data-ttu-id="38d72-113">Description</span><span class="sxs-lookup"><span data-stu-id="38d72-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="38d72-114">maxReadPoolSize</span><span class="sxs-lookup"><span data-stu-id="38d72-114">maxReadPoolSize</span></span>|<span data-ttu-id="38d72-115">Entier qui spécifie combien de messages peuvent être lus de manière simultanée sans allouer de nouveaux lecteurs.</span><span class="sxs-lookup"><span data-stu-id="38d72-115">An integer that specifies how many messages can be read simultaneously without allocating new readers.</span></span> <span data-ttu-id="38d72-116">Des pools plus volumineux permettent au système d'être plus tolérant aux pics d'activité au prix d'une plage de travail plus volumineuse.</span><span class="sxs-lookup"><span data-stu-id="38d72-116">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="38d72-117">La valeur par défaut est 64.</span><span class="sxs-lookup"><span data-stu-id="38d72-117">The default is 64.</span></span>|  
|<span data-ttu-id="38d72-118">maxWritePoolSize</span><span class="sxs-lookup"><span data-stu-id="38d72-118">maxWritePoolSize</span></span>|<span data-ttu-id="38d72-119">Entier qui spécifie combien de messages peuvent être envoyés simultanément sans allouer de nouveaux enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="38d72-119">An integer that specifies how many messages can be sent simultaneously without allocating new writers.</span></span> <span data-ttu-id="38d72-120">Des pools plus volumineux permettent au système d'être plus tolérant aux pics d'activité au prix d'une plage de travail plus volumineuse.</span><span class="sxs-lookup"><span data-stu-id="38d72-120">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="38d72-121">La valeur par défaut est 16.</span><span class="sxs-lookup"><span data-stu-id="38d72-121">The default is 16.</span></span>|  
|<span data-ttu-id="38d72-122">messageVersion</span><span class="sxs-lookup"><span data-stu-id="38d72-122">messageVersion</span></span>|<span data-ttu-id="38d72-123">Spécifie la version SOAP des messages envoyés à l'aide de la liaison.</span><span class="sxs-lookup"><span data-stu-id="38d72-123">Specifies the SOAP version of the messages sent using the binding.</span></span> <span data-ttu-id="38d72-124">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="38d72-124">Valid values are</span></span><br /><br /> <span data-ttu-id="38d72-125">-   Soap11Addressing10</span><span class="sxs-lookup"><span data-stu-id="38d72-125">-   Soap11Addressing10</span></span><br /><span data-ttu-id="38d72-126">-Soap12Addressing10</span><span class="sxs-lookup"><span data-stu-id="38d72-126">-   Soap12Addressing10</span></span><br /><br /> <span data-ttu-id="38d72-127">La valeur par défaut est Soap12Addressing10.</span><span class="sxs-lookup"><span data-stu-id="38d72-127">The default is Soap12Addressing10.</span></span> <span data-ttu-id="38d72-128">Cet attribut est de type <xref:System.ServiceModel.Channels.MessageVersion>.</span><span class="sxs-lookup"><span data-stu-id="38d72-128">This attribute is of type <xref:System.ServiceModel.Channels.MessageVersion>.</span></span>|  
|<span data-ttu-id="38d72-129">writeEncoding</span><span class="sxs-lookup"><span data-stu-id="38d72-129">writeEncoding</span></span>|<span data-ttu-id="38d72-130">Spécifie l'encodage de jeu de caractères à utiliser pour l'émission de messages sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="38d72-130">Specifies the character set encoding to be used for emitting messages on the binding.</span></span> <span data-ttu-id="38d72-131">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="38d72-131">Valid values are</span></span><br /><br /> <span data-ttu-id="38d72-132">-   UnicodeFffeTextEncoding: Codage Unicode BigEndian</span><span class="sxs-lookup"><span data-stu-id="38d72-132">-   UnicodeFffeTextEncoding: Unicode BigEndian encoding</span></span><br /><span data-ttu-id="38d72-133">-   Utf16TextEncoding: Encodage Unicode</span><span class="sxs-lookup"><span data-stu-id="38d72-133">-   Utf16TextEncoding: Unicode encoding</span></span><br /><span data-ttu-id="38d72-134">-   Utf8TextEncoding: codage 8 bits</span><span class="sxs-lookup"><span data-stu-id="38d72-134">-   Utf8TextEncoding: 8-bit encoding</span></span><br /><br /> <span data-ttu-id="38d72-135">La valeur par défaut est Utf8TextEncoding.</span><span class="sxs-lookup"><span data-stu-id="38d72-135">The default is Utf8TextEncoding.</span></span> <span data-ttu-id="38d72-136">Cet attribut est de type <xref:System.Text.Encoding>.</span><span class="sxs-lookup"><span data-stu-id="38d72-136">This attribute is of type <xref:System.Text.Encoding>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="38d72-137">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="38d72-137">Child Elements</span></span>  
  
|<span data-ttu-id="38d72-138">Élément</span><span class="sxs-lookup"><span data-stu-id="38d72-138">Element</span></span>|<span data-ttu-id="38d72-139">Description</span><span class="sxs-lookup"><span data-stu-id="38d72-139">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="38d72-140">\<readerQuotas></span><span class="sxs-lookup"><span data-stu-id="38d72-140">\<readerQuotas></span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))|<span data-ttu-id="38d72-141">Définit les contraintes sur la complexité des messages SOAP pouvant être traités par les points de terminaison configurés avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="38d72-141">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="38d72-142">Cet élément est de type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span><span class="sxs-lookup"><span data-stu-id="38d72-142">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="38d72-143">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="38d72-143">Parent Elements</span></span>  
  
|<span data-ttu-id="38d72-144">Élément</span><span class="sxs-lookup"><span data-stu-id="38d72-144">Element</span></span>|<span data-ttu-id="38d72-145">Description</span><span class="sxs-lookup"><span data-stu-id="38d72-145">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="38d72-146">\<binding></span><span class="sxs-lookup"><span data-stu-id="38d72-146">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="38d72-147">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="38d72-147">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="38d72-148">Notes</span><span class="sxs-lookup"><span data-stu-id="38d72-148">Remarks</span></span>  
 <span data-ttu-id="38d72-149">L'encodage est le processus de transformation d'un message en une séquence d'octets.</span><span class="sxs-lookup"><span data-stu-id="38d72-149">Encoding is the process of transforming a message into a sequence of bytes.</span></span> <span data-ttu-id="38d72-150">Le décodage est le processus inverse.</span><span class="sxs-lookup"><span data-stu-id="38d72-150">Decoding is the reverse process.</span></span> <span data-ttu-id="38d72-151">Windows Communication Foundation (WCF) inclut trois types d’encodage des messages SOAP : Texte, binaire et Message Transmission Optimization Mechanism (MTOM).</span><span class="sxs-lookup"><span data-stu-id="38d72-151">Windows Communication Foundation (WCF) includes three types of encoding for SOAP messages: Text, Binary and Message Transmission Optimization Mechanism (MTOM).</span></span>  
  
 <span data-ttu-id="38d72-152">L'encodage de texte représenté par l'élément `textMessageEncoding` est l'encodeur le plus interopérable, mais le moins efficace pour les messages XML.</span><span class="sxs-lookup"><span data-stu-id="38d72-152">The text encoding represented by the `textMessageEncoding` element is the most interoperable, but the least efficient encoder for XML messages.</span></span>  <span data-ttu-id="38d72-153">L'encodeur de texte crée des messages textuels sur le câble.</span><span class="sxs-lookup"><span data-stu-id="38d72-153">The text encoder creates text-based messages on the wire.</span></span> <span data-ttu-id="38d72-154">Les messages produits par cet encodeur sont adaptés à l'interopérabilité basée sur WS-\*.</span><span class="sxs-lookup"><span data-stu-id="38d72-154">Messages produced by this encoder are suitable for WS-\* based interop.</span></span> <span data-ttu-id="38d72-155">Les services Web ou les clients de ces services comprennent généralement le XML textuel.</span><span class="sxs-lookup"><span data-stu-id="38d72-155">Web service or Web service client can generally understand textual XML.</span></span> <span data-ttu-id="38d72-156">Toutefois, la transmission de grands blocs de données binaires sous forme de texte est la méthode d'encodage de messages XML la moins efficace.</span><span class="sxs-lookup"><span data-stu-id="38d72-156">However, transmitting large blocks of binary data as text is the least efficient method for encoding XML messages.</span></span>  
  
## <a name="example"></a><span data-ttu-id="38d72-157">Exemple</span><span class="sxs-lookup"><span data-stu-id="38d72-157">Example</span></span>  
  
```xml  
<textMessageEncoding maxReadPoolSize="211"
                     maxWritePoolSize="2132"
                     messageVersion="Soap12Addressing10"
                     textEncoding="utf-8" />
```  
  
## <a name="see-also"></a><span data-ttu-id="38d72-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38d72-158">See also</span></span>

- <xref:System.ServiceModel.Configuration.TextMessageEncodingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>
- <xref:System.ServiceModel.Channels.TextMessageEncodingBindingElement>
- [<span data-ttu-id="38d72-159">Sélection d'un encodeur de message</span><span class="sxs-lookup"><span data-stu-id="38d72-159">Choosing a Message Encoder</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-message-encoder.md)
- [<span data-ttu-id="38d72-160">Encodage de message</span><span class="sxs-lookup"><span data-stu-id="38d72-160">Message Encoding</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-encoding.md)
- [<span data-ttu-id="38d72-161">Liaisons</span><span class="sxs-lookup"><span data-stu-id="38d72-161">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="38d72-162">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="38d72-162">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="38d72-163">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="38d72-163">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="38d72-164">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="38d72-164">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
