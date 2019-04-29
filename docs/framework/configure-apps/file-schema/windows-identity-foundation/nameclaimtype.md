---
title: <nameClaimType>
ms.date: 03/30/2017
ms.assetid: 17514d95-f0f5-4789-8e28-346640dc227c
author: BrucePerlerMS
ms.openlocfilehash: 5202e162a7eb5fc4e36d6a6c0a2c18af48872a69
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61791597"
---
# <a name="nameclaimtype"></a><span data-ttu-id="cf816-101">\<nameClaimType></span><span class="sxs-lookup"><span data-stu-id="cf816-101">\<nameClaimType></span></span>
<span data-ttu-id="cf816-102">Définit le type de revendication qui spécifie le <xref:System.Security.Principal.IIdentity.Name%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="cf816-102">Sets the claim type that specifies the <xref:System.Security.Principal.IIdentity.Name%2A> property.</span></span> <span data-ttu-id="cf816-103">Le type de revendication est utilisé pour rechercher un <xref:System.Security.Claims.Claim> dans la collection de <xref:System.Security.Claims.ClaimsIdentity> objets retournés par la <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> méthode de ce gestionnaire de jetons.</span><span class="sxs-lookup"><span data-stu-id="cf816-103">The claim type is used to search for a <xref:System.Security.Claims.Claim> in the collection of <xref:System.Security.Claims.ClaimsIdentity> objects returned by the <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> method of this token handler.</span></span> <span data-ttu-id="cf816-104">La valeur de la revendication correspondante est alors définie comme le nom de la <xref:System.Security.Principal.IIdentity> généré à partir de ce gestionnaire de jetons.</span><span class="sxs-lookup"><span data-stu-id="cf816-104">The value of the matching claim is then set as the name of the <xref:System.Security.Principal.IIdentity> generated from this token handler.</span></span>  
  
 <span data-ttu-id="cf816-105">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="cf816-105">\<system.identityModel></span></span>  
<span data-ttu-id="cf816-106">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="cf816-106">\<identityConfiguration></span></span>  
<span data-ttu-id="cf816-107">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="cf816-107">\<securityTokenHandlers></span></span>  
<span data-ttu-id="cf816-108">\<add></span><span class="sxs-lookup"><span data-stu-id="cf816-108">\<add></span></span>  
<span data-ttu-id="cf816-109">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="cf816-109">\<samlSecurityTokenRequirement></span></span>  
<span data-ttu-id="cf816-110">\<nameClaimType></span><span class="sxs-lookup"><span data-stu-id="cf816-110">\<nameClaimType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cf816-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf816-111">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add>  
        <samlSecurityTokenRequirement>  
          <nameClaimType value=xs:string>  
          </nameClaimType>  
        </samlSecurityTokenRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cf816-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="cf816-112">Attributes and Elements</span></span>  
 <span data-ttu-id="cf816-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="cf816-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cf816-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="cf816-114">Attributes</span></span>  
  
|<span data-ttu-id="cf816-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="cf816-115">Attribute</span></span>|<span data-ttu-id="cf816-116">Description</span><span class="sxs-lookup"><span data-stu-id="cf816-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="cf816-117">par défaut</span><span class="sxs-lookup"><span data-stu-id="cf816-117">value</span></span>|<span data-ttu-id="cf816-118">Chaîne qui spécifie l’URI qui représente le type de revendication de la revendication à utiliser pour le <xref:System.Security.Principal.IIdentity.Name%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="cf816-118">A string that specifies the URI that represents the claim type of the claim to use for the <xref:System.Security.Principal.IIdentity.Name%2A> property.</span></span> <span data-ttu-id="cf816-119">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="cf816-119">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cf816-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cf816-120">Child Elements</span></span>  
 <span data-ttu-id="cf816-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cf816-121">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="cf816-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="cf816-122">Parent Elements</span></span>  
  
|<span data-ttu-id="cf816-123">Élément</span><span class="sxs-lookup"><span data-stu-id="cf816-123">Element</span></span>|<span data-ttu-id="cf816-124">Description</span><span class="sxs-lookup"><span data-stu-id="cf816-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cf816-125">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="cf816-125">\<samlSecurityTokenRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/samlsecuritytokenrequirement.md)|<span data-ttu-id="cf816-126">Fournit une configuration pour le <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> (classe), la <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> classe ou une classe dérivée d’un de ces classes.</span><span class="sxs-lookup"><span data-stu-id="cf816-126">Provides configuration for the <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> class, the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, or a derived class of either of these classes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cf816-127">Notes</span><span class="sxs-lookup"><span data-stu-id="cf816-127">Remarks</span></span>  
 <span data-ttu-id="cf816-128">Le `<nameClaimType>` ensembles d’élément le <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.NameClaimType%2A> propriété lorsqu’un <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> objet est initialisé à partir de la configuration.</span><span class="sxs-lookup"><span data-stu-id="cf816-128">The `<nameClaimType>` element sets the <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.NameClaimType%2A> property when a <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cf816-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="cf816-129">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SamlSecurityTokenHandler, System.IdentityModel">  
    <samlSecurityTokenRequirement>  
        <nameClaimType value="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name" />  
    </samlSecurityTokenRequirement>  
</add>  
```  
  
## <a name="see-also"></a><span data-ttu-id="cf816-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf816-130">See also</span></span>

- <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.NameClaimType%2A>
