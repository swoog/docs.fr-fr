---
title: <certificateValidator>
ms.date: 03/30/2017
ms.assetid: 86161897-c20f-4ad8-9d7f-050c247251bf
author: BrucePerlerMS
ms.openlocfilehash: df52212305e0865b8c03fdd49068cb7c7da4fa38
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55277448"
---
# <a name="certificatevalidator"></a><span data-ttu-id="674a2-101">\<certificateValidator></span><span class="sxs-lookup"><span data-stu-id="674a2-101">\<certificateValidator></span></span>
<span data-ttu-id="674a2-102">Spécifie un type personnalisé pour la validation de certificat.</span><span class="sxs-lookup"><span data-stu-id="674a2-102">Specifies a custom type for certificate validation.</span></span> <span data-ttu-id="674a2-103">Ce type est utilisé uniquement si le `certificateValidationMode` attribut de la [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) élément est défini sur « Custom ».</span><span class="sxs-lookup"><span data-stu-id="674a2-103">This type is used only if the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element is set to "Custom".</span></span>  
  
 <span data-ttu-id="674a2-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="674a2-104">\<system.identityModel></span></span>  
<span data-ttu-id="674a2-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="674a2-105">\<identityConfiguration></span></span>  
<span data-ttu-id="674a2-106">\<certificateValidation></span><span class="sxs-lookup"><span data-stu-id="674a2-106">\<certificateValidation></span></span>  
<span data-ttu-id="674a2-107">\<certificateValidator></span><span class="sxs-lookup"><span data-stu-id="674a2-107">\<certificateValidator></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="674a2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="674a2-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="674a2-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="674a2-109">Attributes and Elements</span></span>  
 <span data-ttu-id="674a2-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="674a2-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="674a2-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="674a2-111">Attributes</span></span>  
  
|<span data-ttu-id="674a2-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="674a2-112">Attribute</span></span>|<span data-ttu-id="674a2-113">Description</span><span class="sxs-lookup"><span data-stu-id="674a2-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="674a2-114">type</span><span class="sxs-lookup"><span data-stu-id="674a2-114">type</span></span>|<span data-ttu-id="674a2-115">Spécifie un type personnalisé qui dérive de la <xref:System.IdentityModel.Selectors.X509CertificateValidator> classe.</span><span class="sxs-lookup"><span data-stu-id="674a2-115">Specifies a custom type that derives from the <xref:System.IdentityModel.Selectors.X509CertificateValidator> class.</span></span> <span data-ttu-id="674a2-116">Définir le `certificateValidationMode` attribut de la [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) élément « Personnalisé » pour utiliser ce type.</span><span class="sxs-lookup"><span data-stu-id="674a2-116">Set the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element to "Custom" to use this type.</span></span> <span data-ttu-id="674a2-117">Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span><span class="sxs-lookup"><span data-stu-id="674a2-117">For more information about how to specify the `type` attribute, see [Custom Type References](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span> <span data-ttu-id="674a2-118">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="674a2-118">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="674a2-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="674a2-119">Child Elements</span></span>  
 <span data-ttu-id="674a2-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="674a2-120">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="674a2-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="674a2-121">Parent Elements</span></span>  
  
|<span data-ttu-id="674a2-122">Élément</span><span class="sxs-lookup"><span data-stu-id="674a2-122">Element</span></span>|<span data-ttu-id="674a2-123">Description</span><span class="sxs-lookup"><span data-stu-id="674a2-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="674a2-124">\<certificateValidation></span><span class="sxs-lookup"><span data-stu-id="674a2-124">\<certificateValidation></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md)|<span data-ttu-id="674a2-125">Contrôle les paramètres qui utilisent des gestionnaires de jetons pour valider les certificats.</span><span class="sxs-lookup"><span data-stu-id="674a2-125">Controls the settings that token handlers use to validate certificates.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="674a2-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="674a2-126">Example</span></span>  
  
```xml  
<certificateValidation certificateValidationMode="Custom"  
                       revocationMode="Online"  
                       trustedStoreLocation="LocalMachine">  
    <certificateValidator type="MyNamespace.CustomValidator, MyAssembly" />    
</certificateValidation>        
```
