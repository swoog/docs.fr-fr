---
title: <peer> de <clientCredentials> élément
ms.date: 03/30/2017
ms.assetid: 505bd987-0042-4622-b68e-94f439729d53
ms.openlocfilehash: 8970100b1ad3019ff4a639d835d1db1430968008
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55275139"
---
# <a name="peer-of-clientcredentials-element"></a><span data-ttu-id="9760e-102">\<homologue > de \<clientCredentials > élément</span><span class="sxs-lookup"><span data-stu-id="9760e-102">\<peer> of \<clientCredentials> Element</span></span>
<span data-ttu-id="9760e-103">Spécifie les informations d'identification utilisées lors de l'authentification de clients de réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="9760e-103">Specifies credentials used when authenticating peer-to-peer clients.</span></span>  
  
 <span data-ttu-id="9760e-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="9760e-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="9760e-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="9760e-105">\<behaviors></span></span>  
<span data-ttu-id="9760e-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="9760e-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="9760e-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="9760e-107">\<behavior></span></span>  
<span data-ttu-id="9760e-108">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="9760e-108">\<clientCredentials></span></span>  
<span data-ttu-id="9760e-109">\<peer></span><span class="sxs-lookup"><span data-stu-id="9760e-109">\<peer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9760e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9760e-110">Syntax</span></span>  
  
```xml  
<peer>
  <certificate />
  <peerAuthentication />
  <messageSenderAuthentication />
</peer>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9760e-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9760e-111">Attributes and Elements</span></span>  
 <span data-ttu-id="9760e-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9760e-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9760e-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="9760e-113">Attributes</span></span>  
 <span data-ttu-id="9760e-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9760e-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9760e-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9760e-115">Child Elements</span></span>  
  
|<span data-ttu-id="9760e-116">Élément</span><span class="sxs-lookup"><span data-stu-id="9760e-116">Element</span></span>|<span data-ttu-id="9760e-117">Description</span><span class="sxs-lookup"><span data-stu-id="9760e-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9760e-118">\<certificate></span><span class="sxs-lookup"><span data-stu-id="9760e-118">\<certificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-element.md)|<span data-ttu-id="9760e-119">Spécifie un certificat X.509 à utiliser pour signer et chiffrer des messages pour les clients de réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="9760e-119">Specifies an X.509 certificate to use for signing and encrypting messages for peer-to-peer clients.</span></span> <span data-ttu-id="9760e-120">.</span><span class="sxs-lookup"><span data-stu-id="9760e-120">.</span></span>|  
|[<span data-ttu-id="9760e-121">\<peerAuthentication></span><span class="sxs-lookup"><span data-stu-id="9760e-121">\<peerAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peerauthentication-element.md)|<span data-ttu-id="9760e-122">Spécifie les options d'authentification pour les clients du réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="9760e-122">Specifies authentication options for peer clients.</span></span>|  
|[<span data-ttu-id="9760e-123">\<messageSenderAuthentication></span><span class="sxs-lookup"><span data-stu-id="9760e-123">\<messageSenderAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/messagesenderauthentication-element.md)|<span data-ttu-id="9760e-124">Spécifie les options d'authentification pour les expéditeurs de messages.</span><span class="sxs-lookup"><span data-stu-id="9760e-124">Specifies authentication options for message senders.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9760e-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9760e-125">Parent Elements</span></span>  
  
|<span data-ttu-id="9760e-126">Élément</span><span class="sxs-lookup"><span data-stu-id="9760e-126">Element</span></span>|<span data-ttu-id="9760e-127">Description</span><span class="sxs-lookup"><span data-stu-id="9760e-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9760e-128">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="9760e-128">\<clientCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|<span data-ttu-id="9760e-129">Spécifie les informations d'identification utilisées pour authentifier un client auprès d'un service.</span><span class="sxs-lookup"><span data-stu-id="9760e-129">Specifies the credentials used to authenticate a client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9760e-130">Notes</span><span class="sxs-lookup"><span data-stu-id="9760e-130">Remarks</span></span>  
 <span data-ttu-id="9760e-131">Cet élément de configuration spécifie les informations d'identification qu'un nœud homologue utilise pour s'authentifier sur les autres nœuds de la maille, ainsi que les paramètres d'authentification qu'un nœud homologue utilise pour authentifier les autres nœuds homologues.</span><span class="sxs-lookup"><span data-stu-id="9760e-131">This configuration element specifies the credentials that a peer node uses to authenticate itself to other nodes in the mesh, as well as authentication settings that a peer node uses to authenticate other peer nodes.</span></span> <span data-ttu-id="9760e-132">Pour plus d’informations, consultez [l’authentification de Message du canal homologue](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95) et [sécurisation des Applications de canal homologue](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md).</span><span class="sxs-lookup"><span data-stu-id="9760e-132">For more information, see [Peer Channel Message Authentication](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95) and [Securing Peer Channel Applications](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9760e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9760e-133">See also</span></span>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.Peer%2A>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Description.ClientCredentials.Peer%2A>
- <xref:System.ServiceModel.Security.PeerCredential>
- [<span data-ttu-id="9760e-134">Réseaux homologues</span><span class="sxs-lookup"><span data-stu-id="9760e-134">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)
- [<span data-ttu-id="9760e-135">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="9760e-135">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- [<span data-ttu-id="9760e-136">Authentification de Message de canal homologue</span><span class="sxs-lookup"><span data-stu-id="9760e-136">Peer Channel Message Authentication</span></span>](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)
- [<span data-ttu-id="9760e-137">Authentification personnalisée de canal homologue</span><span class="sxs-lookup"><span data-stu-id="9760e-137">Peer Channel Custom Authentication</span></span>](https://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)
- [<span data-ttu-id="9760e-138">Sécurisation des applications de canal homologue</span><span class="sxs-lookup"><span data-stu-id="9760e-138">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
- [<span data-ttu-id="9760e-139">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="9760e-139">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
