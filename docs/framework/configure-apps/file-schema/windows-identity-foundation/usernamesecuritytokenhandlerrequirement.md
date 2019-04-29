---
title: <userNameSecurityTokenHandlerRequirement>
ms.date: 03/30/2017
ms.assetid: 6ec3bac1-b014-49ae-843c-c54518cb709a
author: BrucePerlerMS
ms.openlocfilehash: 18769794da8528f085c567264827db5aa6b214f1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790453"
---
# <a name="usernamesecuritytokenhandlerrequirement"></a><span data-ttu-id="52480-101">\<userNameSecurityTokenHandlerRequirement></span><span class="sxs-lookup"><span data-stu-id="52480-101">\<userNameSecurityTokenHandlerRequirement></span></span>
<span data-ttu-id="52480-102">Fournit une configuration pour la <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> classe ou les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="52480-102">Provides configuration for the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="52480-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="52480-103">\<system.identityModel></span></span>  
<span data-ttu-id="52480-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="52480-104">\<identityConfiguration></span></span>  
<span data-ttu-id="52480-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="52480-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="52480-106">\<add></span><span class="sxs-lookup"><span data-stu-id="52480-106">\<add></span></span>  
<span data-ttu-id="52480-107">\<userNameSecurityTokenHandlerRequirement></span><span class="sxs-lookup"><span data-stu-id="52480-107">\<userNameSecurityTokenHandlerRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="52480-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52480-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="52480-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="52480-109">Attributes and Elements</span></span>  
 <span data-ttu-id="52480-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="52480-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="52480-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="52480-111">Attributes</span></span>  
  
|<span data-ttu-id="52480-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="52480-112">Attribute</span></span>|<span data-ttu-id="52480-113">Description</span><span class="sxs-lookup"><span data-stu-id="52480-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="52480-114">membershipProviderName</span><span class="sxs-lookup"><span data-stu-id="52480-114">membershipProviderName</span></span>|<span data-ttu-id="52480-115">Spécifie le <xref:System.Web.Security.MembershipProvider> qui doit être utilisé par le Gestionnaire de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="52480-115">Specifies the <xref:System.Web.Security.MembershipProvider> that should be used by the security token handler.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="52480-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="52480-116">Child Elements</span></span>  
 <span data-ttu-id="52480-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="52480-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="52480-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="52480-118">Parent Elements</span></span>  
  
|<span data-ttu-id="52480-119">Élément</span><span class="sxs-lookup"><span data-stu-id="52480-119">Element</span></span>|<span data-ttu-id="52480-120">Description</span><span class="sxs-lookup"><span data-stu-id="52480-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="52480-121">\<add></span><span class="sxs-lookup"><span data-stu-id="52480-121">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="52480-122">Ajoute le Gestionnaire de jetons de sécurité spécifié à la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="52480-122">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="52480-123">Notes</span><span class="sxs-lookup"><span data-stu-id="52480-123">Remarks</span></span>  
 <span data-ttu-id="52480-124">Le `<userNameSecurityTokenHandlerRequirement>` ensembles d’élément le <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> propriété lorsqu’un <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> objet est initialisé à partir de la configuration.</span><span class="sxs-lookup"><span data-stu-id="52480-124">The `<userNameSecurityTokenHandlerRequirement>` element sets the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> property when a <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="52480-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="52480-125">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler, System.IdentityModel.Services">  
    <userNameSecurityTokenHandlerRequirement membershipProviderName="AspNetSqlProvider/>  
</add>  
```
