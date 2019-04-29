---
title: <service>
ms.date: 03/30/2017
ms.assetid: 13123dd6-c4a9-4a04-a984-df184b851788
ms.openlocfilehash: 68bddc01b02d9885b3f0fc4c2cbc5c3249de03f4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61670394"
---
# <a name="service"></a><span data-ttu-id="6b8f2-101">\<service></span><span class="sxs-lookup"><span data-stu-id="6b8f2-101">\<service></span></span>
<span data-ttu-id="6b8f2-102">L'élément `service` contient les paramètres d'un service Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="6b8f2-102">The `service` element contains the settings for a Windows Communication Foundation (WCF) service.</span></span> <span data-ttu-id="6b8f2-103">Il contient également les points de terminaison qui exposent le service.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-103">It also contains endpoints that expose the service.</span></span>  
  
 <span data-ttu-id="6b8f2-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="6b8f2-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="6b8f2-105">\<services></span><span class="sxs-lookup"><span data-stu-id="6b8f2-105">\<services></span></span>  
<span data-ttu-id="6b8f2-106">\<service></span><span class="sxs-lookup"><span data-stu-id="6b8f2-106">\<service></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6b8f2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b8f2-107">Syntax</span></span>  
  
```xml  
<service behaviorConfiguration="String"
         name="String">
</service>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6b8f2-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6b8f2-108">Attributes and Elements</span></span>  
 <span data-ttu-id="6b8f2-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6b8f2-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="6b8f2-110">Attributes</span></span>  
  
|<span data-ttu-id="6b8f2-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="6b8f2-111">Attribute</span></span>|<span data-ttu-id="6b8f2-112">Description</span><span class="sxs-lookup"><span data-stu-id="6b8f2-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6b8f2-113">behaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b8f2-113">behaviorConfiguration</span></span>|<span data-ttu-id="6b8f2-114">Chaîne qui contient le nom du comportement à utiliser pour instancier le service.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-114">A string that contains the behavior name of the behavior to be used to instantiate the service.</span></span> <span data-ttu-id="6b8f2-115">Le nom du comportement doit être dans la portée, au niveau où le service est défini.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-115">The behavior name must be in scope at the point the service is defined.</span></span> <span data-ttu-id="6b8f2-116">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-116">The default value is an empty string.</span></span>|  
|<span data-ttu-id="6b8f2-117">name</span><span class="sxs-lookup"><span data-stu-id="6b8f2-117">name</span></span>|<span data-ttu-id="6b8f2-118">Attribut de chaîne requis indiquant le type de service à instancier.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-118">Required String attribute that specifies the type of the service to be instantiated.</span></span> <span data-ttu-id="6b8f2-119">Ce paramètre doit correspondre à un type valide.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-119">This setting must equate to a valid type.</span></span> <span data-ttu-id="6b8f2-120">Le format doit être `Namespace.Class.`</span><span class="sxs-lookup"><span data-stu-id="6b8f2-120">The format should be `Namespace.Class.`</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6b8f2-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6b8f2-121">Child Elements</span></span>  
  
|<span data-ttu-id="6b8f2-122">Élément</span><span class="sxs-lookup"><span data-stu-id="6b8f2-122">Element</span></span>|<span data-ttu-id="6b8f2-123">Description</span><span class="sxs-lookup"><span data-stu-id="6b8f2-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6b8f2-124">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="6b8f2-124">\<endpoint></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpoint-element.md)|<span data-ttu-id="6b8f2-125">Collection d’éléments `endpoint` qui exposent ce service.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-125">A collection of `endpoint` elements that expose this service.</span></span>|  
|[<span data-ttu-id="6b8f2-126">\<host></span><span class="sxs-lookup"><span data-stu-id="6b8f2-126">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="6b8f2-127">Spécifie l'hôte de cette instance de service.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-127">Specifies the host of this service instance.</span></span> <span data-ttu-id="6b8f2-128">Cet élément est de type <xref:System.ServiceModel.Configuration.HostElement>.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-128">This element is of type <xref:System.ServiceModel.Configuration.HostElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6b8f2-129">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6b8f2-129">Parent Elements</span></span>  
  
|<span data-ttu-id="6b8f2-130">Élément</span><span class="sxs-lookup"><span data-stu-id="6b8f2-130">Element</span></span>|<span data-ttu-id="6b8f2-131">Description</span><span class="sxs-lookup"><span data-stu-id="6b8f2-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6b8f2-132">\<services></span><span class="sxs-lookup"><span data-stu-id="6b8f2-132">\<services></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/services.md)|<span data-ttu-id="6b8f2-133">Élément racine de tous les éléments de configuration WCF.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-133">The root element of all WCF configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6b8f2-134">Notes</span><span class="sxs-lookup"><span data-stu-id="6b8f2-134">Remarks</span></span>  
 <span data-ttu-id="6b8f2-135">Les services sont définis dans la section `services` du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-135">Services are defined in the `services` section of the configuration file.</span></span> <span data-ttu-id="6b8f2-136">Un assembly peut contenir n'importe quel nombre de services.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-136">An assembly can contain any number of services.</span></span> <span data-ttu-id="6b8f2-137">Chacun dispose de sa propre section de configuration de `service`.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-137">Each service has its own `service` configuration section.</span></span> <span data-ttu-id="6b8f2-138">Cette section et son contenu définissent le contrat de service, le comportement et les points de terminaison de ce service en particulier.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-138">This section and its content define the service contract, behavior, and endpoints of the particular service.</span></span>  
  
 <span data-ttu-id="6b8f2-139">L'élément `behaviorConfiguration` est également facultatif.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-139">The `behaviorConfiguration` element is also optional.</span></span> <span data-ttu-id="6b8f2-140">Il identifie le comportement que le service adopte.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-140">It identifies the behavior the service uses.</span></span> <span data-ttu-id="6b8f2-141">Le comportement spécifié dans cet attribut doit créer une liaison avec un comportement dans la portée du même fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-141">The behavior specified in this attribute must link to a behavior in scope in the same configuration file.</span></span>  
  
 <span data-ttu-id="6b8f2-142">Chaque service expose un ou plusieurs points de terminaison, qui ont leurs propres adresse et liaison.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-142">Each service exposes one or more endpoints, which has its own address and binding.</span></span> <span data-ttu-id="6b8f2-143">Toutes les liaisons utilisées dans le fichier de configuration doivent être définies dans l'étendue du fichier.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-143">All bindings used within the configuration file must be defined in the scope of the file.</span></span> <span data-ttu-id="6b8f2-144">La liaison est liée aux points de terminaison grâce à la combinaison des attributs `name` et `bindingConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-144">Binding are linked to endpoints through the combination of the attributes `name` and `bindingConfiguration`.</span></span> <span data-ttu-id="6b8f2-145">L'attribut `name` décrit la section dans laquelle la liaison est définie.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-145">The `name` attribute describes the section the binding is defined in.</span></span> <span data-ttu-id="6b8f2-146">L'attribut `bindingConfiguration` définit quelle configuration de la section de liaison est utilisée.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-146">The `bindingConfiguration` attribute defines which configuration within the binding section is used.</span></span> <span data-ttu-id="6b8f2-147">Une section de liaison peut définir plusieurs configurations.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-147">A binding section can define several configurations.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6b8f2-148">Exemple</span><span class="sxs-lookup"><span data-stu-id="6b8f2-148">Example</span></span>  
 <span data-ttu-id="6b8f2-149">Il s'agit d'un exemple de configuration de service.</span><span class="sxs-lookup"><span data-stu-id="6b8f2-149">This is an example of a service configuration.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="6b8f2-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b8f2-150">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceElement>
- [<span data-ttu-id="6b8f2-151">Configuration des services</span><span class="sxs-lookup"><span data-stu-id="6b8f2-151">Configuring Services</span></span>](../../../../../docs/framework/wcf/configuring-services.md)
