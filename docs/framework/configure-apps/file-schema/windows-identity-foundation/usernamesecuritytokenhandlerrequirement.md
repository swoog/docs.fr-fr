---
title: '&lt;userNameSecurityTokenHandlerRequirement&gt;'
ms.date: 03/30/2017
ms.assetid: 6ec3bac1-b014-49ae-843c-c54518cb709a
author: BrucePerlerMS
ms.openlocfilehash: dfcaad8b150321fda2a86e601bf57204cbdc1a0e
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47075030"
---
# <a name="ltusernamesecuritytokenhandlerrequirementgt"></a><span data-ttu-id="9e657-102">&lt;userNameSecurityTokenHandlerRequirement&gt;</span><span class="sxs-lookup"><span data-stu-id="9e657-102">&lt;userNameSecurityTokenHandlerRequirement&gt;</span></span>
<span data-ttu-id="9e657-103">Fournit une configuration pour la <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> classe ou les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="9e657-103">Provides configuration for the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="9e657-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="9e657-104">\<system.identityModel></span></span>  
<span data-ttu-id="9e657-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="9e657-105">\<identityConfiguration></span></span>  
<span data-ttu-id="9e657-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="9e657-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="9e657-107">\<add></span><span class="sxs-lookup"><span data-stu-id="9e657-107">\<add></span></span>  
<span data-ttu-id="9e657-108">\<userNameSecurityTokenHandlerRequirement ></span><span class="sxs-lookup"><span data-stu-id="9e657-108">\<userNameSecurityTokenHandlerRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9e657-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e657-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9e657-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9e657-110">Attributes and Elements</span></span>  
 <span data-ttu-id="9e657-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9e657-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9e657-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="9e657-112">Attributes</span></span>  
  
|<span data-ttu-id="9e657-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="9e657-113">Attribute</span></span>|<span data-ttu-id="9e657-114">Description</span><span class="sxs-lookup"><span data-stu-id="9e657-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9e657-115">membershipProviderName</span><span class="sxs-lookup"><span data-stu-id="9e657-115">membershipProviderName</span></span>|<span data-ttu-id="9e657-116">Spécifie le <xref:System.Web.Security.MembershipProvider> qui doit être utilisé par le Gestionnaire de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9e657-116">Specifies the <xref:System.Web.Security.MembershipProvider> that should be used by the security token handler.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9e657-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9e657-117">Child Elements</span></span>  
 <span data-ttu-id="9e657-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9e657-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9e657-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9e657-119">Parent Elements</span></span>  
  
|<span data-ttu-id="9e657-120">Élément</span><span class="sxs-lookup"><span data-stu-id="9e657-120">Element</span></span>|<span data-ttu-id="9e657-121">Description</span><span class="sxs-lookup"><span data-stu-id="9e657-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9e657-122">\<add></span><span class="sxs-lookup"><span data-stu-id="9e657-122">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="9e657-123">Ajoute le Gestionnaire de jetons de sécurité spécifié à la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="9e657-123">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9e657-124">Notes</span><span class="sxs-lookup"><span data-stu-id="9e657-124">Remarks</span></span>  
 <span data-ttu-id="9e657-125">Le `<userNameSecurityTokenHandlerRequirement>` ensembles d’élément le <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> propriété lorsqu’un <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> objet est initialisé à partir de la configuration.</span><span class="sxs-lookup"><span data-stu-id="9e657-125">The `<userNameSecurityTokenHandlerRequirement>` element sets the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> property when a <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9e657-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="9e657-126">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler, System.IdentityModel.Services">  
    <userNameSecurityTokenHandlerRequirement membershipProviderName="AspNetSqlProvider/>  
</add>  
```
