---
title: <issuerMetadata> de <issuedTokenParameters>
ms.date: 03/30/2017
ms.assetid: 1a85ca37-496d-4fa3-8d44-d6c9383d735c
ms.openlocfilehash: 2697d24a731dbf8de3d68bcce7fd52c55ff6dc68
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55276976"
---
# <a name="issuermetadata-of-issuedtokenparameters"></a><span data-ttu-id="49f4d-102">\<issuerMetadata> of \<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="49f4d-102">\<issuerMetadata> of \<issuedTokenParameters></span></span>
<span data-ttu-id="49f4d-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="49f4d-103">\<system.serviceModel></span></span>  
<span data-ttu-id="49f4d-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="49f4d-104">\<bindings></span></span>  
<span data-ttu-id="49f4d-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="49f4d-105">\<customBinding></span></span>  
<span data-ttu-id="49f4d-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="49f4d-106">\<binding></span></span>  
<span data-ttu-id="49f4d-107">\<security></span><span class="sxs-lookup"><span data-stu-id="49f4d-107">\<security></span></span>  
<span data-ttu-id="49f4d-108">\<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="49f4d-108">\<issuedTokenParameters></span></span>  
<span data-ttu-id="49f4d-109">\<issuerMetadata></span><span class="sxs-lookup"><span data-stu-id="49f4d-109">\<issuerMetadata></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="49f4d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49f4d-110">Syntax</span></span>  
  
```xml  
<issuerMetaData address="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="49f4d-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="49f4d-111">Attributes and Elements</span></span>  
 <span data-ttu-id="49f4d-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="49f4d-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="49f4d-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="49f4d-113">Attributes</span></span>  
  
|<span data-ttu-id="49f4d-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="49f4d-114">Attribute</span></span>|<span data-ttu-id="49f4d-115">Description</span><span class="sxs-lookup"><span data-stu-id="49f4d-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="49f4d-116">address</span><span class="sxs-lookup"><span data-stu-id="49f4d-116">address</span></span>|<span data-ttu-id="49f4d-117">Requis.</span><span class="sxs-lookup"><span data-stu-id="49f4d-117">Required.</span></span> <span data-ttu-id="49f4d-118">Chaîne qui spécifie l'adresse du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="49f4d-118">A string that specifies the address of the endpoint.</span></span> <span data-ttu-id="49f4d-119">L'adresse doit être un URI absolu.</span><span class="sxs-lookup"><span data-stu-id="49f4d-119">The address must be an absolute URI.</span></span> <span data-ttu-id="49f4d-120">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="49f4d-120">The default value is an empty string.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="49f4d-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="49f4d-121">Child Elements</span></span>  
  
|<span data-ttu-id="49f4d-122">Élément</span><span class="sxs-lookup"><span data-stu-id="49f4d-122">Element</span></span>|<span data-ttu-id="49f4d-123">Description</span><span class="sxs-lookup"><span data-stu-id="49f4d-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="49f4d-124">\<headers></span><span class="sxs-lookup"><span data-stu-id="49f4d-124">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="49f4d-125">Collection d'en-têtes d'adresses.</span><span class="sxs-lookup"><span data-stu-id="49f4d-125">A collection of address headers.</span></span>|  
|[<span data-ttu-id="49f4d-126">\<identity></span><span class="sxs-lookup"><span data-stu-id="49f4d-126">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="49f4d-127">Identité qui permet l'authentification d'un point de terminaison par les autres points de terminaison qui échangent des messages avec lui.</span><span class="sxs-lookup"><span data-stu-id="49f4d-127">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="49f4d-128">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="49f4d-128">Parent Elements</span></span>  
  
|<span data-ttu-id="49f4d-129">Élément</span><span class="sxs-lookup"><span data-stu-id="49f4d-129">Element</span></span>|<span data-ttu-id="49f4d-130">Description</span><span class="sxs-lookup"><span data-stu-id="49f4d-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="49f4d-131">\<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="49f4d-131">\<issuedTokenParameters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenparameters.md)|<span data-ttu-id="49f4d-132">Indique les paramètres d'un jeton de sécurité émis dans un scénario de sécurité fédéré.</span><span class="sxs-lookup"><span data-stu-id="49f4d-132">Specifies the parameters for an security token issued in a Federated security scenario.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="49f4d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49f4d-133">See also</span></span>
- <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="49f4d-134">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="49f4d-134">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="49f4d-135">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="49f4d-135">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="49f4d-136">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="49f4d-136">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="49f4d-137">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="49f4d-137">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="49f4d-138">Liaisons</span><span class="sxs-lookup"><span data-stu-id="49f4d-138">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="49f4d-139">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="49f4d-139">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="49f4d-140">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="49f4d-140">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="49f4d-141">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="49f4d-141">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
- [<span data-ttu-id="49f4d-142">Guide pratique pour Créer une liaison personnalisée à l’aide de SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="49f4d-142">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [<span data-ttu-id="49f4d-143">Sécurité de liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="49f4d-143">Custom Binding Security</span></span>](../../../../../docs/framework/wcf/samples/custom-binding-security.md)
