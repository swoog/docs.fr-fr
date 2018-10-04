---
title: '&lt;comContract&gt;'
ms.date: 03/30/2017
ms.assetid: 3f8e1c0c-cfdf-4c79-ac65-c64e9323a51c
ms.openlocfilehash: e2addbada7f55076ae919d93c897991a7ec0fcd8
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48779203"
---
# <a name="ltcomcontractgt"></a><span data-ttu-id="5e9ad-102">&lt;comContract&gt;</span><span class="sxs-lookup"><span data-stu-id="5e9ad-102">&lt;comContract&gt;</span></span>
<span data-ttu-id="5e9ad-103">Spécifie un contrat de service d'intégration COM+.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-103">Specifies a COM+ integration service contract.</span></span>  
  
 <span data-ttu-id="5e9ad-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="5e9ad-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="5e9ad-105">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="5e9ad-105">\<comContracts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e9ad-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e9ad-106">Syntax</span></span>  
  
```xml  
<comContracts>  
  <comContract  
      contract="string"  
      namespace="string"  
      name="string"  
      requireSession="Boolean">  
      <exposedMethods>  
         <exposedMethod name="string" />  
      </exposedMethods>  
      <userDefinedTypes>  
         <userDefinedType name="string"  
            typeLibID="string"  
            typeLibVersion="string"  
            typeDefID="string">  
         </userDefinedType>  
      </userDefinedTypes>  
      <persistableTypes>  
         <persistableType id="string"  
            name="string">  
         </persistableType>  
      </persistableTypes>  
  </comContract>  
</comContracts>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5e9ad-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5e9ad-107">Attributes and Elements</span></span>  
 <span data-ttu-id="5e9ad-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5e9ad-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="5e9ad-109">Attributes</span></span>  
  
|<span data-ttu-id="5e9ad-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="5e9ad-110">Attribute</span></span>|<span data-ttu-id="5e9ad-111">Description</span><span class="sxs-lookup"><span data-stu-id="5e9ad-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5e9ad-112">contrat</span><span class="sxs-lookup"><span data-stu-id="5e9ad-112">contract</span></span>|<span data-ttu-id="5e9ad-113">Chaîne qui contient le type de contrat.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-113">A string that contains the contract type.</span></span>|  
|<span data-ttu-id="5e9ad-114">name</span><span class="sxs-lookup"><span data-stu-id="5e9ad-114">name</span></span>|<span data-ttu-id="5e9ad-115">Chaîne qui contient le type de nom.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-115">A string that contains the contract name.</span></span>|  
|<span data-ttu-id="5e9ad-116">namespace</span><span class="sxs-lookup"><span data-stu-id="5e9ad-116">namespace</span></span>|<span data-ttu-id="5e9ad-117">Chaîne qui contient l'espace de noms du contrat.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-117">A string that contains the contract namespace.</span></span>|  
|<span data-ttu-id="5e9ad-118">requiresSession</span><span class="sxs-lookup"><span data-stu-id="5e9ad-118">requiresSession</span></span>|<span data-ttu-id="5e9ad-119">Valeur booléenne qui spécifie si le contrat ne peut être utilisé que sur des liaisons de session.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-119">A Boolean value that specifies whether the contract can only be used on sessionful bindings.</span></span> <span data-ttu-id="5e9ad-120">Lorsque le service est initialisé, l'exécution d'intégration garantit que ce paramètre est cohérent avec le type de liaison à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-120">When the service is initialized, the integration runtime ensures that this setting is consistent with the type of binding to be used.</span></span> <span data-ttu-id="5e9ad-121">Une exception est générée en cas de conflit avec une ou plusieurs liaisons du contrat.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-121">An exception is generated if one or more of the bindings for the contract are in conflict.</span></span> <span data-ttu-id="5e9ad-122">Si cette propriété a la valeur `false`, qu'un canal unidirectionnel est utilisé et qu'un paramètre [out] est présent, une exception est également levée.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-122">If this property is `false`, and a one-way channel is in use and there are any [out] parameters, an exception is also generated.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5e9ad-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5e9ad-123">Child Elements</span></span>  
  
|<span data-ttu-id="5e9ad-124">Élément</span><span class="sxs-lookup"><span data-stu-id="5e9ad-124">Element</span></span>|<span data-ttu-id="5e9ad-125">Description</span><span class="sxs-lookup"><span data-stu-id="5e9ad-125">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="5e9ad-126">persistableTypes</span><span class="sxs-lookup"><span data-stu-id="5e9ad-126">persistableTypes</span></span>|<span data-ttu-id="5e9ad-127">Tous les types persistants.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-127">All the persistable types.</span></span>|  
|<span data-ttu-id="5e9ad-128">userDefinedTypes</span><span class="sxs-lookup"><span data-stu-id="5e9ad-128">userDefinedTypes</span></span>|<span data-ttu-id="5e9ad-129">Collection de types définis par l'utilisateur (UDT) à inclure dans le contrat de service.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-129">A collection of User Defined Types (UDT) that is to be included in the service contract.</span></span>|  
|<span data-ttu-id="5e9ad-130">exposedMethods</span><span class="sxs-lookup"><span data-stu-id="5e9ad-130">exposedMethods</span></span>|<span data-ttu-id="5e9ad-131">Collection de méthodes COM+ exposées lorsque l’interface sur un composant COM+ est exposée en tant que service Web.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-131">A collection of COM+ methods that are exposed when the interface on a COM+ component is exposed as a Web service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5e9ad-132">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5e9ad-132">Parent Elements</span></span>  
  
|<span data-ttu-id="5e9ad-133">Élément</span><span class="sxs-lookup"><span data-stu-id="5e9ad-133">Element</span></span>|<span data-ttu-id="5e9ad-134">Description</span><span class="sxs-lookup"><span data-stu-id="5e9ad-134">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="5e9ad-135">comContracts</span><span class="sxs-lookup"><span data-stu-id="5e9ad-135">comContracts</span></span>|<span data-ttu-id="5e9ad-136">Contient une collection d'éléments `comContract`.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-136">Contains a collection of `comContract` elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5e9ad-137">Notes</span><span class="sxs-lookup"><span data-stu-id="5e9ad-137">Remarks</span></span>  
 <span data-ttu-id="5e9ad-138">Contrats de service d’intégration COM + sont actuellement restreints à le `http://tempuri.org` espace de noms et nom de contrat est dérivé de l’interface COM de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-138">COM+ integration service contracts are currently restricted to the `http://tempuri.org` namespace, and contract name is derived from the supporting COM interface.</span></span> <span data-ttu-id="5e9ad-139">Toutefois, vous pouvez spécifier des alternatives à l'aide de la section `comContracts`, ainsi que l'élément `comContract` dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-139">You can, however, specify alternatives by using the `comContracts` section, as well as the `comContract` element in the configuration file.</span></span> <span data-ttu-id="5e9ad-140">Par exemple, vous pouvez utiliser la configuration suivante pour spécifier l'espace de noms, le nom de contrat et les types définis par l'utilisateur à inclure, ainsi que d'autres paramètres pour un contrat de service.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-140">For example, you can use the following configuration to specify the namespace, contract name, and user defined types to be included, as well as other settings for a service contract.</span></span>  
  
```xml  
<comContracts>  
  <comContract  
      contract="{5163B1E7-F0CF-4B6A-9A02-4AB654F34284}"  
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
  
 <span data-ttu-id="5e9ad-141">Lorsque le service est initialisé, les espaces de noms et les noms de contrat spécifiés sont appliqués aux descriptions de service générées.</span><span class="sxs-lookup"><span data-stu-id="5e9ad-141">When the service is initialized, the specified namespaces and contract names are applied to the generated service descriptions.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e9ad-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e9ad-142">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ComContractElementCollection>  
 <xref:System.ServiceModel.Configuration.ComContractElementCollection>  
 <xref:System.ServiceModel.Configuration.ComContractElement>  
 [<span data-ttu-id="5e9ad-143">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="5e9ad-143">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)  
 [<span data-ttu-id="5e9ad-144">Intégration à des applications COM+</span><span class="sxs-lookup"><span data-stu-id="5e9ad-144">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)  
 [<span data-ttu-id="5e9ad-145">Guide pratique pour configurer des paramètres de service COM+</span><span class="sxs-lookup"><span data-stu-id="5e9ad-145">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
