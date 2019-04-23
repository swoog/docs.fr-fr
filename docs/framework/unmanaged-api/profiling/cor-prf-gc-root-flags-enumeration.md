---
title: COR_PRF_GC_ROOT_FLAGS, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_GC_ROOT_FLAGS
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_GC_ROOT_FLAGS
helpviewer_keywords:
- COR_PRF_GC_ROOT_FLAGS enumeration [.NET Framework profiling]
ms.assetid: 4611ee6f-0f05-4d84-91e1-e83d5e7dd7e4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 263c22a07f363c2752afb50779515de043976e93
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59207706"
---
# <a name="corprfgcrootflags-enumeration"></a><span data-ttu-id="12cef-102">COR_PRF_GC_ROOT_FLAGS, énumération</span><span class="sxs-lookup"><span data-stu-id="12cef-102">COR_PRF_GC_ROOT_FLAGS Enumeration</span></span>
<span data-ttu-id="12cef-103">Indique une propriété d’une racine de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="12cef-103">Indicates a property of a garbage collection root.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12cef-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12cef-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_GC_ROOT_PINNING = 0x1,  
    COR_PRF_GC_ROOT_WEAKREF = 0x2,  
    COR_PRF_GC_ROOT_INTERIOR = 0x4,  
    COR_PRF_GC_ROOT_REFCOUNTED = 0x8,  
} COR_PRF_GC_ROOT_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="12cef-105">Membres</span><span class="sxs-lookup"><span data-stu-id="12cef-105">Members</span></span>  
  
|<span data-ttu-id="12cef-106">Membre</span><span class="sxs-lookup"><span data-stu-id="12cef-106">Member</span></span>|<span data-ttu-id="12cef-107">Description</span><span class="sxs-lookup"><span data-stu-id="12cef-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_GC_ROOT_PINNING`|<span data-ttu-id="12cef-108">La racine empêche un garbage collection de déplacer l’objet.</span><span class="sxs-lookup"><span data-stu-id="12cef-108">The root prevents a garbage collection from moving the object.</span></span>|  
|`COR_PRF_GC_ROOT_WEAKREF`|<span data-ttu-id="12cef-109">La racine n’empêche pas le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="12cef-109">The root does not prevent garbage collection.</span></span>|  
|`COR_PRF_GC_ROOT_INTERIOR`|<span data-ttu-id="12cef-110">La racine fait référence à un champ de l’objet plutôt que l’objet lui-même.</span><span class="sxs-lookup"><span data-stu-id="12cef-110">The root refers to a field of the object rather than the object itself.</span></span>|  
|`COR_PRF_GC_ROOT_REFCOUNTED`|<span data-ttu-id="12cef-111">La racine empêche le garbage collection si le décompte de références de l’objet est une certaine valeur.</span><span class="sxs-lookup"><span data-stu-id="12cef-111">The root prevents garbage collection if the reference count of the object is a certain value.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="12cef-112">Notes</span><span class="sxs-lookup"><span data-stu-id="12cef-112">Remarks</span></span>  
 <span data-ttu-id="12cef-113">`COR_PRF_GC_ROOT_FLAGS` est un masque de bits qui fournit des informations supplémentaires à propos des racines spéciales.</span><span class="sxs-lookup"><span data-stu-id="12cef-113">`COR_PRF_GC_ROOT_FLAGS` is a bitmask that provides additional information about special roots.</span></span> <span data-ttu-id="12cef-114">Toutefois, pas toutes les racines sont spéciales.</span><span class="sxs-lookup"><span data-stu-id="12cef-114">However, not all roots are special.</span></span> <span data-ttu-id="12cef-115">Par exemple, certaines racines ne sont pas des références faibles, des pointeurs intérieurs, épinglés ou comptés par référence.</span><span class="sxs-lookup"><span data-stu-id="12cef-115">For example, some roots are not weak references, interior pointers, pinned, or reference-counted.</span></span> <span data-ttu-id="12cef-116">Pour de telles racines, il n’existe aucun indicateur pour transmettre.</span><span class="sxs-lookup"><span data-stu-id="12cef-116">For such roots, there are no flags to convey.</span></span> <span data-ttu-id="12cef-117">Par conséquent, les méthodes qui utilisent cette énumération, telles que la [ICorProfilerCallback2::RootReferences2](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-rootreferences2-method.md) méthode, envoi 0 pour le masque de bits d’indicateurs, indiquant que tous les indicateurs sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="12cef-117">Therefore, methods that use this enumeration, such as the [ICorProfilerCallback2::RootReferences2](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-rootreferences2-method.md) method, send 0 for the flags bitmask, indicating that all flags are turned off.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="12cef-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12cef-118">Requirements</span></span>  
 <span data-ttu-id="12cef-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="12cef-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="12cef-120">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="12cef-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="12cef-121">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="12cef-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="12cef-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="12cef-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="12cef-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12cef-123">See also</span></span>

- [<span data-ttu-id="12cef-124">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="12cef-124">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
