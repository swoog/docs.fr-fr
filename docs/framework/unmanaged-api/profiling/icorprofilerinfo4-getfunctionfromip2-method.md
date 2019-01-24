---
title: ICorProfilerInfo4::GetFunctionFromIP2, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.GetFunctionFromIP2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::GetFunctionFromIP2
helpviewer_keywords:
- ICorProfilerInfo4::GetFunctionFromIP2 method [.NET Framework profiling]
- GetFunctionFromIP2 method, ICorProfilerInfo4 interface [.NET Framework profiling]
ms.assetid: 46ff70f4-13e9-40a0-802a-0a40abcfc6a0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bded97c23013e60bf2d3c32c4eb25285870977e1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54554190"
---
# <a name="icorprofilerinfo4getfunctionfromip2-method"></a><span data-ttu-id="0ea9b-102">ICorProfilerInfo4::GetFunctionFromIP2, méthode</span><span class="sxs-lookup"><span data-stu-id="0ea9b-102">ICorProfilerInfo4::GetFunctionFromIP2 Method</span></span>
<span data-ttu-id="0ea9b-103">Mappe un pointeur d’instruction de code managé vers la version recompilée au juste d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-103">Maps a managed code instruction pointer to the JIT-recompiled version of a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ea9b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ea9b-104">Syntax</span></span>  
  
```  
HRESULT GetFunctionFromIP2(  
    [in]  LPCBYTE    ip,  
    [out] FunctionID *pFunctionId,  
    [out] ReJITID *pReJitId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0ea9b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ea9b-105">Parameters</span></span>  
 `ip`  
 <span data-ttu-id="0ea9b-106">[in] Le pointeur d’instruction dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-106">[in] The instruction pointer in managed code.</span></span>  
  
 `pFunctionId`  
 <span data-ttu-id="0ea9b-107">[out] L’ID de fonction.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-107">[out] The function ID.</span></span>  
  
 `pReJitId`  
 <span data-ttu-id="0ea9b-108">[out] L’identité de la version recompilée au juste de la fonction.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-108">[out] The identity of the JIT-recompiled version of the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0ea9b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0ea9b-109">Remarks</span></span>  
 <span data-ttu-id="0ea9b-110">`GetFunctionFromIP2` est similaire à `GetFunctionFromIP`, sauf qu’il obtient l’ID recompilé de JIT au lieu de l’ID de la fonction de la fonction qui contient l’adresse IP spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-110">`GetFunctionFromIP2` is similar to `GetFunctionFromIP`, except that it gets the JIT-recompiled ID instead of the function ID of the function that contains the specified IP address.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0ea9b-111">`GetFunctionFromIP2` peut déclencher un garbage collection, tandis que `GetFunctionFromIP` ne sera pas.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-111">`GetFunctionFromIP2` can trigger a garbage collection, whereas `GetFunctionFromIP` will not.</span></span>  <span data-ttu-id="0ea9b-112">Pour plus d’informations, consultez [CORPROF_E_UNSUPPORTED_CALL_SEQUENCE HRESULT](../../../../docs/framework/unmanaged-api/profiling/corprof-e-unsupported-call-sequence-hresult.md).</span><span class="sxs-lookup"><span data-stu-id="0ea9b-112">For more information, see [CORPROF_E_UNSUPPORTED_CALL_SEQUENCE HRESULT](../../../../docs/framework/unmanaged-api/profiling/corprof-e-unsupported-call-sequence-hresult.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0ea9b-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0ea9b-113">Requirements</span></span>  
 <span data-ttu-id="0ea9b-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0ea9b-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0ea9b-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="0ea9b-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="0ea9b-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0ea9b-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0ea9b-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0ea9b-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ea9b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ea9b-118">See also</span></span>
- [<span data-ttu-id="0ea9b-119">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="0ea9b-119">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
