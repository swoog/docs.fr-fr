---
title: <sessionTokenRequirement>
ms.date: 03/30/2017
ms.assetid: 496a1735-cbb7-49d5-a6aa-dd5550462073
author: BrucePerlerMS
ms.openlocfilehash: 0c575e02862884e8f7ecf062138c36fe731f8e19
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271900"
---
# <a name="sessiontokenrequirement"></a><span data-ttu-id="07861-101">\<sessionTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="07861-101">\<sessionTokenRequirement></span></span>
<span data-ttu-id="07861-102">Fournit une configuration pour la <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> classe ou les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="07861-102">Provides configuration for the <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="07861-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="07861-103">\<system.identityModel></span></span>  
<span data-ttu-id="07861-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="07861-104">\<identityConfiguration></span></span>  
<span data-ttu-id="07861-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="07861-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="07861-106">\<add></span><span class="sxs-lookup"><span data-stu-id="07861-106">\<add></span></span>  
<span data-ttu-id="07861-107">\<sessionTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="07861-107">\<sessionTokenRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07861-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07861-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="07861-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="07861-109">Attributes and Elements</span></span>  
 <span data-ttu-id="07861-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="07861-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="07861-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="07861-111">Attributes</span></span>  
  
|<span data-ttu-id="07861-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="07861-112">Attribute</span></span>|<span data-ttu-id="07861-113">Description</span><span class="sxs-lookup"><span data-stu-id="07861-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="07861-114">durée de vie</span><span class="sxs-lookup"><span data-stu-id="07861-114">lifetime</span></span>|<span data-ttu-id="07861-115">Spécifie la durée de vie des jetons de session.</span><span class="sxs-lookup"><span data-stu-id="07861-115">Specifies the lifetime of session tokens.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="07861-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="07861-116">Child Elements</span></span>  
 <span data-ttu-id="07861-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="07861-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="07861-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="07861-118">Parent Elements</span></span>  
  
|<span data-ttu-id="07861-119">Élément</span><span class="sxs-lookup"><span data-stu-id="07861-119">Element</span></span>|<span data-ttu-id="07861-120">Description</span><span class="sxs-lookup"><span data-stu-id="07861-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="07861-121">\<add></span><span class="sxs-lookup"><span data-stu-id="07861-121">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="07861-122">Ajoute le Gestionnaire de jetons de sécurité spécifié à la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="07861-122">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="07861-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="07861-123">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">           
    <sessionTokenRequirement lifetime="10:00" />  
</add>  
```
