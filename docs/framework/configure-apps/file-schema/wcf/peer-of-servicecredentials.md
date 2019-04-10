---
title: <peer> de <serviceCredentials>
ms.date: 03/30/2017
ms.assetid: b134e21d-e5b5-458e-9309-626dbf8db4ed
ms.openlocfilehash: d726ab460141b1e373a1cabf770b8958f50319eb
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59219146"
---
# <a name="peer-of-servicecredentials"></a><span data-ttu-id="74fa4-102">\<homologue > de \<serviceCredentials ></span><span class="sxs-lookup"><span data-stu-id="74fa4-102">\<peer> of \<serviceCredentials></span></span>
<span data-ttu-id="74fa4-103">Spécifie les informations d'identification actuelles d'un nœud homologue.</span><span class="sxs-lookup"><span data-stu-id="74fa4-103">Specifies the current credentials for a peer node.</span></span>  
  
 <span data-ttu-id="74fa4-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="74fa4-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="74fa4-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="74fa4-105">\<behaviors></span></span>  
<span data-ttu-id="74fa4-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="74fa4-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="74fa4-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="74fa4-107">\<behavior></span></span>  
<span data-ttu-id="74fa4-108">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="74fa4-108">\<serviceCredentials></span></span>  
<span data-ttu-id="74fa4-109">\<peer></span><span class="sxs-lookup"><span data-stu-id="74fa4-109">\<peer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="74fa4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74fa4-110">Syntax</span></span>  
  
```xml  
<peer>
  <certificate />
  <peerAuthentication />
  <messageSenderAuthentication />
</peer>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="74fa4-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="74fa4-111">Attributes and Elements</span></span>  
 <span data-ttu-id="74fa4-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="74fa4-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="74fa4-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="74fa4-113">Attributes</span></span>  
 <span data-ttu-id="74fa4-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="74fa4-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="74fa4-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="74fa4-115">Child Elements</span></span>  
  
|<span data-ttu-id="74fa4-116">Élément</span><span class="sxs-lookup"><span data-stu-id="74fa4-116">Element</span></span>|<span data-ttu-id="74fa4-117">Description</span><span class="sxs-lookup"><span data-stu-id="74fa4-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="74fa4-118">\<certificate></span><span class="sxs-lookup"><span data-stu-id="74fa4-118">\<certificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-of-peer.md)|<span data-ttu-id="74fa4-119">Spécifie un certificat X.509 à utiliser pour signer et chiffrer des messages pour les services de réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="74fa4-119">Specifies an X.509 certificate to use for signing and encrypting messages for peer-to-peer services.</span></span> <span data-ttu-id="74fa4-120">.</span><span class="sxs-lookup"><span data-stu-id="74fa4-120">.</span></span>|  
|[<span data-ttu-id="74fa4-121">\<messageSenderAuthentication></span><span class="sxs-lookup"><span data-stu-id="74fa4-121">\<messageSenderAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/messagesenderauthentication.md)|<span data-ttu-id="74fa4-122">Spécifie les options d'authentification pour les expéditeurs de messages.</span><span class="sxs-lookup"><span data-stu-id="74fa4-122">Specifies authentication options for message senders.</span></span>|  
|[<span data-ttu-id="74fa4-123">\<peerAuthentication></span><span class="sxs-lookup"><span data-stu-id="74fa4-123">\<peerAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peerauthentication.md)|<span data-ttu-id="74fa4-124">Spécifie les options d'authentification pour les services du réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="74fa4-124">Specifies authentication options for peer services.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="74fa4-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="74fa4-125">Parent Elements</span></span>  
  
|<span data-ttu-id="74fa4-126">Élément</span><span class="sxs-lookup"><span data-stu-id="74fa4-126">Element</span></span>|<span data-ttu-id="74fa4-127">Description</span><span class="sxs-lookup"><span data-stu-id="74fa4-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="74fa4-128">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="74fa4-128">\<serviceCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|<span data-ttu-id="74fa4-129">Spécifie les informations d’identification à utiliser pour authentifier le service, ainsi que les paramètres liés à la validation des informations d’identification du client.</span><span class="sxs-lookup"><span data-stu-id="74fa4-129">Specifies the credential to be used in authenticating the service, and the client credential validation-related settings.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="74fa4-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74fa4-130">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.Peer%2A>
- <xref:System.ServiceModel.Description.ServiceCredentials.Peer%2A>
- <xref:System.ServiceModel.Security.PeerCredential>
- [<span data-ttu-id="74fa4-131">Réseaux homologues</span><span class="sxs-lookup"><span data-stu-id="74fa4-131">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)
- [<span data-ttu-id="74fa4-132">Peer Channel Message Authentication</span><span class="sxs-lookup"><span data-stu-id="74fa4-132">Peer Channel Message Authentication</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))
- [<span data-ttu-id="74fa4-133">Peer Channel Custom Authentication</span><span class="sxs-lookup"><span data-stu-id="74fa4-133">Peer Channel Custom Authentication</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))
- [<span data-ttu-id="74fa4-134">Sécurisation des applications de canal homologue</span><span class="sxs-lookup"><span data-stu-id="74fa4-134">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
- [<span data-ttu-id="74fa4-135">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="74fa4-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
