---
title: <clientCredentials>
ms.date: 03/30/2017
ms.assetid: 1e6eef0d-a34e-4d74-b0f7-f65d2181858d
ms.openlocfilehash: ebe976df9af0c316e95a1e089412e57a575a6df1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61673372"
---
# <a name="clientcredentials"></a><span data-ttu-id="21f96-101">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="21f96-101">\<clientCredentials></span></span>
<span data-ttu-id="21f96-102">Indique les informations d'identification utilisées pour authentifier le client auprès d'un service.</span><span class="sxs-lookup"><span data-stu-id="21f96-102">Specifies the credentials used to authenticate the client to a service.</span></span>  
  
 <span data-ttu-id="21f96-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="21f96-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="21f96-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="21f96-104">\<behaviors></span></span>  
<span data-ttu-id="21f96-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="21f96-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="21f96-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="21f96-106">\<behavior></span></span>  
<span data-ttu-id="21f96-107">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="21f96-107">\<clientCredentials></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="21f96-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21f96-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="21f96-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="21f96-109">Attributes and Elements</span></span>  
 <span data-ttu-id="21f96-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="21f96-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="21f96-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="21f96-111">Attributes</span></span>  
  
|<span data-ttu-id="21f96-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="21f96-112">Attribute</span></span>|<span data-ttu-id="21f96-113">Description</span><span class="sxs-lookup"><span data-stu-id="21f96-113">Description</span></span>|  
|---------------|-----------------|  
|`supportInteractive`|<span data-ttu-id="21f96-114">Valeur booléenne indiquant si un utilisateur interactif peut sélectionner les informations d'identification d'un client pendant l'exécution.</span><span class="sxs-lookup"><span data-stu-id="21f96-114">A Boolean value that specifies whether an interactive user can be involved in selecting a client credential at runtime.</span></span> <span data-ttu-id="21f96-115">La valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="21f96-115">The default value is `true`.</span></span>|  
|`type`|<span data-ttu-id="21f96-116">Chaîne qui spécifie le type de cet élément de configuration.</span><span class="sxs-lookup"><span data-stu-id="21f96-116">A string that specifies the type of this configuration element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="21f96-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="21f96-117">Child Elements</span></span>  
  
