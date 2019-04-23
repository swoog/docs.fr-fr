---
title: <serviceCredentials>
ms.date: 03/30/2017
ms.assetid: 96db336c-4f7a-4193-81a5-910b8ffd804f
ms.openlocfilehash: d9f8fdf272962916cd08aede484e9bbde55b96a3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59227078"
---
# <a name="servicecredentials"></a><span data-ttu-id="1948e-101">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="1948e-101">\<serviceCredentials></span></span>
<span data-ttu-id="1948e-102">Spécifie l'information d'identification à utiliser pour authentifier le service, ainsi que les paramètres liés à la validation des informations d'identification du client.</span><span class="sxs-lookup"><span data-stu-id="1948e-102">Specifies the credential to be used in authenticating the service and the client credential validation-related settings.</span></span>  
  
 <span data-ttu-id="1948e-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="1948e-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="1948e-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="1948e-104">\<behaviors></span></span>  
<span data-ttu-id="1948e-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="1948e-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="1948e-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="1948e-106">\<behavior></span></span>  
<span data-ttu-id="1948e-107">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="1948e-107">\<serviceCredentials></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1948e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1948e-108">Syntax</span></span>  
  
```xml  
<serviceCredentials type="String">
  <clientCertificate>
  </clientCertificate>
  <issuedTokenAuthentication>
  </issuedTokenAuthentication>
  <peer>
  </peer>
  <secureConversationAuthentication>
  </secureConversationAuthentication>
  <serviceCertificate>
  </serviceCertificate>
  <userNameAuthentication>
  </userNameAuthentication>
  <windowsAuthentication>
  </windowsAuthentication>
</serviceCredentials>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1948e-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1948e-109">Attributes and Elements</span></span>  
 <span data-ttu-id="1948e-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1948e-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1948e-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="1948e-111">Attributes</span></span>  
  
|<span data-ttu-id="1948e-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="1948e-112">Attribute</span></span>|<span data-ttu-id="1948e-113">Description</span><span class="sxs-lookup"><span data-stu-id="1948e-113">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="1948e-114">Chaîne qui spécifie le type de cet élément de configuration.</span><span class="sxs-lookup"><span data-stu-id="1948e-114">A string that specifies the type of this configuration element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1948e-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1948e-115">Child Elements</span></span>  
  
|<span data-ttu-id="1948e-116">Élément</span><span class="sxs-lookup"><span data-stu-id="1948e-116">Element</span></span>|<span data-ttu-id="1948e-117">Description</span><span class="sxs-lookup"><span data-stu-id="1948e-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1948e-118">\<clientCertificate></span><span class="sxs-lookup"><span data-stu-id="1948e-118">\<clientCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-servicecredentials.md)|<span data-ttu-id="1948e-119">Spécifie le certificat à utiliser lorsque le certificat client est disponible hors bande.</span><span class="sxs-lookup"><span data-stu-id="1948e-119">Specifies the certificate to be used when the client certificate is available out-of-band.</span></span> <span data-ttu-id="1948e-120">Cet élément spécifie également les paramètres de validation du certificat client.</span><span class="sxs-lookup"><span data-stu-id="1948e-120">This element also specifies client certificate validation settings.</span></span> <span data-ttu-id="1948e-121">Cet élément est de type <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="1948e-121">This element is of type <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>.</span></span>|  
|[<span data-ttu-id="1948e-122">\<issuedTokenAuthentication></span><span class="sxs-lookup"><span data-stu-id="1948e-122">\<issuedTokenAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenauthentication-of-servicecredentials.md)|<span data-ttu-id="1948e-123">Spécifie le jeton émis actuellement pour ce service.</span><span class="sxs-lookup"><span data-stu-id="1948e-123">Specifies the current issued token for this service.</span></span> <span data-ttu-id="1948e-124">Cet élément est de type <xref:System.ServiceModel.Configuration.IssuedTokenServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="1948e-124">This element is of type <xref:System.ServiceModel.Configuration.IssuedTokenServiceElement>.</span></span>|  
|[<span data-ttu-id="1948e-125">\<peer></span><span class="sxs-lookup"><span data-stu-id="1948e-125">\<peer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-servicecredentials.md)|<span data-ttu-id="1948e-126">Spécifie les informations d'identification actuelles d'un nœud homologue.</span><span class="sxs-lookup"><span data-stu-id="1948e-126">Specifies the current credentials for a peer node.</span></span> <span data-ttu-id="1948e-127">Cet élément est de type <xref:System.ServiceModel.Configuration.PeerCredentialElement>.</span><span class="sxs-lookup"><span data-stu-id="1948e-127">This element is of type <xref:System.ServiceModel.Configuration.PeerCredentialElement>.</span></span>|  
|[<span data-ttu-id="1948e-128">\<secureConversationAuthentication></span><span class="sxs-lookup"><span data-stu-id="1948e-128">\<secureConversationAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/secureconversationauthentication-of-servicecredential.md)|<span data-ttu-id="1948e-129">Spécifie les informations d'identification actuelles pour une conversation sécurisée.</span><span class="sxs-lookup"><span data-stu-id="1948e-129">Specifies the current credentials for a secure conversation.</span></span> <span data-ttu-id="1948e-130">Cet élément est de type <xref:System.ServiceModel.Configuration.SecureConversationServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="1948e-130">This element is of type <xref:System.ServiceModel.Configuration.SecureConversationServiceElement>.</span></span>|  
|[<span data-ttu-id="1948e-131">\<serviceCertificate></span><span class="sxs-lookup"><span data-stu-id="1948e-131">\<serviceCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md)|<span data-ttu-id="1948e-132">Spécifie un certificat utilisé par un service pour s'identifier.</span><span class="sxs-lookup"><span data-stu-id="1948e-132">Specifies a certificate used by a service to identify itself.</span></span> <span data-ttu-id="1948e-133">Cet élément est de type <xref:System.ServiceModel.Configuration.X509RecipientCertificateServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="1948e-133">This element is of type <xref:System.ServiceModel.Configuration.X509RecipientCertificateServiceElement>.</span></span>|  
|[<span data-ttu-id="1948e-134">\<userNameAuthentication></span><span class="sxs-lookup"><span data-stu-id="1948e-134">\<userNameAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/usernameauthentication.md)|<span data-ttu-id="1948e-135">Spécifie les paramètres pour la validation du mot de passe du nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1948e-135">Specifies the settings for username password validation.</span></span> <span data-ttu-id="1948e-136">Cet élément est de type <xref:System.ServiceModel.Configuration.UserNameServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="1948e-136">This element is of type <xref:System.ServiceModel.Configuration.UserNameServiceElement>.</span></span>|  
|[<span data-ttu-id="1948e-137">\<windowsAuthentication></span><span class="sxs-lookup"><span data-stu-id="1948e-137">\<windowsAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/windowsauthentication-of-servicecredentials.md)|<span data-ttu-id="1948e-138">Spécifie les paramètres de validation des informations d’identification Windows.</span><span class="sxs-lookup"><span data-stu-id="1948e-138">Specifies the settings for Windows credential validation.</span></span> <span data-ttu-id="1948e-139">Cet élément est de type <xref:System.ServiceModel.Configuration.WindowsServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="1948e-139">This element is of type <xref:System.ServiceModel.Configuration.WindowsServiceElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1948e-140">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1948e-140">Parent Elements</span></span>  
  
|<span data-ttu-id="1948e-141">Élément</span><span class="sxs-lookup"><span data-stu-id="1948e-141">Element</span></span>|<span data-ttu-id="1948e-142">Description</span><span class="sxs-lookup"><span data-stu-id="1948e-142">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1948e-143">\<behavior></span><span class="sxs-lookup"><span data-stu-id="1948e-143">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="1948e-144">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="1948e-144">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1948e-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1948e-145">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement>
- <xref:System.ServiceModel.Description.ServiceCredentials>
- [<span data-ttu-id="1948e-146">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="1948e-146">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
