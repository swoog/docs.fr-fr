---
title: <add> de <issuerChannelBehaviors>
ms.date: 03/30/2017
ms.assetid: 50710506-e28f-45dd-ab7e-bff6f44173db
ms.openlocfilehash: 5c9937cb6302a194228461f3e2e06ecdf4d43269
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57377753"
---
# <a name="add-of-issuerchannelbehaviors"></a><span data-ttu-id="1be2d-102">\<add> of \<issuerChannelBehaviors></span><span class="sxs-lookup"><span data-stu-id="1be2d-102">\<add> of \<issuerChannelBehaviors></span></span>

<span data-ttu-id="1be2d-103">Ajoute un comportement de point de terminaison à utiliser lors de la communication avec un service STS.</span><span class="sxs-lookup"><span data-stu-id="1be2d-103">Adds an endpoint behavior to be used when communicating with an STS.</span></span>

> [!NOTE]
> <span data-ttu-id="1be2d-104">Si un comportement de point de terminaison contient un [ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) élément, une exception sera levée.</span><span class="sxs-lookup"><span data-stu-id="1be2d-104">If any endpoint behavior contains a [\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) element, an exception will be thrown.</span></span>

<span data-ttu-id="1be2d-105">\<system.ServiceModel>\\</span><span class="sxs-lookup"><span data-stu-id="1be2d-105">\<system.ServiceModel>\\</span></span>
<span data-ttu-id="1be2d-106">\<behaviors>\\</span><span class="sxs-lookup"><span data-stu-id="1be2d-106">\<behaviors>\\</span></span>
<span data-ttu-id="1be2d-107">section d’endpointBehaviors \<comportement > \\</span><span class="sxs-lookup"><span data-stu-id="1be2d-107">endpointBehaviors section \<behavior>\\</span></span>
<span data-ttu-id="1be2d-108">\<clientCredentials>\\</span><span class="sxs-lookup"><span data-stu-id="1be2d-108">\<clientCredentials>\\</span></span>
<span data-ttu-id="1be2d-109">\<issuedToken>\\</span><span class="sxs-lookup"><span data-stu-id="1be2d-109">\<issuedToken>\\</span></span>
<span data-ttu-id="1be2d-110">\<issuerChannelBehaviors > Element\\</span><span class="sxs-lookup"><span data-stu-id="1be2d-110">\<issuerChannelBehaviors> Element\\</span></span>
<span data-ttu-id="1be2d-111">\<add></span><span class="sxs-lookup"><span data-stu-id="1be2d-111">\<add></span></span>

## <a name="syntax"></a><span data-ttu-id="1be2d-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1be2d-112">Syntax</span></span>

```xml
<add issuerAddress="string"
     behaviorConfiguration="string" />
```

## <a name="attributes-and-elements"></a><span data-ttu-id="1be2d-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1be2d-113">Attributes and Elements</span></span>

<span data-ttu-id="1be2d-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1be2d-114">The following sections describe attributes, child elements, and parent elements</span></span>

### <a name="attributes"></a><span data-ttu-id="1be2d-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="1be2d-115">Attributes</span></span>

|<span data-ttu-id="1be2d-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="1be2d-116">Attribute</span></span>|<span data-ttu-id="1be2d-117">Description</span><span class="sxs-lookup"><span data-stu-id="1be2d-117">Description</span></span>|
|---------------|-----------------|
|<span data-ttu-id="1be2d-118">issuerAddress</span><span class="sxs-lookup"><span data-stu-id="1be2d-118">issuerAddress</span></span>|<span data-ttu-id="1be2d-119">URI de l'émetteur de jeton de sécurité avec lequel communiquer.</span><span class="sxs-lookup"><span data-stu-id="1be2d-119">The URI of the security token issuer to communicate with.</span></span>|
|<span data-ttu-id="1be2d-120">behaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="1be2d-120">behaviorConfiguration</span></span>|<span data-ttu-id="1be2d-121">Nom d'un comportement de point de terminaison défini dans le même fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="1be2d-121">The name of an endpoint behavior defined in the same configuration file.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="1be2d-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1be2d-122">Child Elements</span></span>

<span data-ttu-id="1be2d-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1be2d-123">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="1be2d-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1be2d-124">Parent Elements</span></span>

|<span data-ttu-id="1be2d-125">Élément</span><span class="sxs-lookup"><span data-stu-id="1be2d-125">Element</span></span>|<span data-ttu-id="1be2d-126">Description</span><span class="sxs-lookup"><span data-stu-id="1be2d-126">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="1be2d-127">\<issuerChannelBehaviors></span><span class="sxs-lookup"><span data-stu-id="1be2d-127">\<issuerChannelBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)|<span data-ttu-id="1be2d-128">Contient une collection de comportements de point de terminaison de client Windows Communication Foundation (WCF) à utiliser lors de la communication avec les Services de jeton spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1be2d-128">Contains a collection of Windows Communication Foundation (WCF) client endpoint behaviors to be used when communicating with the specified Service Token Services.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1be2d-129">Notes</span><span class="sxs-lookup"><span data-stu-id="1be2d-129">Remarks</span></span>

<span data-ttu-id="1be2d-130">`issuerAddress` contient l'URI du service d'émission de jeton de sécurité avec lequel le client souhaite communiquer.</span><span class="sxs-lookup"><span data-stu-id="1be2d-130">`issuerAddress` contains the URI of the Security Token Service that the client wants to communicate with.</span></span> <span data-ttu-id="1be2d-131">`behaviorConfiguration` pointe vers un comportement de point de terminaison que l’application utilise dans les canaux créés par Windows Communication Foundation (WCF) pour obtenir les jetons émis à partir des Services de jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1be2d-131">`behaviorConfiguration` points to an endpoint behavior that the application uses in the channels created by Windows Communication Foundation (WCF) to get the issued tokens from the Security Token Services.</span></span>

## <a name="see-also"></a><span data-ttu-id="1be2d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1be2d-132">See also</span></span>

- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.IssuerChannelBehaviors%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElement>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElementCollection>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential.IssuerChannelBehaviors%2A>
- [<span data-ttu-id="1be2d-133">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="1be2d-133">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="1be2d-134">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="1be2d-134">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="1be2d-135">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="1be2d-135">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="1be2d-136">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="1be2d-136">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="1be2d-137">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="1be2d-137">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- [<span data-ttu-id="1be2d-138">Guide pratique pour Créer un Client fédéré</span><span class="sxs-lookup"><span data-stu-id="1be2d-138">How to: Create a Federated Client</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="1be2d-139">Guide pratique pour Configurer un émetteur Local</span><span class="sxs-lookup"><span data-stu-id="1be2d-139">How to: Configure a Local Issuer</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)
- [<span data-ttu-id="1be2d-140">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="1be2d-140">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="1be2d-141">\<issuerChannelBehaviors></span><span class="sxs-lookup"><span data-stu-id="1be2d-141">\<issuerChannelBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)
