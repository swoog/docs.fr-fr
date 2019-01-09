---
title: '&lt;service&gt;'
ms.date: 03/30/2017
ms.assetid: 13123dd6-c4a9-4a04-a984-df184b851788
ms.openlocfilehash: ef0ae70440323c1ede5deca60e88f29861760e68
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145508"
---
# <a name="ltservicegt"></a><span data-ttu-id="33362-102">&lt;service&gt;</span><span class="sxs-lookup"><span data-stu-id="33362-102">&lt;service&gt;</span></span>
<span data-ttu-id="33362-103">L'élément `service` contient les paramètres d'un service Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="33362-103">The `service` element contains the settings for a Windows Communication Foundation (WCF) service.</span></span> <span data-ttu-id="33362-104">Il contient également les points de terminaison qui exposent le service.</span><span class="sxs-lookup"><span data-stu-id="33362-104">It also contains endpoints that expose the service.</span></span>  
  
 <span data-ttu-id="33362-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="33362-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="33362-106">\<services></span><span class="sxs-lookup"><span data-stu-id="33362-106">\<services></span></span>  
<span data-ttu-id="33362-107">\<service ></span><span class="sxs-lookup"><span data-stu-id="33362-107">\<service></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="33362-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33362-108">Syntax</span></span>  
  
