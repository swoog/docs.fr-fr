---
title: FunctionLeave3, fonction
ms.date: 03/30/2017
api_name:
- FunctionLeave3
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionLeave3
helpviewer_keywords:
- FunctionLeave3 function [.NET Framework profiling]
ms.assetid: 5d798088-7992-48a0-ae55-d2a7ee31913f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9dce2f961a01b70c0cba50894d670a586a40b605
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64586828"
---
# <a name="functionleave3-function"></a><span data-ttu-id="784ab-102">FunctionLeave3, fonction</span><span class="sxs-lookup"><span data-stu-id="784ab-102">FunctionLeave3 Function</span></span>
<span data-ttu-id="784ab-103">Notifie le profileur que le contrôle a été renvoyé à partir d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="784ab-103">Notifies the profiler that control is being returned from a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="784ab-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="784ab-104">Syntax</span></span>  
  
```  
void __stdcall FunctionLeave3(FunctionOrRemappedID functionOrRemappedID);  
```  
  
## <a name="parameters"></a><span data-ttu-id="784ab-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="784ab-105">Parameters</span></span>  
 `functionOrRemappedID`  
 <span data-ttu-id="784ab-106">[in] L’identificateur de la fonction à partir de laquelle le contrôle est retourné.</span><span class="sxs-lookup"><span data-stu-id="784ab-106">[in] The identifier of the function from which control is returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="784ab-107">Notes</span><span class="sxs-lookup"><span data-stu-id="784ab-107">Remarks</span></span>  
 <span data-ttu-id="784ab-108">Le `FunctionLeave3` fonction de rappel notifie le profileur que les fonctions sont appelées, mais ne prend pas en charge l’inspection de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="784ab-108">The `FunctionLeave3` callback function notifies the profiler as functions are being called, but does not support return value inspection.</span></span> <span data-ttu-id="784ab-109">Utilisez le [ICorProfilerInfo3::SetEnterLeaveFunctionHooks3, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3-method.md) pour enregistrer votre implémentation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="784ab-109">Use the [ICorProfilerInfo3::SetEnterLeaveFunctionHooks3 method](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3-method.md) to register your implementation of this function.</span></span>  
  
 <span data-ttu-id="784ab-110">Le `FunctionLeave3` fonction est un rappel ; vous devez l’implémenter.</span><span class="sxs-lookup"><span data-stu-id="784ab-110">The `FunctionLeave3` function is a callback; you must implement it.</span></span> <span data-ttu-id="784ab-111">L’implémentation doit utiliser le `__declspec(naked)` attribut de classe de stockage.</span><span class="sxs-lookup"><span data-stu-id="784ab-111">The implementation must use the `__declspec(naked)` storage-class attribute.</span></span>  
  
 <span data-ttu-id="784ab-112">Le moteur d’exécution n’enregistre pas les registres avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="784ab-112">The execution engine does not save any registers before calling this function.</span></span>  
  
- <span data-ttu-id="784ab-113">À l’entrée, vous devez enregistrer tous les registres que vous utilisez, y compris celles dans l’unité de virgule flottante (FPU).</span><span class="sxs-lookup"><span data-stu-id="784ab-113">On entry, you must save all registers that you use, including those in the floating-point unit (FPU).</span></span>  
  
- <span data-ttu-id="784ab-114">À la sortie, vous devez restaurer la pile en dépilant tous les paramètres qui ont été envoyés par son appelant.</span><span class="sxs-lookup"><span data-stu-id="784ab-114">On exit, you must restore the stack by popping off all the parameters that were pushed by its caller.</span></span>  
  
 <span data-ttu-id="784ab-115">L’implémentation de `FunctionLeave3` ne doivent pas bloquer, car il sera retarder le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="784ab-115">The implementation of `FunctionLeave3` should not block, because it will delay garbage collection.</span></span> <span data-ttu-id="784ab-116">L’implémentation ne doit pas tenter un garbage collection, car la pile est peut-être pas dans un état de la collection convivial garbage.</span><span class="sxs-lookup"><span data-stu-id="784ab-116">The implementation should not attempt a garbage collection, because the stack may not be in a garbage collection-friendly state.</span></span> <span data-ttu-id="784ab-117">Si un garbage collection est tenté, le runtime bloque jusqu'à ce que `FunctionLeave3` retourne.</span><span class="sxs-lookup"><span data-stu-id="784ab-117">If a garbage collection is attempted, the runtime will block until `FunctionLeave3` returns.</span></span>  
  
 <span data-ttu-id="784ab-118">Le `FunctionLeave3` (fonction) ne doit pas appeler dans du code managé ou provoquer une allocation de mémoire managée en aucune façon.</span><span class="sxs-lookup"><span data-stu-id="784ab-118">The `FunctionLeave3` function must not call into managed code or cause a managed memory allocation in any way.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="784ab-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="784ab-119">Requirements</span></span>  
 <span data-ttu-id="784ab-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="784ab-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="784ab-121">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="784ab-121">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="784ab-122">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="784ab-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="784ab-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="784ab-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="784ab-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="784ab-124">See also</span></span>

- [<span data-ttu-id="784ab-125">FunctionEnter3</span><span class="sxs-lookup"><span data-stu-id="784ab-125">FunctionEnter3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md)
- [<span data-ttu-id="784ab-126">FunctionTailcall3</span><span class="sxs-lookup"><span data-stu-id="784ab-126">FunctionTailcall3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md)
- [<span data-ttu-id="784ab-127">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="784ab-127">FunctionEnter3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md)
- [<span data-ttu-id="784ab-128">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="784ab-128">FunctionLeave3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md)
- [<span data-ttu-id="784ab-129">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="784ab-129">FunctionTailcall3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md)
- [<span data-ttu-id="784ab-130">SetEnterLeaveFunctionHooks3</span><span class="sxs-lookup"><span data-stu-id="784ab-130">SetEnterLeaveFunctionHooks3</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3-method.md)
- [<span data-ttu-id="784ab-131">SetEnterLeaveFunctionHooks3WithInfo</span><span class="sxs-lookup"><span data-stu-id="784ab-131">SetEnterLeaveFunctionHooks3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3withinfo-method.md)
- [<span data-ttu-id="784ab-132">SetFunctionIDMapper</span><span class="sxs-lookup"><span data-stu-id="784ab-132">SetFunctionIDMapper</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setfunctionidmapper-method.md)
- [<span data-ttu-id="784ab-133">SetFunctionIDMapper2</span><span class="sxs-lookup"><span data-stu-id="784ab-133">SetFunctionIDMapper2</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setfunctionidmapper2-method.md)
- [<span data-ttu-id="784ab-134">Fonctions statiques globales de profilage</span><span class="sxs-lookup"><span data-stu-id="784ab-134">Profiling Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
