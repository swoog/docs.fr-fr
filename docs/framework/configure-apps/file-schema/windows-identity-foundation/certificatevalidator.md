---
title: '&lt;certificateValidator&gt;'
ms.date: 03/30/2017
ms.assetid: 86161897-c20f-4ad8-9d7f-050c247251bf
author: BrucePerlerMS
ms.openlocfilehash: 65b8aa6fa4422579ce0d1c5e33d3418ea051612a
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47077653"
---
# <a name="ltcertificatevalidatorgt"></a><span data-ttu-id="4f826-102">&lt;certificateValidator&gt;</span><span class="sxs-lookup"><span data-stu-id="4f826-102">&lt;certificateValidator&gt;</span></span>
<span data-ttu-id="4f826-103">Spécifie un type personnalisé pour la validation de certificat.</span><span class="sxs-lookup"><span data-stu-id="4f826-103">Specifies a custom type for certificate validation.</span></span> <span data-ttu-id="4f826-104">Ce type est utilisé uniquement si le `certificateValidationMode` attribut de la [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) élément est défini sur « Custom ».</span><span class="sxs-lookup"><span data-stu-id="4f826-104">This type is used only if the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element is set to "Custom".</span></span>  
  
 <span data-ttu-id="4f826-105">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="4f826-105">\<system.identityModel></span></span>  
<span data-ttu-id="4f826-106">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="4f826-106">\<identityConfiguration></span></span>  
<span data-ttu-id="4f826-107">\<certificateValidation ></span><span class="sxs-lookup"><span data-stu-id="4f826-107">\<certificateValidation></span></span>  
<span data-ttu-id="4f826-108">\<certificateValidator ></span><span class="sxs-lookup"><span data-stu-id="4f826-108">\<certificateValidator></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f826-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f826-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <certificateValidation>  
      <certificateValidator type=xs:string>  
      </certificateValidator>  
    </certificateValidation>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4f826-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4f826-110">Attributes and Elements</span></span>  
 <span data-ttu-id="4f826-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4f826-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4f826-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="4f826-112">Attributes</span></span>  
  
|<span data-ttu-id="4f826-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="4f826-113">Attribute</span></span>|<span data-ttu-id="4f826-114">Description</span><span class="sxs-lookup"><span data-stu-id="4f826-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4f826-115">type</span><span class="sxs-lookup"><span data-stu-id="4f826-115">type</span></span>|<span data-ttu-id="4f826-116">Spécifie un type personnalisé qui dérive de la <xref:System.IdentityModel.Selectors.X509CertificateValidator> classe.</span><span class="sxs-lookup"><span data-stu-id="4f826-116">Specifies a custom type that derives from the <xref:System.IdentityModel.Selectors.X509CertificateValidator> class.</span></span> <span data-ttu-id="4f826-117">Définir le `certificateValidationMode` attribut de la [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) élément « Personnalisé » pour utiliser ce type.</span><span class="sxs-lookup"><span data-stu-id="4f826-117">Set the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element to "Custom" to use this type.</span></span> <span data-ttu-id="4f826-118">Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span><span class="sxs-lookup"><span data-stu-id="4f826-118">For more information about how to specify the `type` attribute, see [Custom Type References](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span> <span data-ttu-id="4f826-119">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="4f826-119">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4f826-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4f826-120">Child Elements</span></span>  
 <span data-ttu-id="4f826-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4f826-121">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4f826-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4f826-122">Parent Elements</span></span>  
  
|<span data-ttu-id="4f826-123">Élément</span><span class="sxs-lookup"><span data-stu-id="4f826-123">Element</span></span>|<span data-ttu-id="4f826-124">Description</span><span class="sxs-lookup"><span data-stu-id="4f826-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4f826-125">\<certificateValidation ></span><span class="sxs-lookup"><span data-stu-id="4f826-125">\<certificateValidation></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md)|<span data-ttu-id="4f826-126">Contrôle les paramètres qui utilisent des gestionnaires de jetons pour valider les certificats.</span><span class="sxs-lookup"><span data-stu-id="4f826-126">Controls the settings that token handlers use to validate certificates.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="4f826-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="4f826-127">Example</span></span>  
  
```xml  
<certificateValidation certificateValidationMode="Custom"  
                       revocationMode="Online"  
                       trustedStoreLocation="LocalMachine">  
    <certificateValidator type="MyNamespace.CustomValidator, MyAssembly" />    
</certificateValidation>        
```
