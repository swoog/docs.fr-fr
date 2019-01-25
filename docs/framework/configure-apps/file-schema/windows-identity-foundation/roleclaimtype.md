---
title: '&lt;roleClaimType&gt;'
ms.date: 03/30/2017
ms.assetid: 69a49deb-6369-41ba-806b-ae8d21fac64b
author: BrucePerlerMS
ms.openlocfilehash: 6114a95f3942c367849785ce981858f276c0b8fc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54599944"
---
# <a name="ltroleclaimtypegt"></a><span data-ttu-id="be135-102">&lt;roleClaimType&gt;</span><span class="sxs-lookup"><span data-stu-id="be135-102">&lt;roleClaimType&gt;</span></span>
<span data-ttu-id="be135-103">Spécifie le type de revendication qui définit les revendications de type de rôle dans la collection de <xref:System.Security.Claims.ClaimsIdentity> objets retournés par la <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> méthode de gestionnaire de jetons.</span><span class="sxs-lookup"><span data-stu-id="be135-103">Specifies the claim type that defines the role type claims in the collection of <xref:System.Security.Claims.ClaimsIdentity> objects returned by the <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> method of the token handler.</span></span>  
  
 <span data-ttu-id="be135-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="be135-104">\<system.identityModel></span></span>  
<span data-ttu-id="be135-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="be135-105">\<identityConfiguration></span></span>  
<span data-ttu-id="be135-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="be135-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="be135-107">\<add></span><span class="sxs-lookup"><span data-stu-id="be135-107">\<add></span></span>  
<span data-ttu-id="be135-108">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="be135-108">\<samlSecurityTokenRequirement></span></span>  
<span data-ttu-id="be135-109">\<roleClaimType></span><span class="sxs-lookup"><span data-stu-id="be135-109">\<roleClaimType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be135-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be135-110">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="be135-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="be135-111">Attributes and Elements</span></span>  
 <span data-ttu-id="be135-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="be135-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="be135-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="be135-113">Attributes</span></span>  
  
|<span data-ttu-id="be135-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="be135-114">Attribute</span></span>|<span data-ttu-id="be135-115">Description</span><span class="sxs-lookup"><span data-stu-id="be135-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="be135-116">par défaut</span><span class="sxs-lookup"><span data-stu-id="be135-116">value</span></span>|<span data-ttu-id="be135-117">Chaîne qui spécifie l’URI qui représente le type de revendication de la revendication à utiliser pour le type de revendication de rôle.</span><span class="sxs-lookup"><span data-stu-id="be135-117">A string that specifies the URI that represents the claim type of the claim to use for the role claim type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="be135-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="be135-118">Child Elements</span></span>  
 <span data-ttu-id="be135-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="be135-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="be135-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="be135-120">Parent Elements</span></span>  
  
|<span data-ttu-id="be135-121">Élément</span><span class="sxs-lookup"><span data-stu-id="be135-121">Element</span></span>|<span data-ttu-id="be135-122">Description</span><span class="sxs-lookup"><span data-stu-id="be135-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="be135-123">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="be135-123">\<samlSecurityTokenRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/samlsecuritytokenrequirement.md)|<span data-ttu-id="be135-124">Fournit une configuration pour le <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> (classe), la <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> classe ou une classe dérivée d’un de ces classes.</span><span class="sxs-lookup"><span data-stu-id="be135-124">Provides configuration for the <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> class, the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, or a derived class of either of these classes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="be135-125">Notes</span><span class="sxs-lookup"><span data-stu-id="be135-125">Remarks</span></span>  
 <span data-ttu-id="be135-126">Le `<roleClaimType>` ensembles d’élément le <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.RoleClaimType%2A> propriété lorsqu’un <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> objet est initialisé à partir de la configuration.</span><span class="sxs-lookup"><span data-stu-id="be135-126">The `<roleClaimType>` element sets the <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.RoleClaimType%2A> property when a <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="be135-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="be135-127">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SamlSecurityTokenHandler, System.IdentityModel">  
    <samlSecurityTokenRequirement>  
        <roleClaimType value="schemas.microsoft.com/ws/2006/04/identity/claims/role" />  
    </samlSecurityTokenRequirement>  
</add>  
```  
  
## <a name="see-also"></a><span data-ttu-id="be135-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be135-128">See also</span></span>
- <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.RoleClaimType%2A>
