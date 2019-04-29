---
title: <transport> de <netPeerTcpBinding>
ms.date: 03/30/2017
ms.assetid: c44d86d2-1160-44d7-9c7a-297b12eccc7f
ms.openlocfilehash: 157637615abafbd5913e4d90b702bb0224d5f121
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61788321"
---
# <a name="transport-of-netpeertcpbinding"></a><span data-ttu-id="e176c-102">\<transport> of \<netPeerTcpBinding></span><span class="sxs-lookup"><span data-stu-id="e176c-102">\<transport> of \<netPeerTcpBinding></span></span>
<span data-ttu-id="e176c-103">Spécifie les paramètres de sécurité de niveau transport lorsque vous utilisez le [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="e176c-103">Specifies settings for transport level security when using the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>  
  
 <span data-ttu-id="e176c-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="e176c-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="e176c-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="e176c-105">\<bindings></span></span>  
<span data-ttu-id="e176c-106">\<netPeerTcpBinding></span><span class="sxs-lookup"><span data-stu-id="e176c-106">\<netPeerTcpBinding></span></span>  
<span data-ttu-id="e176c-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="e176c-107">\<binding></span></span>  
<span data-ttu-id="e176c-108">\<security></span><span class="sxs-lookup"><span data-stu-id="e176c-108">\<security></span></span>  
<span data-ttu-id="e176c-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="e176c-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e176c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e176c-110">Syntax</span></span>  
  
```xml  
<netPeerTcpBinding>
  <binding>
    <security>
      <transport credentialType="Certificate/Password" />
    </security>
  </binding>
</netPeerTcpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e176c-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e176c-111">Attributes and Elements</span></span>  
 <span data-ttu-id="e176c-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e176c-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e176c-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="e176c-113">Attributes</span></span>  
  
|<span data-ttu-id="e176c-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="e176c-114">Attribute</span></span>|<span data-ttu-id="e176c-115">Description</span><span class="sxs-lookup"><span data-stu-id="e176c-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e176c-116">credentialType</span><span class="sxs-lookup"><span data-stu-id="e176c-116">credentialType</span></span>|<span data-ttu-id="e176c-117">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="e176c-117">Optional.</span></span> <span data-ttu-id="e176c-118">Spécifie le type d'informations d'identification utilisé pour vérifier les messages envoyés avec le transport d'homologues.</span><span class="sxs-lookup"><span data-stu-id="e176c-118">Specifies the type of credentials used to verify messages sent with the peer transport.</span></span> <span data-ttu-id="e176c-119">Cet attribut est de type <xref:System.ServiceModel.PeerTransportCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="e176c-119">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span>|  
  
## <a name="credentialtype-attribute"></a><span data-ttu-id="e176c-120">Attribut credentialType</span><span class="sxs-lookup"><span data-stu-id="e176c-120">credentialType Attribute</span></span>  
  
|<span data-ttu-id="e176c-121">Value</span><span class="sxs-lookup"><span data-stu-id="e176c-121">Value</span></span>|<span data-ttu-id="e176c-122">Description</span><span class="sxs-lookup"><span data-stu-id="e176c-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="e176c-123">Certificat</span><span class="sxs-lookup"><span data-stu-id="e176c-123">Certificate</span></span>|<span data-ttu-id="e176c-124">L'authentification du transport de canal homologue requiert un certificat X509.</span><span class="sxs-lookup"><span data-stu-id="e176c-124">Authentication of the peer channel transport requires an X509 certificate.</span></span>|  
|<span data-ttu-id="e176c-125">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="e176c-125">Password</span></span>|<span data-ttu-id="e176c-126">L'authentification du transport de canal homologue requiert un mot de passe correct.</span><span class="sxs-lookup"><span data-stu-id="e176c-126">Authentication of the peer channel transport requires a correct password.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e176c-127">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e176c-127">Child Elements</span></span>  
 <span data-ttu-id="e176c-128">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e176c-128">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e176c-129">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e176c-129">Parent Elements</span></span>  
  
|<span data-ttu-id="e176c-130">Élément</span><span class="sxs-lookup"><span data-stu-id="e176c-130">Element</span></span>|<span data-ttu-id="e176c-131">Description</span><span class="sxs-lookup"><span data-stu-id="e176c-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e176c-132">\<security></span><span class="sxs-lookup"><span data-stu-id="e176c-132">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netpeerbinding.md)|<span data-ttu-id="e176c-133">Définit les paramètres de sécurité pour le [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="e176c-133">Defines the security settings for the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e176c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e176c-134">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>
- <xref:System.ServiceModel.PeerSecuritySettings.Transport%2A>
- <xref:System.ServiceModel.Configuration.PeerSecurityElement.Transport%2A>
- <xref:System.ServiceModel.PeerTransportSecuritySettings>
- [<span data-ttu-id="e176c-135">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="e176c-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="e176c-136">Liaisons</span><span class="sxs-lookup"><span data-stu-id="e176c-136">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="e176c-137">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="e176c-137">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="e176c-138">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="e176c-138">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="e176c-139">\<binding></span><span class="sxs-lookup"><span data-stu-id="e176c-139">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
