---
title: '&lt;security&gt; de &lt;webHttpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 727cf3d2-6f56-48ad-a59f-ba423edb9c83
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 52146fa08ec63ef63fa996cdc09f9185b9f42e02
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43489680"
---
# <a name="ltsecuritygt-of-ltwebhttpbindinggt"></a><span data-ttu-id="a63c7-102">&lt;security&gt; de &lt;webHttpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="a63c7-102">&lt;security&gt; of &lt;webHttpBinding&gt;</span></span>
<span data-ttu-id="a63c7-103">Spécifie les exigences de sécurité pour un point de terminaison configuré avec un [ \<wsHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="a63c7-103">Specifies the security requirements for an endpoint configured with a [\<wsHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md).</span></span>  
  
 <span data-ttu-id="a63c7-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="a63c7-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="a63c7-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="a63c7-105">\<bindings></span></span>  
<span data-ttu-id="a63c7-106">\<webHttpBinding></span><span class="sxs-lookup"><span data-stu-id="a63c7-106">\<webHttpBinding></span></span>  
<span data-ttu-id="a63c7-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="a63c7-107">\<binding></span></span>  
<span data-ttu-id="a63c7-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="a63c7-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a63c7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a63c7-109">Syntax</span></span>  
  
```xml  
<system.ServiceModel>  
    <bindings>  
        <webHttpBinding>  
            <binding name = "string">  
              <security mode="None/Transport/TransportCredentialOnly">  
                                    <transport clientCredentialType =   
                                     "Basic/Certificate/Digest/None/Ntlm/Windows"  
                                     proxyCredentialType="Basic/Digest/None/Ntlm/Windows"  
                                     realm="string" />  
              </security>  
        </webHttpBinding>  
    </bindings>  
</system.ServiceModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a63c7-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a63c7-110">Attributes and Elements</span></span>  
 <span data-ttu-id="a63c7-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a63c7-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a63c7-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="a63c7-112">Attributes</span></span>  
  
|<span data-ttu-id="a63c7-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="a63c7-113">Attribute</span></span>|<span data-ttu-id="a63c7-114">Description</span><span class="sxs-lookup"><span data-stu-id="a63c7-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a63c7-115">mode</span><span class="sxs-lookup"><span data-stu-id="a63c7-115">mode</span></span>|<span data-ttu-id="a63c7-116">Indique si un point de terminaison utilise la sécurité au niveau du transport ou s'il n'utilise aucune sécurité.</span><span class="sxs-lookup"><span data-stu-id="a63c7-116">Specifies whether transport-level security or no security is used by an endpoint.</span></span> <span data-ttu-id="a63c7-117">La valeur par défaut est `None`.</span><span class="sxs-lookup"><span data-stu-id="a63c7-117">The default is `None`.</span></span> <span data-ttu-id="a63c7-118">Cet attribut est de type <xref:System.ServiceModel.WebHttpSecurityMode>.</span><span class="sxs-lookup"><span data-stu-id="a63c7-118">This attribute is of type <xref:System.ServiceModel.WebHttpSecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="a63c7-119">Mode, attribut</span><span class="sxs-lookup"><span data-stu-id="a63c7-119">Mode Attribute</span></span>  
  
|<span data-ttu-id="a63c7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a63c7-120">Value</span></span>|<span data-ttu-id="a63c7-121">Description</span><span class="sxs-lookup"><span data-stu-id="a63c7-121">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="a63c7-122">None</span><span class="sxs-lookup"><span data-stu-id="a63c7-122">None</span></span>|<span data-ttu-id="a63c7-123">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a63c7-123">Security is disabled.</span></span>|  
|<span data-ttu-id="a63c7-124">Transport</span><span class="sxs-lookup"><span data-stu-id="a63c7-124">Transport</span></span>|<span data-ttu-id="a63c7-125">La sécurité est fournie à l'aide de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a63c7-125">Security is provided using HTTPS.</span></span> <span data-ttu-id="a63c7-126">Le service doit être configuré avec les certificats SSL.</span><span class="sxs-lookup"><span data-stu-id="a63c7-126">The service needs to be configured with SSL certificates.</span></span> <span data-ttu-id="a63c7-127">Le message est entièrement sécurisé à l’aide du protocole HTTPS et le service est authentifié par le client à l’aide du certificat SSL du service.</span><span class="sxs-lookup"><span data-stu-id="a63c7-127">The message is entirely secured using HTTPS and the service is authenticated by the client using the service’s SSL certificate.</span></span> <span data-ttu-id="a63c7-128">L’authentification du client est contrôlée par le `ClientCredentialType` attribut de la [ \<transport >](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-webhttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="a63c7-128">The client authentication is controlled through the `ClientCredentialType` attribute of the [\<transport>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-webhttpbinding.md).</span></span>|  
|<span data-ttu-id="a63c7-129">TransportCredentialOnly</span><span class="sxs-lookup"><span data-stu-id="a63c7-129">TransportCredentialOnly</span></span>|<span data-ttu-id="a63c7-130">Ce mode n'assure pas l'intégrité et la confidentialité des messages.</span><span class="sxs-lookup"><span data-stu-id="a63c7-130">This mode does not provide message integrity and confidentiality.</span></span> <span data-ttu-id="a63c7-131">Il fournit l'authentification du client basée sur le protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="a63c7-131">It provides HTTP-based client authentication.</span></span> <span data-ttu-id="a63c7-132">Ce mode doit être utilisé avec précaution.</span><span class="sxs-lookup"><span data-stu-id="a63c7-132">This mode should be used with caution.</span></span> <span data-ttu-id="a63c7-133">Elle doit être utilisée dans les environnements où la sécurité de transport est fournie par d’autres moyens (tels que IPSec) et seulement l’authentification du client est fournie par l’infrastructure WCF.</span><span class="sxs-lookup"><span data-stu-id="a63c7-133">It should be used in environments where the transport security is being provided by other means (such as IPSec) and only client authentication is provided by the WCF infrastructure.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a63c7-134">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a63c7-134">Child Elements</span></span>  
  
|<span data-ttu-id="a63c7-135">Élément</span><span class="sxs-lookup"><span data-stu-id="a63c7-135">Element</span></span>|<span data-ttu-id="a63c7-136">Description</span><span class="sxs-lookup"><span data-stu-id="a63c7-136">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a63c7-137">\<transport></span><span class="sxs-lookup"><span data-stu-id="a63c7-137">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-webhttpbinding.md)|<span data-ttu-id="a63c7-138">Définit les paramètres de sécurité de transport.</span><span class="sxs-lookup"><span data-stu-id="a63c7-138">Defines the transport security settings.</span></span> <span data-ttu-id="a63c7-139">Cet élément correspond au type <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="a63c7-139">This element corresponds to the <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement> type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a63c7-140">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a63c7-140">Parent Elements</span></span>  
  
|<span data-ttu-id="a63c7-141">Élément</span><span class="sxs-lookup"><span data-stu-id="a63c7-141">Element</span></span>|<span data-ttu-id="a63c7-142">Description</span><span class="sxs-lookup"><span data-stu-id="a63c7-142">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a63c7-143">\<webHttpBinding></span><span class="sxs-lookup"><span data-stu-id="a63c7-143">\<webHttpBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md)|<span data-ttu-id="a63c7-144">Un élément de liaison qui est utilisé pour configurer les points de terminaison Windows Communication Foundation (WCF) Web services qui répondent aux requêtes HTTP au lieu de messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="a63c7-144">A binding element that is used to configure endpoints for Windows Communication Foundation (WCF) Web services that respond to HTTP requests instead of SOAP messages.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a63c7-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a63c7-145">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.WebHttpBindingElement>  
 <xref:System.ServiceModel.Configuration.WSHttpSecurityElement>  
 <xref:System.ServiceModel.WebHttpBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.WebHttpBindingElement.Security%2A>  
 <xref:System.ServiceModel.WebHttpSecurity>  
 [<span data-ttu-id="a63c7-146">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="a63c7-146">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="a63c7-147">Sélection d’un type d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="a63c7-147">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)  
 [<span data-ttu-id="a63c7-148">Liaisons</span><span class="sxs-lookup"><span data-stu-id="a63c7-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="a63c7-149">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="a63c7-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="a63c7-150">Utilisation de liaisons pour configurer les Clients et les Services Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="a63c7-150">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="a63c7-151">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="a63c7-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)  
 [<span data-ttu-id="a63c7-152">Modèle de programmation HTTP web WCF</span><span class="sxs-lookup"><span data-stu-id="a63c7-152">WCF Web HTTP Programming Model</span></span>](../../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md)
