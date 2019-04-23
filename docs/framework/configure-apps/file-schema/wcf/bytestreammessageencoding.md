---
title: <byteStreamMessageEncoding>
ms.date: 03/30/2017
ms.assetid: bbadd8dd-60a2-4007-b959-89373a8a7d60
ms.openlocfilehash: ce9f282ea1101befe3bf99762efa61e9b47b74cf
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59109900"
---
# <a name="bytestreammessageencoding"></a><span data-ttu-id="421df-101">\<byteStreamMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="421df-101">\<byteStreamMessageEncoding></span></span>
<span data-ttu-id="421df-102">Spécifie l'encodage de message sous forme de flux d'octets, avec l'option permettant de spécifier l'encodage de caractères.</span><span class="sxs-lookup"><span data-stu-id="421df-102">Specifies the message encoding as a stream of bytes, with the option to specify the character encoding.</span></span>  
  
 <span data-ttu-id="421df-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="421df-103">\<system.serviceModel></span></span>  
<span data-ttu-id="421df-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="421df-104">\<bindings></span></span>  
<span data-ttu-id="421df-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="421df-105">\<customBinding></span></span>  
<span data-ttu-id="421df-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="421df-106">\<binding></span></span>  
<span data-ttu-id="421df-107">\<binaryMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="421df-107">\<binaryMessageEncoding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="421df-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="421df-108">Syntax</span></span>  
  
```xml  
<byteStreamMessageEncoding />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="421df-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="421df-109">Attributes and Elements</span></span>  
 <span data-ttu-id="421df-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="421df-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="421df-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="421df-111">Attributes</span></span>  
  
|<span data-ttu-id="421df-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="421df-112">Attribute</span></span>|<span data-ttu-id="421df-113">Description</span><span class="sxs-lookup"><span data-stu-id="421df-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="421df-114">messageVersion</span><span class="sxs-lookup"><span data-stu-id="421df-114">messageVersion</span></span>|<span data-ttu-id="421df-115">Spécifie la version SOAP des messages envoyés à l'aide de la liaison.</span><span class="sxs-lookup"><span data-stu-id="421df-115">Specifies the SOAP version of the messages sent using the binding.</span></span> <span data-ttu-id="421df-116">Cette propriété ne peut être affectée que de la valeur de version de message <xref:System.ServiceModel.Channels.MessageVersion.None%2A>.</span><span class="sxs-lookup"><span data-stu-id="421df-116">This property can only be set to the message version value of <xref:System.ServiceModel.Channels.MessageVersion.None%2A>.</span></span> <span data-ttu-id="421df-117">L'encodeur de message en flux d'octets ne prend pas en charge d'autres versions de message.</span><span class="sxs-lookup"><span data-stu-id="421df-117">The byte stream message encoder does not support any other message versions.</span></span><br /><br /> <span data-ttu-id="421df-118">Cet attribut est de type <xref:System.ServiceModel.Channels.MessageVersion>.</span><span class="sxs-lookup"><span data-stu-id="421df-118">This attribute is of type <xref:System.ServiceModel.Channels.MessageVersion>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="421df-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="421df-119">Child Elements</span></span>  
  
|<span data-ttu-id="421df-120">Élément</span><span class="sxs-lookup"><span data-stu-id="421df-120">Element</span></span>|<span data-ttu-id="421df-121">Description</span><span class="sxs-lookup"><span data-stu-id="421df-121">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="421df-122">[\<readerQuotas>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="421df-122">[\<readerQuotas>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))</span></span>|<span data-ttu-id="421df-123">Définit les contraintes sur la complexité des messages SOAP pouvant être traités par les points de terminaison configurés avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="421df-123">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="421df-124">Cet élément est de type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span><span class="sxs-lookup"><span data-stu-id="421df-124">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="421df-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="421df-125">Parent Elements</span></span>  
  
|<span data-ttu-id="421df-126">Élément</span><span class="sxs-lookup"><span data-stu-id="421df-126">Element</span></span>|<span data-ttu-id="421df-127">Description</span><span class="sxs-lookup"><span data-stu-id="421df-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="421df-128">\<binding></span><span class="sxs-lookup"><span data-stu-id="421df-128">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="421df-129">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="421df-129">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="421df-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="421df-130">See also</span></span>

- <xref:System.ServiceModel.Configuration.ByteStreamMessageEncodingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>
- <xref:System.ServiceModel.Channels.ByteStreamMessageEncodingBindingElement>
- [<span data-ttu-id="421df-131">Encodage de message</span><span class="sxs-lookup"><span data-stu-id="421df-131">Message Encoding</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-encoding.md)
- [<span data-ttu-id="421df-132">Sélection d’un encodeur de message</span><span class="sxs-lookup"><span data-stu-id="421df-132">Choosing a Message Encoder</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-message-encoder.md)
- [<span data-ttu-id="421df-133">Liaisons</span><span class="sxs-lookup"><span data-stu-id="421df-133">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="421df-134">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="421df-134">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="421df-135">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="421df-135">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="421df-136">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="421df-136">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
