---
title: '&lt;localIssuer&gt;'
ms.date: 03/30/2017
ms.assetid: 26bdd0df-0e7d-4b9e-bbeb-f28c53769385
ms.openlocfilehash: 7a48cbb3a1e17ac1fc9fa9f43301ef153cdb866c
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151872"
---
# <a name="ltlocalissuergt"></a><span data-ttu-id="cccad-102">&lt;localIssuer&gt;</span><span class="sxs-lookup"><span data-stu-id="cccad-102">&lt;localIssuer&gt;</span></span>
<span data-ttu-id="cccad-103">Spécifie l’adresse et la liaison de l’émetteur local à utiliser pour obtenir un jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="cccad-103">Specifies the address and binding of the local issuer to be used to obtain a security token.</span></span>  
  
 <span data-ttu-id="cccad-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="cccad-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="cccad-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="cccad-105">\<behaviors></span></span>  
<span data-ttu-id="cccad-106">section d’endpointBehaviors</span><span class="sxs-lookup"><span data-stu-id="cccad-106">endpointBehaviors section</span></span>  
<span data-ttu-id="cccad-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="cccad-107">\<behavior></span></span>  
<span data-ttu-id="cccad-108">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="cccad-108">\<clientCredentials></span></span>  
<span data-ttu-id="cccad-109">\<issuedToken ></span><span class="sxs-lookup"><span data-stu-id="cccad-109">\<issuedToken></span></span>  
<span data-ttu-id="cccad-110">\<localIssuer ></span><span class="sxs-lookup"><span data-stu-id="cccad-110">\<localIssuer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cccad-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cccad-111">Syntax</span></span>  
  
