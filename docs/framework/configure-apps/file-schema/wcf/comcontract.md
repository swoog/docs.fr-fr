---
title: <comContract>
ms.date: 03/30/2017
ms.assetid: 3f8e1c0c-cfdf-4c79-ac65-c64e9323a51c
ms.openlocfilehash: 8694f83a731363f83cb09de43214eb4b211ef5ca
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59145065"
---
# <a name="comcontract"></a><span data-ttu-id="97e48-101">\<comContract></span><span class="sxs-lookup"><span data-stu-id="97e48-101">\<comContract></span></span>
<span data-ttu-id="97e48-102">Spécifie un contrat de service d'intégration COM+.</span><span class="sxs-lookup"><span data-stu-id="97e48-102">Specifies a COM+ integration service contract.</span></span>  
  
 <span data-ttu-id="97e48-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="97e48-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="97e48-104">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="97e48-104">\<comContracts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97e48-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97e48-105">Syntax</span></span>  
  
```xml  
<comContracts>
  <comContract contract="String"
               namespace="String"
               name="String"
               requireSession="Boolean">
    <exposedMethods>
      <exposedMethod name="String" />
    </exposedMethods>
    <userDefinedTypes>
      <userDefinedType name="String"
                       typeLibID="String"
                       typeLibVersion="String"
                       typeDefID="String">
      </userDefinedType>
    </userDefinedTypes>
    <persistableTypes>
      <persistableType id="String"
                       name="String">
      </persistableType>
    </persistableTypes>
  </comContract>
</comContracts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="97e48-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="97e48-106">Attributes and Elements</span></span>  
 <span data-ttu-id="97e48-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="97e48-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="97e48-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="97e48-108">Attributes</span></span>  
  
|<span data-ttu-id="97e48-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="97e48-109">Attribute</span></span>|<span data-ttu-id="97e48-110">Description</span><span class="sxs-lookup"><span data-stu-id="97e48-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="97e48-111">contrat</span><span class="sxs-lookup"><span data-stu-id="97e48-111">contract</span></span>|<span data-ttu-id="97e48-112">Chaîne qui contient le type de contrat.</span><span class="sxs-lookup"><span data-stu-id="97e48-112">A string that contains the contract type.</span></span>|  
|<span data-ttu-id="97e48-113">name</span><span class="sxs-lookup"><span data-stu-id="97e48-113">name</span></span>|<span data-ttu-id="97e48-114">Chaîne qui contient le type de nom.</span><span class="sxs-lookup"><span data-stu-id="97e48-114">A string that contains the contract name.</span></span>|  
|<span data-ttu-id="97e48-115">namespace</span><span class="sxs-lookup"><span data-stu-id="97e48-115">namespace</span></span>|<span data-ttu-id="97e48-116">Chaîne qui contient l'espace de noms du contrat.</span><span class="sxs-lookup"><span data-stu-id="97e48-116">A string that contains the contract namespace.</span></span>|  
|<span data-ttu-id="97e48-117">requiresSession</span><span class="sxs-lookup"><span data-stu-id="97e48-117">requiresSession</span></span>|<span data-ttu-id="97e48-118">Valeur booléenne qui spécifie si le contrat ne peut être utilisé que sur des liaisons de session.</span><span class="sxs-lookup"><span data-stu-id="97e48-118">A Boolean value that specifies whether the contract can only be used on sessionful bindings.</span></span> <span data-ttu-id="97e48-119">Lorsque le service est initialisé, l’exécution d’intégration garantit que ce paramètre est cohérent avec le type de liaison à utiliser.</span><span class="sxs-lookup"><span data-stu-id="97e48-119">When the service is initialized, the integration runtime ensures that this setting is consistent with the type of binding to be used.</span></span> <span data-ttu-id="97e48-120">Une exception est générée en cas de conflit avec une ou plusieurs liaisons du contrat.</span><span class="sxs-lookup"><span data-stu-id="97e48-120">An exception is generated if one or more of the bindings for the contract are in conflict.</span></span> <span data-ttu-id="97e48-121">Si cette propriété a la valeur `false`, qu'un canal unidirectionnel est utilisé et qu'un paramètre [out] est présent, une exception est également levée.</span><span class="sxs-lookup"><span data-stu-id="97e48-121">If this property is `false`, and a one-way channel is in use and there are any [out] parameters, an exception is also generated.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="97e48-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="97e48-122">Child Elements</span></span>  
  
|<span data-ttu-id="97e48-123">Élément</span><span class="sxs-lookup"><span data-stu-id="97e48-123">Element</span></span>|<span data-ttu-id="97e48-124">Description</span><span class="sxs-lookup"><span data-stu-id="97e48-124">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="97e48-125">persistableTypes</span><span class="sxs-lookup"><span data-stu-id="97e48-125">persistableTypes</span></span>|<span data-ttu-id="97e48-126">Tous les types persistants.</span><span class="sxs-lookup"><span data-stu-id="97e48-126">All the persistable types.</span></span>|  
|<span data-ttu-id="97e48-127">userDefinedTypes</span><span class="sxs-lookup"><span data-stu-id="97e48-127">userDefinedTypes</span></span>|<span data-ttu-id="97e48-128">Collection de types définis par l'utilisateur (UDT) à inclure dans le contrat de service.</span><span class="sxs-lookup"><span data-stu-id="97e48-128">A collection of User Defined Types (UDT) that is to be included in the service contract.</span></span>|  
|<span data-ttu-id="97e48-129">exposedMethods</span><span class="sxs-lookup"><span data-stu-id="97e48-129">exposedMethods</span></span>|<span data-ttu-id="97e48-130">Collection de méthodes COM+ exposées lorsque l’interface sur un composant COM+ est exposée en tant que service Web.</span><span class="sxs-lookup"><span data-stu-id="97e48-130">A collection of COM+ methods that are exposed when the interface on a COM+ component is exposed as a Web service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="97e48-131">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="97e48-131">Parent Elements</span></span>  
  
|<span data-ttu-id="97e48-132">Élément</span><span class="sxs-lookup"><span data-stu-id="97e48-132">Element</span></span>|<span data-ttu-id="97e48-133">Description</span><span class="sxs-lookup"><span data-stu-id="97e48-133">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="97e48-134">comContracts</span><span class="sxs-lookup"><span data-stu-id="97e48-134">comContracts</span></span>|<span data-ttu-id="97e48-135">Contient une collection d’éléments `comContract`.</span><span class="sxs-lookup"><span data-stu-id="97e48-135">Contains a collection of `comContract` elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="97e48-136">Notes</span><span class="sxs-lookup"><span data-stu-id="97e48-136">Remarks</span></span>  
 <span data-ttu-id="97e48-137">Contrats de service d’intégration COM + sont actuellement restreints à le `http://tempuri.org` espace de noms et nom de contrat est dérivé de l’interface COM de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="97e48-137">COM+ integration service contracts are currently restricted to the `http://tempuri.org` namespace, and contract name is derived from the supporting COM interface.</span></span> <span data-ttu-id="97e48-138">Toutefois, vous pouvez spécifier des alternatives à l'aide de la section `comContracts`, ainsi que l'élément `comContract` dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="97e48-138">You can, however, specify alternatives by using the `comContracts` section, as well as the `comContract` element in the configuration file.</span></span> <span data-ttu-id="97e48-139">Par exemple, vous pouvez utiliser la configuration suivante pour spécifier l'espace de noms, le nom de contrat et les types définis par l'utilisateur à inclure, ainsi que d'autres paramètres pour un contrat de service.</span><span class="sxs-lookup"><span data-stu-id="97e48-139">For example, you can use the following configuration to specify the namespace, contract name, and user defined types to be included, as well as other settings for a service contract.</span></span>  
  
