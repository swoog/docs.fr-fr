---
title: <issuedTokenParameters>
ms.date: 03/30/2017
ms.assetid: 120b3f37-7331-4816-b712-d6aab39655a4
ms.openlocfilehash: 6bdf56e3d2084dec8d44e1c4d3f0c1e50b711b92
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59153138"
---
# <a name="issuedtokenparameters"></a><span data-ttu-id="914e8-101">\<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="914e8-101">\<issuedTokenParameters></span></span>
<span data-ttu-id="914e8-102">Indique les paramètres d'un jeton de sécurité émis dans un scénario de sécurité fédéré.</span><span class="sxs-lookup"><span data-stu-id="914e8-102">Specifies the parameters for a security token issued in a Federated security scenario.</span></span>  
  
 <span data-ttu-id="914e8-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="914e8-103">\<system.serviceModel></span></span>  
<span data-ttu-id="914e8-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="914e8-104">\<bindings></span></span>  
<span data-ttu-id="914e8-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="914e8-105">\<customBinding></span></span>  
<span data-ttu-id="914e8-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="914e8-106">\<binding></span></span>  
<span data-ttu-id="914e8-107">\<security></span><span class="sxs-lookup"><span data-stu-id="914e8-107">\<security></span></span>  
<span data-ttu-id="914e8-108">\<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="914e8-108">\<issuedTokenParameters></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="914e8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="914e8-109">Syntax</span></span>  
  
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
  
## <a name="type"></a><span data-ttu-id="914e8-110">Type</span><span class="sxs-lookup"><span data-stu-id="914e8-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="914e8-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="914e8-111">Attributes and Elements</span></span>  
 <span data-ttu-id="914e8-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="914e8-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="914e8-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="914e8-113">Attributes</span></span>  
  
|<span data-ttu-id="914e8-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="914e8-114">Attribute</span></span>|<span data-ttu-id="914e8-115">Description</span><span class="sxs-lookup"><span data-stu-id="914e8-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="914e8-116">defaultMessageSecurityVersion</span><span class="sxs-lookup"><span data-stu-id="914e8-116">defaultMessageSecurityVersion</span></span>|<span data-ttu-id="914e8-117">Spécifie les versions des caractéristiques de sécurité (WS-Security, WS-Trust, WS-Secure Conversation et WS-Security Policy) devant être prises en charge par la liaison.</span><span class="sxs-lookup"><span data-stu-id="914e8-117">Specifies the versions of the security specifications, (WS-Security, WS-Trust, WS-Secure Conversation and WS-Security Policy) that must be supported by the binding.</span></span> <span data-ttu-id="914e8-118">Cette valeur est de type <xref:System.ServiceModel.MessageSecurityVersion>.</span><span class="sxs-lookup"><span data-stu-id="914e8-118">This value is of type <xref:System.ServiceModel.MessageSecurityVersion>.</span></span>|  
|<span data-ttu-id="914e8-119">inclusionMode</span><span class="sxs-lookup"><span data-stu-id="914e8-119">inclusionMode</span></span>|<span data-ttu-id="914e8-120">Indique les spécifications d'inclusion de jeton.</span><span class="sxs-lookup"><span data-stu-id="914e8-120">Specifies the token inclusion requirements.</span></span> <span data-ttu-id="914e8-121">Cet attribut est de type <xref:System.ServiceModel.Security.Tokens.SecurityTokenInclusionMode>.</span><span class="sxs-lookup"><span data-stu-id="914e8-121">This attribute is of type <xref:System.ServiceModel.Security.Tokens.SecurityTokenInclusionMode>.</span></span>|  
|<span data-ttu-id="914e8-122">keySize</span><span class="sxs-lookup"><span data-stu-id="914e8-122">keySize</span></span>|<span data-ttu-id="914e8-123">Entier qui spécifie la taille de clé de jeton.</span><span class="sxs-lookup"><span data-stu-id="914e8-123">An integer that specifies the token key size.</span></span> <span data-ttu-id="914e8-124">La valeur par défaut est 256.</span><span class="sxs-lookup"><span data-stu-id="914e8-124">The default value is 256.</span></span>|  
|<span data-ttu-id="914e8-125">keyType</span><span class="sxs-lookup"><span data-stu-id="914e8-125">keyType</span></span>|<span data-ttu-id="914e8-126">Valeur correcte de <xref:System.IdentityModel.Tokens.SecurityKeyType> indiquant le type de clé.</span><span class="sxs-lookup"><span data-stu-id="914e8-126">A valid value of <xref:System.IdentityModel.Tokens.SecurityKeyType> that specifies the key type.</span></span> <span data-ttu-id="914e8-127">La valeur par défaut est `SymmetricKey`.</span><span class="sxs-lookup"><span data-stu-id="914e8-127">The default is `SymmetricKey`.</span></span>|  
|<span data-ttu-id="914e8-128">tokenType</span><span class="sxs-lookup"><span data-stu-id="914e8-128">tokenType</span></span>|<span data-ttu-id="914e8-129">Chaîne indiquant le type de jeton.</span><span class="sxs-lookup"><span data-stu-id="914e8-129">A string that specifies the token type.</span></span> <span data-ttu-id="914e8-130">La valeur par défaut est « http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAML »</span><span class="sxs-lookup"><span data-stu-id="914e8-130">The default is "http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAML".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="914e8-131">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="914e8-131">Child Elements</span></span>  
  
