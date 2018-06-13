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
ms.openlocfilehash: 8283139566050b1858a003316dc46581822a9bbb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33450152"
---
# <a name="corprfgcgeneration-enumeration"></a><span data-ttu-id="3467b-102">COR_PRF_GC_GENERATION, énumération</span><span class="sxs-lookup"><span data-stu-id="3467b-102">COR_PRF_GC_GENERATION Enumeration</span></span>
<span data-ttu-id="3467b-103">Identifie une génération de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="3467b-103">Identifies a garbage-collection generation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3467b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3467b-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_GC_GEN_0 = 0,  
    COR_PRF_GC_GEN_1 = 1,  
    COR_PRF_GC_GEN_2 = 2,  
    COR_PRF_GC_LARGE_OBJECT_HEAP = 3  
} COR_PRF_GC_GENERATION;  
```  
  
## <a name="members"></a><span data-ttu-id="3467b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="3467b-105">Members</span></span>  
  
|<span data-ttu-id="3467b-106">Membre</span><span class="sxs-lookup"><span data-stu-id="3467b-106">Member</span></span>|<span data-ttu-id="3467b-107">Description</span><span class="sxs-lookup"><span data-stu-id="3467b-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_GC_GEN_0`|<span data-ttu-id="3467b-108">L’objet est stocké en tant que la génération 0.</span><span class="sxs-lookup"><span data-stu-id="3467b-108">The object is stored as generation 0.</span></span>|  
|`COR_PRF_GC_GEN_1`|<span data-ttu-id="3467b-109">L’objet est stocké en tant que la génération 1.</span><span class="sxs-lookup"><span data-stu-id="3467b-109">The object is stored as generation 1.</span></span>|  
|`COR_PRF_GC_GEN_2`|<span data-ttu-id="3467b-110">L’objet est stocké en tant que la génération 2.</span><span class="sxs-lookup"><span data-stu-id="3467b-110">The object is stored as generation 2.</span></span>|  
|`COR_PRF_GC_LARGE_OBJECT_HEAP`|<span data-ttu-id="3467b-111">L’objet est stocké dans le tas d’objets volumineux.</span><span class="sxs-lookup"><span data-stu-id="3467b-111">The object is stored in the large-object heap.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3467b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3467b-112">Remarks</span></span>  
 <span data-ttu-id="3467b-113">Le garbage collector améliore les performances de gestion de mémoire en divisant les objets en générations selon l’âge.</span><span class="sxs-lookup"><span data-stu-id="3467b-113">The garbage collector improves memory management performance by dividing objects into generations based on age.</span></span> <span data-ttu-id="3467b-114">Le garbage collector utilise actuellement trois générations, 0, 1 et 2, ainsi qu’un segment de tas spécial qui est utilisé pour les objets volumineux.</span><span class="sxs-lookup"><span data-stu-id="3467b-114">The garbage collector currently uses three generations, numbered 0, 1, and 2, plus a special heap segment that is used for large objects.</span></span> <span data-ttu-id="3467b-115">Objets dont la taille est supérieure à une valeur particulière sont stockés dans le tas d’objets volumineux.</span><span class="sxs-lookup"><span data-stu-id="3467b-115">Objects whose size is larger than a particular value are stored in the large-object heap.</span></span> <span data-ttu-id="3467b-116">Les autres objets alloués démarrent appartenant à la génération 0.</span><span class="sxs-lookup"><span data-stu-id="3467b-116">Other allocated objects start out belonging to generation 0.</span></span> <span data-ttu-id="3467b-117">Tous les objets qui existent après le garbage collection dans la génération 0 sont promus à la génération 1.</span><span class="sxs-lookup"><span data-stu-id="3467b-117">All objects that exist after garbage collection occurs in generation 0 are promoted to generation 1.</span></span> <span data-ttu-id="3467b-118">Déplacer les objets qui existent dans la génération 1 après le garbage collection dans la génération 2.</span><span class="sxs-lookup"><span data-stu-id="3467b-118">Objects that exist after garbage collection occurs in generation 1 move into generation 2.</span></span>  
  
 <span data-ttu-id="3467b-119">L’utilisation des générations signifie que le garbage collector doit utiliser uniquement un sous-ensemble des objets alloués à tout moment.</span><span class="sxs-lookup"><span data-stu-id="3467b-119">The use of generations means that the garbage collector has to work with only a subset of the allocated objects at any one time.</span></span>  
  
 <span data-ttu-id="3467b-120">Le `COR_PRF_GC_GENERATION` énumération est utilisée par le [COR_PRF_GC_GENERATION_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-range-structure.md) structure.</span><span class="sxs-lookup"><span data-stu-id="3467b-120">The `COR_PRF_GC_GENERATION` enumeration is used by the [COR_PRF_GC_GENERATION_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-range-structure.md) structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3467b-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3467b-121">Requirements</span></span>  
 <span data-ttu-id="3467b-122">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3467b-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3467b-123">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3467b-123">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3467b-124">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3467b-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3467b-125">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3467b-125">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3467b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3467b-126">See Also</span></span>  
 [<span data-ttu-id="3467b-127">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="3467b-127">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