```xml  
<comContracts>
  <comContract contract="{5163B1E7-F0CF-4B6A-9A02-4AB654F34284}"
               namespace="http://tempuri.org/5163B1E7-F0CF-4B6A-9A02-4AB654F34284"
               name="_Broker"
               requireSession="true">
    <exposedMethods>
      <exposedMethod name="BuyStock" />
      <exposedMethod name="SellStock" />
      <exposedMethod name="ExecuteTransaction" />
    </exposedMethods>
  </comContract>
</comContracts>
```  
  
 <span data-ttu-id="97e48-140">Lorsque le service est initialisé, les espaces de noms et les noms de contrat spécifiés sont appliqués aux descriptions de service générées.</span><span class="sxs-lookup"><span data-stu-id="97e48-140">When the service is initialized, the specified namespaces and contract names are applied to the generated service descriptions.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97e48-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97e48-141">See also</span></span>

- <xref:System.ServiceModel.Configuration.ComContractElementCollection>
- <xref:System.ServiceModel.Configuration.ComContractElementCollection>
- <xref:System.ServiceModel.Configuration.ComContractElement>
- [<span data-ttu-id="97e48-142">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="97e48-142">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)
- [<span data-ttu-id="97e48-143">Intégration à des applications COM+</span><span class="sxs-lookup"><span data-stu-id="97e48-143">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)
- [<span data-ttu-id="97e48-144">Guide pratique pour Configurer les paramètres de Service COM +</span><span class="sxs-lookup"><span data-stu-id="97e48-144">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