|<span data-ttu-id="914e8-132">Élément</span><span class="sxs-lookup"><span data-stu-id="914e8-132">Element</span></span>|<span data-ttu-id="914e8-133">Description</span><span class="sxs-lookup"><span data-stu-id="914e8-133">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="914e8-134">\<additionalRequestParameters></span><span class="sxs-lookup"><span data-stu-id="914e8-134">\<additionalRequestParameters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/additionalrequestparameters-element.md)|<span data-ttu-id="914e8-135">Collection d'éléments de configuration indiquant des paramètres de demande supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="914e8-135">A collection of configuration elements that specify additional request parameters.</span></span>|  
|[<span data-ttu-id="914e8-136">\<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="914e8-136">\<claimTypeRequirements></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/claimtyperequirements-element.md)|<span data-ttu-id="914e8-137">Spécifie une collection de types de revendications requis.</span><span class="sxs-lookup"><span data-stu-id="914e8-137">Specifies a collection of required claim types.</span></span><br /><br /> <span data-ttu-id="914e8-138">Dans un scénario fédéré, les services déclarent les spécifications relatives aux informations d'identification entrantes.</span><span class="sxs-lookup"><span data-stu-id="914e8-138">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="914e8-139">Par exemple, ces informations d'identification doivent posséder un jeu de types de revendications défini.</span><span class="sxs-lookup"><span data-stu-id="914e8-139">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="914e8-140">Chaque élément de la collection indique les types de revendications requis et facultatifs censés apparaître dans les informations d'identification fédérées.</span><span class="sxs-lookup"><span data-stu-id="914e8-140">Each element in this collection specifies the types of required and optional claims expected to appear in a federated credential.</span></span>|  
|[<span data-ttu-id="914e8-141">\<issuer></span><span class="sxs-lookup"><span data-stu-id="914e8-141">\<issuer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuer-of-issuedtokenparameters.md)|<span data-ttu-id="914e8-142">Élément de configuration qui spécifie le point de terminaison émettant le jeton actuel.</span><span class="sxs-lookup"><span data-stu-id="914e8-142">A configuration element that specifies the endpoint that issues the current token.</span></span>|  
|[<span data-ttu-id="914e8-143">\<issuerMetadata></span><span class="sxs-lookup"><span data-stu-id="914e8-143">\<issuerMetadata></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuermetadata-of-issuedtokenparameters.md)|<span data-ttu-id="914e8-144">Élément de configuration qui spécifie l'adresse de point de terminaison correspondant aux métadonnées de l'émetteur de jeton.</span><span class="sxs-lookup"><span data-stu-id="914e8-144">A configuration element that specifies the endpoint address of the token issuer's metadata.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="914e8-145">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="914e8-145">Parent Elements</span></span>  
  
|<span data-ttu-id="914e8-146">Élément</span><span class="sxs-lookup"><span data-stu-id="914e8-146">Element</span></span>|<span data-ttu-id="914e8-147">Description</span><span class="sxs-lookup"><span data-stu-id="914e8-147">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="914e8-148">\<secureConversationBootstrap></span><span class="sxs-lookup"><span data-stu-id="914e8-148">\<secureConversationBootstrap></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/secureconversationbootstrap.md)|<span data-ttu-id="914e8-149">Spécifie les valeurs par défaut utilisées pour initialiser un service de conversation sécurisé.</span><span class="sxs-lookup"><span data-stu-id="914e8-149">Specifies the default values used for initiating a secure conversation service.</span></span>|  
|[<span data-ttu-id="914e8-150">\<security></span><span class="sxs-lookup"><span data-stu-id="914e8-150">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-custombinding.md)|<span data-ttu-id="914e8-151">Spécifie les options de sécurité d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="914e8-151">Specifies the security options for a custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="914e8-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="914e8-152">See also</span></span>

- <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement>
- <xref:System.ServiceModel.Configuration.SecurityElementBase.IssuedTokenParameters%2A>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="914e8-153">Liaisons</span><span class="sxs-lookup"><span data-stu-id="914e8-153">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="914e8-154">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="914e8-154">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="914e8-155">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="914e8-155">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="914e8-156">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="914e8-156">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
- [<span data-ttu-id="914e8-157">Guide pratique pour Créer une liaison personnalisée à l’aide de SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="914e8-157">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [<span data-ttu-id="914e8-158">Sécurité de liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="914e8-158">Custom Binding Security</span></span>](../../../../../docs/framework/wcf/samples/custom-binding-security.md)
- [<span data-ttu-id="914e8-159">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="914e8-159">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="914e8-160">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="914e8-160">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="914e8-161">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="914e8-161">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="914e8-162">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="914e8-162">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