```xml  
<service behaviorConfiguration="String"
         name="String">
</service>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="33362-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="33362-109">Attributes and Elements</span></span>  
 <span data-ttu-id="33362-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="33362-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="33362-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="33362-111">Attributes</span></span>  
  
|<span data-ttu-id="33362-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="33362-112">Attribute</span></span>|<span data-ttu-id="33362-113">Description</span><span class="sxs-lookup"><span data-stu-id="33362-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="33362-114">behaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="33362-114">behaviorConfiguration</span></span>|<span data-ttu-id="33362-115">Chaîne qui contient le nom du comportement à utiliser pour instancier le service.</span><span class="sxs-lookup"><span data-stu-id="33362-115">A string that contains the behavior name of the behavior to be used to instantiate the service.</span></span> <span data-ttu-id="33362-116">Le nom du comportement doit être dans la portée, au niveau où le service est défini.</span><span class="sxs-lookup"><span data-stu-id="33362-116">The behavior name must be in scope at the point the service is defined.</span></span> <span data-ttu-id="33362-117">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="33362-117">The default value is an empty string.</span></span>|  
|<span data-ttu-id="33362-118">name</span><span class="sxs-lookup"><span data-stu-id="33362-118">name</span></span>|<span data-ttu-id="33362-119">Attribut de chaîne requis indiquant le type de service à instancier.</span><span class="sxs-lookup"><span data-stu-id="33362-119">Required String attribute that specifies the type of the service to be instantiated.</span></span> <span data-ttu-id="33362-120">Ce paramètre doit correspondre à un type valide.</span><span class="sxs-lookup"><span data-stu-id="33362-120">This setting must equate to a valid type.</span></span> <span data-ttu-id="33362-121">Le format doit être `Namespace.Class.`</span><span class="sxs-lookup"><span data-stu-id="33362-121">The format should be `Namespace.Class.`</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="33362-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="33362-122">Child Elements</span></span>  
  
|<span data-ttu-id="33362-123">Élément</span><span class="sxs-lookup"><span data-stu-id="33362-123">Element</span></span>|<span data-ttu-id="33362-124">Description</span><span class="sxs-lookup"><span data-stu-id="33362-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="33362-125">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="33362-125">\<endpoint></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpoint-element.md)|<span data-ttu-id="33362-126">Collection d’éléments `endpoint` qui exposent ce service.</span><span class="sxs-lookup"><span data-stu-id="33362-126">A collection of `endpoint` elements that expose this service.</span></span>|  
|[<span data-ttu-id="33362-127">\<hôte ></span><span class="sxs-lookup"><span data-stu-id="33362-127">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="33362-128">Spécifie l'hôte de cette instance de service.</span><span class="sxs-lookup"><span data-stu-id="33362-128">Specifies the host of this service instance.</span></span> <span data-ttu-id="33362-129">Cet élément est de type <xref:System.ServiceModel.Configuration.HostElement>.</span><span class="sxs-lookup"><span data-stu-id="33362-129">This element is of type <xref:System.ServiceModel.Configuration.HostElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="33362-130">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="33362-130">Parent Elements</span></span>  
  
|<span data-ttu-id="33362-131">Élément</span><span class="sxs-lookup"><span data-stu-id="33362-131">Element</span></span>|<span data-ttu-id="33362-132">Description</span><span class="sxs-lookup"><span data-stu-id="33362-132">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="33362-133">\<services></span><span class="sxs-lookup"><span data-stu-id="33362-133">\<services></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/services.md)|<span data-ttu-id="33362-134">Élément racine de tous les éléments de configuration WCF.</span><span class="sxs-lookup"><span data-stu-id="33362-134">The root element of all WCF configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="33362-135">Notes</span><span class="sxs-lookup"><span data-stu-id="33362-135">Remarks</span></span>  
 <span data-ttu-id="33362-136">Les services sont définis dans la section `services` du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="33362-136">Services are defined in the `services` section of the configuration file.</span></span> <span data-ttu-id="33362-137">Un assembly peut contenir n'importe quel nombre de services.</span><span class="sxs-lookup"><span data-stu-id="33362-137">An assembly can contain any number of services.</span></span> <span data-ttu-id="33362-138">Chacun dispose de sa propre section de configuration de `service`.</span><span class="sxs-lookup"><span data-stu-id="33362-138">Each service has its own `service` configuration section.</span></span> <span data-ttu-id="33362-139">Cette section et son contenu définissent le contrat de service, le comportement et les points de terminaison de ce service en particulier.</span><span class="sxs-lookup"><span data-stu-id="33362-139">This section and its content define the service contract, behavior, and endpoints of the particular service.</span></span>  
  
 <span data-ttu-id="33362-140">L'élément `behaviorConfiguration` est également facultatif.</span><span class="sxs-lookup"><span data-stu-id="33362-140">The `behaviorConfiguration` element is also optional.</span></span> <span data-ttu-id="33362-141">Il identifie le comportement que le service adopte.</span><span class="sxs-lookup"><span data-stu-id="33362-141">It identifies the behavior the service uses.</span></span> <span data-ttu-id="33362-142">Le comportement spécifié dans cet attribut doit créer une liaison avec un comportement dans la portée du même fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="33362-142">The behavior specified in this attribute must link to a behavior in scope in the same configuration file.</span></span>  
  
 <span data-ttu-id="33362-143">Chaque service expose un ou plusieurs points de terminaison, qui ont leurs propres adresse et liaison.</span><span class="sxs-lookup"><span data-stu-id="33362-143">Each service exposes one or more endpoints, which has its own address and binding.</span></span> <span data-ttu-id="33362-144">Toutes les liaisons utilisées dans le fichier de configuration doivent être définies dans l'étendue du fichier.</span><span class="sxs-lookup"><span data-stu-id="33362-144">All bindings used within the configuration file must be defined in the scope of the file.</span></span> <span data-ttu-id="33362-145">La liaison est liée aux points de terminaison grâce à la combinaison des attributs `name` et `bindingConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="33362-145">Binding are linked to endpoints through the combination of the attributes `name` and `bindingConfiguration`.</span></span> <span data-ttu-id="33362-146">L'attribut `name` décrit la section dans laquelle la liaison est définie.</span><span class="sxs-lookup"><span data-stu-id="33362-146">The `name` attribute describes the section the binding is defined in.</span></span> <span data-ttu-id="33362-147">L'attribut `bindingConfiguration` définit quelle configuration de la section de liaison est utilisée.</span><span class="sxs-lookup"><span data-stu-id="33362-147">The `bindingConfiguration` attribute defines which configuration within the binding section is used.</span></span> <span data-ttu-id="33362-148">Une section de liaison peut définir plusieurs configurations.</span><span class="sxs-lookup"><span data-stu-id="33362-148">A binding section can define several configurations.</span></span>  
  
## <a name="example"></a><span data-ttu-id="33362-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="33362-149">Example</span></span>  
 <span data-ttu-id="33362-150">Il s'agit d'un exemple de configuration de service.</span><span class="sxs-lookup"><span data-stu-id="33362-150">This is an example of a service configuration.</span></span>  
  
```xml  
<service behaviorConfiguration="testChannelBehavior"
         name="HelloWorld">
  <endpoint address="/HelloWorld2/"
            name="test"
            bindingNamespace="http://www.cohowinery.com/"
            binding="basicHttpBinding"
            contract="IHelloWorld" />
</service>
```  
  
## <a name="see-also"></a><span data-ttu-id="33362-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33362-151">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceElement>  
 [<span data-ttu-id="33362-152">Configuration des services</span><span class="sxs-lookup"><span data-stu-id="33362-152">Configuring Services</span></span>](../../../../../docs/framework/wcf/configuring-services.md)
