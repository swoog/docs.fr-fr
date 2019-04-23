---
title: <endpointDiscovery>
ms.date: 03/30/2017
ms.assetid: 70812717-888a-4748-9640-0df6715ff029
ms.openlocfilehash: 125baba917a49135aaa426df2cfa1a4dbe8ac1e8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59119494"
---
# <a name="endpointdiscovery"></a><span data-ttu-id="c479f-101">\<endpointDiscovery></span><span class="sxs-lookup"><span data-stu-id="c479f-101">\<endpointDiscovery></span></span>
<span data-ttu-id="c479f-102">Spécifie les différents paramètres de découverte d’un point de terminaison, tels que la fonctionnalité de découverte, les portées et toutes les extensions personnalisées de ses métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c479f-102">Specifies the various discovery settings for an endpoint, such as its discoverability, scopes, and any custom extensions to its metadata.</span></span>  
  
<span data-ttu-id="c479f-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="c479f-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="c479f-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="c479f-104">\<behaviors></span></span>  
<span data-ttu-id="c479f-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="c479f-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="c479f-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="c479f-106">\<behavior></span></span>  
<span data-ttu-id="c479f-107">\<endpointDiscovery></span><span class="sxs-lookup"><span data-stu-id="c479f-107">\<endpointDiscovery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c479f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c479f-108">Syntax</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="String">
      <endpointDiscovery enabled="Boolean">
        <scopes>
          <add scope="URI"/>
        </scopes>
        <extensions />
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c479f-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c479f-109">Attributes and Elements</span></span>  
 <span data-ttu-id="c479f-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c479f-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c479f-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="c479f-111">Attributes</span></span>  
  
|<span data-ttu-id="c479f-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="c479f-112">Attribute</span></span>|<span data-ttu-id="c479f-113">Description</span><span class="sxs-lookup"><span data-stu-id="c479f-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c479f-114">enabled</span><span class="sxs-lookup"><span data-stu-id="c479f-114">enabled</span></span>|<span data-ttu-id="c479f-115">Une valeur booléenne qui spécifie si la fonctionnalité de découverte est activée sur ce point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c479f-115">A Boolean value that specifies whether discoverability is enabled on this endpoint.</span></span> <span data-ttu-id="c479f-116">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="c479f-116">The default is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c479f-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c479f-117">Child Elements</span></span>  
  
|<span data-ttu-id="c479f-118">Élément</span><span class="sxs-lookup"><span data-stu-id="c479f-118">Element</span></span>|<span data-ttu-id="c479f-119">Description</span><span class="sxs-lookup"><span data-stu-id="c479f-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c479f-120">\<scopes></span><span class="sxs-lookup"><span data-stu-id="c479f-120">\<scopes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)|<span data-ttu-id="c479f-121">Collection d'URI de portée pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c479f-121">A collection of scope URIs for the endpoint.</span></span> <span data-ttu-id="c479f-122">Plusieurs URI de portée peuvent être associés au même point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c479f-122">More than one scope Uris can be associated with a single endpoint.</span></span>|  
|<span data-ttu-id="c479f-123">[\<extensions>](../../../../../docs/framework/configure-apps/file-schema/wcf/extensions.md) [of \<endpointDiscovery>]</span><span class="sxs-lookup"><span data-stu-id="c479f-123">[\<extensions>](../../../../../docs/framework/configure-apps/file-schema/wcf/extensions.md) [of \<endpointDiscovery>]</span></span>|<span data-ttu-id="c479f-124">Collection d'éléments XML qui vous permet de spécifier des métadonnées personnalisées à publier pour un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c479f-124">A collection of XML elements that allows you to specify custom metadata to be published for an endpoint.</span></span>|  
|<span data-ttu-id="c479f-125">\<types></span><span class="sxs-lookup"><span data-stu-id="c479f-125">\<types></span></span>|<span data-ttu-id="c479f-126">Collection d'interfaces à rechercher.</span><span class="sxs-lookup"><span data-stu-id="c479f-126">A collection of interfaces to search for.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c479f-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c479f-127">Parent Elements</span></span>  
  
