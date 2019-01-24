---
title: ICorProfilerInfo3::SetEnterLeaveFunctionHooks3WithInfo, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.SetEnterLeaveFunctionHooks3WithInfo Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::SetEnterLeaveFunctionHooks3WithInfo
helpviewer_keywords:
- SetEnterLeaveFunctionHooks3WithInfo method [.NET Framework profiling]
- ICorProfilerInfo3::SetEnterLeaveFunctionHooks3WithInfo method [.NET Framework profiling]
ms.assetid: ca8ea534-e441-47b8-be85-466410988c0a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9e5ba0fac05bcab12abccd224b14e504a33b64a8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54746232"
---
# <a name="icorprofilerinfo3setenterleavefunctionhooks3withinfo-method"></a><span data-ttu-id="e3cc8-102">ICorProfilerInfo3::SetEnterLeaveFunctionHooks3WithInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="e3cc8-102">ICorProfilerInfo3::SetEnterLeaveFunctionHooks3WithInfo Method</span></span>
<span data-ttu-id="e3cc8-103">Spécifie les fonctions implémentées par le profileur qui seront appelées sur le [FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md), [FunctionLeave3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md), et [FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md) raccordements de fonctions managées.</span><span class="sxs-lookup"><span data-stu-id="e3cc8-103">Specifies the profiler-implemented functions that will be called on the [FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md), [FunctionLeave3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md), and [FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md) hooks of managed functions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3cc8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3cc8-104">Syntax</span></span>  
  
```  
HRESULT SetEnterLeaveFunctionHooks3WithInfo(  
            [in] FunctionEnter3WithInfo    *pFuncEnter3,  
            [in] FunctionLeave3withInfo    *pFuncLeave3,  
            [in] FunctionTailcall3WithInfo *pFuncTailcall3);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e3cc8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3cc8-105">Parameters</span></span>  
 `pFuncEnter3`  
 <span data-ttu-id="e3cc8-106">[in] Un pointeur vers l’implémentation à utiliser comme la `FunctionEnter3WithInfo` rappel.</span><span class="sxs-lookup"><span data-stu-id="e3cc8-106">[in] A pointer to the implementation to be used as the `FunctionEnter3WithInfo` callback.</span></span>  
  
 `pFuncLeave3`  
 <span data-ttu-id="e3cc8-107">[in] Un pointeur vers l’implémentation à utiliser comme la `FunctionLeave3WithInfo` rappel.</span><span class="sxs-lookup"><span data-stu-id="e3cc8-107">[in] A pointer to the implementation to be used as the `FunctionLeave3WithInfo` callback.</span></span>  
  
 `pFuncTailcall3`  
 <span data-ttu-id="e3cc8-108">[in] Un pointeur vers l’implémentation à utiliser comme la `FunctionTailcall3WithInfo` rappel.</span><span class="sxs-lookup"><span data-stu-id="e3cc8-108">[in] A pointer to the implementation to be used as the `FunctionTailcall3WithInfo` callback.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e3cc8-109">Notes</span><span class="sxs-lookup"><span data-stu-id="e3cc8-109">Remarks</span></span>  
 <span data-ttu-id="e3cc8-110">Le [FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md), [FunctionLeave3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md), et [FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md) fournissent inspection de frame et de l’argument de pile.</span><span class="sxs-lookup"><span data-stu-id="e3cc8-110">The [FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md), [FunctionLeave3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md), and [FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md) hooks provide stack frame and argument inspection.</span></span> <span data-ttu-id="e3cc8-111">Pour accéder à ces informations, le `COR_PRF_ENABLE_FUNCTION_ARGS`, `COR_PRF_ENABLE_FUNCTION_RETVAL`, et/ou `COR_PRF_ENABLE_FRAME_INFO` indicateurs doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="e3cc8-111">To access that information, the `COR_PRF_ENABLE_FUNCTION_ARGS`, `COR_PRF_ENABLE_FUNCTION_RETVAL`, and/or `COR_PRF_ENABLE_FRAME_INFO` flags have to be set.</span></span> <span data-ttu-id="e3cc8-112">Le profileur peut utiliser le [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) méthode pour définir les indicateurs d’événement, puis utiliser le `SetEnterLeaveFunctionHooks3WithInfo` méthode pour enregistrer votre implémentation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="e3cc8-112">The profiler can use the [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) method to set the event flags, and then use the `SetEnterLeaveFunctionHooks3WithInfo` method to register your implementation of this function.</span></span>  
  
 <span data-ttu-id="e3cc8-113">Qu’un seul jeu de rappels peut être actif à la fois, et la version la plus récente est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="e3cc8-113">Only one set of callbacks may be active at a time, and the newest version takes precedence.</span></span> <span data-ttu-id="e3cc8-114">Par conséquent, si un profileur appelle [SetEnterLeaveFunctionHooks2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md) et `SetEnterLeaveFunctionHooks3WithInfo`, `SetEnterLeaveFunctionHooks3WithInfo` est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e3cc8-114">Therefore, if a profiler calls both [SetEnterLeaveFunctionHooks2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md) and `SetEnterLeaveFunctionHooks3WithInfo`, `SetEnterLeaveFunctionHooks3WithInfo` is used.</span></span>  
  
 <span data-ttu-id="e3cc8-115">Le `SetEnterLeaveFunctionHooks3WithInfo` méthode peut être appelée uniquement à partir du profileur [ICorProfilerCallback::Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="e3cc8-115">The `SetEnterLeaveFunctionHooks3WithInfo` method may be called only from the profiler's [ICorProfilerCallback::Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e3cc8-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e3cc8-116">Requirements</span></span>  
 <span data-ttu-id="e3cc8-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e3cc8-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e3cc8-118">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e3cc8-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e3cc8-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e3cc8-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e3cc8-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e3cc8-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3cc8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3cc8-121">See also</span></span>
- [<span data-ttu-id="e3cc8-122">SetEnterLeaveFunctionHooks3</span><span class="sxs-lookup"><span data-stu-id="e3cc8-122">SetEnterLeaveFunctionHooks3</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3-method.md)
- [<span data-ttu-id="e3cc8-123">FunctionEnter3</span><span class="sxs-lookup"><span data-stu-id="e3cc8-123">FunctionEnter3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md)
- [<span data-ttu-id="e3cc8-124">FunctionLeave3</span><span class="sxs-lookup"><span data-stu-id="e3cc8-124">FunctionLeave3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md)
- [<span data-ttu-id="e3cc8-125">FunctionTailcall3</span><span class="sxs-lookup"><span data-stu-id="e3cc8-125">FunctionTailcall3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md)
- [<span data-ttu-id="e3cc8-126">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="e3cc8-126">FunctionEnter3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md)
- [<span data-ttu-id="e3cc8-127">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="e3cc8-127">FunctionLeave3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md)
- [<span data-ttu-id="e3cc8-128">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="e3cc8-128">FunctionTailcall3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md)
- [<span data-ttu-id="e3cc8-129">Fonctions statiques globales de profilage</span><span class="sxs-lookup"><span data-stu-id="e3cc8-129">Profiling Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
- [<span data-ttu-id="e3cc8-130">ICorProfilerInfo3, interface</span><span class="sxs-lookup"><span data-stu-id="e3cc8-130">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)
- [<span data-ttu-id="e3cc8-131">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="e3cc8-131">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="e3cc8-132">Profilage</span><span class="sxs-lookup"><span data-stu-id="e3cc8-132">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
