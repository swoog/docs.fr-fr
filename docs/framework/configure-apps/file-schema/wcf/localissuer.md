---
title: <localIssuer>
ms.date: 03/30/2017
ms.assetid: 26bdd0df-0e7d-4b9e-bbeb-f28c53769385
ms.openlocfilehash: 9a51387cd75d57a6828ecde1dcd788b056f7e27a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61766400"
---
# <a name="localissuer"></a><span data-ttu-id="37138-101">\<localIssuer></span><span class="sxs-lookup"><span data-stu-id="37138-101">\<localIssuer></span></span>
<span data-ttu-id="37138-102">Spécifie l'adresse et la liaison de l'émetteur local à utiliser pour obtenir un jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="37138-102">Specifies the address and binding of the local issuer to be used to obtain a security token.</span></span>  
  
 <span data-ttu-id="37138-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="37138-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="37138-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="37138-104">\<behaviors></span></span>  
<span data-ttu-id="37138-105">section d’endpointBehaviors</span><span class="sxs-lookup"><span data-stu-id="37138-105">endpointBehaviors section</span></span>  
<span data-ttu-id="37138-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="37138-106">\<behavior></span></span>  
<span data-ttu-id="37138-107">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="37138-107">\<clientCredentials></span></span>  
<span data-ttu-id="37138-108">\<issuedToken></span><span class="sxs-lookup"><span data-stu-id="37138-108">\<issuedToken></span></span>  
<span data-ttu-id="37138-109">\<localIssuer></span><span class="sxs-lookup"><span data-stu-id="37138-109">\<localIssuer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="37138-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37138-110">Syntax</span></span>  
  
