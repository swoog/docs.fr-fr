---
title: '&lt;certificate&gt;, élément'
ms.date: 03/30/2017
ms.assetid: 9b3d9233-ef35-477a-bf5d-efd1e80a52f4
ms.openlocfilehash: 5329fb276766ca2bd24f0fd3aef793fbb3b1f8b8
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43397992"
---
# <a name="ltcertificategt-element"></a><span data-ttu-id="3be4f-102">&lt;certificate&gt;, élément</span><span class="sxs-lookup"><span data-stu-id="3be4f-102">&lt;certificate&gt; Element</span></span>
<span data-ttu-id="3be4f-103">Spécifie un certificat X.509 à utiliser pour signer et chiffrer des messages pour les clients de réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="3be4f-103">Specifies an X.509 certificate to use for signing and encrypting messages for peer-to-peer clients.</span></span>  
  
 <span data-ttu-id="3be4f-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="3be4f-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="3be4f-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="3be4f-105">\<behaviors></span></span>  
<span data-ttu-id="3be4f-106">\<endpointBehaviors ></span><span class="sxs-lookup"><span data-stu-id="3be4f-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="3be4f-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="3be4f-107">\<behavior></span></span>  
<span data-ttu-id="3be4f-108">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="3be4f-108">\<clientCredentials></span></span>  
<span data-ttu-id="3be4f-109">\<homologue ></span><span class="sxs-lookup"><span data-stu-id="3be4f-109">\<peer></span></span>  
<span data-ttu-id="3be4f-110">\<certificate></span><span class="sxs-lookup"><span data-stu-id="3be4f-110">\<certificate></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3be4f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3be4f-111">Syntax</span></span>  
  
