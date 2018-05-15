---
title: '&lt;issuer&gt; de &lt;issuedTokenParameters&gt;'
ms.date: 03/30/2017
ms.assetid: d6a95f32-d58c-40fc-8658-dd92564d3c90
ms.openlocfilehash: 459f2f43d3ef9426fbce7e0a0dd067250eb2cc4b
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltissuergt-of-ltissuedtokenparametersgt"></a><span data-ttu-id="212a7-102">&lt;issuer&gt; de &lt;issuedTokenParameters&gt;</span><span class="sxs-lookup"><span data-stu-id="212a7-102">&lt;issuer&gt; of &lt;issuedTokenParameters&gt;</span></span>
<span data-ttu-id="212a7-103">Spécifie le service d'émission de jeton de sécurité (STS) qui émet des jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="212a7-103">Specifies the Security Token Service (STS) that issues security tokens.</span></span>  
  
 <span data-ttu-id="212a7-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="212a7-104">\<system.serviceModel></span></span>  
<span data-ttu-id="212a7-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="212a7-105">\<bindings></span></span>  
<span data-ttu-id="212a7-106">\<customBinding ></span><span class="sxs-lookup"><span data-stu-id="212a7-106">\<customBinding></span></span>  
<span data-ttu-id="212a7-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="212a7-107">\<binding></span></span>  
<span data-ttu-id="212a7-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="212a7-108">\<security></span></span>  
<span data-ttu-id="212a7-109">\<issuedTokenParameters ></span><span class="sxs-lookup"><span data-stu-id="212a7-109">\<issuedTokenParameters></span></span>  
<span data-ttu-id="212a7-110">\<l’émetteur ></span><span class="sxs-lookup"><span data-stu-id="212a7-110">\<issuer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="212a7-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="212a7-111">Syntax</span></span>  
  
```xml  
<issuer address="Uri" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="212a7-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="212a7-112">Attributes and Elements</span></span>  
 <span data-ttu-id="212a7-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="212a7-113">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="212a7-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="212a7-114">Attributes</span></span>  
  
|<span data-ttu-id="212a7-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="212a7-115">Attribute</span></span>|<span data-ttu-id="212a7-116">Description</span><span class="sxs-lookup"><span data-stu-id="212a7-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="212a7-117">address</span><span class="sxs-lookup"><span data-stu-id="212a7-117">address</span></span>|<span data-ttu-id="212a7-118">Chaîne requise.</span><span class="sxs-lookup"><span data-stu-id="212a7-118">Required string.</span></span> <span data-ttu-id="212a7-119">URL du service STS.</span><span class="sxs-lookup"><span data-stu-id="212a7-119">The URL of the STS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="212a7-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="212a7-120">Child Elements</span></span>  
  
|<span data-ttu-id="212a7-121">Élément</span><span class="sxs-lookup"><span data-stu-id="212a7-121">Element</span></span>|<span data-ttu-id="212a7-122">Description</span><span class="sxs-lookup"><span data-stu-id="212a7-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="212a7-123">\<en-têtes ></span><span class="sxs-lookup"><span data-stu-id="212a7-123">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="212a7-124">Collection d’en-têtes d’adresse de points de terminaison pouvant être créée par le générateur.</span><span class="sxs-lookup"><span data-stu-id="212a7-124">A collection of address headers for the endpoints that the builder can create.</span></span>|  
|[<span data-ttu-id="212a7-125">\<identité ></span><span class="sxs-lookup"><span data-stu-id="212a7-125">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="212a7-126">Lors de l'utilisation d'un jeton émis, spécifie des paramètres qui permettent au client d'authentifier le serveur.</span><span class="sxs-lookup"><span data-stu-id="212a7-126">When using an issued token, specifies settings that enable the client to authenticate the server.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="212a7-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="212a7-127">Parent Elements</span></span>  
  
|<span data-ttu-id="212a7-128">Élément</span><span class="sxs-lookup"><span data-stu-id="212a7-128">Element</span></span>|<span data-ttu-id="212a7-129">Description</span><span class="sxs-lookup"><span data-stu-id="212a7-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="212a7-130">\<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="212a7-130">\<issuedTokenParameters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenparameters.md)|<span data-ttu-id="212a7-131">Spécifie le jeton émis en cours.</span><span class="sxs-lookup"><span data-stu-id="212a7-131">Specifies the current issued token.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="212a7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="212a7-132">See Also</span></span>  
 <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters.AdditionalRequestParameters%2A>  
 <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement.AdditionalRequestParameters%2A>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="212a7-133">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="212a7-133">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="212a7-134">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="212a7-134">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="212a7-135">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="212a7-135">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)  
 [<span data-ttu-id="212a7-136">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="212a7-136">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="212a7-137">Liaisons</span><span class="sxs-lookup"><span data-stu-id="212a7-137">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="212a7-138">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="212a7-138">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="212a7-139">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="212a7-139">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="212a7-140">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="212a7-140">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)  
 [<span data-ttu-id="212a7-141">Guide pratique pour créer une liaison personnalisée à l’aide de SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="212a7-141">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)  
 [<span data-ttu-id="212a7-142">Sécurité de liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="212a7-142">Custom Binding Security</span></span>](../../../../../docs/framework/wcf/samples/custom-binding-security.md)
