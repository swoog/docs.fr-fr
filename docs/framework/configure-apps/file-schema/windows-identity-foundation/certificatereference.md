---
title: <certificateReference>
ms.date: 03/30/2017
ms.assetid: 2ac8bc14-e9f1-48fb-b662-f5991558fbe4
author: BrucePerlerMS
ms.openlocfilehash: 6c9c77f96ff6032de43d9b5a257bc0796a19b858
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61667377"
---
# <a name="certificatereference"></a><span data-ttu-id="276f6-101">\<certificateReference></span><span class="sxs-lookup"><span data-stu-id="276f6-101">\<certificateReference></span></span>
<span data-ttu-id="276f6-102">Spécifie les paramètres qui sont utilisés pour rechercher et valider le certificat X.509 dans un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="276f6-102">Specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span>  
  
 <span data-ttu-id="276f6-103">\<system.identityModel.services></span><span class="sxs-lookup"><span data-stu-id="276f6-103">\<system.identityModel.services></span></span>  
<span data-ttu-id="276f6-104">\<federationConfiguration></span><span class="sxs-lookup"><span data-stu-id="276f6-104">\<federationConfiguration></span></span>  
<span data-ttu-id="276f6-105">\<serviceCertificate></span><span class="sxs-lookup"><span data-stu-id="276f6-105">\<serviceCertificate></span></span>  
<span data-ttu-id="276f6-106">\<certificateReference></span><span class="sxs-lookup"><span data-stu-id="276f6-106">\<certificateReference></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="276f6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="276f6-107">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <serviceCertificate>  
      <certificateReference   
        storeName="AddressBook||AuthRoot||CertificateAuthority||Disallowed||My||Root||TrustedPeople||TrustedPublisher"  
        storeLocation="CurrentUser||LocalMachine"  
        x509FindType="FindByThumbprint||FindBySubjectName||FindBySubjectDistinguishedName||FindByIssuerName||FindByIssuerDistinguishedName||FindBySerialNumber||FindByTimeValid||FindByTimeNotYetValid||FindByTimeExpired||FindByTemplateName||FindByApplicationPolicy||FindByCertificatePolicy||FindByExtension||FindByKeyUsage||FindBySubjectKeyIdentifier"  
        findValue=xs:String  
        isChainIncluded=xs:Boolean >  
      </certificateReference>  
    </serviceCertificate>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="276f6-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="276f6-108">Attributes and Elements</span></span>  
 <span data-ttu-id="276f6-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="276f6-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="276f6-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="276f6-110">Attributes</span></span>  
  
