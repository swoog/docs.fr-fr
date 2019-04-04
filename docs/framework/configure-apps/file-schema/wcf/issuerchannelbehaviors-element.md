---
title: <issuerChannelBehaviors> Élément
ms.date: 03/30/2017
ms.assetid: f7378673-8e9b-45b2-98d1-cf5dccdd8c40
ms.openlocfilehash: 7cbd50daa82b0ca937a1bba93786545898b03c8b
ms.sourcegitcommit: 5c2176883dc3107445702724a7caa7ac2f6cb0d3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/03/2019
ms.locfileid: "58890473"
---
# <a name="issuerchannelbehaviors-element"></a><span data-ttu-id="a0bc0-102">\<issuerChannelBehaviors > élément</span><span class="sxs-lookup"><span data-stu-id="a0bc0-102">\<issuerChannelBehaviors> Element</span></span>

<span data-ttu-id="a0bc0-103">Contient une collection de comportements de point de terminaison de client Windows Communication Foundation (WCF) (défini dans la configuration) à utiliser lors de la communication avec les Services de jeton spécifiés.</span><span class="sxs-lookup"><span data-stu-id="a0bc0-103">Contains a collection of Windows Communication Foundation (WCF) client endpoint behaviors (defined in the configuration) to be used when communicating with the specified Service Token Services.</span></span> <span data-ttu-id="a0bc0-104">Les comportements définis ne peut pas inclure les [ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) éléments.</span><span class="sxs-lookup"><span data-stu-id="a0bc0-104">The defined behaviors cannot include any [\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) elements.</span></span>

```xml
<system.ServiceModel>
  <behaviors>
    <endpointBehaviors>
      <behavior>
        <clientCredentials>
          <issuedToken>
            <issuerChannelBehaviors>
```

## <a name="syntax"></a><span data-ttu-id="a0bc0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0bc0-105">Syntax</span></span>

```xml
<issuerChannelBehaviors>
  <add behaviorConfiguration="string"
       issuerAddress="string" />
</issuerChannelBehaviors>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a0bc0-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a0bc0-106">Attributes and Elements</span></span>

<span data-ttu-id="a0bc0-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a0bc0-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="a0bc0-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="a0bc0-108">Attributes</span></span>

<span data-ttu-id="a0bc0-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a0bc0-109">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="a0bc0-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a0bc0-110">Child Elements</span></span>

|<span data-ttu-id="a0bc0-111">Élément</span><span class="sxs-lookup"><span data-stu-id="a0bc0-111">Element</span></span>|<span data-ttu-id="a0bc0-112">Description</span><span class="sxs-lookup"><span data-stu-id="a0bc0-112">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="a0bc0-113">\<add></span><span class="sxs-lookup"><span data-stu-id="a0bc0-113">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-issuerchannelbehaviors.md)|<span data-ttu-id="a0bc0-114">Ajoute un comportement à la collection.</span><span class="sxs-lookup"><span data-stu-id="a0bc0-114">Adds a behavior to the collection.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="a0bc0-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a0bc0-115">Parent Elements</span></span>

|<span data-ttu-id="a0bc0-116">Élément</span><span class="sxs-lookup"><span data-stu-id="a0bc0-116">Element</span></span>|<span data-ttu-id="a0bc0-117">Description</span><span class="sxs-lookup"><span data-stu-id="a0bc0-117">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="a0bc0-118">\<issuedToken></span><span class="sxs-lookup"><span data-stu-id="a0bc0-118">\<issuedToken></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtoken.md)|<span data-ttu-id="a0bc0-119">Spécifie un jeton personnalisé utilisé pour authentifier un client auprès d'un service.</span><span class="sxs-lookup"><span data-stu-id="a0bc0-119">Specifies a custom token used to authenticate a client to a service.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a0bc0-120">Notes</span><span class="sxs-lookup"><span data-stu-id="a0bc0-120">Remarks</span></span>

<span data-ttu-id="a0bc0-121">Utilisez cet élément lorsque des comportements (autres que ceux qui contiennent des éléments `<clientCredentials>`) doivent être utilisés pour communiquer avec un service.</span><span class="sxs-lookup"><span data-stu-id="a0bc0-121">Use this element when any behaviors (other than behaviors that include `<clientCredentials>` elements) must be used to communicate with a service.</span></span> <span data-ttu-id="a0bc0-122">Par exemple, si un [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) élément de comportement doit être inclus.</span><span class="sxs-lookup"><span data-stu-id="a0bc0-122">For example, if a [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) behavior element must be included.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0bc0-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0bc0-123">See also</span></span>

- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.IssuerChannelBehaviors%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElement>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElementCollection>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential.IssuerChannelBehaviors%2A>
- [<span data-ttu-id="a0bc0-124">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="a0bc0-124">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="a0bc0-125">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="a0bc0-125">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="a0bc0-126">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="a0bc0-126">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="a0bc0-127">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="a0bc0-127">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="a0bc0-128">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="a0bc0-128">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- [<span data-ttu-id="a0bc0-129">Procédure : créer un client fédéré</span><span class="sxs-lookup"><span data-stu-id="a0bc0-129">How to: Create a Federated Client</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="a0bc0-130">Procédure : configurer un émetteur local</span><span class="sxs-lookup"><span data-stu-id="a0bc0-130">How to: Configure a Local Issuer</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)
- [<span data-ttu-id="a0bc0-131">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="a0bc0-131">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
