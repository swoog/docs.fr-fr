---
title: '&lt;transport&gt; de &lt;netPeerTcpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: c44d86d2-1160-44d7-9c7a-297b12eccc7f
ms.openlocfilehash: b929c97d0b5d9e021a71e4b88dd3d8a5f2f909a7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54677002"
---
# <a name="lttransportgt-of-ltnetpeertcpbindinggt"></a><span data-ttu-id="ff7da-102">&lt;transport&gt; de &lt;netPeerTcpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="ff7da-102">&lt;transport&gt; of &lt;netPeerTcpBinding&gt;</span></span>
<span data-ttu-id="ff7da-103">Spécifie les paramètres de sécurité de niveau transport lorsque vous utilisez le [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="ff7da-103">Specifies settings for transport level security when using the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>  
  
 <span data-ttu-id="ff7da-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="ff7da-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="ff7da-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="ff7da-105">\<bindings></span></span>  
<span data-ttu-id="ff7da-106">\<netPeerTcpBinding></span><span class="sxs-lookup"><span data-stu-id="ff7da-106">\<netPeerTcpBinding></span></span>  
<span data-ttu-id="ff7da-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="ff7da-107">\<binding></span></span>  
<span data-ttu-id="ff7da-108">\<security></span><span class="sxs-lookup"><span data-stu-id="ff7da-108">\<security></span></span>  
<span data-ttu-id="ff7da-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="ff7da-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ff7da-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff7da-110">Syntax</span></span>  
  
```xml  
<netPeerTcpBinding>
  <binding>
    <security>
      <transport credentialType="Certificate/Password" />
    </security>
  </binding>
</netPeerTcpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ff7da-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ff7da-111">Attributes and Elements</span></span>  
 <span data-ttu-id="ff7da-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ff7da-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ff7da-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="ff7da-113">Attributes</span></span>  
  
|<span data-ttu-id="ff7da-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="ff7da-114">Attribute</span></span>|<span data-ttu-id="ff7da-115">Description</span><span class="sxs-lookup"><span data-stu-id="ff7da-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ff7da-116">credentialType</span><span class="sxs-lookup"><span data-stu-id="ff7da-116">credentialType</span></span>|<span data-ttu-id="ff7da-117">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="ff7da-117">Optional.</span></span> <span data-ttu-id="ff7da-118">Spécifie le type d'informations d'identification utilisé pour vérifier les messages envoyés avec le transport d'homologues.</span><span class="sxs-lookup"><span data-stu-id="ff7da-118">Specifies the type of credentials used to verify messages sent with the peer transport.</span></span> <span data-ttu-id="ff7da-119">Cet attribut est de type <xref:System.ServiceModel.PeerTransportCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="ff7da-119">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span>|  
  
## <a name="credentialtype-attribute"></a><span data-ttu-id="ff7da-120">Attribut credentialType</span><span class="sxs-lookup"><span data-stu-id="ff7da-120">credentialType Attribute</span></span>  
  
|<span data-ttu-id="ff7da-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff7da-121">Value</span></span>|<span data-ttu-id="ff7da-122">Description</span><span class="sxs-lookup"><span data-stu-id="ff7da-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="ff7da-123">Certificat</span><span class="sxs-lookup"><span data-stu-id="ff7da-123">Certificate</span></span>|<span data-ttu-id="ff7da-124">L'authentification du transport de canal homologue requiert un certificat X509.</span><span class="sxs-lookup"><span data-stu-id="ff7da-124">Authentication of the peer channel transport requires an X509 certificate.</span></span>|  
|<span data-ttu-id="ff7da-125">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="ff7da-125">Password</span></span>|<span data-ttu-id="ff7da-126">L'authentification du transport de canal homologue requiert un mot de passe correct.</span><span class="sxs-lookup"><span data-stu-id="ff7da-126">Authentication of the peer channel transport requires a correct password.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ff7da-127">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ff7da-127">Child Elements</span></span>  
 <span data-ttu-id="ff7da-128">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ff7da-128">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ff7da-129">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ff7da-129">Parent Elements</span></span>  
  
|<span data-ttu-id="ff7da-130">Élément</span><span class="sxs-lookup"><span data-stu-id="ff7da-130">Element</span></span>|<span data-ttu-id="ff7da-131">Description</span><span class="sxs-lookup"><span data-stu-id="ff7da-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ff7da-132">\<security></span><span class="sxs-lookup"><span data-stu-id="ff7da-132">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netpeerbinding.md)|<span data-ttu-id="ff7da-133">Définit les paramètres de sécurité pour le [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="ff7da-133">Defines the security settings for the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ff7da-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff7da-134">See also</span></span>
- <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>
- <xref:System.ServiceModel.PeerSecuritySettings.Transport%2A>
- <xref:System.ServiceModel.Configuration.PeerSecurityElement.Transport%2A>
- <xref:System.ServiceModel.PeerTransportSecuritySettings>
- [<span data-ttu-id="ff7da-135">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="ff7da-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="ff7da-136">Liaisons</span><span class="sxs-lookup"><span data-stu-id="ff7da-136">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="ff7da-137">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="ff7da-137">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="ff7da-138">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="ff7da-138">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="ff7da-139">\<binding></span><span class="sxs-lookup"><span data-stu-id="ff7da-139">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
