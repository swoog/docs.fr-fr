---
title: '&lt;security&gt; de &lt;basicHttpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 6432708d-5465-4bd9-bfc2-466742db99cb
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: e39d32a9cc689905bed42f56e4f998bbd8c6e038
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33355026"
---
# <a name="ltsecuritygt-of-ltbasichttpbindinggt"></a><span data-ttu-id="017e0-102">&lt;security&gt; de &lt;basicHttpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="017e0-102">&lt;security&gt; of &lt;basicHttpBinding&gt;</span></span>
<span data-ttu-id="017e0-103">Définit les fonctionnalités de sécurité le [ \<basicHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="017e0-103">Defines the security capabilities of the [\<basicHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span></span>  
  
 <span data-ttu-id="017e0-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="017e0-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="017e0-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="017e0-105">\<bindings></span></span>  
<span data-ttu-id="017e0-106">\<basicHttpBinding></span><span class="sxs-lookup"><span data-stu-id="017e0-106">\<basicHttpBinding></span></span>  
<span data-ttu-id="017e0-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="017e0-107">\<binding></span></span>  
<span data-ttu-id="017e0-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="017e0-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="017e0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="017e0-109">Syntax</span></span>  
  
```xml  
<security mode="Message/None/Transport/TransportWithCredential">  
   <transport  
      clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"  
      proxyCredentialType="Basic/Digest/None/Ntlm/Windows"  
      realm="string" />  
   <message  
      algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
            clientCredentialType="Certificate/IssuedToken/None/UserName/Windows" />  
</security>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="017e0-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="017e0-110">Attributes and Elements</span></span>  
 <span data-ttu-id="017e0-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="017e0-111">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="017e0-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="017e0-112">Attributes</span></span>  
  
|<span data-ttu-id="017e0-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="017e0-113">Attribute</span></span>|<span data-ttu-id="017e0-114">Description</span><span class="sxs-lookup"><span data-stu-id="017e0-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="017e0-115">mode</span><span class="sxs-lookup"><span data-stu-id="017e0-115">mode</span></span>|<span data-ttu-id="017e0-116">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="017e0-116">Optional.</span></span> <span data-ttu-id="017e0-117">Spécifie le type de sécurité qui est utilisé.</span><span class="sxs-lookup"><span data-stu-id="017e0-117">Specifies the type of security that is used.</span></span> <span data-ttu-id="017e0-118">La valeur par défaut est `None`.</span><span class="sxs-lookup"><span data-stu-id="017e0-118">The default is `None`.</span></span> <span data-ttu-id="017e0-119">Cet attribut est de type <xref:System.ServiceModel.BasicHttpSecurityMode>.</span><span class="sxs-lookup"><span data-stu-id="017e0-119">This attribute is of type <xref:System.ServiceModel.BasicHttpSecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="017e0-120">Attribut Mode</span><span class="sxs-lookup"><span data-stu-id="017e0-120">mode Attribute</span></span>  
  
|<span data-ttu-id="017e0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="017e0-121">Value</span></span>|<span data-ttu-id="017e0-122">Description</span><span class="sxs-lookup"><span data-stu-id="017e0-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="017e0-123">Aucun</span><span class="sxs-lookup"><span data-stu-id="017e0-123">None</span></span>|<span data-ttu-id="017e0-124">-Les messages ne sont pas sécurisés pendant le transfert.</span><span class="sxs-lookup"><span data-stu-id="017e0-124">-   Messages are not secured during transfer.</span></span>|  
|<span data-ttu-id="017e0-125">Transport</span><span class="sxs-lookup"><span data-stu-id="017e0-125">Transport</span></span>|<span data-ttu-id="017e0-126">La sécurité est fournie à l'aide du transport HTTPS.</span><span class="sxs-lookup"><span data-stu-id="017e0-126">Security is provided using HTTPS transport.</span></span> <span data-ttu-id="017e0-127">Les messages SOAP sont sécurisés par HTTPS.</span><span class="sxs-lookup"><span data-stu-id="017e0-127">The SOAP messages are secured using HTTPS.</span></span> <span data-ttu-id="017e0-128">Le service est authentifié auprès du client à l'aide du certificat X.509 du service.</span><span class="sxs-lookup"><span data-stu-id="017e0-128">The service is authenticated to the client using the service's X.509 certificate.</span></span> <span data-ttu-id="017e0-129">Le client est authentifié à l'aide du ClientCredentialType fourni.</span><span class="sxs-lookup"><span data-stu-id="017e0-129">The client is authenticated using the ClientCredentialType supplied.</span></span> <span data-ttu-id="017e0-130">Consultez le [ \<transport >](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-basichttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="017e0-130">See the [\<transport>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-basichttpbinding.md).</span></span>|  
|<span data-ttu-id="017e0-131">Message</span><span class="sxs-lookup"><span data-stu-id="017e0-131">Message</span></span>|<span data-ttu-id="017e0-132">La sécurité est fournie à l'aide de la sécurité des messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="017e0-132">Security is provided using SOAP message security.</span></span> <span data-ttu-id="017e0-133">Par défaut, le corps est chiffré et signé.</span><span class="sxs-lookup"><span data-stu-id="017e0-133">By default, the body is encrypted and signed.</span></span> <span data-ttu-id="017e0-134">Pour cette liaison, le système impose que le certificat de serveur soit fourni au client hors bande.</span><span class="sxs-lookup"><span data-stu-id="017e0-134">For this binding, the system requires that the server certificate be provided to the client out of band.</span></span> <span data-ttu-id="017e0-135">Le seul `ClientCredentialType` valide pour cette liaison est `Certificate`.</span><span class="sxs-lookup"><span data-stu-id="017e0-135">The only valid `ClientCredentialType` for this binding is `Certificate`.</span></span>|  
|<span data-ttu-id="017e0-136">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="017e0-136">TransportWithMessageCredential</span></span>|<span data-ttu-id="017e0-137">L'intégrité, la confidentialité et l'authentification de serveur sont fournies par la sécurité du transport.</span><span class="sxs-lookup"><span data-stu-id="017e0-137">Integrity, confidentiality and server authentication are provided by transport security.</span></span> <span data-ttu-id="017e0-138">L'authentification du client est fournie au moyen de la sécurité des messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="017e0-138">Client authentication is provided by means of SOAP message security.</span></span> <span data-ttu-id="017e0-139">Ce mode est utile lorsque l'utilisateur effectue une authentification à l'aide du nom d'utilisateur/mot de passe et qu'il existe un déploiement HTTP pour sécuriser le transfert des messages.</span><span class="sxs-lookup"><span data-stu-id="017e0-139">This mode is relevant when the user is authenticating using username/password and there is an existing HTTP deployment for securing message transfer.</span></span>|  
|<span data-ttu-id="017e0-140">TransportCredentialOnly</span><span class="sxs-lookup"><span data-stu-id="017e0-140">TransportCredentialOnly</span></span>|<span data-ttu-id="017e0-141">Ce mode n'assure pas l'intégrité et la confidentialité des messages.</span><span class="sxs-lookup"><span data-stu-id="017e0-141">This mode does not provide message integrity and confidentiality.</span></span> <span data-ttu-id="017e0-142">Il fournit l'authentification du client basée sur http.</span><span class="sxs-lookup"><span data-stu-id="017e0-142">It provides http-based client authentication.</span></span> <span data-ttu-id="017e0-143">Ce mode doit être utilisé avec précaution.</span><span class="sxs-lookup"><span data-stu-id="017e0-143">This mode should be used with caution.</span></span> <span data-ttu-id="017e0-144">Elle doit être utilisée dans les environnements où la sécurité de transport est fournie par d’autres moyens (tels que IPSec) et seulement l’authentification du client est fournie par l’infrastructure WCF.</span><span class="sxs-lookup"><span data-stu-id="017e0-144">It should be used in environments where the transport security is being provided by other means (such as IPSec) and only client authentication is provided by the WCF infrastructure.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="017e0-145">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="017e0-145">Child Elements</span></span>  
  
|<span data-ttu-id="017e0-146">Élément</span><span class="sxs-lookup"><span data-stu-id="017e0-146">Element</span></span>|<span data-ttu-id="017e0-147">Description</span><span class="sxs-lookup"><span data-stu-id="017e0-147">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="017e0-148">\<transport></span><span class="sxs-lookup"><span data-stu-id="017e0-148">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-basichttpbinding.md)|<span data-ttu-id="017e0-149">Définit les paramètres de sécurité de transport pour un service HTTP de base.</span><span class="sxs-lookup"><span data-stu-id="017e0-149">Defines the transport security settings for a basic HTTP service.</span></span> <span data-ttu-id="017e0-150">Cet élément correspond à <xref:System.ServiceModel.HttpTransportSecurity>.</span><span class="sxs-lookup"><span data-stu-id="017e0-150">This element corresponds to <xref:System.ServiceModel.HttpTransportSecurity>.</span></span>|  
|[<span data-ttu-id="017e0-151">\<message></span><span class="sxs-lookup"><span data-stu-id="017e0-151">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-basichttpbinding.md)|<span data-ttu-id="017e0-152">Définit les paramètres de sécurité de message pour un service HTTP de base.</span><span class="sxs-lookup"><span data-stu-id="017e0-152">Defines the message security settings for a basic HTTP service.</span></span> <span data-ttu-id="017e0-153">Cet élément correspond à <xref:System.ServiceModel.BasicHttpMessageSecurity>.</span><span class="sxs-lookup"><span data-stu-id="017e0-153">This element corresponds to <xref:System.ServiceModel.BasicHttpMessageSecurity>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="017e0-154">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="017e0-154">Parent Elements</span></span>  
  
|<span data-ttu-id="017e0-155">Élément</span><span class="sxs-lookup"><span data-stu-id="017e0-155">Element</span></span>|<span data-ttu-id="017e0-156">Description</span><span class="sxs-lookup"><span data-stu-id="017e0-156">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="017e0-157">liaison</span><span class="sxs-lookup"><span data-stu-id="017e0-157">binding</span></span>|<span data-ttu-id="017e0-158">L’élément de liaison de la [ \<basicHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="017e0-158">The binding element of the [\<basicHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="017e0-159">Notes</span><span class="sxs-lookup"><span data-stu-id="017e0-159">Remarks</span></span>  
 <span data-ttu-id="017e0-160">Par défaut, le message SOAP n'est pas sécurisé et le client n'est pas authentifié.</span><span class="sxs-lookup"><span data-stu-id="017e0-160">By default, the SOAP message is not secured and the client is not authenticated.</span></span> <span data-ttu-id="017e0-161">Cet élément permet de configurer des paramètres de sécurité supplémentaires pour l'élément `basicHttpBinding`.</span><span class="sxs-lookup"><span data-stu-id="017e0-161">This element enables you to configure additional security settings for the `basicHttpBinding` element.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="017e0-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="017e0-162">See Also</span></span>  
 <xref:System.ServiceModel.BasicHttpBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.BasicHttpBindingElement.Security%2A>  
 <xref:System.ServiceModel.Configuration.BasicHttpSecurityElement>  
 <xref:System.ServiceModel.BasicHttpSecurity>  
 [<span data-ttu-id="017e0-163">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="017e0-163">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="017e0-164">Sélection d’un type d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="017e0-164">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)  
 [<span data-ttu-id="017e0-165">Liaisons</span><span class="sxs-lookup"><span data-stu-id="017e0-165">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="017e0-166">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="017e0-166">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="017e0-167">Utilisation de liaisons pour configurer les Clients et les Services Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="017e0-167">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](http://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="017e0-168">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="017e0-168">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
