---
title: '&lt;transport&gt; de &lt;ws2007HttpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 692befa3-8b0b-4ec5-b601-755874e98eb0
ms.openlocfilehash: 5c7e96beee2fc1e4780729e56f10a52b63dde4e8
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48841415"
---
# <a name="lttransportgt-of-ltws2007httpbindinggt"></a><span data-ttu-id="eedc1-102">&lt;transport&gt; de &lt;ws2007HttpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="eedc1-102">&lt;transport&gt; of &lt;ws2007HttpBinding&gt;</span></span>
<span data-ttu-id="eedc1-103">Définit les paramètres d'authentification correspondant au transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="eedc1-103">Defines authentication settings for the HTTP transport.</span></span>  
  
 <span data-ttu-id="eedc1-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="eedc1-104">\<system.serviceModel></span></span>  
<span data-ttu-id="eedc1-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="eedc1-105">\<bindings></span></span>  
<span data-ttu-id="eedc1-106">\<ws2007HttpBinding></span><span class="sxs-lookup"><span data-stu-id="eedc1-106">\<ws2007HttpBinding></span></span>  
<span data-ttu-id="eedc1-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="eedc1-107">\<binding></span></span>  
<span data-ttu-id="eedc1-108">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="eedc1-108">\<security></span></span>  
<span data-ttu-id="eedc1-109">\<transport ></span><span class="sxs-lookup"><span data-stu-id="eedc1-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eedc1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eedc1-110">Syntax</span></span>  
  
```  
transport clientCredentialType =   
       "Basic/Certificate/Digest/None/Ntlm/Windows"  
       proxyCredentialType="Basic/Digest/None/Ntlm/Windows"  
       realm="string"   
```  
  
## <a name="type"></a><span data-ttu-id="eedc1-111">Type</span><span class="sxs-lookup"><span data-stu-id="eedc1-111">Type</span></span>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="eedc1-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="eedc1-112">Attributes and Elements</span></span>  
 <span data-ttu-id="eedc1-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="eedc1-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="eedc1-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="eedc1-114">Attributes</span></span>  
  
