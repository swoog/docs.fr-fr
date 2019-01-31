---
title: <claimType>
ms.date: 03/30/2017
ms.assetid: d17b5831-9a2c-45c4-b0d1-68f48e72e861
author: BrucePerlerMS
ms.openlocfilehash: 6bc185572528d4229ee53f1421eaa5bf27b053e6
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55267233"
---
# <a name="claimtype"></a><span data-ttu-id="c4c9a-101">\<claimType></span><span class="sxs-lookup"><span data-stu-id="c4c9a-101">\<claimType></span></span>
<span data-ttu-id="c4c9a-102">Spécifie une seule revendication facultative ou obligatoire pour les jetons de sécurité entrants.</span><span class="sxs-lookup"><span data-stu-id="c4c9a-102">Specifies a single optional or required claim for incoming security tokens.</span></span>  
  
 <span data-ttu-id="c4c9a-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="c4c9a-103">\<system.identityModel></span></span>  
<span data-ttu-id="c4c9a-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="c4c9a-104">\<identityConfiguration></span></span>  
<span data-ttu-id="c4c9a-105">\<claimTypeRequired></span><span class="sxs-lookup"><span data-stu-id="c4c9a-105">\<claimTypeRequired></span></span>  
<span data-ttu-id="c4c9a-106">\<claimType></span><span class="sxs-lookup"><span data-stu-id="c4c9a-106">\<claimType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4c9a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4c9a-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c4c9a-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c4c9a-108">Attributes and Elements</span></span>  
 <span data-ttu-id="c4c9a-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c4c9a-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c4c9a-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="c4c9a-110">Attributes</span></span>  
  
|<span data-ttu-id="c4c9a-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="c4c9a-111">Attribute</span></span>|<span data-ttu-id="c4c9a-112">Description</span><span class="sxs-lookup"><span data-stu-id="c4c9a-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c4c9a-113">type</span><span class="sxs-lookup"><span data-stu-id="c4c9a-113">type</span></span>|<span data-ttu-id="c4c9a-114">Type de revendication.</span><span class="sxs-lookup"><span data-stu-id="c4c9a-114">The claim type.</span></span> <span data-ttu-id="c4c9a-115">En général, un URI.</span><span class="sxs-lookup"><span data-stu-id="c4c9a-115">Typically a URI.</span></span> <span data-ttu-id="c4c9a-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c4c9a-116">Required.</span></span>|  
|<span data-ttu-id="c4c9a-117">facultatifs</span><span class="sxs-lookup"><span data-stu-id="c4c9a-117">optional</span></span>|<span data-ttu-id="c4c9a-118">Une valeur booléenne qui spécifie si le type de revendication est facultatif.</span><span class="sxs-lookup"><span data-stu-id="c4c9a-118">A boolean value that specifies whether the claim type is optional.</span></span> <span data-ttu-id="c4c9a-119">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="c4c9a-119">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c4c9a-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c4c9a-120">Child Elements</span></span>  
 <span data-ttu-id="c4c9a-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c4c9a-121">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c4c9a-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c4c9a-122">Parent Elements</span></span>  
  
|<span data-ttu-id="c4c9a-123">Élément</span><span class="sxs-lookup"><span data-stu-id="c4c9a-123">Element</span></span>|<span data-ttu-id="c4c9a-124">Description</span><span class="sxs-lookup"><span data-stu-id="c4c9a-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c4c9a-125">\<claimTypeRequired></span><span class="sxs-lookup"><span data-stu-id="c4c9a-125">\<claimTypeRequired></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimtyperequired.md)|<span data-ttu-id="c4c9a-126">Spécifie le jeu de revendications requises pour les jetons de sécurité entrants.</span><span class="sxs-lookup"><span data-stu-id="c4c9a-126">Specifies the set of required claims for incoming security tokens.</span></span>|
