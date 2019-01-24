---
title: ICorProfilerInfo3::EnumJITedFunctions, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.EnumJITedFunctions Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::EnumJITedFunctions
helpviewer_keywords:
- ICorProfilerInfo3::EnumJITedFunctions method [.NET Framework profiling]
- EnumJITedFunctions method [.NET Framework profiling]
ms.assetid: e2847a36-f460-45e2-9b6c-b33b008f40d9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 12f5930fb6d4e149653bc29d2f36b0df72c71447
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498828"
---
# <a name="icorprofilerinfo3enumjitedfunctions-method"></a><span data-ttu-id="7da87-102">ICorProfilerInfo3::EnumJITedFunctions, méthode</span><span class="sxs-lookup"><span data-stu-id="7da87-102">ICorProfilerInfo3::EnumJITedFunctions Method</span></span>
<span data-ttu-id="7da87-103">Retourne un énumérateur pour toutes les fonctions qui ont été précédemment compilé par JIT.</span><span class="sxs-lookup"><span data-stu-id="7da87-103">Returns an enumerator for all functions that were previously JIT-compiled.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7da87-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7da87-104">Syntax</span></span>  
  
```  
HRESULT EnumJITedFunctions([out] ICorProfilerFunctionEnum** ppEnum);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7da87-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7da87-105">Parameters</span></span>  
 `ppEnum`  
 <span data-ttu-id="7da87-106">[out] Un pointeur vers le [ICorProfilerFunctionEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctionenum-interface.md) énumérateur.</span><span class="sxs-lookup"><span data-stu-id="7da87-106">[out] A pointer to the [ICorProfilerFunctionEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctionenum-interface.md) enumerator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7da87-107">Notes</span><span class="sxs-lookup"><span data-stu-id="7da87-107">Remarks</span></span>  
 <span data-ttu-id="7da87-108">Cette méthode peut se chevaucher avec `JITCompilation` rappels comme le [ICorProfilerCallback::JITCompilationStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-jitcompilationstarted-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="7da87-108">This method may overlap with `JITCompilation` callbacks such as the [ICorProfilerCallback::JITCompilationStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-jitcompilationstarted-method.md) method.</span></span> <span data-ttu-id="7da87-109">L’énumérateur retourné par cette méthode n’inclut pas les fonctions qui sont chargées à partir d’images natives générées avec Ngen.exe.</span><span class="sxs-lookup"><span data-stu-id="7da87-109">The enumerator returned by this method does not include functions that are loaded from native images generated with Ngen.exe.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7da87-110">L’énumération retournée inclut uniquement « 0 » pour la valeur de la `COR_PRF_FUNCTION::reJitId` champ.</span><span class="sxs-lookup"><span data-stu-id="7da87-110">The returned enumeration includes only "0" for the value of the `COR_PRF_FUNCTION::reJitId` field.</span></span>  <span data-ttu-id="7da87-111">Si vous avez besoin valide `COR_PRF_FUNCTION::reJitId` valeurs, utilisez le [ICorProfilerInfo4::EnumJITedFunctions2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-enumjitedfunctions2-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="7da87-111">If you require valid `COR_PRF_FUNCTION::reJitId` values, use the [ICorProfilerInfo4::EnumJITedFunctions2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-enumjitedfunctions2-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7da87-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7da87-112">Requirements</span></span>  
 <span data-ttu-id="7da87-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7da87-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7da87-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7da87-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7da87-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7da87-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7da87-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7da87-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7da87-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7da87-117">See also</span></span>
- [<span data-ttu-id="7da87-118">ICorProfilerInfo3, interface</span><span class="sxs-lookup"><span data-stu-id="7da87-118">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)
- [<span data-ttu-id="7da87-119">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="7da87-119">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="7da87-120">Profilage</span><span class="sxs-lookup"><span data-stu-id="7da87-120">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
