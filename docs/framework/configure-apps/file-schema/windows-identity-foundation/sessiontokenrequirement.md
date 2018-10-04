---
title: '&lt;sessionTokenRequirement&gt;'
ms.date: 03/30/2017
ms.assetid: 496a1735-cbb7-49d5-a6aa-dd5550462073
author: BrucePerlerMS
ms.openlocfilehash: 4d5d2348f04ace7596a3a513c5106ea612dc17b7
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48792927"
---
# <a name="ltsessiontokenrequirementgt"></a><span data-ttu-id="9538c-102">&lt;sessionTokenRequirement&gt;</span><span class="sxs-lookup"><span data-stu-id="9538c-102">&lt;sessionTokenRequirement&gt;</span></span>
<span data-ttu-id="9538c-103">Fournit une configuration pour la <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> classe ou les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="9538c-103">Provides configuration for the <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="9538c-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="9538c-104">\<system.identityModel></span></span>  
<span data-ttu-id="9538c-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="9538c-105">\<identityConfiguration></span></span>  
<span data-ttu-id="9538c-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="9538c-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="9538c-107">\<add></span><span class="sxs-lookup"><span data-stu-id="9538c-107">\<add></span></span>  
<span data-ttu-id="9538c-108">\<sessionTokenRequirement ></span><span class="sxs-lookup"><span data-stu-id="9538c-108">\<sessionTokenRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9538c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9538c-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">  
        <sessionTokenRequirement lifetime=TimeSpan >  
        </sessionTokenRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9538c-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9538c-110">Attributes and Elements</span></span>  
 <span data-ttu-id="9538c-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9538c-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9538c-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="9538c-112">Attributes</span></span>  
  
|<span data-ttu-id="9538c-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="9538c-113">Attribute</span></span>|<span data-ttu-id="9538c-114">Description</span><span class="sxs-lookup"><span data-stu-id="9538c-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9538c-115">durée de vie</span><span class="sxs-lookup"><span data-stu-id="9538c-115">lifetime</span></span>|<span data-ttu-id="9538c-116">Spécifie la durée de vie des jetons de session.</span><span class="sxs-lookup"><span data-stu-id="9538c-116">Specifies the lifetime of session tokens.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9538c-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9538c-117">Child Elements</span></span>  
 <span data-ttu-id="9538c-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9538c-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9538c-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9538c-119">Parent Elements</span></span>  
  
|<span data-ttu-id="9538c-120">Élément</span><span class="sxs-lookup"><span data-stu-id="9538c-120">Element</span></span>|<span data-ttu-id="9538c-121">Description</span><span class="sxs-lookup"><span data-stu-id="9538c-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9538c-122">\<add></span><span class="sxs-lookup"><span data-stu-id="9538c-122">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="9538c-123">Ajoute le Gestionnaire de jetons de sécurité spécifié à la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="9538c-123">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="9538c-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="9538c-124">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">           
    <sessionTokenRequirement lifetime="10:00" />  
</add>  
```
