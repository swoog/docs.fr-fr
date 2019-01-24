---
title: '&lt;transport&gt; de &lt;wsHttpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 21e38acf-450a-4bda-82b6-de305e1f7cd8
ms.openlocfilehash: a759f74e923c9d81391abf82fa08491f3b31c990
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54517949"
---
# <a name="lttransportgt-of-ltwshttpbindinggt"></a><span data-ttu-id="da726-102">&lt;transport&gt; de &lt;wsHttpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="da726-102">&lt;transport&gt; of &lt;wsHttpBinding&gt;</span></span>
<span data-ttu-id="da726-103">Définit les paramètres d'authentification correspondant au transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="da726-103">Defines authentication settings for the HTTP transport.</span></span>  
  
 <span data-ttu-id="da726-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="da726-104">\<system.serviceModel></span></span>  
<span data-ttu-id="da726-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="da726-105">\<bindings></span></span>  
<span data-ttu-id="da726-106">\<wsHttpBinding></span><span class="sxs-lookup"><span data-stu-id="da726-106">\<wsHttpBinding></span></span>  
<span data-ttu-id="da726-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="da726-107">\<binding></span></span>  
<span data-ttu-id="da726-108">\<security></span><span class="sxs-lookup"><span data-stu-id="da726-108">\<security></span></span>  
<span data-ttu-id="da726-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="da726-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="da726-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da726-110">Syntax</span></span>  
  
```xml  
<wsHttpBinding>
  <binding>
    <security mode="None|Transport|TransportWithMessageCredential|TransportCredentialOnly">
      <transport clientCredentialType="Basic|Certificate|Digest|None|Ntlm|Windows"
                 proxyCredentialType="Basic|Digest|None|Ntlm|Windows"
                 realm="string" />
        <extendedProtectionPolicy policyEnforcement="Never|WhenSupported|Always"
                                  protectionScenario="TransportSelected|TrustedProxy">
          <customServiceNames>
          </customServiceNames>
        </extendedProtecutionPolicy>
      </transport>
    </security>
  </binding>
</wsHttpBinding>
```  
  
## <a name="type"></a><span data-ttu-id="da726-111">Type</span><span class="sxs-lookup"><span data-stu-id="da726-111">Type</span></span>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="da726-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="da726-112">Attributes and Elements</span></span>  
 <span data-ttu-id="da726-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="da726-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="da726-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="da726-114">Attributes</span></span>  
  
