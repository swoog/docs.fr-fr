---
title: FunctionEnter3, fonction
ms.date: 03/30/2017
api_name:
- FunctionEnter3
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionEnter3
helpviewer_keywords:
- FunctionEnter3 function [.NET Framework profiling]
ms.assetid: ef782c53-dae7-4990-b4ad-fddb1e690d4e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a731df84af0991f80c560db417df0ffe053a5e2b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61598933"
---
# <a name="functionenter3-function"></a><span data-ttu-id="f2ecf-102">FunctionEnter3, fonction</span><span class="sxs-lookup"><span data-stu-id="f2ecf-102">FunctionEnter3 Function</span></span>
<span data-ttu-id="f2ecf-103">Notifie le profileur que le contrôle est passé à une fonction.</span><span class="sxs-lookup"><span data-stu-id="f2ecf-103">Notifies the profiler that control is being passed to a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2ecf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2ecf-104">Syntax</span></span>  
  
```  
void __stdcall FunctionEnter3(FunctionOrRemappedID functionOrRemappedID);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f2ecf-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2ecf-105">Parameters</span></span>  
 `functionOrRemappedID`  
 <span data-ttu-id="f2ecf-106">[in] L’identificateur de la fonction à laquelle le contrôle est passé.</span><span class="sxs-lookup"><span data-stu-id="f2ecf-106">[in] The identifier of the function to which control is passed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f2ecf-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f2ecf-107">Remarks</span></span>  
 <span data-ttu-id="f2ecf-108">Le `FunctionEnter3` fonction de rappel notifie le profileur que les fonctions sont appelées, mais sont l’inspection des arguments non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f2ecf-108">The `FunctionEnter3` callback function notifies the profiler as functions are being called, but does not support argument inspection.</span></span> <span data-ttu-id="f2ecf-109">Utilisez le [ICorProfilerInfo3::SetEnterLeaveFunctionHooks3, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3-method.md) pour enregistrer votre implémentation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f2ecf-109">Use the [ICorProfilerInfo3::SetEnterLeaveFunctionHooks3 method](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3-method.md) to register your implementation of this function.</span></span>  
  
 <span data-ttu-id="f2ecf-110">Le `FunctionEnter3` fonction est un rappel ; vous devez l’implémenter.</span><span class="sxs-lookup"><span data-stu-id="f2ecf-110">The `FunctionEnter3` function is a callback; you must implement it.</span></span> <span data-ttu-id="f2ecf-111">L’implémentation doit utiliser le `__declspec(naked)` attribut de classe de stockage.</span><span class="sxs-lookup"><span data-stu-id="f2ecf-111">The implementation must use the `__declspec(naked)` storage-class attribute.</span></span>  
  
 <span data-ttu-id="f2ecf-112">Le moteur d’exécution n’enregistre pas les registres avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f2ecf-112">The execution engine does not save any registers before calling this function.</span></span>  
  
- <span data-ttu-id="f2ecf-113">À l’entrée, vous devez enregistrer tous les registres que vous utilisez, y compris celles dans l’unité de virgule flottante (FPU).</span><span class="sxs-lookup"><span data-stu-id="f2ecf-113">On entry, you must save all registers that you use, including those in the floating-point unit (FPU).</span></span>  
  
- <span data-ttu-id="f2ecf-114">À la sortie, vous devez restaurer la pile en dépilant tous les paramètres qui ont été envoyés par son appelant.</span><span class="sxs-lookup"><span data-stu-id="f2ecf-114">On exit, you must restore the stack by popping off all the parameters that were pushed by its caller.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2ecf-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2ecf-115">Requirements</span></span>  
 <span data-ttu-id="f2ecf-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f2ecf-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2ecf-117">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="f2ecf-117">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="f2ecf-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f2ecf-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f2ecf-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f2ecf-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2ecf-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2ecf-120">See also</span></span>

- [<span data-ttu-id="f2ecf-121">FunctionLeave3</span><span class="sxs-lookup"><span data-stu-id="f2ecf-121">FunctionLeave3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md)
- [<span data-ttu-id="f2ecf-122">FunctionTailcall3</span><span class="sxs-lookup"><span data-stu-id="f2ecf-122">FunctionTailcall3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md)
- [<span data-ttu-id="f2ecf-123">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="f2ecf-123">FunctionEnter3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md)
- [<span data-ttu-id="f2ecf-124">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="f2ecf-124">FunctionLeave3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md)
- [<span data-ttu-id="f2ecf-125">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="f2ecf-125">FunctionTailcall3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md)
- [<span data-ttu-id="f2ecf-126">SetEnterLeaveFunctionHooks3</span><span class="sxs-lookup"><span data-stu-id="f2ecf-126">SetEnterLeaveFunctionHooks3</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3-method.md)
- [<span data-ttu-id="f2ecf-127">SetEnterLeaveFunctionHooks3WithInfo</span><span class="sxs-lookup"><span data-stu-id="f2ecf-127">SetEnterLeaveFunctionHooks3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3withinfo-method.md)
- [<span data-ttu-id="f2ecf-128">SetFunctionIDMapper</span><span class="sxs-lookup"><span data-stu-id="f2ecf-128">SetFunctionIDMapper</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setfunctionidmapper-method.md)
- [<span data-ttu-id="f2ecf-129">SetFunctionIDMapper2</span><span class="sxs-lookup"><span data-stu-id="f2ecf-129">SetFunctionIDMapper2</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setfunctionidmapper2-method.md)
- [<span data-ttu-id="f2ecf-130">Fonctions statiques globales de profilage</span><span class="sxs-lookup"><span data-stu-id="f2ecf-130">Profiling Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
