---
title: '&lt;security&gt; de &lt;netPeerBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 1ef40d8c-f903-4426-9b08-da81462766d8
author: BrucePerlerMS
ms.openlocfilehash: 1d7ffaf72e34b700f4702b2e531afbf7e842de09
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48844564"
---
# <a name="ltsecuritygt-of-ltnetpeerbindinggt"></a><span data-ttu-id="c0c4f-102">&lt;security&gt; de &lt;netPeerBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="c0c4f-102">&lt;security&gt; of &lt;netPeerBinding&gt;</span></span>
<span data-ttu-id="c0c4f-103">Définit les paramètres de sécurité de la [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md), y compris le type d’authentification utilisé et la sécurité utilisée pour le transport de messages.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-103">Defines the security settings of the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md), including the type of authentication used and the security used for the message transport.</span></span>  
  
 <span data-ttu-id="c0c4f-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="c0c4f-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="c0c4f-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="c0c4f-105">\<bindings></span></span>  
<span data-ttu-id="c0c4f-106">\<netPeerBinding></span><span class="sxs-lookup"><span data-stu-id="c0c4f-106">\<netPeerBinding></span></span>  
<span data-ttu-id="c0c4f-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="c0c4f-107">\<binding></span></span>  
<span data-ttu-id="c0c4f-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="c0c4f-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0c4f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0c4f-109">Syntax</span></span>  
  
```xml  
<netPeerBinding>  
    <binding>  
        <security mode="Message/None/Transport//TransportWithMessageCredential">  
            <transport credentialType="Certificate/Password" />  
        </security>  
    </binding>  
</netPeerBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c0c4f-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c0c4f-110">Attributes and Elements</span></span>  
 <span data-ttu-id="c0c4f-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-111">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c0c4f-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="c0c4f-112">Attributes</span></span>  
  
|<span data-ttu-id="c0c4f-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="c0c4f-113">Attribute</span></span>|<span data-ttu-id="c0c4f-114">Description</span><span class="sxs-lookup"><span data-stu-id="c0c4f-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c0c4f-115">mode</span><span class="sxs-lookup"><span data-stu-id="c0c4f-115">mode</span></span>|<span data-ttu-id="c0c4f-116">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-116">Optional.</span></span> <span data-ttu-id="c0c4f-117">Spécifie le type de sécurité utilisé par les homologues configurés avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-117">Specifies the type of security used by peers configured with this binding.</span></span> <span data-ttu-id="c0c4f-118">La valeur par défaut est `Message`.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-118">The default value is `Message`.</span></span> <span data-ttu-id="c0c4f-119">Cet attribut est de type <xref:System.ServiceModel.SecurityMode>.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-119">This attribute is of type <xref:System.ServiceModel.SecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="c0c4f-120">Attribut Mode</span><span class="sxs-lookup"><span data-stu-id="c0c4f-120">mode Attribute</span></span>  
  
|<span data-ttu-id="c0c4f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0c4f-121">Value</span></span>|<span data-ttu-id="c0c4f-122">Description</span><span class="sxs-lookup"><span data-stu-id="c0c4f-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="c0c4f-123">Message</span><span class="sxs-lookup"><span data-stu-id="c0c4f-123">Message</span></span>|<span data-ttu-id="c0c4f-124">La sécurité SOAP assure l'authentification, l'intégrité et la confidentialité.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-124">SOAP security provides authentication, integrity and confidentiality.</span></span>|  
|<span data-ttu-id="c0c4f-125">None</span><span class="sxs-lookup"><span data-stu-id="c0c4f-125">None</span></span>|<span data-ttu-id="c0c4f-126">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-126">Security is disabled.</span></span>|  
|<span data-ttu-id="c0c4f-127">Transport</span><span class="sxs-lookup"><span data-stu-id="c0c4f-127">Transport</span></span>|<span data-ttu-id="c0c4f-128">La sécurité est fournie à l'aide de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-128">Security is provided using HTTPS.</span></span>|  
|<span data-ttu-id="c0c4f-129">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="c0c4f-129">TransportWithMessageCredential</span></span>|<span data-ttu-id="c0c4f-130">Le protocole HTTPS assure l'authentification et la confidentialité.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-130">HTTPS provides authentication and confidentiality.</span></span> <span data-ttu-id="c0c4f-131">Les messages SOAP fournissent des types d'informations d'identification enrichies.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-131">SOAP messages provide rich credential types.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c0c4f-132">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c0c4f-132">Child Elements</span></span>  
  
|<span data-ttu-id="c0c4f-133">Élément</span><span class="sxs-lookup"><span data-stu-id="c0c4f-133">Element</span></span>|<span data-ttu-id="c0c4f-134">Description</span><span class="sxs-lookup"><span data-stu-id="c0c4f-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c0c4f-135">\<transport></span><span class="sxs-lookup"><span data-stu-id="c0c4f-135">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-netpeertcpbinding.md)|<span data-ttu-id="c0c4f-136">Définit le type de transport pour les messages sécurisés envoyés par des homologues configurés avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-136">Defines the transport type for secured messages sent by peers configured with this binding.</span></span> <span data-ttu-id="c0c4f-137">Cet élément est de type <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-137">This element is of type <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c0c4f-138">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c0c4f-138">Parent Elements</span></span>  
  
|<span data-ttu-id="c0c4f-139">Élément</span><span class="sxs-lookup"><span data-stu-id="c0c4f-139">Element</span></span>|<span data-ttu-id="c0c4f-140">Description</span><span class="sxs-lookup"><span data-stu-id="c0c4f-140">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c0c4f-141">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="c0c4f-141">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="c0c4f-142">Définit toutes les fonctions de liaison de la [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="c0c4f-142">Defines all binding capabilities of the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c0c4f-143">Notes</span><span class="sxs-lookup"><span data-stu-id="c0c4f-143">Remarks</span></span>  
 <span data-ttu-id="c0c4f-144">La sécurité peut être spécifique au message ou au transport.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-144">Security can be either message- or transport-specific.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0c4f-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0c4f-145">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerSecurityElement>  
 <xref:System.ServiceModel.NetPeerTcpBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.NetPeerTcpBindingElement.Security%2A>  
 <xref:System.ServiceModel.PeerSecuritySettings>  
 [<span data-ttu-id="c0c4f-146">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="c0c4f-146">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="c0c4f-147">Sélection d’un type d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="c0c4f-147">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)  
 [<span data-ttu-id="c0c4f-148">Liaisons</span><span class="sxs-lookup"><span data-stu-id="c0c4f-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="c0c4f-149">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="c0c4f-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="c0c4f-150">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="c0c4f-150">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="c0c4f-151">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="c0c4f-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
