---
title: '&lt;Type de revendication&gt;'
ms.date: 03/30/2017
ms.assetid: d17b5831-9a2c-45c4-b0d1-68f48e72e861
author: BrucePerlerMS
ms.openlocfilehash: 805377565b6e835fd9ffba915a003bc56529a3b6
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47234956"
---
# <a name="ltclaimtypegt"></a><span data-ttu-id="8a428-102">&lt;Type de revendication&gt;</span><span class="sxs-lookup"><span data-stu-id="8a428-102">&lt;claimType&gt;</span></span>
<span data-ttu-id="8a428-103">Spécifie une seule revendication facultative ou obligatoire pour les jetons de sécurité entrants.</span><span class="sxs-lookup"><span data-stu-id="8a428-103">Specifies a single optional or required claim for incoming security tokens.</span></span>  
  
 <span data-ttu-id="8a428-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="8a428-104">\<system.identityModel></span></span>  
<span data-ttu-id="8a428-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="8a428-105">\<identityConfiguration></span></span>  
<span data-ttu-id="8a428-106">\<claimTypeRequired ></span><span class="sxs-lookup"><span data-stu-id="8a428-106">\<claimTypeRequired></span></span>  
<span data-ttu-id="8a428-107">\<claimType ></span><span class="sxs-lookup"><span data-stu-id="8a428-107">\<claimType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a428-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a428-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimTypeRequired>  
      <claimType type=URI optional=xs:boolean >  
      </claimType>  
    </claimTypeRequired>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8a428-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="8a428-109">Attributes and Elements</span></span>  
 <span data-ttu-id="8a428-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="8a428-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8a428-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="8a428-111">Attributes</span></span>  
  
|<span data-ttu-id="8a428-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="8a428-112">Attribute</span></span>|<span data-ttu-id="8a428-113">Description</span><span class="sxs-lookup"><span data-stu-id="8a428-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="8a428-114">type</span><span class="sxs-lookup"><span data-stu-id="8a428-114">type</span></span>|<span data-ttu-id="8a428-115">Type de revendication.</span><span class="sxs-lookup"><span data-stu-id="8a428-115">The claim type.</span></span> <span data-ttu-id="8a428-116">En général, un URI.</span><span class="sxs-lookup"><span data-stu-id="8a428-116">Typically a URI.</span></span> <span data-ttu-id="8a428-117">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a428-117">Required.</span></span>|  
|<span data-ttu-id="8a428-118">facultatifs</span><span class="sxs-lookup"><span data-stu-id="8a428-118">optional</span></span>|<span data-ttu-id="8a428-119">Une valeur booléenne qui spécifie si le type de revendication est facultatif.</span><span class="sxs-lookup"><span data-stu-id="8a428-119">A boolean value that specifies whether the claim type is optional.</span></span> <span data-ttu-id="8a428-120">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8a428-120">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8a428-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8a428-121">Child Elements</span></span>  
 <span data-ttu-id="8a428-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8a428-122">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8a428-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8a428-123">Parent Elements</span></span>  
  
|<span data-ttu-id="8a428-124">Élément</span><span class="sxs-lookup"><span data-stu-id="8a428-124">Element</span></span>|<span data-ttu-id="8a428-125">Description</span><span class="sxs-lookup"><span data-stu-id="8a428-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8a428-126">\<claimTypeRequired ></span><span class="sxs-lookup"><span data-stu-id="8a428-126">\<claimTypeRequired></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimtyperequired.md)|<span data-ttu-id="8a428-127">Spécifie le jeu de revendications requises pour les jetons de sécurité entrants.</span><span class="sxs-lookup"><span data-stu-id="8a428-127">Specifies the set of required claims for incoming security tokens.</span></span>|
