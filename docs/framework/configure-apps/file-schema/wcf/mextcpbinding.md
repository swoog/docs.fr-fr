---
title: '&lt;mexTcpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 01baba8d-d784-4255-9ea2-7afff1482bf0
ms.openlocfilehash: a69f0af60d3f6723285ceb239a86775c9a1b510f
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147172"
---
# <a name="ltmextcpbindinggt"></a><span data-ttu-id="58a49-102">&lt;mexTcpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="58a49-102">&lt;mexTcpBinding&gt;</span></span>
<span data-ttu-id="58a49-103">Spécifie les paramètres pour une liaison utilisée dans le cadre de l’échange de messages WS-MetadataExchange (WS-MEX) sur TCP.</span><span class="sxs-lookup"><span data-stu-id="58a49-103">Specifies the settings for a binding used for the WS-MetadataExchange (WS-MEX) message exchange over TCP.</span></span>  
  
 <span data-ttu-id="58a49-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="58a49-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="58a49-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="58a49-105">\<bindings></span></span>  
<span data-ttu-id="58a49-106">\<mexTcpBinding></span><span class="sxs-lookup"><span data-stu-id="58a49-106">\<mexTcpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58a49-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58a49-107">Syntax</span></span>  
  
```xml  
<mexTcpBinding>
  <binding closeTimeout="TimeSpan"
           name="string"
           openTimeout="TimeSpan"
           receiveTimeout="TimeSpan"
           sendTimeout="TimeSpan">
  </binding>
</mexTcpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="58a49-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="58a49-108">Attributes and Elements</span></span>  
 <span data-ttu-id="58a49-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="58a49-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="58a49-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="58a49-110">Attributes</span></span>  
  
|<span data-ttu-id="58a49-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="58a49-111">Attribute</span></span>|<span data-ttu-id="58a49-112">Description</span><span class="sxs-lookup"><span data-stu-id="58a49-112">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="58a49-113"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de fermeture.</span><span class="sxs-lookup"><span data-stu-id="58a49-113">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="58a49-114">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="58a49-114">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="58a49-115">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="58a49-115">The default is 00:01:00.</span></span>|  
|`name`|<span data-ttu-id="58a49-116">Chaîne qui contient le nom de configuration de la liaison.</span><span class="sxs-lookup"><span data-stu-id="58a49-116">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="58a49-117">Cette valeur doit être unique car elle permet d'identifier la liaison.</span><span class="sxs-lookup"><span data-stu-id="58a49-117">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="58a49-118">Chaque liaison porte un `name` et a un attribut `namespace` qui l'identifient de façon unique dans les métadonnées du service.</span><span class="sxs-lookup"><span data-stu-id="58a49-118">Each binding has a `name` and `namespace` attribute that together uniquely identify it in the metadata of the service.</span></span> <span data-ttu-id="58a49-119">De plus, ce nom est unique parmi les liaisons du même type.</span><span class="sxs-lookup"><span data-stu-id="58a49-119">In addition, this name is unique among bindings of the same type.</span></span> <span data-ttu-id="58a49-120">Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d’avoir un nom.</span><span class="sxs-lookup"><span data-stu-id="58a49-120">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="58a49-121">Pour plus d’informations sur la configuration par défaut et les liaisons sans nom et les comportements, consultez [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="58a49-121">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|`openTimeout`|<span data-ttu-id="58a49-122"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'ouverture.</span><span class="sxs-lookup"><span data-stu-id="58a49-122">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="58a49-123">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="58a49-123">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="58a49-124">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="58a49-124">The default is 00:01:00.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="58a49-125"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de réception.</span><span class="sxs-lookup"><span data-stu-id="58a49-125">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="58a49-126">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="58a49-126">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="58a49-127">La valeur par défaut est 00:10:00.</span><span class="sxs-lookup"><span data-stu-id="58a49-127">The default is 00:10:00.</span></span>|  
|`sendTimeout`|<span data-ttu-id="58a49-128"><xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'envoi.</span><span class="sxs-lookup"><span data-stu-id="58a49-128">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="58a49-129">Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="58a49-129">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="58a49-130">La valeur par défaut est 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="58a49-130">The default is 00:01:00.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="58a49-131">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="58a49-131">Child Elements</span></span>  
 <span data-ttu-id="58a49-132">Aucun.</span><span class="sxs-lookup"><span data-stu-id="58a49-132">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="58a49-133">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="58a49-133">Parent Elements</span></span>  
  
|<span data-ttu-id="58a49-134">Élément</span><span class="sxs-lookup"><span data-stu-id="58a49-134">Element</span></span>|<span data-ttu-id="58a49-135">Description</span><span class="sxs-lookup"><span data-stu-id="58a49-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="58a49-136">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="58a49-136">\<bindings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|<span data-ttu-id="58a49-137">Cet élément conserve une collection de liaisons standard et personnalisées.</span><span class="sxs-lookup"><span data-stu-id="58a49-137">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="58a49-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58a49-138">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.MexTcpBindingElement>  
 <xref:System.ServiceModel.Description.MetadataExchangeBindings.CreateMexTcpBinding%2A>  
 [<span data-ttu-id="58a49-139">Guide pratique pour Publier les métadonnées d’un Service à l’aide d’un fichier de Configuration</span><span class="sxs-lookup"><span data-stu-id="58a49-139">How to: Publish Metadata for a Service Using a Configuration File</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)  
 [<span data-ttu-id="58a49-140">Publication et récupération de métadonnées sur une liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="58a49-140">Publishing and Retrieving Metadata Over a Custom Binding</span></span>](../../../../../docs/framework/wcf/extending/publishing-and-retrieving-metadata-over-a-custom-binding.md)  
 [<span data-ttu-id="58a49-141">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="58a49-141">Metadata</span></span>](../../../../../docs/framework/wcf/feature-details/metadata.md)  
 [<span data-ttu-id="58a49-142">Liaisons</span><span class="sxs-lookup"><span data-stu-id="58a49-142">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="58a49-143">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="58a49-143">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="58a49-144">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="58a49-144">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="58a49-145">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="58a49-145">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
