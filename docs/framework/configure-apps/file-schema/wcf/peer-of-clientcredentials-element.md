---
title: <peer> de <clientCredentials> élément
ms.date: 03/30/2017
ms.assetid: 505bd987-0042-4622-b68e-94f439729d53
ms.openlocfilehash: 7074ee992755557d7e5503035c89bdbefd678792
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61783373"
---
# <a name="peer-of-clientcredentials-element"></a><span data-ttu-id="7bb53-102">\<homologue > de \<clientCredentials > élément</span><span class="sxs-lookup"><span data-stu-id="7bb53-102">\<peer> of \<clientCredentials> Element</span></span>
<span data-ttu-id="7bb53-103">Spécifie les informations d'identification utilisées lors de l'authentification de clients de réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="7bb53-103">Specifies credentials used when authenticating peer-to-peer clients.</span></span>  
  
 <span data-ttu-id="7bb53-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="7bb53-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="7bb53-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="7bb53-105">\<behaviors></span></span>  
<span data-ttu-id="7bb53-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="7bb53-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="7bb53-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="7bb53-107">\<behavior></span></span>  
<span data-ttu-id="7bb53-108">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="7bb53-108">\<clientCredentials></span></span>  
<span data-ttu-id="7bb53-109">\<peer></span><span class="sxs-lookup"><span data-stu-id="7bb53-109">\<peer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7bb53-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bb53-110">Syntax</span></span>  
  
```xml  
<peer>
  <certificate />
  <peerAuthentication />
  <messageSenderAuthentication />
</peer>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7bb53-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7bb53-111">Attributes and Elements</span></span>  
 <span data-ttu-id="7bb53-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7bb53-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7bb53-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="7bb53-113">Attributes</span></span>  
 <span data-ttu-id="7bb53-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7bb53-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="7bb53-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7bb53-115">Child Elements</span></span>  
  
|<span data-ttu-id="7bb53-116">Élément</span><span class="sxs-lookup"><span data-stu-id="7bb53-116">Element</span></span>|<span data-ttu-id="7bb53-117">Description</span><span class="sxs-lookup"><span data-stu-id="7bb53-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7bb53-118">\<certificate></span><span class="sxs-lookup"><span data-stu-id="7bb53-118">\<certificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-element.md)|<span data-ttu-id="7bb53-119">Spécifie un certificat X.509 à utiliser pour signer et chiffrer des messages pour les clients de réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="7bb53-119">Specifies an X.509 certificate to use for signing and encrypting messages for peer-to-peer clients.</span></span> <span data-ttu-id="7bb53-120">.</span><span class="sxs-lookup"><span data-stu-id="7bb53-120">.</span></span>|  
|[<span data-ttu-id="7bb53-121">\<peerAuthentication></span><span class="sxs-lookup"><span data-stu-id="7bb53-121">\<peerAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peerauthentication-element.md)|<span data-ttu-id="7bb53-122">Spécifie les options d'authentification pour les clients du réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="7bb53-122">Specifies authentication options for peer clients.</span></span>|  
|[<span data-ttu-id="7bb53-123">\<messageSenderAuthentication></span><span class="sxs-lookup"><span data-stu-id="7bb53-123">\<messageSenderAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/messagesenderauthentication-element.md)|<span data-ttu-id="7bb53-124">Spécifie les options d'authentification pour les expéditeurs de messages.</span><span class="sxs-lookup"><span data-stu-id="7bb53-124">Specifies authentication options for message senders.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="7bb53-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7bb53-125">Parent Elements</span></span>  
  
|<span data-ttu-id="7bb53-126">Élément</span><span class="sxs-lookup"><span data-stu-id="7bb53-126">Element</span></span>|<span data-ttu-id="7bb53-127">Description</span><span class="sxs-lookup"><span data-stu-id="7bb53-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7bb53-128">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="7bb53-128">\<clientCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|<span data-ttu-id="7bb53-129">Spécifie les informations d'identification utilisées pour authentifier un client auprès d'un service.</span><span class="sxs-lookup"><span data-stu-id="7bb53-129">Specifies the credentials used to authenticate a client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7bb53-130">Notes</span><span class="sxs-lookup"><span data-stu-id="7bb53-130">Remarks</span></span>  
 <span data-ttu-id="7bb53-131">Cet élément de configuration spécifie les informations d'identification qu'un nœud homologue utilise pour s'authentifier sur les autres nœuds de la maille, ainsi que les paramètres d'authentification qu'un nœud homologue utilise pour authentifier les autres nœuds homologues.</span><span class="sxs-lookup"><span data-stu-id="7bb53-131">This configuration element specifies the credentials that a peer node uses to authenticate itself to other nodes in the mesh, as well as authentication settings that a peer node uses to authenticate other peer nodes.</span></span> <span data-ttu-id="7bb53-132">Pour plus d’informations, consultez [l’authentification de Message du canal homologue](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90)) et [sécurisation des Applications de canal homologue](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md).</span><span class="sxs-lookup"><span data-stu-id="7bb53-132">For more information, see [Peer Channel Message Authentication](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90)) and [Securing Peer Channel Applications](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7bb53-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bb53-133">See also</span></span>

- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.Peer%2A>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Description.ClientCredentials.Peer%2A>
- <xref:System.ServiceModel.Security.PeerCredential>
- [<span data-ttu-id="7bb53-134">Réseaux homologues</span><span class="sxs-lookup"><span data-stu-id="7bb53-134">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)
- [<span data-ttu-id="7bb53-135">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="7bb53-135">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- <span data-ttu-id="7bb53-136">[Authentification de Message de canal homologue](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="7bb53-136">[Peer Channel Message Authentication](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span></span>
- <span data-ttu-id="7bb53-137">[Authentification personnalisée de canal homologue](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="7bb53-137">[Peer Channel Custom Authentication](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span></span>
- [<span data-ttu-id="7bb53-138">Sécurisation des applications de canal homologue</span><span class="sxs-lookup"><span data-stu-id="7bb53-138">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
- [<span data-ttu-id="7bb53-139">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="7bb53-139">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
