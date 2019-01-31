---
title: <claimsAuthorizationManager>
ms.date: 03/30/2017
ms.assetid: 9354eee3-f692-4ad6-8427-3169686b8bcc
author: BrucePerlerMS
ms.openlocfilehash: 59d47eda97e97629408ece12a1d1dfbe804feb3e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55268092"
---
# <a name="claimsauthorizationmanager"></a><span data-ttu-id="91577-101">\<claimsAuthorizationManager></span><span class="sxs-lookup"><span data-stu-id="91577-101">\<claimsAuthorizationManager></span></span>
<span data-ttu-id="91577-102">Inscrit un gestionnaire d’autorisation des revendications pour les revendications entrantes.</span><span class="sxs-lookup"><span data-stu-id="91577-102">Registers a claims authorization manager for the incoming claims.</span></span>  
  
 <span data-ttu-id="91577-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="91577-103">\<system.identityModel></span></span>  
<span data-ttu-id="91577-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="91577-104">\<identityConfiguration></span></span>  
<span data-ttu-id="91577-105">\<claimsAuthorizationManager></span><span class="sxs-lookup"><span data-stu-id="91577-105">\<claimsAuthorizationManager></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="91577-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91577-106">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimsAuthorizationManager type = xs:string>  
      <optionalConfigurationElements />  
    </claimsAuthorizationManager>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="91577-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="91577-107">Attributes and Elements</span></span>  
 <span data-ttu-id="91577-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="91577-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="91577-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="91577-109">Attributes</span></span>  
  
