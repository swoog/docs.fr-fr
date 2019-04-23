---
title: FunctionIDMapper (fonction)
ms.date: 03/30/2017
api_name:
- FunctionIDMapper
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionIDMapper
helpviewer_keywords:
- FunctionIDMapper function [.NET Framework profiling]
ms.assetid: b8205b60-1893-4303-8cff-7ac5a00892aa
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2de19252b5c978fef38124636e4098ae5ece1b0c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59097936"
---
# <a name="functionidmapper-function"></a><span data-ttu-id="877ac-102">FunctionIDMapper (fonction)</span><span class="sxs-lookup"><span data-stu-id="877ac-102">FunctionIDMapper Function</span></span>
<span data-ttu-id="877ac-103">Notifie le profileur que l’identificateur donné d’une fonction peut être remappé vers un autre ID à utiliser dans le [FunctionEnter2](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md), [FunctionLeave2](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md), et [FunctionTailcall2](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md) rappels pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="877ac-103">Notifies the profiler that the given identifier of a function may be remapped to an alternative ID to be used in the [FunctionEnter2](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md), [FunctionLeave2](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md), and [FunctionTailcall2](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md) callbacks for that function.</span></span> <span data-ttu-id="877ac-104">`FunctionIDMapper` permet également au profileur d'indiquer s'il souhaite recevoir des rappels pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="877ac-104">`FunctionIDMapper` also enables the profiler to indicate whether it wants to receive callbacks for that function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="877ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="877ac-105">Syntax</span></span>  
  
