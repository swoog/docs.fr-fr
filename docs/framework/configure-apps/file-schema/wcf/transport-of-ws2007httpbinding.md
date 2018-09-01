---
title: '&lt;transport&gt; de &lt;ws2007HttpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 692befa3-8b0b-4ec5-b601-755874e98eb0
ms.openlocfilehash: 35af47551f742b0e48220611a874605fb752b626
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43396795"
---
# <a name="lttransportgt-of-ltws2007httpbindinggt"></a><span data-ttu-id="db749-102">&lt;transport&gt; de &lt;ws2007HttpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="db749-102">&lt;transport&gt; of &lt;ws2007HttpBinding&gt;</span></span>
<span data-ttu-id="db749-103">Définit les paramètres d'authentification correspondant au transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="db749-103">Defines authentication settings for the HTTP transport.</span></span>  
  
 <span data-ttu-id="db749-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="db749-104">\<system.serviceModel></span></span>  
<span data-ttu-id="db749-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="db749-105">\<bindings></span></span>  
<span data-ttu-id="db749-106">\<ws2007HttpBinding></span><span class="sxs-lookup"><span data-stu-id="db749-106">\<ws2007HttpBinding></span></span>  
<span data-ttu-id="db749-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="db749-107">\<binding></span></span>  
<span data-ttu-id="db749-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="db749-108">\<security></span></span>  
<span data-ttu-id="db749-109">\<transport ></span><span class="sxs-lookup"><span data-stu-id="db749-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db749-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db749-110">Syntax</span></span>  
  
```  
transport clientCredentialType =   
       "Basic/Certificate/Digest/None/Ntlm/Windows"  
       proxyCredentialType="Basic/Digest/None/Ntlm/Windows"  
       realm="string"   
```  
  
## <a name="type"></a><span data-ttu-id="db749-111">Type</span><span class="sxs-lookup"><span data-stu-id="db749-111">Type</span></span>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="db749-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="db749-112">Attributes and Elements</span></span>  
 <span data-ttu-id="db749-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="db749-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="db749-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="db749-114">Attributes</span></span>  
  
