---
title: '&lt;sessionTokenRequirement&gt;'
ms.date: 03/30/2017
ms.assetid: 496a1735-cbb7-49d5-a6aa-dd5550462073
author: BrucePerlerMS
ms.openlocfilehash: 4d5d2348f04ace7596a3a513c5106ea612dc17b7
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47236885"
---
# <a name="ltsessiontokenrequirementgt"></a><span data-ttu-id="fd9d3-102">&lt;sessionTokenRequirement&gt;</span><span class="sxs-lookup"><span data-stu-id="fd9d3-102">&lt;sessionTokenRequirement&gt;</span></span>
<span data-ttu-id="fd9d3-103">Fournit une configuration pour la <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> classe ou les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="fd9d3-103">Provides configuration for the <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="fd9d3-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="fd9d3-104">\<system.identityModel></span></span>  
<span data-ttu-id="fd9d3-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="fd9d3-105">\<identityConfiguration></span></span>  
<span data-ttu-id="fd9d3-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="fd9d3-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="fd9d3-107">\<add></span><span class="sxs-lookup"><span data-stu-id="fd9d3-107">\<add></span></span>  
<span data-ttu-id="fd9d3-108">\<sessionTokenRequirement ></span><span class="sxs-lookup"><span data-stu-id="fd9d3-108">\<sessionTokenRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd9d3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd9d3-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fd9d3-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="fd9d3-110">Attributes and Elements</span></span>  
 <span data-ttu-id="fd9d3-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="fd9d3-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fd9d3-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="fd9d3-112">Attributes</span></span>  
  
|<span data-ttu-id="fd9d3-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="fd9d3-113">Attribute</span></span>|<span data-ttu-id="fd9d3-114">Description</span><span class="sxs-lookup"><span data-stu-id="fd9d3-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="fd9d3-115">durée de vie</span><span class="sxs-lookup"><span data-stu-id="fd9d3-115">lifetime</span></span>|<span data-ttu-id="fd9d3-116">Spécifie la durée de vie des jetons de session.</span><span class="sxs-lookup"><span data-stu-id="fd9d3-116">Specifies the lifetime of session tokens.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="fd9d3-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fd9d3-117">Child Elements</span></span>  
 <span data-ttu-id="fd9d3-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fd9d3-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="fd9d3-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fd9d3-119">Parent Elements</span></span>  
  
|<span data-ttu-id="fd9d3-120">Élément</span><span class="sxs-lookup"><span data-stu-id="fd9d3-120">Element</span></span>|<span data-ttu-id="fd9d3-121">Description</span><span class="sxs-lookup"><span data-stu-id="fd9d3-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fd9d3-122">\<add></span><span class="sxs-lookup"><span data-stu-id="fd9d3-122">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="fd9d3-123">Ajoute le Gestionnaire de jetons de sécurité spécifié à la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="fd9d3-123">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="fd9d3-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="fd9d3-124">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">           
    <sessionTokenRequirement lifetime="10:00" />  
</add>  
```
