---
title: <endpoint> de <client>
ms.date: 03/30/2017
ms.assetid: de6238ae-bbf8-48e9-a1b5-e24c0bea8afa
ms.openlocfilehash: 3af41ad5b5681b08aac44d984372ab5ac66caf5e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59231199"
---
# <a name="endpoint-of-client"></a><span data-ttu-id="5fdc7-102">\<point de terminaison > de \<client ></span><span class="sxs-lookup"><span data-stu-id="5fdc7-102">\<endpoint> of \<client></span></span>
<span data-ttu-id="5fdc7-103">Spécifie les propriétés du contrat, de la liaison et de l’adresse du point de terminaison du canal employées par les clients pour se connecter aux points de terminaison de service sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-103">Specifies contract, binding, and address properties of the channel endpoint, which is used by clients to connect to service endpoints on the server.</span></span>  
  
 <span data-ttu-id="5fdc7-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="5fdc7-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="5fdc7-105">\<client></span><span class="sxs-lookup"><span data-stu-id="5fdc7-105">\<client></span></span>  
<span data-ttu-id="5fdc7-106">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="5fdc7-106">\<endpoint></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5fdc7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fdc7-107">Syntax</span></span>  
  
```xml  
<endpoint address="String"
          behaviorConfiguration="String"
          binding="String"
          bindingConfiguration="String"
          contract="String"
          endpointConfiguration="String"
          kind="String"
          name="String">
</endpoint>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5fdc7-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5fdc7-108">Attributes and Elements</span></span>  
 <span data-ttu-id="5fdc7-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5fdc7-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="5fdc7-110">Attributes</span></span>  
  
|<span data-ttu-id="5fdc7-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="5fdc7-111">Attribute</span></span>|<span data-ttu-id="5fdc7-112">Description</span><span class="sxs-lookup"><span data-stu-id="5fdc7-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5fdc7-113">adresse</span><span class="sxs-lookup"><span data-stu-id="5fdc7-113">address</span></span>|<span data-ttu-id="5fdc7-114">Attribut de chaîne requis.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-114">Required string attribute.</span></span><br /><br /> <span data-ttu-id="5fdc7-115">Spécifie l'adresse du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-115">Specifies the address of the endpoint.</span></span> <span data-ttu-id="5fdc7-116">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-116">The default is an empty string.</span></span> <span data-ttu-id="5fdc7-117">L'adresse doit être un URI absolu.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-117">The address must be an absolute URI.</span></span>|  
|<span data-ttu-id="5fdc7-118">behaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fdc7-118">behaviorConfiguration</span></span>|<span data-ttu-id="5fdc7-119">Chaîne qui contient le nom de comportement du comportement à utiliser pour instancier le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-119">A string that contains the behavior name of the behavior to be used to instantiate the endpoint.</span></span> <span data-ttu-id="5fdc7-120">Le nom du comportement doit être dans la portée, au niveau où le service est défini.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-120">The behavior name must be in scope at the point the service is defined.</span></span> <span data-ttu-id="5fdc7-121">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-121">The default is an empty string.</span></span>|  
|<span data-ttu-id="5fdc7-122">liaison</span><span class="sxs-lookup"><span data-stu-id="5fdc7-122">binding</span></span>|<span data-ttu-id="5fdc7-123">Attribut de chaîne requis.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-123">Required string attribute.</span></span><br /><br /> <span data-ttu-id="5fdc7-124">Chaîne qui indique le type de liaison à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-124">A string that indicates the type of binding to use.</span></span> <span data-ttu-id="5fdc7-125">Ce type doit posséder une section de configuration inscrite pour pouvoir être référencé.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-125">The type must have a registered configuration section in order to be referenced.</span></span> <span data-ttu-id="5fdc7-126">Il est inscrit en fonction du nom de la section et non en fonction du nom du type de la liaison.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-126">The type is registered by section name, instead of by the type name of the binding.</span></span>|  
|<span data-ttu-id="5fdc7-127">bindingConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fdc7-127">bindingConfiguration</span></span>|<span data-ttu-id="5fdc7-128">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-128">Optional.</span></span> <span data-ttu-id="5fdc7-129">Chaîne qui contient le nom de la configuration de liaison à utiliser lorsque le point de terminaison est instancié.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-129">A string that contains the name of the binding configuration to be used when the endpoint is instantiated.</span></span> <span data-ttu-id="5fdc7-130">La configuration de la liaison doit être dans la portée, au niveau où le point de terminaison est défini.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-130">The binding configuration must be in scope at the point the endpoint is defined.</span></span> <span data-ttu-id="5fdc7-131">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-131">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="5fdc7-132">Cet attribut est utilisé conjointement à `binding` pour référencer une configuration de liaison spécifique dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-132">This attribute is used in conjunction with `binding` to reference a specific binding configuration in the configuration file.</span></span> <span data-ttu-id="5fdc7-133">Définissez cet attribut si vous essayez d’utiliser une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-133">Set this attribute if you are attempting to use a custom binding.</span></span> <span data-ttu-id="5fdc7-134">Sinon, une exception peut être levée.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-134">Otherwise, an exception may be thrown.</span></span>|  
|<span data-ttu-id="5fdc7-135">contrat</span><span class="sxs-lookup"><span data-stu-id="5fdc7-135">contract</span></span>|<span data-ttu-id="5fdc7-136">Attribut de chaîne requis.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-136">Required string attribute.</span></span><br /><br /> <span data-ttu-id="5fdc7-137">Chaîne qui indique le contrat exposé par ce point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-137">A string that indicates which contract this endpoint is exposing.</span></span> <span data-ttu-id="5fdc7-138">L'assembly doit implémenter le type de contrat.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-138">The assembly must implement the contract type.</span></span>|  
|<span data-ttu-id="5fdc7-139">endpointConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fdc7-139">endpointConfiguration</span></span>|<span data-ttu-id="5fdc7-140">Chaîne qui spécifie le nom du point de terminaison standard défini par l'attribut `kind`, qui fait référence aux informations de configuration supplémentaires de ce point de terminaison standard.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-140">A string that specifies the name of the standard endpoint that is set by the `kind` attribute, which references to the additional configuration information of this standard endpoint.</span></span> <span data-ttu-id="5fdc7-141">Le même nom doit être défini dans la section `<standardEndpoints>`.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-141">The same name must be defined in the `<standardEndpoints>` section.</span></span>|  
|<span data-ttu-id="5fdc7-142">kind</span><span class="sxs-lookup"><span data-stu-id="5fdc7-142">kind</span></span>|<span data-ttu-id="5fdc7-143">Chaîne qui spécifie le type de point de terminaison standard appliqué.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-143">A string that specifies the type of standard endpoint applied.</span></span> <span data-ttu-id="5fdc7-144">Le type doit être inscrit dans la section `<extensions>` ou dans machine.config. Si rien n'est spécifié, un point de terminaison de canal commun est créé.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-144">The type must be registered in the `<extensions>` section or in machine.config. If nothing is specified, a common channel endpoint is created.</span></span>|  
|<span data-ttu-id="5fdc7-145">name</span><span class="sxs-lookup"><span data-stu-id="5fdc7-145">name</span></span>|<span data-ttu-id="5fdc7-146">Attribut de chaîne facultatif.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-146">Optional string attribute.</span></span> <span data-ttu-id="5fdc7-147">Cet attribut identifie uniquement un point de terminaison pour un contrat donné.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-147">This attribute uniquely identifies an endpoint for a given contract.</span></span> <span data-ttu-id="5fdc7-148">Vous pouvez définir plusieurs clients pour un type de contrat donné.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-148">You can define multiple clients for a given Contract type.</span></span> <span data-ttu-id="5fdc7-149">Chaque définition doit être différenciée par un nom de configuration unique.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-149">Each definition must be differentiated by a unique configuration name.</span></span> <span data-ttu-id="5fdc7-150">Si cet attribut est omis, le point de terminaison correspondant est utilisé comme point de terminaison par défaut associé au type de contrat spécifié.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-150">If this attribute is omitted, the corresponding endpoint is used as the default endpoint associated with the specified Contract type.</span></span> <span data-ttu-id="5fdc7-151">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-151">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="5fdc7-152">L'attribut `name` d'une liaison est utilisé pour l'exportation de définition à travers WSDL.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-152">The `name` attribute of a binding is used for definition export through WSDL.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5fdc7-153">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5fdc7-153">Child Elements</span></span>  
  
|<span data-ttu-id="5fdc7-154">Élément</span><span class="sxs-lookup"><span data-stu-id="5fdc7-154">Element</span></span>|<span data-ttu-id="5fdc7-155">Description</span><span class="sxs-lookup"><span data-stu-id="5fdc7-155">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5fdc7-156">\<headers></span><span class="sxs-lookup"><span data-stu-id="5fdc7-156">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers.md)|<span data-ttu-id="5fdc7-157">Collection d'en-têtes d'adresses.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-157">A collection of address headers.</span></span>|  
|[<span data-ttu-id="5fdc7-158">\<identity></span><span class="sxs-lookup"><span data-stu-id="5fdc7-158">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="5fdc7-159">Identité qui permet l'authentification d'un point de terminaison par les autres points de terminaison qui échangent des messages avec lui.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-159">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5fdc7-160">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5fdc7-160">Parent Elements</span></span>  
  
|<span data-ttu-id="5fdc7-161">Élément</span><span class="sxs-lookup"><span data-stu-id="5fdc7-161">Element</span></span>|<span data-ttu-id="5fdc7-162">Description</span><span class="sxs-lookup"><span data-stu-id="5fdc7-162">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5fdc7-163">\<client></span><span class="sxs-lookup"><span data-stu-id="5fdc7-163">\<client></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/client.md)|<span data-ttu-id="5fdc7-164">Section de configuration qui définit une liste des points de terminaison auxquels un client peut se connecter.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-164">A configuration section that defines a list of endpoints that a client can connect to.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="5fdc7-165">Exemple</span><span class="sxs-lookup"><span data-stu-id="5fdc7-165">Example</span></span>  
 <span data-ttu-id="5fdc7-166">Il s'agit d'un exemple de configuration de point de terminaison de canal.</span><span class="sxs-lookup"><span data-stu-id="5fdc7-166">This is an example of a channel endpoint configuration.</span></span>  
  
```xml  
<endpoint address="/HelloWorld/"
          bindingConfiguration="usingDefaults"
          name="MyBinding"
          binding="customBinding"
          contract="HelloWorld">
</endpoint>
```  
  
## <a name="see-also"></a><span data-ttu-id="5fdc7-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fdc7-167">See also</span></span>

- <xref:System.ServiceModel.Configuration.ChannelEndpointElement>
- <xref:System.ServiceModel.Configuration.ClientSection>
- <xref:System.ServiceModel.Configuration.ChannelEndpointElementCollection>
- <xref:System.ServiceModel.Configuration.ClientSection.Endpoints%2A>
- <xref:System.ServiceModel.Configuration.ChannelEndpointElement>
- [<span data-ttu-id="5fdc7-168">Configuration du client WCF</span><span class="sxs-lookup"><span data-stu-id="5fdc7-168">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)
- [<span data-ttu-id="5fdc7-169">Clients</span><span class="sxs-lookup"><span data-stu-id="5fdc7-169">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
