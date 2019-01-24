---
title: '&lt;add&gt; de &lt;issuerChannelBehaviors&gt;'
ms.date: 03/30/2017
ms.assetid: 50710506-e28f-45dd-ab7e-bff6f44173db
ms.openlocfilehash: e0f49f71a3f9649492b3ad7ccf263114957ee4e3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54729929"
---
# <a name="ltaddgt-of-ltissuerchannelbehaviorsgt"></a><span data-ttu-id="c264c-102">&lt;add&gt; de &lt;issuerChannelBehaviors&gt;</span><span class="sxs-lookup"><span data-stu-id="c264c-102">&lt;add&gt; of &lt;issuerChannelBehaviors&gt;</span></span>
<span data-ttu-id="c264c-103">Ajoute un comportement de point de terminaison à utiliser lors de la communication avec un service STS.</span><span class="sxs-lookup"><span data-stu-id="c264c-103">Adds an endpoint behavior to be used when communicating with an STS.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c264c-104">Si un comportement de point de terminaison contient un [ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) élément, une exception sera levée.</span><span class="sxs-lookup"><span data-stu-id="c264c-104">If any endpoint behavior contains a [\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) element, an exception will be thrown.</span></span>  
  
 <span data-ttu-id="c264c-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="c264c-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="c264c-106">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="c264c-106">\<behaviors></span></span>  
<span data-ttu-id="c264c-107">section d’endpointBehaviors</span><span class="sxs-lookup"><span data-stu-id="c264c-107">endpointBehaviors section</span></span>  
<span data-ttu-id="c264c-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="c264c-108">\<behavior></span></span>  
<span data-ttu-id="c264c-109">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="c264c-109">\<clientCredentials></span></span>  
<span data-ttu-id="c264c-110">\<issuedToken></span><span class="sxs-lookup"><span data-stu-id="c264c-110">\<issuedToken></span></span>  
<span data-ttu-id="c264c-111">\<issuerChannelBehaviors > élément</span><span class="sxs-lookup"><span data-stu-id="c264c-111">\<issuerChannelBehaviors> Element</span></span>  
<span data-ttu-id="c264c-112">\<add></span><span class="sxs-lookup"><span data-stu-id="c264c-112">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c264c-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c264c-113">Syntax</span></span>  
  
```xml  
<add issuerAddress="string"
     behaviorConfiguraton="string" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c264c-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c264c-114">Attributes and Elements</span></span>  
 <span data-ttu-id="c264c-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c264c-115">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c264c-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="c264c-116">Attributes</span></span>  
  
|<span data-ttu-id="c264c-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="c264c-117">Attribute</span></span>|<span data-ttu-id="c264c-118">Description</span><span class="sxs-lookup"><span data-stu-id="c264c-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c264c-119">issuerAddress</span><span class="sxs-lookup"><span data-stu-id="c264c-119">issuerAddress</span></span>|<span data-ttu-id="c264c-120">URI de l'émetteur de jeton de sécurité avec lequel communiquer.</span><span class="sxs-lookup"><span data-stu-id="c264c-120">The URI of the security token issuer to communicate with.</span></span>|  
|<span data-ttu-id="c264c-121">behaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="c264c-121">behaviorConfiguration</span></span>|<span data-ttu-id="c264c-122">Nom d'un comportement de point de terminaison défini dans le même fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="c264c-122">The name of an endpoint behavior defined in the same configuration file.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c264c-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c264c-123">Child Elements</span></span>  
 <span data-ttu-id="c264c-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c264c-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c264c-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c264c-125">Parent Elements</span></span>  
  
|<span data-ttu-id="c264c-126">Élément</span><span class="sxs-lookup"><span data-stu-id="c264c-126">Element</span></span>|<span data-ttu-id="c264c-127">Description</span><span class="sxs-lookup"><span data-stu-id="c264c-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c264c-128">\<issuerChannelBehaviors></span><span class="sxs-lookup"><span data-stu-id="c264c-128">\<issuerChannelBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)|<span data-ttu-id="c264c-129">Contient une collection de comportements de point de terminaison de client Windows Communication Foundation (WCF) à utiliser lors de la communication avec les Services de jeton spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c264c-129">Contains a collection of Windows Communication Foundation (WCF) client endpoint behaviors to be used when communicating with the specified Service Token Services.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c264c-130">Notes</span><span class="sxs-lookup"><span data-stu-id="c264c-130">Remarks</span></span>  
 <span data-ttu-id="c264c-131">`issuerAddress` contient l'URI du service d'émission de jeton de sécurité avec lequel le client souhaite communiquer.</span><span class="sxs-lookup"><span data-stu-id="c264c-131">`issuerAddress` contains the URI of the Security Token Service that the client wants to communicate with.</span></span> <span data-ttu-id="c264c-132">`behaviorConfiguration` pointe vers un comportement de point de terminaison que l’application utilise dans les canaux créés par Windows Communication Foundation (WCF) pour obtenir les jetons émis à partir des Services de jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c264c-132">`behaviorConfiguration` points to an endpoint behavior that the application uses in the channels created by Windows Communication Foundation (WCF) to get the issued tokens from the Security Token Services.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c264c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c264c-133">See also</span></span>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.IssuerChannelBehaviors%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElement>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElementCollection>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential.IssuerChannelBehaviors%2A>
- [<span data-ttu-id="c264c-134">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="c264c-134">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="c264c-135">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="c264c-135">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="c264c-136">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="c264c-136">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="c264c-137">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="c264c-137">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="c264c-138">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="c264c-138">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- [<span data-ttu-id="c264c-139">Guide pratique pour Créer un Client fédéré</span><span class="sxs-lookup"><span data-stu-id="c264c-139">How to: Create a Federated Client</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="c264c-140">Guide pratique pour Configurer un émetteur Local</span><span class="sxs-lookup"><span data-stu-id="c264c-140">How to: Configure a Local Issuer</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)
- [<span data-ttu-id="c264c-141">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="c264c-141">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="c264c-142">\<issuerChannelBehaviors></span><span class="sxs-lookup"><span data-stu-id="c264c-142">\<issuerChannelBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)