|<span data-ttu-id="21f96-118">Élément</span><span class="sxs-lookup"><span data-stu-id="21f96-118">Element</span></span>|<span data-ttu-id="21f96-119">Description</span><span class="sxs-lookup"><span data-stu-id="21f96-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="21f96-120">\<clientCertificate></span><span class="sxs-lookup"><span data-stu-id="21f96-120">\<clientCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-clientcredentials-element.md)|<span data-ttu-id="21f96-121">Indique le certificat utilisé pour authentifier le client auprès du service.</span><span class="sxs-lookup"><span data-stu-id="21f96-121">Specifies the certificate used to authenticate the client to the service.</span></span> <span data-ttu-id="21f96-122">Cet élément est de type <xref:System.ServiceModel.Configuration.X509InitiatorCertificateClientElement>.</span><span class="sxs-lookup"><span data-stu-id="21f96-122">This element is of type <xref:System.ServiceModel.Configuration.X509InitiatorCertificateClientElement>.</span></span>|  
|[<span data-ttu-id="21f96-123">\<httpDigest></span><span class="sxs-lookup"><span data-stu-id="21f96-123">\<httpDigest></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/httpdigest-element.md)|<span data-ttu-id="21f96-124">Indique un condensat utilisé pour authentifier le client auprès du service.</span><span class="sxs-lookup"><span data-stu-id="21f96-124">Specifies a digest used to authenticate the client to the service.</span></span> <span data-ttu-id="21f96-125">Cet élément est de type <xref:System.ServiceModel.Configuration.HttpDigestClientElement>.</span><span class="sxs-lookup"><span data-stu-id="21f96-125">This element is of type <xref:System.ServiceModel.Configuration.HttpDigestClientElement>.</span></span>|  
|[<span data-ttu-id="21f96-126">\<issuedToken></span><span class="sxs-lookup"><span data-stu-id="21f96-126">\<issuedToken></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtoken.md)|<span data-ttu-id="21f96-127">Spécifie un type de jeton personnalisé utilisé pour authentifier le client à un service STS.</span><span class="sxs-lookup"><span data-stu-id="21f96-127">Specifies a custom token type used to authenticate the client to a Secure Token Service (STS).</span></span> <span data-ttu-id="21f96-128">Cet élément est de type <xref:System.ServiceModel.Configuration.IssuedTokenClientElement>.</span><span class="sxs-lookup"><span data-stu-id="21f96-128">This element is of type <xref:System.ServiceModel.Configuration.IssuedTokenClientElement>.</span></span>|  
|[<span data-ttu-id="21f96-129">\<peer></span><span class="sxs-lookup"><span data-stu-id="21f96-129">\<peer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-clientcredentials-element.md)|<span data-ttu-id="21f96-130">Spécifie des informations d'identification d'homologue actuelles.</span><span class="sxs-lookup"><span data-stu-id="21f96-130">Specifies a current peer credential.</span></span> <span data-ttu-id="21f96-131">Cet élément est de type <xref:System.ServiceModel.Configuration.PeerCredentialElement>.</span><span class="sxs-lookup"><span data-stu-id="21f96-131">This element is of type <xref:System.ServiceModel.Configuration.PeerCredentialElement>.</span></span>|  
|[<span data-ttu-id="21f96-132">\<serviceCertificate></span><span class="sxs-lookup"><span data-stu-id="21f96-132">\<serviceCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecertificate-of-clientcredentials-element.md)|<span data-ttu-id="21f96-133">Spécifie le certificat utilisé pour authentifier le service auprès du client et fournit une structure permettant de définir des options de certificat.</span><span class="sxs-lookup"><span data-stu-id="21f96-133">Specifies the certificate used to authenticate the service to the client and provides a structure for setting certificate options.</span></span> <span data-ttu-id="21f96-134">Ce certificat doit être fourni au client hors bande, à partir du service.</span><span class="sxs-lookup"><span data-stu-id="21f96-134">This certificate must be supplied out-of-band from the service to the client.</span></span> <span data-ttu-id="21f96-135">Cet élément est de type <xref:System.ServiceModel.Configuration.X509RecipientCertificateClientElement>.</span><span class="sxs-lookup"><span data-stu-id="21f96-135">This element is of type <xref:System.ServiceModel.Configuration.X509RecipientCertificateClientElement>.</span></span>|  
|[<span data-ttu-id="21f96-136">\<windows></span><span class="sxs-lookup"><span data-stu-id="21f96-136">\<windows></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/windows-of-clientcredentials-element.md)|<span data-ttu-id="21f96-137">Indique des informations d'identification Windows.</span><span class="sxs-lookup"><span data-stu-id="21f96-137">Specifies a Windows credential.</span></span> <span data-ttu-id="21f96-138">La valeur par défaut correspond aux informations d'identification du thread actuel.</span><span class="sxs-lookup"><span data-stu-id="21f96-138">The default is the credential of the current thread.</span></span> <span data-ttu-id="21f96-139">Cet élément est de type <xref:System.ServiceModel.Configuration.WindowsClientElement>.</span><span class="sxs-lookup"><span data-stu-id="21f96-139">This element is of type <xref:System.ServiceModel.Configuration.WindowsClientElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="21f96-140">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="21f96-140">Parent Elements</span></span>  
  
|<span data-ttu-id="21f96-141">Élément</span><span class="sxs-lookup"><span data-stu-id="21f96-141">Element</span></span>|<span data-ttu-id="21f96-142">Description</span><span class="sxs-lookup"><span data-stu-id="21f96-142">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="21f96-143">\<behavior></span><span class="sxs-lookup"><span data-stu-id="21f96-143">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="21f96-144">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="21f96-144">Specifies an endpoint behavior.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="21f96-145">Notes</span><span class="sxs-lookup"><span data-stu-id="21f96-145">Remarks</span></span>  
 <span data-ttu-id="21f96-146">Les informations d'identification du client permettent d'authentifier le client auprès des services dans les cas où l'authentification mutuelle est requise.</span><span class="sxs-lookup"><span data-stu-id="21f96-146">Client credentials are used to authenticate the client to services in cases where mutual authentication is required.</span></span> <span data-ttu-id="21f96-147">Cette section de configuration peut également servir à spécifier des certificats de service pour les scénarios dans lesquels le client doit sécuriser des messages auprès d'un service à l'aide du certificat de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="21f96-147">This configuration section can also be used to specify service certificates for scenarios where the client must secure messages to a service with the service's certificate.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="21f96-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21f96-148">See also</span></span>

- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Description.ClientCredentials>
- [<span data-ttu-id="21f96-149">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="21f96-149">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="21f96-150">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="21f96-150">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
