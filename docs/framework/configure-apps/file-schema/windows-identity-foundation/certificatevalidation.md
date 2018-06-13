---
title: '&lt;certificateValidation&gt;'
ms.date: 03/30/2017
ms.assetid: 6c54c704-b55e-4631-88ff-4d4a5621554c
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: af4dc459da49b46d70276d3f4bcd5f94d2a91ffe
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32756057"
---
# <a name="ltcertificatevalidationgt"></a><span data-ttu-id="3704e-102">&lt;certificateValidation&gt;</span><span class="sxs-lookup"><span data-stu-id="3704e-102">&lt;certificateValidation&gt;</span></span>
<span data-ttu-id="3704e-103">Contrôle les paramètres qui utilisent des gestionnaires de jetons pour valider les certificats.</span><span class="sxs-lookup"><span data-stu-id="3704e-103">Controls the settings that token handlers use to validate certificates.</span></span> <span data-ttu-id="3704e-104">Ces paramètres sont remplacés si un gestionnaire spécifique est configuré avec son propre validateur.</span><span class="sxs-lookup"><span data-stu-id="3704e-104">These settings are overridden if a specific handler is configured with its own validator.</span></span>  
  
 <span data-ttu-id="3704e-105">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="3704e-105">\<system.identityModel></span></span>  
<span data-ttu-id="3704e-106">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="3704e-106">\<identityConfiguration></span></span>  
<span data-ttu-id="3704e-107">\<certificateValidation ></span><span class="sxs-lookup"><span data-stu-id="3704e-107">\<certificateValidation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3704e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3704e-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3704e-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3704e-109">Attributes and Elements</span></span>  
 <span data-ttu-id="3704e-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3704e-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3704e-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="3704e-111">Attributes</span></span>  
  
|<span data-ttu-id="3704e-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="3704e-112">Attribute</span></span>|<span data-ttu-id="3704e-113">Description</span><span class="sxs-lookup"><span data-stu-id="3704e-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3704e-114">certificateValidationMode</span><span class="sxs-lookup"><span data-stu-id="3704e-114">certificateValidationMode</span></span>|<span data-ttu-id="3704e-115">Un <xref:System.ServiceModel.Security.X509CertificateValidationMode> valeur qui spécifie le mode de validation à utiliser pour le certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="3704e-115">An <xref:System.ServiceModel.Security.X509CertificateValidationMode> value that specifies the validation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="3704e-116">La valeur par défaut est « PeerOrChainTrust ».</span><span class="sxs-lookup"><span data-stu-id="3704e-116">The default value is "PeerOrChainTrust".</span></span> <span data-ttu-id="3704e-117">Pour spécifier un validateur personnalisé, définissez cet attribut à « Custom » et le programme de validation à l’aide de la [ \<certificateValidator >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md) élément.</span><span class="sxs-lookup"><span data-stu-id="3704e-117">To specify a custom validator, set this attribute to "Custom" and specify the validator using the [\<certificateValidator>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md) element.</span></span> <span data-ttu-id="3704e-118">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="3704e-118">Optional.</span></span>|  
|<span data-ttu-id="3704e-119">revocationMode</span><span class="sxs-lookup"><span data-stu-id="3704e-119">revocationMode</span></span>|<span data-ttu-id="3704e-120">Un <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> valeur qui spécifie le mode de révocation à utiliser pour le certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="3704e-120">An <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> value that specifies the revocation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="3704e-121">La valeur par défaut est « Online ».</span><span class="sxs-lookup"><span data-stu-id="3704e-121">The default value is "Online".</span></span> <span data-ttu-id="3704e-122">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="3704e-122">Optional.</span></span>|  
|<span data-ttu-id="3704e-123">trustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="3704e-123">trustedStoreLocation</span></span>|<span data-ttu-id="3704e-124">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> valeur qui spécifie le magasin de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="3704e-124">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the X.509 certificate store.</span></span> <span data-ttu-id="3704e-125">La valeur par défaut est « Ordinateur_local ».</span><span class="sxs-lookup"><span data-stu-id="3704e-125">The default value is "LocalMachine".</span></span> <span data-ttu-id="3704e-126">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="3704e-126">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3704e-127">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3704e-127">Child Elements</span></span>  
  
|<span data-ttu-id="3704e-128">Élément</span><span class="sxs-lookup"><span data-stu-id="3704e-128">Element</span></span>|<span data-ttu-id="3704e-129">Description</span><span class="sxs-lookup"><span data-stu-id="3704e-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3704e-130">\<certificateValidator ></span><span class="sxs-lookup"><span data-stu-id="3704e-130">\<certificateValidator></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md)|<span data-ttu-id="3704e-131">Spécifie un type personnalisé pour la validation de certificat.</span><span class="sxs-lookup"><span data-stu-id="3704e-131">Specifies a custom type for certificate validation.</span></span> <span data-ttu-id="3704e-132">Ce type est utilisé uniquement si la `certificateValidationMode` attribut de la [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) a la valeur « Custom ».</span><span class="sxs-lookup"><span data-stu-id="3704e-132">This type is used only if the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element is set to "Custom".</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="3704e-133">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3704e-133">Parent Elements</span></span>  
  
|<span data-ttu-id="3704e-134">Élément</span><span class="sxs-lookup"><span data-stu-id="3704e-134">Element</span></span>|<span data-ttu-id="3704e-135">Description</span><span class="sxs-lookup"><span data-stu-id="3704e-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3704e-136">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="3704e-136">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="3704e-137">Spécifie les paramètres d’identité au niveau du service.</span><span class="sxs-lookup"><span data-stu-id="3704e-137">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="3704e-138">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="3704e-138">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="3704e-139">Fournit des gestionnaires de jetons de configuration pour une collection de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3704e-139">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3704e-140">Notes</span><span class="sxs-lookup"><span data-stu-id="3704e-140">Remarks</span></span>  
 <span data-ttu-id="3704e-141">A `<certificateValidation>` élément peut être spécifié au niveau du service sous le `<identityConfiguration>` élément ou sur le niveau de regroupement de gestionnaire de jetons de sécurité sous le `<securityTokenHandlerConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="3704e-141">A `<certificateValidation>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="3704e-142">Paramètres sur une collection de gestionnaire de jetons remplacent celles spécifiées sur le service.</span><span class="sxs-lookup"><span data-stu-id="3704e-142">Settings on a token handler collection override those specified on the service.</span></span> <span data-ttu-id="3704e-143">Certains gestionnaires de jetons permettent de spécifier les paramètres de validation de certificat dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="3704e-143">Some token handlers allow you to specify certificate validation settings in configuration.</span></span> <span data-ttu-id="3704e-144">Paramètres sur les gestionnaires de jetons individuels remplacent celles spécifiées à la fois au niveau du service et sur la collection de gestionnaire de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3704e-144">Settings on individual token handlers override those specified both at the service level and on the security token handler collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3704e-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="3704e-145">Example</span></span>  
  
```xml  
<certificateValidation certificateValidationMode="PeerOrChainTrust"  
                       revocationMode="Online"  
                       trustedStoreLocation="LocalMachine" />  
```
