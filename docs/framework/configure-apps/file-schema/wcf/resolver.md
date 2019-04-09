---
title: <resolver>
ms.date: 03/30/2017
ms.assetid: 0c00200c-f135-4e5c-a024-76b72bcbc021
ms.openlocfilehash: 39dcb868bd3ff25451509616e1dac7d41f94cfa1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59075872"
---
# <a name="resolver"></a><span data-ttu-id="3bf1f-101">\<resolver></span><span class="sxs-lookup"><span data-stu-id="3bf1f-101">\<resolver></span></span>
<span data-ttu-id="3bf1f-102">Spécifie un programme de résolution d'homologue utilisé pour résoudre un ID de maille d'homologues en un jeu d'adresses de nœuds d'homologues représentant plusieurs nœuds faisant partie de la maille.</span><span class="sxs-lookup"><span data-stu-id="3bf1f-102">Specifies a peer resolver that is used to resolve a peer mesh ID to a set of peer node addresses that represents several nodes that participate in the mesh.</span></span>  
  
 <span data-ttu-id="3bf1f-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="3bf1f-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="3bf1f-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="3bf1f-104">\<bindings></span></span>  
<span data-ttu-id="3bf1f-105">\<netPeerBinding></span><span class="sxs-lookup"><span data-stu-id="3bf1f-105">\<netPeerBinding></span></span>  
<span data-ttu-id="3bf1f-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="3bf1f-106">\<binding></span></span>  
<span data-ttu-id="3bf1f-107">\<resolver></span><span class="sxs-lookup"><span data-stu-id="3bf1f-107">\<resolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3bf1f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bf1f-108">Syntax</span></span>  
  
```xml  
<resolver mode="Auto/Custom/Pnrp"
          referralPolicy="DoNotShare/Service/Share">
</resolver>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3bf1f-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3bf1f-109">Attributes and Elements</span></span>  
 <span data-ttu-id="3bf1f-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3bf1f-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3bf1f-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="3bf1f-111">Attributes</span></span>  
  
|<span data-ttu-id="3bf1f-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="3bf1f-112">Attribute</span></span>|<span data-ttu-id="3bf1f-113">Description</span><span class="sxs-lookup"><span data-stu-id="3bf1f-113">Description</span></span>|  
|---------------|-----------------|  
|`mode`|<span data-ttu-id="3bf1f-114">Chaîne qui spécifie si l'instance du programme de résolution d'homologue associée à ce service est spécifique au PNRP, à un programme de résolution personnalisé ou si elle est déterminée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="3bf1f-114">A string that specifies whether the peer resolver instance associated with this service is either PNRP-specific, a custom resolver, or automatically determined.</span></span> <span data-ttu-id="3bf1f-115">Cet attribut est de type <xref:System.ServiceModel.PeerResolvers.PeerResolverMode>.</span><span class="sxs-lookup"><span data-stu-id="3bf1f-115">This attribute is of type <xref:System.ServiceModel.PeerResolvers.PeerResolverMode>.</span></span>|  
|`referralPolicy`|<span data-ttu-id="3bf1f-116">Chaîne qui spécifie la manière dont les références sont partagées parmi des homologues.</span><span class="sxs-lookup"><span data-stu-id="3bf1f-116">A string that specifies the way referrals are shared among peers.</span></span> <span data-ttu-id="3bf1f-117">Cet attribut est de type <xref:System.ServiceModel.PeerResolvers.PeerReferralPolicy>.</span><span class="sxs-lookup"><span data-stu-id="3bf1f-117">This attribute is of type <xref:System.ServiceModel.PeerResolvers.PeerReferralPolicy>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3bf1f-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3bf1f-118">Child Elements</span></span>  
  
|<span data-ttu-id="3bf1f-119">Élément</span><span class="sxs-lookup"><span data-stu-id="3bf1f-119">Element</span></span>|<span data-ttu-id="3bf1f-120">Description</span><span class="sxs-lookup"><span data-stu-id="3bf1f-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3bf1f-121">\<headers></span><span class="sxs-lookup"><span data-stu-id="3bf1f-121">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers.md)|<span data-ttu-id="3bf1f-122">Spécifie les paramètres pour un service de programme de résolution d'homologue personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3bf1f-122">Specifies settings for a custom peer resolver service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="3bf1f-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3bf1f-123">Parent Elements</span></span>  
  
|<span data-ttu-id="3bf1f-124">Élément</span><span class="sxs-lookup"><span data-stu-id="3bf1f-124">Element</span></span>|<span data-ttu-id="3bf1f-125">Description</span><span class="sxs-lookup"><span data-stu-id="3bf1f-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3bf1f-126">\<binding></span><span class="sxs-lookup"><span data-stu-id="3bf1f-126">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="3bf1f-127">Définit toutes les fonctions de liaison de la [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="3bf1f-127">Defines all binding capabilities of the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3bf1f-128">Notes</span><span class="sxs-lookup"><span data-stu-id="3bf1f-128">Remarks</span></span>  
 <span data-ttu-id="3bf1f-129">Un programme de résolution de nom d'homologue est un service de découverte utilisé par les canaux homologues afin de rechercher des nœuds d'homologues faisant partie d'une maille d'homologues.</span><span class="sxs-lookup"><span data-stu-id="3bf1f-129">A peer name resolver is a discovery service used by peer channels to find peer nodes that participate in a peer mesh.</span></span> <span data-ttu-id="3bf1f-130">Il est également utilisé pour « inscrire » un nœud avec un maillage d'homologue, le mécanisme par lequel le nœud homologue est connu et disponible à partir du maillage d'homologue.</span><span class="sxs-lookup"><span data-stu-id="3bf1f-130">It is also used to "register" a node with a peer mesh, the mechanism by which the peer node becomes known and available from the peer mesh.</span></span> <span data-ttu-id="3bf1f-131">Pour plus d’informations sur les programmes de résolution homologues, consultez [programmes de résolution homologues](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md).</span><span class="sxs-lookup"><span data-stu-id="3bf1f-131">For more information on peer resolvers, see [Peer Resolvers](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3bf1f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bf1f-132">See also</span></span>

- <xref:System.ServiceModel.PeerResolver>
- <xref:System.ServiceModel.PeerResolvers.PeerResolverSettings>
- <xref:System.ServiceModel.NetPeerTcpBinding.Resolver%2A>
- <xref:System.ServiceModel.Configuration.NetPeerTcpBindingElement.Resolver%2A>
- <xref:System.ServiceModel.Configuration.PeerResolverElement>
- [<span data-ttu-id="3bf1f-133">Programmes de résolution d'homologue</span><span class="sxs-lookup"><span data-stu-id="3bf1f-133">Peer Resolvers</span></span>](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)
- [<span data-ttu-id="3bf1f-134">Ajout d'un programme de résolution personnalisé à une application PeerChannel</span><span class="sxs-lookup"><span data-stu-id="3bf1f-134">Adding a Custom Resolver to a PeerChannel Application</span></span>](https://docs.microsoft.com/previous-versions/ms730105(v=vs.90))