|<span data-ttu-id="da726-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="da726-115">Attribute</span></span>|<span data-ttu-id="da726-116">Description</span><span class="sxs-lookup"><span data-stu-id="da726-116">Description</span></span>|  
|---------------|-----------------|  
|`clientCredentialType`|<span data-ttu-id="da726-117">Spécifie les informations d'identification utilisées pour authentifier le client auprès du service.</span><span class="sxs-lookup"><span data-stu-id="da726-117">Specifies the credential used to authenticate the client to the service.</span></span> <span data-ttu-id="da726-118">Cet attribut est de type <xref:System.ServiceModel.HttpClientCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="da726-118">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|`proxyCredentialType`|<span data-ttu-id="da726-119">Spécifie les informations d'identification utilisées pour authentifier le client auprès d'un proxy de domaine.</span><span class="sxs-lookup"><span data-stu-id="da726-119">Specifies the credential used to authenticate the client to a domain proxy.</span></span> <span data-ttu-id="da726-120">Cet attribut est de type <xref:System.ServiceModel.HttpProxyCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="da726-120">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|`realm`|<span data-ttu-id="da726-121">Chaîne indiquant le domaine de l'authentification de base ou Digest.</span><span class="sxs-lookup"><span data-stu-id="da726-121">A string that specifies the authentication realm for digest or basic authentication.</span></span> <span data-ttu-id="da726-122">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="da726-122">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="da726-123">Un domaine d'authentification spécifie au moins le nom de l'hôte qui exécute l'authentification.</span><span class="sxs-lookup"><span data-stu-id="da726-123">An authentication realm specifies at least the name of the host that performs the authentication.</span></span> <span data-ttu-id="da726-124">Il peut également spécifier une collection d'utilisateurs disposant d'un accès.</span><span class="sxs-lookup"><span data-stu-id="da726-124">It can also specify a collection of users that has access.</span></span> <span data-ttu-id="da726-125">Un utilisateur peut interroger le domaine d'authentification pour vérifier quels noms d'utilisateurs et mots de passe peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="da726-125">A user can query the authentication realm to ascertain which one of the several possible usernames and passwords can be used.</span></span>|  
|`policyEnforcement`|<span data-ttu-id="da726-126">Cette énumération spécifie à quel moment <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> doit être appliqué.</span><span class="sxs-lookup"><span data-stu-id="da726-126">This enumeration specifies when the <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> should be enforced.</span></span><br /><br /> <span data-ttu-id="da726-127">1.  Never : la stratégie n'est jamais appliquée (la protection étendue est désactivée).</span><span class="sxs-lookup"><span data-stu-id="da726-127">1.  Never – The policy is never enforced (Extended Protection is disabled).</span></span><br /><span data-ttu-id="da726-128">2.  WhenSupported : la stratégie est appliquée uniquement si le client prend en charge la protection étendue.</span><span class="sxs-lookup"><span data-stu-id="da726-128">2.  WhenSupported – The policy is enforced only if the client supports Extended Protection.</span></span><br /><span data-ttu-id="da726-129">3.  Always : la stratégie est toujours appliquée.</span><span class="sxs-lookup"><span data-stu-id="da726-129">3.  Always – The policy is always enforced.</span></span> <span data-ttu-id="da726-130">Les clients qui ne prennent pas en charge la protection étendue ne pourront pas être authentifiés.</span><span class="sxs-lookup"><span data-stu-id="da726-130">Clients which don’t support Extended Protection will fail to authenticate.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="da726-131">Attribut clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="da726-131">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="da726-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="da726-132">Value</span></span>|<span data-ttu-id="da726-133">Description</span><span class="sxs-lookup"><span data-stu-id="da726-133">Description</span></span>|  
|-----------|-----------------|  
|`None`|<span data-ttu-id="da726-134">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="da726-134">Security is disabled.</span></span>|  
|`Basic`|<span data-ttu-id="da726-135">Utilise l'authentification de base.</span><span class="sxs-lookup"><span data-stu-id="da726-135">Uses basic authentication.</span></span>|  
|`Digest`|<span data-ttu-id="da726-136">Utilise l'authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="da726-136">Uses digest authentication.</span></span>|  
|`Ntlm`|<span data-ttu-id="da726-137">Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="da726-137">Uses NTLM authentication as a fallback with a Windows domain.</span></span>|  
|`Windows`|<span data-ttu-id="da726-138">Utilise l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="da726-138">Uses integrated Windows authentication.</span></span>|  
|`Certificate`|<span data-ttu-id="da726-139">Utilise des certificats X.509 pour authentifier le client.</span><span class="sxs-lookup"><span data-stu-id="da726-139">Uses X.509 certificates to authenticate the client.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="da726-140">Attribut proxyCredentialType</span><span class="sxs-lookup"><span data-stu-id="da726-140">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="da726-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="da726-141">Value</span></span>|<span data-ttu-id="da726-142">Description</span><span class="sxs-lookup"><span data-stu-id="da726-142">Description</span></span>|  
|-----------|-----------------|  
|`None`|<span data-ttu-id="da726-143">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="da726-143">Security is disabled.</span></span>|  
|`Basic`|<span data-ttu-id="da726-144">Utilise l'authentification de base.</span><span class="sxs-lookup"><span data-stu-id="da726-144">Uses basic authentication.</span></span>|  
|`Digest`|<span data-ttu-id="da726-145">Utilise l'authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="da726-145">Uses digest authentication.</span></span>|  
|`Ntlm`|<span data-ttu-id="da726-146">Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="da726-146">Uses NTLM as a fallback with a Windows domain.</span></span>|  
|`Windows`|<span data-ttu-id="da726-147">Utilise l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="da726-147">Uses integrated Windows authentication.</span></span>|  
|`Certificate`|<span data-ttu-id="da726-148">Utilise des certificats X.509 pour authentifier le client.</span><span class="sxs-lookup"><span data-stu-id="da726-148">Uses X.509 certificates to authenticate the client.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="da726-149">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="da726-149">Child Elements</span></span>  
 <span data-ttu-id="da726-150">Aucun.</span><span class="sxs-lookup"><span data-stu-id="da726-150">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="da726-151">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="da726-151">Parent Elements</span></span>  
  
|<span data-ttu-id="da726-152">Élément</span><span class="sxs-lookup"><span data-stu-id="da726-152">Element</span></span>|<span data-ttu-id="da726-153">Description</span><span class="sxs-lookup"><span data-stu-id="da726-153">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="da726-154">\<security></span><span class="sxs-lookup"><span data-stu-id="da726-154">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-wshttpbinding.md)|<span data-ttu-id="da726-155">Représente les fonctionnalités de sécurité de la [ \<wsHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="da726-155">Represents the security capabilities of the [\<wsHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="da726-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da726-156">See also</span></span>
- <xref:System.ServiceModel.HttpTransportSecurity>
- <xref:System.ServiceModel.WSHttpSecurity.Transport%2A>
- <xref:System.ServiceModel.Configuration.WSHttpSecurityElement.Transport%2A>
- <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>
- [<span data-ttu-id="da726-157">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="da726-157">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="da726-158">Liaisons</span><span class="sxs-lookup"><span data-stu-id="da726-158">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="da726-159">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="da726-159">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="da726-160">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="da726-160">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="da726-161">\<binding></span><span class="sxs-lookup"><span data-stu-id="da726-161">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
