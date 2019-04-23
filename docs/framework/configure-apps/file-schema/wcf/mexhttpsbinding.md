---
title: <mexHttpsBinding>
ms.date: 03/30/2017
ms.assetid: f2ed3774-78b9-4a15-b79b-655f1ad68b86
ms.openlocfilehash: 4e96c28ac9b372092d06538d24d165dde6c5fe48
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59203130"
---
# <a name="mexhttpsbinding"></a><span data-ttu-id="4e7c2-101">\<mexHttpsBinding></span><span class="sxs-lookup"><span data-stu-id="4e7c2-101">\<mexHttpsBinding></span></span>
<span data-ttu-id="4e7c2-102">Spécifie les paramètres pour une liaison utilisée dans le cadre de l’échange de messages WS-MetadataExchange (WS-MEX) sur HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-102">Specifies the settings for a binding used for the WS-MetadataExchange (WS-MEX) message exchange over HTTPS.</span></span>  
  
 <span data-ttu-id="4e7c2-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="4e7c2-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="4e7c2-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="4e7c2-104">\<bindings></span></span>  
<span data-ttu-id="4e7c2-105">\<mexHttpsBinding></span><span class="sxs-lookup"><span data-stu-id="4e7c2-105">\<mexHttpsBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e7c2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e7c2-106">Syntax</span></span>  
  
