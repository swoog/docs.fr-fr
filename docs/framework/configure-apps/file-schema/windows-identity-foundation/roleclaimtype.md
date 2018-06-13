---
title: '&lt;roleClaimType&gt;'
ms.date: 03/30/2017
ms.assetid: 69a49deb-6369-41ba-806b-ae8d21fac64b
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 909df1bd6054d9737f91c30c3c6b2d68b932281c
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32755186"
---
# <a name="ltroleclaimtypegt"></a><span data-ttu-id="b90b2-102">&lt;roleClaimType&gt;</span><span class="sxs-lookup"><span data-stu-id="b90b2-102">&lt;roleClaimType&gt;</span></span>
<span data-ttu-id="b90b2-103">Spécifie le type de revendication qui définit les revendications de type de rôle dans la collection de <xref:System.Security.Claims.ClaimsIdentity> objets retournés par la <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> méthode du Gestionnaire de jeton.</span><span class="sxs-lookup"><span data-stu-id="b90b2-103">Specifies the claim type that defines the role type claims in the collection of <xref:System.Security.Claims.ClaimsIdentity> objects returned by the <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> method of the token handler.</span></span>  
  
 <span data-ttu-id="b90b2-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="b90b2-104">\<system.identityModel></span></span>  
<span data-ttu-id="b90b2-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="b90b2-105">\<identityConfiguration></span></span>  
<span data-ttu-id="b90b2-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="b90b2-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="b90b2-107">\<add></span><span class="sxs-lookup"><span data-stu-id="b90b2-107">\<add></span></span>  
<span data-ttu-id="b90b2-108">\<samlSecurityTokenRequirement ></span><span class="sxs-lookup"><span data-stu-id="b90b2-108">\<samlSecurityTokenRequirement></span></span>  
<span data-ttu-id="b90b2-109">\<roleClaimType ></span><span class="sxs-lookup"><span data-stu-id="b90b2-109">\<roleClaimType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b90b2-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b90b2-110">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b90b2-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b90b2-111">Attributes and Elements</span></span>  
 <span data-ttu-id="b90b2-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b90b2-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b90b2-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="b90b2-113">Attributes</span></span>  
  
|<span data-ttu-id="b90b2-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="b90b2-114">Attribute</span></span>|<span data-ttu-id="b90b2-115">Description</span><span class="sxs-lookup"><span data-stu-id="b90b2-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b90b2-116">par défaut</span><span class="sxs-lookup"><span data-stu-id="b90b2-116">value</span></span>|<span data-ttu-id="b90b2-117">Chaîne qui spécifie l’URI qui représente le type de revendication de la revendication à utiliser pour le type de revendication de rôle.</span><span class="sxs-lookup"><span data-stu-id="b90b2-117">A string that specifies the URI that represents the claim type of the claim to use for the role claim type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b90b2-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b90b2-118">Child Elements</span></span>  
 <span data-ttu-id="b90b2-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="b90b2-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b90b2-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b90b2-120">Parent Elements</span></span>  
  
|<span data-ttu-id="b90b2-121">Élément</span><span class="sxs-lookup"><span data-stu-id="b90b2-121">Element</span></span>|<span data-ttu-id="b90b2-122">Description</span><span class="sxs-lookup"><span data-stu-id="b90b2-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b90b2-123">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="b90b2-123">\<samlSecurityTokenRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/samlsecuritytokenrequirement.md)|<span data-ttu-id="b90b2-124">Fournit la configuration pour le <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> (classe), la <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> classe ou une classe dérivée d’un de ces classes.</span><span class="sxs-lookup"><span data-stu-id="b90b2-124">Provides configuration for the <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> class, the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, or a derived class of either of these classes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b90b2-125">Notes</span><span class="sxs-lookup"><span data-stu-id="b90b2-125">Remarks</span></span>  
 <span data-ttu-id="b90b2-126">Le `<roleClaimType>` ensembles d’éléments le <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.RoleClaimType%2A> propriété lorsqu’un <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> objet est initialisé à partir de la configuration.</span><span class="sxs-lookup"><span data-stu-id="b90b2-126">The `<roleClaimType>` element sets the <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.RoleClaimType%2A> property when a <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b90b2-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="b90b2-127">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SamlSecurityTokenHandler, System.IdentityModel">  
    <samlSecurityTokenRequirement>  
        <roleClaimType value="schemas.microsoft.com/ws/2006/04/identity/claims/role" />  
    </samlSecurityTokenRequirement>  
</add>  
```  
  
## <a name="see-also"></a><span data-ttu-id="b90b2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b90b2-128">See Also</span></span>  
 <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.RoleClaimType%2A>
