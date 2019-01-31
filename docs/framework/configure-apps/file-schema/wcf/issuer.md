---
title: <issuer>
ms.date: 03/30/2017
ms.assetid: 8c49c6ae-fa1a-4179-a84b-613c3216dcde
ms.openlocfilehash: 54f52b1496ada2573949f98e1397b3b7736078d3
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55254507"
---
# <a name="issuer"></a><span data-ttu-id="f6051-101">\<issuer></span><span class="sxs-lookup"><span data-stu-id="f6051-101">\<issuer></span></span>
<span data-ttu-id="f6051-102">Spécifie le service d'émission de jeton de sécurité (STS) qui émet des jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f6051-102">Specifies the Security Token Service (STS) that issues security tokens.</span></span>  
  
 <span data-ttu-id="f6051-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="f6051-103">\<system.serviceModel></span></span>  
<span data-ttu-id="f6051-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="f6051-104">\<bindings></span></span>  
<span data-ttu-id="f6051-105">\<wsFederationHttpBinding></span><span class="sxs-lookup"><span data-stu-id="f6051-105">\<wsFederationHttpBinding></span></span>  
<span data-ttu-id="f6051-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="f6051-106">\<binding></span></span>  
<span data-ttu-id="f6051-107">\<security></span><span class="sxs-lookup"><span data-stu-id="f6051-107">\<security></span></span>  
<span data-ttu-id="f6051-108">\<message></span><span class="sxs-lookup"><span data-stu-id="f6051-108">\<message></span></span>  
<span data-ttu-id="f6051-109">\<issuer></span><span class="sxs-lookup"><span data-stu-id="f6051-109">\<issuer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6051-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6051-110">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f6051-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f6051-111">Attributes and Elements</span></span>  
 <span data-ttu-id="f6051-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f6051-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f6051-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="f6051-113">Attributes</span></span>  
  
|<span data-ttu-id="f6051-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="f6051-114">Attribute</span></span>|<span data-ttu-id="f6051-115">Description</span><span class="sxs-lookup"><span data-stu-id="f6051-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f6051-116">address</span><span class="sxs-lookup"><span data-stu-id="f6051-116">address</span></span>|<span data-ttu-id="f6051-117">Chaîne requise.</span><span class="sxs-lookup"><span data-stu-id="f6051-117">Required string.</span></span> <span data-ttu-id="f6051-118">URL du service STS.</span><span class="sxs-lookup"><span data-stu-id="f6051-118">The URL of the STS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f6051-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f6051-119">Child Elements</span></span>  
  
|<span data-ttu-id="f6051-120">Élément</span><span class="sxs-lookup"><span data-stu-id="f6051-120">Element</span></span>|<span data-ttu-id="f6051-121">Description</span><span class="sxs-lookup"><span data-stu-id="f6051-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f6051-122">\<headers></span><span class="sxs-lookup"><span data-stu-id="f6051-122">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="f6051-123">Collection d’en-têtes d’adresse de points de terminaison pouvant être créée par le générateur.</span><span class="sxs-lookup"><span data-stu-id="f6051-123">A collection of address headers for the endpoints that the builder can create.</span></span>|  
|[<span data-ttu-id="f6051-124">\<identity></span><span class="sxs-lookup"><span data-stu-id="f6051-124">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="f6051-125">Lors de l'utilisation d'un jeton émis, spécifie des paramètres qui permettent au client d'authentifier le serveur.</span><span class="sxs-lookup"><span data-stu-id="f6051-125">When using an issued token, specifies settings that enable the client to authenticate the server.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f6051-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f6051-126">Parent Elements</span></span>  
  
|<span data-ttu-id="f6051-127">Élément</span><span class="sxs-lookup"><span data-stu-id="f6051-127">Element</span></span>|<span data-ttu-id="f6051-128">Description</span><span class="sxs-lookup"><span data-stu-id="f6051-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f6051-129">\<message></span><span class="sxs-lookup"><span data-stu-id="f6051-129">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-element-of-wsfederationhttpbinding.md)|<span data-ttu-id="f6051-130">Définit les paramètres de la sécurité au niveau du message pour le [ \<wsFederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="f6051-130">Defines the settings for the message-level security for the [\<wsFederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f6051-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6051-131">See also</span></span>
- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.Issuer%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>
- [<span data-ttu-id="f6051-132">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="f6051-132">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="f6051-133">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="f6051-133">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="f6051-134">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="f6051-134">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="f6051-135">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="f6051-135">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="f6051-136">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="f6051-136">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="f6051-137">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="f6051-137">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
