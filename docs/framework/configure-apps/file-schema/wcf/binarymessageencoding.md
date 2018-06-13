---
title: '&lt;binaryMessageEncoding&gt;'
ms.date: 03/30/2017
ms.assetid: e4ae3cd4-6b67-4ce1-af4b-9400e0a38dba
ms.openlocfilehash: 298f211eca12d0e76821a2172d93d432dc830507
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32746265"
---
# <a name="ltbinarymessageencodinggt"></a><span data-ttu-id="6538e-102">&lt;binaryMessageEncoding&gt;</span><span class="sxs-lookup"><span data-stu-id="6538e-102">&lt;binaryMessageEncoding&gt;</span></span>
<span data-ttu-id="6538e-103">Définit un encodeur de message binaire qui encode des messages de Windows Communication Foundation (WCF) en binaire sur le câble.</span><span class="sxs-lookup"><span data-stu-id="6538e-103">Defines a binary message encoder that encodes Windows Communication Foundation (WCF) messages in binary on the wire.</span></span>  
  
 <span data-ttu-id="6538e-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="6538e-104">\<system.serviceModel></span></span>  
<span data-ttu-id="6538e-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="6538e-105">\<bindings></span></span>  
<span data-ttu-id="6538e-106">\<customBinding ></span><span class="sxs-lookup"><span data-stu-id="6538e-106">\<customBinding></span></span>  
<span data-ttu-id="6538e-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="6538e-107">\<binding></span></span>  
<span data-ttu-id="6538e-108">\<binaryMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="6538e-108">\<binaryMessageEncoding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6538e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6538e-109">Syntax</span></span>  
  
