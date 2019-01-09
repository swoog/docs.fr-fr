---
title: '&lt;émetteur&gt;'
ms.date: 03/30/2017
ms.assetid: 8c49c6ae-fa1a-4179-a84b-613c3216dcde
ms.openlocfilehash: d2728bf3613b41ed9f0810207d27d6d67477afd2
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149551"
---
# <a name="ltissuergt"></a><span data-ttu-id="bacef-102">&lt;émetteur&gt;</span><span class="sxs-lookup"><span data-stu-id="bacef-102">&lt;issuer&gt;</span></span>
<span data-ttu-id="bacef-103">Spécifie le service d'émission de jeton de sécurité (STS) qui émet des jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="bacef-103">Specifies the Security Token Service (STS) that issues security tokens.</span></span>  
  
 <span data-ttu-id="bacef-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="bacef-104">\<system.serviceModel></span></span>  
<span data-ttu-id="bacef-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="bacef-105">\<bindings></span></span>  
<span data-ttu-id="bacef-106">\<wsFederationHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="bacef-106">\<wsFederationHttpBinding></span></span>  
<span data-ttu-id="bacef-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="bacef-107">\<binding></span></span>  
<span data-ttu-id="bacef-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="bacef-108">\<security></span></span>  
<span data-ttu-id="bacef-109">\<message></span><span class="sxs-lookup"><span data-stu-id="bacef-109">\<message></span></span>  
<span data-ttu-id="bacef-110">\<l’émetteur ></span><span class="sxs-lookup"><span data-stu-id="bacef-110">\<issuer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bacef-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bacef-111">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bacef-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="bacef-112">Attributes and Elements</span></span>  
 <span data-ttu-id="bacef-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="bacef-113">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bacef-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="bacef-114">Attributes</span></span>  
  
|<span data-ttu-id="bacef-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="bacef-115">Attribute</span></span>|<span data-ttu-id="bacef-116">Description</span><span class="sxs-lookup"><span data-stu-id="bacef-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="bacef-117">address</span><span class="sxs-lookup"><span data-stu-id="bacef-117">address</span></span>|<span data-ttu-id="bacef-118">Chaîne requise.</span><span class="sxs-lookup"><span data-stu-id="bacef-118">Required string.</span></span> <span data-ttu-id="bacef-119">URL du service STS.</span><span class="sxs-lookup"><span data-stu-id="bacef-119">The URL of the STS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bacef-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bacef-120">Child Elements</span></span>  
  
|<span data-ttu-id="bacef-121">Élément</span><span class="sxs-lookup"><span data-stu-id="bacef-121">Element</span></span>|<span data-ttu-id="bacef-122">Description</span><span class="sxs-lookup"><span data-stu-id="bacef-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bacef-123">\<en-têtes ></span><span class="sxs-lookup"><span data-stu-id="bacef-123">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="bacef-124">Collection d’en-têtes d’adresse de points de terminaison pouvant être créée par le générateur.</span><span class="sxs-lookup"><span data-stu-id="bacef-124">A collection of address headers for the endpoints that the builder can create.</span></span>|  
|[<span data-ttu-id="bacef-125">\<identité ></span><span class="sxs-lookup"><span data-stu-id="bacef-125">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="bacef-126">Lors de l'utilisation d'un jeton émis, spécifie des paramètres qui permettent au client d'authentifier le serveur.</span><span class="sxs-lookup"><span data-stu-id="bacef-126">When using an issued token, specifies settings that enable the client to authenticate the server.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="bacef-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bacef-127">Parent Elements</span></span>  
  
|<span data-ttu-id="bacef-128">Élément</span><span class="sxs-lookup"><span data-stu-id="bacef-128">Element</span></span>|<span data-ttu-id="bacef-129">Description</span><span class="sxs-lookup"><span data-stu-id="bacef-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bacef-130">\<message></span><span class="sxs-lookup"><span data-stu-id="bacef-130">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-element-of-wsfederationhttpbinding.md)|<span data-ttu-id="bacef-131">Définit les paramètres de la sécurité au niveau du message pour le [ \<wsFederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="bacef-131">Defines the settings for the message-level security for the [\<wsFederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="bacef-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bacef-132">See Also</span></span>  
 <xref:System.ServiceModel.FederatedMessageSecurityOverHttp>  
 <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.Issuer%2A>  
 <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>  
 [<span data-ttu-id="bacef-133">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="bacef-133">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="bacef-134">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="bacef-134">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="bacef-135">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="bacef-135">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="bacef-136">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="bacef-136">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="bacef-137">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="bacef-137">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)  
 [<span data-ttu-id="bacef-138">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="bacef-138">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
