---
title: '&lt;claimsAuthenticationManager&gt;'
ms.date: 03/30/2017
ms.assetid: 6d30a450-6d13-4671-81a8-77e0204500c5
author: BrucePerlerMS
ms.openlocfilehash: 0ec7e44363f87e54eae97b70352f520fe87540be
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48581823"
---
# <a name="ltclaimsauthenticationmanagergt"></a><span data-ttu-id="7837e-102">&lt;claimsAuthenticationManager&gt;</span><span class="sxs-lookup"><span data-stu-id="7837e-102">&lt;claimsAuthenticationManager&gt;</span></span>
<span data-ttu-id="7837e-103">Inscrit un gestionnaire d’authentification des revendications pour les revendications entrantes.</span><span class="sxs-lookup"><span data-stu-id="7837e-103">Registers a claims authentication manager for the incoming claims.</span></span>  
  
 <span data-ttu-id="7837e-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="7837e-104">\<system.identityModel></span></span>  
<span data-ttu-id="7837e-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="7837e-105">\<identityConfiguration></span></span>  
<span data-ttu-id="7837e-106">\<claimsAuthenticationManager ></span><span class="sxs-lookup"><span data-stu-id="7837e-106">\<claimsAuthenticationManager></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7837e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7837e-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimsAuthenticationManager type=xs:string>  
      <optionalConfigurationElements />  
    </claimsAuthenticationManager>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7837e-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7837e-108">Attributes and Elements</span></span>  
 <span data-ttu-id="7837e-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7837e-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7837e-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="7837e-110">Attributes</span></span>  
  
|<span data-ttu-id="7837e-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="7837e-111">Attribute</span></span>|<span data-ttu-id="7837e-112">Description</span><span class="sxs-lookup"><span data-stu-id="7837e-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7837e-113">type</span><span class="sxs-lookup"><span data-stu-id="7837e-113">type</span></span>|<span data-ttu-id="7837e-114">Spécifie un type personnalisé qui dérive de la <xref:System.Security.Claims.ClaimsAuthenticationManager> classe.</span><span class="sxs-lookup"><span data-stu-id="7837e-114">Specifies a custom type that derives from the <xref:System.Security.Claims.ClaimsAuthenticationManager> class.</span></span> <span data-ttu-id="7837e-115">Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé].</span><span class="sxs-lookup"><span data-stu-id="7837e-115">For more information about how to specify the `type` attribute, see [Custom Type References].</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7837e-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7837e-116">Child Elements</span></span>  
 <span data-ttu-id="7837e-117">S’il existe aucune `type` attribut, ou si le `type` les références d’attribut le <xref:System.Security.Claims.ClaimsAuthenticationManager> (classe), le `<claimsAuthenticationManager>` élément ne prend pas d’éléments enfants ; Toutefois, les classes dérivées de <xref:System.Security.Claims.ClaimsAuthenticationManager> peut définir les éléments de configuration enfants.</span><span class="sxs-lookup"><span data-stu-id="7837e-117">If there is no `type` attribute, or if the `type` attribute references the <xref:System.Security.Claims.ClaimsAuthenticationManager> class, the `<claimsAuthenticationManager>` element does not take child elements; however, classes derived from <xref:System.Security.Claims.ClaimsAuthenticationManager> can define child configuration elements.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7837e-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7837e-118">Parent Elements</span></span>  
  
|<span data-ttu-id="7837e-119">Élément</span><span class="sxs-lookup"><span data-stu-id="7837e-119">Element</span></span>|<span data-ttu-id="7837e-120">Description</span><span class="sxs-lookup"><span data-stu-id="7837e-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7837e-121">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="7837e-121">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="7837e-122">Spécifie les paramètres de l’identité de niveau de service.</span><span class="sxs-lookup"><span data-stu-id="7837e-122">Specifies service-level identity settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7837e-123">Notes</span><span class="sxs-lookup"><span data-stu-id="7837e-123">Remarks</span></span>  
 <span data-ttu-id="7837e-124">Le comportement par défaut fourni par le biais du <xref:System.Security.Claims.ClaimsAuthenticationManager> classe renvoie les revendications entrantes.</span><span class="sxs-lookup"><span data-stu-id="7837e-124">The default behavior provided through the <xref:System.Security.Claims.ClaimsAuthenticationManager> class echoes the incoming claims.</span></span> <span data-ttu-id="7837e-125">Si aucun `type` attribut est spécifié ou si le `type` attribut spécifie le <xref:System.Security.Claims.ClaimsAuthenticationManager> (classe), le `<claimsAuthenticationManager>` élément ne prend pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="7837e-125">If no `type` attribute is specified or if the `type` attribute specifies the <xref:System.Security.Claims.ClaimsAuthenticationManager> class, the `<claimsAuthenticationManager>` element does not take child elements.</span></span> <span data-ttu-id="7837e-126">Vous pouvez spécifier le `type` attribut d’inscrire un type dérivé la <xref:System.Security.Claims.ClaimsAuthenticationManager> classe pour implémenter un comportement personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7837e-126">You can specify the `type` attribute to register a type derived from the <xref:System.Security.Claims.ClaimsAuthenticationManager> class to implement custom behavior.</span></span> <span data-ttu-id="7837e-127">Les classes dérivées peuvent prendre en charge la configuration via les éléments enfants de la `<claimsAuthenticationManager>` élément en substituant le <xref:System.Security.Claims.ClaimsAuthenticationManager.LoadCustomConfiguration%2A> méthode pour traiter ces éléments.</span><span class="sxs-lookup"><span data-stu-id="7837e-127">Derived classes can support configuration through child elements of the `<claimsAuthenticationManager>` element by overriding the <xref:System.Security.Claims.ClaimsAuthenticationManager.LoadCustomConfiguration%2A> method to handle these elements.</span></span> <span data-ttu-id="7837e-128">Le schéma défini pour les éléments enfants revient le Concepteur de la classe.</span><span class="sxs-lookup"><span data-stu-id="7837e-128">The schema defined for the child elements is up to the designer of the class.</span></span>  
  
 <span data-ttu-id="7837e-129">Le `<claimsAuthenticationManager>` élément définit les <xref:System.IdentityModel.Configuration.IdentityConfiguration.ClaimsAuthenticationManager%2A?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="7837e-129">The `<claimsAuthenticationManager>` element sets the <xref:System.IdentityModel.Configuration.IdentityConfiguration.ClaimsAuthenticationManager%2A?displayProperty=nameWithType> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7837e-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="7837e-130">Example</span></span>  
  
```xml  
<system.identityModel>  
    <identityConfiguration name="MyIdentity">  
      <claimsAuthenticationManager type="MyNamespace.CustomClaimsAuthenticationManager, MyAssembly"/>          
    </identityConfiguration>  
</microsoft.identityModel>  
```
