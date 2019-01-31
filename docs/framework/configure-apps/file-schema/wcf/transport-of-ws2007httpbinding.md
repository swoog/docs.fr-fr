---
title: <transport> de <ws2007HttpBinding>
ms.date: 03/30/2017
ms.assetid: 692befa3-8b0b-4ec5-b601-755874e98eb0
ms.openlocfilehash: b8f84d0ed6c6248e72e3353675c9da96a0678ae6
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55273304"
---
# <a name="transport-of-ws2007httpbinding"></a><span data-ttu-id="43242-102">\<transport > de \<ws2007HttpBinding ></span><span class="sxs-lookup"><span data-stu-id="43242-102">\<transport> of \<ws2007HttpBinding></span></span>
<span data-ttu-id="43242-103">Définit les paramètres d'authentification correspondant au transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="43242-103">Defines authentication settings for the HTTP transport.</span></span>  
  
 <span data-ttu-id="43242-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="43242-104">\<system.serviceModel></span></span>  
<span data-ttu-id="43242-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="43242-105">\<bindings></span></span>  
<span data-ttu-id="43242-106">\<ws2007HttpBinding></span><span class="sxs-lookup"><span data-stu-id="43242-106">\<ws2007HttpBinding></span></span>  
<span data-ttu-id="43242-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="43242-107">\<binding></span></span>  
<span data-ttu-id="43242-108">\<security></span><span class="sxs-lookup"><span data-stu-id="43242-108">\<security></span></span>  
<span data-ttu-id="43242-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="43242-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="43242-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43242-110">Syntax</span></span>  
  
```xml  
<transport clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"
           proxyCredentialType="Basic/Digest/None/Ntlm/Windows"
           realm="string" />
```  
  
## <a name="type"></a><span data-ttu-id="43242-111">Type</span><span class="sxs-lookup"><span data-stu-id="43242-111">Type</span></span>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="43242-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="43242-112">Attributes and Elements</span></span>  
 <span data-ttu-id="43242-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="43242-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="43242-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="43242-114">Attributes</span></span>  
  