|<span data-ttu-id="276f6-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="276f6-111">Attribute</span></span>|<span data-ttu-id="276f6-112">Description</span><span class="sxs-lookup"><span data-stu-id="276f6-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="276f6-113">storeName</span><span class="sxs-lookup"><span data-stu-id="276f6-113">storeName</span></span>|<span data-ttu-id="276f6-114">Le nom du magasin de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="276f6-114">The name of the X.509 certificate store.</span></span> <span data-ttu-id="276f6-115">La valeur par défaut est « My ».</span><span class="sxs-lookup"><span data-stu-id="276f6-115">The default is "My".</span></span> <span data-ttu-id="276f6-116">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="276f6-116">Optional.</span></span>|  
|<span data-ttu-id="276f6-117">storeLocation</span><span class="sxs-lookup"><span data-stu-id="276f6-117">storeLocation</span></span>|<span data-ttu-id="276f6-118">Un <xref:System.Security.Cryptography.X509Certificates.StoreLocation> valeur qui spécifie l’emplacement du magasin de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="276f6-118">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the location of the X.509 certificate store.</span></span> <span data-ttu-id="276f6-119">La valeur par défaut est « LocalMachine ».</span><span class="sxs-lookup"><span data-stu-id="276f6-119">The default value is "LocalMachine".</span></span> <span data-ttu-id="276f6-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="276f6-120">Optional.</span></span>|  
|<span data-ttu-id="276f6-121">x509FindType</span><span class="sxs-lookup"><span data-stu-id="276f6-121">x509FindType</span></span>|<span data-ttu-id="276f6-122">Un <xref:System.Security.Cryptography.X509Certificates.X509FindType> valeur qui spécifie le type de recherche doit être exécuté.</span><span class="sxs-lookup"><span data-stu-id="276f6-122">An <xref:System.Security.Cryptography.X509Certificates.X509FindType> value that specifies the type of search that is to be executed.</span></span> <span data-ttu-id="276f6-123">La valeur par défaut est « FindBySubjectDistinguishedName ».</span><span class="sxs-lookup"><span data-stu-id="276f6-123">The default is "FindBySubjectDistinguishedName".</span></span> <span data-ttu-id="276f6-124">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="276f6-124">Optional.</span></span>|  
|<span data-ttu-id="276f6-125">findValue</span><span class="sxs-lookup"><span data-stu-id="276f6-125">findValue</span></span>|<span data-ttu-id="276f6-126">Valeur à rechercher dans le magasin de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="276f6-126">The value to search for in the X.509 certificate store.</span></span> <span data-ttu-id="276f6-127">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="276f6-127">Optional.</span></span>|  
|<span data-ttu-id="276f6-128">isChainIncluded</span><span class="sxs-lookup"><span data-stu-id="276f6-128">isChainIncluded</span></span>|<span data-ttu-id="276f6-129">Spécifie si la validation doit être effectuée à l’aide de la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="276f6-129">Specifies whether validation should be performed by using the certificate chain.</span></span> <span data-ttu-id="276f6-130">La valeur par défaut est « true » ; la validation est effectuée à l’aide de la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="276f6-130">The default is "true"; validation is performed by using the certificate chain.</span></span> <span data-ttu-id="276f6-131">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="276f6-131">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="276f6-132">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="276f6-132">Child Elements</span></span>  
 <span data-ttu-id="276f6-133">Aucun.</span><span class="sxs-lookup"><span data-stu-id="276f6-133">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="276f6-134">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="276f6-134">Parent Elements</span></span>  
  
|<span data-ttu-id="276f6-135">Élément</span><span class="sxs-lookup"><span data-stu-id="276f6-135">Element</span></span>|<span data-ttu-id="276f6-136">Description</span><span class="sxs-lookup"><span data-stu-id="276f6-136">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="276f6-137">\<serviceCertificate></span><span class="sxs-lookup"><span data-stu-id="276f6-137">\<serviceCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/servicecertificate.md)|<span data-ttu-id="276f6-138">Configure le certificat qui est utilisé pour chiffrer et déchiffrer les jetons.</span><span class="sxs-lookup"><span data-stu-id="276f6-138">Configures the certificate that is used to encrypt and decrypt tokens.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="276f6-139">Notes</span><span class="sxs-lookup"><span data-stu-id="276f6-139">Remarks</span></span>  
 <span data-ttu-id="276f6-140">Le `<certificateReference>` élément spécifie les paramètres qui sont utilisés pour rechercher et valider le certificat X.509 dans un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="276f6-140">The `<certificateReference>` element specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span> <span data-ttu-id="276f6-141">Lorsqu’il est spécifié comme élément enfant de le `<serviceCertficate>` élément, elle spécifie les paramètres d’emplacement et la vérification du certificat X.509 qui est utilisée pour chiffrer et déchiffrer les jetons.</span><span class="sxs-lookup"><span data-stu-id="276f6-141">When it is specified as the child element of the `<serviceCertficate>` element, it specifies the location and verification settings of the X.509 certificate that is used to encrypt and decrypt tokens.</span></span> <span data-ttu-id="276f6-142">Le `<certificateReference>` élément est représenté par la <xref:System.ServiceModel.Configuration.CertificateReferenceElement> classe.</span><span class="sxs-lookup"><span data-stu-id="276f6-142">The `<certificateReference>` element is represented by the <xref:System.ServiceModel.Configuration.CertificateReferenceElement> class.</span></span>
