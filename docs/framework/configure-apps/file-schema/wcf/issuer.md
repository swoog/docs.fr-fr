---
title: <issuer>
ms.date: 03/30/2017
ms.assetid: 8c49c6ae-fa1a-4179-a84b-613c3216dcde
ms.openlocfilehash: 37d935287fa7dfba640c39071295fd660f4db7c1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59160821"
---
# <a name="issuer"></a><span data-ttu-id="ebed1-101">\<issuer></span><span class="sxs-lookup"><span data-stu-id="ebed1-101">\<issuer></span></span>
<span data-ttu-id="ebed1-102">Spécifie le service d'émission de jeton de sécurité (STS) qui émet des jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ebed1-102">Specifies the Security Token Service (STS) that issues security tokens.</span></span>  
  
 <span data-ttu-id="ebed1-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="ebed1-103">\<system.serviceModel></span></span>  
<span data-ttu-id="ebed1-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="ebed1-104">\<bindings></span></span>  
<span data-ttu-id="ebed1-105">\<wsFederationHttpBinding></span><span class="sxs-lookup"><span data-stu-id="ebed1-105">\<wsFederationHttpBinding></span></span>  
<span data-ttu-id="ebed1-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="ebed1-106">\<binding></span></span>  
<span data-ttu-id="ebed1-107">\<security></span><span class="sxs-lookup"><span data-stu-id="ebed1-107">\<security></span></span>  
<span data-ttu-id="ebed1-108">\<message></span><span class="sxs-lookup"><span data-stu-id="ebed1-108">\<message></span></span>  
<span data-ttu-id="ebed1-109">\<issuer></span><span class="sxs-lookup"><span data-stu-id="ebed1-109">\<issuer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ebed1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebed1-110">Syntax</span></span>  
  
```xml  
<issuer address="Uri">
  <headers>
    <add name="String"
         namespace="String" />
  </headers>
  <identity>
    <certificate encodedValue="String" />
    <certificateReference findValue="String"
                          isChainIncluded="Boolean"
                          storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                          storeLocation="LocalMachine/CurrentUser"
                          x509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
    <dns value="String" />
    <rsa value="String" />
    <servicePrincipalName value="String" />
    <usePrincipalName value="String" />
  </identity>
</issuer>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ebed1-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ebed1-111">Attributes and Elements</span></span>  
 <span data-ttu-id="ebed1-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ebed1-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ebed1-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="ebed1-113">Attributes</span></span>  
  
|<span data-ttu-id="ebed1-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="ebed1-114">Attribute</span></span>|<span data-ttu-id="ebed1-115">Description</span><span class="sxs-lookup"><span data-stu-id="ebed1-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ebed1-116">adresse</span><span class="sxs-lookup"><span data-stu-id="ebed1-116">address</span></span>|<span data-ttu-id="ebed1-117">Chaîne requise.</span><span class="sxs-lookup"><span data-stu-id="ebed1-117">Required string.</span></span> <span data-ttu-id="ebed1-118">URL du service STS.</span><span class="sxs-lookup"><span data-stu-id="ebed1-118">The URL of the STS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ebed1-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ebed1-119">Child Elements</span></span>  
  
|<span data-ttu-id="ebed1-120">Élément</span><span class="sxs-lookup"><span data-stu-id="ebed1-120">Element</span></span>|<span data-ttu-id="ebed1-121">Description</span><span class="sxs-lookup"><span data-stu-id="ebed1-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ebed1-122">\<headers></span><span class="sxs-lookup"><span data-stu-id="ebed1-122">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="ebed1-123">Collection d'en-têtes d'adresse de points de terminaison pouvant être créée par le générateur.</span><span class="sxs-lookup"><span data-stu-id="ebed1-123">A collection of address headers for the endpoints that the builder can create.</span></span>|  
|[<span data-ttu-id="ebed1-124">\<identity></span><span class="sxs-lookup"><span data-stu-id="ebed1-124">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="ebed1-125">Lors de l'utilisation d'un jeton émis, spécifie des paramètres qui permettent au client d'authentifier le serveur.</span><span class="sxs-lookup"><span data-stu-id="ebed1-125">When using an issued token, specifies settings that enable the client to authenticate the server.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ebed1-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ebed1-126">Parent Elements</span></span>  
  
|<span data-ttu-id="ebed1-127">Élément</span><span class="sxs-lookup"><span data-stu-id="ebed1-127">Element</span></span>|<span data-ttu-id="ebed1-128">Description</span><span class="sxs-lookup"><span data-stu-id="ebed1-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ebed1-129">\<message></span><span class="sxs-lookup"><span data-stu-id="ebed1-129">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-element-of-wsfederationhttpbinding.md)|<span data-ttu-id="ebed1-130">Définit les paramètres de la sécurité au niveau du message pour le [ \<wsFederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="ebed1-130">Defines the settings for the message-level security for the [\<wsFederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ebed1-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebed1-131">See also</span></span>

- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.Issuer%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>
- [<span data-ttu-id="ebed1-132">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="ebed1-132">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="ebed1-133">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="ebed1-133">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="ebed1-134">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="ebed1-134">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="ebed1-135">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="ebed1-135">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="ebed1-136">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="ebed1-136">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="ebed1-137">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="ebed1-137">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