|<span data-ttu-id="c479f-128">Élément</span><span class="sxs-lookup"><span data-stu-id="c479f-128">Element</span></span>|<span data-ttu-id="c479f-129">Description</span><span class="sxs-lookup"><span data-stu-id="c479f-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c479f-130">\<behavior></span><span class="sxs-lookup"><span data-stu-id="c479f-130">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="c479f-131">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="c479f-131">Specifies a behavior element.</span></span>|  
|||  
  
## <a name="remarks"></a><span data-ttu-id="c479f-132">Notes</span><span class="sxs-lookup"><span data-stu-id="c479f-132">Remarks</span></span>  
 <span data-ttu-id="c479f-133">Lorsqu'il est ajouté à la configuration de comportement du point de terminaison et si le jeu d'attributs `enabled` a la valeur `true`, cet élément de configuration devient détectable.</span><span class="sxs-lookup"><span data-stu-id="c479f-133">When added to the endpoint’s behavior configuration and with the `enabled` attribute set to `true`, this configuration element enables its discoverability.</span></span> <span data-ttu-id="c479f-134">En outre, vous pouvez utiliser la [ \<étendues >](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)élément enfant à la spécification URI qui peut être utilisé pour filtrer des points de terminaison de service pendant la requête, de portée personnalisés, ainsi que les [ \<extensions >](../../../../../docs/framework/configure-apps/file-schema/wcf/extensions.md) élément enfant à spécifier des métadonnées personnalisées qui doivent être publiées avec les métadonnées détectables standard (EPR, ContractTypeName, BindingName, étendue et ListenURI).</span><span class="sxs-lookup"><span data-stu-id="c479f-134">In addition, you can use the [\<scopes>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)child element to specifying custom scope Uris that can be used to filter service endpoints during query, as well as the [\<extensions>](../../../../../docs/framework/configure-apps/file-schema/wcf/extensions.md) child element to specify custom metadata that should be published along with the standard discoverable metadata (EPR, ContractTypeName, BindingName, Scope and ListenURI).</span></span>  
  
 <span data-ttu-id="c479f-135">Cet élément de configuration dépend de la [ \<serviceDiscovery >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md) élément qui fournit le contrôle au niveau du service de découverte.</span><span class="sxs-lookup"><span data-stu-id="c479f-135">This configuration element is dependent on the [\<serviceDiscovery>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md) element that provides the service level control of discoverability.</span></span> <span data-ttu-id="c479f-136">Cela signifie que les paramètres de cet élément sont ignorés si [ \<serviceDiscovery >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md) n’est pas présent dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="c479f-136">This means that this element’s settings are ignored if [\<serviceDiscovery>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md) is not present in the configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c479f-137">Exemple</span><span class="sxs-lookup"><span data-stu-id="c479f-137">Example</span></span>  
 <span data-ttu-id="c479f-138">L'exemple de configuration suivant spécifie des portées de filtrage et des métadonnées d'extension à publier pour un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c479f-138">The following configuration example specifies filtering scopes and extension metadata to be published for an endpoint.</span></span>  
  
```xml  
<services>
  <service name="CalculatorService"
           behaviorConfiguration="CalculatorServiceBehavior">
    <endpoint binding="basicHttpBinding"
              address="calculator"
              contract="ICalculatorService"
              behaviorConfiguration="calculatorEndpointBehavior" />
  </service>
</services>
<behaviors>
  <serviceBehaviors>
    <behavior name="CalculatorServiceBehavior">
      <serviceDiscovery />
    </behavior>
  </serviceBehaviors>
  <endpointBehaviors>
    <behavior name="calculatorEndpointBehavior">
      <endpointDiscovery enabled="true">
        <scopes>
          <add scope="http://contoso/test1" />
          <add scope="http://contoso/test2" />
        </scopes>
        <extensions>
          <e:Publisher xmlns:e="http://example.org">
            <e:Name>The Example Organization</e:Name>
            <e:Address>One Example Way, ExampleTown, EX 12345</e:Address>
            <e:Contact>support@example.org</e:Contact>
          </e:Publisher>
          <AnotherCustomMetadata>Custom Metadata</AnotherCustomMetadata>
        </extensions>
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="c479f-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c479f-139">See also</span></span>

- <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
