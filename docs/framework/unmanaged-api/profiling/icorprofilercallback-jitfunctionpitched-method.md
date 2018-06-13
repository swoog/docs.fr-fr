---
title: ICorProfilerCallback::JITFunctionPitched, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.JITFunctionPitched
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::JITFunctionPitched
helpviewer_keywords:
- JITFunctionPitched method [.NET Framework profiling]
- ICorProfilerCallback::JITFunctionPitched method [.NET Framework profiling]
ms.assetid: 116085df-7a77-404a-afac-d0557a12b986
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cf51d2a0e7381cd495da8f3846302ec806c34774
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33451410"
---
# <a name="icorprofilercallbackjitfunctionpitched-method"></a><span data-ttu-id="003e2-102">ICorProfilerCallback::JITFunctionPitched, méthode</span><span class="sxs-lookup"><span data-stu-id="003e2-102">ICorProfilerCallback::JITFunctionPitched Method</span></span>
<span data-ttu-id="003e2-103">Notifie le profileur qui une fonction qui a été juste-à-temps (JIT)-compilé a été supprimé de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="003e2-103">Notifies the profiler that a function that has been just-in-time (JIT)-compiled has been removed from memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="003e2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="003e2-104">Syntax</span></span>  
  
```  
HRESULT JITFunctionPitched(  
    [in] FunctionID functionId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="003e2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="003e2-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="003e2-106">[in] L’ID de la fonction qui a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="003e2-106">[in] The ID of the function that was removed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="003e2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="003e2-107">Remarks</span></span>  
 <span data-ttu-id="003e2-108">Si la fonction supprimée est appelée, le profileur reçoit les nouveaux événements de compilation JIT lorsque la fonction est recompilée.</span><span class="sxs-lookup"><span data-stu-id="003e2-108">If the removed function is called, the profiler will receive new JIT-compilation events when the function is recompiled.</span></span> <span data-ttu-id="003e2-109">Actuellement, compilateur JIT common language runtime (CLR) ne supprime pas les fonctions de la mémoire, ce rappel n’est actuellement pas utilisé et n’est pas reçu par le profileur.</span><span class="sxs-lookup"><span data-stu-id="003e2-109">Currently, the common language runtime (CLR) JIT compiler does not remove functions from memory, so this callback is currently not used and will not be received by the profiler.</span></span>  
  
 <span data-ttu-id="003e2-110">La valeur de `functionId` n’est pas valide tant que la fonction est recompilée.</span><span class="sxs-lookup"><span data-stu-id="003e2-110">The value of `functionId` is not valid until the function is recompiled.</span></span> <span data-ttu-id="003e2-111">Lorsque la fonction est recompilée, la même `functionId` valeur sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="003e2-111">When the function is recompiled, the same `functionId` value will be used.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="003e2-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="003e2-112">Requirements</span></span>  
 <span data-ttu-id="003e2-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="003e2-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="003e2-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="003e2-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="003e2-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="003e2-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="003e2-116">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="003e2-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="003e2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="003e2-117">See Also</span></span>  
 [<span data-ttu-id="003e2-118">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="003e2-118">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