```xml  
<localIssuer address="String"
             binding="String"
             bindingConfiguration="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cccad-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="cccad-112">Attributes and Elements</span></span>  
 <span data-ttu-id="cccad-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="cccad-113">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cccad-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="cccad-114">Attributes</span></span>  
  
|<span data-ttu-id="cccad-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="cccad-115">Attribute</span></span>|<span data-ttu-id="cccad-116">Description</span><span class="sxs-lookup"><span data-stu-id="cccad-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="cccad-117">address</span><span class="sxs-lookup"><span data-stu-id="cccad-117">address</span></span>|<span data-ttu-id="cccad-118">Chaîne requise.</span><span class="sxs-lookup"><span data-stu-id="cccad-118">Required string.</span></span> <span data-ttu-id="cccad-119">Spécifie l'URI de l'émetteur local.</span><span class="sxs-lookup"><span data-stu-id="cccad-119">Specifies the URI of the local issuer.</span></span>|  
|<span data-ttu-id="cccad-120">liaison</span><span class="sxs-lookup"><span data-stu-id="cccad-120">binding</span></span>|<span data-ttu-id="cccad-121">Chaîne facultative.</span><span class="sxs-lookup"><span data-stu-id="cccad-121">Optional string.</span></span> <span data-ttu-id="cccad-122">Une des liaisons fournies par le système.</span><span class="sxs-lookup"><span data-stu-id="cccad-122">One of the system-provided bindings.</span></span> <span data-ttu-id="cccad-123">Pour obtenir la liste, consultez [System-Provided Bindings](../../../../../docs/framework/wcf/system-provided-bindings.md).</span><span class="sxs-lookup"><span data-stu-id="cccad-123">For a list, see [System-Provided Bindings](../../../../../docs/framework/wcf/system-provided-bindings.md).</span></span>|  
|<span data-ttu-id="cccad-124">bindingConfiguration</span><span class="sxs-lookup"><span data-stu-id="cccad-124">bindingConfiguration</span></span>|<span data-ttu-id="cccad-125">Chaîne facultative.</span><span class="sxs-lookup"><span data-stu-id="cccad-125">Optional string.</span></span> <span data-ttu-id="cccad-126">Spécifie une configuration de liaison recherchée dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="cccad-126">Specifies a binding configuration found in the configuration file.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cccad-127">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cccad-127">Child Elements</span></span>  
  
|<span data-ttu-id="cccad-128">Élément</span><span class="sxs-lookup"><span data-stu-id="cccad-128">Element</span></span>|<span data-ttu-id="cccad-129">Description</span><span class="sxs-lookup"><span data-stu-id="cccad-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cccad-130">\<identité ></span><span class="sxs-lookup"><span data-stu-id="cccad-130">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="cccad-131">Spécifie les informations d'identité de l'émetteur local.</span><span class="sxs-lookup"><span data-stu-id="cccad-131">Specifies identity information for the local issuer.</span></span>|  
|[<span data-ttu-id="cccad-132">\<en-têtes ></span><span class="sxs-lookup"><span data-stu-id="cccad-132">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="cccad-133">Collection d’en-têtes d’adresse requis pour adresser correctement l’émetteur local.</span><span class="sxs-lookup"><span data-stu-id="cccad-133">A collection of address headers that are required in order to correctly address the local issuer.</span></span> <span data-ttu-id="cccad-134">Vous pouvez utiliser le mot clé `add` pour ajouter un en-tête à cette collection.</span><span class="sxs-lookup"><span data-stu-id="cccad-134">You can use the `add` keyword to add a header to this collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="cccad-135">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="cccad-135">Parent Elements</span></span>  
  
|<span data-ttu-id="cccad-136">Élément</span><span class="sxs-lookup"><span data-stu-id="cccad-136">Element</span></span>|<span data-ttu-id="cccad-137">Description</span><span class="sxs-lookup"><span data-stu-id="cccad-137">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cccad-138">\<issuedToken ></span><span class="sxs-lookup"><span data-stu-id="cccad-138">\<issuedToken></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtoken.md)|<span data-ttu-id="cccad-139">Spécifie un jeton personnalisé utilisé pour authentifier un client auprès d'un service.</span><span class="sxs-lookup"><span data-stu-id="cccad-139">Specifies a custom token used to authenticate a client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cccad-140">Notes</span><span class="sxs-lookup"><span data-stu-id="cccad-140">Remarks</span></span>  
 <span data-ttu-id="cccad-141">Lors de l’obtention d’un jeton émis depuis un service d’émission de jeton de sécurité (STS), l’application cliente doit être configurée avec l’adresse et la liaison à utiliser pour pouvoir communiquer avec le STS.</span><span class="sxs-lookup"><span data-stu-id="cccad-141">When obtaining an issued token from a Security Token Service (STS), the client application must be configured with the address and binding to use to communicate with the STS.</span></span> <span data-ttu-id="cccad-142">Lorsque le <xref:System.ServiceModel.WSFederationHttpBinding> ne fournit pas d’URL pour le service de jeton de sécurité, ou lorsque l’adresse de l’émetteur d’une liaison fédérée est `http://schemas.microsoft.com/2005/12/ServiceModel/Addressing/Anonymous` ou `null`, le canal de client Windows Communication Foundation (WCF) utilise les valeurs spécifiées par `address`et `binding` pour communiquer avec le STS pour obtenir le jeton émis.</span><span class="sxs-lookup"><span data-stu-id="cccad-142">When the <xref:System.ServiceModel.WSFederationHttpBinding> does not supply a URL for the security token service, or when the issuer address of a federated binding is `http://schemas.microsoft.com/2005/12/ServiceModel/Addressing/Anonymous` or `null`, the client's Windows Communication Foundation (WCF) channel uses the values specified by `address` and `binding` to communicate with the STS to obtain the issued token.</span></span> <span data-ttu-id="cccad-143">Pour plus d’informations sur la configuration d’un émetteur local, consultez [Comment : Configurer un émetteur Local](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md).</span><span class="sxs-lookup"><span data-stu-id="cccad-143">For more information on configuring a local issuer, see [How to: Configure a Local Issuer](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="cccad-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="cccad-144">Example</span></span>  
 <span data-ttu-id="cccad-145">L'exemple suivant définit les attributs `address`, `binding` et `bindingConfiguration` d'un élément `localIssuer`.</span><span class="sxs-lookup"><span data-stu-id="cccad-145">The following example sets the `address`, `binding`, and `bindingConfiguration` attributes of a `localIssuer` element.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="cccad-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cccad-146">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.LocalIssuer%2A>  
 <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>  
 <xref:System.ServiceModel.Security.IssuedTokenClientCredential>  
 [<span data-ttu-id="cccad-147">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="cccad-147">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)  
 [<span data-ttu-id="cccad-148">Guide pratique pour Configurer un émetteur Local</span><span class="sxs-lookup"><span data-stu-id="cccad-148">How to: Configure a Local Issuer</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)  
 [<span data-ttu-id="cccad-149">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="cccad-149">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="cccad-150">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="cccad-150">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)  
 [<span data-ttu-id="cccad-151">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="cccad-151">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="cccad-152">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="cccad-152">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="cccad-153">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="cccad-153">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)  
 [<span data-ttu-id="cccad-154">Guide pratique pour Créer un Client fédéré</span><span class="sxs-lookup"><span data-stu-id="cccad-154">How to: Create a Federated Client</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)  
 [<span data-ttu-id="cccad-155">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="cccad-155">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
