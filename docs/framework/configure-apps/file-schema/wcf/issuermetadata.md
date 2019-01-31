---
title: <issuerMetadata>
ms.date: 03/30/2017
ms.assetid: e7eae2c0-cc17-4281-af59-e4eb8d54f92a
ms.openlocfilehash: c557bd903462ccf4029b7317cbd45610e3fba165
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55264451"
---
# <a name="issuermetadata"></a><span data-ttu-id="21ba2-101">\<issuerMetadata></span><span class="sxs-lookup"><span data-stu-id="21ba2-101">\<issuerMetadata></span></span>
<span data-ttu-id="21ba2-102">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="21ba2-102">\<system.serviceModel></span></span>  
<span data-ttu-id="21ba2-103">\<bindings></span><span class="sxs-lookup"><span data-stu-id="21ba2-103">\<bindings></span></span>  
<span data-ttu-id="21ba2-104">\<wsFederationHttpBinding></span><span class="sxs-lookup"><span data-stu-id="21ba2-104">\<wsFederationHttpBinding></span></span>  
<span data-ttu-id="21ba2-105">\<binding></span><span class="sxs-lookup"><span data-stu-id="21ba2-105">\<binding></span></span>  
<span data-ttu-id="21ba2-106">\<security></span><span class="sxs-lookup"><span data-stu-id="21ba2-106">\<security></span></span>  
<span data-ttu-id="21ba2-107">\<message></span><span class="sxs-lookup"><span data-stu-id="21ba2-107">\<message></span></span>  
<span data-ttu-id="21ba2-108">\<issuerMetadata></span><span class="sxs-lookup"><span data-stu-id="21ba2-108">\<issuerMetadata></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="21ba2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21ba2-109">Syntax</span></span>  
  
```xml  
<issuerMetadata address="String">
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
</issuerMetadata>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="21ba2-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="21ba2-110">Attributes and Elements</span></span>  
 <span data-ttu-id="21ba2-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="21ba2-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="21ba2-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="21ba2-112">Attributes</span></span>  
  
|<span data-ttu-id="21ba2-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="21ba2-113">Attribute</span></span>|<span data-ttu-id="21ba2-114">Description</span><span class="sxs-lookup"><span data-stu-id="21ba2-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="21ba2-115">address</span><span class="sxs-lookup"><span data-stu-id="21ba2-115">address</span></span>|<span data-ttu-id="21ba2-116">Attribut `string` requis.</span><span class="sxs-lookup"><span data-stu-id="21ba2-116">Required `string` attribute.</span></span><br /><br /> <span data-ttu-id="21ba2-117">Spécifie l'adresse du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="21ba2-117">Specifies the address of the endpoint.</span></span> <span data-ttu-id="21ba2-118">L'adresse doit être un URI absolu.</span><span class="sxs-lookup"><span data-stu-id="21ba2-118">The address must be an absolute URI.</span></span> <span data-ttu-id="21ba2-119">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="21ba2-119">The default value is an empty string.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="21ba2-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="21ba2-120">Child Elements</span></span>  
  
|<span data-ttu-id="21ba2-121">Élément</span><span class="sxs-lookup"><span data-stu-id="21ba2-121">Element</span></span>|<span data-ttu-id="21ba2-122">Description</span><span class="sxs-lookup"><span data-stu-id="21ba2-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="21ba2-123">\<headers></span><span class="sxs-lookup"><span data-stu-id="21ba2-123">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="21ba2-124">Collection d'en-têtes d'adresses.</span><span class="sxs-lookup"><span data-stu-id="21ba2-124">A collection of address headers.</span></span>|  
|[<span data-ttu-id="21ba2-125">\<identity></span><span class="sxs-lookup"><span data-stu-id="21ba2-125">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="21ba2-126">Identité qui permet l'authentification d'un point de terminaison par les autres points de terminaison qui échangent des messages avec lui.</span><span class="sxs-lookup"><span data-stu-id="21ba2-126">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="21ba2-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="21ba2-127">Parent Elements</span></span>  
  
|<span data-ttu-id="21ba2-128">Élément</span><span class="sxs-lookup"><span data-stu-id="21ba2-128">Element</span></span>|<span data-ttu-id="21ba2-129">Description</span><span class="sxs-lookup"><span data-stu-id="21ba2-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="21ba2-130">\<message></span><span class="sxs-lookup"><span data-stu-id="21ba2-130">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-element-of-wsfederationhttpbinding.md)|<span data-ttu-id="21ba2-131">Définit les paramètres de la sécurité au niveau du message pour le [ \<wsFederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="21ba2-131">Defines the settings for the message-level security for the [\<wsFederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="21ba2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21ba2-132">See also</span></span>
- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuerMetadataAddress%2A>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.IssuerMetadata%2A>
- [<span data-ttu-id="21ba2-133">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="21ba2-133">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="21ba2-134">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="21ba2-134">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="21ba2-135">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="21ba2-135">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="21ba2-136">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="21ba2-136">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
