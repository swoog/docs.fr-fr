---
title: <sessionTokenRequirement>
ms.date: 03/30/2017
ms.assetid: 496a1735-cbb7-49d5-a6aa-dd5550462073
author: BrucePerlerMS
ms.openlocfilehash: 0c575e02862884e8f7ecf062138c36fe731f8e19
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793768"
---
# <a name="sessiontokenrequirement"></a><span data-ttu-id="e3eb8-101">\<sessionTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="e3eb8-101">\<sessionTokenRequirement></span></span>
<span data-ttu-id="e3eb8-102">Fournit une configuration pour la <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> classe ou les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-102">Provides configuration for the <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="e3eb8-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="e3eb8-103">\<system.identityModel></span></span>  
<span data-ttu-id="e3eb8-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="e3eb8-104">\<identityConfiguration></span></span>  
<span data-ttu-id="e3eb8-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="e3eb8-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="e3eb8-106">\<add></span><span class="sxs-lookup"><span data-stu-id="e3eb8-106">\<add></span></span>  
<span data-ttu-id="e3eb8-107">\<sessionTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="e3eb8-107">\<sessionTokenRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3eb8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3eb8-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e3eb8-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e3eb8-109">Attributes and Elements</span></span>  
 <span data-ttu-id="e3eb8-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e3eb8-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="e3eb8-111">Attributes</span></span>  
  
|<span data-ttu-id="e3eb8-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="e3eb8-112">Attribute</span></span>|<span data-ttu-id="e3eb8-113">Description</span><span class="sxs-lookup"><span data-stu-id="e3eb8-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e3eb8-114">durée de vie</span><span class="sxs-lookup"><span data-stu-id="e3eb8-114">lifetime</span></span>|<span data-ttu-id="e3eb8-115">Spécifie la durée de vie des jetons de session.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-115">Specifies the lifetime of session tokens.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e3eb8-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e3eb8-116">Child Elements</span></span>  
 <span data-ttu-id="e3eb8-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e3eb8-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e3eb8-118">Parent Elements</span></span>  
  
|<span data-ttu-id="e3eb8-119">Élément</span><span class="sxs-lookup"><span data-stu-id="e3eb8-119">Element</span></span>|<span data-ttu-id="e3eb8-120">Description</span><span class="sxs-lookup"><span data-stu-id="e3eb8-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e3eb8-121">\<add></span><span class="sxs-lookup"><span data-stu-id="e3eb8-121">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="e3eb8-122">Ajoute le Gestionnaire de jetons de sécurité spécifié à la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-122">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="e3eb8-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="e3eb8-123">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">           
    <sessionTokenRequirement lifetime="10:00" />  
</add>  
```
