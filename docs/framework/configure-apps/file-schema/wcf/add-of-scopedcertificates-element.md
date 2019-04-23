---
title: <add> de <scopedCertificates> élément
ms.date: 03/30/2017
ms.assetid: e21c1ef8-d6d6-4bca-ac5a-6fbf4bd77412
ms.openlocfilehash: 06a624d0146745581dfe907d044d1f7d3b857902
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59119676"
---
# <a name="add-of-scopedcertificates-element"></a><span data-ttu-id="3c263-102">\<Ajouter > de \<scopedCertificates > élément</span><span class="sxs-lookup"><span data-stu-id="3c263-102">\<add> of \<scopedCertificates> Element</span></span>
<span data-ttu-id="3c263-103">Ajoute un certificat X.509 à la collection de certificats étendus.</span><span class="sxs-lookup"><span data-stu-id="3c263-103">Adds an X.509 certificate to the collection of scoped certificates.</span></span>  
  
 <span data-ttu-id="3c263-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="3c263-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="3c263-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="3c263-105">\<behaviors></span></span>  
<span data-ttu-id="3c263-106">section d’endpointBehaviors</span><span class="sxs-lookup"><span data-stu-id="3c263-106">endpointBehaviors section</span></span>  
<span data-ttu-id="3c263-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="3c263-107">\<behavior></span></span>  
<span data-ttu-id="3c263-108">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="3c263-108">\<clientCredentials></span></span>  
<span data-ttu-id="3c263-109">\<serviceCertificate></span><span class="sxs-lookup"><span data-stu-id="3c263-109">\<serviceCertificate></span></span>  
<span data-ttu-id="3c263-110">\<scopedCertificates></span><span class="sxs-lookup"><span data-stu-id="3c263-110">\<scopedCertificates></span></span>  
<span data-ttu-id="3c263-111">\<Ajouter > élément pour \<scopedCertificates ></span><span class="sxs-lookup"><span data-stu-id="3c263-111">\<add> element for \<scopedCertificates></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c263-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c263-112">Syntax</span></span>  
  
