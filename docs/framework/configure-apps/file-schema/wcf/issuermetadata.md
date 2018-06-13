---
title: '&lt;issuerMetadata&gt;'
ms.date: 03/30/2017
ms.assetid: e7eae2c0-cc17-4281-af59-e4eb8d54f92a
ms.openlocfilehash: 5f6b8d2f861c4d64a3b81407de4ce13b42d9b864
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32752931"
---
# <a name="ltissuermetadatagt"></a><span data-ttu-id="5d661-102">&lt;issuerMetadata&gt;</span><span class="sxs-lookup"><span data-stu-id="5d661-102">&lt;issuerMetadata&gt;</span></span>
<span data-ttu-id="5d661-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="5d661-103">\<system.serviceModel></span></span>  
<span data-ttu-id="5d661-104">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="5d661-104">\<bindings></span></span>  
<span data-ttu-id="5d661-105">\<wsFederationHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="5d661-105">\<wsFederationHttpBinding></span></span>  
<span data-ttu-id="5d661-106">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="5d661-106">\<binding></span></span>  
<span data-ttu-id="5d661-107">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="5d661-107">\<security></span></span>  
<span data-ttu-id="5d661-108">\<message></span><span class="sxs-lookup"><span data-stu-id="5d661-108">\<message></span></span>  
<span data-ttu-id="5d661-109">\<issuerMetadata ></span><span class="sxs-lookup"><span data-stu-id="5d661-109">\<issuerMetadata></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5d661-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d661-110">Syntax</span></span>  
  
```xml  
<issuerMetadata address=String" >  
   <headers>  
      <add name="String"  
                 namespace="String" />  
   </headers>  
   <identity>  
           <certificate encodedValue="String"/>  
      <certificateReference findValue="String"   
         isChainIncluded="Boolean"  
         storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"  
         storeLocation="LocalMachine/CurrentUser"  
                  x509FindType=System.Security.Cryptography.X509certificates.X509findtype/>  
      <dns value="String"/>  
      <rsa value="String"/>  
      <servicePrincipalName value="String"/>  
      <usePrincipalName value="String"/>  
   </identity>  
</issuerMetadata>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5d661-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5d661-111">Attributes and Elements</span></span>  
 <span data-ttu-id="5d661-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5d661-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5d661-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="5d661-113">Attributes</span></span>  
  
|<span data-ttu-id="5d661-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="5d661-114">Attribute</span></span>|<span data-ttu-id="5d661-115">Description</span><span class="sxs-lookup"><span data-stu-id="5d661-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5d661-116">address</span><span class="sxs-lookup"><span data-stu-id="5d661-116">address</span></span>|<span data-ttu-id="5d661-117">Attribut `string` requis.</span><span class="sxs-lookup"><span data-stu-id="5d661-117">Required `string` attribute.</span></span><br /><br /> <span data-ttu-id="5d661-118">Spécifie l'adresse du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5d661-118">Specifies the address of the endpoint.</span></span> <span data-ttu-id="5d661-119">L'adresse doit être un URI absolu.</span><span class="sxs-lookup"><span data-stu-id="5d661-119">The address must be an absolute URI.</span></span> <span data-ttu-id="5d661-120">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="5d661-120">The default value is an empty string.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5d661-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5d661-121">Child Elements</span></span>  
  
|<span data-ttu-id="5d661-122">Élément</span><span class="sxs-lookup"><span data-stu-id="5d661-122">Element</span></span>|<span data-ttu-id="5d661-123">Description</span><span class="sxs-lookup"><span data-stu-id="5d661-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5d661-124">\<en-têtes ></span><span class="sxs-lookup"><span data-stu-id="5d661-124">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="5d661-125">Collection d'en-têtes d'adresses.</span><span class="sxs-lookup"><span data-stu-id="5d661-125">A collection of address headers.</span></span>|  
|[<span data-ttu-id="5d661-126">\<identité ></span><span class="sxs-lookup"><span data-stu-id="5d661-126">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="5d661-127">Identité qui permet l'authentification d'un point de terminaison par les autres points de terminaison qui échangent des messages avec lui.</span><span class="sxs-lookup"><span data-stu-id="5d661-127">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5d661-128">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5d661-128">Parent Elements</span></span>  
  
|<span data-ttu-id="5d661-129">Élément</span><span class="sxs-lookup"><span data-stu-id="5d661-129">Element</span></span>|<span data-ttu-id="5d661-130">Description</span><span class="sxs-lookup"><span data-stu-id="5d661-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5d661-131">\<message></span><span class="sxs-lookup"><span data-stu-id="5d661-131">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-element-of-wsfederationhttpbinding.md)|<span data-ttu-id="5d661-132">Définit les paramètres de la sécurité au niveau du message pour le [ \<wsFederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="5d661-132">Defines the settings for the message-level security for the [\<wsFederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5d661-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d661-133">See Also</span></span>  
 <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuerMetadataAddress%2A>  
 <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.IssuerMetadata%2A>  
 [<span data-ttu-id="5d661-134">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="5d661-134">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="5d661-135">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="5d661-135">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="5d661-136">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="5d661-136">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)  
 [<span data-ttu-id="5d661-137">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="5d661-137">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