|<span data-ttu-id="43242-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="43242-115">Attribute</span></span>|<span data-ttu-id="43242-116">Description</span><span class="sxs-lookup"><span data-stu-id="43242-116">Description</span></span>|  
|---------------|-----------------|  
|`clientCredentialType`|<span data-ttu-id="43242-117">Spécifie les informations d'identification utilisées pour authentifier le client auprès du service.</span><span class="sxs-lookup"><span data-stu-id="43242-117">Specifies the credential used to authenticate the client to the service.</span></span> <span data-ttu-id="43242-118">Cet attribut est de type <xref:System.ServiceModel.HttpClientCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="43242-118">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|`proxyCredentialType`|<span data-ttu-id="43242-119">Spécifie les informations d'identification utilisées pour authentifier le client auprès d'un proxy de domaine.</span><span class="sxs-lookup"><span data-stu-id="43242-119">Specifies the credential used to authenticate the client to a domain proxy.</span></span> <span data-ttu-id="43242-120">Cet attribut est de type <xref:System.ServiceModel.HttpProxyCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="43242-120">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|`realm`|<span data-ttu-id="43242-121">Domaine d'authentification correspondant à l'authentification de base ou Digest.</span><span class="sxs-lookup"><span data-stu-id="43242-121">The authentication realm for digest or basic authentication.</span></span> <span data-ttu-id="43242-122">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="43242-122">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="43242-123">Un domaine d'authentification spécifie au moins le nom de l'hôte qui exécute l'authentification.</span><span class="sxs-lookup"><span data-stu-id="43242-123">An authentication realm specifies at least the name of the host that performs the authentication.</span></span> <span data-ttu-id="43242-124">Il peut également spécifier une collection d'utilisateurs disposant d'un accès.</span><span class="sxs-lookup"><span data-stu-id="43242-124">It can also specify a collection of users who have access.</span></span> <span data-ttu-id="43242-125">Un utilisateur peut interroger le domaine d'authentification afin de déterminer les noms d'utilisateur et les mots de passe pouvant être utilisés.</span><span class="sxs-lookup"><span data-stu-id="43242-125">A user can query the authentication realm to determine which one of the several possible usernames and passwords can be used.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="43242-126">Attribut clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="43242-126">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="43242-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="43242-127">Value</span></span>|<span data-ttu-id="43242-128">Description</span><span class="sxs-lookup"><span data-stu-id="43242-128">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="43242-129">None</span><span class="sxs-lookup"><span data-stu-id="43242-129">None</span></span>|<span data-ttu-id="43242-130">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="43242-130">Security is disabled.</span></span>|  
|<span data-ttu-id="43242-131">Basic</span><span class="sxs-lookup"><span data-stu-id="43242-131">Basic</span></span>|<span data-ttu-id="43242-132">Utilise l'authentification de base.</span><span class="sxs-lookup"><span data-stu-id="43242-132">Uses basic authentication.</span></span>|  
|<span data-ttu-id="43242-133">Digest</span><span class="sxs-lookup"><span data-stu-id="43242-133">Digest</span></span>|<span data-ttu-id="43242-134">Utilise l'authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="43242-134">Uses digest authentication.</span></span>|  
|<span data-ttu-id="43242-135">Ntlm</span><span class="sxs-lookup"><span data-stu-id="43242-135">Ntlm</span></span>|<span data-ttu-id="43242-136">Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="43242-136">Uses NTLM authentication as a fallback with a Windows domain.</span></span>|  
|<span data-ttu-id="43242-137">Windows</span><span class="sxs-lookup"><span data-stu-id="43242-137">Windows</span></span>|<span data-ttu-id="43242-138">Utilise l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="43242-138">Uses integrated Windows authentication.</span></span>|  
|<span data-ttu-id="43242-139">Certificat</span><span class="sxs-lookup"><span data-stu-id="43242-139">Certificate</span></span>|<span data-ttu-id="43242-140">Utilise des certificats X.509 pour authentifier le client.</span><span class="sxs-lookup"><span data-stu-id="43242-140">Uses X.509 certificates to authenticate the client.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="43242-141">Attribut proxyCredentialType</span><span class="sxs-lookup"><span data-stu-id="43242-141">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="43242-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="43242-142">Value</span></span>|<span data-ttu-id="43242-143">Description</span><span class="sxs-lookup"><span data-stu-id="43242-143">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="43242-144">None</span><span class="sxs-lookup"><span data-stu-id="43242-144">None</span></span>|<span data-ttu-id="43242-145">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="43242-145">Security is disabled.</span></span>|  
|<span data-ttu-id="43242-146">Basic</span><span class="sxs-lookup"><span data-stu-id="43242-146">Basic</span></span>|<span data-ttu-id="43242-147">Utilise l'authentification de base.</span><span class="sxs-lookup"><span data-stu-id="43242-147">Uses basic authentication.</span></span>|  
|<span data-ttu-id="43242-148">Digest</span><span class="sxs-lookup"><span data-stu-id="43242-148">Digest</span></span>|<span data-ttu-id="43242-149">Utilise l'authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="43242-149">Uses digest authentication.</span></span>|  
|<span data-ttu-id="43242-150">Ntlm</span><span class="sxs-lookup"><span data-stu-id="43242-150">Ntlm</span></span>|<span data-ttu-id="43242-151">Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="43242-151">Uses NTLM as a fallback with a Windows domain.</span></span>|  
|<span data-ttu-id="43242-152">Windows</span><span class="sxs-lookup"><span data-stu-id="43242-152">Windows</span></span>|<span data-ttu-id="43242-153">Utilise l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="43242-153">Uses integrated Windows authentication.</span></span>|  
|<span data-ttu-id="43242-154">Certificat</span><span class="sxs-lookup"><span data-stu-id="43242-154">Certificate</span></span>|<span data-ttu-id="43242-155">Utilise des certificats X.509 pour authentifier le client.</span><span class="sxs-lookup"><span data-stu-id="43242-155">Uses X.509 certificates to authenticate the client.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="43242-156">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="43242-156">Child Elements</span></span>  
 <span data-ttu-id="43242-157">Aucun.</span><span class="sxs-lookup"><span data-stu-id="43242-157">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="43242-158">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="43242-158">Parent Elements</span></span>  
  
|<span data-ttu-id="43242-159">Élément</span><span class="sxs-lookup"><span data-stu-id="43242-159">Element</span></span>|<span data-ttu-id="43242-160">Description</span><span class="sxs-lookup"><span data-stu-id="43242-160">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="43242-161">\<security></span><span class="sxs-lookup"><span data-stu-id="43242-161">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-ws2007httpbinding.md)|<span data-ttu-id="43242-162">Représente les fonctionnalités de sécurité de la [ \<ws2007HttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="43242-162">Represents the security capabilities of the [\<ws2007HttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="43242-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43242-163">See also</span></span>
- <xref:System.ServiceModel.HttpTransportSecurity>
- <xref:System.ServiceModel.Configuration.BasicHttpSecurityElement.Transport%2A>
- <xref:System.ServiceModel.WSHttpSecurity.Transport%2A>
- <xref:System.ServiceModel.Configuration.WSHttpTransportSecurityElement>
- [<span data-ttu-id="43242-164">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="43242-164">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="43242-165">Liaisons</span><span class="sxs-lookup"><span data-stu-id="43242-165">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="43242-166">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="43242-166">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="43242-167">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="43242-167">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="43242-168">\<binding></span><span class="sxs-lookup"><span data-stu-id="43242-168">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
