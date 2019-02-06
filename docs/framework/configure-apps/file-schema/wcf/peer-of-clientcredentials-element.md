---
title: <peer> de <clientCredentials> élément
ms.date: 03/30/2017
ms.assetid: 505bd987-0042-4622-b68e-94f439729d53
ms.openlocfilehash: 8bdb52ccaaa8b41b3321447d2d68f9021a093481
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2019
ms.locfileid: "55758350"
---
# <a name="peer-of-clientcredentials-element"></a><span data-ttu-id="aeae5-102">\<homologue > de \<clientCredentials > élément</span><span class="sxs-lookup"><span data-stu-id="aeae5-102">\<peer> of \<clientCredentials> Element</span></span>
<span data-ttu-id="aeae5-103">Spécifie les informations d'identification utilisées lors de l'authentification de clients de réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="aeae5-103">Specifies credentials used when authenticating peer-to-peer clients.</span></span>  
  
 <span data-ttu-id="aeae5-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="aeae5-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="aeae5-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="aeae5-105">\<behaviors></span></span>  
<span data-ttu-id="aeae5-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="aeae5-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="aeae5-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="aeae5-107">\<behavior></span></span>  
<span data-ttu-id="aeae5-108">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="aeae5-108">\<clientCredentials></span></span>  
<span data-ttu-id="aeae5-109">\<peer></span><span class="sxs-lookup"><span data-stu-id="aeae5-109">\<peer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aeae5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aeae5-110">Syntax</span></span>  
  
```xml  
<peer>
  <certificate />
  <peerAuthentication />
  <messageSenderAuthentication />
</peer>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="aeae5-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="aeae5-111">Attributes and Elements</span></span>  
 <span data-ttu-id="aeae5-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="aeae5-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="aeae5-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="aeae5-113">Attributes</span></span>  
 <span data-ttu-id="aeae5-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="aeae5-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="aeae5-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="aeae5-115">Child Elements</span></span>  
  
|<span data-ttu-id="aeae5-116">Élément</span><span class="sxs-lookup"><span data-stu-id="aeae5-116">Element</span></span>|<span data-ttu-id="aeae5-117">Description</span><span class="sxs-lookup"><span data-stu-id="aeae5-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="aeae5-118">\<certificate></span><span class="sxs-lookup"><span data-stu-id="aeae5-118">\<certificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-element.md)|<span data-ttu-id="aeae5-119">Spécifie un certificat X.509 à utiliser pour signer et chiffrer des messages pour les clients de réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="aeae5-119">Specifies an X.509 certificate to use for signing and encrypting messages for peer-to-peer clients.</span></span> <span data-ttu-id="aeae5-120">.</span><span class="sxs-lookup"><span data-stu-id="aeae5-120">.</span></span>|  
|[<span data-ttu-id="aeae5-121">\<peerAuthentication></span><span class="sxs-lookup"><span data-stu-id="aeae5-121">\<peerAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peerauthentication-element.md)|<span data-ttu-id="aeae5-122">Spécifie les options d'authentification pour les clients du réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="aeae5-122">Specifies authentication options for peer clients.</span></span>|  
|[<span data-ttu-id="aeae5-123">\<messageSenderAuthentication></span><span class="sxs-lookup"><span data-stu-id="aeae5-123">\<messageSenderAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/messagesenderauthentication-element.md)|<span data-ttu-id="aeae5-124">Spécifie les options d'authentification pour les expéditeurs de messages.</span><span class="sxs-lookup"><span data-stu-id="aeae5-124">Specifies authentication options for message senders.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="aeae5-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="aeae5-125">Parent Elements</span></span>  
  
|<span data-ttu-id="aeae5-126">Élément</span><span class="sxs-lookup"><span data-stu-id="aeae5-126">Element</span></span>|<span data-ttu-id="aeae5-127">Description</span><span class="sxs-lookup"><span data-stu-id="aeae5-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="aeae5-128">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="aeae5-128">\<clientCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|<span data-ttu-id="aeae5-129">Spécifie les informations d'identification utilisées pour authentifier un client auprès d'un service.</span><span class="sxs-lookup"><span data-stu-id="aeae5-129">Specifies the credentials used to authenticate a client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="aeae5-130">Notes</span><span class="sxs-lookup"><span data-stu-id="aeae5-130">Remarks</span></span>  
 <span data-ttu-id="aeae5-131">Cet élément de configuration spécifie les informations d'identification qu'un nœud homologue utilise pour s'authentifier sur les autres nœuds de la maille, ainsi que les paramètres d'authentification qu'un nœud homologue utilise pour authentifier les autres nœuds homologues.</span><span class="sxs-lookup"><span data-stu-id="aeae5-131">This configuration element specifies the credentials that a peer node uses to authenticate itself to other nodes in the mesh, as well as authentication settings that a peer node uses to authenticate other peer nodes.</span></span> <span data-ttu-id="aeae5-132">Pour plus d’informations, consultez [l’authentification de Message du canal homologue](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90)) et [sécurisation des Applications de canal homologue](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md).</span><span class="sxs-lookup"><span data-stu-id="aeae5-132">For more information, see [Peer Channel Message Authentication](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90)) and [Securing Peer Channel Applications](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aeae5-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aeae5-133">See also</span></span>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.Peer%2A>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Description.ClientCredentials.Peer%2A>
- <xref:System.ServiceModel.Security.PeerCredential>
- [<span data-ttu-id="aeae5-134">Réseaux homologues</span><span class="sxs-lookup"><span data-stu-id="aeae5-134">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)
- [<span data-ttu-id="aeae5-135">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="aeae5-135">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- <span data-ttu-id="aeae5-136">[Authentification de Message de canal homologue](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="aeae5-136">[Peer Channel Message Authentication](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span></span>
- <span data-ttu-id="aeae5-137">[Authentification personnalisée de canal homologue](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="aeae5-137">[Peer Channel Custom Authentication](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span></span>
- [<span data-ttu-id="aeae5-138">Sécurisation des applications de canal homologue</span><span class="sxs-lookup"><span data-stu-id="aeae5-138">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
- [<span data-ttu-id="aeae5-139">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="aeae5-139">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