```xml  
<certificate findValue="String"   
  
storeLocation="LocalMachine/CurrentUser"  
      storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"  
      X509FindType="FindByThumbPrint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3be4f-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3be4f-112">Attributes and Elements</span></span>  
 <span data-ttu-id="3be4f-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3be4f-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3be4f-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="3be4f-114">Attributes</span></span>  
  
|<span data-ttu-id="3be4f-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="3be4f-115">Attribute</span></span>|<span data-ttu-id="3be4f-116">Description</span><span class="sxs-lookup"><span data-stu-id="3be4f-116">Description</span></span>|  
|---------------|-----------------|  
|`findValue`|<span data-ttu-id="3be4f-117">Chaîne qui contient la valeur à rechercher dans le magasin de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="3be4f-117">A string that contains the value to search for in the X.509 certificate store.</span></span> <span data-ttu-id="3be4f-118">Le type contenu dans l'attribut doit répondre aux spécifications du `x509FindType` spécifié.</span><span class="sxs-lookup"><span data-stu-id="3be4f-118">The type contained in the attribute must satisfy the requirements of the specified `x509FindType`.</span></span> <span data-ttu-id="3be4f-119">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="3be4f-119">The default is an empty string.</span></span>|  
|`storeLocation`|<span data-ttu-id="3be4f-120">Indique l'emplacement du magasin de certificats X.509 utilisé par le client pour valider le certificat de l'homologue.</span><span class="sxs-lookup"><span data-stu-id="3be4f-120">Specifies the location of the X.509 certificate store that the client uses to validate the peer's certificate against.</span></span> <span data-ttu-id="3be4f-121">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3be4f-121">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="3be4f-122">-LocalMachine : magasin de certificats assigné à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="3be4f-122">-   LocalMachine: the certificate store assigned to the local machine.</span></span><br /><span data-ttu-id="3be4f-123">-CurrentUser : magasin de certificats assigné à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="3be4f-123">-   CurrentUser: the certificate store assigned to the current user.</span></span><br /><br /> <span data-ttu-id="3be4f-124">La valeur par défaut est LocalMachine.</span><span class="sxs-lookup"><span data-stu-id="3be4f-124">The default is LocalMachine.</span></span>|  
|`storeName`|<span data-ttu-id="3be4f-125">Spécifie le nom du magasin de certificats X.509 à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="3be4f-125">Specifies the name of the X.509 certificate store to open.</span></span> <span data-ttu-id="3be4f-126">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3be4f-126">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="3be4f-127">-AddressBook : Magasin de certificats pour les autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="3be4f-127">-   AddressBook: Certificate store for other users.</span></span><br /><span data-ttu-id="3be4f-128">-AuthRoot : Magasin de certificats pour autorités de certification tierce (CA).</span><span class="sxs-lookup"><span data-stu-id="3be4f-128">-   AuthRoot: Certificate store for third-party certification authorities (CAs).</span></span><br /><span data-ttu-id="3be4f-129">-CertificateAuthority : Magasin de certificats pour les autorités de certification intermédiaires (CA).</span><span class="sxs-lookup"><span data-stu-id="3be4f-129">-   CertificateAuthority: Certificate store for intermediate certification authorities (CAs).</span></span><br /><span data-ttu-id="3be4f-130">-Interdit : Magasin de certificats pour les certificats révoqués.</span><span class="sxs-lookup"><span data-stu-id="3be4f-130">-   Disallowed: Certificate store for revoked certificates.</span></span><br /><span data-ttu-id="3be4f-131">-My : Magasin de certificats pour les certificats personnels.</span><span class="sxs-lookup"><span data-stu-id="3be4f-131">-   My: Certificate store for personal certificates.</span></span><br /><span data-ttu-id="3be4f-132">-Root : Magasin de certificats pour autorités de certification racine approuvée (CA).</span><span class="sxs-lookup"><span data-stu-id="3be4f-132">-   Root: Certificate store for trusted root certification authorities (CAs).</span></span><br /><span data-ttu-id="3be4f-133">-TrustedPeople : Magasin de certificats pour directement-personnes et ressources.</span><span class="sxs-lookup"><span data-stu-id="3be4f-133">-   TrustedPeople: Certificate store for directly-trusted people and resources.</span></span><br /><span data-ttu-id="3be4f-134">-TrustedPublisher : Magasin de certificats pour les éditeurs directement approuvés.</span><span class="sxs-lookup"><span data-stu-id="3be4f-134">-   TrustedPublisher: Certificate store for directly-trusted publishers.</span></span><br /><br /> <span data-ttu-id="3be4f-135">La valeur par défaut est My.</span><span class="sxs-lookup"><span data-stu-id="3be4f-135">The default is My.</span></span>|  
|`X509FindType`|<span data-ttu-id="3be4f-136">Définit le type de recherche X.509 à exécuter.</span><span class="sxs-lookup"><span data-stu-id="3be4f-136">Defines the type of X.509 search to be executed.</span></span> <span data-ttu-id="3be4f-137">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3be4f-137">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="3be4f-138">-FindByThumbPrint</span><span class="sxs-lookup"><span data-stu-id="3be4f-138">-   FindByThumbPrint</span></span><br /><span data-ttu-id="3be4f-139">-FindBySubjectName</span><span class="sxs-lookup"><span data-stu-id="3be4f-139">-   FindBySubjectName</span></span><br /><span data-ttu-id="3be4f-140">-FindBySubjectDistinguishedName</span><span class="sxs-lookup"><span data-stu-id="3be4f-140">-   FindBySubjectDistinguishedName</span></span><br /><span data-ttu-id="3be4f-141">-FindByIssuerName</span><span class="sxs-lookup"><span data-stu-id="3be4f-141">-   FindByIssuerName</span></span><br /><span data-ttu-id="3be4f-142">-FindByIssuerDistinguishedName</span><span class="sxs-lookup"><span data-stu-id="3be4f-142">-   FindByIssuerDistinguishedName</span></span><br /><span data-ttu-id="3be4f-143">-FindBySerialNumber</span><span class="sxs-lookup"><span data-stu-id="3be4f-143">-   FindBySerialNumber</span></span><br /><span data-ttu-id="3be4f-144">-FindByTimeValid</span><span class="sxs-lookup"><span data-stu-id="3be4f-144">-   FindByTimeValid</span></span><br /><span data-ttu-id="3be4f-145">-FindByTimeNotYetValid</span><span class="sxs-lookup"><span data-stu-id="3be4f-145">-   FindByTimeNotYetValid</span></span><br /><span data-ttu-id="3be4f-146">-FindByTemplateName</span><span class="sxs-lookup"><span data-stu-id="3be4f-146">-   FindByTemplateName</span></span><br /><span data-ttu-id="3be4f-147">-FindByApplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="3be4f-147">-   FindByApplicationPolicy</span></span><br /><span data-ttu-id="3be4f-148">-FindByCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3be4f-148">-   FindByCertificatePolicy</span></span><br /><span data-ttu-id="3be4f-149">-FindByExtension</span><span class="sxs-lookup"><span data-stu-id="3be4f-149">-   FindByExtension</span></span><br /><span data-ttu-id="3be4f-150">-FindByKeyUsage</span><span class="sxs-lookup"><span data-stu-id="3be4f-150">-   FindByKeyUsage</span></span><br /><span data-ttu-id="3be4f-151">-FindBySubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="3be4f-151">-   FindBySubjectKeyIdentifier</span></span><br /><br /> <span data-ttu-id="3be4f-152">Le type contenu dans l'attribut `findValue` doit répondre aux spécifications du `X509FindType` spécifié.</span><span class="sxs-lookup"><span data-stu-id="3be4f-152">The type contained in the `findValue` attribute must satisfy the requirements of the specified `X509FindType`.</span></span><br /><br /> <span data-ttu-id="3be4f-153">La valeur par défaut est FindBySubjectDistinguishedName.</span><span class="sxs-lookup"><span data-stu-id="3be4f-153">The default value is FindBySubjectDistinguishedName.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3be4f-154">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3be4f-154">Child Elements</span></span>  
 <span data-ttu-id="3be4f-155">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3be4f-155">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3be4f-156">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3be4f-156">Parent Elements</span></span>  
  
|<span data-ttu-id="3be4f-157">Élément</span><span class="sxs-lookup"><span data-stu-id="3be4f-157">Element</span></span>|<span data-ttu-id="3be4f-158">Description</span><span class="sxs-lookup"><span data-stu-id="3be4f-158">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3be4f-159">\<peer></span><span class="sxs-lookup"><span data-stu-id="3be4f-159">\<peer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-clientcredentials-element.md)|<span data-ttu-id="3be4f-160">Spécifie les informations d'identification utilisées lors de l'authentification de clients de réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="3be4f-160">Specifies credentials used when authenticating peer-to-peer clients.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3be4f-161">Notes</span><span class="sxs-lookup"><span data-stu-id="3be4f-161">Remarks</span></span>  
 <span data-ttu-id="3be4f-162">Cet élément de configuration contient une instance de X509Certificate2 utilisée lors de l'authentification de voisins dans la maille d'homologues.</span><span class="sxs-lookup"><span data-stu-id="3be4f-162">This configuration element contains a X509Certificate2 instance used when authenticating neighbors in the peer mesh.</span></span>  
  
 <span data-ttu-id="3be4f-163">Pour plus d’informations sur la programmation de peer-to-peer, consultez [mise en réseau Peer-to-Peer](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md).</span><span class="sxs-lookup"><span data-stu-id="3be4f-163">For more information about peer-to-peer programming, see [Peer-to-Peer Networking](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="3be4f-164">Exemple</span><span class="sxs-lookup"><span data-stu-id="3be4f-164">Example</span></span>  
 <span data-ttu-id="3be4f-165">Le code suivant spécifie comment rechercher le certificat utilisé dans un scénario de réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="3be4f-165">The following code specifies how to find the certificate used in a peer-to-peer scenario.</span></span>  
  
```xml  
<behaviors>  
 <endpointBehaviors>  
  <behavior name="MyEndpointBehavior">  
   <clientCredentials>  
    <peer>  
     <certificate findValue="www.contoso.com"   
                   storeLocation="LocalMachine"  
                   x509FindType="FindByIssuerName" />  
    </peer>  
   </clientCredentials>  
  </behavior>  
