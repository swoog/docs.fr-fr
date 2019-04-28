---
title: <issuedToken>
ms.date: 03/30/2017
ms.assetid: b6eae4b7-a6cd-4e1a-b0f6-f407022550b0
ms.openlocfilehash: 83061b283c9430af7bcda9cbc832811fa805ed4c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61756284"
---
# <a name="issuedtoken"></a><span data-ttu-id="784d4-101">\<issuedToken></span><span class="sxs-lookup"><span data-stu-id="784d4-101">\<issuedToken></span></span>
<span data-ttu-id="784d4-102">Spécifie un jeton personnalisé utilisé pour authentifier un client auprès d'un service.</span><span class="sxs-lookup"><span data-stu-id="784d4-102">Specifies a custom token used to authenticate a client to a service.</span></span>  
  
 <span data-ttu-id="784d4-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="784d4-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="784d4-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="784d4-104">\<behaviors></span></span>  
<span data-ttu-id="784d4-105">section d’endpointBehaviors</span><span class="sxs-lookup"><span data-stu-id="784d4-105">endpointBehaviors section</span></span>  
<span data-ttu-id="784d4-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="784d4-106">\<behavior></span></span>  
<span data-ttu-id="784d4-107">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="784d4-107">\<clientCredentials></span></span>  
<span data-ttu-id="784d4-108">\<issuedToken></span><span class="sxs-lookup"><span data-stu-id="784d4-108">\<issuedToken></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="784d4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="784d4-109">Syntax</span></span>  
  
