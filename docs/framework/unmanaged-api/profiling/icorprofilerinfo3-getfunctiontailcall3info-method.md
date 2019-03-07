---
title: ICorProfilerInfo3::GetFunctionTailcall3Info, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.GetFunctionTailcall3Info Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::GetFunctionTailcall3Info
helpviewer_keywords:
- ICorProfilerInfo3::GetFunctionTailcall3Info method [.NET Framework profiling]
- GetFunctionTailcall3Info method [.NET Framework profiling]
ms.assetid: afdb5ac9-5bf5-4b91-b7cb-f81db23d7da3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b3d5d3808f51f921bd3e0c94942a1fb07a35d876
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57487809"
---
# <a name="icorprofilerinfo3getfunctiontailcall3info-method"></a><span data-ttu-id="1772f-102">ICorProfilerInfo3::GetFunctionTailcall3Info, méthode</span><span class="sxs-lookup"><span data-stu-id="1772f-102">ICorProfilerInfo3::GetFunctionTailcall3Info Method</span></span>
<span data-ttu-id="1772f-103">Fournit le frame de pile de la fonction signalée au profileur par la [FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="1772f-103">Provides the stack frame of the function that is being reported to the profiler by the [FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md) function.</span></span> <span data-ttu-id="1772f-104">Cette méthode peut être appelée uniquement pendant le rappel de `FunctionTailcall3WithInfo`.</span><span class="sxs-lookup"><span data-stu-id="1772f-104">This method can be called only during the `FunctionTailcall3WithInfo` callback.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1772f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1772f-105">Syntax</span></span>  
  
```  
HRESULT GetFunctionTailcall3Info(   
            [in]  FunctionID functionId,   
            [in]  COR_PRF_ELT_INFO eltInfo,  
            [out] COR_PRF_FRAME_INFO *pFrameInfo);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1772f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1772f-106">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="1772f-107">[in] Le `FunctionID` de la fonction qui retourne.</span><span class="sxs-lookup"><span data-stu-id="1772f-107">[in] The `FunctionID` of the function that is returning.</span></span>  
  
 `eltInfo`  
 <span data-ttu-id="1772f-108">[in] Handle opaque qui représente des informations sur un frame de pile donné.</span><span class="sxs-lookup"><span data-stu-id="1772f-108">[in] An opaque handle that represents information about a given stack frame.</span></span> <span data-ttu-id="1772f-109">Le profileur doit fournir les mêmes `eltInfo` qui a été donné au profileur par la `FunctionTailcall3WithInfo` (fonction).</span><span class="sxs-lookup"><span data-stu-id="1772f-109">The profiler should provide the same `eltInfo` that was given to the profiler by the `FunctionTailcall3WithInfo` function.</span></span>  
  
 `pFrameInfo`  
 <span data-ttu-id="1772f-110">[out] Handle opaque qui représente des informations génériques sur un frame de pile donné.</span><span class="sxs-lookup"><span data-stu-id="1772f-110">[out] An opaque handle that represents generics information about a given stack frame.</span></span> <span data-ttu-id="1772f-111">Ce handle est uniquement valide pendant le rappel `FunctionTailcall3WithInfo` au cours duquel le profileur a appelé la méthode `GetFunctionTailcall3Info`.</span><span class="sxs-lookup"><span data-stu-id="1772f-111">This handle is valid only during the `FunctionTailcall3WithInfo` callback in which the profiler called the `GetFunctionTailcall3Info` method.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1772f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1772f-112">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1772f-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1772f-113">Requirements</span></span>  
 <span data-ttu-id="1772f-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1772f-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1772f-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="1772f-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="1772f-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1772f-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1772f-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1772f-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1772f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1772f-118">See also</span></span>
- [<span data-ttu-id="1772f-119">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="1772f-119">FunctionEnter3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md)
- [<span data-ttu-id="1772f-120">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="1772f-120">FunctionLeave3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md)
- [<span data-ttu-id="1772f-121">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="1772f-121">FunctionTailcall3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md)
- [<span data-ttu-id="1772f-122">ICorProfilerInfo3, interface</span><span class="sxs-lookup"><span data-stu-id="1772f-122">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)
- [<span data-ttu-id="1772f-123">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="1772f-123">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="1772f-124">Profilage</span><span class="sxs-lookup"><span data-stu-id="1772f-124">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
