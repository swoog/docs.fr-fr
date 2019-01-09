---
title: '&lt;issuedTokenParameters&gt;'
ms.date: 03/30/2017
ms.assetid: 120b3f37-7331-4816-b712-d6aab39655a4
ms.openlocfilehash: 2060f98e94cec9e656420ac073204a82bc592b92
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149239"
---
# <a name="ltissuedtokenparametersgt"></a><span data-ttu-id="0968d-102">&lt;issuedTokenParameters&gt;</span><span class="sxs-lookup"><span data-stu-id="0968d-102">&lt;issuedTokenParameters&gt;</span></span>
<span data-ttu-id="0968d-103">Indique les paramètres d'un jeton de sécurité émis dans un scénario de sécurité fédéré.</span><span class="sxs-lookup"><span data-stu-id="0968d-103">Specifies the parameters for a security token issued in a Federated security scenario.</span></span>  
  
 <span data-ttu-id="0968d-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="0968d-104">\<system.serviceModel></span></span>  
<span data-ttu-id="0968d-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="0968d-105">\<bindings></span></span>  
<span data-ttu-id="0968d-106">\<customBinding ></span><span class="sxs-lookup"><span data-stu-id="0968d-106">\<customBinding></span></span>  
<span data-ttu-id="0968d-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="0968d-107">\<binding></span></span>  
<span data-ttu-id="0968d-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="0968d-108">\<security></span></span>  
<span data-ttu-id="0968d-109">\<issuedTokenParameters ></span><span class="sxs-lookup"><span data-stu-id="0968d-109">\<issuedTokenParameters></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0968d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0968d-110">Syntax</span></span>  
  
```xml  
<issuedTokenParameters defaultMessageSecurityVersion="System.ServiceModel.MessageSecurityVersion"
                       inclusionMode="AlwaysToInitiator/AlwaysToRecipient/Never/Once"
                       keySize="Integer"
                       keyType="AsymmetricKey/BearerKey/SymmetricKey"
                       tokenType="String">
  <additionalRequestParameters />
  <claimTypeRequirements>
    <add claimType="URI"
         isOptional="Boolean" />
  </claimTypeRequirements>
  <issuer address="String"
          binding="" />
  <issuerMetadata address="String" />
</issuedTokenParameters>
```  
  
## <a name="type"></a><span data-ttu-id="0968d-111">Type</span><span class="sxs-lookup"><span data-stu-id="0968d-111">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0968d-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0968d-112">Attributes and Elements</span></span>  
 <span data-ttu-id="0968d-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0968d-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0968d-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="0968d-114">Attributes</span></span>  
  
|<span data-ttu-id="0968d-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="0968d-115">Attribute</span></span>|<span data-ttu-id="0968d-116">Description</span><span class="sxs-lookup"><span data-stu-id="0968d-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0968d-117">defaultMessageSecurityVersion</span><span class="sxs-lookup"><span data-stu-id="0968d-117">defaultMessageSecurityVersion</span></span>|<span data-ttu-id="0968d-118">Spécifie les versions des caractéristiques de sécurité (WS-Security, WS-Trust, WS-Secure Conversation et WS-Security Policy) devant être prises en charge par la liaison.</span><span class="sxs-lookup"><span data-stu-id="0968d-118">Specifies the versions of the security specifications, (WS-Security, WS-Trust, WS-Secure Conversation and WS-Security Policy) that must be supported by the binding.</span></span> <span data-ttu-id="0968d-119">Cette valeur est de type <xref:System.ServiceModel.MessageSecurityVersion>.</span><span class="sxs-lookup"><span data-stu-id="0968d-119">This value is of type <xref:System.ServiceModel.MessageSecurityVersion>.</span></span>|  
|<span data-ttu-id="0968d-120">inclusionMode</span><span class="sxs-lookup"><span data-stu-id="0968d-120">inclusionMode</span></span>|<span data-ttu-id="0968d-121">Indique les spécifications d'inclusion de jeton.</span><span class="sxs-lookup"><span data-stu-id="0968d-121">Specifies the token inclusion requirements.</span></span> <span data-ttu-id="0968d-122">Cet attribut est de type <xref:System.ServiceModel.Security.Tokens.SecurityTokenInclusionMode>.</span><span class="sxs-lookup"><span data-stu-id="0968d-122">This attribute is of type <xref:System.ServiceModel.Security.Tokens.SecurityTokenInclusionMode>.</span></span>|  
|<span data-ttu-id="0968d-123">keySize</span><span class="sxs-lookup"><span data-stu-id="0968d-123">keySize</span></span>|<span data-ttu-id="0968d-124">Entier qui spécifie la taille de clé de jeton.</span><span class="sxs-lookup"><span data-stu-id="0968d-124">An integer that specifies the token key size.</span></span> <span data-ttu-id="0968d-125">La valeur par défaut est 256.</span><span class="sxs-lookup"><span data-stu-id="0968d-125">The default value is 256.</span></span>|  
|<span data-ttu-id="0968d-126">keyType</span><span class="sxs-lookup"><span data-stu-id="0968d-126">keyType</span></span>|<span data-ttu-id="0968d-127">Valeur correcte de <xref:System.IdentityModel.Tokens.SecurityKeyType> indiquant le type de clé.</span><span class="sxs-lookup"><span data-stu-id="0968d-127">A valid value of <xref:System.IdentityModel.Tokens.SecurityKeyType> that specifies the key type.</span></span> <span data-ttu-id="0968d-128">La valeur par défaut est `SymmetricKey`.</span><span class="sxs-lookup"><span data-stu-id="0968d-128">The default is `SymmetricKey`.</span></span>|  
|<span data-ttu-id="0968d-129">tokenType</span><span class="sxs-lookup"><span data-stu-id="0968d-129">tokenType</span></span>|<span data-ttu-id="0968d-130">Chaîne indiquant le type de jeton.</span><span class="sxs-lookup"><span data-stu-id="0968d-130">A string that specifies the token type.</span></span> <span data-ttu-id="0968d-131">La valeur par défaut est « http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAML »</span><span class="sxs-lookup"><span data-stu-id="0968d-131">The default is "http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAML".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0968d-132">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0968d-132">Child Elements</span></span>  
  
