---
title: '&lt;issuerMetadata&gt;'
ms.date: 03/30/2017
ms.assetid: e7eae2c0-cc17-4281-af59-e4eb8d54f92a
ms.openlocfilehash: 22e30e0962ec8d2eb0f7e52f4db143fba9bbf703
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491556"
---
# <a name="ltissuermetadatagt"></a><span data-ttu-id="4c6cb-102">&lt;issuerMetadata&gt;</span><span class="sxs-lookup"><span data-stu-id="4c6cb-102">&lt;issuerMetadata&gt;</span></span>
<span data-ttu-id="4c6cb-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="4c6cb-103">\<system.serviceModel></span></span>  
<span data-ttu-id="4c6cb-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="4c6cb-104">\<bindings></span></span>  
<span data-ttu-id="4c6cb-105">\<wsFederationHttpBinding></span><span class="sxs-lookup"><span data-stu-id="4c6cb-105">\<wsFederationHttpBinding></span></span>  
<span data-ttu-id="4c6cb-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="4c6cb-106">\<binding></span></span>  
<span data-ttu-id="4c6cb-107">\<security></span><span class="sxs-lookup"><span data-stu-id="4c6cb-107">\<security></span></span>  
<span data-ttu-id="4c6cb-108">\<message></span><span class="sxs-lookup"><span data-stu-id="4c6cb-108">\<message></span></span>  
<span data-ttu-id="4c6cb-109">\<issuerMetadata></span><span class="sxs-lookup"><span data-stu-id="4c6cb-109">\<issuerMetadata></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4c6cb-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c6cb-110">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4c6cb-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4c6cb-111">Attributes and Elements</span></span>  
 <span data-ttu-id="4c6cb-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4c6cb-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4c6cb-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="4c6cb-113">Attributes</span></span>  
  
|<span data-ttu-id="4c6cb-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="4c6cb-114">Attribute</span></span>|<span data-ttu-id="4c6cb-115">Description</span><span class="sxs-lookup"><span data-stu-id="4c6cb-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4c6cb-116">address</span><span class="sxs-lookup"><span data-stu-id="4c6cb-116">address</span></span>|<span data-ttu-id="4c6cb-117">Attribut `string` requis.</span><span class="sxs-lookup"><span data-stu-id="4c6cb-117">Required `string` attribute.</span></span><br /><br /> <span data-ttu-id="4c6cb-118">Spécifie l'adresse du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="4c6cb-118">Specifies the address of the endpoint.</span></span> <span data-ttu-id="4c6cb-119">L'adresse doit être un URI absolu.</span><span class="sxs-lookup"><span data-stu-id="4c6cb-119">The address must be an absolute URI.</span></span> <span data-ttu-id="4c6cb-120">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="4c6cb-120">The default value is an empty string.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4c6cb-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4c6cb-121">Child Elements</span></span>  
  
|<span data-ttu-id="4c6cb-122">Élément</span><span class="sxs-lookup"><span data-stu-id="4c6cb-122">Element</span></span>|<span data-ttu-id="4c6cb-123">Description</span><span class="sxs-lookup"><span data-stu-id="4c6cb-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4c6cb-124">\<headers></span><span class="sxs-lookup"><span data-stu-id="4c6cb-124">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="4c6cb-125">Collection d'en-têtes d'adresses.</span><span class="sxs-lookup"><span data-stu-id="4c6cb-125">A collection of address headers.</span></span>|  
|[<span data-ttu-id="4c6cb-126">\<identity></span><span class="sxs-lookup"><span data-stu-id="4c6cb-126">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="4c6cb-127">Identité qui permet l'authentification d'un point de terminaison par les autres points de terminaison qui échangent des messages avec lui.</span><span class="sxs-lookup"><span data-stu-id="4c6cb-127">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4c6cb-128">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4c6cb-128">Parent Elements</span></span>  
  
|<span data-ttu-id="4c6cb-129">Élément</span><span class="sxs-lookup"><span data-stu-id="4c6cb-129">Element</span></span>|<span data-ttu-id="4c6cb-130">Description</span><span class="sxs-lookup"><span data-stu-id="4c6cb-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4c6cb-131">\<message></span><span class="sxs-lookup"><span data-stu-id="4c6cb-131">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-element-of-wsfederationhttpbinding.md)|<span data-ttu-id="4c6cb-132">Définit les paramètres de la sécurité au niveau du message pour le [ \<wsFederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="4c6cb-132">Defines the settings for the message-level security for the [\<wsFederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4c6cb-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c6cb-133">See also</span></span>
- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuerMetadataAddress%2A>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.IssuerMetadata%2A>
- [<span data-ttu-id="4c6cb-134">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="4c6cb-134">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="4c6cb-135">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="4c6cb-135">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="4c6cb-136">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="4c6cb-136">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="4c6cb-137">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="4c6cb-137">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
