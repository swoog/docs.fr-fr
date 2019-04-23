---
title: ICorProfilerInfo3::SetEnterLeaveFunctionHooks3, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.SetEnterLeaveFunctionHooks3 Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::SetEnterLeaveFunctionHooks3
helpviewer_keywords:
- SetEnterLeaveFunctionHooks3 method [.NET Framework profiling]
- ICorProfilerInfo3::SetEnterLeaveFunctionHooks3 method [.NET Framework profiling]
ms.assetid: f0621465-b84f-40ab-a4e5-56a7abc776a7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 73321a28b1c61775d08e2c60ee2b9a863b8250dd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59121678"
---
# <a name="icorprofilerinfo3setenterleavefunctionhooks3-method"></a><span data-ttu-id="e5e01-102">ICorProfilerInfo3::SetEnterLeaveFunctionHooks3, méthode</span><span class="sxs-lookup"><span data-stu-id="e5e01-102">ICorProfilerInfo3::SetEnterLeaveFunctionHooks3 Method</span></span>
<span data-ttu-id="e5e01-103">Spécifie les fonctions implémentées par le profileur qui seront appelées sur le [FunctionEnter3](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md), [FunctionLeave3](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md), et [FunctionTailcall3](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md) fonctions.</span><span class="sxs-lookup"><span data-stu-id="e5e01-103">Specifies the profiler-implemented functions that will be called on the [FunctionEnter3](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md), [FunctionLeave3](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md), and [FunctionTailcall3](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md) functions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5e01-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5e01-104">Syntax</span></span>  
  
```  
HRESULT SetEnterLeaveFunctionHooks3(  
            [in] FunctionEnter3    *pFuncEnter3,  
            [in] FunctionLeave3    *pFuncLeave3,  
            [in] FunctionTailcall3 *pFuncTailcall3);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e5e01-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5e01-105">Parameters</span></span>  
 `pFuncEnter3`  
 <span data-ttu-id="e5e01-106">[in] Un pointeur vers l’implémentation à utiliser comme la `FunctionEnter3` rappel.</span><span class="sxs-lookup"><span data-stu-id="e5e01-106">[in] A pointer to the implementation to be used as the `FunctionEnter3` callback.</span></span>  
  
 `pFuncLeave3`  
 <span data-ttu-id="e5e01-107">[in] Un pointeur vers l’implémentation à utiliser comme la `FunctionLeave3` rappel.</span><span class="sxs-lookup"><span data-stu-id="e5e01-107">[in] A pointer to the implementation to be used as the `FunctionLeave3` callback.</span></span>  
  
 `pFuncTailcall3`  
 <span data-ttu-id="e5e01-108">[in] Un pointeur vers l’implémentation à utiliser comme la `FunctionTailcall3` rappel.</span><span class="sxs-lookup"><span data-stu-id="e5e01-108">[in] A pointer to the implementation to be used as the `FunctionTailcall3` callback.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e5e01-109">Notes</span><span class="sxs-lookup"><span data-stu-id="e5e01-109">Remarks</span></span>  
 <span data-ttu-id="e5e01-110">[FunctionEnter3](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md), [FunctionLeave3](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md), et [FunctionTailcall3](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md) ne fournissent pas inspection de frame et de l’argument de pile.</span><span class="sxs-lookup"><span data-stu-id="e5e01-110">[FunctionEnter3](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md), [FunctionLeave3](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md), and [FunctionTailcall3](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md) hooks do not provide stack frame and argument inspection.</span></span> <span data-ttu-id="e5e01-111">Pour accéder à ces informations, le `COR_PRF_ENABLE_FUNCTION_ARGS`, `COR_PRF_ENABLE_FUNCTION_RETVAL`, et/ou `COR_PRF_ENABLE_FRAME_INFO` indicateurs doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="e5e01-111">To access that information, the `COR_PRF_ENABLE_FUNCTION_ARGS`, `COR_PRF_ENABLE_FUNCTION_RETVAL`, and/or  `COR_PRF_ENABLE_FRAME_INFO` flags have to be set.</span></span> <span data-ttu-id="e5e01-112">Le profileur peut utiliser le [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) méthode pour définir les indicateurs d’événement, puis utiliser le [ICorProfilerInfo3::SetEnterLeaveFunctionHooks3WithInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3withinfo-method.md) méthode pour inscrire votre implémentation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="e5e01-112">The profiler can use the [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) method to set the event flags, and then use the [ICorProfilerInfo3::SetEnterLeaveFunctionHooks3WithInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3withinfo-method.md) method to register your implementation of this function.</span></span>  
  
 <span data-ttu-id="e5e01-113">Qu’un seul jeu de rappels peut être actif à la fois, et la version la plus récente est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="e5e01-113">Only one set of callbacks may be active at a time, and the newest version takes precedence.</span></span> <span data-ttu-id="e5e01-114">Par conséquent, si un profileur appelle la [SetEnterLeaveFunctionHooks2, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md) et `SetEnterLeaveFunctionHooks3` (méthode), `SetEnterLeaveFunctionHooks3` est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e5e01-114">Therefore, if a profiler calls both the [SetEnterLeaveFunctionHooks2 Method](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md) and the `SetEnterLeaveFunctionHooks3` method, `SetEnterLeaveFunctionHooks3` is used.</span></span>  
  
 <span data-ttu-id="e5e01-115">Le `SetEnterLeaveFunctionHooks3` méthode peut être appelée uniquement à partir du profileur [ICorProfilerCallback::Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="e5e01-115">The `SetEnterLeaveFunctionHooks3` method may be called only from the profiler's [ICorProfilerCallback::Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5e01-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5e01-116">Requirements</span></span>  
 <span data-ttu-id="e5e01-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e5e01-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5e01-118">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e5e01-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e5e01-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e5e01-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e5e01-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5e01-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5e01-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5e01-121">See also</span></span>

- [<span data-ttu-id="e5e01-122">SetEnterLeaveFunctionHooks3WithInfo</span><span class="sxs-lookup"><span data-stu-id="e5e01-122">SetEnterLeaveFunctionHooks3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3withinfo-method.md)
- [<span data-ttu-id="e5e01-123">FunctionEnter3</span><span class="sxs-lookup"><span data-stu-id="e5e01-123">FunctionEnter3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md)
- [<span data-ttu-id="e5e01-124">FunctionLeave3</span><span class="sxs-lookup"><span data-stu-id="e5e01-124">FunctionLeave3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md)
- [<span data-ttu-id="e5e01-125">FunctionTailcall3</span><span class="sxs-lookup"><span data-stu-id="e5e01-125">FunctionTailcall3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md)
- [<span data-ttu-id="e5e01-126">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="e5e01-126">FunctionEnter3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md)
- [<span data-ttu-id="e5e01-127">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="e5e01-127">FunctionLeave3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md)
- [<span data-ttu-id="e5e01-128">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="e5e01-128">FunctionTailcall3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md)
- [<span data-ttu-id="e5e01-129">Fonctions statiques globales de profilage</span><span class="sxs-lookup"><span data-stu-id="e5e01-129">Profiling Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
- [<span data-ttu-id="e5e01-130">ICorProfilerInfo3</span><span class="sxs-lookup"><span data-stu-id="e5e01-130">ICorProfilerInfo3</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)
- [<span data-ttu-id="e5e01-131">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="e5e01-131">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="e5e01-132">Profilage</span><span class="sxs-lookup"><span data-stu-id="e5e01-132">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