```xml  
<mexHttpsBinding>
  <binding closeTimeout="TimeSpan"
            name="string"
            openTimeout="TimeSpan"
            receiveTimeout="TimeSpan"
            sendTimeout="TimeSpan">
  </binding>
</mexHttpsBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4e7c2-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4e7c2-107">Attributes and Elements</span></span>  
 <span data-ttu-id="4e7c2-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4e7c2-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="4e7c2-109">Attributes</span></span>  
  
|<span data-ttu-id="4e7c2-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="4e7c2-110">Attribute</span></span>|<span data-ttu-id="4e7c2-111">Description</span><span class="sxs-lookup"><span data-stu-id="4e7c2-111">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="4e7c2-112"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de fermeture.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-112">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="4e7c2-113">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-113">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="4e7c2-114">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-114">The default is 00:01:00.</span></span>|  
|`name`|<span data-ttu-id="4e7c2-115">Chaîne qui contient le nom de configuration de la liaison.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-115">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="4e7c2-116">Cette valeur doit être unique car elle permet d'identifier la liaison.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-116">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="4e7c2-117">Chaque liaison porte un `name` et a un attribut `namespace` qui l’identifient de façon unique dans les métadonnées du service.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-117">Each binding has a `name` and `namespace` attribute that together uniquely identify it in the metadata of the service.</span></span> <span data-ttu-id="4e7c2-118">De plus, ce nom est unique parmi les liaisons du même type.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-118">In addition, this name is unique among bindings of the same type.</span></span> <span data-ttu-id="4e7c2-119">Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d’avoir un nom.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-119">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="4e7c2-120">Pour plus d’informations sur la configuration par défaut et les liaisons sans nom et les comportements, consultez [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="4e7c2-120">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|`openTimeout`|<span data-ttu-id="4e7c2-121"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'ouverture.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-121">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="4e7c2-122">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-122">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="4e7c2-123">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-123">The default is 00:01:00.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="4e7c2-124"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de réception.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-124">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="4e7c2-125">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-125">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="4e7c2-126">La valeur par défaut est 00:10:00.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-126">The default is 00:10:00.</span></span>|  
|`sendTimeout`|<span data-ttu-id="4e7c2-127"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'envoi.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-127">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="4e7c2-128">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-128">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="4e7c2-129">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-129">The default is 00:01:00.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4e7c2-130">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4e7c2-130">Child Elements</span></span>  
 <span data-ttu-id="4e7c2-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-131">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4e7c2-132">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4e7c2-132">Parent Elements</span></span>  
  
|<span data-ttu-id="4e7c2-133">Élément</span><span class="sxs-lookup"><span data-stu-id="4e7c2-133">Element</span></span>|<span data-ttu-id="4e7c2-134">Description</span><span class="sxs-lookup"><span data-stu-id="4e7c2-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4e7c2-135">\<bindings></span><span class="sxs-lookup"><span data-stu-id="4e7c2-135">\<bindings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|<span data-ttu-id="4e7c2-136">Cet élément conserve une collection de liaisons standard et personnalisées.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-136">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4e7c2-137">Notes</span><span class="sxs-lookup"><span data-stu-id="4e7c2-137">Remarks</span></span>  
 <span data-ttu-id="4e7c2-138">Cette liaison est essentiellement une liaison `WSHttpBinding` qui prend en charge la sécurité au niveau du transport à l’aide de certificats.</span><span class="sxs-lookup"><span data-stu-id="4e7c2-138">This binding is essentially a `WSHttpBinding` binding that supports transport-level security using certificates.</span></span> <span data-ttu-id="4e7c2-139">Pour plus d’informations sur la configuration et à l’aide de tel un point de terminaison, consultez [Comment : Configurer un personnalisé WS-Metadata Exchange liaison](../../../../../docs/framework/wcf/extending/how-to-configure-a-custom-ws-metadata-exchange-binding.md), [Comment : Récupérer des métadonnées sur une liaison non - MEX](../../../../../docs/framework/wcf/extending/how-to-retrieve-metadata-over-a-non-mex-binding.md)et l’exemple [personnalisé sécuriser les métadonnées de point de terminaison](../../../../../docs/framework/wcf/samples/custom-secure-metadata-endpoint.md).</span><span class="sxs-lookup"><span data-stu-id="4e7c2-139">For more information about configuring and using such a metadata endpoint, see [How to: Configure a Custom WS-Metadata Exchange Binding](../../../../../docs/framework/wcf/extending/how-to-configure-a-custom-ws-metadata-exchange-binding.md), [How to: Retrieve Metadata Over a non-MEX Binding](../../../../../docs/framework/wcf/extending/how-to-retrieve-metadata-over-a-non-mex-binding.md), and the sample [Custom Secure Metadata Endpoint](../../../../../docs/framework/wcf/samples/custom-secure-metadata-endpoint.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4e7c2-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e7c2-140">See also</span></span>

- <xref:System.ServiceModel.Description.MetadataExchangeBindings.CreateMexHttpsBinding%2A>
- <xref:System.ServiceModel.Configuration.MexHttpsBindingElement>
- [<span data-ttu-id="4e7c2-141">Guide pratique pour Publier les métadonnées d’un Service à l’aide d’un fichier de Configuration</span><span class="sxs-lookup"><span data-stu-id="4e7c2-141">How to: Publish Metadata for a Service Using a Configuration File</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [<span data-ttu-id="4e7c2-142">Publication et récupération de métadonnées sur une liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="4e7c2-142">Publishing and Retrieving Metadata Over a Custom Binding</span></span>](../../../../../docs/framework/wcf/extending/publishing-and-retrieving-metadata-over-a-custom-binding.md)
- [<span data-ttu-id="4e7c2-143">Guide pratique pour Configurer un personnalisé WS-Metadata Exchange de liaison</span><span class="sxs-lookup"><span data-stu-id="4e7c2-143">How to: Configure a Custom WS-Metadata Exchange Binding</span></span>](../../../../../docs/framework/wcf/extending/how-to-configure-a-custom-ws-metadata-exchange-binding.md)
- [<span data-ttu-id="4e7c2-144">Guide pratique pour Récupérer des métadonnées sur une liaison non - MEX</span><span class="sxs-lookup"><span data-stu-id="4e7c2-144">How to: Retrieve Metadata Over a non-MEX Binding</span></span>](../../../../../docs/framework/wcf/extending/how-to-retrieve-metadata-over-a-non-mex-binding.md)
- [<span data-ttu-id="4e7c2-145">Point de terminaison de métadonnées sécurisé personnalisé</span><span class="sxs-lookup"><span data-stu-id="4e7c2-145">Custom Secure Metadata Endpoint</span></span>](../../../../../docs/framework/wcf/samples/custom-secure-metadata-endpoint.md)
- [<span data-ttu-id="4e7c2-146">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="4e7c2-146">Metadata</span></span>](../../../../../docs/framework/wcf/feature-details/metadata.md)
- [<span data-ttu-id="4e7c2-147">Liaisons</span><span class="sxs-lookup"><span data-stu-id="4e7c2-147">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="4e7c2-148">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="4e7c2-148">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="4e7c2-149">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="4e7c2-149">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="4e7c2-150">\<binding></span><span class="sxs-lookup"><span data-stu-id="4e7c2-150">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