```xml  
<add findValue="String"
     storeLocation="CurrentUser/LocalMachine"
     storeName=" CurrentUser/LocalMachine"
     targetUri="string"
     x509Type="FindByThumbprint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindBySerialNumber/FindByTimeExpired/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3c263-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3c263-113">Attributes and Elements</span></span>  
 <span data-ttu-id="3c263-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3c263-114">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3c263-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="3c263-115">Attributes</span></span>  
  
|<span data-ttu-id="3c263-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="3c263-116">Attribute</span></span>|<span data-ttu-id="3c263-117">Description</span><span class="sxs-lookup"><span data-stu-id="3c263-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3c263-118">targetUri</span><span class="sxs-lookup"><span data-stu-id="3c263-118">targetUri</span></span>|<span data-ttu-id="3c263-119">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="3c263-119">String.</span></span> <span data-ttu-id="3c263-120">Spécifie l'URI du service a associé au certificat.</span><span class="sxs-lookup"><span data-stu-id="3c263-120">Specifies the URI of the service associated with the certificate.</span></span>|  
|<span data-ttu-id="3c263-121">findValue</span><span class="sxs-lookup"><span data-stu-id="3c263-121">findValue</span></span>|<span data-ttu-id="3c263-122">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="3c263-122">String.</span></span> <span data-ttu-id="3c263-123">La valeur à rechercher.</span><span class="sxs-lookup"><span data-stu-id="3c263-123">The value to search for.</span></span>|  
|<span data-ttu-id="3c263-124">x509FindType</span><span class="sxs-lookup"><span data-stu-id="3c263-124">x509FindType</span></span>|<span data-ttu-id="3c263-125">Énumération.</span><span class="sxs-lookup"><span data-stu-id="3c263-125">Enumeration.</span></span> <span data-ttu-id="3c263-126">L'un des champs de certificat à rechercher.</span><span class="sxs-lookup"><span data-stu-id="3c263-126">One of the certificate fields to search.</span></span>|  
|<span data-ttu-id="3c263-127">storeLocation</span><span class="sxs-lookup"><span data-stu-id="3c263-127">storeLocation</span></span>|<span data-ttu-id="3c263-128">Énumération.</span><span class="sxs-lookup"><span data-stu-id="3c263-128">Enumeration.</span></span> <span data-ttu-id="3c263-129">L'un des deux emplacements du magasin dans lequel effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="3c263-129">One of the two store locations to search.</span></span>|  
|<span data-ttu-id="3c263-130">storeName</span><span class="sxs-lookup"><span data-stu-id="3c263-130">storeName</span></span>|<span data-ttu-id="3c263-131">Énumération.</span><span class="sxs-lookup"><span data-stu-id="3c263-131">Enumeration.</span></span> <span data-ttu-id="3c263-132">L'un des magasins de systèmes à rechercher.</span><span class="sxs-lookup"><span data-stu-id="3c263-132">One of the system stores to search.</span></span>|  
  
## <a name="findvalue-attribute"></a><span data-ttu-id="3c263-133">findValue, attribute</span><span class="sxs-lookup"><span data-stu-id="3c263-133">findValue Attribute</span></span>  
  
|<span data-ttu-id="3c263-134">Value</span><span class="sxs-lookup"><span data-stu-id="3c263-134">Value</span></span>|<span data-ttu-id="3c263-135">Description</span><span class="sxs-lookup"><span data-stu-id="3c263-135">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="3c263-136">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3c263-136">String</span></span>|<span data-ttu-id="3c263-137">La valeur dépend du champ (spécifié par l'attribut X509FindType) qui est recherché.</span><span class="sxs-lookup"><span data-stu-id="3c263-137">The value depends on the field (specified by the X509FindType attribute) being searched.</span></span> <span data-ttu-id="3c263-138">Par exemple, lors de la recherche d'une empreinte numérique, la valeur doit être une chaîne de nombres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="3c263-138">For example, if searching for a thumbprint, the value must be a string of hexadecimal numbers.</span></span>|  
  
## <a name="x509findtype-attribute"></a><span data-ttu-id="3c263-139">x509FindType, attribut</span><span class="sxs-lookup"><span data-stu-id="3c263-139">x509FindType Attribute</span></span>  
  
|<span data-ttu-id="3c263-140">Value</span><span class="sxs-lookup"><span data-stu-id="3c263-140">Value</span></span>|<span data-ttu-id="3c263-141">Description</span><span class="sxs-lookup"><span data-stu-id="3c263-141">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="3c263-142">Énumération</span><span class="sxs-lookup"><span data-stu-id="3c263-142">Enumeration</span></span>|<span data-ttu-id="3c263-143">Les valeurs incluent : FindByThumbprint, FindBySubjectName, FindBySubjectDistinguishedName, FindByIssuerName, FindByIssuerDistinguishedName, FindBySerialNumber, FindByTimeValid, FindByTimeNotYetValid, FindBySerialNumber, FindByTimeExpired, FindByTemplateName , FindByApplicationPolicy, FindByCertificatePolicy, FindByExtension, FindByKeyUsage, FindBySubjectKeyIdentifier.</span><span class="sxs-lookup"><span data-stu-id="3c263-143">Values include: FindByThumbprint, FindBySubjectName, FindBySubjectDistinguishedName, FindByIssuerName, FindByIssuerDistinguishedName, FindBySerialNumber, FindByTimeValid, FindByTimeNotYetValid, FindBySerialNumber, FindByTimeExpired, FindByTemplateName, FindByApplicationPolicy, FindByCertificatePolicy, FindByExtension, FindByKeyUsage, FindBySubjectKeyIdentifier.</span></span>|  
  
## <a name="storelocation-attribute"></a><span data-ttu-id="3c263-144">storeLocation, attribut</span><span class="sxs-lookup"><span data-stu-id="3c263-144">storeLocation Attribute</span></span>  
  
|<span data-ttu-id="3c263-145">Value</span><span class="sxs-lookup"><span data-stu-id="3c263-145">Value</span></span>|<span data-ttu-id="3c263-146">Description</span><span class="sxs-lookup"><span data-stu-id="3c263-146">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="3c263-147">Énumération</span><span class="sxs-lookup"><span data-stu-id="3c263-147">Enumeration</span></span>|<span data-ttu-id="3c263-148">CurrentUser ou LocalMachine.</span><span class="sxs-lookup"><span data-stu-id="3c263-148">CurrentUser or LocalMachine.</span></span>|  
  
## <a name="storename-attribute"></a><span data-ttu-id="3c263-149">storeName, attribut</span><span class="sxs-lookup"><span data-stu-id="3c263-149">storeName Attribute</span></span>  
  
|<span data-ttu-id="3c263-150">Value</span><span class="sxs-lookup"><span data-stu-id="3c263-150">Value</span></span>|<span data-ttu-id="3c263-151">Description</span><span class="sxs-lookup"><span data-stu-id="3c263-151">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="3c263-152">Énumération</span><span class="sxs-lookup"><span data-stu-id="3c263-152">Enumeration</span></span>|<span data-ttu-id="3c263-153">Les valeurs incluent : AddressBook, AuthRoot, CertificateAuthority, Disallowed, My, racine, TrustedPeople et TrustedPublisher.</span><span class="sxs-lookup"><span data-stu-id="3c263-153">Values include: AddressBook, AuthRoot, CertificateAuthority, Disallowed, My, Root, TrustedPeople, and TrustedPublisher.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3c263-154">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3c263-154">Child Elements</span></span>  
 <span data-ttu-id="3c263-155">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3c263-155">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3c263-156">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3c263-156">Parent Elements</span></span>  
  
|<span data-ttu-id="3c263-157">Élément</span><span class="sxs-lookup"><span data-stu-id="3c263-157">Element</span></span>|<span data-ttu-id="3c263-158">Description</span><span class="sxs-lookup"><span data-stu-id="3c263-158">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3c263-159">\<scopedCertificates></span><span class="sxs-lookup"><span data-stu-id="3c263-159">\<scopedCertificates></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopedcertificates-element.md)|<span data-ttu-id="3c263-160">Représente une collection de certificats X.509 fournie par les services spécifiques (étendus) à des fins d’authentification.</span><span class="sxs-lookup"><span data-stu-id="3c263-160">Represents a collection of X.509 certificates provided by specific services (scoped) for authentication.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3c263-161">Notes</span><span class="sxs-lookup"><span data-stu-id="3c263-161">Remarks</span></span>  
 <span data-ttu-id="3c263-162">Cet élément permet au client de configurer un certificat de service à utiliser en fonction de l'URL du service avec lequel il communique.</span><span class="sxs-lookup"><span data-stu-id="3c263-162">This element enables the client to configure a service certificate to use based on the URL of the service it communicates with.</span></span> <span data-ttu-id="3c263-163">Ceci s'avère particulièrement utile dans les scénarios de jeton émis dans lesquels un client peut communiquer avec plusieurs services (autant le service final que les services de jeton de sécurité intermédiaire).</span><span class="sxs-lookup"><span data-stu-id="3c263-163">This is especially useful in issued token scenarios where a client can be communicating to multiple services (the end service as well as intermediary security token services).</span></span> <span data-ttu-id="3c263-164">Pour les liaisons qui utilisent la sécurité de message basée sur des certificats, ce certificat est utilisé pour chiffrer les messages au service et doit être utilisé par le service pour signer les réponses au client.</span><span class="sxs-lookup"><span data-stu-id="3c263-164">For bindings that use certificate-based message security, this certificate is used to encrypt messages to the service, and is expected to be used by the service for signing replies to the client.</span></span>  
  
 <span data-ttu-id="3c263-165">Le certificat par défaut est utilisé si une liaison requiert un certificat pour le service et qu’aucun certificat spécifique de l’URL du service n’est trouvé dans ScopedCertificates.</span><span class="sxs-lookup"><span data-stu-id="3c263-165">If a binding requires a certificate for the service and no specific certificate for the service URL is found in the ScopedCertificates, the default certificate is used.</span></span>  
  
 <span data-ttu-id="3c263-166">Pour plus d’informations, consultez la section » certificats à étendue » de [Comment : Créer un Client fédéré](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md).</span><span class="sxs-lookup"><span data-stu-id="3c263-166">For more information, see the "Scoped Certificates" section of [How to: Create a Federated Client](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="3c263-167">Exemple</span><span class="sxs-lookup"><span data-stu-id="3c263-167">Example</span></span>  
 <span data-ttu-id="3c263-168">L'exemple suivant illustre l'ajout d'un certificat X.509 à la collection.</span><span class="sxs-lookup"><span data-stu-id="3c263-168">The following example adds an X.509 certificate the collection.</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="MyEndpointBehavior">
      <clientCredentials>
        <serviceCertificate>
          <scopedCertificates>
            <add targetUri="http://www.contoso.com"
                 findValue="www.Contoso.com"
                 storeLocation="LocalMachine"
                 storeName="Root"
                 x509FindType="FindByIssuerName" />
          </scopedCertificates>
        </serviceCertificate>
      </clientCredentials>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="3c263-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c263-169">See also</span></span>

- <xref:System.ServiceModel.Configuration.X509RecipientCertificateClientElement.ScopedCertificates%2A>
- <xref:System.ServiceModel.Configuration.X509ScopedServiceCertificateElementCollection>
- <xref:System.ServiceModel.Configuration.X509ScopedServiceCertificateElement>
- <xref:System.ServiceModel.Security.X509CertificateRecipientClientCredential>
- <xref:System.ServiceModel.Security.X509CertificateRecipientClientCredential.ScopedCertificates%2A>
- [<span data-ttu-id="3c263-170">Guide pratique pour Créer un Client fédéré</span><span class="sxs-lookup"><span data-stu-id="3c263-170">How to: Create a Federated Client</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="3c263-171">Utilisation des certificats</span><span class="sxs-lookup"><span data-stu-id="3c263-171">Working with Certificates</span></span>](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="3c263-172">Sécurisation des clients</span><span class="sxs-lookup"><span data-stu-id="3c263-172">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- [<span data-ttu-id="3c263-173">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="3c263-173">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
