---
title: '&lt;CertificateReference&gt;'
ms.date: 03/30/2017
ms.assetid: 2ac8bc14-e9f1-48fb-b662-f5991558fbe4
author: BrucePerlerMS
ms.openlocfilehash: e04dc90134aadfb8af7b0800c7144963d267f513
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47075081"
---
# <a name="ltcertificatereferencegt"></a><span data-ttu-id="b36ac-102">&lt;CertificateReference&gt;</span><span class="sxs-lookup"><span data-stu-id="b36ac-102">&lt;certificateReference&gt;</span></span>
<span data-ttu-id="b36ac-103">Spécifie les paramètres qui sont utilisés pour rechercher et valider le certificat X.509 dans un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="b36ac-103">Specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span>  
  
 <span data-ttu-id="b36ac-104">\<system.identityModel.services ></span><span class="sxs-lookup"><span data-stu-id="b36ac-104">\<system.identityModel.services></span></span>  
<span data-ttu-id="b36ac-105">\<federationConfiguration ></span><span class="sxs-lookup"><span data-stu-id="b36ac-105">\<federationConfiguration></span></span>  
<span data-ttu-id="b36ac-106">\<serviceCertificate ></span><span class="sxs-lookup"><span data-stu-id="b36ac-106">\<serviceCertificate></span></span>  
<span data-ttu-id="b36ac-107">\<certificateReference ></span><span class="sxs-lookup"><span data-stu-id="b36ac-107">\<certificateReference></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b36ac-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b36ac-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b36ac-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b36ac-109">Attributes and Elements</span></span>  
 <span data-ttu-id="b36ac-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b36ac-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b36ac-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="b36ac-111">Attributes</span></span>  
  
|<span data-ttu-id="b36ac-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="b36ac-112">Attribute</span></span>|<span data-ttu-id="b36ac-113">Description</span><span class="sxs-lookup"><span data-stu-id="b36ac-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b36ac-114">storeName</span><span class="sxs-lookup"><span data-stu-id="b36ac-114">storeName</span></span>|<span data-ttu-id="b36ac-115">Le nom du magasin de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="b36ac-115">The name of the X.509 certificate store.</span></span> <span data-ttu-id="b36ac-116">La valeur par défaut est « My ».</span><span class="sxs-lookup"><span data-stu-id="b36ac-116">The default is "My".</span></span> <span data-ttu-id="b36ac-117">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="b36ac-117">Optional.</span></span>|  
|<span data-ttu-id="b36ac-118">storeLocation</span><span class="sxs-lookup"><span data-stu-id="b36ac-118">storeLocation</span></span>|<span data-ttu-id="b36ac-119">Un <xref:System.Security.Cryptography.X509Certificates.StoreLocation> valeur qui spécifie l’emplacement du magasin de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="b36ac-119">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the location of the X.509 certificate store.</span></span> <span data-ttu-id="b36ac-120">La valeur par défaut est « LocalMachine ».</span><span class="sxs-lookup"><span data-stu-id="b36ac-120">The default value is "LocalMachine".</span></span> <span data-ttu-id="b36ac-121">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="b36ac-121">Optional.</span></span>|  
|<span data-ttu-id="b36ac-122">x509FindType</span><span class="sxs-lookup"><span data-stu-id="b36ac-122">x509FindType</span></span>|<span data-ttu-id="b36ac-123">Un <xref:System.Security.Cryptography.X509Certificates.X509FindType> valeur qui spécifie le type de recherche doit être exécuté.</span><span class="sxs-lookup"><span data-stu-id="b36ac-123">An <xref:System.Security.Cryptography.X509Certificates.X509FindType> value that specifies the type of search that is to be executed.</span></span> <span data-ttu-id="b36ac-124">La valeur par défaut est « FindBySubjectDistinguishedName ».</span><span class="sxs-lookup"><span data-stu-id="b36ac-124">The default is "FindBySubjectDistinguishedName".</span></span> <span data-ttu-id="b36ac-125">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="b36ac-125">Optional.</span></span>|  
|<span data-ttu-id="b36ac-126">findValue</span><span class="sxs-lookup"><span data-stu-id="b36ac-126">findValue</span></span>|<span data-ttu-id="b36ac-127">Valeur à rechercher dans le magasin de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="b36ac-127">The value to search for in the X.509 certificate store.</span></span> <span data-ttu-id="b36ac-128">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="b36ac-128">Optional.</span></span>|  
|<span data-ttu-id="b36ac-129">isChainIncluded</span><span class="sxs-lookup"><span data-stu-id="b36ac-129">isChainIncluded</span></span>|<span data-ttu-id="b36ac-130">Spécifie si la validation doit être effectuée à l’aide de la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="b36ac-130">Specifies whether validation should be performed by using the certificate chain.</span></span> <span data-ttu-id="b36ac-131">La valeur par défaut est « true » ; la validation est effectuée à l’aide de la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="b36ac-131">The default is "true"; validation is performed by using the certificate chain.</span></span> <span data-ttu-id="b36ac-132">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="b36ac-132">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b36ac-133">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b36ac-133">Child Elements</span></span>  
 <span data-ttu-id="b36ac-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b36ac-134">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b36ac-135">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b36ac-135">Parent Elements</span></span>  
  
|<span data-ttu-id="b36ac-136">Élément</span><span class="sxs-lookup"><span data-stu-id="b36ac-136">Element</span></span>|<span data-ttu-id="b36ac-137">Description</span><span class="sxs-lookup"><span data-stu-id="b36ac-137">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b36ac-138">\<serviceCertificate ></span><span class="sxs-lookup"><span data-stu-id="b36ac-138">\<serviceCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/servicecertificate.md)|<span data-ttu-id="b36ac-139">Configure le certificat qui est utilisé pour chiffrer et déchiffrer les jetons.</span><span class="sxs-lookup"><span data-stu-id="b36ac-139">Configures the certificate that is used to encrypt and decrypt tokens.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b36ac-140">Notes</span><span class="sxs-lookup"><span data-stu-id="b36ac-140">Remarks</span></span>  
 <span data-ttu-id="b36ac-141">Le `<certificateReference>` élément spécifie les paramètres qui sont utilisés pour rechercher et valider le certificat X.509 dans un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="b36ac-141">The `<certificateReference>` element specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span> <span data-ttu-id="b36ac-142">Lorsqu’il est spécifié comme élément enfant de le `<serviceCertficate>` élément, elle spécifie les paramètres d’emplacement et la vérification du certificat X.509 qui est utilisée pour chiffrer et déchiffrer les jetons.</span><span class="sxs-lookup"><span data-stu-id="b36ac-142">When it is specified as the child element of the `<serviceCertficate>` element, it specifies the location and verification settings of the X.509 certificate that is used to encrypt and decrypt tokens.</span></span> <span data-ttu-id="b36ac-143">Le `<certificateReference>` élément est représenté par la <xref:System.ServiceModel.Configuration.CertificateReferenceElement> classe.</span><span class="sxs-lookup"><span data-stu-id="b36ac-143">The `<certificateReference>` element is represented by the <xref:System.ServiceModel.Configuration.CertificateReferenceElement> class.</span></span>