```xml  
<localIssuer address="String"
             binding="String"
             bindingConfiguration="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="37138-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="37138-111">Attributes and Elements</span></span>  
 <span data-ttu-id="37138-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="37138-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="37138-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="37138-113">Attributes</span></span>  
  
|<span data-ttu-id="37138-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="37138-114">Attribute</span></span>|<span data-ttu-id="37138-115">Description</span><span class="sxs-lookup"><span data-stu-id="37138-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="37138-116">adresse</span><span class="sxs-lookup"><span data-stu-id="37138-116">address</span></span>|<span data-ttu-id="37138-117">Chaîne requise.</span><span class="sxs-lookup"><span data-stu-id="37138-117">Required string.</span></span> <span data-ttu-id="37138-118">Spécifie l'URI de l'émetteur local.</span><span class="sxs-lookup"><span data-stu-id="37138-118">Specifies the URI of the local issuer.</span></span>|  
|<span data-ttu-id="37138-119">liaison</span><span class="sxs-lookup"><span data-stu-id="37138-119">binding</span></span>|<span data-ttu-id="37138-120">Chaîne facultative.</span><span class="sxs-lookup"><span data-stu-id="37138-120">Optional string.</span></span> <span data-ttu-id="37138-121">Une des liaisons fournies par le système.</span><span class="sxs-lookup"><span data-stu-id="37138-121">One of the system-provided bindings.</span></span> <span data-ttu-id="37138-122">Pour obtenir la liste, consultez [System-Provided Bindings](../../../../../docs/framework/wcf/system-provided-bindings.md).</span><span class="sxs-lookup"><span data-stu-id="37138-122">For a list, see [System-Provided Bindings](../../../../../docs/framework/wcf/system-provided-bindings.md).</span></span>|  
|<span data-ttu-id="37138-123">bindingConfiguration</span><span class="sxs-lookup"><span data-stu-id="37138-123">bindingConfiguration</span></span>|<span data-ttu-id="37138-124">Chaîne facultative.</span><span class="sxs-lookup"><span data-stu-id="37138-124">Optional string.</span></span> <span data-ttu-id="37138-125">Spécifie une configuration de liaison recherchée dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="37138-125">Specifies a binding configuration found in the configuration file.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="37138-126">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="37138-126">Child Elements</span></span>  
  
|<span data-ttu-id="37138-127">Élément</span><span class="sxs-lookup"><span data-stu-id="37138-127">Element</span></span>|<span data-ttu-id="37138-128">Description</span><span class="sxs-lookup"><span data-stu-id="37138-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="37138-129">\<identity></span><span class="sxs-lookup"><span data-stu-id="37138-129">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="37138-130">Spécifie les informations d'identité de l'émetteur local.</span><span class="sxs-lookup"><span data-stu-id="37138-130">Specifies identity information for the local issuer.</span></span>|  
|[<span data-ttu-id="37138-131">\<headers></span><span class="sxs-lookup"><span data-stu-id="37138-131">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="37138-132">Collection d'en-têtes d'adresse requis pour adresser correctement l'émetteur local.</span><span class="sxs-lookup"><span data-stu-id="37138-132">A collection of address headers that are required in order to correctly address the local issuer.</span></span> <span data-ttu-id="37138-133">Vous pouvez utiliser le mot clé `add` pour ajouter un en-tête à cette collection.</span><span class="sxs-lookup"><span data-stu-id="37138-133">You can use the `add` keyword to add a header to this collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="37138-134">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="37138-134">Parent Elements</span></span>  
  
|<span data-ttu-id="37138-135">Élément</span><span class="sxs-lookup"><span data-stu-id="37138-135">Element</span></span>|<span data-ttu-id="37138-136">Description</span><span class="sxs-lookup"><span data-stu-id="37138-136">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="37138-137">\<issuedToken></span><span class="sxs-lookup"><span data-stu-id="37138-137">\<issuedToken></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtoken.md)|<span data-ttu-id="37138-138">Spécifie un jeton personnalisé utilisé pour authentifier un client auprès d'un service.</span><span class="sxs-lookup"><span data-stu-id="37138-138">Specifies a custom token used to authenticate a client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="37138-139">Notes</span><span class="sxs-lookup"><span data-stu-id="37138-139">Remarks</span></span>  
 <span data-ttu-id="37138-140">Lors de l'obtention d'un jeton émis depuis un service d'émission de jeton de sécurité (STS), l'application cliente doit être configurée avec l'adresse et la liaison à utiliser pour pouvoir communiquer avec le STS.</span><span class="sxs-lookup"><span data-stu-id="37138-140">When obtaining an issued token from a Security Token Service (STS), the client application must be configured with the address and binding to use to communicate with the STS.</span></span> <span data-ttu-id="37138-141">Lorsque le <xref:System.ServiceModel.WSFederationHttpBinding> ne fournit pas d’URL pour le service de jeton de sécurité, ou lorsque l’adresse de l’émetteur d’une liaison fédérée est `http://schemas.microsoft.com/2005/12/ServiceModel/Addressing/Anonymous` ou `null`, le canal de client Windows Communication Foundation (WCF) utilise les valeurs spécifiées par `address`et `binding` pour communiquer avec le STS pour obtenir le jeton émis.</span><span class="sxs-lookup"><span data-stu-id="37138-141">When the <xref:System.ServiceModel.WSFederationHttpBinding> does not supply a URL for the security token service, or when the issuer address of a federated binding is `http://schemas.microsoft.com/2005/12/ServiceModel/Addressing/Anonymous` or `null`, the client's Windows Communication Foundation (WCF) channel uses the values specified by `address` and `binding` to communicate with the STS to obtain the issued token.</span></span> <span data-ttu-id="37138-142">Pour plus d’informations sur la configuration d’un émetteur local, consultez [Comment : Configurer un émetteur Local](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md).</span><span class="sxs-lookup"><span data-stu-id="37138-142">For more information on configuring a local issuer, see [How to: Configure a Local Issuer](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="37138-143">Exemple</span><span class="sxs-lookup"><span data-stu-id="37138-143">Example</span></span>  
 <span data-ttu-id="37138-144">L'exemple suivant définit les attributs `address`, `binding` et `bindingConfiguration` d'un élément `localIssuer`.</span><span class="sxs-lookup"><span data-stu-id="37138-144">The following example sets the `address`, `binding`, and `bindingConfiguration` attributes of a `localIssuer` element.</span></span>  
  
```xml  
<system.serviceModel>
  <behaviors>
    <endpointBehaviors>
      <behavior name="MyEndpointBehavior">
        <clientCredentials>
          <issuedToken cacheIssuedTokens="false"
                       defaultKeyEntropyMode="ClientEntropy">
            <localIssuer address="net.tcp://cohowinery/tokens"
                         binding="netTcpBinding"
                         bindingConfiguration="myTcpBindingConfig" />
          </issuedToken>
        </clientCredentials>
      </behavior>
    </endpointBehaviors>
  </behaviors>
</system.serviceModel>
```  
  
## <a name="see-also"></a><span data-ttu-id="37138-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37138-145">See also</span></span>

- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.LocalIssuer%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential>
- [<span data-ttu-id="37138-146">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="37138-146">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="37138-147">Guide pratique pour Configurer un émetteur Local</span><span class="sxs-lookup"><span data-stu-id="37138-147">How to: Configure a Local Issuer</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)
- [<span data-ttu-id="37138-148">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="37138-148">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="37138-149">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="37138-149">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="37138-150">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="37138-150">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="37138-151">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="37138-151">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="37138-152">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="37138-152">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- [<span data-ttu-id="37138-153">Guide pratique pour Créer un Client fédéré</span><span class="sxs-lookup"><span data-stu-id="37138-153">How to: Create a Federated Client</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="37138-154">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="37138-154">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
