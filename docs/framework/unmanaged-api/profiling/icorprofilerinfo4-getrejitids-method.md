---
title: ICorProfilerInfo4::GetReJITIDs, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.GetReJITIDs
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::GetReJITIDs
helpviewer_keywords:
- GetReJITIDs method, ICorProfilerInfo4 interface [.NET Framework profiling]
- ICorProfilerInfo4::GetReJITIDs method [.NET Framework profiling]
ms.assetid: 634ac28c-a5b7-4fc3-af84-256c24ca8177
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9d2d48e5fb070ec0334de579d2e28146177a87b1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59121613"
---
# <a name="icorprofilerinfo4getrejitids-method"></a><span data-ttu-id="d0466-102">ICorProfilerInfo4::GetReJITIDs, méthode</span><span class="sxs-lookup"><span data-stu-id="d0466-102">ICorProfilerInfo4::GetReJITIDs Method</span></span>
<span data-ttu-id="d0466-103">Retourne un tableau d’ID qui identifient tous les-recompilée juste les versions de la fonction spécifiée qui sont toujours allouées.</span><span class="sxs-lookup"><span data-stu-id="d0466-103">Returns an array of IDs that identify all JIT-recompiled versions of the specified function that are still allocated.</span></span> <span data-ttu-id="d0466-104">Cela inclut-recompilée juste les versions de fonctions qui ont été annulées par la suite, mais pas encore libérées (par exemple, lorsque le domaine d’application qui contient la fonction de restauration est en cours d’utilisation).</span><span class="sxs-lookup"><span data-stu-id="d0466-104">This includes JIT-recompiled versions of functions that have been subsequently reverted but not yet freed (for example, when the application domain that contains the reverted function is still in use).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d0466-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0466-105">Syntax</span></span>  
  
```  
HRESULT GetReJITIDs (  
     [in]  FunctionID          functionId,  
     [in]  ULONG               cReJitIds,  
     [out] ULONG *             pcReJitIds,  
     [out, size_is(cReJitIds), length_is(*pcReJitIds)]   ReJITID        reJitIds[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d0466-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0466-106">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="d0466-107">[in] Le `FunctionID` de l’instance de fonction pour lequel énumérer des versions.</span><span class="sxs-lookup"><span data-stu-id="d0466-107">[in] The `FunctionID` of the function instance for which to enumerate versions.</span></span>  
  
 `cReJitIds`  
 <span data-ttu-id="d0466-108">[in] Le nombre d’ID recompilée juste alloués dans le `reJitIds` tableau.</span><span class="sxs-lookup"><span data-stu-id="d0466-108">[in] The number of JIT-recompiled IDs allocated in the `reJitIds` array.</span></span>  
  
 `pcReJitIds`  
 <span data-ttu-id="d0466-109">[out] Le nombre réel d’ID recompilé de JIT.</span><span class="sxs-lookup"><span data-stu-id="d0466-109">[out] The actual number of JIT-recompiled IDs.</span></span>  
  
 `reJitIds`  
 <span data-ttu-id="d0466-110">[out] Tableau alloué par l’appelant qui contiendra les ID recompilée juste pour la fonction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d0466-110">[out] A caller-allocated array that will contain the JIT-recompiled IDs for the specified function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d0466-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d0466-111">Remarks</span></span>  
 `GetReJITIDs` <span data-ttu-id="d0466-112">énumère les ID recompilée juste actives pour une instance de la fonction donnée.</span><span class="sxs-lookup"><span data-stu-id="d0466-112">enumerates the active JIT-recompiled IDs for a given function instance.</span></span> <span data-ttu-id="d0466-113">Il suit le même modèle d’utilisation en tant qu’autre `ICorProfilerInfo` fonctions qui acceptent les mémoires tampons allouées par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="d0466-113">It follows the same usage pattern as other `ICorProfilerInfo` functions that accept caller-allocated buffers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d0466-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0466-114">Requirements</span></span>  
 <span data-ttu-id="d0466-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d0466-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d0466-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d0466-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d0466-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d0466-117">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="d0466-118">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="d0466-118">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="d0466-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0466-119">See also</span></span>

- [<span data-ttu-id="d0466-120">ICorProfilerInfo4, interface</span><span class="sxs-lookup"><span data-stu-id="d0466-120">ICorProfilerInfo4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)
- [<span data-ttu-id="d0466-121">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="d0466-121">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="d0466-122">Profilage</span><span class="sxs-lookup"><span data-stu-id="d0466-122">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
