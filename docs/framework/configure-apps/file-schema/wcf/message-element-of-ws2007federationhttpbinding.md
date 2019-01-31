---
title: <message> élément de <ws2007FederationHttpBinding>
ms.date: 03/30/2017
ms.assetid: 52cd941d-e230-4c82-8b29-333a7d20eca8
ms.openlocfilehash: 9150b6f1ab821f7d062f389c3dbd7fa9119fd0db
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55289703"
---
# <a name="message-element-of-ws2007federationhttpbinding"></a><span data-ttu-id="a82d3-102">\<message > élément de \<ws2007FederationHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="a82d3-102">\<message> element of \<ws2007FederationHttpBinding></span></span>
<span data-ttu-id="a82d3-103">Définit les paramètres pour la sécurité au niveau du message pour le [ \<ws2007FederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007federationhttpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="a82d3-103">Defines settings for the message-level security for the [\<ws2007FederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007federationhttpbinding.md) element.</span></span>  
  
 <span data-ttu-id="a82d3-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="a82d3-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="a82d3-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="a82d3-105">\<bindings></span></span>  
<span data-ttu-id="a82d3-106">\<ws2007FederationHttpBinding></span><span class="sxs-lookup"><span data-stu-id="a82d3-106">\<ws2007FederationHttpBinding></span></span>  
<span data-ttu-id="a82d3-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="a82d3-107">\<binding></span></span>  
<span data-ttu-id="a82d3-108">\<security></span><span class="sxs-lookup"><span data-stu-id="a82d3-108">\<security></span></span>  
<span data-ttu-id="a82d3-109">\<message></span><span class="sxs-lookup"><span data-stu-id="a82d3-109">\<message></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a82d3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a82d3-110">Syntax</span></span>  
  
```xml  
<ws2007FederationBinding>
  <binding>
    <security>
      <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               issuedTokenType="string"
               issuedKeyType="SymmetricKey/PublicKey"
               negotiateServiceCredential="Boolean">
        <claimTypeRequirements>
          <add claimType="URI"
               isOptional="Boolean" />
        </claimTypeRequirements>
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
                                  X509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
            <dns value="String" />
            <rsa value="String" />
            <servicePrincipalName value="String" />
            <usePrincipalName value="String" />
          </identity>
        </issuerMetadata>
        <tokenRequestParameters>
          <xmlElement>
          </xmlElement>
        </tokenRequestParameters>
      </message>
    </security>
  </binding>
</ws2007FederationBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a82d3-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a82d3-111">Attributes and Elements</span></span>  
 <span data-ttu-id="a82d3-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a82d3-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a82d3-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="a82d3-113">Attributes</span></span>  
  
|<span data-ttu-id="a82d3-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="a82d3-114">Attribute</span></span>|<span data-ttu-id="a82d3-115">Description</span><span class="sxs-lookup"><span data-stu-id="a82d3-115">Description</span></span>|  
|---------------|-----------------|  
|`algorithmSuite`|<span data-ttu-id="a82d3-116">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="a82d3-116">Optional.</span></span> <span data-ttu-id="a82d3-117">Définit les algorithmes de chiffrement de message, de signature et de clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-117">Sets the message encryption, signature, and key-wrap algorithms.</span></span> <span data-ttu-id="a82d3-118">Les algorithmes et les tailles de clé sont déterminés par la classe <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>.</span><span class="sxs-lookup"><span data-stu-id="a82d3-118">The algorithms and the key sizes are determined by the <xref:System.ServiceModel.Security.SecurityAlgorithmSuite> class.</span></span> <span data-ttu-id="a82d3-119">Ces algorithmes se mappent à ceux définis dans la spécification Security Policy Language (WS-SecurityPolicy).</span><span class="sxs-lookup"><span data-stu-id="a82d3-119">These algorithms map to those specified in the Security Policy Language (WS-SecurityPolicy) specification.</span></span><br /><br /> <span data-ttu-id="a82d3-120">Consultez le tableau suivant pour connaître les valeurs autorisées.</span><span class="sxs-lookup"><span data-stu-id="a82d3-120">See the following table for possible values.</span></span> <span data-ttu-id="a82d3-121">La valeur par défaut est Basic256.</span><span class="sxs-lookup"><span data-stu-id="a82d3-121">The default value is Basic256.</span></span>|  
|`issuedKeyType`|<span data-ttu-id="a82d3-122">Spécifie le type de clé à émettre.</span><span class="sxs-lookup"><span data-stu-id="a82d3-122">Specifies the type of key to be issued.</span></span> <span data-ttu-id="a82d3-123">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a82d3-123">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="a82d3-124">-   SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="a82d3-124">-   SymmetricKey</span></span><br /><span data-ttu-id="a82d3-125">-   PublicKey</span><span class="sxs-lookup"><span data-stu-id="a82d3-125">-   PublicKey</span></span><br /><span data-ttu-id="a82d3-126">-   BearerKey</span><span class="sxs-lookup"><span data-stu-id="a82d3-126">-   BearerKey</span></span><br /><br /> <span data-ttu-id="a82d3-127">La valeur par défaut est SymmetricKey.</span><span class="sxs-lookup"><span data-stu-id="a82d3-127">The default is SymmetricKey.</span></span> <span data-ttu-id="a82d3-128">Cet attribut est de type <xref:System.IdentityModel.Tokens.SecurityKeyType>.</span><span class="sxs-lookup"><span data-stu-id="a82d3-128">This attribute is of type <xref:System.IdentityModel.Tokens.SecurityKeyType>.</span></span>|  
|`issuedTokenType`|<span data-ttu-id="a82d3-129">URI qui spécifie le type de jeton à émettre.</span><span class="sxs-lookup"><span data-stu-id="a82d3-129">A URI that specifies the type of token to be issued.</span></span> <span data-ttu-id="a82d3-130">La valeur par défaut est `null`.</span><span class="sxs-lookup"><span data-stu-id="a82d3-130">The default is `null`.</span></span>|  
|`negotiateServiceCredential`|<span data-ttu-id="a82d3-131">Valeur qui spécifie si les informations d'identification du service doivent être échangées dans le cadre de la négociation ou sont disponibles hors bande.</span><span class="sxs-lookup"><span data-stu-id="a82d3-131">A value that specifies whether the service credential should be exchanged as part of negotiation or is available out of band.</span></span> <span data-ttu-id="a82d3-132">La valeur par défaut est `true`, ce qui signifie que les informations d'identification du service sont négociées.</span><span class="sxs-lookup"><span data-stu-id="a82d3-132">The default is `true`, which means that the service credential is negotiated.</span></span>|  
  
## <a name="algorithmsuite-attribute"></a><span data-ttu-id="a82d3-133">Attribut algorithmSuite</span><span class="sxs-lookup"><span data-stu-id="a82d3-133">algorithmSuite Attribute</span></span>  
  
|<span data-ttu-id="a82d3-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="a82d3-134">Value</span></span>|<span data-ttu-id="a82d3-135">Description</span><span class="sxs-lookup"><span data-stu-id="a82d3-135">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="a82d3-136">Basic128</span><span class="sxs-lookup"><span data-stu-id="a82d3-136">Basic128</span></span>|<span data-ttu-id="a82d3-137">Utilisez le chiffrement Aes128, Sha1 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-137">Use Aes128 encryption, Sha1 for message digest, and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-138">Basic192</span><span class="sxs-lookup"><span data-stu-id="a82d3-138">Basic192</span></span>|<span data-ttu-id="a82d3-139">Utilisez le chiffrement Aes192, Sha1 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-139">Use Aes192 encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-140">Basic256</span><span class="sxs-lookup"><span data-stu-id="a82d3-140">Basic256</span></span>|<span data-ttu-id="a82d3-141">Utilisez le chiffrement Aes256, Sha1 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-141">Use Aes256 encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-142">Basic256Rsa15</span><span class="sxs-lookup"><span data-stu-id="a82d3-142">Basic256Rsa15</span></span>|<span data-ttu-id="a82d3-143">Utilisez Aes256 pour le chiffrement du message, Sha1 pour le résumé du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-143">Use Aes256 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-144">Basic192Rsa15</span><span class="sxs-lookup"><span data-stu-id="a82d3-144">Basic192Rsa15</span></span>|<span data-ttu-id="a82d3-145">Utilisez Aes192 pour le chiffrement du message, Sha1 pour le résumé du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-145">Use Aes192 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-146">TripleDes</span><span class="sxs-lookup"><span data-stu-id="a82d3-146">TripleDes</span></span>|<span data-ttu-id="a82d3-147">Utilisez le chiffrement TripleDes, Sha1 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-147">Use TripleDes encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-148">Basic128Rsa15</span><span class="sxs-lookup"><span data-stu-id="a82d3-148">Basic128Rsa15</span></span>|<span data-ttu-id="a82d3-149">Utilisez Aes128 pour le chiffrement du message, Sha1 pour le résumé du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-149">Use Aes128 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-150">TripleDesRsa15</span><span class="sxs-lookup"><span data-stu-id="a82d3-150">TripleDesRsa15</span></span>|<span data-ttu-id="a82d3-151">Utilisez le chiffrement TripleDes, Sha1 pour le résumé du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-151">Use TripleDes encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-152">Basic128Sha256</span><span class="sxs-lookup"><span data-stu-id="a82d3-152">Basic128Sha256</span></span>|<span data-ttu-id="a82d3-153">Utilisez Aes256 pour le chiffrement du message, Sha256 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-153">Use Aes256 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-154">Basic192Sha256</span><span class="sxs-lookup"><span data-stu-id="a82d3-154">Basic192Sha256</span></span>|<span data-ttu-id="a82d3-155">Utilisez Aes192 pour le chiffrement du message, Sha256 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-155">Use Aes192 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-156">Basic256Sha256</span><span class="sxs-lookup"><span data-stu-id="a82d3-156">Basic256Sha256</span></span>|<span data-ttu-id="a82d3-157">Utilisez Aes256 pour le chiffrement du message, Sha256 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-157">Use Aes256 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-158">TripleDesSha256</span><span class="sxs-lookup"><span data-stu-id="a82d3-158">TripleDesSha256</span></span>|<span data-ttu-id="a82d3-159">Utilisez TripleDes pour le chiffrement du message, Sha256 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-159">Use TripleDes for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-160">Basic128Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="a82d3-160">Basic128Sha256Rsa15</span></span>|<span data-ttu-id="a82d3-161">Utilisez Aes128 pour le chiffrement du message, Sha256 pour le résumé du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-161">Use Aes128 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-162">Basic192Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="a82d3-162">Basic192Sha256Rsa15</span></span>|<span data-ttu-id="a82d3-163">Utilisez Aes192 pour le chiffrement du message, Sha256 pour le résumé du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-163">Use Aes192 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-164">Basic256Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="a82d3-164">Basic256Sha256Rsa15</span></span>|<span data-ttu-id="a82d3-165">Utilisez Aes256 pour le chiffrement du message, Sha256 pour le résumé du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-165">Use Aes256 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="a82d3-166">TripleDesSha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="a82d3-166">TripleDesSha256Rsa15</span></span>|<span data-ttu-id="a82d3-167">Utilisez TripleDes pour le chiffrement du message, Sha256 pour le condensat du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="a82d3-167">Use TripleDes for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a82d3-168">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a82d3-168">Child Elements</span></span>  
  
|<span data-ttu-id="a82d3-169">Élément</span><span class="sxs-lookup"><span data-stu-id="a82d3-169">Element</span></span>|<span data-ttu-id="a82d3-170">Description</span><span class="sxs-lookup"><span data-stu-id="a82d3-170">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a82d3-171">\<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="a82d3-171">\<claimTypeRequirements></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/claimtyperequirements-element.md)|<span data-ttu-id="a82d3-172">Spécifie une collection de types de revendication pour cette liaison.</span><span class="sxs-lookup"><span data-stu-id="a82d3-172">Specifies a collection of claim types for this binding.</span></span> <span data-ttu-id="a82d3-173">Chaque élément est de type <xref:System.ServiceModel.Configuration.ClaimTypeElement>.</span><span class="sxs-lookup"><span data-stu-id="a82d3-173">Each element is of type <xref:System.ServiceModel.Configuration.ClaimTypeElement>.</span></span>|  
|[<span data-ttu-id="a82d3-174">\<issuer></span><span class="sxs-lookup"><span data-stu-id="a82d3-174">\<issuer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuer.md)|<span data-ttu-id="a82d3-175">Spécifie un point de terminaison qui publie un jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a82d3-175">Specifies an endpoint that issues a security token.</span></span> <span data-ttu-id="a82d3-176">Cet élément est de type <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>.</span><span class="sxs-lookup"><span data-stu-id="a82d3-176">This element is of type <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>.</span></span>|  
|[<span data-ttu-id="a82d3-177">\<issuerMetadata></span><span class="sxs-lookup"><span data-stu-id="a82d3-177">\<issuerMetadata></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuermetadata.md)|<span data-ttu-id="a82d3-178">Spécifie l'adresse de point de terminaison de l'émetteur.</span><span class="sxs-lookup"><span data-stu-id="a82d3-178">Specifies the endpoint address of the issuer.</span></span>|  
|[<span data-ttu-id="a82d3-179">\<tokenRequestParameters></span><span class="sxs-lookup"><span data-stu-id="a82d3-179">\<tokenRequestParameters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/tokenrequestparameters.md)|<span data-ttu-id="a82d3-180">Collection de paramètres de demande de jeton.</span><span class="sxs-lookup"><span data-stu-id="a82d3-180">A collection of token request parameters.</span></span> <span data-ttu-id="a82d3-181">Chaque paramètre est un élément XML.</span><span class="sxs-lookup"><span data-stu-id="a82d3-181">Each parameter is an XML element.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a82d3-182">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a82d3-182">Parent Elements</span></span>  
  
|<span data-ttu-id="a82d3-183">Élément</span><span class="sxs-lookup"><span data-stu-id="a82d3-183">Element</span></span>|<span data-ttu-id="a82d3-184">Description</span><span class="sxs-lookup"><span data-stu-id="a82d3-184">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a82d3-185">\<security></span><span class="sxs-lookup"><span data-stu-id="a82d3-185">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-element-of-ws2007federationhttpbinding.md)|<span data-ttu-id="a82d3-186">Définit les paramètres de sécurité d’une liaison.</span><span class="sxs-lookup"><span data-stu-id="a82d3-186">Defines the security settings for a binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a82d3-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a82d3-187">See also</span></span>
- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp>
- <xref:System.ServiceModel.Configuration.WSFederationHttpSecurityElement.Message%2A>
- <xref:System.ServiceModel.WSFederationHttpSecurity.Message%2A>
 `System.ServiceModel.Configuration.FederatedMessageSecurityElement` 
- [<span data-ttu-id="a82d3-188">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="a82d3-188">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="a82d3-189">Liaisons</span><span class="sxs-lookup"><span data-stu-id="a82d3-189">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="a82d3-190">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="a82d3-190">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="a82d3-191">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="a82d3-191">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="a82d3-192">\<binding></span><span class="sxs-lookup"><span data-stu-id="a82d3-192">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