|<span data-ttu-id="eedc1-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="eedc1-115">Attribute</span></span>|<span data-ttu-id="eedc1-116">Description</span><span class="sxs-lookup"><span data-stu-id="eedc1-116">Description</span></span>|  
|---------------|-----------------|  
|`clientCredentialType`|<span data-ttu-id="eedc1-117">Spécifie les informations d'identification utilisées pour authentifier le client auprès du service.</span><span class="sxs-lookup"><span data-stu-id="eedc1-117">Specifies the credential used to authenticate the client to the service.</span></span> <span data-ttu-id="eedc1-118">Cet attribut est de type <xref:System.ServiceModel.HttpClientCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="eedc1-118">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|`proxyCredentialType`|<span data-ttu-id="eedc1-119">Spécifie les informations d'identification utilisées pour authentifier le client auprès d'un proxy de domaine.</span><span class="sxs-lookup"><span data-stu-id="eedc1-119">Specifies the credential used to authenticate the client to a domain proxy.</span></span> <span data-ttu-id="eedc1-120">Cet attribut est de type <xref:System.ServiceModel.HttpProxyCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="eedc1-120">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|`realm`|<span data-ttu-id="eedc1-121">Domaine d'authentification correspondant à l'authentification de base ou Digest.</span><span class="sxs-lookup"><span data-stu-id="eedc1-121">The authentication realm for digest or basic authentication.</span></span> <span data-ttu-id="eedc1-122">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="eedc1-122">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="eedc1-123">Un domaine d'authentification spécifie au moins le nom de l'hôte qui exécute l'authentification.</span><span class="sxs-lookup"><span data-stu-id="eedc1-123">An authentication realm specifies at least the name of the host that performs the authentication.</span></span> <span data-ttu-id="eedc1-124">Il peut également spécifier une collection d'utilisateurs disposant d'un accès.</span><span class="sxs-lookup"><span data-stu-id="eedc1-124">It can also specify a collection of users who have access.</span></span> <span data-ttu-id="eedc1-125">Un utilisateur peut interroger le domaine d'authentification afin de déterminer les noms d'utilisateur et les mots de passe pouvant être utilisés.</span><span class="sxs-lookup"><span data-stu-id="eedc1-125">A user can query the authentication realm to determine which one of the several possible usernames and passwords can be used.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="eedc1-126">Attribut clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="eedc1-126">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="eedc1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="eedc1-127">Value</span></span>|<span data-ttu-id="eedc1-128">Description</span><span class="sxs-lookup"><span data-stu-id="eedc1-128">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="eedc1-129">None</span><span class="sxs-lookup"><span data-stu-id="eedc1-129">None</span></span>|<span data-ttu-id="eedc1-130">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="eedc1-130">Security is disabled.</span></span>|  
|<span data-ttu-id="eedc1-131">Basic</span><span class="sxs-lookup"><span data-stu-id="eedc1-131">Basic</span></span>|<span data-ttu-id="eedc1-132">Utilise l'authentification de base.</span><span class="sxs-lookup"><span data-stu-id="eedc1-132">Uses basic authentication.</span></span>|  
|<span data-ttu-id="eedc1-133">Digest</span><span class="sxs-lookup"><span data-stu-id="eedc1-133">Digest</span></span>|<span data-ttu-id="eedc1-134">Utilise l'authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="eedc1-134">Uses digest authentication.</span></span>|  
|<span data-ttu-id="eedc1-135">Ntlm</span><span class="sxs-lookup"><span data-stu-id="eedc1-135">Ntlm</span></span>|<span data-ttu-id="eedc1-136">Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="eedc1-136">Uses NTLM authentication as a fallback with a Windows domain.</span></span>|  
|<span data-ttu-id="eedc1-137">Windows</span><span class="sxs-lookup"><span data-stu-id="eedc1-137">Windows</span></span>|<span data-ttu-id="eedc1-138">Utilise l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="eedc1-138">Uses integrated Windows authentication.</span></span>|  
|<span data-ttu-id="eedc1-139">Certificat</span><span class="sxs-lookup"><span data-stu-id="eedc1-139">Certificate</span></span>|<span data-ttu-id="eedc1-140">Utilise des certificats X.509 pour authentifier le client.</span><span class="sxs-lookup"><span data-stu-id="eedc1-140">Uses X.509 certificates to authenticate the client.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="eedc1-141">Attribut proxyCredentialType</span><span class="sxs-lookup"><span data-stu-id="eedc1-141">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="eedc1-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="eedc1-142">Value</span></span>|<span data-ttu-id="eedc1-143">Description</span><span class="sxs-lookup"><span data-stu-id="eedc1-143">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="eedc1-144">None</span><span class="sxs-lookup"><span data-stu-id="eedc1-144">None</span></span>|<span data-ttu-id="eedc1-145">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="eedc1-145">Security is disabled.</span></span>|  
|<span data-ttu-id="eedc1-146">Basic</span><span class="sxs-lookup"><span data-stu-id="eedc1-146">Basic</span></span>|<span data-ttu-id="eedc1-147">Utilise l'authentification de base.</span><span class="sxs-lookup"><span data-stu-id="eedc1-147">Uses basic authentication.</span></span>|  
|<span data-ttu-id="eedc1-148">Digest</span><span class="sxs-lookup"><span data-stu-id="eedc1-148">Digest</span></span>|<span data-ttu-id="eedc1-149">Utilise l'authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="eedc1-149">Uses digest authentication.</span></span>|  
|<span data-ttu-id="eedc1-150">Ntlm</span><span class="sxs-lookup"><span data-stu-id="eedc1-150">Ntlm</span></span>|<span data-ttu-id="eedc1-151">Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="eedc1-151">Uses NTLM as a fallback with a Windows domain.</span></span>|  
|<span data-ttu-id="eedc1-152">Windows</span><span class="sxs-lookup"><span data-stu-id="eedc1-152">Windows</span></span>|<span data-ttu-id="eedc1-153">Utilise l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="eedc1-153">Uses integrated Windows authentication.</span></span>|  
|<span data-ttu-id="eedc1-154">Certificat</span><span class="sxs-lookup"><span data-stu-id="eedc1-154">Certificate</span></span>|<span data-ttu-id="eedc1-155">Utilise des certificats X.509 pour authentifier le client.</span><span class="sxs-lookup"><span data-stu-id="eedc1-155">Uses X.509 certificates to authenticate the client.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="eedc1-156">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eedc1-156">Child Elements</span></span>  
 <span data-ttu-id="eedc1-157">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eedc1-157">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="eedc1-158">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="eedc1-158">Parent Elements</span></span>  
  
|<span data-ttu-id="eedc1-159">Élément</span><span class="sxs-lookup"><span data-stu-id="eedc1-159">Element</span></span>|<span data-ttu-id="eedc1-160">Description</span><span class="sxs-lookup"><span data-stu-id="eedc1-160">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="eedc1-161">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="eedc1-161">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-ws2007httpbinding.md)|<span data-ttu-id="eedc1-162">Représente les fonctionnalités de sécurité de la [ \<ws2007HttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="eedc1-162">Represents the security capabilities of the [\<ws2007HttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="eedc1-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eedc1-163">See Also</span></span>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
 <xref:System.ServiceModel.Configuration.BasicHttpSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.WSHttpSecurity.Transport%2A>  
 <xref:System.ServiceModel.Configuration.WSHttpTransportSecurityElement>  
 [<span data-ttu-id="eedc1-164">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="eedc1-164">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="eedc1-165">Liaisons</span><span class="sxs-lookup"><span data-stu-id="eedc1-165">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="eedc1-166">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="eedc1-166">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="eedc1-167">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="eedc1-167">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="eedc1-168">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="eedc1-168">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
