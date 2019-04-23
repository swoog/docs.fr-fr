---
title: ICorProfilerInfo::SetEnterLeaveFunctionHooks, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.SetEnterLeaveFunctionHooks
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::SetEnterLeaveFunctionHooks
helpviewer_keywords:
- SetEnterLeaveFunctionHooks method [.NET Framework profiling]
- ICorProfilerInfo::SetEnterLeaveFunctionHooks method [.NET Framework profiling]
ms.assetid: 72399636-c219-4ffd-8ac8-39432c9d4641
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a2d45e98f3e7b71375b14c43c4bff4929bc79494
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59142530"
---
# <a name="icorprofilerinfosetenterleavefunctionhooks-method"></a><span data-ttu-id="c49e5-102">ICorProfilerInfo::SetEnterLeaveFunctionHooks, méthode</span><span class="sxs-lookup"><span data-stu-id="c49e5-102">ICorProfilerInfo::SetEnterLeaveFunctionHooks Method</span></span>
<span data-ttu-id="c49e5-103">Spécifie les fonctions implémentées par le profileur à être appelée sur « entrée », « quitter » et « tailcall » de fonctions managées.</span><span class="sxs-lookup"><span data-stu-id="c49e5-103">Specifies profiler-implemented functions to be called on "enter", "leave", and "tailcall" hooks of managed functions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c49e5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c49e5-104">Syntax</span></span>  
  
```  
HRESULT SetEnterLeaveFunctionHooks(  
    [in] FunctionEnter    *pFuncEnter,  
    [in] FunctionLeave    *pFuncLeave,  
    [in] FunctionTailcall *pFuncTailcall);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c49e5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c49e5-105">Parameters</span></span>  
 `pFuncEnter`  
 <span data-ttu-id="c49e5-106">[in] Un pointeur vers l’implémentation à utiliser comme la [FunctionEnter](../../../../docs/framework/unmanaged-api/profiling/functionenter-function.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="c49e5-106">[in] A pointer to the implementation to be used as the [FunctionEnter](../../../../docs/framework/unmanaged-api/profiling/functionenter-function.md) callback.</span></span>  
  
 `pFuncLeave`  
 <span data-ttu-id="c49e5-107">[in] Un pointeur vers l’implémentation à utiliser comme la [FunctionLeave](../../../../docs/framework/unmanaged-api/profiling/functionleave-function.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="c49e5-107">[in] A pointer to the implementation to be used as the [FunctionLeave](../../../../docs/framework/unmanaged-api/profiling/functionleave-function.md) callback.</span></span>  
  
 `pFuncTailcall`  
 <span data-ttu-id="c49e5-108">[in] Un pointeur vers l’implémentation à utiliser comme la [FunctionTailcall](../../../../docs/framework/unmanaged-api/profiling/functiontailcall-function.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="c49e5-108">[in] A pointer to the implementation to be used as the [FunctionTailcall](../../../../docs/framework/unmanaged-api/profiling/functiontailcall-function.md) callback.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c49e5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c49e5-109">Remarks</span></span>  
 <span data-ttu-id="c49e5-110">Dans le .NET Framework version 1.0, chaque pointeur fonction peut être null pour désactiver ce rappel correspondant.</span><span class="sxs-lookup"><span data-stu-id="c49e5-110">In the .NET Framework version 1.0, each function pointer can be null to disable that corresponding callback.</span></span>  
  
 <span data-ttu-id="c49e5-111">Qu’un seul jeu de rappels peut être actif à la fois.</span><span class="sxs-lookup"><span data-stu-id="c49e5-111">Only one set of callbacks can be active at a time.</span></span> <span data-ttu-id="c49e5-112">Par conséquent, si un profileur appelle `SetEnterLeaveFunctionHooks` et [ICorProfilerInfo2::SetEnterLeaveFunctionHooks2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md), puis `SetEnterLeaveFunctionHooks2` est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="c49e5-112">Thus, if a profiler calls both `SetEnterLeaveFunctionHooks` and [ICorProfilerInfo2::SetEnterLeaveFunctionHooks2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md), then `SetEnterLeaveFunctionHooks2` takes precedence.</span></span>  
  
 <span data-ttu-id="c49e5-113">Le `SetEnterLeaveFunctionHooks` méthode peut être appelée uniquement à partir du profileur [ICorProfilerCallback::Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="c49e5-113">The `SetEnterLeaveFunctionHooks` method can be called only from the profiler's [ICorProfilerCallback::Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c49e5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c49e5-114">Requirements</span></span>  
 <span data-ttu-id="c49e5-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c49e5-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c49e5-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c49e5-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c49e5-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c49e5-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c49e5-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c49e5-118">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c49e5-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c49e5-119">See also</span></span>

- [<span data-ttu-id="c49e5-120">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="c49e5-120">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
