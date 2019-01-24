---
title: '&lt;clientCredentials&gt;'
ms.date: 03/30/2017
ms.assetid: 1e6eef0d-a34e-4d74-b0f7-f65d2181858d
ms.openlocfilehash: d8171254fed64a2d9ba526d5714d5707aa1b1c1e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54646053"
---
# <a name="ltclientcredentialsgt"></a><span data-ttu-id="7f971-102">&lt;clientCredentials&gt;</span><span class="sxs-lookup"><span data-stu-id="7f971-102">&lt;clientCredentials&gt;</span></span>
<span data-ttu-id="7f971-103">Indique les informations d'identification utilisées pour authentifier le client auprès d'un service.</span><span class="sxs-lookup"><span data-stu-id="7f971-103">Specifies the credentials used to authenticate the client to a service.</span></span>  
  
 <span data-ttu-id="7f971-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="7f971-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="7f971-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="7f971-105">\<behaviors></span></span>  
<span data-ttu-id="7f971-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="7f971-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="7f971-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="7f971-107">\<behavior></span></span>  
<span data-ttu-id="7f971-108">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="7f971-108">\<clientCredentials></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f971-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f971-109">Syntax</span></span>  
  
```xml  
<clientCredentials type="String"
                   supportInteractive="Boolean" >
  <clientCertificate>
  </clientCertificate>
  <digest>
  </digest>
  <isuedToken>
  </isuedToken>
  <peer>
  </peer>
  <serviceCertificate>
  </serviceCertificate>
  <windowsAuthentication>
  </windowsAuthentication>
</clientCredentials>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7f971-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7f971-110">Attributes and Elements</span></span>  
 <span data-ttu-id="7f971-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7f971-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7f971-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="7f971-112">Attributes</span></span>  
  
|<span data-ttu-id="7f971-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="7f971-113">Attribute</span></span>|<span data-ttu-id="7f971-114">Description</span><span class="sxs-lookup"><span data-stu-id="7f971-114">Description</span></span>|  
|---------------|-----------------|  
|`supportInteractive`|<span data-ttu-id="7f971-115">Valeur booléenne indiquant si un utilisateur interactif peut sélectionner les informations d'identification d'un client pendant l'exécution.</span><span class="sxs-lookup"><span data-stu-id="7f971-115">A Boolean value that specifies whether an interactive user can be involved in selecting a client credential at runtime.</span></span> <span data-ttu-id="7f971-116">La valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="7f971-116">The default value is `true`.</span></span>|  
|`type`|<span data-ttu-id="7f971-117">Chaîne qui spécifie le type de cet élément de configuration.</span><span class="sxs-lookup"><span data-stu-id="7f971-117">A string that specifies the type of this configuration element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7f971-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7f971-118">Child Elements</span></span>  
  
|<span data-ttu-id="7f971-119">Élément</span><span class="sxs-lookup"><span data-stu-id="7f971-119">Element</span></span>|<span data-ttu-id="7f971-120">Description</span><span class="sxs-lookup"><span data-stu-id="7f971-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7f971-121">\<clientCertificate></span><span class="sxs-lookup"><span data-stu-id="7f971-121">\<clientCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-clientcredentials-element.md)|<span data-ttu-id="7f971-122">Indique le certificat utilisé pour authentifier le client auprès du service.</span><span class="sxs-lookup"><span data-stu-id="7f971-122">Specifies the certificate used to authenticate the client to the service.</span></span> <span data-ttu-id="7f971-123">Cet élément est de type <xref:System.ServiceModel.Configuration.X509InitiatorCertificateClientElement>.</span><span class="sxs-lookup"><span data-stu-id="7f971-123">This element is of type <xref:System.ServiceModel.Configuration.X509InitiatorCertificateClientElement>.</span></span>|  
|[<span data-ttu-id="7f971-124">\<httpDigest></span><span class="sxs-lookup"><span data-stu-id="7f971-124">\<httpDigest></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/httpdigest-element.md)|<span data-ttu-id="7f971-125">Indique un condensat utilisé pour authentifier le client auprès du service.</span><span class="sxs-lookup"><span data-stu-id="7f971-125">Specifies a digest used to authenticate the client to the service.</span></span> <span data-ttu-id="7f971-126">Cet élément est de type <xref:System.ServiceModel.Configuration.HttpDigestClientElement>.</span><span class="sxs-lookup"><span data-stu-id="7f971-126">This element is of type <xref:System.ServiceModel.Configuration.HttpDigestClientElement>.</span></span>|  
|[<span data-ttu-id="7f971-127">\<issuedToken></span><span class="sxs-lookup"><span data-stu-id="7f971-127">\<issuedToken></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtoken.md)|<span data-ttu-id="7f971-128">Spécifie un type de jeton personnalisé utilisé pour authentifier le client à un service STS.</span><span class="sxs-lookup"><span data-stu-id="7f971-128">Specifies a custom token type used to authenticate the client to a Secure Token Service (STS).</span></span> <span data-ttu-id="7f971-129">Cet élément est de type <xref:System.ServiceModel.Configuration.IssuedTokenClientElement>.</span><span class="sxs-lookup"><span data-stu-id="7f971-129">This element is of type <xref:System.ServiceModel.Configuration.IssuedTokenClientElement>.</span></span>|  
|[<span data-ttu-id="7f971-130">\<peer></span><span class="sxs-lookup"><span data-stu-id="7f971-130">\<peer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-clientcredentials-element.md)|<span data-ttu-id="7f971-131">Spécifie des informations d'identification d'homologue actuelles.</span><span class="sxs-lookup"><span data-stu-id="7f971-131">Specifies a current peer credential.</span></span> <span data-ttu-id="7f971-132">Cet élément est de type <xref:System.ServiceModel.Configuration.PeerCredentialElement>.</span><span class="sxs-lookup"><span data-stu-id="7f971-132">This element is of type <xref:System.ServiceModel.Configuration.PeerCredentialElement>.</span></span>|  
|[<span data-ttu-id="7f971-133">\<serviceCertificate></span><span class="sxs-lookup"><span data-stu-id="7f971-133">\<serviceCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecertificate-of-clientcredentials-element.md)|<span data-ttu-id="7f971-134">Spécifie le certificat utilisé pour authentifier le service auprès du client et fournit une structure permettant de définir des options de certificat.</span><span class="sxs-lookup"><span data-stu-id="7f971-134">Specifies the certificate used to authenticate the service to the client and provides a structure for setting certificate options.</span></span> <span data-ttu-id="7f971-135">Ce certificat doit être fourni au client hors bande, à partir du service.</span><span class="sxs-lookup"><span data-stu-id="7f971-135">This certificate must be supplied out-of-band from the service to the client.</span></span> <span data-ttu-id="7f971-136">Cet élément est de type <xref:System.ServiceModel.Configuration.X509RecipientCertificateClientElement>.</span><span class="sxs-lookup"><span data-stu-id="7f971-136">This element is of type <xref:System.ServiceModel.Configuration.X509RecipientCertificateClientElement>.</span></span>|  
|[<span data-ttu-id="7f971-137">\<windows></span><span class="sxs-lookup"><span data-stu-id="7f971-137">\<windows></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/windows-of-clientcredentials-element.md)|<span data-ttu-id="7f971-138">Indique des informations d'identification Windows.</span><span class="sxs-lookup"><span data-stu-id="7f971-138">Specifies a Windows credential.</span></span> <span data-ttu-id="7f971-139">La valeur par défaut correspond aux informations d'identification du thread actuel.</span><span class="sxs-lookup"><span data-stu-id="7f971-139">The default is the credential of the current thread.</span></span> <span data-ttu-id="7f971-140">Cet élément est de type <xref:System.ServiceModel.Configuration.WindowsClientElement>.</span><span class="sxs-lookup"><span data-stu-id="7f971-140">This element is of type <xref:System.ServiceModel.Configuration.WindowsClientElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="7f971-141">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7f971-141">Parent Elements</span></span>  
  
|<span data-ttu-id="7f971-142">Élément</span><span class="sxs-lookup"><span data-stu-id="7f971-142">Element</span></span>|<span data-ttu-id="7f971-143">Description</span><span class="sxs-lookup"><span data-stu-id="7f971-143">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7f971-144">\<behavior></span><span class="sxs-lookup"><span data-stu-id="7f971-144">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="7f971-145">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="7f971-145">Specifies an endpoint behavior.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7f971-146">Notes</span><span class="sxs-lookup"><span data-stu-id="7f971-146">Remarks</span></span>  
 <span data-ttu-id="7f971-147">Les informations d'identification du client permettent d'authentifier le client auprès des services dans les cas où l'authentification mutuelle est requise.</span><span class="sxs-lookup"><span data-stu-id="7f971-147">Client credentials are used to authenticate the client to services in cases where mutual authentication is required.</span></span> <span data-ttu-id="7f971-148">Cette section de configuration peut également servir à spécifier des certificats de service pour les scénarios dans lesquels le client doit sécuriser des messages auprès d'un service à l'aide du certificat de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="7f971-148">This configuration section can also be used to specify service certificates for scenarios where the client must secure messages to a service with the service's certificate.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f971-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f971-149">See also</span></span>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Description.ClientCredentials>
- [<span data-ttu-id="7f971-150">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="7f971-150">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="7f971-151">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="7f971-151">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
