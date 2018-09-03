---
title: '&lt;security&gt; de &lt;wsHttpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 8658b162-2ddf-4162-a869-aa517a42288a
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: de2fc0f562b079d5310ed2cd81211e14d4257515
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43468544"
---
# <a name="ltsecuritygt-of-ltwshttpbindinggt"></a><span data-ttu-id="2b2b8-102">&lt;security&gt; de &lt;wsHttpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="2b2b8-102">&lt;security&gt; of &lt;wsHttpBinding&gt;</span></span>
<span data-ttu-id="2b2b8-103">Représente les fonctionnalités de sécurité de la [ \<wsHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="2b2b8-103">Represents the security capabilities of the [\<wsHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md).</span></span>  
  
 <span data-ttu-id="2b2b8-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="2b2b8-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="2b2b8-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="2b2b8-105">\<bindings></span></span>  
<span data-ttu-id="2b2b8-106">\<wsHttpBinding></span><span class="sxs-lookup"><span data-stu-id="2b2b8-106">\<wsHttpBinding></span></span>  
<span data-ttu-id="2b2b8-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="2b2b8-107">\<binding></span></span>  
<span data-ttu-id="2b2b8-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="2b2b8-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b2b8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b2b8-109">Syntax</span></span>  
  
```xml  
<security mode="Message/None/Transport/TransportWithMessageCredential">  
   <transport  
         clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"  
      proxyCredentialType="Basic/Digest/None/Ntlm/Windows"  
      realm="string"   
      defaultClientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"  
      defaultProxyCredentialType="Basic/Digest/None/Ntlm/Windows"  
      defaultRealm="string" />  
   <message  
            clientCredentialType="Certificate/IssuedToken/None/UserName/Windows"  
      algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
       establishSecurityContext="Boolean"   
      negotiateServiceCredential="Boolean"/>  
</security>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2b2b8-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="2b2b8-110">Attributes and Elements</span></span>  
 <span data-ttu-id="2b2b8-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-111">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2b2b8-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="2b2b8-112">Attributes</span></span>  
  
|<span data-ttu-id="2b2b8-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="2b2b8-113">Attribute</span></span>|<span data-ttu-id="2b2b8-114">Description</span><span class="sxs-lookup"><span data-stu-id="2b2b8-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2b2b8-115">mode</span><span class="sxs-lookup"><span data-stu-id="2b2b8-115">mode</span></span>|<span data-ttu-id="2b2b8-116">-Facultatif.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-116">-   Optional.</span></span> <span data-ttu-id="2b2b8-117">Spécifie le type de sécurité appliqué.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-117">Specifies the type of security that is applied.</span></span> <span data-ttu-id="2b2b8-118">La valeur par défaut est `Message`.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-118">The default is `Message`.</span></span><br /><span data-ttu-id="2b2b8-119">-Cet attribut est de type <xref:System.ServiceModel.SecurityMode>.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-119">-   This attribute is of type <xref:System.ServiceModel.SecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="2b2b8-120">Mode, attribut</span><span class="sxs-lookup"><span data-stu-id="2b2b8-120">Mode Attribute</span></span>  
  
|<span data-ttu-id="2b2b8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b2b8-121">Value</span></span>|<span data-ttu-id="2b2b8-122">Description</span><span class="sxs-lookup"><span data-stu-id="2b2b8-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="2b2b8-123">None</span><span class="sxs-lookup"><span data-stu-id="2b2b8-123">None</span></span>|<span data-ttu-id="2b2b8-124">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-124">Security is disabled.</span></span>|  
|<span data-ttu-id="2b2b8-125">Transport</span><span class="sxs-lookup"><span data-stu-id="2b2b8-125">Transport</span></span>|<span data-ttu-id="2b2b8-126">La sécurité est fournie à l'aide de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-126">Security is provided using HTTPS.</span></span> <span data-ttu-id="2b2b8-127">Le service doit être configuré avec les certificats SSL.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-127">The service needs to be configured with SSL certificates.</span></span> <span data-ttu-id="2b2b8-128">Le message est entièrement sécurisé grâce à HTTPS et est authentifié par le client à l'aide du certificat SSL du service.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-128">The message is entirely secured using HTTPS and is authenticated by the client using the service’s SSL certificate.</span></span> <span data-ttu-id="2b2b8-129">L'authentification du client est contrôlée à l'aide de l'attribut `ClientCredentials`.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-129">The client authentication is controlled through the `ClientCredentials` attribute.</span></span> <span data-ttu-id="2b2b8-130">de la [ \<transport >](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-wshttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="2b2b8-130">of the [\<transport>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-wshttpbinding.md).</span></span>|  
|<span data-ttu-id="2b2b8-131">Message</span><span class="sxs-lookup"><span data-stu-id="2b2b8-131">Message</span></span>|<span data-ttu-id="2b2b8-132">La sécurité est fournie à l'aide de la sécurité des messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-132">Security is provided using SOAP message security.</span></span> <span data-ttu-id="2b2b8-133">Par défaut, le corps SOAP est chiffré et signé.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-133">By default, the SOAP body is Encrypted and Signed.</span></span> <span data-ttu-id="2b2b8-134">Ce mode offre diverses fonctionnalités, telles que, si les informations d'identification du service sont disponibles au client hors bande, la suite algorithmique à utiliser et quel niveau de protection à appliquer au corps du message grâce à la propriété Security.Message.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-134">This mode offers a variety of features, such as whether the service credentials are available at the client out of band, the algorithm suite to use, and what level of protection to apply to the message body through the Security.Message property.</span></span> <span data-ttu-id="2b2b8-135">L'authentification du client est exécutée une fois par session et les résultats d'authentification sont mis en cache pour la durée de la session.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-135">Client authentication is performed once per session and the results of authentication are cached for the duration of the session.</span></span>|  
|<span data-ttu-id="2b2b8-136">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="2b2b8-136">TransportWithMessageCredential</span></span>|<span data-ttu-id="2b2b8-137">Dans ce mode, le protocole HTTPS garantit l'intégrité, la confidentialité et l'authentification du serveur, et la sécurité des messages SOAP garantit l'authentification du client.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-137">In this mode, HTTPS provides integrity, confidentiality, and server authentication, and SOAP message security provides client authentication.</span></span> <span data-ttu-id="2b2b8-138">Par défaut, l'authentification du client est exécutée une fois par session et les résultats d'authentification sont mis en cache pour la durée de la session.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-138">By default, client authentication is performed once per session and the results of authentication are cached for the duration of the session.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2b2b8-139">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2b2b8-139">Child Elements</span></span>  
  
|<span data-ttu-id="2b2b8-140">Élément</span><span class="sxs-lookup"><span data-stu-id="2b2b8-140">Element</span></span>|<span data-ttu-id="2b2b8-141">Description</span><span class="sxs-lookup"><span data-stu-id="2b2b8-141">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2b2b8-142">\<transport></span><span class="sxs-lookup"><span data-stu-id="2b2b8-142">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-wshttpbinding.md)|<span data-ttu-id="2b2b8-143">Définit les paramètres de sécurité de transport.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-143">Defines the transport security settings.</span></span> <span data-ttu-id="2b2b8-144">Cet élément correspond au type <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-144">This element corresponds to the <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement> type.</span></span>|  
|[<span data-ttu-id="2b2b8-145">\<message></span><span class="sxs-lookup"><span data-stu-id="2b2b8-145">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-wshttpbinding.md)|<span data-ttu-id="2b2b8-146">Définit les paramètres de sécurité pour le message.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-146">Defines the security settings for the message.</span></span> <span data-ttu-id="2b2b8-147">Cet élément correspond au type <xref:System.ServiceModel.Configuration.MessageSecurityOverHttpElement>.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-147">This element corresponds to the <xref:System.ServiceModel.Configuration.MessageSecurityOverHttpElement> type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2b2b8-148">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2b2b8-148">Parent Elements</span></span>  
  
|<span data-ttu-id="2b2b8-149">Élément</span><span class="sxs-lookup"><span data-stu-id="2b2b8-149">Element</span></span>|<span data-ttu-id="2b2b8-150">Description</span><span class="sxs-lookup"><span data-stu-id="2b2b8-150">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2b2b8-151">\<wsHttpBinding></span><span class="sxs-lookup"><span data-stu-id="2b2b8-151">\<wsHttpBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md)|<span data-ttu-id="2b2b8-152">Liaison sécurisée pour les applications de transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-152">A secure binding for HTTP transport applications.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2b2b8-153">Notes</span><span class="sxs-lookup"><span data-stu-id="2b2b8-153">Remarks</span></span>  
 <span data-ttu-id="2b2b8-154">La classe WSHttpBinding est conçue pour interagir avec les services qui implémentent les spécifications WS-\*.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-154">The WSHttpBinding class is designed for interoperation with services that implement WS-\* specifications.</span></span> <span data-ttu-id="2b2b8-155">La sécurité de transport de cette liaison correspond à Secure Sockets Layer (SSL) sur HTTP, c’est-à-dire à HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2b2b8-155">The transport security for this binding is Secure Sockets Layer (SSL) over HTTP, or HTTPS.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b2b8-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b2b8-156">See Also</span></span>  
 <xref:System.ServiceModel.WSHttpSecurity>  
 <xref:System.ServiceModel.WSHttpBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.WSHttpBindingElement.Security%2A>  
 <xref:System.ServiceModel.Configuration.WSHttpSecurityElement>  
 [<span data-ttu-id="2b2b8-157">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="2b2b8-157">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="2b2b8-158">Liaisons</span><span class="sxs-lookup"><span data-stu-id="2b2b8-158">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="2b2b8-159">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="2b2b8-159">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="2b2b8-160">Utilisation de liaisons pour configurer les Clients et les Services Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="2b2b8-160">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="2b2b8-161">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="2b2b8-161">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
