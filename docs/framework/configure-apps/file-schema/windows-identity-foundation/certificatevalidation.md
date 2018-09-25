---
title: '&lt;certificateValidation&gt;'
ms.date: 03/30/2017
ms.assetid: 6c54c704-b55e-4631-88ff-4d4a5621554c
author: BrucePerlerMS
ms.openlocfilehash: 29881be43f02d275ad135efd97dc8b25a7409beb
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47074786"
---
# <a name="ltcertificatevalidationgt"></a><span data-ttu-id="f11c9-102">&lt;certificateValidation&gt;</span><span class="sxs-lookup"><span data-stu-id="f11c9-102">&lt;certificateValidation&gt;</span></span>
<span data-ttu-id="f11c9-103">Contrôle les paramètres qui utilisent des gestionnaires de jetons pour valider les certificats.</span><span class="sxs-lookup"><span data-stu-id="f11c9-103">Controls the settings that token handlers use to validate certificates.</span></span> <span data-ttu-id="f11c9-104">Ces paramètres sont remplacés si un gestionnaire spécifique est configuré avec son propre validateur.</span><span class="sxs-lookup"><span data-stu-id="f11c9-104">These settings are overridden if a specific handler is configured with its own validator.</span></span>  
  
 <span data-ttu-id="f11c9-105">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="f11c9-105">\<system.identityModel></span></span>  
<span data-ttu-id="f11c9-106">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="f11c9-106">\<identityConfiguration></span></span>  
<span data-ttu-id="f11c9-107">\<certificateValidation ></span><span class="sxs-lookup"><span data-stu-id="f11c9-107">\<certificateValidation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f11c9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f11c9-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <certificateValidation  
      certificateValidationMode="None||ChainTrust||PeerTrust||PeerOrChainTrust||Custom"  
      revocationMode="NoCheck||Offline||Online"  
      trustedStoreLocation="CurrentLocation||LocalMachine" >  
    </certificateValidation>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f11c9-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f11c9-109">Attributes and Elements</span></span>  
 <span data-ttu-id="f11c9-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f11c9-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f11c9-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="f11c9-111">Attributes</span></span>  
  
|<span data-ttu-id="f11c9-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="f11c9-112">Attribute</span></span>|<span data-ttu-id="f11c9-113">Description</span><span class="sxs-lookup"><span data-stu-id="f11c9-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f11c9-114">certificateValidationMode</span><span class="sxs-lookup"><span data-stu-id="f11c9-114">certificateValidationMode</span></span>|<span data-ttu-id="f11c9-115">Un <xref:System.ServiceModel.Security.X509CertificateValidationMode> valeur qui spécifie le mode de validation à utiliser pour le certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="f11c9-115">An <xref:System.ServiceModel.Security.X509CertificateValidationMode> value that specifies the validation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="f11c9-116">La valeur par défaut est « PeerOrChainTrust ».</span><span class="sxs-lookup"><span data-stu-id="f11c9-116">The default value is "PeerOrChainTrust".</span></span> <span data-ttu-id="f11c9-117">Pour spécifier un validateur personnalisé, définissez cet attribut « Personnalisé » et spécifiez le validateur à l’aide de la [ \<certificateValidator >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md) élément.</span><span class="sxs-lookup"><span data-stu-id="f11c9-117">To specify a custom validator, set this attribute to "Custom" and specify the validator using the [\<certificateValidator>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md) element.</span></span> <span data-ttu-id="f11c9-118">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f11c9-118">Optional.</span></span>|  
|<span data-ttu-id="f11c9-119">revocationMode</span><span class="sxs-lookup"><span data-stu-id="f11c9-119">revocationMode</span></span>|<span data-ttu-id="f11c9-120">Un <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> valeur qui spécifie le mode de révocation à utiliser pour le certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="f11c9-120">An <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> value that specifies the revocation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="f11c9-121">La valeur par défaut est « En ligne ».</span><span class="sxs-lookup"><span data-stu-id="f11c9-121">The default value is "Online".</span></span> <span data-ttu-id="f11c9-122">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f11c9-122">Optional.</span></span>|  
|<span data-ttu-id="f11c9-123">trustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="f11c9-123">trustedStoreLocation</span></span>|<span data-ttu-id="f11c9-124">Un <xref:System.Security.Cryptography.X509Certificates.StoreLocation> valeur qui spécifie le magasin de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="f11c9-124">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the X.509 certificate store.</span></span> <span data-ttu-id="f11c9-125">La valeur par défaut est « LocalMachine ».</span><span class="sxs-lookup"><span data-stu-id="f11c9-125">The default value is "LocalMachine".</span></span> <span data-ttu-id="f11c9-126">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f11c9-126">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f11c9-127">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f11c9-127">Child Elements</span></span>  
  
|<span data-ttu-id="f11c9-128">Élément</span><span class="sxs-lookup"><span data-stu-id="f11c9-128">Element</span></span>|<span data-ttu-id="f11c9-129">Description</span><span class="sxs-lookup"><span data-stu-id="f11c9-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f11c9-130">\<certificateValidator ></span><span class="sxs-lookup"><span data-stu-id="f11c9-130">\<certificateValidator></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md)|<span data-ttu-id="f11c9-131">Spécifie un type personnalisé pour la validation de certificat.</span><span class="sxs-lookup"><span data-stu-id="f11c9-131">Specifies a custom type for certificate validation.</span></span> <span data-ttu-id="f11c9-132">Ce type est utilisé uniquement si le `certificateValidationMode` attribut de la [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) élément est défini sur « Custom ».</span><span class="sxs-lookup"><span data-stu-id="f11c9-132">This type is used only if the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element is set to "Custom".</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f11c9-133">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f11c9-133">Parent Elements</span></span>  
  
|<span data-ttu-id="f11c9-134">Élément</span><span class="sxs-lookup"><span data-stu-id="f11c9-134">Element</span></span>|<span data-ttu-id="f11c9-135">Description</span><span class="sxs-lookup"><span data-stu-id="f11c9-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f11c9-136">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="f11c9-136">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="f11c9-137">Spécifie les paramètres de l’identité de niveau de service.</span><span class="sxs-lookup"><span data-stu-id="f11c9-137">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="f11c9-138">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="f11c9-138">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="f11c9-139">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="f11c9-139">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f11c9-140">Notes</span><span class="sxs-lookup"><span data-stu-id="f11c9-140">Remarks</span></span>  
 <span data-ttu-id="f11c9-141">Un `<certificateValidation>` élément peut être spécifié au niveau du service sous le `<identityConfiguration>` élément ou sur le niveau de collection de gestionnaires de jetons de sécurité sous la `<securityTokenHandlerConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="f11c9-141">A `<certificateValidation>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="f11c9-142">Les paramètres sur une collection de gestionnaires de jetons remplacent celles spécifiées sur le service.</span><span class="sxs-lookup"><span data-stu-id="f11c9-142">Settings on a token handler collection override those specified on the service.</span></span> <span data-ttu-id="f11c9-143">Certains gestionnaires de jetons permettent de spécifier les paramètres de validation de certificat dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="f11c9-143">Some token handlers allow you to specify certificate validation settings in configuration.</span></span> <span data-ttu-id="f11c9-144">Paramètres sur les gestionnaires de jetons individuels remplacent celles spécifiées à la fois au niveau du service et sur la collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f11c9-144">Settings on individual token handlers override those specified both at the service level and on the security token handler collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f11c9-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="f11c9-145">Example</span></span>  
  
```xml  
<certificateValidation certificateValidationMode="PeerOrChainTrust"  
                       revocationMode="Online"  
                       trustedStoreLocation="LocalMachine" />  
```
