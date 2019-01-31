---
title: <byteStreamMessageEncoding>
ms.date: 03/30/2017
ms.assetid: bbadd8dd-60a2-4007-b959-89373a8a7d60
ms.openlocfilehash: b1215f864822de7c2df181ff92858cb73700c0d7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55286267"
---
# <a name="bytestreammessageencoding"></a><span data-ttu-id="af733-101">\<byteStreamMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="af733-101">\<byteStreamMessageEncoding></span></span>
<span data-ttu-id="af733-102">Spécifie l'encodage de message sous forme de flux d'octets, avec l'option permettant de spécifier l'encodage de caractères.</span><span class="sxs-lookup"><span data-stu-id="af733-102">Specifies the message encoding as a stream of bytes, with the option to specify the character encoding.</span></span>  
  
 <span data-ttu-id="af733-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="af733-103">\<system.serviceModel></span></span>  
<span data-ttu-id="af733-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="af733-104">\<bindings></span></span>  
<span data-ttu-id="af733-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="af733-105">\<customBinding></span></span>  
<span data-ttu-id="af733-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="af733-106">\<binding></span></span>  
<span data-ttu-id="af733-107">\<binaryMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="af733-107">\<binaryMessageEncoding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="af733-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af733-108">Syntax</span></span>  
  
```xml  
<byteStreamMessageEncoding />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="af733-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="af733-109">Attributes and Elements</span></span>  
 <span data-ttu-id="af733-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="af733-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="af733-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="af733-111">Attributes</span></span>  
  
|<span data-ttu-id="af733-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="af733-112">Attribute</span></span>|<span data-ttu-id="af733-113">Description</span><span class="sxs-lookup"><span data-stu-id="af733-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="af733-114">messageVersion</span><span class="sxs-lookup"><span data-stu-id="af733-114">messageVersion</span></span>|<span data-ttu-id="af733-115">Spécifie la version SOAP des messages envoyés à l'aide de la liaison.</span><span class="sxs-lookup"><span data-stu-id="af733-115">Specifies the SOAP version of the messages sent using the binding.</span></span> <span data-ttu-id="af733-116">Cette propriété ne peut être affectée que de la valeur de version de message <xref:System.ServiceModel.Channels.MessageVersion.None%2A>.</span><span class="sxs-lookup"><span data-stu-id="af733-116">This property can only be set to the message version value of <xref:System.ServiceModel.Channels.MessageVersion.None%2A>.</span></span> <span data-ttu-id="af733-117">L'encodeur de message en flux d'octets ne prend pas en charge d'autres versions de message.</span><span class="sxs-lookup"><span data-stu-id="af733-117">The byte stream message encoder does not support any other message versions.</span></span><br /><br /> <span data-ttu-id="af733-118">Cet attribut est de type <xref:System.ServiceModel.Channels.MessageVersion>.</span><span class="sxs-lookup"><span data-stu-id="af733-118">This attribute is of type <xref:System.ServiceModel.Channels.MessageVersion>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="af733-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="af733-119">Child Elements</span></span>  
  
|<span data-ttu-id="af733-120">Élément</span><span class="sxs-lookup"><span data-stu-id="af733-120">Element</span></span>|<span data-ttu-id="af733-121">Description</span><span class="sxs-lookup"><span data-stu-id="af733-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="af733-122">\<readerQuotas></span><span class="sxs-lookup"><span data-stu-id="af733-122">\<readerQuotas></span></span>](https://msdn.microsoft.com/library/3e5e42ff-cef8-478f-bf14-034449239bfd)|<span data-ttu-id="af733-123">Définit les contraintes sur la complexité des messages SOAP pouvant être traités par les points de terminaison configurés avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="af733-123">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="af733-124">Cet élément est de type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span><span class="sxs-lookup"><span data-stu-id="af733-124">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="af733-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="af733-125">Parent Elements</span></span>  
  
|<span data-ttu-id="af733-126">Élément</span><span class="sxs-lookup"><span data-stu-id="af733-126">Element</span></span>|<span data-ttu-id="af733-127">Description</span><span class="sxs-lookup"><span data-stu-id="af733-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="af733-128">\<binding></span><span class="sxs-lookup"><span data-stu-id="af733-128">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="af733-129">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="af733-129">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="af733-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af733-130">See also</span></span>
- <xref:System.ServiceModel.Configuration.ByteStreamMessageEncodingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>
- <xref:System.ServiceModel.Channels.ByteStreamMessageEncodingBindingElement>
- [<span data-ttu-id="af733-131">Encodage de message</span><span class="sxs-lookup"><span data-stu-id="af733-131">Message Encoding</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-encoding.md)
- [<span data-ttu-id="af733-132">Sélection d’un encodeur de message</span><span class="sxs-lookup"><span data-stu-id="af733-132">Choosing a Message Encoder</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-message-encoder.md)
- [<span data-ttu-id="af733-133">Liaisons</span><span class="sxs-lookup"><span data-stu-id="af733-133">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="af733-134">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="af733-134">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="af733-135">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="af733-135">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="af733-136">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="af733-136">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
