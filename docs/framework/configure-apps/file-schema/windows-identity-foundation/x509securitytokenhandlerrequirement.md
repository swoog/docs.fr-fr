---
title: <x509SecurityTokenHandlerRequirement>
ms.date: 03/30/2017
ms.assetid: aca22c2c-5ae7-42af-9bbd-15c2524692ce
author: BrucePerlerMS
ms.openlocfilehash: 6e8267f170dbb26381564be7b66df5f617156885
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790440"
---
# <a name="x509securitytokenhandlerrequirement"></a><span data-ttu-id="089c5-101">\<x509SecurityTokenHandlerRequirement></span><span class="sxs-lookup"><span data-stu-id="089c5-101">\<x509SecurityTokenHandlerRequirement></span></span>
<span data-ttu-id="089c5-102">Fournit une configuration facultative pour le <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler> classe ou les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="089c5-102">Provides optional configuration for the <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="089c5-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="089c5-103">\<system.identityModel></span></span>  
<span data-ttu-id="089c5-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="089c5-104">\<identityConfiguration></span></span>  
<span data-ttu-id="089c5-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="089c5-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="089c5-106">\<add></span><span class="sxs-lookup"><span data-stu-id="089c5-106">\<add></span></span>  
<span data-ttu-id="089c5-107">\<x509SecurityTokenHandlerRequirement></span><span class="sxs-lookup"><span data-stu-id="089c5-107">\<x509SecurityTokenHandlerRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="089c5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="089c5-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type="System.IdentityModel.Tokens.X509SecurityTokenHandler, System.IdentityModel">  
        <x509SecurityTokenHandlerRequirement>  
          mapToWindows=xs:boolean  
          certificateValidationMode="None||ChainTrust||PeerTrust||PeerOrChainTrust||Custom"  
          certificateValidator="Namespace.Class, Assembly"  
          revocationMode="NoCheck||Offline||Online"  
          trustedStoreLocation="CurrentUser||LocalMachine"  
        </x509SecurityTokenHandlerRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="089c5-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="089c5-109">Attributes and Elements</span></span>  
 <span data-ttu-id="089c5-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="089c5-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="089c5-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="089c5-111">Attributes</span></span>  
  
|<span data-ttu-id="089c5-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="089c5-112">Attribute</span></span>|<span data-ttu-id="089c5-113">Description</span><span class="sxs-lookup"><span data-stu-id="089c5-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="089c5-114">certificateValidationMode</span><span class="sxs-lookup"><span data-stu-id="089c5-114">certificateValidationMode</span></span>|<span data-ttu-id="089c5-115">Un <xref:System.ServiceModel.Security.X509CertificateValidationMode> valeur qui spécifie le mode de validation à utiliser pour le certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="089c5-115">An <xref:System.ServiceModel.Security.X509CertificateValidationMode> value that specifies the validation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="089c5-116">La valeur par défaut est « PeerOrChainTrust ».</span><span class="sxs-lookup"><span data-stu-id="089c5-116">The default value is "PeerOrChainTrust".</span></span>|  
|<span data-ttu-id="089c5-117">mapToWindows</span><span class="sxs-lookup"><span data-stu-id="089c5-117">mapToWindows</span></span>|<span data-ttu-id="089c5-118">Spécifie si le Gestionnaire de jetons doit mapper le jeton de validation à un compte Windows à l’aide de la revendication UPN entrante.</span><span class="sxs-lookup"><span data-stu-id="089c5-118">Specifies whether the token handler should map the validating token to a Windows account by using the incoming UPN claim.</span></span> <span data-ttu-id="089c5-119">La valeur par défaut est « false ».</span><span class="sxs-lookup"><span data-stu-id="089c5-119">The default is "false".</span></span>|  
|<span data-ttu-id="089c5-120">revocationMode</span><span class="sxs-lookup"><span data-stu-id="089c5-120">revocationMode</span></span>|<span data-ttu-id="089c5-121">Un <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> valeur qui spécifie le mode de révocation à utiliser pour le certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="089c5-121">An <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> value that specifies the revocation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="089c5-122">La valeur par défaut est « En ligne ».</span><span class="sxs-lookup"><span data-stu-id="089c5-122">The default value is "Online".</span></span>|  
|<span data-ttu-id="089c5-123">trustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="089c5-123">trustedStoreLocation</span></span>|<span data-ttu-id="089c5-124">Un <xref:System.Security.Cryptography.X509Certificates.StoreLocation> valeur qui spécifie le magasin de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="089c5-124">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the X.509 certificate store.</span></span> <span data-ttu-id="089c5-125">La valeur par défaut est « LocalMachine ».</span><span class="sxs-lookup"><span data-stu-id="089c5-125">The default value is "LocalMachine".</span></span>|  
|<span data-ttu-id="089c5-126">certificateValidator</span><span class="sxs-lookup"><span data-stu-id="089c5-126">certificateValidator</span></span>|<span data-ttu-id="089c5-127">Un type personnalisé qui dérive de <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span><span class="sxs-lookup"><span data-stu-id="089c5-127">A custom type that derives from <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span></span> <span data-ttu-id="089c5-128">Si le `certificateValidationMode` attribut est « Custom », une instance de ce type est utilisée pour valider le certificat émetteur.</span><span class="sxs-lookup"><span data-stu-id="089c5-128">If the `certificateValidationMode` attribute is "Custom", an instance of this type is used for issuer certificate validation.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="089c5-129">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="089c5-129">Child Elements</span></span>  
 <span data-ttu-id="089c5-130">Aucun.</span><span class="sxs-lookup"><span data-stu-id="089c5-130">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="089c5-131">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="089c5-131">Parent Elements</span></span>  
  
|<span data-ttu-id="089c5-132">Élément</span><span class="sxs-lookup"><span data-stu-id="089c5-132">Element</span></span>|<span data-ttu-id="089c5-133">Description</span><span class="sxs-lookup"><span data-stu-id="089c5-133">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="089c5-134">\<add></span><span class="sxs-lookup"><span data-stu-id="089c5-134">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="089c5-135">Ajoute le Gestionnaire de jetons de sécurité spécifié à la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="089c5-135">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="089c5-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="089c5-136">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.X509SecurityTokenHandler, System.IdentityModel">  
    <x509SecurityTokenHandlerRequirement mapToWindows="true"   
                                         certificateValidationMode="PeerOrChainTrust"   
                                         revocationMode="Online"   
                                         trustedStoreLocation="LocalMachine" />  
</add>  
```
