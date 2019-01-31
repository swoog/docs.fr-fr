---
title: <knownCertificates>
ms.date: 03/30/2017
ms.assetid: 678e21b4-6493-47c3-8359-fcf0d37e2138
ms.openlocfilehash: 4c1dc15621138aa692f0a30d285f729c2bd670d3
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55274115"
---
# <a name="knowncertificates"></a><span data-ttu-id="152c0-101">\<knownCertificates></span><span class="sxs-lookup"><span data-stu-id="152c0-101">\<knownCertificates></span></span>
<span data-ttu-id="152c0-102">Représente une collection des certificats X.509 fournis pour authentifier des informations d’identification de sécurité publiées à partir d’un service d’émission de jetons de sécurité (STS).</span><span class="sxs-lookup"><span data-stu-id="152c0-102">Represents a collection of X.509 certificates that are provided to authenticate security credentials issued from a Security Token Service (STS).</span></span>  
  
 <span data-ttu-id="152c0-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="152c0-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="152c0-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="152c0-104">\<behaviors></span></span>  
<span data-ttu-id="152c0-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="152c0-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="152c0-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="152c0-106">\<behavior></span></span>  
<span data-ttu-id="152c0-107">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="152c0-107">\<serviceCredentials></span></span>  
<span data-ttu-id="152c0-108">\<issuedTokenAuthentication></span><span class="sxs-lookup"><span data-stu-id="152c0-108">\<issuedTokenAuthentication></span></span>  
<span data-ttu-id="152c0-109">\<knownCertificates></span><span class="sxs-lookup"><span data-stu-id="152c0-109">\<knownCertificates></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="152c0-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="152c0-110">Syntax</span></span>  
  
```xml  
<knownCertificates>
  <add findValue="String"
       storeLocation="CurrentUser/LocalMachine"
       storeName=" CurrentUser/LocalMachine"
       x509FindType="FindByThumbprint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindBySerialNumber/FindByTimeExpired/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier" />
</knownCertificates>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="152c0-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="152c0-111">Attributes and Elements</span></span>  
 <span data-ttu-id="152c0-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="152c0-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="152c0-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="152c0-113">Attributes</span></span>  
 <span data-ttu-id="152c0-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="152c0-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="152c0-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="152c0-115">Child Elements</span></span>  
  
|<span data-ttu-id="152c0-116">Élément</span><span class="sxs-lookup"><span data-stu-id="152c0-116">Element</span></span>|<span data-ttu-id="152c0-117">Description</span><span class="sxs-lookup"><span data-stu-id="152c0-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="152c0-118">\<add></span><span class="sxs-lookup"><span data-stu-id="152c0-118">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-knowncertificates.md)|<span data-ttu-id="152c0-119">Ajoute un certificat X.509 à la collection.</span><span class="sxs-lookup"><span data-stu-id="152c0-119">Adds an X.509 certificate to the collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="152c0-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="152c0-120">Parent Elements</span></span>  
  
|<span data-ttu-id="152c0-121">Élément</span><span class="sxs-lookup"><span data-stu-id="152c0-121">Element</span></span>|<span data-ttu-id="152c0-122">Description</span><span class="sxs-lookup"><span data-stu-id="152c0-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="152c0-123">\<issuedTokenAuthentication></span><span class="sxs-lookup"><span data-stu-id="152c0-123">\<issuedTokenAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenauthentication-of-servicecredentials.md)|<span data-ttu-id="152c0-124">Spécifie un jeton émis en guise d'information d'identification du service.</span><span class="sxs-lookup"><span data-stu-id="152c0-124">Specifies a token issued as a service credential.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="152c0-125">Notes</span><span class="sxs-lookup"><span data-stu-id="152c0-125">Remarks</span></span>  
 <span data-ttu-id="152c0-126">Le scénario de jeton émis comporte trois étapes.</span><span class="sxs-lookup"><span data-stu-id="152c0-126">The issued token scenario has three stages.</span></span> <span data-ttu-id="152c0-127">Dans la première phase, un client tente d’accéder à un service est appelé un *secure token service*.</span><span class="sxs-lookup"><span data-stu-id="152c0-127">In the first stage, a client trying to access a service is referred to a *secure token service*.</span></span> <span data-ttu-id="152c0-128">Le service d'émission de jeton sécurisé authentifie ensuite le client et émet par la suite un jeton au client, généralement un jeton SAML (Security Assertions Markup Language).</span><span class="sxs-lookup"><span data-stu-id="152c0-128">The secure token service then authenticates the client and subsequently issues the client a token, typically a Security Assertions Markup Language (SAML) token.</span></span> <span data-ttu-id="152c0-129">Le client retourne ensuite au service avec le jeton.</span><span class="sxs-lookup"><span data-stu-id="152c0-129">The client then returns to the service with the token.</span></span> <span data-ttu-id="152c0-130">Le service recherche dans le jeton les données lui permettant de l'authentifier, et par conséquent d'authentifier le client.</span><span class="sxs-lookup"><span data-stu-id="152c0-130">The service examines the token for data that allows the service to authenticate the token and therefore the client.</span></span> <span data-ttu-id="152c0-131">Pour authentifier le jeton, le service doit connaître le certificat utilisé par le service d'émission de jeton sécurisé.</span><span class="sxs-lookup"><span data-stu-id="152c0-131">To authenticate the token, the certificate the secure token service uses must be known to the service.</span></span>  
  
 <span data-ttu-id="152c0-132">Le [ \<issuedTokenAuthentication >](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenauthentication-of-servicecredentials.md) élément est le référentiel pour les certificats de service de jeton sécurisé ce type.</span><span class="sxs-lookup"><span data-stu-id="152c0-132">The [\<issuedTokenAuthentication>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenauthentication-of-servicecredentials.md) element is the repository for any such secure token service certificates.</span></span> <span data-ttu-id="152c0-133">Pour ajouter des certificats, utilisez le [ \<knownCertificates > élément](../../../../../docs/framework/configure-apps/file-schema/wcf/knowncertificates.md).</span><span class="sxs-lookup"><span data-stu-id="152c0-133">To add certificates, use the [\<knownCertificates> element](../../../../../docs/framework/configure-apps/file-schema/wcf/knowncertificates.md).</span></span> <span data-ttu-id="152c0-134">Insérer un [ \<Ajouter >](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-knowncertificates.md) pour chaque certificat, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="152c0-134">Insert an [\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-knowncertificates.md) for each certificate, as shown in the following example.</span></span>  
  
```xml  
<issuedTokenAuthentication>
  <knownCertificates>
    <add findValue="www.contoso.com"
         storeLocation="LocalMachine"
         storeName="My"
         X509FindType="FindBySubjectName" />
  </knownCertificates>
