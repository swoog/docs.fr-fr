---
title: FunctionLeave2 (fonction)
ms.date: 03/30/2017
api_name:
- FunctionLeave2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionLeave2
helpviewer_keywords:
- FunctionLeave2 function [.NET Framework profiling]
ms.assetid: 8cdac941-8b94-4497-b874-4e571785f3fe
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3d6486a90d952208af89428423867a3daa4e8618
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33453357"
---
# <a name="functionleave2-function"></a><span data-ttu-id="6d0cd-102">FunctionLeave2 (fonction)</span><span class="sxs-lookup"><span data-stu-id="6d0cd-102">FunctionLeave2 Function</span></span>
<span data-ttu-id="6d0cd-103">Notifie le profileur qu’une fonction doit retourner à l’appelant et fournit des informations sur la valeur de retour pile fonction et de frame.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-103">Notifies the profiler that a function is about to return to the caller and provides information about the stack frame and function return value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6d0cd-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d0cd-104">Syntax</span></span>  
  
```  
void __stdcall FunctionLeave2 (  
    [in]  FunctionID                        funcId,  
    [in]  UINT_PTR                          clientData,  
    [in]  COR_PRF_FRAME_INFO                func,  
    [in]  COR_PRF_FUNCTION_ARGUMENT_RANGE  *retvalRange  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6d0cd-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d0cd-105">Parameters</span></span>  
 `funcId`  
 <span data-ttu-id="6d0cd-106">[in] Identificateur de la fonction qui retourne.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-106">[in] The identifier of the function that is returning.</span></span>  
  
 `clientData`  
 <span data-ttu-id="6d0cd-107">[in] Identificateur de fonction remappé, avec le profileur spécifié précédemment via le [FunctionIDMapper](../../../../docs/framework/unmanaged-api/profiling/functionidmapper-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="6d0cd-107">[in] The remapped function identifier, which the profiler previously specified via the [FunctionIDMapper](../../../../docs/framework/unmanaged-api/profiling/functionidmapper-function.md) function.</span></span>  
  
 `func`  
 <span data-ttu-id="6d0cd-108">[in] A `COR_PRF_FRAME_INFO` valeur qui pointe vers des informations sur le frame de pile.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-108">[in] A `COR_PRF_FRAME_INFO` value that points to information about the stack frame.</span></span>  
  
 <span data-ttu-id="6d0cd-109">Le profileur doit le traiter en tant que handle opaque qui peut être passé au moteur d’exécution dans le [ICorProfilerInfo2::GetFunctionInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getfunctioninfo2-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="6d0cd-109">The profiler should treat this as an opaque handle that can be passed back to the execution engine in the [ICorProfilerInfo2::GetFunctionInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getfunctioninfo2-method.md) method.</span></span>  
  
 `retvalRange`  
 <span data-ttu-id="6d0cd-110">[in] Un pointeur vers un [COR_PRF_FUNCTION_ARGUMENT_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-function-argument-range-structure.md) structure qui spécifie l’emplacement de mémoire de valeur de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-110">[in] A pointer to a [COR_PRF_FUNCTION_ARGUMENT_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-function-argument-range-structure.md) structure that specifies the memory location of the function's return value.</span></span>  
  
 <span data-ttu-id="6d0cd-111">Pour accéder à la valeur de retour d’informations, le `COR_PRF_ENABLE_FUNCTION_RETVAL` indicateur doit être défini.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-111">In order to access return value information, the `COR_PRF_ENABLE_FUNCTION_RETVAL` flag must be set.</span></span> <span data-ttu-id="6d0cd-112">Le profileur peut utiliser le [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) pour définir les indicateurs d’événement.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-112">The profiler can use the [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) method to set the event flags.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6d0cd-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6d0cd-113">Remarks</span></span>  
 <span data-ttu-id="6d0cd-114">Les valeurs de la `func` et `retvalRange` paramètres ne sont pas valides après le `FunctionLeave2` fonction retourne, car les valeurs peuvent changer ou être détruites.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-114">The values of the `func` and `retvalRange` parameters are not valid after the `FunctionLeave2` function returns because the values may change or be destroyed.</span></span>  
  
 <span data-ttu-id="6d0cd-115">Le `FunctionLeave2` fonction est un rappel ; vous devez l’implémenter.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-115">The `FunctionLeave2` function is a callback; you must implement it.</span></span> <span data-ttu-id="6d0cd-116">L’implémentation doit utiliser le `__declspec`(`naked`) attribut de classe de stockage.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-116">The implementation must use the `__declspec`(`naked`) storage-class attribute.</span></span>  
  
 <span data-ttu-id="6d0cd-117">Le moteur d’exécution n’enregistre pas les registres avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-117">The execution engine does not save any registers before calling this function.</span></span>  
  
-   <span data-ttu-id="6d0cd-118">À l’entrée, vous devez enregistrer tous les registres que vous utilisez, y compris ceux de l’unité à virgule flottante (FPU).</span><span class="sxs-lookup"><span data-stu-id="6d0cd-118">On entry, you must save all registers that you use, including those in the floating-point unit (FPU).</span></span>  
  
-   <span data-ttu-id="6d0cd-119">À la sortie, vous devez restaurer la pile par extraire tous les paramètres qui ont été envoyées par son appelant.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-119">On exit, you must restore the stack by popping off all the parameters that were pushed by its caller.</span></span>  
  
 <span data-ttu-id="6d0cd-120">L’implémentation de `FunctionLeave2` ne doivent pas bloquer, car il sera retarder le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-120">The implementation of `FunctionLeave2` should not block because it will delay garbage collection.</span></span> <span data-ttu-id="6d0cd-121">L’implémentation ne doit pas tenter une opération garbage collection, car la pile est peut-être pas dans un état de nom convivial de la collection garbage.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-121">The implementation should not attempt a garbage collection because the stack may not be in a garbage collection-friendly state.</span></span> <span data-ttu-id="6d0cd-122">Si un garbage collection est tenté, le runtime bloque jusqu'à ce que `FunctionLeave2` retourne.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-122">If a garbage collection is attempted, the runtime will block until `FunctionLeave2` returns.</span></span>  
  
 <span data-ttu-id="6d0cd-123">En outre, le `FunctionLeave2` (fonction) ne doit pas appeler dans du code managé ou de quelque manière qu’une allocation de mémoire managée.</span><span class="sxs-lookup"><span data-stu-id="6d0cd-123">Also, the `FunctionLeave2` function must not call into managed code or in any way cause a managed memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6d0cd-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6d0cd-124">Requirements</span></span>  
 <span data-ttu-id="6d0cd-125">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6d0cd-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6d0cd-126">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="6d0cd-126">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="6d0cd-127">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6d0cd-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6d0cd-128">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6d0cd-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6d0cd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d0cd-129">See Also</span></span>  
 [<span data-ttu-id="6d0cd-130">FunctionEnter2, fonction</span><span class="sxs-lookup"><span data-stu-id="6d0cd-130">FunctionEnter2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md)  
 [<span data-ttu-id="6d0cd-131">FunctionTailcall2, fonction</span><span class="sxs-lookup"><span data-stu-id="6d0cd-131">FunctionTailcall2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md)  
 [<span data-ttu-id="6d0cd-132">SetEnterLeaveFunctionHooks2, méthode</span><span class="sxs-lookup"><span data-stu-id="6d0cd-132">SetEnterLeaveFunctionHooks2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md)  
 [<span data-ttu-id="6d0cd-133">Fonctions statiques globales de profilage</span><span class="sxs-lookup"><span data-stu-id="6d0cd-133">Profiling Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
