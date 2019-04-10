---
title: COR_PRF_GC_GENERATION, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_GC_GENERATION
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_GC_GENERATION
helpviewer_keywords:
- COR_GC_GENERATION_FLAGS enumeration [.NET Framework profiling]
ms.assetid: d6ece160-26ad-4d39-abd7-05acd6f78c48
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0178e2a7877803644bb25e6700306d7ac2ef2d4f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59215889"
---
# <a name="corprfgcgeneration-enumeration"></a><span data-ttu-id="faad7-102">COR_PRF_GC_GENERATION, énumération</span><span class="sxs-lookup"><span data-stu-id="faad7-102">COR_PRF_GC_GENERATION Enumeration</span></span>
<span data-ttu-id="faad7-103">Identifie une génération de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="faad7-103">Identifies a garbage-collection generation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="faad7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="faad7-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_GC_GEN_0 = 0,  
    COR_PRF_GC_GEN_1 = 1,  
    COR_PRF_GC_GEN_2 = 2,  
    COR_PRF_GC_LARGE_OBJECT_HEAP = 3  
} COR_PRF_GC_GENERATION;  
```  
  
## <a name="members"></a><span data-ttu-id="faad7-105">Membres</span><span class="sxs-lookup"><span data-stu-id="faad7-105">Members</span></span>  
  
|<span data-ttu-id="faad7-106">Membre</span><span class="sxs-lookup"><span data-stu-id="faad7-106">Member</span></span>|<span data-ttu-id="faad7-107">Description</span><span class="sxs-lookup"><span data-stu-id="faad7-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_GC_GEN_0`|<span data-ttu-id="faad7-108">L’objet est stocké en tant que génération 0.</span><span class="sxs-lookup"><span data-stu-id="faad7-108">The object is stored as generation 0.</span></span>|  
|`COR_PRF_GC_GEN_1`|<span data-ttu-id="faad7-109">L’objet est stocké en tant que génération 1.</span><span class="sxs-lookup"><span data-stu-id="faad7-109">The object is stored as generation 1.</span></span>|  
|`COR_PRF_GC_GEN_2`|<span data-ttu-id="faad7-110">L’objet est stocké en tant que génération 2.</span><span class="sxs-lookup"><span data-stu-id="faad7-110">The object is stored as generation 2.</span></span>|  
|`COR_PRF_GC_LARGE_OBJECT_HEAP`|<span data-ttu-id="faad7-111">L’objet est stocké dans le tas d’objets volumineux.</span><span class="sxs-lookup"><span data-stu-id="faad7-111">The object is stored in the large-object heap.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="faad7-112">Notes</span><span class="sxs-lookup"><span data-stu-id="faad7-112">Remarks</span></span>  
 <span data-ttu-id="faad7-113">Le garbage collector améliore les performances de gestion de mémoire en divisant les objets dans les générations en fonction de l’âge.</span><span class="sxs-lookup"><span data-stu-id="faad7-113">The garbage collector improves memory management performance by dividing objects into generations based on age.</span></span> <span data-ttu-id="faad7-114">Le garbage collector utilise actuellement trois générations, 0, 1 et 2, ainsi qu’un segment de tas spécial qui est utilisé pour les objets volumineux.</span><span class="sxs-lookup"><span data-stu-id="faad7-114">The garbage collector currently uses three generations, numbered 0, 1, and 2, plus a special heap segment that is used for large objects.</span></span> <span data-ttu-id="faad7-115">Objets dont la taille est supérieure à une valeur particulière sont stockés dans le tas d’objets volumineux.</span><span class="sxs-lookup"><span data-stu-id="faad7-115">Objects whose size is larger than a particular value are stored in the large-object heap.</span></span> <span data-ttu-id="faad7-116">Autres objets alloués commencent appartenant à la génération 0.</span><span class="sxs-lookup"><span data-stu-id="faad7-116">Other allocated objects start out belonging to generation 0.</span></span> <span data-ttu-id="faad7-117">Tous les objets qui existent une fois que le garbage collection se produit dans la génération 0 sont promus à la génération 1.</span><span class="sxs-lookup"><span data-stu-id="faad7-117">All objects that exist after garbage collection occurs in generation 0 are promoted to generation 1.</span></span> <span data-ttu-id="faad7-118">Déplacent des objets qui existent dans la génération 1 après le garbage collection dans la génération 2.</span><span class="sxs-lookup"><span data-stu-id="faad7-118">Objects that exist after garbage collection occurs in generation 1 move into generation 2.</span></span>  
  
 <span data-ttu-id="faad7-119">L’utilisation de générations signifie que le garbage collector doit travailler avec uniquement un sous-ensemble des objets alloués à tout moment.</span><span class="sxs-lookup"><span data-stu-id="faad7-119">The use of generations means that the garbage collector has to work with only a subset of the allocated objects at any one time.</span></span>  
  
 <span data-ttu-id="faad7-120">Le `COR_PRF_GC_GENERATION` énumération est utilisée par le [COR_PRF_GC_GENERATION_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-range-structure.md) structure.</span><span class="sxs-lookup"><span data-stu-id="faad7-120">The `COR_PRF_GC_GENERATION` enumeration is used by the [COR_PRF_GC_GENERATION_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-range-structure.md) structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="faad7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="faad7-121">Requirements</span></span>  
 <span data-ttu-id="faad7-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="faad7-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="faad7-123">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="faad7-123">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="faad7-124">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="faad7-124">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="faad7-125">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="faad7-125">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="faad7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="faad7-126">See also</span></span>

- [<span data-ttu-id="faad7-127">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="faad7-127">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