```xml  
<binaryMessageEncoding   
      maxReadPoolSize="Integer"  
   maxSessionSize="Integer"   
   maxWritePoolSize="Integer"   messageVersion="Soap11Addressing10/Soap12Addressing10" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6538e-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6538e-110">Attributes and Elements</span></span>  
 <span data-ttu-id="6538e-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6538e-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6538e-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="6538e-112">Attributes</span></span>  
  
|<span data-ttu-id="6538e-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="6538e-113">Attribute</span></span>|<span data-ttu-id="6538e-114">Description</span><span class="sxs-lookup"><span data-stu-id="6538e-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6538e-115">maxReadPoolSize</span><span class="sxs-lookup"><span data-stu-id="6538e-115">maxReadPoolSize</span></span>|<span data-ttu-id="6538e-116">Entier qui définit combien de messages peuvent être lus de manière simultanée sans allouer de nouveaux lecteurs.</span><span class="sxs-lookup"><span data-stu-id="6538e-116">An integer that defines how many messages can be read simultaneously without allocating new readers.</span></span> <span data-ttu-id="6538e-117">Des pools plus volumineux permettent au système d'être plus tolérant aux pics d'activité au prix d'une plage de travail plus volumineuse.</span><span class="sxs-lookup"><span data-stu-id="6538e-117">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="6538e-118">La valeur par défaut est 64.</span><span class="sxs-lookup"><span data-stu-id="6538e-118">The default is 64.</span></span>|  
|<span data-ttu-id="6538e-119">maxSessionSize</span><span class="sxs-lookup"><span data-stu-id="6538e-119">maxSessionSize</span></span>|<span data-ttu-id="6538e-120">Entier positif qui définit la taille, en octets, de la mémoire tampon utilisée pour l'encodage.</span><span class="sxs-lookup"><span data-stu-id="6538e-120">A positive integer that sets the size, in bytes, of the buffer used for encoding.</span></span> <span data-ttu-id="6538e-121">Une mémoire tampon plus importante augmente la vitesse d'encodage aux dépens de la taille de la plage de travail.</span><span class="sxs-lookup"><span data-stu-id="6538e-121">A larger buffer increases encoding speed at the expense of the size of the working set.</span></span> <span data-ttu-id="6538e-122">La valeur par défaut est 2048.</span><span class="sxs-lookup"><span data-stu-id="6538e-122">The default is 2048.</span></span>|  
|<span data-ttu-id="6538e-123">maxWritePoolSize</span><span class="sxs-lookup"><span data-stu-id="6538e-123">maxWritePoolSize</span></span>|<span data-ttu-id="6538e-124">Entier qui définit combien de messages peuvent être envoyés simultanément sans allouer de nouveaux enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="6538e-124">An integer that defines how many messages can be sent simultaneously without allocating new writers.</span></span> <span data-ttu-id="6538e-125">Des pools plus volumineux permettent au système d'être plus tolérant aux pics d'activité au prix d'une plage de travail plus volumineuse.</span><span class="sxs-lookup"><span data-stu-id="6538e-125">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="6538e-126">La valeur par défaut est 16.</span><span class="sxs-lookup"><span data-stu-id="6538e-126">The default is 16.</span></span>|  
|<span data-ttu-id="6538e-127">messageVersion</span><span class="sxs-lookup"><span data-stu-id="6538e-127">messageVersion</span></span>|<span data-ttu-id="6538e-128">Spécifie le message SOAP et les versions WS-Addressing qui sont utilisées ou attendues.</span><span class="sxs-lookup"><span data-stu-id="6538e-128">Specifies the SOAP message and WS-Addressing versions that are used or expected.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6538e-129">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6538e-129">Child Elements</span></span>  
  
|<span data-ttu-id="6538e-130">Élément</span><span class="sxs-lookup"><span data-stu-id="6538e-130">Element</span></span>|<span data-ttu-id="6538e-131">Description</span><span class="sxs-lookup"><span data-stu-id="6538e-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6538e-132">\<readerQuotas></span><span class="sxs-lookup"><span data-stu-id="6538e-132">\<readerQuotas></span></span>](http://msdn.microsoft.com/library/3e5e42ff-cef8-478f-bf14-034449239bfd)|<span data-ttu-id="6538e-133">Définit les contraintes sur la complexité des messages SOAP pouvant être traités par les points de terminaison configurés avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="6538e-133">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="6538e-134">Cet élément est de type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span><span class="sxs-lookup"><span data-stu-id="6538e-134">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6538e-135">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6538e-135">Parent Elements</span></span>  
  
|<span data-ttu-id="6538e-136">Élément</span><span class="sxs-lookup"><span data-stu-id="6538e-136">Element</span></span>|<span data-ttu-id="6538e-137">Description</span><span class="sxs-lookup"><span data-stu-id="6538e-137">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6538e-138">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="6538e-138">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="6538e-139">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="6538e-139">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6538e-140">Notes</span><span class="sxs-lookup"><span data-stu-id="6538e-140">Remarks</span></span>  
 <span data-ttu-id="6538e-141">L'encodage est le processus de transformation d'un message en une séquence d'octets.</span><span class="sxs-lookup"><span data-stu-id="6538e-141">Encoding is the process of transforming a message into a sequence of bytes.</span></span> <span data-ttu-id="6538e-142">Le décodage est le processus inverse.</span><span class="sxs-lookup"><span data-stu-id="6538e-142">Decoding is the reverse process.</span></span> <span data-ttu-id="6538e-143">Windows Communication Foundation (WCF) inclut trois types d'encodage des messages SOAP : Texte, Binaire et MTOM (Message Transmission Optimization Mechanism).</span><span class="sxs-lookup"><span data-stu-id="6538e-143">Windows Communication Foundation (WCF) includes three types of encoding for SOAP messages: Text, Binary and Message Transmission Optimization Mechanism (MTOM).</span></span>  
  
 <span data-ttu-id="6538e-144">L'élément `binaryMessageEncoding` spécifie le format binaire .NET pour le code XML et propose des options permettant de spécifier l'encodage de caractères et la version SOAP et WS-Addressing à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6538e-144">The `binaryMessageEncoding` element specifies the .NET Binary Format for XML and has options to specify the character encoding and the SOAP and WS-Addressing version to be used.</span></span> <span data-ttu-id="6538e-145">L'encodeur de message binaire encode des messages de Windows Communication Foundation (WCF) en binaire sur le câble.</span><span class="sxs-lookup"><span data-stu-id="6538e-145">The binary message encoder encodes Windows Communication Foundation (WCF) messages in binary on the wire.</span></span> <span data-ttu-id="6538e-146">Même si cet encodage permet une transmission très rapide des messages, l'interopérabilité basée sur les normes WS-\* est perdue.</span><span class="sxs-lookup"><span data-stu-id="6538e-146">While this encoding results in very fast transmission of messages, interoperability based on the WS-\* standards is lost.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6538e-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="6538e-147">Example</span></span>  
  
```xml  
<binaryMessageEncoding maxReadPoolSize="211"  
   maxWritePoolSize="2132"  
   maxSessionSize="3141" />  
```  
  
## <a name="see-also"></a><span data-ttu-id="6538e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6538e-148">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.BinaryMessageEncodingElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>  
 <xref:System.ServiceModel.Channels.BinaryMessageEncodingBindingElement>  
 [<span data-ttu-id="6538e-149">Encodage de message</span><span class="sxs-lookup"><span data-stu-id="6538e-149">Message Encoding</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-encoding.md)  
 [<span data-ttu-id="6538e-150">Sélection d’un encodeur de message</span><span class="sxs-lookup"><span data-stu-id="6538e-150">Choosing a Message Encoder</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-message-encoder.md)  
 [<span data-ttu-id="6538e-151">Liaisons</span><span class="sxs-lookup"><span data-stu-id="6538e-151">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="6538e-152">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="6538e-152">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="6538e-153">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="6538e-153">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="6538e-154">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="6538e-154">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
