---
title: <certificateValidator>
ms.date: 03/30/2017
ms.assetid: 86161897-c20f-4ad8-9d7f-050c247251bf
author: BrucePerlerMS
ms.openlocfilehash: df52212305e0865b8c03fdd49068cb7c7da4fa38
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61667364"
---
# <a name="certificatevalidator"></a><span data-ttu-id="0ddff-101">\<certificateValidator></span><span class="sxs-lookup"><span data-stu-id="0ddff-101">\<certificateValidator></span></span>
<span data-ttu-id="0ddff-102">Spécifie un type personnalisé pour la validation de certificat.</span><span class="sxs-lookup"><span data-stu-id="0ddff-102">Specifies a custom type for certificate validation.</span></span> <span data-ttu-id="0ddff-103">Ce type est utilisé uniquement si le `certificateValidationMode` attribut de la [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) élément est défini sur « Custom ».</span><span class="sxs-lookup"><span data-stu-id="0ddff-103">This type is used only if the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element is set to "Custom".</span></span>  
  
 <span data-ttu-id="0ddff-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="0ddff-104">\<system.identityModel></span></span>  
<span data-ttu-id="0ddff-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="0ddff-105">\<identityConfiguration></span></span>  
<span data-ttu-id="0ddff-106">\<certificateValidation></span><span class="sxs-lookup"><span data-stu-id="0ddff-106">\<certificateValidation></span></span>  
<span data-ttu-id="0ddff-107">\<certificateValidator></span><span class="sxs-lookup"><span data-stu-id="0ddff-107">\<certificateValidator></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ddff-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ddff-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0ddff-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0ddff-109">Attributes and Elements</span></span>  
 <span data-ttu-id="0ddff-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0ddff-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0ddff-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="0ddff-111">Attributes</span></span>  
  
|<span data-ttu-id="0ddff-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="0ddff-112">Attribute</span></span>|<span data-ttu-id="0ddff-113">Description</span><span class="sxs-lookup"><span data-stu-id="0ddff-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0ddff-114">type</span><span class="sxs-lookup"><span data-stu-id="0ddff-114">type</span></span>|<span data-ttu-id="0ddff-115">Spécifie un type personnalisé qui dérive de la <xref:System.IdentityModel.Selectors.X509CertificateValidator> classe.</span><span class="sxs-lookup"><span data-stu-id="0ddff-115">Specifies a custom type that derives from the <xref:System.IdentityModel.Selectors.X509CertificateValidator> class.</span></span> <span data-ttu-id="0ddff-116">Définir le `certificateValidationMode` attribut de la [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) élément « Personnalisé » pour utiliser ce type.</span><span class="sxs-lookup"><span data-stu-id="0ddff-116">Set the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element to "Custom" to use this type.</span></span> <span data-ttu-id="0ddff-117">Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span><span class="sxs-lookup"><span data-stu-id="0ddff-117">For more information about how to specify the `type` attribute, see [Custom Type References](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span> <span data-ttu-id="0ddff-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0ddff-118">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0ddff-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0ddff-119">Child Elements</span></span>  
 <span data-ttu-id="0ddff-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0ddff-120">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0ddff-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0ddff-121">Parent Elements</span></span>  
  
|<span data-ttu-id="0ddff-122">Élément</span><span class="sxs-lookup"><span data-stu-id="0ddff-122">Element</span></span>|<span data-ttu-id="0ddff-123">Description</span><span class="sxs-lookup"><span data-stu-id="0ddff-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0ddff-124">\<certificateValidation></span><span class="sxs-lookup"><span data-stu-id="0ddff-124">\<certificateValidation></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md)|<span data-ttu-id="0ddff-125">Contrôle les paramètres qui utilisent des gestionnaires de jetons pour valider les certificats.</span><span class="sxs-lookup"><span data-stu-id="0ddff-125">Controls the settings that token handlers use to validate certificates.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="0ddff-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="0ddff-126">Example</span></span>  
  
```xml  
<certificateValidation certificateValidationMode="Custom"  
                       revocationMode="Online"  
                       trustedStoreLocation="LocalMachine">  
    <certificateValidator type="MyNamespace.CustomValidator, MyAssembly" />    
</certificateValidation>        
```
