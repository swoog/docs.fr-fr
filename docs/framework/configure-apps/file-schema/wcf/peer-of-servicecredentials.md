---
title: <peer> de <serviceCredentials>
ms.date: 03/30/2017
ms.assetid: b134e21d-e5b5-458e-9309-626dbf8db4ed
ms.openlocfilehash: 2090e79e6affe8ade6e2e52b94d2c4e1dafe8fa1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266024"
---
# <a name="peer-of-servicecredentials"></a><span data-ttu-id="a2260-102">\<homologue > de \<serviceCredentials ></span><span class="sxs-lookup"><span data-stu-id="a2260-102">\<peer> of \<serviceCredentials></span></span>
<span data-ttu-id="a2260-103">Spécifie les informations d'identification actuelles d'un nœud homologue.</span><span class="sxs-lookup"><span data-stu-id="a2260-103">Specifies the current credentials for a peer node.</span></span>  
  
 <span data-ttu-id="a2260-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="a2260-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="a2260-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="a2260-105">\<behaviors></span></span>  
<span data-ttu-id="a2260-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="a2260-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="a2260-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="a2260-107">\<behavior></span></span>  
<span data-ttu-id="a2260-108">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="a2260-108">\<serviceCredentials></span></span>  
<span data-ttu-id="a2260-109">\<peer></span><span class="sxs-lookup"><span data-stu-id="a2260-109">\<peer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a2260-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2260-110">Syntax</span></span>  
  
```xml  
<peer>
  <certificate />
  <peerAuthentication />
  <messageSenderAuthentication />
</peer>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a2260-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a2260-111">Attributes and Elements</span></span>  
 <span data-ttu-id="a2260-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a2260-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a2260-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="a2260-113">Attributes</span></span>  
 <span data-ttu-id="a2260-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a2260-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="a2260-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a2260-115">Child Elements</span></span>  
  
|<span data-ttu-id="a2260-116">Élément</span><span class="sxs-lookup"><span data-stu-id="a2260-116">Element</span></span>|<span data-ttu-id="a2260-117">Description</span><span class="sxs-lookup"><span data-stu-id="a2260-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a2260-118">\<certificate></span><span class="sxs-lookup"><span data-stu-id="a2260-118">\<certificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-of-peer.md)|<span data-ttu-id="a2260-119">Spécifie un certificat X.509 à utiliser pour signer et chiffrer des messages pour les services de réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="a2260-119">Specifies an X.509 certificate to use for signing and encrypting messages for peer-to-peer services.</span></span> <span data-ttu-id="a2260-120">.</span><span class="sxs-lookup"><span data-stu-id="a2260-120">.</span></span>|  
|[<span data-ttu-id="a2260-121">\<messageSenderAuthentication></span><span class="sxs-lookup"><span data-stu-id="a2260-121">\<messageSenderAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/messagesenderauthentication.md)|<span data-ttu-id="a2260-122">Spécifie les options d'authentification pour les expéditeurs de messages.</span><span class="sxs-lookup"><span data-stu-id="a2260-122">Specifies authentication options for message senders.</span></span>|  
|[<span data-ttu-id="a2260-123">\<peerAuthentication></span><span class="sxs-lookup"><span data-stu-id="a2260-123">\<peerAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peerauthentication.md)|<span data-ttu-id="a2260-124">Spécifie les options d'authentification pour les services du réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="a2260-124">Specifies authentication options for peer services.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a2260-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a2260-125">Parent Elements</span></span>  
  
|<span data-ttu-id="a2260-126">Élément</span><span class="sxs-lookup"><span data-stu-id="a2260-126">Element</span></span>|<span data-ttu-id="a2260-127">Description</span><span class="sxs-lookup"><span data-stu-id="a2260-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a2260-128">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="a2260-128">\<serviceCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|<span data-ttu-id="a2260-129">Spécifie les informations d’identification à utiliser pour authentifier le service, ainsi que les paramètres liés à la validation des informations d’identification du client.</span><span class="sxs-lookup"><span data-stu-id="a2260-129">Specifies the credential to be used in authenticating the service, and the client credential validation-related settings.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a2260-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2260-130">See also</span></span>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.Peer%2A>
- <xref:System.ServiceModel.Description.ServiceCredentials.Peer%2A>
- <xref:System.ServiceModel.Security.PeerCredential>
- [<span data-ttu-id="a2260-131">Réseaux homologues</span><span class="sxs-lookup"><span data-stu-id="a2260-131">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)
- [<span data-ttu-id="a2260-132">Authentification de Message de canal homologue</span><span class="sxs-lookup"><span data-stu-id="a2260-132">Peer Channel Message Authentication</span></span>](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)
- [<span data-ttu-id="a2260-133">Authentification personnalisée de canal homologue</span><span class="sxs-lookup"><span data-stu-id="a2260-133">Peer Channel Custom Authentication</span></span>](https://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)
- [<span data-ttu-id="a2260-134">Sécurisation des applications de canal homologue</span><span class="sxs-lookup"><span data-stu-id="a2260-134">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
- [<span data-ttu-id="a2260-135">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="a2260-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
