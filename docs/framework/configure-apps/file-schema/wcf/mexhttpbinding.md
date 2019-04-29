---
title: <mexHttpBinding>
ms.date: 03/30/2017
ms.assetid: e50b2e1f-9668-41a5-8077-dee7abff9f0f
ms.openlocfilehash: 1aa9512c3d0d52f8cc3c7bd7b82bcfd37c418ce7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61773449"
---
# <a name="mexhttpbinding"></a><span data-ttu-id="43fd0-101">\<mexHttpBinding></span><span class="sxs-lookup"><span data-stu-id="43fd0-101">\<mexHttpBinding></span></span>
<span data-ttu-id="43fd0-102">Spécifie les paramètres pour une liaison utilisée dans le cadre de l’échange de messages WS-MetadataExchange (WS-MEX) sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="43fd0-102">Specifies the settings for a binding used for the WS-MetadataExchange (WS-MEX) message exchange over HTTP.</span></span>  
  
 <span data-ttu-id="43fd0-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="43fd0-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="43fd0-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="43fd0-104">\<bindings></span></span>  
<span data-ttu-id="43fd0-105">\<mexHttpBinding></span><span class="sxs-lookup"><span data-stu-id="43fd0-105">\<mexHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="43fd0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43fd0-106">Syntax</span></span>  
  
```xml  
<mexHttpBinding>
  <binding closeTimeout="TimeSpan"
           name="string"
           openTimeout="TimeSpan"
           receiveTimeout="TimeSpan"
           sendTimeout="TimeSpan">
  </binding>
</mexHttpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="43fd0-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="43fd0-107">Attributes and Elements</span></span>  
 <span data-ttu-id="43fd0-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="43fd0-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="43fd0-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="43fd0-109">Attributes</span></span>  
  
|<span data-ttu-id="43fd0-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="43fd0-110">Attribute</span></span>|<span data-ttu-id="43fd0-111">Description</span><span class="sxs-lookup"><span data-stu-id="43fd0-111">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="43fd0-112"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de fermeture.</span><span class="sxs-lookup"><span data-stu-id="43fd0-112">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="43fd0-113">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="43fd0-113">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="43fd0-114">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="43fd0-114">The default is 00:01:00.</span></span>|  
|`name`|<span data-ttu-id="43fd0-115">Chaîne qui contient le nom de configuration de la liaison.</span><span class="sxs-lookup"><span data-stu-id="43fd0-115">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="43fd0-116">Cette valeur doit être unique car elle permet d'identifier la liaison.</span><span class="sxs-lookup"><span data-stu-id="43fd0-116">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="43fd0-117">Chaque liaison porte un `name` et a un attribut `namespace` qui l’identifient de façon unique dans les métadonnées du service.</span><span class="sxs-lookup"><span data-stu-id="43fd0-117">Each binding has a `name` and `namespace` attribute that together uniquely identify it in the metadata of the service.</span></span> <span data-ttu-id="43fd0-118">De plus, ce nom est unique parmi les liaisons du même type.</span><span class="sxs-lookup"><span data-stu-id="43fd0-118">In addition, this name is unique among bindings of the same type.</span></span> <span data-ttu-id="43fd0-119">Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d’avoir un nom.</span><span class="sxs-lookup"><span data-stu-id="43fd0-119">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="43fd0-120">Pour plus d’informations sur la configuration par défaut et les liaisons sans nom et les comportements, consultez [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="43fd0-120">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|`openTimeout`|<span data-ttu-id="43fd0-121"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'ouverture.</span><span class="sxs-lookup"><span data-stu-id="43fd0-121">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="43fd0-122">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="43fd0-122">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="43fd0-123">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="43fd0-123">The default is 00:01:00.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="43fd0-124"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de réception.</span><span class="sxs-lookup"><span data-stu-id="43fd0-124">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="43fd0-125">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="43fd0-125">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="43fd0-126">La valeur par défaut est 00:10:00.</span><span class="sxs-lookup"><span data-stu-id="43fd0-126">The default is 00:10:00.</span></span>|  
|`sendTimeout`|<span data-ttu-id="43fd0-127"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'envoi.</span><span class="sxs-lookup"><span data-stu-id="43fd0-127">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="43fd0-128">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="43fd0-128">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="43fd0-129">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="43fd0-129">The default is 00:01:00.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="43fd0-130">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="43fd0-130">Child Elements</span></span>  
 <span data-ttu-id="43fd0-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="43fd0-131">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="43fd0-132">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="43fd0-132">Parent Elements</span></span>  
  
|<span data-ttu-id="43fd0-133">Élément</span><span class="sxs-lookup"><span data-stu-id="43fd0-133">Element</span></span>|<span data-ttu-id="43fd0-134">Description</span><span class="sxs-lookup"><span data-stu-id="43fd0-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="43fd0-135">\<bindings></span><span class="sxs-lookup"><span data-stu-id="43fd0-135">\<bindings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|<span data-ttu-id="43fd0-136">Cet élément conserve une collection de liaisons standard et personnalisées.</span><span class="sxs-lookup"><span data-stu-id="43fd0-136">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="43fd0-137">Notes</span><span class="sxs-lookup"><span data-stu-id="43fd0-137">Remarks</span></span>  
 <span data-ttu-id="43fd0-138">Cette liaison est essentiellement une liaison `WSHttpBinding` dont la sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="43fd0-138">This binding is essentially a `WSHttpBinding` binding with security disabled.</span></span> <span data-ttu-id="43fd0-139">Elle prend en charge la plupart des demandes de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="43fd0-139">It supports most metadata requests.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="43fd0-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43fd0-140">See also</span></span>

- <xref:System.ServiceModel.Description.MetadataExchangeBindings.CreateMexHttpBinding%2A>
- <xref:System.ServiceModel.Configuration.MexHttpBindingElement>
- [<span data-ttu-id="43fd0-141">Guide pratique pour Publier les métadonnées d’un Service à l’aide d’un fichier de Configuration</span><span class="sxs-lookup"><span data-stu-id="43fd0-141">How to: Publish Metadata for a Service Using a Configuration File</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [<span data-ttu-id="43fd0-142">Publication et récupération de métadonnées sur une liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="43fd0-142">Publishing and Retrieving Metadata Over a Custom Binding</span></span>](../../../../../docs/framework/wcf/extending/publishing-and-retrieving-metadata-over-a-custom-binding.md)
- [<span data-ttu-id="43fd0-143">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="43fd0-143">Metadata</span></span>](../../../../../docs/framework/wcf/feature-details/metadata.md)
- [<span data-ttu-id="43fd0-144">Liaisons</span><span class="sxs-lookup"><span data-stu-id="43fd0-144">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="43fd0-145">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="43fd0-145">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="43fd0-146">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="43fd0-146">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="43fd0-147">\<binding></span><span class="sxs-lookup"><span data-stu-id="43fd0-147">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