```xml  
<issuedToken cacheIssuedTokens="Boolean"
             defaultKeyEntropyMode="ClientEntropy/ServerEntropy/CombinedEntropy"
             issuedTokenRenewalThresholdPercentage = "0 to 100"
             issuerChannelBehaviors="String"
             localIssuerChannelBehaviors="String"
             maxIssuedTokenCachingTime="TimeSpan">
</issuedToken>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="784d4-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="784d4-110">Attributes and Elements</span></span>  
 <span data-ttu-id="784d4-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="784d4-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="784d4-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="784d4-112">Attributes</span></span>  
  
|<span data-ttu-id="784d4-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="784d4-113">Attribute</span></span>|<span data-ttu-id="784d4-114">Description</span><span class="sxs-lookup"><span data-stu-id="784d4-114">Description</span></span>|  
|---------------|-----------------|  
|`cacheIssuedTokens`|<span data-ttu-id="784d4-115">Attribut booléen facultatif indiquant si les jetons sont mis en cache.</span><span class="sxs-lookup"><span data-stu-id="784d4-115">Optional Boolean attribute that specifies whether tokens are cached.</span></span> <span data-ttu-id="784d4-116">La valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="784d4-116">The default is `true`.</span></span>|  
|`defaultKeyEntropyMode`|<span data-ttu-id="784d4-117">Attribut de chaîne facultatif qui spécifie les valeurs aléatoires (entropies) utilisées pour les opérations de protocole de transfert.</span><span class="sxs-lookup"><span data-stu-id="784d4-117">Optional string attribute that specifies which random values (entropies) are used for handshake operations.</span></span> <span data-ttu-id="784d4-118">Les valeurs comprennent `ClientEntropy`, `ServerEntropy` et `CombinedEntropy`. La valeur par défaut est `CombinedEntropy`.</span><span class="sxs-lookup"><span data-stu-id="784d4-118">Values include `ClientEntropy`, `ServerEntropy`, and `CombinedEntropy`, The default is `CombinedEntropy`.</span></span> <span data-ttu-id="784d4-119">Cet attribut est de type <xref:System.ServiceModel.Security.SecurityKeyEntropyMode>.</span><span class="sxs-lookup"><span data-stu-id="784d4-119">This attribute is of type <xref:System.ServiceModel.Security.SecurityKeyEntropyMode>.</span></span>|  
|`issuedTokenRenewalThresholdPercentage`|<span data-ttu-id="784d4-120">Attribut entier facultatif indiquant le pourcentage d'un délai valide (fourni par l'émetteur du jeton) pouvant s'écouler avant le renouvellement d'un jeton.</span><span class="sxs-lookup"><span data-stu-id="784d4-120">Optional integer attribute that specifies the percentage of a valid time frame (supplied by the token issuer) that can pass before a token is renewed.</span></span> <span data-ttu-id="784d4-121">Les valeurs sont comprises entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="784d4-121">Values are from 0 to 100.</span></span> <span data-ttu-id="784d4-122">La valeur par défaut est 60, c'est-à-dire que 60 % du délai s'écoule avant la tentative de renouvellement.</span><span class="sxs-lookup"><span data-stu-id="784d4-122">The default is 60, which specifies 60% of the time passes before a renewal is attempted.</span></span>|  
|`issuerChannelBehaviors`|<span data-ttu-id="784d4-123">Attribut facultatif indiquant les comportements de canal à utiliser lors d'une communication avec l'émetteur.</span><span class="sxs-lookup"><span data-stu-id="784d4-123">Optional attribute that specifies the channel behaviors to use when communicating with the issuer.</span></span>|  
|`localIssuerChannelBehaviors`|<span data-ttu-id="784d4-124">Attribut facultatif indiquant les comportements de canal à utiliser lors d'une communication avec l'émetteur local.</span><span class="sxs-lookup"><span data-stu-id="784d4-124">Optional attribute that specifies the channel behaviors to use when communicating with the local issuer.</span></span>|  
|`maxIssuedTokenCachingTime`|<span data-ttu-id="784d4-125">Attribut Timespan facultatif indiquant la durée de mise en cache des jetons émis lorsque l'émetteur de jeton (un STS) ne spécifie aucune durée.</span><span class="sxs-lookup"><span data-stu-id="784d4-125">Optional Timespan attribute that specifies the duration that issued tokens are cached when the token issuer (an STS) does not specify a time.</span></span> <span data-ttu-id="784d4-126">La valeur par défaut est « 10675199.02:48:05.4775807 ».</span><span class="sxs-lookup"><span data-stu-id="784d4-126">The default is "10675199.02:48:05.4775807."</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="784d4-127">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="784d4-127">Child Elements</span></span>  
  
|<span data-ttu-id="784d4-128">Élément</span><span class="sxs-lookup"><span data-stu-id="784d4-128">Element</span></span>|<span data-ttu-id="784d4-129">Description</span><span class="sxs-lookup"><span data-stu-id="784d4-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="784d4-130">\<localIssuer></span><span class="sxs-lookup"><span data-stu-id="784d4-130">\<localIssuer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/localissuer.md)|<span data-ttu-id="784d4-131">Spécifie l’adresse de l’émetteur local du jeton et la liaison utilisée pour communiquer avec le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="784d4-131">Specifies the address of the local issuer of the token and the binding used to communicate with the endpoint.</span></span>|  
|[<span data-ttu-id="784d4-132">\<issuerChannelBehaviors></span><span class="sxs-lookup"><span data-stu-id="784d4-132">\<issuerChannelBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)|<span data-ttu-id="784d4-133">Spécifie les comportements de point de terminaison à utiliser lors d'une communication avec un émetteur local.</span><span class="sxs-lookup"><span data-stu-id="784d4-133">Specifies the endpoint behaviors to use when contacting a local issuer.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="784d4-134">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="784d4-134">Parent Elements</span></span>  
  
|<span data-ttu-id="784d4-135">Élément</span><span class="sxs-lookup"><span data-stu-id="784d4-135">Element</span></span>|<span data-ttu-id="784d4-136">Description</span><span class="sxs-lookup"><span data-stu-id="784d4-136">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="784d4-137">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="784d4-137">\<clientCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|<span data-ttu-id="784d4-138">Spécifie les informations d'identification utilisées pour authentifier un client auprès d'un service.</span><span class="sxs-lookup"><span data-stu-id="784d4-138">Specifies the credentials used to authenticate a client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="784d4-139">Notes</span><span class="sxs-lookup"><span data-stu-id="784d4-139">Remarks</span></span>  
 <span data-ttu-id="784d4-140">Un jeton émis est un type d'informations d'identification personnalisé utilisé, par exemple, lors d'une authentification à l'aide d'un service STS dans un scénario fédéré.</span><span class="sxs-lookup"><span data-stu-id="784d4-140">An issued token is a custom credential type used, for example, when authenticating with a Secure Token Service (STS) in a federated scenario.</span></span> <span data-ttu-id="784d4-141">Par défaut, le jeton est un jeton SAML.</span><span class="sxs-lookup"><span data-stu-id="784d4-141">By default, the token is a SAML token.</span></span> <span data-ttu-id="784d4-142">Pour plus d’informations, consultez [fédération et jetons émis](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md).</span><span class="sxs-lookup"><span data-stu-id="784d4-142">For more information, see [Federation and Issued Tokens](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md).</span></span> <span data-ttu-id="784d4-143">et [fédération et jetons émis](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md).</span><span class="sxs-lookup"><span data-stu-id="784d4-143">and [Federation and Issued Tokens](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md).</span></span>  
  
 <span data-ttu-id="784d4-144">Cette section contient les éléments permettant de configurer un émetteur local de jetons ou les comportements utilisés avec un service d'émission de jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="784d4-144">This section contains the elements used to configure a local issuer of tokens, or behaviors used with an security token service.</span></span> <span data-ttu-id="784d4-145">Pour obtenir des instructions sur la configuration d’un client à utiliser un émetteur local, consultez [Comment : Configurer un émetteur Local](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md).</span><span class="sxs-lookup"><span data-stu-id="784d4-145">For instructions on configuring a client to use a local issuer, see [How to: Configure a Local Issuer](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="784d4-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="784d4-146">See also</span></span>

- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.IssuedToken%2A>
- <xref:System.ServiceModel.Description.ClientCredentials.IssuedToken%2A>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential>
- [<span data-ttu-id="784d4-147">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="784d4-147">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="784d4-148">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="784d4-148">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="784d4-149">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="784d4-149">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="784d4-150">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="784d4-150">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- [<span data-ttu-id="784d4-151">Guide pratique pour Créer un Client fédéré</span><span class="sxs-lookup"><span data-stu-id="784d4-151">How to: Create a Federated Client</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="784d4-152">Guide pratique pour Configurer un émetteur Local</span><span class="sxs-lookup"><span data-stu-id="784d4-152">How to: Configure a Local Issuer</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)
- [<span data-ttu-id="784d4-153">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="784d4-153">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
