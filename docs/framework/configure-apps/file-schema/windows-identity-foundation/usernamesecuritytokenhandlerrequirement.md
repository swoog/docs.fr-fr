---
title: '&lt;userNameSecurityTokenHandlerRequirement&gt;'
ms.date: 03/30/2017
ms.assetid: 6ec3bac1-b014-49ae-843c-c54518cb709a
author: BrucePerlerMS
ms.openlocfilehash: dfcaad8b150321fda2a86e601bf57204cbdc1a0e
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49123382"
---
# <a name="ltusernamesecuritytokenhandlerrequirementgt"></a><span data-ttu-id="9a3be-102">&lt;userNameSecurityTokenHandlerRequirement&gt;</span><span class="sxs-lookup"><span data-stu-id="9a3be-102">&lt;userNameSecurityTokenHandlerRequirement&gt;</span></span>
<span data-ttu-id="9a3be-103">Fournit une configuration pour la <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> classe ou les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="9a3be-103">Provides configuration for the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="9a3be-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="9a3be-104">\<system.identityModel></span></span>  
<span data-ttu-id="9a3be-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="9a3be-105">\<identityConfiguration></span></span>  
<span data-ttu-id="9a3be-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="9a3be-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="9a3be-107">\<add></span><span class="sxs-lookup"><span data-stu-id="9a3be-107">\<add></span></span>  
<span data-ttu-id="9a3be-108">\<userNameSecurityTokenHandlerRequirement ></span><span class="sxs-lookup"><span data-stu-id="9a3be-108">\<userNameSecurityTokenHandlerRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9a3be-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a3be-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type="System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler, System.IdentityModel.Services">  
        <userNameSecurityTokenHandlerRequirement membershipProviderName=xs:string >  
        </userNameSecurityTokenHandlerRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9a3be-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9a3be-110">Attributes and Elements</span></span>  
 <span data-ttu-id="9a3be-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9a3be-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9a3be-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="9a3be-112">Attributes</span></span>  
  
|<span data-ttu-id="9a3be-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="9a3be-113">Attribute</span></span>|<span data-ttu-id="9a3be-114">Description</span><span class="sxs-lookup"><span data-stu-id="9a3be-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9a3be-115">membershipProviderName</span><span class="sxs-lookup"><span data-stu-id="9a3be-115">membershipProviderName</span></span>|<span data-ttu-id="9a3be-116">Spécifie le <xref:System.Web.Security.MembershipProvider> qui doit être utilisé par le Gestionnaire de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9a3be-116">Specifies the <xref:System.Web.Security.MembershipProvider> that should be used by the security token handler.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9a3be-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9a3be-117">Child Elements</span></span>  
 <span data-ttu-id="9a3be-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9a3be-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9a3be-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9a3be-119">Parent Elements</span></span>  
  
|<span data-ttu-id="9a3be-120">Élément</span><span class="sxs-lookup"><span data-stu-id="9a3be-120">Element</span></span>|<span data-ttu-id="9a3be-121">Description</span><span class="sxs-lookup"><span data-stu-id="9a3be-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9a3be-122">\<add></span><span class="sxs-lookup"><span data-stu-id="9a3be-122">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="9a3be-123">Ajoute le Gestionnaire de jetons de sécurité spécifié à la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="9a3be-123">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9a3be-124">Notes</span><span class="sxs-lookup"><span data-stu-id="9a3be-124">Remarks</span></span>  
 <span data-ttu-id="9a3be-125">Le `<userNameSecurityTokenHandlerRequirement>` ensembles d’élément le <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> propriété lorsqu’un <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> objet est initialisé à partir de la configuration.</span><span class="sxs-lookup"><span data-stu-id="9a3be-125">The `<userNameSecurityTokenHandlerRequirement>` element sets the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> property when a <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9a3be-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="9a3be-126">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler, System.IdentityModel.Services">  
    <userNameSecurityTokenHandlerRequirement membershipProviderName="AspNetSqlProvider/>  
</add>  
```
