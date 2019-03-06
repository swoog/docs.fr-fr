---
title: Élément <issuerChannelBehaviors>
ms.date: 03/30/2017
ms.assetid: f7378673-8e9b-45b2-98d1-cf5dccdd8c40
ms.openlocfilehash: 3386a287d577681b67bd3ad54a75b0276e29da1f
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57357246"
---
# <a name="issuerchannelbehaviors-element"></a><span data-ttu-id="bb14d-102">\<issuerChannelBehaviors > élément</span><span class="sxs-lookup"><span data-stu-id="bb14d-102">\<issuerChannelBehaviors> Element</span></span>

<span data-ttu-id="bb14d-103">Contient une collection de comportements de point de terminaison de client Windows Communication Foundation (WCF) (défini dans la configuration) à utiliser lors de la communication avec les Services de jeton spécifiés.</span><span class="sxs-lookup"><span data-stu-id="bb14d-103">Contains a collection of Windows Communication Foundation (WCF) client endpoint behaviors (defined in the configuration) to be used when communicating with the specified Service Token Services.</span></span> <span data-ttu-id="bb14d-104">Les comportements définis ne peut pas inclure les [ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) éléments.</span><span class="sxs-lookup"><span data-stu-id="bb14d-104">The defined behaviors cannot include any [\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) elements.</span></span>

<span data-ttu-id="bb14d-105">\<system.ServiceModel>\\</span><span class="sxs-lookup"><span data-stu-id="bb14d-105">\<system.ServiceModel>\\</span></span>
<span data-ttu-id="bb14d-106">\<behaviors>\\</span><span class="sxs-lookup"><span data-stu-id="bb14d-106">\<behaviors>\\</span></span>
<span data-ttu-id="bb14d-107">endpointBehaviors section\\</span><span class="sxs-lookup"><span data-stu-id="bb14d-107">endpointBehaviors section\\</span></span>
<span data-ttu-id="bb14d-108">\<behavior>\\</span><span class="sxs-lookup"><span data-stu-id="bb14d-108">\<behavior>\\</span></span>
<span data-ttu-id="bb14d-109">\<clientCredentials>\\</span><span class="sxs-lookup"><span data-stu-id="bb14d-109">\<clientCredentials>\\</span></span>
<span data-ttu-id="bb14d-110">\<issuedToken>\\</span><span class="sxs-lookup"><span data-stu-id="bb14d-110">\<issuedToken>\\</span></span>
<span data-ttu-id="bb14d-111">\<issuerChannelBehaviors></span><span class="sxs-lookup"><span data-stu-id="bb14d-111">\<issuerChannelBehaviors></span></span>

## <a name="syntax"></a><span data-ttu-id="bb14d-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb14d-112">Syntax</span></span>

```xml
<issuerChannelBehaviors>
  <add behaviorConfiguration="string"
       issuerAddress="string" />
</issuerChannelBehaviors>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="bb14d-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="bb14d-113">Attributes and Elements</span></span>

<span data-ttu-id="bb14d-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="bb14d-114">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="bb14d-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="bb14d-115">Attributes</span></span>

<span data-ttu-id="bb14d-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bb14d-116">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="bb14d-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bb14d-117">Child Elements</span></span>

|<span data-ttu-id="bb14d-118">Élément</span><span class="sxs-lookup"><span data-stu-id="bb14d-118">Element</span></span>|<span data-ttu-id="bb14d-119">Description</span><span class="sxs-lookup"><span data-stu-id="bb14d-119">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="bb14d-120">\<add></span><span class="sxs-lookup"><span data-stu-id="bb14d-120">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-issuerchannelbehaviors.md)|<span data-ttu-id="bb14d-121">Ajoute un comportement à la collection.</span><span class="sxs-lookup"><span data-stu-id="bb14d-121">Adds a behavior to the collection.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="bb14d-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bb14d-122">Parent Elements</span></span>

|<span data-ttu-id="bb14d-123">Élément</span><span class="sxs-lookup"><span data-stu-id="bb14d-123">Element</span></span>|<span data-ttu-id="bb14d-124">Description</span><span class="sxs-lookup"><span data-stu-id="bb14d-124">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="bb14d-125">\<issuedToken></span><span class="sxs-lookup"><span data-stu-id="bb14d-125">\<issuedToken></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtoken.md)|<span data-ttu-id="bb14d-126">Spécifie un jeton personnalisé utilisé pour authentifier un client auprès d'un service.</span><span class="sxs-lookup"><span data-stu-id="bb14d-126">Specifies a custom token used to authenticate a client to a service.</span></span>|

## <a name="remarks"></a><span data-ttu-id="bb14d-127">Notes</span><span class="sxs-lookup"><span data-stu-id="bb14d-127">Remarks</span></span>

<span data-ttu-id="bb14d-128">Utilisez cet élément lorsque des comportements (autres que ceux qui contiennent des éléments `<clientCredentials>`) doivent être utilisés pour communiquer avec un service.</span><span class="sxs-lookup"><span data-stu-id="bb14d-128">Use this element when any behaviors (other than behaviors that include `<clientCredentials>` elements) must be used to communicate with a service.</span></span> <span data-ttu-id="bb14d-129">Par exemple, si un [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) élément de comportement doit être inclus.</span><span class="sxs-lookup"><span data-stu-id="bb14d-129">For example, if a [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) behavior element must be included.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb14d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb14d-130">See also</span></span>

- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.IssuerChannelBehaviors%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElement>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElementCollection>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential.IssuerChannelBehaviors%2A>
- [<span data-ttu-id="bb14d-131">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="bb14d-131">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="bb14d-132">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="bb14d-132">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="bb14d-133">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="bb14d-133">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="bb14d-134">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="bb14d-134">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="bb14d-135">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="bb14d-135">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- [<span data-ttu-id="bb14d-136">Guide pratique pour Créer un Client fédéré</span><span class="sxs-lookup"><span data-stu-id="bb14d-136">How to: Create a Federated Client</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="bb14d-137">Guide pratique pour Configurer un émetteur Local</span><span class="sxs-lookup"><span data-stu-id="bb14d-137">How to: Configure a Local Issuer</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)
- [<span data-ttu-id="bb14d-138">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="bb14d-138">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
