---
title: <roleClaimType>
ms.date: 03/30/2017
ms.assetid: 69a49deb-6369-41ba-806b-ae8d21fac64b
author: BrucePerlerMS
ms.openlocfilehash: 8c7b7c9b42ac72b878aed4e12298dc3655f1e707
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793872"
---
# <a name="roleclaimtype"></a><span data-ttu-id="8e415-101">\<roleClaimType></span><span class="sxs-lookup"><span data-stu-id="8e415-101">\<roleClaimType></span></span>
<span data-ttu-id="8e415-102">Spécifie le type de revendication qui définit les revendications de type de rôle dans la collection de <xref:System.Security.Claims.ClaimsIdentity> objets retournés par la <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> méthode de gestionnaire de jetons.</span><span class="sxs-lookup"><span data-stu-id="8e415-102">Specifies the claim type that defines the role type claims in the collection of <xref:System.Security.Claims.ClaimsIdentity> objects returned by the <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> method of the token handler.</span></span>  
  
 <span data-ttu-id="8e415-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="8e415-103">\<system.identityModel></span></span>  
<span data-ttu-id="8e415-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="8e415-104">\<identityConfiguration></span></span>  
<span data-ttu-id="8e415-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="8e415-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="8e415-106">\<add></span><span class="sxs-lookup"><span data-stu-id="8e415-106">\<add></span></span>  
<span data-ttu-id="8e415-107">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="8e415-107">\<samlSecurityTokenRequirement></span></span>  
<span data-ttu-id="8e415-108">\<roleClaimType></span><span class="sxs-lookup"><span data-stu-id="8e415-108">\<roleClaimType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8e415-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e415-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add>  
        <samlSecurityTokenRequirement>  
          <roleClaimType value=xs:string>  
          </roleClaimType>  
        </samlSecurityTokenRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8e415-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="8e415-110">Attributes and Elements</span></span>  
 <span data-ttu-id="8e415-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="8e415-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8e415-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="8e415-112">Attributes</span></span>  
  
|<span data-ttu-id="8e415-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="8e415-113">Attribute</span></span>|<span data-ttu-id="8e415-114">Description</span><span class="sxs-lookup"><span data-stu-id="8e415-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="8e415-115">par défaut</span><span class="sxs-lookup"><span data-stu-id="8e415-115">value</span></span>|<span data-ttu-id="8e415-116">Chaîne qui spécifie l’URI qui représente le type de revendication de la revendication à utiliser pour le type de revendication de rôle.</span><span class="sxs-lookup"><span data-stu-id="8e415-116">A string that specifies the URI that represents the claim type of the claim to use for the role claim type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8e415-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8e415-117">Child Elements</span></span>  
 <span data-ttu-id="8e415-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8e415-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8e415-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8e415-119">Parent Elements</span></span>  
  
|<span data-ttu-id="8e415-120">Élément</span><span class="sxs-lookup"><span data-stu-id="8e415-120">Element</span></span>|<span data-ttu-id="8e415-121">Description</span><span class="sxs-lookup"><span data-stu-id="8e415-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8e415-122">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="8e415-122">\<samlSecurityTokenRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/samlsecuritytokenrequirement.md)|<span data-ttu-id="8e415-123">Fournit une configuration pour le <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> (classe), la <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> classe ou une classe dérivée d’un de ces classes.</span><span class="sxs-lookup"><span data-stu-id="8e415-123">Provides configuration for the <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> class, the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, or a derived class of either of these classes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8e415-124">Notes</span><span class="sxs-lookup"><span data-stu-id="8e415-124">Remarks</span></span>  
 <span data-ttu-id="8e415-125">Le `<roleClaimType>` ensembles d’élément le <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.RoleClaimType%2A> propriété lorsqu’un <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> objet est initialisé à partir de la configuration.</span><span class="sxs-lookup"><span data-stu-id="8e415-125">The `<roleClaimType>` element sets the <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.RoleClaimType%2A> property when a <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8e415-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="8e415-126">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SamlSecurityTokenHandler, System.IdentityModel">  
    <samlSecurityTokenRequirement>  
        <roleClaimType value="schemas.microsoft.com/ws/2006/04/identity/claims/role" />  
    </samlSecurityTokenRequirement>  
</add>  
```  
  
## <a name="see-also"></a><span data-ttu-id="8e415-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e415-127">See also</span></span>

- <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.RoleClaimType%2A>