```  
UINT_PTR __stdcall FunctionIDMapper (  
    [in]  FunctionID  funcId,   
    [out] BOOL       *pbHookFunction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="877ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="877ac-106">Parameters</span></span>  
 `funcId`  
 <span data-ttu-id="877ac-107">[in] Identificateur de fonction à remapper.</span><span class="sxs-lookup"><span data-stu-id="877ac-107">[in] The function identifier to be remapped.</span></span>  
  
 `pbHookFunction`  
 <span data-ttu-id="877ac-108">[out] Un pointeur vers une valeur qui affecte le profileur `true` s’il souhaite recevoir `FunctionEnter2`, `FunctionLeave2`, et `FunctionTailcall2` rappels ; sinon, il définit cette valeur à `false`.</span><span class="sxs-lookup"><span data-stu-id="877ac-108">[out] A pointer to a value that the profiler sets to `true` if it wants to receive `FunctionEnter2`, `FunctionLeave2`, and `FunctionTailcall2` callbacks; otherwise, it sets this value to `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="877ac-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="877ac-109">Return Value</span></span>  
 <span data-ttu-id="877ac-110">Le profileur retourne une valeur que le moteur d'exécution utilise comme autre identificateur de fonction.</span><span class="sxs-lookup"><span data-stu-id="877ac-110">The profiler returns a value that the execution engine uses as an alternative function identifier.</span></span> <span data-ttu-id="877ac-111">La valeur de retour ne peut pas être null, sauf si `false` est retourné dans `pbHookFunction`.</span><span class="sxs-lookup"><span data-stu-id="877ac-111">The return value cannot be null unless `false` is returned in `pbHookFunction`.</span></span> <span data-ttu-id="877ac-112">Sinon, une valeur de retour null génère des résultats imprévisibles, y compris éventuellement interrompre le processus.</span><span class="sxs-lookup"><span data-stu-id="877ac-112">Otherwise, a null return value will produce unpredictable results, including possibly halting the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="877ac-113">Notes</span><span class="sxs-lookup"><span data-stu-id="877ac-113">Remarks</span></span>  
 <span data-ttu-id="877ac-114">Le `FunctionIDMapper` fonction est un rappel.</span><span class="sxs-lookup"><span data-stu-id="877ac-114">The `FunctionIDMapper` function is a callback.</span></span> <span data-ttu-id="877ac-115">Il est implémenté par le profileur pour remapper un ID de fonction à tout autre identificateur qui est plus utile pour le profileur.</span><span class="sxs-lookup"><span data-stu-id="877ac-115">It is implemented by the profiler to remap a function ID to some other identifier that is more useful for the profiler.</span></span> <span data-ttu-id="877ac-116">Le `FunctionIDMapper` retourne l’autre ID à utiliser pour toute fonction donnée.</span><span class="sxs-lookup"><span data-stu-id="877ac-116">The `FunctionIDMapper` returns the alternate ID to be used for any given function.</span></span> <span data-ttu-id="877ac-117">Le moteur d’exécution répond ensuite à la demande du profileur en passant cet ID secondaire, en plus de l’ID de fonction classique, au profileur dans le `clientData` paramètre de la `FunctionEnter2`, `FunctionLeave2`, et `FunctionTailcall2` hooks, pour identifier la fonction pour laquelle le hook est appelé.</span><span class="sxs-lookup"><span data-stu-id="877ac-117">The execution engine then honors the profiler's request by passing this alternate ID, in addition to the traditional function ID, back to the profiler in the `clientData` parameter of the `FunctionEnter2`, `FunctionLeave2`, and `FunctionTailcall2` hooks, to identify the function for which the hook is being called.</span></span>  
  
 <span data-ttu-id="877ac-118">Vous pouvez utiliser la [ICorProfilerInfo::SetFunctionIDMapper](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setfunctionidmapper-method.md) méthode pour spécifier l’implémentation de la `FunctionIDMapper` (fonction).</span><span class="sxs-lookup"><span data-stu-id="877ac-118">You can use the [ICorProfilerInfo::SetFunctionIDMapper](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setfunctionidmapper-method.md) method to specify the implementation of the `FunctionIDMapper` function.</span></span> <span data-ttu-id="877ac-119">Vous pouvez appeler la `ICorProfilerInfo::SetFunctionIDMapper` méthode qu’une seule fois et nous vous recommandons d’effectuer dans le [ICorProfilerCallback::Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="877ac-119">You can call the `ICorProfilerInfo::SetFunctionIDMapper` method only once, and we recommend that you do so in the [ICorProfilerCallback::Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md) callback.</span></span>  
  
 <span data-ttu-id="877ac-120">Par défaut, il est supposé qu’un profileur que qui définit l’indicateur COR_PRF_MONITOR_ENTERLEAVE à l’aide de [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md), et qui définit des raccordements via [ICorProfilerInfo::SetEnterLeaveFunctionHooks](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setenterleavefunctionhooks-method.md) ou [ICorProfilerInfo2::SetEnterLeaveFunctionHooks2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md), doivent recevoir la `FunctionEnter2`, `FunctionLeave2`, et `FunctionTailcall2` pour chaque fonction.</span><span class="sxs-lookup"><span data-stu-id="877ac-120">By default, it is assumed that a profiler that sets the COR_PRF_MONITOR_ENTERLEAVE flag by using [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md), and which sets hooks via [ICorProfilerInfo::SetEnterLeaveFunctionHooks](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setenterleavefunctionhooks-method.md) or [ICorProfilerInfo2::SetEnterLeaveFunctionHooks2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md), should receive the `FunctionEnter2`, `FunctionLeave2`, and `FunctionTailcall2` callbacks for every function.</span></span> <span data-ttu-id="877ac-121">Toutefois, les profileurs peuvent implémenter `FunctionIDMapper` pour éviter de manière sélective recevoir ces rappels pour certaines fonctions en définissant `pbHookFunction` à `false`.</span><span class="sxs-lookup"><span data-stu-id="877ac-121">However, profilers may implement `FunctionIDMapper` to selectively avoid receiving these callbacks for certain functions by setting `pbHookFunction` to `false`.</span></span>  
  
 <span data-ttu-id="877ac-122">Les profileurs doivent être à tolérance de panne de cas où plusieurs threads d’une application profilée appellent simultanément la même méthode/fonction.</span><span class="sxs-lookup"><span data-stu-id="877ac-122">Profilers should be tolerant of cases where multiple threads of a profiled application are calling the same method/function simultaneously.</span></span> <span data-ttu-id="877ac-123">Dans ce cas, le profileur peut recevoir plusieurs `FunctionIDMapper` rappels pour le même `FunctionID`.</span><span class="sxs-lookup"><span data-stu-id="877ac-123">In such cases, the profiler may receive multiple `FunctionIDMapper` callbacks for the same `FunctionID`.</span></span> <span data-ttu-id="877ac-124">Le profileur doit être certain de retourner les mêmes valeurs de ce rappel lorsqu’elle est appelée plusieurs fois avec le même `FunctionID`.</span><span class="sxs-lookup"><span data-stu-id="877ac-124">The profiler should be certain to return the same values from this callback when it is called multiple times with the same `FunctionID`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="877ac-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="877ac-125">Requirements</span></span>  
 <span data-ttu-id="877ac-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="877ac-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="877ac-127">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="877ac-127">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="877ac-128">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="877ac-128">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="877ac-129">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="877ac-129">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="877ac-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="877ac-130">See also</span></span>

- [<span data-ttu-id="877ac-131">SetFunctionIDMapper, méthode</span><span class="sxs-lookup"><span data-stu-id="877ac-131">SetFunctionIDMapper Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setfunctionidmapper-method.md)
- [<span data-ttu-id="877ac-132">FunctionIDMapper2, fonction</span><span class="sxs-lookup"><span data-stu-id="877ac-132">FunctionIDMapper2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionidmapper2-function.md)
- [<span data-ttu-id="877ac-133">FunctionEnter2, fonction</span><span class="sxs-lookup"><span data-stu-id="877ac-133">FunctionEnter2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md)
- [<span data-ttu-id="877ac-134">FunctionLeave2, fonction</span><span class="sxs-lookup"><span data-stu-id="877ac-134">FunctionLeave2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md)
- [<span data-ttu-id="877ac-135">FunctionTailcall2, fonction</span><span class="sxs-lookup"><span data-stu-id="877ac-135">FunctionTailcall2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md)
- [<span data-ttu-id="877ac-136">Fonctions statiques globales de profilage</span><span class="sxs-lookup"><span data-stu-id="877ac-136">Profiling Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
