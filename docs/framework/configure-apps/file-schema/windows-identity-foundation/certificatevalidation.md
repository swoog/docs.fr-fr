---
title: <certificateValidation>
ms.date: 03/30/2017
ms.assetid: 6c54c704-b55e-4631-88ff-4d4a5621554c
author: BrucePerlerMS
ms.openlocfilehash: 7b8823d792e3f15846a9483d670994be4b368980
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61667351"
---
# <a name="certificatevalidation"></a><span data-ttu-id="e5169-101">\<certificateValidation></span><span class="sxs-lookup"><span data-stu-id="e5169-101">\<certificateValidation></span></span>
<span data-ttu-id="e5169-102">Contrôle les paramètres qui utilisent des gestionnaires de jetons pour valider les certificats.</span><span class="sxs-lookup"><span data-stu-id="e5169-102">Controls the settings that token handlers use to validate certificates.</span></span> <span data-ttu-id="e5169-103">Ces paramètres sont remplacés si un gestionnaire spécifique est configuré avec son propre validateur.</span><span class="sxs-lookup"><span data-stu-id="e5169-103">These settings are overridden if a specific handler is configured with its own validator.</span></span>  
  
 <span data-ttu-id="e5169-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="e5169-104">\<system.identityModel></span></span>  
<span data-ttu-id="e5169-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="e5169-105">\<identityConfiguration></span></span>  
<span data-ttu-id="e5169-106">\<certificateValidation></span><span class="sxs-lookup"><span data-stu-id="e5169-106">\<certificateValidation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5169-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5169-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e5169-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e5169-108">Attributes and Elements</span></span>  
 <span data-ttu-id="e5169-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e5169-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e5169-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="e5169-110">Attributes</span></span>  
  
|<span data-ttu-id="e5169-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="e5169-111">Attribute</span></span>|<span data-ttu-id="e5169-112">Description</span><span class="sxs-lookup"><span data-stu-id="e5169-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e5169-113">certificateValidationMode</span><span class="sxs-lookup"><span data-stu-id="e5169-113">certificateValidationMode</span></span>|<span data-ttu-id="e5169-114">Un <xref:System.ServiceModel.Security.X509CertificateValidationMode> valeur qui spécifie le mode de validation à utiliser pour le certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="e5169-114">An <xref:System.ServiceModel.Security.X509CertificateValidationMode> value that specifies the validation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="e5169-115">La valeur par défaut est « PeerOrChainTrust ».</span><span class="sxs-lookup"><span data-stu-id="e5169-115">The default value is "PeerOrChainTrust".</span></span> <span data-ttu-id="e5169-116">Pour spécifier un validateur personnalisé, définissez cet attribut « Personnalisé » et spécifiez le validateur à l’aide de la [ \<certificateValidator >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md) élément.</span><span class="sxs-lookup"><span data-stu-id="e5169-116">To specify a custom validator, set this attribute to "Custom" and specify the validator using the [\<certificateValidator>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md) element.</span></span> <span data-ttu-id="e5169-117">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="e5169-117">Optional.</span></span>|  
|<span data-ttu-id="e5169-118">revocationMode</span><span class="sxs-lookup"><span data-stu-id="e5169-118">revocationMode</span></span>|<span data-ttu-id="e5169-119">Un <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> valeur qui spécifie le mode de révocation à utiliser pour le certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="e5169-119">An <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> value that specifies the revocation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="e5169-120">La valeur par défaut est « En ligne ».</span><span class="sxs-lookup"><span data-stu-id="e5169-120">The default value is "Online".</span></span> <span data-ttu-id="e5169-121">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="e5169-121">Optional.</span></span>|  
|<span data-ttu-id="e5169-122">trustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="e5169-122">trustedStoreLocation</span></span>|<span data-ttu-id="e5169-123">Un <xref:System.Security.Cryptography.X509Certificates.StoreLocation> valeur qui spécifie le magasin de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="e5169-123">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the X.509 certificate store.</span></span> <span data-ttu-id="e5169-124">La valeur par défaut est « LocalMachine ».</span><span class="sxs-lookup"><span data-stu-id="e5169-124">The default value is "LocalMachine".</span></span> <span data-ttu-id="e5169-125">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="e5169-125">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e5169-126">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e5169-126">Child Elements</span></span>  
  
|<span data-ttu-id="e5169-127">Élément</span><span class="sxs-lookup"><span data-stu-id="e5169-127">Element</span></span>|<span data-ttu-id="e5169-128">Description</span><span class="sxs-lookup"><span data-stu-id="e5169-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e5169-129">\<certificateValidator></span><span class="sxs-lookup"><span data-stu-id="e5169-129">\<certificateValidator></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md)|<span data-ttu-id="e5169-130">Spécifie un type personnalisé pour la validation de certificat.</span><span class="sxs-lookup"><span data-stu-id="e5169-130">Specifies a custom type for certificate validation.</span></span> <span data-ttu-id="e5169-131">Ce type est utilisé uniquement si le `certificateValidationMode` attribut de la [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) élément est défini sur « Custom ».</span><span class="sxs-lookup"><span data-stu-id="e5169-131">This type is used only if the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element is set to "Custom".</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e5169-132">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e5169-132">Parent Elements</span></span>  
  
|<span data-ttu-id="e5169-133">Élément</span><span class="sxs-lookup"><span data-stu-id="e5169-133">Element</span></span>|<span data-ttu-id="e5169-134">Description</span><span class="sxs-lookup"><span data-stu-id="e5169-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e5169-135">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="e5169-135">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="e5169-136">Spécifie les paramètres de l’identité de niveau de service.</span><span class="sxs-lookup"><span data-stu-id="e5169-136">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="e5169-137">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="e5169-137">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="e5169-138">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="e5169-138">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e5169-139">Notes</span><span class="sxs-lookup"><span data-stu-id="e5169-139">Remarks</span></span>  
 <span data-ttu-id="e5169-140">Un `<certificateValidation>` élément peut être spécifié au niveau du service sous le `<identityConfiguration>` élément ou sur le niveau de collection de gestionnaires de jetons de sécurité sous la `<securityTokenHandlerConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="e5169-140">A `<certificateValidation>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="e5169-141">Les paramètres sur une collection de gestionnaires de jetons remplacent celles spécifiées sur le service.</span><span class="sxs-lookup"><span data-stu-id="e5169-141">Settings on a token handler collection override those specified on the service.</span></span> <span data-ttu-id="e5169-142">Certains gestionnaires de jetons permettent de spécifier les paramètres de validation de certificat dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="e5169-142">Some token handlers allow you to specify certificate validation settings in configuration.</span></span> <span data-ttu-id="e5169-143">Paramètres sur les gestionnaires de jetons individuels remplacent celles spécifiées à la fois au niveau du service et sur la collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e5169-143">Settings on individual token handlers override those specified both at the service level and on the security token handler collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e5169-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="e5169-144">Example</span></span>  
  
```xml  
<certificateValidation certificateValidationMode="PeerOrChainTrust"  
                       revocationMode="Online"  
                       trustedStoreLocation="LocalMachine" />  
```