</issuedTokenAuthentication>
```  
  
 <span data-ttu-id="152c0-135">Par défaut, les certificats doivent être obtenus auprès d'un service d'émission de jeton sécurisé.</span><span class="sxs-lookup"><span data-stu-id="152c0-135">By default, the certificates must be obtained from a secure token service.</span></span> <span data-ttu-id="152c0-136">Ces certificats « connus » garantissent que seuls les clients légitimes peuvent accéder à un service.</span><span class="sxs-lookup"><span data-stu-id="152c0-136">These "known" certificates ensure that only legitimate clients can access a service.</span></span>  
  
 <span data-ttu-id="152c0-137">Pour passer en revue les conditions requises pour un client d’être authentifiés par un service fédéré, ainsi que plus d’informations sur l’utilisation de cet élément de configuration, consultez [Comment : Configurer les informations d’identification sur un Service de fédération](../../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md).</span><span class="sxs-lookup"><span data-stu-id="152c0-137">To review conditions required for a client to be authenticated by a federated service, as well as more information on using this configuration element, see [How to: Configure Credentials on a Federation Service](../../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md).</span></span> <span data-ttu-id="152c0-138">Pour plus d’informations sur les scénarios fédérés, consultez [fédération et jetons émis](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md).</span><span class="sxs-lookup"><span data-stu-id="152c0-138">For more information about federated scenarios, see [Federation and Issued Tokens](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md).</span></span>  
  
 <span data-ttu-id="152c0-139">Pour obtenir un exemple qui montre comment remplir la collection dans la configuration, consultez [ \<Ajouter >](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-knowncertificates.md).</span><span class="sxs-lookup"><span data-stu-id="152c0-139">For an example that shows how to populate the collection in configuration, see [\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-knowncertificates.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="152c0-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="152c0-140">See also</span></span>
- <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>
- <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator.AllowedAudienceUris%2A>
- <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator.AudienceUriMode%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenServiceElement.KnownCertificates%2A>
- <xref:System.ServiceModel.Configuration.X509CertificateTrustedIssuerElementCollection>
- <xref:System.ServiceModel.Configuration.X509CertificateTrustedIssuerElement>
- <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.KnownCertificates%2A>
- [<span data-ttu-id="152c0-141">\<add></span><span class="sxs-lookup"><span data-stu-id="152c0-141">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-knowncertificates.md)
- [<span data-ttu-id="152c0-142">\<issuedTokenAuthentication></span><span class="sxs-lookup"><span data-stu-id="152c0-142">\<issuedTokenAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenauthentication-of-servicecredentials.md)
- [<span data-ttu-id="152c0-143">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="152c0-143">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="152c0-144">Guide pratique pour Configurer les informations d’identification sur un Service de fédération</span><span class="sxs-lookup"><span data-stu-id="152c0-144">How to: Configure Credentials on a Federation Service</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md)
- [<span data-ttu-id="152c0-145">Utilisation des certificats</span><span class="sxs-lookup"><span data-stu-id="152c0-145">Working with Certificates</span></span>](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="152c0-146">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="152c0-146">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="152c0-147">\<add></span><span class="sxs-lookup"><span data-stu-id="152c0-147">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-knowncertificates.md)
- [<span data-ttu-id="152c0-148">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="152c0-148">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