|<span data-ttu-id="db749-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="db749-115">Attribute</span></span>|<span data-ttu-id="db749-116">Description</span><span class="sxs-lookup"><span data-stu-id="db749-116">Description</span></span>|  
|---------------|-----------------|  
|`clientCredentialType`|<span data-ttu-id="db749-117">Spécifie les informations d'identification utilisées pour authentifier le client auprès du service.</span><span class="sxs-lookup"><span data-stu-id="db749-117">Specifies the credential used to authenticate the client to the service.</span></span> <span data-ttu-id="db749-118">Cet attribut est de type <xref:System.ServiceModel.HttpClientCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="db749-118">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|`proxyCredentialType`|<span data-ttu-id="db749-119">Spécifie les informations d'identification utilisées pour authentifier le client auprès d'un proxy de domaine.</span><span class="sxs-lookup"><span data-stu-id="db749-119">Specifies the credential used to authenticate the client to a domain proxy.</span></span> <span data-ttu-id="db749-120">Cet attribut est de type <xref:System.ServiceModel.HttpProxyCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="db749-120">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|`realm`|<span data-ttu-id="db749-121">Domaine d'authentification correspondant à l'authentification de base ou Digest.</span><span class="sxs-lookup"><span data-stu-id="db749-121">The authentication realm for digest or basic authentication.</span></span> <span data-ttu-id="db749-122">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="db749-122">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="db749-123">Un domaine d'authentification spécifie au moins le nom de l'hôte qui exécute l'authentification.</span><span class="sxs-lookup"><span data-stu-id="db749-123">An authentication realm specifies at least the name of the host that performs the authentication.</span></span> <span data-ttu-id="db749-124">Il peut également spécifier une collection d'utilisateurs disposant d'un accès.</span><span class="sxs-lookup"><span data-stu-id="db749-124">It can also specify a collection of users who have access.</span></span> <span data-ttu-id="db749-125">Un utilisateur peut interroger le domaine d'authentification afin de déterminer les noms d'utilisateur et les mots de passe pouvant être utilisés.</span><span class="sxs-lookup"><span data-stu-id="db749-125">A user can query the authentication realm to determine which one of the several possible usernames and passwords can be used.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="db749-126">Attribut clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="db749-126">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="db749-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="db749-127">Value</span></span>|<span data-ttu-id="db749-128">Description</span><span class="sxs-lookup"><span data-stu-id="db749-128">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="db749-129">None</span><span class="sxs-lookup"><span data-stu-id="db749-129">None</span></span>|<span data-ttu-id="db749-130">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="db749-130">Security is disabled.</span></span>|  
|<span data-ttu-id="db749-131">Basic</span><span class="sxs-lookup"><span data-stu-id="db749-131">Basic</span></span>|<span data-ttu-id="db749-132">Utilise l'authentification de base.</span><span class="sxs-lookup"><span data-stu-id="db749-132">Uses basic authentication.</span></span>|  
|<span data-ttu-id="db749-133">Digest</span><span class="sxs-lookup"><span data-stu-id="db749-133">Digest</span></span>|<span data-ttu-id="db749-134">Utilise l'authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="db749-134">Uses digest authentication.</span></span>|  
|<span data-ttu-id="db749-135">Ntlm</span><span class="sxs-lookup"><span data-stu-id="db749-135">Ntlm</span></span>|<span data-ttu-id="db749-136">Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="db749-136">Uses NTLM authentication as a fallback with a Windows domain.</span></span>|  
|<span data-ttu-id="db749-137">Windows</span><span class="sxs-lookup"><span data-stu-id="db749-137">Windows</span></span>|<span data-ttu-id="db749-138">Utilise l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="db749-138">Uses integrated Windows authentication.</span></span>|  
|<span data-ttu-id="db749-139">Certificat</span><span class="sxs-lookup"><span data-stu-id="db749-139">Certificate</span></span>|<span data-ttu-id="db749-140">Utilise des certificats X.509 pour authentifier le client.</span><span class="sxs-lookup"><span data-stu-id="db749-140">Uses X.509 certificates to authenticate the client.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="db749-141">Attribut proxyCredentialType</span><span class="sxs-lookup"><span data-stu-id="db749-141">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="db749-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="db749-142">Value</span></span>|<span data-ttu-id="db749-143">Description</span><span class="sxs-lookup"><span data-stu-id="db749-143">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="db749-144">None</span><span class="sxs-lookup"><span data-stu-id="db749-144">None</span></span>|<span data-ttu-id="db749-145">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="db749-145">Security is disabled.</span></span>|  
|<span data-ttu-id="db749-146">Basic</span><span class="sxs-lookup"><span data-stu-id="db749-146">Basic</span></span>|<span data-ttu-id="db749-147">Utilise l'authentification de base.</span><span class="sxs-lookup"><span data-stu-id="db749-147">Uses basic authentication.</span></span>|  
|<span data-ttu-id="db749-148">Digest</span><span class="sxs-lookup"><span data-stu-id="db749-148">Digest</span></span>|<span data-ttu-id="db749-149">Utilise l'authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="db749-149">Uses digest authentication.</span></span>|  
|<span data-ttu-id="db749-150">Ntlm</span><span class="sxs-lookup"><span data-stu-id="db749-150">Ntlm</span></span>|<span data-ttu-id="db749-151">Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="db749-151">Uses NTLM as a fallback with a Windows domain.</span></span>|  
|<span data-ttu-id="db749-152">Windows</span><span class="sxs-lookup"><span data-stu-id="db749-152">Windows</span></span>|<span data-ttu-id="db749-153">Utilise l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="db749-153">Uses integrated Windows authentication.</span></span>|  
|<span data-ttu-id="db749-154">Certificat</span><span class="sxs-lookup"><span data-stu-id="db749-154">Certificate</span></span>|<span data-ttu-id="db749-155">Utilise des certificats X.509 pour authentifier le client.</span><span class="sxs-lookup"><span data-stu-id="db749-155">Uses X.509 certificates to authenticate the client.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="db749-156">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="db749-156">Child Elements</span></span>  
 <span data-ttu-id="db749-157">Aucun.</span><span class="sxs-lookup"><span data-stu-id="db749-157">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="db749-158">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="db749-158">Parent Elements</span></span>  
  
|<span data-ttu-id="db749-159">Élément</span><span class="sxs-lookup"><span data-stu-id="db749-159">Element</span></span>|<span data-ttu-id="db749-160">Description</span><span class="sxs-lookup"><span data-stu-id="db749-160">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="db749-161">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="db749-161">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-ws2007httpbinding.md)|<span data-ttu-id="db749-162">Représente les fonctionnalités de sécurité de la [ \<ws2007HttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="db749-162">Represents the security capabilities of the [\<ws2007HttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="db749-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db749-163">See Also</span></span>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
 <xref:System.ServiceModel.Configuration.BasicHttpSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.WSHttpSecurity.Transport%2A>  
 <xref:System.ServiceModel.Configuration.WSHttpTransportSecurityElement>  
 [<span data-ttu-id="db749-164">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="db749-164">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="db749-165">Liaisons</span><span class="sxs-lookup"><span data-stu-id="db749-165">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="db749-166">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="db749-166">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="db749-167">Utilisation de liaisons pour configurer les Clients et les Services Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="db749-167">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="db749-168">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="db749-168">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