</endpointBehaviors>  
```  
  
## <a name="see-also"></a><span data-ttu-id="3be4f-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3be4f-166">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerCredentialElement>  
 <xref:System.ServiceModel.Configuration.PeerCredentialElement.Certificate%2A>  
 <xref:System.ServiceModel.Configuration.X509PeerCertificateElement>  
 <xref:System.ServiceModel.Security.PeerCredential.Certificate%2A>  
 [<span data-ttu-id="3be4f-167">Utilisation des certificats</span><span class="sxs-lookup"><span data-stu-id="3be4f-167">Working with Certificates</span></span>](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [<span data-ttu-id="3be4f-168">Réseaux homologues</span><span class="sxs-lookup"><span data-stu-id="3be4f-168">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)  
 [<span data-ttu-id="3be4f-169">Authentification de Message de canal homologue</span><span class="sxs-lookup"><span data-stu-id="3be4f-169">Peer Channel Message Authentication</span></span>](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)  
 [<span data-ttu-id="3be4f-170">Authentification personnalisée de canal homologue</span><span class="sxs-lookup"><span data-stu-id="3be4f-170">Peer Channel Custom Authentication</span></span>](https://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)  
 [<span data-ttu-id="3be4f-171">Sécurisation des applications de canal homologue</span><span class="sxs-lookup"><span data-stu-id="3be4f-171">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
