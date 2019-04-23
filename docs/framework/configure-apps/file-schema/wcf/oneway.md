---
title: <oneWay>
ms.date: 03/30/2017
ms.assetid: 00e67e0e-77c0-4695-9138-c0997b0e5f3c
ms.openlocfilehash: bfda2b9d7b3aa5219a3e4c344347d3b10419a7bd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59102412"
---
# <a name="oneway"></a><span data-ttu-id="ad5f2-101">\<oneWay></span><span class="sxs-lookup"><span data-stu-id="ad5f2-101">\<oneWay></span></span>
<span data-ttu-id="ad5f2-102">Active le routage de paquets et l’utilisation de méthodes unidirectionnelles pour une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="ad5f2-102">Enables packet routing and the use of one-way methods for a custom binding.</span></span>  
  
 <span data-ttu-id="ad5f2-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="ad5f2-103">\<system.serviceModel></span></span>  
<span data-ttu-id="ad5f2-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="ad5f2-104">\<bindings></span></span>  
<span data-ttu-id="ad5f2-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="ad5f2-105">\<customBinding></span></span>  
<span data-ttu-id="ad5f2-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="ad5f2-106">\<binding></span></span>  
<span data-ttu-id="ad5f2-107">\<oneWay></span><span class="sxs-lookup"><span data-stu-id="ad5f2-107">\<oneWay></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad5f2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad5f2-108">Syntax</span></span>  
  
```xml  
<oneWay packetRoutable="Boolean">
  <channelPoolSettings idleTimeout="TimeSpan"
                       leaseTimeout="TimeSpan"
                       maxOutboundConnectionsPerEndpopint="Integer" />
</oneWay>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ad5f2-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ad5f2-109">Attributes and Elements</span></span>  
 <span data-ttu-id="ad5f2-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ad5f2-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ad5f2-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="ad5f2-111">Attributes</span></span>  
  
|<span data-ttu-id="ad5f2-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="ad5f2-112">Attribute</span></span>|<span data-ttu-id="ad5f2-113">Description</span><span class="sxs-lookup"><span data-stu-id="ad5f2-113">Description</span></span>|  
|---------------|-----------------|  
|`packetRoutable`|<span data-ttu-id="ad5f2-114">Valeur booléenne qui spécifie si le routage de paquets est activé.</span><span class="sxs-lookup"><span data-stu-id="ad5f2-114">A Boolean value that specifies whether packet routing is enabled.</span></span> <span data-ttu-id="ad5f2-115">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="ad5f2-115">The default is `false`.</span></span>|  
|`MaxAcceptedChannels`|<span data-ttu-id="ad5f2-116">Entier qui spécifie le nombre maximal de canaux qui peuvent être acceptés.</span><span class="sxs-lookup"><span data-stu-id="ad5f2-116">An integer that specifies the maximum number of channels that can be accepted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ad5f2-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ad5f2-117">Child Elements</span></span>  
  
|<span data-ttu-id="ad5f2-118">Élément</span><span class="sxs-lookup"><span data-stu-id="ad5f2-118">Element</span></span>|<span data-ttu-id="ad5f2-119">Description</span><span class="sxs-lookup"><span data-stu-id="ad5f2-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ad5f2-120">\<channelPoolSettings></span><span class="sxs-lookup"><span data-stu-id="ad5f2-120">\<channelPoolSettings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/channelpoolsettings.md)|<span data-ttu-id="ad5f2-121">Objet <xref:System.ServiceModel.Configuration.ChannelPoolSettingsElement> qui contient des propriétés du pool de canaux pour le canal actuel.</span><span class="sxs-lookup"><span data-stu-id="ad5f2-121">A <xref:System.ServiceModel.Configuration.ChannelPoolSettingsElement> object that contains properties of the channel pool for the current channel.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ad5f2-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ad5f2-122">Parent Elements</span></span>  
  
|<span data-ttu-id="ad5f2-123">Élément</span><span class="sxs-lookup"><span data-stu-id="ad5f2-123">Element</span></span>|<span data-ttu-id="ad5f2-124">Description</span><span class="sxs-lookup"><span data-stu-id="ad5f2-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ad5f2-125">\<binding></span><span class="sxs-lookup"><span data-stu-id="ad5f2-125">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="ad5f2-126">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="ad5f2-126">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ad5f2-127">Notes</span><span class="sxs-lookup"><span data-stu-id="ad5f2-127">Remarks</span></span>  
 <span data-ttu-id="ad5f2-128">Pour activer le routage de paquets, une couche de conversion unidirectionnelle est nécessaire (fournie par cet élément).</span><span class="sxs-lookup"><span data-stu-id="ad5f2-128">To enable packet routing, a one-way conversion layer is required, which this element provides.</span></span> <span data-ttu-id="ad5f2-129">Un utilisateur peut créer une liaison personnalisée qui crée une couche pour cette liaison via un transport prenant en charge la session ou de type demande/réponse pour qu'elle puisse router les paquets.</span><span class="sxs-lookup"><span data-stu-id="ad5f2-129">A user can create a custom binding that layers this binding over a session-aware or request-reply transport to make it packet routable.</span></span> <span data-ttu-id="ad5f2-130">Cet élément s'avère également utile lorsque vous souhaitez exposer des méthodes unidirectionnelles de façon plus native.</span><span class="sxs-lookup"><span data-stu-id="ad5f2-130">This element is also useful when you want to expose one-way methods in a more native fashion.</span></span> <span data-ttu-id="ad5f2-131">D'autres transformations peuvent être appliquées sur cette couche, comme le duplex composite et la messagerie fiable.</span><span class="sxs-lookup"><span data-stu-id="ad5f2-131">More transformations can be applied over this layer, such as Composite Duplex and Reliable Messaging.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad5f2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad5f2-132">See also</span></span>

- <xref:System.ServiceModel.Channels.OneWayBindingElement>
- <xref:System.ServiceModel.Configuration.OneWayElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="ad5f2-133">Liaisons</span><span class="sxs-lookup"><span data-stu-id="ad5f2-133">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="ad5f2-134">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="ad5f2-134">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="ad5f2-135">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="ad5f2-135">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="ad5f2-136">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="ad5f2-136">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