|<span data-ttu-id="91577-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="91577-110">Attribute</span></span>|<span data-ttu-id="91577-111">Description</span><span class="sxs-lookup"><span data-stu-id="91577-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="91577-112">type</span><span class="sxs-lookup"><span data-stu-id="91577-112">type</span></span>|<span data-ttu-id="91577-113">Un type personnalisé qui dérive de la <xref:System.Security.Claims.ClaimsAuthorizationManager> classe.</span><span class="sxs-lookup"><span data-stu-id="91577-113">A custom type that derives from the <xref:System.Security.Claims.ClaimsAuthorizationManager> class.</span></span> <span data-ttu-id="91577-114">Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span><span class="sxs-lookup"><span data-stu-id="91577-114">For more information about how to specify the `type` attribute, see [Custom Type References](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="91577-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="91577-115">Child Elements</span></span>  
 <span data-ttu-id="91577-116">S’il existe aucune `type` attribut, ou si le `type` les références d’attribut le <xref:System.Security.Claims.ClaimsAuthenticationManager> (classe), le `<claimsAuthorizationManager>` élément ne prend pas d’éléments enfants ; Toutefois, les classes dérivées de <xref:System.Security.Claims.ClaimsAuthorizationManager> peut définir les éléments de configuration enfants.</span><span class="sxs-lookup"><span data-stu-id="91577-116">If there is no `type` attribute, or if the `type` attribute references the <xref:System.Security.Claims.ClaimsAuthenticationManager> class, the `<claimsAuthorizationManager>` element does not take child elements; however, classes derived from <xref:System.Security.Claims.ClaimsAuthorizationManager> can define child configuration elements.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="91577-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="91577-117">Parent Elements</span></span>  
  
|<span data-ttu-id="91577-118">Élément</span><span class="sxs-lookup"><span data-stu-id="91577-118">Element</span></span>|<span data-ttu-id="91577-119">Description</span><span class="sxs-lookup"><span data-stu-id="91577-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="91577-120">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="91577-120">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="91577-121">Spécifie les paramètres de l’identité de niveau de service.</span><span class="sxs-lookup"><span data-stu-id="91577-121">Specifies service-level identity settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="91577-122">Notes</span><span class="sxs-lookup"><span data-stu-id="91577-122">Remarks</span></span>  
 <span data-ttu-id="91577-123">Le comportement par défaut fourni par le biais du <xref:System.Security.Claims.ClaimsAuthorizationManager> classe autorise toujours les revendications entrantes.</span><span class="sxs-lookup"><span data-stu-id="91577-123">The default behavior provided through the <xref:System.Security.Claims.ClaimsAuthorizationManager> class always authorizes the incoming claims.</span></span> <span data-ttu-id="91577-124">Si aucun `type` attribut est spécifié ou si le `type` attribut spécifie le <xref:System.Security.Claims.ClaimsAuthorizationManager> (classe), le `<claimsAuthorizationManager>` élément ne prend pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="91577-124">If no `type` attribute is specified or if the `type` attribute specifies the <xref:System.Security.Claims.ClaimsAuthorizationManager> class, the `<claimsAuthorizationManager>` element does not take child elements.</span></span> <span data-ttu-id="91577-125">Vous pouvez spécifier le `type` attribut d’inscrire un type dérivé la <xref:System.Security.Claims.ClaimsAuthorizationManager> classe pour implémenter un comportement personnalisé.</span><span class="sxs-lookup"><span data-stu-id="91577-125">You can specify the `type` attribute to register a type derived from the <xref:System.Security.Claims.ClaimsAuthorizationManager> class to implement custom behavior.</span></span> <span data-ttu-id="91577-126">Les classes dérivées peuvent prendre en charge la configuration via les éléments enfants de la `<claimsAuthorizationManager>` élément en substituant le <xref:System.Security.Claims.ClaimsAuthorizationManager.LoadCustomConfiguration%2A> méthode pour traiter ces éléments.</span><span class="sxs-lookup"><span data-stu-id="91577-126">Derived classes can support configuration through child elements of the `<claimsAuthorizationManager>` element by overriding the <xref:System.Security.Claims.ClaimsAuthorizationManager.LoadCustomConfiguration%2A> method to handle these elements.</span></span> <span data-ttu-id="91577-127">Le schéma défini pour les éléments enfants revient le Concepteur de la classe.</span><span class="sxs-lookup"><span data-stu-id="91577-127">The schema defined for the child elements is up to the designer of the class.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="91577-128">Lorsque vous utilisez le <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> ou le <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> classe pour fournir un contrôle d’accès basé sur les revendications dans votre code, la configuration d’identité qui est référencée par le `<federationConfiguration>` élément configure le Gestionnaire d’autorisation des revendications et la stratégie qui est utilisée pour rendre décisions d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="91577-128">When using the <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> or the <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> class to provide claims-based access control in your code, the identity configuration that is referenced by the `<federationConfiguration>` element configures the claims authorization manager and policy that is used to make authorization decisions.</span></span> <span data-ttu-id="91577-129">Cela est vrai, même dans les scénarios qui ne sont pas les scénarios Web passifs, par exemple les applications Windows Communication Foundation (WCF) ou une application qui n’est pas basée sur le Web.</span><span class="sxs-lookup"><span data-stu-id="91577-129">This is true, even in scenarios that are not passive Web scenarios, for example Windows Communication Foundation (WCF) applications or an application that is not Web-based.</span></span> <span data-ttu-id="91577-130">Si l’application n’est pas une application Web passive, le `<claimsAuthorizationManager>` élément (et ses éléments de la stratégie enfant, le cas échéant) de la configuration de l’identité référencée sont les seuls paramètres appliqués.</span><span class="sxs-lookup"><span data-stu-id="91577-130">If the application is not a passive Web application, the `<claimsAuthorizationManager>` element (and its child policy elements, if present) of the referenced identity configuration are the only settings applied.</span></span> <span data-ttu-id="91577-131">Tous les autres paramètres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="91577-131">All other settings are ignored.</span></span> <span data-ttu-id="91577-132">Pour plus d’informations, consultez le [ \<federationConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md) élément.</span><span class="sxs-lookup"><span data-stu-id="91577-132">For more information, see the [\<federationConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md) element.</span></span>  
  
 <span data-ttu-id="91577-133">Cet élément définit les <xref:System.IdentityModel.Configuration.IdentityConfiguration.ClaimsAuthorizationManager%2A?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="91577-133">This element sets the <xref:System.IdentityModel.Configuration.IdentityConfiguration.ClaimsAuthorizationManager%2A?displayProperty=nameWithType> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="91577-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="91577-134">Example</span></span>  
 <span data-ttu-id="91577-135">Le code XML suivant illustre la configuration d’une autorisation de revendications gestionnaire qui implémente la stratégie composée de paires de ressource-action qui spécifient chacune des combinaisons booléennes des revendications comportant un demandeur doit effectuer l’action sur la ressource.</span><span class="sxs-lookup"><span data-stu-id="91577-135">The following XML shows the configuration for a claims authorization manager that implements policy composed of resource-action pairs each of which specifies boolean combinations of the claims that a requestor must possess to perform the action on the resource.</span></span> <span data-ttu-id="91577-136">Vous trouverez le code qui implémente le Gestionnaire d’autorisation des revendications capable d’utiliser cette stratégie dans le `ClaimsBasedAuthorization` exemple.</span><span class="sxs-lookup"><span data-stu-id="91577-136">The code that implements the claims authorization manager capable of using this policy can be found in the `ClaimsBasedAuthorization` sample.</span></span>  
  
```xml  
<system.identityModel>  
    <identityConfiguration>  
      <claimsAuthorizationManager type="ClaimsAuthorizationLibrary.MyClaimsAuthorizationManager, ClaimsAuthorizationLibrary">  
        <policy resource="http://localhost:28491/Developers.aspx" action="GET">  
          <or>  
            <claim claimType="http://schemas.microsoft.com/ws/2008/06/identity/claims/role" claimValue="developer" />  
            <claim claimType="http://schemas.xmlsoap.org/claims/Group" claimValue="Administrator" />  
          </or>  
        </policy>  
        <policy resource="http://localhost:28491/Administrators.aspx" action="GET">  
          <and>  
            <claim claimType="http://schemas.xmlsoap.org/claims/Group" claimValue="Administrator" />  
            <claim claimType="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/country" claimValue="USA" />  
          </and>  
        </policy>  
        <policy resource="http://localhost:28491/Default.aspx" action="GET">  
        </policy>  
        <policy resource="http://localhost:28491/" action="GET">  
        </policy>  
        <policy resource="http://localhost:28491/Claims.aspx" action="GET">  
        </policy>  
      </claimsAuthorizationManager>  
    <identityConfiguration>  
<system.identityModel>  
```