|<span data-ttu-id="0968d-133">Élément</span><span class="sxs-lookup"><span data-stu-id="0968d-133">Element</span></span>|<span data-ttu-id="0968d-134">Description</span><span class="sxs-lookup"><span data-stu-id="0968d-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0968d-135">\<additionalRequestParameters ></span><span class="sxs-lookup"><span data-stu-id="0968d-135">\<additionalRequestParameters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/additionalrequestparameters-element.md)|<span data-ttu-id="0968d-136">Collection d’éléments de configuration indiquant des paramètres de demande supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0968d-136">A collection of configuration elements that specify additional request parameters.</span></span>|  
|[<span data-ttu-id="0968d-137">\<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="0968d-137">\<claimTypeRequirements></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/claimtyperequirements-element.md)|<span data-ttu-id="0968d-138">Spécifie une collection de types de revendications requis.</span><span class="sxs-lookup"><span data-stu-id="0968d-138">Specifies a collection of required claim types.</span></span><br /><br /> <span data-ttu-id="0968d-139">Dans un scénario fédéré, les services déclarent les spécifications relatives aux informations d'identification entrantes.</span><span class="sxs-lookup"><span data-stu-id="0968d-139">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="0968d-140">Par exemple, ces informations d'identification doivent posséder un jeu de types de revendications défini.</span><span class="sxs-lookup"><span data-stu-id="0968d-140">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="0968d-141">Chaque élément de la collection indique les types de revendications requis et facultatifs censés apparaître dans les informations d’identification fédérées.</span><span class="sxs-lookup"><span data-stu-id="0968d-141">Each element in this collection specifies the types of required and optional claims expected to appear in a federated credential.</span></span>|  
|[<span data-ttu-id="0968d-142">\<issuer></span><span class="sxs-lookup"><span data-stu-id="0968d-142">\<issuer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuer-of-issuedtokenparameters.md)|<span data-ttu-id="0968d-143">Élément de configuration qui spécifie le point de terminaison émettant le jeton actuel.</span><span class="sxs-lookup"><span data-stu-id="0968d-143">A configuration element that specifies the endpoint that issues the current token.</span></span>|  
|[<span data-ttu-id="0968d-144">\<issuerMetadata></span><span class="sxs-lookup"><span data-stu-id="0968d-144">\<issuerMetadata></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuermetadata-of-issuedtokenparameters.md)|<span data-ttu-id="0968d-145">Élément de configuration qui spécifie l'adresse de point de terminaison correspondant aux métadonnées de l'émetteur de jeton.</span><span class="sxs-lookup"><span data-stu-id="0968d-145">A configuration element that specifies the endpoint address of the token issuer's metadata.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0968d-146">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0968d-146">Parent Elements</span></span>  
  
|<span data-ttu-id="0968d-147">Élément</span><span class="sxs-lookup"><span data-stu-id="0968d-147">Element</span></span>|<span data-ttu-id="0968d-148">Description</span><span class="sxs-lookup"><span data-stu-id="0968d-148">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0968d-149">\<secureConversationBootstrap ></span><span class="sxs-lookup"><span data-stu-id="0968d-149">\<secureConversationBootstrap></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/secureconversationbootstrap.md)|<span data-ttu-id="0968d-150">Spécifie les valeurs par défaut utilisées pour initialiser un service de conversation sécurisé.</span><span class="sxs-lookup"><span data-stu-id="0968d-150">Specifies the default values used for initiating a secure conversation service.</span></span>|  
|[<span data-ttu-id="0968d-151">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="0968d-151">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-custombinding.md)|<span data-ttu-id="0968d-152">Spécifie les options de sécurité d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="0968d-152">Specifies the security options for a custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0968d-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0968d-153">See Also</span></span>  
 <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters>  
 <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement>  
 <xref:System.ServiceModel.Configuration.SecurityElementBase.IssuedTokenParameters%2A>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="0968d-154">Liaisons</span><span class="sxs-lookup"><span data-stu-id="0968d-154">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="0968d-155">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="0968d-155">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="0968d-156">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="0968d-156">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="0968d-157">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="0968d-157">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)  
 [<span data-ttu-id="0968d-158">Guide pratique pour Créer une liaison personnalisée à l’aide de SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="0968d-158">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)  
 [<span data-ttu-id="0968d-159">Sécurité de liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="0968d-159">Custom Binding Security</span></span>](../../../../../docs/framework/wcf/samples/custom-binding-security.md)  
 [<span data-ttu-id="0968d-160">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="0968d-160">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="0968d-161">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="0968d-161">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="0968d-162">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="0968d-162">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)  
 [<span data-ttu-id="0968d-163">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="0968d-163">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
